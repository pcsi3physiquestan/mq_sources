---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# Fonction d'onde

## Fonction d'onde

### Définition

````{topic} Introduction
La description des interférences nécessite un traitement ondulatoire (quand même!). L'idée a donc été d'associer à chaque particule une fonction dont le comportement peut être associé à celui d'une onde: on y trouvera donc __possiblement__  un terme de propagation et une amplitude et donc les caractéristiques d'une onde. Mais comme on va le voir, on pourra aussi avoir une interprétation de concepts corpusculaires.
````


````{sidebar} Remarque
Ceci constitue un énoncé remanié du premier postulat de la mécanique quantique (en réalité, dans le formalisme de la mécanique quantique, on utilise plus des fonctions mais plus généralement des vecteurs d'état). Précisons qu'il s'agit d'un postulat. Il précise que tout l'information est contenue dans la fonction d'onde (pas de variables cachées qu'on ne connaîtrait pas encore).
````
````{important} __Fonction d'onde__

La connaissance de l'état d'un système donnée à un instant donné est entièrement contenu dans une fonction appelée fonction d'onde $\Psi(M,t)$. Cette fonction doit posséder les caractéristiques suivantes (entre autre):


* Elle est de carré sommable (sur $\mathbb{R}^3$, cf [suite](proba)) .
* Elle est complexe par nature.
````


(proba)=
### Fonction d'onde - Probabilité


Nous avons dit que la fonction d'onde définissait complètement les caractéristiques d'un système. Il convient maintenant de remonter à des grandeurs qu'on peut interprêter à notre échelle. Il ne s'agit pas ici de présenter complètement la théorie quantique (qui nécessite notamment une bonne connaissance d'algèbre linéaire) mais de présenter un point particulier: la notion de probabilité de présence.


````{important} __Probabilité de présence__

La probabilité dP de détecter une particule dans un petit volume $\delta \tau$ autour du point M à un instant t est donné par:

$$
dP = A \vert \Psi^2(M,t) \vert d \tau
$$
où $\vert \Psi^2(M,t) \vert$ est le module au carré de la fonction d'onde. $\Psi^2(M,t)$ est appelée densité de probabilité de présence.

A est un facteur de normalisation de sorte que la probabilité totale sur tout l'espace soit 1.
````

````{topic} Remarques générales

* il s'agit d'une probabilité de présence. Ce qui signifie que temps qu'on a pas réalisé une observation (humaine, appareil... ), on ne sait pas où se trouve la particule. Ce concept est fondamental en mécanique quantique, on n'a accès a priori qu'à des probabilités de présence. Comme on le précisera par la suite, l'observation implique la modification de cette fonction d'onde, autrement dit " perturbe le système " .
* Cette notion a souvent fait penser que le déterminisme n'était plus de mise. Il faut prendre cette idée avec beaucoup de réserves. En effet, si les notions classiques de trajectoire, de position ne sont pas connues avec certitude à chaque instant si l'on ne fait pas la mesure, l'évolution de la fonction est elle parfaitement décrite par la mécanique quantique (équation de Schrödinger): on retrouve alors la notion de déterminisme. Le problème est qu'il n'est plus accessible, avec une précision __théoriquement__  infinie à nos observations. On notera notamment que les mesures expérimentales les plus précises sont associées à la mécanique quantique .
* La probabilité d'observer la particule dans tout l'espace est nécessairement de 1. C'est pourquoi il faut que la somme du moduel au carré sur tout l'espace soit finie (fonction de carré sommable) .
* Une différence fondamentale est l'absence de valeur moyenne. Il s'agit d'une probabilité de présence à un instant t. Dans le cas d'onde classique, il s'agirait de l'énergie reçue graduellement sur une " période ".
````

### Interprétation de l'expérience d'interférence

````{admonition} Exemple
:class: attention

On considère le cas des interférences au moyen d'un dispositif des trous d'Young pour des électrons.

Sachant qu'on peut alors appliquer un "pseudo" principe de superposition à la fonction d'onde associé à l'électron, expliquer, calcul à l'appui, pourquoi cette dernière est cohérente avec le principe d'une répartition des électrons n'étant pas la somme des faisceaux issus des deux fentes.
````

### Remarques (en ligne)

````{attention}

C'est important de ne pas confondre la fonction d'onde associé à une particule (ou plus généralement à un système) et l'amplitude complexe d'une onde classique.

````

````{topic} Analogie mathématique
Rappelons d'abord les caractéristiques générale d'une onde:

* Elle peut se caractériser par une direction (instantanée) et une vitesse (instantanée) de propagation. __Pour simplifier, on pourra supposer une propagation rectiligne uniforme.__
* L'amplitude de l'onde peut se décomposer en somme d'ondes sinusoïdales (décomposition en série de Fourier) auxquelles on peut associer une fréquence $f$, une longueur d'onde $\lambda$ ou directement un vecteur d'onde $\overrightarrow{k} = \frac{2 \pi}{\lambda} \overrightarrow{u}$ où $\overrightarrow{u}$ est la direction de propagation .
* Pour représenter une onde sinusoïdale, on peut utiliser sa représentation complexe $A(M,t) = A(M) e^{j (\omega t - \overrightarrow{k} \cdot \overrightarrow{OM})}$. Cette représentation complexe reste une représentation mathématique permettant des calculs plus aisés (notamment pour les interférence) mais le contenu physique n'est contenu QUE dans la partie réelle de cette représentation .
* La superposition des ondes ne correspond pas nécessairement à un phénomène de propagation: citons en exemple les ondes stationnaires. On peut les décomposer en plusieurs ondes progressives mais la somme donne un effet où il n'y a plus de propagation de l'énergie.
````

````{topic} Différences
Ces différents points peuvent être repris pour étudier mathématiquement la fonction d'onde: c'est d'ailleurs grâce à ces analogies qu'on peut décrire le caractère ondulatoire de la matière mais plusieurs nuances doivent être apportés:

* Dans les cas le plus souvent étudiés, il n'y a pas de phénomènes de propagation, on est donc plus souvent sur des types d'ondes stationnaires (cf le cas du corps noir) .
* La fonction d'onde est cette fois PAR DEFINITION complexe: cela signifie qu'on ne peut se "débarrasser de la partie imaginaire" en passant au réel comme d'un artifice mathématique. Ceci est fondamental est sera précisé en deuxième année (l'équation de Schrödinger est complexe) .
* Si l'on peut toujours se ramener à décomposer un signal en série de Fourier, il faut noter qu'on ne peut associer une fonction purement sinusoïdale à une fonction d'onde: la probabilité de présence totale serait alors infinie.
````

````{topic} Aspects corpusculaires importants
On pourrait croire à travers l'analogie entre onde classique et fonction d'onde que toute la matière n'est qu'onde. Il est important de comprendre que ce n'est pas le cas. En effet, si l'on regarde de plus près la fonction d'onde, on voit plusieurs points importants:

* Rappelons déjà son caractère fondamentalement complexe* La fonction d'onde contient toutes les informations. Elle doit donc pouvoir décrire les expériences où l'interprétation est de nature corpusculaire. Comment décrire la vitesse de la particule. Il apparaît que cette vitesse n'est PAS la célérité de l'onde dans les cas généraux. On voit donc la limite de cette conception .
* La notion d'onde classique suppose un phénomène physique étendu dans l'espace. On peut ainsi observer, dans l'approche classique l'influence d'une onde en plusieurs positions au même instant. Ce n'est PAS le cas pour la fonction d'onde. En effet, la détection d'un phénomène associé au système localise le __système__  à l'endroit donné. Il y alors un "repli" "'' instantanée de la fonction d'onde au point où l'on a détecté la particule (on parle de __réduction du paquet d'onde__ ): on ne peut détecter la particule au même instant ailleurs. C'est d'ailleurs là que l'aspect corpusculaire apparaît.

Ce point est fondamental: il apparaît que l'observation a perturbé le système: son comportement après l'observation n'est plus entièrement déterminée par son état antérieur à la mesure. Comme on ne peut réaliser deux mesures simultanées (rigoureusement parlant), cela signifie que ne pourra avoir deux informations simultanée: ainsi on ne peut connaître simultanément la vitesse et la position d'une particule.

On verra que ce concept s'exprime de manière quantitative grâce aux inégalités d'Heisenberg.
````


## Quantification des états liés

_La quantification des états liés est fondamentale en mécanique quantique. Elle est une conséquence directement du caractère ondulatoire de la matière. Pour simplifier l'explication ce phénomène nous allons nous ramener à traiter la fonction d'onde comme une onde classique. Il faut néanmoins garder en mémoire toutes les précautions mise en évidence ci-dessus. C'est un point important qu'il faut comprendre associé à la notion de complémentarité. La description de tel ou tel phénomène quantique passe par le choix d'une représentation ondulatoire ou corpusculaire. Souvent dans ce choix, on " oublie " momentanément l'autre aspect qui existe bel et bien._

### Principe

````{important} __Le phénomène de quantification__

La quantification des états de la matière correspond au caractère quantifié des états accessible, c'est-à-dire que certaines caractéristiques (énergie, moment cinétique... ) ne peuvent prendre que des valeurs discrètes.
````

````{topic} Exemple : Quantification des états des atomes

Les expériences de spectroscopie ont montré que le spectre d'émission des atomes correspondent à des longueurs d'onde bien précises et discrètes. La relation de Planck-Einstein implique que l'énergie des photons émis et donc les écarts d'énergie entre les niveaux sont discrets: les états d'énergie d'un atome sont donc quantifiés. Ainsi les niveaux énergétiques de l'atome d'hydrogène sont données par: $E_n = -\frac{13.6}{n^2} \rm{eV}$
````

### Méthode - Etude du puits de potentiel infini

````{admonition} Exercice 
:class: attention

Soit un système $\Sigma$ (potentiellement un électron, un atome... ) On considère un puits de potentiel infini:

\begin{align*}
\begin{cases}
E_p(0 < x < L) = 0\\
E_p(x < 0 OU x > L) = \infty
\end{cases}
\end{align*}
On admet que les zones où l'énergie potentielle est infinie impose une probabilité de présence nulle soit $\Psi(M,t) = 0$.

On veut chercher ici les états stationnaires, c'est-à-dire les états dont la fonction d'onde s'écrit: $\Psi(x,t) = Psi_x(x) \times Psi_t(t)$. On admet que dans ces conditions, la fonction d'onde peut s'écrire:

$$
\Psi(x,t) = e^{- \frac{i}{h} E t} \phi(x)
$$
où $E$ est l'énergie de l'état du système considéré et $\phi$ est une fonction sinusoïdale $\phi(x) = A \sin (\frac{2 \pi}{\lambda} x + \alpha)$.

1. Calculer la densité de probabilité de présence d'un état stationnaire si $\phi(x)$ est réelle. Trouver une explication au terme "stationnaire" .
1. Donner un possible sens (sans justification) à $\lambda$ .
1. Montrer qu'avec les conditions aux limites imposées, $\lambda$ ne peut prendre que des valeurs discrètes qu'on notera $\lambda_n$1. Exprimer l'énergie $E_n$ d'un état associé à $\lambda_n$. Conclure quant à la quantification des états d'énergie .
1. Que vaut l'énergie minimale du système? Comparer au cas classique .
1. Déterminer l'écart relatif $\frac{\Delta E}{E}$? Expliquer dans ce cas pourquoi on parle de "limite classique aux grands nombres quantiques" (ou de "continuum" d'énergie).


````

````{important} __A retenir__

On retiendra:
*  que les états stationnaires dans un puits de potentiel infini ont des énergies quantifiées .
* la méthode (forme mathématique initiale admise) pour démontrer la quantification de la longueur d'onde puis de l'énergie .
* Le fait que l'énergie minimale du système ne correspond plus à l'énergie potentielle minimale .
* Le fait qu'au grand nombre quantique (n grand), les états quantifiés sont __relativement__  proches de sorte qu'on puissent parler d'un continuum.


```{figure} ./images/puits_stationnaire.gif
:name: fig_314
:align: center

```
````

### Etude du puits de potentiel infini - Approfondissement

````{admonition} Exercice 
:class: attention

Soit un système $\Sigma$ (potentiellement un électron, un atome... ) On considère un puits de potentiel infini:

\begin{align*}
\begin{cases}
E_p(0 < x < L) = 0\\
E_p(x < 0 OU x > L) = \infty
\end{cases}
\end{align*}
On rappelle que la fonction d'onde des états stationnaires prend la forme:

$$
\Psi(x,t) = e^{- \frac{i}{h} E t} \phi(x)
$$
et que l'énergie $E$ et la longueur d'onde $\lambda$ sont quantifiés:

\begin{align*}
\lambda_n &= \frac{2L}{n}\\
E_n &= n^2 \frac{h^2}{8mL^2}
\end{align*}
On se propose de calculer quelques ordre de grandeurs et d'interprétation le passage du quantique au classique.

On considère une balle (tennis par exemple) glissant sans frottements dans une pièce. Les rebonds sur les murs sont supposés élastiques de sorte que l'allure du potentiel proposés en préambule puisse être considéré comme acceptable.
1. Estimer l'énergie minimale de balle dans une approche quantique puis la vitesse minimale associée. La distinction entre énergie potentielle minimale et énergie minimale dans ce cadre a-t-elle encore un sens?1. En considérant une vitesse acceptable pour une balle de tennis et une incertitude acceptable sur cette vitesse, justifier qu'on puisse considérer que l'état de la balle n'est pas un état stationnaire mais une superposition d'état stationnaire dont on déterminera approximativement le nombre quantique moyen $n_{moy}$ (à commenter) et l'intervalle $\Delta n$ d'états autour de $n_{moy}$ qui se superposent.
1. Observer la vidéo ci-après correspondant à une simulation d'un puits de potentiel infini avec un système dont la fonction d'onde est une superposition d'état quantique stationnaires (on a pris des états entre $n_{moy} - \Delta n$ et $n_{moy} + \Delta n$ et on a sommé les fonctions d'onde). Commenter l'allure obtenue de la probabilité de présence .
1. Observer les deux vidéos de comparaison de densité de probabilité de présence et commenter ce qu'on obtient on commentera notamment ce qu'on obtiendrait avec la balle de tennis.
````

__Superposition d'états quantique__
```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/videos_physique/blob/main/puits_evolution_fin.mp4?raw=true", width=640)
```

__Influence de n moyen__
```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/videos_physique/blob/main/puits_evolution_comparaison.mp4?raw=true", width=640)
```

__Influence de $\Delta n$ moyen__
```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/videos_physique/blob/main/puits_evolution_comparaison2.mp4?raw=true", width=640)
```

````{important} __A retenir__

On retiendra:


* que les états réels sont souvent des superpositions d'état stationnaire. On pourra par la suite mettre cela en lien avec le principe d'indétermination d'Heisenberg .
* que les nombres quantiques mis en jeu et le nombre d'états superposés dans le cas de système macroscopique serait gigantesque. Si la modélisation même du système est discutable, cette étude montre que les interprétations quantiques ne sont pas complètement incohérentes avec la vision classique qu'on retrouve aux aux nombres quantiques: continuum, localisation de la particule.

````

### Bilan

````{important} __Généralisation (admise)__

Considérons un système $\Sigma$ dont l'énergie potentielle est $E_p(x)$. On admet que lorsque des état liés peuvent exister, il s'établit alors une quantification des états liés: l'énergie de ces états ne peut prendre qu'une valeur discrète. L'exemple de puits carrés finis sera vus en seconde année (PC).
````

````{attention}

Nous parlons ici uniquement des états liés. Les états de diffusion  n'impose pas de condition de quantification.

````

````{topic} Exemple : Cas des atomes

Dans les atomes, les électrons sont soumis à un potentiel attracteur newtonien $E_p = -\frac{K}{r}$ avec K>0 (attraction du noyau). Il vient pour des états d'énergie tels que $E < 0$, nous sommes dans des états liés: ce sont les états stables du noyau (une énergie plus forte revient à ioniser l'atome). La propriété précédente explique la quantification des atomes.
````

````{note} __Exemple : Cas de l'oscillateur harmonique__

L'oscillateur harmonique est un système soumis au potentiel:

$$
E_p = \frac{1}{2} k x^2 = \frac{1}{2} m \omega_0^2 x^2
$$
Tous les états possibles sont des états liées. Il vient que tous les états de l'oscillateur harmonique sont liés. On peut montrer (en utilisant l'équation de Schrödinger) que l'énergie des états liés est:

$$
E_n = \hbar \omega_0 (n + \frac{1}{2})
$$
On observe que l'état fondamental (de plus basse énergie) n'est PAS (comme pour le puits quantique) l'énergie nulle (qui correspondrait à un état d'équilibre). C'est un point fondamental qu'on pourra associer par la suite aux inégalités d'Heisenberg.
````

## Inégalités d'Heisenberg

### Enoncé

````{margin}
Le principe d'incertitude relie position et quantitié de mouvement suivant un axe particulier. Il y a la même relation entre $y$ et $p_y$ par exemple. Par contre, il n'y a pas de contrainte entre l'indétermination sur $x$ et sur $p_y$.
````
````{important} __Enoncé__

Considérons un système suivant une évolution unidimensionnelle suivant un axe x. On associe sa position à une grandeur $x$ et sa quantité de mouvement àune grandeur $p_x$. L'indétermination $\Delta x$ sur la position x et l'indétermination $\Delta p_x$ sur l'impulsion $p_x$ sont reliés par la relation:

\begin{align*}
\Delta p_x \Delta x \geq \frac{\hbar}{2}
````

````{topic} Interprétation
Comment intérprêter ce principe? Remarquons trois points:

* le cas des états liés montrent que l'état fondamental ne correspond plus, comme en mécanique classique à un état d'équilibre au sens strict: un tel état n'est plus accessible .
* la notion de réduction du paquet d'onde implique l'impossibilité de mesurer certaines grandeurs successivement .
* Si les états sont quantifiés, cela veut dire qu'un état intermédiaire est impossible: comment le système peut-il alors passer d'un état à un autre?

Ces trois soulignent la différence fondamentale d'approche entre la mécanique classique et la mécanique quantique. Les deux derniers nous montrer que l'on doit renoncer au concept classique de trajectoire d'une particule car cela impliquerait de connaître l'état du système à chaque instant: __on doit admettre que la connaissance d'au moins une grandeur vitesse ou position (voire les deux) est partiellement indéterminée.__  Cela revient à dire que les aspects corpusculaire (associés à la position) et ondulatoire (associés à l'impulsion par la relation de de Broglie), s'ils sont complémentaire et indispensable ne peuvent être observés simultanément. Ce principe est mis en avant par les inégalités d'Heisenberg.

Ce principe signifie qu'on ne rendre ce produit arbitrairement petit: il est impossible de définir à la fois la position et l'impulsion avec une précision arbitraire. Les inégalités d'Heisenberg concerne des grandeurs qu'on dit conjuguées (on ne définira pas précisément ce terme ici).
````



````{topic} Indétermination et incertitude

La notion d'indétermination est souvent rapprochée de la notion d'incertitude d'un point de vue expérimental (on parle d'ailleurs de principe d'incertitude et souvent dans nos estimations on assimilera l'indétermination à l'incertitude minimale possible) MAIS ATTENTION, ce n'est qu'une façon simplifiée de voir les choses car ce principe n'est pas simplement rattaché à l'expérience, il est beaucoup plus fondamental. D'une manière générale, il faut comprendre que la position comme la vitesse sont des observables reliées à la fonction d'onde (exemple: l'observation de la position est reliée la densité de probabilité). La fonction d'onde fluctue dans l'espace. On peut lui associer un écart-type qui quantifie ces fluctuations. Ces fluctuations sont intrinsèques au système et non reliées au principe de mesure.

````

````{topic} Compléments : Cas de l'énergie

De la même manière que impulsion et position sont conjuguées, l'énergie et le temps sont aussi soumis à une inégalité:

$$
\Delta t \Delta E \geq \frac{\hbar}{2}
$$
Cette inégalité est fondamental mais d'une tournure différente car le temps n'est pas soumis aux fluctuations quantiques et quantification. Ici $\Delta t$ correspond un temps caractéristique de l'évolution notoire (d'un point de vue énergétique) du système. Elle est par exemple utilisée pour expliquer simplement la largeur de raie d'un atome.
````

### Interprétation de la diffraction

````{admonition} Exercice 
:class: attention

On considère un faisceau de particules matérielles de longueur d'onde $\lambda$ se propageant dans la direction Ox. On place un écran percé d'un trou de largeur a de manière à réduire la taille du faisceau.

1. Rappeler ce qu'il va se passer si l'on réduite trop la taille du trou .
1. Estimer dans ces condition une indétermination sur la position transverse $z$ de la particule .
1. En déduire une indétermination minimale sur la quantité de mouvement $p_z$ .
1. En déduire une estimation de l'élargissement du faisceau en sortie en calculant l'ouverture angulaire du faisceau $\sin u$. Commenter ce qu'on observe.
````

````{important} __A retenir__

On retiendra que les inégalités d'Heisenberg permettent d'expliquer simplement plusieurs effets quantiques. Mais attention, __il ne s'agit QUE d'estimation d'ordre de grandeur car ce ne sont pas de vrais calculs des indétermination.__ 
````

### Ordre de grandeur

````{admonition} Exercice 
:class: attention

Il est important de savoir estimer si les inégalités d'Heisenberg sont contraignantes ou non pour l'étude de tel ou tel système. Si elles sont contraignantes, cela signifie que la mécanique classique est sûrement mise en défaut.

1. Pour une balle de Tennis ($m = 60 \rm{g}$) frappée à $100 \rm{km.h^{-1}}$. Estimer l'indétermination minimale sur la position de la balle si l'on peut mesurer sa vitesse à $0.1 \rm{km.h^{-1}}$. Le principe d'indétermination a-il une influence a priori sur l'étude du mouvement d'une balle de Tennis?
1. Pour un électron orbitant autour d'un atome estimer l'indétermination sur la position $\Delta x$. En déduire l'indétermination sur la vitesse $v_x$. Commenter.


````

### Contraintes sur l'énergie minimale.

````{admonition} Exercice 
:class: attention

Le principe d'indétermination permet aussi d'expliquer pour l'énergie minimale d'un système ne petu être égale au minimum d'énergie contrairement au cas classique.

1. Généralités: On considère un système mécanique possédant une position d'équilibre stable, donc un minimum d'énergie potentielle. Si le système est dans cet état, que peut-on dire de l'indétermination sur la position? En déduire l'indétermination minimale sur la quantité de mouvement. Commenter.


Cas de l'oscillateur harmonique. On reprendre le cas de l'oscillateur harmonique. On rappelle que les états stationnaires sont quantifiés et que:

$$
E_n = \hbar \omega_0 (n + \frac{1}{2})
$$

1. En considérant le mouvement d'un oscillateur d'un point de vue classique, justifier que l'énergie mécanique du système puisse s'écrire sous la forme: $E = \frac{p_{x,m}^2}{4m} + \frac{k x_m^2}{4}$ où $p_m$ et $x_m$ sont respectivement les amplitudes d'oscillations des grandeurs respectives $p_x$ et$x$ .
1. En considérant le mouvement de l'oscillateur, proposer une relation simple entre $p_{x,m}$ et l'indétermination $\Delta p_x$ et de même entre $x_m$ et l'indétermination $\Delta x$
1. En utilisant les relations de Heisenberg, montrer que l'énergie mécanique possède un minorant qui est une fonction de $E_{\min}(\Delta x)$ .
1. En étudiant la fonction $E_{\min}(\Delta x)$, trouver la valeur minimale que peut prendre l'énergie du système. La comparer avec l'énergie minimale de l'oscillateur harmonique quantique.

````

````{attention}

Cette méthode de raisonnement est à savoir faire sur d'autres systèmes mais attention, il s'agit d'une étude en ordre de grandeur et le résultat trouvé à la fin ne pourrait être utilisé en tant que valeur minimale précise.
````

## Entrainement

### Energie minimale d'un atome

````{admonition} Exercice 
:class: attention


1. On considère le mouvement des électrons comme des orbites circulaires de rayons R autour du noyau. Utiliser les inégalités Heisenberg pour justifier l'existence d'une orbite de rayon minimal* Toujours sous l'hypothèse d'un mouvement circulaire, montrer que l'hypothèse de la quantification du moment cinétique $\overrightarrow{L} = n \hbar \overrightarrow{e_z} $ conduit à montrer la quantification de l'énergie de l'atome. On précisera l'expression des niveaux d'énergie.


````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Inégalités d'Heisenberg._
* _$\Longrightarrow$ Energie mécanique._
* _$\Longrightarrow$ Moment cinétique._

### Etude de l'oscillateur harmonique

````{admonition} Exercice 
:class: attention

On se propose d'aller plus loin dans l'étude de l'oscillateur harmonique.

1. On considère un pendule simple macroscopique utilisable en salle de TP. Estimer au moyen des formules du cours l'énergie de l'état fondamdental $n=1$. Déterminer l'amplitude des oscillations associées. Est-il raisonnable de le distinguer de l'état $E_{p,min} = 0$?* Estimer pour le même pendule l'écart entre deux niveau d'énergie et lui associer l'écart entre deux l'amplitude d'oscillation des deux états. Peut-on parler de continuum?


On s'intéresse maintenant à un oscillateur quelconque (possiblement microscopique) et à la fonction d'onde.

1. Observer l'animation ci-après et commenter brièvement la densité de probabilité en fonction du nombre quantique. On s'intéressera notamment à interprêter les variations aux nombres quantiques ainsi que l'annulation de la densité de probabilité en certains points .
1. On considère le modèle classique d'un oscillateur harmonique possédant une énergie mécanique $E$. Rappeler l'expression de $v(t)$ .
1. L'oscillateur est dans le noir est on prend aléatoirement une photo (avec flash) du montage pour situer le mobile. Expliquer, grâce à $v(t)$ si la probabilité de présence de l'oscillateur sur la photo serra plus plus grande au centre ou sur les côtés .
1. On s'intéresse maintenant à l'oscillateur quantique. Comparer la probabilité de présence pour $n=1$ avec le cas classique .
1. Faire la même comparaison pour un grand nombre quantique. Commenter.


```{figure} ./images/ohq_stationnaire.gif
:name: fig_315
:align: center

```

````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Energie mécanique._
* _$\Longrightarrow$ Oscillateur harmonique classique._