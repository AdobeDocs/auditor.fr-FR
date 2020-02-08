---
description: valeur nulle
seo-description: valeur nulle
seo-title: Rubrique d'essai 1.0.1
title: Rubrique d'essai 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
translation-type: tm+mt
source-git-commit: 712d0768e5e5394372293bf8231c91489519bcd1

---


# Rubrique d&#39;essai 1.0.1{#test-rubric}

## Rubrique d&#39;essai 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## Alertes {#alerts}

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
      1.0.1 
    </draft-comment> <p><b>DTM - placement du rappel pageBottom</b> </p> <p>Poids : 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Informations supplémentaires</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>La gestion dynamique des balises requiert la fonction <span class="codeph"> _satellite.pageBottom()</span> . Ajoutez le script intégré juste avant la balise body de fermeture afin d’assurer la fonctionnalité appropriée de gestion dynamique des balises. </p> <p> <p>Remarque : Il est recommandé que la balise soit la <i>dernière</i> balise dans le <span class="codeph"> &lt;body&gt;</span>. S’il se trouve dans la balise <span class="codeph"> &lt;body&gt;</span> , il a une chance de fonctionner, mais comme il n’est pas recommandé, il peut fonctionner incorrectement ou avec des résultats inattendus ou non souhaités. </p> </p> </td> 
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
      1.0.1 
    </draft-comment> <p><b>Lancement - placement du rappel pageBottom</b> </p> <p>Poids : 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informations supplémentaires</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Une fonction de <span class="codeph"> </span>rappel pageBottom du lancement doit être définie en dernier dans le corps de la page en cas de déploiement synchrone. </p> <p> <p>Remarque : Il est recommandé que la balise soit la <i>dernière</i> balise dans le <span class="codeph"> &lt;body&gt;</span>. S’il se trouve dans la balise <span class="codeph"> &lt;body&gt;</span> , il a une chance de fonctionner, mais comme il n’est pas recommandé, il peut fonctionner incorrectement ou avec des résultats inattendus ou non souhaités. </p> </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise de fermeture <span class="codeph"> &lt;/body&gt;</span> afin d’assurer la fonctionnalité appropriée de gestion dynamique des balises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Lancement - Auto-hébergement</b> </p> <p>Poids : 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>La bibliothèque de lancement est hébergée sur l’instance Akamai d’Adobe à l’adresse <span class="filepath"> .adobedtm.com</span>. </p> <p>L’auto-hébergement est l’approche recommandée pour le chargement du lancement, car elle permet un meilleur contrôle des performances du site Web grâce au contrôle du cache, la réduction des dépendances des scripts tiers et un meilleur contrôle du processus de publication. Les bibliothèques de lancement peuvent être hébergées et gérées via votre propre hébergement Web ou CDN. </p> </td> 
   <td colname="col3"> <p>Bien que l’hébergement de lancement via le CDN Akamai fonctionne dans la plupart des cas, il est recommandé de mettre en oeuvre l’auto-hébergement comme première étape pour améliorer les performances des pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Lancement : doit être déployé de manière asynchrone</b> </p> <p>Poids : 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
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

## Configuration {#configuration}

Cette référence fournit des informations supplémentaires sur les tests effectués par l’auditeur pour la configuration.

Les tests de configuration recherchent des paramètres, des valeurs ou des conflits potentiels spécifiques dans votre implémentation. Le vérificateur évalue les balises en fonction d’autres règles et des bonnes pratiques recommandées.

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Les noms de conversion utilisent uniquement des caractères alphanumériques.</b> </p> <p>Poids : 3 </p> </td> 
   <td colname="col2"> <p>Le paramètre <span class="codeph"> ev_conversion_property_name</span> ne doit contenir que des valeurs numériques et décimales SAUF pour le paramètre "<span class="codeph"> ev_transid</span>" (la valeur <span class="codeph"> ev_transid</span> peut contenir du texte ou des valeurs numériques). </p> <p>Recherchez les pixels <span class="codeph"> everesttech.net</span> qui contiennent un paramètre d’URL commençant par <span class="codeph"> ev_</span>. </p> <p>Exemple : </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Assurez-vous que les paramètres de propriété de transaction contiennent uniquement des valeurs numériques et décimales. </p> <p> <p>Avertissement :  Tout autre type de valeur peut entraîner une perte de données. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Les noms de conversion utilisent des caractères sécurisés pour les URL</b> </p> <p>Poids : 3 </p> </td> 
   <td colname="col2"> <p> Les noms des propriétés de conversion ne doivent pas contenir d’esperluette ou de point d’interrogation. </p> <p> Exemple : </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Assurez-vous que les paramètres de propriété de transaction ne contiennent pas d’esperluette ni de point d’interrogation non codés. Elles rompent le format d’URL. </p> <p> <p>Avertissement : Paramètres de propriété contenant une esperluette non codée ou un point d’interrogation (par exemple : <span class="codeph"> ev_formComplete?=1</span> ou <span class="codeph"> ev_formComplete&amp;Submit=1</span>), peut entraîner une perte de données. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - ID de transaction implémenté correctement</b> </p> <p>Poids : 1 </p> </td> 
   <td colname="col2"> <p> Le nom de propriété <span class="codeph"> ev_transid=</span> ne doit pas être vide. </p> <p>Exemple : </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Le nom de propriété <span class="codeph"> ev_transid=</span> ne doit pas être laissé sans valeur (<span class="codeph"> ev_transid=</span>). S’il n’y a pas de valeur, il peut y avoir perte de données de transaction. Attribuez une valeur à <span class="codeph"> ev_transid=</span> ou supprimez le paramètre du pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Instancié dans DOM</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le code Adobe Analytics n’est pas installé ou ne s’exécute pas. Renvoie 0 lorsqu’aucun code d’analyse n’est trouvé sur une page Web. </p> </td> 
   <td colname="col3"> <p>Vérifiez que la balise Analytics est implémentée sur la page et n’est pas bloquée par les activités de script suivantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Instancié une fois</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le code Adobe Analytics a été détecté plusieurs fois sur la page.. Renvoie 0 lorsqu’aucun code d’analyse n’est trouvé sur une page Web. </p> </td> 
   <td colname="col3"> <p>Assurez-vous qu’il n’y a qu’une seule balise Analytics sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Dernière version</b> </p> <p>Poids : 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de code Analytics. Les bibliothèques de code qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. Renvoie 0 lorsqu’aucun code d’analyse n’est trouvé sur une page Web. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version de la bibliothèque Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Les balises tierces se chargent de manière asynchrone une fois le modèle DOM prêt</b> </p> <p>Poids : 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Pour trouver un équilibre entre une bonne expérience utilisateur et la collecte de données précises, les balises tierces doivent être déclenchées dès que le modèle DOM est prêt. Cela permet de s’assurer que ces scripts de suivi s’exécutent sans affecter la fonctionnalité du site. </p> </td> 
   <td colname="col3"> <p>Résolvez ce problème en ajustant toutes les règles qui exécutent les pixels tiers pour qu’ils se déclenchent à l’aide de l’outil DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Service d’ID Experience Cloud - Dernière version</b> </p> <p>Poids : 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de code du service d’identification des visiteurs, <span class="codeph"> visitorAPI.js</span>. Les bibliothèques de code qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version de la bibliothèque du service d’identification des visiteurs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Lancement - Dernière version</b> </p> <p>Poids : 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Ces pages n’exécutent pas la dernière version de la bibliothèque de codes de lancement (Turbine). Les bibliothèques de code qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. </p> </td> 
   <td colname="col3"> <p> Mettez à jour la bibliothèque de lancement en recréant et en publiant la bibliothèque de lancement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - Dernière version</b> </p> <p>Poids : 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de code Target. Les bibliothèques de code qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version de la bibliothèque Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - mboxDefault précède mboxCreate </b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>L’utilisation appropriée de <span class="codeph"> mboxCreate</span> ressemble à ceci : </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Contenu du client—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Veillez à inclure une balise <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> avant d’appeler <span class="codeph"> mboxCreate()</span>. at.js ne vous en ajoutera pas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - DOCTYPE valide</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Un DOCTYPE non valide a été détecté. Aucune mbox ne sera déclenchée dans ce scénario. </p> <p>Pour at.js, le DOCTYPE doit être en mode Standards, sinon Target ne fonctionnera pas. </p> </td> 
   <td colname="col3"> <p>Mettez à jour DOCTYPE sur la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cohérence des balises {#tag-consistency}

Cette référence fournit plus d’informations sur les tests effectués par l’auditeur pour assurer la cohérence des balises.

Les tests de cohérence de l&#39;auditeur recherchent les incohérences entre toutes les pages numérisées. Il s’agit de valeurs ou de configurations qui doivent être identiques sur toutes les pages du site pour garantir une collecte de données précise.

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Version de code cohérente </b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/choose-implementation-method.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Plusieurs versions du code Analytics ont été trouvées. </p> </td> 
   <td colname="col3"> <p>Remplacez toutes les instances d’Analytics par la version actuelle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Présence des balises {#tag-presence}

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Présence du code</b> </p> <p>Poids : 5 </p> </td> 
   <td colname="col2"> <p> La balise Advertising Cloud n’est pas disponible dans le modèle DOM. </p> </td> 
   <td colname="col3"> <p>Implémentez la balise Advertising Cloud à l’aide de l’extension de lancement de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Marketing Cloud - Pixel de segment implémenté</b> </p> <p>Poids : 5 </p> </td> 
   <td colname="col2"> <p> Mettez à niveau vos pixels de segment Advertising Cloud vers les nouvelles balises d’image uniquement Advertising Cloud. L’utilisation de balises de segment AMO obsolètes peut entraîner une perte de données. </p> </td> 
   <td colname="col3"> <p>Implémentez le pixel de segment Advertising Cloud à l’aide de l’extension de lancement de Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Chargé dans DOM</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La balise Adobe Analytics n’a pas été détectée. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version d’Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Bibliothèque chargée</b> </p> <p>Poids : 5 </p> <p>Informations supplémentaires: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/c_Troubleshooting.html" format="html" scope="external"> Résolution des problèmes de la gestion dynamique des balises</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Ajout de code d’en-tête et de pied de page</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Un objet _satellite global est introuvable dans le modèle DOM. La gestion dynamique des balises n’est pas installée ou ne fonctionne pas. </p> </td> 
   <td colname="col3"> <p>Vérifiez que la bibliothèque DTM est implémentée sur la page et n’est pas bloquée par les activités de script suivantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Un code incorporé</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Les sites de production ne doivent charger qu’une seule bibliothèque DTM. </p> </td> 
   <td colname="col3"> <p>Vérifiez que seule la bibliothèque de production est en cours de chargement sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Le rappel pageBottom existe dans &lt;body&gt;</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le rappel <span class="codeph"> _satellite.pageBottom()</span> est introuvable dans le <span class="codeph"> &lt;body&gt;</span> de la page, ce qui est requis par la gestion dynamique des balises. </p> <p>Ce test échoue si l’ <span class="codeph"> appel pageBottom n’est pas du tout trouvé sur la page ou s’il se trouve dans la balise </span>&lt;head&gt; <span class="codeph"></span> (ou à un autre emplacement inattendu). Elle ne sera transmise que si <span class="codeph"> pageBottom</span> se trouve quelque part dans la balise <span class="codeph"> &lt;body&gt;</span> . S'il ne figure pas du tout sur la page, il ne fonctionnera pas et les deux autres tests <span class="codeph"> PageBottom</span> échoueront également. </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise de fermeture <span class="codeph"> &lt;/body&gt;</span> afin d’assurer la fonctionnalité appropriée de gestion dynamique des balises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - Déclenchement de la balise pageBottom</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La balise <span class="codeph"> pageBottom</span> de la gestion dynamique des balises n’a pas été détectée. </p> <p>Cela peut se produire si l’appel se trouve dans une instruction <span class="codeph"> if</span> qui donne un résultat similaire à <span class="codeph"> if (false) {_satellite.pageBottom()}</span>. Ainsi, bien qu’il puisse exister et être correctement placé, la balise peut encore ne pas se déclencher. </p> </td> 
   <td colname="col3"> <p>Installez l’appel pageBottom <span class="codeph"></span> de la gestion dynamique des balises sur chaque page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Service d’ID Experience Cloud - Présence du code</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-overview.htmlimplementation-guides.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Le code du service d’ID d’expérience Cloud est introuvable. Le MCID (Experience Cloud ID) est vivement recommandé pour garantir que vous tirez le meilleur parti de vos solutions Experience Cloud et est essentiel pour la gestion des identifiants dans les solutions Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Installez la version la plus récente de MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Service d’ID Experience Cloud - Présence des cookies</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-implementation-guides.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le <span class="codeph"> cookie AMCV_</span> est introuvable. Vous devez instancier un objet visiteur à partir du code <span class="codeph"> VisitorAPI.js</span> . </p> </td> 
   <td colname="col3"> <p> S’il s’agit d’une implémentation de la gestion dynamique des balises, vérifiez que l’ID AdobeOrg est correctement entré dans l’outil MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Service d’ID Experience Cloud - Valeur MID présente</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_cookies.html#concept_37156268512445F287CD4BBB2839FFAA__section_C55AF54828DC4CCE89F6118655D694C8" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> La valeur MID est introuvable dans le cookie <span class="codeph"> AMCV_</span> . </p> </td> 
   <td colname="col3"> <p>Testez à nouveau pour vérifier la latence de l’API MCID. Si la condition persiste, contactez le service à la clientèle Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Lancement - Bibliothèque chargée</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Un objet _satellite global est introuvable dans le modèle DOM. Le lancement n’est pas installé ou ne s’exécute pas. </p> </td> 
   <td colname="col3"> <p>Vérifiez que la bibliothèque Launch est implémentée sur la page et n’est pas bloquée par les activités de script suivantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Lancement - Il n’existe pas plusieurs scripts d’intégration</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Il ne doit pas y avoir plusieurs scripts d’intégration chargés sur la page. Les sites de production ne doivent charger qu’une seule bibliothèque de lancement. </p> </td> 
   <td colname="col3"> <p>Vérifiez que seule la bibliothèque de production est en cours de chargement sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - pageBottom callback existe dans &lt;body&gt;</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le rappel <span class="codeph"> _satellite.pageBottom()</span> est introuvable dans le <span class="codeph"> &lt;body&gt;</span> de la page, qui est requis par le lancement. </p> <p>Ce test échoue si l’ <span class="codeph"> appel pageBottom n’est pas du tout trouvé sur la page ou s’il se trouve dans la balise </span>&lt;head&gt; <span class="codeph"></span> (ou à un autre emplacement inattendu). Elle ne sera transmise que si <span class="codeph"> pageBottom</span> se trouve quelque part dans la balise <span class="codeph"> &lt;body&gt;</span> . S'il ne figure pas du tout sur la page, il ne fonctionnera pas et les deux autres tests <span class="codeph"> PageBottom</span> échoueront également. </p> </td> 
   <td colname="col3"> <p>Ajoutez le script intégré juste avant la balise de fermeture <span class="codeph"> &lt;/body&gt;</span> pour garantir la fonctionnalité de lancement appropriée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Lancement - le rappel pageBottom ne doit pas exister lors d’un déploiement asynchrone</b> </p> <p>Poids : 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Bibliothèque chargée dans &lt;head&gt;</b> </p> <p>Poids : 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informations supplémentaires</a> </p> 
    <draft-comment>
      TE61c380082a4b4706b28a84aa047599a7 
    </draft-comment> </td> 
   <td colname="col2"> <p> La bibliothèque Target doit être chargée dans la balise <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
   <td colname="col3"> <p> Vérifiez que la bibliothèque Target est chargée dans la balise <span class="codeph"> &lt;head&gt;</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

