---
audience: end-user
title: Enrichir les audiences Adobe Experience Platform avec des données externes
description: Découvrez comment affiner et enrichir les audiences Adobe Experience Platform avec les données de vos bases de données fédérées à l’aide de la destination de composition d’audiences fédérées.
badge: label="Disponibilité limitée" type="Informative"
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 4%

---

# Enrichir les audiences Adobe Experience Platform avec des données externes {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Créer une destination"
>abstract="Renseignez les paramètres de connexion à la nouvelle base de données fédérée. Utilisez le bouton **[!UICONTROL Se connecter à la destination]** pour valider votre configuration."

Adobe Experience Platform permet une intégration transparente des audiences du portail d’audience avec vos bases de données externes à l’aide de la **destination Adobe de composition d’audience fédérée**. Grâce à cette intégration, vous pouvez exploiter les audiences existantes dans des compositions et les enrichir ou les affiner à l’aide des données de vos bases de données externes pour créer de nouvelles audiences.

Pour ce faire, vous devez configurer une nouvelle connexion dans Adobe Experience Platform à la destination Adobe Federated Audience Composition . Vous pouvez utiliser un planificateur pour envoyer une audience donnée à des fréquences régulières, sélectionner des attributs spécifiques à inclure, tels que les identifiants pour la réconciliation des données. Si vous avez appliqué des politiques de gouvernance et de confidentialité à votre audience, elles seront conservées et renvoyées au portail d’audience une fois l’audience mise à jour.

Supposons, par exemple, que vous stockiez des informations d’achat dans votre entrepôt de données et qu’une audience Adobe Experience Platform cible les clients intéressés par un produit spécifique au cours des deux derniers mois. À l’aide de la destination Composition de l’audience fédérée , vous pouvez :

* Affinez l’audience en fonction des informations d’achat. Par exemple, vous pouvez filtrer l’audience pour cibler les clients qui ont effectué un achat de plus de 150$ uniquement.
* Enrichissez l&#39;audience avec les champs relatifs aux achats, tels que le nom du produit et la quantité achetée.

Les principales étapes pour envoyer des audiences Adobe Experience Platform à la composition d’audiences fédérées Adobe sont les suivantes :

1. Accédez au catalogue des destinations Adobe Experience Platform et sélectionnez la destination Composition d’audience fédérée .

   Dans le volet de droite, sélectionnez **[!UICONTROL Configurer une nouvelle destination]**.

   ![](assets/destination-new.png)

1. Attribuez un nom à la nouvelle connexion, choisissez le **[!UICONTROL Type de connexion]** à utiliser et la **[!UICONTROL base de données fédérée]** à laquelle vous souhaitez vous connecter, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/destination-configure.png)

   La section **[!UICONTROL Alertes]** vous permet d’activer les alertes pour recevoir des notifications sur l’état du flux de données vers votre destination. Pour plus d’informations sur les alertes, consultez la documentation de Adobe Experience Platform au sujet de l’ [abonnement aux alertes de destinations à l’aide de l’interface utilisateur ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts){target="_blank"}

1. L’étape **[!UICONTROL Stratégie de gouvernance et actions d’application]** vous permet de définir vos stratégies de gouvernance des données et de vous assurer que les données utilisées sont conformes lorsque les audiences sont envoyées et actives.

   Lorsque vous avez terminé de sélectionner les actions marketing souhaitées pour la destination, cliquez sur **[!UICONTROL Créer]**.

1. La nouvelle connexion à la destination est créée. Vous pouvez désormais activer les audiences à envoyer vers la destination. Pour ce faire, sélectionnez-le dans la liste et cliquez sur **[!UICONTROL Suivant]**

   ![](assets/destination-activate.png)

1. Sélectionnez les audiences que vous souhaitez envoyer, puis cliquez sur **[!UICONTROL Suivant]**.

1. Configurez le nom du fichier et un planning d&#39;export pour la ou les audiences sélectionnées.

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >Vous trouverez des informations détaillées sur la configuration de la planification et des noms de fichier dans les sections suivantes de la documentation Adobe Experience Platform :
   >
   >* [Planification de l’exportation de l’audience](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
   >* [Configurer les noms de fichiers](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

1. À l’étape **[!UICONTROL Mapping]**, sélectionnez les champs d’attribut et d’identité à exporter pour vos audiences. Pour plus d’informations, consultez l’[ étape de mappage](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"} dans la documentation Adobe Experience Platform.

   ![](assets/destination-attributes.png)

1. Vérifiez la configuration de destination et les paramètres de l’audience, puis cliquez sur **[!UICONTROL Terminer]**.

   ![](assets/destination-review.png)

Les audiences sélectionnées sont désormais activées pour la nouvelle connexion. Vous pouvez ajouter d’autres audiences à envoyer avec cette connexion en revenant à la page **[!UICONTROL Activer les audiences]**. Une fois activées, les audiences ne peuvent pas être supprimées.
