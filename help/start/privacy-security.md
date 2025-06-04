---
title: Confidentialité et sécurité dans la composition d’audiences fédérées
description: Découvrez comment la composition de l’audience fédérée traite de la confidentialité et de la sécurité des données utilisateur, y compris des fonctionnalités telles que la gouvernance des données, l’application du consentement, le contrôle d’accès, le chiffrement des données et la conformité en matière de confidentialité.
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 1%

---


# Confidentialité et sécurité dans la composition d’audiences fédérées

La composition de l’audience fédérée respecte de nombreuses pratiques de sécurité afin de protéger vos données pendant le traitement.

## Privacy Service {#privacy}

La composition de l’audience fédérée fournit les données fédérées que Adobe Experience Platform et Adobe Journey Optimizer peuvent utiliser. Cependant, la composition de l’audience fédérée ne stocke **&#x200B;**&#x200B;aucune des données client provenant de l’un des entrepôts de données. Par conséquent, vous pouvez utiliser Adobe Experience Platform Privacy Service pour vous conformer aux demandes de titulaire de données et de suppression de données.

Par exemple, lorsque vous créez une audience à l’aide du bloc d’activité enregistrer dans la zone de travail de composition, l’audience obtenue est stockée dans le lac de données d’Experience Platform en tant qu’audience externe. Cette audience externe est marquée par son champ d’identité et son espace de noms d’identité. Par conséquent, vous pouvez utiliser Privacy Service pour accéder à ces profils et les supprimer avec une audience externe.

Autrement, après la création d’un enrichissement de profil à l’aide de l’activité enregistrer le profil dans la zone de travail de composition, l’enrichissement obtenu est stocké dans Experience Platform sous la forme d’un schéma activé pour le profil et d’un jeu de données activé pour le profil. Ces données d’enrichissement sont marquées d’un champ d’identité et d’un espace de noms d’identité. Par conséquent, vous pouvez utiliser Privacy Service pour accéder à ces profils et les nettoyer.

Pour plus d’informations sur Privacy Service, consultez la présentation de Privacy Service [&#128279;](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/home){target="_blank"}.

### Demandes d’accès à des informations personnelles {#privacy-requests}

Dans Privacy Service, vous pouvez créer et gérer des demandes individuelles de confidentialité pour accéder aux données client et les supprimer de la composition d’audiences fédérées. Privacy Service fournit une [interface utilisateur](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr){target="_blank"} et une [API RESTful](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/api/overview){target="_blank"} pour vous aider à gérer les demandes de données des clients.

Pour plus d’informations sur la création et la gestion des demandes d’accès à des informations personnelles, consultez le [traitement des informations personnelles dans le guide de l’interface utilisateur de Privacy Service](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Application de la politique de consentement {#consent}

La composition de l’audience fédérée, par le biais d’Experience Platform, propose des outils qui vous permettent d’automatiser l’application du consentement, en veillant à activer les audiences en fonction du consentement fourni à vos clients.

Par exemple, lorsque vous créez une audience à l’aide du bloc d’activité enregistrer dans la zone de travail de composition, l’audience obtenue est stockée dans le lac de données d’Experience Platform en tant qu’audience externe. Experience Platform prend automatiquement en charge la validation du consentement lors de l’activation. Pour plus d’informations, veuillez lire la [FAQ sur Segmentation Service](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Autrement, après avoir créé un enrichissement de profil à l’aide de l’activité enregistrer le profil dans la zone de travail de composition, l’enrichissement obtenu est stocké dans Experience Platform sous la forme d’un schéma activé pour le profil et d’un jeu de données activé pour le profil. Pour les profils existants, les attributs de consentement disponibles sont automatiquement respectés lors de l’activation. Pour les nouveaux profils, les attributs de consentement fournis lors de l’ingestion du profil sont automatiquement respectés lors de l’activation. Pour plus d’informations sur l’application des consentements aux profils, consultez le guide [groupe de champs de consentements et de préférences](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Pour plus d’informations sur l’application des consentements, consultez le guide de l’interface utilisateur [gestion des politiques](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Cycle de vie des données {#data-lifecycle}

Comme la composition de l’audience fédérée ne stocke **&#x200B;**&#x200B;aucune des données client provenant de l’un des entrepôts de données, vous pouvez utiliser Experience Platform pour gérer le cycle de vie des données. Grâce à la gestion avancée du cycle de vie des données, vous pouvez gérer votre cycle de vie des données au niveau des jeux de données et des enregistrements.

Par exemple, lorsque vous créez une audience à l’aide du bloc d’activité enregistrer dans la zone de travail de composition, l’audience obtenue est stockée dans le lac de données d’Experience Platform en tant qu’audience externe. Comme ces données ne sont **pas** stockées dans la composition d’audiences fédérées, les données d’audience et les jeux de données correspondants sont automatiquement supprimés lorsque l’audience est supprimée dans Audience Portal.

Autrement, après avoir créé un enrichissement de profil à l’aide de l’activité enregistrer le profil dans la zone de travail de composition, l’enrichissement obtenu est stocké dans Experience Platform sous la forme d’un schéma activé pour le profil et d’un jeu de données activé pour le profil. Par conséquent, vous pouvez utiliser le cycle de vie des données pour accéder aux profils et les nettoyer.

Pour plus d’informations sur l’utilisation du cycle de vie des données, consultez la [présentation du cycle de vie des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Libellés d’utilisation des données {#data-usage-labels}

Les libellés d’utilisation des données vous permettent de classer les jeux de données et les champs en fonction des politiques de gouvernance qui s’appliquent à ces données. Après avoir créé une audience à l’aide de compositions, vous pouvez appliquer les libellés de données appropriés sur le schéma résultant pour vous assurer qu’elle respecte les restrictions d’utilisation requises.

Pour plus d’informations sur l’utilisation des libellés de données, consultez la [ présentation des libellés d’utilisation des données ](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Chiffrement {#encryption}

Une composition d’audience flexible fournit un chiffrement par le biais d’un chiffrement des données au repos, d’un chiffrement des données en transit et de clés gérées par le client.

Les données au repos font référence aux données client utilisées dans la composition d’audiences fédérées. Les données sont chiffrées par le fournisseur de services cloud et sont utilisées dans la composition d’audiences fédérées sous leur forme chiffrée.

Les données en transit font référence aux données client lors de leur déplacement d’un composant à un autre dans la composition d’audiences fédérées. Les données sont conservées chiffrées dans tous les composants de composition d’audience fédérée à l’aide de TLS 1.3 via HTTPS.

Pour plus d’informations sur la façon dont Adobe gère le chiffrement des données, consultez le guide sur le [ chiffrement des données dans Experience Platform ](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Clés gérées par le client {#customer-managed-keys}

Les clés gérées par la clientèle vous permettent de contrôler vos données en vous permettant d’utiliser vos propres clés de chiffrement pour chiffrer vos données. Comme la composition de l’audience fédérée ne stocke **aucune donnée client** vous pouvez utiliser des clés gérées par le client directement sur les audiences et enrichissements obtenus, puisqu’elles seront stockées dans le lac de données sur Experience Platform.

Pour plus d’informations sur les clés gérées par le client, consultez le [guide des clés gérées par le client](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Journal d’audit {#audit-log}

Toutes les opérations de création, de lecture, de mise à jour et de suppression effectuées dans la composition d’audiences fédérées sont consignées dans le journal d’audit. Vous pouvez utiliser ce journal d’audit pour suivre ces actions, appliquer la responsabilité et prendre en charge les audits de conformité.

Pour plus d’informations, consultez la [présentation du journal d’audit](/help/admin/audit-trail.md){target="_blank"}.

## Contrôle d’accès {#access-control}

Vous pouvez contrôler l’accès à la composition de l’audience fédérée au niveau du champ et au niveau du rôle. Vous pouvez utiliser ces contrôles d’accès pour appliquer les politiques de gouvernance des données, limiter l’exposition des informations sensibles et aligner l’accès sur les responsabilités des utilisateurs et utilisatrices.

Pour plus d’informations sur le contrôle d’accès dans la composition d’audiences fédérées, consultez le [guide sur la composition d’audiences fédérées Access](/help/start/feature-access.md){target="_blank"}.

## Localisation des données {#data-localization}

La composition d’audience fédérée ne stocke **pas** de données client. Par conséquent, vous devez vous assurer que vous **uniquement** connectez vos bases de données externes à la région de sandbox correspondante pour conserver vos données dans la même région. Si vous connectez la base de données d’une autre région à un sandbox, Adobe n’est **pas** responsable de la localisation des données.

## Étapes suivantes {#next-steps}

Vous êtes arrivé au bout de ce guide, vous comprenez mieux les fonctionnalités de confidentialité et de sécurité utilisées pour la composition de l’audience fédérée, notamment la gouvernance des données, la conformité en matière de confidentialité, l’application du consentement, la gestion du cycle de vie des données et le contrôle d’accès.
