---
title: Setja upp bókun millifyrirtækjafærslu
description: Læra hvernig setja á upp milli-fyrirtækjafélaga.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/27/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621, 653_Primary'
ms.service: dynamics-365-business-central
---
# Setja upp færslur milli fyrirtækja

Samstarf milli fyrirtækja auðveldar umsjón með bókhaldsferlum þegar tvö eða fleiri dótturfyrirtæki eiga oft viðskipti við hvert annað. Félagar geta skipst á færslum, t.d. sölu og innkaupum, séð um þær annaðhvort handvirkt eða sjálfvirkt. Til dæmis, þegar félagi sendir sölubókarlínu til annars félaga er stofnuð innkaupabókarlína fyrir félagann sem tekur við.

Bókhaldslykill milli fyrirtækja getur til dæmis verið útgáfa af bókhaldslykli samstillingarfélagans. Hver félagi varpar reikningum sínum á bókhaldslykil milli fyrirtækja. Hver félagi varpar einnig víddum sínum og víddargildum á víddir milli fyrirtækja.

> [!NOTE]
> Í 2023 útgáfu bylgju 1 höfum við kynnt endurbætta **uppsetningarsíðu** milli fyrirtækja. Nýja síða auðveldar uppsetningu MF-félaga með því að sameina öll uppsett verk á einni síðu. Ef þú ert nýr [!INCLUDE [prod_short](includes/prod_short.md)] þá notar þú nýja upplifun. Ef þú ert núverandi viðskiptamaður getur kerfisstjórinn kveikt á aðgerðinni **Samþykkja færsluaðgerðir** milli fyrirtækja færslubóka sjálfkrafa á síðunni **Eiginleikastjórnun** .
>
> Verkhlutar þessa greinar gera ráð fyrir að kveikt sé á eiginleikarofanum. Ef búið er að setja upp MF-félaga er hægt að halda áfram að nota það.

## Verður að byrja fyrir

Áður en hafist er handa við að setja upp milli-fyrirtækjafélaga þarf að taka nokkrar ákvarðanir.

|Ákvörðun  |Heimildasamstæða  |
|---------|---------|
|Hvaða bókhaldslykill á að vera grunnurinn fyrir bókhaldslykil milli fyrirtækja?     | Öll fyrirtæki í félaginu verða að nota sama bókhaldslykil milli fyrirtækja. Hægt er að byggja bókhaldslykil milli fyrirtækja í bókhaldslyklinum frá einu af fyrirtækjunum í félaginu eða stofna nýjan bókhaldslykil milli fyrirtækja. Reikningarnir sem nota á í félaginu eru varpaðir á báða vegu, þannig að hver félagi sendir bæði og tekur á móti færslum í réttum reikningum. Fræðast meira um uppsetningu bókhaldslykils milli fyrirtækja í [Setja upp bókhaldslykil milli fyrirtækja](#set-up-the-intercompany-charts-of-accounts).         |
|Hvaða víddir á að vera grunnurinn fyrir víddir milli fyrirtækja?     | Ef víddir milli fyrirtækja eru notaðar verða þær að vera þær sömu fyrir öll fyrirtæki í félaginu. Þegar víddir milli fyrirtækja hafa verið tilgreindar er víddargildum þeirra varpað. Fræðast meira um vörpun víddargilda í Setja upp víddir [milli](#set-up-intercompany-dimensions) fyrirtækja.        |
|Hvaða félagar eru viðskiptamenn eða lánardrottnar, eða hvort tveggja?     |  Fræðast meira um uppsetningu viðskiptamanna og lánardrottnafyrirtækja í samstarfi milli fyrirtækja í [Setja upp MF-félaga sem viðskiptamenn og lánardrottna](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Á að tilgreina bankareikninga sem nota á í félaginu?| Hægt er að flýta skráningu greiðslufærslna með því að tilgreina bankareikning sem nota skal fyrir hvert fyrirtæki félaga. Fræðast meira um bankareikningana sem nota á [fyrir samstarfsaðila](#specify-the-bank-accounts-to-use-for-intercompany-partners) milli fyrirtækja. |
|Hvernig á að auðkenna fyrirtækin í samstarfinu?     | Allir aðilar verða að samþykkja einkvæman auðkenniskóta MF-félaga fyrir hvert fyrirtæki. Kótanum verður úthlutað á spjöld viðskiptamanna og lánardrottna til að auðkenna tengdar færslur. Fræðast meira um kenni í [Stofna númeraraðir](ui-create-number-series.md).        |
|Hvernig á að meðhöndla vörunúmer?     | Ef vörur eru í millifyrirtækjalínum er annaðhvort hægt að nota eigin vörunúmer eða setja upp vörunúmer félagans fyrir hverja vöru, annaðhvort í reitnum **Vörunr. lánardr.** eða í reitnum **Algeng vara nr.** á birgðaspjaldinu. Einnig er hægt að nota aðgerðina **Vörutilvísun** til að varpa vörunúmerum á milli-fyrirtækjafélaga lýsingar á vörunum. Til að fræðast meira um vörutilvísanir er farið í [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md).        |
|Tengist það forðanum?     | Ef söluviðskipti milli fyrirtækja munu innihalda forða er reiturinn **Innk.mF-félagi fylltur út. Fjárhagsreikn.nr.** á forðaspjaldi sérhvers forða. Í þessum reit er númer MF-fjárhagsreikningsins sem upphæðin fyrir þennan forða bókast á í fyrirtæki félagans. Nánari upplýsingar um forða eru notaðar til að [setja upp forða](projects-how-setup-resources.md).<br><br>**NÓTA**<br>Innkaupafærslur milli fyrirtækja sem innihalda tilföng, eignir og vörugjöld eru ekki studdar að fullu. Reiturinn **Línutegund** er auður í línum innkaupaskjals í félagafyrirtækinu. Uppfæra þarf reitinn handvirkt.        |

## Yfirlit yfir skrefin sem hefjast á

Nota síðuna **Uppsetning** milli fyrirtækja til að setja upp eftirfarandi íhluti í færslum milli fyrirtækja:

* Stillingar milli fyrirtækja í fyrirtækinu.
* Fyrirtækið sem verður samstillingarfélaginn.
* Bókhaldslykill milli fyrirtækja sem allir hann félagar nota til að skiptast á færslum.
* Vörpun milli reikninga í bókhaldslykli og MF-bókhaldslykli fyrir færslur á inn- og útleið fyrir hvern félaga.
* Millifyrirtækjavíddirnar og víddargildin sem á að nota og hvernig þeim er varpað á víddir hvers félaga.
* Fyrirtækin sem eru MF-félagarnir.
* Fyrirtækin sem eru lánardrottnar eða viðskiptamenn eða hvort tveggja.

## Setja upp samstillingarfélaga

Allir félagar verða að nota sama MF-bókhaldslykilinn og sömu millifyrirtækjavíddirnar ef með þarf. Hægt er að spara tíma þegar félagið er sett upp með því að nota bókhaldslykil og víddir eins félaganna sem grunnlínu fyrir bókhaldslykil og víddir milli fyrirtækja. Fyrirtækið sem notað er sem grunnlína er kallað *samstillingarfélaginn*. Yfirleitt er samstillingarfélaginn höfuðstöðvarfyrirtækið en þarf þess ekki.

Á síðunni **Uppsetning** milli fyrirtækja tilgreinir hver félagi samstillingarfélagans í reitnum **Samstillingarfélagi** . Síðan eru bókhaldslyklar milli fyrirtækja og víddir milli fyrirtækja sjálfkrafa tilgreindir fyrir þá, byggt á uppsetningu samstillingarfélagans. Félagarnir nota **síðan síðurnar Vörpun** bókhaldslykils milli fyrirtækja og **MF-víddavörpun** til að varpa bókhaldslykli sínum og víddum á MF-bókhaldslykil og víddir og öfugt. 

> [!NOTE]
> Mikilvægt er að varpa reikningum og víddum í báðar áttir. Það er, bæði að bókhaldslykli og víddum milli fyrirtækja, og frá þeim til eigin reikninga og vídda.

### Tengjast samstarfsaðilum í öðru leigjanda eða umhverfi

Ef einn eða fleiri félagar'er [!INCLUDE [prod_short](includes/prod_short.md)]  í öðru leigjanda eða umhverfi eru nokkur aukaskref til að búa til tenginguna. Skrefin eiga við um alla félaga í öðru leigjanda eða umhverfi.

* Setja upp [!INCLUDE [prod_short](includes/prod_short.md)] sem skráð forrit í Azure portal.
* Bæta við og virkja skráningu forritsins í [!INCLUDE [prod_short](includes/prod_short.md)].
* Skiptast á upplýsingum um uppsetningu milli fyrirtækja. Hver félagi getur fengið þessar upplýsingar í Uppsetning milli fyrirtækja,Aðgerðir,Sundurliðun **·** **tengingar**. **·**

   |Afrita úr uppsetningu félagans  |Afrita í uppsetninguna  |
   |---------|---------|
   |Núverandi tengivefslóð     |Tengivefslóð MF-félaga         |
   |Núgildandi fyrirtækiskenni     |Fyrirtækiskenni MF-félaga         |
   |Samstæðukenni     |Samstæðukenni MF-félaga         |
   |Nafn fyrirtækis     |Fyrirtækisheiti MF-félaga         |

* Skiptast á eftirfarandi sannvottunarstillingum svo að hægt sé að [!INCLUDE [prod_short](includes/prod_short.md)] sannvotta þegar hún tengist. Hver félagi getur fengið þessar upplýsingar í skráða forritinu sínu. Til að fræðast meira um hvernig á að búa til skráð forrit er farið í Búa til [skráð forrit í Azure-gátt](#create-a-registered-app-in-azure-portal).  

  * Biðlarakenni
  * Leyniorð biðlara
  * Endastöð tákn
  * Framsendingarvefslóð

Keyra skal uppsetning milli fyrirtækja,Aðgerðir,Sundurliðun  **·** **·** **tengingar í öllum fyrirtækjum til að tilgreina upplýsingarnar.**  

#### Búa til skráð forrit í Azure portal

Þetta ferli er aðeins nauðsynlegt ef tengja á við samstarfsaðila sem [!INCLUDE [prod_short](includes/prod_short.md)] er í öðrum leigjanda eða umhverfi.

> [!TIP]
> Það er góð hugmynd að hafa textaritil opna, svo sem Notepad, á meðan þú býrð til skráð forrit. Sumar upplýsingarnar eru nauðsynlegar þegar uppsetning milli fyrirtækja er keyrð,Aðgerðir **·** **,** Upplýsingar um **tengingu, svo gott er að hafa upplýsingarnar vel.**

1. Farðu á [Azure-hliðið](https://portal.azure.com/#home).
2.  **Microsoft Entra Velja skal kenniþjónustuna** .
3. Á yfirlitssvæðinu skal velja **Forritaskráningar**.
4. Á síðunni **Skráningar á forriti** skal velja **nýja skráningu**.
5. Gefðu forritinu heiti.
6.  **Velja skal reikninga í hvaða stjórnunarskrá sem er (Hvaða Microsoft Entra kenni leigjandi - Fjöltengill)** reikningstegund.
7. Í reitnum **Velja verkvang** skal velja **Vefur** fyrir framsendingarslóð og útvega URI. Til dæmis \**https://businesscentral.dynamics.com/OAuthLanding.htm**.

  Ef unnið er með ívafið isV gæti þurft aðra URI.

8. Skráðu forritið.
9. Á síðunni Milli-fyrirtækja **app** á yfirlitssvæðinu skal velja **API-heimildir**.
10. Veljið Aðgerðina **Bæta við heimild** .
11. Á flipanum **Microsoft API er** valið **Dynamics 365 Business Central**.
12. Á svæðinu **Biðja um API-heimildir** skal velja **Forritsheimildir** og velja **síðan API. ReadWrite.All** heimild.
13. Í forritinu Milli fyrirtækja **| API-heimildasíða**, veljið **stjórnunarsamþykkt veitingar fyrir aðgerðina Contoso** og veitið síðan samþykki.
14. Á yfirlitssvæðinu skal velja **Vottorð & leyndarmál**.
15. Veldu flipann **Leyndarmál biðlara** og veldu **svo Nýtt leyndarmál** biðlara.
16.  **Leyndarsvæðið** Bæta við biðlara er fært inn heiti á leyndarmálinu og tilgreint hvenær það rennur út.

  > [!NOTE]
  > Allir félagar sem eru í ólíku umhverfi verða að endurnýja leyndarmálið áður en það rennur út.

  > [!IMPORTANT]
  > Afrita kennið í reitnum **Virði** áður en MF-forritið er skilið **eftir | Vottorð & leyndarmál** síðan. Þú þarft það síðar og það verður ekki tiltækt eftir að þú yfirgefur síðuna. Líma til dæmis gildið í textaritli.

17. Á yfirlitssvæðinu skal velja **Yfirlit**.
18. Afrita gildið í reitnum Kenni **forrits** (biðlara). Líma til dæmis gildið í textaritli.
19. Veljið aðgerðina **Endastöðvar** og afritið svo gildið í reitnum **OAuth 2.0 táknendastöð (v2).** . Líma til dæmis gildið í textaritli.
20. Afrita gildið í reitnum **Kenni** leigjanda (leigjanda). Líma til dæmis gildið í textaritli.
21. Í tákngildinu sem var afritað skal skipta **fyrirtækjum** út fyrir gildið sem afritað var úr reitnum **Kenni skráasafns (leigjanda)** í fyrra skrefi.

#### Bæta við og virkja skráða forritið þitt í Business Central

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Microsoft Entra Forritaspjald** og velja síðan viðeigandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Sýsla** skal velja **Virkt**. 
4. Veljið aðgerðina **Samþykki styrks** . 
5. Í reitnum **Heimildasafn** skal velja **D365 INTERCOMPANY CE & DATA ACCESS IC CE** heimildasafn.

## Setja upp bókhaldslykil milli fyrirtækja

Allir félagar verða að nota sama bókhaldslykil milli fyrirtækja og varpa reikningunum í eigin bókhaldslykli á hann. Ef bókhaldslykill fyrirtækisins skilgreinir bókhaldslykil milli fyrirtækja fyrir fyrirtækisfélagana skal fylgja skrefunum í þessum hluta.

Ef XML-skrá sem inniheldur bókhaldslykil milli fyrirtækja er skrefunum fylgt í [Flytja inn eða út bókhaldslykil](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts) milli fyrirtækja.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Velja aðgerðina **MF-bókhaldslykill** .
3. Til að bæta við reikningum er eitt af eftirfarandi gert á síðunni **Bókhaldslykill** milli fyrirtækja:
    * Velja skal **Nýtt** og færa hvern reikning inn í línu á síðunni.  
    * Ef MF-bókhaldslykillinn verður eins og eða svipaður og venjulegi bókhaldslykillinn er hægt að láta fylla síðuna út sjálfkrafa með því að velja **Afrita frá bókhaldslykli** aðgerðina. Hægt er að breyta nýju línunni eins og þurfa þykir.
    * Hafi bókhaldslykill milli fyrirtækja verið settur upp fyrir samstillingarfélaga skal nota aðgerðina **Samstillingaruppsetning** til að afrita þá reikninga.

    > [!TIP]
    > Ef bókhaldslykill milli fyrirtækja er afritaður frá samstillingarfélaga er hægt að nota aðgerðina **Samstillingaruppsetning** til að uppfæra reikninga milli fyrirtækja með þeim breytingum sem félaginn gerir á þeirra.

Næsta skref er að varpa bókhaldslykli í bókhaldslykil milli fyrirtækja. Fræðast meira um [hvernig varpa má bókhaldslykli milli fyrirtækja í bókhaldslykil](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts) fyrirtækisins.

### Flytja inn eða út bókhaldslykil milli fyrirtækja

Samstillingarfyrirtækið getur samnýtt bókhaldslykil sinn með félögum með því að flytja það út í skrá. Félagar geta flutt skrána inn til að sækja bókhaldslykilinn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Velja aðgerðina **MF-bókhaldslykill** .
3. Á síðunni **Bókhaldslykill** milli fyrirtækja skal velja aðgerðina **Flytja inn/Flytja út** og velja svo annaðhvort **Flytja inn** eða **Flytja út**.
4. Velja skal skrána sem á að flytja inn eða flytja út.  

Síðan Bókhaldslykill **milli** fyrirtækja er fylltur út með nýjum eða breyttum fjárhagsreikningslínum samkvæmt MF-bókhaldslyklinum í skránni. Allar fyrirliggjandi, óskyldar línur á síðunni haldast óbreyttar.

## Varpa bókhaldslykli milli fyrirtækja á bókhaldslykil fyrirtækisins  

Þegar bókhaldslykill milli fyrirtækja hefur verið skilgreindur eða fluttur inn skal varpa hverjum millifyrirtækjareikningi með einum af reikningunum. Á síðunni **Bókhaldslykill milli fyrirtækja er tilgreint hvernig fjárhagsreikningar** milli fyrirtækja á innleið varpast á fjárhagsreikninga úr bókhaldslykli fyrirtækisins.

Ef millifyrirtækjareikningarnir og reikningarnir eru með sömu tölur er hægt að varpa reikningunum sjálfkrafa.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.  
2. Velja aðgerðina **MF-bókhaldslykill** .

    > [!TIP]
    > Til að fá aðgang að aðgerðum á síðunni gæti þurft að stækka síðuna í útlit útlitsins.

3. Á síðunni **Bókhaldslykill** milli fyrirtækja skal velja aðgerðina **Vörpun bókhaldslykils** .
4. Hægt er að varpa reikningunum handvirkt eða sjálfvirkt.

    * Til að stofna vörpunina handvirkt skal velja reikning í svæðunum MF-bókhaldslykill **og** fjárhagsbókhaldslykill **og velja svo reikning í fjárhagsnúmerinu**  **.** og **MF-nr.** Reitir
    * Til að varpa reikningum sem hafa sömu númerin sjálfkrafa skal velja línurnar sem á að varpa, velja Varpa á **reikning með sömu aðgerð og** velja síðan bókhaldslykilinn sem á að uppfæra.

    > [!TIP]
    > Ef varpa á mörgum eða kannski öllum reikningum skal velja línu, velja :::image type="icon" source="media/show-more-options-icon.png" border="false"::: og velja **svo Velja meira**.

## Setja upp víddir milli fyrirtækja

Ef félagar munu skiptast á færslum með víddum sem tengjast þeim skal koma sér saman um víddirnar sem allar verða notaðar. Til dæmis getur samstillingarfyrirtækið búið til einfaldaða útgáfu af víddum sínum, flutt þær út í XML-skrá og síðan dreift skránni til hvers félaga. Hver félagi getur flutt XML-skrána inn á síðunni **Millifyrirtækjavíddir** og varpað víddum milli fyrirtækja á víddir sínar. Fræðast meira um víddir milli fyrirtækja á [víddir](#map-intercompany-dimensions-to-your-companys-dimensions) fyrirtækisins.

> [!NOTE]
> Hvert fyrirtæki verður að varpa víddum sínum á víddir milli fyrirtækja fyrir fylgiskjöl á útleið og innsend skjöl. Vörpun reikninga í báðar áttir skiptir miklu máli og viðhalda samkvæmni þvert á fyrirtækin.

Ef félagar nota víddir samstillingarfélagans skal fylgja skrefunum í þessum hluta. Ef samnýta á með XML-skrá sem inniheldur MF-víddirnar er skrefunum fylgt í [Flytja inn eða út millifyrirtækjavíddir](#import-or-export-intercompany-dimensions).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.  
2. Velja aðgerðina **MF-víddir** .
3. Til að bæta við víddum er eitt af eftirfarandi gert á síðunni **Millifyrirtækjavíddir** :
    * Velja skal **Nýtt** og færa hverja vídd síðan inn í línu.  
    * Ef víddir milli fyrirtækja verða eins eða svipaðar og venjulegar víddir er hægt að fylla síðuna sjálfkrafa út með því að velja aðgerðina **Afrita úr víddum** . Síðan er hægt að breyta línunum eftir þörfum.
    * Hafi víddir milli fyrirtækja verið tilgreindar fyrir samstillingarfélaga skal nota aðgerðina **Samstillingaruppsetning** til að afrita þessar víddir.

    > [!TIP]
    > Ef víddir milli fyrirtækja eru afritaðar frá samstillingarfélaga er hægt að nota aðgerðina **Samstillingaruppsetning** til að uppfæra víddir milli fyrirtækja með þeim breytingum sem félaginn gerir á þeirra.  

### Flytja inn eða út víddir milli fyrirtækja  

Samstillingarfyrirtækið getur samnýtt víddir sínar með félögum með því að flytja þær út í skrá. Félagar geta flutt inn skrána til að sækja víddirnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Velja aðgerðina **MF-víddir** .  
3. Á síðunni **Millifyrirtækjavíddir** skal velja aðgerðina **Flytja inn/Út** og velja svo annaðhvort **Flytja inn** eða **Flytja út**.
4. Velja skal skrána sem á að flytja inn eða flytja út.

Næsta skref er að varpa víddunum með víddum milli fyrirtækja. Fræðast meira um víddir milli fyrirtækja á [víddir](#map-intercompany-dimensions-to-your-companys-dimensions) fyrirtækisins.

### Varpa víddum milli fyrirtækja á víddir fyrirtækisins

Þegar búið er að tilgreina víddirnar sem á að nota skal varpa hverri millifyrirtækjavídd með einni af víddum fyrirtækisins og öfugt. Nota síðuna **Vörpun** milli fyrirtækjavídda til að tilgreina vörpunina. Síðan er ferlið endurtekið fyrir víddargildin.

* Tilgreina hvernig millifyrirtækjavíddir í færslum á innleið varpast á víddir af lista fyrirtækisins yfir víddir.
* Tilgreina hvernig víddirnar verða túlkaðar sem millifyrirtækjavíddir í færslum *á* útleið.

Ef einhver af víddunum milli fyrirtækja hefur sama kóta og samsvarandi víddir í fyrirtækinu er hægt að varpa víddunum sjálfkrafa.  

Í eftirfarandi skrefum er MF-víddum fyrst varpað á víddir fyrir innsend skjöl á svæðinu **Millifyrirtækjavíddir** . Síðan er víddum varpað á víddir milli fyrirtækja fyrir skjöl á svæðinu **Núverandi víddir fyrirtækis** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Velja aðgerðina **MF-víddir** .
3. Á síðunni **Millifyrirtækjavíddir** skal velja aðgerðina **Vörpun vídda** .
4. Hægt er að varpa víddunum handvirkt eða sjálfvirkt.

    * Til að stofna vörpunina handvirkt skal velja **vídd á svæðunum Millifyrirtækjavíddir** og **Gildandi víddir** fyrirtækja og velja síðan vídd í reitunum **Víddarkóti** og **MF-víddarkóti** .
    * Til að varpa víddum sem hafa sama kóta sjálfvirkt skal velja línurnar sem á að varpa, velja **Varpa víddum með sömu kótaaðgerð** og velja síðan víddirnar sem á að uppfæra. 

    > [!TIP]
    > Ef varpa á mörgum eða kannski öllum víddum skal velja línu, velja :::image type="icon" source="media/show-more-options-icon.png" border="false"::: og velja **svo Velja meira**.

5. Veljið aðgerðina **Vörpun** víddargilda.
6. Á síðunni **Vörpun** víddagilda milli fyrirtækja eru skrefin til að stofna vörpunina svipuð því sem var gert fyrir víddir.

## Setja upp sniðmát og keyrslur milli fyrirtækjabóka

Setja verður upp færslubókarsniðmát og færslubókarkeyrslu til að nota sjálfgefið fyrir færslur milli fyrirtækja. Sniðmátið og keyrslan skipta sérstaklega miklu máli ef milli-fyrirtækjafærslur eru samþykktar sjálfvirkt frá félögunum. Til að fá nánari upplýsingar um sjálfvirka samþykkt færslna er farið í [Sjálfvirk viðskipti frá milli-fyrirtækjafélögum](#auto-accept-transactions-from-intercompany-partners).   

* Færslubækur eru notaðar til að bóka á fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna- og lánardrottnareikninga. Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum.  Nota síðuna Færslubók **milli fyrirtækja** til að setja upp færslubókarkeyrslu sem á að nota. Stillingarnar sem eiga sérstaklega við millifyrirtækjafærslur eru reikningarnir sem tilgreindir eru í reitunum **MF-reikningstegund** og **MF-reikningur nr** .
* Bókasniðmát gefa færslubókarsíðu sem er hönnuð til sérstakra nota. Þá eru nákvæmlega þeir reitir í bókarsniðmátum sem þörf er á í tilteknum hluta kerfisins. Nota síðuna **Sniðmát færslubóka** til að setja upp sniðmát til að nota fyrir færslur milli fyrirtækja.

Nánari upplýsingar um færslubókarsniðmát og keyrslur er farið í [Nota bókarsniðmát og keyrslur](ui-work-general-journals.md#use-journal-templates-and-batches).

## Setja upp fyrirtæki fyrir færslur milli fyrirtækja

Eftirfarandi skref gera ráð fyrir því að samstillingarfélagi sé settur upp með bókhaldslyklinum og víddunum sem bókhaldslykill og víddir milli fyrirtækja byggjast á. Þú getur sett þær upp sjálfur, en það er yfirleitt fljótlegra að byrja og viðhald er auðveldara, að nota samstillingarfélaga. Nánari upplýsingar um samstillingarfélagann fást með því að fara í [Setja upp samstillingarfélaga](#set-up-a-synchronization-partner).

> [!TIP]
> Mælt er með því að fylla út reitina á flýtiflipanum **Almennt** á síðunni **Uppsetning** milli fyrirtækja fyrir hvern félaga áður en félögum þeirra er bætt við. Þegar samstarfsfyrirtækjum er bætt við fyrir sama leigjanda [!INCLUDE [prod_short](includes/prod_short.md)]  fær MF-kótinn og heiti fyrirtækisins úr uppsetningunni á flýtiflipanum Almennt. Reiturinn **Heiti** fyrirtækis staðfestir að MF-kóti þeirra sé eingildur.

> [!NOTE]
> Ef nota á samstillingarfélaga er reiturinn **Samstillingarfélagi** hafður auður þegar fyrirtækið er sett upp fyrir félagann.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.  
2. Fyllt er í reitina á flýtiflipanum **Almennt á síðunni** Uppsetning **milli fyrirtækja** . [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Á [!INCLUDE[prod_short](includes/prod_short.md)] netinu er ekki hægt að nota staðsetningar skráa til að flytja færslur til félaga vegna þess [!INCLUDE[prod_short](includes/prod_short.md)] að ekki er hægt að komast inn á staðarnetið. Ef þú velur **Staðsetning skráar** í reitnum **Flutningsgerð**, er **Möppuslóð** ekki í boði. Þess í stað verður skránni sótt í **niðurhalsmöppuna** á tölvunni. Þú sendir síðan skrána til einhvers í samstarfsfyrirtækinu, til dæmis í tölvupósti. Til að fá beinar ferli mælum við með því að þú velur **Email**.

Næsta skref er að setja upp samstarfsfyrirtækin.

## Setja upp félaga milli fyrirtækja

Hver félagi verður að bæta öllum öðrum fyrirtækjum við samstarfið sem félaga.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Á flýtiflipanum **Millifyrirtækjafélagar** skal velja **Bæta við**.
3. Fyllt er í reitina á síðunni **MF-félagi** . [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Þrep 2 og 3 eru endurtekin fyrir öll fyrirtæki í samstarfinu.

> [!NOTE]
> Ef kveikt er á víxli sjálfvirkrar færslu **á**  **síðunni** Millifyrirtækjafélagi [!INCLUDE[prod_short](includes/prod_short.md)] bætir skilaboðum sem vara við innkaupareikningum sem afrita upphaflegu innkaupapöntunina. Brýnt er að hafa viðskiptaferli við umsjón tvítekninga. Til dæmis með því að eyða slíkum innkaupapöntunum þegar innkaupareikningurinn berst frá millifyrirtækjafélaga.

### Setja upp félaga milli fyrirtækja sem viðskiptamenn og lánardrottna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Á flýtiflipanum **Millifyrirtækjafélagar** er spjaldsíða félagans opnuð.
3. Eftir því hvað á að gera skal velja viðskiptamanninn eða félagann í reitnum Númer viðskiptamanns **.** eða **Nr.**  lánardrottinsSvæði.

    > [!NOTE]
    > Hafi viðskiptamaður eða lánardrottinn ekki verið stofnaður er hægt að velja **+Nýtt** í fellivalmyndinni til að setja þá upp. Nánari upplýsingar um stofnun viðskiptamanna og lánardrottna eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md) og [Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > Einnig er hægt að tilgreina viðskiptamann eða lánardrottin sem MF-félaga með því að fylla út reitinn **Kóti** MF-félaga á síðunum **Viðskiptamannaspjald** og **Lánardrottnaspjald** .

### Setja upp sjálfgefna fjárhagsreikninga milli fyrirtækjafélaga  

Þegar sölu- eða innkaupalína milli fyrirtækja er stofnuð til að senda sem færslu á útleið er færður inn reikningur úr MF-bókhaldslyklinum sem sjálfgildi fyrir hvaða reikning í fyrirtæki félagans upphæðin er bókuð á. Á síðunni **Fjárhagsspjald**, fyrir reikninga sem reglulega eru notaðir í sölu- eða innkaupalínum á útleið, er hægt að tilgreina sjálfgefinn fjárhagsreikning milli fyrirtækjafélaga. Til dæmis er hægt að færa inn samsvarandi safnreikning lánardrottna úr MF-bókhaldsreikningi fyrir safnreikninga viðskiptamanna. Safnreikningarnir og gjaldfallnar skuldir eru notaðir sem óstillingareikningur fyrir MF-félagann þegar færslur eru bókaðar í færslubækur milli fyrirtækja.  

Þegar fjárhagsreikningur er síðan færður inn í reitinn **Nr. Mótreiknings** í línu milli fyrirtækja með **MF-félaga** í reitnum **Tegund reiknings** er sjálfkrafa fyllt í reitinn **MF-félagi fjárhagsreikningur**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Fjárhagsreikningurinn sem notaður er fyrir færslur milli fyrirtækja er opnaður og í reitnum **Fjárhagsreikningur MF-félaga er færður inn fjárhagsreikningur** MF-félagans sem félaginn bókar á þegar bókað er á fjárhagsreikninginn í línunni.
3. Skref 2 er endurtekið fyrir hvern reikning sem oft er færður inn í reitinn **Mótreikningur nr.** í línu í færslubók eða fylgiskjali milli fyrirtækja.

### Samþykkja færslur sjálfvirkt frá MF-félögum

Til að gera það hraðar til að vinna færslur milli fyrirtækja er hægt að tilgreina að stofna eigi færslubókarlínur sjálfkrafa byggðar á færslum MF-félaga af síðunni **MF-færslubók** . Til að stofna færslur á innleið og útleið sjálfvirkt þarf að kveikja á eftirfarandi vífærslum fyrir hvern félaga:

* Á síðunni **Uppsetning** milli fyrirtækja skal kveikja á víxli **sjálfvirkt. Senda** víxl fyrir samstillingarfélagann. Síðan er tilgreint hvar á að stofna mótteknar millifyrirtækjabókarfærslur með því að fylla út reitina **Sjálfg. MF-færslubókarsniðmát** og **Sjálfg. MF-færslubókarkeyrsla** .

    > [!TIP]
    > Ef reiturinn **Sjálfg. MF-færslubókarsniðmát** er auður þarf að setja upp færslubókarsniðmát til að nota fyrir millifyrirtækjabækur. Nánari upplýsingar um sniðmát og keyrslur er farið í [Setja upp sniðmát færslubóka og keyrslna milli fyrirtækja](#set-up-intercompany-general-journal-templates-and-batches)    

* Á síðunni **Millifyrirtækjafélagi** skal kveikja á víxlinu **Sjálfvirk samþykktar færslur** .

Færslubókarlínur eru stofnaðar fyrir þig en ekki bókaðar.

> [!NOTE]
> Ef fyrirtækið þitt notaði eiginleika innan samstæðu í [!INCLUDE [prod_short](includes/prod_short.md)] á undan 2022 útgáfutímabili 1 til að samþykkja færslur sjálfkrafa þarf stjórnandinn þinn að kveikja á eiginleikanum **Samþykkja almennar færslubókarfærslur innan samstæðu sjálfkrafa** á síðunni **Eiginleikastjórnun**.

### Tilgreina bankareikninga sem nota á fyrir MF-félaga

Til að auðvelda hraðgreiðslur þarf að tilgreina einn eða fleiri bankareikninga sem nota á fyrir MF-félaga. Þegar félagi notar færslubók milli fyrirtækja til að greiða er hægt að tilgreina bankareikninginn í línunni. Bankareikningurinn er notaður sem mótreikningur í fyrirtæki móttöku, sem minnkar þörfina á að færa færslur handvirkt inn.

* Á síðunni MF-félagar er aðgerðin Bankareikningar **valin** til að tilgreina bankareikning sem á að nota á síðunni **MF-félagar** . Reikningsupplýsingarnar eru færðar inn á **bankareikningsspjald** milli fyrirtækja.

## Úrræðaleit vegna uppsetningar milli fyrirtækja

Á síðunni **MF**-uppsetningargrunnur **inniheldur svæðið Greiningargreining milli fyrirtækja** reiti sem gefa til kynna hvort allir íhlutir sem þarf til að skiptast á færslum milli fyrirtækja hafa verið settir upp. Flísarnar eru einnig tiltækar í Hlutverkamiðstöð viðskiptastjóra. Veldu flísar til að komast að því hvað vantar. Til að fá yfirlit yfir íhlutina sem þarf er farið [í Yfirlit yfir verkstigin til að hefjast handa](#overview-of-the-steps-to-get-started).

## Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
