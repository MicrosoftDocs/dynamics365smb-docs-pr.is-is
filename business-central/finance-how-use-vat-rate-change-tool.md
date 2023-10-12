---
title: Stjórna breytingum VSK-hlutfalls
description: Kynntu þér hvernig þú notar breytingarverkfæri VSK-hlutfalls fyrir Dynamics 365 Business Central til að breyta VSK-taxta í samræmi við löggjöf á staðnum.
author: andregu
ms.topic: conceptual
ms.reviewer: bholtorf
ms.workload: na
ms.search.keywords: 'VAT, VAT rate, posting, tax, value-added tax'
ms.search.form: '550,'
ms.date: 06/16/2021
ms.author: andregu
---

# <a name="managing-vat-rate-changes"></a>Stjórna breytingum VSK-hlutfalls

VSK-hlutfall er mismunandi eftir gildandi lögum. Allar breytingar á VSK hafa áhrif á gögnin þín í [!INCLUDE[prod_short](includes/prod_short.md)] hvort VSK-hlutfallið er lækkað, hækkað eða fjarlægt. VSK er tengdur mörgum einingum í [!INCLUDE[prod_short](includes/prod_short.md)], svo sem viðskiptavinum, lánardrottnum, vörum, tilföngum, kostnaðarauka og fjárhagsreikningum. Breytingar á VSK-hlutföllum gerast yfirleitt á tiltekinni dagsetningu, en eftir dagsetninguna verður að breyta uppsetningu VSK, bókunarflokkum o.s.frv. til að ganga úr skugga um að nýjar sölupantanir og innkaupapantanir séu stofnaðar með nýja VSK-hlutfallinu.

## <a name="changing-vat-rates"></a>Breyta VSK-hlutfalli

Besta leiðin til að stjórna breytingu á VSK-hlutfalli er að bóka og loka alveg opnum pöntunum og öðrum fylgiskjölum dagsettum fyrir dagsetningu breytingar á VSK, til að ganga úr skugga um að breytingin hafi ekki áhrif á slíkt. Slíkt er auðveldasta aðferðin til að þú getir stofnað nýjar pantanir og skjöl með nýja VSK-hlutfallinu.

Eftirfarandi aðferð er ráðlögð til að stjórna breytingu á VSK-hlutfalli

1. Bóka og loka alveg opnum pöntunum, færslubókum og öðrum fylgiskjölum fyrir dagsetningu breytingarinnar. Hægt er að bíða fram yfir dagsetningu breytingarinnar svo framarlega að ekki hafi verið bætt við nýjum línum og gengið er úr skugga um að gildisdagsetningin verði á undan skiptidagsetningunni.  
2. Stofna nýja VSK-uppsetningu.  
3. Framkvæmið breytinguna á VSK á einingum (viðeigandi viðskiptavinum, lánardrottnum, vörum o.s.frv.).  
4. Eftir dagsetningu breytingar á VSK stofnar þú ný skjöl sem nota nýja hlutfallið.  


> [!NOTE]  
> Þessa stundina er verið að uppfæra breytingarverkfæri VSK-hlutfalls. Virknin sem minnst er á hér á eftir passar hugsanlega ekki við virkni í umhverfinu þínu. Uppfærslan mun fara fram fyrir 1. júlí 2020 og verður ekki venjuleg mánaðarleg uppfærsla. Þess í stað verða öll umhverfi uppfærð sjálfkrafa (bráðabót). Þegar þessari uppfærslu er lokið birtast þessi skilaboð ekki lengur.  

## <a name="the-vat-rate-change-tool"></a>Notkun breytingaverkfæris VSK-hlutfalls

Breytingarverkfæri VSK-hlutfalls getur hjálpað til við umbreytingu á VSK-hlutföllum í aðalgögnum, færslubókum og pöntunum, að einhverju leyti. Þetta er gagnlegt ef óskað er eftir að umreikna VSK í aðalgögnum á auðveldan hátt eða ef þú hefur pantanir sem þú getur ekki lokað á undan dagsetningu breytingarinnar og verða unnar yfir lengri tíma og fara fram yfir dagsetningu breytingar á VSK-hlutfalli. Tilteknar afmarkanir og takmarkanir á breytingaverkfæri VSK-hlutfalls eiga við.

## <a name="understanding-the-vat-rate-conversion-process-and-limitations"></a>Að skilja umbreytingarferli VSK-hlutfalls og takmarkanir þess

VSK-hlutfall breytingarverkfærið umreiknar VSK-hlutfall fyrir aðalgögn, færslubækur og pantanir á mismunandi hátt. Valin aðalgögn og færslubækur verða uppfærð af nýja almenna vörubókunarflokknum eða VSK-vörubókunarflokki. Ef pöntun hefur verið afhent að fullu eða að hluta munu afhentar vörur halda almenna vörubókunarflokknum eða VSK-vörubókunarflokknum. Ný pöntunarlína verður stofnuð fyrir óafhentar vörur og uppfærð til að samræma núverandi og nýtt VSK eða almenna vörubókunarflokka. Úthlutanir kostnaðarauka, grunnstillingarsniðmát fyrir vörur, frátekningar og vörurakningarupplýsingar uppfærast einnig í samræmi við það. 

Í pöntunarlínum verður einingarverðið uppfært fyrir allar línur af gerðinni Vara og Tilfang ef notað er verð með VSK fyrir vöruna. Fyrir aðrar línugerðir er hægt að ákveða hvort uppfæra eigi einingarverðið eða ekki.

Það eru nokkrir hlutir sem verkfærið getur ekki umbreytt:

* Sölu-eða innkaupapöntunum og reikningum þar sem sendingar hafa verið bókaðar. Þessi skjöl eru bókuð með gildandi VSK-hlutfalli.  
* Skjölum sem hafa bókaða fyrirframgreiðslureikninga. Til dæmis gæti notandi hafa greitt eða móttekið fyrirframgreiðslur á reikningum sem eru ekki loknir áður en breytingaverkfærið VSK-hlutfall er notað. Í þessu tilviki verður mismunur á vsk sem er á gjalddaga og vsk sem hefur verið borgaður í fyrirframgreiðslum þegar reikningnum er lokið. Breytingarverkfæri VSK-hlutfalls sleppir þessum skjölum og það þarf að uppfæra þau handvirkt.  
* Sölu- eða innkaupapöntunum með samhæfingu vöruhúsa ef þær eru að hluta sendar eða mótteknar.  
* Beinar sendingar.
* Sérpantanir. 
* Samsetningpantanir.
* Þjónustusamninga.  
* Kreditreikningar.
* Skilapantanir.
* Verð á vörum (aðalgögn)
* Verð á söluverði (aðalgögn)
* Viðskiptabókunarflokkar fyrir viðskiptavini og lánardrottna.

### <a name="to-prepare-vat-rate-change-conversions"></a>Til að undirbúa umreikning VSK-hlutfalls

Áður en breytingaverkfæri VSK-hlutfalls er sett upp þarf að velja úr eftirfarandi.

* Ef mismunandi hlutföll eru notuð í færslum þarf að búa til nýjar fjárhagsreikninga fyrir hvert hlutfall eða nota gagnaafmarkanir til að flokka færslur eftir hlutfalli.  
* Ef stofnaðir eru nýir fjárhagsreikningar þarf að stofna nýja almenna bókunarflokka.  
* Til að fækka fylgiskjölum sem er breytt skal bóka eins mörg fylgiskjöl og mögulegt er og halda óbókuðum skjölum í lágmarki.  
* Taka öryggisafrit af gögnum.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Til að setja upp breytingaverkfæri VSK-hlutfalls

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á Breyting á VSK-hlutfalli** og velja síðan viðkomandi tengil.  
2. Á flýtiflipunum **Aðalgögn**, **Færslubækur** og **Skjöl** skal velja gildi bókunarflokks af valkostalistanum fyrir nauðsynlega reiti. Í hverjum flokki er hægt að velja hvort eigi að umbreyta VSK-vörubókunarflokkum eða almennum vörubókunarflokkum eða umbreyta báðum gildunum ef þau eru tiltæk í aðalgagnavörunni. Fyrir sum svæði er einnig hægt að setja afmörkun til að umbreyta aðeins hlutmengi gildanna, til dæmis fjárhagsreikningum. 
3. Á flýtiflipanum **Verð með VSK** skaltu velja hvaða línugerðir á pöntunum sem skal uppfæra einingaverð. Einingaverð í línum af gerð vöru og tilfanga verða alltaf uppfærð.

### <a name="to-set-up-product-posting-group-conversion"></a>Til að setja upp vörubókunarflokksumbreytingar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á Breyting á VSK-hlutfalli** og velja síðan viðkomandi tengil.  
2. Á síðunni **Uppsetning á breytingu VSK-hlutfalls** skal annaðhvort velja aðgerðina **Umreikna VSK-vörubókunarflokk** eða **Umreikna almennan vörubókunarflokk**.  
3. Í reitnum **Frá kóða** er færður inn núverandi bókunarflokkur.  
4. Í reitnum **Til kóða** er færður inn nýr bókunarflokkur.  

### <a name="to-perform-vat-rate-change-conversion"></a>Til að umreikna VSK-hlutfall

Breytingarverkfæri VSK-hlutfalls er notað til að stjórna breytinum á stöðluðu VSK-hlutfalli. VSK og útreikningar almenns vörubókunarflokks eru notaðir til að breyta VSK-hlutfalli og viðhalda nákvæmum VSK-skýrslum. Eftirfarandi breytingar eru gerðar, allt eftir uppsetningu:  

* VSK og almennum bókunarflokkum er umbreytt.  
* Breytingar eru innleiddar í fjárhagsreikninga, viðskiptamenn, lánardrottna, opin skjöl, bókarlínum, o.s.frv.  

> [!IMPORTANT]  
> Áður en þú umreiknar VSK-hlutfallsbreytingu, er hægt að prófa umreikninginn. Til að gera það, skal fylgja eftirfarandi skrefum, en vertu viss um að hafa auða gátreitina **Framkvæma umreikning** og **VSK hlutfall breytingarverkfæri lokið**. Við prófun á umreikningi er reiturinn **Umbreytt** í töflu **Breyting á VSK gengi í skráningarfærslu** hreinsað og reiturinn **Umbreytt dagsetning** í töflunni **Breyting á VSK gengi í skráningarfærslu** auður. Þegar umreikningnum er lokið, skal velja **Breytingaskrárfærslur fyrir VSK-hlutfall** til að skoða niðurstöður af prufuumreikningnum. Staðfesta hverja færslu áður en umreikningur er framkvæmdur. Sérstaklega skal staðfesta færslur sem nota eldra VSK-hlutfall.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Breyting á VSK-hlutfalli** og velja síðan tengilinn **Uppsetning á breytingu VSK-hlutfalls**.  
2. Staðfesta að VSK-vörubókunarflokksumbreytingar eða almennar vörubókunarflokksumbreytingar hafi þegar verið settar upp.  
3. Velja skal gátreitinn **Framkvæma umreikning**.  

    > [!IMPORTANT]  
    >  Hreinsa gátreitinn **breytingaverkfæri fyrir VSK gengi lokið**. Gátreiturinn er valinn sjálfvirkt þegar umreikningi vsk-stigs er lokið.  

4. Velja skal **Umreikna** aðgerðina.  
5. Þegar umreikningnum er lokið, skal velja aðgerðina **Breytingaskrárfærslur fyrir VSK-hlutfall** til að skoða niðurstöður umreiknings.  

> [!IMPORTANT]  
> Eftir prófun á umreikningi er reiturinn **Umbreytt** í töflu **Breyting á VSK gengi í skráningarfærslu** valinn og reiturinn **Umbreytt dagsetning** í töflunni **Breyting á VSK gengi í skráningarfærslu** sýnir umreiknuðu dagsetninguna.  

## <a name="see-also"></a>Sjá einnig .

[Setja upp virðisaukaskatt](finance-setup-vat.md)  
[Uppsetning á óinnleystum virðisaukaskatti](finance-setup-unrealized-vat.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Staðbundin virkni í Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
