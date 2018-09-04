# Espacios vectoriales

##Ecuaciones lineales
En este sección estudiaremos las ecuaciones lineales como motivación para el estudio de los conceptos iniciales de matrices. Además estudiaremos las operaciones básicas de suma y producto por un escalar así como el producto de matrices. Luego estudiaremos el concepto de invertibilidad de matrices, para ello definiremos las operaciones elementales por filas. 

Sea $\mathbb{F}$ un cuerpo. Supongamos que queremos hallar $n$ escalares (elementos del cuerpo $\mathbb{F}$) $x_{1},x_{2}, \cdots, x_{n}$ que satisfagan las condiciones:
\begin{equation}
	\begin{array}{ccccc}
		A_{11}x_{1}+&A_{12}x_{2}+&\cdots +&A_{1n}x_{n}=&b_{1}\\
		A_{21}x_{1}+&A_{22}x_{2}+&\cdots +&A_{2n}x_{n}=&b_{2}\\
		\vdots& &\ddots& \vdots& \vdots	\\
		A_{m1}x_{1}+&A_{m2}x_{2}+&\cdots +&A_{mn}x_{n}=&b_{m}
	\end{array}
	(\#eq:sistemalineal)
\end{equation}
donde $b_{i}\in\mathbb{F}$  así como $A_{ij}\in \mathbb{F}$ para todo $1\leq i\leq m$ y $1\leq j\leq n$. Al conjunto de ecuaciones expresadas en \@ref(eq=sistemalineal) se le llama *sistema de $m$ ecuaciones lineales con $n$ incognitas*. A los elementos $A_{ij}$ se les conoce como *coeficientes* del sistema de ecuaciones, siendo espesíficamente el coeficiente de la $i$-ésima fila y la $j$-ésima columna. Una *solución* del sistema es una $n$-tupla $(x_{1},x_{2},\cdots,x_{n})$ (un vector del espacio $\mathbb{R}^{n}$) que satisfaga las ecuaciones \@ref(eq=sistemalineal). Cuando $b_{1}=b_{2}=\cdots b_{m}=0$ se dice que el *sistema de ecuaciones es homogéneo* (cada ecuación es homogénea).

Una forma de resolver un sistema de ecuaciones es con la técnica de eliminación de incógnitas, el cual consiste en multiplicar algunas de las ecuaciones por un escalar de forma que al sumar las ecuaciones se elimine algunas de las incógnitas. Veamos esto con un ejemplo.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-1"><strong>(\#exm:unnamed-chunk-1) </strong></span>	Dado el siguiente sistema homogéneo, sobre el cuerpo de los números reales $\mathbb{R}$
	\begin{eqnarray*}
	\begin{array}{cc}
		x_{1}-4x_{2}+x_{3}&=0\\
		3x_{1}-11x_{2}+2x_{3}&=0
	\end{array}
	\end{eqnarray*}
	Multiplicamos la primera ecuación por el escalar $-3$ y la sumamos a la segunda ecuación, para obtener $-3(x_{1}-4x_{2}+x_{3})+(3x_{1}-11x_{2}+2x_{3})=0$, lo que queda como la siguiente $-3x_{1}+12x_{2}-3x_{3}+3x_{1}-11x_{2}+2x_{3}=0$, sumando términos independientes, obtenemos $x_{2}-x_{3}=0$ por lo tanto $x_{2}=x_{3}$. Ahora, multiplicando por $-2$ la primera ecuación y sumándola a la segunda, se obtiene $-2(x_{1}-4x_{2}+x_{3})+(3x_{1}-11x_{2}+2x_{3})=0$ lo que equivale a $-2x_{1}+8x_{2}-2x_{3}+3x_{1}-11x_{2}+2x_{3}=0$ al sumar los términos semejantes se obtiene que $x_{1}-3x_{2}=0$ por lo que $x_{1}=3x_{2}$. Luego cualquier vector de la forma $(3\lambda,\lambda,\lambda)$ con $\lambda\in\mathbb{R}$ es una solución del sistema homogéneo.
</div>\EndKnitrBlock{example}

En general, este método para resolver un sistema de ecuaciones como \@ref(eq=sistemalineal) consiste en multiplicar por $m$ escalares $c_{1}, c_{2},\cdots ,c_{m}$ cada ecuación del sistema y sumarlas entre si para obtener una *combinación lineal* de las ecuaciones:
\begin{equation}
\begin{array}{ccccccc}
&c_{1}(A_{11}x_{1}&+&\cdots &+&A_{1n}x_{n})=&c_{1}b_{1}\\
&c_{2}(A_{21}x_{1}&+&\cdots &+&A_{2n}x_{n})=&c_{2}b_{2}\\
+&\vdots& &\ddots& &\vdots& \vdots	\\
&c_{m}(A_{m1}x_{1}&+&\cdots &+&A_{mn}x_{n})=&c_{m}b_{m}\\
\cline{2-7}
&(c_{1}A_{11}+\cdots+c_{m}A_{m1})x_{1}&+&\cdots&+&(c_{1}A_{1n}+\cdots +c_{m}A_{mn})x_{n}&=c_{1}b_{1}+\cdots+c_{m}b_{m}
\end{array}
\end{equation}
