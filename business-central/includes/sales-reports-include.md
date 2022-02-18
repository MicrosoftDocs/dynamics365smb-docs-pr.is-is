---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f25e82f8276715d8d5e945bd5d6a309e12502f8e
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104040"
---
Eftirfarandi tafla lýsir sumum helstu skýrslunum í söluskýrslugerð.

|Skýrsla |Kenni hlutar|Description  |
|---------|---------|---------|
|**Viðskiptavinur - Pantanayfirlit**|107| Sýnir sundurliðun pöntunar með magni sem ekki hefur verið afhent fyrir hvern viðskiptamann í þremur 30 daga tímabilum sem byrja hvert á tilgreindri dagsetningu. Einnig eru dálkar með pöntunum sem á eftir að afhenda fyrir og eftir tímabilin þrjú og dálkur með heildarsundurliðun pöntunar hvers viðskiptamanns. Notið skýrsluna til þess að greina áætlað sölumagn fyrirtækis. |
|**Viðskm. - 10 efstu**|111| Sýnir upplýsingar um innkaup viðskiptamanns og stöðu á tilteknu tímabili. Hægt er að velja fjölda viðskiptamanna sem eru taldir með í skýrslu. Aðeins viðskiptamenn sem hafa annaðhvort innkaup á tímabilinu eða stöðu við lok tímabils eru taldir með.<br>Viðskiptamönnum er raðað eftir upphæðum og hægt er að velja hvort þeim er raðað eftir söluupphæð eða stöðu. Skýrslan veitir góða yfirsýn yfir þá viðskiptamenn sem kaupa mest inn eða þá sem skulda mest.|
|**Viðskm. - Vörusala**|113|Þessi skýrsla sýnir lista yfir vörusölu til hvers viðskiptamanns á tilteknu tímabili. Skýrslan felur í sér upplýsingar um magn, upphæð sölu og hugsanlegan afslátt. Nota má skýrsluna við greiningu á viðskiptavinahópum fyrirtækisins, til dæmis.|
|**Birgðir - Sölur viðskm.**|713|Yfirlit séð frá vöruhússsýn. Þetta er annað yfirlit en skýrslan **Viðskm. - Vörusala** og hún sýnir hlutinn fyrst og síðan viðskiptavininn sem keypti vöruna.|
|**Viðskiptamaður - Söluyfirlit**|119|Sýnir söluyfirlit viðskiptamanns fyrir tímabil. Hún er notuð vegna skýrslugerðar fyrir tolla- og skattayfirvöld. Hægt er að taka aðeins með viðskiptamenn með heildarsölu sem er yfir lágmarksupphæð. Einnig er hægt að tilgreina hvort aðsetursupplýsingar um hvern viðskiptamann eigi að koma fram í skýrslunni.<br>Skýrslan er byggð á skráðri sölu (SGM) í viðskiptamannafærslum. Neðst í skýrslunni birtist samanlögð sala í SGM. Samtalan er byggð á viðskiptamönnunum sem teknir eru með í skýrslunni, þ.e. viðskiptamönnunum sem eru innan afmarkananna á flýtiflipanum Viðskiptamenn og sem eru með hærri heildarsölu en sem nemur upphæðinni sem tilgreind er í reitnum **Hærri upphæð (SGM) en** á flýtiflipanum **Valkostir**.|
|**Viðskm. - Staða til dags.**|121|Sýnir hreyfingar á stöðu fyrir tilgreinda viðskiptamenn. Hægt er að nota skýrsluna í t.d. lok fjárhagstímabils eða reikningsárs.|
|**Viðskiptamaður - Prófjöfnuður**|129|Í þessari skýrslu koma fram hreyfingar á stöðu fyrir tilgreinda viðskiptamenn. Hægt er að nota skýrsluna til að sannreyna að staða bókunarflokks viðskiptamanna sé jöfn stöðu samsvarandi fjárhagsreiknings á tilteknum degi. Hægt er að nota skýrsluna í t.d. lok fjárhagstímabils eða reikningsárs. Ef þú þarft ítarlegri útgáfu af þessari skýrslugerð skaltu nota skýrsluna fyrir **Hreyfingar hvers viðskiptamanns** (104).|
|**Söluupplýsingar**|112|[!INCLUDE [reports-sales-statistics](reports-sales-statistics.md)] |
|**Frátekn.möguleikar v. sölu**|209|Sýnir tiltækar vörur til afhendingar í söluskjölum. Notandi ræður því hvort skýrslan eigi við stöðu hvers fylgiskjals eða hverrar sölulínu. Þegar skýrslan er prentuð er einnig hægt að uppfæra magnið sem er tiltækt til afhendingar í reitnum **Magn til afhendingar** í sölulínunum. Þá má nota skýrsluna til þess að tilgreina hvaða fylgiskjöl skal bóka.<br>Einnig er valkostur til að velja magn vörunnar sem á að afhenda. **Athugaðu**: þessi skýrsla er ekki tiltæk fyrir ítarlega virkni vöruhúss.|
|**Staða vöruhúsaafhendingar**|7313|Þessa skýrslu má nota á öllum stöðum þar sem reiturinn **Krefjast afhendingar** er valinn. Skýrslan **Staða vöruhúsaafhendingar** sýnir allar óskráðar sendingarskýrslur fyrir vöruhús, þ.m.t. staðsetningar, hólfakóða, stöðu skjala, magn og o.s.frv. Þessi skýrsla er tilvalin til að fá yfirlit.|
|**Birgðir - Tínslulisti**|813|Birtir lista yfir sölupantanirnar sem varan er hluti af. Eftirfarandi upplýsingar eru birtar um hverja vöru: sölupöntunarlína með nafni viðskiptamannsins, afbrigðiskóði, staðsetningarkóði, hólfakóði, afhendingardagsetning, magn til afhendingar og mælieining. Magn hverrar vöru sem á að afhenda er lagt saman. Skýrsluna má nota þegar vörur eru sóttar í birgðageymsluna.<br>**Athugaðu**: þessi skýrsla er ekki tiltæk fyrir ítarlega virkni vöruhúss.|
|**Birgðir - Sala, biðpöntun**|718|Í þessari skýrslu er birtur listi með pöntunarlínum þar sem komið er fram yfir afhendingardagsetningu. Eftirfarandi upplýsingar birtast um allar vörur í hverri pöntun fyrir sig: númer, nafn viðskiptamanns, símanúmer viðskiptamanns, afhendingardagur, magn í pöntun og magn í biðpöntun. Í skýrslunni kemur einnig fram hvort viðskiptamaðurinn á aðrar vörur í biðpöntun.|
|**Birgðir - Sölupantanir**|708|Birtir lista yfir pantanir sem ekki hafa enn verið afhentar og vörur í þessum pöntunum. Þar kemur fram pöntunarnúmer, nafn viðskiptamanns, dagsetning afhendingar, magn í pöntun, seinkað magn, útistandandi magn og einingarverð, svo og hugsanleg afsláttarprósenta og upphæð. Niðurstöðutölur eru birtar fyrir magn í biðpöntun, útistandandi magn og upphæð fyrir hverja vöru. Nota má skýrsluna til að sjá hvort einhver vandkvæði séu með afhendingar eða hvort búast megi við því.|