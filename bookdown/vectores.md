# Vectores

En este capítulo estudiaremos los vectores, objetos muy usados en la física para representar distintas nociones en las que se deben representar magnitudes,  direcciones y orientación, como lo son el desplazamiento, la velocidad, la fuerza, etc.  Sin embargo, se puden definir los vectores desde una perspectiva más abstracta, como los elementos de un espacio vectorial. En este capítulo nos centraremos en la noción más natural (como en la física) para desrrollar y mostrar las propiedades y operaciones de los vectores, estudiando los vectores en espacios euclideanos.

##Representación geométrica

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-1"><strong>(\#def:unnamed-chunk-1) </strong></span>	Un **vector** $v$ en $\mathbb{R}^{n}$ de dimensión $n$ es una n-tupla de $n$ números reales, de la forma $v=(a_{1}, a_{2},\cdots, a_{n})$. Llamaremos componente $i-$ésima al número $a_{i}$ ($1\leq i\leq n$).
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	Los vectores en $\mathbb{R}^{2}$ pueden representarse como un segmento de recta dirigido (una flecha) determinado por dos puntos en el espacio, $A$ de coordenadas $(x_{A},y_{A})$ y $B$ de coordenadas $(x_{B},y_{B})$, en los que uno es el origen del vector y el otro el extremo, en este caso se denota $\vec{AB}$ y sus coordenadas en el plano serían $\vec{AB}=(x_{B}-x_{A}, y_{B}-y_{A})$. también se puede denotar el vector con una letra minúscula $v=\vec{AB}$. La recta por la que pasa el vector es la **dirección** del vector. 
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-3"><strong>(\#def:unnamed-chunk-3) </strong></span>	La longitud del segmento de recta que define el vector (es decir, la flecha) es la **magnitud** del vector y se denota por $|\vec{AB}|$ (o $|v|$). La **dirección** del vector corresponde a la inclinación de la recta sobre la cual está el vector, esto es el ángulo que forma el vector con la horizontal. La **orientación** o **sentido** del vector representa el sentido en que se recorre el segmento de recta (determina hacia donde apunta la flecha). 
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	Los vectores $\vec{AB}$ y $\vec{BA}$ tienen la misma magnitud, la misma dirección pero sentidos contrarios, por lo que $\vec{BA}=-\vec{AB}$. Los coordenadas de un vector describen un rectángulo en el plano $\mathbb{R}^{2}$ en el que el vector es una de las diagonales (insertar imagen). 
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-5"><strong>(\#def:unnamed-chunk-5) </strong></span>	Dado el vector $v$ de coordenadas $(x,y)$, la magnitud puede calcularse usando el teorema de pitágoras, con $|v|=\sqrt{x^{2}+y^{2}}$; y el ángulo $\theta$ que forma con el eje de las abscisas con $\theta=\arctan(\frac{y}{x})$. El sentido es una noción referencial y se representan sentidos contrarios con los signos positivos ($+$) y negativos ($-$) (el signo $+$ suele omitirse)
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-6"><strong>(\#def:unnamed-chunk-6) </strong></span>	Dos **vectores** son **paralelos** si forman iguales ángulos con el eje de las abscisas. Es decir, $v_{1}=(x_{1},y_{1})$ y $v_{2}=(x_{2},y_{2})$ son paralelos si $\theta_{1}=\arctan(\frac{y_{1}}{x_{2}})=\theta_{2}=\arctan(\frac{y_{2}}{x_{2}})$.
</div>\EndKnitrBlock{definition}

##Operaciones de vectores

Ya vimos que los que los vectores pueden representar conceptos físicos como lo son la distancia, la velocidad o la fuerza. Entonces es conveniente poder sumar estos objetos, para representar suma de distancias o suma de fuerzas, etc. También podemos pensar en multiplicar un vector por un escalar, como sería multiplicar la magnitud de una fuerza. En esta sección veremos que podemos definir varias operaciones entre vectores, sumar, restar y multiplicar vectores como lo hacemos con los números reales. Pero también definirimos operaciones propias de estos objetos, como lo son el producto punto y el producto cruz de vectores.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-7"><strong>(\#def:unnamed-chunk-7) </strong></span>	Dados los vectores $v_{1}=(x_{1},y_{1})$ y $v_{2}=(x_{2},y_{2})$, **la suma** de $v_{1}$ y $v_{2}$ está dada por la suma de las componentes correspondientes, es decir, $v_{1}+v_{2}=(x_{1}+x_{2},y_{1}+y_{2})$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	La suma de vectores tiene las siguientes propiedades:

		(1) Es commutativa, es decir, $v_{1}+v_{2}=v_{2}+v_{1}$, para cuales quiera vectores $v_{1}, v_{2}$.
		(2) Es asociativa, esto es, $(v_{1}+v_{2})+v_{3}=v_{1}+(v_{2}+v_{3})$, para todo $v_{1}, v_{2}$ y $v_{3}$.
		(3) Existencia del elemento neutro o vector cero,  $v+\vec{0}=v$, para todo vector $v$. 
		(4) Para todo vector $v$, existe un vector $v´$ tal que $v+(v´)=\vec{0}$. 
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-9"><strong>(\#def:unnamed-chunk-9) </strong></span>	Dado el vector $v=(x,y)$ , el **vector opuesto** a $v$ es el vector $-v$ dado por el producto de $v$ por el escalar $-1$, es decir, $-v=-1 v=(-x,-y)$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-10"><strong>(\#def:unnamed-chunk-10) </strong></span>	Dado el vector $v=(x,y)$ y un escalar $\lambda\in\mathbb{R}$, **el producto** de $v$ **por un escalar** $\lambda$ está dada por la multiplicación de cada una de las componentes por el escalar, es decir, $\lambda v=(\lambda x,\lambda y)$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	El producto de vectores por un escalar tiene las siguientes propiedades:
	
		(1) Es **commutativa**, es decir, $\lambda v=v\lambda$, para cualquier vector $v$ y cualquier escalar $\lambda$.
		(2) Es **distributiva**, esto es, $\lambda(v_{1}+v_{2})=\lambda v_{1}+\lambda v_{2}$, para todo $v_{1}, v_{2}$ y todo $\lambda$.
		(3) Existencia del **elemento neutro**,  $1v=v$, para todo vector $v$. 
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-12"><strong>(\#def:unnamed-chunk-12) </strong></span>		Dados los vectores $v_{1}=(x_{1},y_{1})$ y $v_{2}=(x_{2},y_{2})$, **la resta** de $v_{1}$ y $v_{2}$ está dada por la suma de $v_{1}$ con el opuesto de $v_{2}$, es decir, $v_{1}-v_{2}=(x_{1},y_{1})-(x_{2},y_{2})=(x_{1}-x_{2},y_{1}-y_{2})$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-13"><strong>(\#exm:unnamed-chunk-13) </strong></span>	Dados los vectores $v_{1}=(10,2)$, $v_{2}=(-5,4)$ y $v_{3}=(-1,-2)$, entonces $$v_{1}+v_{2}=(10,2)+(-5,4)=(10-5,2+4)=(5,6),$$
	 $$v_{1}-v_{2}=(10,2)-(-5,4)=(10-(-5),2-4)=(15,-2) \mbox{ y}$$ $$v_{3}+v_{2}-v_{1}=(-1,-2)+(-5,4)-(10,2)=(-1-5-10,-2+4-2)=(-16,0).$$ También	 
	$$-2v_{1}=-2(10,2)=(-20,-4)\mbox{ y }$$ $$-2v_{1}+3v_{2}-v_{3}=-2(10,2)+3(-5,4)-1(-1,-2)=(-20-15+1,-4+12+2)=(-34,10).$$
</div>\EndKnitrBlock{example}
\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-14"><strong>(\#def:unnamed-chunk-14) </strong></span>	Sean $v_{1}$ y $v_{2}$ vectores, el **producto escalar** de $v_{1}$ y $v_{2}$ es el producto de los módulos $|v_{1}|$ y $|v_{2}|$ y el coseno del ángulo que forman los vectores y se denota $v_{1}\cdot v_{2}$. Es decir, $v_{1}\cdot v_{2}=|v_{1}||v_{2}|\cos \theta$, donde $\theta$ es el ángulo entre $v_{1}$ y $v_{2}$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	La proyección de $v_{1}$ sobre $v_{2}$ es $proy_{v_{2}} v_{1}=|v_{1}|\cos\theta$ donde $\theta$ es el ángulo que forman ambos vectores. Por lo tanto, $v_{1}\cdot v_{2}=|v_{2}| proy_{v_{2}} v_{1}$.
	También podemos calcular el producto escalar del siguiente modo: Sean $v_{1}=(x_{1}, y_{1})$ y $v_{2}=(x_{2}, y_{2})$ vectores, $v_{1}\cdot v_{2}=x_{1}x_{2}+y_{1}y_{2}$. En general, si $v_{1}$ y $v_{2}$ son vectores en $\mathbb{R}^{n}$ tales que $v_{1}=(x_{1},x_{2},\cdots, x_{n})$ y $v_{2}=(y_{1},y_{2},\cdots, y_{n})$, $v_{1}\cdot v_{2}=\sum_{i=1}^{n} x_{i}y_{i}$.
	</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-16"><strong>(\#exm:unnamed-chunk-16) </strong></span>	Dados los vectores $v=(\sqrt{3},1)$ y $u=(\frac{3}{2},\frac{3\sqrt{3}}{2})$, y sabiendo que el ángulo que ellos forman es 30\textdegree, entonces el producto escalar entre ellos $$v\cdot u=|v||u|\cos 30=2\cdot 3\cdot\frac{\sqrt{3}}{2}=3\sqrt{3}$$, ya que $|v|=\sqrt{\sqrt{3}^{2}+1^{2}}=\sqrt{4}=2$ y $|u|=\sqrt{(\frac{3}{2}^{2})+(\frac{3\sqrt{3}}{2})^{2}}=\sqrt{\frac{36}{4}}=3$. Note que si usamos la fórmula analítica podemos calcular el producto escalar $v\cdot u=(\sqrt{3}\cdot \frac{3}{2}) + (1\cdot \frac{3\sqrt{3}}{2})=3\sqrt{3}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-17"><strong>(\#exm:unnamed-chunk-17) </strong></span>	Dados los vectores $v=(1,2)$ y $u=(-3,4)$, el producto escalar es $v\cdot u=1\cdot (-3)+(2\cdot 4)$. Si queremos calcular el ángulo $\alpha$ entre los vectores, usamos la fórmula $v\cdot u=|v||u|\cos\alpha$, como $|v|=\sqrt{1^{2}+2^{2}}=\sqrt{5}$ y $|v|=\sqrt{(-3)^{2}+4^{2}}=5$, entonces $\cos\alpha=\frac{5}{\sqrt{5}\cdot 5}$, por lo tanto $\alpha=\arccos\frac{1}{\sqrt{5}}$.
</div>\EndKnitrBlock{example}
