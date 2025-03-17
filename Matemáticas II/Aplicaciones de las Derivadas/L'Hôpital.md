[[Aplicaciones de las Derivadas]]

## Definición regla de L'Hôpital

- $\frac{H(x)}{} = \frac{f(x)}{g(x)}$
- $g'(x) \neq 0$
- Indeterminación $\frac{0}{0} o\frac{\infty}{\infty}$
$$
\begin{aligned}
\lim_{ x \to a } \frac{f(x)}{g(x)} = \frac{f(x)}{g(x)} = \frac{0}{0} \frac{\infty}{\infty} \\
= \lim_{ x \to a } \frac{f'(x)}{g'(x)}
\end{aligned}
$$

## Ejemplos

$$
\begin{aligned}
\lim_{ x \to 0 } \frac{\sin x}{x} = \frac{0}{0} \\
\lim_{ x \to 0 } \frac{\cos x}{1} = \cos 0 = 1
\end{aligned}
$$

$$
\begin{aligned}
\lim_{ x \to \infty } \frac{\ln x}{x} = \frac{\infty}{\infty} \\
\lim_{ x \to \infty } \frac{\frac{1}{x}}{1} = \lim_{ x \to \infty } \frac{1}{x} = \frac{1}{\infty} = 0
\end{aligned}
$$

$$
\begin{aligned}
\lim_{ x \to a } f(x)^{g(x)} = e^{\lim_{ x \to a } \frac{\ln f(x)}{1/g(x)} } \\
\lim_{ x \to 0 } x^x = 0^0 = e^{\lim_{ x \to 0 } \frac{\ln x}{1/x} } = \frac{\infty}{\infty} = e^{\lim_{ x \to 0 } \frac{1/x}{-1/x^2} } \\
e^{\lim_{ x \to 0 } \frac{-x^2/x}{-1/x^2} } = e^{\lim_{ x \to 0 } -x} = e^0 = 1
\end{aligned}
$$

$$
\begin{align}
\lim_{ x \to a } f(x) \times g(x) = \\
\lim_{ x \to a } \frac{f(x)}{\frac{1}{g(x)}} = \frac{\infty}{\infty} \\
\lim_{ x \to a } \frac{g(x)}{\frac{1}{f(x)}} = \frac{0}{0} 
\end{align}
$$

$$
\begin{align}
e^{-x} \times x = 0 \times \infty = \\
\lim_{ x \to \infty } \frac{e^{-x}}{\frac{1}{x}} \\
\lim_{ x \to \infty } \frac{x}{\frac{1}{e^{-x}}}  \\
 \\
\lim_{ x \to \infty } \frac{-e^{-x}}{-\frac{1}{x^2}} \\
\lim_{ x \to \infty } \frac{-x}{-\frac{1}{e^{-2x}}}
\end{align}
$$