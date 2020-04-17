---
title: Handvirk samstilling á töfluvörpunum | Microsoft Docs
description: Samstillingin afritar gögn milli Common Data Service-eininga og Business Central til að halda báðum kerfum uppfærðum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 015084b999f7488339c98605018bff2bc9a4ded2
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196712"
---
# <a name="manually-synchronize-table-mappings"></a>Samstilla töfluvarpanir handvirkt
Vörpun samþættingartöflu tengir [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflu (færslugerð), t.d. viðskiptamaður, við [!INCLUDE[d365fin](includes/cds_long_md.md)]-einingu, t.d. reikningur. Samstilling á vörpun samþættingartöflu gerir þér kleift að samþætta gögn í öllum færslum í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflunni og [!INCLUDE[d365fin](includes/cds_long_md.md)]-einingunni sem eru tengdar. Að auki, þó háð grunnstillingu töfluvörpunar, getur samstilling búið til og tengt nýjar færslur á lausn endastaðar fyrir ótengdar færslur á upprunastaðnum.  

Að samstilla varpanir samþættingartöflu handvirkt getur verið gagnlegt við fyrstu uppsetningu á samþættingu og greiningu á villum samstillingar.  

Þetta efnisatriði útskýrir þrjár aðferðir til að samstilla varpanir samþættingartöflu handvirkt. Hver aðferð býður upp á mismunandi stig samstillingar.

## <a name="run-a-full-synchronization"></a>Keyra fulla samstillingu
Full samstilling keyrir öll samstillingarverk samþættingar fyrir samstillingu á [!INCLUDE[d365fin](includes/d365fin_md.md)]-færslum og [!INCLUDE[d365fin](includes/cds_long_md.md)]-einingum, eins og það er skilgreint á síðunni **Vörpun samþættingartöflu**. 

Full samstilling framkvæmir eftirfarandi aðgerðir fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] eða [!INCLUDE[d365fin](includes/cds_long_md.md)]-færslur sem eru:

* Ekki tengdar, ný samsvarandi færsla verður búin til og tengd í andstæðri lausn.
Hvort og hvenær færsla er búin til fer eftir samstillingaráttinni. Til dæmis, við samstillingu gagna frá [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamönnum við [!INCLUDE[d365fin](includes/cds_long_md.md)] reikninga , ef til er viðskiptamaður sem er ekki tengdur við reikning, verður nýr reikningur sjálfkrafa stofnaður í [!INCLUDE[d365fin](includes/cds_long_md.md)] og tengdur við viðskiptamanninn í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hið andstæða á við þegar samstillingaráttin er frá [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Fyrir hvern reikning sem er ekki nú þegar tengdur við viðskiptamann, verður nýr viðskiptamaður búinn til í [!INCLUDE[d365fin](includes/d365fin_md.md)] og tengdur við reikninginn í [!INCLUDE[d365fin](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  Til að ná þessu fram, hreinsar fulla samstillingin tímabundið valkostinn **Samst. aðeins tengdar færslur** í vörpun samþættingartöflu sem samstillingarverkið notar. Undir lok ferlisins fyrir fulla samstillingu verður spurt hvort eigi að halda þessum valkosti hreinsuðum fyrir öll verk.  

* Tengt, er samstillingaráttin (t.d. frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[d365fin](includes/cds_long_md.md)] eða frá [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]) ákveðin fyrirfram af vörpunum samþættingartöflu. Frekari upplýsingar er að finna í [Stöðluð einingavörpun fyrir samstillingu](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Venjulega er aðeins notuð full samstilling þegar samþætting er sett upp fyrst milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] og aðeins ein af lausnunum inniheldur gögn, sem þú vilt afrita í hina lausnina. Full samstilling getur verið gagnleg í sýniumhverfi. Vegna þess að full samstilling býr til og tengir færslur milli lausna, er hægt að byrja fyrr á að vinna með samstillingu gagna milli færslna. Aftur á móti ætti aðeins að keyra fulla samstillingu ef þú vilt færslu í [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir hverja færslu í [!INCLUDE[d365fin](includes/cds_long_md.md)] fyrir umbeðnar töfluvarpanir. Annars er hægt að fá óumbeðnar eða tvíteknar færslur í annaðhvort [!INCLUDE[d365fin](includes/d365fin_md.md)] eða [!INCLUDE[d365fin](includes/cds_long_md.md)].  

### <a name="to-run-a-full-synchronization"></a>Að keyra fulla samstillingu  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Common Data Service Uppsetning tengingar** og veldu síðan tengda tengilinn.

    > [!NOTE]
    > Ef ætlunin er að keyra fulla samstillingu fyrir einingar í gegnum Dynamics 365 Sales skal nota síðuna **Microsoft Dynamics 365 Sales uppsetning tengingar** í staðinn.

2.  Veldu aðgerðina **Keyra fulla samstillingu** og síðan skal velja hnappinn **Já**.  
3.  Þegar fullri samstillingu er lokið er hægt að tilgreina hvort leyfa eigi áætluðum samstillingarverkum að búa til nýjar færslur.  

    Ef þú vilt að öll samstillingarverk búi til nýjar færslur á viðtökustaðnum fyrir ótengdar færslur á upprunastaðnum skal velja **Já**. Þetta setur reitinn **Samst. aðeins tengdar færslur** í töfluvarpanir sem samstillingarverkin nota.  

    Ef þú vilt að samstillingarverk keyri eins og þau gerðu á undan fullri samstillingu hvað varðar að búa til nýjar færslur, skal velja **Nei**. Þetta færir reitinn **Samst. aðeins tengdar færslur** í stillinguna sem hann hafði á undan fullri samstillingu.  

Hægt er að skoða niðurstöður fullrar samstillingar á síðunni **Samstillingarverk samþættingar**. Frekari upplýsingar er að finna í [Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Samstilling á öllum breyttum færslum
Hægt er að nota síðuna **Uppsetning CDS-tengingar** til að samstilla breytingar á gögnum í vörpunum samþættingartöflu. Þetta er svipað og full samstilling. Það mun samstilla gögn í öllum tengdum færslum í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflum og [!INCLUDE[d365fin](includes/cds_long_md.md)]-einingum sem eru skilgreindar í töfluvörpunum. Sjálfgefið er að einungis færslur verða samstilltar sem hefur verið breytt síðan þær voru síðast samstilltar. Samstillingarverk samstilla töfluvörpunum í eftirfarandi röð til að koma í veg fyrir að tengingar hafi áhrif á hver aðra milli eininga:  

1.  GJALDMIÐLAR  
2.  SÖLUMENN  
3.  Lánardrottinn  
4.  VIÐSKIPTAMAÐUR  
5.  TENGILIÐIR  

Hægt er að skoða niðurstöður samstillingar á síðunni **Samstillingarverk samþættingar**. Frekari upplýsingar er að finna í [Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Með því að breyta vörpun samþættingartöflu fyrirfram er hægt að skilgreina samstillinguna með afmörkunum til að stýra því hvaða færslur eru samstilltar, eða skilgreint hana til að búa til nýjar færslur í viðtökustað lausnar fyrir ótengdar færslur á upprunastaðnum. Frekari upplýsingar er að finna í [Breyta töfluvörpunum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Að samstilla færslur fyrir allar töflur  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Microsoft Dynamics 365 Sales uppsetning tengingar** og veldu síðan tengda tengilinn.
2.  Veldu aðgerðina **Samstilla breyttar færslur** og síðan **Já**.  

## <a name="synchronize-individual-table-mappings"></a>Samstilla stakar töfluvarpanir
Hægt er að nota síðuna **Vörpun samþættingartöflu** til að keyra samstillingarverk fyrir tilteknar töfluvarpanir. Þetta mun samstilla gögn í öllum tengdum færslum í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflu og [!INCLUDE[d365fin](includes/cds_long_md.md)]-einingu sem eru skilgreindar í töfluvörpun. Sjálfgefið er að einungis færslur verða samstilltar sem hefur verið breytt síðan þær voru síðast samstilltar.  

Með því að breyta vörpun samþættingartöflu fyrirfram er hægt að skilgreina samstillingarverkið til að búa til nýjar færslur í viðtökustað lausnar fyrir ótengdar færslur á upprunastaðnum.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Að samstilla færslur fyrir vörpun samþættingartöflu  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.
2.  Veldu aðgerðina **Samstilla breyttar færslur** og síðan **Já**.  

## <a name="see-also"></a>Sjá einnig  
[Samstilling Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   
