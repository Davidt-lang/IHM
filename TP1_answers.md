# TP1 — Réponses
Réalisé par : David RADOM  

---

## 1) Définition d'un besoin utilisateur — exemple et justification
**Définition**  
Un *besoin utilisateur* est une exigence ou une attente explicite ou implicite qu'une personne  cherche à satisfaire en utilisant un produit ou une interface. Il se formule souvent en termes d'objectifs à atteindre  et non en termes de solution technique.

**Exemple appliqué à l'interface que je conçois (maquette Figma)**  
- **Besoin :** L'utilisateur veut accéder rapidement au contenu principal sans être distrait.  
- **Justification dans l'interface :** J'applique un layout épuré, un en-tête réduit et un CTA (appel à l'action) visible en haut de page pour satisfaire ce besoin. Le contraste et l'ordre visuel priorisent le contenu principal.

---

## 2) Processus du Design Centré Utilisateur (UCD) — à quelle étape suis‑je ?
**Processus UCD (synthèse)**  
1. **Compréhension / Recherche utilisateur** 
2. **Définition des besoins & spécifications**  
3. **Idéation**   
4. **Prototype**   
5. **Test utilisateur** 
6. **Itération / Implémentation**

lien pour regarder mon figma : https://www.figma.com/design/WxccHeO5P3RiLnQRyh5Yh2/exemple-projet?node-id=0-1&t=uM5jtmd7Rmdv1EUp-1

**Étape actuelle **  
Je me place **à l'étape 4 — Prototype , en train de réaliser des maquettes sur Figma et préparer des tests utilisateurs .  
- Si vous **n'avez pas réalisé** les étapes 1–3, **réalisez-les maintenant** et ajoutez-les au dépôt git : `research/` (notes d'interviews, personas), `specs/` (user stories), `sketches/` (photos ou PDFs des croquis).  
- Fichiers à ajouter : `research/persona_*.md`, `flows/user_flow_homepage.png`, `sketches/*.pdf`.

---

## 3) Ajout d'observateurs dans le projet Figma — quel principe UCD appliqué ?
**Action** : Ajouter des observateurs signifie inviter des parties prenantes  avec droit de commentaire ou d'observation dans le fichier Figma.  
**Principe fondamental UCD appliqué** : **Évaluation avec utilisateurs / testabilité** — cela permet de collecter des retours réels et d'itérer en se basant sur l'usage .  
**Comment faire dans Figma** : `Share` → `Invite` → rôle `Can view` ou `Can comment` pour observateurs. Créer une page `Observations` où chaque observateur note ses commentaires structurés (Tâche, Observations, Gravité).

---

## 4) Calques  — définition et bonnes pratiques
**Définition**  
Un **calque**  est un objet positionné dans la pile visuelle d'une maquette : formes, images, textes, groupes, frames. Les calques contrôlent l'empilement  et la structure du document.

**Bonnes pratiques**  
- **Nommage clair et cohérent** : ex. `btn/primary/desktop`, `header/logo`, `card/product`.  
- **Utiliser des groupes/frames logiques** : regrouper par composant (card, header, footer).  
- **Hiérarchie** : Garder la structure Frames → Layout → Components.  
- **Verrouiller et masquer** les calques non‑pertinents pour éviter de les déplacer accidentellement.  
- **Utiliser des sections/pages** pour séparer flows .  
- **Ne pas multiplier des calques identiques** : utiliser des composants réutilisables.  
- **Respecter un système de dossiers  pour éviter l'encombrement**.

## 5) Composantré  — définition
**Définition**  
Un **composant** est un élément UI encapsulé et réutilisable  qui peut être instancié plusieurs fois. Les modifications du composant maître se répercutent sur toutes les instances, améliorant la cohérence et la maintenabilité.

**Bonnes pratiques composants**  
- Nommer : `Component / Button / Primary`  
- Gérer les **variants** 
- Documenter les props/contraintes dans la bibliothèque .

---


