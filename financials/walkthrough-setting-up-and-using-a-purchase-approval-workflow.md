---
title: "Kynning - Uppsetning og notkun verkflæðis innkaupasamþykktar | Microsoft Docs"
description: "Hægt er að gera sjálfvirkt ferli samþykktar á nýjar eða breyttar færslur, t.d. skjöl, færslubókarlínur og spjöld viðskiptamanna með því að stofna verkflæði með skrefum fyrir viðkomandi samþykkjendur. Áður en samþykkisverkflæði eru stofnaðar verður að setja upp samþykkjandi og staðgengill samþykkjanda fyrir hvern notanda samþykktar. Einnig er hægt að setja samþykkjendur takmarkanir til að skilgreina hvaða sölu og innkaupafærslur eru heimilt að samþykkja. Samþykktarbeiðnir og aðrar tilkynningar er hægt að senda sem tölvupóst eða innri athugasemd. Fyrir hverja uppsetningu samþykktarnotanda má einnig setja upp hvenær þeim berast tilkynningar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 58c243000bea5b70666b2a08cdd5696444e22f0f
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa
Hægt er að gera sjálfvirkt ferli samþykktar á nýjar eða breyttar færslur, t.d. skjöl, færslubókarlínur og spjöld viðskiptamanna með því að stofna verkflæði með skrefum fyrir viðkomandi samþykkjendur. Áður en samþykkisverkflæði eru stofnaðar verður að setja upp samþykkjandi og staðgengill samþykkjanda fyrir hvern notanda samþykktar. Einnig er hægt að setja samþykkjendur takmarkanir til að skilgreina hvaða sölu og innkaupafærslur eru heimilt að samþykkja. Samþykktarbeiðnir og aðrar tilkynningar er hægt að senda sem tölvupóst eða innri athugasemd. Fyrir hverja uppsetningu samþykktarnotanda má einnig setja upp hvenær þeim berast tilkynningar.  

 Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Um kynninguna  
Þessi kynning fjallar um eftirfarandi verk:  

-   Uppestning samþykki notendur (þar með talið uppsetning notanda í Windwows og í [!INCLUDE[d365fin](includes/d365fin_md.md)]).  
-   Setja upp tilkynningar fyrir samþykki notendur.  
-   Breyta og virkjun verkflæði samþykkta.  
-   Ræsi verkröð sem sendir tilkynningar.  
-   Óska eftir samþykki á innkaupapöntun, sem Alicia.  
-   Taka á móti tilkynning og síðan samþykkja beiðni, sem Sean.  

## <a name="prerequisites"></a>Frumskilyrði  
Til að ljúka þessari kynningu þarf CRONUS International Ltd. sýnifyrirtækið.

## <a name="story"></a>Ferill  
Sean er yfirnotandi í CRONUS á sinni eigin tölvu.  

Hann stofnar tvo skjalasamþykktarnotendur. Annar er Alicia sem táknar innkaupaaðilinn. Hinn er hann sjálfur, táknar samþykkjanda fyrir Alicia. Sean síðan veitir sjálfum sér ótakmarkaðan innkaupasamþykktarréttur og tilgreinir að hann fær tilkynningar með innri athugasemd um leið og viðeigandi atburðurinn á sér stað. Í síðasta lagi stofnar Sean nauðsynlegt samþykktarverkflæði sem afrit af fyrirliggjandi samþykktarverkflæði innkaupapöntunarsniðmáts, gerir ekki breytingar á fyrirliggjandi skilyrði og svör tilviksins svo virkjar hann verkflæðið.  

Til að sannprófa verkflæði samþykktar, skráir Sean sig fyrir inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Alicia, og krefst svo samþykkis á innkaupapöntun. Síðan Sean skráir sig inn sem hann sjálfur, sér athugasemdin í sinni hlutverkamiðstöð, fylgir tenglinum á samþykktarbeiðnina fyrir innkaupapöntunina og samþykkir beiðnina.  

## <a name="setting-up-the-sample-data"></a>Uppsetning sýnigagna  
Þú verður að stofna nýjan notanda á staðbundinni tölvu og í [!INCLUDE[d365fin](includes/d365fin_md.md)] vera fulltrúi Alicia sem þú munt seinna meir velja sem notanda samþykkis. Þinn eigin notandareikningur táknar Sean.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Til að bæta Alicia sem notanda í staðbundinni tölvunni  

1.  Velja **Ræsa** og í reitnum **Leita í forritum og skrám** og færa inn **Breyta staðbundnum notendum og hópum** og velja svo tengdan tengil.  
2.  Opnið möppuna **Notendur** .  
3.  Í flipanum **Aðgerðir** veljið **Nýr notandi**.  
4.  Í reitnum **Notandanafn** færið inn Alicia.  
5.  Í reitnum **Aðgangsorð** og **Staðfesta Aðgangsorð** er færð inn gild aðgangsorð.  
6.  Hreinsa þarf gátreitinn **Notandi verður að breyta aðgangsorðinu við næstu innskráningu**.  
7.  Loka á **Staðbundnir notendur og hópar** gluggann.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Til að bæta Alicia við sem notanda í [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notendur** og velja svo viðeigandi tengil.  
2.  Í glugganum **Windows Notendur** á flipanum **Heim** í flokknum **Nýtt** veljið **Nýtt**.  
3.  Í glugganum **Notandaspjald** í reitnum **Notandanafn** skal færa inn Alicia.  
4.  Í reitnum **Windows notandanafn** skal velja hnappinn AssistEdit.  
5.  Í **Velja notanda eða hóp** glugga í reit **Færið inn heiti hlutar til að velja** er fært inn Alicia og síðan valið á **Kanna heiti** hnappinn.  
6.  Þegar [NAFN TÖLVU]ALICIA birtist í reitnum, skal velja hnappinn **Í lagi**.  
7.  Á **Heimildasett notanda** flýtiflipanum í reitnum **Heimildasett**, skal velja **SUPER**.  
8.  Í reitnum **Fyrirtæki** skal velja **CRONUS International Ltd.**  
9. Velja hnappinn **Í lagi**.  

## <a name="setting-up-approval-users"></a>Setja upp samþykktarnotendur  
Með því að nota notanda Windows sem var verið að stofna, settu upp Alicia sem samþykktar notanda þar sem þú ert samþykkjandi hennar. Settu upp að samþykktarréttindi þín og tilgreindu hvernig og hvenær þú færð tilkynningu um samþykktarbeiðni.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Til að setja upp þig sjálfan og Alicia sem notendur samþykki  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning samþykkts notanda** og velja svo viðeigandi tengil.  
2.  Í glugganum **Notanandauppsetning samþykktar** á flipanum **Heim** í flokknum **Nýtt** veljið **Nýtt**.  

    > [!NOTE]  
    >  Setja verður upp samþykkjanda áður en hægt er að setja upp notendur sem þurfa sem samþykki þess samþykkjanda. Því verður að setja upp sjálfan þig áður en þú setur upp Alicia.  

3.  Setja upp tvo samþykktarnotendur með því að fylla í reitina eins og lýst er í eftirfarandi töflu.  

    |Notandakenni|Kenni samþykkjanda|Ótakmörkuð innkaupaheimild|  
    |-------------|-----------------|---------------------------------|  
    |[TÖLVA NAFN][ÞÚ]||Valið|  
    |[TÖLVA NAFN][ALICIA]|[TÖLVA NAFN][ÞÚ]||  

## <a name="setting-up-notifications"></a>Tilkynningar settar upp  
Tilgreina hvernig og hvenær þú færð tilkynningu um beiðnir um samþykki.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Til að setja upp hvernig og hvenær þú færð tilkynningu  
1.  Í glugganum **Uppsetning samþykktarnotanda** skal velja línu fyrir sjálfan sig og síðan á **Heim** flipanum í á **Vinnsla** flokknum skal velja **Uppsetning tilkynningar**.  
2.  Í glugganum **Uppsetning tilkynninga** í reitnum **Tilkynningagerð** skal færa inn **Samþykki**  
3.  Veljið reitinn **Sniðmátskóða tilkynninga** og veljið svo hnappinn **Ítarlegt**.  
4.  Í glugganum **Tilkynningasniðmát** í **Heim** í flokknum **Stjórna** veljið **Breyta lista**.  
5.  Í línunni fyrir SAMÞYKKTAR-sniðmát í reitnum **Tilkynningaaðferð** skal færa inn **Athugasemd**.  
6.  Velja hnappinn **Í lagi**.  
7.  Í glugganum **Uppsetning tilkynninga** í flipanum **Heim** í hópnum **Ferli** skal velja **Tilkynningaáætlun**.  
8.  Í glugganum **Tilkynningaáætlun** skal í reitnum **Atburður** velja **Samstundis**.  
9. Velja hnappinn **Í lagi**.  

## <a name="creating-the-approval-workflow"></a>Stofna samþykktarverkflæði  
 Stofna samþykktarverkflæði fyrir innkaupapöntun með því að afrita skref úr verkflæðissniðmáti fyrir samþykktarverkflæði innkaupapöntunar. Hafið fyrirliggjandi verkflæðisþrep óbreyttar og virkið þau síðan í verkflæði.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Til að stofnaog virkja samþykktarverkflæði innkaupapöntunar  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.  
2.  Í glugganum **Verkflæði** á flipanum **Aðgerðir** í hópnum **Almennt** skal velja **Stofna verkflæði úr sniðmáti**.  
3.  Á flipanum **Aðgerðir** í hópnum **Almennt** skal velja **Stofna verkflæði úr sniðmáti**. Glugginn **sniðmát verkflæðis** opnast.  
4.  Veljið verkflæðissniðmát með heitinu „Samþykktarverkflæði innkaupapöntunar“ og veljið síðan hnappinn **Í lagi**.  

    Glugginn **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti. Við gildið í reitnum **Kóði** er bætt við „-01“ til að gefa til kynna að þetta sé fyrsta verkflæðið sem er stofnað úr verkflæðissniðmátinu Samþykktarverkflæði innkaupapöntunar.  
5.  Í haus **Verkflæði** gluggans, veldu **virkjað** gátreitinn.  

## <a name="starting-a-notification-job-queue"></a>Að hefja tilkynningu um vinnslubiðröð  
Ganga skal úr skugga um að verkröð í uppsetningu sé sett upp þannig að hún meðhöndli verkflæðistilkynningar.  

### <a name="to-start-the-notify-job-queue"></a>Til að ræsa verkröðina TILKYNNA  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkraðir** og velja svo viðeigandi tengil.  
2.  Í glugganum **Verkraðir** skal velja línuna TILKYNNA verkröð og svo, á flipanum **Heim** í hópnum **Ferli**, skal velja **Hefja verkröð**.  

## <a name="using-the-approval-workflow"></a>Að nota samþykktarverkflæði  
Nota nýja verkflæðið, Innkaupapöntun verkflæði samþykktar, með því að skrá þig fyrst inn sem Alicia í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fara fram á samþykki á innkaupapöntun. Síðan skaltu skrá þig inn sjálfur, skoða athugasemdina í hlutverkamiðstöð, fylgja tenglinum á samþykktarbeiðnina og síðan samþykkja beiðni.  

Til að framkvæma innskráningu í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem aðrir notendur, verður að nota **Keyra sem annar notandi** virknina.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>Til að skrá sig inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Alicia.  

1.  Fyrir vefbiðlarann í [!INCLUDE[d365fin](includes/d365fin_md.md)], skal á Opna-hnappinum fyrir vefsíðuna í vafranum ýta á Shift + hægri-smella og velja svo **Keyra sem annar notandi**.  

    Fyrir Windows-biðlarann í [!INCLUDE[d365fin](includes/d365fin_md.md)], skal á Opna-hnappinum fyrir forritið ýta á Shift + hægri-smella og velja svo **Keyra sem annar notandi**.  

2.  Í **Windows öryggisatriði** glugganum, færa inn [TÖLVA NAFN]ALICIA og lykilorðið sem krafist er.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Til að óska eftir samþykki á innkaupapöntun, sem Alicia  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupapantanir** og velja svo viðeigandi tengil.  
2.  Veljið línuna fyrir opna innkaupapöntun 104001 og því næst á flipanum **Heim** í flokknum **Stjórna** skal velja **Breyta**.  
3.  Í glugganum **Innkaupapöntun** og á flipanum **Aðgerðir** í hópnum **Samþykki** skal velja **Senda samþykktarbeiðni**.  

    Takið eftir að gildið í reitnum **Staða** hefur breyst í **Bíður samþykktar**.  

4.  Loka [!INCLUDE[d365fin](includes/d365fin_md.md)]  

### <a name="to-approve-the-purchase-order-as-sean"></a>Til að samþykkja innkaupapöntun, sem Sean  

1.  Opnaðu [!INCLUDE[d365fin](includes/d365fin_md.md)] eins og þú gerir almennt. Forritið opnast með þig sem notanda.  
2.  Í hluverkamiðstöð, í **Mínar tilkynningar** glugganum skaltu leita að athugasemd frá Alicia.  

    > [!NOTE]  
    >  Þótt tíðni tilkynningu sé stillt á **Samstundis** mun athugasemdin berast u.þ.b. einni mínútu eftir Alicia senda beiðni um samþykki. Þetta er vegna sjálfgefna endurtekningartíðni af aðgerðinni Verkröð.  

3.  Þegar athugasemdin birtist í glugganum **Mínar tilkynningar** er valið gildið **Samþykktarfærsla: XX, XX** í **Síða** reit. Glugginn **Beiðnir til að samþykkja** opnast og beiðni Aliciu um innkaupapöntun er auðkennd.  
4.  Í glugganum **Beiðnir til að samþykkja** á flipanum **Heim** í hópnum **Ferli** skal velja **Samþykkja**.  

    Gildið í reitnum **Staða** í Alicia á innkaupapöntun breytist í **Útgefin**.  

Nú hefur þú sett upp og prófa einfalt samþykktarverkflæðis samkvæmt fyrstu tvö skref í verkflæði samþykktarverkflæðis innkaupapöntunar. Hægt er að auðveldlega að framlengja þessu verkflæði sjálfkrafa til að bóka innkaupapöntun Alicia sjálfvirkt þegar Sean samþykkir það. Til að gera þetta þarf að virkja verkflæði fyrir innkaupareikningsverkflæði þar sem svar við útgefnar innkaupareikningur er til að bóka hann. Fyrst þarf að breyta skilyrðum tilviksins á fyrsta skrefið verkflæði (innkaup) úr **Reikningur** í **Pöntun**.  

Almenna útgáfan af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur númer sniðmáts verkflæðis fyrir dæmi sem eru studd af forritskóðanum. Megnið af þeim eru fyrir samþykkisverkflæði. Frekari upplýsingar eru í Verkflæðivinnublaði.  

Þú skilgreinir útfærslur af verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins. Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).  

Ef viðskiptasviðsmynd kallar á verkflæðistilvik eða -viðbrögð sem ekki eru studd verður Microsoft-samstarfsaðili að virkja þau með því að sérstilla forritakóðann. Nánari upplýsingar er að finna í [Sýnikennsla: Innleiðing nýrra verkflæðistilvika og svara](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) í þróunar- og IT-pro hjálp.  

## <a name="see-also"></a>Sjá einnig  
[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)   
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)   
[Búa til verkflæði](across-how-to-create-workflows.md)   
[Nota Samþykktarverkflæði](across-how-use-approval-workflows.md)   
[Verkflæði](across-workflow.md)

