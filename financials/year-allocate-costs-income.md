---
title: "Yfirlit yfir verkhluta úthlutunar á kostnaði og tekjum | Microsoft Docs"
description: "Útskýrir verkhluta sem felur í sér að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/07/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1620e69ce8018256780dcba108c31312c02166cb
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-allocate-costs-and-income"></a>Hvernig á að: úthluta kostnaði og tekjum
Hægt er að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð. Framkvæma má úthlutunina miðað við þrjú atriði:

* Magn
* Prósentuhlutfall (%)
* Upphæð

Nota má úthlutunareiginleika með ítrekunarfærslubókum og eignabókum.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Eftirfarandi ferli lýsa því hvernig skal búa sig undir það að úthluta kostnaði í ítrekunarfærslubók með því að skilgreina úthlutunarlykla. Þegar úthlutunarlyklar eru skilgreindir, er færslubókin kláruð og bókuð eins og hver önnur ítrekunarfærslubók. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>setja upp úthlutunarlykla
Hægt er að úthluta færslu úr ítrekunarfærslubók til nokkurra reikninga þegar færslubókin er bókuð. Úthlutunin getur verið í magni, prósentu eða upphæð.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Ítrekunarfærslubók** og velja svo viðeigandi tengil.
2. Veldu **runuheiti** reitinn til að opna **færslubókarkeyrslu** gluggann.
3. Þú getur annað hvort breytt úthlutunum á fyrirliggjandi runu í listanum eða stofna nýja runu með úthlutunum.
   * Til að stofna nýja runu, velja **Nýtt** aðgerð og farið á næsta skref.
   * Til að breyta úthlutunum fyrir núverandi færslubók, veldu færslubók og farðu í skref 7.    
4. Í reitnum **Heiti** er fært inn heiti fyrir keyrsluna, eins og Þrif. Í reitnum **Lýsing** færið inn lýsingu, eins og Hreinsa kostnaðarbók.
5. Lokið glugganum þegar þessu er lokið. Ný, auð ítrekunarbók opnast.
6. Reitirnir í línunni eru fylltir út.
7. Valið er **úthluta** aðgerð.
8. Lína er bætt við fyrir hverja úthlutun. Annaðhvort þarf að fylla út reitinn **Úthlutun %**, **Úthlutunarmagn** eða **Upphæð**. Þú verður einnig að fylla inn í **reikningsnúmer**,  reitinn, og í reitina í altækum víddum ef færslan á að fara í altækar víddir.
9. Þegar prósenta er færð í línu reiknast upphæðin í reitnum **Upphæð** sjálfkrafa. Þessar upphæðir verða að hafa andstætt merki við það sem heildarupphæðin í reitnum **Upphæð** er með í ítrekunarbókinni.
10. Eftir að hafa fært inn úthlutunarlínurnar skal velja **Í lagi** til að fara aftur í gluggann **endurteknar færslubækur**. Svæðið **Úthlutuð upphæð (USD)** er fyllt út og er eins og svæðið **Upphæð**.
11. Bóka skal færslubókina.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Breyta uppsettum úthlutunarlykli.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Ítrekunarfærslubók** og velja svo viðeigandi tengil.
2. Í glugganum**Ítrekunarfærslubók** er færslubók með úthlutun valin.
3. Velja línu með úthlutuninni og velja síðan **úthlutanir**.
4. Breyta viðeigandi reitum, og velja svo hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Lokaár og Tímabil](year-close-years-periods.md)  
[Vinna í færslubókum](ui-work-general-journals.md)    
[Að bóka skjöl og færslubækur](ui-post-documents-journals.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

