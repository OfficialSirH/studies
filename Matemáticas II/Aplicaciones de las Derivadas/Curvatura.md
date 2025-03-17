[[Aplicaciones de las Derivadas]]

## Curvatura, 

### Puntos de inflexión

- cumplen:
	- Hay cambio de curvatura
	- f''(x) = 0 y f'''(x) $\neq$ 0

### ¿Dónde estudiamos la curvatura?

- Puntos problemáticas del dominio
- Puntos donde $\exists$ asintotas verticales
- puntos con f''(x) = 0

### Ejemplo

$$
\begin{aligned}
f(x) = x^2 \text{ si } x < 1 \\
f(x) = \ln(x^2+1) \text{ si } x \geq 1 \\
\\
Dom f(x) = \mathbb{R} - \{x=1\} [x=1] \\
\\
f'(x) = 2x \text{ si } x < 1 \\
f'(x) = \frac{2x}{x^2+1} \text{ si } x \geq 1 \\
\\
f''(x) = 2 \text{ si } x < 1 \\
f''(x) = \frac{2(x^2+1) - 2x \times 2x}{x^2+1} \text{ si } x \geq 1 \\
f''(x) -\frac{2x^2+2}{x^2 + 1} \text{ si } x \geq 1 \\
\\
2 \text{ si } x < 1 \to 2 = 0 \to \text{ no punto de inflexión en x} \\
-\frac{2x^2+2}{x^2+1} \text{ si } x \geq 1 \to \frac{-2x^2+2}{x^2+1} \neq 0 \\
-2x^2 + 2 = 0 \\
2x^2 = 2 \\
x^2 = 1 \\
x = \pm1
\end{aligned}
$$

$$
\begin{aligned}
f(x) = x^3 \\
dom f(x) = \mathbb{R} \\
f''(x) = 6x \to 6x = 0 \to x = 0 \\
f'''(x) = 6 \neq 0 \\
\exists \text{ punto de inflexión en x = 0}
\end{aligned}
$$