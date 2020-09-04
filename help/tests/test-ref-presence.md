---
description: Cette référence fournit des informations supplémentaires sur les tests effectués par Auditor pour assurer la présence des balises.
seo-description: Cette référence fournit des informations supplémentaires sur les tests effectués par Auditor pour assurer la présence des balises.
seo-title: Présence des balises
title: Présence des balises
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: 77ced60ff8e05515521d89d16c32cbad42d1e8d0
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 100%

---


# Présence des balises

Cette référence fournit des informations supplémentaires sur les tests effectués par Auditor pour assurer la présence des balises.

Auditor évalue si la balise existe et si elle se trouve au bon endroit dans le code de votre page.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Critères </th> 
   <th colname="col3" class="entry"> Recommandation </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud : présence du code</b> </p> <p>Poids : 5 </p> </td> 
   <td colname="col2"> <p> La balise Advertising Cloud n’est pas disponible dans le modèle DOM. </p> </td> 
   <td colname="col3"> <p>Implémentez la balise Advertising Cloud à l’aide de l’extension Launch Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud : pixel de segment implémenté</b> </p> <p>Poids : 5 </p> </td> 
   <td colname="col2"> <p> Mettez à niveau vos pixels de segment Advertising Cloud vers les nouvelles balises image seule Advertising Cloud. L’utilisation de balises de segment AMO obsolètes peut entraîner une perte de données. </p> </td> 
   <td colname="col3"> <p>Implémentez le pixel de segment Advertising Cloud à l’aide de l’extension Launch Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics : chargé dans DOM</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/analytics/implementation/home.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La balise Adobe Analytics n’a pas été détectée. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version d’Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM : bibliothèque chargée</b> </p> <p>Poids : 5 </p> <p>Informations supplémentaires : </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Résolution des problèmes de DTM</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Ajout de code d’en-tête et de pied de page</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Un objet _satellite global est introuvable dans le modèle DOM. Dynamic Tag Management n’est pas installé ou ne s’exécute pas. </p> </td> 
   <td colname="col3"> <p>Vérifiez que la bibliothèque DTM est implémentée sur la page et qu’elle n’est pas bloquée par les activités de script suivantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM : un code incorporé</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/client-side/code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Les sites de production ne doivent charger qu’une seule bibliothèque DTM. </p> </td> 
   <td colname="col3"> <p>Vérifiez que seule la bibliothèque de production est en cours de chargement sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM : le rappel pageBottom existe dans &lt;body&gt;</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le rappel <span class="codeph">_satellite.pageBottom()</span> est introuvable dans la balise <span class="codeph">&lt;body&gt;</span> de la page, qui est requise par Dynamic Tag Management. </p> <p>Ce test échoue si l’appel <span class="codeph">pageBottom</span> est introuvable sur la page ou s’il se trouve dans la balise <span class="codeph">&lt;head&gt;</span> (ou à un autre emplacement inattendu). Le test ne sera réussi que si <span class="codeph"> pageBottom</span> se trouve quelque part dans la balise <span class="codeph">&lt;body&gt;</span>. S’il ne figure pas du tout sur la page, il ne fonctionnera pas et les deux autres tests <span class="codeph"> pageBottom</span> échoueront également. </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise <span class="codeph">&lt;/body&gt;</span> de fermeture afin d’assurer le bon fonctionnement de DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM : déclenchement de la balise pageBottom</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La balise DTM <code> pageBottom</code> n’a pas été détectée. </p> <p>Cela peut se produire si le rappel se trouve dans une instruction <code> if</code> dont le résultat est similaire à <code> if (false) {_satellite.pageBottom()}</code>. Ainsi, bien qu’il puisse exister et être correctement placé, la balise peut quand même ne pas se déclencher. </p> </td> 
   <td colname="col3"> <p>Installez le rappel DTM <code> pageBottom</code> sur chaque page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Service Experience Cloud ID : présence du code</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/id-service/using/intro/overview.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Le code du service Experience Cloud ID est introuvable. L’Experience Cloud ID (MCID) est vivement recommandé pour vous assurer de tirer le meilleur parti de vos solutions Experience Cloud et il est essentiel pour la gestion des identifiants dans les solutions Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Installez la dernière version de MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Service Experience Cloud ID : présence du cookie</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/tools/macid.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le cookie <span class="codeph">AMCV_</span> est introuvable. Vous devez instancier un objet visiteur à partir du code <span class="codeph"> VisitorAPI.js</span>. </p> </td> 
   <td colname="col3"> <p> S’il s’agit d’une implémentation de DTM, vérifiez que l’identifiant AdobeOrg est correctement saisi dans l’outil MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Service Experience Cloud ID : présence de la valeur MID</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/id-service/using/intro/cookies.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La valeur MID est introuvable dans le cookie <span class="codeph"> AMCV_</span>. </p> </td> 
   <td colname="col3"> <p>Testez à nouveau pour vérifier la latence de l’API MCID. Si la condition persiste, contactez l’assistance clientèle Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch : bibliothèque chargée</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Un objet _satellite global est introuvable dans le modèle DOM. Launch n’est pas installé ou ne s’exécute pas. </p> </td> 
   <td colname="col3"> <p>Vérifiez que la bibliothèque Launch est implémentée sur la page et qu’elle n’est pas bloquée par les activités de script suivantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch : ne possède pas plusieurs scripts d’intégration</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Il ne doit pas y avoir plusieurs scripts d’intégration chargés sur la page. Les sites de production ne doivent charger qu’une bibliothèque Launch. </p> </td> 
   <td colname="col3"> <p>Vérifiez que seule la bibliothèque de production est en cours de chargement sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch : le rappel pageBottom existe dans &lt;body&gt;</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le rappel <span class="codeph">_satellite.pageBottom()</span> est introuvable dans la balise <span class="codeph">&lt;body&gt;</span> de la page, qui est requise par Launch. </p> <p>Ce test échoue si l’appel <span class="codeph"> pageBottom</span> est introuvable sur la page ou s’il se trouve dans la balise <span class="codeph"> &lt;head&gt; </span> (ou à un autre emplacement inattendu). Le test ne sera réussi que si <span class="codeph"> pageBottom</span> se trouve quelque part dans la balise <span class="codeph">&lt;body&gt;</span>. S’il ne figure pas du tout sur la page, il ne fonctionnera pas et les deux autres tests <span class="codeph"> pageBottom</span> échoueront également. </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise <span class="codeph">&lt;/body&gt;</span> de fermeture afin d’assurer le bon fonctionnement de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch : le rappel pageBottom ne doit pas exister lors d’un déploiement asynchrone</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Le rappel <span class="codeph"> _satellite.pageBottom()</span> a été trouvé sur la page, ce qui ne doit pas être le cas lorsque Launch est déployé de manière asynchrone. </p> </td> 
   <td colname="col3"> <p>Supprimez le script <span class="codeph">_satellite.pageBottom()</span> pour un fonctionnement correct de Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target : présence du code</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Target doit être défini dans le modèle DOM. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version de Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target : bibliothèque chargée dans la balise &lt;head&gt;</b> </p> <p>Poids : 4 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La bibliothèque Target doit être chargée dans la balise <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
   <td colname="col3"> <p> Vérifiez que la bibliothèque Target est chargée dans la balise <span class="codeph">&lt;head&gt;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
