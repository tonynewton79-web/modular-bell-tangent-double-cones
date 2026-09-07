# Verification Results

This repository is expected to verify the following results.

## Exact modular geometry

```text
R_A^2 = I
R_B^2 = I
R_A R_B = -G_AB
tr(G_AB) = 2
G_AB^{-1} = [[1,0],[4/L,1]]
```

The projective action of `G_AB` satisfies

```text
1/u' = 1/u - 4/L.
```

## Contact Fourier multiplier

For

```text
h(t)=1/[2π cosh(t/2)],
```

the direct numerical Fourier transform agrees with

```text
m(k)=sech(πk)
```

to high numerical precision at representative momenta.

## Smooth-edge coefficient

For the normalized bump

```text
χ(x) ∝ exp[-1/(x(1-x))],  0<x<1,
```

the ratio

```text
(1-λ_n) / [(π²/(2n²)) ||χ'||²]
```

converges to `1` as `n` increases.

Representative independently observed values were approximately:

```text
n=128   ratio≈0.9841
n=256   ratio≈0.9959
n=512   ratio≈0.9990
n=1024  ratio≈0.9997
```

## Exact Bell-contact identity

With

```text
q_n=(1-λ_n)/2,
B_n^id=2√2 λ_n²,
```

the finite-`n` relation is exact:

```text
2√2-B_n^id = 8√2 q_n(1-q_n).
```

Equivalently,

```text
(2√2-B_n^id)/(8√2 q_n)=1-q_n=(1+λ_n)/2.
```

## Majorana/Wick/CHSH checks

The finite-dimensional test verifies:

```text
γ_i²=I
{γ_i,γ_j}=0  (i≠j)
```

and the complex Gaussian four-point Wick identity

```text
<a1 a2 b1 b2>
 = <a1 a2><b1 b2>
 - <a1 b1><a2 b2>
 + <a1 b2><a2 b1>.
```

It also verifies

```text
C²=D²=I,
CHSH = √2(A1 B1 + A2 B2),
||CHSH|| ≤ 2√2,
```

with the explicit matrix representation attaining operator norm `2√2`.

## Release provenance

These verification results accompany the archived repository release DOI **10.5281/zenodo.22649540**.
