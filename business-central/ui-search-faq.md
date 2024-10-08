---
title: Algengar spurningar um Viðmótsleit
description: Þessi grein veitir svör við spurningum sem samstarfsaðilar og viðskiptavinir spyrja oft um Viðmótsleitina.
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 03/20/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# <a name="tell-me-faq"></a>Algengar spurningar um Viðmótsleit

Þessi grein svarar spurningum sem háþróaðir notendur okkar spyrja oft um Segðu mér hvað þú vilt gera eiginleika.

## <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Eru allar aðgerðir úr núverandi síðunni minni sýnilegar í Viðmótsleit?

Nei. Aðgerðir í hlutum, t.d. í hlutanum Sölulínur eða Upplýsingakassar, birtast ekki í Tell Me.

## <a name="can-i-search-for-a-specific-record"></a>Get ég leitað að tiltekinni færslu?

Já. Eigi til dæmis fljótlegt að finna sölupöntun skal færa inn kenni hennar og velja svo aðgerðina **Leita að fyrirtækisgögnum** . Ef nafn viðskiptamannsins er aðeins þekkt er það fært inn. Segja mér að niðurstöðum sé raðað eftir tegundum svo að hægt væri að finna pöntunina í flokknum Sölupantanir.

## <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Eru niðurstöðurnar í Viðmótsleit síaðar eftir heimildum?

Ef notandinn er ekki með AccessByPermissions þá birtast aðgerðir ekki. Hins vegar birtast síður og skýrslur í niðurstöðum en krefjast þess að notandinn hafi heimild til að fá aðgang að þeim. Skilaboð birtast ef notandinn hefur ekki heimild til að skoða hlutinn.

## <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Sýnir Viðmótsleit efni úr sérstillingum mínum eða uppsettum viðbótum þriðja aðila?

Aðgerðir, síður og skýrslur sem koma frá viðbótum eru sóttar af viðmótsleit. Fyrir tæknilegar upplýsingar um hvernig á að búa til sérsniðnar síður og skýrslur sýnileg, sjá [Bæta síðum og skýrslum við leit](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

## <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Hvað gerir þetta frábrugðið því sem áður var þekkt sem Síðuleit?

Síðuleit hefur þróast í Viðmótsleit til að hjálpa þér að koma hlutum í verk fljótt. Síðuleit gæti aðeins hjálpað þér að vafra á síður eða skýrslur. Á tæknilegu stigi er Viðmótsleit ekki lengur byggt á eldra hugtakinu MenuSuite.

## <a name="i-use-on-premises--does-that-include-tell-me"></a>Ég nota á staðnum [!INCLUDE[prod_short](includes/prod_short.md)]. Felur það í sér Viðmótsleit?

Þú getur notað Viðmótsleit í vefbiðlaranum á staðnum til að finna aðgerðir, síður og skýrslur en ekki forrit og ráðgjafarþjónustu á AppSource.

## <a name="is-tell-me-available-for-all-form-factors"></a>Er Viðmótsleit aðgengileg fyrir alla myndaþætti?

Já. Það var kynnt á símum og spjaldtölvum í Business Central 2023 útgáfubylgju 2. Í 2023 gefa út bylgju 2 verður að virkja hana í [Eiginleikastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management) með eiginleikanum **: Leita að síðum og gögnum í farsímaforritsrofanum** . Árið 2024 rlease bylgju 1 og síðar er hún alltaf virk.

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language"></a>Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things"></a>Sýnir viðmótsleitin mér hvernig á að nota síður, skýrslur og annað?

Nei, en þú getur auðveldlega nálgast þessar upplýsingar á hjálparsvæðinu. Veldu bara aðgerðina **Leitarhjálp** í **Segðu mér hvað þú vilt gera** síðu eða veldu <kbd>Ctrl</kbd>+<kbd>F1</kbd> á lyklaborðinu þínu. Nánari upplýsingar um hjálparsvæðið fást með því að fara á [hjálparsvæðið](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Hvers vegna sé ég ekki bókamerkistákn fyrir leitarniðurstöðurnar mínar?

Bókamerkjatáknið birtist ekki í glugganum Segja mér þegar sérstillingin er óvirk fyrir notandahlutverk.

## <a name="see-also"></a>Sjá einnig

[Vista og sérsníða listayfirlit](ui-views.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Að finna síður með hlutverkaleit](ui-role-explorer.md)  
[Síða eða skýrsla bókamerkt í Mitt hlutverk](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
