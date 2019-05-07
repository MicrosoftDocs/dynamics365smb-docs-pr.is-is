---
title: Bóka milli-fyrirtækjaskjöl og færslubækur | Microsoft Docs
description: Notaðu milli-fyrirtækjaskjöl til að bóka viðskipti við MF-félaga.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d98cd2c8f4b88856ad55ad607370f130c6421a4d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "928817"
---
# <a name="work-with-intercompany-documents-and-journals"></a>Unnið með samstæðuskjöl og færslubækur
Milli-fyrirtækjaskjöl eru notuð til að bóka viðskipti við milli-fyrirtækjafélaga. Þegar milli-fyrirtækjaskjöl eða færslubókarlína eru bókuð í fyrirtækinu er samsvarandi fylgiskjal eða færslubókarlína stofnuð í MF-úthólfinu sem hægt er að flytja til félagans. Félaginn getur síðan bókað samsvarandi færslu í sínu fyrirtæki án þess að færa gögnin inn aftur.

Fyrir sölu- og innkaupskjöl, mun MF-félagakóði tilheyrandi viðskiptamanns eða lánardrottins tryggja að allar pantanir og reikningar sem eiga við færslur til eða frá þessum félögum stofna þaðan í frá samsvarandi skjöl hjá fyrirtækjafélögum svo að staða reikninganna verði rétt.

Fyrir MF-færslubókarlínu, þarf ekki að tilgreina reikningana fyrir stök söfn bóka, heldur þarf aðeins að gefa upp kenni samstarfsfyrirtækisins. Samsvarandi MF-færslubókarlínur eru síðan stofnaðar í félagafyrirtækinu sem veldur afstemmingu bóka beggja fyrirtækja sem taka þátt í færslunni.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>MF-sölupöntun fyllt út og send:
Hægt er að senda sölu- og innkaupapantanir og vöruskilapantanir áður en bókað er. Ekki er hægt að senda reikninga og kreditreikninga fyrr en þeir hafa verið bókaðir.

Eftirfarandi aðferð lýsir því hvernig eigi að fylla út og senda sölupöntun milli fyrirtækja. Sömu skref eiga við um sölu- og vöruskilapantanir millifyrirtækis, og bókaða millifyrirtækjareikninga og kreditreikninga.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2. Veljið **Nýtt** til að stofna nýja sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gangið úr skugga um að viðskiptamaðurinn sé milli-fyrirtækjafélagi.
5. Til að senda sölupöntunina áður en hún er bókuð er valin aðgerðin **Senda MF-sölupöntun**.

> [!NOTE]
> Ef þú framkvæmir skref 4, mun sölupöntunin verða færð yfir til úthólfs millifyrirtækisins þar sem þú getur sent hana síðar. Frekari upplýsingar er að finna í [Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Fært í milli-fyrirtækjabækur og bókað
Þegar bókuð er almenn færslubókarlína í fyrirtækinu, er samsvarandi færslubókarlína stofunuð í MF-úthólfinu sem hægt er að flytja til félagans. Félaginn getur síðan bókað samsvarandi færslu í sínu fyrirtæki án þess að færa gögnin inn aftur.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **MF-færslubók** og veldu síðan tengda tengilinn.  
2. Viðeigandi færslubókarkeyrsla er opnaður. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).
3. Fyllið inn í reitina eftir þörfum.
4. Í reitinn **MF félagi fjárhagsreikningur nr.** færið inn MF fjárhagsreikninginn sem upphæðin verður bókuð á í fyrirtæki félagans.

    > [!NOTE]
    > Þennan reit verður að fylla út í línu með bankareikningi eða fjárhagsreikningi annað hvort í reitnum **Reikningsnúmer** eða reitnum **Mótreikningsnúmer**.  
5. Valið er **Bóka** aðgerðin.

Færslurnar sem þessu tengjast eru bókaðar í þínu fyrirtæki og færslubók með samsvarandi færslum er stofnuð í úthólfi millifyrirtækisins þar sem þú getur sent þær til fyrirtæki félagans. Frekari upplýsingar er að finna í [Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur](intercompany-how-manage-intercompany-inbox.md).

## <a name="see-also"></a>Sjá einnig
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
