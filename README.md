# Universal Physics Matrix · Invariant Rank-2 Matrix

<div align="center">

**Una matriz invariante de rango 2 sobre 26 dimensiones, con sus propiedades algebraicas verificables y sus proyecciones visuales en 3D.**

[![Three.js](https://img.shields.io/badge/Three.js-r128-black?logo=three.js)](https://threejs.org/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-experimental-orange.svg)]()

</div>

---

## 📐 Objeto Matemático Central

La matriz **M ∈ ℝ²⁶ ˣ ²⁶** que estructura todo este repositorio se define por:

$$
M_{i,j} = 
\begin{cases}
\dfrac{1}{i! \cdot j!} & \text{si } i \equiv j \pmod 2 \\[8pt]
0 & \text{si } i \not\equiv j \pmod 2
\end{cases}
\qquad i, j \in \{0, 1, 2, \ldots, 25\}
$$

### Forma explícita (esquinas visibles)
[ 1 0 1/2! 0 1/24 0 ⋯ 0 1/26! ]
[ 0 1 0 1/6 0 1/120 ⋯ 1/25! 0 ]
[ 1/2! 0 1/4 0 1/48 0 ⋯ 0 1/(2!·26!) ]
[ 0 1/6 0 1/36 0 1/720 ⋯ 1/(3!·25!) 0 ]
[ 1/24 0 1/48 0 1/576 0 ⋯ 0 1/(4!·26!) ]
[ ⋮ ⋮ ⋮ ⋮ ⋮ ⋮ ⋱ ⋮ ⋮ ]
[ 0 1/25! 0 1/(3!·25!) 0 ⋯ ⋯ 1/(25!)² 0 ]
[ 1/26! 0 1/(2!·26!) 0 1/(4!·26!) 0 ⋯ 0 1/(26!)² ]

text

---

## 🔬 Propiedades Verificadas

| Propiedad | Valor | Estado |
|---|---|---|
| **Tamaño** | 26 × 26 | ✅ |
| **Simetría** | `M = Mᵀ` (asimetría máx < 10⁻¹⁵) | ✅ |
| **Rango** | **2** (bloque par R1 + bloque impar R1) | ✅ |
| **Factorización** | `M = v_e · v_eᵀ ⊕ v_o · v_oᵀ` | ✅ |
| **Norma Frobenius** | `‖M‖_F = √(Σᵢⱼ Mᵢⱼ²)` finita | ✅ |
| **Decaimiento** | Factorial `1/i!` (más rápido que cualquier exponencial) | ✅ |

### Descomposición en bloques por paridad

La matriz se descompone en dos bloques diagonales, con ceros fuera de ellos:
pares (13×13) impares (13×13)
┌─────────────┬─────────────┐
pares │ M_ee │ 0 │ M_ee = v_e · v_eᵀ → rango 1
├─────────────┼─────────────┤
impar. │ 0 │ M_oo │ M_oo = v_o · v_oᵀ → rango 1
└─────────────┴─────────────┘
rank(M) = 1 + 1 = 2
