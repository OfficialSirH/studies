[[Derivadas]]

## Concepto de Continuidad

### Continuidad

Una función f(x) es continua en x = a si cumple:
1. $f(x)$ existe en $x = a \to a $\epsilon dom(f(x))$
2. $f(a) = \lim_{ x \to a }f(a) \to f(a) = \lim_{ x \to a^+ }f(a)$

### Discontinuidades

evitable $\to$ existe f(a) y $\lim_{ x \to a }f(x)$ pero 
$f(a) \ne \lim_{ x \to a^+ }f(x) = \lim_{ x \to a^- }f(x)$

## Derivabilidad

Si f(x) es no continua $\to$ no es derivable
aunque el contrario es falso

f(x) es derivable en x = a si
- $a \epsilon dom f(x)$
- f(x) es continua en x = a
- $f'(a) = \lim_{ h \to 0^- } \frac{f(a + h) - f(a)}{h} = \lim_{ h \to 0^+ } \frac{f(a + h) - f(a)}{h}$

### Ejemplo

$$
\begin{aligned}
f(x) = x^2 \text{ en } x = 1
\end{aligned}
$$
- $dom f(x) = \mathbb{R} \to 1 \in Dom f(x)$
- f(x) es continua en x = 1 (función polinómica)
- $f'(x) = 2x \to f'(1) = 2$

$$
\begin{aligned}
\lim_{ h \to 0^+ } \frac{(1 + h)^2 - 1}{h}
= \frac{2h + h^2}{h}
= 2 + h = 2
\end{aligned}
$$
$$
\begin{aligned}
f(x) = x^3 + 1 \\
x = 0 \\
\text{Continua en x = 0} \\
\text{Derivable en x = 0} \\
\end{aligned}
$$
