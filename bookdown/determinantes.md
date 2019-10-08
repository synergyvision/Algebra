#Determinantes

Volveremos sobre el tema de las matrices no solo sobre un cuerpo, sino que lo haremos para matrices cuyos elementos son parte de un anillo comunitativo por unidad.

Recordemos que un anillo comutativo con unidad es un conjunto $K$ con dos operaciones que cumple con los axiomas de grupo para la suma, y con el producto cumple los axiomas de grupo salvo la condición de existencia de un inverso. Un ejemplo natural de anillo conmutativo es el conjunto de los números enteros. Otro ejemplo sería los polinomios sobre un cuerpo. Todo esto ya fué estudiado en el capítulo 1.

Dado un anillo conmutativo con unidad $K$, consideremos la matriz $m\times n$ sobre $K$, esto es una función $A$ de $\{1,2,\cdots, m \} \times \{1,2,\cdots, n \}$ en $K$, que a cada par $(i,j)$ le asigna un elemento $k_{ij}$ de $K$, es decir $A(i,j)=k_{ij}$ tambien denotado por $[K]_{ij}$. La suma y el producto de matrices las definimos como es usual (igual que en las matrices sobre un cuerpo), dadas las matrices $A$ y $B$ sobre el anillo $K$, la matriz suma $A+B$ es la matriz $$(A+B)_{ij}=A_{ij}+B_{ij}$$
y el producto $AB$ es la matriz $$(AB)_{ij}=\sum_{k} A_{ik}B_{kj}$$ 

El resto de las propiedades y resultados vistos antes para matrices con coeficientes en un cuerpo, funcionan igual cuando los coeficientes de la matriz pertenecen a un anillo, salvo los resultados que involucren inversos multiplicativos (dividir). De este modo, las propiedades algebraicas funcionan igual, por ejemplo, la propiedad distributiva del producto respecto a la suma, $A(B+C)=AB+AC$, etc.

Para definir la función determinante podemos seguir dos rutas, la primera y m?s com?n es dando la fórmula explícita del calculo del determinante de una matriz. Un ejemplo de esto es definir el determinante de una matriz cuadrada $A$ de orden $2$ como:
$$ A_{11}A_{22}-A_{12}A_{21}.$$
Para una matriz $3\times 3$, la fórmula se complica un poco mas; suponga que $B$ es una matriz cuadrada de orden $3$, entonces su determinante es:
$$B_{11}B_{22}B_{33}+B_{12}B_{23}B_{31}+B_{21}B_{32}B_{13}-B_{13}B_{22}B_{31}-B_{23}B_{32}B_{11}-B_{12}B_{21}B_{33}.$$
Y si se quiere definir el determinante de una matriz $4\times 4$, la fórmula es aún mas complicada.
El otro camino para definir el determinante de una matriz es definiendo en abstracto una función que se comporte como queremos y luego demostrar que esta función es única (y que coincide con el determinante conocido, es decir, con la fórmula). Este último es el camino que seguiremos.

En la primera parte del capítulo nos dedicaremos a definir la "función determinante" y mostrar que tal función existe. Luego nos dedicaremos a estudiar dicha función.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-1"><strong>(\#def:unnamed-chunk-1) </strong></span>Sea $K$ un anillo conmutativo con unidad, $n$ un entero positivo. Sea $D$ una función que a cada matriz $A$ sobre $K$, de orden $n$ le asigna un escalar $D(A)$ en $K$. Decimos que $D$ es *$n$-lineal* si para cada $i$, $1\leq i\leq n$, $D$ es una función lineal para la fila $i$-ésima cuando las otras $n-1$ filas se dejan fijas.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}En la definición anterior, decir que la función $D$ es lineal en la fila $i$ es equivalente a decir que si $v_{1}, v_{2},\cdots , v_{n}$ son las $n$ filas de la matriz $A$, y se considera la funci?n $D$ solo respecto de la fila $i$, se tiene que $$D(v_{1}, v_{2},\cdots \lambda v_{i}+u_{i},\cdots, v_{n})=\lambda D(v_{1}, v_{2},\cdots v_{i},\cdots, v_{n})+D(v_{1}, v_{2},\cdots u_{i},\cdots, v_{n}).$$ Otra forma de verlo es pensar en la linealidad de la función $D$ cuando se considera una matriz $B$ donde $B_{rj}=0$ si $r\neq i$, donde se cumple que $D(\lambda A+B)=\lambda D(A)+D(B)$.
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-3"><strong>(\#exm:unnamed-chunk-3) </strong></span>Sea $D$ la función que a cada matriz $A$ sobre $K$ de orden $n$, le asigna el valor $D(A)=\prod_{r=1}^{n}A_{rr}=A_{11}A_{22}\cdots A_{nn}$. $D$ es una función $n$-lineal. En efecto, para cada $i$, $1\leq i\leq n$, si consideramos otra matriz $B$ sobre $K$, de oreden $n$, y consideramos a $D$ como una función de la $i$-ésima fila, se tiene que 
$\begin{array}{rl}
D(\lambda A+B)=&(A_{11})(A_{22})\cdots (\lambda A_{ii}+B_{ii}) \cdots (A_{nn})\\
=&(A_{11})(A_{22})\cdots (A_{nn})) (\lambda A_{ii}+B_{ii})\\
=&\lambda ((A_{11})(A_{22})\cdots (A_{nn}))A_{ii}+ ((A_{11})(A_{22})\cdots (A_{nn}))B_{ii})\\
\lambda D(A) + D(B)
\end{array}$
  </div>\EndKnitrBlock{example}

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-4"><strong>(\#lem:unnamed-chunk-4) </strong></span>Una combinación lineal de funciones $n$-lineales, es una función $n$-lineal.</div>\EndKnitrBlock{lemma}
\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Basta considerar la combinación lineal de dos funciones $n$-lineales. Sean $D$ y $E$ dos funciones $n$-lineales y $a\in K$.
Como $(aD+E)(A)=aD(A)+E(A)$ para toda matriz $A$, entonces al fijar la fila $i$ de las matrices $A$ y $B$, considerando un escalar $c\in K$ y $D$ y $E$ son $n$-lineales, se tiene que 
$$\begin{array}{rl}
(aD+E)(cA_{\ast i}+B_{\ast i})=&aD(cA_{\ast i}+B_{\ast i})+E(cA_{\ast i}+B_{\ast i})\\
=&acD(A_{\ast i})+aD(B_{\ast i})+cE(A_{\ast i})+E(B_{\ast i})\\
=&c(aD(A_{\ast i})+E(A_{\ast i}))+(aD(B_{\ast i})+E(B_{\ast i}))\\
=&c(aD+E)(A_{\ast i})+(aD+E)(B_{\ast i})
\end{array}.$$
  </div>\EndKnitrBlock{proof}

El lema anterior nos permite asegurar que el conjunto de funciones $n$-lineales es un subespacio del espacio de las funciones de $\mathcal{M}_{n}$, el espacio de las matrices $n\times n$, en el cuerpo $K$.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm65"><strong>(\#exm:ejm65) </strong></span>La función $D$ definida en el espacio de las matrices cuadradas de orden $2$, como $D(A)=A_{11}A_{22}-A_{12}A_{21}$ es una función bilineal que es combinación lineal de las funciones bilineales $D_{1}(A)=A_{11}A_{22}$ y $D_{2}(A)=A_{12}A_{21}$. En efecto $D=D_{1}-D_{2}$. Es claro que la función $D$ es exactamente el determinante de matrices $2\times 2$. Pero la función $D$ tiene mas propiedades que ser la combinación lineal de funciones bilineales:
(1) $D(I)=1$.
(2) $D(A)=0$, si las filas de $A$ son iguales.
(3) $D(B)=-D(A)$ si $B$ se obtiene de intercambiar las filas de $A$. En efecto, si $B=e_{12}A$ ($B$ se obtiene de intercambiar las filas $1$ y $2$ de $A$), entoces $B_{\ast 1}=A_{\ast 2}$ y $B_{\ast 2}=A_{\ast 1}$. As? 
$$\begin{array}{rl}
D(B)=&B_{11}B_{22}-B_{12}B_{21}\\
=&A_{21}A_{21}-A_{22}A_{11}\\
=&-(A_{22}A_{11}-A_{21}A_{21})\\
=&-D(A)
\end{array}$$
  </div>\EndKnitrBlock{example}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-6"><strong>(\#def:unnamed-chunk-6) </strong></span>Sea $D$ una función n-lineal. Se dice que $D$ es *alternada* si se tiene que:
(i) $D(A)=0$ cuando $A$ tiene dos filas iguales.
(ii) $D(B)=-D(A)$ cuando $B$ se obtiene al aplicar una y solo una operaci?n de cambio de filas a $A$. 
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-7"><strong>(\#def:unnamed-chunk-7) </strong></span>Sea $K$ un anillo conmutativo con unidad y sea $n\in\mathbb{N}$. Sea $D$ una función de $\mathcal{M}_{n}$ en $K$. Decimos que $D$ es una *función determinante* si
(i) es $n$-lineal,
(ii) es alternada y
(iii) $D(I)=0$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-8"><strong>(\#exm:unnamed-chunk-8) </strong></span>La función definida en el ejemplo \@ref(exp:ejem65) es una función determinante. Ya se vió que es $2$-lineal. Es fácil ver que $D(I)=1$ para la matriz identidad $2\times 2$. En efecto, 
$$D\left(\begin{array}{cc}
1&0\\
0&1
\end{array} \right) =1+0=1$$
Y es alternada, ya que
$$\begin{array}{rl}
D\left(\begin{array}{cc}
a&b\\
c&d
\end{array} \right)=&ad-bc\\
=&-(cb-da)\\
=&-D\left(\begin{array}{cc}
c&d\\
a&b
\end{array} \right)\\
\end{array}
$$
  </div>\EndKnitrBlock{example}

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-9"><strong>(\#lem:unnamed-chunk-9) </strong></span>Sea $D$ una función $2$-lineal con la propiedad: si $A$ es una matriz $2\times 2$ con dos filas iguales, $D(A)=0$. Entonces $D$ es alternada.</div>\EndKnitrBlock{lemma}
\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $B$ una matriz que se obtiene de $A$ intercambiando filas. Sean $A_{1\ast}$ y $A_{2\ast}$ la primera y segunda fila de $A$ y $B_{1\ast}$ y $B_{2\ast}$ las respectivas filas de $B$; note que $B_{1\ast}=A_{2\ast}$ y $B_{2\ast}=A_{1\ast}$. Además 
$$\begin{array}{rl}
D(A+B)=&D(A_{1\ast}+B_{1\ast},A_{2\ast}+B_{2\ast})\\
=&D(A_{1\ast}+A_{2\ast},A_{2\ast}+A_{1\ast})\\
\end{array}.$$
Como $D$ es $2$-lineal, se tiene que:
$$\begin{array}{rl}
D(A+B)=&D(A_{1\ast}+A_{2\ast},A_{2\ast}+A_{1\ast})\\
=&D(A_{1\ast},A_{2\ast}+A_{1\ast})+D(A_{2\ast},A_{2\ast}+A_{1\ast})\\
=&D(A_{1\ast},A_{1\ast})+D(A_{1\ast},A_{2\ast})+D(A_{2\ast},A_{1\ast})+D(A_{2\ast},A_{2\ast})\\
=&D(A_{1\ast},A_{2\ast})+D(A_{2\ast},A_{1\ast})
\end{array}.$$
Por hipótesis, $D(A+B)=0$ y $D(A_{1\ast},A_{1\ast})=D(A_{2\ast},A_{2\ast}=0)$, entonces
$$0=D(A_{1\ast},A_{2\ast})+D(A_{2\ast},A_{1\ast})$$
por lo tanto,
$$D(A_{1\ast},A_{2\ast})=-D(A_{2\ast},A_{1\ast}).$$
  </div>\EndKnitrBlock{proof}

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-11"><strong>(\#lem:unnamed-chunk-11) </strong></span>Sea $D$ una función $n$-lineal de las matrices $n\times n$ sobre $K$. Supóngase que $D$ tiene la propiedad: si $A$ es una matriz $n\times n$ con dos filas adyacentes iguales, $D(A)=0$. Entonces $D$ es alternada.</div>\EndKnitrBlock{lemma}
\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $B$ una matriz que se obtiene de $A$ al intercambiar dos filas adyacentes. Por un razonamiento análogo al anterior se sigue que $D$ es alternada. Ahora, si $B$ es el resultado de alternar dos filas cuales quiera de $A$, dig?áos $1\leq i<j\leq n$, podemos obetener $B$ por una sucesión de intercambio de filas adyacentes. Cambiaríamos la fila $i$ con la fila $i+1$, luego la fila $i+1$ (donde yace la fila $i$ de $A$) con la $i+1$ y así sucesivamente hasta alcanzar la posición $j$-ésima; estas son $j-i$ operaciones. De igual forma <subimos> la fila $j$ de $A$ (que ahora yace en la fila $j-1$) aplicando intercambio de filas adyacentes, estas son $j-i-1$ operaciones elementales. De este modo, la operación $e_{ij}(A)$ es igual a aplicar $(j-i)+(j-i+1)=2(j-i)+1$ operaciones de intercambio de filas adyacentes, para las cuales se tiene la propiedad de $D(\hat{A})=-D(A)$. Así $D(B)=(-1)^{2k-1}D(A)=-D(A)$. Ahora, supongamos que $A$ es una matriz con dos filas iguales, digamos $1\leq i<j\leq n$. Si son adyacentes, es decir, $j=i+1$, por hipótesis, $D(A)=0$, si $j>i+1$, intercambiando la fila $A_{j\ast}$ con la fila $A_{i+1\ast}$ obtenmos una matriz $B$ tal que $D(B)=0$, entonces $D(A)=-D(B)=0$.
</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-13"><strong>(\#def:unnamed-chunk-13) </strong></span>Sea $A$ una matriz $n\times n$ ($n>1$) sobre $\mathbb{K}$. Denotaremos por $A(i|j)$ a la matriz $(n-1)\times (n-1)$ que se obtiene eliminando la $i$-ésima fila y la $j$-ésima columna de $A$. Si $D$ es una función $(n-1)$-lineal, definimos *$D_{ij}=D(A(i|j))$*.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-14"><strong>(\#thm:unnamed-chunk-14) </strong></span>Sea $D$ una funci?n $(n-1)$-lineal alternada de las matrices $n-1\times n-1$ sobre $\mathbb{K}$. Para todo $1\leq j\leq n$, la función $$E_{j}(A)=\sum_{i=1}^{n} (-1)^{i+j}A_{ij}D_{ij}(A)$$ es una función $n$-lineal de las matrices $n\times n$. Si $D$ es una función determinante, también lo es $E_{j}$.</div>\EndKnitrBlock{theorem}
