---
description: Cette référence fournit des informations supplémentaires sur les tests effectués par Adobe Experience Platform Auditor pour la configuration.
seo-description: Cette référence fournit des informations supplémentaires sur les tests effectués par Adobe Experience Platform Auditor pour la configuration.
seo-title: Configuration
title: Configuration
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 100%

---


# Configuration

Cette référence fournit des informations supplémentaires sur les tests effectués par Adobe Experience Platform Auditor pour la configuration.

Les tests de configuration recherchent des paramètres, des valeurs ou des conflits potentiels spécifiques dans votre implémentation. Platform Auditor évalue les balises en fonction d’autres règles et des bonnes pratiques recommandées.

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
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud : les noms de conversion utilisent uniquement des caractères alphanumériques</b> </p> <p>Poids : 3 </p> </td> 
   <td colname="col2"> <p>Le paramètre <span class="codeph"> ev_conversion_property_name</span> ne doit contenir que des valeurs numériques et décimales SAUF pour le paramètre « <span class="codeph">ev_transid</span> ». (La valeur <span class="codeph"> ev_transid</span> peut contenir du texte ou des valeurs numériques.) </p> <p>Recherchez les pixels <span class="codeph"> everesttech.net</span> qui contiennent un paramètre d’URL commençant par <span class="codeph"> ev_</span>. </p> <p>Exemple : </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Assurez-vous que les paramètres de propriété de transaction contiennent uniquement des valeurs numériques et décimales. </p> <p> <p>Avertissement : tout autre type de valeur peut entraîner une perte de données. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud : les noms de conversion utilisent uniquement des caractères autorisés pour les URL</b> </p> <p>Poids : 3 </p> </td> 
   <td colname="col2"> <p> Les noms des propriétés de conversion ne doivent pas contenir d’esperluette ni de point d’interrogation. </p> <p> Exemple : </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Assurez-vous que les paramètres de propriété de transaction ne contiennent pas d’esperluette ni de point d’interrogation non codé. Ces caractères rompent le format d’URL. </p> <p> <p>Avertissement : les paramètres de propriété contenant une esperluette ou un point d’interrogation non codé (par exemple : <span class="codeph"> ev_formComplete?=1</span> ou <span class="codeph"> ev_formComplete&amp;Submit=1</span>) peuvent entraîner une perte de données. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud : ID de transaction correctement implémentée</b> </p> <p>Poids : 1 </p> </td> 
   <td colname="col2"> <p> Le nom de propriété <span class="codeph"> ev_transid=</span> ne doit pas être vide. </p> <p>Exemple : </p> <p> <span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Le nom de propriété <span class="codeph"> ev_transid=</span> ne doit pas être laissé sans valeur (<span class="codeph"> ev_transid=</span>). En l’absence de valeur, vous pourriez subir des pertes de données de transaction. Attribuez une valeur à <span class="codeph"> ev_transid=</span> ou supprimez le paramètre du pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics : instancié dans DOM</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/analytics/implementation/home.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le code Adobe Analytics n’est pas installé ou ne s’exécute pas. Renvoie 0 lorsqu’aucun code Analytics n’est trouvé sur une page web. </p> </td> 
   <td colname="col3"> <p>Vérifiez que la balise Analytics est implémentée sur la page et n’est pas bloquée par les activités de script suivantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics : instancié une fois</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/analytics/implementation/home.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Le code Adobe Analytics a été détecté plusieurs fois sur la page. Renvoie 0 lorsqu’aucun code Analytics n’est trouvé sur une page web. </p> </td> 
   <td colname="col3"> <p>Assurez-vous qu’il n’y a qu’une seule balise Analytics sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics : version la plus récente</b> </p> <p>Poids : 3 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de codes Analytics. Les bibliothèques de codes qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. Renvoie 0 lorsqu’aucun code Analytics n’est trouvé sur une page web. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version de la bibliothèque Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM : les balises tierces se chargent de manière asynchrone une fois le modèle DOM prêt</b> </p> <p>Poids : 3 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/resources/load-order.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Pour trouver un équilibre entre une bonne expérience utilisateur et une collecte de données précise, les balises tierces doivent être déclenchées dès que le modèle DOM est prêt. Cela permet de s’assurer que ces scripts de suivi s’exécutent sans affecter la fonctionnalité du site. </p> </td> 
   <td colname="col3"> <p>Résolvez ce problème en ajustant toutes les règles qui exécutent les pixels tiers pour qu’ils se déclenchent dès que le modèle DOM est prêt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Service Experience Cloud ID : dernière version</b> </p> <p>Poids : 2 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/using/tools/macid.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de codes du service d’identification des visiteurs, <span class="codeph"> visitorAPI.js</span>. Les bibliothèques de codes qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version de la bibliothèque du service d’identification des visiteurs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch : version la plus récente</b> </p> <p>Poids : 2 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>Ces pages n’exécutent pas la dernière version de la bibliothèque de codes Platform Launch (Turbine). Les bibliothèques de codes qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. </p> </td> 
   <td colname="col3"> <p> Mettez à jour la bibliothèque Platform Launch en la recréant et en la publiant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target : version la plus récente</b> </p> <p>Poids : 2 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/dtm/implementing/target/update-target-tool.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Vos pages n’exécutent pas la dernière version de la bibliothèque de codes Target. Les bibliothèques de codes qui alimentent les technologies Experience Cloud sont constamment mises à jour et modifiées afin de tirer parti des améliorations de performances et de fournir les dernières fonctionnalités. </p> </td> 
   <td colname="col3"> <p>Installez la dernière version de la bibliothèque Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target : mboxDefault précède mboxCreate </b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/content/help/fr-FR/target/using/implement-target/client-side/mbox-implement/mbox-download.html" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p>L’utilisation correcte de <span class="codeph"> mboxCreate</span> ressemble à ceci : </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Veillez à inclure une balise <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> avant d’appeler <span class="codeph"> mboxCreate()</span>. at.js ne le fera pas à votre place. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target : DOCTYPE valide</b> </p> <p>Poids : 5 </p> <p><a href="https://docs.adobe.com/help/fr-FR/target/using/implement-target/client-side/faq-at-js/target-atjs-faq.html#what-html-doctype-does-atjs-require" format="html" scope="external"> Informations supplémentaires</a> </p> </td> 
   <td colname="col2"> <p> Un DOCTYPE non valide a été détecté. Aucune mbox ne sera déclenchée dans ce scénario. </p> <p>Pour at.js, le DOCTYPE doit être en mode standard, sinon Target ne fonctionnera pas. </p> </td> 
   <td colname="col3"> <p>Mettez à jour le DOCTYPE sur la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

