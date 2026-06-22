---
audience: end-user
title: Enrichir les audiences Adobe Experience Platform avec des données externes
description: Découvrez comment affiner et enrichir les audiences Adobe Experience Platform avec les données de vos bases de données fédérées à l’aide de la destination Composition d’audiences fédérées.
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
TQID: https://experienceleague.adobe.com/g32ycFuhXFq68NmBJjunWZT3m4JpmL108bhMSs-4EYc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ce79e1b9216ca69020155978ac84f29577c5ff8d
workflow-type: ht
source-wordcount: 774
ht-degree: 100%

---

# Enrichir les audiences Adobe Experience Platform avec des données externes {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Créer une destination"
>abstract="Renseignez les paramètres de connexion à la nouvelle base de données fédérée. Utilisez le bouton **[!UICONTROL Se connecter à la destination]** pour valider votre configuration."

Adobe Experience Platform permet une intégration transparente des audiences du portail d’audiences avec vos bases de données externes à l’aide de la **destination Adobe Composition d’audiences fédérées**. Grâce à cette intégration, vous pouvez tirer profit des audiences existantes dans des compositions et les enrichir ou les affiner à l’aide des données de vos bases de données externes pour créer des audiences.

Pour ce faire, vous devez configurer une nouvelle connexion dans Adobe Experience Platform à la destination Adobe Composition d’audiences fédérées. Vous pouvez utiliser un planificateur pour envoyer une audience donnée à des fréquences régulières, puis sélectionner des attributs spécifiques à inclure, tels que les identifiants pour la réconciliation des données. Si vous avez appliqué des politiques de gouvernance et de confidentialité à votre audience, elles seront conservées et renvoyées au portail d’audience une fois l’audience mise à jour.

Supposons que vous stockiez des informations d’achat dans votre entrepôt de données et qu’une audience Adobe Experience Platform cible la clientèle intéressée par un produit spécifique au cours des deux derniers mois. À l’aide de la destination Composition d’audiences fédérées, vous pouvez effectuer les opérations suivantes :

* Affiner l’audience en fonction des informations d’achat. Par exemple, vous pouvez filtrer l’audience pour cibler uniquement la clientèle qui a effectué un achat de plus de 150 dollars.
* Enrichir l’audience avec les champs relatifs aux achats, tels que le nom du produit et la quantité achetée.

## Activer l’audience pour une destination {#activate}

Dans le catalogue de destinations d’Adobe Experience Platform, sélectionnez la destination Composition d’audiences fédérées.Dans le volet de droite, sélectionnez **[!UICONTROL Configurer une nouvelle destination]**.

![Le bouton Configurer une nouvelle destination est mis en surbrillance dans le catalogue des destinations.](assets/destinations/new.png)

La page **[!UICONTROL Configurer une nouvelle destination]** s’affiche.Sur cette page, vous pouvez configurer les détails de votre destination, notamment son nom, sa description, le type de connexion et la base de données fédérée.

![La page Configurer une nouvelle destination s’affiche et indique les détails à ajouter pour créer la destination.](assets/destinations/configure.png)

La section **[!UICONTROL Alertes]** permet d’activer les alertes pour recevoir des notifications sur le statut de votre flux de données vers votre destination. Il s’agit notamment d’alertes pour les retards d’exécutions de flux de données, les échecs d’exécutions, les exécutions réussies, les démarrages d’exécutions et les activations ignorées.

Pour plus d’informations sur les alertes, consultez la documentation d’Adobe Experience Platform sur l’[abonnement aux alertes des destinations dans l’interface d’utilisation](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/ui/alerts){target="_blank"}.

![Les alertes disponibles pour la destination s’affichent.](assets/destinations/alerts.png)

Une fois les détails de la destination configurés, sélectionnez **[!UICONTROL Suivant]**.L’étape **[!UICONTROL Politique de gouvernance et mesures d’application]** s’affiche.Sur cette page, vous pouvez définir vos politiques de gouvernance des données et vous assurer que les données utilisées sont conformes lorsque les audiences sont envoyées et actives.

Lorsque vous avez terminé de sélectionner les actions marketing souhaitées pour la destination, sélectionnez **[!UICONTROL Créer]**.

La nouvelle connexion à la destination est créée. Vous pouvez désormais activer les audiences à envoyer vers la destination. Sélectionnez la destination pour laquelle vous souhaitez activer les audiences, puis sélectionnez **[!UICONTROL Suivant]**.

![Le bouton Activer est mis en surbrillance.](assets/destinations/activate.png)

L’étape **[!UICONTROL Planification]** s’affiche.Vous pouvez sélectionner les audiences que vous souhaitez activer pour la destination.Pour configurer un planning, sélectionnez l’![icône en forme de crayon](assets/do-not-localize/Smock_Edit_18_N.svg) pour modifier votre planning d’exportation.

![La page Activer la destination s’affiche.](assets/destinations/schedule.png)

La fenêtre contextuelle **[!UICONTROL Planification]** s’affiche.Dans cette fenêtre contextuelle, vous pouvez définir vos options d’exportation de fichiers, la fréquence d’exportation et configurer votre planning.

![La fenêtre contextuelle du planning s’affiche.](assets/destinations/schedule-2.png)

>[!NOTE]
>
>Pour activer les audiences plus rapidement, sélectionnez l’option **[!UICONTROL Après l’évaluation du segment]** pour déclencher le traitement d’activation immédiatement après la fin du traitement de segmentation par lots quotidien de Platform.
>
>Pour obtenir des informations détaillées sur la configuration des plannings et des noms de fichiers, consultez les sections suivantes de la documentation d’Adobe Experience Platform :
>
>* [Planifier l’export d’audience](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
>* [Configurer les noms de fichiers](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

Au cours de l’étape du **[!UICONTROL Mappage]**, vous pouvez sélectionner les champs d’attribut et d’identité à exporter pour vos audiences.

>[!IMPORTANT]
>
>Vous **ne pouvez pas** utiliser de colonnes générées par le système lors des activations vers des destinations.La sélection d’une colonne générée par le système entraînera une erreur.

Pour plus d’informations, consultez la [section Mappage](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"} dans la documentation d’Adobe Experience Platform.

![La page de mappage des attributs s’affiche.](assets/destinations/attributes.png)

Vérifiez la configuration de destination et les paramètres de l’audience, puis sélectionnez **[!UICONTROL Terminer]**.

![La page de vérification de la destination s’affiche.](assets/destinations/review.png)

Les audiences sélectionnées sont désormais activées pour la nouvelle connexion. Vous pouvez ajouter d’autres audiences à envoyer avec cette connexion en revenant à la page **[!UICONTROL Activer les audiences]**. Une fois activées, les audiences ne peuvent pas être supprimées.
