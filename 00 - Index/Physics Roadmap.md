**Vault:** Knowledge Map


---

## Phase 0 — Mathematical Tools

### Linear Algebra

**Key concepts**
- Complex numbers: ℂ = {a + bi | a, b ∈ ℝ}, i² = −1
- Complex conjugate: z̄ = a − bi, z·z̄ = |z|²
- Modulus: |z| = √(a² + b²) — distance from the origin in the complex plane
- Inverse: z⁻¹ = z̄ / |z|²
- Polar form: z = r·cis(θ), cis(θ) = cos θ + i sin θ
- De Moivre: zⁿ = rⁿ·cis(nθ)

---

## Phase 1 — Classical Foundation

### Mechanics — Basics

**Kleppner & Kolenkow — *An Introduction to Mechanics*** : the best intro mechanics book
- Ch. 1: Vectors and Kinematics
- Ch. 2: Newton's Laws
- Ch. 3: Forces and Equations of Motion
- Ch. 4: Momentum
- Ch. 5: Energy
- Ch. 6: Angular Momentum and Fixed Axis Rotation
- Ch. 7: Rigid Body Motion and the Conservation of Angular Momentum
- Ch. 9: Central Force Motion
- Ch. 10: The Harmonic Oscillator

**After this book you can:**
- Solve any kinematics problem in 2D and 3D from first principles
- Apply Newton's laws to any system with multiple forces and constraints
- Calculate work, kinetic and potential energy for any configuration
- Analyze elastic and inelastic collisions using conservation of momentum
- Calculate moment of inertia and apply angular momentum conservation to rotating systems
- Derive the equation of motion for a spring-mass system and solve it for position vs time

**Also useful:**
- Morin — *Introduction to Classical Mechanics* : hardest problems, builds the strongest intuition
- Halliday, Resnick & Krane — *Physics Vol. 1* : broader coverage, good reference

**YouTube**
- Walter Lewin — MIT 8.01 : watch the energy and momentum lectures
- Michel van Biezen — short videos on every topic

**Key concepts**
- Kinematics: position, velocity, acceleration in 1D, 2D, 3D
- Newton's 3 laws — F = ma and its consequences
- Work-energy theorem: W = ΔKE
- Conservation of energy: KE + PE = constant
- Linear momentum, impulse, conservation in collisions
- Rotational motion: torque τ = r × F, moment of inertia
- Angular momentum L = r × p and its conservation
- Gravitation: Newton's law, orbital mechanics
- Spring force F = −kx → simple harmonic motion

---

### Mechanics — Oscillators and Coupled Systems

**Taylor — *Classical Mechanics*** : the best intermediate mechanics textbook
- Ch. 5: Oscillations
- Ch. 11: Coupled Oscillators and Normal Modes

**After these chapters you can:**
- Derive the equation of motion for a damped driven oscillator and solve it in steady state
- Calculate the Q factor and resonance linewidth of any oscillator
- Find the amplitude and phase of a driven oscillator at any frequency
- Set up the 2×2 eigenvalue problem for two coupled oscillators
- Find the normal mode frequencies and normal mode shapes
- Recognize that your CW-CCW ring resonator system is exactly this — two coupled oscillators

**Also useful:**
- Marion & Thornton — *Classical Dynamics* → Ch. 12: The Damped Driven Oscillator

**YouTube**
- Walter Lewin — MIT 8.01 (oscillator lectures)
- Michel van Biezen — oscillator videos

**Key concepts**
- Simple, damped, driven harmonic oscillator
- Q factor and resonance linewidth
- Coupled oscillators — normal modes and beat frequency
- Two coupled oscillators → 2×2 eigenvalue problem

---
### Electricity & Magnetism

**Griffiths — *Introduction to Electrodynamics* (4th ed.)** : the best E&M textbook
- Ch. 7: Electrodynamics
- Ch. 8: Conservation Laws
- Ch. 9: Electromagnetic Waves

**After these chapters you can:**
- Write all 4 Maxwell's equations from memory and explain each term physically
- Derive the wave equation ∇²E = μ₀ε₀ ∂²E/∂t² starting from Maxwell's equations
- Explain where the refractive index n = √εᵣ comes from — not as a given but as a consequence
- Apply boundary conditions at a dielectric interface and derive Fresnel coefficients
- Explain why a complex refractive index means the material absorbs light
- Calculate the time-averaged Poynting vector ⟨S⟩ = ½ Re(E × H*) for any plane wave
- Derive Poynting's theorem: ∂u/∂t + ∇·S = −J·E and explain each term physically
- Explain that ⟨S⟩ is the intensity measured in the lab — power per unit area
- Connect the Poynting vector to your CMT: κₑ is proportional to the Poynting flux integrated across the bus-ring gap

**Also useful:**
- Purcell & Morin — *Electricity and Magnetism* : derives magnetism from special relativity, deepest intuition
- Wangsness — *Electromagnetic Fields* : broader and more systematic

**YouTube**
- Walter Lewin — MIT 8.02 : watch the Faraday's law demonstration
- Eugene Khutoryansky — field visualizations
- Zach Star — conceptual E&M

**Key concepts**
- All 4 Maxwell's equations in vacuum and in matter
- Wave equation: ∇²E = μ₀ε₀ ∂²E/∂t² → c = 1/√(μ₀ε₀)
- Refractive index n = √εᵣ
- Poynting vector S = E×H — power flow
- Boundary conditions at dielectric interfaces

---

## Phase 2 — Advanced Framework

### Analytical Mechanics

**Taylor — *Classical Mechanics*** : the best intermediate mechanics textbook
- Ch. 6: Calculus of Variations
- Ch. 7: Lagrange's Equations : start here
- Ch. 13: Hamiltonian Mechanics

**After these chapters you can:**
- Write the Lagrangian for any mechanical system in any coordinate system
- Derive the equations of motion using Euler-Lagrange without drawing a free-body diagram
- Convert any Lagrangian system to Hamiltonian formalism
- Write Hamilton's equations and recognize that da/dt = −iHa is exactly this
- Understand why Poisson brackets become commutators in quantum mechanics

**Landau & Lifshitz — *Mechanics* Vol. 1** : 170 pages of pure insight
- Ch. 1: The Equations of Motion
- Ch. 2: Conservation Laws
- Ch. 7: The Canonical Equations

**After this book you can:**
- Derive all conservation laws from symmetry principles (Noether's theorem)
- See the deep connection between symmetry and conserved quantities
- Understand why the Hamiltonian formalism is the natural language for quantum mechanics

**Also useful:**
- Goldstein, Poole & Safko — *Classical Mechanics* : graduate reference
  - Ch. 1: Survey of the Elementary Principles
  - Ch. 8: The Hamilton Equations of Motion
  - Ch. 9: Canonical Transformations

**YouTube**
- **Leonard Susskind — Classical Mechanics (Stanford)** : 10 lectures, watch all
- Michel van Biezen — Lagrangian playlist

**Key concepts**
- Lagrangian L = T − V and Euler-Lagrange equations
- Hamiltonian H = T + V and Hamilton's equations
- da/dt = −iHa — Hamiltonian equation of motion
- Poisson brackets → commutators in QM

---

### EM Fields & Waves

**Griffiths — *Introduction to Electrodynamics*** : read Ch. 9 here
- Ch. 9: Electromagnetic Waves : most important chapter for photonics

**After this chapter you can:**
- Derive plane wave solutions to Maxwell's equations in a medium
- Explain what a complex refractive index means for wave propagation and loss
- Calculate reflection and transmission coefficients at any interface
- Explain why light slows down in glass from Maxwell's equations — not from definition

**Pozar — *Microwave Engineering*** : bridges Maxwell to waveguide engineering
- Ch. 2: Transmission Line Theory
- Ch. 3: Transmission Lines and Waveguides

**After these chapters you can:**
- Understand S-parameters and recognize that your T(Δ) is S₂₁
- Set up the eigenvalue problem for waveguide modes
- Explain what TE and TM modes are and how they are confined
- Recognize that impedance matching is the same as critical coupling in your ring resonator

**Also useful:**
- Yariv & Yeh — *Photonics* : waveguide and CMT chapters

**YouTube**
- MIT 8.03 — Vibrations and Waves (OCW)

**Key concepts**
- Boundary conditions at dielectric interfaces
- TE and TM waveguide modes — eigenvalue problem
- S-parameters
- Complex refractive index: n = nᵣ + inᵢ
- Impedance matching = critical coupling

---


### Optics

**Hecht — *Optics* (4th ed.)** : the standard optics textbook

*Wave foundations — read first*
- Ch. 2: Wave Motion — the wave equation, monochromatic waves
- Ch. 3: Electromagnetic Theory, Photons, and Light — Helmholtz equation, plane waves, polarization, reflection

*Geometric optics*
- Ch. 4: The Propagation of Light — Fermat's principle, reflection, refraction
- Ch. 5: Geometrical Optics — lenses, mirrors, optical instruments, ABCD matrices

*Wave phenomena*
- Ch. 7: The Superposition of Waves
- Ch. 8: Polarization — Jones vectors, wave plates, Brewster's angle
- Ch. 9: Interference — Young's experiment, thin films, Fabry-Pérot
- Ch. 10: Diffraction — single slit, gratings, circular apertures, resolving power
- Ch. 12: Basics of Coherence Theory — coherence length, coherence time

**After this book you can:**
- Derive the wave equation and the Helmholtz equation from Maxwell's equations
- Write the general monochromatic plane wave solution and identify k, ω, phase
- Apply Snell's law and trace rays through any lens or mirror system
- Use ABCD ray matrices to analyze any sequence of optical elements
- Derive the Fresnel reflection and transmission coefficients at an interface
- Calculate the interference pattern for any two-beam configuration
- Analyze a Fabry-Pérot resonator spectrum — directly the same physics as your ring resonator
- Calculate the diffraction pattern from any aperture geometry
- Describe any polarization state using Jones vectors and calculate its transformation through wave plates
- Define coherence length and coherence time and explain why HOM requires photons within the coherence length
- Know when geometric optics breaks down and wave optics must be used

---

**Goodman — *Introduction to Fourier Optics*** : the definitive book on Fourier optics
- Ch. 2: Analysis of Two-Dimensional Signals and Systems : start here
- Ch. 4: Fresnel and Fraunhofer Diffraction
- Ch. 5: Wave-Optics Analysis of Coherent Optical Systems

**After these chapters you can:**
- Explain why the far field of any aperture is its Fourier transform
- Analyze any 4f optical system as a spatial frequency filter
- Decompose any optical field into spatial modes using overlap integrals
- Explain your mode sorter as a spatial Fourier processor — not just call it one

---

**Goodman — *Statistical Optics*** : the bridge to quantum optics
- Ch. 3: Random Processes
- Ch. 5: Coherence Theory (statistical treatment)
- Ch. 9: Semiclassical Theory of Photoelectric Detection

**After these chapters you can:**
- Describe a light field statistically using its coherence function
- Explain speckle and why it appears with coherent illumination
- Understand semiclassical photodetection — the classical precursor to photon counting
- See why the transition from Statistical Optics to Quantum Optics is a small step, not a large one

---

**Saleh & Teich — *Fundamentals of Photonics*** : most comprehensive single photonics reference
- Ch. 1: Ray Optics
- Ch. 2: Wave Optics
- Ch. 3: Beam Optics
- Ch. 4: Fourier Optics

**After these chapters you can:**
- Work with Gaussian beams and ABCD matrices for any optical system
- Calculate beam waist, Rayleigh range, and mode matching efficiency
- Connect wave optics to ray optics and understand when each applies

**Also useful:**
- Born & Wolf — *Principles of Optics* : the classical reference, very complete
- Voelz — *Computational Fourier Optics* : adds numerical simulation to the theory

**YouTube**
- Huygens Optics — interference and diffraction visualizations : watch before opening the book
- Eugene Khutoryansky — polarization animations
- MIT 8.03 — Vibrations and Waves (OCW) : bridges EM waves to optics
- Applied Science — experimental demonstrations

**Key concepts**

*Wave foundations*
- Wave equation: ∇²u = (1/v²) ∂²u/∂t²
- Helmholtz equation: ∇²U + k²U = 0
- Monochromatic plane wave: U(r,t) = A e^{i(k·r − ωt)}
- Reflection and transmission at an interface — Fresnel coefficients

*Geometric Optics*
- Fermat's principle — light takes the path of stationary optical path length
- Snell's law: n₁ sin θ₁ = n₂ sin θ₂
- Total internal reflection: θ_c = arcsin(n₂/n₁)
- Thin lens equation: 1/f = 1/dₒ + 1/dᵢ
- ABCD ray matrices for any optical element

*Wave Optics*
- Huygens' principle — every point on a wavefront is a new source
- Young's double slit — path difference → phase difference → intensity pattern
- Fabry-Pérot cavity — same resonance condition as your ring resonator: round-trip phase = 2πm
- Single slit diffraction — first zero at sin θ = λ/a
- Diffraction grating — mλ = d sin θ

*Polarization*
- Linear, circular, elliptical polarization
- Jones vector representation
- Malus's law: I = I₀ cos²θ
- Brewster's angle: tan θ_B = n₂/n₁
- Half-wave plate, quarter-wave plate

*Coherence*
- Coherence length: l_c = λ²/Δλ
- Coherence time: τ_c = l_c/c
- Temporal coherence → determines HOM visibility
- Spatial coherence → determines fringe visibility in interference

*Fourier Optics*
- Fraunhofer diffraction = Fourier transform of the aperture
- Spatial modes as orthogonal basis functions
- Mode decomposition and overlap integrals
- 4f optical system and its transfer function
- Gaussian beam optics and ABCD matrices
- OAM vortex beams: e^{ilφ} helical phase
- HG, LG, BG modes and inter-mode transformations

*Statistical Optics*
- Random processes and ensemble averages applied to light
- Mutual coherence function Γ(r₁, r₂, τ)
- Degree of coherence and its relation to fringe visibility
- Speckle statistics
- Semiclassical photodetection — shot noise from a classical field

---


## Phase 3 — Quantum Framework

### Quantum Mechanics 1

**Griffiths — *Introduction to Quantum Mechanics*** : the best QM1 textbook
- Ch. 1: The Wave Function
- Ch. 2: Time-Independent Schrödinger Equation : harmonic oscillator and ladder operators
- Ch. 3: Formalism
- Ch. 4: Quantum Mechanics in Three Dimensions

**After these chapters you can:**
- Write the Schrödinger equation and explain every term physically
- Solve the quantum harmonic oscillator using ladder operators â and â†
- Calculate expectation values of any observable using Dirac notation
- Apply time evolution to any energy eigenstate
- Recognize that the ladder operator algebra for the harmonic oscillator is identical to the algebra for photons — this IS field quantization

**Also useful:**
- Shankar — *Principles of Quantum Mechanics* : cleanest mathematical treatment
- Sakurai & Napolitano — *Modern Quantum Mechanics* : graduate standard

**YouTube**
- **MIT 8.04 — Quantum Physics I (Zwiebach)** : full course, excellent
- **Leonard Susskind — Quantum Mechanics (Stanford)**
- Professor M does Science — Dirac notation and operators

**Key concepts**
- Schrödinger equation: iℏ ∂ψ/∂t = Hψ
- Quantum harmonic oscillator: Eₙ = (n+½)ℏω
- Ladder operators: â|n⟩ = √n|n−1⟩ and â†|n⟩ = √(n+1)|n+1⟩
- Dirac notation: bras ⟨φ|, kets |ψ⟩
- Time evolution: |ψ(t)⟩ = e^{−iHt/ℏ}|ψ(0)⟩

---

### Quantum Mechanics 2

**Griffiths — *Introduction to Quantum Mechanics*** : continue from QM1
- Ch. 5: Identical Particles : read this first
- Ch. 6: Time-Independent Perturbation Theory

**After these chapters you can:**
- Explain from first principles why two identical bosons entering a beam splitter always exit the same port
- Write the correctly symmetrized wavefunction for any system of identical bosons or fermions
- Calculate first-order energy corrections using perturbation theory
- Recognize that coupled-mode theory is perturbation theory applied to Maxwell's equations

**Sakurai & Napolitano — *Modern Quantum Mechanics*** : graduate level, more complete
- Ch. 3: Theory of Angular Momentum
- Ch. 5: Approximation Methods
- Ch. 6: Identical Particles

**After these chapters you can:**
- Work fluently with angular momentum algebra including addition of angular momenta
- Derive selection rules using symmetry arguments
- Recognize that OAM modes are labeled by the eigenvalues of the angular momentum operator Lz

**Also useful:**
- Cohen-Tannoudji — *Quantum Mechanics* Vol. 2 : deepest perturbation theory treatment

**YouTube**
- MIT 8.05 — Quantum Physics II (OCW)
- Leonard Susskind — Quantum Entanglement
- Professor M does Science — angular momentum series

**Key concepts**
- Identical particles: bosons vs fermions
- Symmetrization: |ψ±⟩ ∝ |1⟩|2⟩ ± |2⟩|1⟩
- HOM: two identical bosons always exit the same port
- Second quantization: â, â† operators for fields
- Perturbation theory

---

## Phase 4 — Quantum Photonics : current focus

### Quantum Optics : read this first, now

**Gerry & Knight — *Introductory Quantum Optics*** : the best entry-level quantum optics book
- Ch. 1: Introduction
- Ch. 2: Field Quantization : start here
- Ch. 6: Beam Splitters and Interferometers
- Ch. 7: Nonclassical Light

**After these chapters you can:**
- Quantize the electromagnetic field from scratch starting from Maxwell's equations
- Explain what a Fock state |n⟩ is physically — not as a definition but as n quanta of excitation
- Write the beam splitter transformation in terms of creation and annihilation operators
- Derive from first principles that the HOM coincidence rate is exactly zero for perfectly identical photons
- Calculate HOM visibility as a function of photon distinguishability
- Explain the difference between a coherent state, a Fock state, and a thermal state

**Walls & Milburn — *Quantum Optics*** : graduate standard, more complete
- Ch. 4: Quantum Coherence Functions
- Ch. 6: Quantum Theory of Damping
- Ch. 7: Input-Output Formulation of Optical Cavities

**After these chapters you can:**
- Calculate g⁽²⁾(0) for any quantum state and interpret the result
- Write the input-output equations for a cavity — directly connected to your CMT
- Understand how loss enters the quantum description of a resonator

**Also useful:**
- Mandel & Wolf — *Optical Coherence and Quantum Optics* : the bible, use selectively
- Vogel & Welsch — *Quantum Optics* : best on quantum state tomography

**YouTube**
- **Alain Aspect — Quantum Optics (Institut d'Optique)** : Nobel laureate, covers HOM directly
- **Aephraim Steinberg — Quantum Optics (Toronto)** : clearest full course on YouTube
- MIT 8.422 — Atomic and Optical Physics II (OCW)
- QuTiP tutorials — simulate what you read

**Key concepts**
- Field quantization: photons from first principles
- Fock states |n⟩, coherent states |α⟩
- Beam splitter transformation: â_out = tâ_in + râ_other
- HOM effect: two identical photons → always exit the same port
- Coincidence counting g⁽²⁾(0) — bunching vs antibunching
- Density matrix ρ and Wigner function
- Quantum state tomography

---

## Reading rules

1. Never read a full book — read the chapters that answer a specific question
2. When something blocks you — find the chapter, read it, do two problems, return
3. Current highest priority: **Gerry & Knight Ch. 2 and Ch. 6**
