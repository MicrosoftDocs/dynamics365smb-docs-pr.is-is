---
title: "Hvernig á að: Vinna með tilkynningasniðmát | Microsoft Docs"
description: "Tilkynningar eru sendar til verkflæðisnotenda til að tilkynna þeim um skref sem þeir verað að taka eða upplýsa þá um stöðu verkflæðisskrefa. Notandi setur upp hverjir fá tilkynningar og hvenær með þvíað setja upp samþykktarnotendur, tilkynningaáætlun notenda og umrædd verkflæðisviðbrögð til að skilgreina móttakanda tilkynningar. Nánari upplýsingar er að finna í Uppsetning [Uppsetning Verkflæði Tilkynningar](across-setting-up-workflow-notifications.md)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9163bdb48a10d9b36b670e4bc67c696fbade6b37
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-notification-templates"></a>Hvernig á að: Vinna með tilkynningasniðmát
Tilkynningar eru sendar til verkflæðisnotenda til að tilkynna þeim um skref sem þeir verað að taka eða upplýsa þá um stöðu verkflæðisskrefa. Notandi setur upp hverjir fá tilkynningar og hvenær með þvíað setja upp samþykktarnotendur, tilkynningaáætlun notenda og umrædd verkflæðisviðbrögð til að skilgreina móttakanda tilkynningar. Nánari upplýsingar er að finna í [Uppsetning Verkflæði Tilkynningar](across-setting-up-workflow-notifications.md).  

 Tilkynningar byggjast á sniðmátum sem skilgreina efni og útlit tilkynningarinnar. Hægt er að flytja út efni úr tilkynningasniðmáti, breyta því og síðan flytja það inn í sama eða nýtt tilkynningasniðmát. Þessu er lýst í eftirfarandi ferli.  

 Almenn útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur þrjú tilkynningasniðmát, eitt þar sem tilkynnt er um samþykktarbeiðnir, annað til að tilkynna um nýjar færslur og þriðja til að tilkynna um samþykktarbeiðnir sem komnar eru fram yfir tíma. Þessar þrjár fyrirframskilgreindur tilkynningasniðmát styðja **Tölvupóstur** og **Athugasemd** sem tilkynningaraðferð. Til að skoða efnisinnihald sniðmátanna þriggja skal skoða kaflann „Efnisinnihald tilkynningasniðmáta“ í þessum kafla.

## <a name="to-create-a-new-notification-template"></a>Til að búa til nýtt tilkynningasniðmát  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tilkynningasniðmát** og velja svo viðeigandi tengil.  
2.  Í glugganum **Tilkynningasniðmát** skal velja aðgerðina **Nýtt**.  
3.  Fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kóti**|Auðkenna tilkynningasniðmátið.|  
    |**Lýsing**|Lýsa tilkynningasniðmátinu.|  
    |**Aðferð tilkynningar**|Tilgreina hvort tilkynningin er send með tölvupósti eða sem athugasemd.|  
    |**Tegund**|Tilgreina viðskiptaferlið sem tilkynningin verður notuð fyrir.<br /><br /> Velja eina af eftirtöldum gerðum:<br /><br /> -   **Samþykkt** tilgreinir að sniðmát sé notað til að tilkynna notendum í samþykktarverkflæði.<br />-   **Ný færsla** tilgreinir að sniðmátið sé notað til að tilkynna notendum þegar ný færsla, svo sem viðskiptamannaspjald, bíði samþykktar þeirra.<br />-   **Komið fram yfir á tíma** tilgreinir að sniðmát sé notað til að tilkynna notendum um samþykktarbeiðnir sem eru komnar fram yfir á tíma.|  
    |**Sjálfgefið**|Tilgreina hvort tilkynningasniðmát verði sjálfkrafa notað.|  

## <a name="to-modify-a-notification-template"></a>Tilkynningarsniðmáti breytt  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tilkynningasniðmát** og velja svo viðeigandi tengil.  
2.  Í glugganum **Tilkynningasniðmát** skal velja tilkynningasniðmátið sem á að breyta.  
3.  Velja skal **Efni útflutningssniðmáts** aðgerðina.  
4.  Í glugganum **Flytja út skrá** skal velja hnappinn **Vista** og svo velja heiti og vista HTML-skrá í viðeigandi staðsetningu.  
5.  Hægrismellið á skrána, veljið **Opna með** og veljið síðan viðkomandi forrit.  

    > [!NOTE]  
    >  Efni fyrir tilkynningasniðmát af gerðinni netfang er Í HTML-sniði. Efni fyrir tilkynningasniðmát af gerðinni athugasemd er Í TXT-sniði.  
6.  Breyta efni tilkynningasniðmátsins með því að bæta við, breyta, eða fjarlægja breytur til að skilgreina tilkynningarefni sem óskað er eftir. Sjá fyrir frekari upplýsingar í kaflanum „Efnisinnihald tilkynningasniðmáts“.  

    Halda áfram með innflutningur á breyttu efni í sama eða nýtt tilkynningasniðmát.  
7.  Til að breyta tilkynningasniðmáti sem var flutt inn skal velja það sniðmát sem var valið í skrefi 2 í glugganum **Tilkynningasniðmát**.  

    Að öðrum kosti skal flytja breytt efni sniðmáts inn í nýtt tilkynningasniðmát, fylgja ferlinu „Að stofna nýtt tilkynningasniðmát“ og velja svo nýja tilkynningasniðmátið.  
8.  Velja skal **Efni innflutningssniðmáts** aðgerðina.  
9. Ef breyta skal tilkynningasniðmáti sem þegar er fyrir hendi veljið þá hnappinn **Já** á skilaboðunum sem fjalla um að skrifa yfir núverandi sniðmát.  
10. Í glugganum **Velja skrá til að flytja inn** skal velja HTML-skrána sem breytt var í skrefi 6 og svo velja hnappinn **Opna**.  

Tilkynningasniðmátið sem fyrir var eða nýja sniðmátið í glugganum **Tilkynningasniðmát** hefur nú verið uppfært með breyttu efni.  

### <a name="content-of-the-notification-templates"></a>Efnisinnihald tilkynningasniðmáts  
Þrjár gerðir tilkynningasniðmáts, **Ný færsla**, **Samþykki** og **Komin fram yfir tíma**, hafa allar ólíkt innihald.  

Færibreytugildi eru sjálfkrafa settar inn í tilkynningar í samræmi við tilkynningasniðmátið.  

#### <a name="new-record"></a>Ný færsla  
 ![NAV&#95;notification&#95;template&#95;new&#95;record&#95;type](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Samþykki  
 ![NAV&#95;notification&#95;template&#95;approval&#95;type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Komið fram yfir  
 ![NAV&#95;notification&#95;overdue&#95;type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Sjá einnig  
 [Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)   
 [Hvernig á að: Setja upp tölvupóst](madeira-how-setup-email.md)   
 [Hvernig á að: Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)   
 [Hvernig á að: Setja upp notendur sem samþykkjendur](across-how-to-set-up-approval-users.md)   
 [Hvernig á að: Búa til verkflæði](across-how-to-create-workflows.md)   
 [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)   
 [Verkflæði](across-workflow.md)   

