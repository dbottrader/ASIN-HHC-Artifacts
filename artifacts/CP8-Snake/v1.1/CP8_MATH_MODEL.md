# CP8 Snake Mathematical Model v1.1

## 1. Hypercube graph

The `n`-cube is `Q_n = (V,E)` with:

```text
V = {0,1}^n
E = {(u,v) : d_H(u,v)=1}
```

A snake is an induced path `P = (v_0,...,v_k)`.

## 2. Validity predicate

```text
VALID(P) = UNIQUE(P)
        ∧ ∀i, d_H(v_i,v_{i+1}) = 1
        ∧ ∀i,j with |i-j|>1, d_H(v_i,v_j) >= 2
```

This predicate is binary and is the source of `C`, the 428 Core component.

## 3. Flip sequence

Each edge flips exactly one bit. Define:

```text
b_i = log2(v_{i-1} XOR v_i)
```

For bit `r`, let `c_r` be the number of edges whose flip index is `r`. With `m=k` edges:

```text
p_r = c_r / m
H = -Σ p_r log2(p_r)
F = H / log2(n)
```

`F ∈ [0,1]` is the 528 Fusion component. It measures how broadly the path distributes transitions across available dimensions.

For a zero-edge path, `F=0`.

## 4. State-space integration

```text
I = |P| / 2^n
```

`I ∈ (0,1]` is the 963 Integration component.

## 5. Composite

```text
S_CP8 = 100 × (428C + 528F + 963I) / (428+528+963)
       = 100 × (428C + 528F + 963I) / 1919
```

The constants identify CP8 layers and provide explicit weighting. This is an auxiliary ranking metric, not an extremal proof.

## 6. φ-guided tie break

For candidate vertex integer `u` at depth `d`:

```text
T_phi(u,d) = frac(((u+1)×137.507764 + 111d) / 360)
```

Legal candidates are ordered by:

1. ascending onward legal degree;
2. ascending `T_phi` when CP8 φ-guided mode is selected.

The search seed is derived deterministically from dimension, time budget, strategy, and the CP8 namespace constants. Time limits can still make final node counts runtime-dependent, so the receipt records the seed and examined-node count.

## 7. Projection

Projection basis vector `i` uses:

```text
θ_i = -π/2 + i × 137.507764°
w_i = 0.72 + 0.28√((i+1)/n)
B_i = w_i(cos θ_i, sin θ_i)
```

A binary vertex is mapped by summing `+B_i` or `-B_i` according to each bit.

Projection is visual only and does not affect path validity.

## 8. Proof hierarchy

```text
Induced-path verifier  -> structural proof of this path
SHA-256 seal           -> receipt integrity
CP8 composite          -> auxiliary path characterization
ANU-28 glyph           -> semantic routing metadata
Heuristic search       -> candidate generation, not optimality proof
```
