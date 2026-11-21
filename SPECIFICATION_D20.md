# Polybrutus D20 — Exact twenty-five-point Euclidean specification

**Frozen predecessor:** `Topbrutus/polybrutus-d19@v0.1.0`, source commit `1aa9721edcf6eb374a301863a5c1c4e566e69838`, DOI `10.5281/zenodo.24409343`.

Let `p1,...,p24` be the exact D19 radius-one unit vectors stored in twenty coordinate slots. The original five-simplex coordinate block lies in a four-dimensional centered hyperplane and creates one exact coordinate relation.

For `i=1,...,24`, embed `q_i=(p_i,0)` in 21 storage slots; adjoin `q25=e21=(0,...,0,1)`. The new unit point is perpendicular to all predecessor vectors. Thus `||q25-q_i||²=1+1-2<q25,q_i>=2` for every old point. For radius `R>0`, the 24 new squared pair distances are `2R²`.

All **276 labelled old pair distances** remain precisely unchanged. Total **C(25,2)=300** pairs; intrinsic affine dimension **20**, with 21 storage coordinates and one simplex relation.

Distance-family histogram for `k=4d²/R²`:
```
k:            4  7   8   9  10  12  13  16
multiplicity: 6  2  269   3  10   6   2   2
```
The squared-distance sum is `2447R²/4`. At `R=1`, centroid is `(0,0,1/50,0,0,0,0,0,1/25,...,1/25)`, where the final 1/25 occurs 13 times.

## Selected theoretical weighted graph

Mathematically choose unit scalar masses and complete edge weights `w_ij=R²/d_ij²`; this does not describe an experiment. The added point uniformly couples to 24 old vertices at weight 1/2:

```
L20 = [ L19+(1/2)I24  -(1/2)1 ]
      [ -(1/2)1ᵀ            12  ].
```

If `f6(z)=chiP7(z)/z` is the six-nonzero-mode factor of the canonical seven-vertex graph, then:
```
chi25(z)=z(z-25/2)chi24(z-1/2)/(z-1/2)
        =z(z-25/2)^14(z-12)^4*f6(z-9).
```

Eigenvalue **25/2** has exact multiplicity **14** and eigenvalue **12** multiplicity **4**, exclusively as properties of this chosen ideal graph.
