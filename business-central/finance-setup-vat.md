---
title: Setja upp virðisaukaskatt
description: 'Ganga úr skugga um að rétt reikna, bóka, og tilkynna á VSK vegna sölu eða innkaup. Mælt er með að nota uppsetningarleiðsögn til að setja upp VSK.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 01/31/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts

Neytendur og fyrirtæki greiða virðisaukaskatt (VSK) þegar þau kaupa vörur eða þjónustu. Upphæð VSK til greiðslu getur verið mismunandi, það fer eftir nokkrum þáttum. Í [!INCLUDE[prod_short](includes/prod_short.md)], setur þú upp VSK til að tilgreina taxtana til að nota til að reikna skattaupphæðir, byggt á eftirfarandi færibreytum:

* Hverjum selt er  
* Hverjum keypt er af  
* Það sem er selt  
* Hvað keypt er  

Hægt er að setja upp VSK-útreikning handvirkt, en það getur verið bæði snúið og tímafrekt. Það er auðvelt að nota mismunandi virðisaukaskattshlutföll fyrir mistök og búa til ónákvæmar virðisaukaskattstengdar skýrslur. Til að auðvelda uppsetningu VSK mælum við með því að þú notir uppsetningarleiðbeiningarnar **Uppsetning á VSK** sem gefnar eru upp í vörunni. 

Ef þú vilt hins vegar setja upp VSK-útreikninga á eigin spýtur eða vilt bara fræðast um hvert skref fyrir sig, þá inniheldur þessi grein lýsingar á öllum skrefunum:  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended"></a>Setja upp VSK með leiðbeiningum um uppsetningu með hjálp (ráðlagt)

> [!NOTE]
> Hægt er að nota leiðbeiningarnar **Uppsetning á VSK** aðeins ef þú hefur stofnað *Mitt fyrirtæki* og hefur ekki bókað færslur sem innihalda VSK.

Til að ræsa uppsetningleiðbeiningar með hjálp, fylgið þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið og sláðu inn **Uppsetning með hjálp**. 
2. Veldu **Setja upp virðisaukaskatt (VSK)** og ljúktu við skrefin.
3. Þegar uppsetningu með hjálp er lokið skal fara á síðuna **VSK-bókunargrunnur** og skoða hvort fylla þurfi út fleiri reiti samkvæmt staðbundnum kröfum í þinni útgáfu af [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna á [Staðbundin virkni í Business Central](about-localization.md)  

### <a name="check-the-vat-posting-setup"></a>Skoða VSK-bókunargrunninn

Til að styðja við fljótlega byrjun tilkynnir [!INCLUDE [prod_short](includes/prod_short.md)] þér um fjárhagsreikninga sem vantar í bókunarflokka eða bókunargrunna, eins og á síðunni **VSK-bókunargrunnur**. Þú getur kveikt eða slökkt á þessari tegund tilkynningar með því að nota tilkynninguna *Fjárhagsreikning vantar í bókunarflokki eða uppsetningu* á síðunni **Mínar tilkynningar**. Farðu bara á síðuna **Mínar stillingar** og veldu síðan *Breyta þegar ég fæ tilkynningar*. .  

Ef þú velur slíka tilkynningu býr [!INCLUDE [prod_short](includes/prod_short.md)] sjálfkrafa til þessa bókunargrunna út frá bókunarflokkum í skjalinu eða færslubókinni sem þú ert að vinna í.  

Á þessum tímapunkti geturðu bara fyllt út í fjárhagsreikningana sem vantar. En seinna gætirðu komist að því að upphafleg uppsetning sé röng þegar þú byrjar að fínstilla hana. Og [!INCLUDE [prod_short](includes/prod_short.md)] leyfir ekki eyðingu á uppsetningu VSK bókunar og almennri bókunaruppsetningu þegar færslur hafa verið búnar til byggðar á slíkum stillingum. Frá og með útgáfutímabili 1 árið 2022 getur þú notað reitinn **Útilokað** á síðunni **VSK-bókunargrunnur** til að koma í veg fyrir að notendur noti uppsetningu sem á ekki lengur við fyrir nýjar bókanir.

## <a name="set-up-a-default-vat-date-for-documents-and-journals"></a>Setja upp sjálfgefna VSK-dagsetningu fyrir skjöl og færslubækur

VSK-skýrslugerð í [!INCLUDE [prod_short](includes/prod_short.md)] byggir á að **VSK-dagsetning** innihaldi VSK-færslur í VSK-skýrslum á VSK-tímabili. Hægt er að breyta VSK-dagsetningunni á öllum skjölum og færslubókum en tilgreina verður sjálfgefið gildi fyrir VSK-dagsetninguna.

> [!NOTE]
> Eftir að skjalið eða dagbókin hefur verið bókuð mun **VSK dagsetning** birtast á **VSK færslum** og **G/L Entries** sem og á birta skjalinu ef það er til.

Til að setja upp sjálfgefið gildi fyrir VSK-dagsetningu þarf að fylgja þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Í flýtiflipanum **Almennt**, í reitnum **Sjálfgefinn VSK-dagsetning**, skaltu velja annaðhvort **Bókunardagsetning** eða **Dagsetning skjals**.
3. Loka síðunni.  

> [!NOTE]
> Sjálfgefið er að **Sjálfgefin VSK-dagsetning** sé **Bókunardagsetning**.

### <a name="enabling-or-disabling-the-vat-date-feature"></a>Virkja eða slökkva á VSK Date eiginleikanum

Sum lönd/svæði krefjast þess að fyrirtæki noti tiltekna VSK dagsetningu, en önnur lönd/svæði gera það ekki. Sum lönd/svæði krefjast þess að fyrirtæki breyti virðisaukaskattsdagsetningu við sérstakar aðstæður eftir að þau hafa birt skjöl, en önnur lönd leyfa ekki breytingar á virðisaukaskattsdögum. Til að gera ráð fyrir mismunandi samhengi geturðu valið hvort þú vilt nota þessa virkni og, ef svo er, að hve miklu leyti.

Fylgdu þessum skrefum til að setja upp virðisaukaskattsnotkunarstig:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á **General** Fastflipanum, í reitnum **VSK Dagsetning Notkun**, tilgreinið að hvaða marki þú vilt nota VSK dagsetning eiginleiki. Þú getur valið einn af eftirfarandi valkostum:

| Gerð | Heimildasamstæða |
|--------------------|-----------------------------------------|
| **Notaðu alla virkni VSK Dagsetningar** | Allt sem tengist **VSK Date** virkar sjálfgefið og gefur þér hámarksvirkni **VSK Date** . Þú getur sett upp dagsetninguna, breytt henni í skjölum, tilkynnt út frá henni og breytt dagsetningunni eftir færslu svo framarlega sem tímabilið er ekki lokað eða varið með leyfilegum dagsetningum fyrir færslu. |
| **Notaðu en leyfðu ekki breytingar** | Allt sem tengist **VSK Dagsetning** virkar sjálfgefið með einni undantekningu. Þú getur ekki breytt **VSK dagsetningu** í **VSK færslum**. |
| **Notar ekki VSK Date virkni** | [!INCLUDE [prod_short](includes/prod_short.md)] mun fela og gera **VSK Date** reitina ekki aðgengilega á skjölum, dagbókum og færslum.  **Sjálfgefin VSK dagsetning** er stillt sem **Bókunardagsetning**. |

3. Loka síðunni.

> [!IMPORTANT]
> Jafnvel ef þú velur **Notandi ekki VSK Dagsetning** valkosturinn, mun [!INCLUDE [prod_short](includes/prod_short.md)] nota **VSK Dagsetning** í bakgrunni. Vegna þess að **Sjálfgefin VSK dagsetning** er stillt sem **Bókunardagsetning** og þú getur ekki breytt henni í þessu tilviki, þú munt fá sömu upplifun og án þessa eiginleika. **VSK Date** reitir verða fjarlægðir af öllum síðum, en þessi reitur verður áfram til í töflum og skýrslur munu vinna út frá honum.

### <a name="limiting-periods-for-posting-and-changing-the-vat-date"></a>Takmörkun á bókun og breytingu á VSK dagsetningu

Þú getur komið í veg fyrir að fólk birti eða breyti VSK-færslum á tilteknum tímabilum. Þú stillir takmörkunina með því að nota tvær stillingar:

* Byggt á lokuðu **VSK skilatímabili**
* Byggt á reitunum **Leyfa færslu frá** og **Leyfa færslu á** .

#### <a name="to-limit-posting-based-on-vat-return-period"></a>Til að takmarka bókun miðað við skilatímabil virðisaukaskatts

1. Veldu ![peruna sem opnar TellF Me eiginleikann 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á  **General** Fastflipanum, í reitnum **Stjórn virðisaukaskattstímabils**, skal tilgreina hversu mikil virðisaukaskattsskilatímabil er stjórnað. Eftirfarandi tafla lýsir valkostunum.

| Gerð | Heimildasamstæða |
|--------------------|-----------------------------------------|
| **Lokaðu fyrir færslu innan lokaðs og varaðu við útgefið tímabil** | Koma í veg fyrir að fólk geti bókað skjal eða dagbók, eða að breyta virðisaukaskattsfærslum sem hafa virðisaukaskattsdagsetningu innan lokaðs **VSK skilatímabils**. [!INCLUDE [prod_short](includes/prod_short.md)] sýnir einnig viðvörun ef **VSK skilatímabilið** er opið, en staða **VSK Skil** er **Gefið út** eða **Sent fram**. |
| **Loka fyrir færslu innan lokaðs tímabils** | Koma í veg fyrir að fólk geti póstað skjal eða dagbók, eða að breyta virðisaukaskattsfærslum sem hafa virðisaukaskattsdagsetningu innan lokaðs **VSK skilatímabilsins**. |
| **Varað við færslu á lokuðu tímabili** | Sýndu viðvörun, en ekki loka fyrir bókun, ef þú vilt bóka skjal eða dagbók sem hefur VSK dagsetningu innan lokaðs **VSK skilatímabils**. |
| **Öryrkjar** | Ekki grípa til aðgerða byggt á lokuðu **VSK skilatímabili**. |

#### <a name="limit-posting-based-on-allow-fromto-period"></a>Takmarka færslu byggt á Leyfa frá/til tímabils

> [!NOTE]
> Frá og með Business Central útgáfu 23.1 er þessari stjórn breytt. Í fyrri útgáfum var aðeins ein stjórn á  **uppsetning aðalbókar** síðunnar fyrir bæði bókunardagsetningu og vsk.dagsetningu. Nú eru þessar stýringar skiptar, þannig að stjórn á **General Ledger Setup** síðunni er aðeins fyrir **Bókunardagsetningu** og stjórn á **VSK Uppsetning** síðunni er aðeins fyrir **VSK Dagsetning** aðeins. Það eru líka nýjar dagsetningarstýringar á  **User Setup** síðunni.  

##### <a name="version-231-or-newer"></a>Útgáfa 23.1 eða nýrri

> [!IMPORTANT]
> Þegar þú uppfærir í nýja útgáfu skaltu hafa í huga að gildin eru uppfærð í nýju **Leyfa VSK Dagsetning Frá/Til** í **VSK uppsetningu** síðu byggt á gildunum í **Leyfa bókun frá/til** í **uppsetningu aðalbókar**. Ef þú vilt nota mismunandi dagsetningarstýringar skaltu opna **VSK Setup** síðuna og gera breytingar.  

Þú getur sett upp takmarkanir á fyrirtækinu eða á tilteknum notendastigum.

Til að takmarka allar færslur fyrir allt fyrirtækið:

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **VAT Setup** og veldu síðan tengda hlekkinn.  
2. Á  **VSK Date** Fastflipanum, í reitnum **Allow VSK Date From**, tilgreinirðu VSK dagsetninguna sem þú leyfir frá færslu. Ekki er leyfilegt að bóka skjal eða dagbók með VSK dagsetningu fyrir þessa dagsetningu.  
3. Á  **VSK Dagsetning** Flýtiflipanum, í reitnum **Allow VSK Date To**, tilgreinið VSK dagsetninguna þangað til þú leyfir færslu. Ekki er leyfilegt að bóka skjal eða dagbók með VSK dagsetningu eftir þessa dagsetningu. 

Til að takmarka færslur fyrir tiltekinn notanda:  

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **User Setup** og veldu síðan tengda hlekkinn.  
2. Í reitnum **Notandakenni** tilgreinirðu þann notanda sem hefur leyfi til að skrifa á tilteknu tímabili.  
3. Í reitnum **Leyfa VSK Dagsetning Frá**, tilgreindu VSK dagsetninguna sem þú leyfir bókun frá. Ekki er leyfilegt að bóka skjal eða dagbók með VSK dagsetningu fyrir þessa dagsetningu. 
4. Í reitnum **Leyfa VSK Dagsetning Til** tilgreinirðu VSK dagsetninguna þar sem þú leyfir bókun. Ekki er leyfilegt að bóka skjal eða dagbók með VSK dagsetningu eftir þessa dagsetningu.  

##### <a name="versions-before-231"></a>Útgáfur fyrir 23.1

Þú getur sett upp takmörkun á fyrirtækinu eða tilteknum notendastigum.

Til að takmarka allar færslur fyrir allt fyrirtækið:

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á  **Almennt** flipaflipanum, í reitnum **Leyfa færslu frá**, tilgreinirðu VSK dagsetninguna sem þú leyfir bókun frá. Ekki er leyfilegt að bóka skjal eða dagbók með VSK dagsetningu fyrir þessa dagsetningu.  
3. Á  **Almennt** flipaflipanum, í reitnum **Leyfa færslu á**, skal tilgreina VSK dagsetninguna þar til þú leyfir bókun. Ekki er leyfilegt að bóka skjal eða dagbók með VSK dagsetningu eftir þessa dagsetningu.

Til að takmarka færslur fyrir tiltekinn notanda:

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.  
2. Í reitnum **Notandakenni** tilgreinirðu þann notanda sem hefur leyfi til að birta á tilteknu tímabili.  
3. Í reitnum **Leyfa bókun frá** tilgreinirðu VSK dagsetninguna sem þú leyfir bókun frá. Ekki er leyfilegt að bóka skjal eða dagbók með VSK dagsetningu fyrir þessa dagsetningu.
4. Í reitnum **Leyfa bókun til** tilgreinirðu VSK dagsetninguna þar til þú leyfir bókun. Ekki er leyfilegt að bóka skjal eða dagbók með VSK dagsetningu eftir þessa dagsetningu.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Setja upp VSK-númer fyrir þitt land eða svæði

Til að ganga úr skugga um að rétt VSK-númer séu slegin inn er hægt að skilgreina snið fyrir VSK-númer sem eru notuð í löndum eða svæðum þar sem viðskipti notanda eru stunduð. [!INCLUDE[prod_short](includes/prod_short.md)] sýnir villuboð ef einhver gerir mistök eða notar snið sem er rangt fyrir landið eða svæðið.

Til að setja upp VSK skráningarnúmer skaltu fylgja þessum skrefum:

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lönd/svæði**.
2. Velja skal landið eða svæðið og svo agðerðina **Snið VSK-númers**.
3. Í reitnum **Snið** skal skilgreina sniðin með því að slá inn einn eða fleiri eftirfarandi stafa:  

* **#** Krefst númers sem er ein tala.  
* **@** Krefst stafs. Þetta snið er ekki hástöfum.  
* **?** Leyfir hvaða staf sem er.  

    > [!TIP]
    > Hægt er að nota þessa stafi svo framarlega sem þeir eru alltaf til staðar í sniði landsins eða svæðisins. Þannig að ef þú þarft að setja punkt eða bandstrik á milli talnasetta geturðu skilgreint sniðið sem ##.####.### eða @@-###-### .  

## <a name="set-up-vat-business-posting-groups"></a>Setja upp VSK-viðskiptabókunarflokka

VSK-viðskiptabókunarflokkar á að tákna markaðina þar sem þú stundar viðskiptum við viðskiptamenn og lánardrottna, og tilgreina hvernig á að reikna og bóka VSK á sérhverjum markaði. Dæmi um VSK viðskiptabókunarflokka eru **Innanlands** og **Evrópusambandið (ESB)**.  

Nota skal kóða sem auðvelt er að muna og er auðkennandi fyrir viðskiptaflokkinn, til dæmis **ESB**, **Ekki-ESB**, eða **Innlent**. Hver kóði verður að vera einstakur, sem þýðir að þú getur sett upp eins marga kóða og þú þarft, en þú getur ekki haft sama kóða oftar en einu sinni í töflu.

Til að setja upp VSK-viðskiptabókunarflokk er þessu skrefum fylgt:

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-viðskiptabókunarflokka** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

Hægt er að setja upp sjálfgefna VSK-viðskiptabókunarflokka með því að tengja þá við almenna viðskiptabókunarflokka. [!INCLUDE[prod_short](includes/prod_short.md)] úthlutar sjálfkrafa VSK-viðskiptabókunarflokkinum þegar þú úthlutar viðskiptabókunarflokki til viðskiptamanns, lánardrottins eða fjárhagsreiknings.

## <a name="set-up-vat-product-posting-groups"></a>Uppsetning VSK-vörubókunarflokka

VSK-vörubókunarflokkar tákna þær vörur og tilföng sem þú kaupir eða selur, og ákvarða hvernig skal reikna út og bóka VSK eftir tegund vöru eða tilfangs.

Gott er að nota kóða sem auðvelt er að muna og lýsa genginu, svo sem **VSK** eða **Núll**, **VSK10** eða **Lækkun** fyrir 10 prósenta VSK og **VSK25** eða **Standard** fyrir 25 prósent.

Til að setja upp VSK-viðskiptabókunarflokk er þessu skrefum fylgt:

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-vörubókunarflokk** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Sameina VSK-bókunarflokka og VSK-bókunaruppsetningar

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar VSK-upphæðir í sölu og innkaup á grundvelli VSK-bókunaruppsetninga, sem eru samsetningar VSK-viðskipta- og vörubókunarflokka. Fyrir hverja samsetningu geturðu valið VSK-prósenta, VSK-útreikningstegund, og fjárhagsreikninga fyrir bókun VSK sem tengist sölu, innkaupum, og bakfærðum gjöldum. Einnig er hægt að tilgreina hvort endurreikna skal VSK þegar greiðsluafsláttur er veittur eða fenginn.  

Hægt er að setja upp ótakmarkaðan fjölda samsetninga. Til að flokka uppsetningarsamsetningar VSK bókunar með svipuðum eiginleikum, skilgreinið **VSK auðkenni** fyrir hvern hóp og úthlutað auðkenninu til hópmeðlima.  

> [!NOTE]
> A **VSK auðkenni** er kóði sem þú getur notað til að flokka svipaða eiginleika. Við mælum með að þú notir mismunandi VSK auðkenni fyrir mismunandi VSK prósentur.  

Til að sameina VSK-bókunaruppsetningar skal fylgja eftirfarandi skrefum:

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 5.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Úthluta VSK-bókunarflokkum sjálfvirkt til fjölda eininga

Eigi að beita sömu VSK-bókunarflokkum á fjölda eininga, er hægt að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] sem gerir það sjálfvirkt. Hægt er að gera þetta á tvennan hátt:

* Hægt er að úthluta VSK-viðskiptabókunarflokkum til almennra viðskiptabókunarflokka eða sniðmáts viðskiptamanns eða lánardrottins
* Hægt er að úthluta VSK-vörubókunarflokkum til almennum vörubókunarflokkum  

VSK-viðskipta- eða vörubókunarflokki er úthlutað þegar valið er viðskipta- eða vörubókunarflokki fyrir viðskiptamann, lánardrottinn, vöru eða tilföng.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Úthluta VSK-bókunarflokka á reikninga, viðskiptamenn, lánardrottna, vörur og tilföng

Eftirfarandi hlutar útskýra hvernig á að úthluta VSK-bókunarflokkum til einstakra einingar.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Hvernig á að úthluta VSK-bókunarflokkum til einstakra fjárhagsreikninga

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 6.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Opna **Fjárhagsreikningur** spjaldið fyrir reikninginn.  
3. Á **Bókun** Flýtiflipanum, í **Alm. bókunartegund** reitnum, er valið annaðhvort **Sölu** eða **Innkaupa**.  
4. Velja skal VSK-bókunarflokkana til að nota fyrir sölureikninginn eða kaupreikninginn.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Að úthluta VSK-viðskiptabókunarflokkum til viðskiptamenn og lánardrottna.

1. Veldu ![peru sem opnar Segðu mér eiginleikann 7.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinur** eða **Lánardrottinn** og velja síðan viðkomandi tengil.  
2. Á **Viðskiptamaður** eða **Lánardrottinn** spjaldinu, víkið flýtiflipann **Reikningar**.  
3. Veljið VSK-viðskiptabókunarflokkana.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Til að úthluta VSK-vörubókunarflokkar til einstakra vörur og tilföng.

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 8.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vara** eða **Tilfang** og velja síðan viðkomandi tengil.  
2. Gert er eitt af eftirfarandi:  

    * Á **Vöru** spjaldinu, stækkið **Verð & Bókun** Flýtiflipann, og velja síðan **Sýna fleiri** til að birta **VAT Vörubókunarflokkur** reitinn.  
    * Á **Tilfang** spjaldinu, stækkið **Reikningagerð** flipann.  
3. Veljið VSK-vörubókunarflokk.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Setja upp ákvæði til að útskýra VSK undanþágu eða óstaðlaðra VSK taxta

VSK-klausa er sett upp til að lýsa upplýsingum um hvaða tegund VSK er notuð. Reglur stjórnvalda gætu krafist þessara upplýsinga. Þegar búið er að setja upp VSK-ákvæði og tengja það við VSK-bókunaruppsetningu, birtist VSK-ákvæðið á öllum prentuðum söluskjölum sem nota VSK-bókunaruppsetningarflokkinn.

Ef með þarf er einnig hægt að tilgreina hvernig skal þýða VSK ákvæði yfir á öðrum tungumálum. Þegar söluskjal sem inniheldur VSK-kenni er stofnað og prentað, mun skjalið innihalda VSK-ákvæðið sem var þýtt. Tilgreindur tungumálakóðinn á viðskiptamannaspjaldinu ákvarðar tungumálið.

Þegar óhefðbundin VSK-hlutföll eru notuð í mismunandi skjalagerðum, t.d. reikningum eða kreditreikningum, er venjulega krafist þess að fyrirtæki láti undanþágutexta (VSK-klausu) fylgja með til að útskýra af hverju minni virðisaukaskattur eða enginn virðisaukaskattur hefur verið reiknaður. Hægt er að skilgreina mismunandi VSK-klausur til að hafa með í viðskiptaskjölum eftir gerð skjals, t.d. reikningur eða kreditreikningur. Þetta er gert á síðunni **VSK-klausur eftir skjalagerð**.

Hægt er að breyta eða eyða VSK-klausu og þá birtast breytingarnar í myndaðri skýrslu. Hins vegar [!INCLUDE[prod_short](includes/prod_short.md)] heldur ekki sögu um breytinguna. Í skýrslunni eru VSK-klausulýsingar prentaðar og birtar fyrir allar línur í skýrslunni ásamt VSK-upphæðinni og upphæð VSK-stofnsins. Ef VSK-klausa hefur ekki verið skilgreind fyrir neinar línur í söluskjalinu er öllum hlutanum sleppt þegar skýrslan er prentuð.

### <a name="to-set-up-vat-clauses"></a>Að setja upp VSK-ákvæði

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 9.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Á **VSK ákvæði** síðunni, skal búa til nýja línu.  
3. Í reitnum **Kóði** er auðkenni ákvæðisins slegið inn. Þessi kóði er notuð til að úthluta ákvæðinu á VSK-bókunarflokka.  
4. Í reitnum **Lýsing** er færður inn texti VSK-undanþágu sem þú vilt að birtist á fylgiskjölum sem geta innihaldið VSK. Í reitinn **Lýsing 2** skal færa inn meiri texta ef þörf krefur. Textinn verður sýndur á nýjum skjalalínum.
5. Veldu aðgerðina **Lýsing eftir gerð skjals**.
6. Á síðunni **VSK-klausur eftir skjalagerð** skal fylla í reitina til að setja upp hvaða texta VSK-undanþágu á að birta fyrir hvaða skjalagerð.  
7. Valfrjálst: Til að úthluta VSK-ákvæði til VSK-bókunaruppsetningar strax, veljið **Uppsetning**, og velja síðan ákvæðið. Ef þú vilt bíða, er hægt að úthluta ákvæðinu síðar á síðunni **VSK-Bókunaruppsetning**.  
8. Valfrjálst: Til að tilgreina hvernig skal þýða VSK-ákvæðið er **Þýðingar** aðgerðin valin.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Til að úthluta VSK-ákvæði til VSK-bókunaruppsetningar

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 10.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.  
2. Í dálkinum **VSK-Ákvæði** skal velja ákvæðið sem nota á fyrir hvert VSK-bókunaruppsetningu sem það á við um.  

### <a name="to-specify-translations-for-vat-clauses"></a>Að tilgreina þýðingar fyrir VSK-ákvæði

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 11.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Þýðingar**.  
3. Í reitnum **Tungumálakóði** skal velja tungumál sem þýtt er yfir á.  
4. Í reitunum **Lýsing** og **Lýsing 2** eru færðar inn þýðingar á lýsingunum. Þessi texti er birtur í þýddum VSK-skýrsluskjölum.  

### <a name="to-specify-extended-text-for-vat-clauses"></a>Til að tilgreina lengdan texta fyrir VSK-klausur

> [!NOTE]  
> Ef landið eða svæðið þitt krefst lengri texta fyrir VSK-klausur en sjálfgefna útgáfan styður er hægt að tilgreina lengri texta fyrir VSK-klausur sem *lengri texti* þannig að hann prentist á sölu- og innkaupaskýrslur.  

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 11.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Lengdir textar**.  
3. Valið er aðgerðin **Nýtt**.  
4. Fyllt er í reitina **Tungumálakóði** og **Lýsing**.  
5. Frjálst er að velja reitinn **Allir tungumálakóðar** eða tilgreina viðeigandi tungumál í reitnum **Tungumálakóði** ef þú notar tungumálakóða.  
6. Reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út ef afmarka á tímabil fyrir lengdan texta.  
7. Í línunum **Texti** skaltu skrifa lengri texta fyrir VSK-klausur.  
8. Veldu viðeigandi reiti fyrir skjalategundir sem á að prenta lengda textann á.  
9. Loka síðunni.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Stofna VSK-bókunaruppsetningu til að sjá um VSK vegna Innflutnings

Aðgerðin *VSK vegna innflutnings* er notuð þegar á að bóka fylgiskjal þar sem öll upphæðin er VSK. Þetta þarf að gera ef reikningur kemur frá skattyfirvöldum fyrir VSK á innfluttar vörur.  

Til að setja upp kóða fyrir VSK vegna innflutnings, skal fylgja þessum skrefum:  

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 12.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-vörubókunarflokk** og velja síðan viðkomandi tengil.  
2. Á síðunni VSK-vörubókunarflokkar, skal setja upp nýja VSK-vörubókunarflokkur fyrir VSK vegna innflutnings.  
3. Veldu ![peruna sem opnar Segðu mér eiginleikann 13.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.  
4. Á síðunni VSK-bókunaruppsetning skal stofna nýja lína, eða nota VSK-viðskiptabókunarflokk sem fyrir er í samsetningu með nýja VSK-vörubókunarflokknum fyrir VSK vegna innflutnings.  
5. Í reitnum **SK-Útreikningstegund** skal velja **Fullur VSK**.  
6. Í **VSK-sölureikningur** reitinn skal færa inn fjárhagsreikningurinn sem á að nota til að bóka VSK vegna innflutnings. Allir aðrir reikninga eru valfrjáls.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Nota bakfærðan VSK fyrir viðskipti milli ESB-landa eða svæða

Sum fyrirtæki verða að nota bakfærðan VSK þegar þau eiga viðskipti við önnur fyrirtæki. Reglan gildir til dæmis fyrir innkaup frá ESB-löndum/svæðum og sölu til ESB-landa/svæða.  

> [!NOTE]  
> Þessi regla á við þegar skipt er við fyrirtæki sem eru skráð VSK-skyld í öðrum ESB-löndum/svæðum. Ef skipt er beint við viðskiptamenn í öðrum ESB-löndum/svæðum ætti að hafa samband við skattayfirvöld til að fá upplýsingar um viðeigandi VSK-reglur.  

> [!TIP]  
> Þú getur staðfest að fyrirtæki sé skráð sem virðisaukaskattsskylt í öðru ESB landi/svæði með því að nota þjónustu ESB VSK Registration Number Validation. Þjónustan er tiltæk án endurgjalds í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Staðfesta VSK-skráningarnúmer](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Sala til ESB-landa eða svæða

VSK er ekki reiknaður af sölu til virðisaukaskattskyldra fyrirtækja í öðrum ESB löndum/svæðum. Tilkynna þarf virði sölu til ESB-landa/svæða sérstaklega á VSK-yfirlitinu.  

Til að reikna VSK rétt fyrir sölu til ESB-landa/ svæða ætti að:  

* Setja upp línu fyrir sölu með sömu upplýsingum fyrir innkaup. Ef línur eru þegar uppsettar í glugganum **VSK-bókunargrunnur** fyrir innkaup frá ESB-löndum/-svæðum er einnig hægt að nota línurnar fyrir sölu.  
* Úthluta VSK-viðskiptabókunarflokkunum í reitnum **VSK viðsk.bókunarflokkur** á flýtiflipanum **Reikningar** í viðskiptamannaspjöldum ESB-viðskiptamanna. Einnig ætti að færa inn VSK-númer viðskiptamannsins í reitnum **VSK-númer** á flýtiflipanum **Erlent**.  

Þegar sala til viðskiptamanns í öðru ESB-landi/svæði er bókuð er VSK-upphæðin reiknuð og VSK-færsla með upplýsingum um bakfærðan VSK og VSK-stofn (upphæðina sem notuð er til að reikna VSK-upphæðina) stofnuð. Engar færslur eru bókaðar í VSK-reikningana í fjárhagnum.

Ef þú vilt nota samsetningu virðisaukaskattsfyrirtækjabókunarhóps og VSK vörubókunarflokks til að tilkynna sem þjónustu í reglubundnum virðisaukaskattsskýrslum skaltu merkja við **ESB Þjónusta** reitinn.

> [!NOTE]  
> Reiturinn **ESB-þjónusta** á aðeins við um virðisaukaskattsskýrslur. Reiturinn er ekki tengdur **Þjónustuyfirlýsingunni** eða **Intrastat fyrir þjónustu** eiginleikunum.

## <a name="vat-rounding-for-documents"></a>VSK-sléttun fyrir fylgiskjöl

Upphæðir í fylgiskjölum sem ekki hafa verið bókaðar eru sléttaðar og birtar á þann hátt sem samsvarar lokasléttun upphæða sem búið er að bóka. VSK er reiknaður fyrir heilt skjal, sem þýðir að VSK sem er reiknaður í fylgiskjali er byggður á summu allra lína með sama VSK-kenni í skjalinu.  

## <a name="set-up-vat-reporting"></a>Setja upp VSK-skýrslur

Setja verður upp upplýsingar um hvernig skattayfirvöld í landinu eða svæðinu þínu krefjast þess að þú sendir inn VSK-skýrslur. Eftirfarandi skref sýna algengustu upplýsingarnar. Hins vegar gæti verið þörf á öðrum skrefum í þínu landi eða á þínu svæði. Frekari upplýsingar er að finna í viðeigandi greind í hlutanum *Staðbundin virkni* á svæðinu vinstra megin.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Sjá einnig .

[Uppsetning á sniðmáti VSK-yfirlits og heiti VSK-yfirlits](finance-how-setup-vat-statement.md)  
[Setja upp óinnleystan virðisaukaskatt](finance-setup-unrealized-vat.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Unnið með breytingaverkfæri VSK-hlutfalls](finance-how-use-vat-rate-change-tool.md)  
[Staðfesta VSK-skráningarnúmer](finance-how-validate-vat-registration-number.md)  
[Staðbundin virkni í Business Central](about-localization.md)  
[VSK-skýrslur í þýsku útgáfunni](LocalFunctionality/Germany/vat-reporting.md)  
[Belgískur VSK](LocalFunctionality/Belgium/belgian-vat.md)  
[Ítalskur VSK](LocalFunctionality/Italy/italian-vat.md)  
[Setja upp rafrænan VSK og ICP-yfirlýsingar í hollensku útgáfunni](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[VSK-skýrslur í spænsku útgáfunni](LocalFunctionality/Spain/vat-reports.md)  
[Setja upp bókun á vöru- og þjónustuskatti í áströlsku útgáfunni](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[VSK í tékknesku útgáfunni](LocalFunctionality/Czech/finance-vat.md)  
[VSK-skýrslur í norsku útgáfunni](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Skráning vöru- og þjónustuskatts og samræmds söluskatts í Kanada](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
