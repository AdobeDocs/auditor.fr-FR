---
description: 'null'
seo-description: valeur nulle
seo-title: FAQ sur Auditor
title: FAQ sur Auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: 631656ed4442f7f0083b1c99a725328a1c51ff9f
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 97%

---


# FAQ sur Auditor {#auditor-faq}

Cet article contient les réponses aux questions fréquentes sur Adobe Experience Platform Auditor.

* [Qu’est-ce qu’Auditor ?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [Mon entreprise peut-elle utiliser Auditor ?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Quelles sont les technologies Adobe évaluées par Auditor ?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Combien d’audits puis-je réaliser ?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [Qu’est-ce qui est analysé pendant l’audit ?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Combien de temps dure un audit ?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Quelles sont les informations fournies dans un rapport ?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [Quelle est l’utilité de ces informations ?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Auditor peut-il réaliser un audit sur des technologies autres que celles d’Adobe ?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Puis-je approuver mes adresses IP pour autoriser la numérisation des pages...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Auditor utilise-t-il les mêmes plages d’adresses IP qu’ObservePoint ?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Qu’est-ce qu’Auditor ? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Auditor est un service d’Adobe Experience Cloud qui a été co-développé avec ObservePoint, l’expert en validation d’implémentations numériques.

Auditor permet aux clients d’analyser jusqu’à 500 pages web à la fois et de recevoir un rapport. Ce dernier leur indique comment améliorer les implémentations d’Adobe Experience Cloud, afin de bénéficier pleinement de leur investissement dans Adobe.

## Puis-je utiliser Auditor ? {#section-f90094050d1e44929066a942833435cf}

Toutes les organisations clientes d’Adobe Experience Cloud bénéficient d’un accès gratuit à Auditor (à compter du 1er mai 2018). Chaque utilisateur doit accepter les conditions d’utilisation d’Adobe/ObservePoint dans l’interface utilisateur d’Adobe Experience Cloud avant d’accéder à cette fonctionnalité. Pour revenir sur ces conditions, contactez votre gestionnaire de compte.

## Comment puis-je accéder à Auditor ? {#section-531ff85f94384831a89cbb4109549daf}

Une fois connecté à [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), vous pouvez accéder à Auditor en cliquant sur **[!UICONTROL Activation]** dans la barre de navigation supérieure. Vous pouvez également accéder directement à [https://auditor.adobe.com](https://auditor.adobe.com).

## Quelles sont les technologies Adobe évaluées par Auditor ? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Service Experience Cloud ID (anciennement Service de Marketing Cloud ID)
* Target

Les solutions Adobe suivantes ne sont actuellement pas incluses dans le schéma de test. La prise en charge de ces solutions est prévue pour les prochaines mises à jour.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## Combien d’audits puis-je réaliser ? {#section-caac1e50ce1249aeba76308f3ef03fa0}

Il n’y a pas de limite au nombre d’audits que vous pouvez réaliser. Les utilisateurs sont limités à l’exécution d’un audit à la fois. Une erreur se produit si vous essayez de lancer un audit avec les mêmes paramètres que celui en cours d’exécution.

## Qu’est-ce qui est analysé pendant l’audit ? {#section-6d068ed69ece4a1bb6d0c34454550c45}

La technologie ObservePoint analyse actuellement les adresses URL trouvées dans les liens de document. Les liens trouvés dans les boutons, les widgets de pagination et d’autres éléments de page de ce type ne sont pas analysés.

## Comment puis-je suggérer de nouveaux critères pour les tests d’Auditor ? {#section-926e6ef9225b4f0bb19c2927d634cd77}

Vous pouvez envoyer des suggestions de test via la communauté d’Auditor en cliquant sur **[!UICONTROL Share Feedback]** (Partager des commentaires) sur cette page : [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Combien de temps dure un audit ? {#section-5086ae27ef1f4671a9d951348654633a}

Le temps nécessaire à la réalisation d’un audit dépend de nombreux facteurs, dont :

* Le temps de chargement de la page

   Le moteur ObservePoint charge chaque page de l’audit dans un navigateur. Plus une page se charge rapidement, plus l’audit est effectué rapidement.
* Les connexions simultanées

   Adobe Auditor utilise une connexion unique pour consulter chaque page. Les comptes ObservePoint complets utilisent jusqu’à 10 moteurs à la fois.
* Le silence réseau

   Après le chargement de chaque page, l’audit attend un silence réseau de sept secondes avant de passer à la page suivante. Si une page envoie un grand nombre de requêtes réseau après son chargement, l’attente expire au bout de 60 secondes.
* Les nouvelles tentatives sur certaines pages

   Si une page ou une balise est introuvable, l’audit stocke cette URL et y revient ultérieurement dans l’audit. L’audit consulte une page jusqu’à trois fois pour s’assurer que l’erreur n’a pas été provoquée par un problème transitoire.
* Le traitement

   Après l’exécution d’un audit, toutes les données collectées sont traitées et filtrées d’après les règles. Ce temps de traitement est important, même s’il reste inférieur à l’analyse elle-même.

>[!NOTE]
>
>Adobe Auditor effectue une analyse à la fois. Les comptes ObservePoint complets peuvent réaliser plusieurs audits consécutifs.

## Quelles sont les informations fournies dans un rapport ? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Chaque analyse génère un rapport indiquant les adresses URL analysées, les problèmes détectés sur ces pages web et des recommandations pour corriger les problèmes détectés.

Les résultats des analyses sont répartis en trois catégories :

* Configuration
* Cohérence des balises
* Présence des balises

Outre ces trois catégories, le rapport fournit des alertes contenant des informations à connaître, mais qui ne nécessitent pas forcément une action immédiate.

Les recommandations incluses dans ces catégories sont ensuite réparties en trois catégories supplémentaires :

* Fortement recommandé
* Recommandé
* À savoir

## Quelle est l’utilité de ces informations ? {#section-9308c1ea882048b781087ae6d2eee9f0}

Toutes les recommandations fournies par Auditor sont destinées à vous aider à résoudre un problème lié à votre implémentation des solutions Adobe Experience Cloud, telles que DTM ou Target. Pour faciliter cela, l’équipe d’Auditor s’est efforcée de fournir des instructions très précises sur ce qui doit être fait et où. Vous pouvez exporter une feuille de calcul contenant toutes les adresses URL analysées et tous les résultats de test, afin d’identifier facilement les zones problématiques. Voici un exemple de recommandation pour une implémentation de DTM :

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Rappel pageBottom en fermeture</b> </p> <p>Une fonction _satellite.pageBottom() est requise pour une implémentation correcte de DTM. Ajoutez le script intégré juste avant la balise &lt;/body&gt; de fermeture afin d’assurer le bon fonctionnement de DTM. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Auditor peut-il réaliser un audit sur des technologies autres que celles d’Adobe ? {#section-f6e73c56083b4815bbf901296038bcd4}

Non. Cependant, l’offre complète d’ObservePoint permet aux clients de réaliser un audit de toutes les balises et technologies marketing, et ainsi de les contrôler. En tant que client Adobe, vous avez accès à un compte d’évaluation gratuit. Pour accéder à votre compte d’évaluation, rendez-vous sur la [page Auditor d’ObservePoint](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## Can I approve my IP addresses to allow scanning pages that are protected by a login? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Cette fonctionnalité n’est actuellement pas prise en charge sans l’offre complète d’ObservePoint.

## Auditor utilise-t-il les mêmes plages d’adresses IP qu’ObservePoint ? {#section-39512b156e194787981bdd572ff5b5a9}

L’analyse est effectuée par ObservePoint. Ce sont donc les mêmes adresses IP qui sont utilisées.

Consultez la [documentation ObservePoint](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) pour en savoir plus.
