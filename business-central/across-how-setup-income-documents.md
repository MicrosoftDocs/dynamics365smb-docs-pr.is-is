---
title: Setja upp Skjöl á innleið| Microsoft Docs
description: Nota eiginleikann Skjöl á innleið til að stofna rafræn skjöl, stjórna OCR-verkum, flytja inn reikninga og umbreyta myndaskrám.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0a33652ac230e63607957916308ee960d14a2b47
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188469"
---
# <a name="set-up-incoming-documents"></a>Setja upp skjöl á innleið
Ef stofnaðar eru færslubókarlínur úr færslum skjala á innleið verður að tilgreina í á síðunni **Uppsetning fyrir skjöl á innleið** hvaða sniðmát færslubókar og runu á að nota.

Ef notendur eiga ekki að geta stofnað reikninga eða færslubókarlínur úr færslum skjala á innleið nema skjöl séu fyrst samþykkt verður að setja upp samþykkjendur verkflæðis.

Til að breyta PDF og myndaskrám í rafræn skjöl sem er hægt að breyta í til dæmis innkaupareikninga innan [!INCLUDE[d365fin](includes/d365fin_md.md)], verður að fyrst að setja upp eiginleikann OCR og virkja þjónustuna.

Þegar eiginleikinn Skjöl á innleið er uppsettur, er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til. Nánari upplýsingar er að finna í [Vinna skjöl á innleið](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Setja upp valkostinn fyrir skjal á innleið
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning skjala á innleið** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Að setja upp samþykkjendur fyrir skjöl á innleið
Samþykkjendur skjala á innleið verða að vera uppsettir sem notendur sem samþykkja verkflæði.

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Á síðunni **Uppsetning fyrir samþykki notanda** er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi. Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Til að setja upp OCR-þjónustu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning OCR-þjónustu** og veldu síðan tengda tengilinn.
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Innskráningargögnin þín eru sjálfkrafa dulrituð.

## <a name="see-also"></a>Sjá einnig
[Vinnsla skjala á innleið](across-process-income-documents.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
