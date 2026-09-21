# Animation Recipes (Production-ready)

Start from the recipe, then adapt. Curves use the tokens:
--ease-out: cubic-bezier(0.23, 1, 0.32, 1);
--ease-in-out: cubic-bezier(0.77, 0, 0.175, 1);
--ease-drawer: cubic-bezier(0.32, 0.72, 0, 1);

## Button press
```css
.button {
  transition: transform 160ms var(--ease-out);
}
.button:active {
  transform: scale(0.97);
}
```
Scale children too. Gate :hover separately.

## Dropdown / Popover / Menu / Select
```css
.popover {
  transform-origin: var(--transform-origin);
  transition: opacity 200ms var(--ease-out), transform 200ms var(--ease-out);
}
.popover[data-starting-style],
.popover[data-ending-style] {
  opacity: 0;
  transform: scale(0.95);
}
```

## Tooltip
```css
.tooltip {
  transform-origin: var(--transform-origin);
  transition: transform 125ms var(--ease-out), opacity 125ms var(--ease-out);
}
.tooltip[data-starting-style],
.tooltip[data-ending-style] {
  opacity: 0;
  transform: scale(0.97);
}
.tooltip[data-instant] {
  transition-duration: 0ms;
}
```
First tooltip has delay; subsequent ones are instant.

## Modal
```css
.modal {
  transform-origin: center;
  transition: opacity 250ms var(--ease-out), transform 250ms var(--ease-out);
}
.modal[data-starting-style],
.modal[data-ending-style] {
  opacity: 0;
  transform: scale(0.96);
}
.backdrop {
  transition: opacity 250ms var(--ease-out);
}
```

## Drawer / Sheet
```css
.drawer {
  transform: translateY(0);
  transition: transform 500ms var(--ease-drawer);
}
.drawer[data-closed] {
  transform: translateY(100%);
}
```
Add drag → use spring + velocity handoff.

## Toast
```css
.toast {
  opacity: 1;
  transform: translateY(0);
  transition: opacity 400ms ease, transform 400ms ease;
  @starting-style {
    opacity: 0;
    transform: translateY(100%);
  }
}
```

## Accordion / Collapse
```css
.content {
  overflow: hidden;
  transition: height 200ms var(--ease-out), opacity 200ms var(--ease-out);
}
```
Measure height in JS; never animate to auto. Keep short.

## Stagger group entrance
```css
.item {
  opacity: 0;
  transform: translateY(8px);
  animation: fadeIn 300ms var(--ease-out) forwards;
}
.item:nth-child(2) { animation-delay: 50ms; }
.item:nth-child(3) { animation-delay: 100ms; }
.item:nth-child(4) { animation-delay: 150ms; }
@keyframes fadeIn {
  to { opacity: 1; transform: translateY(0); }
}
```
30–80ms between items. Decorative only — never block interaction.

## Hold to confirm (destructive)
```css
.overlay {
  clip-path: inset(0 100% 0 0);
  transition: clip-path 200ms var(--ease-out);
}
.button:active .overlay {
  clip-path: inset(0 0 0 0);
  transition: clip-path 2s linear;
}
.button:active {
  transform: scale(0.97);
}
```
Linear for progress fill. Slow press, snappy release.

## Tab indicator (clip-path technique)
Duplicate the tab list. Style the copy as active. Animate clip-path so text + background change in perfect sync.

## Scroll reveal (marketing only)
```css
.reveal {
  clip-path: inset(0 0 100% 0);
  transition: clip-path 600ms var(--ease-in-out);
}
.reveal[data-visible] {
  clip-path: inset(0 0 0 0);
}
```
Use IntersectionObserver once. Never on daily functional UI.

## Drag to dismiss
- Pointer capture
- Multi-touch protection
- Damping past boundaries (rising resistance)
- Velocity-based dismiss threshold
- Settle with spring: { type: "spring", duration: 0.5, bounce: 0.2 }

## Mask imperfect crossfade
```css
.content.transitioning {
  filter: blur(2px);
  opacity: 0.7;
}
```
Keep blur ≤ 4–8px.

## Programmatic without library (WAAPI)
```js
element.animate(
  [{ clipPath: 'inset(0 0 100% 0)' }, { clipPath: 'inset(0 0 0 0)' }],
  { duration: 1000, fill: 'forwards', easing: 'cubic-bezier(0.77, 0, 0.175, 1)' }
);
```
