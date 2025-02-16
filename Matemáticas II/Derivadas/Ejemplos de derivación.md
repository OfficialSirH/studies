[[Derivadas]]

$$
\begin{aligned}
f(x) = 5 \rightarrow f(x) = k \\
f'(x) = 0 \rightarrow f'(x) = 0
\end{aligned}
$$

$$
\begin{aligned}
f(x) = 2x^2 \rightarrow f(x) = kx^n \\
f'(x) = 2 \times 2 \times x^{2-1} = 4x \rightarrow f'(x) = k\times nx^{n-1} \\
\\
f(x) = 3x^2 + x \\
f'(x) = 3\times 2 \times x^{2-1} + 1 \times x^{1-1} = 6x + 1 \\
\\
f(x) = 5x^{-3} = \frac{5}{x^3} \rightarrow a^{-n} = \frac{1}{a^n} \\
f'(x) = 5 \times -3 \times x^{-3-1} = 15x^{-4} = \frac{-15}{x^4} \\
\\
\sqrt[n]{ a^m } = a^{m/n} \\
f(x) = \sqrt[3]{ 2x^5 } = (2x^5)^{1/3} \\
f(x) = 2^{1/3} \times (x^5)^{1/3} = \sqrt[3]{ 2 } \times x^{5/3} \\
f'(x) = \sqrt[3]{ 2 } \times \frac{5}{3}x^{5/3 - 1} = \sqrt[3]{ 2 } \times \frac{5}{3}x^{2/3} \\
= \frac{5\sqrt[3]{ 2 }}{3} \times \sqrt[3]{ x^2 }
\end{aligned}
$$
$$
\begin{aligned}
f(x) = ka^x \rightarrow f'(x) = k \times a^x \times \ln(a) \\
f(x) = 3 \times 4^x \rightarrow f'(x) 3 \times 4^x \times \ln(4) \\
f(x) = e^x \rightarrow f'(x) = e^x \\
\ln e = 1 \\
\end{aligned}
$$
$$
\begin{aligned}
\ln = \log_{e} \\
f(x) = \ln(x) \rightarrow f'(x) = \frac{1}{x} \\
f(x) = \log_{a}(x) \rightarrow f'(x) = \frac{1}{x} \times \frac{1}{\ln a} \\
\frac{1}{\ln e} = \frac{1}{1}
\end{aligned}
$$
$$
\begin{aligned}
f(x) = \cos(x) \rightarrow f'(x) = -\sin(x) \\
f(x) = \sin(x) \rightarrow f'(x) = \cos(x) \\
f(x) = \tan(x) = \frac{\sin(x)}{\cos(x)} \rightarrow f'(x) = \frac{1}{\cos^2x} = 1 + \tan^2x = \sin^2x \\
\cos(x) = \frac{1}{\sin(x)} \\
\sin(x) = \frac{1}{\cos(x)} \\
\cot(x) = \frac{1}{\tan(x)}
\end{aligned}
$$
$$
\begin{aligned}
f(x) = \arcsin(x) \rightarrow f'(x) = \frac{1}{\sqrt{ 1 - x^2 }} \\
f(x) = \arctan(x) \rightarrow f'(x) = \frac{1}{1 + x^2}
\end{aligned}
$$
## Regla de la cadena

$$
\begin{aligned}
h(x) = f(g(x)) \\
h'(x) = (f(g(x)))' = f'(g(x)) \times g'(x) \\
\\
\text{Ej: } h(x) = \cos(3x) \\
h'(x) = -\sin(3x) \times 3 \\
= -3\sin(3x) \\
\\
h(x) = \arcsin(2x^2) \\
h'(x) = \frac{1}{\sqrt{ 1 - (2x^2)^2 }} \times 4x \\
= \frac{4x}{\sqrt{ 1 - (2x^2)^2 }} \\
\\
h(x) = e^{2x^2+x} \rightarrow h'(x) = e^{2x^2+x} \times (4x^2+1) \\
\\
h(x) = (x^2 + 2x)^3 \\
h'(x) = 3(x^2 + 2x)^{3-1} \times (2x + 2) \\
= 3(x^2 + 2x)^2 \times (2x + 2) \\
\\
h(x) = \ln(x^3) \rightarrow h'(x) = \frac{1}{x^3} \times 3x^2 \\
= \frac{3}{x}
\end{aligned}
$$