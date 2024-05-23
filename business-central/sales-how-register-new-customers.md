---
title: Skrá nýja viðskiptamenn með því að búa til viðskiptamannaspjald (myndband)
description: Lýsir því hvernig skal stofna viðskiptamannaspjald til að skrá upplýsingar um alla nýja viðskiptamenn eða viðskiptavin sem selt er til.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 02/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Skrá nýja viðskiptamenn

Viðskiptamenn eru tekjuleiðin þín. Þú verður að skrá þig hver viðskiptavinur sem þú selur sem viðskiptavinakort. Viðskiptamannaspjöld innihalda upplýsingarnar sem þarf til að selja viðskiptamanninum vörur. Frekari upplýsingar er að finna í [Reikningsfæra sölur](sales-how-invoice-sales.md) og [Skrá nýjar vörur](inventory-how-register-new-items.md).  

Áður en hægt er að skrá nýja viðskiptamenn þarf að setja upp ýmsar sölukóða sem hægt er að velja úr þegar viðskiptamannaspjöldin eru fyllt út. Frekari upplýsingar má finna á [Uppsetning sölu](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## Bæta við nýjum viðskiptamönnum

Hægt er að bæta við nýjum viðskiptamanni handvirkt með því að fylla út síðuna **Viðskiptamannaspjald** eða hægt er að nota sniðmát sem innihalda fyrirframskilgreindar upplýsingar. Til dæmis er hægt að búa til sniðmát fyrir mismunandi forstillingargerðir viðskiptamanna. Með því að nota sniðmát sparast tími þegar nýjum viðskiptamönnum er bætt við og það hjálpar til við að tryggja að upplýsingarnar séu réttar hverju sinni. 

Ef þú býrð til:
* Mörg sniðmát til að nota með fleiri en einni tegund viðskiptamanns, þú getur valið hentugt sniðmát þegar þú bætir við sniðmáti.
* Aðeins eitt sniðmát er notað fyrir alla nýja viðskiptamenn. 

Þegar sniðmát er stofnað geturðu notað aðgerðina **Nota sniðmát** til að nota það í einum eða fleiri viðskiptamönnum. Til að búa til sniðmát skaltu fylla inn upplýsingarnar sem á að nota aftur á síðunni **Viðskiptamannaspjald**, síðan vista hana sem sniðmát. Frekari upplýsingar eru í hlutanum [Til að vista viðskiptamannaspjaldið sem sniðmát](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template).

> [!TIP]
> Það getur reynst gagnlegt að sérsníða síðuna **Sniðmát viðskiptamanns** þegar þú stofnar sniðmát. Þú gætir til dæmis viljað bæta reitnum **Lánamark** við sniðmátið. Nánari upplýsingar [um vinnusvæðið](/dynamics365/business-central/ui-personalization-user#start-personalizing-by-using-the-personalization-mode) sérstilla.

Þú getur einnig stofnað viðskiptamann út frá tengilið. Frekari upplýsingar eru í hlutanum [Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### Að stofna nýtt viðskiptamannaspjald

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Með aðgerðinni **Verð og afsláttur** er hægt að hafa umsjón með sérverði eða afslætti fyrir viðskiptamann þegar pöntun uppfyllir ákveðin skilyrði. Þegar keypt er tiltekin vara, pantað lágmarksmagn eða keypt fyrir dagsetningu, t.d. þegar herferð lýkur, eru dæmi um slík skilyrði. Frekari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).

Viðskiptamaðurinn hefur nú verið skráður og viðskiptamannaspjaldið má nú nota í söluskjölum.  

### Til að vista viðskiptamannaspjaldið sem sniðmát

Þú getur notað viðskiptamannaspjald sem sniðmát þegar ný viðskiptamannaspjöld eru búin til.

1. Á síðunni **Viðskiptamannaspjald** skal velja aðgerðina **Vista sem sniðmát**. Síðan **Viðskiptamannasniðmát** opnast og sýnir viðskiptamannaspjaldið sem sniðmát.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir viðskiptamanninn.
4. Breyttu eða færðu inn víddarkóða sem þú vilt nota fyrir ný viðskiptamannaspjöld sem stofnuð eru með þessu sniðmáti.  
5. Þegar nýja viðskiptamannssniðmátinu er lokið er valið **Í lagi**.

Viðskiptamannasniðmátinu verður bætt við lista viðskiptamannasniðmáta og hægt er að nota það til að búa til ný viðskiptamannaspjöld.

## Eyða viðskiptamannaspjöldum

Ef bókuð eru viðskipti vegna viðskiptamanns er ekki hægt að eyða viðskiptamannaspjaldinu þar sem þörf gæti verið á færslum við endurskoðun. Til að eyða viðskiptamannaspjöldum með fjárhagsfærslum skal hafa samband við samstarfsaðila Microsoft til að gera það með kóða.  

## Vinna með hámarksskuldir

Lánamörk, stöður og greiðsluskilmálar gera [!INCLUDE [prod_short](includes/prod_short.md)] kleift að gefa út viðvörun um lánamark og gjaldfallna stöðu þegar sölupöntun er slegin inn. Ennfremur gera einingar innheimtuskilmála og vaxtaskilmála þér kleift að reikningsfæra vexti og/eða aukagjöld.  

Reiturinn **Lánamark** á viðskiptamannaspjaldinu tilgreinir hámarksupphæð sem viðskiptamaðurinn má fara umfram greiðslustöðuna áður en viðvörun er gefin út. Þegar upplýsingar eru færðar inn í færslubækur, tilboð, pantanir og reikninga, [!INCLUDE [prod_short](includes/prod_short.md)]  prófar bæði söluhausinn og einstakar sölulínur til að ákvarða hvort farið sé fram úr hámarksskuldinni.

Hægt er að bóka jafnvel þótt hámarksskuldin sé komin yfir. Auður reitur merkir að engin hámarksskuld viðskiptamanns er til.  

Hægt er að velja um að fá ekki viðvaranir þegar farið er fram úr hámarksskuld viðskiptamanns og hægt er að tilgreina hvaða tegundir aðvarana á að skoða.

### Viðvaranir lánamarks tilgreindar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi**, velja svo viðeigandi tengil.

2. Í flýtiflipanum **Almennt**, í reitnum **Viðvaranir lánamarks**, skal velja viðeigandi valkost eins og lýst er í eftirfarandi töflu:

    |Valkostur| Description|
    |------|------------|
    |**Báðar aðvaranir**| Báðir reitirnir **Lánamark** og **Gjaldfallin staða** á spjaldi viðskiptamannsins eru athugaðir og aðvörun er send ef viðskiptamaður fer yfir lánamarkið eða er með gjaldfallna stöðu.|
    |**Hámarksskuld**|Gildið í reitnum **Lánamark** á spjaldi viðskiptavinar er borið saman við innistæðu hans, og viðvörun birtist ef innistæðan er yfir þessari upphæð.|
    |**Upphæð vanskila**|Svæðið **Gjaldfallin staða** í spjaldi viðskiptamanns er athugað og viðvörun birtist ef staða viðskiptamanns er gjaldfallin.|
    |**Engin aðvörun**|Engar lánaviðvaranir eru sýndar varðandi stöðu viðskiptamanns.|

## Úthluta sölumanni

Hægt er að úthluta sölumönnum á sendist-til aðsetur viðskiptamanns í stað reikningsaðseturs þeirra svo að söluskýrslurnar endurspegli rétta landfræðilega dreifingu á sölu. Ef sölumanni er úthlutað á sendist-til aðsetur viðskiptamanns fæst nákvæmari innsýn og betrun forðaúthlutunar.

Úthluta sölumanni á síðunni **Viðskiptamaður** með því að velja **Viðskiptamaður** og síðan **Sendist-til aðsetur** til að opna síðuna **Sendist-til - Aðsetur - Listi** . Velja Skal **Stjórna** og breyta **svo** til að opna síðuna **Sendist-til aðsetursspjald** . Kóti **sölumanns er færður** inn eða valinn til að velja sölumanninn.

Þegar valkosturinn **Annað afhendingaraðsetur** er valinn sem **Sendist-til** birgðageymsla á söluskjali **uppfærist Kóti** sölumanns svo hann passi við sölumanninn **frá Sendist-til í stað þess að** reikningsfæra á **aðsetrið** . 

## Sjá einnig .

[Skilgreina Greiðsluhætti](finance-payment-methods.md)  
[Sameina tvítekin atriði](sales-how-merge-duplicate-records.md)  
[Stofnun númeraraða](ui-create-number-series.md)  
[Virkja hlutaafhendingu með sendingarráðleggingum](sales-how-send-partial-shipments.md)  
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Nota kortaþjónustu til að finna staðsetningar og leiðsagnir](across-online-maps.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
