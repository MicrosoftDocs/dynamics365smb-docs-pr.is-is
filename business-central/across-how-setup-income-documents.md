---
title: Setja upp skjöl á innleið
description: 'Setja upp eiginleikann Skjöl á innleið til að stofna rafræn skjöl, stjórna OCR-verkum, flytja inn reikninga og umbreyta myndaskrám.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="set-up-incoming-documents" />Setja upp skjöl á innleið

Ef stofnaðar eru færslubókarlínur úr færslum skjala á innleið verður að tilgreina í á síðunni **Uppsetning fyrir skjöl á innleið** hvaða sniðmát færslubókar og runu á að nota.

Þegar eiginleikinn **Skjöl á innleið** er uppsettur, er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til. Frekari upplýsingar eru í [Stofna færslur skjala á innleið](across-how-create-income-document-records.md).

## <a name="to-set-up-the-incoming-documents-feature" />Setja upp valkostinn fyrir skjal á innleið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning fyrir skjal á innleið** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sem hluti af uppsetningunni þarf að ákveða hvort krefjast eigi samþykkis á skjölum á innleið. Til að krefjast samþykkis þarf að [setja upp samþykkjendur og samþykktarverkflæði](#to-set-up-approvers-of-incoming-document-records). Ef fyrirtækið ætlar ekki að krefjast samþykkis er hægt að sleppa næsta hluta.

Að lokum, ef þú notar OCR-þjónustu til að umbreyta PDF eða myndaskrám sem standa fyrir skjöl á innleið [þarf að setja hana upp](#to-set-up-an-ocr-service). Að öðrum kosti er einnig hægt að sleppa þeim hluta.

## <a name="to-set-up-approvers-of-incoming-document-records" />Að setja upp samþykkjendur fyrir skjöl á innleið

Ef þú vilt ekki að notendur búi til reikninga eða almennar færslubókarlínur úr færslum skjala á innleið nema skjölin séu fyrst samþykkt skaltu setja upp samþykktarferli fyrir skjöl á innleið. Samþykkjendur skjala á innleið verða að vera uppsettir sem notendur sem samþykkja verkflæði.

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Á síðunni **Uppsetning fyrir samþykki notanda** er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi. Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service" />Til að setja upp OCR-þjónustu

Til að breyta PDF- og myndaskrám í rafræn skjöl sem þú getur umbreytt í reikninga, kreditreikninga eða færslubókarlínur skal setja upp OCR-eiginleikann. Að öðrum kosti er hægt að stofna færslur handvirkt til að tákna ytri skjölin.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning OCR-þjónustu** og svo velja viðeigandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Innskráningargögnin þín eru sjálfkrafa dulrituð.

Frekari upplýsingar eru í [Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics--business-central" />Sjá tengda [Microsoft þjálfun](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
