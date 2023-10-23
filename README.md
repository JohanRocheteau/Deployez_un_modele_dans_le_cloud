# Projet N°7 : Déployez un modèle dans le cloud

## Mise en situation :

- **Entreprise :**  Fruits!
- **Logo :** ![Logo](PhotosReadme/Logo.png)
- **Activité :** Préserver la biodiversité des fruits via des traitements spécifiques pour chaque espèce de fruits en développant des robots cueilleurs intelligents.
- **But :**
    - Mettre à disposition du grand public une application mobile qui permettrait aux utilisateurs de prendre en photo un fruit et d'obtenir des informations sur ce fruit.
    - Construire une première version de l'architecture Big Data nécessaire à une augmentation de la quantité de données.
- **Jeu de données :** [Kaggle](https://www.kaggle.com/datasets/moltean/fruits) ou [Téléchargement direct](https://s3.eu-west-1.amazonaws.com/course.oc-static.com/projects/Data_Scientist_P8/fruits.zip)
- **Notebook initial :** [Notebook de l'alternant](https://s3.eu-west-1.amazonaws.com/course.oc-static.com/projects/Data_Scientist_P8/Mode_ope%CC%81ratoire.zip)
- **Missions :**
    - S'approprier les réalisés par l’alternant et de compléter la chaîne de traitement.
    - Il n’est pas nécessaire d’entraîner un modèle pour le moment.
    - Mettre en place les premières briques de traitement qui serviront lorsqu’il faudra passer à l’échelle en termes de volume de données !
- **Contrainte :**
    - Continuerer à développer des scripts en Pyspark et à utiliser le cloud AWS pour profiter d’une architecture Big Data (EMR, S3, IAM). 
    - Démontrer la mise en place d’une instance EMR opérationnelle, ainsi qu’expliquer pas à pas le script PySpark, que vous aurez complété. 
    - Traitement de diffusion des poids du modèle Tensorflow sur les clusters (broadcast des “weights” du modèle) qui avait été oublié par l’alternant.
    - Ajouter une étape de réduction de dimension de type PCA en PySpark.
    - Respecter les contraintes du RGPD : localisation = Paris

## Réalisations :

- **Librairies principales :** Pyspark, PIL, Tensorflow
- **Etapes réalisées :**
    - Ouvertures des images
    - Enregistrement des liens pour charger les images + récupération des noms de dossiers (noms des fruits)
    - Ouverture du modèle de réseau de neurones + suppression des deux dernières étapes
    - Extraction des features via le modèle MobilNetV2
    - Reduction des features via PCA de pyspark ![Logo](PhotosReadme/LogoSpark.png)
    - Enregistrement des données extraites au format parquet
    - Passage sur un modèle AWS de type PAAS (EMR EC2) avec enregistrement des images et des donnnées sur S3
      ![logo](PhotosReadme/LogoAWS.png)
      ![logo](PhotosReadme/LogoEMR.png)
      ![logo](PhotosReadme/LogoS3.png)     
