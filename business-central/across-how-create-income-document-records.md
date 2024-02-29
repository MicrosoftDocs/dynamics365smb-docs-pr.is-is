---
title: Stofna færslur skjala á innleið
description: 'Notaðu aðrar aðgerðir á síðu skjala á innleið til að fara yfir kvittanir vegna kostnaðar, hafa umsjón með OCR-verkum, umbreyta skrám skjala á innleið og hengja ytri skrár við.'
author: jswymer
ms.topic: how-to
ms-service: dynamics-365-business-central
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 03/2/2023
ms.author: jswymer
ms.custom: bap-template
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
---
# <a name="create-incoming-document-records"></a>Stofna skjalaskrár á innleið

Á síðunni **Skjöl á innleið** er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur í. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.

Til að skrá ytra skjal í [!INCLUDE[prod_short](includes/prod_short.md)] þarf fyrst að stofna eða ljúka við færslu skjals á innleið. Þú getur gert þessi verk handvirkt eða þú getur tekið mynd af ytra skjalinu til að búa til færslu fyrir skjal á innleið með myndaskrá í viðhengi.

Áður en hægt er að nota valkostinn **Skjöl á innleið** þarf að framkvæma áskilda uppsetningu. Frekari upplýsingar eru í [Setja upp skjöl á innleið](across-how-setup-income-documents.md).

## <a name="approve-or-reject-an-incoming-document"></a>Samþykkja eða hafna skjali á innleið

Ef þú hefur sett upp eiginleikann **Skjöl á innleið** til að krefjast samþykkis fyrir því að búa til skjöl, verða notendur með viðeigandi réttindi að samþykkja færslurnar áður en þær eru afgreiddar. Frekari upplýsingar er að finna í [Setja upp samþykkjendur fyrir skjöl á innleið](across-how-setup-income-documents.md#to-set-up-approvers-of-incoming-document-records).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Valin er línan með skjalinu sem á að samþykkja eða hafna og síðan valið á **Samþykkja** eða **Hafna** aðgerðir.

Ef færsla skjals á innleið er samþykkt er gátreiturinn **Losað** á línu skjal á innleið valinn. Notandi sem stjórnar t.d. stofnun innkaupareikninga getur haldið áfram að vinna úr færslunni.

## <a name="create-an-incoming-document-record-by-taking-a-photo"></a>Stofna skjalfærslu á innleið með því að taka mynd

> [!NOTE]  
> Eftirfarandi ferli á aðeins við um [!INCLUDE[prod_short](includes/prod_short.md)] biðlara spjaldtölva og síma.

1. Í hlutverkamiðstöðinni skaltu velja reitinn **Búa til skjal á innleið frá myndavél** og síðan fara í skref 4.
2. Annars skal velja táknið ![Ljósapera sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
3. Á síðunni **Skjöl á innleið** skal **Nýtt** og síðan velja **Stofna úr myndavél**. Kveikt er á myndavél spjaldtölvu eða síma.
4. Taktu mynd af skjali, t.d. innkaupakvittun, sem á að afgreiða sem skjal á innleið og veldu svo hnappinn **Nota**.

    Ný færsla skjals á innleið er stofnað með mynd í viðhengi.

## <a name="attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Tengja mynd við færslu sem þegar er til skjals með því að taka mynd

> [!NOTE]  
> Eftirfarandi ferli á aðeins við um [!INCLUDE[prod_short](includes/prod_short.md)] biðlara spjaldtölva og síma.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Opnið kort fyrir fyrirliggjandi færsla skjal á innleið.
3. Á síðu skjalafærslu skal velja **Afgreiða** og síðan velja **Hengja við mynd úr myndavél**. Kveikt er á myndavél spjaldtölvu eða síma.
4. Taktu mynd af skjali, t.d. innkaupakvittun, sem á að afgreiða sem skjal á innleið og veldu svo hnappinn **Nota**.

    Myndin er hengja við færsla skjal á innleið.

## <a name="create-an-incoming-document-record-manually"></a>Stofna skjalafærslu handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Veldu **Nýtt** og síðan aðgerðina **Stofna úr skrá**.  
3.  **Á síðunni INSERT-skrá**  skal gera eina eftirfarandi skref hengdu skrá sem táknar skjalið sem er á innleið:

   [!INCLUDE[file-upload](includes/file-upload.md)]

4. Einnig er hægt að  **Velja nýju**  aðgerðina og gera eftirfarandi skref:

    1. Til að tengja skrá er hægt að velja  **vinnsluviðhengdu** > **skrá**.
    2.  **Á síðunni INSERT-skrá**  er valin sú skrá sem stendur fyrir skjalið sem um ræðir eða valið  **er smella hér til að fletta**  til að finna og opna skrána.
    3. Á síðunni **Skjal á innleið** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Sjá einnig .

[Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md)
[Stofna færslur yfir skjöl á innleið, beint úr skjölum og færslum](across-how-connect-disconnect-income-document-records.md)
[Finna bókuð fylgiskjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md)
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
