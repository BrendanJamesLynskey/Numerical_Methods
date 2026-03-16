# Numerical Methods Visualiser

An interactive single-file HTML application for exploring four core areas of numerical methods with real-time visualisation.

## Features

### 1. Root Finding
- **Methods:** Bisection, Newton-Raphson, Secant, Fixed-Point Iteration
- Step-by-step animation showing each iteration on the function graph
- Newton-Raphson tangent lines, bisection interval narrowing, secant lines, and fixed-point cobweb diagrams
- Convergence plot (log error vs iteration)
- Side-by-side method comparison
- Preset functions: `x^3-x-2`, `cos(x)-x`, `exp(-x)-x`, `x^2-2`

### 2. Numerical Integration
- **Methods:** Left/Right/Midpoint Rectangle, Trapezoidal, Simpson's 1/3, Simpson's 3/8, Gauss-Legendre (2-point, 3-point)
- Visual overlay of rectangles, trapezoids, parabolic arcs, or Gauss nodes on the function plot
- Adjustable number of panels with live re-rendering
- Convergence analysis: log-log error vs n plot showing order of each method

### 3. ODE Solvers
- **Methods:** Euler, Improved Euler (Heun), RK4, Adaptive RK45 (Dormand-Prince)
- Animated step-by-step solution curve drawing
- Overlay of exact solution (when provided) for error comparison
- Error vs time plot
- Adjustable step size to demonstrate instability with large h
- Presets: exponential growth/decay, logistic equation, trigonometric ODE

### 4. Interpolation
- **Methods:** Lagrange polynomial, Newton's divided differences, Cubic spline
- Click on the canvas to place data points; right-click to remove
- Optional display of Lagrange basis functions
- Runge phenomenon demonstration with adjustable equally-spaced point count on 1/(1+25x^2)
- Presets: Runge function, sine wave, step function, quadratic

## Usage

Open `index.html` in any modern web browser. No build step, server, or external dependencies required (fonts are loaded from Google Fonts for styling, but the app functions without them).

### Math Expression Syntax

User-entered functions support:
- Arithmetic: `+`, `-`, `*`, `/`, `^`
- Functions: `sin`, `cos`, `tan`, `asin`, `acos`, `atan`, `exp`, `log` (natural), `sqrt`, `abs`, `sinh`, `cosh`, `tanh`, `ceil`, `floor`
- Constants: `pi`, `e`
- Parentheses for grouping

Examples:
- `x^3 - x - 2`
- `cos(x) - x`
- `exp(-x^2)`
- `1/(1 + 25*x^2)`

## Technology

- Vanilla JavaScript with HTML5 Canvas rendering
- Safe math expression parser (no `eval`)
- DM Sans + JetBrains Mono fonts
- Dark theme with teal, amber, rose, and purple accent colours
