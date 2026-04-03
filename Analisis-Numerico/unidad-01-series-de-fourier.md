---
fecha: 2026-03-29 2026-03-29
materia: Analisis-Numerico
unidad: "1"
tema: Series de Fourier, serie trigonometrica de fourier
tags: []
---
# Propiedades generales
- Las series de fourier son mas generales que las series de Taylor
- Desarrollar una funcion en una serie de fourier **implica** escribir a dicha funcion como **combinacion lienal** de las funciones de una **base ortonormal**

Se dice que una funcion es seccionalmente continua
$Sea\ f: [a;b]\to \mathbb{R}$
$$
f\text{ es seccionalmente continua} \iff \text{ tiene un numero finitio de saltos finitos}
$$
- Toda funcion $f$ seccionalmente continua en $[a;b]$ es integrable en $[a;b]$
## Espacio vectorial de funciones seccionalmente continuas
$$
F=\{f/f:[a;b]\to \mathbb{R} \land f\text{ es seccionalmente continua en } [a;b]\}
$$
$B=\{f_{1}(x),f_{2}(x),f_{3}(x),\dots,f_{n}(x),\dots\}$ es base de $F$ si y solo si:
$\forall f \in F:f(x)=k_{1}f_{1}(x)+k_{2}f_{2}(x)+\dots+k_{n}f_{n}(x)+\dots$
$$
\forall f \in F: f(x)=\sum_{n=1}^\infty k_{n}f_{n}(x)
$$
Para el caso de la serie trigonometrica de fourier la base debe ser **ortonormal**
Sea $B=\{v_{1},v_{2},\dots ,v_{n}\}$
$$
B\text{ es ortogonal }\iff \forall v_{i},v_{j}\in B:i\neq j\implies<v_{i}\cdot v_{j}> =0
$$
$$
B\text{ es ortonormal }\iff \forall v_{i},v_{j}\in B:i\neq j\implies<v_{i}\cdot v_{j}> =0 \land ||v_{i}||=1
$$
## Producto interior y norma en el espacio vectorial $F$

$$
<f\cdot g> =\int_{a}^b f(x)\cdot g(x) dx
$$
$$
||f|| =\sqrt{ <f\cdot f> }=\sqrt{ \int_{a}^b f^{2}(x)dx }
$$
