---
description: informations sur les tests Adobe Experience Platform Auditor
seo-description: informations sur les tests Adobe Experience Platform Auditor
seo-title: Schéma de test 0.0.8
title: Schéma de test 0.0.8
uuid: c62b7169-a650-4650-876f-c254eb57cb25
exl-id: 0313e271-5664-4a34-9e3c-8cb1c61d8b93
translation-type: ht
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: ht
source-wordcount: '2008'
ht-degree: 100%

---

# Schéma de test 0.0.8 {#test-rubric}

## Schéma de test 0.0.8

<!-- Note to writer: Please review the tables on this page for formatting and accuracy. Compare to original file.-->

![](assets/space.png)

## Alertes {#alerts}

Cette référence fournit des informations supplémentaires sur les alertes affichées par Adobe Experience Platform Auditor pour les tests.

Les alertes indiquent les problèmes que vous devez connaître, mais qui n’affectent pas votre score.

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
    <td colname="col1"> <p><b>Advertising Cloud : balise de conversion correcte implémentée</b> </p> <p>Poids : 0 </p> </td> 
    <td colname="col2"> <p>Vérifiez si c’est la balise de conversion appropriée qui est utilisée. </p> <p> <p>Avertissement : l’utilisation des balises de conversion obsolètes de TubeMogul peut entraîner une perte de données. </p> </p> </td> 
    <td colname="col3"> <p>Mettez à niveau vos pixels de conversion vers les nouvelles balises de conversion image seule Advertising Cloud. </p> <p>Cela peut être réalisé facilement avec l’extension Advertising Cloud pour Adobe Experience Platform Launch. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud : balise image seule</b> </p> <p>Poids : 0 </p> </td> 
    <td colname="col2"> <p>Le format de pixel d’image Advertising Cloud doit correspondre à l’un des formats recommandés suivants : </p> <p> 
      <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
       <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph">http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph">http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph">http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
      </ul> </p> </td> 
    <td colname="col3"> <p>Mettez à niveau vos pixels Advertising Cloud vers les nouvelles balises image seule Advertising Cloud, afin de complètement tirer parti de la fonctionnalité d’Advertising Cloud. </p> <p>Cela peut être réalisé facilement avec l’extension Advertising Cloud pour Platform Launch. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud : pixels de segment, synchronisation DSP activée</b> </p> <p>Poids : 0 </p> </td> 
    <td colname="col2"> <p>Vérifiez si le pixel du segment TubeMogul contient un paramètre de synchronisation DSP, et demandez que ce paramètre soit ajouté au pixel. </p> <p>Le paramètre de synchronisation DSP est déterminé par l’utilisation d’un paramètre de chaîne de requête. </p> <p>SI la balise est déclenchée sur<span class="codeph"> (« https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt; »</span> </p> <p> OU <span class="codeph"> « http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt; »</span> </p> <p> OU <span class="codeph"> « http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;? »</span> </p> <p>ET que la balise contient le paramètre d’URL <span class="codeph"> « sid= »)</span> </p> <p>ALORS vérifiez si le paramètre d’URL <span class="codeph"> « cs=0 »</span> ou<span class="codeph"> « cs=1 »</span> existe et, si ce n’est pas le cas, veillez à ce que <span class="codeph">« cs=1 »</span> soit ajouté à ces pixels afin que les taux de correspondance de l’audience puissent s’améliorer. </p> </td> 
    <td colname="col3"> <p> Ajoutez le paramètre d’URL <span class="codeph"> « cs=1 »</span> à vos pixels Advertising Cloud afin que la synchronisation DSP puisse se produire, ce qui augmente les taux de correspondance d’audience. </p> <p>Cela peut être réalisé très facilement avec l’extension Advertising Cloud pour Platform Launch. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM : placement du rappel pageBottom</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informations supplémentaires</a> </p> 
     <!--
       TEa9df69942f404055a64262889c8b21d3 
     --> </td> 
    <td colname="col2"> <p> Dynamic Tag Management requiert la fonction <span class="codeph">_satellite.pageBottom()</span>. </p> <p>Il est recommandé que la balise soit la <i>dernière</i> balise dans <span class="codeph"> &lt;body&gt;</span>. Si elle se trouve dans la balise <span class="codeph">&lt;body&gt;</span>, elle a une chance de fonctionner ; mais comme ce n’est pas la bonne pratique, il se peut qu’elle ne fonctionne pas correctement, ou avec des résultats inattendus ou non souhaités. </p> </td> 
    <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise <span class="codeph">&lt;/body&gt;</span> de fermeture afin d’assurer le bon fonctionnement de DTM. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Service Experience Cloud ID : utiliser une seule AdobeOrg</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/id-service/using/intro/id-request.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p>Dans une implémentation MCID normale, une seule AdobeOrg doit être utilisée. </p> </td> 
    <td colname="col3"> <p>Vérifiez que plusieurs identifiants AdobeOrg existent pour cette implémentation. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target : contenu dans mboxDefault</b> </p> <p>Poids : 0 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Le contenu doit exister dans mboxDefault lors de l’utilisation d’at.js. </p> </td> 
    <td colname="col3"> <p>Vérifiez que le contenu est disponible. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Configuration {#configuration}

Cette référence fournit des informations supplémentaires sur les tests effectués par Platform Auditor concernant la configuration.

Platform Auditor évalue les balises en fonction d’autres règles et des bonnes pratiques recommandées.

<table id="table_A8A1FC360482447185C8460A18426638"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Test </th> 
    <th colname="col2" class="entry"> Critères </th> 
    <th colname="col3" class="entry"> Recommandation </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud : les noms de conversion utilisent uniquement des caractères alphanumériques</b> </p> <p>Poids : 3 </p> </td> 
    <td colname="col2"> <p>Le paramètre <span class="codeph"> ev_conversion_property_name</span> ne doit contenir que des valeurs numériques et décimales SAUF pour le paramètre « <span class="codeph">ev_transid</span> ». (La valeur <span class="codeph"> ev_transid</span> peut contenir du texte ou des valeurs numériques.) </p> <p>Recherchez les pixels <span class="codeph"> everesttech.net</span> qui contiennent un paramètre d’URL commençant par <span class="codeph"> ev_</span>. </p> <p>Exemple : </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47</span> </p> </td> 
    <td colname="col3"> <p> Assurez-vous que les paramètres de propriété de transaction contiennent uniquement des valeurs numériques et décimales. </p> <p> <p>Avertissement : tout autre type de valeur peut entraîner une perte de données. </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud : les noms de conversion utilisent uniquement des caractères autorisés pour les URL</b> </p> <p>Poids : 3 </p> </td> 
    <td colname="col2"> <p> Les noms des propriétés de conversion ne doivent pas contenir d’esperluette ni de point d’interrogation. </p> <p> Exemple : </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>Assurez-vous que les paramètres de propriété de transaction ne contiennent pas d’esperluette ni de point d’interrogation non codé. Ces caractères rompent le format d’URL. </p> <p> <p>Avertissement : les paramètres de propriété contenant une esperluette ou un point d’interrogation non codé (par exemple : <span class="codeph"> ev_formComplete?=1</span> ou <span class="codeph"> ev_formComplete&amp;Submit=1</span>) peuvent entraîner une perte de données. </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud : ID de transaction correctement implémentée</b> </p> <p>Poids : 1 </p> </td> 
    <td colname="col2"> <p> Le nom de propriété <span class="codeph"> ev_transid=</span> ne doit pas être vide. </p> <p>Exemple : </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>Le nom de propriété <span class="codeph"> ev_transid=</span> ne doit pas être laissé sans valeur (<span class="codeph"> ev_transid=</span>). En l’absence de valeur, vous pourriez subir des pertes de données de transaction. Attribuez une valeur à <span class="codeph"> ev_transid=</span> ou supprimez le paramètre du pixel. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics : instancié dans DOM</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/analytics/implementation/home.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Le code Adobe Analytics n’est pas installé ou ne s’exécute pas. Renvoie 0 lorsqu’aucun code Analytics n’est trouvé sur une page web. </p> </td> 
    <td colname="col3"> <p>Vérifiez que la balise Analytics est implémentée sur la page et n’est pas bloquée par les activités de script suivantes. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics : instancié une fois</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/analytics/implementation/home.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Le code Adobe Analytics a été détecté plusieurs fois sur la page. Renvoie 0 lorsqu’aucun code Analytics n’est trouvé sur une page web. </p> </td> 
    <td colname="col3"> <p>Assurez-vous qu’il n’y a qu’une seule balise Analytics sur la page. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics : version la plus récente</b> </p> <p>Poids : 3 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de codes Analytics. Les bibliothèques de codes qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. Renvoie 0 lorsqu’aucun code Analytics n’est trouvé sur une page web. </p> </td>       
    <td colname="col3"> <p>Installez la dernière version de la bibliothèque Analytics. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM : auto-hébergement</b> </p> <p>Poids : 4 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> La bibliothèque DTM est hébergée sur l’instance Akamai d’Adobe à l’adresse <span class="filepath">assets.adobedtm.com</span>. </p> <p> L’auto-hébergement est l’approche recommandée pour le chargement de DTM, car cela permet un meilleur contrôle des performances du site web grâce au contrôle du cache, ce qui réduit les dépendances à des scripts tiers, et un meilleur contrôle du processus de publication. Les bibliothèques DTM peuvent être hébergées et gérées par le biais de votre propre hébergement web ou réseau de diffusion de contenu. </p> </td> 
    <td colname="col3"> <p>L’auto-hébergement est l’approche recommandée pour le chargement de DTM sur une page. Bien que l’hébergement de DTM par le biais du réseau de diffusion de contenu Akamai fonctionne dans la plupart des cas, l’auto-hébergement améliore les performances des pages. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM : les balises tierces se chargent de manière asynchrone une fois le modèle DOM prêt</b> </p> <p>Poids : 3 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/resources/load-order.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p>Pour trouver un équilibre entre une bonne expérience utilisateur et une collecte de données précise, les balises tierces doivent être déclenchées dès que le modèle DOM est prêt. Cela permet de s’assurer que ces scripts de suivi s’exécutent sans affecter la fonctionnalité du site. </p> </td> 
    <td colname="col3"> <p>Résolvez ce problème en ajustant toutes les règles qui exécutent les pixels tiers pour qu’ils se déclenchent dès que le modèle DOM est prêt. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Service Experience Cloud ID : dernière version</b> </p> <p>Poids : 2 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/tools/macid.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de codes du service d’identification des visiteurs, <span class="codeph"> visitorAPI.js</span>. Les bibliothèques de codes qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. </p> </td> 
    <td colname="col3"> <p>Installez la dernière version de la bibliothèque du service d’identification des visiteurs. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target : version la plus récente</b> </p> <p>Poids : 2 </p> <p><a href="https://marketing.adobe.com/resources/help/fr_FR/dtm/target/" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de codes Target. Les bibliothèques de codes qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. </p> </td> 
    <td colname="col3"> <p>Installez la dernière version de la bibliothèque Target. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target : mboxDefault précède mboxCreate </b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p>L’utilisation correcte de <span class="codeph"> mboxCreate</span> ressemble à ceci : </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
    <td colname="col3"> <p>Veillez à inclure une balise <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> avant d’appeler <span class="codeph"> mboxCreate()</span>. at.js ne le fera pas à votre place. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target : DOCTYPE valide</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Un DOCTYPE non valide a été détecté. Aucune mbox ne sera déclenchée dans ce scénario. </p> <p>Pour at.js, le DOCTYPE doit être en mode standard, sinon Target ne fonctionnera pas. </p> </td> 
    <td colname="col3"> <p>Mettez à jour le DOCTYPE sur la page. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Cohérence des balises {#tag-consistency}

Cette référence fournit des informations supplémentaires sur les tests effectués par Platform Auditor pour assurer la cohérence des balises.

Platform Auditor évalue si les balises sont cohérentes entre les URL.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Test </th> 
    <th colname="col2" class="entry"> Critères </th> 
    <th colname="col3" class="entry"> Recommandation </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Analytics : version de code cohérente </b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/analytics/implementation/home.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Plusieurs versions du code Analytics ont été trouvées. </p> </td> 
    <td colname="col3"> <p>Remplacez toutes les instances d’Analytics par la version actuelle. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Présence des balises {#tag-presence}

Cette référence fournit des informations supplémentaires sur les tests effectués par Platform Auditor pour assurer la présence des balises.

Platform Auditor évalue si la balise existe et si elle se trouve au bon endroit dans le code de votre page, etc.

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
    <td colname="col3"> <p>Implémentez la balise Advertising Cloud à l’aide de l’extension Advertising Cloud pour Platform Launch. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud : pixel de segment implémenté</b> </p> <p>Poids : 5 </p> </td> 
    <td colname="col2"> <p> Mettez à niveau vos pixels de segment Advertising Cloud vers les nouvelles balises image seule Advertising Cloud. L’utilisation de balises de segment AMO obsolètes peut entraîner une perte de données. </p> </td> 
    <td colname="col3"> <p>Implémentez le pixel de segment Advertising Cloud à l’aide de l’extension Advertising Cloud pour Platform Launch. </p> </td> 
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
    <td colname="col2"> <p> La balise <span class="codeph"> pageBottom</span> de DTM n’a pas été détectée. </p> <p>Cela peut se produire si l’appel se trouve dans une instruction <span class="codeph">if</span> qui donne un résultat similaire à <span class="codeph">if (false) {_satellite.pageBottom()}</span>. Ainsi, bien qu’il puisse exister et être correctement placé, la balise peut quand même ne pas se déclencher. </p> </td> 
    <td colname="col3"> <p>Installez l’appel <span class="codeph">pageBottom</span> de DTM sur chaque page. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Service Experience Cloud ID : présence du cookie</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/tools/macid.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Le cookie <span class="codeph">AMCV_</span> est introuvable. Vous devez instancier un objet visiteur à partir du code <span class="codeph"> VisitorAPI.js</span>. </p> </td> 
    <td colname="col3"> <p> S’il s’agit d’une implémentation de DTM, vérifiez que l’identifiant AdobeOrg est correctement saisi dans l’outil MCID. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Service Experience Cloud ID : présence de la valeur MID</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/id-service/using/intro/cookies.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> La valeur mid est introuvable dans le cookie <span class="codeph"> AMCV_</span>. </p> </td> 
    <td colname="col3"> <p>Testez à nouveau pour vérifier la latence de l’API MCID. Si la condition persiste, contactez l’assistance clientèle Adobe. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Service Experience Cloud ID : doit être installé</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/id-service/using/intro/overview.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
    <td colname="col2"> <p> Le code du service Experience Cloud ID est introuvable. L’ECID est vivement recommandé pour vous assurer de tirer le meilleur parti de vos solutions Experience Cloud et il est essentiel pour la gestion des identifiants dans les solutions EC. </p> </td> 
    <td colname="col3"> <p>Installez la dernière version de MCID. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target : bibliothèque chargée dans la balise &lt;head&gt;</b> </p> <p>Poids : 4 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informations supplémentaires</a> </p> 
     <!--
       TE61c380082a4b4706b28a84aa047599a7 
     --> </td> 
    <td colname="col2"> <p> La bibliothèque Target doit être chargée dans la balise <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
    <td colname="col3"> <p> Vérifiez que la bibliothèque Target est chargée dans la balise <span class="codeph">&lt;head&gt;</span>. </p> </td> 
   </tr> 
  </tbody> 
</table>
