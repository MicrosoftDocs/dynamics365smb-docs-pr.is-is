---
title: Setja upp skjöl á innleið
description: Setja upp aðgerðina utanaðkomandi skjöl til að stofna rafræn skjöl, stjórna verkum OCR, flytja inn reikninga og umbreyta myndskrám.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/14/2022
ms.author: edupont
ms.openlocfilehash: b26e2871eb4685df8e6e276a32b15f53bc0a2c85
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079377"
---
# <a name="set-up-incoming-documents"></a>Setja upp skjöl á innleið

Ef stofnaðar eru færslubókarlínur úr færslum skjala á innleið verður að tilgreina í á síðunni **Uppsetning fyrir skjöl á innleið** hvaða sniðmát færslubókar og runu á að nota.

**Þegar aðgerðin þegar skjöl** eru sett upp er hægt að nota aðrar aðgerðir til að fara yfir kostnaðarinnhreyfingar, stjórna verkum OCR, og umbreyta skrám á innleið, handvirkt eða sjálfvirkt, til viðkomandi skjala eða færslubókarlína. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til. Frekari upplýsingar er að finna [í búa til færslur á innleið](across-how-create-income-document-records.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Setja upp valkostinn fyrir skjal á innleið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning fyrir skjal á innleið** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sem hluti af uppsetningunni þarf að ákveða hvort krefjast eigi samþykkis á skjölum á innleið. Til að þurfa samþykki þarf [að setja upp samþykkjendur og samþykktarverkflæði](#to-set-up-approvers-of-incoming-document-records). Ef fyrirtækið ætlar ekki að krefjast samþykkis er hægt að sleppa næsta kafla.

Að lokum ef notuð er OCR þjónusta til að umbreyta PDF-eða myndskrám sem tákna móttekin skjöl [verður að setja það upp](#to-set-up-an-ocr-service). Að öðrum kosti er einnig hægt að sleppa þeim hluta.

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Að setja upp samþykkjendur fyrir skjöl á innleið

Ef notendur eiga ekki að stofna reikninga eða færslubókarlínur úr skrám á innleið nema skjölin séu fyrst samþykkt skal setja upp samþykktarferli fyrir skjölin sem berast. Samþykkjendur skjala á innleið verða að vera uppsettir sem notendur sem samþykkja verkflæði.

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Á síðunni **Uppsetning fyrir samþykki notanda** er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi. Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Til að setja upp OCR-þjónustu

Til að kveikja PDF-og myndskrár inn í rafræn skjöl sem hægt er að umbreyta í reikninga, kreditreikninga eða færslubókarlínur, skal setja upp OCR-aðgerðina. Að öðrum kosti er hægt að stofna færslur handvirkt til að tákna ytri skjölin.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning OCR-þjónustu** og svo velja viðeigandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Innskráningargögnin þín eru sjálfkrafa dulrituð.

Frekari upplýsingar eru í [Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]