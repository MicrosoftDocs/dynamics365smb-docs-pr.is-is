---
title: Setja upp bókun millifyrirtækjafærslu
description: Lærðu að setja upp samstæðusamstarf.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 09/27/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621'
---
# Setja upp samstæðufærslur

Með samstæðusamstarfi er auðveldara að halda utan um bókhaldsferla þegar tvö eða fleiri dótturfélög eiga oft viðskipti við hvort annað. Samstarfsaðilar geta gengið að viðskiptum, svo sem sölu og innkaupum, og meðhöndlað þá annaðhvort handvirkt eða sjálfvirkt. Til dæmis, þegar félagi sendir sölubókarlínu til annars samstarfsaðila, er stofnuð innkaupalína fyrir viðtökufélagana.

Bókhaldslykillinn getur t.d. verið útgáfa af bókhaldslykli samstillingar félaga. Sérhver samstarfsaðili kortvarpar reikninga sína á bókhaldslykil samstæðunnar. Hver samstarfsaðili varpar einnig inn víddum og víddargildum á víddir milli fyrirtækja.

> [!NOTE]
> Í 2023 út bylgjan 1 við höfum kynnt okkur bætta  **uppsetningu Samstæðuuppsetningar** . Nýja síðan auðveldar uppsetningu samstæðusamstarfs með því að sameina öll uppsett verk á einni síðu. Ef þú ert nýbúinn  [!INCLUDE [prod_short](includes/prod_short.md)] þá ertu nú þegar að nota nýja upplifunina. Ef viðskiptavinur er til staðar getur kerfisstjóri kveikt á aðgerðum í  **almennu færslubókarhreyfingum sjálfkrafa til að samþykkja MF-færslur**  innan samstæðu á  **síðu aðgangsstjórnunar** .
>
> Verkin í þessari grein gera ráð fyrir að kveikt sé á aðgangsrofi. Ef þú ert búinn að setja upp samstæðusamstarf er hægt að nota það áfram.

## Verður að byrja fyrir

Áður en hafist er handa við að setja upp samstæðusamstarf hafa verið teknar nokkrar ákvarðanir til að gera.

|Ákvörðun  |Heimildasamstæða  |
|---------|---------|
|Hvaða bókhaldslykla á að vera grunnur að bókhaldslykli samstæðunnar?     | Öll fyrirtæki í samstarfinu verða að nota bókhaldslykil MF-samstæðu. Hægt er að byggja bókhaldslykil milli fyrirtækja á bókhaldslyklum frá einu fyrirtækjanna í samstarfinu eða stofna nýjan bókhaldslykil innan samstæðu. Lyklar sem nota á eru notaðir í samnýtingu á báða vegu þannig að hver félagi sendir bæði og tekur við færslum á réttum reikningum. Frekari upplýsingar um uppsetningu bókhaldslykils milli fyrirtækja í  [samstæðulínuritum lykla](#set-up-the-intercompany-charts-of-accounts).         |
|Hvaða víddir eiga að vera undirstaða samstæðuvíddanna?     | Ef víddir MF eru notaðar verða þær að vera þær sömu fyrir öll fyrirtækin í samstarfinu. Þegar víddir milli fyrirtækja eru tilgreindar skal varpa víddargildum þeirra. Frekari upplýsingar um vörpun víddargilda til að  [Setja upp víddir](#set-up-intercompany-dimensions) milli fyrirtækja.        |
|Hvaða samstarfsaðilar eru viðskiptamenn eða Lánardrottnar, eða hvort tveggja?     |  Frekari upplýsingar um uppsetningu viðskiptamanna og lánardrottna fyrirtækja í samstæðusamstarfi á  [að setja upp samstæðufélaga sem viðskiptavini og lánardrottna](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Á að tilgreina bankareikninga til að nota í samstarfinu?| Hægt er að flýta ferlinu við að skrá greiðslufærslur með því að tilgreina bankareikning sem á að nota fyrir hvert samstarfsfyrirtæki.  [Frekari upplýsingar eru tilgreindar í bankareikningum til að nota fyrir samstæðufélaga](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Hvernig á að auðkenna fyrirtækin í samstarfinu?     | Allir aðilar verða að vera sammála um einstakan auðkenniskóða félaga innan samstæðu hvers fyrirtækis. Kótanum er úthlutað á viðskiptamanna-og lánardrottnaspjöld til að auðkenna tengdar færslur. Frekari upplýsingar um auðkenni eru stofnaðar í  [númeraröð](ui-create-number-series.md).        |
|Hvernig á að meðhöndla vörunúmera?     | Ef vörur í samstæðu innihalda atriði er annaðhvort hægt að nota eigin vörunúmer eða setja upp vörunúmer félaganúmera fyrir hverja vöru, annað hvort í reitnum  **Vörunr.** svæðinu eða í  **sameiginlegum vörulið nr.** á birgðaspjaldinu. Einnig er hægt að nota  **tilvísunaraðgerðina vörutilvísun**  til að varpa vörunúmerum á MF-félaga-lýsingu á vörunum. Til að fræðast meira um vöruvísanir er farið í að  [nota vörutilvísanir](inventory-how-use-item-cross-refs.md).        |
|Eru auðlindir í viðnum?     | Ef tilföng innan samstæðu verða með forða er fyllt út í  **MF-félagafærslum. Nr.**  Fjárhagsreikn.á forðaspjaldinu fyrir hvern forða. Í þessum reit er númer þess fjárhagslykils samstæðu sem upphæðin fyrir þennan forða verður bókuð á í félagafélaginu. Til að fræðast meira um tilföng er farið að  [Setja upp tilföng](projects-how-setup-resources.md).<br><br>**Athugið**<br>Innkaupafærslur milli fyrirtækja sem innihalda tilföng, eignir og vörugjöld eru ekki studdar að fullu. Í félagasamfélaginu er  **reiturinn Tegund**  línu auður í innkaupaskjalslínum sem innihalda þessa aðila. Uppfæra þarf reitinn handvirkt.        |

## Yfirlit yfir skrefin til að komast af stað

 **Notaðu síðuna Samstæðuuppsetning**  til að setja upp eftirfarandi íhluti í samstæðufærslum:

* Samstæðustillingar fyrirtækisins.
* Fyrirtækið sem verður samstillingarfélaginn.
* Bókhaldslyklar milli fyrirtækja sem allir sem hann félagar nota til að skiptast á færslum.
* Varpanir á milli lykla í bókhaldslykli og bókhaldslykli milli fyrirtækja fyrir inn-og útfærslur fyrir hvert félagatal.
* Víddir milli fyrirtækja og víddargilda sem á að nota og hvernig þær eru kortlagðar í víddum fyrir hvert félagatal.
* Félög sem eru aðilar samstæðunnar.
* Félög sem eru Lánardrottnar eða viðskiptamenn, eða hvort tveggja.

## Setja upp samstillingarfélaga

Allir samstarfsaðilar verða að nota bókhaldslykil milli fyrirtækja og, ef þörf krefur, sömu MF-víddir. Hægt er að vista tíma þegar samstarfið er sett upp með því að nota bókhaldslykla og víddir fyrir einn af félögunum sem grunnlínu fyrir bókhaldslykil og víddir milli fyrirtækja. Fyrirtækið sem notað er sem Grunnlína er kallað  *samstillingarfélaginn*. Algengast er að samstillingarfélaginn sé fyrirsvarsfélagið en þarf ekki að vera það.

 **Á síðu Samstæðuuppsetningarinnar**  Tilgreinir hver samstarfsaðili samstillingarfélagana í  **reitnum samstillingarfélagi** . Á eftir eru bókhaldslyklar milli fyrirtækja og samstæðuvíddir sjálfkrafa tilgreindar fyrir þær á grundvelli uppsetningar samstillingarfélaganna. Félagarnir nota  **síðan bókhaldslykil**  milli fyrirtækja og  **vörpun MF-vídda**  til að varpa bókhaldslykli þeirra og víddum á bókhaldslykil milli fyrirtækja og vídda og öfugt. 

> [!NOTE]
> Mikilvægt er að kortleggja reikninga og víddir í báðar áttir. Það er, bæði á bókhaldslykil milli fyrirtækja og í víddum, og úr þeim á eigin lykla og víddir.

### Tengja saman samstarfsaðila í öðrum leigjanda eða umhverfi

Ef eitt eða fleiri samstarfsverkefni  [!INCLUDE [prod_short](includes/prod_short.md)]  eru í öðru leigjanda eða umhverfi eru nokkur aukaskref til að skapa tenginguna. Þrepin eiga við um alla samstarfsaðila í öðrum leigjanda eða umhverfi hans.

* Sett upp  [!INCLUDE [prod_short](includes/prod_short.md)]  sem skrásett App í Azure Portal.
* Bæta við og virkja App skráningu í [!INCLUDE [prod_short](includes/prod_short.md)].
* Skiptast á upplýsingum um samstæðuuppsetningar sínar. Hver félagi getur fengið þessar upplýsingar úr uppsetningarleiðbeiningum MF-félaga á  **milli-umhverfi** .

   |Afritun úr uppsetningu félaganna  |Afrita í uppsetninguna  |
   |---------|---------|
   |Núverandi tengivefslóð     |Tengivefslóð MF-félaga         |
   |Núgildandi fyrirtækiskenni     |Fyrirtækiskenni MF-félaga         |
   |Samstæðukenni     |Samstæðukenni MF-félaga         |
   |Nafn fyrirtækis     |Fyrirtækisheiti MF-félaga         |

* Skiptast á eftirfarandi sannvottunarstillingar þannig að hægt sé að  [!INCLUDE [prod_short](includes/prod_short.md)]  staðfesta hvenær það tengist. Hver félagi getur fengið þessar upplýsingar úr skráðu forriti sínu. Til að fræðast nánar um hvernig á að búa til skrásett App skaltu fara að búa til  [skrásett App í Azure Portal](#create-a-registered-app-in-azure-portal).  

  * Biðlarakenni
  * Leyniorð biðlara
  * Endastöð tákins
  * Framsendingarvefslóð

Keyrið leiðbeiningar um  **uppsetningu á Milliumhverfi**  MF-félaga í öllum fyrirtækjum til að tilgreina upplýsingarnar. Til að ræsa leiðbeiningarnar, á  **síðu MF-félaga**, er Uppsetningaraðgerðin  **tengja utan á milli notuð** .

#### Búðu til skrásett App í Azure Portal

Þetta ferli er einungis nauðsynlegt ef tengja skal saman samstarfsaðila  [!INCLUDE [prod_short](includes/prod_short.md)]  sem eru í öðru leigjanda eða umhverfi.

> [!TIP]
> Það er góð hugmynd að hafa textaritinn opinn, eins og Notepad, á meðan þú býrð til skrásett App. Eitthvað af upplýsingunum er nauðsynlegt þegar Uppsetningarleiðbeiningar MF-  **félaga eru keyrðar**  og því er gott að hafa upplýsingarnar handhægar.

1. Fara á  [Azure Portal](https://portal.azure.com/#home).
2.  **Microsoft Entra Veldu kenni**  þjónustu.
3. Í skoðunarrúðu er hægt að velja  **forritskráningar**.
4.  **Veldu**  nýja skráningu  **á síðunni App skráningar**.
5. Gefðu forritinu nafn.
6. Velja skal lykla í hvaða fyrirtækjaskrá sem er  **(hvers kyns  Microsoft Entra  reikningagerð leigjanda)** .
7. Fyrir áframakið URI, í  **Velja pallasvæði**, velja  **vef** og veita síðan URI. Til dæmis \**https://businesscentral.dynamics.com/OAuthLanding.htm**.

  Ef þú ert að vinna með ígræðsla ÍSS gætir þú þurft annan URI.

8. Skrá app.
9.  **API-heimildir**  á síðu MF-forritsins  **, á skoðunarrúðunni, er valið**.
10.  **Veldu aðgerðina bæta við heimild** .
11.  **Á flipanum Microsoft API**  er valið **Dynamics 365 Business Central**.
12.  **Í glugganum biðja um API-heimildarúðuna**  er valið  **beitarheimildir** og síðan er  **valið API. Lesiskrift. öll**  leyfi.
13.  **Á MF-App | API heimildasíða**, velja  **samþykki styrkþega fyrir contoso**  Action og veita síðan samþykki.
14. Á Yfirlitssvæði er valið  **vottorð & leyndarmál**.
15.  **Flipinn biðlararitarar**  er valinn og síðan er nýr viðskiptavinur  **valinn**.
16. Í svæðinu  **Bæta við leyniglugganum**, skal færa inn nafn leynis og tilgreina hvenær það rennur.

  > [!NOTE]
  > Allir samstarfsaðilar sem eru í ólíku umhverfi verða að endurnýja leyndarmálið áður en það rennur út.

  > [!IMPORTANT]
  > Afrita á KENNIÐ í  **reitnum gildi**  áður en hægt er að  **yfirgefa MF-App | Vottorð & ritar**  bls. Þú þarft hana í seinna skrefi og verður ekki laus eftir að þú ferð af síðunni. Til dæmis skal líma gildið í textaritli.

17. Í skoðunarrúðunni er valið  **Yfirlit**.
18. Afritið gildið í  **REITNUM kenni**  forrits (biðlara). Til dæmis skal líma gildið í textaritli.
19.  **Veljið endapunkta**  aðgerðar og afritið síðan gildið í  **reitnum oauth 2,0 táknarendastöðin (v2)** . Til dæmis skal líma gildið í textaritli.
20. Afritið gildið í  **reitnum skráasafn (leigjandi)** . Til dæmis skal líma gildið í textaritli.
21. Í gildi táknrita er skipt út  **stofnunum**  með gildið sem afritað var af  **kennireitnum**  skráasafn (leigjandi) í fyrra þrepi.

#### Bæta við og gera þitt skráða App í viðskiptum miðsvæðis

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn  **Microsoft Entra  Umsóknarkort** og veldu síðan tengda tengilinn.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3.  **Í reitnum Staða**  er valið  **virkt**. 
4. Velja skal  **aðgerðina veita samþykki** . 
5. Í reitnum leyfi sett  **er valið**  API-Cross umhverfis-og  **Samstæðuleyfi í samstæðu** .

## Setja upp bókhaldslykla milli fyrirtækja

Allir félagar verða að nota bókhaldslykil MF-samstæðu og varpa reikningunum í bókhaldslykil þeirra. Ef Bókhaldslykill fyrirtækisins skilgreinir bókhaldslykil samstæðunnar fyrir félagasamfélögin skal fylgja skrefunum í þessum kafla.

Ef notað er XML-skrá sem geymir bókhaldslykil milli fyrirtækja skal fara eftir skrefunum í  [innflutningi eða útflutningi bókhaldslykils](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Velja skal  **aðgerðina MF-bókhaldslykil** .
3. Til að bæta við lyklum skal gera einn af eftirfarandi á  **bókhaldslykli**  samstæðu-síðu:
    * Veldu  **nýtt** og þá færðu inn hvern lykil á línu á síðunni.  
    * Ef MF-bókhaldslykillinn verður eins og eða svipaður og venjulegi bókhaldslykillinn er hægt að láta fylla síðuna út sjálfkrafa með því að velja **Afrita frá bókhaldslykli** aðgerðina. Hægt er að breyta nýju línunni eins og þurfa þykir.
    * Ef sett hefur verið upp Bókhaldslykill milli fyrirtækja fyrir samstillingarfélaga skal nota  **aðgerðina Uppsetning**  samstillingar til að afrita þá reikninga.

    > [!TIP]
    > Ef Bókhaldslykill milli fyrirtækja er afritaður úr samstillingarfélagi er hægt að nota  **aðgerðina Uppsetning**  samstillingar til að uppfæra samstæðureikningana með öllum breytingum sem félaginn gerir með þesum.

Næsta skref er að varpa bókhaldslykli á bókhaldslykla milli fyrirtækja. Frekari upplýsingar á  [varpa bókhaldslykil milli fyrirtækja í bókhaldslykil](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts) fyrirtækisins.

### Flytja inn bókhaldslykil eða flytja út eða út

Samstillingarfyrirtækið getur samnýtt bókhaldslykil sinn með samstarfsaðilum með því að flytja það út í skrá. Félagar geta flutt inn skrána til að fá bókhaldslykilinn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Velja skal  **aðgerðina MF-bókhaldslykil** .
3.  **Á síðunni bókhaldslykil**  fyrirtækja skal velja  **aðgerðina innflutningur/útflutningur**  og velja  **síðan innflutning**  eða  **útflutning**.
4. Veldu skrána sem á að flytja inn eða út.  

 **Síða MF-bókhaldslykils**  er fyllt út með nýjum eða Ritstýrð fjárhagsreikningslínum samkvæmt bókhaldslykli samstæðunnar í skránni. Allar fyrirliggjandi, óskyldar línur á síðunni haldast óbreyttar.

## Varpa bókhaldslykli milli fyrirtækja á bókhaldslykil fyrirtækisins  

Þegar bókhaldslykill milli fyrirtækja hefur verið skilgreindur eða fluttur út skal varpa hverjum samstæðureikningi í einn reikninga.  **Á síðunni Bókhaldslykill**  milli fyrirtækja er hægt að tilgreina hvernig fjárhagsreikningar milli fyrirtækja í færslum á innleið eiga að vera á fjárhagsreikningum í bókhaldslyklum fyrirtækisins.

Ef samstæðureikningarnir og reikningarnir hafa sömu númer er hægt að varpa lyklum sjálfkrafa.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.  
2. Velja skal  **aðgerðina MF-bókhaldslykil** .

    > [!TIP]
    > Til að komast í aðgerðir á síðunni gæti þurft að útvíkka síðuna til að skoða yfirlit yfir breiða uppsetningu.

3.  **Á síðunni Bókhaldslykill**  milli fyrirtækja er hægt að  **Velja vörpun**  bókhaldslykils.
4. Hægt er að varpa lyklum handvirkt eða sjálfvirkt.

    * Til að stofna handvirkt vörpun þarf að velja lykil á  **milli MF-bókhaldslykils**  og  **fjárhagsbókhaldslykils**, og velja svo lykil í reitnum  **fjárhags nr.** Og  **MF nr.** Reitir
    * Til að varpa sjálfkrafa upp lyklum sem hafa sömu númer skaltu velja línurnar sem á að varpa, velja  **kortið í Reikn. með sömu**  aðgerð og velja síðan bókhaldslykla sem á að uppfæra.

    > [!TIP]
    > Ef þú vilt varpa mörgum eða kannski öllum lyklum skaltu velja línu, velja  :::image type="icon" source="media/show-more-options-icon.png" border="false"::: og velja síðan  **Velja nánar**.

## Setja upp samstæðuvíddir

Ef samstarfsaðilar skiptast á færslum með víddum sem tengjast þeim eru það sammála víddunum sem allir munu nota. Til dæmis getur samstillingarfyrirtækið stofnað einfalda útgáfu af víddunum, flutt þær út í XML-skrá og síðan dreift skránni til hvers samstarfsaðila. Hver félagi getur flutt inn XML-skrána á  **síðu MF-vídda**  og varpað því næst samstæðuvíddunum á víddir sínar. Frekari upplýsingar um  [vörpun MF-vídda í víddir](#map-intercompany-dimensions-to-your-companys-dimensions) fyrirtækisins.

> [!NOTE]
> Hvert fyrirtæki verður að varpa víddunum á víddir milli fyrirtækja fyrir útsend skjöl og móttekin skjöl. Vörslureikningar í báðar áttir eru mikilvægir og hjálpa til við að viðhalda samræmi á milli fyrirtækjanna.

Ef samstarfsaðilar vilja nota samstæðuvíddir samstillingar félaga er fylgt skrefunum í þessum kafla. Ef samnýta á notkun á XML-skrá sem inniheldur víddir milli fyrirtækja er fylgt eftir skrefum í  [innflutningi eða útflutningi samstæðuvídda](#import-or-export-intercompany-dimensions).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.  
2. Velja skal  **aðgerðina MF-víddir** .
3. Til að bæta við víddum er eitt af eftirfarandi á  **síðunni MF-víddir** :
    * Velja  **skal nýtt** og færa síðan inn hverja vídd í línu.  
    * Ef millifyrirtækjavíddirnar verða samskonar eða svipaðar og venjulegu víddirnar þínar er hægt að fylla út á síðunni sjálfkrafa með því að  **Velja afritið úr aðgerðinni víddir** . Á eftir er hægt að breyta línunum eftir þörfum.
    * Ef víddir á milli fyrirtækja hafa verið tilgreindar fyrir samstillingarfélaginn er Uppsetningaraðgerð Samstillingaruppsetningar  **notuð**  til að afrita þær víddir.

    > [!TIP]
    > Ef víddir milli fyrirtækja eru afritaðar frá samstillingarfélagi er hægt að nota  **aðgerðina Uppsetning**  samstillingar til að uppfæra víddir milli fyrirtækja með öllum breytingum sem félagið gerir á þesum.  

### Flytja inn eða út víddir fyrirtækja  

Samstillingarfyrirtækið getur samnýtt víddir sínar með samstarfsaðilum með því að flytja þær út í skrá. Félagar geta flutt skrána inn til að fá víddirnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Velja skal  **aðgerðina MF-víddir** .  
3.  **Á síðunni millifyrirtækjavíddir**  er valin  **aðgerðin innflutningur/útflutningur**  og síðan er annað hvort  **valið innflutningur**  eða  **útflutningur**.
4. Veldu skrána sem á að flytja inn eða út.

Næsta skref er að varpa víddunum með MF-víddum. Frekari upplýsingar um  [vörpun MF-vídda í víddir](#map-intercompany-dimensions-to-your-companys-dimensions) fyrirtækisins.

### Varpa víddum milli fyrirtækja á víddir fyrirtækisins

Þegar víddirnar sem á að nota eru tilgreindar skal varpa hverri MF-vídd með einni af víddum fyrirtækisins og öfugt. Nota skal  **síðuna víddir millifyrirtækjsvörunar**  til að tilgreina vörpun. Eftir á skal endurtaka ferlið fyrir víddargildin.

* Tilgreinið hvernig MF-víddir í færslum á innleið eiga að vera í víddum af lista yfir fyrirtæki af víddum fyrirtækisins.
* Tilgreina hvernig víddir verða þýddar á MF-víddir í færslum  *á* útleið.

Ef einhver MF-víddir hafa sama kóta og samsvarandi víddir í fyrirtækinu er hægt að varpa víddunum sjálfkrafa.  

Í eftirfarandi skrefum eru fyrst að varpa MF-víddum á víddir fyrir skjöl á innleið í  **MF-víddrúðunni** . Síðan er hægt að varpa víddum á víddir milli fyrirtækja fyrir útsend skjöl  **í gildandi rúðunni fyrirtækjavíddir** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2. Velja skal  **aðgerðina MF-víddir** .
3.  **Á síðunni millifyrirtækjavíddir**  er valin  **aðgerðin víddarvörpun** .
4. Hægt er að varpa víddunum handvirkt eða sjálfvirkt.

    * Til að stofna handvirkt vörpun þarf  **·**  **·**  að velja vídd og velja síðan vídd í  **reitunum disa. kóti**  og  **MF-Dim.** 
    * Til að varpa sjálfkrafa í víddir sem hafa sama kóta skal velja línurnar sem á að varpa, velja  **síðan víddir korts með sömu kóðaðgerðinni**  og velja síðan víddirnar sem á að uppfæra. 

    > [!TIP]
    > Ef þú vilt varpa mörgum eða ef til vill öllum víddum skaltu velja línu, velja  :::image type="icon" source="media/show-more-options-icon.png" border="false"::: og velja síðan  **Velja nánar**.

5.  **Velja vörpun**  víddargilda.
6.  **Á vörpun**  síðna MF-víddargilda eru skrefin til að búa til vörpun svipuð því sem gert var fyrir víddir.

## Setja upp færslubókarsniðmát og keyrslur innan samstæðu

Setja verður upp færslubókarsniðmát og almenna færslubókarkeyrslu til að nota sjálfgefið fyrir færslur milli fyrirtækja. Sniðmátið og Runa eru sérstaklega mikilvæg ef samstæðufærslur eru sjálfkrafa samþykktar af félögunum. Frekari upplýsingar um sjálfvirka samþykkt færslna má fá með því að fara í  [sjálfvirkar færslur frá samstæðufélögum](#auto-accept-transactions-from-intercompany-partners).   

* Almennar færslubækur eru notaðar til að bóka á fjárhagslykla og aðra lykla, svo sem banka, viðskiptavini og lánardrottnalykla. Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum.   **Nota skal síðuna færslubók innan samstæðu**  til að setja upp almenna færslubókarkeyrslu til að nota. Stillingarnar sem eru ákveðnar í samstæðufærslum eru lyklar sem tilgreindir eru í  **MF-reikningagerð**  og  **MF-Reikningur nr** .
* Færslubókarsniðmát gefa færslubókarsíðu sem hönnuð er fyrir tiltekið málefni. Þ.e. svæðin í færslubókarsniðmátunum eru nákvæmlega þau sem þörf er á fyrir tiltekinn hluta forritsins.  **Notaðu síðuna Almennir færslubókasniðmát**  til að setja upp sniðmát til að nota fyrir samstæðufærslur.

Til að fræðast meira um sniðmát og keyrslur færslubóka er farið í  [Sniðmát færslubóka og runur](ui-work-general-journals.md#use-journal-templates-and-batches).

## Setja upp fyrirtæki fyrir færslur innan samstæðu

Eftirfarandi leiðbeiningar gera ráð fyrir að samstillingarfélagi sé settur upp með bókhaldslyklum og víddum sem byggja á bókhaldslykil og víddir milli fyrirtækja. Hægt er að setja þau upp sjálfur en yfirleitt er fljótlegra að fara í gang og viðhald er auðveldara, til að þú getir notað samstillingarfélaga. Frekari upplýsingar um samstillingarfélaga er að fá með því að  [Setja upp samstillingarfélaga](#set-up-a-synchronization-partner).

> [!TIP]
> Gott ráð er að fylla út reitina á  **flipanum Almennt**  á  **samstæðuuppsetningarsíðunni**  fyrir hvern félaga áður en félögum þeirra er bætt við. Þegar bætt er við samstarfsfyrirtæki sem er í sama leigjanda,  [!INCLUDE [prod_short](includes/prod_short.md)]  fær MF-númer þeirra og nafn fyrirtækis úr uppsetningu þeirra á flipanum Almennt.  **Reiturinn Heiti**  fyrirtækis mun sannreyna að MF-Kóði þeirra sé einstakur.

> [!NOTE]
> Ef notaður er samstillingarfélagi skal láta  **samstillingarfélagakvöldin**  vera auð þegar fyrirtækið er sett upp fyrir samstarfið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.  
2.  **Á síðu Samstæðuuppsetningar**  er fyllt út í reitina á  **flipanum Almennt** . [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Í  [!INCLUDE[prod_short](includes/prod_short.md)]  Online er ekki hægt að nota skráarstaðsetningar til að flytja færslur í samstarfsaðila þar  [!INCLUDE[prod_short](includes/prod_short.md)]  sem ekki er hægt að fá aðgang að þínu staðarneti. Ef þú velur **Staðsetning skráar** í reitnum **Flutningsgerð**, er **Möppuslóð** ekki í boði. Þess í stað verður skráin sótt í  **möppunni niðurhal**  í tölvunni. Þú sendir síðan skrána til einhvers í samstarfsfyrirtækinu, til dæmis í tölvupósti. Í meira mæli í beinu framhaldi mælum við með því að þú veljir  **email**.

Næsta skref er að setja upp samstarfsfyrirtækin.

## Setja upp samstæðufélaga

Hver félagi þarf að bæta öll önnur félög í samstarfinu sem félagatal.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2.  **Á fastflipa samstæðufélaga**  er valið  **Bæta við**.
3.  **Á síðu félaga**  innan samstæðu er fyllt út í reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Þrep 2 og 3 eru endurtekin fyrir öll fyrirtæki í samstarfinu.

> [!NOTE]
> Ef slökkt er á samstæðubókun ef kveikt er á  **Auto. samþykkja skipta á færslu**  á  **MF-síðu**  félagapósti  [!INCLUDE[prod_short](includes/prod_short.md)]  boðar að vara við Tvítekið innkaupareikninga upprunalegu innkaupapöntunarinnar. Mikilvægt er að hafa viðskiptaferla til að stjórna tvítekningum. Til dæmis með því að eyða slíkum innkaupapöntunum þegar innkaupareikningurinn berst frá millifyrirtækjafélaga.

### Setja upp samstæðufélaga sem viðskiptavini og lánardrottna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samstæðu** og velja síðan viðkomandi tengil.
2.  **Á fastflipanum samstarfsaðilar**  samstæðunnar er kortasíða opnuð fyrir félagana.
3. Eftir því hvað á að gera skal velja viðskiptavin eða félaga í reitnum  **viðskm.** Eða  **Lánardr.** svæði.

    > [!NOTE]
    > Ef viðskiptavinurinn eða lánardrottinn hefur ekki verið stofnaður er hægt að velja  **+ nýtt**  í fellivalmyndinni til að setja þær upp. Til að fræðast meira um stofnun viðskiptavina og lánardrottna er farið í að  [skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  og  [skrá nýja lánardrottna](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > Einnig er hægt að tilgreina viðskiptavin eða lánardrottinn sem samstæðufélaga með því að fylla í  **reitinn MF-félagskóti**  á  **Kortasíðum viðskiptamannakorta**  og  **lánardrottnaspjaldinu** .

### Setja upp sjálfgefna fjárhagslykla MF-félaga innan samstæðu  

Þegar sölu-eða innkaupalína samstæðu er stofnuð til að senda sem færslur á útleið, Færið inn lykil úr bókhaldslykli samstæðunnar sem sjálfgefið fyrir reikning í fyrirtæki félagins sem upphæðin er bókuð á.  **Á spjaldinu**  fjárhagsreikningur fyrir lykla sem eru reglulega notaðir á sölu-og innkaupalínur milli fyrirtækja er hægt að tilgreina sjálfgefinn fjárhagslykil MF-félaga. Til dæmis er hægt að færa inn samsvarandi safnreikning lánardrottna úr MF-bókhaldsreikningi fyrir safnreikninga viðskiptamanna. Viðskiptakröfur og útistandandi Viðskiptakröfur eru notaðar sem Off-stilling lykill fyrir MF-félaga þegar færslur eru bókaðar í MF-færslubók.  

Þegar fjárhagsreikningur er síðan færður inn í reitinn **Nr. Mótreiknings** í línu milli fyrirtækja með **MF-félaga** í reitnum **Tegund reiknings** er sjálfkrafa fyllt í reitinn **MF-félagi fjárhagsreikningur**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Fjárhagsreikningurinn sem er notaður fyrir MF-færslur er opnaður og í  **reitnum Sjálfgefinn MF-félagi**  er færður inn Fjárhagslykill samstæðuleiknings sem félaginn bókar um leið og bókað er á fjárhag línunnar.
3. Skref 2 er endurtekið fyrir hvern reikning sem oft er færður inn í reitinn **Mótreikningur nr.** í línu í færslubók eða fylgiskjali milli fyrirtækja.

### Sjálfvirk samþykkt færslna frá samstæðufélögum

Til að gera það fljótara að vinna samstæðufærslur er hægt að tilgreina að stofna eigi sjálfkrafa færslubókarlínur byggðar á færslum MF-félaga úr  **síðunni MF-færslubók** . Til að sjálfvirk stofna og útsendum færslum verður að kveikja á eftirtöldum toggi fyrir hvern félaga:

*  **Á síðu Samstæðuuppsetningarinnar**  er kveikt á  **Auto. senda færslur**  til skipta fyrir félagan samstillt. Tilgreinið síðan hvar á að stofna mótteknar MF-færslur innan samstæðu með því að fylla  **út reitina sjálfgefið MF-Alm**  **·** .

    > [!TIP]
    >  **Ef sjálfgefna reiturinn fyrir sniðmát**  MF-Alm. færslubókar er auður þarf að setja upp færslubókarsniðmát til að nota fyrir MF-færslubækur. Frekari upplýsingar um sniðmát og keyrslur er að fá með því að fara í  [Sniðmát almennra færslubóka innan samstæðu og runur](#set-up-intercompany-general-journal-templates-and-batches)    

*  **Á síðu MF-félaga**  er kveikt á víxlun með  **sjálfvirkum Samþykkslafærslum** .

Færslubókarlínur eru stofnaðar fyrir þig en ekki bókaðar.

> [!NOTE]
> Ef fyrirtækið þitt notaði eiginleika innan samstæðu í [!INCLUDE [prod_short](includes/prod_short.md)] á undan 2022 útgáfutímabili 1 til að samþykkja færslur sjálfkrafa þarf stjórnandinn þinn að kveikja á eiginleikanum **Samþykkja almennar færslubókarfærslur innan samstæðu sjálfkrafa** á síðunni **Eiginleikastjórnun**.

### Tilgreina Bankareikningar sem á að nota fyrir samstæðufélaga

Til að auðvelda beingreiðslur er tilgreindur einn eða fleiri Bankareikningar til að nota fyrir samstæðufélaga. Þegar félagi notar færslubók innan samstæðu til að ganga frá greiðslu geta þeir tilgreint bankareikninginn í línunni. Bankareikninginn er notaður sem Mótreikningur í móttökufyrirtækinu, sem heldur þörfinni að færa handvirkt inn færslur.

* Til að tilgreina bankareikning sem á að nota, á  **síðunni Samstæðuaðilar**, skal velja  **aðgerðina Bankareikningar** .  **Í spjaldi** samstæðubankareiknings eru færðar inn reikningsupplýsingar.

## Úrræðaleit vegna samstæðuuppsetningar

 **Á síðu samstæðuuppsetningar**  inniheldur rúða í  **samstæðu-uppsetningarrúðu**  flísar sem gefa til kynna hvort búið er að setja upp alla íhluti sem þarf til að skiptast á samstæðufærslum. Einnig er hægt að nálgast flísarnar á hlutverkamiðstöð Viðskiptastjóra. Veldu flísarnar til að finna út hvað vantar. Yfirlit yfir nauðsynlega íhluti er að  [fá með því að fara í yfirlit yfir skrefin til að byrja](#overview-of-the-steps-to-get-started).

## Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]