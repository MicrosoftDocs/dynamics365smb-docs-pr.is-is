---
title: Setja upp Skjöl á innleið| Microsoft Docs
description: Nota eiginleikann Skjöl á innleið til að stofna rafræn skjöl, stjórna OCR-verkum, flytja inn reikninga og umbreyta myndaskrám.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 313de95353fc42b222fa95cd36d320881a7fbdb8
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442586"
---
# <a name="set-up-incoming-documents"></a>Setja upp skjöl á innleið

Ef stofnaðar eru færslubókarlínur úr færslum skjala á innleið verður að tilgreina í á síðunni **Uppsetning fyrir skjöl á innleið** hvaða sniðmát færslubókar og runu á að nota.

Ef notendur eiga ekki að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt verður að setja upp samþykkjendur verkflæðis.

Til að breyta PDF og myndaskrám í rafræn skjöl sem er hægt að breyta í til dæmis innkaupareikninga innan [!INCLUDE[prod_short](includes/prod_short.md)], verður að fyrst að setja upp eiginleikann OCR og virkja þjónustuna. Veljið uppfærslupakka sem er viðeigandi fyrir fyrirtækið og/eða landið/svæðið. Að öðrum kosti er hægt að stofna færslur handvirkt til að tákna ytri skjölin.  

Þegar eiginleikinn Skjöl á innleið er uppsettur, er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til. Nánari upplýsingar er að finna í [Vinna skjöl á innleið](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Setja upp valkostinn fyrir skjal á innleið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning fyrir skjal á innleið** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sem hluti af uppsetningunni þarf að ákveða hvort krefjast eigi samþykkis á skjölum á innleið. Til að krefjast samþykkis þarf að setja upp samþykkjendur og samþykktarverkflæði. Ef fyrirtækið ætlar ekki að krefjast samþykkis er hægt að sleppa næsta hluta.  

Að verður að setja það upp ef þjónusta er notuð til að umbreyta PDF-skrám eða myndskrám sem tákna skjöl á innleið. Að öðrum kosti er einnig hægt að sleppa þeim hluta.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Að setja upp samþykkjendur fyrir skjöl á innleið

Það má setja upp samþykktarferli fyrir skjöl á innleið. Samþykkjendur skjala á innleið verða að vera uppsettir sem notendur sem samþykkja verkflæði.

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Á síðunni **Uppsetning fyrir samþykki notanda** er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi. Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Til að setja upp OCR-þjónustu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning OCR-þjónustu** og svo velja viðeigandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Innskráningargögnin þín eru sjálfkrafa dulrituð.

Frekari upplýsingar eru í [Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-also"></a>Sjá einnig

[Vinnsla skjala á innleið](across-process-income-documents.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]