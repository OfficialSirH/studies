[[Representación de funciones]]

## Ejemplo 1

Se considera una ventana rectangular en la que el lado superior se ha sustituido por un triángulo equilátero. Sabiendo que el perímetro de la ventana es 6,6 m, hallar sus dimensiones para que la superficie sea máxima.

$$
\begin{align}
S(x,y) = S_{R} + S_{T} \\
S_{R} = x \times y \\
S_{T} = \frac{x \times h}{2} \\
 \\
x^2 = h^2 \times \left( \frac{x}{2} \right)^2 \\
h = \sqrt{ x^2 - \frac{x^2}{4} } = \frac{x}{2}\sqrt{ 3 } \\
 \\
S_{T} = \frac{x}{2} \times \frac{x}{2}\sqrt{ 3 } = \frac{x^2\sqrt{ 3 }}{4} \\
S(x,y) = x \times y + \frac{x^2\sqrt{ 3 }}{4} \\
 \\
P(x,y) = 3 \times x + 2y = 6'6m \\
y = 3'3 - \frac{3}{2}x \\
 \\
S(x) = x\left( 3'3 - \frac{3}{2}x \right) + \frac{x^2\sqrt{ 3 }}{4} \\
 = 3'3x - \frac{3}{2}x^2 + \frac{x^2\sqrt{ 3 }}{4} \\
 = x^2\left( \frac{\sqrt{ 3 }}{4} - \frac{3}{2} \right) + 3'3x \\
 \\
S'(x) = 2x\left( \frac{\sqrt{ 3 }}{4} - \frac{3}{2} \right) + 3'3 \\
= x\left( \frac{\sqrt{ 3 }}{2} - 3 \right) + 3'3 \\
S'(x) = 0 \to x\left( \frac{\sqrt{ 3 }}{2} - 3 \right) + 3'3 = 0 \\
x \approx 1'55 \\
 \\
y = 3'3 - \frac{3}{2}x \to  \\
3'3 - \frac{3}{2} \times 1'55 \approx 0'975
\end{align}
$$

## Ejemplo 2

El propietario de un edificio tiene alquilados los 40 pisos del mismo a un precio de 600 euros cada uno. Por cada 60 euros que el propietario aumenta el precio observa que pierde un inquilino. ¿a qué precio le convienen alquilar los pisos para obtener la mayor ganancia posible?(Ayuda: llamar x = nº de 60 euros que aumenta o lo que es lo mismo el nº inquilinos perdidos.)

$$
\begin{align}
G(x) = (600 + 60x) \times (40 - x) \\
= 60 \times 40 = 2400 \text{ 0 < x < 40} \\
 \\
G'(x) = 60(40 - x) + (600 + 60x) \times (-1) \\
= 2400 -60x - 600 - 60x \\
= 1800 - 120x = 0 \\
x = \frac{1800}{120} = \frac{180}{12}  \\ = \frac{9 \times 4 \times 5}{4 \times 3} = \frac{3 \times 5}{1} = 15 \\
 \\
600 + 15 \times 60 = 600 + 900 = 1500 \text{ euros}
\end{align}
$$