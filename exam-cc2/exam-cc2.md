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

$$ \begin{align}
  \int_{\mathbf{R}} \widehat{f}(y) g(y)\ \mathrm{d}y
  & = \int_{\mathbf{R}} ( \int_{\mathbf{R}} e^{-2i\pi yx}f(x)\ \mathrm{d}x ) g(y)\ \mathrm{d}y\\
  & = \int_{\mathbf{R}} f(x) ( \int_{\mathbf{R}} e^{-2i\pi yx}g(y)\ \mathrm{d}y ) \ \mathrm{d}x\\
  & = \int_{\mathbf{R}} f(x) \widehat{g}(x)\ \mathrm{d}x.
\end{align} $$

### 1.2
Soit $a > 0$, on définit $\psi(x) = a e^{-\pi x^2}$, $x \in \mathbf{R}$. Déterminer $a$ pour que $||\widehat{\psi}||_1=1$. (On prend cette valeur pour $a$ dans la suite de l'exercice.) 

**Réponse.** $a=1$

### 1.3
Pour $n \geq 1$, pose $\psi_n(x) := \psi(x/n)$, $x \in \mathbf{R}$. Montrer que, quelle que soit $f \in L^1(\mathbf{R})$, la suite $(\widehat{\psi_n} * f)_n$ converge vers $f$ dans $L^1(\mathbf{R})$ quand $n \to \infty$.

**Réponse.** Comme $\widehat{\psi}=\psi$, $||\widehat{\psi}||_1 = 1$ ; on a $\widehat{\psi_n}(\xi)=n\widehat{\psi}(n\xi)$, et encore $||\widehat{\psi_n}||_1=1$. Soit $f$ dans $L^1(\mathbf{R})$ et soit $\varepsilon > 0$. Il existe $g$ continue à support compact telle que $||f-g||_1 \leq \varepsilon$, donc

$$ \begin{align}
  ||\widehat{\psi_n} * f - f||_1 & \leq ||\widehat{\psi_n} * (f-g)||_1 + ||\widehat{\psi_n} * g - g||_1 + ||f-g||_1\\
  & \leq ||\widehat{\psi_n}||_1 ||f-g||_1 + ||\widehat{\psi_n} * g - g||_1 + \varepsilon\\
  & \leq 2\varepsilon + ||\widehat{\psi_n} * g - g||_1
\end{align} $$

et (changement de variable $z=ny$ puis Fubini)

$$ \begin{align}
  ||\widehat{\psi_n} * g - g||\_1 & = \int_{\mathbf{R}} | \int_{\mathbf{R}} \widehat{\psi_n}(y)g(x-y)\ \mathrm{d}y - g(x) |\ \mathrm{d}x\\
  & \leq \int_{\mathbf{R}} \widehat{\psi}(z) ( \int_{\mathbf{R}} |g(x-z/n)-g(x)|\ \mathrm{d}x )\ \mathrm{d}z 
\end{align} $$

sachant qu'on peut majorer l'intégrale interne par $\varepsilon$ pour $n$ assez grand par uniforme continuité de $g$.

### 1.4
On considère désormais $f$ dans $L^1(\mathbf{R})$ telle que $\widehat{f}=0$. Soit $b$ dans $\mathbf{R}$, montrer que

$$ \widehat{\psi_n} * f(b) = 0. $$

**Indication.** On pourra considérer le produit $\widehat{f}(y)\psi_n(y) e^{2i\pi by}$.

**Réponse.**

$$ \begin{align}
  0 &= \int_{\mathbf{R}} \widehat{f}(y)\psi_n(y)e^{2i\pi by}\ \mathrm{d}y\\
  &= \int_{\mathbf{R}} f(x) \widehat{\psi_n(y)e^{2i\pi by}}(x)\ \mathrm{d}x \text{ (par 1.1)}\\
  &= \int_{\mathbf{R}} f(x) \widehat{\psi_n}(x-b)\ \mathrm{d}x\\
  &= \int_{\mathbf{R}} f(x) \widehat{\psi_n}(b-x)\ \mathrm{d}x \text{ (parité)}\\
  &= \widehat{\psi_n} * f(b).
\end{align} $$

### 1.5
En déduire que $f=0$. Que conclut-on ?

**Réponse.** Comme $0 = \widehat{\psi_n} * f \to f$ dans $L^1(\mathbf{R})$, $f=0$ et on injectivité de la transformée de Fourier sur cet espace.

## Exercice 2 (10 points)

### 2.1
Soit $a > 0$. Déterminer la transformée de Fourier de $h_a(x) := e^{-a|x|}$, $x \in \mathbf{R}$. 

**Réponse.**

$$ \widehat{h_a}(\xi) = \frac{2a}{a^2 + 4\pi^2\xi^2} $$

### 2.2
Soit $\beta \in \mathbf{R}$. À l'aide de la question précédente, montrer que

$$ e^{-|\beta|} = \frac{2}{\pi} \int_0^\infty \frac{\cos(\beta y)}{1+y^2}\ \mathrm{d}y. $$

**Réponse.** Soit $\beta \in \mathbf{R}$, d'après la question précédente (avec $a=1$ et en utilisant la parité)

$$ \begin{align}
  e^{-|\beta|} &= \mathscr{F}^{-1}(\frac{2}{1+4\pi^2\xi^2})\\
  &= 2\int_0^\infty \cos(2\pi\beta\xi) \frac{2}{1+4\pi^2\xi^2}\ \mathrm{d}\xi\\
  &= \frac{2}{\pi} \int_0^\infty \cos(\beta y) \frac{2}{1+y^2}\ \mathrm{d}y.
\end{align} $$

### 2.3
En déduire que

$$ e^{-|\beta|} = \int_0^\infty \frac{1}{\sqrt{\pi u}}e^{-u-\beta^2/(4u)}\ \mathrm{d}u. $$

**Indication.** On pourra utiliser le fait que

$$ \frac{1}{1+y^2} = \int_0^\infty e^{-(1+y^2)u}\ \mathrm{d}u,\quad y \in \mathbf{R}. $$

**Réponse.** On vérifie (Tonelli) qu'on peut Fubiniser l'intégrale ci-dessous, d'où

$$ \begin{align}
  e^{-|\beta|} &= \frac{2}{\pi} \int_0^\infty \cos(\beta y) ( \int_0^\infty e^{-(1+y^2)u}\ \mathrm{d}u ) \ \mathrm{d}y\\
  &= \frac{1}{\pi} \int_0^\infty e^{-u} \underbrace{( 2\int_0^\infty \cos(\beta y) e^{-uy^2}\ \mathrm{d}y}_{=\widehat{e^{-uy^2}(\beta/(2\pi))}} )\ \mathrm{d}u\\
\end{align} $$

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