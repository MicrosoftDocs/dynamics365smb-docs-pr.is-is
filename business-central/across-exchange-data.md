---
title: Gagnaskipti
description: 'Skiptast á rafrænum viðskiptaskjölum, til dæmis bankaskrám, á milli Business Central og utanaðkomandi aðila.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'exchange data, external files, electronic documents, AMC Banking, OCT, SEPA'
ms.date: 06/10/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Gagnaskipti
Hægt er að skipta á gögnum á milli [!INCLUDE[prod_short](includes/prod_short.md)] og ytri skráa í tengslum við algeng viðskiptaverk, s.s. að senda og taka á móti rafrænum skjölum og flytja inn og út bankaskrár.  

Áður en hægt er að senda og taka á móti rafrænum skjölum eða flytja inn og út bankaskrár verður að setja upp gagnaskiptaramma til að vinna úr gagnaskjölum eða straumum. Auk þess verður að setja upp tengd svæði, t.d. viðskiptamenn sem fá senda rafræna reikninga eða AMC Banking 365 Fundamentals viðbótina ef þú sendir umskráningu bankaskráa til utanaðkomandi þjónustuaðila. Nánari upplýsingar er að finna í [Uppsetning gagnaskipta](across-set-up-data-exchange.md).  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Umbreyta söluskjalafærslum í [!INCLUDE[prod_short](includes/prod_short.md)] í staðlað snið og senda þær sem rafræn skjöl sem viðskiptamenn geta fengið inn í kerfið sitt.|[Senda rafræn skjöl](sales-how-to-send-electronic-documents.md)|  
|Nota OCR-þjónustu til að breyta PDF eða myndaskrám í rafræn skjöl sem hægt er að breyta í færslur fyrir skjöl í [!INCLUDE[prod_short](includes/prod_short.md)].|[Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md)|  
|Taka á móti rafrænum skjölum, annaðhvort úr OCR-þjónusta eða skjalaskiptaþjónusta, í stöðluðu sniði sem umbreytt er í viðeigandi innkaupaskjalsfærslu í [!INCLUDE[prod_short](includes/prod_short.md)].|[Taka við og umbreyta rafræn skjölum](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Flytjið bankayfirlitsskrá inn á síðuna **greiðsluafstemmingarbók** sem fyrsta skrefið í afstemmingu greiðsla eða inn á síðuna **Afstemming bankareiknings** sem fyrsta skrefið í að afstemma bankareikninga.|[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)|  
|Flytja greiðslur úr **greiðslubók** síðunni í bankaskrá sem er hlaðið upp á rafrænan bankareikning til vinnslu.|[Flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Gerðu rafrænar greiðslur í samræmi við SEPA-kreditfærslustaðla ESB.|[Greiða með AMC Banking 365 Fundamentals viðbótinni eða SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Gefið bankanum fyrirmæli um að flytja greiðsluupphæðir af bankareikningum viðskiptavina á bankareikninga fyrirtækisins í samræmi við uppsetningu SEPA-beingreiðslna.|[Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Nota gengi þjónustuveitu gjaldeyrisviðskipta til að uppfæra síðuna **Gengi**.|[Uppfæra gengi](finance-how-update-currencies.md)|  
|Skoðið hvaða skráareiginleikar eru varpaðir á reiti í [!INCLUDE[prod_short](includes/prod_short.md)] við innflutning SEPA CAMT yfirlitsskráa.|[Reitarvörpum við innflutning SEPA CAMT skráa](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Útflutningsgögn fyrir Intrastat-skýrslugerð í [!INCLUDE[prod_short](includes/prod_short.md)].|[Setja upp Intrastat skýrslugerð](finance-how-setup-report-intrastat.md)|
|Skoðaðu hvaða reitum í [!INCLUDE[prod_short](includes/prod_short.md)] hefur verið varpað á skráareiginleika við útflutning greiðsluskráa með AMC Banking 365 Fundamentals viðbótinni.|[Reitarvörpun við útflutning greiðsluskrá með AMC Banking 365 Fundamentals viðbótinni](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## Sjá einnig  
[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Rafræn gagnaskipti](across-data-exchange.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)   
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Skjöl á innleið](across-income-documents.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
