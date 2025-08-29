---
title: Contrôle d’accès dans la composition d’audiences fédérées
description: Découvrez comment gérer l’accès aux données pour les utilisateurs et les utilisatrices dans la composition d’audiences fédérées.
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: a26e5a2b106426113764d3f2f668ddfbbff85b01
workflow-type: ht
source-wordcount: '606'
ht-degree: 100%

---

# Contrôle d’accès dans la composition d’audiences fédérées

Vous pouvez utiliser le contrôle d’accès pour fournir un accès en fonction du rôle aux sandbox et à la composition d’audiences fédérées.

## Gérer l’accès aux sandbox {#access-sandboxes}

Lorsque vous achetez la composition d’audiences fédérées Adobe Experience Platform, un profil de produit est créé pour chaque sandbox actif à ce moment-là. Ce profil de produit est créé dans l’Admin Console sous la carte de produit **Adobe Experience Platform** et suit cette convention de nommage : `ACP_FAC - <<SandboxName>> - admin.`. Pour accéder à la composition d’audiences fédérées pour un sandbox spécifique, les personnes doivent être ajoutées au profil de produit créé pour ce sandbox.

Par exemple, si un nouveau sandbox nommé « fac-test » est activé, un profil de produit correspondant « ACP_FAC - fac-test - admin » est créé. Pour accéder à la composition d’audiences fédérées avec ce sandbox, les personnes doivent être ajoutées à ce profil de produit.

## Gérer l’accès à la composition d’audiences fédérées

Vous pouvez gérer l’accès en attribuant les autorisations requises pour accéder aux différents aspects de la composition d’audiences fédérées. Ces autorisations doivent ensuite être attribuées aux utilisateurs et utilisatrices qui ont besoin d’accéder à la **composition d’audiences fédérées**.

>[!NOTE]
>
>Seules les personnes membres de l’équipe d’administration peuvent attribuer des autorisations à d’autres utilisateurs ou utilisatrices.

1. Accédez au menu **[!UICONTROL Autorisations]**.
1. Dans le menu **[!UICONTROL Rôles]**, sélectionnez le **[!UICONTROL Rôle]** à mettre à jour.

   ![](assets/access_fda_1.png)

1. Sélectionnez **[!UICONTROL Modifier]** pour modifier les autorisations du rôle.

   ![](assets/access_fda_2.png)

1. Ajoutez les autorisations requises pour la personne. Vous pouvez ajouter les autorisations suivantes pour accéder à la composition d’audiences fédérées :

   | Autorisation | Description |
   | ---------- | ----------- |
   | Gestion des données fédérées | Utilisez cette autorisation pour gérer tous les aspects de la composition d’audiences fédérées. Cette autorisation englobe les opérations suivantes : Gestion de la base de données fédérée, Gestion du schéma fédéré, Gestion du modèle de données fédérées et Gestion des compositions fédérées. |
   | Gestion de la base de données fédérées | Utilisez cette autorisation pour ajouter, afficher, mettre à jour et supprimer vos connexions aux bases de données fédérées. |
   | Affichage de la base de données fédérées | Utilisez cette autorisation pour afficher vos connexions aux bases de données fédérées. |
   | Gestion du schéma fédéré | Utilisez cette autorisation pour créer, afficher, mettre à jour, supprimer et actualiser des schémas. |
   | Affichage des données de schéma fédéré | Utilisez cette autorisation pour afficher l’onglet de données dans la section de schéma. |
   | Affichage du schéma fédéré | Utilisez cette autorisation pour afficher les tables de schéma. |
   | Gestion du modèle de données fédérées | Utilisez cette autorisation pour créer, afficher, mettre à jour et supprimer des modèles de données. |
   | Affichage du modèle de données fédérées | Utilisez cette autorisation pour afficher les modèles de données. |
   | Affichage du journal d’audit de fédération | Utilisez cette autorisation pour afficher le journal d’audit de la composition d’audiences fédérées. |
   | Gestion des compositions fédérées | Utilisez cette autorisation pour créer, afficher, mettre à jour et supprimer des compositions fédérées. |
   | Affichage des compositions fédérées | Utilisez cette autorisation pour afficher les compositions fédérées. |

   ![](assets/permissions.png)

1. Une fois les modifications nécessaires effectuées, cliquez sur **[!UICONTROL Enregistrer]**.

Les autorisations des utilisateurs et utilisatrices déjà affectés à ce rôle seront automatiquement mises à jour et ils auront accès à la composition d’audiences fédérées.

Pour attribuer ce rôle à de nouvelles personnes, procédez comme suit :

1. Accédez à l’onglet **[!UICONTROL Utilisateurs et utilisatrices]** dans votre tableau de bord Rôle et cliquez sur **[!UICONTROL Ajouter des utilisateurs et des utilisatrices]**.

   ![](assets/access_fda_4.png)

1. Saisissez le nom ou l’adresse e-mail de la personne ou effectuez votre sélection dans la liste disponible. Cliquez ensuite sur **[!UICONTROL Enregistrer]**.

Vous pouvez également attribuer l’un des rôles préexistants aux utilisateurs et utilisatrices, en fonction des autorisations dont ils ou elles ont besoin. Pour plus d’informations sur l’attribution de rôles préexistants à une personne, consultez le [guide sur la gestion des personnes pour un profil de produit](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/ui/users).

| Nom du rôle | Autorisations |
| --------- | ----------- |
| Gestionnaires de données FAC | <ul><li>Gestion des compositions fédérées</li><li>Affichage des bases de données fédérées</li><li>Affichage des schémas fédérés</li><li>Affichage des données de schéma fédéré</li><li>Affichage des modèles de données fédérées</li></ul> |
| Gestionnaires de composition FAC | <ul><li>Gestion des compositions fédérées</li></ul> |
| Administrateurs et administratrices FAC | <ul><li>Gestion des données fédérées</li></ul> |

La personne recevra un e-mail avec des instructions pour accéder à votre instance. Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez [cette documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/users).

## Gérer l’accès à des compositions spécifiques

Vous pouvez gérer l’accès à une composition spécifique en appliquant des étiquettes d’accès.

Pour plus d’informations sur l’application d’étiquettes d’accès à une composition, consultez la section [Appliquer des étiquettes d’accès](/help/compositions/gs-compositions.md#access-labels) du guide des compositions.
