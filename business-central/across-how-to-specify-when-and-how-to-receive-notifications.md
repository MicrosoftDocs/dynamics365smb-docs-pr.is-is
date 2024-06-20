---
title: Tilgreina hvenær og hvernig tilkynningar um verkflæði berast
description: Þegar notendur eru settir upp í verkflæði samþykkta er hægt að tilgreina hvernig og hvenær hver samþykktarnotandi fær tilkynningar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '663, 1500, 1512, 1513,'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Tilgreina hvenær og hvernig tilkynningar um verkflæði berast

Í verkflæðum sem krefjast þess að einhver samþykki breytingar verði settar upp þarf að setja upp samþykktarnotendur sem samþykkja eða hafna breytingum. Til dæmis gæti einhver samþykkt nýjar færslur. Mikilvægur hluti notandauppsetningar samþykktar er að tilgreina hvernig og hvenær notanda er tilkynnt um breytinguna. Til dæmis er hægt að tilgreina að samþykkisnotandi fái strax tölvupóst þegar einhver stofnar nýjan viðskiptamann. Einnig er hægt að tímasetja tilkynningar sem eiga að afhenda, til dæmis vikulega eða mánaðarlega.

Einnig er hægt að breyta tilkynningauppsetningu með því að **velja Breyta tilkynningastillingum** í hvaða tilkynningu sem er.  

> [!NOTE]
> Tilkynningar eru afhentar samkvæmt tilkynningastillingum móttakanda, ekki sendanda. Það er mikilvægur aðgreining vegna þess að það þýðir að þegar einhver biður um samþykki sem hluta af verkflæði er beiðni þeirra ekki endilega send strax. Þess í stað er hún afhent samkvæmt tilkynningaáætluninni sem tilgreind er í tilkynningastillingum samþykkjanda.

Áður en hægt er að setja upp tilkynningarkjörstillingar samþykktarnotanda verður að setja notandann upp sem samþykktarnotanda. Frekari upplýsingar má finna á [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Til að nota tölvupóst sem tilkynningaraðferð verður að setja upp tölvupóst fyrir sendanda og móttakanda [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar má finna á [Setja upp tölvupóst](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Skref í verkflæðum

Mörg verkflæðisskref samþykktar snýst um að tilkynna notendum um atburð sem þeir verða að bregðast við. Til dæmis getur eitt skref í verkflæði verið að tilvik óski eftir að Notandi 1 samþyki nýja færslu. Tengd viðbrögð eru að tilkynning er sent Notanda 2, sem er samþykkjandi. Í næsta skrefi verkflæðis getur tilvik verið að Notandi 2 samþykki nýja færslu. Tengd viðbrögð eru að tilkynning er sent Notanda 3 til að hefja ferli með samþykktri færslu. Í verkflæðisskrefum sem taka til samþykkta er hver tilkynning bundin samþykktarfærslu. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

## <a name="specify-when-and-how-approval-users-receive-notifications"></a>Tilgreina hvenær og hvernig notendur fá tilkynningar um samþykktir

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samþykktarnotanda**, velja síðan viðkomandi tengil.  
2. Velja skal línuna fyrir notandann sem setja á upp kjörstillingar tilkynninga fyrir og svo skal velja aðgerðina **Tilkynningagrunnur** .  
3. Á síðunni **Uppsetning verkflæðistilkynninga** skal fylla út reitina eins og lýst er í eftirfarandi töflu.  

   > [!NOTE]
   > Ef síðan Tilkynningargrunnur **verkflæðis er opnuð** á síðunni **Notandauppsetning samþykktar er tilkynningaruppsetningin** tengd samþykktarnotandanum. Notandinn sem samþykkir fær alltaf tilkynningar um verkflæði samkvæmt uppsetningu tilkynninga. Ef aðgerðin *Segja mér* er notuð til að opna síðuna **Tilkynningargrunnur** verkflæðis á uppsetning tilkynninga við alla notendur.

   |Svæði|Heimildasamstæða|
   |-----|-----------|
   |**Gerð tilkynningar**|Tilgreina skal tegund atviksins sem tilkynningin snýst um.<br /><br /> Einn af eftirfarandi kostum er valinn:<br /><br /> -   **Ný færsla** tilgreinir að tilkynningin sé um nýja færslu, svo sem skjal, sem notandinn þarf að bregðast við.<br />-   **Samþykktir** tilgreinir að tilkynningin fjalli um eina eða fleiri samþykktarbeiðnir.<br />-   **Liðin** dagsetning tilgreinir að tilkynningin sé til að minna notendur á að þeir séu of seinir í að starfa eftir atburð.|
   |**Aðferð tilkynningar**|Tilgreina hvort tilkynningin er tölvupóstur eða innri athugasemd.|

   Hægt er að tilgreina útlit tölvupóststilkynninga með því að sérstilla Skýrslu 1320, Tilkynningapóstur. Frekari upplýsingar eru í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).

   Tilgreint var hvernig notandi fær tilkynningar. Tilgreina skal hvenær notandi fær tilkynningar.  
4. Veldu **Áætlun tilkynninga**.  
5. Á síðunni **Tilkynningaáætlun** skal fylla út reitina eins og lýst er í eftirfarandi töflu.  

   |Svæði|Heimildasamstæða|
   |-----|-----------|
   |**Endurtekning**|Tilgreina ítrekunarmynstur þar sem tilkynningar eru sendar notandanum.|
   |**Tími**|Tilgreina hvenær dagstilkynningar eru sendar notandanum þegar gildið í reitnum **Endurtekning** er allt annað en **samstundis**.|
   |**Dagleg tíðni**|Tilgreinið á hvers kyns dögum notandinn fær tilkynningar þegar gildið í **Endurtekning** reitnum er **Daglega**.<br /><br /> Velja **vikudag** til að fá tilkynningar alla daga vinnuvikunnar. Velja **Daglega** til að fá tilkynningar hvern dag vikunnar, þar á meðal um helgar.|
   |**Mánudagur** til **Sunnudags**|Tilgreinið á hvers kyns dögum notandinn fær tilkynningar þegar gildið í **Endurtekning** reitnum er **Vikulega**.|
   |**Mánaðardagur**|Tilgreinið hvort notandinn fær tilkynningar á fyrsta, síðasta eða tilteknum degi mánaðarins.|
   |**Dagsetning mánaðarlegrar tilkynningar**|Tilgreinið á hvaða degi mánaðarins notandinn fær tilkynningar þegar gildið í **Mánaðardagur** reitnum er **Sérsniðið**.|

## <a name="change-when-and-how-you-receive-notifications"></a>Breyta hvenær og hvernig notandi fær tilkynningar

1. Í einni af tilkynningunum sem þú fékkst, annaðhvort sem tölvupóst eða athugasemd, skal velja **Breyta tilkynningastillingum**.  
2. Á síðunni **Tilkynningargrunnur** verkflæðis skal breyta kjörstillingum tilkynninga eins og lýst er í skrefum 3-5 hér á undan.
   1. Staðfesta skal að rétt tilkynning sé valin í reitnum **Tegund tilkynningar** .
   2. Velja skal hvort fá eigi tilkynningu með tölvupósti eða athugasemd í reitnum  **Tilkynningaraðferð** .
   3. Tilkynningaáætlun **er** valin til að breyta tíðni og endurtekningum sem sendar eru tilkynningar í.

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Uppsetning tilkynninga um samþykktarverkflæði](across-setting-up-workflow-notifications.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Nota Samþykktarverkflæði](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
