# A Geometric Proof of the Leibniz Formula for π via Gibbs Phasor Chain Convergence

**Author:** Sanjin Redzic, B.Sc.  
**Date:** March 14, 2026 (Pi Day)  
**License:** MIT

---

## What This Is

A new proof of the Leibniz formula

$$\frac{\pi}{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots$$

in which the value π is **constructed geometrically**, not imported from any external identity.

The proof uses the phasor chain arising from Fourier partial sums — a polygonal path in the complex plane formed by chaining arm vectors tip-to-tail. As the number of harmonics increases, the polygon converges to a circle. The ratio of its circumference to its diameter is π. The Leibniz partial sums are the axis projection of the chain endpoint. The value π/4 falls out of the geometry.

## The Core Idea

Every Fourier partial sum is a chain of rotating complex vectors. At odd harmonics, these arms have lengths 1, 1/3, 1/5, 1/7, ... and they chain together in the complex plane.

- At **zero curvature** (θ = 0): all arms align into a straight line.
- At the **Gibbs angle** (θ = π/(N+1)): the arms fold into a regular (N+1)-gon — a polygon that converges to a circle.
- At **maximum curvature** (θ = π/2): the arms fold back on themselves along the imaginary axis, alternating sign. The endpoint coordinate **is** the Leibniz sum 1 − 1/3 + 1/5 − 1/7 + ⋯

The Gibbs polygon and the Leibniz series are two states of the **same geometric object**, connected by a continuous curvature deformation. As N → ∞, the polygon becomes a circle, and π emerges from the ratio of circumference to radius.

π is not assumed. It is **produced** by the geometry.

## What Makes This Different from Standard Proofs

All known proofs of the Leibniz formula import π from an external source — the Taylor series of arctan(x), the periodicity of e^(iθ), or the Gaussian integral. In every case, π is a **known input**.

In this proof:

- π **emerges** as the limiting ratio of arc length to radius in a polygon that converges to a circle.
- The polygon is not imposed by construction (as in Archimedes); it **arises naturally** from the equal angular spacing of the Fourier phasor chain.
- The Dirichlet kernel is revealed as the **intrinsic velocity** of the curvature deformation, and the integral representation of the Leibniz sum follows from integrating this velocity.
- The sinc function sin(u)/u is identified as the **chord density** of the limiting circle.
- The convergence rate of the Leibniz series decomposes into a polygon-to-circle error of O(1/N²) and a Gibbs tail residual of O(1/N) — the engine is fast, the truncation is slow.

## The Gibbs Phenomenon as the Origin of π

The Gibbs overshoot is conventionally treated as a convergence defect — a nuisance to be windowed away. This proof reframes it: the Gibbs phenomenon is **where π comes from**. The overshoot exists because the phasor polygon is trying to become a circle and hasn't finished yet. The 18% overshoot factor Si(π)/(π/2) − 1 contains the same π, leaking out of the same geometry, before the limit is complete.

## Repository Contents

| File | Description |
|------|-------------|
| `Gibbs Pi Preview.png` | Visualization of the 9th Harmonic and its Phasor Chain |
| `Geometric Proof of the Leibnitz Formula for Pi Via Gibbs Phasor Chain Convergence.pdf` | Compiled paper (9 pages) |
| `README.md` | This file |

## Building from Source

```bash
pdflatex pi_gibbs_v2.tex
pdflatex pi_gibbs_v2.tex   # second pass for cross-references
```

## Background and Prior Work

This proof builds on the phasor chain geometry established in:

- **S. Redzic**, "Phasor chain geometry in Fourier partial sums: The Gibbs (N+1)-gon and its convergence to the apeirogon," 2025. [GitHub](https://github.com/ninjas1337). MIT License.

which proved that the Gibbs phasor chain at N harmonics folds into a regular (N+1)-gon, with a connection to the Archimedean construction of π via the apeirogon.

## Key References

- R. Roy, "The discovery of the series formula for π by Leibniz, Gregory and Nilakantha," *Mathematics Magazine*, 63(5), 291–306, 1990.
- K. Plofker, *Mathematics in India*, Princeton University Press, 2009.
- A. Zygmund, *Trigonometric Series*, 3rd ed., Cambridge University Press, 2002.
- E. Hewitt & R.E. Hewitt, "The Gibbs–Wilbraham phenomenon: An episode in Fourier analysis," *Archive for History of Exact Sciences*, 21(2), 129–160, 1979.
- P. Beckmann, *A History of Pi*, St. Martin's Press, 1971.

## Context

The proof was developed on March 14, 2026 — Pi Day — connecting cross-domain intuition from structural engineering vector analysis, Fourier methods in vibration and fatigue, process control on centrifugal compressors, and electrical phasor theory. The insight originated from a visualization of the Gibbs phenomenon that made the Dirichlet kernel visible as a physical chain of rotating arm vectors in the complex plane, revealing the circle hiding inside the odd-harmonic sum.

---

*Published as dated prior art under MIT License.*
