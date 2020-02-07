---
description: Cette référence fournit des informations supplémentaires sur les alertes affichées par l’auditeur pour les tests.
seo-description: Cette référence fournit des informations supplémentaires sur les alertes affichées par l’auditeur pour les tests.
seo-title: Alertes
title: Alertes
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 762ff31ca4d5ed69d1b813589e419c51a40d5920

---


# Alertes{#alerts}

Cette référence fournit des informations supplémentaires sur les alertes affichées par l’auditeur pour les tests.

Les alertes indiquent les problèmes que vous devez connaître, mais qui n’affectent pas votre score. Il s’agit de recommandations de bonnes pratiques qui, dans certains cas, peuvent ne pas s’appliquer à votre mise en oeuvre.

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
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Balise de conversion correcte implémentée</b> </p> <p>Poids : 0 </p> </td> 
   <td colname="col2"> <p>Vérifiez si la balise de conversion appropriée est utilisée. </p> <p> <p>Avertissement :  L’utilisation des balises de conversion obsolètes de TubeMogul peut entraîner une perte de données. </p> </p> </td> 
   <td colname="col3"> <p>Mettez à niveau vos pixels de conversion vers les nouvelles balises de conversion Image seule Advertising Cloud. </p> <p>Cela peut être réalisé facilement avec l’extension de lancement de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Balise JS correcte utilisée</b> </p> <p>Poids : 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud doit utiliser les dernières balises JavaScript. </p> </td> 
   <td colname="col3"> <p>Mettez à niveau votre code JavaScript Advertising Cloud vers la dernière version. L’utilisation de versions JavaScript obsolètes peut entraîner la perte de fonctionnalités. </p> <p>Pour ce faire, utilisez l’extension de lancement de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Balise Image uniquement</b> </p> <p>Poids : 0 </p> </td> 
   <td colname="col2"> <p>Le format de pixel d’image Advertising Cloud doit correspondre à l’un des formats recommandés suivants : </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Mettez à niveau vos pixels Advertising Cloud vers les nouvelles balises image uniquement Advertising Cloud, afin de tirer parti de la fonctionnalité complète Advertising Cloud. </p> <p>Cela peut être réalisé facilement avec l’extension de lancement de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Segment Pixels DSP Synchronisation activée</b> </p> <p>Poids : 0 </p> </td> 
   <td colname="col2"> <p>Vérifiez si le pixel du segment TubeMogul contient un paramètre de synchronisation DSP, et demandez que ce paramètre soit ajouté au pixel. </p> <p>Le paramètre de synchronisation DSP est déterminé par l’utilisation d’un paramètre de chaîne de requête. </p> <p>SI la balise est déclenchée sur<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;")</span> </p> <p> OU <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OU <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>ET la balise contient le paramètre d’URL <span class="codeph"> "sid=")</span> </p> <p>Vérifiez ensuite si le paramètre d’URL <span class="codeph"> "cs=0"</span> ou<span class="codeph"> "cs=1"</span> existe et, si vous ne le recommandez pas, <span class="codeph"> "cs=1"</span> doit être ajouté à ces pixels afin que les taux de correspondance de l’audience puissent s’améliorer. </p> </td> 
   <td colname="col3"> <p> Ajoutez le paramètre d’URL <span class="codeph"> "cs=1"</span> à vos pixels Advertising Cloud afin que la synchronisation DSP puisse se produire, ce qui augmente les taux de correspondance d’audience. </p> <p>Cela peut être réalisé facilement avec l’extension de lancement de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM - placement du rappel pageBottom</b> </p> <p>Poids : 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Informations supplémentaires</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>La gestion dynamique des balises requiert la fonction <span class="codeph"> _satellite.pageBottom()</span> . Ajoutez le script intégré juste avant la balise de fermeture <span class="codeph"> &lt;/body&gt;</span> afin d’assurer la fonctionnalité appropriée de gestion dynamique des balises. </p> <p> <p>Remarque : Il est recommandé que la balise soit la <i>dernière</i> balise dans le <span class="codeph"> &lt;body&gt;</span>. S’il se trouve dans la balise <span class="codeph"> &lt;body&gt;</span> , il a une chance de fonctionner, mais comme il n’est pas recommandé, il peut fonctionner incorrectement ou avec des résultats inattendus ou non souhaités. </p> </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise de fermeture <span class="codeph"> &lt;/body&gt;</span> afin d’assurer la fonctionnalité appropriée de gestion dynamique des balises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Gestion dynamique des balises - Auto-hébergé</b> </p> <p>Poids : 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La bibliothèque DTM est hébergée sur l’instance Akamai d’Adobe à l’adresse <span class="filepath"> .adobedtm.com</span>. </p> <p> L’auto-hébergement est l’approche recommandée pour le chargement de la gestion dynamique des balises, car elle permet un meilleur contrôle des performances du site Web grâce au contrôle du cache, la réduction des dépendances des scripts tiers et un meilleur contrôle du processus de publication. Les bibliothèques de gestion dynamique des balises peuvent être hébergées et gérées via votre propre hébergement Web ou CDN. </p> </td> 
   <td colname="col3"> <p>L’auto-hébergement est l’approche recommandée pour charger la gestion dynamique des balises sur une page. Bien que l’hébergement de la gestion dynamique des balises via le CDN Akamai fonctionne dans la plupart des cas, l’auto-hébergement améliore les performances des pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Service d’ID Experience Cloud - N’utiliser qu’un seul AdobeOrg</b> </p> <p>Poids : 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Dans une implémentation MCID normale, une seule AdobeOrg doit être utilisée. </p> </td> 
   <td colname="col3"> <p>Vérifiez que plusieurs ID AdobeOrg existent pour cette implémentation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Lancement - placement du rappel pageBottom</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Informations supplémentaires</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Une fonction de <span class="codeph"> </span>rappel pageBottom doit être définie en dernier dans le corps de la page lors du lancement synchrone. </p> <p> <p>Remarque : Il est recommandé que la balise soit la <i>dernière</i> balise dans le <span class="codeph"> &lt;body&gt;</span>. S’il se trouve dans la balise <span class="codeph"> &lt;body&gt;</span> , il a une chance de fonctionner, mais comme il n’est pas recommandé, il peut fonctionner incorrectement ou avec des résultats inattendus ou non souhaités. </p> </p> </td> 
   <td colname="col3"> <p>Le lancement requiert la fonction <span class="codeph"> _satellite.pageBottom()</span> pour les déploiements synchrones. Ajoutez le script intégré juste avant la balise de fermeture <span class="codeph"> &lt;/body&gt;</span> pour garantir la fonctionnalité de lancement appropriée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Lancement - Auto-hébergement</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Prise en main du lancement</a> </p> <p><a href="https://docs.adobelaunch.com/client-side-information/asynchronous-deployment" format="https" scope="external"> Lancement d’un déploiement asynchrone</a> </p> </td> 
   <td colname="col2"> <p>La bibliothèque de lancement est hébergée sur l’instance Akamai d’Adobe à l’adresse <span class="filepath"> .adobedtm.com</span>. </p> <p>L’auto-hébergement est l’approche recommandée pour le chargement du lancement, car elle permet un meilleur contrôle des performances du site Web grâce au contrôle du cache, la réduction des dépendances des scripts tiers et un meilleur contrôle du processus de publication. Les bibliothèques de lancement peuvent être hébergées et gérées via votre propre hébergement Web ou CDN. </p> </td> 
   <td colname="col3"> <p>Bien que l’hébergement de lancement via le CDN Akamai fonctionne dans la plupart des cas, il est recommandé de mettre en oeuvre l’auto-hébergement comme première étape pour améliorer les performances des pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Lancement : doit être déployé de manière asynchrone</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Le lancement doit être déployé de manière asynchrone pour des performances optimales. </p> </td> 
   <td colname="col3"> <p>Inclure le paramètre async dans le script intégré pour garantir la fonctionnalité de lancement asynchrone appropriée </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Contenu dans mboxDefault</b> </p> <p>Poids : 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le contenu doit exister dans mboxDefault lors de l’utilisation d’at.js. </p> </td> 
   <td colname="col3"> <p>Vérifiez que le contenu est disponible. </p> </td> 
  </tr> 
 </tbody> 
</table>

