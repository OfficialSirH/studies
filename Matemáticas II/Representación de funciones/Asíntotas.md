[[Representación de funciones]]

## Asíntota Vertical

$[x = a]$
- Se analizan en:
	- Puntos no pertenecientes al dominio
	- Puntos de salto de funciones a trotos
	> Puntos de estudio

Si f(x) tiene como domino $Dom f(x) = \mathbb{R} - \{x = a\}$
Tendrá asíntota vertical si:
$\lim_{ x \to a }f(x) = \pm \infty$
- $\lim_{ x \to a^+ } f(x) = nº\pm \infty$
- $\lim_{ x \to a^- } f(x) = nº\pm \infty$

### Ejemplo

$f(x) = \ln(x+1)$
$Dom f(x) = (-1, \infty)$
$\lim_{ x \to -1^- } \ln(x+1) \neq \exists$
$\lim_{ x \to -1^+ } \ln(x+1) = -\infty$

## Asíntota Horziontal

$[y = a]$
Existe asíntota horziontal en y = a para f(x) si:

$\lim_{ x \to -\infty }f(x) = a$
o
$\lim_{ x \to +\infty }f(x) = a$

### Ejemplo

$f(x) = \frac{x}{x^2+1}$
$Dom f(x) = \mathbb{R}$
$\frac{\lim_{ x \to -\infty }x}{x^2+1}= \frac{\infty}{\infty} (IND)$
$\frac{\lim_{ x \to +\infty }x}{x^2+1}= \frac{\infty}{\infty} (IND)$

## Asíntotas oblicuas

$[y = mx+n]$
No hay si existen A. horizontales

Calcula:
$m = \frac{\lim_{ x \to \pm\infty }f(x)}{x}$
$n = \lim_{ x \to \pm\infty }[f(x) - mx]$

### Ejemplo

$f(x) = \frac{x^3}{x^2+1}$
$Dom f(x) = \mathbb{R} \to /\exists A.V$
$\lim_{ x \to \pm\infty }f(x) = \pm \infty \to /\exists A.H$
