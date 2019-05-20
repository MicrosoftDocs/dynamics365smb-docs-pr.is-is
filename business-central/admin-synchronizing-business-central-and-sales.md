---
title: Samstilling og samþætting gagna | Microsoft Docs
description: Samstillingin afritar gögn milli færslna Dynamics 365 for Sales og Business Central og heldur gögnum í báðum kerfum uppfærðum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: e52010384de83d95011cb29a88cad17a5eba817c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247141"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-for-sales"></a>Samstilling gagna í Business Central og Dynamics 365 for Sales
Við samþættingu [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að ákveða hvort eigi að samstilla gögn á völdum svæðum af færslum [!INCLUDE[d365fin](includes/d365fin_md.md)] (t.d. viðskiptamenn, tengiliðir og sölumenn) við samsvarandi færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] (s.s. reikningar, tengiliðir og notendur). Háð gerð færslu, er hægt að samstilla gögn úr [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)] eða öfugt. Frekari upplýsingar er að finna í [Samþætting við Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Samstilling notar eftirfarandi einingar:

* Vörpun samþættingartöflu
* Varpanir samþættingarreits
* Samstillingarreglur
* Tengdar færslur

Þegar samstilling er sett upp geturðu tengt færslur [!INCLUDE[d365fin](includes/d365fin_md.md)] við færslur [!INCLUDE[crm_md](includes/crm_md.md)] til að samstilla gögn þeirra. Þú getur byrjað samstillingu handvirkt eða samkvæmt áætlun. Eftirfarandi tafla veitir yfirlit yfir leiðir til að samstilla færslur.  

|  Tegund  |  Aðferð  |  Sjá  |  
|--------|----------|-------|  
|Handvirk samstilling|Samstilla samkvæmt færslu fyrir færslu.<br /><br /> Hægt er að samstilla einstakar færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)], t.d. viðskiptamann, við samsvarandi færslu [!INCLUDE[crm_md](includes/crm_md.md)], t.d. reikning. Svona koma notendur venjulega til með að vinna með [!INCLUDE[crm_md](includes/crm_md.md)]-gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Tengja og samstilla færslur handvirkt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Samstilla á grunni töfluvörpunar.<br /><br /> Hægt er að samstilla allar færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflu með [!INCLUDE[crm_md](includes/crm_md.md)]-einingu.|[Samstilla einstakar töfluvarpanir](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Samstilla allar breyttar færslur fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla allar færslur sem hefur verið breytt í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflum frá síðustu samstillingu.|[Samstilling á öllum breyttum færslum](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Full samstilling allra gagna fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla öll gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflum og [!INCLUDE[crm_md](includes/crm_md.md)]-einingum sem er varpað, og stofna nýjar færslur í lausn viðtökustaðar fyrir ótengdar færslur í lausn upprunastaðar.<br /><br /> Full samstilling samstillir öll gögn og hunsar tengingu. Venjulega er gerð full samstilling þegar samþætting er sett upp og aðeins ein lausnin inniheldur gögn. Full samstilling getur einnig verið gagnleg í sýniumhverfi.|[Keyra fulla samstillingu](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Áætluð samstilling|Samstilla allar breytingar á gögnum fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] með áætluðu millibili með því að setja upp verk í verkröðinni.|[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Stöðluð einingavörpun Sales fyrir samstillingu
Einingar í [!INCLUDE[crm_md](includes/crm_md.md)], t.d. reikningar, eru samþættir við jafngildar gerðir af einingum í [!INCLUDE[d365fin](includes/d365fin_md.md)], t.d. viðskiptamenn. Til að vinna með [!INCLUDE[crm_md](includes/crm_md.md)]-gögn eru tenglar settir upp, kallast tengingar, milli eininga í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

Eftirfarandi töflur birta staðlaða vörpun milli eininga í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] sem [!INCLUDE[d365fin](includes/d365fin_md.md)] veitir.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Stefna samstillingar|Sjálfgefin sía|
|-------------------------------------------|-----|-------------------------|--------------|
|Sölumaður/innkaupaaðili|Notandi|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Tengiliðasía Sales: **Staða** er **Nei**, **Notandi með leyfi** er **Já**, stilling samþættingarnotanda er **Nei**|
|Viðskiptamaður|Reikningur|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Afmörkun á reikningi Sales: **Venslagerð** er **Viðskiptamaður** og **Staða** er **Virk**.|
|Tengiliður|Tengiliður|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] tengiliðarsía: **Gerð** er **Einstaklingur** og tengilið er úthlutað til fyrirtækis. Tengiliðasía Sales: Tengiliðnum er úthlutað á fyrirtæki og yfireining viðskiptamannsgerðar er **Reikningur**|
|Gjaldmiðill|Gjaldmiðill færslu|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Mælieining|Einingarflokkur|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Vara|Vara|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Tengiliðasía Sales: **Gerð afurðar** er **Birgðir Sales**|
|Forði|Vara|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Tengiliðasía Sales: **Gerð afurðar** er **Þjónusta**|
|Verðflokkur viðskiptamanna|Verðlisti|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Söluverð|Verðlisti vöru|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] tengiliðarsía: **Sölukóði** er ekki auður, **Sölugerð** er **Verðflokkur viðskiptamanns**|
|Tækifæri|Tækifæri|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Sölureikningshaus|Reikningsfæra|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Sölureikningslína|Reikningsfæra vöru|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Sölupöntunarhaus|Sölupöntun|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Síur söluhauss: **Gerð skjals** er Pöntun, **Staða** er útgefin|
|Athugasemdir sölupöntunar|Athugasemdir sölupöntunar|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Ábending fyrir stjórnendur: Skoðun á vörpunum einingar
Hægt er að skoða vörpunina milli eininga í [!INCLUDE[crm_md](includes/crm_md.md)] og töflurnar í [!INCLUDE[d365fin](includes/d365fin_md.md)] á síðunni **Vörpun samþættingartöflu** þar sem einnig er hægt að nota afmarkanir. Skilgreining á vörpun milli reita í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflum og reita í [!INCLUDE[crm_md](includes/crm_md.md)]-einingum á síðunni **Vörpun samþættingarreits** þar sem hægt er að bæta við viðbótarreglum fyrir vörpun. Þetta getur til dæmis verið gagnlegt ef nauðsynlegt er að úrræðaleita samstillingu.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Ábending fyrir þróunaraðila: Vörpun reita í Business Central í safn valkosta í Sales
Ef þú ert þróunaraðili og langar til að bæta valkostum við safn valkosta í [!INCLUDE[crm_md](includes/crm_md.md)], þá þarftu að vita þetta. Þremur töflum í [!INCLUDE[d365fin](includes/d365fin_md.md)] er varpað á valreiti einingarinnar **Reikningur** í [!INCLUDE[crm_md](includes/crm_md.md)]. Færslunum í töflunum sem ekki eru tengdar við valkostina í [!INCLUDE[crm_md](includes/crm_md.md)] verður sleppt við samstillingu. Þetta þýðir að reiturinn **Valkostur** verður auður í [!INCLUDE[crm_md](includes/crm_md.md)].

Eftirfarandi tafla sýnir varpanir frá [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflum fyrir reitinn **Valkostur** í einingunni **Reikningur** í [!INCLUDE[crm_md](includes/crm_md.md)].

|Tafla|Reitur valkostar í reikningseiningunni|
|----------------------|-------------------------------------------|
|Greiðsluskilmálar|Greiðsluskilmálar|
|Afhendingarmáti|Heimilisfang 1: Flutningsskilmálar|
|Flutningsaðili|Heimilisfang 1: Afhendingarmáti|

### <a name="synchronization-rules"></a>Samstillingarreglur
Í eftirfarandi töflu er lýst reglum sem stjórna samstillingu á milli forritanna.

> [!NOTE]  
> Breytingar á gögnum í [!INCLUDE[crm_md](includes/crm_md.md)] sem voru gerðar af notandareikningi [!INCLUDE[crm_md](includes/crm_md.md)]-tengingar eru ekki samstilltar. Mælt er með því að gögnum sé ekki breytt á meðan reikningurinn er notaður. Frekari upplýsingar er að finna í [Uppsetning samþættingar við Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tafla|Regla|
|-----|----|
|Viðskiptavinum|Áður en hægt er að samstilla viðskiptamann við reikning verður sölumaðurinn sem er viðskiptamanni er úthlutaður að vera tengdur við notandi í [!INCLUDE[crm_md](includes/crm_md.md)]. Af þessum sökum skal, þegar samstillingarverkið VIÐSKIPTAMENN - Dynamics 365 for Sales er keyrt og þú setur það upp til að stofna nýjar færslur, skaltu ganga úr skugga um að samstilla sölumenn við notendur [!INCLUDE[crm_md](includes/crm_md.md)] áður en þú samstillir viðskiptamenn við reikninga í [!INCLUDE[crm_md](includes/crm_md.md)]. <br /> <br />VIÐSKIPTAMENN - Samstillingarverk fyrir Dynamics 365 for Sales samstillir aðeins reikninga sem hafa venslagerðina viðskiptamaður.|
|Tengiliður|Aðeins tengiliðir í [!INCLUDE[crm_md](includes/crm_md.md)] sem eru tengdir við reikningur verða stofnaðir í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Gildið á kóða sölumanns skilgreinir eiganda tengdu einingarinnar í [!INCLUDE[crm_md](includes/crm_md.md)].|
|Gjaldmiðlar|Gjaldmiðlar tengjast við færslugjaldmiðla í [!INCLUDE[crm_md](includes/crm_md.md)] sem byggja á ISO-kóðum. Aðeins gjaldmiðlar sem eru með staðlaður ISO-kóði verða tengdir og samstilltir við færslugjaldmiðla.|
|Mælieiningar|Mælieiningar eru samstillar við einingahópa í [!INCLUDE[crm_md](includes/crm_md.md)]. Aðeins er hægt að skilgreina eina mælieiningu í einingahópnum.|
|Birgðir|Þegar vörur eru samstilltar við [!INCLUDE[crm_md](includes/crm_md.md)] afurðir mun [!INCLUDE[d365fin](includes/d365fin_md.md)] sjálfkrafa stofna verðlista í [!INCLUDE[crm_md](includes/crm_md.md)]. Til að forðast samstillingarvillur ætti ekki að breyta þessum verðlisti handvirkt.|
|Sölumenn|Sölumenn eru tengdir kerfisnotendum í [!INCLUDE[crm_md](includes/crm_md.md)]. Notandinn verður að vera virkur og hafa leyfi og má ekki vera samþættingarnotandinn. Athugaðu að þetta er fyrsta taflan sem þarf að samstilla vegna þess að hún er notuð í viðskiptavinum, tengiliðum, tækifærum og sölureikningum.|
|Forði|Tilföng eru samstillt við vörur [!INCLUDE[crm_md](includes/crm_md.md)] sem hafa þjónustu sem vörugerðina.|
|Verðflokkar viðskm.|Verðflokkar viðskiptavinar eru samstilltir við verðlista Sales.|
|Söluverð|Söluverð sem eru með verðflokk viðskiptavinar sem sölugerð og eru með skilgreindan sölukóða eru samstillt við verðlistalínur [!INCLUDE[crm_md](includes/crm_md.md)]|
|Tækifæri|Tækifæri eru samstillt við tækifæri [!INCLUDE[crm_md](includes/crm_md.md)]. Gildið á kóða sölumanns skilgreinir eiganda tengdu einingarinnar í [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bókaðir sölureikningar|Bókaðir sölureikningar eru samstilltir við sölureikninga. Áður en hægt er að samstilla reikning er betra að samstilla allar aðrar einingar sem geta verið hluti af reikningnum, frá sölumanni til verðlista. Gildið á kóða sölumanns í fyrirsögn reiknings skilgreinir eiganda tengdu einingarinnar í Sales.|
|Sölupantanir|Útgefin sölupöntun (hausar) er samstillt við sölupöntun. Áður en hægt er að samstilla pöntun er betra að samstilla allar aðrar einingar sem geta verið hluti af pöntuninni, frá sölumanni til verðlista. Gildið á kóða sölumanns í pöntunarhaus skilgreinir eiganda tengdu einingarinnar í Sales.|  

## <a name="see-also"></a>Sjá einnig  
[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Samþætting við Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
