# TP1 — Réponses
Réalisé par : David RADOM  

---

## 1) Définition d'un besoin utilisateur — exemple et justification
**Définition**  
Un *besoin utilisateur* est une exigence ou une attente explicite ou implicite qu'une personne (utilisateur) cherche à satisfaire en utilisant un produit ou une interface. Il se formule souvent en termes d'objectifs à atteindre (ex : "je veux trouver un produit rapidement") et non en termes de solution technique.

**Exemple appliqué à l'interface que je conçois (maquette Figma)**  
- **Besoin :** L'utilisateur veut accéder rapidement au contenu principal sans être distrait.  
- **Justification dans l'interface :** J'applique un layout épuré, un en-tête réduit et un CTA (appel à l'action) visible en haut de page pour satisfaire ce besoin. Le contraste et l'ordre visuel priorisent le contenu principal.

> Indiquez dans votre dépôt Git les fichiers qui prouvent la prise en compte du besoin : `research/personas.md`, `user_stories.md`, captures Figma (frames) nommées `Homepage_priority` et un fichier README expliquant le mapping besoin → élément UI.

---

## 2) Processus du Design Centré Utilisateur (UCD) — à quelle étape suis‑je ?
**Processus UCD (synthèse)**  
1. **Compréhension / Recherche utilisateur** (contextual inquiry, interviews, personas)  
2. **Définition des besoins & spécifications** (user stories, jobs-to-be-done)  
3. **Idéation** (sketches, flows)  
4. **Prototype** (low‑fi → hi‑fi dans Figma)  
5. **Test utilisateur** (usability testing, observation)  
6. **Itération / Implémentation**

**Étape actuelle (réponse fournie)**  
Je me place **à l'étape 4 — Prototype (maquettage)**, en train de réaliser des maquettes sur Figma et préparer des tests utilisateurs (étape 5).  
- Si vous **n'avez pas réalisé** les étapes 1–3, **réalisez-les maintenant** et ajoutez-les au dépôt git : `research/` (notes d'interviews, personas), `specs/` (user stories), `sketches/` (photos ou PDFs des croquis).  
- Fichiers à ajouter : `research/persona_*.md`, `flows/user_flow_homepage.png`, `sketches/*.pdf`.

---

## 3) Ajout d'observateurs dans le projet Figma — quel principe UCD appliqué ?
**Action** : Ajouter des observateurs signifie inviter des parties prenantes (collègues, formateur, utilisateurs tests) avec droit de commentaire ou d'observation dans le fichier Figma.  
**Principe fondamental UCD appliqué** : **Évaluation avec utilisateurs / testabilité** — cela permet de collecter des retours réels et d'itérer en se basant sur l'usage (principe d'itération et d'évidence utilisateur).  
**Comment faire dans Figma** : `Share` → `Invite` → rôle `Can view` ou `Can comment` pour observateurs. Créer une page `Observations` où chaque observateur note ses commentaires structurés (Tâche, Observations, Gravité).

---

## 4) Calques (layers) — définition et bonnes pratiques
**Définition**  
Un **calque** (layer) est un objet positionné dans la pile visuelle d'une maquette : formes, images, textes, groupes, frames. Les calques contrôlent l'empilement (z-order) et la structure du document.

**Bonnes pratiques**  
- **Nommage clair et cohérent** : ex. `btn/primary/desktop`, `header/logo`, `card/product`.  
- **Utiliser des groupes/frames logiques** : regrouper par composant (card, header, footer).  
- **Hiérarchie** : Garder la structure Frames → Layout → Components.  
- **Verrouiller et masquer** les calques non‑pertinents pour éviter de les déplacer accidentellement.  
- **Utiliser des sections/pages** pour séparer flows (ex : `Page - Wireframes`, `Page - Prototype HiFi`).  
- **Ne pas multiplier des calques identiques** : utiliser des composants réutilisables (voir section composants).  
- **Respecter un système de dossiers (pages) pour éviter l'encombrement**.

> Si je constate des calques mal nommés ou non groupés dans vos fichiers, la consigne indique une pénalité de -3 points par non‑conformité. Vérifiez le fichier Figma et renommez.

---

## 5) Composant (réutilisable) — définition
**Définition**  
Un **composant** est un élément UI encapsulé et réutilisable (bouton, champ de formulaire, card) qui peut être instancié plusieurs fois. Les modifications du composant maître se répercutent sur toutes les instances, améliorant la cohérence et la maintenabilité.

**Bonnes pratiques composants**  
- Nommer : `Component / Button / Primary`  
- Gérer les **variants** (états : default, hover, pressed, disabled)  
- Documenter les props/contraintes dans la bibliothèque (autolayout rules, resizing).

---

## 6) Boutons (design system) — primaire / secondaire / tertiaire et variantes d'états
**Spécification (exemple)**

- **Bouton primaire**  
  - Usage : action principale (ex : "Soumettre", "Acheter")  
  - Taille : 44–48 px hauteur recommandée  
  - Texte : 16 px, weight 600  
  - États (variants) : `default`, `hover`, `pressed`, `disabled`, `loading`  
  - Feedback attendu : transition d'opacité et effet d'élévation (shadow) + cursor `pointer`.

- **Bouton secondaire**  
  - Usage : action moins prioritaire (ex : "Annuler")  
  - Style : outline ou background faible  
  - États : mêmes variants que primaire.

- **Bouton tertiaire**  
  - Usage : actions contextuelles (lien textuel)  
  - Style : texte uniquement, underline optionnel  
  - États : `default`, `hover`, `disabled`.

**Implémentation Figma (variantes)**  
- Créer un composant `Button` avec **Variants** pour `type` (primary/secondary/tertiary) et `state` (default/hover/pressed/disabled/loading).  
- Définir tokens pour couleurs, espaces et typographie dans `Styles` (Text/Color/Effect).

---

## 7) Wayfinding — définition et mise en œuvre
**Définition**  
Le *wayfinding* désigne l'ensemble des éléments qui aident l'utilisateur à se repérer et à se diriger dans une interface (navigation, repères visuels, feedback d'état, titres, fil d'Ariane).

**Implémentation dans l'interface**  
- **Structure claire de navigation** : barre nav principale, sous‑menus logique, breadcrumb (fil d'Ariane).  
- **Indicateurs d'état** : item actif sur la navigation, titre de page visible, microcopy d'aide.  
- **Points de repère visuels** : icônes constantes, couleurs cohérentes pour sections.  
- **Accessibilité** : contrasts WCAG, focus visible (outline).  
- Ajouter `breadcrumbs` sur les pages profondes et un `side-menu` avec item actif mis en évidence.

---

## 8) Affordance d'un bouton (Don Norman) — comment s'assurer de l'affordance ?
**Conseils concrets**  
- **Rendre l'élément cliquable évident** : forme avec contours et ombre légère, taille suffisante.  
- **Utiliser un libellé explicite** (verbe d'action) — ex : "Ajouter au panier".  
- **Feedback instantané** : hover/pushed states, micro-animations, changement de curseur.  
- **Proximité** : placer le bouton à proximité de l'objet/texte lié pour montrer l'action attendue.  
- **Affordance perçue et réelle** : garantir que le comportement attendu (clic = action) se réalise (pas d'incertitude sur l'action).  
- **Tests** : réaliser premiers tests utilisateurs pour vérifier que les utilisateurs reconnaissent le bouton comme actionnable.

---

## 9) Checklist à ajouter au dépôt Git
- `research/personas.md` — personas et synthèse interviews  
- `research/user_stories.md` — user stories prioritaires  
- `sketches/` — croquis scannés ou photos  
- `figma_links.md` — liens vers les fichiers Figma et instructions d'accès (inclure observateurs)  
- `design_system/buttons.md` — spécifications des boutons et tokens  
- `README.md` — description du projet, étapes UCD réalisées et à réaliser

---

### Remarques finales
- J'ai suivi les consignes du TP et intégré les notions User Centered Design et Figma.  
- Relisez l'orthographe avant dépôt (la consigne indique -3 points si >5 fautes).  
- Si vous voulez, je peux générer automatiquement un exemple de `personas.md` et `user_stories.md` préremplis et un modèle de fichier `figma_links.md` à ajouter au dépôt.

---
