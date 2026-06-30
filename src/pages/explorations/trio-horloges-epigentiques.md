---
layout: ../../layouts/GeneralLayout.astro
backHref: /exploration-menu/
backLabel: Retour
---

![img_titre](/images/trio_horloges_epigenetiques/page_titre.png)

*Un trio d'improvisation où l'ADN des individus B1-158 et C1-008 dialoguent aux synthétiseurs monophoniques, tandis que l'ADN de l'individu A1-002 les accompagne aux percussions électroniques.*

▶ [Voir la vidéo](https://drive.proton.me/urls/3RPZ1HDF1G#pKNTLvA45Sdf) | [Ecouter l'audio](https://drive.proton.me/urls/AWHZGMNNXR#pZKoaR1TEGSa)

---
**Sommaire**
- [Introduction](#introduction)
- [Origine des données](#origine-des-données)
- [Accordage du Thereminscule](#accordage-du-thereminscule)
- [Mixage audio](#mixage-audio)
- [A la fin, ça donne quoi ?](#a-la-fin-ça-donne-quoi-)
- [Un grand merci](#un-grand-merci)


---

## Introduction

Dans cette exploration, chaque piste est entièrement jouée au [*Thereminuscule*](/articles/thereminuscule-principe-conception-perspective-juin2026/), un programme informatique capable de transformer n'importe quel flux de donnée en musique.
Les données ici proviennent d'expériences scientifiques menées par une équipe de chercheur·euses de l'Ifremer, du CNRS et de l'entreprise réunionaise COOOL, à la frontière entre génétique et écologie.

Les données ainsi receuillies sont stockée dans des fichiers [CSV](https://fr.wikipedia.org/wiki/Comma-separated_values) qu'il est ensuite possible de lire au travers du *Thereminuscule* pour produire une piste [MIDI](https://fr.wikipedia.org/wiki/Musical_Instrument_Digital_Interface) contenant les notes à jouer. 
Au sein d'un logiciel de musique assitée par ordinateur (MAO), les pistes MIDI sont associées des instruments virtuels, aussi appelés [VSTi](https://fr.wikipedia.org/wiki/Virtual_Studio_Technology), puis mixées afin de produire le résultat final.

Les instruments seront joués en parcourant les sequences ADN de trois thons albacores.
Les niveaux de methylation de chaques sites génomiques dirigent les mélodies.

## Origine des données

Dans leur article *“Searching for shared epigenetic clocks: evaluating ultra-conserved markers in a de novo genome assembly of the albacore tuna”*, publié en 2026 dans la revue *GeroScience*, cette équipe dévoile une solution innovante pour déterminer l’âge des thons à partir de l’analyse de leur ADN depuis un petit échantillon prélevé sur la nageoire [1].
Les auteurs expliquent qu’il est possible d’estimer l’âge d’un individu grâce à son *horloge épigénétique*. Le principe consiste à parcourir, ou séquencer, certaines régions du génome de l’individu afin d’y rechercher des marqueurs associés au vieillissement : les groupes méthyle.

<img 
  src="/images/trio_horloges_epigenetiques/graphical_abstract_paper.png" 
  alt="graphical abstract paper" 
  style="width: 400px; max-width: 100%; height: auto;  display: block; margin: 2rem auto;"
/>

> [1] Chevrier, T., Bonhommeau, S., Thompson, M. et al. Searching for shared epigenetic clocks: evaluating ultra-conserved markers in a de novo genome assembly of the albacore tuna. GeroScience (2026). https://doi.org/10.1007/s11357-026-02192-0

Le jeu de données associé aux résultats présentés dans cette publication a été rendu public, on peut le télécharger librement sur [leur GitHub ici](https://github.com/ThomasCOOOL/Albacore_epigenetic_clock
) !

Dans cette exploration, on garde seulement les mesures de méthylation de l'ADN de trois thons albacores, aussi connus sous leurs noms de scène par : *fish-a1-002*, *fish-b1-158* et *fish-c1-008*.

Une première étape de traitement est necessaire pour uniformiser ces données afin de les rendre "compatible" avec le Thereminuscule. Pour pouvoir être téléchargée et rejouée ensuite simplement, elles sont mises à disposition dans une librairie de signaux dédiée.

⚡ *Rendez-vous sur la page [Thereminuscule Signal Library](https://wildflux-experience.github.io/thereminuscule-signal-library/) pour plus de signaux !*

Les images ci-dessous sont un aperçu des signaux "bruts", tels que présentés dans le jeu de données initial, avant qu'ils ne soient transformées en mélodies.

![plot_](/images/trio_horloges_epigenetiques/raw_plot_fish_a1.png)

**fish-a1-002** :  7637 points | [voir dans la librairie](https://wildflux-experience.github.io/thereminuscule-signal-library/signals/biology/albacore-epigenetic-clock/)


![plot_](/images/trio_horloges_epigenetiques/raw_plot_fish_b1.png)

**fish-b1-158** :  7637 points | [voir dans la librairie](https://wildflux-experience.github.io/thereminuscule-signal-library/signals/biology/albacore-epigenetic-clock/)


![plot_](/images/trio_horloges_epigenetiques/raw_plot_fish_c1.png)

**fish-c1-008** :  7637 points | [voir dans la librairie](https://wildflux-experience.github.io/thereminuscule-signal-library/signals/biology/albacore-epigenetic-clock/)


## Accordage du Thereminscule

Le Théréminuscule est configuré pour jouer en Si bémol Phrygien (Bb2, phrygian).
Le tempo de base est de 120 bpm et les notes sont jouées à la croche (1/8). 

![](/images/trio_horloges_epigenetiques/gamme_sibemol_phrygien_piano.png)

> Gamme de Si bémol Phrygien (7 notes) : Si♭ | Do♭ | Ré♭ | Mi♭ | Fa | Sol♭ | La♭

Chaque piste est enregistrée séparement.
Les notes s'enchainent en parcourant chaque site génomique dans l'ordre, au tempo de base (120 bpm, croche).
La hauteur de la note est définie par les niveaux de méthylation qui évoluent entre 0 et 1.
Chaque signal comprend à l'origine 7637 sites à parcourir, seuls les 2400 premiers sont jouées dans cette exploration.


![cubase_miditrack_fish_c1](/images/trio_horloges_epigenetiques/cubase_miditrack_fish_c1.png)

> Partition MIDI jouée par l'ADN de l'individu fish-c1-008.

## Mixage audio

Le mixage audio est réalisé avec Cubase Pro 12 (malheureusement pas open-source).
Les pistes sont synchronisée entre elles de sorte qu'à chaque instant les notes jouées correspondent au même site du génome de nos 3 individus.
Le morceaux final dure environ 3:50 minutes.

![cubase_timeline](/images/trio_horloges_epigenetiques/cubase_timeline.png)

Dans ce mix, chaque piste est dupliquée pour y appliquer 2-3 sons différents en paralèlle.
En plus des signaux, un drone en Si bémol (+ quinte) joue une nappe de fond.
Pour rendre le résultat plus musical et introduire de la variation dans l'intensité, le mix final applique des variations de volume sur chaque piste pour leur permettre d'entrer petit à petit ou liberer de l'espace sur certaines parties.

On utilise le synthetisuer virtuel [Odin 2](https://thewavewarden.com/pages/odin-2) pour creer le son à partir des pistes MIDI. Odin 2 est gratuit, open-source et d'une super qualité audio pour ce genre d'expérimentation !

![odin2_track_fish_a1_drum_machine](/images/trio_horloges_epigenetiques/odin2_track_fish_a1_drum_machine.png)
> Exemple : Réglage du synthétiseur Odin 2 pour produire le son de la "drum machine" jouée par l'ADN de l'individu fish-a1-002

![odin2_track_fish_c1_synth_psyche](/images/trio_horloges_epigenetiques/odin2_track_fish_c1_synth_psyche.png)
> Exemple : Réglage du synthétiseur Odin 2 pour produire le son d'un des synthétisuers monophoniques jouées par l'ADN de l'individu fish-c1-008

## A la fin, ça donne quoi ?

Et bien, ça donne une production sonore assez expérimentale, pas necessairement recommandée comme musique d'ambiance pour un barbecue dominical.

Cela dit, profiter de cette écoute pour présenter les musicien·nes derrière l'oeuvre semble crée une connexion innatendue entre une équipe de chercheur·euses sur l'Ile de La Réunion, les profondeurs de l'ADN et notre perception de la frontière où s'arrete le *son* et commence la *musique*.

![cubase_main_audio_track](/images/trio_horloges_epigenetiques/cubase_main_audio_track.png)
*⚡ Clique [ici](https://drive.proton.me/urls/AWHZGMNNXR#pZKoaR1TEGSa) pour écouter ou télécharger l'audio au format MP3.*

Ici, le morceaux est joué à partir des données de 3 individus, mais  8 individus au total sont disponibles directement dans la librairie [albacore-epigenetic-clock](https://wildflux-experience.github.io/thereminuscule-signal-library/signals/biology/albacore-epigenetic-clock/).
Dont, l'ADN de deux larves, aussi connus sous les noms de : larvae-18BG & larvae-23BGD.

🎙️ "Stay tuned!"

## Un grand merci

A Thomas et Sylvain, auteurs de l'étude à l'origine de ces données, pour être entré dans le délire.
