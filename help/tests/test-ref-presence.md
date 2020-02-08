---
description: Cette référence fournit des informations supplémentaires sur les tests effectués par l’auditeur pour la présence de balises.
seo-description: Cette référence fournit des informations supplémentaires sur les tests effectués par l’auditeur pour la présence de balises.
seo-title: Présence des balises
title: Présence des balises
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Présence des balises

Cette référence fournit des informations supplémentaires sur les tests effectués par l’auditeur pour la présence de balises.

Le vérificateur évalue si la balise existe et si elle se trouve au bon endroit dans le code de votre page.

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
   <td colname="col1"> <p><b>Advertising Cloud - Présence du code</b> </p> <p>Poids : 5 </p> </td> 
   <td colname="col2"> <p> La balise Advertising Cloud n’est pas disponible dans le modèle DOM. </p> </td> 
   <td colname="col3"> <p>Implémentez la balise Advertising Cloud à l’aide de l’extension de lancement de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Marketing Cloud - Pixel de segment implémenté</b> </p> <p>Poids : 5 </p> </td> 
   <td colname="col2"> <p> Mettez à niveau vos pixels de segment Advertising Cloud vers les nouvelles balises d’image uniquement Advertising Cloud. L’utilisation de balises de segment AMO obsolètes peut entraîner une perte de données. </p> </td> 
   <td colname="col3"> <p>Implémentez le pixel de segment Advertising Cloud à l’aide de l’extension de lancement de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics - Chargé dans DOM</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La balise Adobe Analytics n’a pas été détectée. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version d’Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Bibliothèque chargée</b> </p> <p>Poids : 5 </p> <p>Informations supplémentaires: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Résolution des problèmes de la gestion dynamique des balises</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Ajout de code d’en-tête et de pied de page</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Un objet _satellite global est introuvable dans le modèle DOM. La gestion dynamique des balises n’est pas installée ou ne fonctionne pas. </p> </td> 
   <td colname="col3"> <p>Vérifiez que la bibliothèque DTM est implémentée sur la page et n’est pas bloquée par les activités de script suivantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Un code incorporé</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Les sites de production ne doivent charger qu’une seule bibliothèque DTM. </p> </td> 
   <td colname="col3"> <p>Vérifiez que seule la bibliothèque de production est en cours de chargement sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - Le rappel pageBottom existe dans &lt;body&gt;</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le rappel <span class="codeph"> _satellite.pageBottom()</span> est introuvable dans le <span class="codeph"> &lt;body&gt;</span> de la page, ce qui est requis par la gestion dynamique des balises. </p> <p>Ce test échoue si l’ <span class="codeph"> appel pageBottom n’est pas du tout trouvé sur la page ou s’il se trouve dans la balise </span>&lt;head&gt; <span class="codeph"></span> (ou à un autre emplacement inattendu). Elle ne sera transmise que si <span class="codeph"> pageBottom</span> se trouve quelque part dans la balise <span class="codeph"> &lt;body&gt;</span> . S'il ne figure pas du tout sur la page, il ne fonctionnera pas et les deux autres tests <span class="codeph"> PageBottom</span> échoueront également. </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise de fermeture <span class="codeph"> &lt;/body&gt;</span> afin d’assurer la fonctionnalité appropriée de gestion dynamique des balises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - Déclenchement de la balise pageBottom</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La balise DTM <code> pageBottom</code> n’a pas été détectée. </p> <p>Cela peut se produire si l’appel se trouve dans une <code> if</code> instruction qui produit quelque chose de similaire à <code> if (false) {_satellite.pageBottom()}</code>. Ainsi, bien qu’il puisse exister et être correctement placé, la balise peut encore ne pas se déclencher. </p> </td> 
   <td colname="col3"> <p>Installez l’appel DTM <code> pageBottom</code> sur chaque page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Service d’ID Experience Cloud - Présence du code</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Le code du service d’ID d’expérience Cloud est introuvable. Le MCID (Experience Cloud ID) est vivement recommandé pour garantir que vous tirez le meilleur parti de vos solutions Experience Cloud et est essentiel pour la gestion des identifiants dans les solutions Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Installez la version la plus récente de MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Service d’ID Experience Cloud - Présence des cookies</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le <span class="codeph"> cookie AMCV_</span> est introuvable. Vous devez instancier un objet visiteur à partir du code <span class="codeph"> VisitorAPI.js</span> . </p> </td> 
   <td colname="col3"> <p> S’il s’agit d’une implémentation de la gestion dynamique des balises, vérifiez que l’ID AdobeOrg est correctement entré dans l’outil MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Service d’ID Experience Cloud - Valeur MID présente</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La valeur MID est introuvable dans le cookie <span class="codeph"> AMCV_</span> . </p> </td> 
   <td colname="col3"> <p>Testez à nouveau pour vérifier la latence de l’API MCID. Si la condition persiste, contactez le service à la clientèle Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Lancement - Bibliothèque chargée</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Un objet _satellite global est introuvable dans le modèle DOM. Le lancement n’est pas installé ou ne s’exécute pas. </p> </td> 
   <td colname="col3"> <p>Vérifiez que la bibliothèque Launch est implémentée sur la page et n’est pas bloquée par les activités de script suivantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Lancement - Il n’existe pas plusieurs scripts d’intégration</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Il ne doit pas y avoir plusieurs scripts d’intégration chargés sur la page. Les sites de production ne doivent charger qu’une seule bibliothèque de lancement. </p> </td> 
   <td colname="col3"> <p>Vérifiez que seule la bibliothèque de production est en cours de chargement sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - pageBottom callback existe dans &lt;body&gt;</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le rappel <span class="codeph"> _satellite.pageBottom()</span> est introuvable dans le <span class="codeph"> &lt;body&gt;</span> de la page, qui est requis par le lancement. </p> <p>Ce test échoue si l’ <span class="codeph"> appel pageBottom n’est pas du tout trouvé sur la page ou s’il se trouve dans la balise </span>&lt;head&gt; <span class="codeph"></span> (ou à un autre emplacement inattendu). Elle ne sera transmise que si <span class="codeph"> pageBottom</span> se trouve quelque part dans la balise <span class="codeph"> &lt;body&gt;</span> . S'il ne figure pas du tout sur la page, il ne fonctionnera pas et les deux autres tests <span class="codeph"> PageBottom</span> échoueront également. </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise de fermeture <span class="codeph"> &lt;/body&gt;</span> pour garantir la fonctionnalité de lancement appropriée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Lancement - le rappel pageBottom ne doit pas exister lors d’un déploiement asynchrone</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Le rappel <span class="codeph"> _satellite.pageBottom()</span> a été trouvé sur la page, ce qui ne doit pas être le cas lorsque le lancement est déployé de manière asynchrone. </p> </td> 
   <td colname="col3"> <p>Supprimez le script<span class="codeph"> _satellite.pageBottom()</span> pour activer la fonctionnalité de lancement appropriée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Présence du code</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Target doit être défini dans le DOM. </p> </td> 
   <td colname="col3"> <p>Installez la version la plus récente de Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target - Bibliothèque chargée dans &lt;head&gt;</b> </p> <p>Poids : 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La bibliothèque Target doit être chargée dans la balise <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
   <td colname="col3"> <p> Vérifiez que la bibliothèque Target est chargée dans la balise <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>
