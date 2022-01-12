---
title: Skrá nýja viðskiptamenn með því að búa til viðskiptamannaspjald (inniheldur myndskeið)
description: Lýsir því hvernig skal stofna viðskiptamannaspjald til að skrá upplýsingar um alla nýja viðskiptamenn eða biðlara sem selt er til.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.search.form: 7, 21, 22, 33, 42, 43, 367, 368, 369, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305
ms.date: 09/24/2021
ms.author: edupont
ms.openlocfilehash: 87fb7f0612a623a6f4bcd901beed1c7227b46c23
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2021
ms.locfileid: "7939964"
---
# <a name="register-new-customers"></a>Skrá nýja viðskiptamenn

Viðskiptamenn eru uppruni tekna. Þú verður að skrá þig hver viðskiptavinur sem þú selur sem viðskiptavinakort. Viðskiptamannaspjald inniheldur upplýsingarnar sem þarf til að selja vörur til viðskiptamannsins. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md) og [Skrá nýja hluti](inventory-how-register-new-items.md).  

Áður en hægt er að skrá nýja viðskiptamenn þarf að setja upp ýmsar sölukóða sem hægt er að velja úr þegar fyllt eru út viðskiptamannaspjöld. Nánari upplýsingar er að finna í [Uppsetning sölu](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Bæta við nýjum viðskiptavinum
Hægt er að bæta við nýjum viðskiptamanni handvirkt með því að fylla út reitina á síðunni **Viðskiptamannaspjald** eða hægt er að nota sniðmát sem innihalda fyrirframskilgreindar upplýsingar. Til dæmis er hægt að búa til sniðmát fyrir mismunandi forstillingargerðir viðskiptamanna. Með því að nota sniðmát sparast tími þegar nýjum viðskiptamönnum er bætt við og það hjálpar til við að tryggja að upplýsingarnar séu réttar hverju sinni. Ef þú stofnar sniðmát fyrir fleiri en eina gerð af viðskiptamanni geturðu valið sniðmátið sem á að nota þegar þú bætir við viðskiptamanni. Ef þú býrð aðeins til eitt sniðmát verður það notað fyrir alla nýja viðskiptamenn. Þegar sniðmát er stofnað geturðu notað aðgerðina **Nota sniðmát** til að nota það í einum eða fleiri viðskiptamönnum. Til að búa til sniðmát fyllir þú inn upplýsingarnar sem þú vilt endurnota á síðu viðskiptamannaspjaldsins og vistar það síðan sem sniðmát. Frekari upplýsingar er að finna í [Að vista viðskiptamannaspjald sem sniðmát](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template)

> [!TIP]
> Það getur reynst gagnlegt að sérsníða síðuna **Sniðmát viðskiptamanns** þegar þú stofnar sniðmát. Þú gætir til dæmis viljað bæta reitnum **Lánamark** við sniðmátið. Frekari upplýsingar eru í [Sérstilling verksvæðis](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Þú getur einnig stofnað viðskiptamann út frá tengilið. Frekari upplýsingar eru í [Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card"></a>Að stofna nýtt viðskiptamannaspjald

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Með aðgerðinni **Verð og afsláttur** er hægt að hafa umsjón með sérverði eða afslætti fyrir viðskiptamann þegar pöntun uppfyllir ákveðin skilyrði. Til dæmis gætu viðmiðin verið þegar viðkomandi kaupir ákveðna vöru, pantar lágmarksmagn eða kaupir fyrir dagsetningu, til dæmis þegar herferð lýkur. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).

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

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.

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
