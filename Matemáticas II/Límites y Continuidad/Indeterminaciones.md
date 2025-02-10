[[Límites y Continuidad]]

## Teorema de Existencia

$$
\lim_{ x \to a^+ } f(x) = \lim_{ x \to a^- } f(x)
$$
$$
\exists \lim_{ x \to a } f(x)
$$

## Sumo/Resta

$k \pm 0 = k$
$k \pm \infty = \pm \infty$
$\infty + \infty = \infty$
$\infty - \infty = IND$

## Producto y Cociente

$$
\begin{aligned}
k*\infty &= \\
\infty \text{ si } k \gt 0 \\
-\infty \text{ si } k \lt 0 \\
\\
k*-\infty &= \\
-\infty \text{ si } k \gt 0 \\
\infty \text{ si } k \lt 0 \\
\\
0*\infty \text{ \& } \infty*0 &= IND \\
\infty*\infty &= \infty \\
\infty*-\infty &= \infty \\
\\
\frac{k}{0} &= \\
+\infty \text{ si } k \gt 0 \\
-\infty \text{ si } k \lt 0 \\
\\
\frac{k}{\pm \infty} &= 0 \\
\\
\frac{0}{\infty} &= 0 \\
\\
\frac{\pm\infty}{0} &= \pm \infty \\
\\
\frac{0}{0} &= IND \\
\\
\frac{\infty}{\infty} &= IND \\
\end{aligned}
$$

## Exponencial

$$
\begin{aligned}
a^\infty &= \infty \text{ \& } a^{-\infty} = 0 \\
\text{si } a &\neq 1 \\
\text{porque } 1^\infty &= IND \\
\\
0^0 &= IND \\
\infty^0 &= IND \\
0^\infty &= IND 
\end{aligned}
$$

## Ejemplos

$$
\lim_{ x \to 0 } \overbrace{\left( \frac{1}{x} - \frac{1}{x^2} \right)}^{\infty - \infty} = \lim_{ x \to 0 } \left( \frac{x-1}{x^2} \right) = \overbrace{\frac{0-1}{0} = \frac{-1}{0}}^{k / 0} = -\infty
$$

$$
\lim_{ x \to \infty } (x - \sqrt{ x }) = \lim_{ x \to \infty } \left[ (x - \sqrt{ x }) * \frac{x+\sqrt{ x }}{x+\sqrt{ x }} \right] = \lim_{ x \to \infty } \left[ \frac{x^2 - x}{x+\sqrt{ x }} \right] = \frac{\infty}{\infty} IND
$$
Tipo $\frac{\infty}{\infty}$
- operar (factorizar y simplificar)
- dividir entre potencia de mayor exponente
- dividir por la potencia de menor exponente
- CCI $x \to \infty : x! \gt a^x \gt x^n \gt nx \gt \sqrt[n]{ x } \gt \log_{n}x$
- L'Hopital $\frac{\infty}{\infty}, \frac{0}{0} : \lim_{ x \to a } \frac{f(x)}{g(x)} = \lim_{ x \to a } \frac{f'(x)}{g'(x)}$
### Dividir
$$
\frac{\infty}{\infty}IND = \lim_{ x \to \infty } \frac{\left( \frac{x^2}{x^2} - \frac{x}{x^2} \right)}{\frac{x}{x^2}+\sqrt{ \frac{x}{x^4} }} = \frac{\left( 1 - \frac{1}{\infty} \right)}{\frac{1}{\infty} + \sqrt{ \frac{1}{\infty} }} = \frac{1 - 0}{0 + 0} = \frac{1}{0} = \infty]
$$
### CCI
$$
\frac{\infty}{\infty}IND = \lim_{ x \to \infty } \frac{x^2}{x} = \lim_{ x \to \infty } x = \infty  
$$


$$
\lim_{ x \to 2 } \frac{x-2}{-x^2+4} = \frac{0}{0} = \lim_{ x \to 2 } \frac{-2}{-2x} = \frac{1}{2} 
$$

Tipo $1^\infty$


$$
\lim_{ x \to a }f(x)^{g(x)} = 1^\infty IND = e^{\lim_{ x \to a } g(x) * (f(x) - 1) }
$$
$$
\lim_{ x \to 0 } (x+1)^{1/x} = (0+1)^{1/0} = 1^\infty IND = e^{\lim_{ x \to 0 } 1/x * (x + 1 - 1)} = e^{\lim_{ x \to 0 } 1/x} = e^1 = e]
$$
$e \approx 2'77$
