---
title: Uppsetning og notkun verkflæðis innkaupasamþykktar | Microsoft Docs
description: Hægt er að gera sjálfvirkt ferli samþykktar á nýjar eða breyttar færslur, t.d. skjöl, færslubókarlínur og spjöld viðskiptamanna með því að stofna verkflæði með skrefum fyrir viðkomandi samþykkjendur. Áður en samþykkisverkflæði eru stofnaðar verður að setja upp samþykkjandi og staðgengill samþykkjanda fyrir hvern notanda samþykktar. Einnig er hægt að stilla upphæðartakmörk samþykkjenda til að skilgreina hvaða sölu- og innkaupafærslur þeir mega samþykkja. Samþykktarbeiðnir og aðrar tilkynningar er hægt að senda sem tölvupóst eða innri athugasemd. Fyrir hverja uppsetningu samþykktarnotanda má einnig setja upp hvenær þeim berast tilkynningar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: aad06d141b8c4a07782a27187f7fa5f580ebe28e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759993"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa

Hægt er að gera sjálfvirkt ferli samþykktar á nýjar eða breyttar færslur, t.d. skjöl, færslubókarlínur og spjöld viðskiptamanna með því að stofna verkflæði með skrefum fyrir viðkomandi samþykkjendur. Áður en samþykkisverkflæði eru stofnaðar verður að setja upp samþykkjandi og staðgengill samþykkjanda fyrir hvern notanda samþykktar. Einnig er hægt að stilla upphæðartakmörk samþykkjenda til að skilgreina hvaða sölu- og innkaupafærslur þeir mega samþykkja. Samþykktarbeiðnir og aðrar tilkynningar er hægt að senda sem tölvupóst eða innri athugasemd. Fyrir hverja uppsetningu samþykktarnotanda má einnig setja upp hvenær þeim berast tilkynningar.

> [!NOTE]
> Til viðbótar við Workflow-virknina innan [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að nota Power Automate til að skilgreina verkflæði fyrir tilvik í [!INCLUDE[prod_short](includes/prod_short.md)]. Hafa skal í huga að þótt þetta séu tvö aðskilin verkflæðiskerfi, þá eru öll Flow-sniðmát sem búin eru til með Power Automate bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Notkun Business Central í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md).  

 Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Um kynninguna

Þessi kynning fjallar um eftirfarandi verk:  

- Setja upp notendur samþykktar.  
- Setja upp tilkynningar fyrir samþykki notendur.  
- Breyta og virkjun verkflæði samþykkta.  
- Óska eftir samþykki á innkaupapöntun, sem Alicia.  
- Taka á móti tilkynning og síðan samþykkja beiðni, sem Sean.  

## <a name="story"></a>Ferill

Sean er yfirnotandi í CRONUS. Hann stofnar tvo skjalasamþykktarnotendur. Annar er Alicia sem táknar innkaupaaðilinn. Hinn er sá sem stendur fyrir samþykktaraðila Alicia. Sean síðan veitir sjálfum sér ótakmarkaðan innkaupasamþykktarréttur og tilgreinir að hann fær tilkynningar með innri athugasemd um leið og viðeigandi atburðurinn á sér stað. Í síðasta lagi stofnar Sean nauðsynlegt samþykktarverkflæði sem afrit af fyrirliggjandi samþykktarverkflæði innkaupapöntunarsniðmáts, gerir ekki breytingar á fyrirliggjandi skilyrði og svör tilviksins svo virkjar hann verkflæðið.  

Til að sannprófa verkflæði samþykktar, skráir Sean sig fyrir inn í [!INCLUDE[prod_short](includes/prod_short.md)] sem Alicia og biður svo um samþykki á innkaupapöntun. Síðan skráir Sean sig inn sem hann sjálfur, sér athugasemdina í Mitt hlutverk, fylgir tenglinum á samþykktarbeiðnina fyrir innkaupapöntunina og samþykkir beiðnina.  

## <a name="users"></a>Notendur

Áður en þú getur sett upp samþykktarnotendur og tilkynningaaðferð þeirra verðurðu að ganga úr skugga um að tveir notendur séu til í [!INCLUDE[prod_short](includes/prod_short.md)]: Einn mun tákna Aliciu. Hinn notandinn, þú sjálf(ur), táknar Sean. Nánari upplýsingar er að finna í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)

### <a name="setting-up-approval-users"></a>Setja upp samþykktarnotendur

Þegar þú hefur skráð þig inn sem þú sjálf(ur) skal setja upp Aliciu sem samþykktaraðila sem ert þú sjálf(ur). Settu upp að samþykktarréttindi þín og tilgreindu hvernig og hvenær þú færð tilkynningu um samþykktarbeiðni.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Til að setja upp þig sjálfan og Alicia sem notendur samþykki

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning samþykktar** og veldu síðan tengda tengilinn.  
2. Á síðunni **Notandauppsetning samþykktar** skal velja aðgerðina **Nýtt**.  

    > [!NOTE]  
    >  Setja verður upp samþykkjanda áður en hægt er að setja upp notendur sem þurfa sem samþykki þess samþykkjanda. Því verður að setja upp sjálfan þig áður en þú setur upp Alicia.  

3. Setja upp tvo samþykktarnotendur með því að fylla í reitina eins og lýst er í eftirfarandi töflu.  

    |Notandakenni|Kenni samþykkjanda|Ótakmörkuð innkaupaheimild|  
    |-------------|-----------------|---------------------------------|  
    |ÞÚ||Valið|  
    |ALICIA|ÞÚ||  

### <a name="setting-up-notifications"></a>Tilkynningar settar upp

Í þessari kynningu er notandanum tilkynnt með innri athugasemd um beiðnir til að samþykkja. Samþykktartilkynningu er einnig hægt að senda með tölvupósti og hægt að bæta við svarskrefi verkflæðis sem tilkynnir sendanda þegar beiðni er samþykkt eða henni er hafnað. Frekari upplýsingar eru í [Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Til að setja upp hvernig og hvenær þú færð tilkynningu

1. Á síðunni **Notandauppsetning samþykktar** velur notandi línuna fyrir sjálfa(n) sig og svo aðgerðina **Tilkynningagrunnur**.  
2. Á síðunni **Uppsetning tilkynninga** í reitnum **Tilkynningagerð** skal velja **Samþykki**.  
3. Í reitnum **Aðferð tilkynningar** skal velja **Athugasemd**.  
4. Á síðunni **Tilkynningagrunnur** skal velja aðgerðina **Áætlun tilkynninga**.  
5. Á síðunni **Tilkynningaáætlun** í reitnum **Endurtekning** skal velja **Samstundis**.  

## <a name="creating-the-approval-workflow"></a>Stofna samþykktarverkflæði

Stofna skal samþykktarverkflæði innkaupapöntunar með því að afrita skrefin úr verkflæðissniðmáti **Samþykktarverkflæði innkaupapöntunar**. Hafið fyrirliggjandi verkflæðisþrep óbreyttar og virkið þau síðan í verkflæði.  

> [!TIP]
> Einnig er hægt að bæta við svarskrefi verkflæðis til að tilkynna sendanda þegar beiðni er samþykkt eða henni er hafnað. Frekari upplýsingar eru í [Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md).

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Til að stofnaog virkja samþykktarverkflæði innkaupapöntunar

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkflæði** og veldu síðan tengda tengilinn.  
2. Á síðunni **Verkflæði** skal velja aðgerðina **Nýtt verkflæði úr sniðmáti**.  
3. Á síðunni **Verkflæðissniðmát** skal velja verkflæðissniðmát með heitinu **Samþykktarverkflæði innkaupapöntunar** og velja síðan hnappinn **Í lagi**.  

    Síðan **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti. Við gildið í reitnum **Kóði** er bætt við *-01* til að gefa til kynna að þetta sé fyrsta verkflæðið sem er stofnað úr verkflæðissniðmátinu **Samþykktarverkflæði innkaupapöntunar**.  
4. Á haus síðunnar **Verkflæði** skal velja gátreitinn **Virkjað**.  

## <a name="using-the-approval-workflow"></a>Að nota samþykktarverkflæði

Nota nýja verkflæðið, verkflæði samþykktar fyrir Innkaupapöntun, með því að skrá þig fyrst inn sem Alicia í [!INCLUDE[prod_short](includes/prod_short.md)] til að fara fram á samþykki á innkaupapöntun. Síðan skaltu skrá þig inn sjálf(ur), skoða athugasemdina í hlutverkamiðstöð, fylgja tenglinum á samþykktarbeiðnina og síðan samþykkja beiðni.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Til að óska eftir samþykki á innkaupapöntun, sem Alicia

1. Skrá inn sem Alicia.
2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.  
3. Velja skal línu fyrir opna innkaupapöntun 106001 og svo aðgerðina **Breyta**.  
4. Á síðunni **Innkaupapöntun** skal velja **Senda samþykktarbeiðni** aðgerðina.  

Takið eftir að gildið í reitnum **Staða** hefur breyst í **Bíður samþykktar**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Til að samþykkja innkaupapöntun, sem Sean

1. Skrá inn sem Sean.
2. Á Mitt hlutverk, í svæðinu **Sjálfsafgreiðsla** skaltu velja reitinn **Beiðnir til að samþykkja**.
3. Á síðunni **Beiðnir til að samþykkja** skaltu velja línuna um innkaupapöntunina frá Alicia go velja svo aðgerðina **Samþykkja**.  

Gildið í reitnum **Staða í** innkaupapöntun frá Alicia breytist í **Losað**.  

Nú hefur þú sett upp og prófa einfalt samþykktarverkflæðis samkvæmt fyrstu tvö skref í verkflæði samþykktarverkflæðis innkaupapöntunar. Auðvelt er að víkka þetta verkflæði til að það bóki sjálfkrafa innkaupapöntun Alicia þegar Sean samþykkir hana. Til að gera þetta þarf að virkja verkflæði fyrir innkaupareikningsverkflæði þar sem svar við útgefnar innkaupareikningur er til að bóka hann. Fyrst þarf að breyta skilyrðum tilviksins á fyrsta skrefið verkflæði (innkaup) úr **Reikningur** í **Pöntun**.  

Almenna útgáfan af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur númer sniðmáts verkflæðis fyrir dæmi sem eru studd af forritskóðanum. Megnið af þeim eru fyrir samþykkisverkflæði.  

Þú skilgreinir útfærslur af verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins. Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).  

Ef viðskiptasviðsmynd kallar á verkflæðistilvik eða -viðbrögð sem ekki eru studd verður Microsoft-samstarfsaðili að virkja þau með kóðanum, en einnig er hægt að setja upp verkflæði með Power Automate. Frekari upplýsingar er að finna í [Notkun [!INCLUDE[prod_short](includes/prod_short.md)] í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md) eða [Tilvik í AL](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al) í hjálp fyrir forritara, eftir því sem við á.

## <a name="see-also"></a>Sjá einnig

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Búa til verkflæði](across-how-to-create-workflows.md)  
[Nota Samþykktarverkflæði](across-how-use-approval-workflows.md)  
[Verkflæði](across-workflow.md)  
[Notkun Business Central í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]