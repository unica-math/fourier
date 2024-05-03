![PNS](http://caillau.perso.math.cnrs.fr/logo-unica.png)
## M1 MPA
# Analyse de Fourier et distributions
# 2023-24

# Exam CC no. 2

**Durée 2H. Les exercices sont indépendants. Documents non autorisés.**

## Exercice 1 (10 points)

### 1.1
Soient $f$ et $g$ dans $L^1(\mathbf{R})$, montrer que

$$ \int_{\mathbf{R}} \widehat{f}(y) g(y)\ \mathrm{d}y = \int_{\mathbf{R}} f(y) \widehat{g}(y)\ \mathrm{d}y. $$

**Réponse.** Par Tonelli,

$$ \int_{\mathbf{R}} |\widehat{f}(y) g(y)|\ \mathrm{d}y
 = \int_{\mathbf{R}} | \int_{\mathbf{R}} e^{-2i\pi yx}f(x)\ \mathrm{d}x | g(y)\ \mathrm{d}y \leq ||f||_1 ||g||_1 < \infty $$

 donc l'intégrale (de même que l'autre par symétrie) est bien définie, et Fubini s'applique :

$$ \begin{array}{rcl} \displaystyle
  \int_{\mathbf{R}} \widehat{f}(y) g(y)\ \mathrm{d}y
  & = & \int_{\mathbf{R}} ( \int_{\mathbf{R}} e^{-2i\pi yx}f(x)\ \mathrm{d}x ) g(y)\ \mathrm{d}y\\
  & = & \int_{\mathbf{R}} f(x) ( \int_{\mathbf{R}} e^{-2i\pi yx}g(y)\ \mathrm{d}y ) \ \mathrm{d}x\\
  & = & \int_{\mathbf{R}} f(x) \widehat{g}(x)\ \mathrm{d}x.
\end{array} $$

### 1.2
Soit $a > 0$, on définit $\psi(x) = a e^{-\pi x^2}$, $x \in \mathbf{R}$. Déterminer $a$ pour que $||\widehat{\psi}||_1=1$. (On prend cette valeur pour $a$ dans la suite de l'exercice.) 

**Réponse.**

### 1.3
Pour $n \geq 1$, pose $\psi_n(x) := \psi(x/n)$, $x \in \mathbf{R}$. Montrer que, quelle que soit $f \in L^1(\mathbf{R})$, la suite $(\widehat{\psi_n} * f)_n$ converge vers $f$ dans $L^1(\mathbf{R})$ quand $n \to \infty$.

**Réponse.**

### 1.4
On considère désormais $f$ dans $L^1(\mathbf{R})$ telle que $\widehat{f}=0$. Soit $b$ dans $\mathbf{R}$, montrer que

$$ \widehat{\psi_n} * f(b) = 0. $$

**Indication.** On pourra considérer le produit $\widehat{f}(y)\psi_n(y) e^{2i\pi by}$.

**Réponse.**

### 1.5
En déduire que $f=0$. Que conclut-on ?

**Réponse.**

## Exercice 2 (10 points)

### 2.1
Soit $a > 0$. Déterminer la transformée de Fourier de $h_a(x) := e^{-a|x|}$, $x \in \mathbf{R}$. 

**Réponse.**

### 2.2
Soit $\beta \in \mathbf{R}$. À l'aide de la question précédente, montrer que

$$ e^{-|\beta|} = \frac{2}{\pi} \int_0^\infty \frac{\cos(\beta y)}{1+y^2}\ \mathrm{d}y. $$

**Réponse.**

### 2.3
En déduire que

$$ e^{-|\beta|} = \int_0^\infty \frac{1}{\sqrt{\pi u}}e^{-u-\beta^2/(4u)}\ \mathrm{d}u. $$

**Indication.** On pourra utiliser le fait que

$$ \frac{1}{1+y^2} = \int_0^\infty e^{-(1+y^2)u}\ \mathrm{d}u,\quad y \in \mathbf{R}. $$

**Réponse.**

### 2.4
On considère désormais $f(x) := e^{-|x|}$, $x \in \mathbf{R^d}$. (Pour $d \geq 1$, on note $|x|=\sqrt{|x_1|^2 + \cdots + |x_d|^2}$.) Pour $u > 0$, on pose $g_u(x) := e^{-|x|^2/(4u)}$, $x \in \mathbf{R}^d$. Montrer que

$$ \widehat{f}(\xi) = \int_0^\infty \frac{1}{\sqrt{\pi u}} e^{-u}\ \widehat{g_u}(\xi)\ \mathrm{d}u,\quad \xi \in \mathbf{R^d}. $$

**Réponse.**

### 2.5
Calculer $\widehat{g_u}$ et en déduire que

$$ \widehat{f}(\xi) = \frac{2^d\pi^{(d-1)/2}\ \Gamma(\frac{d+1}{2})}{(1+4\pi^2|\xi|^2)^{(d+1)/2}}\ ,\quad \xi \in \mathbf{R}^d, $$

où

$$ \Gamma(y) := \int_0^\infty t^{y-1}e^{-t}\ \mathrm{d}t,\quad y > 0. $$

**Indication.** On rappelle que $\widehat{e^{-\pi|x|^2}} = e^{-\pi|\xi|^2}$. 

**Réponse.**