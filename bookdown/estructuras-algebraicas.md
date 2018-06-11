# Estructuras algebraicas
## Conjuntos
Abordaremos los temas relacionados con la teoría de conjuntos desde una perspectiva intuitiva, más bien oparacional para abordar los conceptos básicos necesarios para desarrollar el resto de los capítulos.

### Definiciones Iniciales

Entenderemos por **conjunto** a una colección de objetos cualesquiera. Las palabras *conjunto, colecci\'on, familia* suelen ser usadas para denotar este objeto matemático. Los objetos que conforman un conjunto son llamados comunmente **elementos** (o **miembros**) del conjunto. Los conjuntos suelen denotarse con letras mayúsculas $A, B, C, P,\cdots$, mientras que los miembros que los conforman generalmente se denotan con letras minúsculas $a,b, x, y,\cdots$. Si $C$ es un conjunto y $x$ es un elemento de $C$, escribiremos $x\in C$ (o equivalentemente $C\ni x$) lo que se lee *$x$ pertenece al conjunto $C$*. Para denotar lo contrario usaremos el símbolo $\notin$, así $x\notin C$ significa que *$x$ no pertenece a $C$ o $x$ no es miembro de $C$*.

\smallskip

Puede ocurrir que elementos de un conjunto también pertenezcan a otro conjunto. En el caso que todo elemento de un conjunto $A$ es miembro del conjunto $C$ decimos que **$A$ es subconjunto de $C$** (o $C$ contiene a $A$), lo que denotaremos $A\subseteq C$. Es decir, si $x\in A$, entonces $x\in C$ para todo $x$, implica que $A\subseteq C$. Note que es posible que $A$ y $C$ tengan exactamente los mismos elementos, en este caso diremos que los conjuntos $A$ y $C$ son iguale y lo denotaremos por $A=C$. Sin embargo debemos comprobar que $A\subseteq C$ y $C\subseteq A$ para asegurar que $A=C$. En otro caso, cuando $A\subseteq C$ pero $A$ no es igual al conjunto $C$, diremos que **$A$ es un subconjunto propio de $C$** (o **$A$ está propiamente contenido en $C$**).

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-1"><strong>(\#exm:unnamed-chunk-1) </strong></span>El conjunto formado por 0, 1, 2, 3, 4, etc. es el llamado conjunto de los **números naturales** y se denota por $\mathbb{N}$.

Se debe saber que podemos definir un conjunto describiendo uno a uno sus miembros. Esto se hace encerrándolos entre llaves. Así, el conjunto de los números naturales es $\mathbb{N}=\{0, 1, 2, 3, 4,\cdots\}$.

Denotaremos por $\mathbb{N}^{*}=\{ 1, 2, 3, \cdots \}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-2"><strong>(\#exm:unnamed-chunk-2) </strong></span>Dado el conjunto de los números enteros $\mathbb{Z}=\{\cdots,-3,-2,-1,0,1,2,3,\cdots \}$, el conjunto de los números pares (enteros pares) es el conjunto de los números de la forma $2k$ donde $k$ es un entero.
	
También se puede describir el conjunto anterior así: 
  
$$\{p\in\mathbb{Z}| p=2k \mbox{ para algún } k\in\mathbb{Z} \}$$ 
  
lo cual se lee: _el conjunto formado por todos los números enteros_ $p$ _tales que_ $p=2k$ _para algún número entero_ $k$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-3"><strong>(\#exm:unnamed-chunk-3) </strong></span>Denotaremos el conjunto de los números reales po $\mathbb{R}$. El conjunto de las soluciones de la ecuación $7x^{2}+4x-32=0$ es $C=\{x\in\mathbb{R}| x \mbox{ es solución de } 7x^{2}+4x-32=0 \}$.
  </div>\EndKnitrBlock{example}

### Operaciones entre conjuntos

Dados dos conjuntos $A$ y $B$ podemos definir nuevos conjuntos a partir de estos, con las operaciones entre conjuntos que definiremos a continuación.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:uniondeconjuntos"><strong>(\#def:uniondeconjuntos) </strong></span>Dados dos conjuntos $A$ y $B$, el conjunto **unión** de $A$ y $B$ es el conjunto $A\cup B = \{ x| x\in A \mbox{ o } x\in B \}$.
</div>\EndKnitrBlock{definition}

Es decir, la unión de los conjuntos $A$ y $B$ es el conjunto formados por aquellos elementos que pertenezcan a al menos uno de los dos conjuntos, así un elemento que pertenezca tanto a $A$ como a $B$, es miembro de $A\cup B$.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:intersecciondeconjuntos"><strong>(\#def:intersecciondeconjuntos) </strong></span>Dados dos conjuntos $A$ y $B$, el conjunto **intersección** de $A$ y $B$ es el conjunto $A\cap B = \{ x| x\in A \mbox{ y } x\in B \}$.
</div>\EndKnitrBlock{definition}

En otras palabras, la intersección de $A$ y $B$ es el conjunto formado por aquellos elementos que pertenecen a ambos conjuntos simultaneamente.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-4"><strong>(\#exm:unnamed-chunk-4) </strong></span>Dados los conjuntos $A$ y $B$, tales que $B\subseteq A$ ($B$ es subconjunto de $A$).  Se tiene que $A\cup A=A$, más aún $A\cup B=A$. Además $A\cap A=A$ y $A\cap B=B$. 
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-5"><strong>(\#exm:unnamed-chunk-5) </strong></span>Sean $A=\{a,b,c\}$ y $B=\{c,d,e\}$. $A\cup B=\{a,b,c,d,e\}$ y $A\cap B=\{c\}$.  Además $\mathcal{P}(A)=\{\ \emptyset, \{a\}, \{b\}, \{c\}, \{a,b\}, \{a,c\}, \{c,b\}, \{a,b,c\}\}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-6"><strong>(\#exm:unnamed-chunk-6) </strong></span>Dado el conjunto de los números enteros, $\mathbb{Z}$. Los subconjuntos $\mathbb{Z}^{+}=\{p\in\mathbb{Z}| p \mbox{ es un entero positivo} \}$ y $\mathbb{Z}^{-}=\{p\in\mathbb{Z}| p \mbox{ es un entero negativo} \}$. Se tiene que $\mathbb{Z}\cap \mathbb{Z}^{+}=\mathbb{Z}^{+}$ y  $\mathbb{Z}\cup \mathbb{Z}^{-}=\mathbb{Z}$.

Ahora bien, pensemos en el conjunto $\mathbb{Z}^{+}\cap\mathbb{Z}^{-}$. Note que no existe nímero entero que pertenezca a $\mathbb{Z}^{+}$ y $\mathbb{Z}^{-}$ simultaneamente. Para que la intersección esté bien definida, el resultado debería ser un conjunto. Con ese fin daremos la siguiente definición.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:conjuntovacio"><strong>(\#def:conjuntovacio) </strong></span>Diremos que un conjunto es **vacío** si no posee elementos y lo denotaremos por $\emptyset$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}El conjunto vacío es único. Basta con demostrar que dados dos conjuntos $\emptyset$ y $\emptyset_{1}$, se cumple que $\emptyset\subseteq \emptyset_{1}$ y $\emptyset_{1}\subseteq\emptyset$.
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:conjuntodiferencia"><strong>(\#def:conjuntodiferencia) </strong></span>Dados dos conjuntos $A$ y $B$, el **conjunto diferencia** $A-B$ es el conjunto $\{x\in A | x\notin B \}$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-8"><strong>(\#exm:unnamed-chunk-8) </strong></span>Dados los conjuntos de los números enteros, $\mathbb{Z}$ y el conjunto de los números naturales $\mathbb{N}=\{0,1,2,3,4,\cdots \}$, el conjunto diferencia $\mathbb{Z}-\mathbb{N}=\{p\in\mathbb{Z}| p\notin \mathbb{N} \}$ es decir, el conjunto de los números enteros que no son números naturales, que no es más que $\mathbb{Z}^{-}$.
</div>\EndKnitrBlock{example}


*Generalización de unión e intersección*

Las operaciones entre conjuntos definidas antes consideran solo dos conjuntos, sin embargo podemos extender las nociones de unión e intesección de conjuntos a una cantidad cualquiera de conjuntos, finita o no.

Dado $n\in\mathbb{N}$. La unión de $n$ conjuntos $A_{1}, A_{2},\cdots,A_{n}$, puede definirse claramente a partir de la unión de dos conjuntos así:

i) Hallamos el conjunto unión de los primeros dos conjuntos $A_{1}\cup A_{2}$ (definición \@ref(def:uniondeconjuntos)).

ii) Ahora unimos el conjunto obtenido en el paso i. con el siguiente conjunto $A_{3}$, esto es $(A_{1}\cup A_{2})\cup A_{3}$.

iii) Repetimos el paso anterior hasta unir todos los conjuntos.

El algoritmo anterior nos muestra que es posible unir una cantidad finita cualquiera de conjuntos. Analogamente se pueden intersecctar $n$ conjuntos, siendo $n$ un número natural cualquiera.

Ahora bien, la unión e intersección de una cantidad arbitraria (no necesariamente finita) también se puede definir.

Dado $I$ un conjunto de índices. Una familia indexada por $I$ es una colección $\mathcal{F}=\{A_{\alpha} | \, \alpha\in I \}$. Note que esta definición permite que el conjunto $I$ sea cualquier conjunto, finito o infinito. Se suele usar el conjunto de los números enteros positivos como conjunto de índices (para numerar) pero se puede usar cualquier otro conjunto.

La **unión** de los conjuntos $A_{\alpha}$, con $\alpha\in I$, el el conjunto $\bigcup\mathcal{F}=\bigcup_{\alpha\in I} A_{\alpha}=\{x|\, x\in A_{\alpha} \mbox{ para algún } \alpha\in I \}$. De forma análoga, la **intersección** de los conjuntos $A_{\alpha}$, con $\alpha\in I$, es el conjunto $\bigcap A_{\alpha}=\{x|\, x\in A_{\alpha} \mbox{ para todo } \alpha\in I \}$. Vale resaltar que cuando $I$ es un conjunto finito, digamos $I=\{1,2,\cdots, n\}$, se tiene que $\bigcup A_{\alpha}=\{x|\, x\in A_{\alpha} \mbox{ para algún } \alpha\in I \}=\{x|\, x\in A_{1} \mbox{ o } x\in A_{2}\mbox{ o }\cdots \mbox{ o } x\in A_{n} \}=A_{1}\cup A_{2},\cdots , A_{n}$.

### Producto cartesiano

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-9"><strong>(\#def:unnamed-chunk-9) </strong></span>Dados $a$ y $b$ miembros de los conjuntos $A$ y $B$ respectivamente, llamaremos *par ordenado al arreglo $(a,b)$. Diremos que dos pares ordenados $(a,b)$ y $(c,d)$ son iguales (es decir $(a,b)=(c,d)$ si y solo si $a=c$ y $b=d$.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-10"><strong>(\#def:unnamed-chunk-10) </strong></span>Sean $A$ y $B$ dos conjuntos. El *producto cartesiano de $A$ y $B$* es el conjunto $A\times B$ formado por todos los pares ordenados $(a,b)$, donde $a\in A$ y $b\in B$. Es decir $A\times B=\{(a,b)| \, a\in A \mbox{ y } b\in B \}$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-11"><strong>(\#exm:unnamed-chunk-11) </strong></span>Si $A=\{1,2,3\}$ y $B=\{3,4,5\}$, entonces el producto cartesiano de $A$ y $B$ es el conjunto

$A\times B=\{ (1,3), (1,4), (1,5), (2,3), (2,4), (2,5), (3,3), (3,4), (3,5)\}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Dados los conjuntos $A$ y $B$, podemos considerar los conjuntos $A\times B$ y $B\times A$. Como conjuntos son distintos, aunque existe una relación entre ellos (se discutirá mas adelante cuando se definan correspondencias biyectivas ). De igual forma se puede definir el producto cartesiano de una cantidad finita de conjuntos (de forma análoga a la unión de conjuntos). Si $A$, $B$ y $C$ son conjuntos, podemos definir el conjunto $A\times B\times C$ formado por los arreglos (terna ordenada) del tipo $(a,b,c)$, donde $a\in A$, $b\in B$ y $c\in C$. Más aun, se puede definir el producto cartesiano para una cantidad arbitraria de conjuntos. Dado un conjunto de índices $I$, el producto cartesiano de una familia indexada por $I$, $\mathcal{F}=\{A_{\alpha}|\, \alpha\in I \}$, es el conjunto de aplicaciones $f:I\longrightarrow \bigcup\mathcal{F} \mbox{ tales que } f(\alpha)\in A_{\alpha}$, es decir $\prod_{\alpha \in I} A_{\alpha}=\{f:I\longrightarrow\bigcup \mathcal{F} |\, f(\alpha)\in A_{\alpha} \}$. Por último, queremos recalcar que es posible hacer el producto cartesiano de un conjunto consigo mismo, esto es $A\times A$ formado, como es natural por los pares $(a,b)$, con  $a$ y $b$ elementos de $A$. En este caso se puede denotar $A^{2}$ al producto cartesiano de $A$ consigo mismo (y se denota $A^{n}$ al producto cartesiano de $A$ consigo mismo $n$ veces). Para $A^{2}$ llamamos **diagonal** al conjunto formado por los pares de la forma $(a,a)$ y se denota por $\Delta$, es decir, $\Delta=\{(a,a)|\, a\in A \}$.
</div>\EndKnitrBlock{remark}

## Relaciones de Equivalencia

\smallskip

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-13"><strong>(\#def:unnamed-chunk-13) </strong></span>Dados dos conjuntos $A$ y $B$, una **relación de $A$ sobre $B$**, es un subconjunto $R$ del producto cartesiano $A\times B$. En el caso que $R\subseteq A\times A$, se dice que $R$ es una relación sobre $A$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-14"><strong>(\#def:unnamed-chunk-14) </strong></span>Dada un relación $R$ sobre un conjunto no vacío $A$. Decimos que:

i) $R$ es **reflexiva** si para todo $a\in A$, se tiene que $(a,a)\in R$ (es decir, la diagonal $\Delta$ es subconjunto de $R$).

ii) $R$ es **simétrica** si para todo $a,b \in A$, se cumple que: $(a,b)\in R \Leftrightarrow  (b,a)\in R$.

iii) $R$ es **transitiva** si para todo $a,b, c \in A$, se cumple que: $(a,b)\in R$ y  $(b,c)\in R$ $\Rightarrow (a,c)\in R$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-15"><strong>(\#def:unnamed-chunk-15) </strong></span>Una relación $R$ sobre un conjunto no vacío $A$, que es reflexiva, simétrica y transitiva, se dice **de equivalencia**.</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Si $R$ es una relación sobre $A$, el hecho de que $(a,b)\in R$ se puede denotar como $aRb$ o como $a\simeq b$ cuando el contexto lo permita y quede claro cual es la relación.
De este modo, $R$ es una relación de equivalencia si para todo $a,b,c\in A$ se tiene que: 
  
i) $aRa$,

ii) $aRb\Leftrightarrow bRa$ y 

iii) $aRb$ y $bRc\Rightarrow aRc$.
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-9"><strong>(\#exm:ejm1-9) </strong></span>**La igualdad** es una relación de equivalencia.
Dado el conjunto de los números reales $\mathbb{R}$, la igualdad es la relación $aRb$ siempre que $a$ y $b$ sean el mismo número real y se denota por $a=b$. Es claramente reflexiva ya que $a=a$; simétrica pues $a=b$ implica que $a$ y $b$ son el mismo número real y por lo tanto $b=a$ y es transitiva ya que si $a=b$ y $b=a$, entonces $a,b$ y $c$ son el mismo número real, lo que implica que $a=c$.
Note que el conjunto donde definimos la igualdad (los reales $\mathbb{R}$) es irrelevante. Esta relación puede (y de hecho está) definida sobre cualquien conjunto.
</div>\EndKnitrBlock{example}
	
\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-10"><strong>(\#exm:ejm1-10) </strong></span>Dado el conjunto de los números enteros $\mathbb{Z}$, definamos la siguiente relación $R$: $(a,b)\in R$ si y solo si $b-a$ es un número par (o lo que es igual, es un múltiplo de $2$).
$R$ es una relación reflexiva, ya que $a-a=0$ y cero es múltiplo de $2$. Es simétrica ya que si $b-a$ es un número par, entonces $a-b$ también lo es. Ahora mostremos que es transitiva, sean $a, b$ y $c$ números enteros tales que $(a,b)\in R$ y $(b,c)\in R$, entonces $b-a$ y $c-b$ son números pares como también su suma $c-a=(c-b)+(b-a)$, por lo tanto $(a,c)\in R$. En consecuencia, $R$ es una relación de equivalencia.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-11"><strong>(\#exm:ejm1-11) </strong></span>**La congruencia modular**. Definiremos la siguiente relación sobre el conjunto de los números enteros, $\mathbb{Z}$. Dado un número natural $n$, para cuales quiera enteros $a$ y $b$, decimos que $aRb$ si y solo si $b-a$ es divisible por $n$ (o equivalentemente, $b-a$ es múltiplo de $n$); lo denotamos por $a\cong b\mbox{ mod } n$ y se lee *$a$ congruente con $b$ módulo $n$*.
Es fácil demostrar que la relación es reflexiva.
Supongamos que $a\cong b \mbox{ mod } n$, entonces $b-a=kn$ para algún $k\in\mathbb{Z}$. Luego, $a-b=-kn$ por lo tanto $b\cong a \mbox{ mod } n$. Entonces la relación es simétrica.
Ahora supongamos que $a\cong b \mbox{ mod } n$ y $b\cong c \mbox{ mod } n$. Se tiene así que existen $k,q\in\mathbb{Z}$ tales que $b-a=kn$ y $c-b=qn$. De este modo $c-a=(c-b)+(b-a)=(q-k)n$, de donde se sigue que $a\cong c \mbox{ mod } n$.
De lo anterior se sigue que la relación de congruencia módulo $n$ es una relación de equivalencia.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-17"><strong>(\#def:unnamed-chunk-17) </strong></span>Dados una relación de equivalencia $R$ sobre un conjunto $A$ y $a\in A$. Definimos **la clase de equivalencia de $a$** como el conjunto $[a]=\{b\in A | aRb\}$. También se denota por $cl(a)$ o $\tilde{a}$.
</div>\EndKnitrBlock{definition}

Pensemos en las clases de equivalencias de los ejemplos anteriores. La clase de equivalencia de $a$ para la relación *igualdad* \@ref(exm:ejm1-9) es el conjunto cuyo único elemento es $a$. Mientras que en el ejemplo \@ref(exm:ejm1-10), la relación solo define dos clases de equivalencia, el conjunto de los números enteros pares y el conjunto de los números enteros impares. En el caso de la *congruencia módulo $n$* \@ref(exm:ejm1-11), la clase de equivalencia de un entero $a$ es el conjunto $\{b\in\mathbb{Z}| a\cong b\mbox{ mod } n \}=\{b\in\mathbb{Z}| b-a=kn\mbox{ para algún } k\in\mathbb{Z} \}=\{b\in\mathbb{Z}| b=kn+a\mbox{ para algún } k\in\mathbb{Z} \}$ es decir, todos los enteros $b$ que tienen por resto $a$ al ser divididos por $n$.


\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-18"><strong>(\#def:unnamed-chunk-18) </strong></span>Dado un conjunto $A$, **una partición de $A$** es una colección de subconjuntos no vacíos de $A$, disjuntos dos a dos, tales que la unión de ellos es todo $A$. Es decir, $\{ B_{i}\subseteq A |\,, i\in I\}$, donde $I$ es un conjunto de índices y se tiene que: 
  
i)  $B_{i}\neq\emptyset$ para todo $i\in I$.

ii) $B_{i}\neq B_{j}$, para $i,j\in I$ y $i\neq j$.

iii) $\bigcup_{i\in I} B_{i}=A$.
	
Cada subconjunto $B_{i}$ es una parte de $A$.
</div>\EndKnitrBlock{definition}


\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-19"><strong>(\#thm:unnamed-chunk-19) </strong></span>Las clases de equivalencia definidas por una relación de equivalencia sobre un conjunto $A$ definen una partición de $A$. Recíprocamente, una partición de un conjunto $A$, induce una relación de equivalencia sobre $A$ de forma que las clases de equivalencia corresponden a las partes de la partición.
</div>\EndKnitrBlock{theorem}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Sea $R$ una clase de equivalencia sobre $A$. Por la reflexividad de $R$ se tiene que $a\in[a]$, por lo tanto $\bigcup_{a\in A} [a]= A$ y $[a]$ es no vacío. Supongamos que $[a]\cap [b]\neq\emptyset$, entonces existe $c\in A$ tal que $c\in [a]\cap [b]$, por transitividad, $aRb$, por lo tanto $[a]=[b]$, es decir, si dos clases no son disjuntas, son iguales.
Recíprocamente, sea  $\{ B_{i}\subseteq A |\,, i\in I\}$ una partición. Definimos la relación $R$, sobre $A$, así: para $a,b\in A$, $aRb$ si y solo si existe $i\in I$ tal que $a,b\in B_{i}$, esto es, $a$ y $b$ pertenecen a la misma parte $B_{i}$. Es muy fácil ver que esta relación es de equivalencia.
</div>\EndKnitrBlock{proof}

## Funciones

Veamos ahora la definición de función (o aplicación), concepto importantísimo en toda la matemática y bastante conocido y usado en la educación matemáticas desde los niveles más básicos. Digamos que una *función* es una regla de asignación entre conjuntos, por ejemplo la función  que asigna a cada número real $r$ su parte entera $\lVert n \rVert$ (el mayor entero menor o igual que $r$), es una función del conjunto de los números reales $\mathbb{R}$ al conjunto de los números enteros y su regla de asignación es la antes descrita. La relación $y=x^{2}$, es una función de $\mathbb{R}$ en si mismo que a cada número real $x$ le relaciona su cuadrado $x^{2}$, desde otro punto de vista, los pares $(x,y)$ pertenecen a la función si $y=x^{2}$, dicho de otro modo, los pares $(x,x^{2})$ forman parte de la función.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-21"><strong>(\#def:unnamed-chunk-21) </strong></span>Dados dos conjuntos no vacíos $A$ y $B$, una **función de $A$ en $B$** es un subconjunto $G$ de $A\times B$ tal que para cada $a\in A$, existe un único $b\in B$, tal que $(a,b)\in G$. Lo denotamos por $f: A\longrightarrow B$, con $f(a)=b$. Llamaremos **dominio de $f$** al conjunto $A$ (y se denota $dom(f$) y **codominio** al conjunto $B$. También se suelen llamar conjunto de partida y conjunto de llegada respectivamente.
                                          </div>\EndKnitrBlock{definition}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:identidad"><strong>(\#exm:identidad) </strong></span>Dado un conjunto $A$ no vacío, la **función identidad** es aquella que a cada $a$, le asigna el mismo elemento $a$. Esto es, $i: A\longrightarrow A$ definida por $i(a)=a$ para todo $a\in A$, que no es más que la diagonal de $A\times A$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-12"><strong>(\#exm:ejm1-12) </strong></span>Sea $f: \mathbb{R}\longrightarrow\mathbb{R}$ definida por $f(x)=x^{2}$. Los pares de la forma $(x,x^{2})$ forman parte de la función. El conjunto $dom(f)=\mathbb{R}$ y su codominio es $\mathbb{R}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-13"><strong>(\#exm:ejm1-13) </strong></span>Dados $\mathbb{Z}$ el conjunto de los números enteros, y $\mathbb{Q}$ el conjunto de los números racionales, definimos $f:\mathbb{Z}\times\mathbb{Z}\longrightarrow\mathbb{Q}$ de la siguiente forma $f((m,n))=\frac{m}{n}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-14"><strong>(\#exm:ejm1-14) </strong></span>Dados $\mathbb{Z}$ el conjunto de los números enteros, y $\mathbb{Q}$ el conjunto de los números racionales, definimos $f:\mathbb{Q}\longrightarrow \mathbb{Z}\times\mathbb{Z}$ de la siguiente forma. Dado un número racional $q\in\mathbb{Q}$, existen enteros sin factores comunes $m$ y $n$ tales que $q=\frac{m}{n}$. Así, $f(q)=(m,n)$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-15"><strong>(\#exm:ejm1-15) </strong></span>Sean $A$ y $B$ conjuntos no vacíos tales que $A\subseteq B$, $\imath: A \longrightarrow B$ dada por $\imath(a)=a$ es la función \textit{inclusión de $A$ en $B$}.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-16"><strong>(\#exm:ejm1-16) </strong></span>Sea $C$ el conjunto $\{a,b,c\}$. Podemos definir la siguiente función $f:C\longrightarrow C$, donde $f(a)=b$, $f(b)=c$ y $f(c)=a$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-17"><strong>(\#exm:ejm1-17) </strong></span>Sean $A$ y $B$ conjuntos no vacíos. $\pi: A\times B\longrightarrow A$ dada por $\pi((a,b))=a$ es la función \textit{proyección de $A\times B$ sobre $A$}. Se puede definir de forma análoga la proyección sobre $B$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-18"><strong>(\#exm:ejm1-18) </strong></span>Dado un conjunto $C$ sobre el cual está definida una relación de equivalencia $R$. Llamaremos **conjunto cociente** al conjunto de las clases de equivalencia definidas por $R$, esto es $C/R=\{[a] | a\in C \}$. Definimos $f:C\longrightarrow C/R$, como $f(a)=[a]$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-22"><strong>(\#def:unnamed-chunk-22) </strong></span>Una función $f:A\longrightarrow B$ se dice **sobreyectiva** si para todo $b\in B$, existe $a\in A$ tal que $f(a)=b$.
</div>\EndKnitrBlock{definition}

Otra forma de entender la sobreyectividad es pensar que la función "cubre" todo el conjunto de llegada (el codominio).
También podemos entenderla en términos de la imagen de la función, que definiremos a continuación: dada $f:A\longrightarrow B$, si $C\subseteq A$, definimos la **imagen de un conjunto $C$** como el conjunto $\{f(a) | a\in C \}$, al cual denotamos por $f[C]$ o $f''C$. El conjunto imagen del dominio se llamará **Imagen de $f$** a secas, este es $f[A]$ y también se denota $Img(f)$. Entonces la  sobreyectividad es equivalente a que la imagen de $f$ sea igual al codominio, es decir $f[A]=B$.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-23"><strong>(\#def:unnamed-chunk-23) </strong></span>Una función $f:A\longrightarrow B$ se llamará **inyectiva** si para todo $a\mbox{ y }b\in A$, si $a\neq b$, entonces $f(a)\neq f(b)$.
</div>\EndKnitrBlock{definition}

Un función inyectiva es pues una función que a cada elemento del dominio le asocia elementos distintos del codominio. Para entender mejor esta definición, definiremos imagen inversa: dada $f:A\longrightarrow B$, si $C\subseteq B$, definimos la **imagen inversa de un conjunto $C$** como el conjunto $\{a | f(a)\in C \}$ y se denota por $f^{-1}[C]$. De este modo, una función es inyectiva si la imagen inversa de los subconjuntos unitarios del codominio tienen a lo sumo un elemento, es decir, $f^{-1}[\{b\}]$ tiene un elemento o es vacío, para todo $b\in B$.

En los ejemplos que antes vimos, la función identidad es sobreyectiva e inyectiva, es decir **biyectiva** (cuando una función es inyectiva y sobreyectiva se le llama biyectiva). La función del ejemplo \@ref(exm:ejm1-12) no es inyectiva, basta ver que $f(1)=f(-1)$. Tampoco es sobreyectiva, no existe número real que tenga un cuadrado negativo. Los ejemplos \@ref(exm:ejm1-15) y \@ref(exm:ejm1-16) muestran funciones biyectivas. Pero los ejemplos \@ref(exm:ejm1-13) y \@ref(exm:ejm1-18) son funciones sobreyectivas que no son inyectivas, mientras que el ejemplo \@ref(exm:ejm1-15) muestra una función inyectiva que no es sobreyectiva.

A continuación definirimos cuando dos funciones son iguales. Intiutivamente, dos funciones serán iguales cuando expresen la misma regla de asignación sobre los mismos objetos. En seguida la definición formal:

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-24"><strong>(\#def:unnamed-chunk-24) </strong></span>Dos funciones $f$ y $g$ de $A$ en $B$, se dicen que son **iguales** si $f(a)=g(a)$ para todo $a\in A$.
</div>\EndKnitrBlock{definition}

Podemos también plantear la situación en la que se relacionen los elementos de dos conjuntos pasando por un tercer conjunto haciendo uso de dos funciones. Es decir, una regla de asignación entre los elementos de un conjunto $A$, en otro conjunto $B$, y otra regla que relacione a los elementos de $B$ con un conjunto $C$ se pueden componer para obtener una regla (una función) de $A$ a $C$.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-25"><strong>(\#def:unnamed-chunk-25) </strong></span>Sean $f:A\longrightarrow B$ y $g:B\longrightarrow C$ dos funciones. La composición de $f$ y $g$ es una función de $A$ en $B$ que asigna a cada $a\in A$ el elemento $g(f(a))\in C$. Se denota por $g\circ f$. Entonces $g\circ f: A\longrightarrow B$, definido por $(g\circ f)(a)=g(f(a))$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Note que el dominio de la función $g$ (la segunda en ser aplicada) debe ser igual al codominio de la función $f$ (pudiése ser un subconjunto del codominio).

Es importante el orden de las funciones, en el contexto general descrito en la definición, no tiene sentido pensar en la composición $f\circ g$, ya que $g(b)$ es un elemento del conjunto $C$ que no es el dominio de $f$, por lo tanto la expresión $f(g(b))$ carece de sentido, salvo que $B$ sea subconjunto de $A$.
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-27"><strong>(\#exm:unnamed-chunk-27) </strong></span>Sea $A=\{a,b,c\}$. Sean $f:A\longrightarrow A$ y $g:A\longrightarrow A$ funciones definida por $f(a)=b$, $f(b)=c$ y $f(c)=a$ y $g(a)=a$, $g(b)=c$ y $g(c)=b$. Entonces $(g\circ f)(a)=g(f(a))=g(b)=c$, $(g\circ f)(b)=g(f(b))=g(c)=b$ y $(g\circ f)(c)=g(f(c))=g(a)=a$. Análogamente,  $(f\circ g)(a)=b$, $(f\circ g)(b)=a$ y $(f\circ g)(c)=c$. Aunque ambas funciones compuestas, $g\circ f$ y $f\circ g$ son funciones de $A$ en si mismo, no son iguales ya que  $(g\circ f)(a)=c$ y $(f\circ g)(a)=b$, es decir $(g\circ f)(a)\neq (f\circ g)(a)$
  </div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-28"><strong>(\#exm:unnamed-chunk-28) </strong></span>Sea $A=\{a,b,c\}$. Sean $f:A\longrightarrow A$ y $g:A\longrightarrow A$ funciones definida por $f(a)=b$, $f(b)=c$ y $f(c)=a$ y $g(b)=a$, $g(c)=b$ y $g(a)=c$. Entonces $g\circ f$  (y $f\circ g$) es la función identidad de $A$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-29"><strong>(\#exm:unnamed-chunk-29) </strong></span>Dadas las siguientes funciones $f:\mathbb{R}\longrightarrow \mathbb{Z}:x\longmapsto \lVert x\rVert$, la notación que sigue de los dos puntos, $x\longmapsto \lVert x\rVert$ nos indica la regla de asignación, esto es $f(x)=\lVert x\rVert$, donde $\lVert x\rVert$ denota la \textit{parte entera} del número real $x$, a saber: \textit{el mayor entero menor o igual a $x$}. Y la función $g:\mathbb{Z}\longrightarrow \{0,e\}$, definida por 

\begin{equation}
	g(p) = \left\{
	\begin{array}{ll}
	0      & \mbox{ si } p \mbox{ es un número par } \\
	e      & \mbox{ si } p \mbox{ es un número impar }
 \end{array}
	\right.
\end{equation}
	
Entonces, la función $g\circ f$ aplica números reales en $\{0,e\}$. Sin embargo $f\circ g$ no puede definirse, ya que el codominio de $g$ no es un subconjunto del dominio de $f$.
	
Calculemos $g\circ f$ para algunos números: $(g\circ f)(\frac{1}{2})=g(\lVert \frac{1}{2} \rVert)=g(0)=0$, $(g\circ f)(\frac{-3}{2})=g(\lVert \frac{-3}{2} \rVert)=g(-2)=0$ y $(g\circ f)(\pi)=g(\lVert \pi \rVert)=g(3)=e$.
</div>\EndKnitrBlock{example}

Al igual que se pueden componer dos funciones, $f$ y $g$, también se puede hacer con una cantidad cualquiera (finita) de funciones. Dadas las funciones  $f:A\longrightarrow B$, $g:B\longrightarrow C$ y $h:\longrightarrow D$, podemos componer $f$ y $g$ y obtener una función de $A$ en $C$. Y a su vez, componer esta función (la compuesta $g\circ f$ de $A$ en $C$) con la función $h$ y así obtener $h\circ (g\circ f)$ de $A$ en $D$, que es la compuesta de las tres funciones.  En este caso cabe preguntarse si es igual $h\circ (g\circ f)$ que $(h\circ g)\circ f$. El siguiente resultado contesta esta pregunta.

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-30"><strong>(\#lem:unnamed-chunk-30) </strong></span>Sean $f:A\longrightarrow B$, $g:B\longrightarrow C$ y $h:\longrightarrow D$ funciones. Entonces $h\circ (g\circ f)=(h\circ g)\circ f$.
</div>\EndKnitrBlock{lemma}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Lo primero que debemos notar es que tanto $h\circ (g\circ f)$ como $(h\circ g)\circ f$ tienen el mismo dominio y codominio. Efectivamente, $h\circ (g\circ f)$ tiene por dominio el conjunto $A$, porque es dominio de $g\circ f$ (ya vimos antes que el dominio y el codominio de $g\circ f$ son el dominio de $f$ y el codominio de $g$ respectivamente), y su codominio es $D$, el codominio de $h$. Del mismo modo $(h\circ g)\circ f$ tiene dominio $A$ (al ser $dom(f)=A$) y codominio $D$ (que es el codominio de $h\circ g$).
Ahora demostremos que para cada $a\in A$, $(h\circ (g\circ f))(a)=((h\circ g)\circ f)(a)$. Y es muy fácil de ver, $$(h\circ (g\circ f))(a)=h(g\circ f)(a)=h(g(f(a)))=(h\circ g)(f(a))=((h\circ g)\circ f)(a)$$ lo que demuestra lo que queríamos.
</div>\EndKnitrBlock{proof}

Qué sucederá con la composición de dos funciones inyectivas, o sobreyectivas. Esto se muestra en este resultado:

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:lema1-2"><strong>(\#lem:lema1-2) </strong></span>Sean $f:A\longrightarrow B$ y $g:B\longrightarrow C$ dos funciones. Entonces:
  
1) $g\circ f$ es sobreyectiva si $f$ y $g$ lo son.

2) $g\circ f$ es inyectiva si $f$ y $g$ lo son.
</div>\EndKnitrBlock{lemma}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}
1) Supongamos que $f$ y $g$ son funciones sobreyectivas. Sea $c\in C$, como $g$ es sobreyectiva, existe $b\in B$ tal que $c=g(b)$. Y como $f$ es sobreyectiva, existe $a\in A$ tal que $b=f(a)$. Se tiene que dado $c$ existe $a$ tal que $c=g(b)=g(f(a))=(g\circ f)(a)$, por lo tanto $g\circ f$ es sobreyectiva.

2) Supongamos que $f$ y $g$ son funciones inyectivas. Sean $a_{1}, a_{2}\in A$, tales que $a_{1}\neq a_{2}$. Como $f$ es inyectiva, se tiene que $f(a_{1})\neq f(a_{2})$. Ahora, como $f(a_{1}) \mbox{ y }f(a_{2})\in B$ y $f(a_{1})\neq f(a_{2})$, de la inyectividad de $g$ se sigue que $g(f(a_{1}))\neq g(f(a_{2}))$, es decir, $(g\circ f)(a_{1})\neq (g\circ f)(a_{2})$, por lo tanto $g\circ f$ es inyectiva.
</div>\EndKnitrBlock{proof}

Si una función $f$ de $A$ en $B$ es biyectiva, para cada $b\in B$ existe $a\in A$ tal que $f(a)=b$, y de la inyectividad se tiene que $a$ es único. De esta manera se puede definir una nueva función de $B$ en $A$ que guarda una extrecha relación con $f$ (pues se define a partir de ella). Dicha función es la **inversa** de $f$. Definámosla formalmente.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-33"><strong>(\#def:unnamed-chunk-33) </strong></span>Dada una función biyectiva $f: A \longrightarrow B$, la \textit{función inversa de $f$} es la función $f^{-1}$, definida así $f^{-1}(b)=a$ si y solo si $f(a)=b$.
</div>\EndKnitrBlock{definition}

Además, para cada $a\in A$, sea $b=f(a)$, de donde $(f^{-1}\circ f)(a)=f^{-1}(f(a))=f^{-1}(b)=a$. Es decir, $f^{-1}\circ f$ es la identidad de $A$ (en sí mismo). Análogamente se puede probar que $f\circ f^{-1}$ es la identidad de $B$. Esto es la demostración del siguiente resultado.

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-34"><strong>(\#lem:unnamed-chunk-34) </strong></span>Dada una función $f:A\longrightarrow B$ biyectiva, las funciones $f^{-1}\circ f$ y $f\circ f^{-1}$ son iguales a la función identidad (correspondiente a los conjuntos $A$ y $B$).
</div>\EndKnitrBlock{lemma}

Recíprocamente, si dada una función $f: A\longrightarrow B$, existe una función $g:B\longrightarrow A$ tal que $g\circ f$ y $f\circ g$ son la función identidad (sobre $A$ y $B$ respectivamente), entonces se tiene que $f$ es sobreyectiva, en efecto, dado $b\in B$, $b=(f\circ g)(b)$, ya que $f\circ g$ es la identidad (sobre $B$) por lo tanto $b=f(g(b))=f(a)$ para algún $a\in A$ (donde $a=g(b)$). Observemos también que $f$ es inyectiva, ya que si $f(a_{1})=f(a_{2})$ se tiene que $g(f(a_{1}))=g(f(a_{2}))$, como $g\circ f$ es la identidad (sobre $A$) se tiene que $a_{1}=a_{2}$. Esto se puede expresar como sigue.

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-35"><strong>(\#lem:unnamed-chunk-35) </strong></span>La función $f:A\longrightarrow B$ es biyectiva si y solo si existe una función $g:B\longrightarrow A$ tal que $g\circ f$ y $f\circ g$ son la función identidad sobre $A$ y $B$ respectivamente.
</div>\EndKnitrBlock{lemma}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-36"><strong>(\#def:unnamed-chunk-36) </strong></span>Sea $C$ un conjunto no vacío. $\mathcal{A}(C)$ es el conjunto de todas las funciones biyectivas de $C$ sobre sí mismo.
</div>\EndKnitrBlock{definition}

Respecto a este conjunto, si consideramos la operación *composición de funciones*, tenemos que $\mathcal{A}(C)$ es cerrado bajo esta operación, esto lo demostramos ya en el lema \@ref(lem=lema1-2). Además, como vimos antes, la composición de funciones es asociativa. Sabemos que la identidad y la función inversa son funciones biyectivas (pertenecen también al conjunto $\mathcal{A}(C)$). Es decir, tenemos un conjunto ($\mathcal{A}(C)$) con una operación (la composición de funciones) que tiene una estructura especial (la de grupo). Profundizaremos en esto en la siguiente sección.

## Cardinales

En esta sección demostraremos solo algunos resultados referidos a cardinalidad y números cardinales, solo aquellos que nos sean realmente útiles para el tema que nos ocupa en este trabajo. Quien desee ver las otras demostraciones y ahondar en este tema puede referirse a <añadir bibliografia...Kunen>.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-37"><strong>(\#def:unnamed-chunk-37) </strong></span>Dos conjuntos $A, B$ son equipotentes si existe una biyección $f:A \longrightarrow B$ y se denota por $A\sim B$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:teo1-2"><strong>(\#thm:teo1-2) </strong></span>La equipotencia es una relación de equivalencia.
</div>\EndKnitrBlock{theorem}
\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}La función identidad (de un conjunto en si mismo) es una biyección, por lo tanto la equipotencia es una relación reflexiva. Si $A\sim B$, existe una biyección $f:A\longrightarrow B$. Ya vimos antes que una función biyectiva es invertible y su inversa es $f^{-1}$ es una biyección de $B$ en $A$, lo que muestra que la simetría. Dadas dos biyecciones $f: A\longrightarrow B$ y $g:B\longrightarrow C$, la composición $g\circ f$ es una biyección de $A$ en $C$, por lo tanto la equipotencia es transitiva.
</div>\EndKnitrBlock{proof}

Podemos preguntarnos cuántos elementos tiene un conjunto. Una forma de "contar" los elementos que tiene un conjunto es la siguiente: Sean $A_{0}=\emptyset$ y para cada número natural $n$, sea $A_{n}=\{1,2,..., n\}$. Es fácil ver que $A_{n}=A_{m}$ si y solo si $n=m$ \@ref(exr:ejc1). De este modo, para ver que un conjunto $C$ tiene $n$ elementos basta ver que es equipotente con $A_{n}$, es decir $C\sim A_{n}$. Diremos que un conjunto es **finito** si es equipotente con algún $A_{n}$ para algún $n\in\mathbb{N}$. Si un conjunto no es finito diremos que es **infinito**. 

Lo anterior nos da una idea del concepto de cardinalidad, que formalmente se definiría como sigue.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-39"><strong>(\#def:unnamed-chunk-39) </strong></span>Dado un conjunto $C$, la clase de equivalencia definida por la relación de equipotencia se conoce como el **cardinal** (o **cardinalidad** o **número cardinal**) de $C$ y se denota por $|C|$.
</div>\EndKnitrBlock{definition}

En algunos libros pueden conseguirse otras definiciones de cardinalidad. Los números cardinales pueden ser definidos mas formalmente como un objeto matemático y son de gran importancia en teoría de conjuntos, teniendo ellos mismos una importancia intrínseca, Sin embargo, la definición que presentamos se adecua perfectamente a los temas que trabajaremos aquí.
De la definición anterior y el teorema \@ref(thm:teo1-2) podemos ver los cardinales tienen las siguientes propiedades:

i) Todo conjunto tiene un único número cardinal.
ii) Dos conjuntos tienen el mismo número cardinal si y solo si son equipotentes.
iii) El cardinal de un conjunto finito es la cantidad de elementos que lo conforman.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-40"><strong>(\#exm:unnamed-chunk-40) </strong></span>La cardinalidad de los conjuntos $A_{n}$ definidos antes es $n$ (la cantidad de elementos que tiene el conjunto).
La cardinalidad del conjunto de los números naturales es $\aleph_{0}$ (se lee alef cero) (también puede conseguirse en alguna literatura que $|\mathbb{N}|=\omega$ y así el primer cardinal infinito $\aleph_{0}$, es igual el ordinal omega). Cualquier conjunto de cardinalidad $\aleph_{0}$, se dice **numerable**. Si un conjunto no es numerable, diremos que es un conjunto **no numerable**.
El número cardinal del conjunto de los números enteros $\mathbb{Z}$ es $\aleph_{0}$, por lo tanto es un conjunto numerable, al igual que el conjunto de los números racionales $\mathbb{Q}$. Por otro lado, el conjunto de los números reales no es numerable.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-41"><strong>(\#def:unnamed-chunk-41) </strong></span>	Sean $\alpha$ y $\beta$ dos números cardinales. La **suma $\alpha +\beta$** está definida como el número cardinal del conjunto $A\cup B$, donde $\alpha=|A|$ y $\beta=|B|$ y $A$ y $B$ son disjuntos. El producto $\alpha\beta$ está definido como el número cardinal $|A\times B|$, con $\alpha=|A|$ y $\beta=|B|$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}	No es necesario que los conjuntos $A$ y $B$ sean disjuntos para la definición del producto $\alpha\beta$. Dados dos cardinales $\alpha$ y $\beta$, siempre se pueden hallar conjuntos disjuntos $A$ y $B$ tales que $\alpha=|A|$ y $\beta=|B|$. De la definición de cardinal y de los teoremas anteriores, se sigue que las definiciones de suma $\alpha +\beta$ y producto $\alpha\beta$ son independientes de la elección de los conjuntos $A$ y $B$.
</div>\EndKnitrBlock{remark}

Las operaciones de suma y productos de números cardinales cardinales son asociativas y commutativa, además se cumple la ley distributiva. Esto no lo demostraremos aquí porque escapa del alcance de este texto. De esto se tiene que la suma y el productos de cardinales finitos es coincidente con la suma y el producto de números naturales no negativos, por lo que existe el elemento identidad para la suma, no es más que el cardinal del conjunto vacío, $0=|\emptyset|$. Pero el producto de cardinales infinitos no coincide con el álgebra natural, por ejemplo el producto del cardinal $\aleph_{0}$ con él mismo, es $\aleph_{0}$. Así, si $A$ y $B$ son conjuntos numerables, $A\times B$ es un conjunto numerable. Para más detalle sobre este tema pueden referirse a HACER REFERENCIA AQUÍ- KUNEN Y DI PRISCO.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-43"><strong>(\#def:unnamed-chunk-43) </strong></span>	Sean $\alpha$ y $\beta$ números cardinales y sean $A$ y $B$ conjuntos tales que $\alpha=|A|$ y $\beta=|B|$. Decimos que \textit{$\alpha$ es menor o igual que $\beta$} y lo denotamos así $\alpha\leq\beta$, si y solo si $A$ es equipotente con un subconjunto de $B$ (es decir, existe una función inyectiva $f:A\longrightarrow B$). Decimos que **$\alpha$ es estrictamente menor que $\beta$** y lo denotamos así $\alpha<\beta$, si $\alpha\leq\beta$ y $\alpha\neq\beta$.
</div>\EndKnitrBlock{definition}
Es claro que la definicióon de $\leq$ no depende de la elección de los conjuntos $A$ y $B$.
 
 \BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-44"><strong>(\#thm:unnamed-chunk-44) </strong></span>	Sea $A$ un conjunto. Entonces $|A|\leq|\mathcal{P}(A)$.
 </div>\EndKnitrBlock{theorem}
 
 \BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}	 Sea $f:A\longrightarrow \mathcal{P}(A)$ la función $f(a)=\{a\}$. Dados $a,b\in A$, si $\{a\}\neq\{b\}$, por definición de igualdad de conjuntos, se tiene que $a\neq b$, por lo tanto $A\leq \mathcal{P}(A)$. Ahora veamos que $A\neq\mathcal{P}(A)$, note que el conjunto $B=\{a\in A: a\notin f(a) \}\subseteq A$ no pertenece al conjunto $Img(A)$, es decir, no existe $a\in A$ tal que $f(a)=B$. 
 </div>\EndKnitrBlock{proof}

Enunciaremos el conocido *Teorema de Schroeder-Bernstein* sin demostración. El lector interesado en estos temas puede remitirse a HACER REFERENCIA AQUí.

\BeginKnitrBlock{theorem}\iffalse{-91-84-101-111-114-101-109-97-32-100-101-32-83-99-104-114-111-101-100-101-114-45-66-101-114-110-115-116-101-105-110-93-}\fi{}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-46"><strong>(\#thm:unnamed-chunk-46)  \iffalse (Teorema de Schroeder-Bernstein) \fi{} </strong></span>	 Si $A$ y $B$ son conjuntos tales que $|A|\leq |B|$ y $|B|\leq |A|$. Entonces $|A|=|B|$.
 </div>\EndKnitrBlock{theorem}
 

### Ejercicios

\BeginKnitrBlock{exercise}<div class="exercise"><span class="exercise" id="exr:ejc1"><strong>(\#exr:ejc1) </strong></span>Dados los conjuntos $A_{0}=\emptyset$ y para cada número natural $n$, sea $A_{n}=\{1,2,..., n\}$. Demuestre que $A_{n}=A_{m}$ si y solo si $n=m$.

Supongamos que $A_{n}=A_{m}$, entonces es fácil ver que $n=M$ (en caso contrario se tendría que $n<m$ o $n>m$). Recíprocamente, si $n=m$, por definición es claro que $A_{n}\subseteq A_{m}$ y $A_{m}\subseteq A_{n}$.
</div>\EndKnitrBlock{exercise}

\BeginKnitrBlock{exercise}<div class="exercise"><span class="exercise" id="exr:ejc2"><strong>(\#exr:ejc2) </strong></span>Denuestre que los conjuntos $\mathbb{Z}$, $\mathbb{Q}$ son conjuntos numerables.

Basta probar que $\mathbb{Z}\sim \mathbb{N}$ y $\mathbb{Q}\sim \mathbb{N}$. Para esto debemos hallar biyecciones entre los conjuntos. Sea $f:\mathbb{Z}\longrightarrow \mathbb{N}$ definida así: 
  $$f(n) = \left\{
	\begin{array}{ll}
	-2n-1      & \mbox{ si } n<0\\
	2n      & \mbox{ si } n>=0
	\end{array}
	\right.$$
Es fácil ver que $f$ es una biyección, ya que $f$ asigna cada número entero negativo a los números naturales impares (1, 3, 5, ...) y cada número entero positivo a los números naturales pares (0, 2, 4, ...).
     Por otro lado, la función $g:\mathbb{Z}\times\mathbb{N} \longrightarrow \mathbb{Q}$ definida por $f(a,n)=\frac{a}{n}$ es sobreyectiva. Se puede hallar una función inyectiva $\hat{g}$ de $\mathbb{Z}\times\mathbb{N}$ en $\mathbb{Q}$. Por lo tanto $|\mathbb{Q}|\leq |\mathbb{Z}\times\mathbb{N}|$. Como $\mathbb{Z}\times\mathbb{N}$ es numerable, se tiene que $\mathbb{Q}$ es numerable.
    </div>\EndKnitrBlock{exercise}


## Teoría de Grupos

En esta sección estudiaremos un objeto matemático de gran importancia, los grupos. En la sección anterior vimos un grupo que surgió de manera natural, $\mathcal{C}$ junto a la operación composición de funciones, pero el grupo más familiar es el de los números enteros (con la operación suma), con el que nos topamos desde la infancia; en ambos ejemplos vemos que la operación es asociativa, tiene un elemento neutro (la función identidad en el primer caso y el número cero en el caso de los números naturales) y un elemento inverso (la función inversa en un caso y el opuesto en el caso de los naturales).

A continuación presentaremos la definición formal de grupo así como un amplio repertorio de resultados bien conocidos en álgebra respecto a este objeto.

Dado un conjunto no vacío $G$, una *operación binaria* es una función $G\times G\longrightarrow G$. Comunmente se usan las notaciones $a\ast b$ o  $a\cdot b$ para denotar la imagen de $(a,b)$ por la función, aunque puede también usarse $ab$ (obviando el punto como se hace para expresar el producto de dos números) o incluso $a+b$ cuando la operación es la suma usual (como sucede con los números enteros).

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-47"><strong>(\#def:unnamed-chunk-47) </strong></span>Un par $(G,\ast)$, donde $G$ es un conjunto no vacío y una operacón binaria $\ast:G\times G\longrightarrow G$, forman un **grupo** si:
  
i) Para todo $a,b,c\in G$, $(a\ast b)\ast c=a\ast (b\ast c)$. Es decir, la operación es *asociativa*.
		
ii) Existe un elemento $e\in G$ tal que $a\ast e=e\ast a=a$. Llamaremos a tal elemento *neutro (o identidad) bilateral* de $G$.
		
iii) Para todo $a\in G$, existe un elemento $a^{-1}\in G$ tal que $a^{-1}\ast a=a\ast a^{-1}=e$, llamado *inverso* de $a$.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Puede hacerse referencia al grupo nombrando solo el conjunto $G$ cuando quede claro cual es la operación.
Si una operacón binaria $\ast:G\times G\longrightarrow G$ es asociativa (i.), se dice que $(G,\ast)$ es un *semigrupo*. Llamaremos *monoide* a un semigrupo con identidad (ii.). De este modo, se puede decir que un grupo es un monoide con inverso (bilateral).
</div>\EndKnitrBlock{remark}

Un semigrupo $G$ se llamará **abeliano** o **commutativo** si la operación es

iv) Commutativa, es decir, $a*b=b*a$, para todo $a, b\in G$.
   
El **orden** de un grupo $G$ es la cantidad de elementos que tiene el grupo, es decir, la cardinalidad de $G$ ($|G|$). También se denota $o(G)$ Decimos que un grupo es de **orden finito** (o simplemente finito) si $|G|$ es finito. En caso contrario decimos que el grupo es **infinito**.

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-49"><strong>(\#exm:unnamed-chunk-49) </strong></span>El conjunto de los números enteros con el producto usual es un monoide ya que el producto es una operación asociativa y el número uno (1) es el elemento identidad. Como ya lo hemos mencionado, el conjunto de los números enteros, $\mathbb{Z}$ con la operación suma (la suma usual de enteros), forman un grupo. El lector podrá verificar fácilmente que la operación suma es cerrada, es asociativa, que el cero es el elemento neutro ($e$ en la definición) y que cada elemento tiene un inverso ($a^{-1}=-a$). Además es claro que se trata de un grupo abeliano (la suma es una operación commutativa). A un grupo cuya operación es la suma, como en este ejemplo, lo llamaremos **grupo aditivo**, si es el producto, lo denominaremos **grupo multiplicativo**.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-50"><strong>(\#exm:unnamed-chunk-50) </strong></span>Dado el conjunto $G={1,-1}$. Definimos la operación $\ast:G\times G \longrightarrow G$ como el producto de números reales usual. El par $(G,\ast)$ forman un grupo abeliano de orden $2$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-51"><strong>(\#exm:unnamed-chunk-51) </strong></span>El conjunto de los números racionales $\mathbb{Q}$ con la suma usual, es un grupo abeliano.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-52"><strong>(\#exm:unnamed-chunk-52) </strong></span>Consideremos un cuadrado cuyos vértices estan numerados consecutivamente $1,2,3,4$ centrado en el origen del palno cartesiano y de lados paralelos a los ejes coordenados.

Sea $C_{4}$ el conjunto formado por las siguientes transformaciones: $R$, una rotación de $90º$ del cuadrado. $R^{2}$ una rotación de $180º$ del cuadrados. $R^{3}$ una rotación de $270º$ del cuadrado (todas en el sentido de las agujas del reloj, centradas en el origen). $I$, una rotación de $360º$ (igual que antes en sentido horario, centrada en el origen). $T_{x}$ y $T_{y}$, reflexiones sobre los ejes $x$ y $y$ respectivamente y $T_{I}$ y $T_{II}$ reflexiones sobre las diagonales que pasan por los vértices que están en el primer y tercer cuadrante (la primera) y en el segundo y cuarto cuadrante (la segunda). Con la operación *composición de funciones*, el conjunto $C_{4} = {R, R^{2}, R^{3}, I, T_{x}, T_{y}, T_{I}, T_{II}}$ es un grupo no abeliano de orden $8$ llamado el **grupo de simetría del cuadrado**.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-53"><strong>(\#exm:unnamed-chunk-53) </strong></span>Sea $C$ un conjunto no vacío y $\mathcal{A}(C)$ el conjunto de todas las biyecciones de $C$ en si mismo. Con la operación composición de funciones vista en la sección anterior, $\mathcal{A}(C)$ forma un grupo (no abeliano). En efecto, la composición de funciones biyectivas es asociativa, la identidad es una función biyectiva y toda biyección tiene una inversa. Los elementos de $\mathcal{A}(C)$ son llamados **permutaciones** y $\mathcal{A}(C)$ es llamado el grupo de permutaciones sobre $C$. Si $C=\{1,2, ..., n\}$, entonces $\mathcal{A}(C)$ es llamdo el **grupo simétrico sobre $n$ letras** y se denota $S_{n}$. Se puede ver que $|S_{n}|=n!$ (ejercicio \@ref(exr:ejc3)).
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}Dado un elemento $f\in S_{n}$, podemos representarlo por $\left(  {\begin{array}{ccccc}
	1 & 2 & 3 & \cdots & n \\
	i_{1} & i_{2} & i_{3} & \cdots & i_{n}\\
	\end{array} } \right) $. Y el producto de dos de estos elementos, $f, g\in\mathcal{C}$ es la composición de dos biyecciones $f\circ g$, y puede representarse por un arreglo como el anterior tomando en cuenta que $(f\circ g)(k)=f(g(k))=f(i_{k})$. Si suponemos que $f,g\in S_{5}$, donde $f$ está representado por $\left(  {\begin{array}{ccccc}
	1 & 2 & 3 & 4 & 5 \\
	3 & 4 & 1 & 2 & 5 \\
	\end{array} } \right) $, y $g$ es la biyección
 $\left(  {\begin{array}{ccccc}
	1 & 2 & 3 & 4 & 5 \\
	5 & 4 & 3 & 2 & 1 \\
	\end{array} } \right) $. Entonces  $f\circ g$ es  tal que $(f\circ g)(1)=f(g(1))=f(5)=5$, análogamente con los números del $2$ al $5$, por lo tanto, $f\circ g$ es $\left(  {\begin{array}{ccccc}
	1 & 2 & 3 & 4 & 5 \\
	5 & 2 & 1 & 4 & 3 \\
	\end{array} } \right) $. Mientras que $g\circ f$ es $\left(  {\begin{array}{ccccc}
	1 & 2 & 3 & 4 & 5 \\
	3 & 2 & 5 & 4 & 1 \\
	\end{array} } \right) $. Lo que evidencia que $S_{n}$ no es necesariamente un grupo abeliano.
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejm1-21"><strong>(\#exm:ejm1-21) </strong></span>Dados $G$ y $H$ dos grupos con identidades $e_{G}$ y $e_{H}$ respectivamente. Consideremos el producto cartesiano $G\times H$ y la operación binaria $(a,b)\ast (c,d)=(a\ast c,b\ast d)$ donde $a\ast c\in G$ y $b\ast d\in H$. Con esta operación $G\times H$ es un grupo con identidad $(e_{G}, e_{H})$ y con inverso $(a^{-1}, b^{-1})$ para cada elemento $(a,b)\in G\times H$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-55"><strong>(\#def:unnamed-chunk-55) </strong></span>Una relación de equivalencia sobre un monoide $G$ que satisface que si $a_{1}\sim a_{2}$ y $b_{1}\sim b_{2}$, entonces $a_{1}b_{1}\sim a_{2}b_{2}$ para todo $a_{1},a_{2},b_{1},b_{2}\in G$, se llama **relación de congruencia**.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{theorem}<div class="theorem"><span class="theorem" id="thm:unnamed-chunk-56"><strong>(\#thm:unnamed-chunk-56) </strong></span>Si $\sim$ es una relación de congruencia sobre un monoide $G$, entonces el conjunto $G/\sim$ de todas las clases equivalencia de $(G,\sim)$ es un monoide con la operación binaria definida por $[a][b]=[ab]$. Si $G$ es un grupo abeliano, entoces $(G,\sim)$ lo és.
</div>\EndKnitrBlock{theorem}
\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Como $\sim$ es una relación de equivalencia, se tiene que:
  (1) Si $[a_{1}]=[a_{2}]$ y $[b_{1}]=[b_{2}]$, $a_{1}\sim a_{2}$ y $b_{1}\sim b_{2}$, entonces $a_{1}b_{1}\sim a_{2}b_{2}$, es decir, $[a_{1}b_{1}]= [a_{2}b_{2}]$. Entonces la operación está bien definida. $G/\sim$ tiene un elemento neutro, para todo $a\in G$ se tiene que $[a][e]=[ae]=[a]=[ea]=[e][a]$, donde $e\in G$ es el elemento neutro del monoide. La operación es asociativa, en efecto, $[a]([b][c])=[a][bc]=[a(bc)]=[(ab)c]=[ab][c]=([a][b])[c]$. De aquí concluímos que $G/\sim$ es un monoide.
Supongamos que $G$ es un grupo abeliano, entonces cada $a\in G$ tiene un elemento inverso  $a^{-1}\in G$. De este modo, para cada $[a]\in G/\sim$, se tiene que $[a^{-1}]\in G/\sim$ es el inverso de $[a]$ ya que $[a][a^{-1}]=[aa^{-1}]=[e]=[a^{-1}][a]=[a^{-1}][a]$. Así $G/\sim$ es un grupo. Fácilmente se ve que si $G$ es abeliano, entonces $G/\sim$ lo és, ya que $[a][b]=[ab]=[ba]=[b][a]$. 
</div>\EndKnitrBlock{proof}
Este teorema dota de otros ejemplos, tanto de monoides como de grupos:

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-58"><strong>(\#exm:unnamed-chunk-58) </strong></span>Para un entero fijo, la relación de congruencia modular es una relación de congruencia sobre el grupo aditivo $\mathbb{Z}$. Como $(\mathbb{Z}, +)$ es un grupo abeliano, se tiene que $\mathbb{Z}_{n}$ es un grupo aditivo abeliano, con la operación natural $[a]+[b]=[a+b]$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-59"><strong>(\#exm:unnamed-chunk-59) </strong></span>$(Z,\ast)$ es un monoide sobre $\mathbb{Z}$ con la multiplicación usual de enteros. por lo tanto $\mathbb{Z}_{n}$ es un monoide, con la operación $[a]\ast[b]=[a\ast b]$.
</div>\EndKnitrBlock{example}

Veremos algunos resultados muy técnicos que nos serán útiles mas adelante.

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-60"><strong>(\#lem:unnamed-chunk-60) </strong></span>Sea $G$ un grupo, entonces se tiene que:
  
  1) el elemento identidad de $G$ es único;

  2) para cada $a\in G$, el inverso $a^{-1}$ es único;

  3) para todo $a\in G$, se tiene que $(a^{-1})^{-1}=a$;
  
  4) para $a,b\in G$, se tiene que $(a*b)^{-1}=b^{-1}*a^{-1}$.
  </div>\EndKnitrBlock{lemma}
\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}
1) Supongamos que $e, f\in G$ son tales que, $\forall a\in G$, $a*e=e*a=a$ y $a*f=f*a=a$. En particular, $f*e=f$ y $f*e=e$, de donde se sigue que $e=f$.

2) Sea $a\in G$, veamos que si $a*x=a*y$, entonces $x=y$; en efecto, sea $b$ un inverso de $a$, es decir, $a*b=b*a=e$. De la igualdad $a*x=a*y$ se tiene que $b*(a*x)=b*(a*y)$ y así $(b*a)*x=(b*a)*y$, por lo tanto $x=y$. De este modo, si dos elemento $b,c\in G$ son dos inversos de $a$ se tiene que $a*b=e=a*c$ y de lo anterior se sigue que $b=c$.

3) Sabemos que $a^{-1}*(a^{-1})^{-1}=e=a^{-1}*a$, por lo que demostramos en la parte b), se sigue fácilmente que $(a^{-1})^{-1}=a$.

4) De la asociatividad se tiene la igualdad $(a*b)*(b^{-1}*a^{-1})=(a*(b*b^{-1})*a^{-1})=a*e*a^{-1}=e$. Y por la unicidad del elemento inverso (demostrada justo antes) se sigue que $(a*b)^{-1}$ es igual a $b^{-1}*a^{-1}$.
</div>\EndKnitrBlock{proof}

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-62"><strong>(\#def:unnamed-chunk-62) </strong></span>Un subconjunto $H$ de un grupo $G$, se llama **subgrupo** de $G$ si respecto a la operación definida sobre $G$, él mismo forma un grupo.
</div>\EndKnitrBlock{definition}
Suponga que $G$ es un grupo y $H\subseteq G$ es un subconjunto cerrado bajo la operación de grupo definida sobre G, es decir, para todo $a,b\in H$ se tiene que $ab\in H$. Y cada elemento de $H$ tiene su inverso también en $H$, esto es, si $a\in H$, entonces $a^{-1}\in H$. Es claro que $H$ será un semigrupo de $G$.
 Esto lo mostramos en el siguiente resultado:

\BeginKnitrBlock{lemma}<div class="lemma"><span class="lemma" id="lem:unnamed-chunk-63"><strong>(\#lem:unnamed-chunk-63) </strong></span>Un subconjunto no vacío $H$ de un grupo $G$, es un subgrupo si y solo si:
  
  1) para cada $a,b\in H$, $ab\in H$.

  2) para cada $a\in H$, $a^{-1}\in H$.
</div>\EndKnitrBlock{lemma}

\BeginKnitrBlock{proof}<div class="proof">\iffalse{} <span class="proof"><em>Demostración. </em></span>  \fi{}Es claro que si $H\subseteq G$ es un subgrupo de $G$, cumple 1 y 2.
Recíprocamente, supongamos que $H\subseteq G$, cumple con 1 y 2. Faltaría ver que la operación es asociativa en $H$ y que el elemento neutro está en $H$. La ley asociativa se hereda de $G$ (si la operación es asociativa en $G$, de igual forma lo será en $H$). Como para cada elemento de $H$ tiene un inverso, existen $a, a^{-1}\in H$; además se tiene que la operación es cerrada en $H$, luego $e=aa^{-1}\in H$. Por lo tanto se tiene que $H$ es un grupo (con la operación heredada de $G$). 
</div>\EndKnitrBlock{proof}

### Ejercicios

\BeginKnitrBlock{exercise}<div class="exercise"><span class="exercise" id="exr:unnamed-chunk-65"><strong>(\#exr:unnamed-chunk-65) </strong></span>Sea $G$ un grupo y $C$ un conjunto no vacío. Sea $M(C,G)$ el conjunto de todas las funciones $f:C\longrightarrow G$. Definamos la operación de grupo como la suma de funciones, es decir, para cada $f,g\in M(C,G)$, $f\ast g = f +g$. Demuestre que $M(C,G)$ es un grupo, es abeliano si $G$ lo es.

Respuesta: Es claro que la suma de funciones es cerrada en $M(C,G)$. Sean $f,g,h\in M(C,G)$, para cada $a\in C$, $(f+(g+h))(a)=f(a)+((g+h)(a))=f(a)+(g(a)+h(a))$ como $G$ es un grupo, la suma es asociativa, luego $f(a)+(g(a)+h(a))=(f(a)+g(a))+h(a)=((f+g)(a))+h(a)=((f+g)+h)(a)$; por lo tanto la suma de funciones es asociativa.
</div>\EndKnitrBlock{exercise}

\BeginKnitrBlock{exercise}<div class="exercise"><span class="exercise" id="exr:ejc3"><strong>(\#exr:ejc3) </strong></span>Demuestre que el grupo simétrico sobre $n$ letras es de orden $n!$.
	Respuesta: Pensemos en el grupo simétrico $S_{3}$. El orden del grupo es equivalente a contar todas las posibles biyecciones de un conjunto de $3$ elementos, a saber:\\
	$\left(  {\begin{array}{ccc}
		1 & 2 & 3\\
		i_{1} & i_{2} & i_{3}\\
		\end{array} } \right) $. Nótese que $1$ tiene $3$ posibles imágenes $i_{1}$, luego de fijada la imagen de $1$, restas $2$ posibles imágenes de $2$, $i_{2}$ y luego de fijadas las imágenes de $1$ y $2$, le queda una sola posibilidad a $3$. De donde podemos concluír que existen $3!$ posibles biyecciones de $\{1,2,3\}$ en sí mismo.\\
	Análogamente, contar los elementos de $S_{n}$ es equivalente a contar las posibles permutaciones del conjunto $\{1,2,3,\cdots, n\}$.
</div>\EndKnitrBlock{exercise}

\BeginKnitrBlock{exercise}<div class="exercise"><span class="exercise" id="exr:unnamed-chunk-66"><strong>(\#exr:unnamed-chunk-66) </strong></span>Demuestre que el grupo del ejemplo \@ref(exm:ejm1-21) es un grupo de orden $|G||H|$. Además muestre que $G\times H$ es un grupo abeliano si $G$ y $H$ lo son.
Respuesta: Sabemos que $|G\times H|=|G||H|$, lo que demuestra que el orden del grupo es el producto $|G||H|$. Ahora supongamos que $G$ y $H$ son abelianos, luego $(a,b)\ast (c,d)=(a\ast c,b\ast d)=(c\ast a,d\ast b)=(c,d)\ast (a,b)$.
</div>\EndKnitrBlock{exercise}