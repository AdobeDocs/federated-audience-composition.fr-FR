---
title: Présentation de l’assistant AI
description: Découvrez comment utiliser l’assistant d’IA, notamment sa connaissance des produits, ses informations opérationnelles et la création de compositions d’audiences fédérées.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
source-git-commit: 226679a38d0ad17726fd743f5df3b74879a2dd32
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 16%

---

# Vue d’ensemble de l’Assistant IA {#ai-assistant}

L’Assistant IA est une fonctionnalité de l’interface d’utilisation conçue pour vous aider à parcourir et à comprendre les concepts d’Adobe. Vous pouvez utiliser l’assistant d’IA pour mieux comprendre les cas d’utilisation de la connaissance des produits dans plusieurs produits de Adobe Experience Cloud, y compris la composition des audiences fédérées.

>[!CAUTION]
>
>Avant de pouvoir utiliser l’assistant IA, vous devez accepter les directives d’utilisation de l’IA générative d’Adobe Experience Cloud. Apprenez-en davantage sur le contrat dans la présentation de l’[assistant AI (hérité)](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home){target="_blank"}.

Dans la composition d’audiences fédérées, vous pouvez accéder à la connaissance des produits pour découvrir les concepts d’Adobe liés à divers aspects du processus. L’assistant AI prend en charge quatre types d’utilisation : **découverte ouverte** (explorez les concepts de produit à partir de la documentation d’Experience League), **apprentissage et dépannage ciblés** (posez des questions sur des fonctionnalités ou caractéristiques spécifiques), **informations opérationnelles** (posez des questions sur vos objets dans la composition d’audiences fédérées) et **création de compositions d’audiences fédérées**.

## Accès {#access}

Pour accéder à l’assistant AI, sélectionnez ![icône de l’assistant AI](/help/start/assets/ai-assistant/icon.png) dans la barre supérieure. L’’ssistant IA s’affiche dans la partie droite de l’écran. Vous pouvez sélectionner ![Texte secondaire de l’image de plongée](assets/do-not-localize/Smock_FullScreen_18_N.svg "icône Développer") pour développer la fenêtre de l’assistant AI.

![L’icône de l’assistant AI est mise en surbrillance et indique comment accéder à l’assistant AI.](/help/start/assets/ai-assistant/access.png)

## Utilisation de l’assistant AI {#using}

Une fois que vous avez ouvert l’assistant AI, saisissez votre question dans le champ en bas de l’écran, puis appuyez sur Entrée. La réponse à votre question s’affiche maintenant. Vous pouvez utiliser les pouces vers le haut ou vers le bas pour évaluer votre réponse.

![Un exemple de question et de réponse dans l’assistant AI s’affiche.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Exemples de questions {#sample-questions}

Les requêtes suivantes indiquent les types de questions que vous pouvez poser à l’assistant AI :

| Type de requête | Exemple de question |
| ---------- | --------------- |
| Ouvrir la découverte | <ul><li>Qu’est-ce que la composition d’audiences fédérées ?</li></ul> |
| Apprentissage ciblé | <ul><li>Comment configurer un compte de base de données fédérée Snowflake ?</li><li>Comment créer une composition fédérée ?</li></ul> |
| Informations opérationnelles | <ul><li>Combien de bases de données fédérées ai-je dans mon sandbox ?</li><li>Combien de schémas ai-je créés au cours des 30 derniers jours ?</li></ul> |
| Création d’une composition d’audience fédérée | <ul><li>Créez une audience fédérée de clients résidant au Royaume-Uni.</li></ul> |

De plus, vous pouvez utiliser l’assistant d’IA pour créer de manière autonome une composition d’audience fédérée.

## Créer une audience {#create-audience}

Vous pouvez utiliser l’assistant d’IA pour créer une composition d’audience fédérée à l’aide d’invites en langage naturel. Lorsque vous utilisez l’assistant AI pour créer une audience, l’assistant AI crée un plan basé sur votre invite et l’exécute dans votre navigateur à l’aide de l’automatisation optimisée par l’IA.

Par exemple, si vous demandez à l’assistant AI de « créer une audience fédérée de clients résidant au Royaume-Uni à l’aide du schéma CUSTOMERS_Table », l’assistant AI exposera le plan qu’il entreprendra pour créer l’audience, y compris les étapes telles que la navigation vers la page des compositions fédérées, la manière dont l’agent créera la composition et l’enregistrement de l’audience une fois celle-ci terminée.

![Un exemple de question et de réponse s’affiche.](/help/start/assets/ai-assistant/ask-create.png)

Si le plan semble précis, vous pouvez sélectionner **[!UICONTROL Exécuter]** pour laisser l’agent passer par son automatisation. L’agent, dans le navigateur , passe de manière autonome par les étapes de création de la composition demandée dans l’interface utilisateur de composition d’audience fédérée. Si, à tout moment, vous souhaitez arrêter l’automatisation, sélectionnez **[!UICONTROL Arrêter]**.

![Le plan a été exécuté et l’agent l’exécute de manière autonome.](/help/start/assets/ai-assistant/execute-plan.png)

Actuellement, la compétence de création d’audience prend en charge les fonctionnalités supplémentaires suivantes :

- Planificateur
   - Vous pouvez créer des compositions fédérées qui s’exécutent selon un planning récurrent. Les valeurs prises en charge sont les suivantes : **Une fois** et **Quotidien**.
- Déduplication
   - Vous pouvez dédupliquer les enregistrements de données fédérées lors de la réconciliation des données

## Étapes suivantes

Pour plus d’informations sur l’assistant AI, notamment sur les exemples d’objectifs que vous pouvez atteindre avec l’assistant AI et sur le fonctionnement de l’assistant AI, consultez la [présentation de l’assistant AI](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home){target="_blank"}.

Pour obtenir la liste complète des questions opérationnelles d’Insight que vous pouvez poser sur la composition des audiences fédérées, lisez la section [informations opérationnelles](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
