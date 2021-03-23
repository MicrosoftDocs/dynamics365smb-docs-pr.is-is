---
title: Skrá nýja viðskiptamenn með því að stofna viðskiptamannaspjald
description: Lýsir því hvernig skal stofna viðskiptamannaspjald til að skrá upplýsingar um alla nýja viðskiptamenn eða biðlara sem selt er til.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: d873c1546cebfccc6d2549b1de2b9d111589c553
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573427"
---
# <a name="register-new-customers"></a>Skrá nýja viðskiptamenn

Viðskiptamenn eru uppruni tekna. Þú verður að skrá þig hver viðskiptavinur sem þú selur sem viðskiptavinakort. Viðskiptamannaspjald inniheldur upplýsingarnar sem þarf til að selja vörur til viðskiptamannsins. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md) og [Skrá nýja hluti](inventory-how-register-new-items.md).  

Áður en hægt er að skrá nýja viðskiptamenn þarf að setja upp ýmsar sölukóða sem hægt er að velja úr þegar fyllt eru út viðskiptamannaspjöld. Nánari upplýsingar er að finna í [Uppsetning sölu](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Bæta við nýjum viðskiptavinum

Til að skrá nýjan viðskiptavin þarf að fylla út viðskiptamannsspjald. Hægt er að búa til sniðmátum fyrir mismunandi forstillingar viðskiptavina eða hægt er að bæta við viðskiptavinum án sniðmáta.  

> [!NOTE]  
> Ef viðskiptamannasniðmát eru til fyrir mismunandi tegundir viðskipamanna, þá birtist sjálfkrafa síða þegar búið er til nýtt viðskiptamannaspjald og hægt er að velja viðeigandi sniðmát. Ef aðeins eitt viðskiptamanna sniðmát er fyrir hendi, nota ný viðskiptamannaspjöld alltaf það sniðmát.  

### <a name="to-create-a-new-customer-card"></a>Að stofna nýtt viðskiptamannaspjald

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.  
2. Á síðunni **Viðskiptamenn** skal velja aðgerðina **Nýtt**.

    Ef aðeins eitt viðskiptamannasniðmát er fyrir hendi, opnast nýtt viðskiptamannaspjald með reiti útfyllta með upplýsingum úr sniðmátinu.

    Ef fleiri en eitt viðskiptamannasniðmát er fyrir hendi, þá birtist sjálfkrafa síða með tiltækum viðskiptamannasniðmátum. Í því tilviki, fylgið næstu tveimur skrefum.
3. Á síðunni **Velja sniðmát fyrir nýjan viðskiptamann** skal velja sniðmátið sem á að nota fyrir nýja viðskiptamannaspjaldið.
4. Velja hnappinn **Í lagi**. Nýtt viðskiptamannaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í reitina.  
5. Því næst skal færa inn eða breyta reitum á viðskiptamannaspjaldinu eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Á flýtiflipanum **Söluverð** er hægt að sjá sérverð eða afslætti sem veittir eru fyrir viðskiptamanninn ef ákveðin skilyrði eru uppfyllt, svo sem vara, lágmarkspöntunarmagn eða lokadagur. Hver lína stendur fyrir sértilboðsverð eða línuafslátt. Hver dálkur táknar viðmiðun sem verða að sækja til að réttlæta sérstakt verð sem þú slærð inn í **Einingaverð** sviði, eða línuafslátt sem þú slærð inn í **Línuafsláttur %**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).

Viðskiptamaðurinn hefur nú verið skráður og viðskiptamannaspjaldið má nú nota í söluskjölum.

Ef nota á þetta viðskiptamannaspjald sem sniðmát þegar ný viðskiptamannaspjöld eru búin til, vistið það sem sniðmát. Nánari upplýsingar eru í eftirfarandi kafla.  

### <a name="to-save-the-customer-card-as-a-template"></a>Til að vista viðskiptamannaspjaldið sem sniðmát

1. Á síðunni **Viðskiptamannaspjald** skal velja aðgerðina **Vista sem sniðmát**. Síðan **Viðskiptamannasniðmát** opnast og sýnir viðskiptamannaspjaldið sem sniðmát.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir viðskiptamanninn.
4. Breyta eða færa inn víddarkóða sem munu gilda fyrir ný viðskiptamannaspjöld sem stofnuð eru með sniðmátinu.  
5. Þegar lokið hefur verið við nýja viðskiptamannasniðmátið skal velja hnappinn **Í lagi**.

Viðskiptamannasniðmátinu verður bætt við lista viðskiptamannasniðmáta þannig að hægt er að nota það til að búa til ný viðskiptamannaspjöld.

## <a name="deleting-customer-cards"></a>Eyðir viðskiptavinaspjöldum

Ef þú hefur bókað færslu fyrir viðskiptavin er ekki hægt að eyða spjaldinu þar sem hugsanlega þarf að nota fjárhagsfærslurnar í endurskoðun. Til að eyða viðskiptamannaspjöldum með fjárhagsfærslum skal hafa samband við samstarfsaðila Microsoft til að gera það með kóða.  

## <a name="managing-credit-limits"></a>Stjórna lánamörkum

Lánamörk, stöður og greiðsluskilmálar gera [!INCLUDE [prod_short](includes/prod_short.md)] kleift að gefa út viðvörun um lánamark og gjaldfallna stöðu þegar sölupöntun er slegin inn.  Ennfremur gera aðgerðir vegna greiðsluskilmála og vaxtaskilmála það kleift að innheimta vexti og/eða viðbótargjöld.  

Reiturinn **Lánamark** á viðskiptamannaspjaldinu tilgreinir hámarksupphæð sem viðskiptamaðurinn má fara umfram greiðslustöðuna áður en viðvörun er gefin út. Síðan þegar færðar eru inn upplýsingar í færslubækur, tilboð, pantanir og reikninga mun [!INCLUDE [prod_short](includes/prod_short.md)] prófa söluhausana og stakar sölulínur til að sjá hvort farið hafi verið yfir lánamarkið.

Hægt er að bóka þótt farið hafi verið yfir skuldamörk. Ef reiturinn er hafður auður eru engin mörk á hámarksskuld viðkomandi viðskiptamanns.  

Hægt er að velja um það að ekki séu birtar aðvaranir um að lánsfjárupphæð viðskiptamanns hafi náð hámarki, og hægt er að tilgreina aðgerðir aðvarana sem birtast.

### <a name="to-specify-credit-limit-warnings"></a>Viðvaranir lánamarks tilgreindar

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölugrunnur** og veldu síðan tengda tengilinn.

2. Í flýtiflipanum **Almennt**, í reitnum **Viðvaranir lánamarks**, skal velja viðeigandi valkost eins og lýst er í eftirfarandi töflu:

    |Valkostur| Description|
    |------|------------|
    |**Báðar aðvaranir**| Kerfið athugar bæði reitina **Hámarksskuld** og **Gjaldfallið** á spjaldi viðskiptamannsins og sendir aðvörun er viðskiptamaður hefur farið fram yfir hámarksskuld sína eða hefur gjaldfallna stöðu.|
    |**Hámarksskuld**|Gildið í reitnum **Lánamark** á spjaldi viðskiptavinar er borið saman við innistæðu hans, og viðvörun birtist ef innistæðan er yfir þessari upphæð.|
    |**Upphæð vanskila**|Svæðið **Gjaldfallin staða** í spjaldi viðskiptamanns er athugað og viðvörun birtist ef staða viðskiptamanns er gjaldfallin.|
    |**Engin aðvörun**|Engar viðvaranir eru sýndar um stöðu viðskiptavinar.|

## <a name="see-also"></a>Sjá einnig

[Skilgreina Greiðsluhætti](finance-payment-methods.md)  
[Sameina tvítekin atriði](sales-how-merge-duplicate-records.md)  
[Stofnun númeraraða](ui-create-number-series.md)  
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]