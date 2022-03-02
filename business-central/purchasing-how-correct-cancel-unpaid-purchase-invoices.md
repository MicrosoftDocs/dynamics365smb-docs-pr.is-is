---
title: Breyta eða hætta við ógreidda innkaupareikninga (inniheldur myndband)
description: Útskýrir hvernig á að leiðrétta, hætta við, eða afturkalla bókaðan innkaupareikning og stofna sjálfvirkt innkaupakreditreikning.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.search.form: 138, 140, 146
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8689425ebb2bfb20791a731aa37892faa692c233
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143427"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Leiðrétta eða afturkalla ógreidda innkaupareikninga

Hægt er að leiðrétta eða afturkalla bókaðan innkaupareikning. Þetta er gagnlegt þegar leiðrétta á innsláttarmistök eða breyta kaupunum snemma í pöntunarferlinu.

Ef þegar hefur verið greitt fyrir vörur á bókuðum innkaupareikningi er ekki hægt að leiðrétta eða hætta við úr bókaða innkaupareikningnum. Þess í stað verður þú að handvirkt skapa innkaupakreditreikning til að snúa við innkaup, valfrjálst stjórnað með vöruskilapöntun innkaupa. Sama gildir ef ætlunin er að breyta bókuðum innkaupareikningi sem var byggður á sameinuðum innkaupakvittunum. Nánari upplýsingar er að finna í [Vinna úr innkaupaskilum eða afturköllunum](purchasing-how-process-purchase-returns-cancellations.md).

Á síðunni **Bókaður innkaupareikningur** er hægt að velja hnappinn **Leiðrétting** eða hnappinn **Hætta við**. Þegar bókaður innkaupareikningur er leiðréttur eða afturkallaður, er bókaður innkaupakreditreikningur jafnaður við allar fjárhags- og raunbirgðafærslur sem búnar voru til við bókun hins upphaflega innkaupareiknings. Þetta bakfærir hinn bókaða innkaupareikning í fjárhagslegum færslum og lætur hina leiðréttu bókaða innkaupakreditreikninga í endurskoðunarrakninguna. Hér á eftir er notkun **Leiðrétting** og **Hætta við** lýst.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a>Til að leiðrétta bókaðan innkaupareikning.
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir innkaupareikningar** og velja síðan viðkomandi tengil.  
2. Veljið bókaða innkaupareikninginn sem á að leiðrétta.  

    > [!NOTE]  
    >   Ef gátreiturinn **Hætta við** er valinn, er ekki hægt að leiðrétta þennan bókaða sölureikning þar sem hann hefur þegar verið leiðréttur eða afturkallaður.
3. Á síðunni **Bókaður innkaupareikningur** skal velja **Rétt**.

    Nýr sölureikningur með sömu upplýsingum er stofnaður þar sem hægt er að gera leiðréttinguna. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md). Reiturinn **Hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.

    Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.
4. Veljið **Sýna leiðréttan kreditreikning** til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Til að afturkalla bókaðan innkaupareikning.
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir innkaupareikningar** og velja síðan viðkomandi tengil.  
2. Veljið bókaða innkaupareikninginn sem á að afturkalla.

    > [!NOTE]  
    >   Ef gátreiturinn **Afturkalla** er valinn, er ekki hægt að afturkalla þennan bókaða sölureikning þar sem hann hefur þegar verið leiðréttur eða afturkallaður.
3. Á síðunni **Bókaður innkaupareikningur** skal velja **Afturkalla**.

    Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Reiturinn **Hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.
4. Veljið **Sýna leiðréttan kreditreikning** til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

### <a name="partial-invoice-posting-also-supported"></a>Takmörkuð bókun reiknings er einnig studd
Ef Afturköllunin tengist takmarkaðri bókun á reiknings er upprunaleg innkaupapöntunarlína uppfærð til að endurspegla afturkallað Reikningsfært magn. Reitirnir **Magn til reikningsf.** og **Reikn.fært magn** á tengdri innkaupapöntunarlínu er endurstilltir á gildin fyrir takmarkaða bókun.

## <a name="see-also"></a>Sjá einnig
[Innkaup](purchasing-manage-purchasing.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]