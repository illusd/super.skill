# Animation Libraries Reference (Top 30 Core)

Curated from the most popular and battle-tested GitHub libraries. Always prefer the cheapest tool that satisfies the purpose (see Build Mode sequence). Use a library only when CSS / WAAPI / Motion is insufficient.

## 1. Universal / Native JavaScript Core

| Library | Stars-level | Best for | When to choose | Notes |
| --- | --- | --- | --- | --- |
| **GSAP** (GreenSock) | Industry standard | Complex timelines, sequences, ScrollTrigger, performance-critical | Multi-step orchestrated motion, SVG, canvas, cross-framework | Most powerful; paid plugins for advanced features. Pair with Lenis. |
| **Anime.js** | Lightweight | Simple declarative animations, staggered sequences | Quick one-off effects without heavy deps | Extremely intuitive API. |
| **Popmotion** | Functional | Low-level, pure functions; base of older Framer Motion | Custom physics or when you need maximum control | More low-level than modern Motion. |
| **Velocity.js** | High perf | jQuery-like API with better performance | Legacy codebases still using jQuery-style animate | Declining relevance for new projects. |
| **Mo.js** | Motion graphics | Explosions, particles, geometric shapes, burst effects | Decorative motion-graphics / delight moments | Specialized, not for everyday UI. |
| **Tween.js** | Tweening | 3D / Canvas / WebGL value interpolation | Pair with Three.js or custom render loops | Pure math tween engine. |

## 2. Pure CSS & Lightweight Preset Libraries

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **Animate.css** | Ready-made class-based effects | Rapid prototyping, marketing pages | Just add class. Prefer custom CSS for production UI. |
| **Magic CSS** | Special visual effects | One-off wow moments | Use sparingly. |
| **Hover.css** | Hover interactions | Buttons, cards, links | Good starting point; refine durations & easings. |
| **SpinKit** | Loading spinners | Pure CSS loaders | Excellent, zero JS. |

## 3. React / Frontend Ecosystem

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **Framer Motion** (now Motion) | Gestures, layout animations, springs, exit animations | Almost any React UI motion | Preferred React solution. Use full `transform` strings under load. |
| **React Spring** | Physics-based springs | Highly natural, interruptible motion | Alternative to Motion for pure spring feel. |
| **Remotion** | Programmatic video | Generate MP4 from React components | Not for runtime UI; for video production. |
| **AutoAnimate** | Zero-config list/DOM transitions | Quick add/remove/reorder animations | Amazing for lists; still respect frequency rules. |
| **React Flip Toolkit** | FLIP technique | Complex layout transitions | Specialized FLIP helper. |

## 4. 3D / WebGL / Rendering Engines

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **Three.js** | Full 3D scenes | Any serious WebGL work | The standard. |
| **React Three Fiber (R3F)** | Declarative 3D in React | React + Three.js projects | Pairs with @react-three/drei. |
| **Theatre.js** | Visual timeline for 3D/WebGL | Designers + engineers collaborating on complex sequences | Has visual editor. |
| **PixiJS** | High-performance 2D | Games, particle-heavy 2D, high FPS | WebGL 2D specialist. |
| **Babylon.js** | Full game engine | Games, advanced 3D with physics | Microsoft, WebGPU ready. |

## 5. SVG / Vector / After Effects

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **Lottie-Web** | After Effects exports | Complex illustrated animations from designers | JSON from Bodymovin. Keep file size in check. |
| **Vivus.js** | SVG stroke drawing | Line-drawing / signature effects | Perfect for path reveal. |
| **SVG.js** | SVG manipulation + animation | Lightweight SVG control | Clean API. |
| **Snap.svg** | Modern SVG | Vector graphics animation | Adobe open-source. |

## 6. Scroll-driven & Text Effects

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **Lenis** | Smooth scroll | Modern smooth-scrolling sites | Current favorite; pairs perfectly with GSAP ScrollTrigger. |
| **ScrollReveal** | Scroll-triggered reveals | Elements entering viewport | Simple and effective. |
| **AOS** (Animate On Scroll) | CSS-based scroll animations | Quick scroll effects | Lightweight. |
| **Rellax.js** | Parallax | Lightweight parallax layers | Pure JS, no deps. |
| **Typed.js** | Typewriter effect | Text typing animations | Classic. |
| **tsParticles** | Particle systems | Background particles, stars, confetti | Modular and powerful. |

## Decision Heuristics (aligned with Super skill)

1. **Can CSS / `@starting-style` / WAAPI do it?** → Do not reach for a library.
2. **React UI with gestures / layout / springs?** → Motion (Framer Motion) or React Spring.
3. **Complex timeline / ScrollTrigger / multi-element orchestration?** → GSAP.
4. **Designer-provided AE animation?** → Lottie.
5. **3D scene?** → Three.js (+ R3F if React).
6. **Smooth scroll page?** → Lenis + GSAP ScrollTrigger.
7. **List add/remove?** → AutoAnimate (then refine).
8. **Decorative particles / bursts?** → tsParticles or Mo.js.
9. **Stroke drawing?** → Vivus or pure CSS/SVG.

Always apply the frequency gate, purpose test, and Never Ship rules even when using a library. Libraries make bad motion easier to ship — the craft bar remains the same.

## 7. Advanced Scroll & Parallax

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **Locomotive Scroll** | High-end smooth scroll + parallax | Premium marketing sites, WebGL combinations | Very smooth inertia; heavier than Lenis |
| **Lax.js** | Lightweight scroll-bound transforms | Bind scale/rotate/translate to scroll progress with zero deps | Excellent for simple scroll-driven effects |
| **Parallax.js** | Device orientation + mouse parallax | Gyro on mobile + mouse depth on desktop | Depth layers react to device/mouse |
| **Sal.js** | High-performance scroll reveals | Intersection Observer based, no jank | Lightweight alternative to AOS/ScrollReveal |

## 8. Creative Coding, Canvas & Pseudo-3D

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **p5.js** | Generative art, creative coding | Complex canvas drawings, interactive generative animation | Artist/designer favorite |
| **Zdog** | Pseudo-3D (flat 3D look) | Canvas/SVG with charming retro 3D geometry | Actually 2D math with 3D appearance |
| **Paper.js** | Vector scripting on Canvas | Bezier curves, path animation, complex vector work | Strong path tools |
| **Fabric.js** | Interactive canvas objects | Drag, transform, animate objects on canvas | Object model on top of canvas |

## 9. Physics & Data-Driven

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **Matter.js** | 2D rigid-body physics | Collisions, gravity, bounce, real physics simulation | Best pure 2D physics for the web |
| **Cannon-es** | 3D physics | Pair with Three.js for real 3D collisions | Modern fork of Cannon.js |
| **KUTE.js** | High-perf tweening + SVG morph | Extreme performance tweens, powerful SVG morphing | Specialized morph engine |
| **D3.js** | Data-driven transitions | Complex data viz animations, geometric transitions | Industry standard for data animation |

## 10. Text, Micro-interactions & Special UI

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **Hamburgers** | Hamburger menu animations | Multiple CSS hamburger icon styles | Pure CSS collection |
| **CSShake** | Shake / vibrate effects | Error states, attention, warning feedback | CSS-only shake |
| **Baffle.js** | Text scramble / decode | Cyberpunk / hacker-style title reveals | Character scramble effect |
| **Micron.js** | Micro-interactions via data attributes | Quick bounce, jelly, flash feedback on elements | Attribute-driven micro interactions |

## 11. Framework-Specific & Complex Components

| Library | Best for | When to choose | Notes |
| --- | --- | --- | --- |
| **@vueuse/motion** | Vue declarative motion | Vue projects needing Framer-Motion-like API | VueUse ecosystem |
| **React Move** | Data-driven React transitions | Complex array enter/exit with D3-inspired model | Good for data-heavy lists |
| **Swiper** | Modern carousels / sliders | 3D Coverflow, Cards, Cube transitions | Most capable slider library |
| **Rough.js** | Hand-drawn / sketchy style | Rough, organic, hand-drawn animation look | Continuous redraw for life-like jitter |

## Updated Decision Heuristics

- Smooth scroll → **Lenis** (preferred) or Locomotive Scroll (heavier premium)
- Simple scroll-bound transform → **Lax.js** or pure CSS scroll-driven animations
- 2D physics → **Matter.js**
- 3D physics + Three.js → **Cannon-es**
- Generative / creative canvas → **p5.js**
- Pseudo-3D charm → **Zdog**
- SVG morph → **KUTE.js** or GSAP MorphSVG
- Data viz transitions → **D3.js**
- Vue motion → **@vueuse/motion**
- Carousel / 3D slider → **Swiper**
- Hand-drawn feel → **Rough.js**
- Micro feedback → prefer pure CSS or Micron.js only for quick prototypes
