# Reproducibility Notes

## Environment

Recommended:

- Python 3.10 or newer
- NumPy
- SciPy
- SymPy
- pytest

Install dependencies with:

```bash
pip install -r requirements.txt
```

## Test philosophy

The repository separates exact algebraic checks from controlled numerical checks.

### Exact checks

`test_modular_geometry.py` verifies the symbolic reflection and parabolic matrices.

`test_exact_edge_identity.py` verifies algebraically that

```text
2√2 - B_n^id = 8√2 q_n (1-q_n)
```

when

```text
q_n=(1-λ_n)/2,
B_n^id=2√2 λ_n².
```

`test_majorana_chsh.py` verifies finite-dimensional CAR identities, the full complex Wick contraction, and the CHSH operator identity.

### Numerical checks

`test_contact_spectral_edge.py` directly quadratures the Fourier transform of

```text
h(t)=1/[2π cosh(t/2)]
```

and compares it with `sech(πk)`.

`test_smooth_edge_asymptotics.py` evaluates the exact smooth bump declared in the analysis and confirms convergence to the leading `n^-2` coefficient.

## Important Wick-contraction convention

Majorana two-point contractions between distinct modes can be purely imaginary. They must remain complex until the four-point Wick combination is assembled. Taking the real part of individual two-point contractions before Wick reduction can create a false failure.

## Interpretation

Passing these tests verifies the declared formulas and numerical asymptotics implemented here. It does not by itself promote the model-specific result to a theorem for arbitrary interacting or nonfactorizing conformal field theories.

## Citable archive

The frozen repository release is archived on Zenodo as DOI **10.5281/zenodo.22649540**: https://doi.org/10.5281/zenodo.22649540
