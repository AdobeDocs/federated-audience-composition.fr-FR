---
source-git-commit: d8ce0aecffcf6b85aa6c41e2520efbf564806098
workflow-type: tm+mt
source-wordcount: '2814'
ht-degree: 2%
---
# Documentation de Adobe Experience Platform : instructions de copilote

Ce référentiel (`experience-platform.en`) est la documentation publique de Adobe Experience Platform.
Chaque élément de contenu que vous rédigez, modifiez ou révisez DOIT suivre les règles ci-dessous.

## Ne pas limiter ou recadrer les requêtes

Répondez à la demande qui a été faite, pas à une petite demande. Ne pas redéfinir une demande
aussi petit qu’il était et ne remettez pas une tâche partielle décrite comme terminée.
Chaque ligne de ce référentiel peut être corrigée, quels que soient l’auteur, le contenu écrit ou le moment : « préexistant ».
« ne fait pas partie de cette différence » et « hors de portée » ne sont pas des raisons de laisser une violation non corrigée.
Lorsque vous êtes invité à corriger les violations, corrigez-les toutes, quel que soit leur âge. Si quelque chose bloque vraiment
le travail, dites exactement ce qui est annulé et ce qui l’est, et arrêtez.

## &#x200B;1. Voix, tonalité et style

### Écriture axée sur l’utilisateur

Centrez l’utilisateur et non la fonction. Écrivez ce que l’utilisateur ou l’utilisatrice peut **faire**, et non ce que la fonction fait.

- Utiliser la deuxième personne (« vous ») et l&#39;humeur impérative pour les instructions.
- Utilisez « vous » lorsque vous parlez d’eux-mêmes à l’audience, et non « les utilisateurs ». « Utilisateurs » est
acceptable lorsqu’il fait référence à un rôle (par exemple, un administrateur gérant des utilisateurs).
- Évitez les options « La fonction X vous permet de... » ou « La fonction X vous permet de... ». Définissez l’utilisateur comme
le sujet ou l&#39;utilisation d&#39;humeur impérative.
  - Mauvais : « L’API du serveur peut être utilisée sur les serveurs ». Méthode acceptable : « Utiliser l’API du serveur sur les serveurs ».
  - Mauvais : « Les champs calculés permettent de créer des valeurs... » Bon : « Utilisez des champs calculés.
    pour créer des valeurs... »
- Surveillez si « vous pouvez » est surutilisé. C&#39;est bien, mais cela peut créer des phrases répétitives ou verbeuses.
- Utilisez « select » pour choisir des options dans une liste ou mettre le texte en surbrillance. Utilisez « click » uniquement pour
actions explicites de la souris. Évitez de nommer le type de contrôle (bouton, lien), sauf si nécessaire pour
désambiguïsation.
- Utilisez « Ouvrir » / « Fermer » pour les applications et les fenêtres ou panneaux principaux.
- Utilisez « Quitter » pour quitter un site ou une expérience (par exemple, « Quitter Report Builder »).
- Utilisez « accéder à » ou « accéder à » pour la navigation.
- Utilisez « Lire la vidéo » et non « Regarder la vidéo ».
- Utilisez « Afficher », « Afficher » ou « Tout afficher », et non « Tout voir ».
- Utilisez « connexion » / « déconnexion », et non « connexion » / « déconnexion ».
- Évitez d’utiliser « afin de ». Utilisez « to » à la place.
- Évitez « utiliser ». Utilisez plutôt « use ».
- Évitez les adjectifs vagues tels que « rapide » ou « facile ». Soyez précis : « Ce processus prend généralement
5 minutes. »
- Évitez les adverbes faibles : très, extrêmement, incroyablement.

### Structure de phrase et de paragraphe

- Cible 20 mots ou moins par phrase (35 max.). Une pensée par phrase.
- Paragraphes : 125 mots maximum, idéalement 100 ou moins. 4 à 5 phrases maximum. Pas de murs de texte.
- Utilisez une voix active. Évitez les constructions passives et les nominalisations (par exemple, « créer », non
« création »).
- Utilisez une structure objet-verbe-objet simple.
- Evitez les faux sujets (« C&#39;est... », « Il y a... »).
- Utilisez le même mot de manière cohérente. Ne faites pas pivoter les synonymes.
- Pas d&#39;humour, d&#39;argot, de jargon, ou d&#39;exemples spécifiques à la culture (doit bien se localiser).
- Utilisez la virgule Oxford dans les listes de trois éléments ou plus.
- Écrivez les nombres entiers de zéro à neuf ; utilisez les chiffres de 10 et plus.
- Pas de point-virgule. Utilisez plutôt un point et une nouvelle phrase.
- N’utilisez PAS de tirets EM, de tirets en fin ou de tirets en prose. Reformuler à la place. Les tirets sont
autorisé uniquement dans les adjectifs composés qui apparaissent dans l’interface utilisateur, les noms de fichier et le code.
- N’utilisez PAS de règles horizontales (`---` ou `***`). Elles ne sont pas prises en charge dans Experience League.

### Scannabilité

- Les lecteurs doivent saisir la portée de l’article uniquement à partir du titre, des en-têtes et des légendes.
- 2 à 5 sous-sections maximum par section.
- Cible 7 étapes par tâche ; 10 est le maximum pratique. Diviser les procédures plus longues en sous-tâches.
- 8 éléments maximum par liste à puces.
- Utilisez des tableaux lorsqu’ils facilitent l’analyse des listes de termes/définitions.
- Le contenu doit avoir un score inférieur à 10 lors d’un test de lisibilité (après avoir supprimé les noms appropriés).
et titres).

### Écriture pour la découverte de l’IA

- Insérez des termes clés (noms de produits, noms de fonctionnalités, tâches) dans le corps du texte et le texte du lien, et pas seulement
dans les images ou les tableaux complexes.
- Écrivez des en-têtes et des premiers paragraphes clairs et autonomes.
- Faites des phrases courtes et directes.
- Utilisez des formats structurés (étapes numérotées, puces courtes, en-têtes de style définition) pour
procédures et comparaisons.
- Incluez des synonymes ou d’autres termes lors de la première utilisation (par exemple, « ECID (Experience Cloud ID) »).
- Veillez à ce que les champs de métadonnées (titre, description, balises de fonctionnalité) soient complets et précis.

## &#x200B;2. Balises de localisation (toujours applicables)

La traduction automatique s’exécute automatiquement à chaque validation dans la version principale.

### `[!DNL Product Name]` : Ne Pas Localiser

Appliquer aux noms de produits Adobe (`[!DNL Analytics]`, `[!DNL Target]`, `[!DNL Campaign]`,
`[!DNL Experience Platform]`), noms de produits tiers (`[!DNL Mozilla Firefox]`,
`[!DNL Workfront]`), des noms fonctionnels qui peuvent prêter à confusion (`[!DNL Pass]`,
`[!DNL Campaign]`) et des opérateurs booléens utilisés comme termes logiques (`[!DNL AND]`, `[!DNL OR]`).

NE pas appliquer aux URL, noms de fichiers, noms de répertoires, blocs de code, acronymes ou termes déjà utilisés
dans la base de données Ne pas traduire .

Dans le texte du lien, supprimez les crochets de balise : `[Adobe](https://www.adobe.com)`, pas
`[[!DNL Adobe]](https://www.adobe.com)`.

### `[!UICONTROL Label]` : contrôles de l’interface utilisateur

Obligatoire sur chaque élément d’interface utilisateur cliquable dans les étapes de procédure et sur les noms de fonctionnalité,
éléments de navigation, noms de page, options, champs et onglets, comme indiqué dans l’interface.

- Gras dans les étapes et la navigation : `Select **[!UICONTROL Destinations]** from the left navigation.`
- Italique acceptable dans le texte conceptuel (sans étape) pour plus de clarté.
- Dans les tableaux HTML : utilisez `<span class="uicontrol">term</span>` au lieu de ``.
- Dans le texte du lien : supprimez les crochets de balise.
- La majuscule doit correspondre exactement à l’interface.
- Ne s’applique PAS aux termes génériques utilisés de manière conceptuelle (« segment », « mesure », « campagne »), sauf
faisant référence à l’élément d’interface utilisateur, de longues phrases, des blocs de code, des acronymes ou des descriptions d’icône
(utilisez le nom du pointeur/de l’info-bulle de l’icône, le cas échéant).

### `[!DONOTLOCALIZE]` : exclure des sections entières

```markdown
>[!DONOTLOCALIZE]
>
>Content that must not be translated.
```

Inutile dans les blocs de code ; ils ne sont pas localisés par défaut.

### Où les balises peuvent et ne peuvent pas être utilisées

- Peut être utilisé dans : paragraphes, listes, titres, tableaux, badges, texte secondaire et métadonnées.
- Ne peut pas être utilisé dans : blocs de code, acronymes.
- Si un champ de métadonnées commence par une balise `[!DNL]` ou ``, placez l’ensemble du champ entre crochets
La valeur entre guillemets ou la validation échoue.

## &#x200B;3. Terminologie et valorisation de marque

### Noms de produits

Utilisez toujours ces formulaires exacts. Inclure « Adobe » à la première référence dans un guide. NE PAS précéder
les noms de produits comportant le caractère « », sauf si le nom officiel l’inclut.

| Correct | NE JAMAIS utiliser |
|---|---|
| Adobe Experience Platform | AEP, AXP, Adobe XP, Adobe Cloud Platform |
| Experience Platform (référence secondaire) | Platform (seule, sauf si le contexte est sans ambiguïté) |
| Adobe Real-Time CDP | RTCDP, ARTCDP |
| Real-Time CDP (secondaire) | Real-Time CDP (en minuscules « t ») |
| Adobe Real-Time Customer Data Platform | — |
| Profil client en temps réel | Profil client en temps réel, profil unifié |
| Adobe Journey Optimizer | AJO |
| Adobe Customer Journey Analytics | CJA |
| Customer Journey Analytics (secondaire) | — |
| Adobe Real-Time CDP Collaboration | RTCDP Collaboration, RTCDP Collab, Collab |
| Connexions Adobe Real-Time CDP | Connexions RTCDP, Connexions AEP, Connexions (seules) |
| Adobe Experience Platform Edge Network | Platform Edge Network, Platform Edge, Adobe Experience Edge |
| Balises (nom du produit) | Launch (obsolète) |
| Gestion des décisions | Offer Decisioning (entre parenthèses uniquement : « anciennement Offer Decisioning ») |
| flux de données (un mot, en minuscules) | flux de données, configuration edge |
| Analysis Workspace | analysis workspace, workspace, Workspace |
| Adobe AI | Sensei (obsolète) |
| Adobe GenAI | — |
| Adobe GenStudio for Performance Marketing | — |

- « Real-Time » utilise toujours R majuscule et T majuscule lorsqu’ils font partie d’un nom de produit.
- « Editions » est en minuscules de manière générique ; « Edition » est mis en majuscules dans le cadre d’une édition de produit
nom (par exemple, « Adobe Real-Time CDP B2C Edition »).
- N’abrégez PAS les noms de produits dans la documentation destinée aux utilisateurs (pas d’AEP, CJA, AJO, RTCDP).
Exceptions limitées : les acronymes peuvent apparaître entre parenthèses lors de la première utilisation pour l’optimisation pour les moteurs de recherche ou dans la table des matières
entrées, métadonnées de description et en-têtes pour lesquels la longueur pose problème.
- Majuscules dans Analytics : les noms des panneaux sont en minuscules (vide, attribution, expérimentation,
Structure libre ; exception : « Zone de travail de Parcours »). Les noms des visualisations sont en minuscules (barre, anneau,
histogramme, ligne, arborescence, texte).

### Terminologie des fonctionnalités et des concepts

| Correct | NE PAS utiliser |
|---|---|
| transfert d’événement | transfert côté serveur, Launch côté serveur |
| placer sur la liste autorisée | whitelist |
| PLACE SUR LA LISTE BLOQUÉE / | mettre sur liste noire |
| principal/réplica OU principal/secondaire (serveurs) | maître/esclave |
| principal (branche GitHub) | master |
| pirate éthique | pirate à chapeau blanc |
| remarketing | reciblage |
| groupe de champs | mixin (obsolète), extensions, mixins |
| expiration automatique des données | TTL, durée de vie, expiration |
| sandbox hors production | évaluation (comme nom d’environnement) |
| définition de segment | segment (seul, au sens de la définition) |
| ID (toujours en majuscules) | Id |
| ingestion / ingérer / ingérer | intégration (pour ajouter des données à Platform) |
| jeu de données / jeux de données | Fichier de données, fichiers de jeux de données |
| contrôle d’accès | autorisations (pour la fonctionnalité Platform) ; |
| widget | carte de mesures (obsolète) |
| variable d’espace réservé | variable factice |
| indisponible/verrouillé/désactivé/désactivé | grisé |
| contrôle de cohérence | contrôle de santé mentale |
| intégré | natif (comme synonyme de natif) |
| priorité élevée | clouer |
| hérité | clause de droits acquis |
| principal/principal/source | maître (comme descripteur) |

### Termes internes uniquement : NE JAMAIS utiliser dans les documents publics

| Terme interne | Utiliser plutôt |
|---|---|
| AEP | Adobe Experience Platform |
| PALMIER | gestion des sandbox/contrôle d’accès |
| BIOME | environment |
| Hydrate / hydratation | créer/remplir |
| Profil unifié | Profil client en temps réel |
| Évaluation (environnement) | sandbox hors production |
| DTM | Balises |
| Locataire | Organisation/organisation IMS |
| CRUD | créer, lire, mettre à jour et supprimer (épeler) |
| Siphon, BSO, Ethos | noms de code internes, jamais externes |
| Houblon | RGPD interne/condition de contrôle d’accès |
| Fréquence | terme publicitaire non visible par l&#39;utilisateur |
| Pipeline | terme interne de l’infrastructure Adobe |

## &#x200B;4. Langue inclusive et accessibilité

### Principes linguistiques inclusifs

- Utilisez des termes non sexistes : « représentant commercial » et non « vendeur », « modérateur » et non « président ».
- Préférez la deuxième personne (« vous ») pour éviter les pronoms de genre.
- Utilisez le singulier « they » pour une personne dont le genre est inconnu. NE PAS l’utiliser.
- Incluez des noms de cultures non blanches dans des exemples (par exemple, Ayesha, Ibrahim, Vignesh, Quynh).
N&#39;utilisez PAS uniquement des noms culturellement blancs.
- NE PAS confondre le sexe (homme/femme) avec le sexe (homme/femme).
- Capitalisez les nationalités, les peuples, les races (autres que les « blancs », selon l’API Stylebook) et les tribus.
- Utilisez le langage « personne d’abord » : « personnes qui utilisent la technologie d’assistance », et non « personnes handicapées ».
- Évitez les euphémismes comme « incapables ». Évitez les descripteurs utilisés comme noms : « the store, »
« les sourds. »
- Évitez les termes qui reflètent l&#39;identité/l&#39;appropriation culturelle : animal spirituel, sherpa, pow-wow,
guru, ninja, tribu.

### Terminologie non exhaustive à éviter

| Utilisation | Not |
|---|---|
| / PLACER SUR LA LISTE AUTORISÉE / | liste blanche/liste noire |
| principal/réplica OU principal/secondaire | maître/esclave |
| principal (branche git) | master |
| priorité élevée | clouer |
| variable d’espace réservé | variable factice |
| indisponible/verrouillé/désactivé/désactivé | grisé |
| contrôle de cohérence | contrôle de santé mentale |
| intégré | natif (comme synonyme) |
| autorité / expert | guru / ninja |
| membres de votre groupe | membres de votre tribu |
| réunion | pow wow / encerclez les wagons |
| modèle / esprit de parenté | animal spiritueux |
| guide | Sherpa |
| hérité | clause de droits acquis |
| entreprise futile | marche de la mort |
| ridicule / incompétent / imprévisible | stupide / boiteux / fou |
| pirate éthique / non éthique | chapeau blanc / chapeau noir hacker |
| Lire la vidéo | Regarder la vidéo |
| Afficher / Afficher / Tout accéder | Tout voir |

### Accessibilité : description de l’interface utilisateur

Ne décrivez PAS les éléments de l’interface utilisateur par couleur ou position de l’écran. Utilisez chronologique, et non spatial,
langue :

| Utilisation | Not |
|---|---|
| D&#39;Abord, Ensuite, Enfin | Au-Dessus, En Dessous |
| Dans la barre de menus | À gauche |
| Avant / Après | En haut/en bas de l’écran |

Décrivez le rôle des commandes, et non leur apparence :

| Utilisation | Not |
|---|---|
| Sélectionner une recherche | Cliquez sur l’icône de loupe |
| Modifier | L’icône en forme de crayon |
| Activé/Désactivé | Basculer / basculer / activer |
| Menu | Tiroir latéral |
| Saisir l’adresse e-mail | Saisissez votre adresse e-mail |
| Enregistrer | Le bouton « Enregistrer » |
| Annuler | Fermer |

N’utilisez PAS uniquement la couleur pour véhiculer l’information. Associez toujours la couleur au texte ou à la forme.

### Accessibilité : texte secondaire, liens et vidéos

- **Texte secondaire** : décrivez ce que l’image montre, pas seulement son nom d’écran. Utilisation terminée
phrases, mots complets (les lecteurs d’écran épellent des abréviations) et incluent le texte approprié
à partir de l’image. Les images qui véhiculent des informations indépendantes du texte environnant DOIVENT comporter
texte secondaire.
- **Liens** : n’utilisez jamais « cliquer ici » ou « lien » comme texte du lien. Effacer la destination de
le texte du lien seul.
- **Vidéos** : ne doit PAS être lu automatiquement. Fournissez toujours un texte secondaire, une transcription ou un lien vers
des instructions écrites. Incluez des légendes significatives.

## &#x200B;5. Principes fondamentaux de la syntaxe Markdown

### FrontMATTER (obligatoire sur chaque fichier)

```yaml
---
title: Title Case Title Here
description: Learn how to... or Learn about... (150-160 chars, sentence case).
---
```

- N’ajoutez PAS de `exl-id` lors de la création d’une page. Il est généré automatiquement lors de la publication
l&#39;heure. Ne conservez que `exl-id` champs qui existent déjà sur les pages existantes.
- Titre : casse du titre, 60 caractères max., pas de barre verticale ni de nom de produit (ajouté automatiquement).
Les titres de concept sont des groupes nominaux ; les titres de tâche sont des groupes verbaux.
- Description : casse de phrase, 150 à 160 caractères. La première phrase résume ; la deuxième est une
call to action. Ne commencez PAS par le nom du produit et ne copiez PAS le premier paragraphe mot.

### Titres

- `#` = H1 (un par page, première ligne après le front). `##`, `###` pour les sous-sections. Jamais
ignorer les niveaux.
- Cible de 5 mots ou moins, 69 caractères max. Ligne vide avant et après chaque en-tête.
- Chaque en-tête doit être suivi du corps du texte ; ne superposez jamais les en-têtes ni ne placez de liste/tableau/note
directement sous un titre.
- Cas de condamnation. Les en-têtes de concept sont des substantifs ; les en-têtes de tâche sont des verbes impératifs
(évitez les rebonds).
- Pas de titres abstraits avec un seul mot (« Présentation », « Introduction ») sans décrire le sujet.
- Identifiants d’ancre personnalisée : `## Section title {#section-id}` (minuscules, avec traits d’union).

### Liens, images et code

- Les références croisées internes utilisent des chemins relatifs à la racine : `[text](/help/path/to/file.md)`.
Les liens externes utilisent des URL de `https://` absolue.
- N’utilisez jamais « cliquer ici » ou « lien » comme texte du lien. Évitez les URL brutes dans le corps du texte.
- Texte de remplacement : `![alt text](path/to/image.png)`. Phrases complètes, pas de début « Cette image montre... ».
- Captures d’écran : thème léger uniquement, aucune donnée client, aucune interface utilisateur tierce, aucune image de code.
- Les blocs de code clôturés utilisent des accents graves triples avec un identifiant de langue. Les blocs de code ne sont pas
localisé (aucun DNL/UICONTROL nécessaire à l&#39;intérieur).
- Vidéos : `>[!VIDEO](url?quality=12&learn=on)`. Ne jamais lire automatiquement ; toujours fournir une transcription
ou une alternative écrite.

### Admonitions

```markdown
>[!NOTE]
>
>Note content here.
```

Une ligne de `>` vide doit séparer la ligne de balise du contenu ; chaque ligne de suite commence
avec `>`. NE PAS placer un `[!NOTE]` immédiatement après un bloc de `[!CONTEXTUALHELP]`.

### Fenêtres contextuelles d’aide (`[!CONTEXTUALHELP]`)

`[!CONTEXTUALHELP]` bloque les infobulles contextuelles de flux que l’ingénierie lie à l’expérience
Interface utilisateur de Platform. Ils se trouvent dans la documentation mais s’affichent sous forme de fenêtres contextuelles intégrées au produit via un flux JSON
générée au moment de la création.

```markdown
## Configure file names {#configure-file-names}

>[!CONTEXTUALHELP]
>id="platform_destinations_activate_filename"
>title="Configure file name"
>abstract="For file-based destinations, a unique file name is generated per segment. Use the file name editor to create and edit a unique file name or keep the default name."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations.html#file-names" text="Learn more in documentation"
```

Champs obligatoires : `id`, `title`, `abstract`. Tout le reste est facultatif.

**Emplacement:**
- Le bloc doit venir directement après un en-tête (`#`, `##` ou `###`) qui a un explicite
ID d’ancrage (par exemple, `### Section title {#section-id}`). Aucun paragraphe ou autre contenu entre
l’en-tête et le bloc, ou la fenêtre contextuelle ne s’affiche pas.
- Plusieurs blocs de `[!CONTEXTUALHELP]` peuvent apparaître consécutivement dans la même section (par exemple,
une par champ (en cours de documentation).
- NE PAS placer un bloc `[!NOTE]` immédiatement après un bloc `[!CONTEXTUALHELP]`. Ça casse
le rendu sur Experience League (limitation de plateforme connue).

Syntaxe de **ID:**
- Format : `id="platform_<yourarea>_<workflow>_<uiitem>"`, par ex.
  `id="platform_destinations_activate_deduplicationkey"`.
- Les identifiants peuvent contenir des majuscules.
- Les identifiants doivent être uniques pour l’ensemble du jeu de documents (vérifiés au moment de la création). Le même ID peut être réutilisé
à plusieurs emplacements d’interface utilisateur par ingénierie, ce qui produit un contenu contextuel identique dans
chaque endroit. C&#39;est prévu.

**Les liens dans une fenêtre contextuelle utilisent `additional-url`, et non HTML intégré :**
- Pour ajouter un lien, utilisez une ligne distincte : `>additional-url="URL" text="Link text"`. Ne PAS incorporer
  `<a href="...">` ou markdown `[text](url)` dans la chaîne `abstract` à cet effet.
- La valeur `additional-url` DOIT inclure `.html` dans le chemin d’accès ou le lien ne s’affichera pas dans
l’interface utilisateur (par exemple, `https://experienceleague.adobe.com/docs/experience-platform/path/to/page.html#anchor`,
pas le nouveau formulaire `/en/docs/...` sans extension utilisé dans les liens de corps de texte ailleurs).
- Maximum de deux lignes `additional-url` par bloc.
- Un premier lien est généré automatiquement à partir de l’en-tête de section lors de la création de Jenkins. Vous
n’ajoutez pas celui-ci manuellement et vous ne pouvez pas le renommer.

**Autre syntaxe prise en charge :**
- Le champ `abstract` prend en charge HTML/markdown de base pour l’accent et la structure : `<b>`,
  `<br>`, `<ul><li>`, `**bold**`.
- Les liens vidéo sont pris en charge par le même mécanisme `additional-url`/`text`, pointant vers une
URL de vidéo directe ou URL de YouTube.

**Remarque sur le workflow :** lors de la gestion d’un nouvel ID de fenêtre contextuelle à l’équipe d’interface utilisateur/d’ingénierie (généralement via une
un ticket Jira), fournissez également une URL de secours (préférez une goURL s’il en existe une pour cette page) et
l’emplacement de l’interface utilisateur. Cette solution de secours est distincte de la `additional-url` utilisée dans la documentation
markdown.

### Listes et tableaux

- Utilisez `*` ou `-` de manière cohérente dans un seul article ; ne le mélangez pas.
- Les listes numérotées utilisent des `1.` pour chaque élément. Les procédures en une seule étape utilisent une puce, pas `1.`.
- Pas de cases à cocher de liste de tâches de style GitHub (`- [ ]`) ; non pris en charge dans Experience League.
- Entourez les listes et les tableaux de lignes vides. Garder les éléments de liste grammaticalement parallèles.

### Dénomination des fichiers et des dossiers

- Noms de fichier Markdown : minuscules avec des tirets, pas de majuscules/traits de soulignement/points/espaces.
- Utilisez des slugs descriptifs (`create-calculated-metric.md`), pas des noms nus comme `overview.md`.
- Les images se trouvent dans un sous-dossier `assets/` ; les images qui ne doivent pas être localisées s’y trouvent
  `do-not-localize/`.

## &#x200B;6. Conventions de structure et de table des matières

- Trois types de contenu, séparés : **Concept** (quoi/pourquoi, noms), **Tâche**
(comment, en-têtes impératifs, toujours précédés d’un concept), **Référence** (champs,
paramètres, tableaux).
- Étapes : chacune d’elles est une seule phrase complète commençant par un verbe ou l’objectif. Cible 7
étapes par tâche, 10 au maximum ; diviser les procédures plus longues en sous-tâches.
- TOC.md : entrées de cas de phrase, ID d’ancrage valides sur chaque en-tête de section, pas de doublon
entrées de fichier, aucun commentaire de liste intermédiaire.
- Cacher une page de la navigation avec `{hide-from-toc}` dans `TOC.md` (pas frontMATTER). Masquer
depuis des moteurs de recherche avec `hide: true` dans frontend.
- Dénomination de la branche : aucun préfixe de nom d’utilisateur. Utilisez le numéro de ticket Jira et un titre avec une balise
(e.g., `PLAT-12345-Update-Guardrail-Limits`). Nommez la branche et le titre de la requête de tirage de la même manière.

## &#x200B;7. Orthographe et ponctuation

- Orthographe anglais américain : couleur, reconnaître, licence, tandis que, expiration, compteur, parmi
(pas de couleur, de reconnaissance, de licence, d’expiration, de compteur, etc.).
- Réservez des guillemets pour citer des personnes ; ne citez pas de chaînes d’interface utilisateur (utilisez gras +
  `` à la place).
- Utilisez l’italique pour les termes utilisés comme termes (*profil*, et non « profil »). Utilisez des accents graves pour le code,
paramètres, noms de fichiers et texte saisi.
- Gras uniquement pour les éléments de l’interface utilisateur dans les procédures (avec ``) et les termes clés au début
introduction.
- Pas de point-virgule, pas de tirets/traits d’union em/en dans la prose, pas de règles horizontales (voir section 1).

## &#x200B;8. Vérifier la liste de contrôle

Avant de terminer toute modification, vérifiez les points suivants :

- Voix axée sur l’utilisateur, voix active, deuxième personne, pas de « vous permet de »/« vous permet de »
- Phrases ≤20 mots, paragraphes ≤125 mots
- En-têtes : casse de phrase, ≤5 mots/69 caractères, suivi du corps du texte, aucun niveau ignoré
- Noms et formulaires de produits corrects ; aucun terme obsolète, interne uniquement ou non inclusif
- `` sur chaque élément de l’interface utilisateur par étapes ; `[!DNL]` sur chaque nom de produit/tiers.
- Aucune balise dans les blocs de code ; champs de métadonnées balisés placés entre guillemets
- Syntaxe de l&#39;avertissement correcte ; marqueurs de liste cohérents ; aucune liste de tâches ; aucune règle horizontale
- Le texte de remplacement est descriptif et complet ; pas de « clic ici » ; pas de langage spatial/directionnel
- Aucune couleur utilisée seule pour transmettre des informations ; les vidéos ne sont pas lues automatiquement
- FrontMatter requis présent ; liens internes relatifs à la racine ; noms de fichier avec traits d’union en minuscules
