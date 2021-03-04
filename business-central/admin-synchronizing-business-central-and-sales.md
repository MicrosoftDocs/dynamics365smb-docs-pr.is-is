---
title: Samstilling og samþætting gagna | Microsoft Docs
description: Samstillingin afritar gögn milli tafla Microsoft Dataverse og Business Central og heldur gögnunum í báðum kerfum uppfærðum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 83de0f6eb46921afdb4e69fbbe5260670a7fdbbc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755098"
---
# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Samstilling gagna í Business Central með Microsoft Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Við samþættingu [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að ákveða hvort eigi að samstilla gögn á völdum svæðum [!INCLUDE[prod_short](includes/prod_short.md)] (t.d. viðskiptamenn, tengiliðir og sölumenn) við samsvarandi línur í [!INCLUDE[prod_short](includes/cds_long_md.md)] (s.s. reikningar, tengiliðir og notendur). Háð gerðar línu, er hægt að samstilla gögn úr [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] eða öfugt. Frekari upplýsingar er að finna í [Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Samstilling notar eftirfarandi einingar:

* Vörpun samþættingartöflu
* Varpanir samþættingarreits
* Samstillingarreglur
* Tengdar færslur

Þegar samstilling er sett upp geturðu tengt færslur [!INCLUDE[prod_short](includes/prod_short.md)] við línur [!INCLUDE[prod_short](includes/cds_long_md.md)] til að samstilla gögn þeirra. Þú getur byrjað samstillingu handvirkt eða samkvæmt áætlun. Eftirfarandi tafla veitir yfirlit yfir leiðir til að samstilla.  

|  Tegund  |  Aðferð  |  Sjá  |  
|--------|----------|-------|  
|Handvirk samstilling|Samstilla línu fyrir línu.<br /><br /> Hægt er að samstilla einstakar færslur í [!INCLUDE[prod_short](includes/prod_short.md)], t.d. viðskiptamann, við samsvarandi línu [!INCLUDE[prod_short](includes/cds_long_md.md)], t.d. reikning. Svona koma notendur venjulega til með að vinna með [!INCLUDE[prod_short](includes/cds_long_md.md)]-gögn í [!INCLUDE[prod_short](includes/prod_short.md)].|[Tengja og samstilla færslur handvirkt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Samstilla á grunni töfluvörpunar.<br /><br /> Hægt er að samstilla allar færslur í [!INCLUDE[prod_short](includes/prod_short.md)]-töflu með [!INCLUDE[prod_short](includes/cds_long_md.md)]-töflu.|[Samstilla einstakar töfluvarpanir](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Samstilla allar breyttar færslur fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla allar færslur sem hefur verið breytt í [!INCLUDE[prod_short](includes/prod_short.md)]-töflum frá síðustu samstillingu.|[Samstilling á öllum breyttum færslum](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Full samstilling allra gagna fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla öll gögn í [!INCLUDE[prod_short](includes/prod_short.md)]-töflum og [!INCLUDE[prod_short](includes/cds_long_md.md)]-töflum sem er varpað, og stofna nýjar færslur eða línur í lausn viðtökustaðar fyrir ótengdar færslur í lausn upprunastaðar.<br /><br /> Full samstilling samstillir öll gögn og hunsar tengingu. Venjulega er gerð full samstilling þegar samþætting er sett upp og aðeins ein lausnin inniheldur gögn. Full samstilling getur einnig verið gagnleg í sýniumhverfi.|[Keyra fulla samstillingu](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Áætluð samstilling|Samstilla allar breytingar á gögnum fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] með áætluðu millibili með því að setja upp verk í verkröðinni.|[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-table-mapping-for-synchronization"></a>Stöðluð töfluvörpun fyrir samstilling
Töflur í [!INCLUDE[prod_short](includes/cds_long_md.md)], t.d. reikningar, eru samþættar við jafngildar gerðir af töflum í [!INCLUDE[prod_short](includes/prod_short.md)], t.d. viðskiptavini. Til að vinna með [!INCLUDE[prod_short](includes/cds_long_md.md)]-gögn eru tenglar settir upp, kallast tengingar, milli tafla í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)].

Eftirfarandi töflur birta staðlaða vörpun milli tafla í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Hægt er að endurstilla breytingar á grunnstillingu sem gerðar voru á vörpunum samþættingartöflu og reita í sjálfgefnar stillingar með því að velja varpanirnar og velja síðan **Nota sjálfgefinn samstillingargrunn**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Stefna samstillingar | Sjálfgefin sía |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Sölumaður/innkaupaaðili | Notandi | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] tengiliðasía: **Staða** er **Nei**, **Notandi með leyfi** er **Já**, stilling samþættingarnotanda er **Nei** |
| Viðskiptamaður | Reikningur | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] reikningssía: **Gerð vensla** er **Viðskiptavinur** og **Staða** er **Virkur**. [!INCLUDE[prod_short](includes/prod_short.md)] sía: **Lokað** er autt (viðskiptavinur er ekki útilokaður). |
| Lánardrottinn | Reikningur | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] afmörkun á reikningi: **Venslagerð** er **Lánardrottinn** og **Staða** er **Virk**. [!INCLUDE[prod_short](includes/prod_short.md)] sía: **Lokað** er autt (lánardrottinn er ekki útilokaður). |
| Tengiliður | Tengiliður | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] tengiliðasía: **Gerð** er **Einstaklingur** og tengilið er úthlutað á fyrirtæki. [!INCLUDE[prod_short](includes/cds_long_md.md)] tengiliðasía: Tengiliðnum er úthlutað á fyrirtæki og yfireining viðskiptamannsgerðar er **Reikningur** |
| Gjaldmiðill | Gjaldmiðill færslu | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |


### <a name="tip-for-admins-viewing-table-mappings"></a>Ábending fyrir stjórnendur: Skoðun töfluvarpana
Hægt er að skoða vörpunina milli tafla í [!INCLUDE[prod_short](includes/cds_long_md.md)] og í [!INCLUDE[prod_short](includes/prod_short.md)] á síðunni **Vörpun samþættingartöflu** þar sem einnig er hægt að nota afmarkanir. Skilgreining á vörpun milli reita í [!INCLUDE[prod_short](includes/prod_short.md)]-töflum og dálka í [!INCLUDE[prod_short](includes/cds_long_md.md)]-töflum á síðunni **Vörpun samþættingarreits** þar sem hægt er að bæta við viðbótarreglum fyrir vörpun. Þetta getur til dæmis verið gagnlegt ef nauðsynlegt er að úrræðaleita samstillingu.

## <a name="see-also"></a>Sjá einnig  
[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]