[[Derivadas]]

$$
\begin{aligned}
m = \frac{f(b)-f(a)}{b - a} = \frac{\Delta f(x)}{\Delta x} \\
\end{aligned}
$$$$
\begin{aligned}
\lim_{ \Delta x \to 0 } \frac{\Delta f(x)}{\Delta x} = \frac{df(x)}{dx} = f'(x) \\
\\
\lim_{ \Delta x \to 0 } \frac{\Delta f(x)}{\Delta x} = \lim_{ (b-a) \to 0 } \frac{f(b) - f(a)}{b - a} = \lim_{ h \to 0 } \frac{f(a + h) - f(a)}{a + h - a} \\
= \lim_{ h \to 0 } \frac{f(a + h) - f(a)}{h} = f'(a)  
\end{aligned}
$$
$$
\begin{aligned}
\lim_{ x \to a }  \frac{f(x) - f(a)}{x - a}
\end{aligned}
$$
Recta Tangente
$$
\begin{aligned}
y &= mx + n \\
y - f(x_{0}) &= \underbrace{f'(x_{0})}_{\text{ m }}(x-x_{0})
\end{aligned}
$$
$$
\begin{aligned}
f(x) = 2x^2 + 1 \\
\text{ hallar la recta tangente de f(x) en el punto x = 2} \\
y - f(x_{0}) = f'(x_{0})(x - \underbrace{x_{0}}_{2}) \\
f(x_{0}) = 2 \times 2^2 + 1 = 9 = f(2) \\
f'(2) = \lim_{ h \to 0 } \frac{f(a + h) - f(a)}{h} \\
= \lim_{ h \to 0 } \frac{f(2+h) - f(2)}{h} \\
= \lim_{ h \to 0 } \frac{2(2 + h)^2 + 1 - 9}{h} \\
= \lim_{ h \to 0 } \frac{2 (4 + 4h + h^2) + 1 - 9}{h} \\
= \lim_{ h \to 0 } \frac{8h + 2h^2}{h} = \frac{0}{0} \\
\lim_{ h \to 0 } \frac{(h + 4)2h}{h} \\
= \lim_{ h \to 0 } (h+4)2 = (0 + 4)2 = 8 \\
\\
f'(2) = 8 \\
x_{0} = 2 \\
f(2) = 9 \\
y - f(x_{0}) = f'(x_{0})(x - x_{0}) \\
y - f(2) = f'(2)(x - 2) \\
y - 9 = 8(x - 2) \\
y = 8x - 7
\end{aligned}
$$
