---
title: Birgða- og vöruhúsaskýrslur og greiningar
description: Finna út hvaða birgða- og vöruhúsaskýrslur eru í boði í staðlaðri útgáfu Business Central til að halda utan um reksturinn.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216369"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Birgða- og vöruhúsaskýrslur og Analytics í Business Central

Birgða- og vöruhúsaskýrsla í [!INCLUDE [prod_short](includes/prod_short.md)] gerir starfsmönnum í birgðum og rekstri kleift að fá innsýn í og tölfræði um núverandi og fyrri vöruhúsaaðgerðir.  

## <a name="reports"></a>Skýrslur

Eftirfarandi tafla lýsir sumum helstu skýrslunum í vörhúsaskýrslugerð.

|Skýrsla |Kenni hlutar|Description  |
|---------|---------|---------|
|**Birgðir - til ráðst. skv. áætlun**|707|Til að fá yfirlit yfir tiltekna hluti/birgðahaldseiningar og framboð þeirra. Þessi skýrsla sýnir uppsöfnuð gildi eins og brúttóþarfir, áætlaðar og fyrirhugaðar móttöku, birgðir o.s.frv. |
|**Verðmat birgða**|1001|Birtir verðmætamat birgða fyrir tilteknar vörur. Skýrslan sýnir einnig upplýsingar um verðmæti birgðaaukningar og birgðaminnkunar á tilteknum tíma.|
|**Vara útrunnin - Magn**|5809|Sýnir yfirlit yfir magn valdra vara í birgðum sem hafa gildistíma innan ákveðins tímabils. Listinn sýnir fjölda eininga valinnar vöru sem renna út á tilteknu tímabili. Útprentaða fylgiskjalið sýnir fjölda eininga sem renna út á þremur jafn löngum tímabilum og heildarbirgðamagn hverrar vöru sem er tilgreind þegar skýrslan er sett upp.<br>Tilgreina má efni skýrslunnar með því að setja afmarkanir. Ef engar afmarkanir eru settar nær skýrslan til allra færslna. Magnið í skýrslunni endurspeglar aðeins magn vöru sem hefur skilgreindan gildistíma.|
|**Aldurssamsetning vöru - Magn** eða **Aldurssamsetning vöru - Virði**|5807 eða 5808|Sýnir yfirlit um núverandi aldurssamsetningu valinna vara í birgðaskrá. Í listanum sést sá fjöldi eininga eða gilda valinnar vöru sem var bætt við eða fjarlægður úr birgðum og hvenær. Vörum er bætt í birgðir, eða þær fjarlægðar, vegna innkaupa, sölu, aukningar eða minnkunar.|
|**Birgðir - Kostn.og söluv.listi**|716|Birtir lista yfir verðupplýsingar um tilteknar vörur eða birgðaeiningar: innkaupsverð, síðasta innkaupsverð, einingarverð, hagnaðarprósenta og hagnaður. |
|**Vöruhúsahólfalisti**|7319|Sýnir yfirlit yfir vöruhúsahólf, uppsetningu þeirra og vörumagnið í hólfunum. Hægt er að nota þessa skýrslu á öllum stöðum, sem eru með „hólf“ sem skyldusvæði. |
|**Staða vöruhúsaafhendingar**|7313|Sýnir yfirlit opin upprunaskjöl með afhentum vörum eða vörur til afhendingar fyrir hverja birgðageymslu. Þessa skýrslu má nota á öllum stöðum þar sem **Áskildar sendingar** eru virkar. **Staða vöruhúsasendingar** sýnir staðsetningar, hólfakóða, skjalastöðu, magn.|
|**Birgðir - Tínslulisti**|813|Birtir lista yfir sölupantanirnar sem varan er hluti af. Eftirfarandi upplýsingar eru birtar um hverja vöru: sölupöntunarlína með nafni viðskiptamannsins, afbrigðiskóði, kóði birgðageymslu, afhendingardagsetning, magn til afhendingar og mælieining. Magn hverrar vöru sem á að afhenda er lagt saman. Skýrsluna má nota þegar vörur eru sóttar í birgðageymsluna.<br>ATHUGAÐU: þessi virkni er ekki tiltæk fyrir ítarlega virkni vöruhúss.|
|**Leiðréttingarhólf vöruhúss**|7320|Þessi sérskýrsla er eingöngu ætluð fyrir ítarlegt vöruhús og sýnir eftirstandandi magn í sjálfu leiðréttingarhólfinu. Venjulega ætti þetta tiltekna hólf að vera tóm. Eina ástæðan fyrir því að þetta hólf sé fullt er vegna efnislegrar talningar eða ef magn vöru hafði verið fjarlægt eða bætt við vöruhúsið|


## <a name="tasks"></a>Verk

Eftirfarandi greinar lýsa sumum lykilverkum til að greina stöðu fyrirtækisins:

* [Stofna greiningarskýrslur](bi-how-create-analysis-views-reports.md)  
* [Skoða tiltækileika vöru](inventory-how-availability-overview.md)


## <a name="see-also"></a>Sjá einnig .

[Uppsetning birgða](inventory-setup-inventory.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
