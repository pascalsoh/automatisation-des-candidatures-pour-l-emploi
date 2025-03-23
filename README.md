**SYSTÈME AUTOMATISÉ DE GESTION DES CANDIDATURES** 

 Ce projet vise à exploiter la puissance de Microsoft Power Automate pour créer un flux de travail automatisé qui recueille les informations fournies par les candidats via un formulaire, les intègre dans une liste SharePoint et envoie automatiquement des e-mails de confirmation aux candidats.
Pour le faire, nous avons : 
- D'abord créer le **formulaire** avec **Microsoft forms** : ce formulaire possède 6 champs à savoir :
  * le nom,
  * le prénom,
  * le numéro de téléphone,
  * l'adresse mail,
  * le lien veers le CV
  * la lettre de motivation
    
- Ensuite on crée une **liste** dans **SharePoint** : cette liste a les mêmes champs que l'on retrouve dans le formulaire créé précédemment.
- Enfin, on part dans **Power Automate** : ici, nous automatisons l'envoi des mail de confirmation aux candidats de la reception de leurs candidatures. pour ce faire, nous allons :
  
  * D'abord, prendre **Lorsqu'une nouvelle réponse est envoyée** comme **déclencheur automatique** : ici, on choisit le formulaire qu'on a créé avec Microsoft forms au tout début
  * Ensuite, choisir comme action **Obtenir les détails de la réponse** : comme ce qui a été fait précédemment, on choisit le formulaire créé avec Microsoft forms pour avoir accès à tous ses champs afin de l'utiliser plutard.
  * Après, prendre comme action **Créer un élément** dans SharePoint: cette action nous permet de lier le formulaire et la liste sharepoint afin que lorsque le formulaire est rempli, tous les éléments qui s'y trouvent vont se stocker dans la liste SharePoint.
  * Enfin, selectionner comme action **Envoyer un e-mail (V2)** : ici, on va utiliser les adresses mails stockés dans la liste SharePoint pour envoyer le mail de confirmation aux candidats.
 
![Power Automate automatisation](https://github.com/pascalsoh/automatisation-des-candidatures-pour-l-emploi/blob/98a9c8b960bb709a081fc67b5a774691db936901/Capture%20d'%C3%A9cran%202025-03-23%20231910.png)
