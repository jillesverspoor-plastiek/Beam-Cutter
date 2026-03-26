# Beam-Cutter
A browser-based cutting stock optimizer that calculates the most efficient way to cut required lengths from standard-length beams, minimizing material waste and the number of beams needed.

Features
    
- Column Generation algorithm with two-phase simplex LP solver and unbounded knapsack pricing subproblem — provably near-optimal results
- Saw kerf loss per cut accounted for in all calculations
- Supports any unit (mm, cm, m, inches, etc.)
- Visual per-beam cutting plan with color-coded segments
- LP lower bound and optimality gap displayed so you know exactly how close to optimal the solution is
- Decimal length support with automatic integer scaling
- Runs entirely in the browser — no install, no server, no dependencies

How it works

The tool solves the classic https://en.wikipedia.org/wiki/Cutting_stock_problem using Column Generation: it iteratively builds an optimal set of cutting patterns by solving a master LP relaxation and a knapsack pricing subproblem, then rounds the fractional solution to integers with a greedy reduction pass.

Usage

Open beam-cutter.html in any modern browser. No build step or installation required.
