# Animation Vocabulary (curated)

Use these exact terms. Prefer the closest authentic match over inventing new ones.

## Entrances & Exits
- **Fade in / Fade out** — Opacity change only
- **Slide in** — Enters from off-screen
- **Scale in** — Grows from smaller size (usually + fade)
- **Pop in** — Appears with slight overshoot / bounce
- **Reveal** — Uncovered by clip-path or mask
- **Origin-aware animation** — Scales/grows from its trigger, not center

## Sequencing
- **Stagger** — Cascade with small delay (30–80 ms) between items
- **Orchestration** — Deliberate timing of multiple motions into one whole
- **Delay / Duration / Fill mode**

## Movement
- **Translate / Scale / Rotate / Skew**
- **3D tilt / Flip / Perspective**
- **Transform origin**

## State Transitions
- **Crossfade** — Simultaneous fade out + fade in in same place
- **Morph** — One shape becomes another (Dynamic Island style)
- **Shared element transition** — Element travels and transforms between states
- **Layout animation** — Size/position change animates instead of snapping
- **Accordion / Collapse**
- **Direction-aware transition** — Forward vs back have opposite directions

## Scroll
- **Scroll reveal** — Enters as it enters viewport
- **Scroll-driven animation** — Progress tied to scroll position
- **Parallax**
- **View transition / Page transition**

## Feedback & Interaction
- **Press / Tap feedback** — Subtle scale-down on press
- **Hold to confirm** — Progress fill while held
- **Drag / Drag to reorder / Swipe to dismiss**
- **Rubber-banding** — Resistance + snap-back past boundary (iOS overscroll)
- **Shake / Wiggle** — Error signal
- **Ripple**

## Easing
- **Ease-out** — Fast start, slow end (default for UI response)
- **Ease-in** — Slow start (usually avoid on UI)
- **Ease-in-out** — For on-screen movement
- **Linear** — Constant (marquees, progress)
- **Cubic-bezier / Asymmetric easing**

## Springs
- **Spring** — Physics-driven (no fixed duration)
- **Stiffness / Damping / Mass / Bounce**
- **Momentum / Velocity**
- **Interruptible animation** — Can be redirected mid-flight while carrying velocity
- **Perceptual duration**

## Looping & Ambient
- **Marquee / Loop / Alternate (yoyo)**
- **Pulse / Float / Idle animation / Orbit**

## Polish
- **Blur** (soft mask for imperfect crossfades)
- **Clip-path / Mask**
- **Skeleton / Shimmer**
- **Number ticker / Tabular numbers / Typewriter / Text morph / Line drawing**

## Performance concepts
- **Jank / Dropped frame / Compositing / will-change / Layout thrashing**
- **Hardware acceleration** (transform + opacity)

## Principles
- **Purposeful animation** · **Frequency of use** · **Spatial consistency**
- **Anticipation / Follow-through / Squash & stretch**
- **Perceived performance** · **Reduced motion**
