---
audience: end-user
title: Vue d’ensemble de l’éditeur d’expression
description: Découvrez comment utiliser les fonctions de l’éditeur d’expression pour créer une requête dans le concepteur de requête.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: 93f4a16d00c71059672c4c6a51ff36debb6c9cee
workflow-type: ht
source-wordcount: '4108'
ht-degree: 100%

---

# Vue d’ensemble de l’éditeur d’expression {#expression}

La modification d’une expression consiste à saisir manuellement des conditions pour former une règle. Ce mode permet d’utiliser des fonctions avancées, vous permettant ainsi de manipuler les valeurs utilisées afin de réaliser des requêtes spécifiques : manipulation de dates, de chaînes, de champs numériques, tris, etc.

## Utiliser l’éditeur d’expression {#edit}

L’éditeur d’expression est disponible à partir du bouton **[!UICONTROL Modifier une expression]** du concepteur de requête, disponible pour les champs **[!UICONTROL Attribut]** et **[!UICONTROL Valeur]** lors de la configuration d’une condition personnalisée.

| Accéder depuis le champ **[!UICONTROL Attribut]** | Accéder depuis le champ **[!UICONTROL Valeur]** |
|  ---  |  ---  |
| ![](assets/expression-editor-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/edit-expression.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

L’éditeur d’expression fournit :

* un **champ de saisie (1)**, dans lequel l’expression est définie ;
* la liste des **champs (2)** disponibles, utilisables dans l’expression et correspondant au schéma, ou dimension de ciblage, de la requête ;
* des **fonctions d’assistance (3)**, triées par catégorie.

Modifiez l’expression en saisissant une expression directement dans le champ de saisie. Pour ajouter un champ ou une fonction d’assistance, placez le curseur dans l’expression à l’endroit où vous souhaitez l’ajouter, puis sélectionnez le bouton +.

![](assets/expression-editor.png){zoomable="yes"}

Lorsque votre expression est prête, sélectionnez **[!UICONTROL Confirmer]**. L’expression s’affiche dans le champ sélectionné. Pour la modifier, ouvrez l’éditeur d’expression et apportez les modifications souhaitées.

L’exemple ci-dessous présente une expression configurée pour le champ **[!UICONTROL Valeur]**. Pour la modifier, vous devez ouvrir l’éditeur d’expression à l’aide du bouton **[!UICONTROL Modifier une expression]**.

![](assets/edit-expression-value.png){zoomable="yes"}

## Fonctions d’assistance

L’outil d’édition de requêtes permet d’utiliser des fonctions avancées pour réaliser un filtrage complexe en fonction des résultats souhaités et des types de données manipulées. Les fonctions suivantes sont disponibles :

<!-- ### Aggregate

The aggregate functions are used to perform calculations on a set of values.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StdDev** | Returns the standard deviation of the values given. | StdDev(&lt;VALUE&gt;) | StdDev([0,3,5]) | -->

<!-- 

>[!TAB Databricks]

Aggregate functions are not available.

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") |

>[!TAB Redshift]

Aggregate functions are not available. -->

<!-- 

>[!TAB Snowflake]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") | -->

<!-- 
>[!TAB Vertica]

Aggregate functions are not available. -->

<!-- 
>[!ENDTABS] 
-->

### Date

Les fonctions de date sont utilisées pour manipuler des valeurs de date ou d’heure.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Ajoute le nombre d’années spécifié à la date et à l’heure indiquées. | AddYears(&lt;DATEHEURE>, &lt;NOMBRE>) | AddYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMonths** | Ajoute le nombre de mois spécifié à la date et à l’heure indiquées. | AddMonths(&lt;DATEHEURE>, &lt;NOMBRE>) | AddMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **AddDays** | Ajoute le nombre de jours spécifié à la date et à l’heure indiquées. | AddDays(&lt;DATEHEURE>, &lt;NOMBRE>) | AddDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **AddHours** | Ajoute le nombre d’heures spécifié à la date et à l’heure indiquées. | AddHours(&lt;DATEHEURE>, &lt;NOMBRE>) | AddHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMinutes** | Ajoute le nombre de minutes spécifié à la date et à l’heure indiquées. | AddMinutes(&lt;DATEHEURE>, &lt;NOMBRE>) | AddMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **AddSeconds** | Ajoute le nombre de secondes spécifié à la date et à l’heure indiquées. | AddSeconds(&lt;DATEHEURE>, &lt;NOMBRE>) | AddSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **SubYears** | Soustrait le nombre d’années spécifié à la date et à l’heure indiquées. | SubYears(&lt;DATEHEURE>, &lt;NOMBRE>) | SubYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMonths** | Soustrait le nombre de mois spécifié à la date et à l’heure indiquées. | SubMonths(&lt;DATEHEURE>, &lt;NOMBRE>) | SubMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **SubDays** | Soustrait le nombre de jours spécifié à la date et à l’heure indiquées. | SubDays(&lt;DATEHEURE>, &lt;NOMBRE>) | SubDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **SubHours** | Soustrait le nombre d’heures spécifié à la date et à l’heure indiquées. | SubHours(&lt;DATEHEURE>, &lt;NOMBRE>) | SubHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMinutes** | Soustrait le nombre de minutes spécifié à la date et à l’heure indiquées. | SubMinutes(&lt;DATEHEURE>, &lt;NOMBRE>) | SubMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **SubSeconds** | Soustrait le nombre de secondes spécifié à la date et à l’heure indiquées. | SubSeconds(&lt;DATEHEURE>, &lt;NOMBRE>) | SubSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **Year** | Extrait l’année de l’objet date/heure donné. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Month** | Extrait le mois de l’objet date/heure donné. | Month(&lt;DATEHEURE>) | Month(&quot;2019-12-15 15:30:00&quot;) |
| **Jour** | Extrait le jour de l’objet date/heure donné. | Day(&lt;DATEHEURE>) | Day(&quot;2019-12-15 15:30:00&quot;) |
| **DayOfYear** | Extrait le jour de l’année de l’objet date/heure donné. Par exemple, si la date et l’heure indiquées sont le 2 février, la valeur 33 est renvoyée. | DayOfYear(&lt;DATEHEURE>) | DayOfYear(&quot;2019-12-15 15:30:00&quot;) |
| **WeekDay** | Extrait le jour de la semaine de l’objet date/heure donné, sous la forme d’un nombre compris entre 0 et 6, avec 0 représentant le dimanche. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Hour** | Extrait la valeur de l’heure de l’objet date/heure donné. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Minute** | Extrait la valeur de minute de l’objet date/heure donné. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Second** | Extrait la valeur de seconde de l’objet date/heure donné. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **YearsDiff** | Trouve la différence entre les dates et heures données, avec une granularité en années. | YearsDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | YearsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsDiff** | Trouve la différence entre les dates et heures données, avec une granularité en mois. | MonthsDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | MonthsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **DaysDiff** | Trouve la différence entre les dates et heures données, avec une granularité en jours. | DaysDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | DaysDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **HoursDiff** | Trouve la différence entre les dates et heures données, avec une granularité en heures. | HoursDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | HoursDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MinutesDiff** | Trouve la différence entre les dates et heures données, avec une granularité en minutes. | MinutesDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | MinutesDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **SecondsDiff** | Trouve la différence entre les dates et heures données, avec une granularité en secondes. | SecondsDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | SecondsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **YearsOld** | Trouve la différence entre la date et l’heure données et le moment présent, avec une granularité en années. | YearsOld(&lt;DATEHEURE>) | YearsOld(&quot;2019-12-25 15:30:00&quot;) |
| **MonthsOld** | Trouve la différence entre la date et l’heure données et le moment présent, avec une granularité en mois. | MonthsOld(&lt;DATEHEURE>) | MonthsOld(&quot;2019-12-25 15:30:00&quot;) |
| **DaysOld** | Trouve la différence entre la date et l’heure données et le moment présent, avec une granularité en jours. | DaysOld(&lt;DATEHEURE>) | DaysOld(&quot;2019-12-25 15:30:00&quot;) |
| **GetDate** | Obtient la date actuelle du serveur. | GetDate() | GetDate() |
| **DateOnly** | Tronque la date et l’heure pour ne conserver que l’année, le mois et le jour. | DateOnly(&lt;DATEHEURE>) | DateOnly(&quot;2019-12-25 15:30:00&quot;) |
| **ToDate** | Convertit le champ en champ de date. | ToDate(&lt;DATEHEURE>) | ToDate(&quot;2019-12-25 15:30:00&quot;) |
| **ToDateTime** | Convertit le champ en champ de date/heure. | ToDateTime(&lt;DATE>) | ToDateTime(&quot;2019-12-25 15:30:00&quot;) |
| **ToTimestamp** | Convertit le champ en champ d’horodatage. | ToTimestamp(&lt;DATEHEURE>) | ToTimestamp(&quot;2019-12-25 15:30:00&quot;) |
| **Oldest** | Renvoie la date la plus ancienne parmi les deux indiquées. | Oldest(&lt;DATEHEURE>, &lt;DATEHEURE>) | Oldest(&quot;2015-02-13 11:59:59&quot;, &quot;2016-04-13 19:28:14&quot;) |
| **TruncDate** | Tronque la date et l’heure à l’unité la plus proche, en fonction de la valeur numérique donnée. Si la valeur numérique est égale à 60, elle est tronquée à la minute la plus proche. Si la valeur numérique est égale à 3 600, elle est tronquée à l’heure la plus proche. Si la valeur numérique est égale à 86 400, elle est tronquée au jour le plus proche. Sinon, elle est tronquée à la seconde la plus proche. | TruncDate(&lt;DATEHEURE>, &lt;NOMBRE>) | TruncDate(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncDateTZ** | Tronque la date et l’heure à l’unité la plus proche, en fonction de la valeur numérique donnée, et définit la date et l’heure sur le fuseau horaire spécifié. Si la valeur numérique est égale à 60, elle est tronquée à la minute la plus proche. Si la valeur numérique est égale à 3 600, elle est tronquée à l’heure la plus proche. Si la valeur numérique est égale à 86 400, elle est tronquée au jour le plus proche. | TruncDateTZ(&lt;DATEHEURE>, &lt;NOMBRE>, &lt;FUSEAUHORAIRE>) | TruncDateTZ(&quot;2016-04-13 19:28:14&quot;, 3600, &quot;America/Los_Angeles&quot;) |
| **TruncTime** | Définit la date et l’heure sur le 1er janvier 2000 et arrondit le reste de la date et de l’heure à l’unité la plus proche, en fonction de la valeur numérique donnée. Si la valeur numérique est égale à 60, elle est tronquée à la minute la plus proche. Si la valeur numérique est égale à 3 600, elle est tronquée à l’heure la plus proche. | TruncTime(&lt;DATEHEURE>, &lt;NOMBRE>) | TruncTime(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncQuarter** | Tronque la date et l’heure à la première date du trimestre le plus proche. | TruncQuarter(&lt;DATEHEURE>) | TruncQuarter(&quot;2016-04-13 19:28:14&quot;) |
| **TruncYear** | Tronque la date et l’heure à la première date de l’année la plus proche. | TruncYear(&lt;DATEHEURE>) | TruncYear(&quot;2016-04-13 19:28:14&quot;) |
| **TruncWeek** | Tronque la date et l’heure au dimanche de la semaine la plus proche. | TruncWeek(&lt;DATEHEURE>) | TruncWeek(&quot;2016-04-13 19:28:14&quot;) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- | **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | -->


<!-- 
>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncDateTZ** | Truncates the datetime to the nearest unit, based on the numerical value given, and sets the datetime to the specified timezone. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. | TruncDateTZ(&lt;DATETIME&gt;, &lt;NUMBER&gt;, &lt;TIMEZONE&gt;) | TruncDateTZ("2016-04-13 19:28:14", 3600, "America/Los_Angeles") |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |

>[!TAB Redshift]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **ConvertTimezone** | Converts the datetime from its timezone to the timezone of the external account. | ConvertTimezone(&lt;DATETIME&gt;) | ConvertTimezone("2019-12-25 15:30:00") |

 -->

>[!TAB Snowflake]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Ajoute le nombre d’années spécifié à la date et à l’heure indiquées. | AddYears(&lt;DATEHEURE>, &lt;NOMBRE>) | AddYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMonths** | Ajoute le nombre de mois spécifié à la date et à l’heure indiquées. | AddMonths(&lt;DATEHEURE>, &lt;NOMBRE>) | AddMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **AddDays** | Ajoute le nombre de jours spécifié à la date et à l’heure indiquées. | AddDays(&lt;DATEHEURE>, &lt;NOMBRE>) | AddDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **AddHours** | Ajoute le nombre d’heures spécifié à la date et à l’heure indiquées. | AddHours(&lt;DATEHEURE>, &lt;NOMBRE>) | AddHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMinutes** | Ajoute le nombre de minutes spécifié à la date et à l’heure indiquées. | AddMinutes(&lt;DATEHEURE>, &lt;NOMBRE>) | AddMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **AddSeconds** | Ajoute le nombre de secondes spécifié à la date et à l’heure indiquées. | AddSeconds(&lt;DATEHEURE>, &lt;NOMBRE>) | AddSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **SubYears** | Soustrait le nombre d’années spécifié à la date et à l’heure indiquées. | SubYears(&lt;DATEHEURE>, &lt;NOMBRE>) | SubYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMonths** | Soustrait le nombre de mois spécifié à la date et à l’heure indiquées. | SubMonths(&lt;DATEHEURE>, &lt;NOMBRE>) | SubMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **SubDays** | Soustrait le nombre de jours spécifié à la date et à l’heure indiquées. | SubDays(&lt;DATEHEURE>, &lt;NOMBRE>) | SubDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **SubHours** | Soustrait le nombre d’heures spécifié à la date et à l’heure indiquées. | SubHours(&lt;DATEHEURE>, &lt;NOMBRE>) | SubHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMinutes** | Soustrait le nombre de minutes spécifié à la date et à l’heure indiquées. | SubMinutes(&lt;DATEHEURE>, &lt;NOMBRE>) | SubMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **SubSeconds** | AdSubstractsds le nombre de secondes spécifié à la date et et à l’heure indiquées. | SubSeconds(&lt;DATEHEURE>, &lt;NOMBRE>) | SubSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **Year** | Extrait l’année de l’objet date/heure donné. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Month** | Extrait le mois de l’objet date/heure donné. | Month(&lt;DATEHEURE>) | Month(&quot;2019-12-15 15:30:00&quot;) |
| **Jour** | Extrait le jour de l’objet date/heure donné. | Day(&lt;DATEHEURE>) | Day(&quot;2019-12-15 15:30:00&quot;) |
| **DayOfYear** | Extrait le jour de l’année de l’objet date/heure donné. Par exemple, si la date et l’heure indiquées sont le 2 février, la valeur 33 est renvoyée. | DayOfYear(&lt;DATEHEURE>) | DayOfYear(&quot;2019-12-15 15:30:00&quot;) |
| **WeekDay** | Extrait le jour de la semaine de l’objet date/heure donné, sous la forme d’un nombre compris entre 1 et 7, 1 représentant le dimanche. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Hour** | Extrait la valeur de l’heure de l’objet date/heure donné. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Minute** | Extrait la valeur de minute de l’objet date/heure donné. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **Second** | Extrait la valeur de seconde de l’objet date/heure donné. | Year(&lt;DATEHEURE>) | Year(&quot;2019-12-15 15:30:00&quot;) |
| **YearsDiff** | Trouve la différence entre les dates et heures données, avec une granularité en années. | YearsDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | YearsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsDiff** | Trouve la différence entre les dates et heures données, avec une granularité en mois. | MonthsDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | MonthsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **DaysDiff** | Trouve la différence entre les dates et heures données, avec une granularité en jours. | DaysDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | DaysDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **HoursDiff** | Trouve la différence entre les dates et heures données, avec une granularité en heures. | HoursDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | HoursDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MinutesDiff** | Trouve la différence entre les dates et heures données, avec une granularité en minutes. | MinutesDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | MinutesDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **SecondsDiff** | Trouve la différence entre les dates et heures données, avec une granularité en secondes. | SecondsDiff(&lt;DATEHEURE>, &lt;DATEHEURE>) | SecondsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsOld** | Trouve la différence entre la date et l’heure données et le moment présent, avec une granularité en mois. | MonthsOld(&lt;DATEHEURE>) | MonthsOld(&quot;2019-12-25 15:30:00&quot;) |
| **DaysOld** | Trouve la différence entre la date et l’heure données et le moment présent, avec une granularité en jours. | DaysOld(&lt;DATEHEURE>) | DaysOld(&quot;2019-12-25 15:30:00&quot;) |
| **GetDate** | Obtient la date actuelle du serveur. | GetDate() | GetDate() |
| **DateOnly** | Tronque la date et l’heure pour ne conserver que l’année, le mois et le jour. | DateOnly(&lt;DATEHEURE>) | DateOnly(&quot;2019-12-25 15:30:00&quot;) |
| **ToDate** | Convertit le champ en champ de date. | ToDate(&lt;DATEHEURE>) | ToDate(&quot;2019-12-25 15:30:00&quot;) |
| **ToDateTime** | Convertit le champ en champ de date/heure. | ToDateTime(&lt;DATE>) | ToDateTime(&quot;2019-12-25 15:30:00&quot;) |
| **ToTimestamp** | Convertit le champ en champ d’horodatage. | ToTimestamp(&lt;DATEHEURE>) | ToTimestamp(&quot;2019-12-25 15:30:00&quot;) |
| **Oldest** | Renvoie la date la plus ancienne parmi les deux indiquées. | Oldest(&lt;DATEHEURE>, &lt;DATEHEURE>) | Oldest(&quot;2015-02-13 11:59:59&quot;, &quot;2016-04-13 19:28:14&quot;) |
| **TruncDate** | Tronque la date et l’heure à l’unité la plus proche, en fonction de la valeur numérique donnée. Si la valeur numérique est égale à 60, elle est tronquée à la minute la plus proche. Si la valeur numérique est égale à 3 600, elle est tronquée à l’heure la plus proche. Si la valeur numérique est égale à 86 400, elle est tronquée au jour le plus proche. Sinon, elle est tronquée à la seconde la plus proche. | TruncDate(&lt;DATEHEURE>, &lt;NOMBRE>) | TruncDate(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncDateTZ** | Tronque la date et l’heure à l’unité la plus proche, en fonction de la valeur numérique donnée, et définit la date et l’heure sur le fuseau horaire spécifié. Si la valeur numérique est égale à 60, elle est tronquée à la minute la plus proche. Si la valeur numérique est égale à 3 600, elle est tronquée à l’heure la plus proche. Si la valeur numérique est égale à 86 400, elle est tronquée au jour le plus proche. | TruncDateTZ(&lt;DATEHEURE>, &lt;NOMBRE>, &lt;FUSEAUHORAIRE>) | TruncDateTZ(&quot;2016-04-13 19:28:14&quot;, 3600, &quot;America/Los_Angeles&quot;) |
| **TruncTime** | Définit la date et l’heure sur le 1er janvier 2000 et arrondit le reste de la date et de l’heure à l’unité la plus proche, en fonction de la valeur numérique donnée. Si la valeur numérique est égale à 60, elle est tronquée à la minute la plus proche. Si la valeur numérique est égale à 3 600, elle est tronquée à l’heure la plus proche. | TruncTime(&lt;DATEHEURE>, &lt;NOMBRE>) | TruncTime(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncQuarter** | Tronque la date et l’heure à la première date du trimestre le plus proche. | TruncQuarter(&lt;DATEHEURE>) | TruncQuarter(&quot;2016-04-13 19:28:14&quot;) |
| **TruncYear** | Tronque la date et l’heure à la première date de l’année la plus proche. | TruncYear(&lt;DATEHEURE>) | TruncYear(&quot;2016-04-13 19:28:14&quot;) |
| **TruncWeek** | Tronque la date et l’heure au dimanche de la semaine la plus proche. | TruncWeek(&lt;DATEHEURE>) | TruncWeek(&quot;2016-04-13 19:28:14&quot;) |
| **ConvertNTZ** | Convertit un horodatage sans fuseau horaire à un horodatage avec fuseau horaire. Le fuseau horaire associé sera celui du compte externe. | ConvertNTZ(&lt;DATEHEURE>) | ConvertNTZ(&quot;2024-06-24 14:43:49&quot;) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- 
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | 
-->

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") |
-->

>[!ENDTABS]

>[!NOTE]
>
>Notez que la fonction **Dateonly** prend uniquement le fuseau horaire du serveur, et non celui de l’opérateur ou de l’opératrice.

### Géomarketing

Les fonctions de géomarketing sont utilisées pour manipuler des valeurs géographiques.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **Distance** | Renvoie la distance entre deux points donnés par leur longitude et leur latitude, exprimées en degrés, sous forme de nombre double. | Distance(&lt;NOMBRE>, &lt;NOMBRE>, &lt;NOMBRE>, &lt;NOMBRE>) | Distance(40.345, 39.2345, -35.5834, 34.599) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Redshift]

Geomarketing functions are not available.

-->

>[!TAB Snowflake]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **Distance** | Renvoie la distance entre deux points donnés par leur longitude et leur latitude, exprimées en degrés, sous forme de nombre double. | Distance(&lt;NOMBRE>, &lt;NOMBRE>, &lt;NOMBRE>, &lt;NOMBRE>) | Distance(40.345, 39.2345, -35.5834, 34.599) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

-->

>[!ENDTABS]

### Numérique

Les fonctions numériques sont utilisées pour convertir du texte en nombres.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **Mod** | Renvoie le reste du premier nombre divisé par le second. | Mod(&lt;NOMBRE>, &lt;NOMBRE>) | Mod (3, 2) |
| **Percent** | Calcule le pourcentage du premier nombre par rapport au second. | Percent(&lt;NOMBRE>, &lt;NOMBRE>) | Percent(1, 2) |
| **Random** | Renvoie un nombre aléatoire compris entre 0 (inclusif) et 1 (exclusif). | Random() | Random () |
| **Round** | Renvoie le nombre indiqué à la décimale demandée la plus proche. | Round(&lt;NOMBRE>, &lt;NOMBRE>) | Round(4.5394, 2) |
| **ToDouble** | Convertit le nombre indiqué en nombre double. | ToDouble(&lt;NOMBRE>) | ToDouble(5) |
| **ToInteger** | Convertit le nombre indiqué en entier. | ToInteger(&lt;NOMBRE>) | ToInteger(45) |
| **ToInt64** | Convertit le nombre indiqué en un entier 64 bits. | ToInt64(&lt;NOMBRE>) | ToInt64(493) |
| **Trunc** | Tronque le nombre indiqué au nombre de décimales demandé. | Trunc(&lt;NOMBRE>, &lt;NOMBRE>) | Trunc(36.9348934, 3) |

<!-- 
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Floor** | Rounds down the provided number to the nearest integer. For example, if the provided number is 3.8, it will return 3. | Floor(&lt;NUMBER&gt;) | Floor(3.8) |
| **Greatest** | Returns the larger number between the two provided numbers. | Greatest(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Greatest(1, 2) |
| **Least** | Returns the smaller number between the two provided numbers. | Least(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Least (1,2) |
 -->

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Redshift]

Numeric functions are not available.

--->

>[!TAB Snowflake]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **Mod** | Renvoie le reste du premier nombre divisé par le second. | Mod(&lt;NOMBRE>, &lt;NOMBRE>) | Mod (3, 2) |
| **Percent** | Calcule le pourcentage du premier nombre par rapport au second. | Percent(&lt;NOMBRE>, &lt;NOMBRE>) | Percent(1, 2) |
| **Random** | Renvoie un nombre aléatoire compris entre 0 (inclusif) et 1 (exclusif). | Random() | Random () |
| **ToDouble** | Convertit le nombre indiqué en nombre double. | ToDouble(&lt;NOMBRE>) | ToDouble(5) |
| **ToInteger** | Convertit le nombre indiqué en entier. | ToInteger(&lt;NOMBRE>) | ToInteger(45) |
| **ToInt64** | Convertit le nombre indiqué en un entier 64 bits. | ToInt64(&lt;NOMBRE>) | ToInt64(493) |
| **Trunc** | Tronque le nombre indiqué au nombre de décimales demandé. | Trunc(&lt;NOMBRE>, &lt;NOMBRE>) | Trunc(36.9348934, 3) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

--->

>[!ENDTABS]

### Autres

Ce tableau contient les autres fonctions disponibles.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **Case** | Renvoie la première valeur si l’expression est vraie. Dans le cas contraire, renvoie la deuxième valeur. | Case(When(&lt;EXPRESSION> &lt;VALEUR>), Else(&lt;VALEUR>)) | Case(When(a > b, &quot;yes&quot;), Else(&quot;no&quot;)) |
| **When** | Utilisé dans le cadre de la fonction Case. Utilisé pour vérifier l’expression dans Case. | When(&lt;EXPRESSION> &lt;VALEUR>) | When(a > b, &quot;yes&quot;) |
| **Else** | Utilisé dans le cadre de la fonction Case. Utilisé pour choisir l’autre option, si l’expression When est fausse. | Else(&lt;VALEUR>) | Else (&quot;no&quot;) |
| **Coalesce** | Renvoie la première valeur non nulle. | Coalesce(&lt;VALEUR>, &lt;VALEUR>) | Coalesce (&quot;&quot;, &quot;string&quot;) |
| **Decode** | Renvoie la première option si les valeurs sont égales. Renvoie la seconde option si les valeurs ne sont pas égales. | Decode(&lt;VALEUR>, &lt;VALEUR>, &lt;VALEUR>, &lt;VALEUR>) | Decode(1, 2, &quot;true&quot;, &quot;false&quot;) |
| **GetEmailDomain** | Extrait le domaine d’une adresse e-mail indiquée. | GetEmailDomain(&lt;CHAÎNE>) | GetEmailDomain(&quot;sample@example.com&quot;) |
| **Iif** | Renvoie la première option si la condition est vraie et renvoie la seconde option si la condition est fausse. | Iif(&lt;CONDITION>, &lt;VALEUR>, &lt;VALEUR>) | Iif(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | Renvoie la première option si la chaîne est vide. Dans le cas contraire, renvoie la seconde option. | IsEmptyString( &lt;CHAÎNE> ,&lt;VALEUR>, &lt;VALEUR>) | IsEmptyString(&quot;string&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **NewUUID** | Génère un nouvel UUID unique. | NewUUID() | NewUUID() |
| **NoNull** | Renvoie la chaîne indiquée si elle n’est pas vide et renvoie une chaîne vide si la chaîne fournie est vide. | NoNull(&lt;CHAÎNE>) | NoNull(&quot;test&quot;) |
| **IsBitSet** | Effectue une opération bit à bit ET (&amp;) sur les nombres indiqués. Vous pouvez ainsi vérifier si le bit du premier paramètre est défini à la position indiquée dans le second paramètre. | IsBitSet(&lt;NOMBRE>, &lt;NOMBRE>) | IsBitSet(5, 3) |
| **ClearBit** | Vous pouvez ainsi effacer le bit du premier paramètre à la position indiquée dans le second paramètre. | ClearBit(&lt;NOMBRE>, &lt;NOMBRE>) | |
| **SetBit** | Effectue une opération bit à bit OU (\|) sur les nombres indiqués. Vous pouvez ainsi définir le bit dans le premier paramètre à la position indiquée dans le second paramètre. | SetBit(&lt;NOMBRE>, &lt;NOMBRE>) | SetBit(5, 3) |
| **RowId** | Renvoie le numéro de la ligne. | RowId() | RowId() |
| **ToBoolean** | Convertit la valeur en booléen. | ToBoolean(&lt;VALEUR>) | ToBoolean(a=b) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBool(&lt;VALUE&gt;) | ToBool(a=b) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |

>[!TAB Redshift]

Other functions are not available.

--->

>[!TAB Snowflake]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **Case** | Renvoie la première valeur si l’expression est vraie. Dans le cas contraire, renvoie la deuxième valeur. | Case(When(&lt;EXPRESSION> &lt;VALEUR>), Else(&lt;VALEUR>)) | Case(When(a > b, &quot;yes&quot;), Else(&quot;no&quot;)) |
| **When** | Utilisé dans le cadre de la fonction Case. Utilisé pour vérifier l’expression dans Case. | When(&lt;EXPRESSION> &lt;VALEUR>) | When(a > b, &quot;yes&quot;) |
| **Else** | Utilisé dans le cadre de la fonction Case. Utilisé pour choisir l’autre option, si l’expression When est fausse. | Else(&lt;VALEUR>) | Else (&quot;no&quot;) |
| **GetEmailDomain** | Extrait le domaine d’une adresse e-mail indiquée. | GetEmailDomain(&lt;CHAÎNE>) | GetEmailDomain(&quot;sample@example.com&quot;) |
| **Iif** | Renvoie la première option si la condition est vraie et renvoie la seconde option si la condition est fausse. | Iif(&lt;CONDITION>, &lt;VALEUR>, &lt;VALEUR>) | Iif(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | Renvoie la première option si la chaîne est vide. Dans le cas contraire, renvoie la seconde option. | IsEmptyString( &lt;CHAÎNE> ,&lt;VALEUR>, &lt;VALEUR>) | IsEmptyString(&quot;string&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **ToBoolean** | Renvoie 1 si la valeur est vraie. Renvoie 0 si la valeur est fausse. | ToBoolean(&lt;VALEUR>) | ToBoolean(a=b) |
| **ToBooleanType** | Convertit la valeur en booléen. | ToBooleanType(&lt;VALEUR>) | ToBooleanType(a=b) |
| **IsBitSet** | Effectue une opération bit à bit ET (&amp;) sur les nombres indiqués. Vous pouvez ainsi vérifier si le bit du premier paramètre est défini à la position indiquée dans le second paramètre. | IsBitSet(&lt;NOMBRE>, &lt;NOMBRE>) | IsBitSet(5, 3) |
| **ClearBit** | Vous pouvez ainsi effacer le bit du premier paramètre à la position indiquée dans le second paramètre. | ClearBit(&lt;NOMBRE>, &lt;NOMBRE>) | |
| **SetBit** | Effectue une opération bit à bit OU (\|) sur les nombres indiqués. Vous pouvez ainsi définir le bit dans le premier paramètre à la position indiquée dans le second paramètre. | SetBit(&lt;NOMBRE>, &lt;NOMBRE>) | SetBit(5, 3) |
| **RowId** | Renvoie le numéro de la ligne. | RowId() | RowId() |
| **NewUUID** | Génère un nouvel UUID unique. | NewUUID() | NewUUID() |
| **NoNull** | Renvoie la chaîne indiquée si elle n’est pas vide et renvoie une chaîne vide si la chaîne fournie est vide. | NoNull(&lt;CHAÎNE>) | NoNull(&quot;test&quot;) |
| **AESEncrypt** | Chiffre la chaîne fournie avec le type de chiffrement AES. | AESEncrypt() | AESEncrypt(&quot;hello&quot;) |
| **ObjectConstruct** | Crée un objet basé sur les paires clé/valeur indiquées. | ObjectConstruct(&lt;CHAÎNE>, &lt;CHAÎNE>) | ObjectConstruct(&quot;key&quot;, &quot;value&quot;) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **Coalesce** | Returns the first non-null value. | Coalesce(&lt;VALUE&gt;, &lt;VALUE&gt;) | Coalesce ("", "string") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBoolean(&lt;VALUE&gt;) | ToBoolean(a=b) |

-->

>[!ENDTABS]

### Chaîne

Les fonctions de chaîne sont utilisées pour manipuler un ensemble de chaînes.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Prend deux chaînes et vérifie si elles ne sont ni nulles ni vides. | AllNonNull2(&lt;CHAÎNE>, &lt;CHAÎNE>) | AllNonNull2(&quot;&quot;, &quot;string2&quot;) |
| **AllNonNull3** | Prend trois chaînes et vérifie si elles ne sont ni nulles ni vides. | AllNonNull3(&lt;CHAÎNE>, &lt;CHAÎNE>, &lt;CHAÎNE>) | AllNonNull3(&quot;&quot;, &quot;one&quot;, &quot;three&quot;) |
| **Ascii** | Prend une chaîne et renvoie le résultat. | Ascii(&lt;CHAÎNE>) | Ascii (&quot;foo&quot;) |
| **Char** | Prend un tableau de points de code Unicode et renvoie la chaîne résultante. | Char(&lt;ARRAY>) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Trouve la première occurrence de la sous-chaîne spécifiée dans la chaîne principale. | Charindex(&lt;CHAÎNE>, &lt;SOUSCHAÎNE>) | Charindex (&quot;bar@example.com&quot;, &quot;@&quot;) |
| **dataLength** | Renvoie le nombre d’octets dans la chaîne. | dataLength(&lt;CHAÎNE>) | dataLength(&quot;My string&quot;) |
| **GetLine** | Renvoie la ligne demandée de la chaîne indiquée. | GetLine(&lt;CHAÎNE>, &lt;NOMBRE>) | GetLine(multilinestring, 5) |
| **IfEquals** | Prend quatre chaînes et renvoie la troisième chaîne si les deux premières chaînes sont égales et renvoie la quatrième chaîne si les deux premières chaînes ne sont pas égales. | IfEquals(&lt;CHAÎNE>, &lt;CHAÎNE>, &lt;CHAÎNE>, &lt;CHAÎNE>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **IsMemoNull** | Renvoie 1 si la chaîne est nulle, sinon 0. | IsMemoNull(&lt;CHAÎNE>) | IsMemoNull(&quot;hello&quot;) |
| **JuxtWords** | Prend deux chaînes et les combine en une seule chaîne. Des espaces entre les chaînes sont ajoutés si nécessaire. | JuxtWords(&lt;CHAÎNE>, &lt;CHAÎNE>) | JuxtWords(&quot;Hello&quot;, &quot;World&quot;) |
| **JuxtWords3** | Prend trois chaînes et les combine en une seule chaîne. Des espaces entre les chaînes sont ajoutés si nécessaire. | JuxtWords3(&lt;CHAÎNE>, &lt;CHAÎNE>, &lt;CHAÎNE>) | JuxtWords3(&quot;Hello&quot;, &quot;New&quot;, &quot;World&quot;) |
| **Left** | Prend une chaîne et renvoie les caractères les plus à gauche comme spécifié. | Left(&lt;CHAÎNE>, &lt;NOMBRE>) | Left(&quot;Substring&quot;, 3) |
| **Length** | Renvoie la longueur de la chaîne. | Length(&lt;CHAÎNE>) | Length(&quot;MyString&quot;) |
| **Md5Digest** | Convertit la chaîne hachée MD5 en sa représentation hexadécimale. | Md5Digest(&lt;CHAÎNE>) | Md5Digest(&quot;String&quot;) |
| **MemoContains** | Vérifie si la chaîne contient la sous-chaîne indiquée. | MemoContains(&lt;CHAÎNE>, &lt;CHAÎNE>) | MemoContains(&quot;string&quot;, &quot;str&quot;) |
| **Right** | Prend une chaîne et renvoie les caractères les plus à droite comme spécifié. | Right(&lt;CHAÎNE>, &lt;NOMBRE>) | Right (&quot;Substring&quot;, 3) |
| **Smart** | Renvoie la chaîne avec la première lettre de chaque mot en majuscule. | Smart(&lt;CHAÎNE>) | Smart(&quot;hello world&quot;) |
| **Substring** | Prend une chaîne et renvoie une partie de la chaîne indiquée, en fonction des positions données. | Substring(&lt;CHAÎNE>, &lt;NOMBRE_GAUCHE>, NOMBRE_DROIT>) | Substring(&quot;Substring&quot;, 3, 5) |
| **Sha256Digest** | Convertit la chaîne hachée SHA256 en sa représentation hexadécimale. | Sha256Digest(&lt;CHAÎNE>) | Sha256Digest(&quot;string&quot;) |
| **Sha512Digest** | Convertit la chaîne hachée SHA512 en sa représentation hexadécimale. | Sha512Digest(&lt;CHAÎNE>) | Sha512Digest(&quot;string&quot;) |
| **ToString** | Renvoie la valeur sous forme de chaîne. | ToString(&lt;VALEUR>) | ToString(123) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **IsMemoNull** |  Returns 1 if the string is null, otherwise it returns 0. | IsMemoNull(&lt;STRING&gt;) | IsMemoNull("hello") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Redshift]

String functions are not available.

-->

>[!TAB Snowflake]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Prend deux chaînes et vérifie si elles ne sont ni nulles ni vides. | AllNonNull2(&lt;CHAÎNE>, &lt;CHAÎNE>) | AllNonNull2(&quot;&quot;, &quot;string2&quot;) |
| **AllNonNull3** | Prend trois chaînes et vérifie si elles ne sont ni nulles ni vides. | AllNonNull3(&lt;CHAÎNE>, &lt;CHAÎNE>, &lt;CHAÎNE>) | AllNonNull3(&quot;&quot;, &quot;one&quot;, &quot;three&quot;) |
| **Char** | Prend un tableau de points de code Unicode et renvoie la chaîne résultante. | Char(&lt;ARRAY>) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Trouve la première occurrence de la sous-chaîne spécifiée dans la chaîne principale. | Charindex(&lt;CHAÎNE>, &lt;SOUSCHAÎNE>) | Charindex (&quot;bar@example.com&quot;, &quot;@&quot;) |
| **dataLength** | Renvoie le nombre d’octets dans la chaîne. | dataLength(&lt;CHAÎNE>) | dataLength(&quot;My string&quot;) |
| **GetLine** | Renvoie la ligne demandée de la chaîne indiquée. | GetLine(&lt;CHAÎNE>, &lt;NOMBRE>) | GetLine(multilinestring, 5) |
| **IfEquals** | Prend quatre chaînes et renvoie la troisième chaîne si les deux premières chaînes sont égales et renvoie la quatrième chaîne si les deux premières chaînes ne sont pas égales. | IfEquals(&lt;CHAÎNE>, &lt;CHAÎNE>, &lt;CHAÎNE>, &lt;CHAÎNE>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **IsMemoNull** | Renvoie 1 si la chaîne est nulle, sinon 0. | IsMemoNull(&lt;CHAÎNE>) | IsMemoNull(&quot;hello&quot;) |
| **JuxtWords** | Prend deux chaînes et les combine en une seule chaîne. Des espaces entre les chaînes sont ajoutés si nécessaire. | JuxtWords(&lt;CHAÎNE>, &lt;CHAÎNE>) | JuxtWords(&quot;Hello&quot;, &quot;World&quot;) |
| **JuxtWords3** | Prend trois chaînes et les combine en une seule chaîne. Des espaces entre les chaînes sont ajoutés si nécessaire. | JuxtWords3(&lt;CHAÎNE>, &lt;CHAÎNE>, &lt;CHAÎNE>) | JuxtWords3(&quot;Hello&quot;, &quot;New&quot;, &quot;World&quot;) |
| **Left** | Prend une chaîne et renvoie les caractères les plus à gauche comme spécifié. | Left(&lt;CHAÎNE>, &lt;NOMBRE>) | Left(&quot;Substring&quot;, 3) |
| **Length** | Renvoie la longueur de la chaîne. | Length(&lt;CHAÎNE>) | Length(&quot;MyString&quot;) |
| **Line** | Renvoie la ligne numérotée spécifiée à partir de la chaîne. | Line(&lt;CHAÎNE>, &lt;NOMBRE>) | Line(multilinestring, 5) |
| **Md5Digest** | Convertit la chaîne hachée MD5 en sa représentation hexadécimale. | Md5Digest(&lt;CHAÎNE>) | Md5Digest(&quot;String&quot;) |
| **Replace** | Prend une chaîne et remplace toutes les instances de la sous-chaîne par une sous-chaîne de remplacement. | Replace(&lt;CHAÎNE>, &lt;STRING&amp;gt, &lt;STRING&amp;gt) | Replace(&quot;Captain Steve&quot;, &quot;Captain&quot;, &quot;Engineer&quot;) |
| **Right** | Prend une chaîne et renvoie les caractères les plus à droite comme spécifié. | Right(&lt;CHAÎNE>, &lt;NOMBRE>) | Right (&quot;Substring&quot;, 3) |
| **Sha256Digest** | Convertit la chaîne hachée SHA256 en sa représentation hexadécimale. | Sha256Digest(&lt;CHAÎNE>) | Sha256Digest(&quot;string&quot;) |
| **Sha512Digest** | Convertit la chaîne hachée SHA512 en sa représentation hexadécimale. | Sha512Digest(&lt;CHAÎNE>) | Sha512Digest(&quot;string&quot;) |
| **Smart** | Renvoie la chaîne avec la première lettre de chaque mot en majuscule. | Smart(&lt;CHAÎNE>) | Smart(&quot;hello world&quot;) |
| **ToString** | Renvoie la valeur sous forme de chaîne. | ToString(&lt;VALEUR>) | ToString(123) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |

-->

>[!ENDTABS]

### Période

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Renvoie une séquence de lignes en fonction de la partition du tableau et de la séquence de tri. | RowNum(PartitionBy(&lt;EXPRESSION>), OrderBy(&lt;EXPRESSION>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Sépare les lignes d’entrée en différentes partitions, selon l’expression donnée. | PartitionBy(&lt;EXPRESSION>) | PartitionBy(division) |
| **OrderBy** | Trie le résultat au sein de la partition. | OrderBy(&lt;EXPRESSION>) | OrderBy(age) |
| **Desc** | Permet à votre fonction OrderBy de trier par ordre décroissant, plutôt que par ordre croissant. | Desc(OrderBy(&lt;EXPRESSION>)) | Desc(OrderBy(age)) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Redshift]

Window functions are not available.

--->

>[!TAB Snowflake]

| Nom | Description | Syntaxe | Exemple |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Renvoie une séquence de lignes en fonction de la partition du tableau et de la séquence de tri. | RowNum(PartitionBy(&lt;EXPRESSION>), OrderBy(&lt;EXPRESSION>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Sépare les lignes d’entrée en différentes partitions, selon l’expression donnée. | PartitionBy(&lt;EXPRESSION>) | PartitionBy(division) |
| **OrderBy** | Trie le résultat au sein de la partition. | OrderBy(&lt;EXPRESSION>) | OrderBy(age) |
| **Desc** | Permet à votre fonction OrderBy de trier par ordre décroissant, plutôt que par ordre croissant. | Desc(OrderBy(&lt;EXPRESSION>)) | Desc(OrderBy(age)) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

-->

>[!ENDTABS]
