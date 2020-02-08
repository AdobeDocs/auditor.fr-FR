---
description: Cette référence fournit des informations supplémentaires sur les tests effectués par l’auditeur pour la configuration.
seo-description: Cette référence fournit des informations supplémentaires sur les tests effectués par l’auditeur pour la configuration.
seo-title: Configuration
title: Configuration
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Configuration

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
    </draft-comment> <p><b>Lancement - Dernière version</b> </p> <p>Poids : 2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Informations supplémentaires</a> </p> </td> 
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

