# Emotion Field Visualisation
## Technical Specification for a Three.js Particle System
### Mapping the (F, N, D, P) Tuple Schema onto a Dynamic Representation Space

**For:** Developer building the visualisation
**Context:** Companion to *Ideasthesia as Geometry* (S.B. & Claude, April 2026)
**Colour theme:** Teal `#0891B2` (primary) · Orange `#F97316` (accent)

---

## What This Is

A 3D particle-field visualisation encoding Anthropic's 171-emotion activation vectors as particles in a space where:

- **Position** encodes the affective circumplex (Anthropic's PC1/PC2 axes)
- **Particle physics** encodes the tuple schema (Form, Neighbourhood, Dynamics, Packing-Dim)
- **Field behaviour** encodes precision-weighting (the formal model's C_t = λ_t · γ_t)

The goal is not decoration. The visualisation makes a testable structural claim: emotions that cluster in 2D (same valence, same arousal) should visually separate in 3D and behave differently under field perturbation.

---

## Axes

| Axis | Encodes | Source |
|---|---|---|
| X | PC1 (valence: positive → negative) | Anthropic 171-vector PCA |
| Y | PC2 (arousal: high → low) | Anthropic 171-vector PCA |
| Z | Packing-Dim (P axis: sp0D → den3D) | Tuple coding |
| Particle mass | Semantic precision λ (certainty of concept) | Formal model |

The X/Y plane reproduces the affective circumplex. Z lifts the plane into a field with depth. Mass determines how particles resist perturbation.

---

## Tuple → Particle Property Mapping

### Form (F) → Trail Shape

The trail is the history of the particle's trajectory over the last N frames. Shape is determined by the velocity field assigned to each Form class.

| F value | Trail behaviour | Implementation note |
|---|---|---|
| `point` | Near-stationary. Tight circular micro-oscillation. Very short trail. | Low velocity magnitude, high damping. |
| `vector` | Directed, asymptotic. Trail is a clean arc in one direction. | Constant velocity component in assigned direction, moderate damping. |
| `loop` | Closes on itself. Trail forms a visible orbit or spiral return. | Rotational velocity component; trail persists long enough to show the loop. |
| `convergence` | Multiple incoming arcs meeting at a point. If rendering a cluster, particles curve toward each other. | Attractive force toward cluster centroid; trails show the inward curves. |
| `collapse` | Trail contracts and thins. Final point is a terminus. Particle dies at end of life. | Velocity decays to zero; particle fades and respawns at a new position after terminal state. |

### Neighbourhood (N) → Inter-particle Forces

| N value | Force behaviour |
|---|---|
| `clustered` | Mild positive attraction to nearby same-quadrant particles. Flocking-like cohesion. |
| `isolated` | Repulsion or indifference to neighbours. Particle moves without influence. |
| `contrastive` | Active repulsion from adjacent particles. Boundary maintained. |
| `gradient` | No clear boundary force. Particle diffuses into adjacent regions. Low directional bias. |

**Boundary modifier → visual boundary:**
- `b∅` — no border rendering
- `b~` — soft glow/halo at particle edge
- `b#` — sharp bright ring; particle clearly defined against neighbours

### Dynamics (D) → Velocity Behaviour and Lifetime

| D value | Velocity behaviour | Lifetime |
|---|---|---|
| `stable` | Velocity holds under field perturbation. Resistant to noise. | Long; continuous. |
| `recursive` | Velocity field loops: particle returns to prior position after displacement. | Long; continuous. |
| `drifting` | Velocity shifts systematically with neighbour field. Coherent drift in semantic direction. | Medium; gradual fade. |
| `terminal` | Velocity decays to zero. Particle dims and disappears. Respawns elsewhere after pause. | Short; definite end. |

### Packing-Dim (P) → Particle Density and Size Cluster

| P value | Visual encoding |
|---|---|
| `sp0D` | Single, small particle. Isolated dot. No cluster. |
| `sp1D` | Small particle with faint directional trail. |
| `med1D` | Medium particle; trail shows directionality. |
| `med2D` | Medium particle cluster (3–5 particles) moving coherently. |
| `den2D` | Dense cluster (8–12 particles). Clear swarm behaviour. |
| `den3D` | Dense 3D swarm with Z-spread. Full volume occupation. |

---

## Precision Weighting → Particle Mass

The formal model's coupling strength is C_t = λ_t · γ_t.

**Mass implementation:**
- High precision (semantically certain, high-frequency concept) → **heavy particle** → resists field perturbation, holds trajectory
- Low precision (ambiguous, rare concept) → **light particle** → deflected easily by neighbouring field, shows K_S mechanism in action

Map mass to a logarithmic scale from corpus frequency or semantic certainty estimate. If Anthropic's 171-vector data includes confidence scores, use those directly.

---

## Field Architecture

### Base Field

Use 3D Simplex noise (as in the reference CodePen: [https://codepen.io/ImagineProgramming/pen/LpOJzM](https://codepen.io/ImagineProgramming/pen/LpOJzM)) as the underlying flow field:

```javascript
// Simplex noise field — gives coherent directional flow
const fieldVector = (x, y, z, t) => {
  const nx = simplex.noise4D(x * scale, y * scale, z * scale, t * timeScale);
  const ny = simplex.noise4D(x * scale + 100, y * scale, z * scale, t * timeScale);
  const nz = simplex.noise4D(x * scale, y * scale + 100, z * scale, t * timeScale);
  return new THREE.Vector3(nx, ny, nz).multiplyScalar(fieldStrength);
};
```

Field strength is modulated by mass: `acceleration = fieldVector / particle.mass`.

### Particle Velocity Integration

```javascript
// Per-frame update
particle.velocity.add(fieldVector(particle.position, time).divideScalar(particle.mass));
particle.velocity.multiplyScalar(dampingFactor); // 0.92–0.96 depending on D value
particle.position.add(particle.velocity);

// Store trail
particle.trail.push(particle.position.clone());
if (particle.trail.length > trailLength) particle.trail.shift();
```

Damping factor by D class:
- `stable`: 0.97 (very little decay)
- `recursive`: 0.94 + return force toward origin
- `drifting`: 0.92 + coherent drift bias
- `terminal`: 0.85 (rapid decay; triggers death when speed < threshold)

---

## Data Format

Each emotion is a JSON object:

```json
{
  "label": "desperation",
  "pc1_valence": -0.82,
  "pc2_arousal": 0.71,
  "tuple": {
    "F": "collapse",
    "N": "contrastive",
    "N_boundary": "sharp",
    "D": "terminal",
    "P": "den2D"
  },
  "mass": 0.4,
  "colour": "#0891B2"
}
```

Position initialised at `(pc1_valence * scaleX, pc2_arousal * scaleY, packingDimToZ(P))`.

Suggested Z mapping:
```javascript
const packingZ = { sp0D: -2, sp1D: -1, med1D: 0, med2D: 0.5, den2D: 1.5, den3D: 2.5 };
```

---

## Colour Scheme

- **Primary particle colour:** Teal `#0891B2` — default for all particles
- **High-arousal positive quadrant:** Teal brightened toward white
- **High-arousal negative quadrant:** Orange `#F97316` — fear, desperation, panic cluster
- **Low-arousal negative quadrant:** Teal darkened (grief, sadness, despair)
- **Low-arousal positive quadrant:** Teal + orange mix (content, peaceful, serene)
- **Trail:** Particle colour at 30–60% opacity, fading with age
- **Terminal particles:** Dim to near-black before respawn
- **Background:** Near-black (`#0a0a0a`) — the field needs depth

---

## Interactions

| Interaction | Behaviour |
|---|---|
| Hover particle | Show label + tuple code. Pause particle motion. |
| Click particle | Isolate particle cluster; dim all others to 10% opacity. Show full tuple breakdown in sidebar. |
| Drag field | Rotate 3D view. |
| Scroll | Zoom. |
| Space bar | Freeze/unfreeze field (let user study static geometry). |
| `P` key | Toggle Packing-Dim Z-axis spread (collapse to 2D / expand to 3D). Lets user see the circumplex vs the full geometry. |
| `V` key | Toggle valence/arousal labels on axes. |
| Slider: field strength | Modulate simplex noise amplitude. Shows how light vs heavy particles respond differently (precision-weighting in action). |

---

## The Key Visual Test

The central claim is: emotions that cluster in 2D (same X/Y position in the circumplex) should **visually separate** in this space — either by Z position, by trail shape, or by divergent behaviour under field perturbation.

Build one test scene first with just six pairs:

| Pair | Expected separation |
|---|---|
| fear vs anxiety | Trail: arc vs orbit. Dynamics: drifts vs returns. |
| terrified vs panicked | Trail: narrowing vs fragmenting. Motion: frozen vs chaotic. |
| joy vs excitement | Trail: orbit vs forward arc. |
| content vs peaceful | Trail: near-still vs diffusing. Z: similar but N separates. |
| desperation vs fear | Trail: collapsing vs directed. Motion: decelerates to zero vs moves. |
| grief vs sadness | Trail: loop vs settling point. |

If the particle behaviours predicted by the tuple codings are visible in the render, and if they match Anthropic's causal steering profiles for these pairs, the notation adds real explanatory power.

---

## Three.js Library Suggestions

```html
<!-- Core -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<!-- Orbit controls -->
<script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/controls/OrbitControls.js"></script>
<!-- Simplex noise -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/simplex-noise/2.4.0/simplex-noise.min.js"></script>
<!-- Post-processing (optional: bloom for trails) -->
<script src="https://cdn.jsdelivr.net/npm/three@0.128.0/examples/js/postprocessing/EffectComposer.js"></script>
```

For trail rendering, use `THREE.BufferGeometry` with `LineSegments` and update vertex positions each frame. Bloom post-processing (`UnrealBloomPass`) gives trails a natural glow without performance cost.

---

## What This Is Not

This visualisation does not claim the particle behaviour *is* what happens in representational space. It is an instrument for testing whether the tuple schema predicts measurable separation in Anthropic's activation geometry. If the pairs that the notation codes as Form-different show greater cosine distance in the 171-vector space than Form-same pairs (controlling for valence/arousal), and if that separation is visible in the visualisation, then the notation adds explanatory power. If it is not, the notation is elegant but empty. The visualisation makes the prediction visible. The data decides.
