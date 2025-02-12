---
title: Accéder à la composition de l’audience fédérée
description: Découvrez les autorisations requises pour la composition d’audiences fédérées
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
hide: true
hidefromtoc: true
source-git-commit: e9cc50cbcbd076f784c924bd941e4396c14190ce
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 36%

---

# Accéder à la composition de l’audience fédérée {#feature-access}

## Gérer l’accès aux sandbox {#access-sandboxes}

Lorsque vous achetez le module complémentaire Composition d’audiences fédérées, un profil de produit est créé pour chaque sandbox actif à ce moment-là. Ce profil de produit est créé dans l’Admin Console sous la carte de produit **Adobe Experience Platform** et suit cette convention de nommage : `ACP_FAC - <<SandboxName>> - admin.`. Pour accéder à la composition d’audiences fédérées pour un sandbox spécifique, les personnes doivent être ajoutées au profil de produit créé pour ce sandbox.

Par exemple, si un nouveau sandbox nommé « fac-test » est activé, un profil de produit correspondant « ACP_FAC - fac-test - admin » est créé. Pour accéder à la composition d’audiences fédérées avec ce sandbox, les personnes doivent être ajoutées à ce profil de produit.

## Gérer l’accès à la composition d’audiences fédérées

>[!AVAILABILITY]
>
>Les autorisations sont disponibles dans le cadre de la version de mars.

Pour accéder à la **composition de l’audience fédérée**, vous devez d’abord vous assurer que l’autorisation **Gérer les données fédérées** est affectée aux rôles appropriés. Ces rôles doivent ensuite être attribués aux utilisateurs et utilisatrices qui ont besoin d’accéder à la **composition d’audiences fédérées**.

Notez que seuls les administrateurs ont la possibilité d’attribuer des autorisations.

1. Accédez au menu **[!UICONTROL Autorisations]**.

1. Dans le menu **[!UICONTROL Rôles]**, sélectionnez le **[!UICONTROL Rôle]** que vous souhaitez mettre à jour.

   ![](assets/access_fda_1.png)

1. Cliquez sur **[!UICONTROL Modifier]** pour modifier les autorisations de votre rôle.

   ![](assets/access_fda_2.png)

1. Ajoutez la ressource **Federated Data**, puis sélectionnez **[!UICONTROL Gérer les données fédérées]** dans le menu déroulant.

   ![](assets/access_fda_3.png)

1. Une fois les modifications nécessaires effectuées, cliquez sur **[!UICONTROL Enregistrer]**.

Les autorisations des utilisateurs et utilisatrices déjà affectés à ce rôle seront automatiquement mises à jour et auront accès à la composition de l’audience fédérée.

Pour attribuer ce rôle aux nouveaux utilisateurs :

1. Accédez à l’onglet **[!UICONTROL Utilisateurs]** dans votre tableau de bord Rôle et cliquez sur **[!UICONTROL Ajouter des utilisateurs]**.

   ![](assets/access_fda_4.png)

1. Saisissez le nom ou l’adresse e-mail de l’utilisateur ou sélectionnez-en un dans la liste disponible. Une fois que vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]**.

L’utilisateur recevra alors un e-mail contenant des instructions pour accéder à votre instance. Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez cette [documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/users).
