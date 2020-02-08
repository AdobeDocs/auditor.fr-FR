---
description: valeur nulle
seo-description: valeur nulle
seo-title: Auditor FAQ
title: FAQ sur l’auditeur
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# FAQ sur l’auditeur{#auditor-faq}

Cet article contient les réponses aux questions fréquentes sur Adobe Experience Platform Audit.

* [Qu&#39;est-ce que le vérificateur?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [Mon entreprise est-elle admissible à l&#39;utilisation du vérificateur?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Quelles sont les technologies Adobe évaluées par l’auditeur ?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Combien d&#39;audits puis-je exécuter ?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [Qu’est-ce qui est analysé pour un audit ?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Combien de temps dure un audit ?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Quelles informations sont fournies dans un rapport ?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [Quelle est l&#39;utilité de cette information ?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [L’auditeur peut-il contrôler la technologie non Adobe ?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Puis-je mettre en liste blanche mes adresses IP pour permettre la numérisation des pages...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [L’auditeur utilise-t-il les mêmes plages d’adresses IP que Observepoint ?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Qu&#39;est-ce que le vérificateur? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

L’auditeur est un service d’Adobe Experience Cloud qui a été co-développé avec ObservePoint, expert en validation des implémentations numériques.

Auditeur permet aux clients d’analyser jusqu’à 500 pages Web à la fois et de recevoir un rapport qui montre comment améliorer leurs mises en oeuvre Adobe Experience Cloud pour qu’ils reçoivent la valeur totale de leur investissement Adobe.

## Est-ce que je peux utiliser le vérificateur? {#section-f90094050d1e44929066a942833435cf}

Tous les clients d’Adobe Experience Cloud bénéficient d’un accès gratuit à l’auditeur (à compter du 1er mai 2018). Chaque utilisateur doit consentir aux conditions d’utilisation d’Adobe/ObservePoint dans l’interface utilisateur d’Adobe Experience Cloud avant d’accéder à la fonctionnalité. Pour exclure ces conditions, contactez votre gestionnaire de compte.

## Comment puis-je accéder à l&#39;Auditeur ? {#section-531ff85f94384831a89cbb4109549daf}

Une fois connecté à [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), vous pouvez accéder à Auditor en cliquant sur **[!UICONTROL Activation]** dans la barre de navigation supérieure. Vous pouvez également accéder directement à [https://auditor.adobe.com](https://auditor.adobe.com).

## Quelles sont les technologies Adobe évaluées par l’auditeur ? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Recherche Advertising Cloud
* Analytics
* DTM
* Service d’ID Experience Cloud (anciennement Service de Marketing Cloud ID)
* Target

Les solutions Adobe suivantes ne sont pas actuellement incluses dans la rubrique de test. La prise en charge de ces solutions est prévue pour les futures mises à jour.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## Combien d&#39;audits puis-je exécuter ? {#section-caac1e50ce1249aeba76308f3ef03fa0}

Le nombre d’audits que vous pouvez exécuter est illimité. Les utilisateurs sont limités à un audit exécuté à la fois. Une erreur se produit si vous tentez de lancer un audit avec les mêmes paramètres que celui en cours d’exécution.

## Qu’est-ce qui est analysé pour un audit ? {#section-6d068ed69ece4a1bb6d0c34454550c45}

La technologie ObservePoint analyse actuellement les URL trouvées dans les liens de document. Les liens trouvés dans les boutons, les widgets de pagination et d’autres éléments de page de ce type ne sont pas analysés.

## Comment puis-je suggérer de nouveaux critères pour les tests du vérificateur? {#section-926e6ef9225b4f0bb19c2927d634cd77}

Vous pouvez envoyer des suggestions de test via la communauté des auditeurs (Auditor Community) en cliquant sur **[!UICONTROL Share Feedback]** (Partager les commentaires) sur cette page : [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Combien de temps dure un audit ? {#section-5086ae27ef1f4671a9d951348654633a}

De nombreux facteurs contribuent au temps nécessaire à la réalisation d’une vérification, notamment :

* Temps de chargement de page

   Le moteur ObservePoint charge chaque page de l’audit dans un navigateur. Plus une page est chargée rapidement, plus l’audit est effectué rapidement.
* Connexions simultanées

   Adobe Audit utilise une connexion unique pour visiter chaque page. Les comptes ObservePoint complets utilisent jusqu’à 10 moteurs à la fois.
* Silence réseau

   Une fois chaque page chargée, l’audit attend un silence réseau de sept secondes avant de passer à la page suivante. Si une page envoie un grand nombre de requêtes réseau qui se produisent après le chargement de la page, l’attente expire au bout de 60 secondes.
* Nouvelles tentatives de page

   Si une page ou une balise est introuvable, l’audit stocke cette URL et y revient ultérieurement dans l’audit. L’audit consulte une page jusqu’à trois fois pour s’assurer que l’erreur n’a pas été provoquée par un problème temporaire.
* Traitement

   Après l’exécution d’un audit, toutes les données qu’il a collectées sont traitées et filtrées dans les règles. Ce temps de traitement est important, bien que cela ne prenne pas autant de temps que l&#39;analyse elle-même.

>[!NOTE]
>
>Adobe auditeur exécute une analyse unique à la fois. Les comptes ObservePoint complets peuvent exécuter plusieurs audits consécutivement.

## Quelles informations sont fournies dans un rapport ? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Chaque analyse génère un rapport qui indique les URL qui ont été numérisées, les problèmes détectés sur ces pages Web et des recommandations sur la manière de corriger les problèmes détectés.

Les résultats des analyses sont répartis en trois catégories :

* Configuration
* Cohérence des balises
* Présence des balises

Outre ces trois catégories, le rapport fournit des alertes contenant des informations dont vous devez être conscient, mais qui ne nécessitent pas nécessairement une action immédiate.

Les recommandations incluses dans ces catégories sont ensuite réparties en trois catégories supplémentaires :

* Très recommandé
* Recommandée
* Transmis

## Quelle est l&#39;utilité de cette information ? {#section-9308c1ea882048b781087ae6d2eee9f0}

Toutes les recommandations fournies par l’intermédiaire de l’auditeur sont destinées à vous aider à prendre des mesures pour résoudre un problème lié à votre implémentation des solutions Adobe Experience Cloud, telles que la gestion dynamique des balises ou Target. Pour faciliter cette tâche, l&#39;équipe du vérificateur a travaillé de façon intensive pour fournir des instructions très précises sur ce qui doit être fait là où. Vous pouvez exporter une feuille de calcul contenant toutes les URL analysées et tous les résultats de test afin de pouvoir identifier facilement les zones à problème. Voici un exemple de recommandation pour une implémentation de gestion dynamique des balises :

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>rappel pageBottom dernier</b> </p> <p>Une fonction _satellite.pageBottom() est requise pour une implémentation de gestion dynamique des balises correcte. Ajoutez le script intégré juste avant la balise &lt;/body&gt; de fermeture pour garantir la fonctionnalité de gestion dynamique des balises appropriée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## L’auditeur peut-il contrôler la technologie non Adobe ? {#section-f6e73c56083b4815bbf901296038bcd4}

Non. Cependant, l’offre complète d’ObservePoint permet aux clients de contrôler et de surveiller toutes vos balises et technologies marketing. En tant que client Adobe, vous avez accès à un compte d’évaluation gratuit. Pour accéder à votre compte d’évaluation, consultez la page [Auditeur d’](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&utm_medium=Auditor&utm_campaign=Premium)ObservePoint.

## Puis-je mettre en liste blanche mes adresses IP pour permettre la numérisation des pages protégées par une connexion ? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Cette fonctionnalité n’est actuellement pas prise en charge sans l’offre complète d’ObservePoint.

## L’auditeur utilise-t-il les mêmes plages d’adresses IP que ObservePoint ? {#section-39512b156e194787981bdd572ff5b5a9}

L’analyse est effectuée par ObservePoint, de sorte que les mêmes adresses IP sont utilisées.

Voir la documentation [](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) ObservePoint pour en savoir plus.
