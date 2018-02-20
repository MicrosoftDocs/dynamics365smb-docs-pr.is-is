---
title: "Hvernig á að: Bóka birgðakostnað í fjárhag| Microsoft Docs"
description: "Lýsir því hvernig skal vinna með efnislegar vörur sem þú átt viðskipti með, til dæmis að meðhöndla birgðir í vöruhúsinu."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 07/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b71ca658374679860fae487c60d52502ce8eb243
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-inventory-costs-with-the-general-ledger"></a>Afstemma birgðakostnað í fjárhag
Þegar birgðafærslur, til dæmis söluafhending, innkaupareikningur eða birgðaleiðrétting eru bókaðar eru breytingar á kostnaði hinnar leiðréttu vöru skráðar í virðisfærslum birgða. Til að endurspegla þessar breytingar á birgðavirði í ársreikningum, er birgðakostnaður bókaður sjálfkrafa á tengda birgðareikninga í fjárhag. Fyrir hverja birgðafærslu sem er bókuð er viðeigandi gildi bókað í birgðareikninginn, leiðréttingarreikninginn og KSV-reikninginn í fjárhagnum.

Sjálfvirk kostnaðarbókun er skilgreind í reitnum **Sjálfvirk kostnaðarbókun** í glugganum **Uppsetning birgða**.

Þó svo birgðakostnaður sé bókaður sjálfkrafa í fjárhag þarf samt að tryggja að kostnaður vara sé framsendur á viðeigandi sölufærslur á útleið, sérstaklega þar sem vörur eru seldar áður en reikningur er gefinn út fyrir kaupunum. Í kerfinu er þetta kallað kostnaðarleiðrétting. Vörukostnaður er sjálfkrafa leiðréttur þegar vörufærslur eru bókaðar en einnig er hægt að leiðrétta vörukostnað handvirkt. Nánari upplýsingar eru í [Leiðrétta kostnað](inventory-how-adjust-item-costs.md).

## <a name="to-post-inventory-costs-manually"></a>Handvirk bókun birgðakostnaðar
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bóka birgðakostnað í fjárhag** og velja svo viðeigandi tengil.
2. Birgðakostnaður er bókaður handvirkt í fjárhaginn með því að keyra runuvinnsluna. Þegar þessi keyrsla er keyrð eru fjárhagsfærslur stofnaðar á grundvelli virðisfærslna. Hægt er að bóka færslurnar þannig að þær eru teknar saman eftir bókunarhóp.

> [!NOTE]  
> Þegar þessi keyrsla er keyrð gæti kerfið rekist á villur sem hafa með uppsetningu sem vantar að gera eða ósamhæfa víddaruppsetningu. Ef keyrslan rekst á villur í víddaruppsetningunni hefur hún þessar villur að engu og notar víddir virðisfærslunnar. Í tilfelli annarra villna hoppar runuvinnslan yfir bókun virðisfærslnanna og telur þær upp við lok skýrslunnar í hluta sem heitir “Færslur sem hoppað var yfir.” Til að bóka þessar færslur þarf að laga villurnar.

Hægt er að sjá lista af villum áður en bókunarrunuvinnslan er keyrð með því að keyra skýrsluna **Bóka birgðabreytingar - Prófun**. Prófunarskýrslan telur upp allar þær villur sem finnast meðan á bókuninni stendur. Þá er hægt að laga villurnar og keyra bókunarkeyrslu birgðakostnaðar án þess að sleppa neinum færslum.

Til að fá yfirlit yfir það hvaða gildi var hægt að bóka í fjárhaginn án þess að framkvæma bókunina er hægt að keyra keyrsluna **Bóka birgðabreytingar** án þess að bóka gildin raunverulega í fjárhaginn. Hægt er að gera þetta með því að taka hakið úr reitnum **Bóka** á beiðnisíðunni. Á þennan hátt framleiðir kerfið bara skýrslu sem sýnir gildin sem eru tilbúin til bókunar í fjárhaginn þegar keyrslan er keyrð, en eru ekki bókuð.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a>Endurskoða afstemmingu á milli birgðabókar og fjárhags.
Glugginn **Birgðir - Fjárhagsafstemmingar** veitir eftirfarandi:

- Sýnir mun á afstemmingu með því að bera saman skráningar í fjárhag og birgðahöfuðbók (virðisfærslur).
- Sýnir óafstemmdar kostnaðarupphæðir í virðisfærslum í fjárhag eins og þeim væri varpað í samsvarandi birgðatengda reikninga í fjárhag og ber saman við samtölur sem raunverulega eru skráðar í sömu reikninga í fjárhag.
- Sýnir uppbyggingu fjárhags með tvöföldum færslum með myndrænni uppsetningu gagna. KSV-færsla hefur t.d. samsvarandi birgðafærslu.
- Gerir notendum kleift að kafa niður og sjá færslur sem kostnaðarupphæð er samsett úr.
- Er með afmörkunum svo hægt sé að þrengja greiningu eftir dagsetningu, vöru og birgðageymslu.
- Skýrir ástæður fyrir frávikum í afstemmingu með skilaboðum með upplýsingum.


Í dálkinum **Heiti** lengst til vinstri í grindinni sjást ýmsar tegundir fjárhagsreikninga sem tengjast birgðunum.

Dálkarnir **Birgðir**, **Birgðir (Bráðabirgða)**, og **VÍV birgðir** sýna reikningsfært, óreikningsfært, og samtölu VÍV fyrir hverja tegund fjárhagsreiknings. Þær eru reiknaðar með virðisfærslum, það er, samtölunum er varpað í þær gerðir fjárhagsreikninga þar sem þær munu enda þegar þær eru bókaðar endanlega í fjárhag.

Dálkurinn **Samtala** sýnir summu (feitletraða) virðisfærsluupphæða í þremur birgðadálkum.

**Samtala fjárhags** sýnir upphæðirnar (feitletraðar) fyrir hverja tegund fjárhagsreiknings í fjárhag. Þær eru reiknaðar með fjárhagsfærslum, það er tákna birgðakostnað sem þegar hefur verið bókaður í Fjárhag.

Dálkurinn **Mismunur** sýnir muninn á gildinu í reitunum **Samtala fjárhags** og **Samtala**.

Efst í glugganum **Birgðir - Afstemming fjárhags** er hægt að færa inn afmarkanir til að afmarka t.d. tímabil sem sækja á upplýsingar fyrir.

Ef gátmerki er sett í reitinn **Sýna viðvörun** og misræmi er á milli birgðasamtala og fjárhagssamtala birtir kerfið skilaboð í **Viðvörun** reit grindarinnar þar sem misræmið er útskýrt. Ef viðvörunarreiturinn er valinn birtir kerfið meiri upplýsingar um merkingu viðvörunarinnar.

Þegar þú hefur fært inn allar viðeigandi afmarkanir, skal velja **Sýna fylki** aðgerðina. Gögnin eru reiknuð og fylkisglugginn kemur upp.

Í dálkinum lengst til vinstri í grindinni sjást ýmsar tegundir fjárhagsreikninga sem tengjast birgðunum. Grindin sýnir því næst reikningsfærðar, óreikningsfærðar og VÍV birgðasamtölur fyrir hverja reikningstegund. Þessar samtölur eru reiknaðar út frá virðisfærslum.

Næstu dálkar sýna samtölur sömu reikningstegunda sem reiknaðar voru úr fjárhagsfærslunum.

Veldu upphæðina í hvaða samtölureit sem er til að sjá birgðaskýrslufærslurnar sem voru notaðar við útreikninginn. Fyrir birgðasamtölur eru birgðaskýrslufærslurnar summur virðisfærslna fyrir vörurnar. Fyrir fjárhagssamtölur eru birgðaskýrslufærslurnar summur úr fjárhagsfærslum.

## <a name="see-also"></a>Sjá einnig  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

