---
description: Cette référence fournit des informations supplémentaires sur les tests effectués par Adobe Experience Platform Auditor.
seo-description: This reference provides more information about the tests Adobe Experience Platform Auditor performs.
seo-title: Test reference
title: Référence sur les tests
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
exl-id: b368bf43-2007-4f98-a965-ed8fc07c0fdf
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 100%

---

# Référence sur les tests{#test-reference}

Cette référence fournit des informations supplémentaires sur les tests effectués par Adobe Experience Platform Auditor.

**Version du schéma de test actuel :** 1.0.5

Chaque test est pondéré. Le score de test est égal au poids attribué. Si vous réussissez un test avec un poids de cinq, vous recevez cinq points.

* 0 : vous avertit au sujet de problèmes que vous devez connaître, mais qui n’affectent pas votre score.
* 1 : optimisation recommandée. Aucune incidence sur la précision des données.
* 2 : un échec signifie que vous n’aurez pas accès aux fonctionnalités et correctifs Experience Cloud les plus récents.
* 3 : teste l’efficacité et la conformité de l’implémentation aux bonnes pratiques.
* 4 : un échec signifie que vous collectez peut-être des données non fiables.
* 5 : un échec signifie que vous pouvez subir une perte de données.

Les tests sont des réussites ou des échecs. Ils vérifient la conformité ou la non-conformité aux conditions de test. Il n’existe pas de score partiel pour une conformité partielle. Par exemple, si le test vérifie la version la plus récente d’une solution Adobe et que vous n’avez qu’une version de retard, vous obtenez le même score que si vous aviez cinq versions de retard. Les versions les plus récentes incluent des améliorations de performances et des corrections de bogues. Il est donc recommandé d’utiliser la version la plus récente.

Il est **vivement recommandé** de corriger les résultats de niveau 4 ou 5.

Il est **recommandé** de corriger les résultats de niveau 1 à 3.

## Quelles sont les technologies Adobe évaluées par Platform Auditor ?  {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Service Experience Cloud ID (anciennement Service de Marketing Cloud ID)
* Target

Les solutions Adobe suivantes ne sont actuellement pas incluses dans le schéma de test. La prise en charge de ces solutions est prévue pour les prochaines mises à jour.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Adobe Experience Platform Launch
