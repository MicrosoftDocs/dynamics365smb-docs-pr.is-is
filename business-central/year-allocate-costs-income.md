---
title: Yfirlit yfir verk sem á að úthluta kostnaði og tekjum
description: Lýsir verkhlutunum til að úthluta færslu ítrekunarfærslubókar á nokkra mismunandi reikninga þegar færslubókin er bókuð.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.form: '283, 5629'
ms.date: 02/05/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="allocate-recurring-costs-and-income"></a>Úthluta ítrekuðum kostnaði og tekjum

Hægt er að úthluta færslu ítrekunarfærslubókar á nokkra reikninga þegar færslubókin er bókuð. Hægt er að fá nánari upplýsingar um ítrekunarfærslubækur með því að fara í [Vinna með ítrekunarbækur](ui-work-general-journals.md#work-with-recurring-journals). 

Framkvæma má úthlutunina miðað við þrjú atriði:

* Magn
* Prósentuhlutfall (%)
* Upphæð

Úthlutunaraðgerðirnar vinna með ítrekunarfærslubækur og eignabækur.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Eftirfarandi ferli lýsa því hvernig skal búa sig undir það að úthluta kostnaði í ítrekunarfærslubók með því að skilgreina úthlutunarlykla. Þegar úthlutunarlyklar eru skilgreindir, er færslubókin kláruð og bókuð eins og hver önnur ítrekunarfærslubók. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>setja upp úthlutunarlykla

Hægt er að úthluta færslu úr ítrekunarfærslubók til nokkurra reikninga þegar færslubókin er bókuð. Úthlutunin getur verið í magni, prósentu eða upphæð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurtekin færslubók** og velja síðan viðkomandi tengil.
2. Veldu reitinn **Runuheiti** til að opna síðuna **Færslubókarkeyrslur**.
3. Þú getur annað hvort breytt úthlutunum á fyrirliggjandi runu í listanum eða stofnað nýja runu með úthlutunum.
   * Til að stofna nýja runu, velja **Nýtt** aðgerð og farið á næsta skref.
   * Til að breyta úthlutunum fyrir núverandi færslubók, veldu færslubók og farðu í skref 7.    
4. Í reitnum **Heiti** er fært inn heiti fyrir keyrsluna, eins og Þrif. Í reitnum **Lýsing** skal færa inn lýsingu, eins og Hreinsa kostnaðarbók.
5. Að því loknu er síðunni lokað. Ný, auð ítrekunarbók opnast.
6. Reitirnir í línunni eru fylltir út.
7. Valið er **úthluta** aðgerð.
8. Lína er bætt við fyrir hverja úthlutun. Annaðhvort þarf að fylla út reitinn **Úthlutun %**, **Úthlutunarmagn** eða **Upphæð**. Einnig þarf að fylla út reitinn **Reikningsnr.** og í reitina í altækum víddum ef færslan á að fara í altækar víddir.
9. Þegar prósenta er færð í línu reiknast upphæðin í reitnum **Upphæð** sjálfkrafa. Þessar upphæðir verða að hafa andstætt merki við það sem heildarupphæðin í reitnum **Upphæð** er með í ítrekunarbókinni.
10. Eftir að hafa fært inn úthlutunarlínurnar skal velja **Í lagi** til að fara aftur á síðuna **endurteknar færslubækur**. Svæðið **Úthlutuð upphæð (USD)** er fyllt út og er eins og svæðið **Upphæð**.
11. Bóka skal færslubókina.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Til að breyta uppsettum úthlutunarlykli

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurtekin færslubók** og velja síðan viðkomandi tengil.
2. Á síðunni **Ítrekunarfærslubók** er færslubók með úthlutun valin.
3. Veljið línuna með úthlutuninni og veljið svo aðgerðina **Úthlutanir** .
4. Breyta skal viðeigandi reitum og velja **síðan Í lagi**.

## <a name="see-also"></a>Sjá einnig .

[Lokaár og Tímabil](year-close-years-periods.md)  
[Vinna í færslubókum](ui-work-general-journals.md)    
[Að bóka skjöl og færslubækur](ui-post-documents-journals.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
