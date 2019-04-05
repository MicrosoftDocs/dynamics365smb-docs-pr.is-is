---
title: 'Hvernig á að: Tilgreina hvenær og hvernig á að fá tilkynningar | Microsoft Docs'
description: Þegar notendur eru settir upp í samþykktarverkflæði verður að tilgreina á síðunum Tilkynningagrunnur og Tilkynningaáætlun hvenær og hvernig hver notandi fær tilkynningar um skref í samþykktarverkflæði. Einstakir notendur geta einnig breytt tilkynningastillingum sínum með þí að velja hnappinn Breyta tilkynningastillingum á hverri tilkynningu.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/08/2018
ms.author: sgroespe
ms.openlocfilehash: 8bb1b2815740e3acfeb984c1b7cbad160dcd1016
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800257"
---
# <a name="specify-when-and-how-to-receive-notifications"></a>Tilgreina hvenær og hvernig á að fá tilkynningar
Þegar notendur eru settir upp í samþykktarverkflæði verður að tilgreina á síðunum **Tilkynningagrunnur** og **Tilkynningaáætlun** hvenær og hvernig hver notandi fær tilkynningar um skref í samþykktarverkflæði. Einstakir notendur geta einnig breytt tilkynningastillingum sínum með þí að velja hnappinn **Breyta tilkynningastillingum** á hverri tilkynningu.  

 Áður en hægt er að setja upp tilkynningastillingar samþykktarnotanda verður að setja notanda upp sem samþykktarnotanda Nánari upplýsingar eru í [Setja upp notendur sem samþykkjendur](across-how-to-set-up-approval-users.md).  

 Hægt er að tilgreina útlit tölvupóststilkynninga með því að sérstilla Skýrslu 1320, Tilkynningapóstur. Frekari upplýsingar er að finna á [Búa til og breyta sérsniðnu skýrslu- eða skjalaútliti](ui-how-create-custom-report-layout.md).  

 Mörg skref samþykktarverkflæðis snúast um að láta notendur vita að tilvik hafi átt sér stað og þeir þurfi að bregðast við því. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu. Tengd viðbrögð eru að tilkynning er sent Notanda 2, sem er samþykkjandi. Í næsta skrefi verkflæðis getur tilvik verið að Notandi 2 samþykki nýja færslu. Tengd viðbrögð eru að tilkynning er sent Notanda 3 til að hefja ferli með samþykktri færslu. Í öllum skref verkflæðis sem snúast um samþykki eru tilkynningar tengdar samþykktarfærslu. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

## <a name="specify-when-and-how-users-receive-notifications"></a>Tilgreinið hvenær og hvernig notendur fá tilkynningar  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **samþykki notandauppsetningar** og veldu síðan tengda tengilinn.  
2.  Veljið línu fyrir notanda sem á að nota til að setja upp tilkynningarstillingar fyrir og því næst er valið **Uppsetning tilkynninga**.  
3.  Á síðunni **Tilkynningagrunnur** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Gerð tilkynningar**|Tilgreinið hvaða gerð tilviks tilkynning fjallar um.<br /><br /> Einn af eftirfarandi kostum er valinn:<br /><br /> -   **Ný færsla** tilgreinir að tilkynningin sé um nýja færslu, svo sem skjal, sem notandinn þarf að bregðast við.<br />-   **Samþykktir** tilgreinir að tilkynningin fjalli um eina eða fleiri samþykktarbeiðnir.<br />-   **Komið fram yfir tíma** tilgreinir að tilkynningin er um áminningu notenda um að þeir séu seinir að bregðast við viðburði.|  
    |**Aðferð tilkynningar**|Tilgreina hvort tilkynningin er tölvupóstur eða innri athugasemd.|

    Hægt er að tilgreina útlit tölvupóststilkynninga með því að sérstilla Skýrslu 1320, Tilkynningapóstur. Frekari upplýsingar er að finna á [Búa til og breyta sérsniðnu skýrslu- eða skjalaútliti](ui-how-create-custom-report-layout.md).

    Tilgreint hefur verið hvernig notandi fær tilkynningar. Halda áfram að ákveða hvenær notandi fær tilkynningar.  

4.  Veldu **Áætlun tilkynninga**.  
5.  Á síðunni **Áætlun tilkynninga** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

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
2.  Á síðunni **Tilkynningagrunnur** skal breyta tilkynningarstillingunum eins og lýst er í fyrra ferli.  

## <a name="see-also"></a>Sjá einnig  
 [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)   
 [Búa til og breyta sérsniðnu skýrslu- eða skjalaútliti](ui-how-create-custom-report-layout.md)   
 [Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)   
 [Uppsetning verkflæðis](across-set-up-workflows.md)   
 [Nota verkflæði](across-use-workflows.md)
