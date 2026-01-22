# Projet SQL — Gestion d’un Festival de Musique (SQLite)

## Contexte & Objectif
Ce projet a pour objectif de **concevoir, implémenter et exploiter une base de données relationnelle**
permettant la **gestion complète d’un festival de musique**, depuis la programmation des concerts
jusqu’à la participation du public.

Il couvre l’ensemble du cycle de conception d’une base de données :
**modélisation, implémentation SQL et requêtage avancé**.

---

## Démarche de conception
1. **Analyse du besoin métier**
   - Gestion des organisateurs, artistes, scènes, concerts, participants et billets
2. **Modélisation conceptuelle**
   - MCD / UML des entités et relations
3. **Transformation logique**
   - Passage du MCD vers un **MLD relationnel**
4. **Implémentation physique**
   - Création des tables SQLite avec :
     - clés primaires et étrangères
     - contraintes d’intégrité (CHECK, UNIQUE)
     - règles de cohérence référentielle
5. **Exploitation de la base**
   - Requêtes SQL simples et avancées
   - Vues, sous-requêtes, CTE et fonctions analytiques

---

## Modèle de données
### Entités principales
- **Organisateur**
- **Artiste**
- **Scène**
- **Concert**
- **Participant**
- **Billet**

Relations clés :
- Un organisateur gère plusieurs artistes et scènes
- Un artiste peut donner plusieurs concerts
- Un concert se déroule sur une scène
- Un participant peut acheter plusieurs billets
- Un billet est lié à un concert et à un participant

---

## Données & Volume
- Base SQLite peuplée avec **données réalistes**
- Environ **180 lignes** au total
- Forte volumétrie sur :
  - Participants
  - Billets
- Faible volumétrie volontaire sur :
  - Scènes  
 Permet de tester efficacement les **jointures, agrégats et analyses**

---

## Requêtes réalisées
- Sélections simples et filtrées
- Jointures (`INNER`, `LEFT`)
- Agrégations (`COUNT`, `SUM`)
- `GROUP BY` / `HAVING`
- Sous-requêtes
- **Vues SQL**
- **CTE (WITH)** et fonctions de fenêtrage (`RANK()`)

Exemples d’analyses :
- Nombre de concerts par scène
- Artistes programmés au moins 3 fois
- Recettes par jour de concert
- Classement des artistes par nombre de concerts
- Dépenses des participants (y compris ceux sans billet)

---

## Technologies
- **SQLite**
- **SQL standard**
- **Python** (`sqlite3`, `pandas`) pour l’exécution et la visualisation des résultats

---

## Compétences mises en œuvre
- Modélisation de données relationnelles
- Conception MCD / MLD
- Intégrité référentielle
- SQL avancé (vues, CTE, fonctions analytiques)
- Exploitation et analyse de données

---

*Ce projet illustre une approche complète et rigoureuse de la conception et de l’exploitation d’une base de données relationnelle dans un contexte métier réaliste.*
