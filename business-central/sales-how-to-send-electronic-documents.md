---
title: Senda rafræn skjöl
description: Kynntu þér hvernig nota á Business Central til að senda rafreikninga og kreditreikninga á PEPPOL-sniði.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="send-electronic-documents" />Senda rafræn skjöl

Almenn útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] styður sendingu rafrænna reikninga og kreditreikninga á PEPPOL-sniði, sem er snið sem er stutt af stærstu skjalaskiptaþjónustuaðilunum. Þjónustuaðili í skjalaskiptaþjónustu sendir rafræn skjöl á milli viðskiptaaðila. Til að veita stuðning á öðrum rafrænu formi er notaður gagnaskiptarammi.  

 Í almennri útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] er skjalaskiptaþjónusta forstillt og tilbúinn til uppsetningar fyrir fyrirtækið. Frekari upplýsingar, sjá [Setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md). Hins vegar verður í sumum tilvikum að setja upp forrit. Frekari upplýsingar eru í [Algengar spurningar um rafrænar reikningsfærslur](faq-electronic-invoicing.yml).  

 Til að senda sölureikning sem rafrænt PEPPOL-skjal skal velja sem **Rafrænt skjal** valkostinn í á **Bóka og senda** svargluggi. Einnig er hægt setja upp sjálfgefna forstillingu skjalasendingar viðskiptamanns úr þeim svarglugga. Fyrst þarf að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, viðskiptavini, atriði, og mælieiningar. Þau eru notuð til að bera kennsl á viðskiptafélaga og vörur þegar gögnum er umbreytt í reiti í [Setja upp rafræn skjöl sending og móttaka](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice" />Til að senda rafrænan sölureikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.  

2. Nýr sölureikningur er búinn til.  

3. Þegar sölureikningurinn er tilbúinn til innheimtu skaltu velja aðgerðina **Bóka og senda**.  

     Ef sjálfgefið sendisnið viðskiptamannsins er **Rafrænt skjal**, mun það sjást í **Bóka og senda staðfestingu** svarglugganum. Þannig þarf aðeins að velja **Já** hnappinn til að bóka og senda reikninginn rafrænt á völdu sniði.  

4. Í **Bóka og senda staðfestingu** svarglugganum er hnappurinn AssistEdit til hægri við **Senda skjal til** reitinn valinn.  

5. Í **Senda skjal til** svarglugganum í á **Rafrænt skjal** reitnum er valið **Gegnum skjalaskiptaþjónustu**.  

6. Í **Snið** reitnum er valið **PEPPOL**.  

7. Velja hnappinn **Í lagi**. Svarglugginn **Bóka og senda staðfestingu** birtist. **Rafrænt skjal (PEPPOL)** er bætt við **Senda skjal til** reitinn.  

8. Velja hnappinn **Já**.  

     Sölureikningur er bókaður og sendur til viðskiptamannsins á PEPPOL-sniði.  

    > [!NOTE]  
    >  Einnig er hægt að senda bókaða sölureikninga sem rafrænt skjal. Ferlið er það sama og lýst er í þessu efnisatriði fyrir óbókuð söluskjöl. Á síðunni **Bókaður sölureikningur** skal velja aðgerðina **Aðgerðakladdi** til að skoða stöðu rafræna skjalsins.  

## <a name="see-related-microsoft-trainingtrainingmoduleselectronic-documents-dynamics--business-centralindex" />Sjá tengda [Microsoft þjálfun](/training/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also" />Sjá einnig

[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md)  
[Setja upp sendingu og móttöku rafrænna skjala](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md)  
[Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)  
[Rafræn gagnaskipti](across-data-exchange.md)  
[Algengar spurningar um rafrænar reikningsfærslur](faq-electronic-invoicing.yml)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
