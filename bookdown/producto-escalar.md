# Producto escalar

En este capítulo estaremos considerando espacios vectoriales reales y complejos, por lo tanto cada vez que se mencione un cuerpo se estará haciendo referencia al cuerpo de los números reales, $\mathbb{R}$, o al cuerpo de los números complejos, $\mathbf{C}$. Y se hará una abstracción de lo que en el capítulo 2 se presentó como el producto punto entre vectores.

\BeginKnitrBlock{definition}<div class="definition"><span class="definition" id="def:unnamed-chunk-1"><strong>(\#def:unnamed-chunk-1) </strong></span>Sea $\mathbb{F}$ un cuerpo ($\mathbb{R}$ o $\mathbf{C}$), y $V$ un espacio vectorial sobre $\mathbb{F}$. Un *producto interno* (o *producto interior*) sobre $V$ es una operación binaria de $V\times V$ en $\mathbb{F}$, $(\alpha,\beta)\mapsto (\alpha|\beta)$ tal que para todo $\alpha,\beta,\gamma\in V$ y $c,d\in\mathbb{F}$:
[a] $(\alpha|\beta)=\bar{(\beta|\alpha)}$, donde la barra indica la conjugación compleja;
[b] $(c\alpha+d\beta|\gamma)=c(\alpha|\gamma)+d(\beta|\gamma)$ y
[c] $(\alpha|\alpha)>0$ si $\alpha\neq 0$.

En el caso que tal operación exista, decimos que $V$ es un *espacio vectorial con producto interno*.
</div>\EndKnitrBlock{definition}

\BeginKnitrBlock{remark}<div class="remark">\iffalse{} <span class="remark"><em>Nota. </em></span>  \fi{}De (a) y (b) se sigue que $(\alpha|c\beta+\gamma)=\bar{c}(\alpha|\beta)+(\alpha|\gamma)$.
</div>\EndKnitrBlock{remark}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-3"><strong>(\#exm:unnamed-chunk-3) </strong></span>En el espacio vectorial $\mathbf{C}^{n}$, la operación $(\alpha|\beta)=\sum_{i=1}^{n} x_{i}\bar{y_{i}}$, donde $\alpha=(x_{1},x_{2},\cdots,x_{n})$ y $\beta=(y_{1},y_{2},\cdots,y_{n})$; es un producto interno, llamado el *producto interno canónico en* $\mathbf{C}^{n}$.
Por otro lado, si consideramos esta misma operación sobre $\mathbb{R}$, la conjugación queda sin efecto y así el *producto interno canónico en* $\mathbb{R}$ es la operación $(\alpha|\beta)=\sum_{i=1}^{n} x_{i}y_{i}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-4"><strong>(\#exm:unnamed-chunk-4) </strong></span>En $\mathbb{C}^{2}$ definimos la operación $((x,y)|(z,w))=2x\bar{z}+x\bar{w}+y\bar{z}+y\bar{w}$ es un producto interno.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:ejemplo85"><strong>(\#exm:ejemplo85) </strong></span>Sea $V=\mathbb{F}^{n\times n}$, el espacio de todas las matrices $n\times n$ sobre $\mathbb{F}$. Entonces $V$ es isomorfo de forma natural al espacio $\mathbb{F}^{n^{2}}$, entonces se sigue: $$(A|B)=\sum_{i,j}A_{ij}\bar{B}_{ij}$$ define un producto interno sobre $V$. Si definimos $[B^{\ast}]_{kj}=\bar{B}_{jk}$, entonces $(A|B)=tr(AB^{\ast})=tr(B^{\ast}A)$. 
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-5"><strong>(\#exm:unnamed-chunk-5) </strong></span>Sea $V$ el espacio vectorial de las funciones continuas de valores complejos definidas en el intervalo $[0,1]$. La operación $$(f|g)=\int_{0}^{1} f(t)\bar{g(t)}dt$$ es un producto interno en $V$. Para funciones a valores reales, la misma operación omitiendo el conjugado, es un producto interno sobre el espacio respectivo.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-6"><strong>(\#exm:unnamed-chunk-6) </strong></span>Se pueden construír productos internos a partir de un producto interno dado. Sean $V$ y $W$ espacios vectoriales sobre $\mathbb{F}$. Sea $(|)$ es un producto interno en $W$. Sea $T$ una transformación lineal inyectiva de $V$ en $W$, entonces la operación $$p_{T}(\alpha|\beta)=(T\alpha|T\beta)$$ define un producto interno en $V$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-7"><strong>(\#exm:unnamed-chunk-7) </strong></span>Sea $\mathbb{F}^{n\times 1}$ el espacio de las matrices columnas $n\times 1$ sobre $\mathbb{F}$ y sea $P$ una matriz $n\times n$ invertible. Definimos la operación $$(A|B)=B^{\ast}P^{\ast}PA$$ para $A,B\in \mathbb{F}^{n\times 1}$. Si identificamos la matriz $1\times 1$ con el único elemento que la conforma, tenemos una operación de $\mathbb{F}^{n\times 1}\times \mathbb{F}^{n\times 1}$ en el campo $\mathbb{F}$ que resulta ser un producto interno. Note que si $P$ es la matriz unidad, entonces la operación es la misma (esencialmente) que la del ejemplo \@ref{ejemplo85}. También es un caso particular del ejemplo anterior.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-8"><strong>(\#exm:unnamed-chunk-8) </strong></span>Sea $V$ un espacio vectorial de dimensión finita y sea $\mathcal{B}=\{\beta_{1},\beta_{2},\cdots,\beta_{n}\}$ una base ordenada de $V$. Sean $\epsilon_{1},\epsilon_{2},\cdots,\epsilon_{n}$ la base canónica en $\mathbb{F}^{n}$. Sea $T$ la transformación lineal de $V$ en $\mathbb{F}^{n}$ definida por $T\beta_{j}=\epsilon_{j}$, para cada $1\leq j\leq n$. Entonces $$p_{T}(\sum_{i=1}^{n}x_{i}\beta_{i}\sum_{j=1}^{n}y_{j}\beta_{j})=\sum_{i=1}^{n} x_{i}\bar{y_{i}}$$ es un producto interno en vista del ejemplo anterior. De este modo, para cada base de $V$, existe un producto interno sobre $V$ con la propiedad $(\beta_{i}|\beta_{j})=\delta_{ij}$.
</div>\EndKnitrBlock{example}

\BeginKnitrBlock{example}<div class="example"><span class="example" id="exm:unnamed-chunk-9"><strong>(\#exm:unnamed-chunk-9) </strong></span>Sea $V$ el espacio de las funciones continuas en el intervalo $[0,1]$ y $W=V$. Sean $T$ el operador $(Tf)(t)=tf(t)$ para $0\leq t\leq 1$. Es fácil ver que $T$ es lineal, además que $T$ es no singular, en efecto, $Tf=0$ si y solo si $tf(t)=0$ para todo $0\leq t\leq 1$, si y solo si $f(t)=0$ para todo $0< t\leq 1$. Pero en $t=0$, como $f$ es continua, $f(0)=0$. 
</div>\EndKnitrBlock{example}