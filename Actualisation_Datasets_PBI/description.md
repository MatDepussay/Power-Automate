📊 Flow - Actualisation séquencée de rapports Power BI depuis un bouton dans le rapport

🎯 Objectif  
Permet d’actualiser le modèle sémantique de deux rapports Power BI hébergés dans **deux espaces de travail différents**, à la demande, via un bouton intégré dans le rapport.  
Un délai de 5 minutes est respecté entre les deux appels à l'API Power BI afin d’éviter les limitations de fréquence (throttling) liées à l’API REST.

⚙️ Déclencheur  
- Bouton intégré dans le rapport Power BI (Power Automate Visual)
- Le flow est appelé par un clic utilisateur, dans le contexte de la visualisation du rapport

🔁 Étapes principales  
1. Détection du clic sur le bouton Power Automate dans le rapport.  
2. Envoi d’une première requête à l’API REST Power BI pour actualiser le dataset du **rapport 1** dans l’**espace de travail A** :
3. Insertion d’un délai de 5 minutes (`Delay` = `PT5M`) afin de respecter les limites d’usage de l’API.  
4. Envoi d’une seconde requête à l’API REST Power BI pour actualiser le dataset du **rapport 2** dans l’**espace de travail B** :
5. (Optionnel) Ajout d’une notification de confirmation (par e-mail ou Teams) ou d’un journal de logs dans un fichier/log SharePoint.

🔐 Connexions requises  
- Power BI  

📄 Fichier JSON  
Le fichier `flow_definition.json` contient la définition complète du flow, avec tous les appels API et délais intégrés.  
Il peut être importé directement dans Power Automate via l’option d'import de flux.


## 🖼️ Schéma
Ajoute [ici](./schema_flux.png) d'un schéma illustrant le flow :
