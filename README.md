# Simulation numérique d’un système non strictement hyperbolique  
## Dynamique des nuages de poussière et ondes delta

---

##  Description
Ce projet étudie la dynamique de deux **nuages de poussière en collision** modélisés par un **système non strictement hyperbolique sans pression**.  
L’objectif est de comprendre et de simuler la formation d’ondes **delta** (structures singulières qui apparaissent lors des collisions et interactions non classiques).  

Le travail combine :
- **Analyse théorique** (solution exacte via l’article de LeVeque),  
- **Implémentation numérique** (schéma de Godunov adapté),  
- **Comparaison numérique vs théorique** sur différents régimes de propagation des ondes.

---

## Objectifs
- Étudier le système :  
  \[
  \begin{cases}
  ∂_t ρ + ∂_x(ρu) = 0 \\
  ∂_t (ρu) + ∂_x(ρu^2) = 0
  \end{cases}
  \]

  où \(ρ(x,t)\) est la densité et \(u(x,t)\) la vitesse.

- Implémenter le **schéma de Godunov** pour résoudre numériquement ce système.  
- Construire la **solution exacte** en s’appuyant sur les résultats théoriques de LeVeque.  
- Simuler la collision de deux nuages de poussière et suivre l’évolution des **ondes delta**.  
- Comparer solutions numériques et analytiques pour valider la méthode.  

---

## Méthodologie
1. **Schéma de Godunov**  
   - Formulation conservative avec flux numérique dépendant du signe de la vitesse.  
   - Traitement spécifique pour éviter la division par zéro (ρ₀ fixé).  

2. **Construction de la solution exacte**  
   - Collision de deux nuages initialisés à \(t=-1\).  
   - Évolution en trois phases :  
     - **Onde delta initiale** (choc de deux nuages).  
     - **Raréfaction-choc delta** (un nuage entièrement accrété).  
     - **Double raréfaction delta** (deux nuages accrétés).  

3. **Validation numérique**  
   - Simulation sur un domaine spatial \(x ∈ [-3,6]\).  
   - Comparaison des pics de densité avec les prédictions analytiques.  
   - Vérification de la conservation de la masse malgré l’étalement numérique.  

---

##  Résultats
- **Phase 1 (t ≈ 1.21)** :  
  Le nuage de gauche est entièrement accrété dans l’onde delta.  

- **Phase 2 (t ≈ 4.25)** :  
  Le nuage de droite est accrété → apparition d’une **rarefaction-choc delta**.  

- **Phase 3 (t > 4.25)** :  
  Formation d’une **double rarefaction delta**.  

🔹 Le schéma numérique capture correctement la position et la dynamique des ondes delta, mais avec un effet de **diffusion numérique** :  
- Pics de densité réalistes mais étalés.  
- Conservation de la masse validée.  

---

## Compétences mises en œuvre
- **Analyse avancée de PDE hyperboliques non strictement hyperboliques**.  
- Mise en place du **schéma de Godunov** adapté aux systèmes singuliers.  
- Implémentation numérique en **Python / MATLAB**.  
- Utilisation d’outils analytiques (fonctions de Heaviside, Dirac, invariants).  
- Validation des résultats numériques par comparaison avec la théorie.  

---

## Organisation
- `rapport/Projet_système_non_strictement_hyperbolique.pdf` → Rapport complet avec théorie, schéma et résultats.  
- `code/` → Implémentation du schéma de Godunov (Python/MATLAB).  
- `figures/` → Graphiques illustrant l’évolution des ondes delta.  
- `README.md` → Présentation synthétique et professionnelle du projet.  

---

##  Perspectives
- Étendre le modèle à des systèmes **multi-dimensionnels**.  
- Utiliser des **schémas numériques plus précis** (HLL, HLLC, solveurs de Riemann exacts).  
- Étudier l’influence d’une **pression faible** pour modéliser des gaz rares.  
- Application possible en **astrophysique** (dynamique des disques de poussière, formation planétaire).  

---


## Conclusion:
- Ce projet illustre une **maîtrise solide en simulation numérique et analyse mathématique**.  
- Démonstration de compétences en **méthodes numériques pour PDE**, modélisation et calcul scientifique.  
- Capacité à traiter des systèmes difficiles (non strictement hyperboliques, solutions singulières).  
- Compétences transférables vers :  
  - **Simulation physique** (fluide, mécanique des milieux granulaires, astrophysique),  
  - **Ingénierie numérique**,  
  - **Data science appliquée**.
 

  ## Auteur
**Bréhima Samaké**  
Projet académique – Encadré par le Prof. Tran Quang-Huy  

---

