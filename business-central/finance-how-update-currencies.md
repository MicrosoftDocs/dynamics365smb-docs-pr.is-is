---
title: Uppfæra gengi gjaldmiðils| Microsoft Docs
description: Fylgstu með upphæðum í mismunandi gjaldmiðlum með gjaldmiðilskóðum og leyfðu Business Central að hjálpa þér að stilla gengi bókaðra færslna með utanaðkomandi þjónustu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: be39f8a56dc95ed48e339e89513a103d044faa08
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2020
ms.locfileid: "2952675"
---
# <a name="update-currency-exchange-rates"></a>Uppfæra gengi
Þar sem fyrirtæki starfa að auknum mæli í fleiri löndum/svæðum verður æ mikilvægara fyrir þau að geta átt viðskipti og skráð fjárhag sinn í fleiri en einum gjaldmiðli. Setja þarf upp kóða fyrir hvern gjaldmiðil sem notaður er ef keypt er eða selt í öðrum gjaldmiðlum en staðbundinn gjaldmiðill, ef eitthvað er útistandandi eða gjaldfallið í öðrum gjaldmiðlum, eða ef fjárhagsfærslur eru skráðar í mismunandi gjaldmiðlum.

Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM), en þú getur sett hann upp til að einnig nota annan gjaldmiðil með rétt gengi stillt. Sé öðrum gjaldmiðli gefin svokölluð skilgreining Viðbótarskýrslugjaldmiðill mun [!INCLUDE[d365fin](includes/d365fin_md.md)] skrá upphæðirnar sjálfkrafa bæði í SGM og þessum viðbótarskýrslugjaldmiðli í hverri fjárhagsfærslu og í öðrum færslum á borð við færslur fyrir VSK. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Gengi leiðrétt
Vegna þess hve tíðar gengisbreytingar eru verður reglubundið að leiðrétta aðra jafngildisgjaldmiðla í kerfinu. Sé það ekki gert verða upphæðir misvísandi sem hafa verið umreiknaðar úr erlendum (eða aukalegum) gjaldmiðlum og bókaðar í fjárhag í SGM. Að auki verður að uppfæra daglegar færslur sem eru bókaðar áður en daglegt gengi er fært inn eftir að upplýsingarnar um daglegt gengi hafa verið færðar inn.

Keyrslan **Stilla gengi** er notuð til að lagfæra handvirkt gengi bókaðs viðskiptamanns, lánardrottins og bankareikningsfærslna. Hún getur einnig uppfært upphæðir annars skýrslugjaldmiðils í fjárhagsfærslum. Einnig er hægt að leiðrétta gengi sjálfkrafa með því að nota þjónustu. Frekari upplýsingar er að finna í [Að setja upp þjónustu um gengi gjaldmiðils](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### <a name="effect-on-customers-and-vendors"></a>Áhrif á viðskiptamenn og lánardrottna
Keyrslan leiðréttir gjaldmiðilinn í reikningum viðskiptamanna og lánardrottna með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hverja gjaldmiðilsstöðu og bókar upphæðirnar á fjárhagslykilinn sem tilgreindur er í reitnum **Reikningur óinnleysts hagnaðar** eða í reitnum **Reikningur óinnleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á reikninginn útistandandi - gjaldfallið í fjárhag.

Keyrslan vinnur allar opnar viðskiptamanna- og lánardrottnafærslur. Ef gengismunur er á færslu stofnar keyrslan nýjan sundurliðaða viðskiptamanna- eða lánardrottnafærslu sem endurspeglar leiðréttu upphæðinna í viðskiptamanna- eða lánardrottnafærslunni.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Víddir í fjárhagsfærslum viðskiptavina og lánardrottna
Leiðréttingarfærslum er úthlutað víddum úr viðskiptavina-/lánardrottnafærslum og leiðréttingar eru bókaðar eftir samsetningum á víddagildum.

### <a name="effect-on-bank-accounts"></a>Áhrif á bankareikninga
Keyrslan leiðréttir gjaldmiðilinn í bankareikningum með því að nota gengið sem gildir fyrir bókunardagsetninguna sem tilgreind er í keyrslunni. Keyrslan reiknar mismuninn fyrir hvern bankareikning sem er með gjaldmiðilskóða og bókar upphæðirnar á fjárhagslykilinn sem er tilgreindur í reitnum **Reikningur innleysts hagnaðar** eða í reitnum **Reikningur innleysts taps** á síðunni **Gjaldmiðlar**. Jöfnunarfærslurnar bókast sjálfkrafa á fjárhag bankareikninga sem eru tilgreindir í bókunarflokki bankareikninga. Keyrslan reiknar eina færslu á hvern gjaldmiðil í hverjum bókunarflokki.

#### <a name="dimensions-on-bank-account-entries"></a>Víddir í bankareikningsfærslum
Leiðréttingarfærslum vegna fjárhagsreiknings bankareikningsins og vegna hagnaðar-/tapreiknings er úthlutað sjálfgefnum víddum bankareikningsins.

### <a name="effect-on-gl-accounts"></a>Áhrif á fjárhagsreikninga
Ef bókað er í öðrum skýrslugjaldmiðli er hægt að láta keyrsluna búa til nýjar fjárhagsfærslur fyrir gjaldmiðilsmismun á SGM og öðrum skýrslugjaldmiðli. Keyrslan reiknar mismuninn miðað við hverja einstaka fjárhagsfærslu og leiðréttir fjárhagsfærsluna með tilliti til innihaldi reitsins **Gengisleiðrétting** fyrir hvern fjárhagslykil.

##### <a name="dimensions-on-gl-account-entries"></a>Víddir í fjárhagsreikningsfærslum
Leiðréttingarfærslunum er úthlutað sjálfgefnu víddunum í reikningunum sem þær eru bókaðar á.

> [!Important]
> Áður en hægt er að nota keyrsluna verður að færa inn gengið sem á að nota til þess að leiðrétta gengismun gjaldeyrisins. Þetta er gert á síðunni **Gengi gjaldmiðla**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Setja upp þjónustu um gengi gjaldmiðils
Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum uppfærðum, t.d. FloatRates.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónusta um gengi gjaldmiðils** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Fylltu í reitina eftir því sem nauðsyn krefur á síðunni **Þjónusta fyrir gengi gjaldmiðils**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veldu reitinn **Virkt** til að virkja þjónustuna.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Til að uppfæra gengi í gegnum þjónustu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gjaldmiðlar** og veldu síðan tengda tengilinn.
2. Veldu aðgerðina **Uppfæra gengi**.

Gildið í **Gengi** reitnum á síðunni **Gjaldmiðlar** er uppfært með nýjustu gengi gjaldmiðilsins.

## <a name="see-related-training-at-microsoft-learnlearnpathsuse-multiple-currencies-dynamics-365-business-central"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig
[Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
