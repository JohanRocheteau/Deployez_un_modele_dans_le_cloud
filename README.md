# Projet N°7 : Déployez un modèle dans le cloud

## Mise en situation :

- **Entreprise :**  Fruits!
- **Logo :**
- **Activité :** Préserver la biodiversité des fruits via des traitements spécifiques pour chaque espèce de fruits en développant des robots cueilleurs intelligents.
- **But :**
    - Mettre à disposition du grand public une application mobile qui permettrait aux utilisateurs de prendre en photo un fruit et d'obtenir des informations sur ce fruit.
    - Construire une première version de l'architecture Big Data nécessaire à une augmentation de la quantité de données.
- **Jeu de données :**[Kaggle](https://www.kaggle.com/datasets/moltean/fruits) ou [Téléchargement direct](https://s3.eu-west-1.amazonaws.com/course.oc-static.com/projects/Data_Scientist_P8/fruits.zip)
- 
- 



Votre collègue Paul vous indique l’existence d’un document, formalisé par un alternant qui vient de quitter l’entreprise. Il a testé une première approche dans un environnement Big Data AWS EMR, à partir d’un jeu de données constitué des images de fruits et des labels associés (en téléchargement direct à ce lien). Le notebook réalisé par l’alternant servira de point de départ pour construire une partie de la chaîne de traitement des données.
Votre mission

Vous êtes donc chargé de vous approprier les travaux réalisés par l’alternant et de compléter la chaîne de traitement.

Il n’est pas nécessaire d’entraîner un modèle pour le moment.

L’important est de mettre en place les premières briques de traitement qui serviront lorsqu’il faudra passer à l’échelle en termes de volume de données !
Contraintes

Lors de son brief initial, Paul vous a averti des points suivants :

    Vous devrez tenir compte dans vos développements du fait que le volume de données va augmenter très rapidement après la livraison de ce projet. Vous continuerez donc à développer des scripts en Pyspark et à utiliser le cloud AWS pour profiter d’une architecture Big Data (EMR, S3, IAM). Si vous préférez, vous pourrez transférer les traitements dans un environnement Databricks
    Vous devez faire une démonstration de la mise en place d’une instance EMR opérationnelle, ainsi qu’ expliquer pas à pas le script PySpark, que vous aurez complété : 
        d’un traitement de diffusion des poids du modèle Tensorflow sur les clusters (broadcast des “weights” du modèle) qui avait été oublié par l’alternant. Vous pourrez vous appuyer sur l’article “Distributed model inference using TensorFlow Keras” disponible dans les ressources
        d’une étape de réduction de dimension de type PCA en PySpark 
    Vous respecterez les contraintes du RGPD : dans notre contexte, vous veillerez à paramétrer votre installation afin d’utiliser des serveurs situés sur le territoire européen 
    Votre retour critique de cette solution sera également précieuse, avant de décider de la généraliser
    La mise en œuvre d’une architecture Big Data de type EMR engendrera des coûts. Vous veillerez donc à ne maintenir l’instance EMR opérationnelle que pour les tests et les démos.
