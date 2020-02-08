---
description: Après avoir exécuté un test, la carte de performance affiche des informations sur un audit.
seo-description: Après avoir exécuté un test, la carte de performance affiche des informations sur un audit.
seo-title: Scorecard
title: Scorecard
uuid: a765cd6a-d3d6-4438-9621-d7899385a518
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Scorecard{#scorecard}

Après avoir exécuté un test, la carte de performance affiche des informations sur un audit.

Cliquez sur le nom de votre audit dans la page Auditeur pour afficher les résultats de votre test.

![](assets/report.png)

Utilisez la carte de performance pour voir comment l’audit a obtenu des résultats dans les catégories suivantes :

* Note globale
* Présence des balises

   Evalue si la balise existe et si elle se trouve au bon endroit dans le code de votre page.
* Cohérence des balises

   Evalue si les balises sont cohérentes entre les URL.
* Configuration

   Evalue les balises en fonction d’autres règles et des bonnes pratiques recommandées.
* Alerte

   Les alertes indiquent les problèmes que vous devez connaître, mais qui n’affectent pas votre score.

Votre score dépend du poids de chaque test et du fait que vous réussissiez ou échouez. Si vous réussissez, votre score augmente du nombre de points égal au poids du test.

* 0 : Vous avertit des problèmes que vous devez connaître, mais qui n’affectent pas votre score.
* 1 : Recommande une optimisation. Aucune incidence sur la précision des données.
* 2 : Si ce test échoue, vous n’aurez pas accès aux dernières fonctionnalités et correctifs d’Adobe Experience Cloud.
* 3 : Teste l’efficacité et le respect des meilleures pratiques recommandées par l’implémentation.
* 4 : L’échec signifie que vous collectez peut-être des données non fiables.
* 5 : L’échec signifie que vous pouvez constater une perte de données.

La carte de performance répertorie tous les problèmes de niveau 4 ou 5 comme **vivement recommandé** que vous corrigiez.

La carte de performance répertorie les problèmes de niveau 1 à 3, comme **recommandé** que vous corrigiez.

Cliquez sur **[!UICONTROL Télécharger le rapport]** pour télécharger un fichier Excel ou PDF contenant les informations signalées par l’audit.

Outre le score pour chaque catégorie, la carte de performance répertorie les correctifs recommandés ou fortement recommandés, ainsi que les éléments qui ont réussi le test. Cliquez sur chaque publication pour afficher des détails supplémentaires dans la zone à droite. Cliquez de nouveau pour approfondir l’analyse et voir des recommandations sur la manière de résoudre le problème. L’exemple suivant montre les détails d’une publication recommandée dans la carte de performance illustrée ci-dessus :

![](assets/report-issue-details.png)

Cliquez sur les catégories dans la partie supérieure de l’écran pour afficher les problèmes rencontrés dans chaque catégorie.

## Quelles pages faisaient partie du test ? {#section-fd38ffeb868648e89c34c5772fa65f46}

Vous pouvez afficher les listes des URL qui ont réussi ou échoué votre test.

Dans la Scorecard, cliquez sur un nom de test ou sur le lien **[!UICONTROL Voir tout]** sous chaque en-tête de catégorie. Cela vous amène aux détails des tests. Pour chaque test, vous pouvez voir la description du test et la liste des URL qui ont échoué et réussi. Ces informations sont également incluses dans les rapports téléchargés.
