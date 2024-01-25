---
title: Tilgreina sjálfgefinn prentara
description: Upplýsingar um mismunandi leiðir til að setja upp prentara sem á að nota sjálfgefið fyrir prentverk.
author: jswymer
ms.topic: how-to
ms.reviewer: na
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="specify-a-default-printer"></a><a name="default"></a>Tilgreina sjálfgefinn prentara

Eftir að prentarar hafa verið settir upp í Aðalsafni er hægt að tilgreina hvaða prentara á að nota að sjálfgefnu. Það eru nokkrar leiðir til að tilgreina að prentarar geti notað sjálfgefið fyrir skýrslur og önnur prentverk. Sjálfgefinn prentari er gagnlegur ef unnið er með mismunandi skýrslur sem krefjast mismunandi prentara vegna staðsetningar þeirra í fyrirtækinu eða útprentunarmöguleika.

> [!IMPORTANT]
> Einu prentararnir sem hægt er að tilgreina sem sjálfgildi eru  **Microsoft PRINT í PDF**  og Cloud prentarar sem þegar hafa verið settir upp til notkunar í viðskiptamiðinu, eins og email prentarar og Universal PRINT prentarar. Skýprentarar eru yfirleitt settir upp af admin. Nánari upplýsingar  [fást í uppsetningu prentara og í stjórnun](admin-printer-setup-overview.md).   

## <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Stilla prentara sem sjálfgefinn prentara fyrir öll prentverk

Á síðunni **Prentarastjórnun** er hægt að setja upp prentara sem sjálfgefinn prentara fyrir öll prentverk. Hægt er að tilgreina prentarann sem sjálfgefinn fyrir einn notanda eða alla notendur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.

    > [!TIP]
    > Einnig er hægt að opna síðuna **Prentarastjórnun** af síðunni **Prentaraval** með því að velja **Prentarastjórnun**.  
2. Á síðunni **Prentarastjórnun** skal velja prentara af listanum, velja **Stjórna**, því næsta velja **Stilla sem sjálfgefinn prentara fyrir mig** eða **Stilla sem sjálfgefinn prentara fyrir alla notendur**.

> [!NOTE]
> Ef sjálfgefnum prentari er stilltur í **Prentarastjórnun** verður færslu bætt við í **Prentaravalinu**.

## <a name="set-a-default-printer-for-specific-reports"></a>Stilla sjálfgefinn prentara fyrir tilteknar skýrslur

Síðan **Prentaraval** gerir kleift að tilgreina prentarann sem skýrsla notar að sjálfgefnu. Sjálfgefnir prentarar eru stilltir á grundvelli notandareiknings. Hægt er að stilla sjálfgefinn prentara fyrir eingöngu sjálfan sig, annan notanda eða alla notendur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentaraval** og velja síðan viðkomandi tengil. Einnig er hægt að velja síðuna **Prentarastjórnun**, síðan velja aðgerðina **Prentaraval**.
2. Velja skal aðgerðina **Nýtt** til að bæta við prentaravali fyrir tiltekna skýrslu.
3. Fyllið inn reitina eftir þörfum.

Tilgreind skýrsla er nú uppsett til prentunar í völdum sjálfgefnum prentara.

> [!NOTE]
> Þegar skýrslan er prentuð er hægt að velja arða með því að nota reitinn **Prenta** á skýrslubeiðnisíðunni.

> [!NOTE]
> Ef ekki er sett upp skýrsla fyrir tiltekinn prentara á síðunni **Prentaraval** verður hún prentuð á sjálfgefinn prentara fyrirtækisins, eins og það er skilgreint á síðunni **Prentarastjórnun**.

Þú eða stjórnandinn getur einnig notað síðuna **Prentaraval** til að skilgreina önnur afbrigði prentunar fyrir notendur og skýrslur. Eftirfarandi tafla lýsir samsetningu gilda til að tilgreina mismunandi prentunaruppsetningu fyrir skýrslu.

|Til                                                 |Stilla eftirfarandi gildi:                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Prenta skýrslu í tilteknum prentara fyrir alla notendur |Tilgreinið gildi í reitunum **Kenni skýrslu** og **Prentaraheiti** og skiljið reitinn **Kenni notanda** eftir auðan.|
|Prenta allar skýrslur í tilteknum prentara fyrir tiltekinn notanda|Tilgreinið gildi í reitunum **Kenni notanda** og **Prentaraheiti** og skiljið reitinn **Kenni skýrslu** eftir auðan. Þessi færsla gerir það sama og aðgerðin **Stilla sem sjálfgefinn prentara fyrir mig** á síðunni **Prentstýring**.|
|Stilla sjálfgefinn prentara fyrir allar skýrslur fyrir alla notendur|Tilgreinið gildi í reitnum **Prentaraheiti** og skiljið reitina **Kenni notanda** og **Kenni skýrslu** eftir auða. Þessi færsla gerir það sama og aðgerðin **Stilla sem sjálfgefinn prentara fyrir alla notendur** á síðunni **Prentstýring**.|
|Prenta tiltekna skýrslu á sjálfgefnum prentara notanda|Tilgreinið gildi í reitnum **Kenni skýrslu** og skiljið reitina **Prentaraheiti** og **Kenni notanda** eftir auða.|
|Prenta tiltekna skýrslu í tilteknum prentara fyrir tiltekinn notanda|Tilgreinið gildi í öllum þremur reitunum.|

> [!NOTE]
> Sértækara prentaraval hefur forgang fram yfir almennara prentaraval. Prentaraval sem hefur til dæmis gildi í reitunum **Notandakenni**, **Skýrslukenni** og **Prentaraheiti** hefur forgang fram yfir prentaraval sem er með auðar færslur í reitunum **Notandakenni** eða **Skýrslukenni**.

## <a name="choosing-the-printer-when-running-a-report"></a>Val á prentara þegar skýrsla er keyrð

Í stað þess að nota sjálfgefinn prentara þegar skýrsla er keyrð er hægt að hnekkja þessari stillingu af beiðnisíðunni. Veldu einfaldlega prentarann sem á að nota fyrir þessa skýrslugerð í fellivalmyndinni **Prentari**.

## <a name="sizing-print-jobs"></a>Stærð prentverka stillt

Skýjaprentun er hönnuð fyrir skjöl af hæfilegri stærð. Flestar skýjaþjónustur, þ.m.t. PrintNode og HP ePrint, eru með 10 MB hámark fyrir hvert verk. Ef þú þarft að prenta stærri skýrslur gætirðu þurft að skipta þeim í margar útprentanir.

## <a name="see-also"></a>Sjá einnig .

[Prentarastjórnun](admin-printer-setup-overview.md)  
[Setja upp Universal PRINT prentarar](admin-printer-setup-universal-print.md)  
[Setja upp email prentara](admin-printer-setup-email.md)  
[Prenta skýrslu](ui-work-report.md#PrintReport)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Keyra runuvinnslur](ui-how-run-batch-jobs.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
