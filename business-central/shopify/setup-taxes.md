---
title: Setja upp skatta fyrir Shopify tengingu
description: Hvernig á að setja upp skatta í Shopify og rekstur miðsvæðis.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 0070d583752002cc34ebff74dee2906c289b7136
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317485"
---
# <a name="set-up-taxes-for-the-shopify-connection"></a>Setja upp skatta fyrir Shopify tenginguna

Í þessari grein munum við rannsaka hvernig ýmsar stillingar í Shopify IMPACT eru hæðst verð og skattar sem birtast viðskiptavininum. Við munum einnig Skoða hvernig á að samskipa [!INCLUDE[prod_short](../includes/prod_short.md)] til að styðja stillingar í Shopify. Þessari grein er ekki ætlað að vera heildstæð skattlagningarhandbók. Til að fá frekari upplýsingar er haft samband við viðkomandi skattyfirvöld eða skattfagra.  

Í greininni er gert ráð fyrir að skylt sé að greiða skatta þegar selja á vörur á staðnum eða alþjóðlega.

## <a name="if-you-sell-domestically"></a>Ef þú selur Innanfrá 

Þegar notandi er skilgreindur Shopify til að innheimta skatta í heimalandi eða svæði notanda er hægt að ákveða hvernig birta eigi verð á Storefront. Þetta er gert með því að virkja eða **gera óvirkan öll verð eru með skattskipta** í [**stillingum skatta og skyldur**](https://www.shopify.com/admin/settings/taxes) í **Shopify admin**.

Algengt er að hafa á þessum víxl virkjanir fyrir slík lönd sem Ástralía, Austurríki, Belgía, Tékkland, Danmörk, Finnland, Frakkland, Þýskaland, Ísland, Ítalía, Holland, Nýja Sjáland, Noregur, Spánn, Svíþjóð, Sviss og Bretland. Á mörkuðum eins og þessum eru verð *100 EUR* skilgreind í afurðakortinni sem er þegar Virðisauki (VSK) og það sama verð birtist viðskiptamanni á Storefront stílsniðinu og við útskrift.  

Í Bandaríkjunum og Kanada búast Viðskiptavinir við að sjá afurðaverð án skatta, sem bætast við við innritun. Þannig að **öll verð eru með skattsvæði** er yfirleitt ekki valið. Í þessu tilfelli er verðið *$100* skilgreint á vöruspjaldinu þar sem verðið er án skatts. Á útskriftarstiginu bætast skattar ofan á verðið til að stemma af við útskriftir alls.

Til að styðja við atburðarásina þar sem **skattur** er valinn á [!INCLUDE[prod_short](../includes/prod_short.md)] hliðinni er reiturinn sniðmát sniðmáts **fylltur út** á **Shopify verkstæðissíðunni** til að komast í sniðmátið með eftirfarandi svæðum:  
<!--I changed that last part of the sentence above because it didn't track logically. Just wanted to let you know in case I introduced an inaccuracy.-->

1. **Almennur viðskiptabókunarflokkur**, notaður fyrir innlenda viðskiptavini.  
2. **VSK-viðskiptabókunarflokkur**, notaður fyrir innlenda viðskiptavini.  
3. **Verð með VSK** stillt á *Já*.  

Skilgreinið nú vöruverð á **birgðaspjaldinu** eða **söluverði LST**, með eða án skatts. Þegar útflutningur á verði til Shopify, kerfið reiknar verðið sem á að innihalda innlenda skatta þá sýnir það verð í vöruspjaldinu í Shopify.

> [!NOTE]
> Ef Connector er samskipað Shopify til að stofna viðskiptavini sjálfkrafa gæti þurft að hafa fleiri reiti í sniðmátinu, svo sem **bókunarflokk** viðskiptamanna. Ef sjálfgefinn viðskiptamaður er notaður fyrir innfluttar pantanir skal ganga úr skugga um að viðskiptamaðurinn hafi sömu reiti. Þú þarft samt að fylla út **Sniðmátskóta** viðskiptamanns eins og tilgreint er að ofan, þar sem **verðin ásamt skattverði**/**með VSK** í stofnaða söluskjalinu fara ekki eftir viðskiptamanninum heldur á **sniðmátinu** viðskiptavinur úr Shopify vinnukorti eða sniðmáti viðskiptamanns á hvert land.

## <a name="if-you-sell-internationally"></a>Ef þú selur alþjóðleg

Í þessum kafla munum við kanna stillingar fyrir atburðarás þar sem þú ert nauðsynleg til að innheimta skatta þegar selt er til annars lands eins og annarra landa í ESB. 

**Shopify Sem stendur styður Connector** Extension eingöngu útflutning á einu verði. Shopify sjálfkrafa á við um staðbundna skatta, gjaldmiðla og sléttun. **Í öllum verðum felst að skattaðili** leiðir niðurstöður í aðgerðunum sem er lýst í eftirfarandi undirköflum.

### <a name="all-prices-include-tax-is-selected"></a>*Öll verð fela í sér að skattur* er valinn

||Sölu innanlands|Erlent land þar sem þú ert að innheimta skatta|Framandi land þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í Storefront stílsniðinu|1200|1200|1200|
|Skatthlutfall prósentu|20|25|0|
|Verð hjá útskriftarferð|1200|1200|1200|

Verð fyrir dvöl viðskiptavina er óbreytt, óháð staðsetningu þeirra, en þú hefur áhrif á framlegð þína vegna skatttaxta hér á landi.

### <a name="all-prices-include-tax-is-not-selected"></a>*Öll verð eru með skatti* er ekki valinn

||Sölu innanlands|Erlent land þar sem þú ert að innheimta skatta|Framandi land þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í Storefront stílsniðinu|1000|1000|1000|
|Skatthlutfall prósentu|20|25|0|
|Verð hjá útskriftarferð|1200|1250|1000|

Shopify bætir staðbundnum skatti ofan á verðið sem skilgreint er á vöruspjaldinu eftir því hvaðan vörur eru sendar til.

## <a name="dynamic-tax-inclusive-pricing"></a>Breytilegar verðlagingar á skattframtali innifaldar

Vegna þess að mismunandi lönd hafa mismunandi kröfur eftir því hvort þú ert með skatt á sýnt verð eða ekki getur þú skipt á [dynamic Skattlagning með verðlagningu](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) í Shopify. Þetta gerir aðgerðina skattþátttöku sjálfvirkt virka. 
<!--I added the last sentence to complete the thought. I hope that's okay.-->

Velja **taka eða útiloka skatt samkvæmt landi** viðskiptamanns á **öðrum mörkuðum-kjörgengur** hluti [**stillinga markaða**](https://www.shopify.com/admin/settings/markets) í **Shopify admin**.  

> [!NOTE]
> Þessi stilling hefur ekki áhrif á framsetningu verðs á innlendum mörkuðum þar sem stýrt er af **öllum verðum með skattvíxla**.

### <a name="all-prices-include-tax-is-selected"></a>*Öll verð fela í sér að skattur* er valinn

||Sölu innanlands|Erlent land þar sem skattur er innifalinn í verði|Erlent land þar sem skattur er undanskilinn|
|------------------------|--------|--------|--------|
|Verð sem birtist í Storefront stílsniðinu|1200|1250|1000|
|Skatthlutfall prósentu|20|25|10|
|Verð hjá útskriftarferð|1200|1250|1100|

Verð fyrir hvern viðskiptavin breytast eftir staðsetningu þeirra.

### <a name="all-prices-include-tax-is-not-selected"></a>*Öll verð eru með skatti* er ekki valinn

||Sölu innanlands|Erlent land þar sem skattur er innifalinn í verði|Erlends lands, þar sem skattur er undanskilinn|
|------------------------|--------|--------|--------|
|Verð sem birtist í Storefront stílsniðinu|1000|1250|1000|
|Skatthlutfall prósentu|20|25|10|
|Verð hjá útskriftarferð|1200|1250|1100|

> [!NOTE]
> Á öllum verðum er **með Skattframtal** breytir ekki hvernig verð eru birt til alþjóðlegra viðskiptavina.

## <a name="if-you-sell-to-eu-customers"></a>Ef selt er til ESB-viðskiptavina

Mismunandi ESB-lönd eru með mismunandi skatthlutföll sveitarfélaga. Ef þú ert hins vegar staðsettur í ESB og selur til annarra ESB landa getur þú notað skatthlutfallið í einhverjum tilvikum.  

**Kannaðu reitinn INNHEIMTA VSK** í **Evrópusambandinu** hluta af [**stillingum skatta og skyldur**](https://www.shopify.com/admin/settings/taxes) í **Shopify admin**.

|Innheimta VSK|VSK hlutfall|
|-|-|
|Micro-Business Undanþága|Notaðu innlendu skatthlutfallið þitt fyrir alla sölu inni á ESB|
|Skráning einnar stöðvaðra vinnuskyldu eða lands|Nota VSK-hlutfall af heimalandi viðskiptamanns|


### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Innheimta VSK sett á einnar stanga verkstæðisskráningu

Í dæminu **hér á eftir er öllum verðum með skattvíxla** virkt. Verðið á vöruspjaldinu er stillt á *1200*. 
        
|-|Sölu innanlands|Framandi land|
|------------------------|--------|--------|
|Verð sem birtist í Storefront stílsniðinu|1200|1250|
|Skatthlutfall prósentu|20|25|
|Verð hjá útskriftarferð|1200|1250|       
        
### <a name="collect-vat-set-to-micro-business-exemption"></a>Innheimta virðisaukaskatt sem sett er á Micro-Business undanþáguna

Í dæminu **hér á eftir er öllum verðum með skattvíxla** virkt. Verðið á vöruspjaldinu er stillt á *1200*. 
        
|-|Sölu innanlands|Erlendis með bundnu skatthlutfalli 25 prósent.|
|------------------------|--------|--------|
|Verð sem birtist í Storefront stílsniðinu|1200|1200|
|Skatthlutfall prósentu|20|20|
|Verð hjá útskriftarferð|1200|1200|           
    
Shopify Hunsar skatthlutfall í erlendu landi þegar reiknað er út endanlegt verð og nýtir það skatthlutfallið innanlands.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Innflutningur Shopify pantana seldur til alþjóðlegra viðskiptavina

Ef verið er að innheimta skatta frá mörgum löndum, þá þarf líklegast að skilgreina landlegu stillingu í [!INCLUDE[prod_short](../includes/prod_short.md)]. Þetta er nauðsynlegt vegna þess að þegar söluskjal er stofnað í [!INCLUDE[prod_short](../includes/prod_short.md)], reiknar kerfið út skatta í stað þess að endurnýta þá sem fluttir eru inn Shopify.

Lands-/svæðisbundnar stillingar eru valdar í **Shopify glugganum Sniðmát** viðskiptamanns.
<!--Should this be "window" or "page"? I haven't been seeing "window" is use elsewhere, but I don't know what the interface looks like for this action.--> Þar er hægt að skilgreina **Sjálfgefinn viðskm. nr.** Eða **Sniðmát viðskiptamanns nr.**. Í öðru hvoru tilviki skal ganga úr skugga um að valinn Viðskiptamaður eða sniðmát hafi eftirfarandi reiti skilgreinda:

1. **Almennur viðskiptabókunarflokkur** (notað fyrir erlenda viðskiptamenn).
2. **VSK-viðskiptabókunarflokk** (notað fyrir erlenda viðskiptamenn).
3. **Verð með VSK** (stilla með stillingu á Shopify hliðinni):
* Velja *skal Já* ef **öll verð eru með skatti** er virkjaður og **taka með eða útiloka skatt samkvæmt því að land** viðskiptamanns er óvirkt.
* Velja Nei ef *öll verð eru með skatti* er **ekki** hægt **að nota eða útiloka að skattur sem byggður er á landi** viðskiptamanns sé gerður óvirkur.
* Velja *Já* ef **hafa á með eða útiloka að skattur samkvæmt landi** viðskiptamanns er virkjaður og land eða svæði er skráð í skattframtali sem [tekur til landa](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Velja *skal Nei* ef **hafa á með eða útiloka skatt samkvæmt landi** viðskiptamanns er virkt og land/svæði er ekki skráð í skattalöndum sem eru innifalin í [skatti](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
<!--I changed "Set" to "Choose" since "Set" really isn't an instruction we use. if they're toggling, we then would say "Toggle" as in "Toggle *No* if...."-->
> 
[!Note]
> Stillingin **verð með VSK** fylgir sniðmátinu, ekki frá tilteknum viðskiptamanni. Þess vegna skiptir miklu máli að hafa viðskiptamannssniðmátið skilgreint.

## <a name="other-tax-remarks"></a>Aðrar skattaummælis

Á meðan innflutt Shopify pöntun inniheldur upplýsingar um skatta, fá skattaútreiknaðar þegar söluskjal er stofnað. Sem endurútreikningur þýðir að mikilvægt er að VSK/tax stillingar séu réttar í [!INCLUDE[prod_short](../includes/prod_short.md)].

- Margföldum afurðskatti eða VSK-taxta. Sumar vörutegundir eru til dæmis gjaldgengar í minni skatthlutföll. Hægt er að [nota aðgerðina skattahnekking](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) í Shopify. Þegar vörur eru fluttar inn og stofnaðar í [!INCLUDE[prod_short](../includes/prod_short.md)], nota þær skattuppsetningu sem útfylltar í vörusniðmátskótanum í Shopify versluninni. Áður en pantanir eru fluttar inn með slíkar vörur þarf að uppfæra VSK-vörubókunarflokkinn.  

- Aðsetur-háð skatthlutföll. Svæðið Forgangur **skattsvæðis er** notað ásamt **töflunni Sniðmát** viðskiptamanns til að skrifa yfir staðlaðar röksemdir sem fylla **út kóta** skattsvæðisins í söluskjalinu. **Svæðið Forgangur** skattsvæðis Tilgreinir forgang varðandi það hvar aðgerðin á að fara með upplýsingarnar um landið eða svæðið og ríkið eða héraðið. Síðan er samsvarandi færsla í Shopify sniðmátum viðskiptamanns auðkennd og **Skattsvæðiskóti**, **skattskyld** og **VSK-Bus. bókunarflokkur** er notaður þegar söluskjal er stofnað.  

## <a name="see-also"></a>Sjá einnig

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
