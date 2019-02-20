---
title: "Setja upp upplýsingar fyrir tengiliði| Microsoft Docs"
description: "Útskýrir hvernig skal tilgreina upplýsingar og kóða, t.d. um starfsgreinahópa og viðskiptasambönd, áður en þú setur upp tengiliði."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: is-is
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Uppsetning tengiliða
Þegar tengiliðir eru stofnaðir má færa inn nákvæmar upplýsingar, eins og þær starfsgreinar sem fyrirtækjatengiliðirnir tilheyra og viðskiptatengsl við tengiliðina.

Áður en tengiliðir eru stofnaðir og upplýsingar skráðar um viðskiptatengsl þarf að setja upp kótana sem notaðir verða til að úthluta þessum upplýsingum til fyrirtækjatengiliða og einstaklinga. Hægt er að setja upp kóta fyrir pósthópa, starfsgreinahópa, viðskiptatengsl, veftengingar, stjórnunarstig og starfsábyrgð.

Með uppsetningu þessara upplýsinga eykst skipulag við stofnun tengiliða, og skilvirkni eykst þegar hægt er að finna alla tengiliði sem tilheyra tilteknum hóp. Allir hópar í fyrirtækinu geta nálgast þessar upplýsingar sem gerir samskipti við tengiliðina árangursríkari.

Í tengslum við uppsetningu á tengiliðunum þína verður þú að setja upp viðskiptatengslin sem ert með fyrir tengiliðina, til dæmis væntanlegur viðskiptamaður, banki, ráðgjafi eða þjónustuveitandi. Nánari upplýsingar er að finna í [Uppsetning viðskiptatengsla á tengiliðafyrirtækjum](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Uppsetning iðnaðarhópa fyrir tengiliðafyrirtæki
Starfsgreinahópar eru notaðir til að tilgreina tegund starfsgreinar sem tengiliðirnir tilheyra, til dæmis smásöluaðilar eða bílgreinaiðnaðurinn.

Notkun starfsgreinahópa á tengiliði er tveggja þrepa ferli. Fyrst skilgreina starfsgreinarhópakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver starfsgreinarhóp. Þegar kominn er starfsgreinarhópakóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

> [!NOTE]  
>   Ef á að samstilla tengiliði við lánardrottna, viðskiptamenn eða bankareikninga í öðrum hlutum kerfisins er ráðlegt að setja upp viðskiptatengsl fyrir þá.

### <a name="to-define-an-industry-group-code"></a>Til að skilgreina kóða starfsgreinarhóps
Kóði starfsgreinarhópsins skilgreinir tegund eða flokk hópsins, til dæmis ADVERT fyrir auglýsingar eða Press fyrir sjónvarp og útvarp. Hægt er að hafa nokkrar starfsgreinarhópakóða. Til að skilgreina starfsgreinarhópa skal nota síðuna **Starfsgreinarhópar**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsgreinahópar** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

### <a name="AssignIndustryGroupContact"></a> Starfsgreinahópum úthlutað á tengilið
Þú getur ekki Úthluta Starfsgreinahópar á tengilið - aðeins fyrirtæki.

1. Tengiliðurinn er opnaður.
2. Valið er **Fyrirtæki** aðgerð, og síðan **starfsgreinarhópar** aðgerð. Síðan **Starfsgreinahópar tengiliða** birtist.
3. Í reitnum **starfsgreinarhópakóði** veljið starfsgreinahópinn sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum starfsgreinahópum og óskað er. Einnig má nota sömu aðferð til að úthluta Starfsgreinahópar úr Tengiliðalista.

Fjöldi iðnaðarhópa sem þú hefur úthlutað tengiliðnum birtist á **Fjöldi starfsgreinahópa** reitnum í **Hlutunarviðmið** hlutanum á síðunni **Tengiliður**.

Þegar tengiliðum hefur verið úthlutað starfsgreinarhópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Setja upp pósthópa fyrir tengiliði
pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar. Til dæmi er hægt að setja upp pósthóp með þeim tengiliðum sem eiga að fá tilkynningu um að skrifstofan hafi flutt, eða annan hóp til að senda gjafir á hátíðum.

Notkun pósthópar á tengiliði er tveggja þrepa ferli. Fyrst skilgreina pósthópskóða. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver pósthóp. Þegar kominn er pósthópskóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.

### <a name="to-define-mailing-group-codes"></a>Skilgreina pósthópskóða
Pósthópskóði skilgreinir tegund eða flokk hóps, eins og Move fyrir flutning skrifstofu, GIFT fyrir hátíðsgjöf. Hægt er að hafa nokkrar starfsgreinarhópakóða. Til að skilgreina starfsgreinarhópa skal nota síðuna **Pósthópar**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Pósthópar** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

### <a name="AssignMailGroupContact"></a> Pósthópum úthlutað á tengiliði
1. Tengiliðurinn er opnaður.
2. Valið er **Pósthópar** aðgerð. Síðan **Pósthópar tengiliða** birtist.
3. Í reitnum **Pósthópskóði** veljið pósthópinn sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum pósthópum og óskað er. Einnig má nota sömu aðferð til að úthluta pósthópum úr Tengiliðalisti.

Fjöldi pósthópa sem þú hefur úthlutað tengiliðnum birtist í **Fjöldi pósthópa** í hlutanum **hlutaaðgerðin** á síðunni **Tengliður**.

Eftir að tengiliðum hefur verið úthlutað pósthópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Uppsetning á öðrum aðsetrum tengiliða
Hægt er að velja annað aðsetur þangað sem stundum má senda tengiliðum póst og upplýsingar, til dæmis sumarbústaðinn þeirra. Hægt er að úthluta einu eða fleirum dagsetningarbilum á hvert annað aðsetur sem hefur verið fært inn fyrir tengiliðina til að tilgreina hvenær hvert þeirra er í gildi.

### <a name="to-assign-an-alternate-address"></a>Til að úthluta öðru aðsetri
1. Tengiliðurinn er opnaður.
2. Veljið aðgerðina **Annað aðsetur** og veljið síðan **Spjald**. Síðan **Önnur aðs. tengiliðar - listi** opnast.
3. Nýtt aðsetur er fært inn og reitirnir á síðunni **Önnur aðsetur tengiliðar** eru fylltir út.

Skrefin eru endurtekin til að úthluta eins mörgum öðrum aðsetrum og óskað er. Tilgreina má eitt eða fleiri dagsetningarsvið fyrir hvert annað aðsetur.

Einnig má nota sömu aðferð til að úthluta öðrum aðsetrum af síðunni tengiliðalisti.

### <a name="to-assign-an-alternate-address-date-range"></a>Til að úthluta öðru dagsetningasviði aðseturs
1. Tengiliðurinn er opnaður.
2. Veljið aðgerðina **Annað aðsetur** og veljið síðan **Dagsetningabil**. Síðan **Dags.bil á öðru aðsetri tengiliðar** opnast.
3. Veljið aðgerðina **Nýtt**.
4. Í reitnum **Kóði annars aðs. tengiliðar** skal velja aukaaðsetur fyrir þennan tengilið og síðan er fyllt inn í reitina **Upphafsdagsetning** og **Lokadagsetning**.

Skrefin eru endurtekin til að úthluta eins mörgum dagsetningasviðum og óskað er.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Uppsetning starfsábyrgða fyrir tengiliði
Þú getur bætt við upplýsingum um starfsábygð tengiliðar til að gefa til kynna hvað tengiliðurinn er ábyrgur fyrir innan síns fyrirtækistil dæmis upplýsingatækni, stjórnun eða framleiðsla. Þessar upplýsingar er hægt að nota þegar færðar eru inn upplýsingar um tengiliði.

Notkun starfsábyrgðir á tengiliði er tveggja þrepa ferli. Fyrst skilgreinirðu starfsábyrgðarkóða. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver starfsábyrgð. Þegar kominn er starfsábyrgðarkóði er hægt að byrja að úthluta kóðanum til tengiliða.

### <a name="to-define-a-job-responsibility-code"></a>Að skilgreina starfsábyrgðarkóða
Starfsábyrgðarkóði skilgreinir tegund eða flokk verks, eins og markaðssetning eða innkaup. Hægt er að hafa nokkra starfsábyrgðarkóða. Til að skilgreina starfsábyrgð á að nota síðuna **starfsábyrgð**-.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Starfsábyrgð** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Að úthluta starfsábyrgð á tengilið
Þú getur ekki úthluta Starfsábyrgðum á tengiliðafyrirtæki:

1. opið tengilið.
2. Veljið aðgerðina **Einstaklingur** og veljið síðan aðgerðina **starfsábyrgðir**. Síðan **Starfsábyrgðir tengiliðar** birtist.
3. Í reitnum **Starfsábyrgðarkóði** veljið starfsábyrgð sem á að úthluta.

Skrefin eru endurtekin til að úthluta eins mörgum starfsábyrgðum og óskað er. Einnig má nota sömu aðferð til að úthluta Starfsábyrgð úr Tengiliðalisti.

Fjöldi vinnuverkefna sem þú hefur úthlutað tengiliðnum birtist á **Fjöldi starfsábyrgða** í hlutanum **Hlutunarviðmið** á síðunni **Tengiliður**.

Eftir að tengiliðum hefur verið úthlutað starfsábyrgðum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Uppsetning stjórnunarstiga fyrir tengiliði
Hægt er að úthluta stjórnunarstigum á tengiliði til að tilgreina hvaða stöðu þeir hafa innan fyrirtækis, til dæmis forstjóri. Þessar upplýsingar er hægt að nota þegar færðar eru inn upplýsingar um tengiliði.

Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli. Fyrst að skilgreina viðskiptatengslakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl. Þegar kominn er viðskiptatengslakóði er hægt að byrja að úthluta kóðanum til tengiliða.

### <a name="to-define-an-organizational-level-code"></a>Skilgreining viðskiptatengslakóða
Viðskiptatengslakóði skilgreinir tegund eða flokk stjórnunarstigs, eins og framkvæmdastjóri eða fjármálastjóri. Hægt er að hafa nokkra viðskiptatengslakóða. Síðan **Stjórnunarstig** er notuð til að skilgreina stjórnunarstigið.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Stjórnunarstig** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Að úthluta skipulagsstigum til tengiliðs
Aðeins er hægt að úthluta stjórnunarstigum á einstaklinga, ekki á fyrirtæki. Aðeins er hægt að úthluta einu stjórnunarstigi á hvern tengilið.

1. Tengiliðurinn er opnaður.
2. Í reitnum **Stjórnunarstig** skal velja kóðann sem á að úthluta.

Þegar tengiliðum hefur verið úthlutað stjórnunarstigi er hægt að nota þær upplýsingar til að stofna hluta.

Eftir að tengiliðum hefur verið úthlutað starfsábyrgðum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Uppsetning veftenginga fyrir tengiliðafyrirtæki
Hægt er að nota veftengingar með tengiliðafyrirtækjum til að þekkja t.d. leitarvélar og vefsvæði á netinu sem óskað er eftir að nota til að leita að upplýsingum um tengiliðina. Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.

Notkun veftenginga á tengiliði er tveggja þrepa ferli. Fyrst að skilgreina veftengingakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hverja veftengingu. Þegar kominn er veftengingakóði er hægt að byrja að úthluta kóðanum til tengiliða.

### <a name="to-define-a-web-source-code"></a>Skilgreina veftengingarkóða
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **veftengingar** og veldu síðan tengda tengilinn.
2. Veljið aðgerðina **Nýtt**.
3. Fyllt er í reitina **Kóti**, **Lýsing** og **URL**.

    Sláið inn %1 í reitinn **URL** til að setja inn staðgengil fyrir leitarorð í slóðinni. Þegar veftengingin er ræst frá tengilið er %1 skipt út fyrir leitarorð, t.d. heiti fyrirtækisins sem fært var inn á síðuna **Veftenging tengiliðar**.

Skrefin eru endurtekin til að setja upp eins margar veftengingar og óskað er.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Úthluta veftengingum á tengiliðarfyrirtæki
Þegar veftengingu er úthlutað er tilgreint hvaða leitarvél og leitarorð kerfið eigi að nota til að finna umbeðnar upplýsingar.

1. Tengiliðurinn er opnaður.
2. Veljið aðgerðina **Fyrirtæki** og veljið síðan aðgerðina **Veftenging**. Síðan **Veftenglar tengiliða** birtist.
3. Í reitnum **Veftengingarkóði** skal velja veftenginguna sem á að úthluta.
4. Í reitinn **Leitarorð** er fært inn leitarorðið sem á að nota til að finna upplýsingarnar.

Skrefin eru endurtekin til að úthluta eins mörgum veftengingum og óskað er.

Einnig má nota sömu aðferð til að úthluta veftengingum á síðunni **Tengiliðalisti**.

## <a name="see-also"></a>Sjá einnig
[Vinna með tengiliði](marketing-contacts.md)  
[Umsjón sölutækifæra](marketing-manage-sales-opportunities.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

