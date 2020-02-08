---
description: Cette référence fournit plus d’informations sur les tests effectués par l’auditeur.
seo-description: Cette référence fournit plus d’informations sur les tests effectués par l’auditeur.
seo-title: Référence de test
title: Référence de test
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 0c116f699b697ad010ee074ac67159a49ec09ccd

---


# Référence de test{#test-reference}

Cette référence fournit plus d’informations sur les tests effectués par l’auditeur.

**Version du schéma de test actuel** : 1.0.5

Chaque test est pondéré. Votre score de test est égal au poids attribué. Si vous réussissez un test avec un poids de cinq points, vous recevez cinq points.

* 0 : Vous avertit des problèmes que vous devez connaître, mais qui n’affectent pas votre score.
* 1 : Recommande une optimisation. Aucune incidence sur la précision des données.
* 2 : Si ce test échoue, vous n’aurez pas accès aux dernières fonctionnalités et correctifs d’Experience Cloud.
* 3 : Teste l’efficacité et la conformité de l’implémentation aux meilleures pratiques.
* 4 : L’échec signifie que vous collectez peut-être des données non fiables.
* 5 : L’échec signifie que vous pouvez constater une perte de données.

Les tests sont transmis/échoués. Ils testent la conformité ou la non-conformité aux conditions de test, de sorte qu’il n’y a pas de scores partiels pour la conformité partielle. Par exemple, si le test recherche la dernière version d’une solution Adobe et que vous n’avez qu’une version en retard, vous obtenez le même score que si vous étiez cinq versions précédentes. Les versions les plus récentes incluent des améliorations de performances et des correctifs de bogues. Il est donc recommandé d’utiliser la version la plus récente.

Il est **vivement recommandé** de corriger les résultats de niveau 4 ou 5.

Il est **recommandé** de corriger les résultats de niveau 1 à 3.

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

## Catégories de test {#section-630181db21ef4eec9ce6a13a0482bb55}

Cette référence de test divise les tests en catégories suivantes :
