👥 Flow - Récupération des membres d'une équipe Microsoft Teams (V2)
🎯 Objectif
Ce flow permet d'extraire automatiquement la liste des membres de toutes les équipes Microsoft Teams auxquelles l'utilisateur appartient, en enregistrant l’information avec une date d'extraction. Un traitement de nettoyage est ensuite effectué pour supprimer les doublons intelligemment.

⚙️ Déclencheur
Déclenchement manuel via Power Automate

Peut également être intégré à un flux planifié pour une mise à jour régulière

🔁 Étapes principales
Récupération des équipes Microsoft Teams dont je suis membre (List my joined teams)

Pour chaque équipe :

Récupération des canaux (List channels)

Pour chaque canal :

Récupération des membres (Get channel members)

Ajout d’une ligne dans Excel pour chaque membre avec :

Nom de l’équipe

Nom du canal

Nom complet du membre

Adresse email

Date d’extraction

Rôle dans le canal (membre, propriétaire, invité…)

Suppression intelligente des doublons via un script externe :

Les doublons sont identifiés sur le trio (Personne, Canal, Équipe)

En cas de doublon, la version avec la date la plus ancienne est conservée

💡 Contrairement à la version précédente, aucune suppression de lignes existantes n’est effectuée au début du processus : les doublons sont gérés a posteriori de manière ciblée.

🔐 Connexions requises
Microsoft Teams / Office 365 Groups

Excel Online (Business) ou SharePoint (selon l'emplacement du fichier)

📄 Fichier JSON
Le fichier flow_definition.json contient l’ensemble des actions du flow. Il peut être importé dans Power Automate via "Importer une solution" ou "Nouveau flux > Importer un package".

🖼️ Schéma du flow
[Ancienne version](./Schema_fluxV1.png)

[Nouvelle version](./Schema_flux.png)
