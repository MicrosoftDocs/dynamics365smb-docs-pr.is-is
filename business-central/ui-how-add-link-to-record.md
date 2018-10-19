---
title: "Hvernig á að tengja úr skrám í ytri upplýsingar eða forrit | Microsoft Docs"
description: "Setja tengil í skjal eða vefsíðu á tiltekna skrá, s.s. viðskiptavin eða fylgiskjal."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c2e70ad534a28cf5062e9e54a2dfbd3af6afaa39
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Bæta við tengli á vefsíður, skjöl, eða forrit á skrám.
Á tilgreindri skrá, eins og t.d. viðskiptamanni, skjali eða sölupöntun, er hægt að bæta við tengli í ytra skjal, vefsíðu eða forrit. Einnig gæti verið þörf á tengli sem opnar nýjan auðan tölvupóst á tiltekinn viðtakanda þegar hann er valinn. Spjaldasíðan fyrir sumar skrár, s.s. viðskiptamanna- eða lánardrottnaspjöld, innihalda reitinn **Heimasíða** þar sem hægt er að færa inn vefslóð (URL). Til að hafa aðra tengla með er hægt að nota aðferðina sem lýst er í þessari grein.

Annað dæmi gæti verið þegar þú tekur á móti prentuðum reikningum frá lánardrottnum. Hægt að skanna þá inn og geyma sem pdf-skrár á SharePoint-setri. Síðan hægt er að búa til tengil úr innkaupareikningi í [!INCLUDE[d365fin_md](includes/d365fin_md.md)] við viðkomandi reikning í SharePoint. Einnig er hægt að tengja af vöruspjaldi yfir á samsvarandi síðu í netvörulista lánardrottins.

## <a name="to-add-a-link-on-a-record"></a>Bæta tengli við skrá   

1.  Færslan sem á að tengja við er opnuð, t.d. viðskiptamannaspjald eða sölupöntun. Ef tengja á við sérstaka línu, t.d. færslubókarlínu, er hún valin.  

2.  Velja aðgerðin **Tenglar** til að opna gluggana **Tenglar** sem sýna alla núgildandi tengla sem hefur verið bætt við skrána.

3. Til að bæta við nýjum tengli, skal velja **+nýr**.

4.  Í reitnum **Tengill aðsetur** færið inn

    -   Til að tengja skrá á þinni tölvu eða neti, færa inn fulla slóð og skráarheiti, eins og t.d. **C:My Documentsinvoice1.doc**.
    -   Til að tengja á vefsíðu, færa inn vefslóðina (URL) eins og t.d. **www.microsoft.com**.
    -   Til að tengja á vefsíðu, færa inn vefslóðina (URL) eins og t.d. **www.microsoft.com**.
    -   Til að tengja forrit, færa inn tilgreindan streng til að opna forritið. Til dæmis, til að opna OneNote með tilgreindri síðu, færa inn **onenote:///C:My Documentstest.one**. Eða, til að opna Outlook með nýjum tómum tölvupósti til tiltekins viðtakanda skal færa inn **mailto:testalias**.  

5.  Reiturinn **Lýsing** er fylltur út með upplýsingum um tengilinn.  

6.  Veldu hnappinn **Vista**.  

## <a name="to-delete-a-link-from-a-record"></a>Til að eyða tengli úr færslu:  

Til að eyða tengli, í **Tenglar** í glugganum geturðu valið **...** og svo **Eyða**.

Ef notandi eyðir einni færslu, t.d. sölupöntunarlínu, sölupöntun eða viðskiptamanni, er öllum tenglum þeirrar færslu líka eytt. Ef færslum er hins vegar eytt með runuvinnslu, t.d. runuvinnslunni **Eyða reikningsfærðum sölupöntunum**, eru tenglarnir geymdir áfram í töflunni . Til að eyða tenglunum úr gagnagrunninum þarf að keyra kótaeininguna **Eyða færslutenglum án tilvísana**. Til að gera þetta skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða færslutenglum án tilvísana** og veldu síðan tengda tengilinn.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  In the **Data Deletion** window, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Sjá einnig  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

