---
layout: ../../layouts/GeneralLayout.astro
title: Le Thereminuscule et ses Nano-Modules
description: Principe, conception et perpectives - Juin 2026
backHref: /articles-menu/
backLabel: Retour
---

*... EN COURS D'ECRITURE ...*

--- 

**Sommaire**

- [Introduction](#introduction)
- [Jouer à l’intuition et sans fausses notes](#jouer-à-lintuition-et-sans-fausses-notes)
- [Le Thereminuscule](#le-thereminuscule)
  - [Qu’est-ce que c’est ?](#quest-ce-que-cest-)
  - [Comment ça fonctionne ?](#comment-ça-fonctionne-)
    - [Les Sources](#les-sources)
    - [Les Processeurs](#les-processeurs)
    - [Les Traducteurs](#les-traducteurs)
    - [Les Performeurs](#les-performeurs)
- [Les Nano-Modules](#les-nano-modules)
  - [Qu’est ce que c’est ?](#quest-ce-que-cest--1)
  - [Présentation des modules “originaux”](#présentation-des-modules-originaux)
  - [Des possibilités quasi-infinies](#des-possibilités-quasi-infinies)
    - [Fabriquer pour comprendre](#fabriquer-pour-comprendre)
    - [Jouer pour ressentir](#jouer-pour-ressentir)
    - [Contempler pour questionner](#contempler-pour-questionner)
- [Pour conclure](#pour-conclure)

---

## Introduction

Le Thereminuscule et ses Nano-Modules cherchent à rendre perceptibles des phénomènes physiques en transformant des signaux, mesures et interactions en expériences sonores sensibles et partageables (Figure 1).

![image_illu_thereminuscule](/images/illustration_principe_thereminscule_annote_200dpi.png)

> ***Figure 1**. Illustration du concept au cœur des dispositifs WildFlux.*

... A COMPLETER ...

## Jouer à l’intuition et sans fausses notes

L’improvisation musicale repose sur la capacité d’un musicien à inventer, dans l’instant, une suite de notes cohérentes porteuses d’une emotion spécifique, qui se base sur la trame rythmique et harmonique proposée par les autres interprètes. Connaissant à l’avance la partition, l’artiste peut alors libérer son imagination et puiser dans son vocabulaire musical pour créer une ligne mélodique, un solo, qui vient dialoguer avec trame musicale déjà en place.

![image_illu_impro](/images/thereminuscule_principe_conception_perspective_juin2026/illustration_solo_levier_creatif_annote_200dpi.png)

> ***Figure 2**. Illustration des différents leviers créatifs que le musicien considère lorsqu’il compose un solo.*

Selon un modèle simpliste, on peut identifier certains leviers créatifs que le musicien doit considérer et apprivoiser pour produire un solo qui à du sens (Figure 2, *voir note*):

- **La  fondamentale** : Ou autrement dit la note de référence, est la note atour de laquelle le musicien va construire sa lige mélodique. Celle-ci doit être en accord avec la trame harmonique du morceau sur lequel il improvise.
- **La couleur** : Ou autrement dit la gamme, est l’ensemble des notes “secondaires” qui complète la notes de référence. La musique occidentale est composée de 12 notes (ou tons). Choisir un sous-ensemble spécifique parmi ce 12 notes revient à choisir sa gamme. Chacune va être teintée d’une “couleur” ou “d’émotions” spécifiques en fonction des notes qui la composent. Ici aussi les gammes utilisées doivent être en accord, dans une certaine limite, avec la trame harmonique du morceau sur laquelle le musicien improvise.
- **Le rythme** : Il s’agit ici de la rapidité à laquelle les notes vont être jouées. D’une manière générale la rapidité à laquelle les notes sont produites doit être liée au tempo de la trame musicale. Cependant le musicien, tant qu’il joue sur des multiples du tempo initial (croche, noire, blanche, triolet, …), a la possibilité d’accélérer ou ralentir son débit de notes pour nuancer son expression.
- **L’intensité** : Simplement la “force” avec laquelle on veut produire les notes, comme on choisirait de jouer sèchement ou délicatement les touches d’un piano ou les cordes d’une guitare.
- **La dynamique** : Il s’agit ici de la plage de notes à parcourir (point de départ et étendue) et de la manière de les enchainer. Les notes se répètent indéfiniment allant du plus grave au plus aigue rebouclant à chaque fois sur ce qu’on appelle l’octave (même note mais un cran plus grave ou aigue). On peut par exemple, choisir de restreindre son expression à un ensemble de notes proches, pour créer des motifs stables et puissants, où à l’inverse choisir d’exploiter une large plage de notes, comme on se promènerait sur l’ensemble des touches d’un piano, produisant des lignes mélodiques plus ample et plus expressive.
- **La note finale** : Parmi les notes “élues”, définies sur l’instant par la fondamentale, la gamme et la dynamique, il s’agit enfin pour le musicien de choisir lesquelles jouer et dans quel ordre. On décide alors d’une direction et on parcourt ces notes, du grave à l’aigu. On a alors le choix de parcourir ces notes une à une, trois par trois, en montant, en descendant, lentement ou rapidement, ou bien sur selon des motifs plus complexes. Cette dynamique est centrale dans l’improvisation ou la composition musicale.

Chacune des composantes décrites ci-dessus occupe une place bien définie. Par exemple, dans la musique populaire, tandis que la fondamentale et la gamme sont largement contraintes par la trame musicale sur laquelle on improvise, le rythme, l’intensité et surtout la dynamique des notes, offrent un espace plus ouvert à l’expression personnelle du musicien sur le moment.

Dans le cadre de la pratique d’un instrument “classique” ou “traditionnel” comme la guitare, le violon, le piano, la flûte, etc., maîtriser ces différentes composantes créatives demande du temps et de la pratique. Si l’on imagine maintenant, pour une partition ou un enchaînement d’accords donnés, un instrument capable de s’accorder automatiquement sur la trame de fond, il ne reste alors qu’à interagir ces différents leviers créatifs. C’est la fonction principale du *Thereminuscule*. Au travers de ce programme, on s’affranchit ainsi des règles musicales formelles et des techniques propres à chaque instruments, il suffit de laisser parler son intuition pour diriger la mélodie selon sa propre sensibilité, ou plus généralement la “sensibilité” du système qui pilote le *Thereminuscule*.


*Note: Cette classification est une simplification pratique pour les besoins de l’explication. Elle repose plus sur la manière dont les concepts ont été intégrés au Thereminuscule, que sur une méthode ou théorie musicale réelle et approuvée.*

## Le Thereminuscule

### Qu’est-ce que c’est ?

Le *Thereminuscule*, ou plus précisément le `thereminuscule-engine`, est un programme informatique écrit en Python et à l’origine de ce projet. Il est conçu pour générer automatiquement des lignes mélodiques cohérentes et permet d’exploiter en temps réel n’importe quel flux de données entrant comme moyen d’interagir avec celles-ci, à la fois sur les notes mais aussi sur l’expressivité avec laquelle elles sont jouées.

[SCHEMA PRINCIPE] 

> ***Figure 3**. Fonctionnement illustré du `thereminuscule-engine`.*

Sa fonction principale, illustrée en Figure 3, est donc de convertir une suite de nombres “quelconques”, ou flux de donnée, en une suite de notes spécifique au format MIDI. En entrée du programme on retrouve les *Sources,* elles lisent des valeurs numériques depuis l’extérieur du programme et les transformes en signaux exploitables par les *Processeurs.*  Ces objets sont en quelque sorte la “machinerie interne” du programme, c’est ici que l’on va associer chaque nombre à une note précise, que l’on va choisir sa hauteur, son intensité, sa durée, etc …. En sortie du programme on retrouve les *Traducteurs,* ces objets-ci permettent d’exprimer la note choisie, et ses caractéristiques en un format exploitable par d’autres instrument ou logiciel de musique comme les VSTi. Au milieu, en guise de cheffe d’orchestre, on retrouve l’*Horloge* qui se charge de cadencer les autres parties pour que l’ensemble joue au bon tempo. Enfin, les *Performeurs* permettent de modifier en “live” les différents paramètres de réglage, ou “d’accordage”, du *Thereminuscule.*

### Comment ça fonctionne ?

Les sections suivantes présente les grandes lignes du fonctionnement du *Thereminuscule*. Il s’agit ici d’une première version jouable du programme (`*thereminuscule-engine-v1.0.0*`), les fonctionnalités discutées ci-dessous sont amenées à évoluer et s’enrichir au fil du projet et des contributions des participants.

#### Les Sources

Le *Thereminuscule* inclut 3 types de sources qui se distinguent selon l’origine de la donnée.

Soit, la donnée vient du programme lui-même. Il génère génère en interne des suites de nombre selon des séquences prédéfinies ou sur la base de signaux classiques tel que des sinusoïdes. Ces sources sont nommées `Sequencer` et `Generator`.

Soit, la donnée est lue depuis un fichier local qui contient les informations intéressantes. Le fichier pouvant contenir n’importe quel type d’information, ce type de source permet par exemple de générer des mélodies à partir de données scientifiques, tant que l’on peut les exprimer sous forme de tableaux de grandeurs numériques. Ces sources sont nommées `DataPlayer`.

Soit, la donnée est lue en “live” depuis une base de donnée en ligne ou un dispositif électronique externe comme les *Nano-Modules* ! Ces sources sont nommées `ControlStream`. Le fonctionnement des  *Nano-Modules* est décrit dans la section suivante.

Avant son traitement par les *Processeurs*, la “note brute” issue des sources, est d’abord exprimée sous forme de valeur numérique “8bits” pouvant aller de 0 à 255. Ici, 0 représente la plus petite valeur numérique que l’on s’attend à lire dans le flux de donnée entrant, 255 représente la plus grande attendue.

#### Les Processeurs

Les signaux issues des *Sources* (”note brutes”) passent par différentes étapes de traitement avant d’aboutir à l’élection d’une note finale spécifique. Les opération effectuées à chaque étape dépendent des paramètres de réglage du *Thereminuscule*, comme le choix de la note fondamentale, de la gamme, de la dynamique voulue, etc… A l’issue du traitement on obtient une note liée directement à la valeur numérique initialement lue par la source, mais surtout cohérente ave le reste des notes déjà produites et à produire.

L’exemple qui suit illustre la conversion d’une valeur numérique “8 bits” (de 0 à 255) en une note de musique par le *Processeur* nommé `Scaler`.  La valeur prise pour exemple est 168, qui se situe environ au 2/3 de la plage des valeurs possibles en sortie des sources. Le Thereminuscule est réglé pour jouer sur une gamme de *Do* majeur à partir du 2ème octave (ou *C2* en anglais et 36 en MIDI). La note finale élue correspondant à la valeur 168, est la note de *Si* du 4ème octave (ou *B4* en anglais et 71 en MIDI)

▶ Paramètres de réglage Thereminuscule utilisés par le `Scaler`:

| Paramètre | Variable dans le programme | Valeur exemple |
| --- | --- | --- |
| La fondamentale | `fonda` | C2 = 36 en MIDI |
| La gamme | `scale.nb_note` et `scale.interval` | Majeure → `nb_note` = 7 et `interval` = [2, 2, 1, 2, 2, 2, 1] |
| La hauteur | `pitch` | +1 |
| La dynamique | `scalespread` | +3 |

▶ Algorithme de conversion du `Scaler` :

```python
# ETAPE 1 : de la valeur brute à l'identificant de la note en fonction de la dynamique

8bit_value = 168
noterange = scale.nb_note * scalespread = 7 * 3 = 21
note_id = int ((8bit_value / 255) * noterange) = int((168 / 255) * 21) = 13

# ETAPE 2 : de l'identifiant à la note finale en fonction de la fondamentale et de la gamme

fonda_midi = 36 = "C2"
true_fonda = int(fonda_midi + pitch * 12) = int(36 + 12) = 48 = "C3"
loc_pitch = int(note_id / nb_note) = int(13 / 7) = 1
loc_ind = int(mod(note_id, nb_note)) = 6
loc_interval = int(sum(interval[:loc_ind])) = int(sum([2, 2, 1, 2, 2, 2]) = 11
note_midi = true_fonda + loc_pitch * 12 + loc_interval = 48 + 12 + 11 = 71 = "B4"
```

Il existe un deuxième *Processeur* qui agit en parallèle du `Scaler` présenté précédemment, il s’agit de la matrice de modulation ou `ModulationMatrix` . Cet objet-ci exploite également le signal issues des sources mais cette fois-ci non pas pour calculer la note finale à jouer, mais pour moduler en temps réel les paramètres de réglage du *Thereminuscule,* ouvrant ainsi la voie à plus de possibilités sonores et d’interactions avec les mélodies produites. En plus des 4 paramètres principaux décrits plus haut, la modulation permet aussi d’influer sur la vitesse à laquelle les notes sont jouées et leurs intensités.

N’importe qu’elle source peut être choisie pour le calcul de la note finale avec le `Scaler`. Et plusieurs sources en parallèle peuvent servir à moduler les différents paramètres simultanément au travers de la  `ModulationMatrix`.

#### Les Traducteurs

Texte

#### Les Performeurs

Texte

[SCREENSHOT UI DE L'ENGINE]

> ***Figure X**. Vue d’ensemble des paramètres de réglage du Thereminuscule qui peuvent être modifiés en live par les Performeurs. Dans cet exemple il s’agit d’une simple interface pour contrôler le Thereminuscule avec la souris ou un écran tactile depuis un ordinateur / tablette / téléphone.*

## Les Nano-Modules

### Qu’est ce que c’est ?

Les *Nano-Modules* sont des dispositifs électroniques simples et peu coûteux, capables de convertir des grandeurs physiques, au sens large, en flux de données numériques compatibles avec le Thereminuscule. Ils assurent la passerelle entre monde réel et monde virtuel. Les façons de mesurer l’effet d’une action, d’un mouvement ou d’un état, via une grandeur physique et un capteur adapté, sont nombreuses, ouvrant ainsi la voie à une grande variété de *Nano-Modules* à imaginer !

Dans cette approche, des plateformes comme Arduino ou Raspberry Pi jouent un rôle important. Leur popularité et la richesse de leurs écosystèmes open-source et “Do It Yourself” (DIY) ont largement contribué à rendre la conception de dispositifs électroniques et de programmes informatiques accessible au plus grand nombre. Simples à utiliser, peu coûteuses et soutenues par d’immenses communautés créatives (ex: https://www.instructables.com/), elles constituent aujourd’hui des supports pédagogiques et expérimentaux particulièrement adaptés aux publics plus jeunes ou non initiés (ex1, ex2, ex3). Dans le cadre du projet WildFlux, elles serviront autant de base pour des ateliers de fabrication d’instruments atypiques, où chacun pourra assembler son propre *Nano-Module* comme un jeu de construction, que de terrain d’expérimentation pour imaginer rapidement de nouvelles formes d’interaction sonore.

### Présentation des modules “originaux”

Description rapide du nano-ultrasonic made in WildFlux et du nano-fishnchip made in LIRMM

### Des possibilités quasi-infinies

Il existe une multitude de façons de mesurer une grandeur physique à l’aide d’un capteur électronique adapté : lumière, pression, mouvement, température, humidité, vibration, son, champ magnétique, distance, etc. À cela s’ajoute la liberté de concevoir la partie mécanique ou matérielle du *Nano-Module* elle-même. Un objet peut être pensé pour réagir à une action, un geste, une déformation, un état ou un phénomène extérieur, qu’il soit provoqué par l’apprenti musicien ou directement issu d’un phénomène naturel. Cette combinaison entre capteurs, formes physiques et modes d’interaction ouvre un champ presque infini de possibilités pour imaginer de nouveaux instruments. La diversités de grandeurs physiques et des modes d’interactions à l’oeuvre ouvre la porte sur la vulgarisation de faits scientifiques au travers d’experimentations pratiques.

La liste ci-dessous présente une palette de Nano-Modules possiblement réalisables, certains étant plutôt axés sur la facilité de conception, d’autre sur la jouabilité ou encore la curiosité de l’objet en lui-même.

#### Fabriquer pour comprendre

*Ces modules explorent des principes physiques simples, facilement observables et manipulables : la lumière, la conductivité, la résistance électrique, le contact, l’eau, le corps humain ou encore le magnétisme. Leur objectif n’est pas seulement de produire un signal numérique exploitable par le Thereminuscule, mais aussi de rendre perceptible le lien entre un phénomène concret et la mélodie produite. Ils sont bien adaptés aux ateliers de fabrication et à la médiation scientifique.*

- Boîte à lumière
- Dessin graphite
- Pince-crocodile orchestra
- Circuit humain
- Bassin à doigts
- Pendule magnétique

La **Boîte à lumière** propose de jouer avec l’ombre, la transparence et la couleur. En ouvrant une boîte, en faisant passer des papiers colorés ou en tournant une roue devant un capteur, les variations lumineuses deviennent des données musicales.

Le **Dessin graphite** repose sur un principe tout aussi accessible : un simple tracé au crayon papier ou à la peinture conductrice devient une piste résistive que l’on peut toucher, parcourir ou modifier.

Avec le **Pince-crocodile orchestra**, différents objets du quotidien, pâte salée, éponge humide, métal, fruit, papier aluminium, sont reliés au système afin d’explorer leur conductivité.

Le **Circuit humain** prolonge cette idée en faisant des participants eux-mêmes une partie du circuit: en se touchant ou en reliant plusieurs points conducteurs, ils produisent collectivement un flux de données.

Le **Bassin à doigts** introduit quant à lui l’eau comme interface sensible : la présence des doigts, le niveau du liquide ou sa conductivité influencent directement le signal.

Le **Pendule magnétique** ouvre une dimension plus contemplative. Un aimant suspendu oscille au-dessus de capteurs et rend audible une force invisible. Le mouvement, l’amortissement et la variation du champ magnétique deviennent une matière musicale lente et hypnotique.

#### Jouer pour ressentir

*Ces modules ont une intention plus instrumentale : ils doivent permettre un geste suffisamment précis, réactif et intuitif pour orienter la trajectoire musicale du Thereminuscule en temps réel.*

- Baguette et maracas magiques
- Ruban mélodique et Joystick
- Manivelle et Volant d’expression
- Flûte numérique

Les **Baguettes et maracas magiques** transforment les mouvements de la main en données musicales. L’inclinaison, les secousses ou l’énergie du geste deviennent une manière de diriger la mélodie, entre instrument de percussion, objet rituel et baguette de chef d’orchestre.

Le **Ruban mélodique et Joystick** propose une approche plus précise : un ruban résistif ou un potentiomètre linéaire permet de parcourir une plage de valeurs de manière continue, tandis qu’un joystick ajoute une modulation complémentaire avec l’autre main.

La **Manivelle et le Volant d’expression** s’appuient sur un geste circulaire simple et physique. Tourner une manivelle ou un petit volant permet de produire un flux continu ou cyclique, donnant à l’utilisateur une sensation directe de mouvement, de vitesse et de progression dans l’espace musical.

La **Flûte numérique**, enfin, mobilise le souffle comme geste expressif. En soufflant plus ou moins fort dans un tube, l’utilisateur influence la hauteur, l’intensité ou la vitesse de la ligne mélodique, tout en retrouvant l’intuition corporelle des instruments à vent.

#### Contempler pour questionner

*Ces modules sont davantage portés par leur forme, leur imaginaire ou leur dimension plastique : soleil, nuages, matière frottée, eau qui sèche, branche qui plie, foule, jardin, méduse, écume, magnétisme, constellation. Leur rôle n’est pas seulement de produire un contrôle musical, mais aussi de faire surgir une question, une image ou une situation.*

- Mini centrale solaire
- Frottoir sonore
- Pluie et évaporation musicale
- Branche musicale
- Foule en délire
- Jardin sonore miniature
- Méduse suspendue
- Écume de données
- Constellation magnétique

La **Mini centrale solaire** transforme la lumière en source musicale. Un petit panneau solaire, orienté à la main ou exposé à des “soleils” artificiels, réagit aux ombres et aux nuages translucides que l’on place devant lui.

Le **Frottoir sonore** explore quant à lui la vibration des matières : bois, métal, carton, tissu ou papier produisent chacun une réponse différente lorsqu’ils sont frottés sur une surface équipée d’un capteur.

Avec **Pluie et évaporation musicale**, l’eau devient une matière temporelle. Les gouttes, l’humidité puis le séchage progressif d’une surface produisent un flux lent et changeant.

La **Branche musicale** traduit la flexion d’une tige ou d’une structure souple, entre geste humain et évocation du vivant.

La **Foule en délire** déplace encore le rôle du public : les applaudissements, voix ou bruits collectifs ne sont plus seulement une réaction, mais deviennent une force qui module la musique.

Le **Jardin sonore miniature** propose une écoute symbolique du végétal et de son environnement, à travers l’humidité, la lumière, la température ou l’arrosage de plusieurs petits pots.

La **Méduse suspendue** donne forme aux mouvements de l’air grâce à une sculpture légère, sensible aux courants ou aux ventilateurs.

**Écume de données** explore les bulles, vagues et remous d’un petit récipient d’eau comme un paysage sonore miniature.

Enfin, la **Constellation magnétique** met en scène une force invisible : des aimants déplacés sur une carte étoilée composent des configurations spécifiques mesurables, qui influencent le *Thereminuscule*.

## Pour conclure

... A COMPLETER ...