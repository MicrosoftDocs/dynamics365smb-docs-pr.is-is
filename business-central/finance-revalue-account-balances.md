---
title: Endurmeta stöðu fjárhagur reikninga
description: Læra að endurmeta fjárhagur reikningsstöðu áður en ársreikningar eru framleiddir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 08/06/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# Endurmeta stöðu fjárhagur reikninga

Ef notaðir eru fjárhagur (fjárhagsreikningar) til að skrá, efnahagsvörur í erlendum gjaldmiðlum, skal endurmeta reikningsstöðuna áður en ársreikningar eru framleiddir. Gengi gjaldmiðla breytist oft og endurmat hjálpar til við að gera ársreikningana nákvæmari.

## Setja upp endurmat

Hver reikningur sem á að taka með í endurmat á síðunni **Fjárhagsspjald** er settur upp. Hægt er að velja hvort bóka eigi leiðréttingar á endurmati á raunverulegum eða reikningum fyrir áætlaðan hagnað/tap. Við bókun hagnaðar og gengistaps við gengisleiðréttingu fylgir venjuleg bókunarregla. Það er til dæmis gert fyrir hverja uppsetningu á síðunni **Gjaldmiðlar** . Til að [fræðast meira um gengisleiðréttingar er farið í Uppfæra gengi gjaldmiðla](finance-how-update-currencies.md).

Í reitnum **Bókun** upprunagjaldmiðils er hægt að setja upp villuleit fyrir gjaldmiðla sem leyft er að bóka á einstaka fjárhagsreikninga til að lágmarka villur:

* Allir gjaldmiðlar (auður)
* Margir gjaldmiðlar
* Sami gjaldmiðill
* Staðbundinn gjaldmiðill

## Keyra endurmat

Til að endurmeta upphæðir í erlendum gjaldmiðli í staðbundinn gjaldmiðill fyrir fjárhagsreikningsstöðu á **síðunni Bókhaldslykill** skal nota aðgerðina **Endurmat fjárhagsgjaldmiðils** til að hefja keyrslu. Keyrslan býr til leiðréttingarfærslur í færslubókinni sem valin er. Þegar færslurnar eru bókaðar er staða staðbundinn gjaldmiðill (SGM) leiðrétt fyrir reikninginn. Fjárhagsreikningsstöður sem birtast alltaf í SGM endurspegla nú breytingar á þeim gjaldmiðlum sem færslur voru bókaðar í. Þetta endurmat gerir kleift að búa til nákvæmari fjárhagsskýrslu með minni fyrirhöfn.

Ef annar skýrslugjaldmiðill (AGM) er notaður eru fjárhagsendurmatsfærslurnar með upphæðina AGM. Upphæðin samsvarar aðeins SGM upphæðinni í þessum færslum, ekki staða ÍSM í fjárhagsreikningnum. Ef AGM-gengi er leiðrétt eftir að leiðréttingarnar hafa verið bókaðar er gengisleiðréttingin keyrð einu sinni enn til að leiðrétta allar fjárhagsfærslur.

> [!IMPORTANT]
> Endurmat fjárhagsreiknings uppfyllir hugsanlega ekki allar kröfur um viðskipti og eign skráningar sem þarf að endurmeta. Til dæmis fyrir fjármálafyrirtæki, verðbréf, leigueignir eða ef þær eru notaðar fyrir tiltekið eða mikið magn viðskipta eða eigna. Mælt er með því að þú ræðir við endurskoðandann hvort þú getir notað eiginleikann og hvernig þú notar hana. Til dæmis ef þú leyfir gjaldmiðlum að blanda saman fyrir reikning eða ef þú þarft að halda sérstakan reikning fyrir hvern eign þú vilt rekja.

> [!NOTE]
> Endurmat gefur ekki kost á að jafna eða ógilda færslur, líkt og hægt er að nota við viðskiptamanna- og lánardrottnafærslur. Leiðréttingar gerast á grundvelli stöðu á hverjum gjaldmiðli.

## Endurmeta reikninga á móti gengisleiðréttingum viðskiptamanna og lánardrottna

Endurmat einfaldar verkið við leiðréttingu á fjárhagsreikningsstöðum. Aðgerðin endurmetur stöðuna á hvern gjaldmiðil á hvern fjárhagsreikning líkt og gert er til leiðréttingar á fjárhagsreikningum sem tengjast bankareikningum. Ef fjárhagsreikningur er notaður til að rekja margar eignir skal íhuga að nota reikning lánardrottins eða viðskiptamanns í staðinn.

> [!NOTE]
> Endurmat fjárhagsreiknings uppfyllir hugsanlega ekki allar kröfur um viðskipti og eign skráningar sem þarf að endurmeta. Til dæmis fyrir fjármálafyrirtæki, verðbréf, leigueignir eða ef þær eru notaðar fyrir tiltekið eða mikið magn viðskipta eða eigna. Mælt er með því að þú ræðir við endurskoðandann hvort þú getir notað eiginleikann og hvernig þú notar hana. Til dæmis ef þú leyfir gjaldmiðlum að blanda saman fyrir reikning eða ef þú þarft að halda sérstakan reikning fyrir hvern eign þú vilt rekja.

Eftirfarandi dæmi sýnir mismuninn á því að nota fjárhagsreikning og nota lánardrottnareikning til að rekja stöðu tveggja peningalegra eigna sem nota erlendan gjaldmiðil.

**Nota skal fjárhagsreikning** Ef einn fjárhagsreikningur er notaður til að rekja annaðhvort margar eignir (til dæmis lán eða eignir) í sama gjaldmiðli eða einstakar hlutafærslur fyrir sama eign en samt í sama gjaldmiðli gerir fjárhagsendurmat eina færslu fyrir hvert endurmat fyrir gjaldmiðilinn. Ekki er hægt að rekja leiðréttingar á einstökum eignum eða einstökum viðskiptum í sömu eign.

**Nota skal lánardrottnareikning** Ef settar eru upp margar eignir sem lánardrottnar og færslur eru bókaðar á þær, annaðhvort í sama eða mismunandi gjaldmiðlum, færðu leiðréttingu á hvern lánardrottin. Ef kveikt er á **bókun eftir færsluvíxli** í **verkraðarfærslunni Leiðrétta gengi** gjaldmiðils færðu leiðréttingarfærslu fyrir hverja lánardrottnafærslu.

Mismunurinn skiptir máli þegar metið er hvort fjárhagsendurmat sé réttur eiginleiki fyrir skýrslugerðarþarfir.

> [!TIP]
> Mælt er með því að þú spyrjir endurskoðandann eða endurskoðandann hvaða tegund reiknings hentar fyrirtækinu best. Einnig gæti verið til forrit fyrir [!INCLUDE [prod_short](includes/prod_short.md)]  [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central) það er bara rétt fyrir viðskiptaaðstæður þínar.

## Sjá einnig .

[Fara yfir upphæðir í fjárhagur reikningum](finance-review-accounts.md)    
[Að átta sig á fjárhagur og bókhaldslykli](finance-general-ledger.md)  
