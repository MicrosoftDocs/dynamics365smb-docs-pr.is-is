---
title: Stofna verkflæði til að tengja verk
description: Hægt er að stofna verkflæði sem tengja viðskiptaferlisverk sem framkvæmd eru af ólíkum notendum og fela í sér kerfisverk eins og sjálfvirka bókun sem skref í verkflæði.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2021
ms.author: edupont
ms.openlocfilehash: 2734f4d65869ba666a53333c9338239a1cb1a1b4
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588227"
---
# <a name="create-workflows-to-connect-business-process-tasks"></a>Stofna verkflæði til að tengja verk viðskiptaferla

Hægt er að stofna verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af verkflæðistilvikum sem breytt er af tilvikaskilyrðum og verkflæðisviðbrögðum með viðbragðavalkostum. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.  

Þegar verkflæði eru stofnuð er hægt að afrita skref úr núgildandi verkflæði eða úr verkflæðissniðmátum. Verkflæðissniðmát eru óbreytanleg verkflæði sem eru til staðar í altæku útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)]. Kóði fyrir verkflæðissniðmát sem er bætt við af Microsoft eru merkt með "MS-", eins og í "MS-PIW". Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

Ef viðskiptasviðsmynd kallar á verkflæðistilvik eða -viðbrögð sem ekki eru studd verður Microsoft-samstarfsaðili að virkja þær með því að búa til viðbót sem innleiðir viðeigandi verkflæðistilvik.  

> [!NOTE]  
> Allar tilkynningar um verkflæðisskref eru sendar um verkröð. Gakktu úr skugga um að verkröðin endurspegli viðskiptaþarfir þínar. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Skýring á verkflæðisdæmi.":::

Verkflæðið skiptist í þrennt:

1) **Þegar atburður** Þetta er þar sem ræsingin er valin.
    Dæmi um ræsingu gæti verið:
    - Aðalgagnafærslu er breytt
    - Færslubókarlína er stofnuð
    - skjal á innleið er búið til eða gefið út
    - Óskað er eftir samþykki skjals

2) **Með því skilyrði** **Skilyrðin** eru tengd tilvikinu og opna á að búa til síur þegar tilvikið er ræst
3) **Svarið sem fylgir** **Svörin** svara því hvað felst í næsta skrefi vinnunnar.

Fyrir báðar gerðir tilvika eru tilvikin skilgreind af kerfinu. Bæta verður við nýjum tilvikum með þróun á viðbót.

## <a name="to-create-a-workflow"></a>Til að stofna verkflæði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Verkflæði** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Til að stofna verkflæði úr verkflæðissniðmáti, skal velja á síðunni **Verkflæði** aðgerðina **Stofna verkflæði úr sniðmáti**. Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  
5. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
6. Í **Flokkur** reitnum skal tilgreina hvaða flokki verkflæðið tilheyrir.  
7. Í reitnum **Þegar tilvik** skal tilgreina tilvik sem verður að eiga sér stað til að að verkflæðisskref geti hafist.  

    Þegar reiturinn er valinn opnast síðan **Verkflæðitilvik** þar sem hægt er að velja úr öllum tilvikum verkflæðis sem til eru.  
8. Í reitnum **Skilyrði**, tilgreinið eitt eða fleiri skilyrði sem þarf að uppfylla áður en tilvikið í **Þegar tilvik** reitnum getur átt sér stað.  

    Þegar reiturinn er valinn opnast síðan **Skilyrði tilviks** þar sem valið er úr lista yfir síureit sem eru viðeigandi sem skilyrði fyrir viðkomandi tilvik. Hægt er að bæta nýja afmörkunarreitirnir sem á að nota sem atburðurinn skilyrði. Þú stillir tilvikaaðstæður með sama hætti og þú stillir afmarkanir á skýrslubeiðnisíðum.  

    Ef verkflæðistilvik er breyting á tilteknum reit í færslu opnast síðan **Skilyrði tilviks** með valkostum um að velja reit og gerð breytingar.  

    1. Til að tilgreina reitarbreytingu fyrir tilvik skal, á síðunni **Aðstæður tilviks** í reitnum **Reitur** velja reitinn sem er breytt.  
    2. Í reitnum **Stjórnandi** skal velja annað hvort **Minnkað**, **Aukið**, eða **Breytt**.  
9. Í reitnum **Þá svörun**, tilgreinið viðbrögð sem fylgja þegar verkflæðistilvik á sér stað.  

     Þegar reiturinn er valinn opnast síðan **Verkflæðiviðbrögð** þar sem hægt er að velja úr öllum verkflæðisviðbrögðum sem til eru og stilla valkosti viðbragðs fyrir valda viðbragðið.  
10. Á flýtiflipanum **Valkostir fyrir valið svar** tilgreinið valkosti fyrir verkflæðissvarið með því að elja gildi í ýmsum reitum sem birtast, sem hér segir:  

    1. Til að tilgreian valkosti fyrir verkflæðissvar sem felur í sér að senda tilkyningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði|Description|  
        |-----|-----------|  
        |**Tilkynna sendanda**|Tilgreindu hvort samþykkisbeiðandi fái tilkynningu í staðinn fyrir viðtakanda samþykkisbeiðninnar. Ef gátreiturinn er valinn er slökkt á reitnum **Notandaauðkenni viðtakanda** vegna þess að tilkynning berst til þess sem sendi beiðnina fær tilkynningu í staðinn. Heiti verkflæðissvars breytist til samræmis, í **Búa til tilkynningu fyrir &lt;Sendanda&gt;**. Ef gátreiturinn er ekki valinn er heiti verkflæðissvars **Búa til tilkynningu fyrir &lt;Notanda&gt;**.
        |**Notandaauðkenni viðtakanda**|Tilgreina þarf notanda sem tilkynningin verður að senda á. **Athugið**: Þessi valmöguleiki er aðeins tiltækur fyrir verkflæðisvörun með staðgengil fyrir tiltekinn notanda. Fyrir verkflæðissvör án staðgengils notenda er móttakandi tilkynningar yfirleitt skilgreinist eftir notandauppsetning samþykktar.|  
        |**Færslugerð tilkynningar**|Tilgreinir hvort tilkynning verkflæðis hafi farið af stað vegna breytinga á færslu, samþykktarbeiðni eða því að gögn séu ekki til á réttum tíma.|
        |**Tengja marksíðu**|Tilgreindu aðra síðu sem tengill í tilkynningunni opnar í stað þeirrar sjálfgefnu. Athugið að síðan verður að hafa sömu upprunatöflu og viðkomandi færsla.|
        |**Sérsniðinn tengill**|Tilgreindu vefslóð tengils sem er bætt við tilkyninninguna auk tengilsins við síðuna.|  

    2. Til að tilgreina valkosti fyrir verkflæðissvar sem felur í sér að senda tilkynningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði|Description|  
        |-----|-----------|  
        |**Reikniregla gjalddaga**|Tilgreina hversu margir dagar mega líða þar til leysa þarf úr samþykktarbeiðni frá þeim degi sem hún var send.|
        |**Framselja eftir**|Tilgreina ef og þegar samþykkisbeiðni er sjálfkrafa úthluta á viðeigandi varamann. Hægt er að velja sjálfkrafa að úthluta einn, tvo eða fimm dögum eftir þá dagsetning þegar beðið var um samþykkt.|
        |**Gerð samþykkjanda**|Tilgreina hver er samþykkjandi, samkvæmt uppsetningu á notendum samþykktar og notendur verkflæði. Þegar reiturinn er stilltur á **Sölumaður/innkaupaaðili** tilgreinir sú stilling að notandinn sem settur er upp í reitnum **Sölumaður/Innk. Kóði** á síðunni **Uppsetning á notanda samþykktar** ákvarði samþykkjanda. Færslur fyrir samþykktarbeiðni eru þá stofnaðar samkvæmt gildinu í reitnum **Afmörkunargerð samþykkjanda**. Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-workflow-users.md).|
        |**Sýna staðfestingarskilaboð**|Tilgreina ef staðfestingarskilaboð birtist notendum eftir að þeir óska ​​eftir samþykki.|
        |**Afmörkunargerð samþykkjanda**|Tilgreindu hvernig samþykktartakmarkanir þeirra sem samþykkja hafa áhrif á færslur samþykktarbeiðna sem eru stofnaðar fyrir þau. Hæfur samþykkjandi er samþykkjandi sem hefur samþykktarmörk sem eru hærri en gildið á umræddri beiðni. Eftirfarandi valmöguleikar eru til staðar: <ol><li>**Keðja samþykkjenda** tilgreinir að færslur samþykktarbeiðni eru stofnaðar fyrir alla samþykkjendur frá og með fyrsta samþykkjanda sem uppfyllir skilyrði</li><li>**Beinn samþykkjandi** tilgreinir að samþykktarbeiðnisfærsla er aðeins stofnuð fyrir næsta samþykkjanda, sama hver samþykktarmörk hans eru.</li><li>**Fyrsti hæfi samþykkjandi** tilgreinir að samþykktarbeiðnisfærsla er aðeins stofnuð fyrir fyrsta samþykkjanda sem uppfyllir skilyrði.</li></ol>|
    3. Til að tilgreina valkostir fyrir verkflæðissvar sem inniheldur að stofna færslubókarlínur skal fylla í reitirnir eins og lýst er í eftirfarandi töflu.  

        |Svæði|Description|  
        |-----|-----------|  
        |**Heiti sniðmáts færslubókar**|Tilgreina heiti sniðmáts færslubókarinnar sem stofnuð eru í tilteknu bókarlínurnar.|  
        |**Heiti færslubókarkeyrslu**|Tilgreina heiti sniðmáts færslubókarrununnar sem stofnuð eru í tilteknu bókarlínurnar.|  

11. Velja skal hnappana **Auka inndrátt** og **Minnka inndrátt** til að draga tilviksheiti inn í reitnum **Þegar** til að skilgreina stöðu skrefsins í verkflæðinu.  

    1. Tilgreinið að skrefið sé næst í verkflæðisröðinni með því að draga tilviksheitið inn undir tilviksheiti fyrra skrefs.  
    2. Tilgreinið að skrefið sé eitt af valkvæðum skrefum sem gætu hafist, allt eftir skilyrðum þess með, með því að setja tilviksheitið í sama inndrátt og önnur valkvæð skref. Raðið slíkum valskrefum eftir forgangi með því að setja mikilvægasta skrefið efst.  

    > [!NOTE]  
    >  Aðeins er hægt að breyta inndrætti skrefs sem ekki hefur skref á eftir sér.  

12. Endurtakið skref 7 til 11 til að bæta fleiri verkflæðisskrefum við, annaðhvort fyrir eða eftir skrefið sem var verið að stofna.  
13. Veljið gátreitinn **Virkja** til að tilgreina að verkflæði hefjist um leið og tilvik á fyrsta skerfi af gerðinni **Komustaður** á sér stað. Frekari upplýsingar eru í [Nota verkflæði](across-use-workflows.md).  

> [!NOTE]  
> Ekki skal virkja verkflæði þar til víst er að verkflæði sé lokið að að umrædd verkflæðisskref geti hafist.  

> [!TIP]  
> Til að sjá tengsl á milli tafla sem eru notaðar í verkflæði skal velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið og færa síðan inn **Verkflæði – Töflutengsl**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Dæmi um hvernig nýtt verkflæði er búið til með því að nota fyrirliggjandi tilvik

Í eftirfarandi dæmi er nýtt vinnuferli gert til að samþykkja breytingar á nafni núverandi lánardrottni:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Verkflæði** opnast.
3. Í verkflæðishlutanum skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.

    |Svæði  |Gildi:  |
    |---------|---------|
    |**Kóði**|**VENDAPN-01**|
    |**Lýsing**|**Samþykki fyrir nafnbreytingu lánardrottins** |
    |**Flokkur**|**INNK**|

4. Til að búa til fyrsta verkflæðisskrefið skal fylgja þessum skrefum.

    1. Í reitnum **Þegar tilvik** skal tilgreina að *Lánardrottnafærslu er breytt*.  
    2. Í reitnum **Með skilyrði** skal velja orðið **Alltaf** og síðan á síðunni **Skilyrði tilviks** skal velja tengilinn **Bæta við skilyrði þegar gildi í reit breytist** og velja síðan reitinn *Heiti*.  

      Niðurstaðan úr þessu skrefi er að skilyrðið lesist sem *Heiti er breytt*.  
    3. Í reitnum **Þá svar** skal velja tengilinn **Velja svar** og síðan á síðunni **Verkflæðissvör**, í reitnum **Velja svar**, skal velja svarið *Snúa aftur gildinu í reit \<Field\> í færslunni og vista breytingarnar* og síðan í hlutanum **Valkostir fyrir valið svar** skal tilgreina reitinn *Heiti*.  
    4. Veldu tengilinn **Bæta fleiri svörum við** og bættu síðan færslu við fyrir *Stofna samþykktarbeiðni fyrir færsluna með því að nota samþykktargerð <%1> og <%2>.* svar.  
    5. Í hlutanum **Valkostir fyrir valið svar** fyrir nýja svarið skaltu breyta reitnum **Gerð samþykkjanda** í *Notendaflokkur verkflæðis* og síðan í reitnum **Notendaflokkur verkflæðis** skal tilgreina notendaflokkinn sem á við.  

    Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  
    6. Bættu við þriðja svarinu: *Senda samþykktarbeiðni fyrir færsluna og stofna tilkynningu.*  
    7. Bættu við fjórða svarinu: *Sýna skilaboð „%1“* og síðan í hlutanum **Valkostir fyrir valið svar**, í skilaboðareitnum, skaltu tilgreina **Samþykktarbeiðni var send**.  
    8. Veldu hnappinn Í lagi til að fara aftur í verkflæðisskrefið.  

5. Í næstu línu skal bæta við nýju verkflæðisskrefi fyrir *Samþykktarbeiðni er samþykkt.* tilvik.  

    1. Í reitnum **Þegar tilvik** skal tilgreina *Samþykktarbeiðni er samþykkt*.  
    2. Veldu línuvalmyndina og veldu svo **Auka inndrátt**.  
    3. Í reitnum **Með skilyrði** skal velja orðið **Alltaf** og síðan í reitnum **Bíður samþykkis** skal tilgreina *0*.  

      Niðurstaðan úr þessu skrefi er að skilyrðið er svohljóðandi: *Bíður samþykkis:0* til að gefa til kynna að þetta sé síðasti samþykkjandinn.  
    4. Í reitnum **Þá svar** skal velja tengilinn **Velja svar** og síðan á síðunni **Verkflæðissvör**, í reitnum **Velja svar**, skal velja svarið *Senda samþykktarbeiðni fyrir færsluna og stofna tilkynningu*.  
    5. Velja hnappinn Í lagi.  
6. Í næstu línu bætir þú við öðru verkflæðisskrefi fyrir tilvikið *Samþykktarbeiðni er samþykkt*.  

    1. Í reitnum **Þegar tilvik** skal tilgreina *Samþykktarbeiðni er samþykkt*.
    2. Í reitnum **Með skilyrði** skal velja orðið **Alltaf** og síðan í reitnum **Bíður samþykkis** skal tilgreina *>0*.  

      Niðurstaðan úr þessu skrefi er að skilyrðið er svohljóðandi: *Bíður samþykkis:>0* til að gefa til kynna að þetta sé *ekki* síðasti samþykkjandinn.  
    3. Í reitnum **Þá svar** skal velja tengilinn **Velja svar** og síðan á síðunni **Verkflæðissvör**, í reitnum **Velja svar**, skal velja svarið *Senda samþykktarbeiðni fyrir færsluna og stofna tilkynningu*.  
    4. Veldu hnappinn Í lagi.  
7. Í næstu línu skal bæta við nýju verkflæðisskrefi fyrir tilvikið *Samþykktarbeiðni er hafnað*.  

    1. Í reitnum **Þegar tilvik** skal tilgreina *Samþykktarbeiðni er hafnað*.  
    2. Í reitnum **Með skilyrði** skal halda gildinu *Alltaf*.  
    3. Í reitnum **Þá svar** skal velja tengilinn **Velja svar** og síðan á síðunni **Verkflæðissvör**, í reitnum **Velja svar**, skal velja svarið *Fleygja nýju gildunum*.  
    4. Veldu tengilinn **Bæta fleiri svörum við** og bættu síðan færslu við fyrir *Hafna samþykktarbeiðni fyrir færsluna og stofna tilkynningu*
    5. Veldu hnappinn Í lagi.  
8. Í næstu línu skal bæta við öðru verkflæðisskrefi fyrir tilvikið *Samþykktarbeiðni er hafnað*.  

    1. Í reitnum **Þegar tilvik** skal tilgreina *Samþykktarbeiðni er hafnað*.  
    2. Í reitnum **Með skilyrði** skal halda gildinu *Alltaf*.  
    3. Í reitnum **Þá svar** skal velja tengilinn **Velja svar** og síðan á síðunni **Verkflæðissvör**, í reitnum **Velja svar**, skal velja svarið *Senda samþykktarbeiðni fyrir færsluna og stofna tilkynningu*.  
    4. Veldu hnappinn Í lagi.  
9. Til að virkja verkflæðið skal velja reitinn **Virkjað**.  

Eftirfarandi mynd sýnir yfirlit yfir niðurstöður ferlisins.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Skýring á samþykktarverkflæði lánardrottnaheitis.":::

Næst þarftu að prófa verkflæðið með því að opna lánardrottin sem er til staðar og breyta heitinu. Staðfestu að samþykkisbeiðni sé gerð um breytingu á heiti lánardrottins.

## <a name="see-also"></a>Sjá einnig

[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)  
[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)  
[Eyða verkflæðum](across-how-to-delete-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Uppsetning verkflæðis](across-set-up-workflows.md)  
[Nota verkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
