---
title: Tilgreina hvenær og hvernig eigi að taka á móti Verkflæðistilkynningum
description: Þegar notendur eru settir upp í samþykktarverkflæði er hægt að tilgreina hvernig og hvenær hver samþykktarnotandi fær tilkynningar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/09/2022
ms.author: edupont
ms.openlocfilehash: 7b70da08a4fb8ffdb7ff16544b511576f9af0f86
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585510"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Tilgreina hvenær og hvernig eigi að taka á móti Verkflæðistilkynningum

Þegar samþykktarnotendur eru settir upp í verkflæði þar sem óskað er eftir að samþykkja breytingar, eins og þegar nýjar færslur eru stofnaðar eða þegar einhver biður um samþykki, verður að tilgreina hvernig og hvenær samþykktarnotandinn er látinn vita. Til dæmis er hægt að tilgreina samþykkinotanda til að fá strax tölvupóst þegar einhver stofnar nýjan viðskiptavin. Einnig er hægt að raða tilkynningunum sem á að halda og afhenda þær t.d. með vikulegu eða mánaðarlegu millibili.

Fólk getur einnig breytt uppsetningu tilkynninga með því að velja **Breyta tilkynningastillingum** á hvaða tilkynningu sem er.  

> [!NOTE]
> Tilkynningar eru afgreiddar samkvæmt tilkynningastillingum fyrir móttakanda, ekki sendanda. Það er mikilvægur greinarmunur því það þýðir að þegar einhver biður um samþykki sem hluti af verkflæði þá er beiðni þeirra ekki endilega send strax. Þess í stað verður hann afhentur í samræmi við tilkynningaáætlunina sem tilgreind er í tilkynningastillingum samþykkjanda.

Áður en hægt er að setja upp tilkynningar um samþykki notanda þarf að setja upp notandann sem samþykkinotanda. Frekari upplýsingar um [uppsetningu Samþykktarnotenda](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Ef þú vilt nota tölvupóst sem tilkynningarmáta þarf að setja tölvupóst upp fyrir bæði sendanda og móttakanda í [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar er að setja upp í [tölvupósti](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Skref í verkflæði

Margar samþykktarverkflæðisskref eru um að tilkynna notendum að tilvik sem þeir verða að bregðast við hafi átt sér stað. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu. Tengd viðbrögð eru að tilkynning er sent Notanda 2, sem er samþykkjandi. Í næsta skrefi verkflæðis getur tilvik verið að Notandi 2 samþykki nýja færslu. Tengd viðbrögð eru að tilkynning er sent Notanda 3 til að hefja ferli með samþykktri færslu. Fyrir verkflæðisskref sem tengjast samþykktum er hver tilkynning bundin við samþykktarfærslu. Frekari upplýsingar á [verkflæði](across-workflow.md).  

## <a name="specify-when-and-how-approval-users-receive-notifications"></a>Tilgreina hvenær og hvernig taka eigi við tilkynningum vegna samþykkinotenda  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **notendauppsetningu** samþykkisins, velja síðan tengda tengilinn.  
2. Velja skal línuna fyrir notandann sem setja á upp óskir um tilkynningar fyrir og velja **síðan uppsetningaraðgerðina** tilkynning.  
3. **Á uppsetningarsíðu** tilkynninga er fyllt út í reitina eins og lýst er í eftirfarandi töflu.  

   > [!NOTE]
   > Ef Uppsetningarsíða **tilkynningarinnar er opnuð** frá **uppsetningarsíðu** samþykktarnotanda er tilkynningaskyldan tengd notandanum. Samþykkinotandinn skal alltaf taka við verkflæðistilkynningum í samræmi við uppsetningu tilkynningarinnar. Ef aðgerðin segja *aðgerðina er notuð* til að opna **uppsetningarsíðu** tilkynninga, gildir tilkynningauppsetningin fyrir alla notendur.

   |Svæði|Lýsing|
   |-----|-----------|
   |**Gerð tilkynningar**|Tilgreina skal þá tegund tilvika sem tilkynningin tekur til.<br /><br /> Einn af eftirfarandi kostum er valinn:<br /><br /> -   **Ný færsla** tilgreinir að tilkynningin sé um nýja færslu, svo sem skjal, sem notandinn þarf að bregðast við.<br />-   **Samþykktir** tilgreinir að tilkynningin fjalli um eina eða fleiri samþykktarbeiðnir.<br />-   **Gjaldfelling** Tilgreinir að tilkynningin eigi að minna notendur á að þeir séu seint í leikgerð á atburði.|
   |**Aðferð tilkynningar**|Tilgreina hvort tilkynningin er tölvupóstur eða innri athugasemd.|

   Hægt er að tilgreina útlit tölvupóststilkynninga með því að sérstilla Skýrslu 1320, Tilkynningapóstur. Frekari upplýsingar er að [Stofna og breyta skipan](ui-how-create-custom-report-layout.md) sérsniðinnar skýrslu.

   Notandi hefur nú tilgreint hvernig notandinn fær tilkynningar. Halda áfram að ákveða hvenær notandi fær tilkynningar.  
4. Veldu **Áætlun tilkynninga**.  
5. **Á Tilkynningaáætlun** síðu er fyllt út í reitina eins og lýst er í eftirfarandi töflu.  

   |Svæði|Lýsing|
   |-----|-----------|
   |**Endurtekning**|Tilgreinið ítrekunarmynstur sem tilkynningar eru sendar til notanda.|
   |**Tími**|Tilgreinið hvað tíma dagtilkynninga eru sendar til notandans þegar gildið í **endurtekningarsvæðinu** er eitthvað annað en **samstundis**.|
   |**Dagleg tíðni**|Tilgreinið á hvers kyns dögum notandinn fær tilkynningar þegar gildið í **Endurtekning** reitnum er **Daglega**.<br /><br /> Velja **vikudaga** til að taka á móti tilkynningum alla daga vinnuvikunnar. Velja **Daglega** til að fá tilkynningar hvern dag vikunnar, þar á meðal um helgar.|
   |**Mánudagur** til **Sunnudags**|Tilgreinið á hvers kyns dögum notandinn fær tilkynningar þegar gildið í **Endurtekning** reitnum er **Vikulega**.|
   |**Mánaðardagur**|Tilgreinið hvort notandinn fær tilkynningar á fyrsta, síðasta eða tilteknum degi mánaðarins.|
   |**Dagsetning mánaðarlegrar tilkynningar**|Tilgreinið á hvaða degi mánaðarins notandinn fær tilkynningar þegar gildið í **Mánaðardagur** reitnum er **Sérsniðið**.|

## <a name="change-when-and-how-you-receive-notifications"></a>Breyta hvenær og hvernig notandi fær tilkynningar

1. Á einni af þeim tilkynningum sem þú hefur móttekið, annaðhvort sem tölvupóstur eða athugasemd, skaltu velja **Breyta tilkynningastillingum**.  
2. Á uppsetningarsíðu **tilkynningarinnar er breytt tilkynningarkjörum eins og þeim er lýst í skrefum 3-5 hér að** framan.
   1. Staðfesta að rétt tilkynning sé valin undir **reitnum Tilkynningagerð**.
   2. Veljið hvort fá eigi tilkynningu um tölvupóst eða athugasemd undir **Tilkynningaraðferðarsvæði**.
   3. **Veljið Tilkynningaráætlunina** til að breyta tíðni og endurtekningu þeirra tilkynninga sem sendar eru.

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Uppsetning tilkynninga um samþykktarverkflæði](across-setting-up-workflow-notifications.md)  
[Uppsetning Samþykktarverkflæðis](across-set-up-workflows.md)  
[Nota samþykktarverkflæði](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
