# Analyse des accidents corporels de la route (BAAC 2025)

> Version de travail — compléter les éléments marqués « à renseigner » avant la remise.

## Auteurs
Noms et prénoms : à renseigner (les deux membres du groupe).

## Prérequis
Accès au cluster Onyxia et à son stockage S3 ; environnement d’exécution et versions des outils : à préciser après choix de la chaîne de traitement.

## Jeu de données
BAAC 2025 — fichier Caractéristiques. Source : [bases annuelles des accidents corporels de la circulation](https://www.data.gouv.fr/datasets/bases-de-donnees-annuelles-des-accidents-corporels-de-la-circulation-routiere-annees-de-2005-a-2025). Licence Ouverte / Open Licence. Date de téléchargement : à renseigner. Le CSV source local fait 6,62 Mo ; l’extrait de travail, limité aux 11 colonnes utiles, fait 2,58 Mo et contient 55 093 accidents.

## Problématique
Comment les accidents corporels recensés en France en 2025 se répartissent-ils selon l’heure, les conditions atmosphériques déclarées et le département ? L’analyse porte sur les accidents enregistrés, pas sur un risque rapporté au trafic exposé.

## Chemins S3
Données d’entrée utilisées par le pipeline : `s3://<bucket>/accidents/raw/caract-2025_reduit.csv` (bucket à renseigner).
Résultats agrégés : `s3://<bucket>/accidents/processed/` (nom du résultat à préciser).

## Reproduction
1. Obtenir le fichier Caractéristiques 2025 depuis la source ci-dessus et préparer l’extrait de travail ; la procédure exacte sera fournie dans `src/`.
2. Déposer l’extrait dans le préfixe S3 `accidents/raw/`.
3. Lancer le traitement depuis Onyxia avec la commande qui sera documentée dans `src/`.
4. Vérifier indépendamment les agrégats et consulter le résultat dans `accidents/processed/`.
5. Pour relancer, supprimer ou remplacer les sorties précédentes selon la méthode documentée dans `src/`, puis reprendre à l’étape 3.

Les commandes, outils, noms de sorties et méthode de redémarrage restent à compléter après validation du workflow Onyxia. Les captures d’exécution seront ajoutées dans `evidence/`.
