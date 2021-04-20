---
description: Créer un nouvel audit dans Adobe Experience Platform Auditor
seo-description: Créer un nouvel audit dans Adobe Experience Platform Auditor
seo-title: Créer un nouvel audit dans Adobe Experience Platform Auditor
title: Créer un nouvel audit dans Adobe Experience Platform Auditor
uuid: bd6798bb-3fab-4091-9e07-d3d1e5fdd087
exl-id: 1c4eed8e-4d49-49af-95c5-df13c9f13e4a
translation-type: ht
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: ht
source-wordcount: '517'
ht-degree: 100%

---

# Création d’un audit {#create-a-new-audit}

>[!NOTE]
>
>Les utilisateurs sont limités à l’exécution d’un audit à la fois. Une erreur se produit si vous essayez de lancer un audit avec les mêmes paramètres que celui en cours d’exécution. Afin d’en créer un autre, vous pouvez utiliser le lien contenu dans le message d’erreur pour annuler l’audit en cours.

Si vous le souhaitez, utilisez le lien au bas de la page pour accéder à un compte d’évaluation gratuit et complet avec ObservePoint.

1. Dans la liste d’Auditor, cliquez sur **[!UICONTROL New Audit]**.

   L’écran [!DNL New Audit] s’affiche.

   ![](assets/config.png)

1. (Obligatoire) Nommez l’audit.

   Le nom ne peut excéder 250 caractères.
1. (Obligatoire) Spécifiez l’URL de début.

   Le protocole est requis lors de la spécification de l’URL de début. L’URL de début est la page à partir de laquelle l’audit commence à analyser. Une fois lancé, Adobe Experience Platform Auditor analyse jusqu’à 500 pages, en suivant les liens qui commencent à l’URL de début. Consultez [Filtres d’inclusion et d’exclusion](../create-audit/filters.md) pour en savoir plus. L’URL de début ne peut excéder 250 caractères.

   >[!NOTE]
   >
   >Dans certains cas, analyser 500 pages peut prendre jusqu’à 48 heures.

1. Spécifiez une ou plusieurs adresses électroniques pour les notifications concernant cet audit.

   Vous pouvez indiquer plusieurs adresses en les séparant par une virgule. Par défaut, le demandeur est averti. Les adresses électroniques sont validées en temps réel. Si vous saisissez une adresse non valide, vous en êtes averti à l’écran.

   Chaque adresse électronique est limitée à 250 caractères maximum, fin de domaine incluse (par exemple, .com).

1. Spécifiez les [!UICONTROL filtres d’inclusion].

   Ce champ peut contenir des adresses URL exactes, des adresses URL partielles ou des expressions régulières. Utilisez ce champ pour les critères auxquels chaque URL doit correspondre. Les adresses URL analysées qui ne correspondent pas aux critères du [!UICONTROL filtre d’inclusion] ne sont pas incluses dans les résultats de l’audit.

   Vous pouvez saisir les répertoires à analyser dans l’audit. Vous pouvez également effectuer un audit interdomaines ou d’autoréférence, pour lequel vous devez lancer l’audit sur un domaine et le terminer sur un autre. Pour ce faire, saisissez les domaines à parcourir. Pour les modèles d’URL complexes, utilisez une expression régulière.

   >[!NOTE]
   >
   >Si vous incluez une page dans vos filtres, mais qu’elle n’est pas connectée à l’URL de début ou que Platform Auditor analyse 500 pages avant d’atteindre cette page, la page ne sera pas analysée et ne sera pas incluse dans les résultats du test.

   Les filtres d’inclusion sont limités à 1 000 caractères par ligne.

   Consultez [Liste d’inclusion](../create-audit/filters.md) pour en savoir plus.
1. Spécifiez les filtres d’exclusion.

   La [!UICONTROL liste d’exclusion] empêche l’analyse de certaines adresses URL. Utilisez des adresses URL exactes, des adresses URL partielles ou des expressions régulières, comme vous le feriez dans la [!UICONTROL liste d’inclusion].

   Une pratique courante consiste à exclure un lien de déconnexion si l’audit comporte une session utilisateur (par exemple : `/logout` signifie toute URL contenant la chaîne `/logout`).

   Les filtres d’exclusion sont limités à 1 000 caractères par ligne.

   Consultez [Liste d’exclusion](../create-audit/filters.md) pour en savoir plus.
1. (Facultatif) Si vous le souhaitez, vous pouvez tester les filtres d’inclusion et d’exclusion, ainsi que tester vos adresses URL.

   Saisissez les filtres et les adresses URL, puis cliquez sur **[!UICONTROL Apply]** pour exécuter le test.

   ![](assets/test-advanced-filters.png)

1. Cliquez sur **[!UICONTROL Run Report]**.
