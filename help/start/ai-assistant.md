---
title: Vue d’ensemble d’assistant IA
description: Découvrez comment utiliser l’assistant IA, notamment sa connaissance des produits, ses informations opérationnelles et la création de compositions d’audiences fédérées.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
TQID: https://experienceleague.adobe.com/j-KXucjaZa4dNSjg5POqxh7KOSUHG5CnBkBLFA6rPVs
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fda4d9d7b45833d7e080ae80f42b7ca5ce36b3ad
workflow-type: ht
source-wordcount: 651
ht-degree: 100%

---

# Vue d’ensemble de l’Assistant IA {#ai-assistant}

L’Assistant IA est une fonctionnalité de l’interface d’utilisation conçue pour vous aider à parcourir et à comprendre les concepts d’Adobe. Vous pouvez utiliser l’Assistant IA pour les cas d’utilisation liés à la connaissances des produits dans plusieurs produits Adobe Experience Cloud, notamment la composition d’audiences fédérées.

>[!CAUTION]
>
>Avant de pouvoir utiliser l’assistant IA, vous devez accepter les directives d’utilisation de l’IA générative d’Adobe Experience Cloud. Apprenez-en davantage sur le contrat dans la [vue d’ensemble de l’Assistant IA (hérité)](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home){target="_blank"}.

Dans la composition d’audiences fédérées, vous pouvez accéder à la connaissance des produits pour découvrir les concepts d’Adobe liés à divers aspects du processus. L’assistant IA prend en charge quatre types d’utilisation : **Découverte ouverte** (explorez les concepts de produit à partir de la documentation d’Experience League), **Apprentissage et dépannage ciblés** (posez des questions sur des fonctionnalités ou caractéristiques spécifiques), **Informations opérationnelles** (posez des questions sur vos objets dans la composition d’audiences fédérées) et **Création de compositions d’audiences fédérées**.

## Accès {#access}

Accédez à l’assistant IA en sélectionnant ![the AI Assistant icon](/help/start/assets/ai-assistant/icon.png) dans la barre supérieure. L’’ssistant IA s’affiche dans la partie droite de l’écran. Vous pouvez sélectionner ](assets/do-not-localize/Smock_FullScreen_18_N.svg "Dive image alt text ![the Expand icon") pour développer la fenêtre de l’assistant IA.

![L’icône de l’assistant AI est mise en surbrillance et indique comment accéder à l’assistant AI.](/help/start/assets/ai-assistant/access.png)

## Utilisation de l’assistant IA {#using}

Une fois l’assistant IA ouvert, saisissez votre question dans le champ en bas de l’écran et appuyez sur Entrée. La réponse à votre question s’affiche maintenant. Vous pouvez utiliser les pouces vers le haut ou vers le bas pour évaluer votre réponse.

![Un exemple de question et de réponse dans l’assistant AI s’affiche.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Exemples de questions {#sample-questions}

Les requêtes suivantes indiquent les types de questions que vous pouvez poser à l’assistant AI :

| Type de requête | Exemple de question |
| ---------- | --------------- |
| Découverte ouverte | <ul><li>Qu’est-ce que la composition d’audiences fédérées ?</li></ul> |
| Apprentissage ciblé | <ul><li>Comment configurer un compte de base de données fédérée Snowflake ?</li><li>Comment créer une composition fédérée ?</li></ul> |
| Informations opérationnelles | <ul><li>Combien de bases de données fédérées ai-je dans mon sandbox ?</li><li>Combien de schémas ai-je créés au cours des 30 derniers jours ?</li></ul> |
| Création d’une composition d’audiences fédérées | <ul><li>Créez une audience fédérée de clients résidant au Royaume-Uni.</li></ul> |

De plus, vous pouvez utiliser l’assistant IA pour créer de manière autonome une composition d’audiences fédérées.

## Créer une audience {#create-audience}

Vous pouvez utiliser l’assistant IA pour créer une composition d’audiences fédérées à l’aide de prompts en langage naturel. Lorsque vous utilisez l’assistant IA pour créer une audience, l’assistant IA crée un plan basé sur votre prompt et l’exécute dans votre navigateur à l’aide de l’automatisation optimisée par l’IA.

Par exemple, si vous demandez à l’assistant IA de « créer une audience fédérée de clients résidant au Royaume-Uni à l’aide du schéma CUSTOMERS_Table », l’assistant IA exposera le plan qu’il entreprendra pour créer l’audience, y compris les étapes telles que la navigation vers la page des compositions fédérées, la manière dont l’agent créera la composition et l’enregistrement de l’audience une fois celle-ci terminée.

![Un exemple de question et de réponse s’affiche.](/help/start/assets/ai-assistant/ask-create.png)

Si le plan semble précis, vous pouvez sélectionner **[!UICONTROL Exécuter]** pour que l’agent lance son processus d’automatisation.L’agent, dans le navigateur, passe de manière autonome par les étapes de création de la composition demandée dans l’interface utilisateur de composition d’audiences fédérées. Si, à tout moment, vous souhaitez arrêter l’automatisation, sélectionnez **[!UICONTROL Arrêter]**.

![Le plan a été exécuté et l’agent l’exécute de manière autonome.](/help/start/assets/ai-assistant/execute-plan.png)

Actuellement, la compétence de création d’audience prend en charge les fonctionnalités supplémentaires suivantes :

- Planificateur
   - Vous pouvez créer des compositions fédérées qui s’exécutent selon un planning récurrent.Les valeurs acceptées comprennent **Une fois** et **Au quotidien**.
- Déduplication
   - Vous pouvez dédupliquer les enregistrements de données fédérées lors de la réconciliation des données.

## Étapes suivantes

Pour plus d’informations sur l’assistant IA, notamment sur les exemples d’objectifs que vous pouvez atteindre avec l’assistant IA et sur son fonctionnement, consultez la [vue d’ensemble de l’assistant IA](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home){target="_blank"}.

Pour obtenir la liste complète des questions relatives aux informations opérationnelles que vous pouvez poser sur la composition d’audiences fédérées, lisez la section [Informations opérationnelles](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
