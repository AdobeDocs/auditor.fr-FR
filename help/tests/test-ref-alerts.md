---
description: Cette référence fournit des informations supplémentaires sur les alertes affichées par Adobe Experience Platform Auditor pour les tests.
seo-description: Cette référence fournit des informations supplémentaires sur les alertes affichées par Adobe Experience Platform Auditor pour les tests.
seo-title: Alertes
title: Alertes
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: ht
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: ht
source-wordcount: '936'
ht-degree: 100%

---


# Alertes {#alerts}

Cette référence fournit des informations supplémentaires sur les alertes affichées par Adobe Experience Platform Auditor pour les tests.

Les alertes indiquent les problèmes que vous devez connaître, mais qui n’affectent pas votre score. Il s’agit de recommandations de bonnes pratiques qui, dans certains cas, peuvent ne pas s’appliquer à votre mise en œuvre.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Critères </th> 
   <th colname="col3" class="entry"> Recommandation </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud : balise de conversion correcte implémentée</b> </p> <p>Poids : 0 </p> </td> 
   <td colname="col2"> <p>Vérifiez si c’est la balise de conversion appropriée qui est utilisée. </p> <p> <p>Avertissement : l’utilisation des balises de conversion obsolètes de TubeMogul peut entraîner une perte de données. </p> </p> </td> 
   <td colname="col3"> <p>Mettez à niveau vos pixels de conversion vers les nouvelles balises de conversion image seule Advertising Cloud. </p> <p>Cela peut être réalisé facilement avec l’extension Advertising Cloud pour Adobe Experience Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud : balise JS correcte utilisée</b> </p> <p>Poids : 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud doit utiliser les dernières balises JavaScript. </p> </td> 
   <td colname="col3"> <p>Mettez à niveau votre JavaScript Advertising Cloud vers la dernière version. L’utilisation de versions JavaScript obsolètes peut entraîner la perte de fonctionnalités. </p> <p>Pour ce faire, utilisez l’extension Advertising Cloud pour Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud : balise image seule</b> </p> <p>Poids : 0 </p> </td> 
   <td colname="col2"> <p>Le format de pixel d’image Advertising Cloud doit correspondre à l’un des formats recommandés suivants : </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph">http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph">http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph">http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Mettez à niveau vos pixels Advertising Cloud vers les nouvelles balises image seule Advertising Cloud, afin de complètement tirer parti de la fonctionnalité d’Advertising Cloud. </p> <p>Cela peut être réalisé facilement avec l’extension Advertising Cloud pour Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud : pixels de segment, synchronisation DSP activée</b> </p> <p>Poids : 0 </p> </td> 
   <td colname="col2"> <p>Vérifiez si le pixel du segment TubeMogul contient un paramètre de synchronisation DSP, et demandez que ce paramètre soit ajouté au pixel. </p> <p>Le paramètre de synchronisation DSP est déterminé par l’utilisation d’un paramètre de chaîne de requête. </p> <p>SI la balise est déclenchée sur<span class="codeph"> (« https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt; »</span> </p> <p> OU <span class="codeph"> « http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt; »</span> </p> <p> OU <span class="codeph"> « http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;? »</span> </p> <p>ET que la balise contient le paramètre d’URL <span class="codeph"> « sid= »)</span> </p> <p>ALORS vérifiez si le paramètre d’URL <span class="codeph"> « cs=0 »</span> ou<span class="codeph"> « cs=1 »</span> existe et, si ce n’est pas le cas, veillez à ce que <span class="codeph">« cs=1 »</span> soit ajouté à ces pixels afin que les taux de correspondance de l’audience puissent s’améliorer. </p> </td> 
   <td colname="col3"> <p> Ajoutez le paramètre d’URL <span class="codeph"> « cs=1 »</span> à vos pixels Advertising Cloud afin que la synchronisation DSP puisse se produire, ce qui augmente les taux de correspondance d’audience. </p> <p>Cela peut être réalisé très facilement avec l’extension Advertising Cloud pour Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    --> <p><b>DTM : placement du rappel pageBottom</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informations supplémentaires</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamic Tag Management requiert la fonction <span class="codeph">_satellite.pageBottom()</span>. Ajoutez le script intégré juste avant la balise <span class="codeph">&lt;/body&gt;</span> de fermeture afin d’assurer le bon fonctionnement de DTM. </p> <p> <p>Remarque : Il est recommandé que la balise soit la <i>dernière</i> balise dans <span class="codeph"> &lt;body&gt;</span>. Si elle se trouve dans la balise <span class="codeph"> &lt;body&gt;</span>, elle a une chance de fonctionner ; mais comme ce n’est pas la bonne pratique, il se peut qu’elle ne fonctionne pas correctement, ou avec des résultats inattendus ou non souhaités. </p> </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise <span class="codeph">&lt;/body&gt;</span> de fermeture afin d’assurer le bon fonctionnement de DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM : auto-hébergement</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La bibliothèque DTM est hébergée sur l’instance Akamai d’Adobe à l’adresse <span class="filepath">assets.adobedtm.com</span>. </p> <p> L’auto-hébergement est l’approche recommandée pour le chargement de DTM, car cela permet un meilleur contrôle des performances du site web grâce au contrôle du cache, ce qui réduit les dépendances à des scripts tiers, et un meilleur contrôle du processus de publication. Les bibliothèques DTM peuvent être hébergées et gérées par le biais de votre propre hébergement web ou réseau de diffusion de contenu. </p> </td> 
   <td colname="col3"> <p>L’auto-hébergement est l’approche recommandée pour le chargement de DTM sur une page. Bien que l’hébergement de DTM par le biais du réseau de diffusion de contenu Akamai fonctionne dans la plupart des cas, l’auto-hébergement améliore les performances des pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Service Experience Cloud ID : utiliser une seule AdobeOrg</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/id-service/using/intro/id-request.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Dans une implémentation MCID normale, une seule AdobeOrg doit être utilisée. </p> </td> 
   <td colname="col3"> <p>Vérifiez que plusieurs identifiants AdobeOrg existent pour cette implémentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch : placement du rappel pageBottom</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>Platform Launch doit avoir une fonction de rappel <span class="codeph">pageBottom</span> qui doit être définie en dernier dans le corps de la page lors du déploiement synchrone. </p> <p> <p>Remarque : Il est recommandé que la balise soit la <i>dernière</i> balise dans <span class="codeph"> &lt;body&gt;</span>. Si elle se trouve dans la balise <span class="codeph"> &lt;body&gt;</span>, elle a une chance de fonctionner ; mais comme ce n’est pas la bonne pratique, il se peut qu’elle ne fonctionne pas correctement, ou avec des résultats inattendus ou non souhaités. </p> </p> </td> 
   <td colname="col3"> <p>Platform Launch requiert la fonction <span class="codeph"> _satellite.pageBottom()</span> pour les déploiements synchrones. Ajoutez le script intégré juste avant la balise <span class="codeph">&lt;/body&gt;</span> de fermeture afin d’assurer le bon fonctionnement de Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch : auto-hébergement</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Prise en main d’Adobe Experience Platform Launch</a> </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/reference/client-side-info/asynchronous-deployment.html" format="https" scope="external"> Déploiement asynchrone de Platform Launch</a> </p> </td> 
   <td colname="col2"> <p>La bibliothèque Platform Launch est hébergée sur l’instance Akamai d’Adobe à l’adresse <span class="filepath">assets.adobedtm.com</span>. </p> <p>L’auto-hébergement est l’approche recommandée pour le chargement de Platform Launch, car elle permet un meilleur contrôle des performances du site web grâce au contrôle du cache, la réduction des dépendances des scripts tiers et un meilleur contrôle du processus de publication. Les bibliothèques Platform Launch peuvent être hébergées et gérées via votre propre hébergement web ou CDN. </p> </td> 
   <td colname="col3"> <p>Bien que l’hébergement de Platform Launch par le biais du réseau de diffusion de contenu Akamai fonctionne dans la plupart des cas, il est recommandé de mettre en œuvre l’auto-hébergement comme première étape pour améliorer les performances des pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch : doit être déployé de manière asynchrone</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Platform Launch doit être déployé de manière asynchrone pour des performances optimales. </p> </td> 
   <td colname="col3"> <p>Incluez le paramètre « async » dans le script intégré pour garantir un fonctionnement asynchrone correct de Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target : contenu dans mboxDefault</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le contenu doit exister dans mboxDefault lors de l’utilisation d’at.js. </p> </td> 
   <td colname="col3"> <p>Vérifiez que le contenu est disponible. </p> </td> 
  </tr> 
 </tbody> 
</table>

