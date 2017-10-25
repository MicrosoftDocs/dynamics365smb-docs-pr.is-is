---
title: "Hvernig á að: Tilgreina hvenær og hvernig á að fá tilkynningar | Microsoft Docs"
description: "Þegar notendur eru settir upp í samþykktarverkflæði verður að tilgreina í gluggunum Tilkynningagrunnur og Tilkynningaáætlun hvenær og hvernig hver notandi fær tilkynningar um skref í samþykktarverkflæði. Einstakir notendur geta einnig breytt tilkynningastillingum sínum með þí að velja hnappinn Breyta tilkynningastillingum á hverri tilkynningu."
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
ms.openlocfilehash: db0e3f159a0d6a793ed5881118ecff6d0bf6a529
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-specify-when-and-how-to-receive-notifications"></a>Hvernig á að: Tilgreina hvenær og hvernig á að fá tilkynningar
Þegar notendur eru settir upp í samþykktarverkflæði verður að tilgreina í gluggunum **Tilkynningagrunnur** og **Tilkynningaáætlun** hvenær og hvernig hver notandi fær tilkynningar um skref í samþykktarverkflæði. Einstakir notendur geta einnig breytt tilkynningastillingum sínum með þí að velja hnappinn **Breyta tilkynningastillingum** á hverri tilkynningu.  

 Áður en hægt er að setja upp tilkynningastillingar samþykktarnotanda verður að setja notanda upp sem samþykktarnotanda Nánari upplýsingar eru í [Hvernig á að: Setja upp notendur sem samþykkjendur](across-how-to-set-up-approval-users.md)  

 Með því að setja upp tilkynningasniðmát er útlit og innihald tilkynninga skilgreint. Nánari upplýsingar eru í [Hvernig á að: Vinna með tilkynningasniðmát](across-how-to-manage-notification-templates.md).  

 Mörg skref samþykktarverkflæðis snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu. Tengd viðbrögð eru að tilkynning er sent Notanda 2, sem er samþykkjandi. Í næsta skrefi verkflæðis getur tilvik verið að Notandi 2 samþykki nýja færslu. Tengd viðbrögð eru að tilkynning er sent Notanda 3 til að hefja ferli með samþykktri færslu. Í öllum skref verkflæðis sem snúast um samþykki eru tilkynningar tengdar samþykktarfærslu. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Tilgreinið hvenær og hvernig notendur fá tilkynningar  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning samþykkts notanda** og velja svo viðeigandi tengil.  
2.  Veljið línu fyrir notanda sem á að nota til að setja upp tilkynningarstillingar fyrir og því næst er valið **Uppsetning tilkynninga**.  
3.  Í glugganum **Tilkynningagrunnur** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Gerð tilkynningar**|Tilgreinið hvaða gerð tilviks tilkynning fjallar um.<br /><br /> Einn af eftirfarandi kostum er valinn:<br /><br /> -   **Ný færsla** tilgreinir að tilkynningin sé um nýja færslu, svo sem skjal, sem notandinn þarf að bregðast við.<br />-   **Samþykktir** tilgreinir að tilkynningin fjalli um eina eða fleiri samþykktarbeiðnir.<br />-   **Komið fram yfir tíma** tilgreinir að tilkynningin er um áminningu notenda um að þeir séu seinir að bregðast við viðburði.|  
    |**Sniðmátskóði tilkynningar**|Tilgreinið kóða tilkynningasniðmátsins sem er notað til að stofna tilkynningar fyrir notandann.|  
    |**Snjallar tilkynningar**|Tilgreinið hvort notandinn fær eina tilkynningu fyrir hvern viðburð eða uppsafnaðar tilkynningar.<br /><br /> Ef gátreitur **Snjallar tilkynningar** er ekki valinn mun notandi fá tilkynningar sem safna saman upplýsingum um tilvik sem eiga sér stað innan sama endurtekningarmynsturs í tilkynningaáætlun.|  

     Tilgreint hefur verið hvernig notandi fær tilkynningar. Halda áfram að ákveða hvenær notandi fær tilkynningar.  

4.  Veldu **Áætlun tilkynninga**.  
5.  Í glugganum **Áætlun tilkynninga** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Endurtekning**|Tilgreinið endurtekningarmynstur þar sem notandi fær tilkynningar.|  
    |**Tími**|Tilgreinir hvenær dagsins notandinn fær tilkynningar þegar gildið í **Endurtekning** reitnum er frábrugðið **Strax**.|  
    |**Dagleg tíðni**|Tilgreinið á hvers kyns dögum notandinn fær tilkynningar þegar gildið í **Endurtekning** reitnum er **Daglega**.<br /><br /> Velja **Virkur dagur** til að fá tilkynningar hvern virkan dag vikunnar. Velja **Daglega** til að fá tilkynningar hvern dag vikunnar, þar á meðal um helgar.|  
    |**Mánudagur** til **Sunnudags**|Tilgreinið á hvers kyns dögum notandinn fær tilkynningar þegar gildið í **Endurtekning** reitnum er **Vikulega**.|  
    |**Mánaðardagur**|Tilgreinið hvort notandinn fær tilkynningar á fyrsta, síðasta eða tilteknum degi mánaðarins.|  
    |**Dagsetning mánaðarlegrar tilkynningar**|Tilgreinið á hvaða degi mánaðarins notandinn fær tilkynningar þegar gildið í **Mánaðardagur** reitnum er **Sérsniðið**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Breyta hvenær og hvernig notandi fær tilkynningar  
1.  Í einni tilkynningu sem borist hefur, annaðhvort í tölvupósti eða sem athugasemd, skal velja hnappinn **Breyta tilkynningastillingum**.  
2.  Í glugganum **Tilkynningagrunnur** skal breyta tilkynningarstillingunum eins og lýst er í fyrra ferli.  

## <a name="see-also"></a>Sjá einnig  
 [Hvernig á að: Setja upp notendur sem samþykkjendur](across-how-to-set-up-approval-users.md)   
 [Hvernig á að: Vinna með tilkynningasniðmát](across-how-to-manage-notification-templates.md)   
 [Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)   
 [Uppsetning verkflæðis](across-set-up-workflows.md)   
 [Nota verkflæði](across-use-workflows.md)

