# WashOnline – Prototype de démarrage d’une machine

Ce projet correspond à une **implémentation partielle de l'application WashOnline**, développée dans le cadre d'un projet de conception d'interface.

L’objectif de ce prototype est de développer le **circuit complet de démarrage d’une machine déjà réservée**, conformément aux décisions ergonomiques définies dans les livrables précédents.

Ce prototype se concentre sur la synchronisation entre l’application mobile et la machine physique afin d’éviter les incohérences d’état identifiées dans l’analyse UX.

---

# Fonctionnalité développée

La partie développée correspond au **parcours utilisateur de démarrage d’une machine déjà réservée**.

Le flux implémenté est le suivant :
Machine réservée
      ↓
Préparation (Timer)
      ↓
Machine lancée
      ↓
Suivi du cycle


Ce circuit permet de simuler le comportement réel d'une laverie connectée.

---

# Écrans implémentés

## 1. Page Laverie

Cette page représente la **vue principale de la laverie**.

Elle affiche l'ensemble des machines sous forme de badges indiquant leur état.

Chaque badge contient :

- une icône de machine à laver
- le numéro de la machine
- son statut

Trois états sont représentés :

- **Disponible**
- **En préparation**
- **Occupée**

Dans le cadre du prototype, l'utilisateur sélectionne une **machine déjà réservée** pour lancer le processus de démarrage.

---

## 2. Page Préparation

Cette page correspond à l'état intermédiaire **"Machine en préparation"** introduit dans la conception UX.

Cet état représente la phase durant laquelle :

- la machine est réservée
- l'utilisateur se rend physiquement à la machine
- le cycle n'est pas encore lancé

### Timer

Un **temporisateur** est lancé automatiquement pour représenter le temps laissé à l'utilisateur pour démarrer la machine.

### Redémarrage du timer

Si la machine n'est pas lancée dans le délai prévu, l'utilisateur peut :

- prolonger le temps de préparation
- redémarrer le timer

Cette fonctionnalité permet de gérer les cas où l'utilisateur a besoin de plus de temps pour charger son linge.

---

## 3. Page Suivi de cycle

Une fois la machine réellement démarrée, l'application passe à la page **Suivi de cycle**.

Cette page permet de suivre l'état du lavage.

Les informations affichées incluent :

- la machine utilisée
- le temps écoulé
- le statut du cycle

Cet écran confirme que la machine est désormais **en cours d'utilisation**.

---


