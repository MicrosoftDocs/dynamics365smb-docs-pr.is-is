---
title: Uppsetning og notkun á samþykktarverkflæði innkaupa
description: Þessi kynning fer með þig í gegnum öll stigin sem felast í því að setja upp og nota samþykktarverkflæði innkaupa í Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: edupont
---
# Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa

Hægt er að gera sjálfvirkt ferli samþykktar á nýjar eða breyttar færslur, t.d. skjöl, færslubókarlínur og spjöld viðskiptamanna með því að stofna verkflæði með skrefum fyrir viðkomandi samþykkjendur.

Áður en samþykkisverkflæði eru stofnaðar verður að setja upp samþykkjandi og staðgengill samþykkjanda fyrir hvern notanda samþykktar. Einnig er hægt að stilla upphæðartakmörk samþykkjenda til að skilgreina hvaða sölu- og innkaupafærslur þeir mega samþykkja. Samþykktarbeiðnir og aðrar tilkynningar er hægt að senda sem tölvupóst eða innri athugasemd. Fyrir hverja uppsetningu samþykktarnotanda má einnig setja upp hvenær þeim berast tilkynningar.

> [!NOTE]
> Til viðbótar við Workflow-virknina innan [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að nota Power Automate til að skilgreina verkflæði fyrir tilvik í [!INCLUDE[prod_short](includes/prod_short.md)]. Hafa skal í huga að þótt þetta séu tvö aðskilin verkflæðiskerfi, þá eru öll Flow-sniðmát sem búin eru til með Power Automate bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar í [Nota Business Central í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md).  

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

## Um kynninguna

Þessi kynning er sviðsmynd sem sýnir eftirfarandi verk:  

- Setja upp notendur samþykktar  
- Setja upp tilkynningar fyrir samþykktarnotendur  
- Breyta og virkja samþykktarverkflæði  
- Óska eftir samþykki innkaupapöntunar (sem Alicia)  
- Að fá tilkynningu og samþykkja síðan beiðnina (sem Sean)  

## Ferill

Sean er yfirnotandi í CRONUS. Hann stofnar tvo skjalasamþykktarnotendur. Annar er Alicia sem táknar innkaupaaðilinn. Hinn er sá sem stendur fyrir samþykktaraðila Alicia. Sean gefur sér síðan ótakmarkaðar innkaupaheimildir og tilgreinir að hann muni fá tilkynningar innri hnúts um leið og viðeigandi tilvik gerist. Að lokum býr Sean til nauðsynlegt samþykktarverkflæði sem afrit af fyrirliggjandi sniðmáti *Verkflæði samþykktar innkaupapöntunar*, skilur eftir öll fyrirliggjandi skilyrði og svarmöguleika óbreytt og virkjar síðan verkflæðið.  

Til að prófa samþykktarverkflæðið skráir Sean sig inn í [!INCLUDE[prod_short](includes/prod_short.md)] sem Alicia og biður síðan um samþykki á innkaupapöntun. Síðan skráir Sean sig inn sem hann sjálfur, sér athugasemdin í „Mínu hlutverki“, fylgir tenglinum á samþykktarbeiðnina fyrir innkaupapöntunina og samþykkir beiðnina.  

## Notendur

Áður en þú getur sett upp samþykktarnotendur og tilkynningaaðferð þeirra verðurðu að ganga úr skugga um að þessir notendur séu til í [!INCLUDE[prod_short](includes/prod_short.md)]: Einn mun tákna Aliciu. Hinn notandinn, þú sjálf(ur), táknar Sean. Frekari upplýsingar eru í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md).

### Setja upp notendur samþykktar

Þegar þú ert skráð(ur) inn sem þú sjálf(ur) skaltu setja upp Aliciu sem samþykktarnotanda sem er þú sjálf(ur) samþykktaraðili fyrir. Settu upp samþykktarheimildir þínar og tilgreindu hvernig og hvenær þér er tilkynnt um samþykktarbeiðnir.  

#### Til að setja upp þig sjálfan og Alicia sem notendur samþykki

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning á notanda samþykktar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Notandauppsetning samþykktar** skal velja aðgerðina **Nýtt**.  

    > [!NOTE]  
    >  Setja verður upp samþykkjanda áður en hægt er að setja upp notendur sem þurfa sem samþykki þess samþykkjanda. Það þýðir að þú verður að setja þig upp áður en þú getur sett Aliciu upp.  

3. Setja upp tvo samþykktarnotendur með því að fylla í reitina eins og lýst er í eftirfarandi töflu.  

    |Notandakenni|Kenni samþykkjanda|Ótakmörkuð innkaupaheimild|  
    |-------|-----------|---------------------------|  
    |ÞÚ||Valið|
    |ALICIA|ÞÚ||

### Tilkynningar settar upp

Í þessari kynningu er notandanum tilkynnt með innri athugasemd um beiðnir til að samþykkja. Samþykktartilkynningu er einnig hægt að senda með tölvupósti og hægt að bæta við svarskrefi verkflæðis sem tilkynnir sendanda þegar beiðni er samþykkt eða henni er hafnað. Frekari upplýsingar eru í [Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### Til að setja upp hvernig og hvenær þú færð tilkynningu

1. Á síðunni **Notandauppsetning samþykktar** velur notandi línuna fyrir sjálfa(n) sig og svo aðgerðina **Tilkynningagrunnur**.  
2. Á síðunni **Uppsetning tilkynninga** í reitnum **Tilkynningagerð** skal velja **Samþykki**.  
3. Í reitnum **Aðferð tilkynningar** skal velja **Athugasemd**.  
4. Á síðunni **Tilkynningagrunnur** skal velja aðgerðina **Áætlun tilkynninga**.  
5. Á síðunni **Tilkynningaáætlun** í reitnum **Endurtekning** skal velja **Samstundis**.  

## Samþykktarverkflæðið stofnað

Stofna skal samþykktarverkflæði innkaupapöntunar með því að afrita skrefin úr sniðmátinu **Samþykktarverkflæði innkaupapöntunar**. Hafið fyrirliggjandi verkflæðisþrep óbreyttar og virkið þau síðan í verkflæði.  

> [!TIP]
> Einnig er hægt að bæta við svarskrefi verkflæðis til að tilkynna sendanda þegar beiðni er samþykkt eða henni er hafnað. Frekari upplýsingar eru í [Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md).

### Til að stofnaog virkja samþykktarverkflæði innkaupapöntunar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Á síðunni **Verkflæði** skal velja **Aðgerðir** og svo **Nýtt** og svo **Nýtt vinnuflæði úr Sniðmáti** aðgerðina.  
3. Á síðunni **Verkflæðissniðmát** skal velja verkflæðissniðmát með heitinu **Samþykktarverkflæði innkaupapöntunar**.  

   Síðan **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti. Við gildið í reitnum **Kóði** er bætt við *-01* til að gefa til kynna að þetta sé fyrsta verkflæðið sem er stofnað úr sniðmátinu **Samþykktarverkflæði innkaupapöntunar**.  
4. Í hausnum á síðunni **Verkflæði** skal kveikja á **Virkjað**.  

## Nota samþykktarverkflæðið

Nota nýja samþykktarverkflæði innkaupapöntunar með því að skrá þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] sem Alicia til að biðja um samþykki á innkaupapöntun. Síðan skaltu skrá þig inn, skoða athugasemdina í „Mínu hlutverki“, fylgja tenglinum á samþykktarbeiðnina og síðan samþykkja beiðni.  

### Til að óska eftir samþykki á innkaupapöntun, sem Alicia

1. Skrá inn sem Alicia.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir**, velja síðan viðkomandi tengil.  
3. Veldu línuna sem á að opna *innkaupapöntun 106001*.  
4. Á síðunni **Innkaupapöntun** skal velja **Aðgerðir**, svo **Biðja um samþykki** og svo **Senda samþykktarbeiðni** aðgerðina.  

Takið eftir að gildið í reitnum **Staða** hefur breyst í **Bíður samþykktar**.  

### Til að samþykkja innkaupapöntun, sem Sean

1. Skrá inn sem Sean.
2. Í „Mínu hlutverki“, á svæðinu **Sjálfsafgreiðsla**, skal velja **Beiðnir til að samþykkja**.
3. Á síðunni **Beiðnir til að samþykkja** skal velja línuna um innkaupapöntunina frá Aliciu, síðan velja aðgerðina **Samþykkja**.  

Gildið í reitnum **Staða í** innkaupapöntun frá Alicia breytist í **Losað**.  

Nú hefurðu sett upp og prófað einfalt samþykktarverkflæði samkvæmt fyrstu tveimur skrefunum í **Samþykktarverkflæði innkaupapöntunar**. Auðvelt er að víkka þetta verkflæði til að það bóki sjálfkrafa innkaupapöntun Alicia þegar Sean samþykkir hana. Til að gera þetta þarftu að virkja **Verkflæði innkaupareiknings** þannig að svar við útgefnum innkaupareikningi er að bóka hann. Fyrst þarf að breyta skilyrðum tilviksins á fyrsta skrefið verkflæði (innkaup) úr **Reikningur** í **Pöntun**.  

Almenna útgáfan af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur mörg verkflæðissniðmát fyrir sviðsmyndir sem eru studdar af forritskóðanum. Flest þessara sniðmáta eru fyrir verkflæði samþykktar.  

Þú skilgreinir afbrigði af verkflæðum með því að fylla út reiti í verkflæðislínum úr föstum listum yfir gildi viðburðar og svars sem táknar sviðsmyndirnar sem eru studdar af forritskóðanum. Frekari upplýsingar eru á [Búa til verkflæði](across-how-to-create-workflows.md).  

[!INCLUDE[workflow](includes/workflow.md)]

## Sjá tengda [Microsoft þjálfun](/training/modules/use-approval-workflows/)

## Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)  
[Nota Samþykktarverkflæði](across-how-use-approval-workflows.md)  
[Verkflæði](across-workflow.md)  
[Nota Business Central í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
