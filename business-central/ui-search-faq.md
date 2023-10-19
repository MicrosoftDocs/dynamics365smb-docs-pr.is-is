---
title: Algengar spurningar um Viðmótsleit
description: Þessi grein veitir svör við spurningum sem samstarfsaðilar og viðskiptavinir spyrja oft um Viðmótsleitina.
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 09/21/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# <a name="tell-me-faq"></a>Algengar spurningar um Viðmótsleit

Þessi grein svarar spurningum sem háþróaður notandi okkar spyr oft um það að segja mér hvað þú vilt gera lögun.

## <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Eru allar aðgerðir úr núverandi síðunni minni sýnilegar í Viðmótsleit?

Nei. Aðgerðir í hlutum, eins og sölulínunum hluti eða Factkassar, eru ekki birtar í segja mér.

## <a name="can-i-search-for-a-specific-record"></a>Get ég leitað að ákveðinni færslu?

Já. Ef til dæmis á að finna sölupöntun á fljótlegan hátt, Færið inn kenni hennar og veljið  **síðan gagnaaðgerðir**  leitarfyrirtækisins. Ef þú þekkir aðeins nafn viðskiptamannsins skaltu slá það inn. Segðu mér að raða niðurstöðum eftir gerð svo að þú gætir fundið pöntunina í sölupöntunartegundinni.

## <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Eru niðurstöðurnar í Viðmótsleit síaðar eftir heimildum?

Ef notandinn hefur ekki Aukaleyfi eru aðgerðir ekki birtar. Hins vegar birtast síður og skýrslur í niðurstöðum en krefjast þess að notandinn hafi heimild til að fá aðgang að þeim. Skilaboð birtast ef notandinn hefur ekki heimild til að skoða hlutinn.

## <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Sýnir Viðmótsleit efni úr sérstillingum mínum eða uppsettum viðbótum þriðja aðila?

Aðgerðir, síður og skýrslur sem koma frá viðbótum eru sóttar af viðmótsleit. Fyrir tæknilegar upplýsingar um hvernig á að búa til sérsniðnar síður og skýrslur sýnileg, sjá [Bæta síðum og skýrslum við leit](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

## <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Hvað gerir þetta frábrugðið því sem áður var þekkt sem Síðuleit?

Síðuleit hefur þróast í Viðmótsleit til að hjálpa þér að koma hlutum í verk fljótt. Síðuleit gæti aðeins hjálpað þér að vafra á síður eða skýrslur. Á tæknilegu stigi er Viðmótsleit ekki lengur byggt á eldra hugtakinu MenuSuite.

## <a name="i-use-on-premises--does-that-include-tell-me"></a>Ég nota á staðnum [!INCLUDE[prod_short](includes/prod_short.md)]. Felur það í sér Viðmótsleit?

Þú getur notað Viðmótsleit í vefbiðlaranum á staðnum til að finna aðgerðir, síður og skýrslur en ekki forrit og ráðgjafarþjónustu á AppSource.

## <a name="is-tell-me-available-for-all-form-factors"></a>Er Viðmótsleit aðgengileg fyrir alla myndaþætti?

Já. Það var kynnt á símum og spjaldtölvum í Business Central 2023 út Wave 2, en það verður að virkja í  [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management)  með  **aðgerðinni: leita að síðum og gögnum í Mobile App**  Switch. 

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language"></a>Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things"></a>Sýnir viðmótsleitin mér hvernig á að nota síður, skýrslur og annað?

Nei, en þú getur auðveldlega nálgast þessar upplýsingar á hjálparsvæðinu. Veldu  **bara aðgerðina leita í Hjálp**  í  **Segðu hvað þú vilt gera**  síðu eða veldu  <kbd>CTRL</kbd>+<kbd>F1</kbd>  á lyklaborðinu. Til að fræðast meira um Hjálparrúðuna er farið í  [hjálparrúðu](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Hvers vegna sé ég ekki bókamerkistákn fyrir leitarniðurstöðurnar mínar?

Táknið fyrir bókamerki birtist ekki í glugganum segja mér þegar sérsnið er gert óvirkt fyrir notendahlutverk.

## <a name="see-also"></a>Sjá einnig

[Vista og sérsníða listayfirlit](ui-views.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Að finna síður með hlutverkaleit](ui-role-explorer.md)  
[Síða eða skýrsla bókamerkt í Mitt hlutverk](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
