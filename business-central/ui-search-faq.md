---
title: Algengar spurningar um Viðmótsleit | Microsoft Docs
description: Þessi grein veitir svör við spurningum sem samstarfsaðilar og viðskiptamenn spyrja oft um Viðmótsleit.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f7534d1e3365dd02b6f9f1afde03b5de76640e1a
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914886"
---
# <a name="tell-me-faq"></a>Algengar spurningar um Viðmótsleit
Þetta efnisatriði svarar spurningum sem reyndir notendur spyrja oft um eiginleika viðmótsleitar.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Eru allar aðgerðir úr núverandi síðunni minni sýnilegar í Viðmótsleit?
Nei. Aðgerðir í hlutum, svo sem sölulínur eða upplýsingakassar, birtast ekki í Viðmótsleit.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Eru niðurstöðurnar í Viðmótsleit síaðar eftir heimildum?
Ef notandinn hefur ekki AccessByPermissions þá eru aðgerðir ekki sýndar. Hins vegar birtast síður og skýrslur í niðurstöðum en krefjast þess að notandinn hafi heimild til að fá aðgang að þeim. Skilaboð birtast ef notandinn hefur ekki leyfi til að skoða hlutinn.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Sýnir Viðmótsleit efni úr sérstillingum mínum eða uppsettum viðbótum þriðja aðila?
Aðgerðir, síður og skýrslur sem koma frá viðbótum eru sóttar með Viðmótsleit, en sérsniðin hjálpargögn eru það ekki. Fyrir tæknilegar upplýsingar um hvernig á að búa til sérsniðnar síður og skýrslur sýnileg, sjá [Bæta síðum og skýrslum við leit](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Hvað gerir þetta frábrugðið því sem áður var þekkt sem Síðuleit?
Síðuleit hefur þróast í Viðmótsleit til að hjálpa þér að koma hlutum í verk fljótt. Síðuleit gæti aðeins hjálpað þér að vafra á síður eða skýrslur. Á tæknilegu stigi er Viðmótsleit ekki lengur byggt á eldra hugtakinu MenuSuite.

### <a name="i-use-on-premises-d365fin-does-that-include-tell-me"></a>Ég nota á staðnum [!INCLUDE[d365fin](includes/d365fin_md.md)]. Felur það í sér Viðmótsleit?
Þú getur notað Viðmótsleit í vefbiðlaranum á staðnum til að finna aðgerðir, síður og skýrslur en ekki skjöl, eða forrit og ráðgjafarþjónustu á AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>Er Viðmótsleit aðgengileg fyrir alla myndaþætti?
Viðmótsleit er aðeins í boði í vefbiðlaranum eða Windows skjáborðsforritinu.

### <a name="are-the-documentation-results-available-in-any-language"></a>Eru niðurstöður fyrir fylgiskjöl tiltæk á hvaða tungumáli sem er?
Hjálparefnin birtast á því tungumáli sem þú hefur tilgreint í **Stillingarnar mínar** , ef hjálp er til staðar á því tungumáli.

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Hvers vegna sé ég ekki bókamerkistákn fyrir leitarniðurstöðurnar mínar?
Bókamerkjatákn er ekki birt í glugganum „Viðmótsleit“ þegar sérstillingar eru óvirkar fyrir notandahlutverk.


## <a name="see-also"></a>Sjá einnig  
[Vista og sérsníða listayfirlit](ui-views.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Að finna síður með hlutverkaleit](ui-role-explorer.md)  
[Síða eða skýrsla bókamerkt í Mitt hlutverk](ui-bookmarks.md)
