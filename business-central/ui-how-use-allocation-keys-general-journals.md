---
title: Nota úthlutunarlykla í færslubókum | Microsoft Docs
description: Lærðu hvernig þú getur notað úthlutunarlykla í færslubókum.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: af18a94f5cf6b24b0da24821499e3866487207be
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918539"
---
# <a name="use-allocation-keys-in-general-journals"></a>Nota úthlutunarlykla í færslubókum
Hægt er að úthluta færslu úr færslubók til nokkurra reikninga þegar færslubókin er bókuð. Úthlutunin getur verið í magni, prósentu eða upphæð.

## <a name="to-set-up-allocation-keys"></a>setja upp úthlutunarlykla
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Ítrekunarfærslubók** og veldu síðan tengda tengilinn.
2. Veldu reitinn **Runuheiti** til að opna síðuna **Færslubókarkeyrslur** .
3. Þú getur annað hvort breytt úthlutunum á fyrirliggjandi runu í listanum eða stofnað nýja runu með úthlutunum.
   * Til að stofna nýja runu, velja **Nýtt** aðgerð og farið á næsta skref.
   * Til að breyta úthlutunum fyrir núverandi færslubók, veldu færslubók og farðu í skref 7.    
4. Í reitnum **Heiti** er fært inn heiti fyrir keyrsluna, eins og Þrif. Í reitnum **Lýsing** skal færa inn lýsingu, eins og Hreinsa kostnaðarbók.
5. Að því loknu er síðunni lokað. Ný, auð ítrekunarbók opnast.
6. Reitirnir í línunni eru fylltir út.
7. Valið er **úthluta** aðgerð.
8. Lína er bætt við fyrir hverja úthlutun. Annaðhvort þarf að fylla út reitinn **Úthlutun %** , **Úthlutunarmagn** eða **Upphæð** . Einnig þarf að fylla út reitinn **Reikningsnr.** og í reitina í altækum víddum ef færslan á að fara í altækar víddir.
9. Þegar prósenta er færð í línu reiknast upphæðin í reitnum **Upphæð** sjálfkrafa. Þessar upphæðir verða að hafa andstætt merki við það sem heildarupphæðin í reitnum **Upphæð** er með í ítrekunarbókinni.
10. Eftir að hafa fært inn úthlutunarlínurnar skal velja **Í lagi** til að fara aftur á síðuna **endurteknar færslubækur** . Svæðið **Úthlutuð upphæð (USD)** er fyllt út og er eins og svæðið **Upphæð** .
11. Bóka skal færslubókina.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Til að breyta uppsettum úthlutunarlykli
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Ítrekunarfærslubók** og veldu síðan tengda tengilinn.
2. Á síðunni **Ítrekunarfærslubók** er færslubók með úthlutun valin.
3. Velja línu með úthlutuninni og velja síðan **úthlutanir** .
4. Breyta viðeigandi reitum, og velja svo hnappinn **Í lagi** .

## <a name="see-also"></a>Sjá einnig
[Vinna í færslubókum](ui-work-general-journals.md)  
[Bókun skjala og færslubóka](ui-post-documents-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
