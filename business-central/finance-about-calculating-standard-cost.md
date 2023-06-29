---
title: Um umreikning staðalkostnaðar
description: Í kerfi staðalkostnaðar er kostnaðarverð birgða ákvarðað á grundvelli ásættanlegs eða viðbúins kostnaðar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: edupont
---
# <a name="about-calculating-standard-cost"></a><a name="about-calculating-standard-cost"></a>Um umreikning staðalkostnaðar

Mörg framleiðslufyrirtæki velja matsgrundvöll staðlaðs kostnaðarverðs. Þetta á einnig við fyrir fyrirtæki sem framkvæma létta framleiðslu, til dæmis samsetningu og röðun í sett. Í stöðluðu kostnaðarverðskerfi er kostnaðarverð birgða ákvarðað á grundvelli einhvers ásættanlegs eða viðbúins kostnaðar. Rannsóknir á fyrri kostnaði og áætluðum framtíðarkostnaði  geta skapað grundvöllinn fyrir stöðluðu kostnaðarverði. Þessi kostnaður er frystur þar til ákvörðun er tekin um að breyta honum. Raunverulegur kostnaður við framleiðslu vöru er frábrugðinn því staðlaða kostnaðarverði sem metið er. Raunverulegi kostnaðurinn er borinn saman við staðlað kostnaðarverð tiltekinnar vöru og munur á þeim eða *frávik* eru fundin og greind til að auðvelda stjórnun.  

Hægt er að viðhalda stöðluðum kostnaði fyrir vörur fyllt er á með innkaupum, samsetningu og framleiðslu. Fyrir hverja áfyllingaraðferð, getur staðlaður kostnaður samanstaðið af eftirfarandi einingum.  

|Áfyllingarkerfið|Staðlaðir kostnaðarliðir|  
|--------------------------|----------------------------|  
|**Innkaup**|Beinn efniskostnaður og sameiginlegur efniskostnaður, ef nauðsyn krefur.|  
|**Samsetning**|Beinn efniskostnaður er beinn eða fastur vinnukostnaður og sameiginlegur kostnaður.|  
|**Framl.pöntun**|Beinn efniskostnaður,vinnukostnaður, undirverktakakostnaður og sameiginlegur kostnaður.|  

## <a name="setting-up-standard-costs"></a><a name="setting-up-standard-costs"></a>Uppsetning staðlaðs kostnaðarverðs

Þar sem staðlað kostnaðarverðframleiddrar eða samsettrar vöru getur samanstaðið af mörgum kostnaðarliðum, þar með talið efnis-, afkastagetu- (vinnu-) og undirverktakakostnaði (beinum og sameiginlegum), þarf að búa til staðlað kostnaðarverð fyrir hvern þessara liða.  

Bókhaldsverkhluti vöruvinnslufyrirtækis sem notar staðlaðan kostnaðarútreikning er:  

- Áætla staðlað kostnaðarverð fyrir fullunna vöru og setja á birgðarspjaldið.  
- Skrá skal og ráðstafa raunverulegum kostnaði aðalkostnaðarliða og gera frávikum rétt skil.  

Telja þarf saman allan íhlutakostnaðinn til að ákvarða beinan kostnað fullunninnar vöru. Samsett eða framleidd vara getur falið í sér undirsamsetningar, sem einnig samanstanda af mörgum íhlutum.  

Eftirfarandi lykilkostnaðarliðir mynda samtölu beins kostnaðar vöru sem er fullunnin:  

- Efniskostnaður.  
- Getukostnaður  
- Undirverktakakostnaður fyrir framleiddar vörur eingöngu.  

### <a name="material-costs"></a><a name="material-costs"></a>Efniskostnaður

Efniskostnaður er kostnaður sem tengist undirsamsetningum og aðkeyptum hráefnum. Efniskostnaðarverð getur samanstaðið af beinum og óbeinum kostnaðarliðum.  

- Beinn efniskostnaður er reikningsfærð upphæð fyrir aðkeypt hráefni eða framleiðslukostnaður undirsamsetningar.  
- Óbeinn efniskostnaður, eða *sameiginlegur kostnaður*, getur til dæmis verið birgðageymslukostnaður fyrir fullunnu vöruna þegar búið er að framleiða hana.  

Uppsetning efniskostnaðar keyptra vara sem hafa áhrif á beinan og óbeinan kostnað veltur á því hvaða kostnaðaraðferð er valin fyrir vöruna sem er tilgreind. Kostnaðarupplýsingar fyrir aðra hvora aðferð kostnaðarútreiknings eru settar upp. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

Kostnaður úrkasts (framleiðsla eingöngu) er annar þáttur í útreikningi á heildarefniskostnaði sem taka þarf tillit til. Þegar vissu magni af hráefni er hent við það að setja saman eða framleiða vöru verður það yfirleitt til þess að meira magn af íhlutum þarf til að framleiða þá vöru. Það eykur svo efniskostnað þeirra íhluta sem eru notaðir við framleiðslu yfirvöru. Úrkastskostnaður efnis er settur upp á annað hvort framleiðsluuppskriftinni eða -leiðinni.  

Hægt er að setja efniskostnað framleiddrar vöru fram á tvo vegu sem samsvara eftirfarandi útreikningsgrundvöllum staðlaðs kostnaðarverðs:  

|Grunnur fyrir útreikning kostnaðarverðs|Útreikningur efniskostnaðar|  
|----------------------------|-------------------------------|  
|Eitt stig|Framleidd vara er jöfn heildarkostnaði allra keyptra eða undirsamsettra vara í framleiðsluuppskrift vörunnar.|  
|Samantekið stig eða mörg stig|Framleidd vara er samtala efniskostnaðar fyrir allar undirsamsetningar á uppskrift þeirrar vöru og kostnaðar allra aðkeyptra vara á framleiðsluuppskrift þeirrar vöru.|  

### <a name="capacity-costs"></a><a name="capacity-costs"></a>Getukostnaður

Getukostnaður er sá kostnaður sem er tengdur við kostnað við innanhússvinnuafl og vélar. Setja verður upp kostnað fyrir sérhvern forða (í samsetningarstjórnun) og verk eða vélastöð á leið (í framleiðslu). Eins og með efni er hægt að finna bæði beina og óbeina kostnaðarliði getu. Til dæmis getur beinn kostnaður við vinnustöð verið viðurkenndi verslunartaxtinn við framkvæmd sérstakrar aðgerðar. Óbeini kostnaðurinn fyrir vinnustöð getur falið í sér einhvern almenn verksmiðjuútgjöld eins og lýsingu, húshitun og svo framvegis. Hægt er að setja sameiginlegan getukostnað fram sem óbeina kostnaðarprósentu eða fastan taxta sameiginlegs kostnaðar, svipað og með efniskostnað.  

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

### <a name="subcontractor-costs"></a><a name="subcontractor-costs"></a>Undirverktakakostnaður

Undirverktakakostnaður er sá kostnaður sem er tengdur við þjónustu sem utanaðkomandi birgjar og undirverktakar bjóða upp á. Svipað og með efni og afkastagetu kann undirverktakakostnaður að samanstanda af bæði beinum og sameiginlegum upphæðum. Beinn undirverktakakostnaður felur í sér raunverulegt gjald fyrir hverja veitta þjónustueiningu. Sameiginlegur undirverktakakostnaður getur til dæmis falið í sér frakt- og meðhöndlunarkostnað sem fyrirtækið lendir í í samhengi við pöntun undirverktaka.  

Þar sem undirverktakastarfsemi færsla á afkastagetu út fyrir fyrirtækið er kostnaðurinn við þjónustu undirverktaka (beinn og óbeinn) settur upp á vinnustöðvarspjaldinu sem stendur fyrir undirverktakaaðgerðina.  

## <a name="updating-standard-costs"></a><a name="updating-standard-costs"></a>Uppfærsla staðlaðs kostnaðarverðs

Til að uppfæra eða reikna staðlað kostnaðarverð fyrir samsetningarvörur er aðgerðin notuð af birgðaspjaldinu.  

Ferlið til að uppfæra eða reikna út staðlaðan kostnað samanstendur yfirleitt af eftirfarandi verkum:  

1.  Uppfærslu kostnaðar á íhluta- og afkastagetustigunum. Frekari upplýsingar, sjá **Leggja til staðlaðan vörukostnað** og **Leggja til staðlaðan afkastakostnað** runuvinnslurnar.  
2.  Samstilling og samantekt íhluta- og afkastakostnaðarins til að reikna út heildarframleiðslukostnað varanna. Nánari upplýsingar er að finna í [Að reikna út staðalkostnað á samsetningaríhlut](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Innleiðing staðlaðs kostnaðar sem færður var inn þegar fyrri keyrsla var keyrð. Staðlaður kostnaður tekur ekki gildi fyrr en hann er innleiddur. Notaðu runuvinnsluna **Innleiða breytingu á stöðluðu kostnaðarverði**, sem uppfærir breytingar á staðalkostnaði á vörum með þeim sem er í töflunni vinnublað staðlaðs kostnaðarverðs.  
4.  Innleiðing breytinga til að uppfæra reitinn **Kostn.verð** á birgðaspjaldinu og framkvæmd endurmats á birgðum. Nánari upplýsingar eru í [Endurmat birgða](inventory-how-revalue-inventory.md).

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md)  
[Uppfæra staðlaðan kostnað](finance-how-to-update-standard-costs.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
