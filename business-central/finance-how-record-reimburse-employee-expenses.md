---
title: Skrá og endurgreiða starfsmannaútgjöld
description: Bóka útgjöld starfsmanna með færslubók á reikning starfsmanns og bóka síðan greiðslu á bankareikning hans til að endurgreiða útgjöld í viðskiptaerindum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: reimbursement
ms.search.form: '63, 234, 625, 5224, 5237, 5238, 5239, 5240'
ms.date: 03/13/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Skrá og endurgreiða starfsmannaútgjöld

[!INCLUDE[prod_short](includes/prod_short.md)] styður færslur fyrir starfsmenn á svipaðan hátt og fyrir lánardrottna. Til eru bókunarflokkar starfsmanna, sem eiga að tryggja að fjárhagsfærslur starfsmanna séu bókaðar á viðeigandi reikninga í færslubókinni.

> [!NOTE]  
> Endurgreiðslur til starfsmanna styðja ekki aflsætti og greiðsluvikmörk.

Ef starfsmenn eyða sínum eigin peningum í viðskiptaerindum, er hægt að bóka útgjöldin á reikning starfsmanns. Þá geturðu endurgreitt starfsmanninum með því að framkvæma greiðslu inn á bankareikning starfsmannsins, á svipaðan hátt og þú borgar lánardrottnum.  

Þessi grein útskýrir hvernig á að skrá kostnaðinn í bókunum og hvernig á að endurgreiða starfsmanninum. Fyrirtækið kann að vera með gátt eða forrit þar sem starfsmenn geta sent inn kostnaðarskýrslur.

[!INCLUDE [prod_short](includes/prod_short.md)] er nógu sveigjanlegt til að henta mörgum mismunandi leiðum. Nákvæm reikningsnúmer sem nota á fara eftir stillingum og ferlum fyrirtækisins.  

Nota má færslubækur fyrir reikninga starfsmanna til að skrá útgjöld starfsmanna og endurgreiðslur í erlendum gjaldmiðlum og rekja síðan upphæðirnar og bera þær saman við móttökur. Skildu reiknivélina eftir í skrifborðsskúffunni þinni - Business Central getur leiðrétt gengið fyrir þig. Þegar færslubækur eru notaðar til að bóka viðskipti fyrir starfsmannareikninga, t.d. þegar kostnaður er endurgreiddur, er hægt að nota reitinn **Gjaldmiðilskóti** til að tilgreina gjaldmiðil viðskiptanna. Ef gjaldmiðill er tilgreindur er hægt að nota sömu eiginleika og þegar færslur eru skráðar í viðskiptamanna- og lánardrottnabók. Starfsmenn geta til dæmis skráð kostnað í evrum en fengið greitt í dollurum.

Til að tryggja að gengi upphæðanna sé uppfært er hægt að leiðrétta stöðu starfsmanna þegar keyrslan gengi gjaldmiðils er keyrð. Ef nota á gengistöfluna en gera upp stöðu starfsmanna í heimagjaldmiðli er hægt að útiloka reikninga starfsmanna þegar gengi er leiðrétt.

## Skrá útgjöld starfsmanns

Útgjöld starfsmanna eru bókuð á síðunni **Færslubók**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.  
2. Viðeigandi færslubók keyrsla er opnaður. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).
3. Fyllið í reitina eftir þörfum í nýrri færslubókarlínu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Endurtakið skref 3 fyrir öll útgjöld sem starfsmaður hefur stofnað til.

    > [!TIP]  
    > Ef þú vilt færa inn fleiri kostnaðarlínur fyrir ofan eina mótreikningslínu fyrir bankareikning starfsmanns, skaltu velja gátreitinn **Leggja til afstemmingarupphæð** á línunni fyrir þína keyrslu á síðunni **færslubókakeyrslur**. Þá verður reiturinn **Upphæð** á mótreikningslínunni sjálfkrafa fylltur út með gildinu sem er nauðsynlegt til að jafna útgjöldin.
5. Veljið **Bóka** aðgerðina til að skrá útgjöldin á reikning starfsmanns.

## Endurgreiða starfsmanni

Þú endurgreiðir starfsmanni með því að bóka greiðslur á bankareikning hans á síðunni **greiðslubók**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.
2. Viðeigandi greiðslubók keyrsla er opnaður. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).
3. Fyllið inn reitina eftir þörfum. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).
4. Að öðrum kosti skal velja **Leggja til starfsmannagreiðslu** aðgerðina til að setja sjálfvirkt inn færslubókarlínu fyrir endurgreiðslu í bið til starfsmanns.
5. Valið er **bóka** aðgerð til að skrá endurgreiðsluna.  

## Afstemma endurgreiðslur við fjárhagsfærslur starfsmanns

Þú jafnar greiðslu til starfsmanns við tengdar og opnar fjárhagsfærslur starfsmanns á sama hátt og greiðslur til lánardrottins, til dæmis á síðunni **Greiðsluafstemmingarbók**, byggt á tengdum bankayfirlitsfærslum. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md). Einnig er hægt að jafna handvirkt á síðunni **Fjárhagsfærslur starfsmanna**. Frekari upplýsingar er að finna í [Afstemma greiðslu lánardrottins með greiðslubók eða úr færslum í lánardrottnabók](payables-how-apply-purchase-transactions-manually.md).  

## Sjá einnig

[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]