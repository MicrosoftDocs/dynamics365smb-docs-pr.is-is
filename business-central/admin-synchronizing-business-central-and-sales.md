---
title: Samstilling og samþætting gagna | Microsoft Docs
description: Samstillingin afritar gögn milli færslna Common Data Service og Business Central og heldur gögnunum í báðum kerfum uppfærðum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 07/23/2020
ms.author: bholtorf
ms.openlocfilehash: 2c7b7c4175f4c17e01c114f76d0b14834e0409ae
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617705"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Samstilling gagna í Business Central með Common Data Service

Við samþættingu [!INCLUDE[d365fin](includes/cds_long_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að ákveða hvort eigi að samstilla gögn á völdum svæðum af færslum [!INCLUDE[d365fin](includes/d365fin_md.md)] (t.d. viðskiptamenn, tengiliðir og sölumenn) við samsvarandi færslur í [!INCLUDE[d365fin](includes/cds_long_md.md)] (s.s. reikningar, tengiliðir og notendur). Háð gerð færslu, er hægt að samstilla gögn úr [!INCLUDE[d365fin](includes/cds_long_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)] eða öfugt. Frekari upplýsingar er að finna í [Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Samstilling notar eftirfarandi einingar:

* Vörpun samþættingartöflu
* Varpanir samþættingarreits
* Samstillingarreglur
* Tengdar færslur

Þegar samstilling er sett upp geturðu tengt færslur [!INCLUDE[d365fin](includes/d365fin_md.md)] við færslur [!INCLUDE[d365fin](includes/cds_long_md.md)] til að samstilla gögn þeirra. Þú getur byrjað samstillingu handvirkt eða samkvæmt áætlun. Eftirfarandi tafla veitir yfirlit yfir leiðir til að samstilla færslur.  

|  Tegund  |  Aðferð  |  Sjá  |  
|--------|----------|-------|  
|Handvirk samstilling|Samstilla samkvæmt færslu fyrir færslu.<br /><br /> Hægt er að samstilla einstakar færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)], t.d. viðskiptamann, við samsvarandi færslu [!INCLUDE[d365fin](includes/cds_long_md.md)], t.d. reikning. Svona koma notendur venjulega til með að vinna með [!INCLUDE[d365fin](includes/cds_long_md.md)]-gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Tengja og samstilla færslur handvirkt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Samstilla á grunni töfluvörpunar.<br /><br /> Hægt er að samstilla allar færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflu með [!INCLUDE[d365fin](includes/cds_long_md.md)]-einingu.|[Samstilla einstakar töfluvarpanir](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Samstilla allar breyttar færslur fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla allar færslur sem hefur verið breytt í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflum frá síðustu samstillingu.|[Samstilling á öllum breyttum færslum](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Full samstilling allra gagna fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla öll gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflum og [!INCLUDE[d365fin](includes/cds_long_md.md)]-einingum sem er varpað, og stofna nýjar færslur í lausn viðtökustaðar fyrir ótengdar færslur í lausn upprunastaðar.<br /><br /> Full samstilling samstillir öll gögn og hunsar tengingu. Venjulega er gerð full samstilling þegar samþætting er sett upp og aðeins ein lausnin inniheldur gögn. Full samstilling getur einnig verið gagnleg í sýniumhverfi.|[Keyra fulla samstillingu](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Áætluð samstilling|Samstilla allar breytingar á gögnum fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] með áætluðu millibili með því að setja upp verk í verkröðinni.|[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Stöðluð einingavörpun fyrir samstillingu
Einingar í [!INCLUDE[d365fin](includes/cds_long_md.md)], t.d. reikningar, eru samþættir við jafngildar gerðir af einingum í [!INCLUDE[d365fin](includes/d365fin_md.md)], t.d. viðskiptavini. Til að vinna með [!INCLUDE[d365fin](includes/cds_long_md.md)]-gögn eru tenglar settir upp, kallast tengingar, milli eininga í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)].

Eftirfarandi töflur birta staðlaða vörpun milli eininga í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] sem [!INCLUDE[d365fin](includes/d365fin_md.md)] veitir.

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)] | Stefna samstillingar | Sjálfgefin sía |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Sölumaður/innkaupaaðili | Notandi | [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)] tengiliðasía: **Staða** er **Nei**, **Notandi með leyfi** er **Já**, stilling samþættingarnotanda er **Nei** |
| Viðskiptamaður | Reikningur | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)] reikningssía: **Gerð vensla** er **Viðskiptavinur** og **Staða** er **Virkur**. [!INCLUDE[d365fin](includes/d365fin_md.md)] sía: **Lokað** er autt (viðskiptavinur er ekki útilokaður). |
| Lánardrottinn | Reikningur | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)] afmörkun á reikningi: **Venslagerð** er **Lánardrottinn** og **Staða** er **Virk**. [!INCLUDE[d365fin](includes/d365fin_md.md)] sía: **Lokað** er autt (lánardrottinn er ekki útilokaður). |
| Tengiliður | Tengiliður | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] tengiliðasía: **Gerð** er **Einstaklingur** og tengilið er úthlutað á fyrirtæki. [!INCLUDE[d365fin](includes/cds_long_md.md)] tengiliðasía: Tengiliðnum er úthlutað á fyrirtæki og yfireining viðskiptamannsgerðar er **Reikningur** |
| Gjaldmiðill | Gjaldmiðill færslu | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] |  |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Ábending fyrir stjórnendur: Skoðun á vörpunum einingar
Hægt er að skoða vörpunina milli eininga í [!INCLUDE[d365fin](includes/cds_long_md.md)] og töflurnar í [!INCLUDE[d365fin](includes/d365fin_md.md)] á síðunni **Vörpun samþættingartöflu** þar sem einnig er hægt að nota afmarkanir. Skilgreining á vörpun milli reita í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflum og reita í [!INCLUDE[d365fin](includes/cds_long_md.md)]-einingum á síðunni **Vörpun samþættingarreits** þar sem hægt er að bæta við viðbótarreglum fyrir vörpun. Þetta getur til dæmis verið gagnlegt ef nauðsynlegt er að úrræðaleita samstillingu.

## <a name="see-also"></a>Sjá einnig  
[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
