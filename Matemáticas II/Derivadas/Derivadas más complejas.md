[[Derivadas]]

## Repaso Regla de La Cadena

$$
\begin{aligned}
h(x) &= f(g(x)) \\
h'(x) &= f'(g(x)) \times g'(x)
\end{aligned}
$$

$$
\begin{aligned}
h(x) = \overbrace{\arctan(\underbrace{5x^2}_{g(x)})}^{f(g(x))}
\rightarrow h'(x) = \frac{1}{1 + (5x^2)^2} \times 10x
= \frac{10x}{1 + (5x^2)^2}
\end{aligned}
$$

$$
\begin{aligned}
h(x) = \ln(3x^2 + x) \\
h'(x) = \frac{1}{3x^2 + x} \times (6x + 1) = \frac{6x + 1}{3x^2 + x}
\end{aligned}
$$

## Derivada de un Cociente

$$
\begin{aligned}
h(x) = \frac{f(x)}{g(x)} \\
h'(x) = \frac{f'(x) \times g(x) - f(x) \times g'(x)}{(g(x))^2}
\end{aligned}
$$

$$
\begin{aligned}
h(x) = \frac{3x^2 + 1}{(x^3 - x)} \\
h'(x) = \frac{6x(x^3 - x) - (3x^2 + 1) \times (3x^2 - 1)}{(x^3 - x)^2} \\
h'(x) = \frac{6x^4 - 6x^2 - (9x^4 - 1)}{(x^3 - x)^2} \\
h'(x) = \frac{6x^4 - 6x^2 - 9x^4 + 1}{(x^3 - x)^2}
\end{aligned}
$$

## Derivada de un Producto

$$
\begin{aligned}
h(x) = f(x) \times g(x) \\
h'(x) = f'(x) \times g(x) + f(x) \times g'(x)
\end{aligned}
$$

$$
\begin{aligned}
h(x) = x^2e^{-x} \\
h'(x) = 2x \times e^{-x} + x^2 \times e^{-x} \times (-1) \\
= 2xe^{-x} - x^2e^{-x} \\
= (2 - x)
\end{aligned}
$$

## Propiedad: Suma o Resta

$$
\begin{aligned}
h(x) = f(x) \pm g(x) \to h'(x) = f'(x) \pm g'(x) 
\end{aligned}
$$

$$
\begin{aligned}
h(x) = 5\underbrace{(\underbrace{x^3 + 1}_{g(x)})^2}_{f(g(x))} \to h'(x) = 5 \times 2(x^3 + 1) \times 3x^2
\end{aligned}
$$

$$
\begin{aligned}
h(x) = \frac{5}{x^2 + 1} = 5(x^2 + 1)^{-1} \\
h'(x) = 5 \times (-1) (x^2 + 1)^{-2} \times 2x
\end{aligned}
$$
