---
title: Setja upp virðisaukaskatt
description: 'Ganga úr skugga um að rétt reikna, bóka, og tilkynna á VSK vegna sölu eða innkaup. Mælt er með að nota uppsetningarleiðsögn til að setja upp VSK.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Setja upp útreikninga og bókunaraðferðir fyrir virðisaukaskatt

Neytendur og fyrirtæki greiða virðisaukaskatt (VSK) þegar þau kaupa vörur eða þjónustu. Upphæð VSK til greiðslu getur verið mismunandi, það fer eftir nokkrum þáttum. Í [!INCLUDE[prod_short](includes/prod_short.md)], setur þú upp VSK til að tilgreina taxtana til að nota til að reikna skattaupphæðir, byggt á eftirfarandi færibreytum:

* Hverjum selt er  
* Hverjum keypt er af  
* Það sem er selt  
* Hvað keypt er  

Hægt er að setja upp VSK-útreikning handvirkt, en það getur verið bæði snúið og tímafrekt. Auðvelt er að nota mismunandi VSK-verð fyrir misgáning og búa til ónákvæmar VSK-skýrslur. Til að auðvelda VSK er mælt með því að nota leiðsagnarforritið **UPPSETNING VSK-uppsetningar** .

Eigi hinsvegar sjálfur að setja upp VSK-útreikninga eða fræðast um hvert þrep inniheldur þessi grein lýsingar á hverju verkstigi.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## Setja upp VSK með leiðbeiningum um uppsetningu með hjálp (ráðlagt)

> [!NOTE]
> Aðeins er hægt að nota **leiðbeiningar um VSK-uppsetningar** ef fyrirtækið Mitt hefur *verið stofnað* og ekki hafa verið bókaðar færslur sem innihalda VSK. Til að fræðast meira um Fyrirtækið mitt er farið í [Stofna ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).

Til að ræsa uppsetningleiðbeiningar með hjálp, fylgið þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið og sláðu inn **Uppsetning með hjálp**. 
2. Veldu **Setja upp virðisaukaskatt (VSK)** og ljúktu við skrefin.
3. Þegar uppsetningu með aðstoð hefur verið lokið er farið á **síðuna VSK-bókunargrunnur** til að kanna hvort fylla þurfi út fleiri reiti í samræmi við staðbundnar kröfur í útgáfu notandans [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna á [Staðbundin virkni í Business Central](about-localization.md)  

### Skoða VSK-bókunargrunninn

Til að styðja við fljótlega byrjun tilkynnir [!INCLUDE [prod_short](includes/prod_short.md)] þér um fjárhagsreikninga sem vantar í bókunarflokka eða bókunargrunna, eins og á síðunni **VSK-bókunargrunnur**. Hægt er að kveikja eða slökkva á þessari tilkynningu með því að nota **fjárhagsreikninginn sem vantar í bókunarflokk eða uppsetningartilkynningu** á síðunni **Mínar tilkynningar** . Farðu bara á **stillingarsíðuna mínar** og veldu **svo tengilinn Breyta þegar ég fæ tilkynningar** .  

Ef tilkynningin [!INCLUDE [prod_short](includes/prod_short.md)]  er valin stofnar bókunargrunnur á grundvelli bókunarflokkanna í fylgiskjalinu eða færslubókinni sem verið er að vinna með.  

Á þessum tímapunkti geturðu bara fyllt út í fjárhagsreikningana sem vantar. En þegar uppsetningin er fínstillt enn frekar síðar gæti verið ljóst að upphafleg uppsetningin er röng. [!INCLUDE [prod_short](includes/prod_short.md)] leyfir ekki að VSK-bókunargrunni og almennum bókunargrunni sé eytt eftir að þær hafa verið notaðar til að stofna færslur. Til að koma í veg fyrir að fólk noti ranglega uppsetningu sem ekki á lengur við fyrir nýjar bókanir er hægt að nota reitinn **Lokað** á síðunni **Alm. bókunargrunnur** .

## Setja upp sjálfgefna VSK-dagsetningu fyrir skjöl og færslubækur

VSK-skýrslugerð í [!INCLUDE [prod_short](includes/prod_short.md)] byggir á að **VSK-dagsetning** innihaldi VSK-færslur í VSK-skýrslum á VSK-tímabili. Hægt er að breyta VSK-dagsetningunni á öllum skjölum og færslubókum en tilgreina verður sjálfgefið gildi fyrir VSK-dagsetninguna.

> [!NOTE]
> Þegar fylgiskjal eða færslubók **hefur verið bókuð birtist VSK-dagsetningin** í **VSK-færslum** og fjárhagsfærslum **sem og** á bókaða fylgiskjalinu ef til er.

Til að setja upp sjálfgefið gildi fyrir VSK-dagsetningu þarf að fylgja þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Í flýtiflipanum **Almennt**, í reitnum **Sjálfgefinn VSK-dagsetning**, skaltu velja annaðhvort **Bókunardagsetning** eða **Dagsetning skjals**.
3. Loka síðunni.  

> [!NOTE]
> Sjálfgefið er að **Sjálfgefin VSK-dagsetning** sé **Bókunardagsetning**.

### Aðgerðin VSK-dagsetning virk eða óvirk

Sum lönd/svæði krefjast þess að fyrirtæki noti tiltekna VSK-dagsetningu en önnur lönd/svæði ekki. Í sumum löndum/svæðum þurfa einnig fyrirtæki að breyta VSK-dagsetningunni þegar þau bóka skjöl en önnur lönd/svæði leyfa ekki breytingar á VSK-dagsetningum. Til að leyfa mismunandi samhengi er hægt að velja hvort nota eigi þessa aðgerð og, ef svo er, að hvaða marki.

Til að setja upp stig notkunar VSK-dagsetninga skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á flýtiflipanum **Almennt**, í reitnum **Notkun** VSK-dags. er tilgreint að hve langan tíma á að nota aðgerðina VSK-dagsetning. Hægt er að velja um einn af eftirfarandi valkostum:

   | Gerð | Heimildasamstæða |
   |--------------------|-----------------------------------------|
   | **Nota alla VSK-dagsetningaraðgerðina** | Allt sem tengist VSK-dagsetningu **virkar sjálfgefið og þannig er hægt að** nota hámarks **VSK-dagsetningaraðgerð** . Hægt er að setja upp dagsetninguna, breyta henni í fylgiskjölum, tilkynna út frá henni og breyta dagsetningunni eftir bókun svo lengi sem tímabilið er ekki lokað eða varið með leyfilegum dagsetningum til bókunar. |
   | **Nota en leyfa ekki breytingar** | Allt sem tengist **VSK-dagsetningu** er sjálfgefið með einni undantekningu. Ekki er hægt að breyta VSK-dagsetningunni **í** **VSK-færslum**. |
   | **Aðgerðin VSK-dagsetning ekki notuð** | [!INCLUDE [prod_short](includes/prod_short.md)] felur og gerir reitina **VSK-dagsetning** ekki tiltæka í fylgiskjölum, færslubókum og færslum.  **Sjálfgefin VSK-dagsetning** er grunnstillt sem **Bókunardagsetning**. |

3. Loka síðunni.

> [!IMPORTANT]
> Jafnvel þótt valkosturinn **Vsk-dagsetningar sé** ekki notaður [!INCLUDE [prod_short](includes/prod_short.md)]  notar **VSK-dagsetning** í bakgrunni.  **Þar sem sjálfgefin VSK-dagsetning** er grunnstillt sem **bókunardagsetning** og því er ekki hægt að breyta í þessu tilviki verður sama reynsla og án þessarar aðgerðar. **VSK-dagsetningarreitirnir** verða fjarlægðir af öllum síðum en þessi reitur er enn til í töflum og skýrslur munu vinna eftir honum.

### Takmarka tímabil við bókun og breyta VSK-dagsetningu

Hægt er að koma í veg fyrir að fólk bóki eða breyti VSK-færslum á tilteknum tímabilum. Takmörkunin er stillt með tveimur stillingum:

* Byggt á lokuðu **VSK-vöruskilatímabili**
* Á grundvelli reitanna **Bókun leyfð frá** og **Leyfa bókun á** .

#### Takmarka bókun byggða á tímabili VSK-vöruskila

1.  ![Veldu Lightbulb sem opnar TellF Me eiginleika 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á flýtiflipanum **Almennt**, í reitnum **Stjórna VSK-tímabili**, er tilgreint gráðu í eftirliti VSK-vöruskilatímabils. Eftirfarandi tafla lýsir valkostunum.

| Gerð | Heimildasamstæða |
|--------------------|-----------------------------------------|
| **Loka bókun innan lokaðs og vara við útgefnu tímabili** | Koma í veg fyrir að fólk bóki fylgiskjal eða færslubók eða breytingum á VSK-færslum með VSK-dagsetningu innan lokaðs **VSK-vöruskilatímabils**. [!INCLUDE [prod_short](includes/prod_short.md)] Einnig birtist viðvörun ef **VSK-vöruskilatímabilið** er opið en staða VSK-vöruskila **er** **Útgefin** eða **Send**. |
| **Loka bókun innan lokaðs tímabils** | Koma í veg fyrir að fólk bóki fylgiskjal eða færslubók eða breytingum á VSK-færslum með VSK-dagsetningu innan lokaða **VSK-skilatímabilsins**. |
| **Vara við bókun á lokuðu tímabili** | Sýna aðvörun en loka ekki á bókun ef bóka á fylgiskjal eða færslubók með VSK-dagsetningu innan lokaðs **VSK-vöruskilatímabils**. |
| **Fatlaður** | Framkvæma engar aðgerðir byggðar á lokuðu **VSK-skilatímabili**. |

#### Takmarka bókun byggða á Leyfa frá/til tímabili

> [!NOTE]
> Stýringin breytist frá og með Business Central útgáfu 23.1. Í fyrri útgáfum var aðeins ein stýring á síðunni **Fjárhagsgrunnur** fyrir bæði bókunardagsetningu og VSK-dagsetningu. Nú er þessum stýringum skipt þannig að stjórnin á síðunni **Fjárhagsgrunnur** er aðeins fyrir **bókunardagsetninguna** og stýring á síðunni **VSK-uppsetning** er aðeins fyrir **VSK-dagsetninguna** . Einnig eru nýjar dagsetningarstýringar á síðunni **Notandauppsetning** .  

##### Útgáfa 23.1 eða nýrri

> [!IMPORTANT]
> Þegar uppfært er í nýja umbreytingu skal hafa í huga að gildi eru uppfærð í nýju **Vsk-dags. frá/til** á **síðunni VSK-uppsetning** sem byggð eru á gildunum í **Bókun leyfð frá/til** í **fjárhagsgrunninum**. Ef nota á mismunandi dagsetningarstýringar er síðan VSK-uppsetning **opnuð** og breytingar gerðar.  

Hægt er að setja upp takmarkanir á fyrirtækinu eða á tilteknum notendastigum.

Til að takmarka allar bókanir fyrir allt fyrirtækið:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **VSK-grunn** og velja síðan viðeigandi tengil.  
2. Á flýtiflipanum **VSK-dags** . í reitnum **Leyfa VSK-dags** . frá skal tilgreina VSK-dagsetninguna sem hægt er að bóka. Bókun fylgiskjals eða færslubókar með VSK-dagsetningu fyrir þessa dagsetningu er ekki leyfð.  
3. Á flýtiflipanum **VSK-dags** . í reitnum **Leyfa VSK-dags** . er tilgreind VSK-dagsetningin sem hægt er að bóka til. Bókun fylgiskjals eða færslubókar með VSK-dagsetningu eftir þessa dagsetningu er ekki leyfð. 

Til að takmarka bókanir tiltekins notanda:  

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Notandauppsetning** og velja síðan viðeigandi tengil.  
2. Í reitnum **Kenni notanda** er tilgreindur sá notandi sem hefur heimild til að bóka á tilteknu tímabili.  
3. Í reitnum **Leyfa VSK-dags. frá** skal tilgreina VSK-dagsetninguna sem hægt er að bóka frá. Bókun fylgiskjals eða færslubókar með VSK-dagsetningu fyrir þessa dagsetningu er ekki leyfð. 
4. Í reitnum **Leyfa VSK-dags. til** skal tilgreina VSK-dagsetninguna sem hægt er að bóka til. Bókun fylgiskjals eða færslubókar með VSK-dagsetningu eftir þessa dagsetningu er ekki leyfð.  

##### Útgáfur fyrir 23.1 

Hægt er að setja upp takmörkun á fyrirtækinu eða tilteknum notendastigum.

Til að takmarka allar bókanir fyrir allt fyrirtækið:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á flýtiflipanum **Almennt**, í reitnum **Bókun leyfð frá**, er tilgreind VSK-dagsetningin sem hægt er að bóka frá. Bókun fylgiskjals eða færslubókar með VSK-dagsetningu fyrir þessa dagsetningu er ekki leyfð.  
3. Á flýtiflipanum **Almennt**, í reitnum **Bókun leyfð til**, er tilgreind VSK-dagsetningin sem hægt er að bóka til. Bókun fylgiskjals eða færslubókar með VSK-dagsetningu eftir þessa dagsetningu er ekki leyfð.

Til að takmarka bókanir tiltekins notanda:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.  
2. Í reitnum **Kenni notanda** er tilgreindur sá notandi sem leyfir að bóka á tilteknu tímabili.  
3. Í reitnum **Bókun leyfð frá** er tilgreind VSK-dagsetningin sem hægt er að bóka frá. Bókun fylgiskjals eða færslubókar með VSK-dagsetningu fyrir þessa dagsetningu er ekki leyfð.
4. Í reitnum **Bókun leyfð til er tilgreind VSK-dagsetningin sem hægt er að** bóka til. Bókun fylgiskjals eða færslubókar með VSK-dagsetningu eftir þessa dagsetningu er ekki leyfð.

## Setja upp VSK-númer fyrir landið/svæðið

Til að tryggja að fólk færi inn gild VSK-númer er hægt að skilgreina snið FYRIR VSK-númer sem notuð eru í þeim löndum/svæðum sem notandi á viðskipti í. [!INCLUDE[prod_short](includes/prod_short.md)] birtir villuboð ef einhver gerir mistök eða notar rangt snið fyrir landið/svæðið.

Til að setja upp VSK-númer skal fylgja eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lönd/svæði**.
2. Velja skal landið eða svæðið og svo agðerðina **Snið VSK-númers**.
3. Í reitnum **Snið** skal skilgreina sniðin með því að slá inn einn eða fleiri eftirfarandi stafa:  

* **#** Krefst númers sem er ein tala.  
* **@** Krefst stafs. Þetta snið er ekki hástafað.  
* **?** Leyfir hvaða staf sem er.  

    > [!TIP]
    > Hægt er að nota þessa stafi svo framarlega sem þeir eru alltaf til staðar í sniði landsins eða svæðisins. Ef taka þarf með tímabil eða bandstrik milli tölusetta er hægt að skilgreina sniðið sem ##.####.### eða @@-###-###.  

## Setja upp VSK-viðskiptabókunarflokka

VSK-viðskiptabókunarflokkar á að tákna markaðina þar sem þú stundar viðskiptum við viðskiptamenn og lánardrottna, og tilgreina hvernig á að reikna og bóka VSK á sérhverjum markaði. Dæmi um VSK viðskiptabókunarflokka eru **Innanlands** og **Evrópusambandið (ESB)**.  

Nota skal kóða sem auðvelt er að muna og er auðkennandi fyrir viðskiptaflokkinn, til dæmis **ESB**, **Ekki-ESB**, eða **Innlent**. Hver kóti verður að vera einstakur, þ.e. hægt er að setja upp eins marga kóta og þörf krefur, en ekki er hægt að hafa sama kótann oftar en einu sinni í töflu.

Til að setja upp VSK-viðskiptabókunarflokk er þessu skrefum fylgt:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleika 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-viðskiptabókunarflokka** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

Hægt er að setja upp sjálfgefna VSK-viðskiptabókunarflokka með því að tengja þá við almenna viðskiptabókunarflokka. [!INCLUDE[prod_short](includes/prod_short.md)] úthlutar sjálfkrafa VSK-viðskiptabókunarflokkinum þegar þú úthlutar viðskiptabókunarflokki til viðskiptamanns, lánardrottins eða fjárhagsreiknings.

## Uppsetning VSK-vörubókunarflokka

VSK-vörubókunarflokkar tákna þær vörur og tilföng sem þú kaupir eða selur, og ákvarða hvernig skal reikna út og bóka VSK eftir tegund vöru eða tilfangs.

Mælt er með því að nota kóta sem auðvelt er að muna og lýsa hlutfallinu, t.d **. ÁN-VSK** eða **Núll**, **VSK10** eða **Lækkað** fyrir 10 prósent VSK og **VSK25** eða **Staðlað** fyrir 25 prósent.

Til að setja upp VSK-viðskiptabókunarflokk er þessu skrefum fylgt:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleika 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-vörubókunarflokk** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

## Sameina VSK-bókunarflokka og VSK-bókunaruppsetningar

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar VSK-upphæðir í sölu og innkaup á grundvelli VSK-bókunaruppsetninga, sem eru samsetningar VSK-viðskipta- og vörubókunarflokka. Fyrir hverja samsetningu geturðu valið VSK-prósenta, VSK-útreikningstegund, og fjárhagsreikninga fyrir bókun VSK sem tengist sölu, innkaupum, og bakfærðum gjöldum. Einnig er hægt að tilgreina hvort endurreikna skal VSK þegar greiðsluafsláttur er veittur eða fenginn.  

Hægt er að setja upp ótakmarkaðan fjölda samsetninga. Til að flokka samsetningar VSK-bókunargrunns með svipuðum eigindum er kenni **VSK skilgreint** fyrir hvern flokk og kenni úthlutað á meðlimi flokksins.  

> [!NOTE]
>  **Vsk-kenni** er kóti sem hægt er að nota til að flokka svipaða eiginleika. Mælt er með að notuð séu mismunandi VSK-kenni fyrir mismunandi VSK-prósentur.  

Til að sameina VSK-bókunaruppsetningar skal fylgja eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 5.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Úthluta VSK-bókunarflokkum sjálfvirkt til fjölda eininga

Eigi að beita sömu VSK-bókunarflokkum á fjölda eininga, er hægt að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] sem gerir það sjálfvirkt.

* Hægt er að úthluta VSK-viðskiptabókunarflokkum til almennra viðskiptabókunarflokka eða sniðmáta viðskiptamanna eða lánardrottna.
* Hægt er að úthluta VSK-vörubókunarflokkum í almenna vörubókunarflokka.  

VSK-viðskipta- eða vörubókunarflokki er úthlutað þegar valið er viðskipta- eða vörubókunarflokki fyrir viðskiptamann, lánardrottinn, vöru eða tilföng.

## Úthluta VSK-bókunarflokka á reikninga, viðskiptamenn, lánardrottna, vörur og tilföng

Eftirfarandi hlutar útskýra hvernig á að úthluta VSK-bókunarflokkum til einstakra einingar.

### Hvernig á að úthluta VSK-bókunarflokkum til einstakra fjárhagsreikninga

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 6.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Opna **Fjárhagsreikningur** spjaldið fyrir reikninginn.  
3. Á **Bókun** Flýtiflipanum, í **Alm. bókunartegund** reitnum, er valið annaðhvort **Sölu** eða **Innkaupa**.  
4. Velja skal VSK-bókunarflokkana til að nota fyrir sölureikninginn eða kaupreikninginn.  

### Að úthluta VSK-viðskiptabókunarflokkum til viðskiptamenn og lánardrottna.

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 7.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinur** eða **Lánardrottinn** og velja síðan viðkomandi tengil.  
2. Á **Viðskiptamaður** eða **Lánardrottinn** spjaldinu, víkið flýtiflipann **Reikningar**.  
3. Veljið VSK-viðskiptabókunarflokkana.  

### Til að úthluta VSK-vörubókunarflokkar til einstakra vörur og tilföng.

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 8.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vara** eða **Tilfang** og velja síðan viðkomandi tengil.  
2. Framkvæmdu eitt af eftirfarandi skrefum:  

    * Á **Vöru** spjaldinu, stækkið **Verð & Bókun** Flýtiflipann, og velja síðan **Sýna fleiri** til að birta **VAT Vörubókunarflokkur** reitinn.  
    * Á **Tilfang** spjaldinu, stækkið **Reikningagerð** flipann.  
3. Veljið VSK-vörubókunarflokk.  

## Setja upp klausur til að útskýra VSK-undanþágu eða óafgreiðanlega VSK-taxta

VSK-klausa er sett upp til að lýsa upplýsingum um hvaða tegund VSK er notuð. Stjórnvöld geta krafist þessara upplýsinga. Þegar VSK-klausa hefur verið sett upp og hún tengd VSK-bókunargrunni birtist VSK-klausan á prentuðum söluskjölum sem nota uppsetningu VSK-bókunarflokksins.

Ef með þarf er einnig hægt að tilgreina hvernig skal þýða VSK ákvæði yfir á öðrum tungumálum. Þegar söluskjal með VSK-kenni er stofnað og prentað er fylgiskjalið með umreiknaða VSK-klausunni. Tilgreindur tungumálakóðinn á viðskiptamannaspjaldinu ákvarðar tungumálið.

Þegar utanbirgða VSK-taxtar eru notaðir í mismunandi tegundum fylgiskjala, svo sem reikningum eða kreditreikningum, gæti þurft að hafa undanþágutexta (VSK-klausu). Undanþágutextinn segir til um hvers vegna reiknuð var lækkuð VSK eða VSK-hlutfall núll. Hægt er að skilgreina mismunandi VSK-klausur til að hafa með á viðskiptaskjölum fyrir hverja tegund fylgiskjals á síðunni **VSK-klausur eftir tegund** fylgiskjals.

Hægt er að breyta eða eyða VSK-klausu og breytingarnar birtast í skýrslu sem er búin til. Hins vegar [!INCLUDE[prod_short](includes/prod_short.md)]  heldur ekki sögu breytinganna. Í skýrslunni eru VSK-klausulýsingar prentaðar og birtar fyrir allar línur í skýrslunni ásamt VSK-upphæðinni og upphæð VSK-stofnsins. Ef VSK-klausa er ekki skilgreind fyrir neinar línur í söluskjalinu er öllum hlutanum sleppt þegar skýrslan er prentuð.

### Að setja upp VSK-ákvæði

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 9.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Á **VSK ákvæði** síðunni, skal búa til nýja línu.  
3. Í reitnum **Kóði** er auðkenni ákvæðisins slegið inn. Þessi kóði er notuð til að úthluta ákvæðinu á VSK-bókunarflokka.  
4. Í reitnum **Lýsing** er færður inn texti VSK-undanþágu sem þú vilt að birtist á fylgiskjölum sem geta innihaldið VSK. Í reitinn **Lýsing 2** skal færa inn meiri texta ef þörf krefur. Textinn birtist í nýjum línum skjals.
5. Veldu aðgerðina **Lýsing eftir gerð skjals**.
6. Á síðunni **VSK-klausur eftir skjalagerð** skal fylla í reitina til að setja upp hvaða texta VSK-undanþágu á að birta fyrir hvaða skjalagerð.  
7. Valfrjálst: Til að úthluta VSK-ákvæði til VSK-bókunaruppsetningar strax, veljið **Uppsetning**, og velja síðan ákvæðið. Ef þú vilt bíða, er hægt að úthluta ákvæðinu síðar á síðunni **VSK-Bókunaruppsetning**.  
8. Valfrjálst: Til að tilgreina hvernig skal þýða VSK-ákvæðið er **Þýðingar** aðgerðin valin.

### Til að úthluta VSK-ákvæði til VSK-bókunaruppsetningar

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 10.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.  
2. Í dálkinum **VSK-Ákvæði** skal velja ákvæðið sem nota á fyrir hvert VSK-bókunaruppsetningu sem það á við um.  

### Að tilgreina þýðingar fyrir VSK-ákvæði

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 11.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Þýðingar**.  
3. Í reitnum **Tungumálskóti** er valið tungumálið sem verið er að þýða á.  
4. Í reitunum **Lýsing** og **Lýsing 2** eru færðar inn þýðingar á lýsingunum. Þessi texti er birtur í þýddum VSK-skýrsluskjölum.  

### Til að tilgreina lengdan texta fyrir VSK-klausur

> [!NOTE]  
> Ef landið eða svæðið þitt krefst lengri texta fyrir VSK-klausur en sjálfgefna útgáfan styður er hægt að tilgreina lengri texta fyrir VSK-klausur sem *lengri texti* þannig að hann prentist á sölu- og innkaupaskýrslur.  

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 11.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-ákvæði** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Lengdir textar**.  
3. Valið er aðgerðin **Nýtt**.  
4. Fyllt er í reitina **Tungumálakóði** og **Lýsing**.  
5. Frjálst er að velja reitinn **Allir tungumálakóðar** eða tilgreina viðeigandi tungumál í reitnum **Tungumálakóði** ef þú notar tungumálakóða.  
6. Reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út ef afmarka á tímabil fyrir lengdan texta.  
7. Í línunum **Texti** skaltu skrifa lengri texta fyrir VSK-klausur.  
8. Veldu viðeigandi reiti fyrir skjalategundir sem á að prenta lengda textann á.  
9. Loka síðunni.  

## Stofna VSK-bókunaruppsetningu til að sjá um VSK vegna Innflutnings

Aðgerðin *Flytja inn VSK* er notuð þegar bóka þarf fylgiskjal þar sem öll upphæðin er VSK. Þessi aðgerð er notuð ef móttekinn er reikningur frá skattayfirvöldum vegna VSK fyrir innfluttar vörur.  

Til að setja upp kóða fyrir VSK vegna innflutnings, skal fylgja þessum skrefum:  

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 12.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-vörubókunarflokk** og velja síðan viðkomandi tengil.  
2. Á síðunni VSK-vörubókunarflokkar, skal setja upp nýja VSK-vörubókunarflokkur fyrir VSK vegna innflutnings.  
3.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 13.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-bókunargrunnur** og velja síðan viðkomandi tengil.  
4. Á síðunni VSK-bókunaruppsetning skal stofna nýja lína, eða nota VSK-viðskiptabókunarflokk sem fyrir er í samsetningu með nýja VSK-vörubókunarflokknum fyrir VSK vegna innflutnings.  
5. Í reitnum **SK-Útreikningstegund** skal velja **Fullur VSK**.  
6. Í **VSK-sölureikningur** reitinn skal færa inn fjárhagsreikningurinn sem á að nota til að bóka VSK vegna innflutnings. Allir aðrir reikninga eru valfrjáls.  

## Nota bakfærðan VSK fyrir viðskipti milli ESB-landa/svæða

Sum fyrirtæki verða að nota bakfærðan VSK þegar þau eiga viðskipti við önnur fyrirtæki. Reglan gildir til dæmis fyrir innkaup frá ESB-löndum/svæðum og sölu til ESB-landa/svæða.  

> [!NOTE]  
> Þessi regla á við þegar skipt er við fyrirtæki sem eru skráð VSK-skyld í öðrum ESB-löndum/svæðum. Ef skipt er beint við viðskiptamenn í öðrum ESB-löndum/svæðum ætti að hafa samband við skattayfirvöld til að fá upplýsingar um viðeigandi VSK-reglur.  

> [!TIP]  
> Hægt er að staðfesta að fyrirtæki sé skráð sem VSK-skyld í öðru ESB-landi/svæði með því að nota þjónustuna ESB-VSK-númer staðfesting. Þjónustan er tiltæk án endurgjalds í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Staðfesta VSK-skráningarnúmer](finance-how-validate-vat-registration-number.md).

### Sala til ESB-landa/svæða

VSK er ekki reiknaður á sölu til VSK-skyldra fyrirtækja í öðrum ESB-löndum/svæðum. Tilkynna þarf virði sölu til ESB-landa/svæða sérstaklega á VSK-yfirlitinu.  

Til að reikna VSK rétt fyrir sölu til ESB-landa/ svæða ætti að:  

* Setja upp línu fyrir sölu með sömu upplýsingum fyrir innkaup. Ef settar eru upp línur á síðunni **VSK-bókunargrunnur** fyrir innkaup frá ESB-löndum/svæðum er einnig hægt að nota þessar línur fyrir sölu.  
* Úthluta VSK-viðskiptabókunarflokkunum í reitnum **VSK viðsk.bókunarflokkur** á flýtiflipanum **Reikningar** í viðskiptamannaspjöldum ESB-viðskiptamanna. Einnig ætti að færa inn VSK-númer viðskiptamannsins í reitnum **VSK-númer** á flýtiflipanum **Erlent**.  

Þegar sala til viðskiptamanns í öðru ESB-landi/svæði [!INCLUDE [prod_short](includes/prod_short.md)]  er bókuð reiknar VSK-upphæðina og stofnar VSK-færslu samkvæmt upplýsingum um bakfærðan VSK og VSK-stofn. Þessi upphæð er notuð til að reikna VSK-upphæðina. Engar færslur eru bókaðar í VSK-reikningana í fjárhagnum.

Ef nota á samsetningu VSK-viðskiptabókunarflokks og VSK-vörubókunarflokks fyrir skýrslugerð sem þjónustu í tímabils VSK-skýrslum er reiturinn ESB-þjónusta **merktur** .

> [!NOTE]  
> Reiturinn **ESB-þjónusta** á aðeins við um VSK-skýrslur. Þessi reitur tengist ekki aðgerðunum **Þjónustuskýrsla** eða **Intrastat for Services** .

## VSK-sléttun fyrir fylgiskjöl

Upphæðir í fylgiskjölum sem ekki eru bókaðar eru sléttaðar og birtar til samræmis við lokasléttun upphæða sem eru bókaðar. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar VSK fyrir allt fylgiskjalið. VSK-útreikningurinn byggist á samtölu allra lína með sama VSK-kenni í fylgiskjalinu.  

## Setja upp VSK-skýrslur

Setja verður upp upplýsingar um hvernig skattayfirvöld í landinu eða svæðinu þínu krefjast þess að þú sendir inn VSK-skýrslur. Eftirfarandi skref sýna algengustu upplýsingarnar. Hins vegar krefst landið eða svæðið önnur skref. Frekari upplýsingar er að finna í viðeigandi greind í hlutanum *Staðbundin virkni* á svæðinu vinstra megin.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## Sjá einnig .

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
