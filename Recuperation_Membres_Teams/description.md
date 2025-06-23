# 👥 Flow - Récupération des membres d'une équipe Microsoft Teams

## 🎯 Objectif
Ce flow permet de récupérer automatiquement la liste des membres des équipes Microsoft Teams ou je suis présent et de la stocker (ou utiliser) pour un usage administratif ou analytique.

## ⚙️ Déclencheur
- Manuel ou planifié via un autre flow

## 🔁 Étapes principales
1. Connexion à Microsoft Teams via un connecteur.
2. Appel de l’API Graph ou d’un connecteur natif pour récupérer les membres de l’équipe.
3. Traitement de la réponse : filtrage, transformation si besoin.
4. Export des données dans un fichier Excel, SharePoint, ou autre selon le besoin.

## 🔐 Connexions requises
- Microsoft Teams
- (Optionnel) Excel, SharePoint ou autre pour la sortie

## 📄 Fichier JSON
Le fichier `flow_definition.json` contient le flow complet, réutilisable dans Power Automate.

## 🖼️ Schéma du flow
*(Tu peux ajouter une image ici : `schema_flux.png`)*
