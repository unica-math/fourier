![PNS](http://caillau.perso.math.cnrs.fr/logo-unica.png)
## M1 MPA
# Analyse de Fourier et distributions
# 2024-25

# Exam CC no. 1

**Durée 2 H. Documents non autorisés.**

## Exercice 1 (3 points)

Soit $\rho$ dans $L^1(\mathbf{R})$ telle que $\int_{\mathbf{R}} \rho(x)\,\mathrm{d}x = 1$. Pour $n$ dans $\mathbf{N}$ on pose $\rho_n(x) : = n \rho(nx)$. Soit $\varphi$ dans $\mathscr{C}_c(\mathbf{R})$, montrer que

$$ \int_{\mathbf{R}} \rho_n(x) \varphi(x)\,\mathrm{d}x \to \varphi(0),\quad n \to \infty. $$
 
**Réponse.** On pose $y=nx$ et on voit que

$$ \int_{\mathbf{R}} \rho_n(y) \varphi(y/n)\,\mathrm{d}y \to \varphi(0),\quad n \to \infty $$

par CV dominée puisque $\varphi$ est continue en $0$ et que

$$ |\rho_n(y) \varphi(y/n)| \leq \|\varphi\|_\infty |\rho(y)|. $$


## Exercice 2 (7 points)

Soit $(f_n)_n$ une suite de (classes de) fonctions dans $L^1(X,\mathscr{B},\mu)$, où $(X,\mathscr{B},\mu)$ est un espace mesuré (qu'on pourra supposer $\sigma$-fini). On suppose que

$$ \sum_{n=0}^\infty \|f_n\|_1 < \infty. $$

### 2.1

Montrer que 

$$ \int_{\mathbf{X}} \sum_{n=0}^\infty |f_n|\,\mathrm{d}\mu < \infty. $$


**Réponse.** Par CV monotone appliquée à la suite des sommes partielles de la série de (classes de) fonctions de terme général $|f_n(x)|$, somme et intégrale commutent. [Aussi : Tonelli.]

### 2.2

Montrer que, presque pour tout $x$ dans $X$, la série de terme général $f_n(x)$ est absolument convergente, et en déduire l'existence de $f$, mesurable, telle que cette série converge simplement presque partout vers $f$.

**Réponse.** D'après la question précédente, on a CVS $\mu$-presque pour tout $x$ de la série de terme général $|f_n(x)|$, donc CVS $\mu$-p.p. de la série voulue dans $\mathbf{R}$, complet.

### 2.3

Montrer que $f$ appartient à $L^1(X,\mathscr{B},\mu)$.

**Réponse.** Pour $N \in \mathbf{N}$, majorer selon

$$ \int_X |\sum_{n=0}^\infty f_n(x)|\,\mathrm{d}\mu \leq \int_X \sum_{n=0}^\infty |f_n(x)|\,\mathrm{d}\mu < \infty. $$

### 2.4

À l'aide du théorème de convergence dominée, montrer que la série de terme général $f_n$ converge vers $f$ dans $L^1(X,\mathscr{B},\mu)$.

**Réponse.** La convergence simple de la suite des sommes partielles $\mu$-p.p. est connue et, pour tout $N \in \mathbf{N}$,

$$ |\sum_{n=0}^N f_n(x)|\,\mathrm{d}\mu \leq \sum_{n=0}^\infty |f_n(x)| $$

dont le second membre est intégrable, d'où le résultat par CV dominée.

### 2.5

Soit $(E,\|\cdot\|)$ un espace vectoriel normé sur lequel, pour les séries, la convergence normale (*i.e.* $\sum_{n=0}^\infty \|x_n\| < \infty$) implique la convergence (*i.e.* convergence des sommes partielles $(\sum_{n=0}^N x_n)_N$). Montrer qu'un tel espace est complet. La réciproque est-elle vraie ?

**Indication.** On pourra montrer que toute suite de Cauchy $(x_n)$ de $E$ possède une suite extraite telle que $\| x_{\varphi(n + 1)} - x_{\varphi(n)} \| \leq 1/2^n$.

**Réponse.** Soit $(x_n)_n$ de Cauchy ; on peut extraire pour avoir $\| x_{\varphi(n + 1)} - x_{\varphi(n)} \| \leq 1/2^n$, de sorte que la série de terme général $x_{\varphi(n + 1)} - x_{\varphi(n)}$ est normalement convergente, donc convergente. La suite $(x_n)_n$ possède par conséquent une valeur d'adhérence, donc converge puisqu'elle est de Cauchy. La réciproque est vraie (appliquer le critère de Cauchy à la suite des sommes partielles).

## Exercice 3 (6 points)

Soient $f$ dans $L^1(\mathbf{R})$ et $g$ dans $L^p(\mathbf{R})$, $1 < p \leq \infty$. Le but de l'exercice est de (re)démontrer que la convolution est bien définie dans ce cas (sans réutiliser le résultat général vu en TD pour $1/p + 1/q = 1 + 1/r$).

### 3.1

Montrer que la convolution $(f * g)(x)$ est bien définie pour tout $x$ dans $\mathbf{R}$ quand $p = \infty$, et que $f * g$ appartient à $L^\infty(\mathbf{R})$ avec 

$$ \|f * g\|_\infty \leq \|f\|_1 \|g\|_\infty. $$

**Réponse.** À $x$ fixé, il suffit de majorer $|f(y)g(x-y)|$ par $\|g\|_\infty |f(y)|$ p.p. $y$ pour avoir l'existence et la majoration voulue.

### 3.2

On suppose désormais $1 < p < \infty$, et on note $q$ l'exposant conjugué de $p$. Remarquer que

$$ |f(x-y)g(y)| = |f(x-y)|^{1/q}|f(x-y)|^{1/p}|g(y)|, $$

et montrer que, presque pour tout $x$, les fonctions de la variable $y$ définies par $|f(x-y)|^{1/q}$ d'une part, $|f(x-y)|^{1/p}|g(y)|$ d'autre part, sont respectivement dans $L^q(\mathbf{R})$ et $L^p(\mathbf{R})$.

**Réponse.** Presque pour tout $x$, $|f(x-y)||g(y)|^p$ est intégrable comme convolution de fonctions $L^1$.
### 3.3

En déduire que  la convolution $(f * g)(x)$ est bien définie presque pour tout $x$ dans $\mathbf{R}$, et que $f * g$ appartient à $L^p(\mathbf{R})$ avec 

$$ \|f * g\|_p \leq \|f\|_1 \|g\|_p. $$

**Réponse.** Presque pour tout $x$, on peut appliquer Hölder au produit précédent, soit

$$ \int_{\mathbf{R}} |f(x-y)g(y)|\,\mathrm{d}y \leq \|f\|_1^{1/q} (|f| * |g|^p)^{1/p}(x) < \infty, $$

ce qui montre que la convolution est bien définie et permet ensuite de majorer selon

$$ \int_{\mathbf{R}} |f * g(x)|^p\,\mathrm{d}x \leq \|f\|_1^{p/q} \|f\|_1 \|g\|_p, $$

d'où l'appartenance à $L^p$ et la majoration voulue.

## Exercice 4 (4 points)

On définit, pour $t > 0$,

$$ g_t(x) := \frac{1}{\sqrt{2\pi t}} e^{-\frac{x^2}{2t}},\quad x \in \mathbf{R}. $$

### 4.1

Soient $0 < s < t$, montrer que le produit de convolution $g_{t-s} * g_s$ est bien défini et donner sa régularité. 

**Réponse.** Les fonctions $g_t$ sont dans tous les $L^p$, $p \in [1,\infty]$, donc leur convolution aussi. Elle est aussi uniformément continue (prendre deux exposants conjugués). (On peut aussi vérifier qu'elle est $\mathscr{C}^\infty$.)

### 4.2

Montrer que $g_{t-s} * g_s = g_t$ et interpréter ce résultat en termes de probabilités.

**Réponse.** Remarquer que, pour $x$ et $y$ réels,

$$ \frac{(x-y)^2}{2(t-s)} + \frac{y^2}{2s} = \frac{x^2}{2t} + \underbrace{\frac{t}{2s(t-s)}}_{=: \alpha}(y-sx/t)^2, $$

puis calculer la convolution en changeant de variable selon $z = \sqrt{\alpha}(y-sx/t)$. On en déduit l'expression voulue, ce qui montre que la somme de deux v.a. de lois normales indépendantes centrées a pour variance la somme des variances.  
