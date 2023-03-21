---
title: Setja upp skatta fyrir Shopify tengingu
description: Hvernig á að setja upp skatta í Shopify og Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# Setja upp skatta fyrir Shopify tenginguna

Í þessari grein munum við skoða hvernig ýmsar stillingar Shopify hafa áhrif á verð og skatta netverslunarinnar sem birtast viðskiptavininum. Við skoðum einnig hvernig á að stilla [!INCLUDE[prod_short](../includes/prod_short.md)] til stuðnings við stillingar í Shopify. Þessari grein er ekki ætlað að vera ítarlegur leiðarvísir um skattlagningu. Hafðu samband við skattyfirvöld á staðnum eða skattalegan fagaðila til að fá frekari upplýsingar.  

Greinin gerir ráð fyrir að þú hafir skattskyldu þegar þú selur vörur hérlendis eða alþjóðlega.

## Ef þú selur innanlands

Þegar þú hefur stillt hvernig Shopify innheimtir skatta í heimalandi þínu eða á svæði getur þú ákveðið hvernig þú vilt birta verð í netversluninni þinni.
Þú getur stjórnað þessu með því að virkja eða slökkva á „**Allt verð með skatti** í stillingum fyrir [**Skatta og gjöld**](https://www.shopify.com/admin/settings/taxes) gjöld í **Shopify stjórnendamiðstöðinni**.

Algengt er að kveikja á þessum valkosti fyrir lönd eins og Ástralíu, Austurríki, Belgíu, Bretland, Danmörk, Finnland, Frakkland, Holland, Ísland, Ítalíu, Noreg, Nýja-Sjáland, Spán, Sviss, Svíþjóð, Tékkland, og Þýskaland. Á mörkuðum eins og þessum er verðið *EUR 100* sem skilgreint er á vöruspjaldinu nú þegar með virðisaukaskatti (VSK) og að sama verð sé birt fyrir viðskiptavini í vefverslun og þegar gengið er frá kaupum.  

Viðskiptavinir í Bandaríkjunum og Kanada eru vanir að sjá vöruverð án skatta sem er bætt við þegar gengið er frá kaupum. Þannig að reiturinn fyrir **Allt verð með skatti** er yfirleitt ekki valinn. Í þessu tilviki er verðið *$100* sem skilgreint á vöruspjaldinu án skatta. Þegar gengið er frá kaupum verða skattar lagðir ofan á verðið til að reikna út heildarupphæð kaupa.

Til að styðja við þá sviðsmynd þar sem **Allt verð með skatti** er valin á [!INCLUDE[prod_short](../includes/prod_short.md)] hliðinni er fyllt út í reitinn fyrir **Sniðmátskóði viðskiptavinar** á síðunni fyrir **Shopify verslunarkort** til að fá aðgang að sniðmátinu með eftirfarandi reitum sem eru skilgreindir:  

1. **Almennur viðskiptabókunarflokkur**, notaður fyrir innlenda viðskiptavini.  
2. **VSK-viðskiptabókunarflokkur,** notaður fyrir innlenda viðskiptavini.  
3. **Verð með VSK** stillt á *já*.  

Skilgreindu nú vöruverð í reitnum **Birgðarspjald** eða **Söluverðslisti** með eða án skatts. Við útflutning á verði til Shopify reiknar kerfið út það verð sem á að taka innlenda skatta og sýnir síðan það verð í viðkomandi vöruspjaldi Shopify.

> [!NOTE]
> Ef þú stilltir Shopify tengilinn til að búa til viðskiptavini sjálfkrafa gætirðu þurft fleiri reiti í sniðmátinu, svo sem **Bókunarflokk viðskiptavinar**. Ef þú notar sjálfgefinn viðskiptavin fyrir innfluttar pantanir skaltu ganga úr skugga um að viðskiptavinurinn sé með sömu reiti útfyllta. Þú þarft samt að fylla út **Sniðmátskóði viðskiptavinar** eins og tilgreint er hér að ofan, vegna þess að reiturinn **Verð með skatti**/**Verð með VSK** í stofnuðu söluskjali fer ekki eftir viðskiptavini, heldur eftir **Sniðmáti viðskiptavinar** af verslunarkorti Shopify eða sniðmáti viðskiptavinar í hverju landi fyrir sig.

## Ef þú selur alþjóðlega

Í þessum hluta skoðum við stillingar fyrir sviðsmyndir þar sem þú þarft að innheimta skatta þegar þú selur til annars lands, svo sem annarra landa í ESB.

Sem stendur **Shopify styður** tengiviðbótin aðeins útflutning á einu verði. Shopify er sjálfkrafa lagt á staðbundna skatta, gjaldmiðla og námundun. **Allt verð með skatti** birtir niðurstöður í aðgerðunum sem lýst er í eftirfarandi undirköflum.

### *Allt verð með skatti* er valið

|-|Sala innanlands|Erlent land þar sem þú innheimtir skatt|Erlent land þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1200|1200|1200|
|Prósenta skattur gefa einkunn|20|25|0|
|Verð þegar gengið er frá kaupum|1200|1200|1200|

Verðið fyrir viðskiptavininn helst óbreytt, óháð staðsetningu þeirra, en hagnaðarhlutfall þitt verður fyrir áhrifum vegna mismunandi skatthlutfalla í hverju landi fyrir sig.

### *Allt verð með skatti* er ekki valið

|-|Sala innanlands|Erlent land þar sem þú innheimtir skatt|Erlent land þar sem þú ert ekki að innheimta skatta|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1000|1000|1000|
|Prósenta skattur gefa einkunn|20|25|0|
|Verð þegar gengið er frá kaupum|1200|1250|1000|

Shopify bætir staðbundnir skattar ofan á það verð sem skilgreint er á vörusphaldinu miðað við hvert varan er send.

## Sveigjanleg verðlagning með skatti

Þar sem mismunandi lönd gera mismunandi kröfur eftir því hvort skattur er innifalinn í verðinu eða ekki, getur þú breytt yfir í [Sveigjanlega verðlagningu með skatti](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) í Shopify. Þannig er skatturinn sjálfvirkt tekinn með.

Veldu **Taka með eða undanskilja skatt miðað við land viðskiptavinar** í hlutanum **Aðrir markaðir - stillingar** í stillingunum [**Markaðir**](https://www.shopify.com/admin/settings/markets) í **Shopify stjórnandamiðstöðinni**.  

> [!NOTE]
> Þessi stilling hefur ekki áhrif á framsetningu verðs á innlendum mörkuðum sem er stjórnað af valkostinum **Allt verð með skatti**.

### *Allt verð með skatti* er valið

|-|Sala innanlands|Erlent land þar sem virðisaukaskattur er innifalinn í verði|Erlent land þar sem skattur er undanþeginn|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1200|1250|1000|
|Prósenta skattur gefa einkunn|20|25|10|
|Verð þegar gengið er frá kaupum|1200|1250|1100|

Verð fyrir hvern viðskiptavin breytist eftir því hver staðsetning þeirra er.

### *Allt verð með skatti* er ekki valið

|-|Sala innanlands|Erlent land þar sem virðisaukaskattur er innifalinn í verði|Erlent land, þar sem skattur er undanskilinn|
|------------------------|--------|--------|--------|
|Verð sem birtist í netversluninni|1000|1250|1000|
|Prósenta skattur gefa einkunn|20|25|10|
|Verð þegar gengið er frá kaupum|1200|1250|1100|

> [!NOTE]
> **Allt verð með skatti** breytir ekki því hvernig verð er birt alþjóðlegum viðskiptavinum.

## Ef þú selur innan ESB

Mismunandi ESB lönd eru með mismunandi staðbundna skatthlutfall. Ef þú ert staðsett/ur í ESB og selur til annarra ESB-landa er í sumum tilvikum hægt að nota staðbundna skatthlutfallið hjá þér.  

Hakaðu við reitinn **Innheimta VSK** í hlutanum **Evrópusambandið** í [**Skattar og gjöld**](https://www.shopify.com/admin/settings/taxes) í **Shopify stjórnendamiðstöðinni**.

|Innheimta VSK|VSK-hlutfall|
|-|-|
|Undanþága fyrir smáfyrirtæki|Notaðu innlenda skatthlutfallið þitt fyrir alla sölu innan ESB|
|Skráning vefverslunar eða landsbundin skráning|Nota VSK-hlutfall í landi viðskiptavinar þíns|


### Innheimta VSK sem er stilltur á skráningu í netverslun

Í eftirfarandi dæmi er kveikt á víxlhnappnum **Allt verð með skatti**. Verðið á vöruspjaldinu er stillt á *1200*.
        
|-|Sala innanlands|Erlent land|
|------------------------|--------|--------|
|Verð sem birtist í netversluninni|1200|1250|
|Prósenta skattur gefa einkunn|20|25|
|Verð þegar gengið er frá kaupum|1200|1250|       
        
### Innheimta VSK sem er stilltur á undanþágu vegna smáfyrirtækja

Í eftirfarandi dæmi er kveikt á víxlhnappnum **Allt verð með skatti**. Verðið á vöruspjaldinu er stillt á *1200*.
        
|-|Sala innanlands|Erlent land með 25 prósent staðbundið skatthlutfall.|
|------------------------|--------|--------|
|Verð sem birtist í netversluninni|1200|1200|
|Prósenta skattur gefa einkunn|20|20|
|Verð þegar gengið er frá kaupum|1200|1200|           
    
Shopify hunsar skatthlutfallið í erlenda landinu við útreikning á endanlegu verði og notar innlenda skatthlutfallið.

## Innflutningur Shopify pantana seldur til alþjóðlegra viðskiptavina

Ef þú ert að innheimta skatta frá mörgum löndum er líklegast að þú þurfir að skilgreina landsbundnar stillingar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Slíkt er áskilið vegna þess að þegar söluskjal verður búið til á [!INCLUDE[prod_short](../includes/prod_short.md)] reiknar kerfið út skatta í stað þess að endurnýta skatta flutta inn frá Shopify.

Stillingar fyrir land/svæði eru valdar í glugganum **Shopify Sniðmát viðskiptavinar**. Þar getur þú skilgreint **Sjálfgefið nr. viðskiptavinar** eða **Sniðmátsnr. viðskiptamanns.**. Í báðum tilvikum skal ganga úr skugga um að eftirfarandi reitir séu skilgreindir fyrir valinn viðskiptavin eða sniðmát:

1. **Almennur viðskiptabókunarflokkur** (notaður fyrir erlenda viðskiptavini).
2. **VSK-viðskiptabókunarflokkur** (notaður fyrir erlenda viðskiptavini).
3. **Verð með VSK** (í samræmi við stillingu hér til Shopify hliðar):
* Veldu *Já* ef kveikt er á **Allt verð er með skatti** og slökkt er á **Taka með eða undanskilja skatt miðað við land viðskiptavinar**.
* Veldu *Nei* ef slökkt er á **Allt verð með skatti** og slökkt er á **Taka með eða undanskilja skatt miðað við land viðskiptavinar**.
* Veldu *Já* ef kveikt er á **Taka með eða undanskilja skatt miðað við land viðskiptavinar** og landið eða svæðið er skráð í [Lönd þar sem skattur er innifalinn](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Veldu *Nei* ef kveikt er á **Taka með eða undanskilja skatt miðað við land viðskiptavinar** og land/svæði er ekki skráð í [Lönd þar sem skattur er innifalinn](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

[!Note]
> Stillingarnar í reitnum **Allt verð með VSK** eru úr sniðmátinu, ekki frá tilteknum viðskiptavini. Þess vegna er mikilvægt að sniðmát viðskiptavinarins sé skilgreint.

## Aðrar athugasemdir um skatta

Þó að innflutt Shopify pöntun innihaldi upplýsingar um skatta eru skattarnir endurreiknaðir þegar söluskjal er búið til. Endurútreikningur þýðir að mikilvægt er að VSK/skattur stillingarnar séu réttar í [!INCLUDE[prod_short](../includes/prod_short.md)].

- Mörg vöruskatts- eða VSK-hlutföll. Til dæmis eru tilteknir vöruflokkar gjaldgengir fyrir lægri skatthlutfalli. Hægt er að nota eiginleikann [hnekking skatts](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) í Shopify. Þegar hlutir eru fluttir inn og búnir til í [!INCLUDE[prod_short](../includes/prod_short.md)] nota þeir skattauppsetninguna eins og hún er útfyllt í sniðmáti vörunnar í Shopify versluninni. Áður en þú flytur inn pantanir með slíkum vörum þarftu að uppfæra VSK-vörubókunarflokkinn.  

- Skatthlutföll háð heimilisfangi. Notaðu reitinn **Forgangur skattsvæðis** ásamt **Sniðmát viðskiptavinar** til að skrifa yfir stöðluðu rökin sem fylla út **Skattsvæðiskóða** í söluskjalinu. Reiturinn **Forgangur skattsvæðis** tilgreinir forgang varðandi það hvar aðgerðin á að taka við upplýsingum um landið eða svæðið og fylkið eða héraðið. Þá er samsvarandi skrá í Shopify sniðmátum viðskiptavina auðkennd og **Skattsvæðiskóði**, **Skattskylda** og **VSK-viðsk.bókunarflokkur** eru notaðar þegar söluskjal er búið til.  

## Sjá einnig

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
