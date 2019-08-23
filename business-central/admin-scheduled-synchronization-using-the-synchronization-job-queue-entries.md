---
title: Samstilling Business Central og Dynamics 365 for Sales | Microsoft Docs
description: Kynntu þér hvernig á að samstilla gögn milli Business Central og Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 07/16/2019
ms.author: bholtorf
ms.openlocfilehash: 9290730bb559d4ac03a437a49ed81b09f3c01853
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755219"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-for-sales"></a>Áætla samstillingu milli Business Central og Dynamics 365 for Sales
Hægt er að samstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] með áætluðu millibili með því að setja upp verk í verkröðinni. Samstillingarverkin samstilla gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)] færslum og [!INCLUDE[crm_md](includes/crm_md.md)] færslum sem hafa þegar verið tengdar. Eða fyrir færslur sem eru ekki þegar tengdar, allt eftir stefnu samstillingar og reglum, geta samstillingarverk stofnað og tengd nýjar færslur í lendingarkerfinu. Nokkur samstillingarverk eru í boði beint úr kassanum. Hægt er að skoða þau á síðunni **Verkraðarfærslur**. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Samstillingarferli  
Hvert verkraðarfærsla samstillingarverks notar sértæka vörpun samþættingartöflu sem tilgreinir hvaða [!INCLUDE[d365fin](includes/d365fin_md.md)] töflu og [!INCLUDE[crm_md](includes/crm_md.md)] einingu á að samstilla. Töfluvarpanir innihalda einnig nokkrar stillingar sem stýra því hvaða færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] töflunni [!INCLUDE[crm_md](includes/crm_md.md)] einingunni verða samstilltar.  

Til að samstilla gögn verða [!INCLUDE[crm_md](includes/crm_md.md)] einingafærslur að vera tengdar við [!INCLUDE[d365fin](includes/d365fin_md.md)] færslur. Til dæmis verður [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamaður að vera tengdur við [!INCLUDE[crm_md](includes/crm_md.md)] reikning. Þú getur sett upp tengi handvirkt, áður en samstillingarverk eru keyrð, eða láta samstillingu störf setja upp tengi sjálfkrafa. Eftirfarandi listi lýsir því hvernig gögn eru samstillt milli [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)] og þegar þú ert að nota verkraðarfærslur samstillingarverka. Frekari upplýsingar er að finna í [Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Sjálfgefið eru aðeins færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem eru tengdar við færslur í [!INCLUDE[crm_md](includes/crm_md.md)] samstilltar. Þú getur breytt töfluvörpun á milli [!INCLUDE[crm_md](includes/crm_md.md)] einingar og [!INCLUDE[d365fin](includes/d365fin_md.md)] töflu þannig að heildasamstillingarverkin stofni nýjar færslur í endanlegum gagnagrunni fyrir hverja færslu í upprunagagnagrunninum sem ekki var tengd. Nýju færslur eru einnig tengdar við samsvarandi færslur í upptökum. Til dæmis, þegar þú samstillir viðskiptamenn við [!INCLUDE[crm_md](includes/crm_md.md)] reikninga er búinn til ný reikningsfærsla fyrir hvern viðskiptamann í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nýir reikningar eru sjálfkrafa tengdur við viðskiptamenn í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þar sem samstillingu í þessu tilfelli er tvíátta, nýr viðskiptamaður er búinn til og tengdur fyrir hvern [!INCLUDE[crm_md](includes/crm_md.md)] reikning sem er ekki þegar tengdur.  

    > [!NOTE]  
    > Til eru reglur og afmarkanir sem ákvarða hvaða gögn eru samstillt. Frekari upplýsingar eru í [Samstillingarreglur](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Þegar nýjar færslur eru stofnaðar í [!INCLUDE[d365fin](includes/d365fin_md.md)], nota þær annaðhvort sniðmát sem er skilgreint fyrir vörpun samþættingartöflunnar eða sjálfgefna sniðmátið sem tiltækt er fyrir færslugerðina. Reitirnir eru fylltir með gögnum úr [!INCLUDE[d365fin](includes/d365fin_md.md)] eða [!INCLUDE[crm_md](includes/crm_md.md)], fer eftir samstillingaráttinni. Frekari upplýsingar er að finna í [Hvernig á að: Breyta töfluvörpunum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Við síðari samstillingar, aðeins skrár sem hafa verið breytt eða bætt við eftir síðustu árangursríka samstillingu starf fyrir aðila verður uppfærður.  

     Nýjum færslum í [!INCLUDE[crm_md](includes/crm_md.md)] er bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef gögnum í reitum í [!INCLUDE[crm_md](includes/crm_md.md)] færslum hafa breyst eru gögnin afrituð í samsvarandi reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Við tvíátta samstillingu er verkið samstillt frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)], og því næst frá [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Sjálfgefnar Verkraðarfærslur samstillingar  
Eftirfarandi tafla lýsir sjálfgefnu samstillingarverkunum.  

|Verkraðarfærsla|Description|Stefna|Vörpun samþættingartöflu|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|TENGILIÐUR - Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] tengiliði við [!INCLUDE[d365fin](includes/d365fin_md.md)] tengiliði.|Í báðar áttir|Tengiliður|  
|GJALDMIÐILL – Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] færslugjaldmiðla við [!INCLUDE[d365fin](includes/d365fin_md.md)] gjaldmiðla.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|GJALDMIÐLAR|  
|VIÐSKIPTAMAÐUR - Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga við [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamenn.|Í báðar áttir|VIÐSKIPTAMAÐUR|  
|VERÐFL.VIÐSKIPTAM.-VERÐ - Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] söluverðlista við [!INCLUDE[d365fin](includes/d365fin_md.md)] verðflokka viðskiptamanns.| |VERÐFLOKKAR VIÐSKIPTAMANNS-LISTAR SÖLUVERÐS|
|VARA - AFURÐ - Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] vörur við [!INCLUDE[d365fin](includes/d365fin_md.md)] atriði.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|ATRIÐI-VARA|
|POSTEDSALESINV-INV - Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga við [!INCLUDE[d365fin](includes/d365fin_md.md)] bókaða sölureikninga.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|REIKNINGAR-BÓKAÐIR SÖLUREIKNINGAR|
|FORÐI-AFURÐ - Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] vörur við [!INCLUDE[d365fin](includes/d365fin_md.md)] tilföng.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|TILFÖNG-VARA|  
|SÖLUFÓLK – Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[d365fin](includes/d365fin_md.md)] sölumenn við [!INCLUDE[crm_md](includes/crm_md.md)] notendur.|Frá [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]|SÖLUMENN|
|SALESPRC-PRODUCTPRICE - Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] afurðarverð við [!INCLUDE[d365fin](includes/d365fin_md.md)] söluverð.||AFURÐARVERÐ-SÖLUVERÐ|
|MÆLIEINING - Dynamics 365 for Sales samstillingarverk|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] einingahópa við [!INCLUDE[d365fin](includes/d365fin_md.md)] mælieiningar.|Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÆLIEINING|  
|Tölfræði um viðskiptamann - Dynamics 365 for Sales samstilling|Uppfærir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga með nýjustu [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamannagögnunum. Í [!INCLUDE[crm_md](includes/crm_md.md)] birtast upplýsingarnar í **Tölfræði fyrir Business Central-reikning** skjámynd flýtiyfirlits yfir reikninga sem eru tengdir við [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamenn.<br /><br /> Einnig er hægt að uppfæra þessi gögn handvirkt úr hverri viðskiptamannafærslu. Frekari upplýsingar er að finna í [Hvernig á að: Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Athugið:** Þessi verkraðarfærsla á aðeins við ef [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættingarlausnin er sett upp í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Um samþættingarlausn Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Á ekki við.|Á ekki við.|   

## <a name="to-view-the-synchronization-job-log"></a>Til að skoða kladda samstillingarverks  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Samstillingarkladdi samþættingar** og veldu síðan tengda tengilinn.
2.  Ef ein eða fleiri villur koma upp í samstillingarverki birtist fjöldi villna í dálkinum **Mistókst** . Veljið þá tölu til að skoða villur í verkinu.  

    > [!TIP]  
    > Þú getur skoðað allar villur í samstillingaverkum með því að opna villukladda samstillingarverka beint.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Til að skoða kladda samstillingarverks úr töfluvörpunum  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Varpanir samþættingartöflu** og veldu síðan viðeigandi tengil.
2.  Á síðunni **Vörpun samþættingartöflu** skal velja færslu og síðan velja **Kladdi fyrir samstillingarverk samþættingar**.  

## <a name="to-view-the-synchronization-error-log"></a>Til að skoða villukladda samstillingar  
* Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Samstillingarvilla samþættingar** og veldu síðan tengda tengilinn.

## <a name="see-also"></a>Sjá einnig  
[Samstilling gagna í Business Central og Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Samstilla töfluvarpanir handvirkt](admin-manual-synchronization-of-table-mappings.md)  
[Áætla samstillingu milli Business Central og Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Um samstillingu Dynamics 365 Business Central við Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



