---
layout: ../../layouts/GeneralLayout.astro
backHref: /exploration-menu/
backLabel: Retour
---

![img_titre](/images/toccata_sous_marine_eaux_reunionaises/page_titre.png)

*Qu'est-ce que ça donne si, les plongées d'une tortue verte jouent de la harpe électrique, la nage d'une raie fouet joue du syntéthiseur monophonique, tandis que la ligne de basse est confiée à la température mésurée par une bouée qui flotte en surface ?*

▶ [Voir la vidéo](https://drive.proton.me/urls/44DWY86BPG#6ZK5iCAJsdzx) | [Ecouter l'audio](https://drive.proton.me/urls/H9C4RFR9YM#M8rjSqhouhwa)

---

**Sommaire**
- [Introduction](#introduction)
- [Origine des données](#origine-des-données)
- [Accordage du Thereminscule](#accordage-du-thereminscule)
- [Mixage audio](#mixage-audio)
- [A la fin, ça donne quoi ?](#a-la-fin-ça-donne-quoi-)

---

## Introduction

Dans cette exploration, chaque piste est entièrement jouée au [*Thereminuscule*](/articles/thereminuscule-principe-conception-perspective-juin2026/), un programme informatique capable de transformer n'importe quel flux de donnée en musique.
Les données ici proviennent d'expériences scientifiques menées par une équipe chercheurs de l'Ifremer et du CNRS qui visent à étudier le comportement de la megafaune marine autour de l'Ile de la Réunion. 

Les données ainsi receuillies sont stockée dans des fichiers [CSV](https://fr.wikipedia.org/wiki/Comma-separated_values) qu'il est ensuite possible de lire au travers du *Thereminuscule* pour produire une piste [MIDI](https://fr.wikipedia.org/wiki/Musical_Instrument_Digital_Interface) contenant les notes à jouer. 
Au sein d'un logiciel de musique assitée par ordinateur (MAO), les pistes MIDI sont associées des instruments virtuels, aussi appelés [VSTi](https://fr.wikipedia.org/wiki/Virtual_Studio_Technology), puis mixées afin de produire le résultat final.

Les instruments seront confiés à la temperature collectée en surface par une bouée intrumentée ainsi qu'aux profondeurs collectées par des marques attachées à une tortue marine verte et une raie fouet.


## Origine des données

Ces données ont toutes la particularité d'avoir été collectées à la Réunion, avec des dispositifs open-source specialement développés par cette équipe de chercheurs. Elles font partie d'un plus vaste jeu de donnée, public lui aussi [1]

<img 
  src="/images/toccata_sous_marine_eaux_reunionaises/turtle_tag_pics.png" 
  alt="turtle_tag_pics" 
  style="width: 500px; max-width: 100%; height: auto;  display: block; margin: 2rem auto;"
/>


> [1] Mohan Julien, Gogendeau Pierre, Boyer Alexandre, Goharzadeh Andrea, Etienne Titouan, de Knyff Laurent, A’bear Luke, Sanchez Cheryl, Quillard Mireille, Paute François-Elie, Bernard Serge, Bonhommeau Sylvain (2024). A bio-logging dataset on the diving behaviours of juvenile sea turtles from the southwestern Indian Ocean. SEANOE. https://doi.org/10.17882/102544

Dans cette exploration, on garde les données des balises nommées *dcp-urelease-018*, *turtle-iot-046* et *ray-urelease-63b*. 

Une première étape de traitement est necessaire pour uniformiser ces données afin de les rendre "compatible" avec le Thereminuscule. Pour pouvoir être téléchargée et rejouée ensuite simplement, elles sont mises à disposition dans une librairie de signaux dédiée.

⚡ *Rendez-vous sur la page [Thereminuscule Signal Library](https://wildflux-experience.github.io/thereminuscule-signal-library/) pour plus de signaux !*

Les images ci-dessous sont un aperçu des signaux "bruts", représentant les grandeurs physiques effectivement mesurées, avant qu'elles ne soient transformées en mélodies.

![plot_dcp](/images/toccata_sous_marine_eaux_reunionaises/rawplot_dcp_temp.png)

**dcp-urelease-018** :  ~18 jours | 3004 points | [voir dans la librairie](https://wildflux-experience.github.io/thereminuscule-signal-library/signals/wildlife/dcp-urelease-018/)

![plot_turtle](/images/toccata_sous_marine_eaux_reunionaises/rawplot_turtle_dive.png)

**turtle-iot-046** :  ~6 jours | 8097 points | [voir dans la librairie](https://wildflux-experience.github.io/thereminuscule-signal-library/signals/wildlife/turtle-iot-046/)

![plot_ray](/images/toccata_sous_marine_eaux_reunionaises/rawplot_ray_dive.png)

**ray-urelease-63b** :  ~15 jours | 992 points | [voir dans la librairie](https://wildflux-experience.github.io/thereminuscule-signal-library/signals/wildlife/ray-urelease-63b/)



## Accordage du Thereminscule

Le Théréminuscule est configuré pour jouer en Mi Ionien (E2, ionian).
Le tempo de base est de 120 bpm et les notes sont jouées à la croche (1/8). 
La matrice de modulation est activée.


![](/images/toccata_sous_marine_eaux_reunionaises/gamme_E_ionian_piano.png)

> Gamme de Mi Ionien (7 notes) : Mi | Fa# | Sol# | La | Si | Do# | Ré# 

Chaque piste est enregistrée séparement.
Pour chaque piste, une des grandeurs physiques mesurées (*variable*) sert au choix de la note, une seconde sert à la modulation, sorte de controle d'effet pour les synthétizeurs utilisés ensuite.

**Piste : dcp-urelease-018**

La temperature mésurée en surface par cette bouée instrumentée dirige la hauteur des notes. Les déplacements moyens de la bouée autour de sa position centrale servent à moduler son expression.

![cubase_project_piste_dcp](/images/toccata_sous_marine_eaux_reunionaises/cubase_project_piste_dcp.png)

- Hauteur de note : *atmospheric-temperature*
- Effet de la modulation : *mean-displacement -> midi.modulation*

Les notes s'enchainent en respectant la temporalité propre des mesures mais le signal est accéléré x1000.
Le signal original contient environ 18 jours d'enregistrement mais seul les 5 premiers jours sont joués dans cette mélodie.

**Piste : turtle-iot-046**

Les profondeurs mesurées par la balise pendant que la tortue nage, plonge ou refait surface, dirigent la hauteur des notes. Les temperatures moyennes de l'eau enregistrées durant servent à moduler son expression.

![cubase_project_piste_turtle](/images/toccata_sous_marine_eaux_reunionaises/cubase_project_piste_turtle.png)

- Hauteur de note : *dive-depth*
- Effet de la modulation : *water-temperature -> midi.modulation*


Les notes s'enchainent en respectant la temporalité propre des mesures mais le signal est accéléré x120.
Le signal original contient environ 6 jours d'enregistrement mais seul les 15 premieres heures sont jouées dans cette mélodie.

**Piste : ray-urelease-63b**

Les profondeurs mesurées par la balise pendant que la raie nage dirigent la hauteur des notes. Les temperatures moyennes de l'eau enregistrées durant servent à moduler son expression.

![cubase_project_piste_ray](/images/toccata_sous_marine_eaux_reunionaises/cubase_project_piste_ray.png)

- Hauteur de note : *dive-depth*
- Effet de la modulation : *dive-temperature -> midi.modulation*


Les notes s'enchainent linéairement au tempo de base (120bpm, croche) en jouant les mesures les unes après les autres.
Le signal original contient environ 15 jours d'enregistrement où chaque mesure est espacée de ~10 minutes.
Le signal est répété ~1.3 fois dans cette mélodie.

## Mixage audio

Le mixage audio est réalisé avec Cubase Pro 12 (malheureusement pas open-source).
Les pistes ne sont pas synchronisée car les signaux n'ont pas vraiement ici de lien temporel entre eux, chaque piste est démarrée arbitrairement pour creer un progression dans le début du morceaux.
Dans ce mix, chaque piste est doublée pour y appliquer 2 sons différents.
Le morceaux final dure un peu plus de 6 minutes.

![cubase_project_timeline](/images/toccata_sous_marine_eaux_reunionaises/cubase_project_timeline.png)

On utilise les synthetisuers virtuels [Surge XT](https://surge-synthesizer.github.io/) et [Odin 2](https://thewavewarden.com/pages/odin-2) pour creer le son a partir des pistes MIDI, tout deux open-source et d'une super qualité audio.

![cubase_project_ray_odin2](/images/toccata_sous_marine_eaux_reunionaises/cubase_project_ray_odin2.png)
> Exemple : Réglage du synthétiseur Odin 2 pour la première piste qui joue les profils de plongée de la raie fouet.

![cubase_project_ray_surgext](/images/toccata_sous_marine_eaux_reunionaises/cubase_project_ray_surgext.png)
> Exemple : Réglage du synthétiseur Surge XT pour la seconde piste qui joue les profils de plongée de la raie fouet.

La piste de percussion electronique en arrière plan n'est liée à aucune mesure réelle, elle a été composéé après coup, pour amener un peu de rythme et de dynamique au mix final.

## A la fin, ça donne quoi ?

*⚡ Clique [ici](https://drive.proton.me/urls/H9C4RFR9YM#M8rjSqhouhwa) pour écouter ou télécharger l'audio au format MP3.*

Et bien, ça donne une production sonore assez expérimentale. Il ne faut pas s'attendre à mettre l'ambiance avec aux prochaines convivialitées.
Mais, présenter les musicien·nes derrière l'oeuvre peut très certainements mener à des échanges curieux et informatifs.

> Comment on obtient le profils de plongée d'une tortue marine ou d'une raie fouet évoluant aux larges des côtes Réunionnaises ?
> 
> Pourquoi cette information est-utile pour la préservation de ces espèces, de leurs habitats et de la bio-diversitée autour ?
>
> Comment sont mises en oeuvre les recherches et les expererimentations qui produisent ces connaissances ?
>
> Où se rendre pour en apprendre plus et aller discuter avec les personnes qui travaillent, s'impliquent et militent autour de ces thématiques, à la croisée des sciences du vivant, de l'informatique et de l'information publique .

A l'écoute, il semble que l'intrication de ces trois mélodies tend à creer une ensemble musical, parfois produisant des impulsions presque "pop", avec des motis facilement reconnaissables pour nos oreilles et notre cerveaux. Parfois un peu moins, les motifs sont plus instables, moins harmonieux, perçus comme à la juste limite d'une suite de note completement aléatoire, de fait moins agréable à écouter. Il se créer souvent une certaine tension, mais typiquement résolue ensuite par la réapparition de motifs plus harmonieux.

Un autre effet intérressant et que par certains moments, dans les données brutes on retrouve de "grands" sauts de valeur, suivis de périodes de variations plus réduites. Ceci à pour effet de produire des mélodies qui "oscillent" ou "évoluent" autour de 2-3 notes pendant un certain temps.
Cependant, le fait de jouer des motifs de 2-3 notes (petites variations), à partir d'une position arbitraire dans la gamme (dernier grand saut), revient à changer subtilement le mode sur lequel on joue (au sens de la théorie musicale).
Créant ainsi aux hasard des coincidences, des variations de "couleur" des mélodies générées. Les modes étant chacun teinté d'une émotion représentative, il se crée naturellement des passages plus mélacoliques, joyeux ou intenses.
