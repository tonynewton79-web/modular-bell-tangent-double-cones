# Modular Bell Geometry of Two Tangent Double Cones

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22649540.svg)](https://doi.org/10.5281/zenodo.22649540)

Reproducibility repository for the analytic and computational checks supporting the tangent-double-cone modular/Bell construction in the free massless Majorana model.

**Author:** Tony Newton  
**Research affiliation:** Newton Astro Labs, London, UK  
**Archived release DOI:** [10.5281/zenodo.22649540](https://doi.org/10.5281/zenodo.22649540)

## What this repository verifies

The repository independently checks the main algebraic and numerical components of the construction:

1. **Parabolic relative modular geometry**
   - `R_A^2 = R_B^2 = I`
   - `R_A R_B = -G_AB`
   - `G_AB^{-1}` has the stated sign structure
   - `tr(G_AB)=2`, identifying the projective transformation as parabolic

2. **Tangent contact spectral edge**
   - The logarithmic contact kernel
     `h(t)=1/[2π cosh(t/2)]`
     has Fourier multiplier
     `m(k)=sech(πk)`.
   - The multiplier reaches the spectral edge `m(0)=1`.

3. **Smooth contact-edge asymptotics**
   - Uses the compactly supported bump
     `χ(x) ∝ exp[-1/(x(1-x))]`, `0<x<1`.
   - Verifies numerically
     `1-λ_n ~ (π²/(2n²)) ||χ'||²`.

4. **Exact Bell-contact identity**
   - With
     `q_n=(1-λ_n)/2` and `B_n^id=2√2 λ_n²`, verifies the exact finite-`n` identity
     `2√2-B_n^id = 8√2 q_n(1-q_n)`.

5. **Majorana/Wick/CHSH algebra**
   - Builds an explicit Jordan-Wigner Majorana representation.
   - Checks Majorana involution and anticommutation relations.
   - Verifies the complex fermionic Wick four-point identity.
   - Verifies the CHSH operator reduction and Tsirelson operator norm.

## Repository layout

```text
.
├── README.md
├── REPRODUCIBILITY.md
├── RESULTS.md
├── AUTHORS.md
├── CITATION.cff
├── LICENSE
├── requirements.txt
├── run_all_tests.py
├── tests/
│   ├── test_modular_geometry.py
│   ├── test_contact_spectral_edge.py
│   ├── test_smooth_edge_asymptotics.py
│   ├── test_exact_edge_identity.py
│   └── test_majorana_chsh.py
└── .github/workflows/tests.yml
```

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python run_all_tests.py
```

Or run with pytest:

```bash
pytest -q
```

## Expected release condition

A clean run should end with all tests passing. The tests are designed as reproducibility checks of declared analytic identities and controlled numerical relations; they are not evidence for a universal interacting-QFT theorem.

## Scope

The explicit contact operator, smooth Majorana sequence, Wick reduction, and Bell construction tested here are scoped to the declared free massless Majorana setting. The projective parabolic matrix identities are exact algebraic checks.

## Authorship and use

All repository code, test organization, reproducibility scripts, and certificate criteria in this GitHub package are presented under the sole repository authorship of **Tony Newton**.

## Archived release

The citable archived release of this repository is deposited on Zenodo with DOI **10.5281/zenodo.22649540**.

Preferred software citation: **Tony Newton, _Modular Bell Geometry of Two Tangent Double Cones: Reproducibility Code and Tests_, version 1.0.0, Zenodo, 2026. DOI: 10.5281/zenodo.22649540.**
