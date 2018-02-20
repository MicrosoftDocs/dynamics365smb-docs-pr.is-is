---
title: "Senda rafræn skjöl | Microsoft Docs"
description: "lærðu hvernig á að senda reikninga rafrænt"
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fae5e37b8f1fcca84a474b2eac2039f7fc6d8245
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="send-electronic-documents"></a>Senda rafræn skjöl
Almenn útgáfa [!INCLUDE[d365fin](includes/d365fin_md.md)] styður sendingu rafrænna reikninga og kreditreikninga á PEPPOL-sniði, sem er stutt af stærstu skjalaskiptaþjónustuaðilunum. Þjónustuaðili í skjalaskiptaþjónustu sendir rafræn skjöl á milli viðskiptaaðila. Til að veita stuðning á öðrum rafrænu formi er notaður gagnaskiptarammi.  

 Í almennri útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)] er skjalaskiptaþjónusta forstillt og tilbúinn til uppsetningar fyrir fyrirtækið. Frekari upplýsingar, sjá [Setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md).  

 Til að senda sölureikningi sem rafrænt PEPPOL-skjal er valinn valkosturinn **Rafrænt skjal** í **Bóka og senda** svarglugganum þar sem einnig er hægt að setja það upp sem sjálfgefið sendisnið skjals viðskiptamannsins. Fyrst þarf að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, viðskiptavini, atriði, og mælieiningar. Þau eru notuð til að bera kennsl á viðskiptafélaga og vörur þegar gögnum er umbreytt í reiti í [Setja upp rafræn skjöl sending og móttaka](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Til að senda rafrænan sölureikning  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.  

2.  Nýr sölureikningur er búinn til.  

3.  Þegar hægt er að reikningsfæra sölureikninginn, á **Aðgerðir** flipanum í flokknum **Bókun** er valið **Bóka og senda**.  

     Ef sjálfgefið sendisnið viðskiptamannsins er **Rafrænt skjal**, mun það sjást í **Bóka og senda staðfestingu** svarglugganum og aðeins þarf að velja **Já** hnappinn til að bóka og senda reikninginn rafrænt á völdu sniði.  

4.  Í **Bóka og senda staðfestingu** svarglugganum er hnappurinn AssistEdit til hægri við **Senda skjal til** reitinn valinn.  

5.  Í **Senda skjal til** svarglugganum í á **Rafrænt skjal** reitnum er valið **Gegnum skjalaskiptaþjónustu**.  

6.  Í **Snið** reitnum er valið **PEPPOL**.  

7.  Velja hnappinn **Í lagi**. Svarglugginn **Bóka og senda staðfestingu** birtist. **Rafrænt skjal (PEPPOL)** er bætt við **Senda skjal til** reitinn.  

8.  Velja hnappinn **Já**.  

     Sölureikningur er bókaður og sendur til viðskiptamannsins sem rafrænt skjal á PEPPOL-sniði.  

    > [!NOTE]  
    >  Einnig er hægt að senda bókaða sölureikninga sem rafrænt skjal. Ferlið er það sama og lýst er í þessu efnisatriði fyrir óbókuð söluskjöl. Í glugganum **Bókaðir sölureikningar**, á flipanum **Aðgerðir**, í flokknum **Almennt**, veljið **Aðgerðakladdi** til að skoða stöðu rafræna skjalsins. Frekari upplýsingar, sjá **Aðgerðakladdi**.  

## <a name="see-also"></a>Sjá einnig  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md)  
[Setja upp sendingu og móttöku rafrænna skjala](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md)  
[Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)  
[Rafræn gagnaskipti](across-data-exchange.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

