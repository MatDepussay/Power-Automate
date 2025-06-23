# 🔄 Flow - Actualisation séquencée des datasets Power BI

## 🎯 Objectif
Permettre l'actualisation manuelle de plusieurs datasets Power BI via un **bouton intégré dans un rapport** tout en **respectant un délai de 5 minutes entre chaque actualisation** pour éviter de surcharger les appels API.

## ⚙️ Déclencheur
- Bouton Power BI déclencheur via **Power BI Service + Power Automate Visual**

## 🔁 Étapes principales
1. Le flow est déclenché depuis un rapport Power BI via un bouton (visual Power Automate).
2. Appel de l’API Power BI pour actualiser le premier dataset (`POST https://api.powerbi.com/v1.0/myorg/datasets/{datasetId}/refreshes`)
3. Attente de 5 minutes (`Delay` action)
4. Appel de l’API pour le 2e dataset
5. Répéter l’attente et l’actualisation autant de fois que nécessaire.

## ⏱️ Délai entre chaque dataset
- `Delay` → 5 minutes (`PT5M`) entre chaque appel d'API
- Permet de contourner les limites de fréquence de l’API REST Power BI

## 🔐 Connexions utilisées
- Power BI

## 📄 Fichier JSON
Le fichier `flow_definition.json` contient l’ensemble des actions et peut être importé dans Power Automate.

## 🖼️ Schéma
Ajoute [ici](./schema_flux.png) d'un schéma illustrant le flow :
