# Infographie — Arosa Lenzerheide / Analyse Doughnut (v2.0)

**ENV-101 · EPFL · Printemps 2026** — Projet de durabilité systémique.

Ce bundle contient une infographie HTML/CSS/JS autonome (un seul fichier, aucune dépendance externe en dehors de Google Fonts) appliquant le cadre de l'économie du Doughnut de Kate Raworth à l'étude de cas du domaine skiable d'Arosa Lenzerheide (Grisons, CH).

## Fichier principal

- `project/Infographie.html` — le document complet.

## Structure du document

1. **01 / DOUGHNUT** — diagramme interactif des 21 dimensions (9 plafond + 12 plancher), avec filtres (toutes / liens structurels / plafond / plancher) et panneau de détail navigable.
2. **02 / SYSTÈME** — stocks, flux, boucles de rétroaction (R climat, B offre/demande). Synchronisation avec le doughnut : cliquer sur un stock ouvre la dimension correspondante.
3. **03 / TRAJECTOIRE** — projection 2010→2050 (courbe lissée illustrative CH2018 RCP 4.5), KPI animés, commentaire dynamique, marqueurs jalons politiques (2030 Paris, 2040 CH2050), zone de basculement.
4. **04 / MÉTHODE** — périmètre, sources primaires vs. estimées, limites, bibliographie formalisée (10 références, DOI cliquables).

## Interactions

- **Clic** ou **Tab + Entrée** sur un segment du doughnut ou un stock du système.
- **Flèches ← →** : navigation entre sections (hors mode input).
- **F** : bascule mode présentation (plein écran).
- **Esc** : quitter présentation.
- **Boutons toolbar** : Imprimer / PDF, Télécharger CSV, Mode présentation.

## Accessibilité

- Skip-link en haut de page.
- `tabindex`, `role` et `aria-label` sur tous les éléments interactifs.
- `aria-live="polite"` sur les panneaux dynamiques (détail doughnut, commentaire timeline).
- Support `prefers-reduced-motion` (désactive animations des flux et tweens KPI).
- Focus visible sur tous les contrôles (amber).
- Contraste respecté (palette navy / ink sur paper).

## Impression & export

- `@media print` : styles optimisés pour A4, dépliage des panneaux de détail, couleurs forcées, masquage des contrôles.
- Export CSV : projections 2010-2050 avec en-tête méta (date, source, cadre).

## Changelog

- **v2.0 (2026-04-21)** — Refonte majeure : rigueur académique (section Méthode, bibliographie formalisée, correction des chiffres vérifiés), labels du doughnut sur arcs, synchronisation doughnut ↔ systèmes, échelle Y timeline corrigée (60–160), marqueurs 2030/2040, zone de basculement, commentaire dynamique, tween KPI, toolbar (print / CSV / présentation), accessibilité clavier complète, support mobile.
- **v1.0** — Version initiale (prototype Claude Design).
