---
title: Confidentialité et sécurité de la composition d’audiences fédérées
description: Découvrez comment la composition d’audiences fédérées traite la confidentialité et la sécurité des données d’utilisation, y compris les fonctionnalités telles que la gouvernance des données, l’application du consentement, le contrôle d’accès, le chiffrement des données et la conformité en matière de confidentialité.
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 8076a7851d0cd5cd84a7c48c6f1783b452864903
workflow-type: ht
source-wordcount: '1085'
ht-degree: 100%

---

# Confidentialité et sécurité de la composition d’audiences fédérées

La composition d’audiences fédérées respecte de nombreuses pratiques de sécurité afin de protéger vos données pendant le traitement.

## Privacy Service {#privacy}

La composition d’audiences fédérées fournit les données fédérées qu’Adobe Experience Platform et Adobe Journey Optimizer peuvent utiliser. Cependant, la composition d’audiences fédérées ne stocke **aucune** des données clientèle provenant des entrepôts de données. Par conséquent, vous pouvez utiliser Adobe Experience Platform Privacy Service pour vous conformer aux demandes des personnes titulaires de données et aux demandes de suppression de données.

Par exemple, lorsque vous créez une audience à l’aide du bloc d’activité Enregistrer dans la zone de travail de la composition, l’audience obtenue est stockée dans le lac de données d’Experience Platform en tant qu’audience externe. Cette audience externe est marquée par son champ d’identité et son espace de noms d’identité. Par conséquent, vous pouvez utiliser Privacy Service pour accéder à ces profils et les supprimer avec une audience externe.

Autrement, après la création d’un enrichissement de profil à l’aide de l’activité Enregistrer le profil dans la zone de travail de la composition, l’enrichissement obtenu est stocké dans Experience Platform sous la forme d’un schéma activé pour le profil et d’un jeu de données activé pour le profil. Ces données d’enrichissement sont marquées d’un champ d’identité et d’un espace de noms d’identité. Par conséquent, vous pouvez utiliser Privacy Service pour accéder à ces profils et les nettoyer.

Pour plus d’informations sur Privacy Service, veuillez commencer par lire la [vue d’ensemble de Privacy Service](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/home){target="_blank"}.

### Demandes d’accès à des informations personnelles {#privacy-requests}

Dans Privacy Service, vous pouvez créer et gérer des demandes individuelles d’accès et de suppression de données des clientes et clients de la composition d’audiences fédérées. Privacy Service fournit une [interface d’utilisation](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr){target="_blank"} et une [API RESTful](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/api/overview){target="_blank"} pour vous aider à gérer les demandes de données de la clientèle.

Pour plus d’informations sur la création et la gestion des demandes d’accès à des informations personnelles, consultez les [traitements des informations personnelles dans le guide de l’interface d’utilisation de Privacy Service](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Application des politiques de consentement {#consent}

La composition d’audiences fédérées, par le biais d’Experience Platform, propose des outils qui vous permettent d’automatiser l’application du consentement, en veillant à activer les audiences en fonction du consentement fourni à votre clientèle.

Par exemple, lorsque vous créez une audience à l’aide du bloc d’activité Enregistrer dans la zone de travail de la composition, l’audience obtenue est stockée dans le lac de données d’Experience Platform en tant qu’audience externe. Experience Platform prend automatiquement en charge la validation du consentement lors de l’activation. Pour plus d’informations, veuillez lire les [Questions fréquentes sur Segmentation Service](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Autrement, après la création d’un enrichissement de profil à l’aide de l’activité Enregistrer le profil dans la zone de travail de la composition, l’enrichissement obtenu est stocké dans Experience Platform sous la forme d’un schéma activé pour le profil et d’un jeu de données activé pour le profil. Pour les profils existants, les attributs de consentement disponibles sont automatiquement respectés lors de l’activation. Pour les nouveaux profils, les attributs de consentement fournis lors de l’ingestion du profil sont automatiquement respectés lors de l’activation. Pour plus d’informations sur l’application des consentements aux profils, consultez le [guide sur le groupe de champs de consentements et de préférences](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Pour plus d’informations sur l’application de consentements, consultez le [guide de l’interface d’utilisation des politiques de gestion](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Cycle de vie des données {#data-lifecycle}

Comme la composition d’audiences fédérées ne stocke **aucune** des données clientèle provenant des entrepôts de données, vous pouvez utiliser Experience Platform pour gérer le cycle de vie des données. Grâce à la gestion avancée du cycle de vie des données, vous pouvez gérer votre cycle de vie des données au niveau des jeux de données et des enregistrements.

Par exemple, lorsque vous créez une audience à l’aide du bloc d’activité Enregistrer dans la zone de travail de la composition, l’audience obtenue est stockée dans le lac de données d’Experience Platform en tant qu’audience externe. Comme ces données ne sont **pas** stockées dans la composition d’audiences fédérées, les données d’audience et les jeux de données correspondants sont automatiquement supprimés lorsque l’audience est supprimée dans Audience Portal.

Autrement, après la création d’un enrichissement de profil à l’aide de l’activité Enregistrer le profil dans la zone de travail de la composition, l’enrichissement obtenu est stocké dans Experience Platform sous la forme d’un schéma activé pour le profil et d’un jeu de données activé pour le profil. Par conséquent, vous pouvez utiliser le cycle de vie des données pour accéder aux profils et les nettoyer.

Pour plus d’informations sur le cycle de vie des données, consultez la [vue d’ensemble du cycle de vie des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Libellés d’utilisation des données {#data-usage-labels}

Les libellés d’utilisation des données vous permettent de classer les jeux de données et les champs en fonction des politiques de gouvernance qui s’appliquent à ces données. Après avoir créé une audience à l’aide de compositions, vous pouvez appliquer les libellés de données appropriés sur le schéma résultant pour vous assurer qu’elle respecte les restrictions d’utilisation requises.

Pour plus d’informations sur l’utilisation des libellés de données, consultez la [vue d’ensemble des libellés d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Chiffrement {#encryption}

Une composition d’audiences flexible fournit un chiffrement des données au repos, un chiffrement des données en transit et des clés gérées par la clientèle.

Les données au repos font référence aux données clientèle utilisées dans la composition d’audiences fédérées. Les données sont chiffrées par le fournisseur de service cloud et sont utilisées dans la composition d’audiences fédérées sous leur forme chiffrée.

Les données en transit font référence aux données clientèle lors de leur déplacement d’un composant à un autre dans la composition d’audiences fédérées. Les données sont conservées chiffrées dans tous les composants de composition d’audiences fédérées à l’aide de TLS 1.3 via HTTPS.

Pour plus d’informations sur la façon dont Adobe gère le chiffrement des données, consultez le guide sur le [chiffrement des données dans Experience Platform ](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Clés gérées par la clientèle {#customer-managed-keys}

Les clés gérées par la clientèle vous permettent de contrôler vos données en utilisant vos propres clés de chiffrement pour chiffrer vos données. Comme la composition d’audiences fédérées ne stocke **aucune** donnée clientèle, vous pouvez utiliser des clés gérées par la clientèle directement sur les audiences et enrichissements obtenus, puisqu’ils seront stockés dans le lac de données sur Experience Platform.

Pour plus d’informations sur les clés gérées par la clientèle, consultez le [guide des clés gérées par la clientèle](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Journal d’audit {#audit-log}

Toutes les opérations de création, de lecture, de mise à jour et de suppression effectuées dans la composition d’audiences fédérées sont consignées dans le journal d’audit. Vous pouvez utiliser ce journal d’audit pour suivre ces actions, appliquer la responsabilité et prendre en charge les audits de conformité.

Pour plus d’informations, consultez la [vue d’ensemble du journal d’audit](/help/admin/audit-trail.md){target="_blank"}.

## Contrôle d’accès {#access-control}

Vous pouvez contrôler l’accès à la composition d’audiences fédérées au niveau du champ et au niveau du rôle. Vous pouvez utiliser ces contrôles d’accès pour appliquer les politiques de gouvernance des données, limiter l’exposition des informations sensibles et aligner l’accès sur les responsabilités des utilisateurs et utilisatrices.

Pour plus d’informations sur le contrôle d’accès dans la composition d’audiences fédérées, lisez le [guide d’accès à la composition d’audiences fédérées](/help/start/feature-access.md){target="_blank"}.

## Localisation des données {#data-localization}

La composition d’audiences fédérées ne stocke **pas** de données clientèle. Par conséquent, vous devez vous assurer que vous connectez **uniquement** vos bases de données externes à la région de sandbox correspondante pour conserver vos données dans la même région. Si vous connectez la base de données d’une autre région à un sandbox, Adobe n’est **pas** responsable de la localisation des données.

## Étapes suivantes {#next-steps}

Après avoir lu ce guide, vous devez avoir toutes les clés pour mieux comprendre les fonctionnalités de confidentialité et de sécurité utilisées pour la composition d’audiences fédérées, notamment la gouvernance des données, la conformité en matière de confidentialité, l’application du consentement, la gestion du cycle de vie des données et le contrôle d’accès.
