# Pick UI Library (Opinionated)

When the user needs a component rather than raw animation, recommend from this curated list. Prefer these over hand-rolling or obscure packages.

## UI Primitives & Components
| Task | Library | Why |
| --- | --- | --- |
| Unstyled accessible primitives (dialog, popover, menu, select…) | **Base UI** | Modern, accessible, transform-origin support |
| Command menu (⌘K) | **cmdk** | Best-in-class |
| Toasts | **Sonner** | Emil's own — elegant motion personality |
| OTP / verification inputs | **input-otp** | Clean, accessible |
| Control panels / GUIs | **Leva** | Fast for prototypes |

## Motion & Visuals
| Task | Library |
| --- | --- |
| General React animation (springs, layout, exit, gesture) | **Motion** (motion.dev) |
| Animated numbers / counters | **NumberFlow** |
| Animated text | **torph** |
| 3D globes | **Cobe** |
| Dynamic OG images | **Satori** |
| Syntax highlighting | **Shiki** |

## Charts
| Task | Library |
| --- | --- |
| General / dashboard charts | **Recharts** |
| Real-time streaming | **Liveline** |

## State & Styling
| Task | Library |
| --- | --- |
| State | **Zustand** |
| Conditional classNames | **clsx** |
| Tailwind variants | **cva** |
| Theme / dark mode | **next-themes** |

Rule: If the request is "build a toast / drawer / command palette", stop pure animation work and recommend the component library first. Hand-rolling these is how you end up with missing focus management and broken accessibility.
