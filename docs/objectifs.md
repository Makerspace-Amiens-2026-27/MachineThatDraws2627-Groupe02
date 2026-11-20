---
layout: default
nav_order: 2
title: Objectifs du projet
---


---
layout: default
title: Objectifs du projet
nav_order: 2
permalink: /objectifs.html
---

# Objectifs du projet

## Contexte

Dans le cadre de notre formation d'ingénieur à UniLaSalle Amiens, nous réalisons un projet pédagogique au Makerspace intitulé **Machine That Draws**.

L'objectif est de concevoir et fabriquer une machine capable de reproduire automatiquement des dessins sur une feuille de papier, à partir d'instructions programmées ou d'un dessin transmis depuis un ordinateur.

Ce projet nous permet de mettre en pratique différentes compétences en mécanique, en électronique et en programmation. Nous devons notamment réfléchir à la conception de la structure, au choix des composants, à la commande des moteurs et à la précision des déplacements.

Après avoir étudié plusieurs architectures de machines à dessiner, nous avons choisi de nous orienter vers une **architecture cartésienne XY**.

Le fonctionnement repose sur le déplacement d'un stylo selon deux axes perpendiculaires :
- L'axe X permet le déplacement horizontal.
- L'axe Y permet le déplacement vertical.
- Un mécanisme supplémentaire permet de lever et d'abaisser le stylo.

Nous souhaitons utiliser autant que possible le matériel disponible au Makerspace, notamment les rails ou glissières et les servomoteurs présents dans l'atelier.

À ce stade, nous avons commencé l'inventaire du matériel. La conception mécanique et les essais de fonctionnement restent à réaliser.

---

## Problème et public cible

### Problématique

Comment concevoir une machine automatisée, simple à utiliser et suffisamment précise pour reproduire différents dessins sur une feuille A4, tout en utilisant au maximum les ressources disponibles au Makerspace ?

La principale difficulté consiste à transformer des instructions informatiques en déplacements mécaniques précis.

Pour obtenir un dessin correct, la machine doit coordonner les mouvements sur les deux axes, maintenir la feuille immobile et contrôler le contact du stylo avec le papier.

Nous devons également trouver un compromis entre la précision, la simplicité de fabrication, la fiabilité et les possibilités d'amélioration du prototype.

### Public cible

Notre machine est principalement destinée à un usage pédagogique et à des démonstrations au Makerspace.

Elle pourra notamment être utilisée par :
- Les étudiants souhaitant découvrir la programmation et la commande de systèmes automatisés.
- Les enseignants et encadrants pour illustrer le fonctionnement d'un système mécatronique.
- Les utilisateurs du Makerspace intéressés par la fabrication numérique et le dessin automatisé.

Notre objectif n'est pas de fabriquer une machine industrielle, mais de réaliser un prototype fonctionnel, compréhensible et évolutif.

### Utilisation envisagée

Nous souhaitons que la machine puisse fonctionner de deux manières :

**Mode 1 : dessins préprogrammés**

L'utilisateur lance un programme contenant les instructions nécessaires pour dessiner une forme géométrique simple, comme un carré, un triangle ou un cercle.

**Mode 2 : dessin transmis depuis un ordinateur**

L'utilisateur transmet un dessin à la machine depuis un ordinateur.

Le dessin devra être converti en instructions de déplacement compatibles avec le système de commande.

Cette deuxième fonctionnalité sera développée progressivement, après validation des premiers mouvements et des dessins simples.

À terme, nous souhaitons également pouvoir reproduire des dessins plus élaborés, des logos et des écritures.

---

## Cahier des charges

### 1. Présentation du besoin

Nous souhaitons concevoir une machine à dessiner automatisée utilisant une architecture cartésienne XY.

La machine devra être capable de déplacer un stylo sur une feuille A4 et de reproduire un dessin en suivant des coordonnées définies.

Elle devra également pouvoir lever et abaisser automatiquement le stylo afin de réaliser plusieurs traits indépendants.

Le prototype devra être suffisamment fiable pour répéter plusieurs fois un même dessin, tout en restant accessible à des étudiants dans le cadre d'un projet pédagogique.

### 2. Fonction principale

**FP1 : Reproduire automatiquement un dessin sur une feuille A4.**

Pour assurer cette fonction, la machine devra :
- Déplacer le stylo horizontalement sur l'axe X.
- Déplacer le stylo verticalement sur l'axe Y.
- Coordonner les déplacements des deux axes.
- Lever et abaisser automatiquement le stylo.
- Interpréter des instructions de dessin.
- Maintenir la feuille en position pendant le tracé.

### 3. Fonctions principales et contraintes

| Référence | Fonction | Description | Critère de validation |
|---|---|---|---|
| FP1 | Reproduire un dessin | Réaliser automatiquement un dessin sur papier. | Dessin identifiable et conforme à la forme demandée. |
| FP2 | Exécuter un dessin programmé | Tracer des formes définies dans le programme. | Réalisation d'un carré, d'un triangle et d'un cercle. |
| FP3 | Recevoir un dessin depuis un ordinateur | Convertir un dessin en instructions de déplacement. | Reproduction d'un dessin simple transmis depuis un ordinateur. |
| FT1 | Déplacer le stylo sur X | Assurer le mouvement horizontal du stylo. | Déplacement contrôlé sur toute la course utile. |
| FT2 | Déplacer le stylo sur Y | Assurer le mouvement vertical du stylo. | Déplacement contrôlé sur toute la course utile. |
| FT3 | Lever et abaisser le stylo | Permettre de réaliser plusieurs traits séparés. | Deux traits distincts sans liaison indésirable. |
| FT4 | Commander les mouvements | Utiliser un système électronique programmable. | Exécution d'une séquence de déplacements. |
| FT5 | Maintenir la feuille | Éviter le déplacement du papier. | Feuille immobile pendant un dessin complet. |
| FT6 | Guider les déplacements | Assurer des mouvements réguliers. | Absence de blocage sur les deux axes. |
| FC1 | Respecter le format A4 | Permettre le dessin sur une feuille A4. | Feuille de 210 × 297 mm correctement positionnée. |
| FC2 | Assurer la stabilité | Limiter les vibrations et les déformations. | Aucun déplacement visible de la structure pendant le tracé. |
| FC3 | Privilégier le matériel disponible | Utiliser les composants présents au Makerspace. | Inventaire et justification des composants retenus. |
| FC4 | Permettre la maintenance | Faciliter l'accès aux composants. | Possibilité de remplacer un stylo ou un composant sans démonter toute la machine. |
| FC5 | Assurer la sécurité | Éviter les mouvements incontrôlés. | Possibilité d'arrêter les déplacements et absence de blocage dangereux. |

### 4. Contraintes dimensionnelles

Le format de papier choisi est le **A4**, de dimensions 210 × 297 mm.

Nous souhaitons exploiter presque toute la surface de la feuille, en conservant de petites marges pour éviter que le stylo ne dépasse du papier.

À titre de première hypothèse, nous proposons une marge de 10 mm sur chaque côté.

Cela correspondrait à une surface de dessin utile de :

- Largeur : 210 - 20 = **190 mm**.
- Longueur : 297 - 20 = **277 mm**.

La surface utile envisagée serait donc de **190 × 277 mm**.

Ces dimensions restent provisoires. Elles devront être adaptées aux courses réellement disponibles sur les rails ou glissières.

### 5. Objectifs de performance

| Critère | Objectif envisagé | Méthode de vérification | Statut |
|---|---|---|---|
| Format du papier | A4 : 210 × 297 mm | Vérification des dimensions du support. | Confirmé |
| Surface utile | Environ 190 × 277 mm | Mesure des courses X et Y. | Proposition |
| Précision dimensionnelle | Écart maximal visé de ±2 mm sur un carré de 100 mm | Mesure des côtés du carré tracé. | Objectif provisoire |
| Répétabilité | Écart maximal visé de 2 mm entre des tracés répétés | Superposition ou mesure de trois dessins identiques. | Objectif provisoire |
| Déplacement X | Mouvement régulier sur toute la course | Test de déplacement horizontal. | À tester |
| Déplacement Y | Mouvement régulier sur toute la course | Test de déplacement vertical. | À tester |
| Levage du stylo | Contact et retrait automatiques | Réalisation de deux traits séparés. | À tester |
| Maintien du papier | Aucun glissement visible | Observation pendant un dessin complet. | À tester |
| Dessins programmés | Au moins trois formes simples | Carré, triangle et cercle. | À développer |
| Dessins importés | Au moins un dessin simple depuis un ordinateur | Test d'importation et de reproduction. | À développer |
| Fiabilité | Trois dessins successifs sans intervention | Répétition d'une séquence de dessin. | Objectif provisoire |

Ces valeurs correspondent aux performances que nous souhaitons atteindre. Elles ne constituent pas des résultats expérimentaux.

Elles pourront être ajustées après les premiers essais et en fonction du matériel disponible.

### 6. Contraintes matérielles et électroniques

Pour réaliser notre machine, nous envisageons les éléments suivants :

| Élément | Rôle | Situation actuelle |
|---|---|---|
| Rails ou glissières | Guider les déplacements X et Y. | Disponibles au Makerspace, dimensions à vérifier. |
| Moteurs des axes X et Y | Assurer les déplacements du stylo. | Type définitif à déterminer. |
| Servomoteurs | Motorisation à étudier, notamment pour le levage du stylo. | Disponibles, références à identifier. |
| Carte Arduino | Commander les mouvements de la machine. | Solution envisagée. |
| Système de transmission | Transmettre le mouvement des moteurs aux chariots. | À choisir. |
| Porte-stylo | Maintenir le stylo et permettre son déplacement. | À concevoir. |
| Mécanisme de levage | Lever et abaisser le stylo automatiquement. | À concevoir. |
| Structure | Supporter les différents éléments mécaniques. | À dimensionner et fabriquer. |
| Support de feuille | Maintenir le papier pendant le dessin. | À concevoir. |
| Alimentation | Fournir l'énergie aux composants électroniques. | À définir selon les moteurs. |

**Point de vigilance :**

Les servomoteurs disponibles ne sont pas nécessairement adaptés aux déplacements linéaires des axes X et Y.

Nous devrons vérifier leurs caractéristiques avant de valider leur utilisation.

Si nécessaire, nous envisagerons des moteurs pas à pas pour les déplacements XY et un servomoteur pour le levage du stylo.

### 7. Priorités de développement

Pour organiser notre travail, nous avons défini trois niveaux de priorité.

**Priorité 1 : prototype mécanique fonctionnel**

- Réaliser la structure.
- Installer les guidages X et Y.
- Mettre en place les moteurs.
- Obtenir des déplacements contrôlés.
- Installer le porte-stylo.

**Priorité 2 : réalisation des premiers dessins**

- Programmer les déplacements.
- Tracer des lignes horizontales et verticales.
- Réaliser des formes géométriques simples.
- Ajouter le levage automatique du stylo.
- Vérifier la précision et la répétabilité.

**Priorité 3 : fonctionnalités avancées**

- Transmettre un dessin depuis un ordinateur.
- Convertir le dessin en instructions.
- Reproduire des logos, des écritures ou des dessins plus complexes.
- Améliorer la précision et la fiabilité.

Cette organisation nous permet de commencer par une machine simple et fonctionnelle avant de développer les fonctionnalités supplémentaires.

### 8. Validation finale du projet

Nous considérerons notre projet comme abouti lorsque la machine pourra :

1. Accueillir et maintenir une feuille A4.
2. Déplacer automatiquement le stylo sur les deux axes.
3. Lever et abaisser le stylo sans intervention manuelle.
4. Dessiner correctement plusieurs formes géométriques simples.
5. Reproduire plusieurs fois un même dessin.
6. Recevoir et reproduire au moins un dessin simple depuis un ordinateur.

Les cinq premiers points permettront de valider le fonctionnement mécanique et électronique de base.

Le dernier point permettra de valider la fonctionnalité d'importation de dessins, qui sera développée dans un second temps.

---

## État actuel du projet

À ce jour, nous avons :

- Étudié différentes architectures de machines à dessiner.
- Choisi l'architecture cartésienne XY.
- Défini le format A4 comme support de dessin.
- Identifié les principales fonctions attendues.
- Commencé l'inventaire du matériel disponible au Makerspace.

Il nous reste à terminer l'inventaire, vérifier les caractéristiques des composants, réaliser les premiers plans mécaniques et commencer les essais de motorisation.

Le cahier des charges pourra évoluer en fonction des contraintes découvertes pendant la conception et la fabrication.
