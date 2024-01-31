---
title: Um umreikning staðalkostnaðar
description: Í kerfi staðalkostnaðar er kostnaðarverð birgða ákvarðað á grundvelli ásættanlegs eða viðbúins kostnaðar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
ms.service: dynamics-365-business-central
---
# Um umreikning staðalkostnaðar

Mörg framleiðslufyrirtæki velja matsgrundvöll staðlaðs kostnaðarverðs. Þetta á einnig við fyrir fyrirtæki sem framkvæma létta framleiðslu, til dæmis samsetningu og röðun í sett. Í stöðluðu kostnaðarverðskerfi er kostnaðarverð birgða ákvarðað á grundvelli einhvers ásættanlegs eða viðbúins kostnaðar. Rannsóknir á fyrri kostnaði og áætluðum framtíðarkostnaði  geta skapað grundvöllinn fyrir stöðluðu kostnaðarverði. Þessi kostnaður er frystur þar til ákvörðun er tekin um að breyta honum. Raunverulegur kostnaður við framleiðslu afurðar getur verið frábrugðinn áætluðum stöðluðum kostnaði. Raunverulegi kostnaðurinn er borinn saman við staðlað kostnaðarverð tiltekinnar vöru og munur á þeim eða *frávik* eru fundin og greind til að auðvelda stjórnun.  

Hægt er að viðhalda stöðluðum kostnaði fyrir vörur fyllt er á með innkaupum, samsetningu og framleiðslu. Fyrir hverja áfyllingaraðferð, getur staðlaður kostnaður samanstaðið af eftirfarandi einingum.  

|Áfyllingarkerfið|Staðlaðir kostnaðarliðir|  
|--------------------------|----------------------------|  
|**Innkaup**|Beinn efniskostnaður og kostnaður við efniskostnað ef þess er krafist.|  
|**Samsetning**|Beinn efniskostnaður er beinn eða fastur vinnukostnaður og sameiginlegur kostnaður.|  
|**Framl.pöntun**|Beinn efniskostnaður,vinnukostnaður, undirverktakakostnaður og sameiginlegur kostnaður.|  

## Uppsetning staðlaðs kostnaðarverðs

Þar sem staðlað kostnaðarverðframleiddrar eða samsettrar vöru getur samanstaðið af mörgum kostnaðarliðum, þar með talið efnis-, afkastagetu- (vinnu-) og undirverktakakostnaði (beinum og sameiginlegum), þarf að búa til staðlað kostnaðarverð fyrir hvern þessara liða.  

Bókhaldsverkhluti vöruvinnslufyrirtækis sem notar staðlaðan kostnaðarútreikning er:  

- Áætla staðlað kostnaðarverð fyrir fullunna vöru og setja á birgðarspjaldið.  
- Skrá skal og ráðstafa raunverulegum kostnaði aðalkostnaðarliða og gera frávikum rétt skil.  

Telja þarf saman allan íhlutakostnaðinn til að ákvarða beinan kostnað fullunninnar vöru. Samsett eða framleidd vara getur falið í sér undirsamsetningar, sem einnig samanstanda af mörgum íhlutum.  

Eftirfarandi lykilkostnaðarliðir mynda samtölu beins kostnaðar vöru sem er fullunnin:  

- Efniskostnaður.  
- Getukostnaður  
- Undirverktakakostnaður fyrir framleiddar vörur eingöngu.  

### Efniskostnaður

Efniskostnaður er kostnaður sem tengist undirsamsetningum og aðkeyptum hráefnum. Efniskostnaðarverð getur samanstaðið af beinum og óbeinum kostnaðarliðum.  

- Beinn efniskostnaður er reikningsfærð upphæð fyrir aðkeypt hráefni eða framleiðslukostnaður undirsamsetningar.  
- Óbeinn efniskostnaður eða  *rekstrarkostnaður* getur táknað þætti eins og flutningskostnað birgða fyrir tilbúna vöru eftir að hún hefur verið framleidd.  

Uppsetning efniskostnaðar keyptra vara sem hafa áhrif á beinan og óbeinan kostnað veltur á því hvaða kostnaðaraðferð er valin fyrir vöruna sem er tilgreind. Kostnaðarupplýsingar fyrir aðra hvora aðferð kostnaðarútreiknings eru settar upp. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

Kostnaður við rýrnun (aðeins framleiðsla) er annar Stuðull til að hafa í huga þegar reiknaður er heildarefniskostnaður. Þegar vissu magni af hráefni er hent við það að setja saman eða framleiða vöru verður það yfirleitt til þess að meira magn af íhlutum þarf til að framleiða þá vöru. Það eykur svo efniskostnað þeirra íhluta sem eru notaðir við framleiðslu yfirvöru. Úrkastskostnaður efnis er settur upp á annað hvort framleiðsluuppskriftinni eða -leiðinni.  

Hægt er að setja efniskostnað framleiddrar vöru fram á tvo vegu sem samsvara eftirfarandi útreikningsgrundvöllum staðlaðs kostnaðarverðs:  

|Grunnur fyrir útreikning kostnaðarverðs|Útreikningur efniskostnaðar|  
|----------------------------|-------------------------------|  
|Eitt stig|Framleidd vara er jöfn heildarkostnaði allra keyptra eða undirsamsettra vara í framleiðsluuppskrift vörunnar.|  
|Samantekið stig eða mörg stig|Framleidd vara er samtala efniskostnaðar fyrir allar undirsamsetningar á uppskrift þeirrar vöru og kostnaðar allra aðkeyptra vara á framleiðsluuppskrift þeirrar vöru.|  

### Getukostnaður

Getukostnaður er sá kostnaður sem er tengdur við kostnað við innanhússvinnuafl og vélar. Setja verður upp kostnað fyrir sérhvern forða (í samsetningarstjórnun) og verk eða vélastöð á leið (í framleiðslu). Eins og með efni er hægt að finna bæði beina og óbeina kostnaðarliði getu. Til dæmis getur Beinn kostnaður vinnustöðvar verið stofngengi sem stofnað er til til að framkvæma tiltekna aðgerð. Óbeinn kostnaður fyrir vinnustöð getur staðið undir einhverjum almennum verksmiðjukostnaði, svo sem lýsingu, hitun og þess háttar. Hægt er að setja sameiginlegan getukostnað fram sem óbeina kostnaðarprósentu eða fastan taxta sameiginlegs kostnaðar, svipað og með efniskostnað.  

Uppsetning getukostnaðar á samsettum vörum samanstendur af eftirfarandi liðum:  

- Beint og óbeint kostnaðarverð forða.  
- Föst eða bein forðanotkunartegund.  

Uppsetning getukostnaðar á framleiddum vörum samanstendur af eftirfarandi liðum:  

- Beint og óbeint kostnaðarverð véla- eða vinnustöðvar.  
- uppsetning tíma og lotustærðar  

Framleiðslufyrirtæki þarf framleiðslufyrirtæki að koma á fót þeim stöðluðu tímahröðum sem eru nauðsynlegir til að framkvæma aðgerðir í véla- og vinnustöðvum til að geta reiknað út staðlaðan getukostnað. Heildartíminn sem það tekur að ljúka við aðgerð samanstendur yfirleitt af uppsetningar- og keyrslutíma, auk bið- og færslutíma.  

Hraði hverrar tímagerðar fyrir hverja vél eða vinnustöð er settur upp á sérstakri leið.  

> [!NOTE]  
>  Keyrslutímahraði gildir fyrir hverja vörueiningu sem framleidd er, en uppsetningartímahraði gildir fyrir hverja lotu. Þess vegna þarf að deila leiðaruppsetningartíma hverrar aðgerðar yfir lotustærðina. Lotustærðin er tilgreind í samsvarandi reit í flýtiflipanum **Áfylling** á síðunni **Birgðaspjald**.  

Til að tilgreina uppsetningartíma á leiðinni fyrir áætlun en ekki taka þessi útgjöld með í stöðluðum kostnaðarútreikningi skal hreinsa reitinn **Kostnaður með uppsetningu** á flýtiflipanum **Almennt á síðunni Framleiðsluuppsetning**.  

Á eins stigs grundvelli er þetta sá vinnukostnaður sem þarf til að framleiða fullunnu framleiðsluvöruna og er tilgreint á leið framleiðsluvörunnar. Á margra stiga grundvelli er þetta afkastakostnaðurinn sem er tilgreindur fyrir hverja framleidda vöru á uppskrift yfirvörunnar.  

### Undirverktakakostnaður

Undirverktakakostnaður er sá kostnaður sem er tengdur við þjónustu sem utanaðkomandi birgjar og undirverktakar bjóða upp á. Svipað og með efni og afkastagetu kann undirverktakakostnaður að samanstanda af bæði beinum og sameiginlegum upphæðum. Beinn undirverktakakostnaður felur í sér raunverulegt gjald fyrir hverja veitta þjónustueiningu. Til dæmis getur kostnaður undirverktaka fyrir kostnað fyrir flutning og umsjón með kostnaði verið í fyrirtækinu með undisamið pöntun.  

Þar sem undirverktakastarfsemi færsla á afkastagetu út fyrir fyrirtækið er kostnaðurinn við þjónustu undirverktaka (beinn og óbeinn) settur upp á vinnustöðvarspjaldinu sem stendur fyrir undirverktakaaðgerðina.  

## Uppfærsla staðlaðs kostnaðarverðs

Til að uppfæra eða reikna staðlað kostnaðarverð fyrir samsetningarvörur er aðgerðin notuð af birgðaspjaldinu.  

Ferlið til að uppfæra eða reikna út staðlaðan kostnað samanstendur yfirleitt af eftirfarandi verkum:  

1.  Uppfærslu kostnaðar á íhluta- og afkastagetustigunum. Frekari upplýsingar, sjá **Leggja til staðlaðan vörukostnað** og **Leggja til staðlaðan afkastakostnað** runuvinnslurnar.  
2.  Samstilling og samantekt íhluta- og afkastakostnaðarins til að reikna út heildarframleiðslukostnað varanna. Nánari upplýsingar er að finna í [Að reikna út staðalkostnað á samsetningaríhlut](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Innleiðing staðlaðs kostnaðar sem færður var inn þegar fyrri keyrsla var keyrð. Staðallinn kostnaður tekur ekki gildi fyrr en þau eru útfærð. Notaðu runuvinnsluna **Innleiða breytingu á stöðluðu kostnaðarverði**, sem uppfærir breytingar á staðalkostnaði á vörum með þeim sem er í töflunni vinnublað staðlaðs kostnaðarverðs.  
4.  Innleiðing breytinga til að uppfæra reitinn **Kostn.verð** á birgðaspjaldinu og framkvæmd endurmats á birgðum. Nánari upplýsingar eru í [Endurmat birgða](inventory-how-revalue-inventory.md).

## Nota runuvinnslur til að uppfæra staðalkostnað
Í eftirfarandi köflum er lýst runuvinnslum sem hægt er að nota til að uppfæra staðalkostnað.
### Leggja til staðalkostnað vöru

 Býr til tillögur um breytingar á kostnaði og kostnaðarhlutdeild staðalkostnaðar á birgðaspjöldum. Þegar keyrslunni er lokið er hægt að sjá niðurstöðuna í glugganum Vinnublað staðlaðs kostnaðarverðs.

> [!NOTE]  
> Þessi keyrsla er eingöngu ætluð fyrir keypta vöru. Ef uppfæra á vöru með framleiðsluuppskrift eða samsetningaruppskrift verður fyrst að fylla út vinnublaðið með öllum íhlutunum og keyra síðan keyrsluna taka saman staðlað kostnaðarverð.

Keyrslan býr aðeins til tillögur. Það innleiða ekki þær breytingar sem lagðar eru til. Ef tillögurnar eru fullnægjandi og eiga að innleiða þær, þ.e. uppfæra þær á birgðaspjöldin og setja þær inn í endurmatsbókina, þá skal velja innleiða breytingar á stöðluðu kostnaðarverði í glugganum Vinnublað staðlaðs kostnaðarverðs.
#### Valkostir

**Staðlaður kostnaður** : færður inn Leiðréttingarstuðull sem á að nota til að uppfæra staðalkostnaðinn. Einnig er hægt að velja sléttunaraðferð fyrir nýja staðlaða kostnaðinn. Fylla verður út í svæðið með aukastöfum fyrir prósentuhækkun, til dæmis 1,1.

**Óbeinn kostnaður%** : færður er inn leiðréttingarstuðullinn sem á að nota til að uppfæra óbeina kostnaðinn%. Einnig er hægt að velja sléttunaraðferð fyrir nýja óbeina kostnaðar%. Fylla verður út í svæðið með aukastöfum fyrir prósentuhækkun, til dæmis 1,1.

**Hlutfall** sameiginlegs kostnaðar: Færa skal inn leiðréttingarstuðulinn sem á að nota til að uppfæra hlutfall sameiginlegs kostnaðar. Einnig er hægt að velja sléttunaraðferð fyrir nýtt hlutfall sameiginlegs kostnaðar. Fylla verður út í svæðið með aukastöfum fyrir prósentuhækkun, til dæmis 1,1.

### Leggja til staðalkostn. vinnu-/vélast.

Stofnar tillögur um breytingar á kostnaði og kostnaðarhlutdeild staðalkostnaðar vinnustöðvar, vélastöðvar eða forðaspjöld. Þegar keyrslunni er lokið er hægt að sjá niðurstöðuna í  **glugganum Vinnublað**  staðlaðs kostnaðarverðs.

Keyrslan býr aðeins til tillögur. Það innleiða ekki þær breytingar sem lagðar eru til. Ef tillögurnar eru fullnægjandi og koma á þeim í framkvæmd, þ.e. uppfæra þær á vinnu-/vélastöð-og forðaspjöldum og setja þau inn í gluggann endurmatsbókin, þá er valið  **innleiða breytingar**  á stöðluðu kostnaðarverði í  **glugganum Vinnublað**  staðlaðs kostnaðarverðs.

Þegar keyrslan er keyrð og óskað er eftir að skoða áhrif á framleiðslu eða samsetningardeildir þá keyrir  **keyrslan rúlla upp staðlað kostnaðarverð**  til að uppfæra staðalkostnað á vinnustöðvar, vélastöðvar, samsetningaraðföng, framl. uppskriftir og samsetningaruppskriftir.
#### Valkostir
**Staðlaður kostnaður** : færður inn Leiðréttingarstuðull sem á að nota til að uppfæra staðalkostnaðinn. Einnig er hægt að velja  **sléttunaraðferð**  fyrir nýja staðlaða kostnaðinn. Fylla verður út í svæðið með aukastöfum fyrir prósentuhækkun, til dæmis 1,1.

**Óbeinn kostnaður%** : færður er inn leiðréttingarstuðullinn sem á að nota til að uppfæra óbeina kostnaðinn%. Einnig er hægt að velja sléttunaraðferð fyrir nýja óbeina kostnaðar%. Fylla verður út í svæðið með aukastöfum fyrir prósentuhækkun, til dæmis 1,1.

**Hlutfall** sameiginlegs kostnaðar: Færa skal inn leiðréttingarstuðulinn sem á að nota til að uppfæra hlutfall sameiginlegs kostnaðar. Einnig er hægt að velja sléttunaraðferð fyrir nýtt hlutfall sameiginlegs kostnaðar. Fylla verður út í svæðið með aukastöfum fyrir prósentuhækkun, til dæmis 1,1.

### Bóka birgðakostnað í fjárhag

 Skráir magn og virði breytinga í birgðir í birgðafærslum og virðisfærslum þegar birgðafærslur eru bókaðar, svo sem sölusendingar eða innkaupamóttökur.

Ef gátreiturinn Sjálfvirk kostnaðarbókun  **er valinn**  í  **glugganum Birgðagrunnur**  er birgðakostnaður ekki skráður breytilegur í fjárhag, og Kostnaðarauki er ekki reiknaður með sölu. Þess vegna þarf að bóka í fjárhag handvirkt með því að keyra  **keyrsluna Bóka birgðakostnaður**  við til að uppfæra fjárhag og hugsanlega prenta skýrslu um virðisfærslurnar sem eru bókaðar.

Keyrslan notar virðisfærslur sem grundvöll hennar. Til að reikna virði þess sem á að bóka notar hann mismuninn milli  **reitsins Kostnaðarupphæð (raunverul**  .)  **og**  kostnaðarbókaðs í fjárhag í virðisfærslunum. Ef gátreiturinn áætluð kostnaðarbókun  **var valinn**  í  **glugganum Birgðagrunnur**  mun keyrslan einnig bóka mismuninn  **á reitnum Kostnaðarupphæð (Væntanlegt)**  og  **exp. kostnaður bókaður í**  fjárhag í bráðabirgðareikningum í fjárhag.

> [!NOTE]
> Ef gátreiturinn áætluð kostnaðarbókun  **hefur ekki verið valinn**  í  **glugganum Birgðagrunnur**  mun Síðasti kafli skýrslunnar skrá virðisfærslur sem er sleppt vegna þess að þeir standa fyrir áætluðum kostnaði.

> [!NOTE] 
> Ef runuvinnslan felur í sér villu sem varðar uppsetningu vídda eða víddar, þá hnekkir keyrslan villuna og bókar færslunni í fjárhag með víddum virðisfærslunnar.

Ef ganga á úr skugga um að runuvinnslan rekist ekki á villur er hægt að keyra  **keyrsluna Post Invt. Kostnaður við fjárhags-prófunarskýrslu**  til að sjá allar villur sem gætu komið upp. Síðan er hægt að lagfæra villurnar og keyra  **keyrsluna Bóka birgðakostnaður við**  og vita að það vinnur úr öllum færslum.
 
> [!IMPORTANT]  
> Áður en þessi keyrsla er notuð ætti að keyra  **keyrsluna Leiðr. kostn. birgðafærslur** . Þetta tryggir að kostnaður sem er bókaður í Fjárhag verði leiðréttur þegar þessi keyrsla er keyrð.
#### Valkostir

|Valkostur  |Heimildasamstæða  |
|--------------|---------|
|**Bókunaraðferð**|Keyrslan getur annað hvort bókað birgðavirði í fjárhag fyrir hvern bókunarflokk eða hverja bókaða færslu. Ef bókað er á hverja færslu fæst nákvæm sundurliðun á því hvaða áhrif birgðir hafa á fjárhag, en einnig margar fjárhagsfærslur. Ef bókað er á hvern bókunarflokk stofnar keyrslan fjárhagsfærslu fyrir hverja bókunardagsetningu á hverja bókunarflokkasamsetningu. Það merkir að fjárhagsfærslan er stofnuð fyrir hverja samsetningu bókunardagsetninga, almenna viðskiptabókunarflokka, almenna framleiðslubókunarflokka, birgðabókunarflokka og staðsetningarkóta. Að auki stofnar runuvinnslan aðskildar fjárhagsfærslur fyrir kostnað með mismunandi formerki.|
|**Fylgiskjal nr.**|Í þennan reit má tilgreina fylgiskjalsnúmer ef aðgerðin Bóka eftir birgðabókunarflokki var valin. Númer fylgiskjals birtist í bókuðum færslum.|
|**Færsla**|Veljið þetta svæði ef óskað er eftir að keyrslan bóki sjálfkrafa í fjárhag. Ef ekki er valið að bóka birgðakostnaður í fjárhag prentast aðeins prófunarskýrsla sem sýnir gildin sem hægt er að bóka fjárhag, og í skýrslunni birtast:  **Prófunarskýrsla (ekki bókuð)**.|

### Leggja saman staðl. kostnaðarv.

Veltir upp stöðluðum kostnaði samsettra og framleiddra vara. Þær hafa áhrif á breytinguna á stöðluðum kostnaði íhluta sem lagðir eru til við  **keyrsluna Leggja til staðlað kostnaðarverð**  vöru. Að auki eru þau áhrif breytinga á stöðluðum kostnaði á framleiðslugetu og samsetningu forða  **sem keyrslan leggja til staðlað kostnaðarverð**  vinnu/vélastöðvar leggur til.

Þegar búið er að keyra annaðhvort eða báðar þessar runuvinnslur og rúllan er keyrð eru allar breytingar á stöðluðu kostunum á vinnublaðinu kynntar í tengdri framleiðslu eða samsetningu uppskrifta og kostnaður er notaður á hverju UPPSKRIFTARSTIGI.

> [!NOTE] 
> Þessi aðgerð rúllar aðeins staðalkostnaðinum á birgðaspjöldin, ekki á BIRGÐASPJÖLDIN.

Keyrslan býr aðeins til tillögur. Það innleiða ekki þær breytingar sem lagðar eru til. Ef tillögurnar eru fullnægjandi og koma á þeim í framkvæmd, þ.e. uppfæra þær á birgðaspjöldin og setja þær inn í  **gluggann endurmatsbókaráætlun**, þá er hægt að nota  **keyrsluna Innleiða breytingu**  á stöðluðu kostnaðarverði. Keyrslan er notuð úr  **glugganum Vinnublað**  staðlaðs kostnaðarverðs.
#### Valkostir

**Dagsetning** útreikninga: færð er inn dagsetningin sem á við útgáfu FRAMLEIÐSLUUPPSKRIFTARINNAR sem á að gera rúlluna til.
 
### Innleiða breytingu á stöðluðu kostnaðarverði

Uppfærir breytingar á stöðluðum kostnaði í  **töflunni Vara**  með þeim í  **töflunni vinnublað**  staðlaðs kostnaðarverðs. Hægt er að stofna breytingatillögur staðlaðs kostnaðarverðs með  **keyrslunni Leggja til staðlað kostnaðarverð**  vöru og/eða tillögugerð  **vinnu-/**  vélastöðvar og einnig er hægt að breyta þeim. Efni allra reitanna í breytingatillögunum um staðlað kostnaðarverð er flutt. Þegar tillögur um breytingar eru gerðar á stöðluðum kostnaði er hægt að skoða þær á birgðaspjaldinu og/eða á vinnu-/vélastöðspjöldin. Einnig er stofnuð endurmatsbók til að uppfæra virði fyrirliggjandi birgða.
#### Valkostir

**Bókunardags**.: Hér er færð inn dagsetningin þegar endurmat á að fara fram.

**Númer** fylgiskjals: Hér er færð inn tala endurmatsbókarlínanna. Ef það er númeraröð sem er sett upp í keyrsluheiti birgðabókar fylgir númer fylgiskjals þeim færslum sem bókaðar eru í endurmatsbókina. Annars er hægt að rita númer handvirkt.

**Sniðmát** birgðabókar: Hér er fært inn heiti sniðmáts fyrir endurmatsbókina.

**Heiti** birgðabókarkeyrslu: Hér er skráð heiti raunverulegrar endurmatsbókar

Velja  **í lagi**  til að ræsa runuvinnsluna. Ef ekki á að keyra runuvinnsluna núna skal velja  **Hætta**  við til að loka glugganum.

## Sjá einnig .

[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  
[Uppfæra staðlaðan kostnað](finance-how-to-update-standard-costs.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
