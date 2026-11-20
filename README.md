# Analyse de l'évolution de l'inflation en France, 2015-2025 (Excel)

Projet d'économie appliquée (Master 1, Université de La Réunion) – analyse descriptive réalisée uniquement avec Microsoft Excel : formules simples, sans macro ni VBA.

**Problématique** : comment l'inflation a-t-elle évolué en France entre 2015 et 2025, et quelles sont les principales phases de cette évolution ?

## Contenu

| Fichier / feuille | Rôle |
|---|---|
| `Inflation_France_2015_2025.xlsx` | Classeur complet (6 feuilles ci-dessous) |
| `Tableau_de_bord` | Indicateurs clés, enseignements, 4 graphiques, synthèse par phase |
| `Donnees` | Données saisies (police bleue) avec provenance ligne par ligne |
| `Calculs` | Variations, indice chaîné, rang, catégories forte/modérée/faible, phases, 5e graphique |
| `Statistiques` | Statistiques descriptives et tableau des phases |
| `Controles` | 19 contrôles : valeurs manquantes, plausibilité, recalcul des taux depuis les indices |
| `Sources` | Sources, liens, date de consultation, limites |

Le rapport et la fiche portfolio sont fournis en documents séparés.

## Indicateur retenu

**IPC – ensemble des ménages, France hors Mayotte, variation annuelle moyenne** (INSEE), valeurs publiées à 1 décimale. Compléments : IPC hors énergie, IPC services (INSEE) ; IPCH France et Union européenne (Eurostat, 2016-2025) ; indices annuels base 100 = 2015 (INSEE) pour les contrôles.

## Sources (consultées le 19/11/2026)

- INSEE, *L'essentiel sur… l'inflation* – https://www.insee.fr/fr/statistiques/4268033 (IPC 2015-2023)
- INSEE, *Informations rapides n° 8* – https://www.insee.fr/fr/statistiques/8726461 (2024-2025)
- INSEE, séries BDM 011814640 (ensemble), 011814375 (hors énergie), 011814289 (services), 001764363 (indices base 2015)
- Eurostat, *Consumer prices – inflation* – https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Consumer_prices_-_inflation (IPCH UE) ; dataset `prc_hicp_ainr`

Détail complet dans la feuille `Sources`.

## Étapes de réalisation

1. Recherche et sélection des séries officielles ; choix de l'indicateur.
2. Import et organisation dans `Donnees` (saisie en bleu, provenance par ligne).
3. Contrôles (`Controles`) : complétude, doublons, valeurs aberrantes, recalcul des taux 2021-2025 depuis les indices INSEE, cohérence de l'indice chaîné avec l'indice publié.
4. Calculs (`Calculs`, `Statistiques`) : moyenne, médiane, écart-type, quartiles, extrêmes, hausse cumulée, moyennes par phase.
5. Classification : forte inflation ≥ 2 % (cible BCE), faible < 1 % (seuils modifiables en `Calculs!R6:R7`).
6. Graphiques et tableau de bord.
7. Vérification : recalcul sans erreur de formule, cohérence graphiques/données, rendu contrôlé.

## Limites et données indisponibles

- IPCH France et UE 2015 : non collectés ; indices annuels 2016, 2017, 2019 : non collectés (cellules vides, rien n'est estimé).
- IPCH France 2016-2023 : relayé par un site secondaire (euroflation.com, qui cite Eurostat) ; à recouper sur le Data Browser Eurostat avant publication.
- 2025 : résultats publiés par l'INSEE début 2026 ; caractère définitif non confirmé.
- Champ France hors Mayotte : pas de mesure spécifique à La Réunion.
- Analyse descriptive : aucune causalité n'est établie.
- L'agrégat UE d'Eurostat change de périmètre avec les élargissements.

## Ouverture

Ouvrir le classeur dans Excel (aucune macro). Pour modifier les seuils ou les bornes de phases, changer les cellules à fond jaune ou en police bleue ; tout se recalcule.
