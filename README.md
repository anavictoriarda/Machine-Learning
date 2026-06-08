[README.md](https://github.com/user-attachments/files/28689989/README.1.md)
# Machine Learning — Notas Matemáticas

Documentos en LaTeX sobre algoritmos de aprendizaje automático no supervisado, con énfasis en formulación matemática rigurosa, demostraciones y variantes.

---

## Contenido

### `K.tex` — Algoritmo K-means
Presentación en Beamer (formato 16:9) que cubre la formulación matemática del algoritmo K-means y sus variantes.

**Temas:**
- Introducción al clustering (jerárquico vs. particional)
- Formulación como problema de optimización combinatoria (minimización de SSE / inertia)
- Algoritmo de Lloyd: pasos de asignación y actualización de centroides
- Convergencia: demostración de convergencia finita a mínimo local
- Inicialización con K-means++
- Elección de K: método del codo y coeficiente de silueta
- Variantes: Mini-batch K-means, Online K-means, Kernel K-means, K-medoids, K-medians
- Aplicaciones: segmentación de clientes, compresión de imágenes, detección de anomalías
- Limitaciones y casos de uso

**Herramientas:** `beamer` (tema metropolis), `tikz`, `pgfplots`

---

### `PCA.tex` — Análisis por Componentes Principales
Documento de artículo (~1000 líneas) con tratamiento teórico avanzado de PCA, escrito por César Galindo.

**Temas:**
- Formulación variacional: maximización de varianza y minimización de error de reconstrucción
- Teorema espectral y descomposición en valores singulares (SVD)
- PCA probabilístico (PPCA) y conexión con modelos latentes gaussianos
- Kernel PCA: extensión no lineal mediante el truco del kernel
- PCA disperso (Sparse PCA): transiciones de fase y umbralizado suave
- PCA robusto (RPCA): descomposición bajo rango + disperso, algoritmo SVT (ADMM)
- Aplicaciones en IA: visualización de embeddings, detección de anomalías (estadístico Q), aceleración de t-SNE/UMAP, conexión con autoencoders lineales

**Herramientas:** `amsmath`, `amsthm`, `geometry`, estilo IHES

---

## Compilación

```bash
# Para K.tex (presentación Beamer)
pdflatex K.tex

# Para PCA.tex (artículo)
pdflatex PCA.tex
```

Requiere una distribución LaTeX completa (TeX Live o MiKTeX) con los paquetes `beamer`, `metropolis`, `tikz`, `pgfplots`, `amsmath`, `amsthm`, `mathtools`.

---

## Referencias principales

- Lloyd, S. P. (1982). Least squares quantization in PCM. *IEEE Transactions on Information Theory*.
- Arthur & Vassilvitskii (2007). K-means++: The advantages of careful seeding. *SODA*.
- Bishop, C. M. (2006). *Pattern Recognition and Machine Learning*. Springer.
- Candès et al. (2011). Robust principal component analysis? *Journal of the ACM*.
- Tipping & Bishop (1999). Probabilistic principal component analysis. *JRSS-B*.
- Schölkopf, Smola & Müller (1998). Nonlinear component analysis as a kernel eigenvalue problem. *Neural Computation*.
