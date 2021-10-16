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
# Dualité onde-corpuscule

## Ondes et corpuscules en mécanique classique

````{admonition} Exercice 
:class: attention

On se propose ici de faire rapidement un bilan sur les concepts d'ondes et de corpuscule en mécanique classique.

* Rappeler brièvement les propriétés physiques qu'on associe à un corpuscule.
* Rappeler brièvement les propriétés physiques qu'on associe à une onde.
* Classer les objets physiques ci-après suivant qu'ils soient des corpuscules ou des ondes __dans la théorie classique.__ 
    * Electrons
    * Atomes
    * Lumière
````
````{admonition} Fondamental : A retenir... 
:class: attention

On retiendra qu'en mécanique classique, les objets physiques sont soit des corpuscules, soit des ondes.

Attention, cela n'empêche pas l'interaction entre les deux types d'objets. Ainsi, la théorie classique prévoit l'interaction entre la matière et la lumière
````

## Expériences importantes

### Effet photoélectrique

Observer la vidéo suivante  appelée "Effet photoélectrique - Présentation" dans la partie mécanique quantique.

__Effet photoélectrique - Présentation.__  
```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/videos_physique/blob/main/photoelectrique_presentation-converted.mp4?raw=true", width=640)
```

````{admonition} Exercice 
:class: attention

1. Pourquoi les électrons ne peut aller sans éclairage de l'armature négative vers l'armature positive ? Traduire cela en traçant __l'allure__  de l'énergie potentielle des électrons d'une armature à l'autre .
1. Que faut-il simplement pour que les électrons franchissent la barrière de potentiel mise en évidence à la question précédente ? Comment est-ce réalisé ici ? Expliquer ainsi ce qu'est l'effet photoélectrique .
1. Du point de vue classique (ondulatoire) de la lumière, peut-on expliquer l'effet photoélectrique présenté dans la vidéo de présentation.
    1. Regarder maintenant les deux vidéos suivantes appelées "Effet photoélectrique - Effet de seuil" et "Effet photoélectrique - Effet de seuil et intensité". Expliquer pourquoi de telles observations sont contradictoires avec la vision classique de la lumière .
    1. Dans la vision quantique, la lumière est __aussi__  composée corpusculaire, c'est à dire composée de quantas de lumière appelés photons dont l'énergie dépend de la fréquence $\nu$ du rayonnement : $E_{photon} = h \nu$ (relation de Planck-Einstein) où h est la constante dite de Planck ($h = 6,63 \times 10^{-34} \rm{J.s}$. Interprêter l'effet photoélectrique grâce à la notion de photon .
    1. Expliquer pourquoi cette vision corpusculaire permet d'expliquer l'existence d'un effet de seuil.
1. On donne le potentiel d'extraction du Sodium, c'est-à-dire l'énergie minimale nécessaire pour libérer des électrons de l'armature. $W_S = 2.5 eV$. Comparer la fréquence seuil des photons associées avec celle observée dans la vidéo "Effet photoélectrique - Influence du matériau". A l'inverse, estimer le potentiel d'extraction du Zinc et du Calcium.
````

__Effet photoélectrique - Effet de seuil.__  
```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/videos_physique/blob/main/photoelectrique_seuil-converted.mp4?raw=true", width=640)
```

__Effet photoélectrique - Effet de seuil et intensité.__  
```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/videos_physique/blob/main/photoelectrique_intensite-converted.mp4?raw=true", width=640)
```

__Effet photoélectrique - Influence du matériau.__  
```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/videos_physique/blob/main/photoelectrique_materiau-converted.mp4?raw=true", width=640)
```


````{admonition} Fondamental : Le photon
:class: attention

On retiendra que le modèle corpusculaire de la lumière décrit la décrit comme un ensemble de "quantas de lumière" appelée photons. Ces derniers ont les caractéristiques suivantes :


* Leur énergie est (relation de Planck-Einstein) : $E = h \nu$ où h est la constante de Planck et $\nu$ la fréquence du rayonnement .
* Leur charge électrique est nulle* Leur masse est nulle* Leur vitesse est toujours la vitesse de la lumière : ce sont des particules relativistes .
* Leur quantité de mouvement est $\overrightarrow{p} = \frac{h}{\lambda}\overrightarrow{u} = \hbar \overrightarrow{k}$ où $\hbar = \frac{h}{2 \pi}$, $\overrightarrow{u}$ est un vecteur unitaire dans la direction et le sens de propagation de la lumière et $\overrightarrow{k} = \frac{2\pi}{\lambda} \overrightarrow{u}$.
````

### Diffraction et interférences de la matière

````{admonition} Exercice 
:class: attention

En 1927 Thomson de son côté et Davisson et Gerner du leur réalisent un expérience de diffraction d'un faisceau d'électrons par une fente fine ou un cristal. Depuis, des expériences de diffraction pour des atomes et molécules ont été réalisées.

Depuis 1989, on a aussi réalisé des expériences d'interférences de matière (électron 1989, Hélium 1991, fullerènes 1999). Il s'agit de la " classique " expérience des fentes d'Young. Notons néanmoins que sa réalisation pratique pour de la matière est plus complexe que pour la lumière.

1. Si l'on considère que les électrons sont uniquement des corpuscules (vision classique), expliquez pourquoi on ne peut obtenir de figure d'interférences (Remarque: ces observations expliquent aussi pourquoi le modèle purement corpusculaire de la lumière n'est pas valable) .
1. Dans leur expérience, Davisson et Gerner bombardèrent du nickel (paramètre de maille $a = 0.215 nm$) avec des électrons. La formule de Bragg permet de relier l'angle de diffraction aux paramètres de l'expérience: $2a \sin \theta = \lambda$. Ils mesurèrent un angle de $50 ^{\circ}$. Estimer ainsi la longueur d'onde des électrons puis leur énergie .
1. En réalité, l'énergie des électrons était de 54eV. Expliquer les causes possibles de cet écart.
````

````{admonition} Fondamental : Dualité onde-corpuscule de la matière.
:class: attention

On retiendra que d'un point de vue quantique, on peut associer un caractère corpusculaire associé à une énergie E et une quantité de mouvement $\overrightarrow{p}$ ET un caractère ondulatoire associé à une longueur d'onde $\lambda$ (ou de vecteur d'onde ) et une fréquence $f$ (ou une pulsation $\omega$). Les deux aspects de la particule sont reliées par la relation de de Broglie:

\begin{equation}
\overrightarrow{p} = \hbar \overrightarrow{k} = \frac{h}{\lambda}\overrightarrow{u}
\end{equation}
où $\overrightarrow{u}$ est la direction de propagation de la lumière.
````

```{dropdown} Remarque : Longueur d'onde et masse

Dans le cas de particules matérielles, la quantité de mouvement s'écrit $\overrightarrow{p} = m \overrightarrow{v}$ donc plus la masse est grande, plus la longueur d'onde est faible. Comme on le verra avec les critères quantiques, cela rejoint l'idée que plus le système est gros, moins le traitement quantique est nécessaire.
```

## La dualité onde-corpuscule

### Interférences électrons à électrons.

````{admonition} Exercice 
:class: attention

Observer la vidéo suivante sur une expérience d'interférences électrons par électrons expliquer l'aspect dual de l'interprétation ondes-corpuscules de la matière.

````

```{code-cell} ipython3
---
tags: [remove-input]
---
from IPython.display import Video
Video("https://github.com/pcsi3physiquestan/videos_physique/blob/main/interference_electron.mp4?raw=true", width=640)
```

### Critères quantiques


Nous avons évoqué le parallèle entre la mécanique classique-quantique et l'optique géométrique-ondulatoire. Ce parallèle est d'autant plus important qu'il va nous permettre de situer si les effets quantiques doivent nécessairement être pris en compte ou non. Rappelons par exemple que la loi de Dulong-Petit (approche classique) est largement valable à température ambiante. Elle ne l'est plus à basse température. Cela signifie que l'approche quantique n'est pas nécessaire à température ambiante, elle le devient à basse température.


````{admonition} Fondamental : Crtière sur la longueur d'onde
:class: attention

Par analogie avec l'approximation de l'optique géométrique, on peut considérer que l'approche de la mécanique classique reste valable tant que les dimensions du corps considéré sont grandes devant la longueur d'onde de de Broglie associé au système.
````


L'inconvénient du critère précédent est qu'il demande de comparer deux caractéristiques du corps. On peut chercher à se ramener à une comparaison avec une constante fondamentale (à l'image de la comparaison avec la célérité de la lumière pour décider d'un traitement relativiste). Ici, la constante fondamentale adaptée est __la constante de Planck__  $h$. En effet le critère sur la longueur d'onde peut se réécrire: $a >> \lambda = \frac{h}{p}$ soit $ap >> h$.


````{admonition} Fondamental : Critère sur l'action
:class: attention

Le traitement classique reste valable tant que l'action caractéristique $S$ du système est grande devant la constante de Planck.
````

### Utilisation du critère quantique

````{admonition} Exercice 
:class: attention

1. En utilisant le critère sur la longueur d'onde, expliquer pourquoi un homme qui marche ne nécessite pas un traitement quantique .
1. En utilisant le critère sur l'action, justifier qu'une planète gravitant autour d'un Soleil ne nécessite pas un traitement quantique mais qu'un électron autour d'un noyau le nécessite.


````

## Travaux dirigés

### Ordres de grandeur

````{admonition} Exercice 
:class: attention

1. Estimer la quantité de photons reçus par seconde par une photo-cathode de surface $S = 1 \rm{cm^{2}}$ exposée au rayonnement d'un lampe au sodium ($\lambda = 589 \rm{nm}$) ponctuelle émettant avec une puissance $P=15\rm{W}$ à une distance $d=1\rm{m}$ .
1. Estimer la quantité de photons reçus par seconde par la pupille dilatée d'un humain regardant une étoile de rayon $R = 10^5 \rm{km}$ émettant principalement dans le rouge comme un corps noir et située à une distance de 20 années lumières. On sait que:
    * Pour un corps noir, la puissance rayonnée par unité de surface du corps noir __à sa surface__ est $P_S = \sigma T^4$ avec $\sigma = 5.7 \times 10^{-8} \rm{W.m^{-2}.K^{-4}}$ est la constante de Stefan.
    * La longueur d'onde correspondant au maximum d'émission est reliée à la température du corps noir par la loi de déplacement de Wien: $\lambda_{max} T = cste = 0.2898 \rm{K.cm}$
1. Commenter la difficulté d'obtenir une éclairement "un photon par un photon".
````

### Pression de radiation

````{admonition} Exercice 
:class: attention

Soit un faisceau monochromatique de puissance surfacique $P_S$ et de longueur d'onde $\lambda$ se réfléchissant sur un miroir parfait avec un angle $\theta$. Par un bilan de quantité de mouvement sur les photons, déterminer la pression (appelée pression de radiation) exercée par le faisceau lumineux sur le miroir. On supposera le milieu environnant assimilable au vide.

````


