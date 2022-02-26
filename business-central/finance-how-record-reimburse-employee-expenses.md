---
title: Skrá og endurgreiða starfsmannaútgjöld
description: Bóka útgjöld starfsmanna með færslubók á reikning starfsmanns og bóka síðan greiðslu á bankareikning hans til að endurgreiða útgjöld í viðskiptaerindum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.search.form: 63, 234, 625, 5224, 5237, 5238, 5239, 5240
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 02299f484f510b8d78ecdfda4447046a650af21c
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972958"
---
# <a name="record-and-reimburse-employees-expenses"></a>Skrá og endurgreiða starfsmannaútgjöld

[!INCLUDE[prod_short](includes/prod_short.md)] styður færslur fyrir starfsmenn á svipaðan hátt og fyrir lánardrottna. Til eru bókunarflokkar starfsmanna, sem eiga að tryggja að fjárhagsfærslur starfsmanna séu bókaðar á viðeigandi reikninga í færslubókinni.

> [!NOTE]  
> Starfsmannafærslur er eingöngu hægt að bóka í staðbundna gjaldmiðlinum. Endurgreiðslur til starfsmanna styðja ekki aflsætti og greiðsluvikmörk.

Ef starfsmenn eyða sínum eigin peningum í viðskiptaerindum, er hægt að bóka útgjöldin á reikning starfsmanns. Þá geturðu endurgreitt starfsmanninum með því að framkvæma greiðslu inn á bankareikning starfsmannsins, á svipaðan hátt og þú borgar lánardrottnum.  

> [!TIP]
> Þessi grein útskýrir hvernig á að skrá kostnaðinn í bókunum og hvernig á að endurgreiða starfsmanninum. Fyrirtækið kann að vera með gátt eða forrit þar sem starfsmenn geta sent inn kostnaðarskýrslur.

[!INCLUDE [prod_short](includes/prod_short.md)] er nógu sveigjanlegt til að henta mörgum mismunandi leiðum. Nákvæm reikningsnúmer sem nota á fara eftir stillingum og ferlum fyrirtækisins.  

## <a name="to-record-an-employees-expense"></a>Skrá útgjöld starfsmanns

Útgjöld starfsmanna eru bókuð á síðunni **Færslubók**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.  
2. Viðeigandi færslubók keyrsla er opnaður. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).
3. Fyllið í reitina eftir þörfum í nýrri færslubókarlínu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Endurtakið skref 3 fyrir öll útgjöld sem starfsmaður hefur stofnað til.

    > [!TIP]  
    > Ef þú vilt færa inn fleiri kostnaðarlínur fyrir ofan eina mótreikningslínu fyrir bankareikning starfsmanns, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu á síðunni **færslubókakeyrslur**. Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna útgjöldin.
5. Veljið **Bóka** aðgerðina til að skrá útgjöldin á reikning starfsmanns.

## <a name="to-reimburse-an-employee"></a>Endurgreiða starfsmanni

Þú endurgreiðir starfsmanni með því að bóka greiðslur á bankareikning hans á síðunni **greiðslubók**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.
2. Viðeigandi greiðslubók keyrsla er opnaður. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).
3. Fyllið inn í reitina eftir þörfum. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).
4. Að öðrum kosti skal velja **Leggja til starfsmannagreiðslu** aðgerðina til að setja sjálfvirkt inn færslubókarlínu fyrir endurgreiðslu í bið til starfsmanns.
5. Valið er **bóka** aðgerð til að skrá endurgreiðsluna.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Afstemma endurgreiðslur við fjárhagsfærslur starfsmanns

Þú jafnar greiðslu til starfsmanns við tengdar og opnar fjárhagsfærslur starfsmanns á sama hátt og greiðslur til lánardrottins, til dæmis á síðunni **Greiðsluafstemmingarbók**, byggt á tengdum bankayfirlitsfærslum. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md). Einnig er hægt að jafna handvirkt á síðunni **Fjárhagsfærslur starfsmanna**. Frekari upplýsingar er að finna í [Afstemma greiðslu lánardrottins með greiðslubók eða úr færslum í lánardrottnabók](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Sjá einnig

[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]