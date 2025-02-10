[[Límites y Continuidad]]

$A \equiv \{(x,f(x))\} = \{(a,f(a)),(b,f(b)),(c,f(c)),...\} _{a \neq b \neq c \neq ...}$
$\downarrow$
$y = f(x)$

```functionplot
---
title: f(x) = -x^2 + 1
bounds: [-5, 5, -5, 5]
disableZoom: true
grid: true
---
f(x)=-x^2+1
```


# Dominio

Polinómica $f(x) = P(x)$
$Dom(f(x)) = \mathbb{R}$
```functionplot
---
bounds: [-10, 10, -10, 10]
disableZoom: true
grid: true
---
f(x)=x^3+x
```
$f(x) = x^3 + x \Rightarrow Dom(f(x)) = \mathbb{R}$


Racional $f(x) = \frac{P(x)}{Q(x)}$
$Dom(f(x)) = \mathbb{R} - \{x \in \mathbb{R}: Q(x) = 0\}$
```functionplot
---
bounds: [-10, 10, -10, 10]
disableZoom: true
grid: true
---
f(x)=1/x
```
$f(x)=1/x \Rightarrow Dom(f(x)) = \mathbb{R} - \{x = 0\}$


Exponencial $f(x) = a^{P(x)}$
$Dom(f(x)) = \{x \in \mathbb{R}: P(x) \ge 0\}$
```functionplot
---
bounds: [-10, 10, -10, 10]
disableZoom: true
grid: true
---
f(x)=3^x
```
$f(x) = x^3 \Rightarrow Dom(f(x)) = \mathbb{R}$


Logarítmica $f(x) = \log(P(x))$
$Dom(f(x)) = \{x \in \mathbb{R}: P(x) \gt 0\}$
```functionplot
---
bounds: [-10, 10, -10, 10]
disableZoom: true
grid: true
---
f(x)=log(x+1)
```
$f(x) = \ln(x + 1) \Rightarrow Dom(f(x)) = (-1,\infty)$


Racional $f(x) = \sqrt{P(x)}$
$Dom(f(x)) = \mathbb{R}$
```functionplot
---
bounds: [-10, 10, -10, 10]
disableZoom: true
grid: true
---
f(x)=sqrt(x+1)
```
$f(x) = \sqrt{x + 1} \Rightarrow Dom(f(x)) = [-1, \infty)$


Combinación de varios tipos:
$Dom(f(x))$ se obtiene con el conjunto de restricciones
```functionplot
---
bounds: [-10, 10, -10, 10]
disableZoom: true
grid: true
---
f(x)=div(sqrt(x+1),x+1)
```
$$f(x) = \frac{\sqrt{x + 1}}{x + 1} \Rightarrow Dom(f(x)) = (-1, \infty)$$


Cortes con los ejes
$0X: (x,y) = (x_0,0)$ $f(x_0) = 0$
$-x_0^2 + 1 = 0 \Rightarrow x_0 = \pm1$
$(x,y) = (-1,0)$ $\&$ $(1,0)$

$0Y: (x,y) = (0,y_0)$ $f(0) = y_0$
$-0^2 + 1 = y_0 \Rightarrow y_0 = +1$
$(x,y) = (0,1)$


## Ejemplos:

$$
\begin{aligned}
\lim_{x \rightarrow a}f(x) &= f(a) \\
f(x) &= x^2 + 1 \\
\lim_{x \rightarrow \underbrace{0}_{\text{a}}} x^2 + 1 &= 0^2 + 1 = \underbrace{1}_{\text{f(a)}}
\end{aligned}
$$
$$
\begin{aligned}
a^- &\approx -0.001 = 0^- \\
a &= 0 \\
a^+ &\approx 0.001 = 0^+
\end{aligned}
$$
Límite existes:
$$\lim_{x \rightarrow a^+} f(x) = \lim_{x \rightarrow a^-} f(x)$$
