---
title: Um umreikning staðalkostnaðar
description: Í kerfi staðalkostnaðar er kostnaðarverð birgða ákvarðað á grundvelli ásættanlegs eða viðbúins kostnaðar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
ms.service: dynamics-365-business-central
---
# <a name="about-calculating-standard-cost"></a>Um umreikning staðalkostnaðar

Mörg framleiðslufyrirtæki velja matsgrundvöll staðlaðs kostnaðarverðs. Þetta á einnig við fyrir fyrirtæki sem framkvæma létta framleiðslu, til dæmis samsetningu og röðun í sett. Í stöðluðu kostnaðarverðskerfi er kostnaðarverð birgða ákvarðað á grundvelli einhvers ásættanlegs eða viðbúins kostnaðar. Rannsóknir á fyrri kostnaði og áætluðum framtíðarkostnaði  geta skapað grundvöllinn fyrir stöðluðu kostnaðarverði. Þessi kostnaður er frystur þar til ákvörðun er tekin um að breyta honum. Raunkostnaður við framleiðslu vöru getur verið frábrugðinn áætluðu stöðluðu kostnaðarverði. Raunverulegi kostnaðurinn er borinn saman við staðlað kostnaðarverð tiltekinnar vöru og munur á þeim eða *frávik* eru fundin og greind til að auðvelda stjórnun.  

Hægt er að viðhalda stöðluðum kostnaði fyrir vörur fyllt er á með innkaupum, samsetningu og framleiðslu. Fyrir hverja áfyllingaraðferð, getur staðlaður kostnaður samanstaðið af eftirfarandi einingum.  

|Áfyllingarkerfið|Staðlaðir kostnaðarliðir|  
|--------------------------|----------------------------|  
|**Innkaup**|Beinn efniskostnaður og sameiginlegur efniskostnaður ef þess er krafist.|  
|**Samsetning**|Beinn efniskostnaður er beinn eða fastur vinnukostnaður og sameiginlegur kostnaður.|  
|**Framl.pöntun**|Beinn efniskostnaður,vinnukostnaður, undirverktakakostnaður og sameiginlegur kostnaður.|  

## <a name="setting-up-standard-costs"></a>Uppsetning staðlaðs kostnaðarverðs

Þar sem staðlað kostnaðarverðframleiddrar eða samsettrar vöru getur samanstaðið af mörgum kostnaðarliðum, þar með talið efnis-, afkastagetu- (vinnu-) og undirverktakakostnaði (beinum og sameiginlegum), þarf að búa til staðlað kostnaðarverð fyrir hvern þessara liða.  

Bókhaldsverkhluti vöruvinnslufyrirtækis sem notar staðlaðan kostnaðarútreikning er:  

- Áætla staðlað kostnaðarverð fyrir fullunna vöru og setja á birgðarspjaldið.  
- Skrá skal og ráðstafa raunverulegum kostnaði aðalkostnaðarliða og gera frávikum rétt skil.  

Telja þarf saman allan íhlutakostnaðinn til að ákvarða beinan kostnað fullunninnar vöru. Samsett eða framleidd vara getur falið í sér undirsamsetningar, sem einnig samanstanda af mörgum íhlutum.  

Eftirfarandi lykilkostnaðarliðir mynda samtölu beins kostnaðar vöru sem er fullunnin:  

- Efniskostnaður.  
- Getukostnaður  
- Undirverktakakostnaður fyrir framleiddar vörur eingöngu.  

### <a name="material-costs"></a>Efniskostnaður

Efniskostnaður er kostnaður sem tengist undirsamsetningum og aðkeyptum hráefnum. Efniskostnaðarverð getur samanstaðið af beinum og óbeinum kostnaðarliðum.  

- Beinn efniskostnaður er reikningsfærð upphæð fyrir aðkeypt hráefni eða framleiðslukostnaður undirsamsetningar.  
- Óbeinn efniskostnaður eða *sameiginlegur kostnaður* getur táknað einingar eins og birgðahaldskostnað fullunninnar vöru eftir að hún hefur verið framleidd.  

Uppsetning efniskostnaðar keyptra vara sem hafa áhrif á beinan og óbeinan kostnað veltur á því hvaða kostnaðaraðferð er valin fyrir vöruna sem er tilgreind. Kostnaðarupplýsingar fyrir aðra hvora aðferð kostnaðarútreiknings eru settar upp. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

Kostnaður úrkasts (aðeins framleiðsla) er annar stuðull sem taka skal tillit til þegar heildarefniskostnaður er reiknaður. Þegar vissu magni af hráefni er hent við það að setja saman eða framleiða vöru verður það yfirleitt til þess að meira magn af íhlutum þarf til að framleiða þá vöru. Það eykur svo efniskostnað þeirra íhluta sem eru notaðir við framleiðslu yfirvöru. Úrkastskostnaður efnis er settur upp á annað hvort framleiðsluuppskriftinni eða -leiðinni.  

Hægt er að setja efniskostnað framleiddrar vöru fram á tvo vegu sem samsvara eftirfarandi útreikningsgrundvöllum staðlaðs kostnaðarverðs:  

|Grunnur fyrir útreikning kostnaðarverðs|Útreikningur efniskostnaðar|  
|----------------------------|-------------------------------|  
|Eitt stig|Framleidd vara er jöfn heildarkostnaði allra keyptra eða undirsamsettra vara í framleiðsluuppskrift vörunnar.|  
|Samantekið stig eða mörg stig|Framleidd vara er samtala efniskostnaðar fyrir allar undirsamsetningar á uppskrift þeirrar vöru og kostnaðar allra aðkeyptra vara á framleiðsluuppskrift þeirrar vöru.|  

### <a name="capacity-costs"></a>Getukostnaður

Getukostnaður er sá kostnaður sem er tengdur við kostnað við innanhússvinnuafl og vélar. Setja verður upp kostnað fyrir sérhvern forða (í samsetningarstjórnun) og verk eða vélastöð á leið (í framleiðslu). Eins og með efni er hægt að finna bæði beina og óbeina kostnaðarliði getu. Til dæmis getur beinn kostnaður vinnustöðvar verið sá vinnutaxti sem búið er að framkvæma tiltekna aðgerð. Óbeinn kostnaður vinnustöðvar getur táknað nokkur almenn verksmiðjuútgjöld, svo sem lýsing, hitun og svo framleiðsla. Hægt er að setja sameiginlegan getukostnað fram sem óbeina kostnaðarprósentu eða fastan taxta sameiginlegs kostnaðar, svipað og með efniskostnað.  

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

### <a name="subcontractor-costs"></a>Undirverktakakostnaður

Undirverktakakostnaður er sá kostnaður sem er tengdur við þjónustu sem utanaðkomandi birgjar og undirverktakar bjóða upp á. Svipað og með efni og afkastagetu kann undirverktakakostnaður að samanstanda af bæði beinum og sameiginlegum upphæðum. Beinn undirverktakakostnaður felur í sér raunverulegt gjald fyrir hverja veitta þjónustueiningu. Undirverktakakostnaður sameiginlegs kostnaðar getur til dæmis táknað flutnings- og meðhöndlunarkostnað sem fyrirtækið verður fyrir með pöntun undirverktaka.  

Þar sem undirverktakastarfsemi færsla á afkastagetu út fyrir fyrirtækið er kostnaðurinn við þjónustu undirverktaka (beinn og óbeinn) settur upp á vinnustöðvarspjaldinu sem stendur fyrir undirverktakaaðgerðina.  

## <a name="updating-standard-costs"></a>Uppfærsla staðlaðs kostnaðarverðs

Til að uppfæra eða reikna staðlað kostnaðarverð fyrir samsetningarvörur er aðgerðin notuð af birgðaspjaldinu.  

Ferlið til að uppfæra eða reikna út staðlaðan kostnað samanstendur yfirleitt af eftirfarandi verkum:  

1.  Uppfærslu kostnaðar á íhluta- og afkastagetustigunum. Frekari upplýsingar, sjá **Leggja til staðlaðan vörukostnað** og **Leggja til staðlaðan afkastakostnað** runuvinnslurnar.  
2.  Samstilling og samantekt íhluta- og afkastakostnaðarins til að reikna út heildarframleiðslukostnað varanna. Nánari upplýsingar er að finna í [Að reikna út staðalkostnað á samsetningaríhlut](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Innleiðing staðlaðs kostnaðar sem færður var inn þegar fyrri keyrsla var keyrð. Staðlað kostnaðarverð tekur ekki gildi fyrr en það er innleitt. Notaðu runuvinnsluna **Innleiða breytingu á stöðluðu kostnaðarverði**, sem uppfærir breytingar á staðalkostnaði á vörum með þeim sem er í töflunni vinnublað staðlaðs kostnaðarverðs.  
4.  Innleiðing breytinga til að uppfæra reitinn **Kostn.verð** á birgðaspjaldinu og framkvæmd endurmats á birgðum. Nánari upplýsingar eru í [Endurmat birgða](inventory-how-revalue-inventory.md).

## <a name="use-batch-jobs-to-update-standard-costs"></a>Nota keyrslur til að uppfæra staðlað kostnaðarverð
Eftirfarandi hlutar lýsa keyrslunum sem hægt er að nota til að uppfæra staðlað kostnaðarverð.
### <a name="suggest-item-standard-cost"></a>Leggja til staðalkostnað vöru

 Stofnar tillögur um breytingar á kostnaði og kostnaðarhlutdeild staðlaðs kostnaðar á birgðaspjöldum. Að lokinni keyrslu má sjá niðurstöður úr glugganum Vinnublað staðlaðs kostnaðarverðs.

> [!NOTE]  
> Þessi keyrsla er eingöngu ætluð fyrir innkeyptar vörur. Ef uppfæra á vöru með framleiðsluuppskrift eða samsetningaruppskrift þarf fyrst að fylla út vinnublaðið með öllum íhlutunum og keyra síðan keyrsluna Leggja saman staðl. kostnaðarverð.

Keyrslan býr aðeins til tillögur. Hún framkvæmir ekki breytingarnar sem lagðar voru til. Ef tillögurnar eru fullnægjandi og koma á þeim í framkvæmd, það er að uppfæra þær á birgðaspjöldunum og setja þær inn í Endurmatsbókina, velja síðan Innleiða breytingar á stöðluðu kostnaðarverði í glugganum Vinnublað staðlaðs kostnaðarverðs.
#### <a name="options"></a>Valkostir

**Staðlað kostn.verð**: Færður er inn leiðréttingarstuðullinn sem á að nota til að uppfæra staðlað kostnaðarverð. Einnig er hægt að velja sléttunaraðferð fyrir nýja staðlaða kostnaðarverðið. Fylla þarf út reitinn með aukastöfum fyrir prósentuhækkunina, til dæmis 1,1.

**Óbein kostnaðar%**: Færa skal inn leiðréttingarstuðulinn sem á að nota til að uppfæra óbeina kostnaðar%. Einnig er hægt að velja sléttunaraðferð fyrir nýja óbeina kostnaðar%. Fylla þarf út reitinn með aukastöfum fyrir prósentuhækkunina, til dæmis 1,1.

**Hlutfall** sameiginlegs kostnaðar: Færður er inn leiðréttingarstuðullinn sem á að nota til að uppfæra hlutfall sameiginlegs kostnaðar. Einnig er hægt að velja sléttunaraðferð fyrir nýtt hlutfall sameiginlegs kostnaðar. Fylla þarf út reitinn með aukastöfum fyrir prósentuhækkunina, til dæmis 1,1.

### <a name="suggest-workmach-ctr-std-cost"></a>Leggja til staðalkostn. vinnu-/vélast.

Stofnar tillögur um breytingar á kostnaði og kostnaðarhlutdeild í stöðluðu kostnaðarverði á vinnustöð, vélastöð eða forðaspjöldum. Að lokinni keyrslu má sjá niðurstöður úr **glugganum Vinnublað** staðlaðs kostnaðarverðs.

Keyrslan býr aðeins til tillögur. Hún framkvæmir ekki breytingarnar sem lagðar voru til. Ef tillögurnar eru fullnægjandi og koma á þeim í framkvæmd, það er að uppfæra þær á vinnu-/véla- og forðaspjöldunum og setja þær inn í gluggann Endurmatsbók, skal velja **Innleiða breytingar á** stöðluðu kostnaðarverði í **glugganum Vinnublað** staðlaðs kostnaðarverðs.

Þegar keyrslan hefur verið keyrð og skoða á áhrifin á framleiðslu- eða samsetningardeildirnar er keyrslan Leggja saman staðlað **kostnaðarverð keyrð** til að uppfæra staðlað kostnaðarverð í vinnustöðvum, vélastöðvum, samsetningarforða, framleiðsluuppskriftum og samsetningaruppskriftum.
#### <a name="options-1"></a>Valkostir
**Staðlað kostn.verð**: Færður er inn leiðréttingarstuðullinn sem á að nota til að uppfæra staðlað kostnaðarverð. Einnig er hægt að velja **sléttunaraðferð** fyrir nýja staðlaða kostnaðarverðið. Fylla þarf út reitinn með aukastöfum fyrir prósentuhækkunina, til dæmis 1,1.

**Óbein kostnaðar%**: Færa skal inn leiðréttingarstuðulinn sem á að nota til að uppfæra óbeina kostnaðar%. Einnig er hægt að velja sléttunaraðferð fyrir nýja óbeina kostnaðar%. Fylla þarf út reitinn með aukastöfum fyrir prósentuhækkunina, til dæmis 1,1.

**Hlutfall** sameiginlegs kostnaðar: Færður er inn leiðréttingarstuðullinn sem á að nota til að uppfæra hlutfall sameiginlegs kostnaðar. Einnig er hægt að velja sléttunaraðferð fyrir nýtt hlutfall sameiginlegs kostnaðar. Fylla þarf út reitinn með aukastöfum fyrir prósentuhækkunina, til dæmis 1,1.

### <a name="post-inventory-cost-to-gl"></a>Bóka birgðakostnað í fjárhag

 Skráir breytingar á magni og virði birgða í birgðafærslum og virðisfærslum þegar birgðafærslur eru bókaðar, t.d. söluafhendingar eða innkaupamóttökur.

Ef gátreiturinn **Sjálfvirk kostnaðarbókun** hefur ekki verið valinn í **glugganum Birgðagrunnur** er birgðakostnaður ekki skráður kviklega í fjárhag og KSV er ekki reiknaður með sölu. Þess vegna verður að bóka í fjárhag handvirkt með því að keyra **keyrsluna Bóka birgðabreytingar** til að uppfæra fjárhaginn og prenta skýrslu um virðisfærslurnar sem eru bókaðar.

Keyrslan notar virðisfærslur sem grunn. Til að reikna gildið sem á að bóka er notaður mismunurinn á reitunum **Kostnaðarupphæð (raunverul.)** og **Kostnaðarbókað í fjárhag** í virðisfærslunum. Ef gátreiturinn **Væntanl. kostn. bók. í fjárhag** hefur verið valinn í **glugganum Birgðagrunnur** bókar keyrslan einnig mismuninn á reitunum **Kostnaðarupphæð (væntanl.)** og Reitnum **Væntanl. kostn. bókaður í fjárhag** á bráðabirgðareikninga í fjárhag.

> [!NOTE]
> Ef gátreiturinn **Væntanl. kostn. bók. í fjárhag** hefur ekki verið valinn í **glugganum Birgðagrunnur** birtir síðasti hluti skýrslunnar virðisfærslur sem er sleppt þar sem þær standa fyrir væntanlegan kostnað.

> [!NOTE] 
> Ef keyrslan rekst á villu vegna vídda eða víddaruppsetningar hnekkir keyrslan villunni og bókar færsluna í fjárhaginn með því að nota víddir virðisfærslunnar.

Ef ganga þarf úr skugga um að keyrslan rekist ekki á villur er hægt að keyra keyrsluna **Bóka birgðafrávik. Kostnaður í fjárhag - Prófunarskýrsla** til að sjá allar villur sem komu upp. Síðan er hægt að **laga villurnar og keyra keyrsluna** Bóka birgðabreytingar með vissu um að hún vinnur allar færslur.
 
> [!IMPORTANT]  
> Áður en þessi keyrsla er notuð ætti að keyra keyrsluna **Leiðr. kostnað - Birgðafærslur** . Þetta tryggir að kostnaður sem er bókaður í Fjárhag verði leiðréttur þegar þessi keyrsla er keyrð.
#### <a name="options-2"></a>Valkostir

|Valkostur  |Heimildasamstæða  |
|--------------|---------|
|**Bókunaraðferð**|Keyrslan getur annaðhvort bókað birgðavirði í fjárhag á hvern bókunarflokk eða á hverja bókaða færslu. Ef bókað er á hverja færslu fæst nákvæm sundurliðun á því hvaða áhrif birgðir hafa á fjárhag, en einnig margar fjárhagsfærslur. Ef bókað er á hvern bókunarflokk býr keyrslan til samsetningu fjárhagsfærslu fyrir hverja bókunardagsetningu fyrir hvern bókunarflokk. Það merkir að fjárhagsfærslan er stofnuð fyrir hverja samsetningu bókunardagsetninga, almenna viðskiptabókunarflokka, almenna framleiðslubókunarflokka, birgðabókunarflokka og staðsetningarkóta. Auk þess stofnar keyrslan sérstakar fjárhagsfærslur fyrir kostnað með mismunandi merkjum.|
|**Númer fylgiskjals**|Í þennan reit má tilgreina fylgiskjalsnúmer ef aðgerðin Bóka eftir birgðabókunarflokki var valin. Númer fylgiskjalsins kemur fram í bókuðum færslum.|
|**Færsla**|Þessi reitur er valinn ef keyrslan á að bókast sjálfkrafa í fjárhag. Ef ekki er valið að bóka birgðakostnað í fjárhag prentar keyrslan aðeins prófunarskýrslu sem sýnir virði sem hægt er að bóka í fjárhag og í skýrslunni birtist **prófunarskýrsla (óbókuð)**.|

### <a name="roll-up-standard-cost"></a>Leggja saman staðl. kostnaðarv.

Samantekt staðlaðs kostnaðarverðs samsettra og framleiddra vara. Það hefur áhrif á breytingar á stöðluðu kostnaðarverði íhluta sem lagt er til í keyrslunni **Leggja til staðalkostnað** vöru. Þar að auki hafa þau áhrif á breytingar á stöðluðu kostnaðarverði framleiðslugetu og samsetningarforða sem lagt er til í keyrslunni **Leggja til staðalkostn** . vinnu-/vélast.

Þegar búið er að keyra aðra hvora keyrsluna eða báðar og samantektin er gerð eru allar breytingar á stöðluðu kostnaðarverði á vinnublaðinu kynntar í tengdum framleiðslu- eða samsetningaruppskriftum og kostnaðurinn er notaður á hverju uppskriftarstigi.

> [!NOTE] 
> Þessi aðgerð tekur aðeins saman staðlað kostnaðarverð á birgðaspjöldunum, ekki á birgðahaldseiningaspjöldunum.

Keyrslan býr aðeins til tillögur. Hún framkvæmir ekki breytingarnar sem lagðar voru til. Ef tillögurnar eru fullnægjandi og koma á þeim í framkvæmd, þ.e. uppfæra þær á birgðaspjöldunum og setja þær inn í **gluggann Endurmatsbók**, þá er hægt að nota **keyrsluna Innleiða breytingu á stöðluðu kostnaðarverði** . Þessi keyrsla er opnuð í **glugganum Vinnublað** staðlaðs kostnaðarverðs.
#### <a name="options-3"></a>Valkostir

**Dagsetning útreiknings** Rituð er dagsetningin sem á við útgáfu framleiðsluuppskriftarinnar sem gera á samantektina fyrir.
 
### <a name="implement-standard-cost-change"></a>Innleiða breytingu á stöðluðu kostnaðarverði

Uppfærir breytingar á stöðluðu kostnaðarverði í **töflunni Vara** með þeim sem eru í **töflunni Vinnublað** staðlaðs kostnaðarverðs. Hægt er að stofna breytingatillögur um staðlað kostnaðarverð með keyrslunni **Leggja** til staðalkostnað **vöru og/eða Leggja til staðalkostn** . vinnu-/vélast. og einnig er hægt að breyta þeim. Efni allra reitanna í breytingatillögunum um staðlað kostnaðarverð er flutt. Þegar tillögur um breytingar á stöðluðu kostnaðarverði eru innleiddar er hægt að skoða þær á birgðaspjaldinu og/eða vinnu-/vélastöðvarspjöldunum. Einnig er stofnuð endurmatsbók til að uppfæra virði fyrirliggjandi birgða.
#### <a name="options-4"></a>Valkostir

**Bókunardags.**: Hér er færð inn dagsetningin þegar endurmatið á að fara fram.

**Númer** fylgiskjals:Færa skal inn númer endurmatsbókarlínanna. Ef númeraröð er sett upp í heiti birgðabókarkeyrslunnar fylgir fylgiskjalsnúmerið færslunum sem gerðar eru með því að bóka endurmatsbókina. Annars er hægt að rita númer handvirkt.

**Sniðmát** birgðabókar: Færa skal inn heiti sniðmáts endurmatsbókar.

**Heiti** birgðabókarkeyrslu: Færa skal inn heiti sjálfrar endurmatsbókarinnar.

Valið er **Í lagi** til að hefja keyrsluna. Ef ekki á að keyra keyrsluna núna er Hætta við **valið** til að loka glugganum.

## <a name="see-also"></a>Sjá einnig .

[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  
[Uppfæra staðlaðan kostnað](finance-how-to-update-standard-costs.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
