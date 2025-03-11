[[Aplicaciones de las Derivadas]]

## Monotonia -> Intervalos de crecimiento

- Una función crece si f'(x) > 0
- Una función decrece si f'(x) < 0

- Una función es constante si f'(x) = 0

- Monótonas estrictamente creciente si f'(x) > 0 $\forall x \in Domf(x)$
- Monótonas estrictamente decreciente si f'(x) < 0 $\forall x \in Domf(x)$

## Extremos relativos de una función

![[Extremos relativos de una función.png]]
- Hay un extremo relativo en los valores de x que cumplen f'(x) = 0
	- si f'(x) > 0 -> f'(x) < 0 Máximo
	- si f'(x) < 0 -> f'(x) > 0 Mínimo

### Hallar extremos relativos:
f(x) = x^2 + 1
1. puntos crítica f'(x) = 0
	- f'(x) = 2x
	- 2x = 0
	- x = 0
2. Recta real
![[Recta real.png]]
Hay un mínimo en x = 0
Decrece: (-INF, 0)
Crece: (0, INF)

### Un extremo relativo (máximo o mínimo): Debe cumplir los siguientes requisitos

- Debe provocar un cambio en la monotonía
- f'(x) = 0

### ¿Dónde estudia la monotonía?

- Puntos problemáticas del dominio
- Puntos de salto
- Puntos críticos (f'(x) = 0)
	- Solo estos son candidatos a extremos relativos

$$
\begin{aligned}
f(x) = \frac{1}{x} \text{ si } x\leq 0 \\
f(x) = x^2 + 2x - 1 \text{ si } x > 0 \\
\\
Dom(f(x)) = \mathbb{R} - \{0\} \\
A. verticales: \lim_{ x \to 0^+ }[x^2 + 2x - 1] = -1 \\
\lim_{ x \to 0^- } \frac{1}{x} = \frac{1}{0^-} = -\infty 
\exists a.verticale \\
x = 0 \\
\text{ ¿puntos críticos? } \\
f'(x) = 0 \\
f'(x) = -\frac{1}{x^2} \text{ si } x\leq 0 \\
f'(x) = 2x + 2 \text{ si } x > 0 \\
\\
f(-1) = \frac{1}{-1} < 0 \\
f(1) = 1^2 + 2 \times 1 - 1 = 2
\end{aligned}
$$
0 no es punto crítico -> Extremo

## Teorema de weierstrass

- Si f(x) es continua en [a, b]
	- Puede averiguar que -f(x) alcanza un extremo en dicho intervalo.