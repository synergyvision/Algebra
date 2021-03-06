# Espacios vectoriales
En este capítulo estudiaremos los espacios vectoriales, un concepto abstrato de una estructura cerrada bajo combinaciones lineales. Veremos que las matrices son objetos muy útiles para trabajar en espacios vectoriales. Por esta razón estudiaremos algunos aspectos básicos de estos objetos. Como motivación para el estudio de las matrices iniciaremos el capítulo estudiando las ecuaciones lineales y poco a poco iremos acercándonos al estudio de los espacios vectoriales.

## Ecuaciones lineales
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
donde $b_{i}\in\mathbb{F}$  así como $A_{ij}\in \mathbb{F}$ para todo $1\leq i\leq m$ y $1\leq j\leq n$. Al conjunto de ecuaciones expresadas en \@ref(eq:sistemalineal) se le llama *sistema de $m$ ecuaciones lineales con $n$ incognitas*. A los elementos $A_{ij}$ se les conoce como *coeficientes* del sistema de ecuaciones, siendo específicamente el coeficiente de la $i$-ésima fila y la $j$-ésima columna. Una *solución* del sistema es una $n$-tupla $(x_{1},x_{2},\cdots,x_{n})$ (un vector del espacio $\mathbb{R}^{n}$) que satisfaga las ecuaciones \@ref(eq:sistemalineal). Cuando $b_{1}=b_{2}=\cdots b_{m}=0$ se dice que el *sistema de ecuaciones es homogéneo* (cada ecuación es homogénea).

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

En general, este método para resolver un sistema de ecuaciones como \@ref(eq:sistemalineal) consiste en multiplicar por $m$ escalares $c_{1}, c_{2},\cdots ,c_{m}$ cada ecuación del sistema y sumarlas entre si para obtener una *combinación lineal* de las ecuaciones:

\begin{equation}
\begin{array}{ccccccc}
&c_{1}(A_{11}x_{1}&+&\cdots &+&A_{1n}x_{n})=&c_{1}b_{1}\\
&c_{2}(A_{21}x_{1}&+&\cdots &+&A_{2n}x_{n})=&c_{2}b_{2}\\
+&\vdots& &\ddots& &\vdots& \vdots	\\
&c_{m}(A_{m1}x_{1}&+&\cdots &+&A_{mn}x_{n})=&c_{m}b_{m}\\
&(c_{1}A_{11}+\cdots+c_{m}A_{m1})x_{1}&+&\cdots&+&(c_{1}A_{1n}+\cdots +c_{m}A_{mn})x_{n}&=c_{1}b_{1}+\cdots+c_{m}b_{m}
\end{array}
\end{equation}

Es claro que cualquier solución del sistema \@ref(eq:sistemalineal) es solución de la combinación lineal antes descrita.
Ahora bien, si formamos un sistema de $k$ ecuaciones lineales en las que cada una de ellas es una combinación lineal de las $m$ ecuaciones del sistema original, como sigue:
\begin{equation}
\begin{array}{ccccc}
B_{11}x_{1}+&B_{12}x_{2}+&\cdots +&B_{1n}x_{n}=&d_{1}\\
B_{21}x_{1}+&B_{22}x_{2}+&\cdots +&B_{2n}x_{n}=&d_{2}\\
\vdots& &\ddots& \vdots& \vdots	\\
B_{k1}x_{1}+&B_{k2}x_{2}+&\cdots +&B_{kn}x_{n}=&d_{k}
\end{array}
\end{equation}(\#eq:sistema2)

se tiene que $(x_{1},x_{2},\cdots, x_{n})$ es solución de \@ref(eq:sistema2) si lo es del sistema \@ref(eq:sistemalineal). Lo contrario no es necesariamente cierto, sin embargo si las ecuaciones de \@ref(eq:sistemalineal) son combinación lineal de las ecuaciones \@ref(eq:sistema2) entonces podemos estar seguros que toda solución del sistema \@ref(eq:sistema2) es también solución de \@ref(eq:sistemalineal). En este caso diremos que *son sistemas de ecuaciones equivalentes*. Y la observación podemos señalarla así:

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-2"><strong>(\#thm:unnamed-chunk-2) </strong></span>	Sistemas de ecuaciones lineales equivalentes tienen exactamente las mismas soluciones.</div>\EndKnitrBlock{theorem}

Lo anterior nos permite buscar las soluciones de cualquier sistema de ecuaciones lineales, buscando un sistema equivalente que sea mas fácil de resolver (por excelencia, trivial). Este método lo explicaremos en la siguiente sección.

## Matrices

En la sección anterior vimos que cuando realizamos combinaciones lineales de ecuaciones lineales, lo que importa son los coeficientes de las ecuaciones originales, siendo las incógnitas prescindibles. Esto nos permite trabajar directamente con los coeficientes para hallar un nuevo sistema lineal equivalente mas sencillo. Por esta razón arreglaremos tales coeficientes en forma rectángular para trabajar con ellos de forma directa. Estos objetos se llaman *matrices*. En la primera parte de esta sección se dará una definición formal y mas general de estos objetos, se definiran algunas operaciones con estos objetos. Para luego volver al problema original, la resolución de sistemas de ecuaciones lineales.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-3"><strong>(\#def:unnamed-chunk-3) </strong></span>Para enteros positivos $m$ y $n$, *una matriz $m\times n$ sobre el cuerpo $\mathbb{F}$* es una función $A$ del conjunto de los pares $(i,j)\in\{1,2,\cdots m\}\times\{1,2,\cdots n\}$ en el cuerpo $\mathbb{F}$. El *orden de la matriz $A$* es $m\times n$. Los *elementos de la matriz $A$* son los escalares $A(i,j)=a_{ij}$. Suele representarse como un arreglo rectángular de $m$ filas y $n$ columnas, donde el elemento $a_{ij}$ ocupa el puesto en la fila $i$ y la columna $j$ del arreglo, como sigue 

\begin{equation*}
		\left[ \begin{array}{cccc}
		a_{11}&a_{12}&\cdots &a_{1n}\\
		a_{21}&a_{22}&\cdots &a_{2n}\\
		\vdots& \ddots& \vdots& \vdots\\
		a_{m1}&a_{m2}&\cdots &a_{mn}
		\end{array}\right] 
\end{equation*}

La *$i$-ésima fila de la matriz $A$* es el arreglo $A_{i*}=[a_{i1}\; a_{i2}\;\cdots\; a_{in}]$ (puede entenderse como un vector de $\mathbb{R}^{n}$) y la \textit{$j$-ésima columna de la matriz $A$} es el arreglo $A_{*j}=\left[ \begin{array}{c}a_{1j}\\ 
	a_{2j}\\
	\vdots\\
	a_{mj}
	\end{array}\right]$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-4"><strong>(\#def:unnamed-chunk-4) </strong></span>Dadas las matrices $A$ y $B$ de orden $n\times m$, sobre el cuerpo $\mathbb{F}$, *la suma de las matrices $A$ y $B$*, es la matriz $A+B$ formada por los elementos $(a+b)_{ij}=a_{ij}+b_{ij}$ (la función suma $(A+B)(i,j)=A(i,j)+B(i,j)$). También se puede expresar como:

\begin{equation*}
		\left[ \begin{array}{cccc}
			a_{11} & a_{12} & \cdots & a_{1n}\\
			a_{21} & a_{22} & \cdots & a_{2n}\\
			\vdots & \vdots & \ddots & \vdots\\
			a_{m1} & a_{m2} & \cdots & a_{mn}\\
		\end{array}\right]+
		\left[ \begin{array}{cccc}
		b_{11} & b_{12} & \cdots & b_{1n}\\
		b_{21} & b_{22} & \cdots & b_{2n}\\
		\vdots & \vdots & \ddots & \vdots\\
		b_{m1} & b_{m2} & \cdots & b_{mn}\\
		\end{array}\right]=
		\left[ \begin{array}{cccc}
		a_{11} + b_{11}& a_{12} + b_{12}& \cdots & a_{1n}+ b_{1n}\\
		a_{21} + b_{21} & a_{22} + b_{22} & \cdots & a_{2n} + b_{2n}\\
		\vdots & \vdots & \ddots & \vdots\\
		a_{m1} + b_{m1} & a_{m2} + b_{m2} & \cdots & a_{mn} + b_{mn}\\
		\end{array}\right]
\end{equation*}</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-5"><strong>(\#def:unnamed-chunk-5) </strong></span>Dada una matriz $A$ de orden $m\times n$ sobre el cuerpo $\mathbb{F}$ y un escalar $\lambda\in\mathbb{F}$. El *producto de la matriz $A$ por el escalar $\lambda$* es la matriz $\lambda A$, donde cada elemento $[\lambda A]_{ij}=\lambda a_{ij}$, es decir:

\begin{equation*}
		\lambda A=
		\lambda \left[ \begin{array}{cccc}
			a_{11} & a_{12} & \cdots & a_{1n}\\
			a_{21} & a_{22} & \cdots & a_{2n}\\
			\vdots & \vdots & \ddots & \vdots\\
			a_{m1} & a_{m2} & \cdots & a_{mn}\\
		\end{array}\right]=
		\left[ \begin{array}{cccc}
			\lambda a_{11}& \lambda a_{12}& \cdots & \lambda a_{1n}\\
			\lambda a_{21}& \lambda a_{22}& \cdots & \lambda a_{2n}\\
			\vdots & \vdots & \ddots & \vdots\\
			\lambda a_{m1}& \lambda a_{m2}& \cdots & \lambda a_{mn}\\
		\end{array}\right]
\end{equation*}</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-6"><strong>(\#def:unnamed-chunk-6) </strong></span>Sean $A$ y $B$ matrices de orden $m\times n$ y $n\times p$ respectivamente, el *producto $AB$* es la matriz $C$ de orden $m\times p$ cuyos elementos $ij$ son $[C]_{ij}=\sum_{k=1}^{n} A_{ik}B_{kj}$.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-7"><strong>(\#exm:unnamed-chunk-7) </strong></span>Dadas las matrices $A=\left[ \begin{array}{cc}
	1 & 0 \\
	-3 & 1
	\end{array}\right]$, $B=\left[ \begin{array}{ccc}
	5 & -1 & 2 \\
	15 & 4 & 8
	\end{array}\right]$ y $C=\left[ \begin{array}{ccc}
	-2 & 1 & 5\\
	-1 & -5 & 1
	\end{array}\right]$, entonces el producto de la matriz $C$ por el escalar $-2$ es: 

$$-2 C=\left[ \begin{array}{ccc}
	(-2)(-2) & (-2)(1) & (-2)(5)\\
	(-2)(-1) & (-2)(-5) & (-2)(1)
\end{array}\right]=\left[ \begin{array}{ccc}
	4 & -2 & -10\\
	2 & 10 & -2
\end{array}\right]$$.

El producto $AB$ es la matriz: 

$$\left[ \begin{array}{cc}
	1 & 0 \\
	-3 & 1
	\end{array}\right]\left[ \begin{array}{ccc}
	5 & -1 & 2 \\
	15 & 4 & 8
	\end{array}\right]=\left[ \begin{array}{ccc}
		5 & -1 & 2\\
		0 & 7 & 2
\end{array}\right]$$

Y la suma 

$$AB+C=\left[ \begin{array}{ccc}
		3 & 0 & 7\\
		-1 & 2 & 3
\end{array}\right]$$

Note que no podemos realizar el producto $BA$, pues no está definido. Para realizar un producto de matrices, el número de columnas del primer factor debe ser igual al número de filas del segundo factor.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-8"><strong>(\#exm:unnamed-chunk-8) </strong></span>Dadas las matrices $A=\left[ \begin{array}{cc}
	1 & -2 \\
	0 & 1 \\
	-2 & 0
	\end{array}\right]$ y $B=\left[ \begin{array}{ccc}
	1 & 0 & 1 \\
	0 & 2 & 1
	\end{array}\right]$, entonces los productos:
	$AB=\left[ \begin{array}{ccc}
	1 & -4 & -1\\
	0 & 2 & 1 \\
	-2 & 0 & -2
	\end{array}\right]$ y $BA=\left[ \begin{array}{cc}
	-1 & -2  \\
	-2 & 2  
	\end{array}\right]$.\\
	Por otro lado, si se tienen las matrices $C=\left[ \begin{array}{cc}
	1 & -2 \\
	3 & -1 \\
	\end{array}\right]$ y 
	$D=\left[ \begin{array}{cc}
	1 & -2  \\
	-1 & 2 
	\end{array}\right]$, entonces los productos:
	$CD=\left[ \begin{array}{cc}
	3 & -6 \\
	4 & -7 
	\end{array}\right]$ y $DC=\left[ \begin{array}{cc}
	-5 & 0  \\
	5 & 0  
	\end{array}\right]$
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}En los casos en que expresemos el producto $AB$ sin detallar el orden de las matrices, supondremos que el producto está bien definido. De los ejemplos anteriores podemos ver que aunque los productos $AB$ y $BA$ esten bien definidos, no necesariamente se tiene que $AB=BA$, esto es, el producto de matrices no es conmutativo.</div>\EndKnitrBlock{remark}

Ahora estudiaremos las *operaciones elementales de filas* que pueden aplicarse a una matriz, el fin de aplicar estas operaciones es obtener una matriz equivalente a la original (para obtener sistemas de ecuaciones lineales equivalentes) que corresponda a los coeficientes de un sistema lineal sencillo de resolver. 

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-10"><strong>(\#def:unnamed-chunk-10) </strong></span>Una matriz $R$ de orden $m\times n$ se llama una *matriz escalón reducida por filas* si:

(1) El primer elemento no nulo de cada fila no nula es igual a $1$, al cual llamaremos *pivote*.

(2) las columnas que contienen a un pivote (de cualquier fila), tienen el restos de sus elemento igual a cero.

(3) toda fila nula de $R$, está debajo de las filas con elementos no nulos.

(4) suponiendo que las filas no nulas de $R$ son las filas $1,2,\cdots, r$ y que el pivote de la fila $i\leq r$ está en la columna $k_{i}$, entonces $k_{1}< k_{2}< \cdots < k_{r}$.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Una matriz que cumpla las primeras dos condiciones se llama *matriz reducida por filas*.</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-12"><strong>(\#exm:unnamed-chunk-12) </strong></span>La *matriz identidad* $n\times n$ (cuadrada), definida por la función 

$$[I]_{ij}=delta_{ij}=\left\{ \begin{array}{cc}
	1 &\mbox{ si } i=j\\
	0 &\mbox{ si } i\neq j
	\end{array}\right. $$

La función $\delta_{ij}$ es conocida como la *delta de Kronecker*. Es de hacer notar que la matriz identidad se define como una matriz de cualquier orden, mientras que sea cuadrada, es decir, el número de filas es igual al número de columnas.Por ejemplo la matriz identidad de orden $4\times 4$ luce así:

$$\left[\begin{array}{cccc}
	1 & 0 & 0 & 0\\
	0 & 1 & 0 & 0\\
	0 & 0 & 1 & 0\\
	0 & 0 & 0 & 1
\end{array} \right]$$

Las matrices 

$$\left[\begin{array}{cccc}
	0 & 1 & 0 & 4\\
	0 & 0 & 1 & 5\\
	0 & 0 & 0 & 0
	\end{array} \right] \mbox{ y }
	\left[\begin{array}{ccccc}
	0 & 1 & -3 & 0 & \frac{1}{2}\\
	0 & 0 & 0 & 1 & 2\\
	0 & 0 & 0 & 0 & 0
	\end{array} \right] $$
	  
son matrices escalonadas reducidas.

Pero estas matrices  

$$\left[\begin{array}{cccc}
	0 & 1 & 0 & 4\\
	0 & 0 & 1 & 5\\
	0 & 0 & 0 & 2
	\end{array} \right] \mbox{ y }\left[\begin{array}{cccc}
	0 & 1 & 0 & \frac{4}{3}\\
	0 & 0 & 1 & 5\\
	1 & 0 & 0 & -1
	\end{array} \right]$$

no lo son. La primera no lo es ya que el primer elemento no nulo de la última fila no es $1$. La segunda matriz no cumple la definición, el pivote de la tercera fila está en la columna $1$, mientras que el de la primera primera fila está en la columna $2$ ($2\nless 1$).</div>\EndKnitrBlock{example}

Podremos ver mas adelante que los sistemas de ecuaciones asociadas a matrices escalonadas reducidas son mas fáciles de resolver. Entonces es conveniente hallar una  matriz escalonada reducida que tenga un sistema de ecuaciones equivalente al original para así resolver el sistema fácilmente. 

## Ecuaciones lineales y matrices

Dado un sistema de ecuaciones lineales como \@ref(eq:sistemalineal)
\begin{equation}
\begin{array}{ccccc}
A_{11}x_{1}+&A_{12}x_{2}+&\cdots +&A_{1n}x_{n}=&b_{1}\\
A_{21}x_{1}+&A_{22}x_{2}+&\cdots +&A_{2n}x_{n}=&b_{2}\\
\vdots& &\ddots& \vdots& \vdots	\\
A_{m1}x_{1}+&A_{m2}x_{2}+&\cdots +&A_{mn}x_{n}=&b_{m}
\end{array}
\end{equation}
Podemos representar este sistema de ecuaciones como un sistema matricial $AX=B$, donde $A$ es la matriz de los coeficientes del sistema de ecuaciones, $X$ es una matriz de incógnitas y $B$ una matriz de términos independientes de la siguiente forma:
\begin{equation}
	\left[ \begin{array}{cccc}
		A_{11}&A_{12}&\cdots &A_{1n}\\
		A_{21}&A_{22}&\cdots &A_{2n}\\
		\vdots& \ddots& \vdots& \vdots\\
		A_{m1}&A_{m2}&\cdots &A_{mn}
	\end{array}\right] 
	\cdot
	\left[ \begin{array}{c}
		x_{1}\\
		x_{2}\\
		\vdots\\
		x_{n}
	\end{array}\right] =
	\left[ \begin{array}{c}
		b_{1}\\
		b_{2}\\
		\vdots\\
		b_{n}
	\end{array}\right] 
\end{equation}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-13"><strong>(\#thm:unnamed-chunk-13) </strong></span>Sean $A$, $B$ y $C$ matrices sobre el cuerpo de escalares $\mathbb{F}$. Supongamos que los productos $BC$ y $A(BC)$ están definidos. Entonces, $AB$ y $(AB)C$ también están definidos y $A(BC)=(AB)C$.
</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Como $BC$ y $A(BC)$ están definidos, se tiene que el número de columnas de $B$ es igual al número de filas de $C$ y que el número de columnas de $A$ es igual al número de filas de $BC$ (y por lo tanto, igual al número de filas de $B$). Supongamos que $B$ es de orden $n\times p$, $C$ es de orden $p\times q$ y $A$ de orden $m\times n$, así $A(BC)$ es de orden $m\times q$. Claramente, $AB$ está definida y será de orden $m\times p$, como $C$ es de orden $p\times q$, $(AB)C$ está bien definido y será de orden $m\times q$. Ahora veamos que los productos $A(BC)$ y $(AB)C$ además de tener el mismo orden, coinciden en cada elemento.
	$\begin{array}{rl}
	[A(BC)]_{ij} & =\sum_{r=1}^{n} [A]_{ir}[BC]_{rj}\\
	             & =\sum_{r=1}^{n} [A]_{ir} \sum_{s=1}^{p} [B]_{rs} [C]_{sj}\\
	             & =\sum_{r=1}^{n}\sum_{s=1}^{p} [A]_{ir}[B]_{rs} [C]_{sj}\\
	             & =\sum_{s=1}^{p}\sum_{r=1}^{n} [A]_{ir}[B]_{rs} [C]_{sj}\\
	             & =\sum_{s=1}^{p}(\sum_{r=1}^{n} [A]_{ir}[B]_{rs}) [C]_{sj}\\
	             & =\sum_{s=1}^{p} [AB]_{is} [C]_{sj}\\
	             & =[(AB)C]_{ij}
	\end{array}$
</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}El producto de una matriz cuadrada $A$ de orden $n\times n$, consigo misma, se puede denotar por $A^{2}=AA$. Note que $A^{2}$ es de orden $n\times n$, luego el producto $AA^{2}$ está defindo y se denotará $A^{3}$. En general, el producto de cualquier matriz cuadrada consigo misma, $r$ veces, está definida y se denota $A^{r}=AA\cdots A$.</div>\EndKnitrBlock{remark}

Ahora veremos las operaciones elementales por filas que corresponden a hacer combinaciones lineales entre las filas de la matriz de coeficientes (equivalente a hacerlo con las ecuaciones del sistema). Las *\textit{*operaciones elementales por filas* son tres:

(1) Multiplicar una fila de la matriz $A$ por un escalar no nulo $\lambda$.
	
(2) Intercambio de dos filas de la matriz $A$.
	
(3) Sustituír la $i$-ésima fila de la matriz $A$, por la suma de la fila $r$ mas un múltiplo de la fila $s$-ésima.

Podemos denotar en forma de función (entre fila) las operaciones elementales por fila del siguiente modo.
Si $A$ es una matriz $m\times n$, una operación elemental de filas es una función $e$ que se le aplica a la matriz $A$, asociándole la matriz $e(A)$, que corresponde al resultado de alguna de las operaciones antes descritas. esto es:

(1) Denotaremos $\lambda e_{r}$ a la operación 
	$[e(A)]_{ij}=\left\{ \begin{array}{cc}
	\lambda [A]_{ij} & \mbox{ si } i=r \\
	\left[A\right]_{ij} & \mbox{ si } i\neq r
	\end{array}\right.$, con $r\leq m$ y $\lambda\neq 0$.
	
(2) Denotaremos $e_{rs}$ a la operación 
	$[e(A)]_{ij}=\left\{ \begin{array}{cc}
	[A]_{sj} & \mbox{ si } i=r \\
	\left[ A\right]_{rj} & \mbox{ si } i=s \\
	\left[A\right]_{ij} & \mbox{ en otro caso } 
	\end{array}\right.$, con $r\neq s \leq m$.
	
(3) Denotaremos $\lambda e_{rs}$ a la operación 
	$[e(A)]_{ij}=\left\{ \begin{array}{cc}
	[A]_{ij}+\lambda [A]_{sj} & \mbox{ si } i=r \\
	\left[A\right]_{ij} & \mbox{ si } i\neq r
	\end{array}\right.$, con $r\neq s \leq m$.

Note que cualquiera de las tres operaciones elementales por filas se puede "revertir" con una operación del mismo tipo. Para el primer tipo, basta con multiplicar la misma fila por el inverso de $\lambda$, $\frac{1}{\lambda}$. Para el intercambio de las filas $r$ y $s$ basta volver a intercambiar las filas. Para el tercer tipo de operación, $\lambda A_{rs}$, debemos aplicar $-\lambda A_{rs}$ y regresaremos a la matriz original. Esto es la demostración del siguiente teorema.

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-16"><strong>(\#thm:unnamed-chunk-16) </strong></span>Para cada operación elemental de filas $e$ existe una operación elemental de filas $e_{1}$ del mismo tipo tal que $e_{1}(e(A))=e(e_{1}(A))=A$. Es decir, cada operación elemental de filas, tiene una operación inversa del mismo tipo.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-17"><strong>(\#def:unnamed-chunk-17) </strong></span>Si $A$ y $B$ son dos matrices del mismo orden sobre el mismo cuerpo de escalares y $B$ se obtiene de aplicar una cantidad finita de operaciones elementales por filas a la matriz $A$, entonces decimos que *$B$ es equivalente por filas a $A$*.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Del teorema anterior se puede verificar que si una matriz $B$ es equivalente por filas a otra matriz $A$, entonces $A$ es equivalente por filas con $B$. También se puede ver que toda matriz es equivalente por filas a si misma. Por último se puede demostrar que si $A$ es equivalente por filas a $B$ y $B$ es equivalente por filas a $C$, entonces $A$ es equivalente por filas a $C$. De lo anterior, se tiene que la equivalencia por filas es una relación de equivalencia.</div>\EndKnitrBlock{remark}

Como ya lo hemos mencionado, aplicar una operación elemental por filas es equivalente a hacer combinaciones lineales con las ecuaciones del sistema, por lo tanto al obtener matrices equivalentes por filas tendremos sistemas de ecuaciones equivalentes.

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-19"><strong>(\#thm:unnamed-chunk-19) </strong></span>Si $A$ y $B$ son matrices equivalentes por filas, los sistemas homogeneos de ecuaciones lineales $AX=0$ y $BX=0$ tinen exactamente las mismas soluciones.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Basta suponer que $B$ se obtiene de aplicar una operación elemental $e$ a la matriz $A$. Luego, las ecuaciones del sistema $BX=0$ son combinaciones lineales de las ecuaciones del sistema $AX=0$, por lo que cada solución de $AX=0$ es solución de $BX=0$. Análogamente,  cada solución de $BX=0$ es solución de $AX=0$, ya que $A$ se obtiene al aplicar la operación elemental inversa de $e$ a la matriz $B$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm45"><strong>(\#exm:ejm45) </strong></span>Dada la matriz de coeficientes 

$$A=\left[  \begin{array}{cccc}
	2 & -1 & 3 & 2 \\
	1 & 4 & 0 & -1 \\
	2 & 6 & -1 & 5
	\end{array}\right]$$
  
podemos hallar una matriz escalonada reducida por fila equivalente a $A$, de la siguiente forma:
	
$$\left[  \begin{array}{cccc}
	2 & -1 & 3 & 2 \\
	1 & 4 & 0 & -1 \\
	2 & 6 & -1 & 5
	\end{array}\right]   \stackrel{-2 e_{21}}{\longrightarrow}
	\left[	\begin{array}{cccc}
	0 & -9 & 3 & 4 \\
	1 & 4 & 0 & -1 \\
	2 & 6 & -1 & 5
	\end{array}\right]$$
  
$$\stackrel{-2 e_{23}}{\longrightarrow}
	\left[ 
	\begin{array}{cccc}
	0 & -9 & 3 & 4 \\
	1 & 4 & 0 & -1 \\
	0 & -2 & -1 & 7
	\end{array}\right] \stackrel{\frac{-1}{2} e_{3}}{\longrightarrow}
	\left[ 
	\begin{array}{cccc}
		0 & -9 & 3 & 4 \\
		1 & 4 & 0 & -1 \\
		0 & 1 & \frac{1}{2} & \frac{-7}{2}
	\end{array}\right]$$
  
$$\stackrel{-4 e_{32}}{\longrightarrow}
	\left[ 
	\begin{array}{cccc}
		0 & -9 & 3 & 4 \\
		1 & 0 & -2 & 13 \\
		0 & 1 & \frac{1}{2} & \frac{-7}{2}
	\end{array}\right] \stackrel{9 e_{31}}{\longrightarrow}
	\left[ 
	\begin{array}{cccc}
		0 & 0 & \frac{15}{2} & \frac{-55}{2} \\
		1 & 0 & -2 & 13 \\
		0 & 1 & \frac{1}{2} & \frac{-7}{2}
	\end{array}\right]$$
  
$$\stackrel{\frac{2}{15} e_{1}}{\longrightarrow}
  \left[ 
	\begin{array}{cccc}
		0 & 0 & 1 & \frac{-11}{3} \\
		1 & 0 & -2 & 13 \\
		0 & 1 & \frac{1}{2} & \frac{-7}{2}
	\end{array}\right] \stackrel{2 e_{12}}{\longrightarrow}
	\left[ 
	\begin{array}{cccc}
		0 & 0 & 1 & \frac{-11}{3} \\
		1 & 0 & 0 & \frac{17}{3} \\
		0 & 1 & \frac{1}{2} & \frac{-7}{2}
	\end{array}\right]$$
  
$$\stackrel{\frac{-1}{2} e_{13}}{\longrightarrow}
	\left[ 
	\begin{array}{cccc}
	0 & 0 & 1 & \frac{-11}{3} \\
	1 & 0 & 0 & \frac{17}{3} \\
	0 & 1 & 0 & \frac{-5}{3}
	\end{array}\right] \stackrel{e_{12}}{\longrightarrow}
  \left[ 
	\begin{array}{cccc}
	1 & 0 & 0 & \frac{17}{3} \\
	0 & 0 & 1 & \frac{-11}{3} \\
	0 & 1 & 0 & \frac{-5}{3}
	\end{array}\right]$$
  
$$\stackrel{e_{32}}{\longrightarrow}
	\left[ 
	\begin{array}{cccc}
	1 & 0 & 0 & \frac{17}{3} \\
	0 & 1 & 0 & \frac{-5}{3} \\
	0 & 0 & 1 & \frac{-11}{3}
	\end{array}\right]$$
	
De donde se tiene que los sistemas de ecuaciones lineales

$$\left\lbrace 
\begin{array}{ccccc}
2x_{1} & -x_{2} & +3x_{3} & +2x_{4} & =0\\
x_{1} & +4x_{2} &  & -x_{4} &=0\\
2x_{1} & +6x_{2} & -x_{3} & +5x_{4} & =0
\end{array}
\right.$$
  
y

$$\left\lbrace 
\begin{array}{ccccc}
	x_{1} &  &  & +\frac{17}{3}x_{4} &=0 \\
 & x_{2} &  & +\frac{-5}{3}x_{4} &=0 \\
  &  & x_{3} & +\frac{-11}{3}x_{4} &=0 
\end{array} 
\right. $$ 
	  
son equivalentes y por lo tanto tienen las mismas soluciones. Del segundo sistema salta a la vista que una solución es de la forma $(\frac{-17}{3}\lambda,\frac{5}{3}\lambda,\frac{11}{3}\lambda,\lambda)$ para cualquier número real $\lambda$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-21"><strong>(\#exm:unnamed-chunk-21) </strong></span>Dada la ecuación con coeficientes en el cuerpo de los números complejos $\mathbb{C}$:

$$\left\lbrace 
	\begin{array}{ccc}
	-x_{1} & +ix_{2} &=0\\
	-ix_{1} & +3x_{2} &=0\\
	x_{1} & +2x_{2} & =0
	\end{array}
	\right.$$
	
La matriz de coeficientes es 

$$A=\left[  \begin{array}{cc}
	-1 & i \\
	-i & 3 \\
	1 & 2 
	\end{array}\right]$$
  
Hallemos una matriz escalonada reducida por fila equivalente a $A$:

$$\left[  \begin{array}{cc}
	-1 & i \\
	-i & 3 \\
	1 & 2 
	\end{array}\right]   \stackrel{e_{13}}{\longrightarrow}
	\left[	\begin{array}{cc}
	1 & 2 \\
	-i & 3 \\
	-1 & i 
	\end{array}\right]$$
  
$$\stackrel{i e_{12}}{\longrightarrow}
	\left[ 
	\begin{array}{cc}
	1 & 2 \\
	0 & 3+2i \\
	-1 & i 
	\end{array}\right] \stackrel{1 e_{13}}{\longrightarrow}
	\left[ 
	\begin{array}{cc}
	1 & 2 \\
	0 & 3+2i \\
	0 & 2+i 
	\end{array}\right]$$
  
$$\stackrel{\frac{1}{3+2i} e_{2}}{\longrightarrow}
\left[ 
	\begin{array}{cc}
	1 & 2 \\
	0 & 1 \\
	0 & 2+i 
	\end{array}\right] \stackrel{-2 e_{21}}{\longrightarrow}
	\left[ 
	\begin{array}{cc}
	1 & 0 \\
	0 & 1 \\
	0 & 2+i 
	\end{array}\right] \stackrel{-2-i e_{23}}{\longrightarrow}
	\left[ 
	\begin{array}{cc}
	1 & 0 \\
	0 & 1 \\
	0 & 2+i 
	\end{array}\right]$$
	
De donde se tiene que la solución del sistema $AX=0$ es la trivial $(0,0,0)$, ya que $AX=0$ es equivalente al sistema 

$$\left[ \begin{array}{cc}
1 & 0 \\
0 & 1 \\
0 & 2+i 
\end{array}\right] \cdot \left[ \begin{array}{c}
x_{1} \\
x_{2} 
\end{array}\right] = \left[ \begin{array}{c}
0 \\
0 
\end{array}\right]$$
</div>\EndKnitrBlock{example}

Dada cualquier matriz $A$ de orden $m\times n$, podemos hallar una matriz equivalente por filas que sea escalonda reducida por filas, realizando un número finito de operaciones por filas según el siguiente algoritmo. Toda fila nula de la matriz se mueven hacia abajo de la matriz por medio de la operación intercambio de filas, de forma que todas ellas queden en las últimas filas de la matriz, es decir, supongamos que existen $r\leq m$ filas no nulas, entonces las últimas filas $r+1, r+2, \cdots, m$ serán las filas de ceros, de forma que el bloque superior $1,2,\cdots, r$ serán las filas no nulas. Luego, considerando esta nueva matriz (la llamaremos $A$, por comodidad). Sea $a_{1k_{1}}$ el primer elemento no nulo de la primera fila ($k_{1}$ es la columna donde aparece el primer elemento no nulo de la fila $1$), si $a_{1k_{1}}=1$, se cumple la condición (1), si no es así, aplicamos la operación $\frac{1}{a_{1k_{1}}} e_{1}$ para hacer que el pivote sea $1$. Ahora, debemos hacer que todo elemento en esa columna sea cero  si está en otra fila (condición (2)), para esto aplicamos la operación $-a_{ik_{1}}e_{i}$ para cada fila $1\neq i\leq r$. Pasamos a la siguiente fila, $A_{2\ast}$, consideramos el primer elemento no nulo de dicha fila, $a_{2k_{2}}$, donde $k_{2}$ es la columna que ocupa. Si $a_{2k_{2}}=1$, no haremos nada, en otro caso, aplicamos la operación $\frac{1}{a_{2k_{2}}} e_{2}$, con esto se cumple la condición (1) para esta fila. Ahora aplicamos $-a_{ik_{2}}e_{i}$ para cada fila $2\neq i\leq r$, con esto se cumple la condición (2). Repetimos este proceso para cada una de las filas no nulas de $A$, es decir, para las filas $1,2,\cdots, r$. Ahora ordenamos las filas no nulas intercambiando filas para lograr que se cumpla la condición (4), es decir, que se cumpla que $p_{1}< p_{2}< \cdots < p_{r}$, llamando $p_{i}$ a la columna del pivote de la fila $i$ luego de aplicar las operaciones elementales por filas. Es claro que estas operaciones son siempre posibles de aplicar a cualquier matriz, en un número finito de pasos.
De lo anterior podemos concluir que siempre podemos reducir una matriz a una escalonada. Podemos expresarlo como un teorema, cuya demostración es el algoritmo anterior.

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-22"><strong>(\#thm:unnamed-chunk-22) </strong></span>Toda matriz $m\times n$ sobre el cuerpo $\mathbb{F}$ es equivalente por filas a una matriz escalonada reducida por filas.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-23"><strong>(\#thm:unnamed-chunk-23) </strong></span>Si $A$ es una matriz $m\times n$ con $m<n$, el sistema homogéneo de ecuaciones lineales $AX=0$ tiene una solución no trivial.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $R$ una matriz escalón reducida por filas equivalente por filas a la matriz $A$. Entonces $AX=0$ y $RX=0$ tienen exactamente las mismas soluciones. Supongamos que $R$ tiene $r$ filas no nulas, luego $r<n$, luego el sistema de ecuaciones $RX=0$ consta de $r$ ecuaciones no triviales, a saber, suponiendo que $x_{k_{i}}$ es la incógnita que aparece en la posición del pivote de la fila $i$,

$$\begin{array}{ccc}
	x_{k_{1}}+& \sum_{j=1}^{n-r}c_{1j}u_{j}=&0\\
	\vdots & & \vdots\\
	x_{k_{r}}+& \sum_{j=1}^{n-r}c_{rj}u_{j}=&0
	\end{array}$$
	  
donde las $n-r$ incógnitas diferentes de $x_{k_{1}}, x_{k_{2}},\cdots, x_{k_{r}}$ las denotamos $u_{1}, u_{2}, \cdots, u_{n-r}$. Note que la incógnita $x_{k_{i}}$ aparece solo en la $i$-ésima ecuación. De esta forma, podemos dar valores arbitrarios a $u_{1}, u_{2}, \cdots, u_{n-r}$ y así hallar una solución no trivial, que a su vez es solución del sistema $AX=0$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:teorema6"><strong>(\#thm:teorema6) </strong></span>Si $A$ es una matriz cuadrada $n\times n$. Entonces $A$ es equivalente por filas a la matriz identidad si y solo si, el sistema de ecuaciones $AX=0$ tiene solo la solución trivial $X=0$.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Si $A$ es equivalente por filas a la identidad, por el teorema anterior $AX=0$ y $IX=0$ tienen exactamente las mismas soluciones, por lo tanto la única solución es $X=0$. Ahora, supongamos que $AX=0$ tiene unicamente la solución trivial; supongamos que $R$ es la matriz escalonada reducida equivalente a $A$, y sea $r\leq n$ el número de filas no nulas; entonces $RX=0$ tiene unicamente la solución trivial (por el teorema anterior), luego $r\geq n$, por lo tanto $r=n$, por lo tanto $R=I$. </div>\EndKnitrBlock{proof}

Todos los teoremas anteriores hacen referencia a sistemas homogéneos $AX=0$, el cual siempre tiene solución, la solución trivial $X=0$. Cabe preguntar que sucede con los sistemas no homogéneos $AX=B$. Un sistema no homogéneo no tiene necesariamente solución. Estudiemos esto a continuación.

Dado el sistema no homogéneo $AX=B$, con $A$ de orden $m\times n$; consideramos la *matriz aumentada*, $\hat{A}$ de orden $m\times (n+1)$, cuyas primeras $n$ columnas son iguales a las columnas de $A$ y la columna $n+1$ corresponde a $B$, es decir, $\hat{A}_{\ast j}=A_{\ast j}$ para $j\leq n$ y $\hat{A}_{\ast n+1}=B_{1}$. Se aplicará a esta matriz, $\hat{A}$ las mismas operaciones elementales por filas que se le aplican a la matriz $A$ para llevarla a una matriz escalonada reducidas por filas $R$, y así se obtendrá una matriz $\hat{R}$ cuya última fila son los escalares $z_{1}, z_{2},\cdots z_{m}$ (que serán combinaciones lineales de los coeficientes $b_{1}, b_{2},\cdots, b_{m}$). Es claro que los sistemas $AX=B$ y $RX=Z$ tienen las mismas soluciones (la demostración es análoga al de los sistemas homogéneos). Es fácil ver cuando el sistema $\hat{R}X=Z$ tiene solución. Si $\hat{R}$ tiene $r$ filas no nulas, donde el pivote de la fila $i$ está en la columna $k_{i}$ entonces las primeras $r$ ecuaciones expresarán las primeras $r$ incógnitas, $x_{k_{1}}, x_{k_{2}}, \cdots, x_{k_{r}}$ por las $n-r$ incógnitas restantes, $x_{j}$ y los escalares $z_{1}, z_{2},\cdots, z_{r}$. Y las últimas $m-r$ ecuaciones son:

$$\begin{array}{cc}
0= & z_{r+1}\\
\vdots & \vdots\\
0= & z_{m}
\end{array}$$

Por lo tanto, para que el sistema tenga solución debe suceder que $z_{r+1}=z_{r+2}=\cdots=z_{m}=0$. Si esto ocurre entonces las soluciones del sistema se obtienen dando valores arbitrarios a la $n-j$ incógnitas $x_{j}$.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-26"><strong>(\#exm:unnamed-chunk-26) </strong></span>Sea 

$$A=\left[\begin{array}{ccc}
	1 & -2 & 1\\
	2 & 1 & 1\\
	0 & 5 & -1
	\end{array} \right] $$
  
la matriz de coeficientes del sistema $AX=B$, donde 

$$B=\left[\begin{array}{c}
	b_{1}\\
	b_{2}\\
	b_{3}
	\end{array} \right]$$.

Luego la matriz extendida es 

$$\hat{A}=\left[\begin{array}{ccc|c}
	1 & -2 & 1 & b_{1}\\
	2 & 1 & 1 & b_{2}\\
	0 & 5 & -1 & b_{3}
	\end{array} \right]$$
  
Reducimos la matriz:
  
$$\left[\begin{array}{ccc|c}
	1 & -2 & 1 & b_{1}\\
	2 & 1 & 1 & b_{2}\\
	0 & 5 & -1 & b_{3}
	\end{array} \right] \stackrel{-2 e_{12}}{\longrightarrow} 
	\left[\begin{array}{ccc|c}
	1 & -2 & 1 & b_{1}\\
	0 & 5 & -1 & b_{2}-2b_{1}\\
	0 & 5 & -1 & b_{3}
	\end{array} \right]$$
  
$$\stackrel{\frac{1}{5} e_{2}}{\longrightarrow}
	\left[\begin{array}{ccc|c}
	1 & -2 & 1 & b_{1}\\
	0 & 1 & -\frac{1}{5} & \frac{1}{5}(b_{2}-2b_{1})\\
	0 & 5 & -1 & b_{3}
	\end{array} \right] \stackrel{ 2e_{21}}{\longrightarrow}
  \left[\begin{array}{ccc|c}
	1 & 0 & \frac{3}{5} & \frac{1}{5}(b_{1}+2b_{2})\\
	0 & 1 & -\frac{1}{5} & \frac{1}{5}(b_{2}-2b_{1})\\
	0 & 5 & -1 & b_{3}
	\end{array} \right]$$
  
$$\stackrel{ -5e_{23}}{\longrightarrow}
	\left[\begin{array}{ccc|c}
	1 & 0 & \frac{3}{5} & \frac{1}{5}(b_{1}+2b_{2})\\
	0 & 1 & -\frac{1}{5} & \frac{1}{5}(b_{2}-2b_{1})\\
	0 & 0 & 0 & b_{3}-b_{2}+2b_{1}
	\end{array} \right]$$
  
Luego, el sistema tiene solución solo si $2b_{1}-b_{2}+b_{3}=0$. Si esta condición se cumple, entonces una solución para el sistema es de la forma:

$$\begin{array}{cc}
	x_{1}= &-\frac{3}{5}x_{3}+\frac{1}{5}(b_{1}+2b_{2})\\
	x_{2}= &\frac{1}{5}x_{3}+\frac{1}{5}(b_{2}-2b_{1})
	\end{array}$$
	  
para cualquier valor de $x_{3}$.</div>\EndKnitrBlock{example}

Note que la igualdad $A(BC)=(AB)C$ implica, entre otras cosas, que combinaciones lineales de combinaciones lineales de las filas de $C$, son otra vez combinaciones lineales de las filas de $C$.
Si $C$ es una matriz que se obtiene de aplicar una operación elemental de fila a $B$, entonces las filas de $C$ son combinación lineal de las filas de $B$, por lo tanto debe existir una matriz $A$, tal que $C=AB$. Pueden existir muchas matrices con tal propiedad; veremos como escoger una de ellas.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-27"><strong>(\#def:unnamed-chunk-27) </strong></span>Una matriz $m\times m$ es una *matriz elemental* si se obtiene de aplicar una sola operación elemental de filas a la matriz identidad (de orden $m\times m$).
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-28"><strong>(\#exm:unnamed-chunk-28) </strong></span>Una matriz elementa de orden $2\times 2$ es necesariamente como alguna de las siguientes: 
  
$$ \left[ \begin{array}{cc}
	0 & 1\\
	1 & 0
	\end{array} \right] , 
	\left[ \begin{array}{cc}
	1 & \lambda\\
	0 & 1
	\end{array} \right] ,
	\left[ \begin{array}{cc}
	1 & 0\\
	\lambda & 1
	\end{array} \right]  \mbox{ con }\lambda\in \mathbb{F}$$
  
o
	
$$\left[ \begin{array}{cc}
	\delta & 0\\
	0 & 1
	\end{array} \right] , 
	\left[ \begin{array}{cc}
	1 & 0\\
	0 & \delta
\end{array} \right] \mbox{ con } \delta\neq 0$$</div>\EndKnitrBlock{example}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-29"><strong>(\#thm:unnamed-chunk-29) </strong></span>Sea $E$ una matriz elemental que corresponde a la operación elemental por filas $e$. Sea $A$ una matriz $m\times n$. Entonces $e(A)=EA$.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Note que el elemento $[EA]_{ij}$ se obtien de la $i$-ésima fila de $E$ y la $j$-ésima columna de $A$. Estudiemos cada tipo de operación por separado, comenzaremos con la mas complicada y las otras dos se dejan como ejercicio. Supongamos que $e= \lambda e_{sr}$ (se sustituye la fila $r$ por la fila $r$ mas $\lambda$ veces la fila $s$). Se tiene que $E=\lambda e_{sr}(I)$, por lo tanto:
  
$$[E]_{ik}=
		\left\{ \begin{array}{lc}
		\delta_{ik} & i\neq r\\
		\delta_{rk}+\lambda \delta_{sk} & i=r
		\end{array} 
		\right.$$
		  
Luego

$$ [EA]_{ij}=\sum_{k=1}^{m} [E]_{ik}[A]_{kj}=
	\left\{ \begin{array}{lc}
		a_{ik} & i\neq r \\
		a_{rk}+\lambda a_{sk} & i=r
		\end{array} 
	\right.$$
		  
Por lo tanto $EA=e(A)$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-31"><strong>(\#cor:unnamed-chunk-31) </strong></span>Sean $A$ y $B$ matrices de orden $m\times n$ sobre el cuerpo $\mathbb{F}$. Entonces $B$ es equivalente por filas a $A$ si y solo si $B=PA$, donde $P$ es un producto de matrices elementales $m\times m$.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Supongamos que $E_{1}, E_{2},\cdots, E_{k}$ matrices elementales correspondientes a las operaciones elementales por fila $e_{1}, e_{2},\cdots, e_{k}$. Entonces $B=e_{1}\circ e_{2}\circ\cdots \circ e_{k}(A)$ si y solo si $B=E_{1} E_{2} \cdots E_{k} A=PA$, con $P=E_{1} E_{2} \cdots E_{k}$.</div>\EndKnitrBlock{proof}

Si $A$ es una matriz equivalente por filas a $B$, el corolario anterior asegura que existe $P$, tal que $B=PA$, donde $P$ es producto de matrices elementales. Por otro lado se tiene que $B$ es equivalente por filas a $A$, luego existe una matriz $Q$, producto de matrices elementales, tal que $A=QB$. En particular, esto es cierto para la matriz identidad, es decir $I=QB=QP$. Veremos que la existencia de la matriz $Q$, tal que $QP=I$ es equivalente al hecho de que $P$ es producto de matrices elementales.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-33"><strong>(\#def:unnamed-chunk-33) </strong></span>Sea $A$ una matriz (cuadrada) $n\times n$ sobre el cuerpo $\mathbb{F}$. Una matriz $B$ $n\times n$, tal que $BA=I$ se llama *inversa izquierda* de $A$; una matriz $B$ $n\times n$, tal que $AB=I$ se llama *inversa derecha* de $A$. Si $AB=BA=I$, entonces $B$ se llama *inversa bilateral* de $A$ y en este caso se dice que $A$ es *invertible*.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-34"><strong>(\#lem:unnamed-chunk-34) </strong></span>Si una matriz $A$ tiene una inversa izquierda $B$ y una inversa derecha $C$, entonces $B=C$.</div>\EndKnitrBlock{lemma}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Suponga que $BA=I$ y $AC=I$. Entonces $B=BI=B(AC)=(BA)C=IC=C$</div>\EndKnitrBlock{proof}

Del corolario anterior tenemos que si $A$ tiene una inversa derecha y una inversa izquierda, entonces son iguales, la llamos *la inversa de $A$* y la denotámos $A^{-1}$.

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-36"><strong>(\#thm:unnamed-chunk-36) </strong></span>Dadas las matrices $A$ y $B$ de orden $n\times n$ sobre el cuerpo $\mathbb{F}$. Se tiene que:

(1) Si $A$ es invertible, entonces $A^{-1}$ también lo es y $(A^{-1})^{-1}=A$.

(2) Si $A$ y $B$ son invertibles, entonces $AB$ también lo es y $(AB)^{-1}=B^{-1}A^{-1}$.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}De la simetría de la definición de inversa, se sigue la parte $1$. Para la segunda parte se sigue de $(AB)(B^{-1}A^{-1})=A(BB^{-1})A^{-1}=AIA^{-1}=AA^{-1}=I$ y $(B^{-1}A^{-1})(AB)=B^{-1}(A^{-1}A)B=B^{-1}IB=B^{-1}B=I$.</div>\EndKnitrBlock{proof}

Del resultado anterior se tiene que el producto de matrices invertible, es invertible.

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-38"><strong>(\#thm:unnamed-chunk-38) </strong></span>Toda matriz elemental es invertible.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $E$ una matriz elemental y sea $e$ la operación elemental de filas que corresponde a $E$, es decir, $E=e(I)$. Sea $\hat{e}$ la operación inversa de $e$, y $\hat{E}=\hat{e}(I)$. Entonces $\hat{E}E=\hat{e}(E)=\hat{e}(e(I))=(\hat{e}\circ e) (I)= I$. Análogamente se tiene que $E\hat{E}=I$. Luego $\hat{E}=E^{-1}$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-40"><strong>(\#thm:unnamed-chunk-40) </strong></span>Sea $A$ una matriz $n\times n$. Entonces los siguientes enunciados son equivalentes:
	
(1) $A$ es invertible.

(2) $A$ es equivalente por filas a la identidad (de orden $n\times n$).

(3) $A$ es producto de matrices elementales.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $R=E_{1}E_{2}\cdots E_{n}A$ una matriz esacalonada reducida equivalente por filas a la matriz $A$ (donde $E_{1}E_{2}\cdots E_{n}$ son matrices elementales). Entonces, $A=E_{n}^{-1}\cdots E_{2}^{-1}E_{1}^{-1}R$, ya que las matrices elementales son invertibles. Como el producto de matrices invertibles, es invertible, $A$ es invertible si y solo si $R$ lo es; como $R$ es una matriz cuadrada esacalonada reducida por filas, entonces $R$ es invertible si y solo si $R$ es la identidad. Luego, $A$ es invertible si y solo si $R=I$, entonces, $A=E_{n}^{-1}\cdots E_{2}^{-1}E_{1}^{-1}I=E_{n}^{-1}\cdots E_{2}^{-1}E_{1}^{-1}$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-42"><strong>(\#cor:unnamed-chunk-42) </strong></span>Si $A$ es una matriz invertible $n\times n$ y si la sucesión de operaciones elementales $e_{1}\circ e_{2}\circ \cdots \circ e_{n}$ reduce a la matriz $A$ a la identidad, entonces la misma sucesión de operaciones elementales aplicadas a $I$, nos da $A^{-1}$, la inversa de $A$.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-43"><strong>(\#cor:unnamed-chunk-43) </strong></span>Sean $A$ y $B$ dos matrices $m\times n$. Entonces $B$ es equivalente por filas a $A$ si y solo si $B=PA$, donde $P$ es una matriz invertible $m\times m$.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-44"><strong>(\#thm:unnamed-chunk-44) </strong></span>Sea $A$ una matriz $n\times n$. Entonces los siguientes enunciados son equivalentes:

(1) $A$ es invertible.

(2) El sistema homogéneo $AX=0$ tiene una única solución ($X=0$).

(3) El sistema de ecuaciones asociado a $AX=B$ tiene una solución $X$ para cada matriz $B$ de orden $n\times 1$.
	</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}El sistema homogéneo $AX=0$ si y solo si $A$ es equivalente por filas al la identidad ( por el teorema \@ref(thm:teorema6). Del teorema anterior, se tiene que $(1)$ y $(2)$ son equivalentes. Ahora supongámos que $A$ es invertible, entonces la solución de $AX=B$ viene dada por $X=A^{-1}$. Recíprocamente, supongamos que $AX=B$ tiene una solución para cada $B$. Sea $R$ la matriz escalonada reducida por filas equivalente por filas a $A$. Necesariamente $R=I$, ya que si $R$ tiene al menos una fila identicamente igual a cero, entonces el sistema $RX=C$, donde 
                                                                                        
$$C=\left[ \begin{array}{c}
	0\\
	0\\
	\vdots\\
	0\\
	1
\end{array}\right]$$
  
no tiene solución, lo que es una contradicción. Por lo tanto se tiene que $R=I$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-46"><strong>(\#cor:unnamed-chunk-46) </strong></span>Una matriz cuadrada que tiene una inversa izquierda o una inversa a la derecha es invertible.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $A$ una matriz $n\times n$. Supongamos que $A$ tiene una inversa a la izquierda, es decir, existe $B$ tal que $BA=I$. Así, $AX=0$ tiene unicamente la solución trivial, ya que $X=IX=B(AX)$. Por lo tanto $A$ es invertible. Supóngase que $A$ tiene una inversa a la derecha, es decir, existe $C$ tal que $AC=I$. entoces $C$ tiene una inversa a la izquierda y por lo tanto es invertible, así $A=ACC^{-1}=IC^{-1}=C^{-1}$ de donde se tiene que $A$ es invertible de inversa $C$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-48"><strong>(\#cor:unnamed-chunk-48) </strong></span>Sea $A=A_{1}A_{2}\cdots A_{n}$, donde $A_{1}, A_{2}, \cdots , A_{n}$ son matrices cuadradas. Entonces $A$ es invertible si y solo si cada $A_{i}$ es invertible.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Supongamos que cada $A_{i}$ es invertible, como el producto de matrices invertibles es invertible, se tiene que $A$ es invertible. Recíprocamente, supongamos que $A$ es invertible, entonces $AX=0$ tiene unicamente la solución trivial. Por lo tanto, $(A_{1}A_{2}\cdots A_{n-1})A_{n}X=AX=0$ tiene unicamente la solución trivial, si y solo si $A_{n}X=0$ tiene solo la solución trivial, de donde se sigue que $A_{n}$ es invertible. Luego, $AA^{-1}=A_{1}A_{2}\cdots A_{n-1}$, considerando $(A_{1}A_{2}\cdots A_{n-2})A_{n-1}X=AA^{-1}X=0$, de forma análoga a lo anterior, se puede demostrar que $A_{n-1}$ es invertible. Continuando de esta forma se demuestra que cada $A_{i}$ es invertible.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Sea $A$ una matriz $m\times n$ y sea $AX=B$, y sea $R$ la matriz escalonada reducida por filas equivalentes por fila a $A$, entonces $R=PA$, donde $P$ es una matriz invertible $m\times m$; las soluciones de $RX=PB$ son las mismas que las del sistema $AX=B$. Hallar $PB$ es equivalente a reducir por filas la matriz $A$, esto se hace considerando la matriz aumentada $\hat{A}$ y aplicandole operaciones elementales por fila hasta reducir a $A$ a una matriz escalonada reducida, lo obtenido en la última columna será la matriz $PB$.</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-51"><strong>(\#exm:unnamed-chunk-51) </strong></span>Sea 

$$A=\left[\begin{array}{cc}
	2 & -1\\
	1 & 3 
	\end{array} \right]$$
  
la matriz de coeficientes del sistema $AX=B$, donde 

$$B=\left[\begin{array}{c}
	b_{1}\\
	b_{2}
	\end{array} \right]$$.

Luego la matriz extendida es 
	
$$\hat{A}=\left[\begin{array}{cc|c}
	 2 & -1 & b_{1}\\
	 1 & 3 & b_{2}
	\end{array} \right]$$
  
Reducimos la matriz:

$$\left[\begin{array}{cc|c}
	2 & -1 & b_{1}\\
	1 & 3 & b_{2}
	\end{array} \right] \stackrel{e_{12}}{\longrightarrow} 
	\left[\begin{array}{cc|c}
	1 & 3 & b_{2}\\
	2 & -1 & b_{1}
	\end{array} \right] \stackrel{-2 e_{12}}{\longrightarrow}
	\left[\begin{array}{cc|c}
	1 & 3 & b_{2}\\
	0 & -7 & b_{1}-2b_{2}
	\end{array} \right]$$
  
$$\stackrel{ -\frac{1}{7}e_{2}}{\longrightarrow}
	\left[\begin{array}{cc|c}
	1 & 3 &   b_{2}\\
	0 & 1 & \frac{1}{7}(2b_{2}-b_{1})
	\end{array} \right] \stackrel{ -3e_{21}}{\longrightarrow}
	\left[\begin{array}{cc|c}
	1 & 0 &  \frac{1}{7}(b_{2}+3b_{1})\\
	0 & 1 & \frac{1}{7}(2b_{2}-b_{1})
	\end{array} \right]$$
  
De donde se tiene que 

$PB=\left[ \begin{array}{c}
	\frac{1}{7}(b_{2}+3b_{1})\\
	\frac{1}{7}(2b_{2}-b_{1})
	\end{array}\right]$, o también que 
$A^{-1}=\left[\begin{array}{cc}
	\frac{3}{7} & \frac{1}{7}\\
	-\frac{1}{7} & \frac{2}{7} 
	\end{array} \right]$.

También podemos llegar a la inversa de $A$ aplicando las operaciones elementales antes descritas para reducir a $A$, a la identidad. Es decir:
	  
$$\left[\begin{array}{cc|cc}
	2 & -1 & 1 & 0\\
	1 & 3 & 0 & 1
	\end{array} \right] \stackrel{e_{12}}{\longrightarrow} 
	\left[\begin{array}{cc|cc}
	1 & 3 & 0 & 1\\
	2 & -1 & 1 & 0
	\end{array} \right]$$
  
$$\stackrel{-2 e_{12}}{\longrightarrow}
	\cdots 
	\left[\begin{array}{cc|cc}
	1 & 0 &  \frac{3}{7} & \frac{1}{7}\\
	0 & 1 &  -\frac{1}{7} & \frac{2}{7}
	\end{array} \right]$$</div>\EndKnitrBlock{example}

## Teoría de espacios vectoriales

En los sitemas de ecuaciones lineales vimos que las combinaciones lineales de soluciones del sistema volvía a ser una solución. Este no es el único ámbito en el que sucede y es interesante este comportamiento, el concepto de espacios vectoriales generaliza esto. Estudiaremos a continuación estas estructuras algebraicas.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-52"><strong>(\#def:unnamed-chunk-52) </strong></span>Dado un cuerpo $\mathbb{F}$, un *espacio vectorial* sobre el cuerpo $\mathbb{K}$ es un conjunto $V$ de objetos llamados *vectores*, dotado de dos operaciones, *suma* y *producto por un escalar*, con las siguientes propiedades:
	
(1) cerrado bajo la suma: para todo $u,v\in V$, se tiene que $u+v\in V$;
		
(2) la suma es comutativa: para todo $u,v\in V$, $u+v=v+u$;
		
(3) la suma es asociativa: para todo $u, v, ww\in V$, $(u+v)+w=u+(v+w)$;
		
(4) existe un único vector nulo, $0\in V$, tal que para todo $u\in V$, $u+0=u$;
		
(5) para cada vector $u\in V$, existe un único vector opuesto, $-u$, tal que $u+(-u)=0$;
		
(6) cerrado bajo el producto por un escalar: para todo $\lambda\in\mathbb{F}$ y todo $u\in V$, se tiene que $\lambda \cdot u\in V$ (se puede abreviar la notación quitando el punto $\lambda u$);
		
(7) para todo $u\in V$, $1u=u$;
		
(8) para todo $u\in V$ y para todo $\lambda, \gamma\in\mathbb{F}$, $(\lambda\gamma)u=\lambda(\gamma u)$;
	
(9) para todo $u, v\in V$ y $\lambda in\in\mathbb{F}$, $\lambda(u+v)=\lambda u+\lambda v$;
		
(10) para todo $u\in V$ y para todo $\lambda, \gamma\in\mathbb{F}$, $(\lambda +\gamma)u=\lambda u + \gamma u$.</div>\EndKnitrBlock{definition}

Note que un espacio vectorial consta de cuatro cosas, un cuerpo, un conjunto no vacío de vectores y dos operaciones. Cuando no hay posibilidad de confusión, se hará referencia solo al espacio $V$, omitiendo el resto de los objetos. Puede ocurrir que el mismo conjunto $V$ forme parte de dos espacios vectoriales distintos.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-53"><strong>(\#exm:unnamed-chunk-53) </strong></span>*El conjunto de las $n$-tuplas*, $\mathbb{F}^{n}$. Sea $\mathbb{F}$ un cuerpo y sea $V$ el conjunto de todas las $n$-tuplas $u=(x_{1}, x_{2}, \cdots , x_{n})$ de escalares $x_{i}\in\mathbb{F}$. Dados $u=(x_{1}, x_{2}, \cdots , x_{n}), v=(y_{1}, y_{2}, \cdots , y_{n})\in V$ y el escalar $\lambda\in \mathbb{F}$, definimos:
  
La suma $u+v=(x_{1}, x_{2}, \cdots , x_{n})+(y_{1}, y_{2}, \cdots , y_{n})=(x_{1}+y_{1}, x_{2}+y_{2}, \cdots , x_{n}+y_{n})$ y $\lambda u=\lambda(x_{1}, x_{2}, \cdots , x_{n})=(\lambda x_{1},\lambda x_{2}, \cdots ,\lambda x_{n})$.

Es fácil ver que estas operaciones así definidas cumplen con las 10 condiciones de la definición.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-54"><strong>(\#exm:unnamed-chunk-54) </strong></span>*El espacio de las matrices* $m\times n$, $\mathbb{F}^{m\times n}$. Sea $\mathbb{F}$ un cuerpo, y sean $m$ y $n$ enteros positivos. Sea el conjunto $\mathbb{F}^{m\times n}$ el conjunto de todas las matrices de orden $m\times n$ sobre el cuerpo $\mathbb{F}$. La suma de dos vectores y el producto por un escalar se definen de la forma usual, sean $A,B\in\mathbb{F}^{m\times n}$ y $\lambda\in\mathbb{F}$, $[A+B]_{ij}=[A]_{ij}+[B]_{ij}$ y $[\lambda A]_{ij}=\lambda [A]_{ij}$.

Note que, $\mathbb{F}^{1\times n}=\mathbb{F}^{n}$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-55"><strong>(\#exm:unnamed-chunk-55) </strong></span>*El espacio de funciones de un conjunto en un cuerpo*. Sea $\mathbb{F}$ y $C$ un conjunto no vacío cualquiera. Sea $V$ el conjunto de funciones de $C$ en $\mathbb{F}$. La suma de dos vectores $f, g\in V$, se define como la suma usual de funciones, $(f+g)(c)=f(c)+g(c)$ y el producto por un escalar se define como $(\lambda f)(c)=\lambda f(c)$. Las condiciones se cumplen, ya que $\mathbb{F}$ es un cuerpo: 

(1) claramente las operaciones así definidas, son cerradas.
		
(2) como la suma en $\mathbb{F}$ es conmutativa, $(f+g)(c)=f(c)+g(c)=g(c)+f(c)=(g+f)(c)$;
		
(3) como la suma en $\mathbb{F}$ es asociativa, $((f+g)+h)(c)=(f(c)+g(c))+h(c)=f(c)(g(c)+h(c))=(f+(g+h))(c)$;
		
(4) el único vector nulo es la función cero, que asigna el escalar cero (del cuerpo $\mathbb{F}$) a cada elemento $c\in C$, esto es $f(c)\equiv 0$;
		
(5) para toda función $f$, $-f$, definda como $(-f)(c)=-f(c)$, es el elemento opuesto;
		
(6) claramente, $(1f)(c)=1f(c)=f(c)$;
		
(7) $(\lambda\gamma f)(c)=(\lambda\gamma) f(c)= \lambda(\gamma f(c))=(\lambda(\gamma f))(c)$;
		
(8) $(\lambda(f+g))(c)=(\lambda f)(c)+(\lambda g)(c)=((\lambda f)+(\lambda g))(c)$;
		
(9) $((\lambda + \gamma)f)(c)=(\lambda f+ \gamma f)(c)$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-56"><strong>(\#exm:unnamed-chunk-56) </strong></span>*El espacio de las funciones polinómicas sobre el cuerpo* $\mathbb{F}$. Sea $\mathbb{F}$ un cuerpo y sea $V$ el conjunto de las funciones de $\mathbb{F}$ en $\mathbb{F}$, de la forma $f(x)=c_{0}+c_{1}x+\cdots+c_{n}x^{n}$, donde $c_{0}, c_{1},\cdots c_{n}$ son escalares fijos de $\mathbb{F}$ y $n$ un entero positivo cualquiera, una función de este tipo se llama *función polinómica*. Las operaciones de suman y producto por escalares se definen como en el ejemplo anterior. Es fácil ver que $f+g$ y $\lambda f$ son funciones polinómicas y cumplen con las condiciones de la definición.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-57"><strong>(\#def:unnamed-chunk-57) </strong></span>Una *combinación lineal* de los vectores $u_{1}, u_{2}, \cdots, u_{n}$ de un espacio vectorial $V$, es un vector $v\in V$, tal que $v=\sum_{i=1}^{n} \lambda_{i}u_{i}$, para algunos escalares $\lambda_{1}, \lambda_{2}, \cdots, \lambda_{n}$.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Note que una combinación lineal de vectores, es un vector del espacio gracias a que las operaciones de suma y producto por un escalar son cerradas.

Una combinación lineal de combinaciones lineales de vectores, es una combinación lineal de vectores.

Dados los vectores $u_{1}, u_{2}, \cdots, u_{n}$, de las propiedades de asociatividad de la suma y las propiedades distributivas, se tiene que $\sum_{i=1}^{n} \lambda_{i}u_{i} + \sum_{i=1}^{n} \gamma_{i}u_{i}=\sum_{i=1}^{n} (\lambda_{i}+\gamma_{i})u_{i}$.</div>\EndKnitrBlock{remark}

Mucho del álgebra está motivado por la geometría, las palabras "espacio" y vector tienen una connotación geométrica. Los vectores en el espacio $\mathbb{R}^{3}$ son ternas $(x,y,z)$ donde cada entrada representa una coordenada en el espacio. Esto se estudia en el capítulo de vectores.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-59"><strong>(\#def:unnamed-chunk-59) </strong></span>Sea $V$ un espacio vectorial sobre el cuerpo $\mathbb{F}$. Un *subespacio* de $V$ es un subconjunto $W\subseteq V$ que junto a las mismas operaciones de suma y producto por un escalar definidas en $V$, es en si mismo un espacio vectorial sobre $\mathbb{F}$.

Escribiremos $W\prec V$ para decir que $W$ es un subespacio de $V$.</div>\EndKnitrBlock{definition}

De este modo para comprobar que un subconjunto de vectores $W$ de un espacio vectorial $V$, es un subespacio de $V$, debemos ver que la suma y el producto por un escalar son operaciones cerradas, es decir, para todo $u,v\in W$ se debe tener que $u+v\in W$ y $\lambda v\in W$, para calquier escalar $\lambda$ en $\mathbb{F}$; que el elemento neutro (para la suma) pertenece a $W$, y que todo vector de $W$, tiene un opuesto en $W$, es decir para todo $v\in W$, $-v\in W$. Las otras propiedades se heredan del espacio vectorial $V$.

En alguna literatura se puede conseguir que la definición de subespacio vectorial es un subconjunto $W$ que tiene la siguiente propiedad: para todo $u,v\in W$ y todo $\lambda\in\mathbb{F}$, $\lambda u+v\in W$. Sin embargo, se puede demostrar la equivalencia entre ambas afirmaciones.

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-60"><strong>(\#thm:unnamed-chunk-60) </strong></span>Un subconjunto no vacío $W$ de $V$ es un subespacio de $V$ si y solo si, para todo par de vectores $u,v$ de $W$ y todo escalar $\lambda$ en el cuerpo $\mathbb{F}$, se tinen que el vector (combinación lineal) $\lambda u + v$ está en $W$.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $W$ un subconjunto de vectores con la propiedad de que $\forall u,v\in W$ y $\forall \lambda\in\mathbb{F}$, $\lambda u + v\in W$. Sea $r\in W$, ya que $W$ no es vacío, entonces, por la propiedad del conjunto $(-1)r+r=-r+r=0\in W$, lo que indica que $W$ contiene al elemento neutro; así $(-1)r+0=-r\in W$, por lo que $W$ tiene al opuesto de todo sus vectores; en general $\lambda u +0\in W$, es decir el producto por un escalar es cerrado; de este modo, si $u,v\in W$, $u+v=(1)u+v\in W$, por lo que se tiene que la suma es cerrada; de donde se concluye que $W$ es un subespacio. Recíprocamente, si $W$ es un subespacio, por definición se tiene que cumple que $\forall u,v\in W$ y $\forall \lambda\in\mathbb{F}$, $\lambda u + v\in W$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-62"><strong>(\#exm:unnamed-chunk-62) </strong></span>Dado un espacio vectorial $V$, el mismo $V$ es subespacio de $V$. El conjunto cuyo único elemento es el vector cero $\{\vec{0}\}$ es subespacio de $V$, llamado el subespacio nulo de $V$. Estos dos subespacios son los subespacios triviales de $V$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-63"><strong>(\#exm:unnamed-chunk-63) </strong></span>En el espacio $\mathbb{F}^{n}$, el conjunto de las $n$-tuplas $(x_{1}, x_{2},\cdots , x_{n})$ donde $x_{i}=0$, para algún $i$ fijo, es un subespacio de $\mathbb{F}^{n}$. Pero el conjunto de las $n$-tuplas, tales que $x_{i}+kx_{j}=p$ no es un subespacio.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-64"><strong>(\#exm:unnamed-chunk-64) </strong></span>El espacio de las funciones polinómicas es subespacio del espacio de todas las funciones.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-65"><strong>(\#exm:unnamed-chunk-65) </strong></span>Una matriz cuadrada $n\times n$, es una *matriz simétrica* si $a_{ij}=a_{ji}$ para todo $1\leq i,j\leq n$. El conjunto de las matrices simétricas es un subespacio del espacio de las matrices $n\times n$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-66"><strong>(\#exm:unnamed-chunk-66) </strong></span>Una matriz cuadrada $n\times n$ sobre el cuerpo de los números complejos $\mathbb{C}$ es una *matriz hermítica* (o *autoadjunta*) si $a_{jk}=\bar{a_{kj}}$ para todo $1\leq j,k\leq n$, donde la barra sobre el escalar $a_{kj}$ denota la conjugación compleja. El conjunto de las matrices hermíticas es un subespacio sobre el espacio de las matrices cuadradas $n\times n$ sobre $\mathbb{R}$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-67"><strong>(\#exm:unnamed-chunk-67) </strong></span>El espacio de las soluciones de un sistema  homogéneo de ecuaciones. Dada una matriz $A$ $m\times n$, el conjunto de las soluciones, de la ecuación $AX=0$, forman un subespacio del espacio de las matrices $n\times 1$. Para esto basta ver que dadas dos soluciones del sistema $X_{1}$ y $X_{2}$, la matriz $\lambda X_{1} + X_{2}$, con $\lambda$ un escalar cualquiera, es también solución del sistema. Esto es fácil de ver, ya que

$$\begin{array}{cl}
[A(\lambda X_{1}+X_{2})]_{ij}&=\sum_{k=1}^{n} [A]_{ik}[\lambda X_{1}+ X_{2}]_{kj}\\
	                           &=\sum_{k=1}^{n} [A]_{ik}\lambda [X_{1}]_{kj}+ A_{ik}[X_{2}]_{kj}\\
	                           &=\sum_{k=1}^{n} \lambda ([A]_{ik} [X_{1}]_{kj})+ ([A]_{ik}[X_{2}]_{kj})\\
	                           &=\lambda \sum_{k=1}^{n} ([A]_{ik} [X_{1}]_{kj}) + \sum_{k=1}^{n} ([A]_{ik}[X_{2}]_{kj})\\
	                           &=\lambda[AX_{1}]_{ij} + [AX_{2}]_{ij}
\end{array}$$
	 </div>\EndKnitrBlock{example}

De hecho, la demostración del ejemplo anterior se puede generalizar.

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-68"><strong>(\#lem:unnamed-chunk-68) </strong></span>Sea $A$ una matriz $m\times n$ sobre el cuerpo $\mathbb{F}$.

Si $B$ y $C$ matrices $n\times p$ sobre el mismo cuerpo, y $\lambda$ un escalar. Entonces $A(\lambda B + C)=\lambda(AB)+ AC$.

Si $B$ y $C$ matrices $q\times m$ sobre el mismo cuerpo, y $\lambda$ un escalar. Entonces $(\lambda B + C)A=\lambda(BA)+ CA$.
</div>\EndKnitrBlock{lemma}
	
\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-69"><strong>(\#thm:unnamed-chunk-69) </strong></span>Sea $V$ un espacio vectorial. Entonces la intersección de una colección arbitraria de subespacios de $V$, es un subespacio de $V$.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $\{W_{\alpha} \}$ una colección de subespacios de $V$. Sea $W=\bigcap _{\alpha} W_{\alpha}$ la intersección de la colección de subespacios. Note que el vector cero pertece a todo $W_{\alpha}$ ya que cada $W_{\alpha}$ es un subespacio de $V$; por lo tanto el vector cero pertenece a la intersección $W$, así $W$ no es vacío. Sean $u,v\in W$, y $\lambda$ un escalar. Entonces $u,v\in W_{\alpha}$ para todo $\alpha$, como cada $W_{\aleph}$ es un subespacio, se tiene que $\lambda u + v\in W_{\alpha}$ para todo $\alpha$, de donde se sigue que $\lambda u +v\in W$, lo que muestra que $W\prec V$.</div>\EndKnitrBlock{proof}

Del teorema anterior dado un subconjunto no vacío $S$ de un espacio vectorial, podemos construír un subespacio que contenga a $S$ y que sea mínimo (en el sentido de la contención).

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-71"><strong>(\#def:unnamed-chunk-71) </strong></span>Sea $S$ un conjunto de vectores de un espacio vectorial $V$. El *subespacio generado* por $S$ es la intersección de todos los subespacios que contienen a $S$ y se denota $\left\langle S \right\langle$. Es decir, $\left\langle S \right\rangle =\bigcap \{W\prec V : S\subseteq W \}$. Cuando $S$ es un conjunto finito de vectores, $u_{1}, u_{2},\cdots u_{n}$ se denota $\left\langle u_{1}, u_{2},\cdots u_{n} \right\rangle$ y dicimos simplemente que $\left\langle u_{1}, u_{2},\cdots u_{n} \right\rangle$ es el subespacio generado por los vectores $u_{1}, u_{2},\cdots u_{n}$.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-72"><strong>(\#thm:unnamed-chunk-72) </strong></span>Sea $V$ un espacio vectorial y $S\subseteq V$ no vacío. El subespacio generado por $S$, $\left\langle S \right\rangle$, es el conjunto de todas las combinaciones lineales de los vectores de $S$.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $L(S)$ el conjunto de todas las combinaciones lineales de $S$, es decir, $L(S)=\{\sum_{i=1}^{n} \lambda_{i} u_{i}: \lambda_{i}\mbox{ es un escalar, } u_{i}\in S, n\in\mathbb{N} \}$. Es claro que $L(S)\subseteq \left\langle S \right\rangle$, ya que toda combinación lineal de elementos de $S$ es un elemento de $\left\langle S \right\rangle$ (por definición de subespacio).

Ahora, veamos la otra contención. Para esto, veamos que $L(S)$ es un subespacio vectorial que contiene a $S$ (y así tendremos que $\left\langle S \right\rangle\subseteq L(S)$). Primero, como $S\subseteq L(S)$ se tiene que $L(S)$ no es vacío. Sean $v, w\in L(S)$, como combinaciones lineales de combinaciones lineales, vuelven a ser combinaciones lineales (del mismo conjunto de vectores) entonces $\gamma v + w\in L(S)$, lo que muestra que $L(S)$ es un subespacio de $V$ que contiene al conjunto $S$, por ser $\left\langle S \right\rangle$ el menor subespacio con esta propiedad, se tiene que $\left\langle S \right\rangle\subseteq L(S)$.

Por lo que $\left\langle S \right\rangle = L(S)$.</div>\EndKnitrBlock{proof}

Se puede usar $L(S)$ o $\left\langle S \right\rangle$ indistintamente para denotar el subespacio generado por $S$.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-74"><strong>(\#def:unnamed-chunk-74) </strong></span>Sean $S_{1}, S_{2},\cdots, S_{n}\subseteq V$, la suma de $S_{1}, S_{2},\cdots, S_{n}$ es el conjunto de todos las sumas $v_{1}+v_{2}+\cdots + v_{n}$ con $v_{i}\in S_{i}$, para cada $1\leq i\leq n$ y se denota $S_{1}+S_{2}+\cdots+S_{n}$ o $\sum_{i=1}^{n} S_{i}$.</div>\EndKnitrBlock{definition}

Note que si $W_{1}, W_{2}, \cdots, W_{n}$ son subespacios de un espacio vectorial $V$, entonces $W=W_{1}+W_{2}+\cdots +W_{n}$ es subespacio de $V$, que contienen a cada $W_{i}$, con $1\leq i\leq n$. Entonces $W=W_{1}+W_{2}+\cdots +W_{n}=\left\langle W_{1}\cup W_{2}\cdots W_{n}\right\rangle$.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm361"><strong>(\#exm:ejm361) </strong></span>Sean $v_{1}=(1,0,2,0,1), v_{2}=(0,1,0,3,2), v_{3}=(0,0,1,0,0)$ vectores del espacio $\mathbb{R}^{5}$. El subespacio generado por $v_{1}, v_{2}, v_{3}$ es el espacio $\left\langle v_{1}, v_{2}, v_{3}\right\rangle =\{\lambda_{1}v_{1}+\lambda_{2}v_{2}+\lambda_{3}v_{3}: \lambda_{1}, \lambda_{2},\lambda_{3}\in\mathbb{R} \}$. Como $\alpha=\lambda_{1}v_{1}+\lambda_{2}v_{2}+\lambda_{3}v_{3}=(\lambda_{1},\lambda_{2},2\lambda_{1}+\lambda_{3},3\lambda_{2},\lambda_{1}+2\lambda_{2})$, se tiene que $\left\langle v_{1}, v_{2}, v_{3}\right\rangle =\{v\in\mathbb{R}^{5}:(\lambda_{1},\lambda_{2},2\lambda_{1}+\lambda_{3},3\lambda_{2},\lambda_{1}+2\lambda_{2})\mbox{ con } \lambda_{1}, \lambda_{2},\lambda_{3}\in\mathbb{R}\}\subseteq\mathbb{R}^{5}$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-75"><strong>(\#exm:unnamed-chunk-75) </strong></span>Las matrices de la forma 

$$\left[ \begin{array}{cc} 
	a & b\\
	c & 0
	\end{array}\right]\mbox{ con }a,b,c\in\mathbb{R}$$
  
forman un subespacio de $\mathbb{R}^{2\times 2}$. Llamemos $W_{1}=\{A\in\mathbb{R}^{2\times 2}: a_{22}=0  \}$. Sean $A, B\in W_{1}$, entonces $\lambda A + B\in W_{1}$, pues $[\lambda A + B\in W_{1}]_{ij}=\lambda a_{ij} + b_{ij}$ y así, $[\lambda A + B\in W_{1}]_{22}=\lambda a_{22} + b_{22}=0$.

Las matrices de la forma 

$$\left[ \begin{array}{cc} 
	a & 0\\
	0 & b
	\end{array}\right] \mbox{ con } a,b,c\in\mathbb{R}$$
  
también son un subespacio de $\mathbb{R}^{2\times 2}$. Si llamemos $W_{2}=\{A\in\mathbb{R}^{2\times 2}: a_{12}=a_{21}=0  \}$, se tiene que $\mathbb{R}^{2\times 2}=W_{1}+W_{2}$.

También se puede ver que $W_{1}\cap W_{2}$ es el subespacio de las matrices de la forma 

$$\left[ \begin{array}{cc} 
	a & 0\\
	0 & 0
	\end{array}\right]\mbox{ con } a\in\mathbb{R}$$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-76"><strong>(\#exm:unnamed-chunk-76) </strong></span>Sea $A$ una matriz $m\times n$, sobre un cuerpo $\mathbb{F}$. Los *vectores filas* de la matriz $A$ son vectores de $\mathbb{R}^{n}$ dados por $A_{i\ast}=(a_{i1},a_{i2},\cdots, a_{in})$, con $1\leq i\leq n$. El espacio fila de la matriz $A$ es el espacio generado por los vectores fila, es decir, $\left\langle A_{1\ast},A_{2\ast}, \cdots A_{m\ast} \right\rangle $. El subespacio visto en el ejemplo \@ref(exm:ejm361) es exactamente el espacio fila de la matriz 

$$\left[ \begin{array}{ccccc} 
	1 & 0 & 2 & 0 & 1 \\
	0 & 1 & 0 & 3 & 2 \\
	0 & 0 & 1 & 0 & 0
	\end{array}\right]$$
  
Pero también es el espacio fila de la siguiente matriz

$$\left[ \begin{array}{ccccc} 
	1 & 0 & 2 & 0 & 1 \\
	0 & 1 & 0 & 3 & 2 \\
	0 & 0 & 1 & 0 & 0 \\
	-2 & -1 & -3 & -3 & -4
	\end{array}\right]$$
  
Ya que la última fila es combinación lineal de las anteriores. Sim embargo, el espacio fila de la matriz 
	
$$\left[ \begin{array}{ccccc} 
	1 & 0 & 2 & 0 & 1 \\
	0 & 1 & 0 & 3 & 2 \\
	0 & 0 & 1 & 0 & 0 \\
	0 & 0 & 0 & 1 & -1
	\end{array}\right]$$
  
es diferente, esto es porque las filas de esta matriz son linealmente independientes.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-77"><strong>(\#def:unnamed-chunk-77) </strong></span>Un subconjunto $S$ de un espacio vectorial $V$ es *linealmente dependiente* (se puede abreviar l.d.) si existen vectores $v_{1}, v_{2},\cdots ,v_{n}\in S$ distintos y escalares $\lambda_{1}, \lambda_{2}, \cdots , \lambda_{n}$ no todos nulos tales que la combinación lineal $\lambda_{1}v_{1}+\lambda_{2}v_{2}+\cdots +\lambda_{n}v_{n}=0$ sea igual al vector cero.

Un conjunto que no es linealmente dependiente, se llama *linealmente independiente*. Se puede abreviar l.i.</div>\EndKnitrBlock{definition}

Si el conjunto es finito $S=\{v_{1}, v_{2},\cdots ,v_{n}\}$ podemos decir directamente que los vectores $v_{1}, v_{2},\cdots ,v_{n}$ son l.d. o l.i. (según corresponda) obviando el nombre del conjunto $S$.

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Se tiene que:
	
1. Todo conjunto que contiene a un conjunto l.d., es un conjunto l.d.
		
2. Todo subconjunto de un conjunto l.i., es l.i.

3. Todo conjunto que contenga el vector cero es l.d.

4. Un conjunto $S$ es l.i. si y solo si toda combinación lineal de vectores de $S$ que es igual a cero, implica que todos los escalares de dicha combinación lineal son iguales a cero, es decir, si para todo $n\in \mathbb{N}$, $\lambda_{1}v_{1}+\lambda_{2}v_{2}+\cdots +\lambda_{n}v_{n}=0$, donde $v_{i}\in S$ para $0\leq i\leq n$, entonces $\lambda_{1}=\lambda_{2}= \cdots =\lambda_{n}=0$.
	</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-79"><strong>(\#def:unnamed-chunk-79) </strong></span>*Una base* de un espacio vectorial $V$, es un conjunto de vectores linealmente independientes de $V$, cuyo espacio generado coincide con $V$. El espacio $V$ es de *dimensión finita* si tiene una base finita.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-80"><strong>(\#exm:unnamed-chunk-80) </strong></span>Los vectores $v_{1}=(1,0,2,0,1), v_{2}=(0,1,0,3,2), v_{3}=(0,0,1,0,0), v_{4}=(2,1,5,3,4)$ son linealmente dependientes, ya que $2v_{1}+v_{2}+v_{3}-v_{4}=0$. Pero $v_{1}=(1,0,2,0,1), v_{2}=(0,1,0,3,2), v_{3}=(0,0,1,0,0)$ son linealmente independientes, ya que $\lambda v_{1}+\lambda v_{2}+\lambda v_{3}=0$ solo si $\lambda_{1}=\lambda_{2}=\lambda_{3}=0$. Note que cualquier otra combinación lineal (de dos o menos vectores) es igual a cero solo cuando sus escalares son todos cero.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-81"><strong>(\#exm:unnamed-chunk-81) </strong></span>Sean $e_{1}, e_{2}, \cdots ,e_{n}$ vectores de $\mathbb{R}^{n}$ tales que 

$$[e_{i}]_{j}=\left\lbrace \begin{array}{cc}
	1 & \mbox{ si } i=j\\
	0 & \mbox{ si } i\neq j
	\end{array}\right. $$
	  
Donde $[e_{i}]_{j}$ denota la $j-$ésima posición (entrada o coordenada) del vector $e_{i}$. Es decir, los vectores $e_{1}, e_{2}, \cdots ,e_{n}$ son $n$ vectores casi iguales a cero, salvo que en la coordenada $i-$ésima $e_{i}$ es igual a $1$. Serían así:

$$\begin{array}{cl}
	e_{1}=& (1, 0, 0, \cdots , 0, 0)\\
	e_{2}=& (0, 1, 0, \cdots , 0, 0)\\
	\vdots & \vdots \\
	e_{i}=& (0, \cdots, 1,\cdots , 0)\mbox{ , en la posición } i\\
	\vdots & \vdots \\
	e_{n}=& (0, 0, \cdots, 0, 0, 1)
	\end{array}$$
	  
Sea $v=(x_{1}, x_{2},\cdots, x_{n})\in \mathbb{R}^{n}$ un vector cualquiera. Se tiene que $v=(x_{1}, x_{2},\cdots, x_{n})=x_{1}e_{1}+x_{2}e_{2}+\cdots+ x_{n}e_{n}$, lo que muestra que todo vector de $\mathbb{R}^{n}$ se puede escribir como combinación lineal de los vectores $e_{1}, e_{2}, \cdots ,e_{n}$, o lo que es igual, que estos vectores generan a todo el espacio, es decir, $\left\langle e_{1}, e_{2}, \cdots, e_{n}\right\rangle=\mathbb{R}^{n}$.

Ahora es fácil ver que $\{e_{1}, e_{2}, \cdots ,e_{n}\}$ es un conjunto l.i., por lo tanto forman una base para el espacio $\mathbb{R}^{n}$. Lo que nos permite decir que $\mathbb{R}^{n}$ es un espacio de dimensión finita. A la base $\{e_{1}, e_{2}, \cdots ,e_{n}\}$ se le conoce con el nombre de base canónica de $\mathbb{R}^{n}$.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-82"><strong>(\#exm:unnamed-chunk-82) </strong></span>Sea $A\in \mathcal{M}_{n}(\mathbb{F})$ invertible. Sean $A_{1\ast}, A_{2\ast},\cdots, A_{n\ast}$ los vectores fila de la $A$. $A_{1\ast}, A_{2\ast},\cdots, A_{n\ast}$ son l.i. ya que $\lambda_{1} A_{1\ast}+\lambda_{2} A_{2\ast}+\cdots+\lambda_{n} A_{n\ast}=0$ si y solo si $AX=0$, donde $X$ es la matriz $n\times 1$ formada por los $\lambda_{i}$. Como $AX=0\Leftrightarrow X=A^{-1}0\Leftrightarrow \lambda_{1}=\lambda_{2}=\cdots=\lambda_{n}=0$. Además forman una base del espacio de las matrices filas $\mathcal{M}_{1\times n}(F)$: Sea $B=(b_{11} b_{12},\cdots,b_{1n})$, sea $X=A^{-1}B\Leftrightarrow AX=B$. Luego, el espacio de las matrices filas $\mathcal{M}_{1\times n}(F)$, es un espacio de dimensión finita.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-83"><strong>(\#exm:unnamed-chunk-83) </strong></span>El espacio de las funciones polinómicas sobre $\mathbb{R}$.

Sea $S=\{f_{k}(x)=x^{k}: k\geq 0 \}=\{1, x, x^{2},\cdots \}$. Sea $n$ un entero positivo, consideremos la combinación lineal  $f(x)=\lambda_{0}+\lambda_{1}x+\lambda_{2}x^{2}+\cdots + \lambda_{n}x^{n}$, entonces $f(x)=0$ para todo $x\in \mathbb{F}$ si y solo si $\lambda_{1}=\lambda_{2}=\cdots=\lambda_{n}=0$. Por lo tanto $S$ es un conjunto linealmente independiente. Cualquier subconjunto finito de $S$ no genera a todo el espacio, Lo que demuestra que el espacio de las funciones polinómicas es de dimensión infinita.</div>\EndKnitrBlock{example}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-84"><strong>(\#thm:unnamed-chunk-84) </strong></span>Sea $V$ un espacio vectorial generado por un conjunto finito de $n$ vectores $v_{1}, v_{2},\cdots, v_{n}$. Entonces todo subconjunto de $V$ linealmente independiente no tiene mas de $n$ vectores.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Veamos que $S=\{u_{1}, u_{2}, \cdots, u_{m} \}$, con $m\geq n$, es linealmente dependiente. Como $v_{1}, v_{2},\cdots, v_{n}$ generan a todo el espacio $V$, cada $u_{i}$ se escribe como combinación lineal de los $v_{j}$, es decir, 

$$\begin{array}{cc}
		u_{1}=&\lambda_{11}v_{1}+\lambda_{12}v_{2}+\cdots +\lambda_{1n}v_{n}\\
		u_{2}=&\lambda_{21}v_{1}+\lambda_{22}v_{2}+\cdots +\lambda_{2n}v_{n}\\
		\vdots& \ddots\\
		u_{m}=&\lambda_{m1}v_{1}+\lambda_{m2}v_{2}+\cdots +\lambda_{mn}v_{n}
	\end{array} \mbox{ donde } \lambda_{ij} \mbox{ es un escalar }$$
	
Tomemos una combinación lineal de los vectores de $S$ y la igualamos a cero $x_{1} u_{1}+ x_{2} u_{2}+ \cdots+ x_{m} u_{m}=0$, esto es 
		
$$(x_{1},x_{2},\cdots, x_{m}) \left(\left[ \begin{array}{cccc}
		\lambda_{11} & \lambda_{12} & \cdots & \lambda_{1n}\\
		\lambda_{21} & \lambda_{22} & \cdots & \lambda_{2n}\\
		\vdots & & \ddots & \\
		\lambda_{m1} & \lambda_{m2} & \cdots & \lambda_{mn}\\
	\end{array}
	\right] \left[ \begin{array}{c}
		v_{1}\\
		v_{2}\\
		\vdots\\
		v_{n}
	\end{array} \right]  \right)=0 $$
		  
Es decir, 

$$(x_{1},x_{2},\cdots, x_{m}) \left[ \begin{array}{cccc}
	\lambda_{11} & \lambda_{12} & \cdots & \lambda_{1n}\\
	\lambda_{21} & \lambda_{22} & \cdots & \lambda_{2n}\\
	\vdots & & \ddots & \\
	\lambda_{m1} & \lambda_{m2} & \cdots & \lambda_{mn}\\
	\end{array}
	\right] =0\Leftrightarrow \left[ \begin{array}{cccc}
		\lambda_{11} & \lambda_{12} & \cdots & \lambda_{1n}\\
		\lambda_{21} & \lambda_{22} & \cdots & \lambda_{2n}\\
		\vdots & & \ddots & \\
		\lambda_{m1} & \lambda_{m2} & \cdots & \lambda_{mn}\\
	\end{array}
	\right] \left[ \begin{array}{c}
	x_{1}\\
	x_{2}\\
	\vdots\\
	x_{n}
	\end{array} \right] =0$$
		  
Como $m>n$ tiene múltiples soluciones, esto es, existen $x_{1},x_{2},\cdots, x_{m}$ no todos ceros tales que $x_{1} u_{1}+ x_{2} u_{2}+ \cdots+ x_{m} u_{m}=0$, por lo tanto $S$ es linealmente dependiente.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-86"><strong>(\#cor:unnamed-chunk-86) </strong></span>Si $V$ en un espacio de dimensión finita, entonces dos bases cualesquiera tienen el mismo número (finito) de elementos.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Como $V$ es de dimensión finita, tiene una base finita, digamos $B=\{v_{1}, v_{2}, \cdots, v_{n} \}$. Sea $B´$ una base de $V$, entonces $B´$ tiene una cantidad finita de vectores, digamos $B´=\{u_{1}, u_{2}, \cdots, u_{m} \}$ con $m\leq n$. Análogamente, $n\leq m$, por lo tanto $n=m$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-88"><strong>(\#def:unnamed-chunk-88) </strong></span>Llamaremos *dimensión* al número de vectores de una base de un espacio de dimensión finita y se denota $\dim V$.</div>\EndKnitrBlock{definition}

Podemos reformular el teorema anterior en términos de la definición anterior.

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:coro374"><strong>(\#cor:coro374) </strong></span>Sea $V$ un espacio de dimensión finita y sea $n=\dim V$. Entonces:

(1) Cualquier conjunto $S\subseteq V$ que contenga más de $n$ vectores es l.d.

(2) Ningún subconjunto de $V$ que contenga menos de $n$ vectores puede generar a $V$.
</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-89"><strong>(\#exm:unnamed-chunk-89) </strong></span>(1) $\mathbb{R}^{n}$ tiene dimensión $n$. Ya vimos antes que la base canónica de $\mathbb{R}^{n}$ está formada por los vectores $e_{1}, e_{2}, \cdots ,e_{n}$,  
		
$$[e_{i}]_{j}=\left\lbrace \begin{array}{cc}
		1 & \mbox{ si } i=j\\
		0 & \mbox{ si } i\neq j
		\end{array}\right. $$ 
		Luego, toda base de $\mathbb{R}^{n}$ tiene $n$ vectores.
		
(2) El espacio de las matrices de orden $m\times n$, $\mathcal{M}_{m\times n}(\mathbb{F})$, tiene como base al conjunto de matrices $E^{ij}$ de la forma
		
$$[E^{ij}]st=\left\{\begin{array}{cc}
		1 & \mbox{ si } i=s \mbox{ y } j=t\\
		0 & \mbox{ en otro caso }
		\end{array}\right. $$
		  
Hay $mn$ matrices de esta forma, por lo tanto la dimensión del espacio $\mathcal{M}_{m\times n}(\mathbb{F})$ es $mn$.
		
(3) Dada una matriz $A$, el espacio soluci\ón del sistema homogéneo $AX=0$, tiene dimensión igual al número de filas no nulas de la matriz escalonada reducida por filas equivalente a $A$.</div>\EndKnitrBlock{example}

Vamos a convenir dar dimensión cero al espacio nulo.

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-90"><strong>(\#lem:unnamed-chunk-90) </strong></span>Sea $S$ un subconjunto linealmente independiente de un espacio vectorial $V$. Sea $v\in V\setminus\left\langle S \right\rangle$. Entonces $S\cup \{v\}$ es linealmente independiente.</div>\EndKnitrBlock{lemma}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sean $u_{1}, u_{2},\cdots, u_{n}\in S$; tomemos $\lambda_{1}u_{1}+\lambda_{2}u_{2}+\cdots +\lambda_{n}u_{n}+\gamma v=0$, necesariamente $\gamma=0$ porque en otro caso, $v=\gamma^{-1}(\lambda_{1}u_{1}+\lambda_{2}u_{2}+\cdots +\lambda_{n}u_{n})=\gamma^{-1}\lambda_{1}u_{1}+\gamma^{-1}\lambda_{2}u_{2}+\cdots +\gamma^{-1}\lambda_{n}u_{n}$ y así $v\in\left\langle S \right\rangle$. Como $S$ es l.i. se tiene que si $\lambda_{1}u_{1}+\lambda_{2}u_{2}+\cdots +\lambda_{n}u_{n}+\gamma v=0$, entonces $\lambda_{1}u_{1}+\lambda_{2}u_{2}+\cdots +\lambda_{n}u_{n}=0$, por lo tanto,  $\lambda_{1}=\lambda_{2}=\cdots=\lambda_{n}=\gamma=0$ de donde se sigue que $S\cup \{v\}$ es l.i.
</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-92"><strong>(\#thm:unnamed-chunk-92) </strong></span>Sea $V$ un espacio de dimensión finita. Sea $W\prec V$, entonces todo subconjunto $S\subseteq W$ l.i. es finito y es parte de una base de $W$ (esta base debe ser finita).
</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}	Sea $n=\dim V$. Sea $S=S_{0}\subseteq W$ un conjunto l.i. Por el corolario \ref{coro3.72}, $S_{0}$ tiene a lo sumo $n$ vectores. Si $S_{0}$ genera a $W$, esto es $\left\langle S_{0}\right\rangle=W$, el mismo es la base de $W$. Si no, existe $v_{1}\in W\setminus\left\langle S_{0} \right\rangle$, y por el corolario anterior, $S_{1}=S_{0}\cup\{v_{1}\}$ es l.i. Si $\left\langle S_{1}\right\rangle=W$, ya tenemos la base de $W$, sino repetimos el proceso, tomamos $v_{2}\in W\setminus\left\langle S_{1} \right\rangle$ y construimos $S_{2}=S_{1}\cup\{v_{2}\}$ un conjunto l.i. Volvemos a preguntarnos si $S_{2}$ genera al subespacio $W$, si la respuesta es afirmativa, conseguimos la base, si no, continuamos con este proceso hasta hallar $k$ vectores $\{v_{1}, v_{2}, \cdots, v_{k}\}$, que completen una base para el subespacio $W$, a saber $S_{k}=S_{0}\cup \{v_{0}, v_{1}, \cdots, v_{k}\}$. Note que este proceso es finito ya que la dimensión de $V$ es finita.
</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-94"><strong>(\#cor:unnamed-chunk-94) </strong></span>Sea $V$ un espacio vectorial de dimensión finita. Sea $W$ un subespacio propio de $V$. Entonces $\dim W < \dim V$, por lo tanto $W$ es de dimensión finita.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Si $W$ es el subespacio nulo se tiene el resultado de forma trivial. Supongamos que $W$ no es el espacio nulo. Sea $\vDash\in W$, entonces $\{v\}$ es l.i. y por el teorema anterior $v$ pertenece a $B$ una base finita de $W$, y $B$ no tiene mas de $\dim V$ vectores. Por lo tanto $\dim W\leq \dim V$. Pero como $W$ es un subespacio propio de $V$, existe $u\in V\setminus W$, y así $B\cup\{u\}$ es un conjunto l.i., por lo tanto cualquier base de $V$ tiene mas de $\dim W$ elementos, entonces $\dim V > \dim W$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-96"><strong>(\#cor:unnamed-chunk-96) </strong></span>En todo espacio $V$ de dimensión finita, todo conjunto de vectores linealmente independientes es parte de una base.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-97"><strong>(\#cor:unnamed-chunk-97) </strong></span>Sea $A\in\mathcal{M}_{n}(\mathbb{F})$. Si los vectores filas de $A$ son un conjunto linealmente independientes de $\mathbb{F}^{n}$, entonces $A$ es invertible.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sean $v_{1}, v_{2},\cdots, v_{n}$ los vectores filas de $A$ (es decir $v_{i}=A_{i*}$ para cada $1\leq i\leq n$) y supongamos que es un conjunto l.i. Sea $W=\left\langle v_{1}, v_{2},\cdots, v_{n}\right\rangle$, entonces $\dim W=n$, así $W=\mathbb{F}^{n}$. Además, los vectores $e_{i}$, 

$$[e_{i}]_{j}=\left\lbrace \begin{array}{cc}
	1 & \mbox{ si } i=j\\
	0 & \mbox{ si } i\neq j
	\end{array}\right.$$ 

que forman la base canónica de $\mathbb{F}^{n}$ se escriben como combinación lineal de los vectores $v_{1}, v_{2},\cdots, v_{n}$. Esto es, existen escalares $\lambda_{ij}\in \mathbb{F}$ tales que: $e_{i}=\sum_{j=1}^{n} b_{ij}v_{j}$ para cada $1\leq i\leq n$. Es decir, $BA=I$, donde $[B]_{ij}=b_{ij}$.
</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-99"><strong>(\#thm:unnamed-chunk-99) </strong></span>Si $W_{1}$ y $W_{2}$ son subespacios de dimensión finita de un espacio vectorial $V$, entonces $W_{1}+W_{2}$ es de dimensión finita y $\dim W_{1}+\dim W_{2}=\dim (W_{1}\cap W_{2}) + \dim (W_{1}+W_{2})$.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Como $W_{1}\cap W_{2}$ es un subespacio vectorial y $W_{1}\cap W_{2}\subseteq W_{1}$ y $W_{1}\cap W_{2}\subseteq W_{2}$ se sigue que $W_{1}\cap W_{2}$ tiene una base finita $B=\{v_{1}, v_{2},\cdots, v_{k} \}$ que es parte de una base de $W_{1}$, digamos $B_{1}=\{v_{1}, v_{2},\cdots, v_{k}, u_{1}, u_{2}, \cdots, u_{m} \}$ y de base de $W_{2}$, digamos $B_{2}=\{v_{1}, v_{2},\cdots, v_{k}, w_{1}, w_{2}, \cdots, w_{n} \}$ así el subespacio $W_{1}+W_{2}$ es generado por los vectores $v_{1}, v_{2},\cdots, v_{k}, u_{1}, u_{2}, \cdots, u_{m}, w_{1}, w_{2}, \cdots, w_{n}$ los cuales forman un conjunto l.i.
	
En efecto, tomemos la combinación lineal $\sum_{i=1}^{k} \lambda_{i}v_{i} + \sum_{i=1}^{m} \gamma_{i}u_{1} + \sum_{i=1}^{n} \delta_{i}w_{i}=0$ si y solo si 

$$-\sum_{i=1}^{n} \delta_{i}w_{i}=\sum_{i=1}^{k} \lambda_{i}v_{i} + \sum_{i=1}^{m} \gamma_{i}u_{1}.$$
  
Luego $-\sum_{i=1}^{n} c_{i}w_{i}\in W_{1}$. Además $\sum_{i=1}^{n} c_{i}w_{i}\in W_{2}$, entonces $\sum_{i=1}^{n} c_{i}w_{i}\in W_{1}\cap W_{2}$ por lo que $$\sum_{i=1}^{n} c_{i}w_{i}=\sum_{i=1}^{k} a_{i}v_{i},$$ Entonces $\sum_{i=1}^{n} c_{i}w_{i}-\sum_{i=1}^{k} a_{i}v_{i}=0$.

Como $B_{2}$ es una base, se tiene que $\lambda_{1}=\lambda_{2}=\cdots=\lambda_{k}=\delta_{1}=\delta_{2}=\cdots=\delta_{n}=0$, en particular $\delta_{i}=0$ para cada $1 \leq i\leq n$. De este modo $$\sum_{i=1}^{k} \lambda_{i}v_{i} + \sum_{i=1}^{m} \gamma_{i}u_{1}=0.$$ Como $B_{1}$ es base, $\lambda_{1}=\lambda_{2}=\cdots=\lambda_{k}=\gamma_{1}=\gamma_{2}=\cdots=\gamma_{m}=0$, de donde se tiene que $B_{1}\cup B_{2}$ es base de $W_{1}+W-{2}$.

Finalmente, $\dim W_{1}+\dim W_{2}=(k+m)+(k+n)=k+(k+m+n)=\dim (W_{1}\cup W_{2})+\dim (W_{1}+W_{2})$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-101"><strong>(\#def:unnamed-chunk-101) </strong></span>El *rango fila* de una matriz $A$ de orden $n\times m$, es la dimensión del espacio fila de la $A$. </div>\EndKnitrBlock{definition}

Note que, si $P\in\mathcal{M}_{k\times m}(\mathbb{R})$, entonces $B=PA\in\mathcal{M}_{k\times n}(\mathbb{R})$ por lo tanto sus vectores fila son $v=P_{i1}u_{1}+P_{i2}u_{2}+\cdots+P_{im}u_{m}$, donde $P_{ij}=[P]_{i1}$ y $u_{j}=A_{j\ast}=(a_{j1}, a_{j2},\cdots, a_{jn})$. Entonces, el espacio fila de $B$ es un subespacio del espacio fila de $A$. Si $P$ es una matriz invertible $m\times m$, entonces $A=P^{-1}B$ y de forma análoga, el espacio fila de la matriz $A$ es subespacio del espacio fila de la matriz $B$. Esto lo describimos en el siguiente teorema.

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-102"><strong>(\#thm:unnamed-chunk-102) </strong></span>Las matrices equivalentes por filas tienen el mismo espacio fila.</div>\EndKnitrBlock{theorem}

Así solo basta estudiar el espacio fila de la matriz escalón reducida por filas.

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-103"><strong>(\#thm:unnamed-chunk-103) </strong></span>Sea $R$ una matriz escalón reducida por filas, no nula. Entonces los vectores filas no nulas de $R$ forman una base del espacio fila de $R$.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $R\in\mathcal{M}_{n}(\mathbb{R})$ como en la hipótesis. Sean $s_{1}, s_{2},\cdots, s_{r}$ los vectores filas no nulos de $R$, esto es, $r_{i}=(s_{i1}, s_{i2},\cdots, s_{in})$ para todo $1\leq i\leq r$. Es claro que $s_{1}, s_{2},\cdots, s_{r}$ generan el espacio fila de $R$. Como $R$ es escalón reducida por filas, se tiene que existen $k_{1}<k_{2}<\cdots<k_{r}\in\mathbb{N}$ tales que $[R]_{ij}=0$ si $j<k_{i}$ y $[R]_{ik_{j}}=\delta_{ij}$.

Consideremos $\lambda_{1}s_{1}+ \lambda_{2}s_{2}+\cdots+ \lambda_{r}s_{r}=0$ si y solo si $\lambda_{1}=\lambda_{2}=\cdots=\lambda_{r}$ ya que $\lambda_{1}s_{1}+ \lambda_{2}s_{2}+\cdots+ \lambda_{r}s_{r}=(b_{1}, b_{2}, \cdots, b_{n})$ si y solo si $b_{k_{j}}=\sum_{i=1}^{r} \lambda_{i}s_{ik_{j}}=\lambda_{j}s_{jk_{j}}=\lambda_{j}$ por lo tanto $s_{1}, s_{2},\cdots, s_{r}$ son l.i.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-105"><strong>(\#thm:unnamed-chunk-105) </strong></span>Sean $m$ y $n$ enteros positivos y sea $W$ un subespacio de $\mathbb{R}^{n}$ tal que $\dim W\leq m$. Entonces existe una única matriz escalón reducida por filas $m\times n$ que tiene a $W$ como espacio fila.</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sean $v_{1}, v_{2}, \cdots, v_{m}\in\mathbb{R}^{n}$ vectores generadores de $W$.

Sea $A$ una matriz $m\times n$ cuyas filas son los vectores $v_{i}$, es decir, $A_{i\ast}=v_{i}$ para cada $1\leq i\leq m$. Si $R$ es una matriz escalón reducida por filas equivalente a la matriz $A$, entonces $W$ es el espacio fila de la matriz $R$ y por lo tanto de la matriz $A$.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-107"><strong>(\#cor:unnamed-chunk-107) </strong></span>Cada matriz $A$ es equivalente por filas a una y solo una mtriz escalón reducida por filas.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Si dos matrices escalón reducida por filas tienen el mismo espacio fila,  entonces ellas son identicas.</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{corollary}<div class="corollary"><span class="corollary" id="cor:unnamed-chunk-109"><strong>(\#cor:unnamed-chunk-109) </strong></span>Dos matrices $A$ y $B$ son equivalentes por filas si y solo si $A$ y $B$ tienen el mismo espacio fila.</div>\EndKnitrBlock{corollary}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Es claro que si $A\sim B$, entonces $A$ y $B$ tienen el mismo espacio fila.

Supongamos que $A$ y $B$ tienen el mismo espacio fila. Sean $R$ y $S$ dos matrices escalonadas reducidas por fila, equivalentes a $A$ y $B$ respectivamente. Como $R\sim A$ y $B\sim S$, entonces $R$ y $S$ tienen el mismo espacio fila, luego $R=S$ de donde se tiene que $A\sim B$.
</div>\EndKnitrBlock{proof}

### Espacio cociente

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-111"><strong>(\#def:unnamed-chunk-111) </strong></span>Sea $W$ un subespacio de un espacio vectorial $V$. Si $u$ y $v$ son vectores en $V$, diremos que *$u$ es congruente con $v$ módulo $W$* si el vector $v-u\in W$. Esto lo denotaremos $u\cong v\mbox{ mó d }W$.
</div>\EndKnitrBlock{definition}

La congruencia módulo $W$, es una relación de equivalencia sobre $V$:

(a) $u\cong u\mbox{ mó d }W$, ya que $u-u=0\in W$.

(b) $u\cong v\mbox{ mó d }W$ si y solo si $-1(u-v)\in W$ si y solo si $v\cong u\mbox{ mó d }W$.

(c) Si $u\cong v\mbox{ mó d }W$ y $v\cong w\mbox{ mó d }W$, entonces $w-u=w-v+v-u\in W$ si y solo si $u\cong w\mbox{ mó d } W$.

Las clases de equivalencia de un vector $v\in V$ es el conjunto $[v]:=\{u\in V: u\cong v\mbox{ mó d } W \}=\{u\in V: v-u\in W \}=v+W$. A los conjuntos $v+W$ los llamaremos clases laterales de $W$.
	
## Ejercicios

(1) Muestre que el conjunto de las matrices hermíticas $n\times n$ es un espacio vectorial sobre el conjunto de los números reales $\mathbb{R}$.

Respuesta: Sea $V$ el conjunto de las matrices $n\times n$ de la forma 

$$\left[ \begin{array}{cccc}
		x_{11}+iy_{11} & x_{12}+iy_{12} & \cdots & x_{1n}+iy_{1n}\\
			x_{21}+iy_{21} & x_{22}+iy_{22} & \cdots & x_{2n}+iy_{2n}\\
			\vdots        & \vdots        & \ddots & \vdots       \\
			x_{n1}+iy_{n1} & x_{n2}+iy_{n2} & \cdots & x_{nn}+iy_{nn}
	\end{array}\right] $$

tal que $a_{jk}=x_{jk}+iy_{jk}=x_{kj}-iy_{kj}=\overline{x_{kj}+iy_{kj}}=\overline{a_{kj}}$; sea el conjunto de los números reales $\mathbb{R}$, el conjunto de escalares y consideremos las operaciones de suma y producto por un escalar las usuales para las matrices. Entonces se tiene que:

(i) La suma de matrices en $V$ es cerrada: Sean $A, B\in V$, como $\overline{a_{jk}+b_{jk}}=\overline{a_{kj}}+\overline{b_{kj}}$, entonces $\forall A,B\in V$, $A+B\in V$.

(ii) La suma en $V$ es conmutativa: ya que la suma de números complejos es conmutativa.

(iii) La suma en $V$ es asociativa: se sigue de la propiedad asociativa de los números complejos.

(iv) Existe el elemento neutro: la matriz nula es hermítica.

(v) Existencia del elemento opuesto: dada la una matriz $A\in V$, $-A$ es hermítica.

(vi) El producto de una matriz por un escalar, es cerrada: como $\lambda \overline{x_{jk}+iy_{jk}}=\lambda (x_{jk}-iy_{jk})=\lambda x_{jk}-\lambda iy_{jk}$, se tiene que $\lambda A$ es hermítica, si $A$ es hermítica.

(vii) Claramente $1A=A$ para todo $A\in V$, ya que $1(x_{jk}+iy_{jk})=x_{jk}+iy_{jk}$.

(viii) Sean $\lambda,\gamma\in\mathbb{R}$ y $A\in V$, se tiene que $(\lambda\gamma) a_{jk}=(\lambda\gamma)(x_{jk}+iy_{jk})=(\lambda\gamma) x_{jk}+(\lambda\gamma) iy_{jk}=\lambda(\gamma x_{jk})+\lambda(\gamma iy_{jk})=\lambda(\gamma (x_{jk}+ iy_{jk}))=\lambda(\gamma a_{jk})$, por lo tanto $(\lambda\gamma)A=\lambda(\gamma A)$.

(ix) Para todo $A, B\in V$ y todo $\lambda\in\mathbb{R}$, $\lambda(a_{jk}+b_{jk})=\lambda a_{jk} + \lambda b_{jk}$ ya que el producto por un escalar es distributivo respecto de la suma de números complejos.

(x) Para todo $A\in V$ y todo $\lambda,\gamma\in\mathbb{R}$, $(\lambda+\gamma)a_{jk}=\lambda a_{jk} + \gamma a_{jk}$ ya que el producto por un escalar es distributivo respecto de la suma de números complejos.

De donde se sigue que $(V,\mathbb{R},+,\cdot)$ es un espacio vectorial.
