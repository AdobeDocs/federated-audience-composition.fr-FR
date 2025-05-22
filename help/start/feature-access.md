---
title: Accéder à la composition d’audiences fédérées
description: Découvrir les autorisations requises pour la composition d’audiences fédérées
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 7f8ba57e0fd53350690e391e015f5161b2b7d04e
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 40%

---

# Accéder à la composition d’audiences fédérées {#feature-access}

## Gérer l’accès aux sandbox {#access-sandboxes}

Lorsque vous achetez la composition d’audiences fédérées Adobe Experience Platform, un profil de produit est créé pour chaque sandbox actif à ce moment-là. Ce profil de produit est créé dans l’Admin Console sous la carte de produit **Adobe Experience Platform** et suit cette convention de nommage : `ACP_FAC - <<SandboxName>> - admin.`. Pour accéder à la composition d’audiences fédérées pour un sandbox spécifique, les personnes doivent être ajoutées au profil de produit créé pour ce sandbox.

Par exemple, si un nouveau sandbox nommé « fac-test » est activé, un profil de produit correspondant « ACP_FAC - fac-test - admin » est créé. Pour accéder à la composition d’audiences fédérées avec ce sandbox, les personnes doivent être ajoutées à ce profil de produit.

## Gérer l’accès à la composition d’audiences fédérées

Pour accéder à la **composition d’audiences fédérées**, vous devez d’abord vous assurer d’attribuer les autorisations requises pour accéder aux différents aspects de la composition d’audiences fédérées. Ces rôles doivent ensuite être attribués aux utilisateurs et utilisatrices qui ont besoin d’accéder à la **composition d’audiences fédérées**.

Notez que seule l’équipe d’administration a la possibilité d’attribuer des autorisations.

1. Accédez au menu **[!UICONTROL Autorisations]**.

1. Dans le menu **[!UICONTROL Rôles]**, sélectionnez le **[!UICONTROL Rôle]** à mettre à jour.

   ![](assets/access_fda_1.png)

1. Sélectionnez **[!UICONTROL Modifier]** pour modifier les autorisations de votre rôle.

   ![](assets/access_fda_2.png)

1. Ajoutez les autorisations requises pour l’utilisateur. Vous pouvez ajouter les autorisations suivantes pour accéder à la composition d’audiences fédérées :

   | Autorisation | Description |
   | ---------- | ----------- |
   | Gestion des données fédérées | Utilisez cette autorisation pour gérer tous les aspects de la composition des audiences fédérées. Cette autorisation englobe les opérations suivantes : Gérer la base de données fédérée, Gérer le schéma fédéré, Gérer le modèle de données fédérée et Gérer les compositions fédérées. |
   | Gestion de la base de données fédérée | Utilisez cette autorisation pour ajouter, afficher, mettre à jour et supprimer vos connexions aux bases de données fédérées. |
   | Afficher la base de données fédérée | Utilisez cette autorisation pour afficher vos connexions aux bases de données fédérées. |
   | Gestion du schéma fédéré | Utilisez cette autorisation pour créer, afficher, mettre à jour, supprimer et actualiser des schémas. |
   | Affichage Des Données De Schéma Fédéré | Utilisez cette autorisation pour afficher l’onglet de données dans la section de schéma. |
   | Afficher le schéma fédéré | Utilisez cette autorisation pour afficher les tables de schéma. |
   | Gestion du modèle de données fédérées | Utilisez cette autorisation pour créer, afficher, mettre à jour et supprimer des modèles de données. |
   | Afficher le modèle de données fédéré | Utilisez cette autorisation pour afficher les modèles de données. |
   | Afficher le journal d&#39;audit de fédération | Utilisez cette autorisation pour afficher le journal d’audit de la composition d’audiences fédérées. |
   | Gestion des compositions fédérées | Utilisez cette autorisation pour créer, afficher, mettre à jour et supprimer des compositions fédérées. |
   | Afficher les compositions fédérées | Utilisez cette autorisation pour afficher les compositions fédérées. |

   ![](assets/permissions.png)

1. Une fois les modifications nécessaires effectuées, sélectionnez **[!UICONTROL Enregistrer]**.

Les autorisations des utilisateurs et utilisatrices déjà affectés à ce rôle seront automatiquement mises à jour et ils auront accès à la composition d’audiences fédérées.

Pour attribuer ce rôle à de nouvelles personnes, procédez comme suit :

1. Accédez à l’onglet **[!UICONTROL Utilisateurs]** dans votre tableau de bord Rôle et sélectionnez **[!UICONTROL Ajouter des utilisateurs]**.

   ![](assets/access_fda_4.png)

1. Saisissez le nom ou l’adresse e-mail de la personne ou effectuez votre sélection dans la liste disponible. Une fois que vous avez terminé, sélectionnez **[!UICONTROL Enregistrer]**.

Vous pouvez également attribuer l’un des rôles préexistants aux utilisateurs et utilisatrices, en fonction des autorisations dont ils ou elles ont besoin. Pour plus d’informations sur l’attribution de rôles préexistants à un utilisateur, consultez le guide [ sur la gestion des utilisateurs pour un profil de produit](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/ui/users).

| Nom du rôle | Autorisations |
| --------- | ----------- |
| Gestionnaires de données AEC | <ul><li>Gestion des compositions fédérées</li><li>Affichage des bases de données fédérées</li><li>Affichage des schémas fédérés</li><li>Affichage Des Données De Schéma Fédéré</li><li>Affichage des modèles de données fédérés</li></ul> |
| Gestionnaires de composition d&#39;AEC | <ul><li>Gestion des compositions fédérées</li></ul> |
| Administrateurs AEC | <ul><li>Gestion des données fédérées</li></ul> |

La personne recevra un e-mail avec des instructions pour accéder à votre instance. Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez [cette documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/users).
