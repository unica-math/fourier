
![PNS](http://caillau.perso.math.cnrs.fr/logo-unica.png)
## M1 MPA
# Analyse de Fourier et distributions
# 2024-25

# Exam CC no. 2

**Durée 2 H. Documents non autorisés.**

## Exercice 1 (6 points)

On considère une fonction qui à tout $(t,x)\in [0,+\infty[\times \mathbf{R}$, associe $u(t,x)\in \mathbf{R}.$ On suppose que pour $t\geq 0$, $u(t,\cdot), \partial_t u(t,\cdot), \partial_x u(t,\cdot)$ et $\partial_{xx} u(t,\cdot)$ sont toutes dans $L^1(\mathbf{R})$. On cherche à décrire un tel $u$ vérifiant l'équation de la chaleur unidimensionnelle : 

$$ \partial_t u(t,x) = \partial_{xx}u(t,x),\quad (t,x) \in ]0,+\infty[\times \mathbf{R}, $$

$$ u(0,x) = u_0(x),\quad x \in \mathbf{R}. $$

### 1.1

Pour tout $t> 0$ fixé, exprimer $\mathscr{F}(\partial_{xx}u(t,\cdot))$ en fonction de $\widehat{u}(t,\xi) = \mathscr{F}(u(t,\cdot))$.

### 1.2

Montrer que pour tout $\xi \in \mathbf{R}$, $t\mapsto \widehat{u}(t,\xi)$ satisfait une équation différentielle linéaire. En déduire la valeur de $\widehat{u}(t,\xi)$ en fonction de $\widehat{u}_0(\xi)$.

### 1.3

En déduire $u(t,x)$ pour tout $t>0$ et $x\in \mathbf{R}$ sous la forme d'un produit de convolution.

*Indication.* On rappelle qu'une gaussienne $e^{-ax^2/2}$, $a > 0$, a pour transformée de Fourier $(1/\sqrt{a})e^{-\xi^2/(2a)}$.

### 1.4

Pour $t > 0$, on considère la distribution tempérée $G_t = T_{g_t}$ définie par la gaussienne

$$ g_t(x) := \frac{1}{\sqrt{4\pi t}} e^{-x^2/(4t)}. $$

Montrer que $G_t$ tend vers $\delta$ dans $\mathscr{S}'(\mathbf{R})$ quand $t$ tend vers $0$. Que peut-on en déduire ?

## Exercice 2 (6 points)

Soit $T$ une distribution tempérée telle que $T' = 0$. On note $\mathscr{D}(\mathbf{R})$ l'ensemble des fonctions $\mathscr{C}^\infty$ à support compact.

### 2.1

Montrer que $T$ s'annule sur toute fonction de l'ensemble

$$ \mathscr{A} = \{ \varphi',\ \varphi \in \mathscr{D}(\mathbf{R}) \}. $$

### 2.2

Montrer que l'ensemble $\mathscr{A}$ est égal à

$$ \mathscr{B} = \{ \psi\in \mathscr{D}(\mathbf{R}) \text{ t.q. } \int_{\mathbf{R}} \psi = 0 \}. $$

### 2.3

Soit $\varphi \in \mathscr{D}(\mathbf{R})$, et soit $\varphi_0$ une fonction de $\mathscr{D}(\mathbf{R})$ telle que $\int_{\mathbf{R}} \varphi_0 = 1$ ; remarquer que $\varphi - (\int_{\mathbf{R}} \varphi) \varphi_0$ appartient à $\mathscr{B}$, et en déduire qu'il existe une constante $C$ telle que

$$ \langle T, \varphi \rangle = \langle T_C, \varphi \rangle. $$

### 2.4

Conclure. 

*Indication.* On pourra utiliser la densité de $\mathscr{D}(\mathbf{R})$ dans $\mathscr{S}(\mathbf{R})$.

## Exercice 3 (8 points)

On rappelle que

$$ \langle \mathrm{vp}\frac{1}{x},\varphi \rangle := \lim_{\varepsilon \to 0} \int_{|x| \geq \varepsilon} \frac{\varphi(x)}{x}\,\mathrm{d}x $$

définit une distribution tempérée.

## 3.1

Montrer que, pour $\varphi \in \mathscr{S}(\mathbf{R})$,

$$ \langle \mathrm{vp}\frac{1}{x},\varphi \rangle = \int_0^1 \frac{\varphi(x) - \varphi(-x)}{x}\,\mathrm{d}x + \int_{|x| \geq 1} \frac{\varphi(x)}{x}\,\mathrm{d}x. $$

## 3.2 

Soit $\varepsilon > 0$, montrer qu'à la fonction $v_\varepsilon(x) := \frac{x}{x^2 + \varepsilon^2}$ on peut associer une distribution tempérée, $V_\varepsilon := T_{v_\varepsilon}$.

## 3.3

Montrer que $V_\varepsilon$ tend vers $\mathrm{vp}\frac{1}{x}$ dans $\mathscr{S}'(\mathbf{R})$ quand $\varepsilon$ tend vers $0$.

## 3.4

Montrer que $x \cdot \mathrm{vp}\frac{1}{x} = T_1$.

## 3.5

En déduire $(\widehat{\mathrm{vp}\frac{1}{x}})'$.

## 3.6

En déduire (à l'aide du **2.4**) qu'il existe une constante $C$ telle que 

$$ \widehat{\mathrm{vp}\frac{1}{x}} = S + T_C $$

où $S$ est une distribution que l'on précisera.
