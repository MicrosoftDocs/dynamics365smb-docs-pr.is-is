---
title: Hvernig skal búa til verkflæði | Microsoft Docs
description: Hægt er að stofna verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0db0e2e6705a7d2fd1907227996d8c258dcbc554
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754793"
---
# <a name="create-workflows"></a>Búa til verkflæði
Hægt er að stofna verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af verkflæðistilvikum sem breytt er af tilvikaskilyrðum og verkflæðisviðbrögðum með viðbragðavalkostum. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.  

Þegar verkflæði eru stofnuð er hægt að afrita skref úr núgildandi verkflæði eða úr verkflæðissniðmátum. Verkflæðissniðmát eru óbreytanleg verkflæði sem eru til staðar í altæku útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)]. Kóði fyrir verkflæðissniðmát sem er bætt við af Microsoft eru merkt með "MS-", eins og í "MS-PIW". Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

Ef viðskiptasviðsmynd kallar á verkflæðistilvik eða -viðbrögð sem ekki eru studd verður Microsoft-samstarfsaðili að virkja þau með því að sérstilla forritakóðann.  

> [!NOTE]  
>  Allar tilkynningar um verkflæðisskref eru sendar um verkröð. Ganga skal úr skugga um að verkröð í uppsetningu sé sett upp þannig að hún meðhöndli verkflæðistilkynningar og að **Byrja sjálfkrafa frá NAS** gátreiturinn sé valinn. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Til að stofna verkflæði  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkflæði** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð. Síðan **Verkflæði** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Til að stofna verkflæði úr verkflæðissniðmáti, skal velja á síðunni **Verkflæði** aðgerðina **Stofna verkflæði úr sniðmáti**. Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  
5. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
6. Í **Flokkur** reitnum skal tilgreina hvaða flokki verkflæðið tilheyrir.  
7. Í reitnum **Þegar tilvik** skal tilgreina tilvik sem verður að eiga sér stað til að að verkflæðisskref geti hafist.  

    Þegar reiturinn er valinn opnast síðan **Verkflæðitilvik** þar sem hægt er að velja úr öllum tilvikum verkflæðis sem til eru.  
8. Í reitnum **Skilyrði**, tilgreinið eitt eða fleiri skilyrði sem þarf að uppfylla áður en tilvikið í **Þegar tilvik** reitnum getur átt sér stað.  

    Þegar reiturinn er valinn opnast síðan **Skilyrði tilviks** þar sem valið er úr lista yfir síureit sem eru viðeigandi sem skilyrði fyrir viðkomandi tilvik. Hægt er að bæta nýja afmörkunarreitirnir sem á að nota sem atburðurinn skilyrði. Þú stillir tilvikaaðstæður með sama hætti og þú stillir afmarkanir á skýrslubeiðnisíðum.  

    Ef verkflæðistilvik er breyting á tilteknum reit í færslu opnast síðan **Skilyrði tilviks** með valkostum um að velja reit og gerð breytingar.  

    1.  Til að tilgreina reitarbreytingu fyrir tilvik skal, á síðunni **Aðstæður tilviks** í reitnum **Reitur** velja reitinn sem er breytt.  
    2.  Í reitnum **Stjórnandi** skal velja annað hvort **Minnkað**, **Aukið**, eða **Breytt**.  
9. Í reitnum **Þá svörun**, tilgreinið viðbrögð sem fylgja þegar verkflæðistilvik á sér stað.  

     Þegar reiturinn er valinn opnast síðan **Verkflæðiviðbrögð** þar sem hægt er að velja úr öllum verkflæðisviðbrögðum sem til eru og stilla valkosti viðbragðs fyrir valda viðbragðið.  
10. Á flýtiflipanum **Valkostir fyrir valið svar** tilgreinið valkosti fyrir verkflæðissvarið með því að elja gildi í ýmsum reitum sem birtast, sem hér segir:  

    1.  Til að tilgreian valkosti fyrir verkflæðissvar sem felur í sér að senda tilkyningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði|Description|  
        |----------------------------------|---------------------------------------|  
        |**Tilkynna sendanda**|Tilgreindu hvort samþykkisbeiðandi fái tilkynningu í staðinn fyrir viðtakanda samþykkisbeiðninnar. Ef gátreiturinn er valinn er slökkt á reitnum **Notandaauðkenni viðtakanda** vegna þess að tilkynning berst til þess sem sendi beiðnina fær tilkynningu í staðinn. Heiti verkflæðissvars breytist til samræmis, í **Búa til tilkynningu fyrir &lt;Sendanda&gt;**. Ef gátreiturinn er ekki valinn er heiti verkflæðissvars **Búa til tilkynningu fyrir &lt;Notanda&gt;**.
        |**Notandaauðkenni viðtakanda**|Tilgreina þarf notanda sem tilkynningin verður að senda á. Athugið: Þessi valmöguleiki er aðeins tiltækur fyrir verkflæðisvörun með staðarhaldara fyrir tiltekinn notanda. Fyrir verkflæðissvör án staðgengils notenda er móttakandi tilkynningar yfirleitt skilgreinist eftir notandauppsetning samþykktar.|  
        |**Færslugerð tilkynningar**|Tilgreinir hvort tilkynning verkflæðis hafi farið af stað vegna breytinga á færslu, samþykktarbeiðni eða því að gögn séu ekki til á réttum tíma.|
        |**Tengja marksíðu**|Tilgreina aðra síðu [!INCLUDE[prod_short](includes/prod_short.md)] sem tengill í tilkyninningunni opnar í stað þeirrar sjálfgefnu.<br /><br />Athugið að síðan verður að hafa sömu upprunatöflu og viðkomandi færsla.|  
        |**Sérsniðinn tengill**|Tilgreinir vefslóð tengils sem er bætt við tilkyninninguna auk tengilsins við síðuna í [!INCLUDE[prod_short](includes/prod_short.md)].|  
    2.  Til að tilgreina valkosti fyrir verkflæðissvar sem felur í sér að senda tilkynningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði|Description|  
        |----------------------------------|---------------------------------------|  
        |**Reikniregla gjalddaga**|Tilgreina hversu margir dagar mega líða þar til leysa þarf úr samþykktarbeiðni frá þeim degi sem hún var send.|  
        |**Framselja eftir**|Tilgreina ef og þegar samþykkisbeiðni er sjálfkrafa úthluta á viðeigandi varamann. Hægt er að velja sjálfkrafa að úthluta einn, tvo eða fimm dögum eftir þá dagsetning þegar beðið var um samþykkt.|  
        |**Gerð samþykkjanda**|Tilgreina hver er samþykkjandi, samkvæmt uppsetningu á notendum samþykktar og notendur verkflæði.<br /><br /> Eftirfarandi möguleikar eru til staðar:<br /><br /> -   **Sölumaður/innkaupaaðili** tilgreinir að notandinn sem settur er upp í reitnum **Sölumaður/Innk. Kóði** á síðunni **Samþykkt notandauppsetning** ákvarði samþykkjanda. Færslur fyrir samþykktarbeiðni eru þá stofnaðar samkvæmt gildinu í reitnum **Afmörkunargerð samþykkjanda**.<br />     Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-workflow-users.md).|  
        |**Sýna staðfestingarskilaboð**|Tilgreina ef staðfestingarskilaboð birtist notendum eftir að þeir óska ​​eftir samþykki.|  
        |**Afmörkunargerð samþykkjanda**|Tilgreina hvernig samþykktartakmarkanir þeirra sem samþykkja hafa áhrif á færslur samþykktarbeiðna sem eru stofnaðar fyrir þau. Hæfur samþykkjandi er samþykkjandi sem hefur samþykktarmörk sem eru hærri en gildið á umræddri beiðni.<br /><br /> Eftirfarandi möguleikar eru til staðar:<br /><br /> 1.  **Keðja samþykkjenda** tilgreinir að færslur samþykktarbeiðni eru stofnaðar fyrir alla samþykkjendur frá og með fyrsta samþykkjanda sem uppfyllir skilyrði.<br />2.  **Beinn samþykkjandi** tilgreinir að samþykktarbeiðnisfærsla er aðeins stofnuð fyrir næsta samþykkjanda, sama hver samþykktarmörk hans eru.<br />3.  **Fyrsti hæfi samþykkjandi** tilgreinir að samþykktarbeiðnisfærsla er aðeins stofnuð fyrir fyrsta samþykkjanda sem uppfyllir skilyrði.<br />|  
    3.  Til að tilgreina valkostir fyrir verkflæðissvar sem inniheldur að stofna færslubókarlínur skal fylla í reitirnir eins og lýst er í eftirfarandi töflu.  

        |Svæði|Description|  
        |----------------------------------|---------------------------------------|  
        |**Heiti sniðmáts færslubókar**|Tilgreina heiti sniðmáts færslubókarinnar sem stofnuð eru í tilteknu bókarlínurnar.|  
        |**Heiti færslubókarkeyrslu**|Tilgreina heiti sniðmáts færslubókarrununnar sem stofnuð eru í tilteknu bókarlínurnar.|  

11. Velja skal hnappana **Auka inndrátt** og **Minnka inndrátt** til að draga tilviksheiti inn í reitnum **Þegar** til að skilgreina stöðu skrefsins í verkflæðinu.  
    1.  Tilgreinið að skrefið sé næst í verkflæðisröðinni með því að draga tilviksheitið inn undir tilviksheiti fyrra skrefs.  
    2.  Tilgreinið að skrefið sé eitt af valkvæðum skrefum sem gætu hafist, allt eftir skilyrðum þess með, með því að setja tilviksheitið í sama inndrátt og önnur valkvæð skref. Raðið slíkum valskrefum eftir forgangi með því að setja mikilvægasta skrefið efst.  

    > [!NOTE]  
    >  Aðeins er hægt að breyta inndrætti skrefs sem ekki hefur skref á eftir sér.  

12. Endurtakið skref 7 til 11 til að bæta fleiri verkflæðisskrefum við, annaðhvort fyrir eða eftir skrefið sem var verið að stofna.  
13. Veljið gátreitinn **Virkja** til að tilgreina að verkflæði hefjist um leið og tilvik á fyrsta skerfi af gerðinni **Komustaður** á sér stað. Frekari upplýsingar eru í [Nota verkflæði](across-use-workflows.md).  

> [!NOTE]  
>  Ekki skal virkja verkflæði þar til víst er að verkflæði sé lokið að að umrædd verkflæðisskref geti hafist.  

> [!TIP]  
>  Til að sjá tengsl á milli tafla sem eru notaðar í verkflæði, veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") og sláðu svo inn **Verkflæði – töflutengsl**.  

## <a name="see-also"></a>Sjá einnig  
[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)   
[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)   
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)   
[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)   
[Eyða verkflæðum](across-how-to-delete-workflows.md)   
[Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Uppsetning verkflæðis](across-set-up-workflows.md)   
[Nota verkflæði](across-use-workflows.md)   
[Verkflæði](across-workflow.md)      


[!INCLUDE[footer-include](includes/footer-banner.md)]