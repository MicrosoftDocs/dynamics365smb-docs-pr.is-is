---
title: Setja upp skýrslur til að prenta á sérstökum prenturum | Microsoft Docs
description: Kynntu þér hvernig skal tilgreina prentara fyrir skýrslu og nota síðuna „Prentaraval“.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e088d13ead96111023df7781f0d6d1c1dcd58cfc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760293"
---
# <a name="set-up-printers"></a>Setja upp prentara
Vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] er skýjaþjónusta nær hún ekki til staðbundinna prentara sem eru tengdir vélum notanda. Hins vegar er hægt að tengjast skýjavirkum prenturum. Í almennri útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] er skýjaprentari með heitið **Tölvupóstsprentari** uppsettur sem viðbót og er tilbúinn til notkunar eftir upphaflega uppsetningu.

Ef skýjaprentari er ekki uppsettur, eða ef uppsettur prentari mistekst, er prentun valin sjálfkrafa fyrir prentvalkosti vafrans. Þetta er gefið í skyn með þessu gildi í reitnum **Prentari** á síðu skýrslubeiðna: *(ekkert, vafrinn sér um þetta)*.

Á síðunni **Prentarastjórnun** er hægt að skoða uppsetta prentara. Þegar búið er að setja upp einn eða fleiri prentara er hægt að opna síðuna **Prentaraval** til að setja upp fyrir notandareikninginn hvaða tilteknu skýrslur á að prenta fyrir tiltekinn prentara.

Þegar prentari er settur upp og úthlutaður á tilteknar skýrslur er hægt að prenta skýrslu með því að velja hnappinn **Prenta** á síðu skýrslubeiðni. Frekari upplýsingar er að finna í [Prenta skýrslu](ui-work-report.md#PrintReport).

### <a name="sizing-print-jobs"></a>Stærð prentverka stillt
Skýjaprentun er hönnuð fyrir skjöl af hæfilegri stærð. Flestar skýjaþjónustur, þ.m.t. PrintNode og HP ePrint, eru með 10 MB hámark fyrir hvert verk. Ef þú þarft að prenta stærri skýrslur gætirðu þurft að skipta þeim í margar útprentanir.

## <a name="to-set-up-a-printer"></a>Uppsetning prentara
Á síðunni **Prentarastjórnun** er hægt að skoða prentarana sem eru settir upp og hægt er að fá aðgang að síðunni **Stillingar** fyrir hvern prentara til að breyta fyrirliggjandi uppsetningu eða setja upp nýjan prentara.

Í eftirfarandi ferli er útskýrt hvernig skal setja upp fyrirliggjandi prentarann **Tölvupóstprentari**, sem er foruppsett viðbót.

> [!NOTE]
> Til að nota tölvupóstsprentun er nauðsynlegt að setja upp tölvupóstsvirkni. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Prentarastjórnun** og veldu síðan tengda tengilinn.
2. Velja skal línu fyrir prentarann **Tölvupóstprentari** og velja síðan aðgerðina **Breyta stillingum prentara**.
3. Á síðunni **Stillingar** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Velja verður viðeigandi pappírsstærð handvirkt fyrir prentara þar sem enginn staðbundinn prentari eða notandastillingar geta verið geymdir.
    >
    > Hafið í huga að viðbót tölvupóstsprentara er sjálfgefið stillt á pappírsstærð **A4**, sem er til dæmis ekki hentugt í Norður-Ameríku.
4. Til að gera prentara sjálfgefinn, skal á síðunni **Prentarastjórnun** velja **Velja sem sjálfgefinn prentara**.

### <a name="privacy-notice"></a>Persónuverndaryfirlýsing
Ef viðbót tölvupóstsprentara er notuð verða öll eða sum prentverk send til netfangsins sem gefið var upp þegar prentarinn var grunnstilltur. Eindregið er mælt með því að einkvæmt tölvupóstskenni sé tengt við prenttæki með því að nota aðeins opinbera þjónustu sem framleiðandi vélbúnaðar veitir, svo sem HP ePrint, KonicaMinolta EveryonePrint eða Epson Email Print.

Nauðsynlegt er að gera allar nauðsynlegar persónuverndarráðstafanir, þar á meðal að tryggja að prentlausnin fyrir tölvupóst hafi rétt skilgreindar heimildir, persónuverndarstillingar og varðveislureglur. Það er á ábyrgð notanda að gefa upp rétt, staðfest og starfhæft netfang. Frekari upplýsingar er að finna í [Yfirlýsing Microsoft um persónuvernd](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>Til að velja hvaða prentara prenta hvaða skýrslur

Á síðunni **Prentaraval** er hægt að setja upp fyrir notandareikninginn hvaða skýrslur eru prentaðar með hvaða prentara. Þetta er gagnlegt ef unnið er með mismunandi skýrslur sem krefjast mismunandi prentara vegna staðsetningar þeirra í fyrirtækinu eða útprentunarmöguleika.

> [!IMPORTANT]
> Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum getur síðan **Prentaraval** aðeins verið notuð fyrir prentara sem prentaraviðbótin skilgreinir. Ekki er hægt að nota hana fyrir staðbundna prentara.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Prentaraval** og veldu síðan tengda tengilinn. Að öðrum kosti er hægt að velja prentara á síðunni **Prentarastjórnun** og velja síðan aðgerðina **Prentaraval**.
2. Velja skal aðgerðina **Nýtt** til að bæta við prentaravali fyrir tiltekna skýrslu.
3. Fyllið inn reitina eftir þörfum.

Tilgreind skýrsla er nú uppsett til prentunar í völdum sjálfgefnum prentara.

> [!NOTE]
> Þegar skýrslan sem um ræðir er prentuð út er hægt að hnekkja þessari uppsetningu með því að velja annan prentara á beiðnisíðunni **Prentstillingar**.

> [!NOTE]
> Ef ekki er sett upp skýrsla fyrir tiltekinn prentara á síðunni **Prentaraval** verður hún prentuð á sjálfgefinn prentara fyrirtækisins, eins og það er skilgreint á síðunni **Prentarastjórnun**.

Þú eða stjórnandinn getur einnig notað síðuna **Prentaraval** til að skilgreina önnur afbrigði prentunar fyrir notendur og skýrslur. Eftirfarandi tafla lýsir samsetningu gilda til að tilgreina mismunandi prentunaruppsetningu fyrir skýrslu.

|Til að                                                 |Stilla eftirfarandi gildi:                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Prenta skýrslu í tilteknum prentara fyrir alla notendur |Tilgreinið gildi í reitunum **Kenni skýrslu** og **Prentaraheiti** og skiljið reitinn **Kenni notanda** eftir auðan.|
|Prenta allar skýrslur í tilteknum prentara fyrir tiltekinn notanda|Tilgreinið gildi í reitunum **Kenni notanda** og **Prentaraheiti** og skiljið reitinn **Kenni skýrslu** eftir auðan.|
|Stilla sjálfgefinn prentara fyrir allar skýrslur|Tilgreinið gildi í reitnum **Prentaraheiti** og skiljið reitina **Kenni notanda** og **Kenni skýrslu** eftir auða.|
|Prenta tiltekna skýrslu á sjálfgefnum prentara notanda|Tilgreinið gildi í reitnum **Kenni skýrslu** og skiljið reitina **Prentaraheiti** og **Kenni notanda** eftir auða.|
|Prenta tiltekna skýrslu í tilteknum prentara fyrir tiltekinn notanda|Tilgreinið gildi í öllum þremur reitunum.|

> [!NOTE]
> Sértækara prentaraval hefur forgang fram yfir almennara prentaraval. Prentaraval sem hefur til dæmis gildi í reitunum **Notandakenni**, **Skýrslukenni** og **Prentaraheiti** hefur forgang fram yfir prentaraval sem er með auðar færslur í reitunum **Notandakenni** eða **Skýrslukenni**.

## <a name="see-also"></a>Sjá einnig
[Prenta skýrslu](ui-work-report.md#PrintReport)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Keyra runuvinnslur](ui-how-run-batch-jobs.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
