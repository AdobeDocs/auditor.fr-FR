---
description: Les filtres d’inclusion limitent les liens qu’un audit peut analyser à partir de l’URL de début. Les filtres d’exclusion empêchent un audit d’analyser des liens.
seo-description: Les filtres d’inclusion limitent les liens qu’un audit peut analyser à partir de l’URL de début. Les filtres d’exclusion empêchent un audit d’analyser des liens.
seo-title: Filtres d’inclusion et d’exclusion
title: Filtres d’inclusion et d’exclusion
uuid: 477fc38c-7351-42dd-8209-2fb7549ee34c
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 85%

---


# Filtres d’inclusion et d’exclusion {#include-and-exclude-filters}

Les filtres d’inclusion limitent les liens qu’un audit peut analyser à partir de l’URL de début. Les filtres d’exclusion empêchent un audit d’analyser des liens.

<!--
Content from ObservePoint (https://help.observepoint.com/articles/2872121-include-and-exclude-filters) with their permission. Modified slightly for style and Auditor emphasis.
-->

Les filtres d’inclusion et d’exclusion fournissent des instructions pour les audits. Lorsque vous laissez les filtres d’inclusion et d’exclusion vides, un audit peut analyser tous les liens qu’il rencontre, en commençant par les liens sur l’URL de début.

![](assets/filter.png)

En appliquant des filtres d’inclusion, des filtres d’exclusion ou une combinaison des deux, vous pouvez donner des instructions quant aux liens qu’un audit peut analyser.

Any item in the [!UICONTROL Include Filters] field restricts the scan to only the pages that match that item. Any item in an [!UICONTROL Exclude Filters] field prevents any pages that match that item from being scanned.

Les filtres d’inclusion et d’exclusion peuvent être des adresses URL complètes, des adresses URL partielles ou des expressions régulières qui correspondent à une page valide.

## Ordre de priorité {#section-e9d42419dd3f459bb20e7a33c6104f12}

1. L’**URL de début** prévaut sur tout le reste et sera toujours consultée lors d’un audit, même si l’URL correspond à un élément des filtres d’exclusion. L’URL de début est toujours consultée avant toute autre URL.

   ![](assets/startingpage.png)

   Dans l’image ci-dessus, l’audit détecte les liens à partir de la propriété `document.links` de la page de début. Ces liens peuvent être analysés lors de l’audit.

1. Les **adresses URL d’inclusion** doivent être liées à une page de début, ou elles ne pourront pas être découvertes et consultées.

   ![](assets/includefilter.png)

   Dans l’image ci-dessus, l’ajout d’un filtre d’inclusion limite les adresses URL éligibles à celles qui correspondent au filtre. Désormais, seuls cinq liens peuvent être analysés par l’audit.

1. Les **adresses URL d’exclusion** empêchent l’éligibilité des liens.

   ![](assets/excludefilter.png)

   Dans l’image ci-dessus, l’ajout d’un filtre d’exclusion empêche l’éligibilité des liens des adresses URL. Maintenant, seuls trois liens peuvent être analysés par l’audit.

## URL de début {#section-ccb46abcd96f4a8ab171245015d2b724}

Adobe Experience Platform Auditor requiert une seule page pour l&#39;URL de démarrage. L’URL de début est toujours consultée avant toute autre URL. Tout lien découvert à partir de la page de début peut être consulté, sous réserve qu’il respecte les filtres d’inclusion et d’exclusion. Si un élément d’exclusion correspond à une URL de début, il est ignoré.

## Filtres d’inclusion {#section-7626060a56a24b658f8c05f031ac3f5f}

Les filtres d’inclusion limitent les liens pouvant être analysés au cours d’un audit. Les filtres d’inclusion peuvent être :

* des adresses URL complètes ;
* des adresses URL partielles ;
* des expressions régulières correspondant à des adresses URL complètes ou partielles ;
* une combinaison des options ci-dessus.

L’ajout d’adresses URL ou d’expressions régulières au filtre d’inclusion ne garantit pas la consultation de ces adresses URL spécifiques lors de l’audit. L’audit inspecte les liens de l’URL de début, puis parcourt les liens éligibles. L’audit poursuit ce processus d’inspection et de navigation jusqu’à ce que la limite de 500 adresses URL analysées soit atteinte ou jusqu’à épuisement des liens éligibles.

>[!NOTE]
>
>Dans certains cas, analyser 500 pages peut prendre jusqu’à 48 heures.

Par défaut, un audit analyse tous les sous-domaines de l’URL de début. À moins qu’il soit explicitement remplacé par un filtre d’inclusion, l’analyse utilisera le filtre d’inclusion regex suivant :

`^https?://([^/:\?]*\.)?mysite.com`

Ainsi, tout lien figurant sur la page de l’URL de début peut être consulté. Il correspond à n’importe quelle page sur n’importe quel sous-domaine de l’URL de début.

L’utilisation du filtre d’inclusion par défaut offre un large éventail d’analyse aux audits. Pour cibler certaines sections ou pages, indiquez des instructions d’audit spécifiques en ajoutant des filtres dans cette zone. Dans ce cas, remplacez la valeur par défaut par les répertoires que vous souhaitez analyser dans votre audit. Vous pouvez également utiliser l’option Inclure des filtres pour effectuer un contrôle inter-domaines dans lequel vous devez début l’audit sur un domaine et se terminer sur un autre. Pour ce faire, saisissez les domaines que vous souhaitez parcourir. Dans tous les cas, pour qu’une URL de filtre Inclure soit trouvée, elle doit être découverte sur une page vérifiée.

Les filtres Inclure peuvent contenir des URL exactes, des URL partielles ou des expressions régulières. Par exemple, si l’URL de début est [!DNL http://mysite.com], les pages suivantes sont éligibles à l’analyse par défaut (notez les caractères en gras) :

```html
http://mysite.com
http
<b>s</b>://mysite.com
http://
<b>www</b>.mysite.com/home
http://
<b>dev</b>.mysite.com/home
http://
<b>my</b>.mysite.com/products/products_and_services.html
```

Pour les modèles d’URL complexes, utilisez le [testeur d’expression régulière d’ObservePoint](https://regex.observepoint.com/).

## Filtres d’exclusion {#section-00aa5e10c878473b91ba0844bebe7ca9}

Les filtres d’exclusion empêchent l’analyse de certaines adresses URL. Vous pouvez utiliser des adresses URL exactes, des adresses URL partielles ou des expressions régulières. Toute URL correspondant à un élément des filtres d’exclusion ne sera pas consultée. Si votre URL de début est incluse dans les filtres d’exclusion, elle n’est pas exclue pour autant. L’URL de début est toujours analysée lors d’un audit.

## Test des filtres et adresses URL {#section-3cfa125b1756411395a64701e128efa0}

Vous pouvez tester vos filtres et URL dans Platform Auditor.

Lorsque vous créez un audit, cliquez sur **[!UICONTROL Test Advanced Filters]**. Saisissez les filtres et adresses URL, puis cliquez sur **[!UICONTROL Apply]**.

![](assets/test-advanced-filters.png)

## Documentation d’ObservePoint {#section-79cdc8e850d047969b6d2badf6bbd6f9}

Cet article a été élaboré en collaboration avec ObservePoint. Pour obtenir les informations les plus récentes, reportez-vous à la [documentation d’ObservePoint](https://help.observepoint.com/).
