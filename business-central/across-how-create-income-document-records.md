---
title: Stofna færslur skjala á innleið
description: Notaðu aðrar aðgerðir á síðu skjala á innleið til að fara yfir kvittanir vegna kostnaðar, hafa umsjón með OCR-verkum, umbreyta skrám skjala á innleið og hengja ytri skrár við.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 4244801207874f1629d59d4b3a66de98fb9d2bed
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522407"
---
# <a name="create-incoming-document-records"></a>Stofna færslur skjala á innleið
Á síðunni **Skjöl á innleið** er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur í. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.

Til að skrá ytra skjal í [!INCLUDE[prod_short](includes/prod_short.md)] verður fyrst að stofna eða ljúka við færslu fyrir skjal á innleið. Þú getur gert þetta með handvirkt, eða þú getur tekið mynd af ytra skjal og síðan að búa til skjal á innleið með myndaskrá í viðhengi.

Áður en hægt er að nota valkostinn Skjöl á innleið þarf að framkvæma áskilda uppsetningu. Frekari upplýsingar eru í [Setja upp skjöl á innleið](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Til að samþykkja eða hafna fylgiskjali á innleið
Ef notendur eiga að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt er hægt að setja upp samþykkjendur sem verða að samþykkja færslur áður en þær má vinna.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Valin er línan með skjalinu sem á að samþykkja eða hafna og síðan valið á **Samþykkja** eða **Hafna** aðgerðir.

Ef færsla skjals á innleið er samþykkt er gátreiturinn **Losað** á línu skjal á innleið valinn. Notandi sem stjórnar t.d. stofnun innkaupareikninga getur haldið áfram að vinna úr færslunni.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Til að stofna færslur skjala á innleið með því að taka mynd
> [!NOTE]  
>   Eftirfarandi ferli á aðeins við um [!INCLUDE[prod_short](includes/prod_short.md)] biðlara spjaldtölva og síma.

1. Á forritastikunni skal velja **Stofna skjal á innleið úr myndavél** reitinn og fara svo í skref 4..
2. Að öðrum kosti skal á forritastikunni velja valkostahnappinn, velja **Skjöl á innleið** og velja svo **Öll**.
3. Á síðunni **Skjöl á innleið** skal velja úrfellingarmerkishnappinn og svo **Stofna úr myndavél**. Kveikt er á myndavél spjaldtölvu eða síma.
4. Takið mynd af skjali, t.d. innkaupakvittun, sem á að vinna sem skjal á innleið, og veljið svo hnappur **Í lagi**.

    Ný færsla skjals á innleið er stofnað með mynd í viðhengi.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Til að hengja mynd við skjal á innleið færsla með því að taka mynd
> [!NOTE]  
>   Eftirfarandi ferli á aðeins við um [!INCLUDE[prod_short](includes/prod_short.md)] biðlara spjaldtölva og síma.

1. Á forritastikunni velja valkostahnappinn, velja **Skjöl á innleið** og velja svo **Öll**.
2. Opnið kort fyrir fyrirliggjandi færsla skjal á innleið.
3. Á síðunni **Skjal á innleið** skal velja úrfellingarmerkishnappinn og svo **Hengja við mynd úr myndavél**. Kveikt er á myndavél spjaldtölvu eða síma.
4. Takið mynd af skjali, t.d. innkaupakvittun, sem á að vinna sem skjal á innleið, og veljið svo hnappur **Í lagi**.

    Myndin er hengja við færsla skjal á innleið.

## <a name="to-create-an-incoming-document-record-manually"></a>Tila ð búa til færslu skjals á innleið handvirkt
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Aðgerðin **Stofna úr Skrá** er valin.  
3. Á síðunni **Setja inn skrá** skal velja skrá og svo **Opna**. Skráin er hengd við sjálfkrafa.
4. Einnig er hægt að velja aðgerðina **Nýtt**.
5. Ef tengja á skrá, skal velja **Tengja Skrá** aðgerð.
6. Á síðunni **Setja inn skrá** skal velja skrána sem táknar skjalið á innleið og svo hnappinn **Opna**.
7. Á síðunni **Skjal á innleið** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Sjá einnig
[Vinnsla skjala á innleið](across-process-income-documents.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]