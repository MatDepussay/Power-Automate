👥 Flow - Récupération des membres d'une équipe Microsoft Teams

🎯 Objectif  
Ce flow permet de récupérer automatiquement la liste des membres de toutes les équipes Microsoft Teams où la personne qui déclenche le flux est membre. Ces données peuvent ensuite être utilisées à des fins administratives ou d'analyse. 

⚙️ Déclencheur  
- Déclenchement manuel via Power Automate
- Peut aussi être déclenché automatiquement via un autre flow planifié

🔁 Étapes principales  
1. Lecture du fichier Excel de destination pour lister les lignes existantes.  
2. Suppression de toutes les lignes afin d’éviter les doublons lors de l’actualisation des données.  
3. Récupération de toutes les équipes Microsoft Teams dont je suis membre (`List my joined teams`).  
4. Pour chaque équipe :
   - Récupération de la liste des canaux (`List channels`).  
   - Pour chaque canal :
     - Récupération des membres (`Get channel members`).  
     - Ajout d’une ligne dans Excel pour chaque membre avec les informations suivantes :  
       - Nom de l’équipe  
       - Nom du canal  
       - Nom complet du membre  
       - Adresse email  
       - Rôle dans le canal (membre, propriétaire, invité, etc.)
5. Le fichier Excel final contient donc une ligne **par personne, par canal, par équipe**, ce qui permet des analyses croisées précises.

🔐 Connexions requises  
- Microsoft Teams / Office 365 Groups  
- Excel Online (Business) ou SharePoint (selon destination)

📄 Fichier JSON  
Le fichier `flow_definition.json` contient toutes les actions du flow. Il peut être importé dans Power Automate via "Importer une solution" ou "Nouveau flux > Importer un package".


## 🖼️ Schéma du flow
Ajoute [ici](./Schema_flux.png) d'un schéma illustrant le flow :
