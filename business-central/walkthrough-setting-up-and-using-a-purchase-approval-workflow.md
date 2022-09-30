---
title: Uppsetning og notkun á samþykktarverkflæði innkaupa
description: Þessi kynning fer með þig í gegnum öll stigin sem felast í því að setja upp og nota samþykktarverkflæði innkaupa í Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: bf58b9f1c0702275df1dc6e2884444369d084b80
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585410"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa

Hægt er að gera sjálfvirkt ferli samþykktar á nýjar eða breyttar færslur, t.d. skjöl, færslubókarlínur og spjöld viðskiptamanna með því að stofna verkflæði með skrefum fyrir viðkomandi samþykkjendur.

Áður en samþykkisverkflæði eru stofnaðar verður að setja upp samþykkjandi og staðgengill samþykkjanda fyrir hvern notanda samþykktar. Einnig er hægt að stilla upphæðamörk samþykkjendur til að skilgreina hvaða sölu-og innkaupafærslur þeir eru hæfir til að samþykkja. Samþykktarbeiðnir og aðrar tilkynningar er hægt að senda sem tölvupóst eða inneignarnótur. Fyrir hverja uppsetningu samþykktarnotanda má einnig setja upp hvenær þeim berast tilkynningar.

> [!NOTE]
> Til viðbótar við Workflow-virknina innan [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að nota Power Automate til að skilgreina verkflæði fyrir tilvik í [!INCLUDE[prod_short](includes/prod_short.md)]. Hafa skal í huga að þótt þetta séu tvö aðskilin verkflæðiskerfi, þá eru öll Flow-sniðmát sem búin eru til með Power Automate bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prod_short](includes/prod_short.md)]. [Frekari upplýsingar eru í notkun miðsvæðis í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md).  

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði. Frekari upplýsingar á [verkflæði](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Um þetta Walk

Þessi gönguleið er atburðarás sem sýnir eftirtalin verkefni:  

- Setja upp notendur samþykktar  
- Setja upp tilkynningar fyrir samþykktarnotendur  
- Breyta og virkja samþykktarverkflæði  
- Beiðni um samþykki innkaupapöntunar (sem Alicia)  
- Móttekur tilkynningu og samþykkir síðan beiðnina (sem Sean)  

## <a name="story"></a>Ferill

Sean er yfirnotandi í CRONUS. Hann stofnar tvo skjalasamþykktarnotendur. Annar er Alicia sem táknar innkaupaaðilinn. Hinn er sá sem stendur fyrir samþykktaraðila Alicia. Sean gefur sjálfur út ótal innkaupasamþykktarréttindi og Tilgreinir að hann fái tilkynningar með innri nótum um leið og viðkomandi atburður á sér stað. Loks býr Sean til áskilið samþykktarverkflæði sem afrit af fyrirliggjandi *sniðmáti fyrir samþykki* á innkaupapöntun, fer með öll núverandi skilyrði og svarmöguleika óbreytt og virkjar svo verkflæðið.  

Til að prófa samþykktarverkflæðið, skráir Sean sig á [!INCLUDE[prod_short](includes/prod_short.md)] sem Alicia og biður síðan um samþykki innkaupapöntunar. Sean undirritar þá í eins og sér, sér nótuna í hlutverkamiðstöð sinni, segir tengilinn á samþykkisbeiðni fyrir innkaupapöntunina og samþykkir beiðnina.  

## <a name="users"></a>Notendur

Áður en hægt er að setja upp samþykktarnotendur og tilkynningameðferð þeirra verður að ganga úr skugga um að notendur séu í [!INCLUDE[prod_short](includes/prod_short.md)] : einn notandi stendur fyrir Alicia. Hinn notandinn, þú sjálf(ur), táknar Sean. Frekari upplýsingar hjá [Stofna notendur samkvæmt leyfum](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Setja upp notendur samþykktar

Þegar skráð í hann er sjálfur, setjið þá upp Alicia sem samþykktarnotanda sem samþykkjandi er sjálfur. Setjið upp samþykktarheimildir og Tilgreinið hvernig og hvenær verið er að tilkynna um samþykktarbeiðnir.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Til að setja upp þig sjálfan og Alicia sem notendur samþykki

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning á notanda samþykktar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Notandauppsetning samþykktar** skal velja aðgerðina **Nýtt**.  

    > [!NOTE]  
    >  Setja verður upp samþykkjanda áður en hægt er að setja upp notendur sem þurfa sem samþykki þess samþykkjanda. Það þýðir að þú verður að stilla þig upp áður en þú getur stillt Alicia upp.  

3. Setja upp tvo samþykktarnotendur með því að fylla í reitina eins og lýst er í eftirfarandi töflu.  

    |Notandakenni|Kenni samþykkjanda|Ótakmörkuð innkaupaheimild|  
    |-------|-----------|---------------------------|  
    |ÞÚ||Valið|
    |ALICIA|ÞÚ||

### <a name="setting-up-notifications"></a>Tilkynningar settar upp

Í þessum gönguvefum er notandinn látinn vita með innri athugasemd um beiðnir til samþykktar. Einnig er hægt að senda samþykktartilkynningar með tölvupósti og hægt er að bæta við svarþrepi verkflæðis sem lætur sendanda vita þegar beiðni er samþykkt eða henni er hafnað. Frekari upplýsingar eru tilgreindar í [Tilgreinið hvenær og hvernig á að taka á móti tilkynningum](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Til að setja upp hvernig og hvenær þú færð tilkynningu

1. Á síðunni **Notandauppsetning samþykktar** velur notandi línuna fyrir sjálfa(n) sig og svo aðgerðina **Tilkynningagrunnur**.  
2. Á síðunni **Uppsetning tilkynninga** í reitnum **Tilkynningagerð** skal velja **Samþykki**.  
3. Í reitnum **Aðferð tilkynningar** skal velja **Athugasemd**.  
4. Á síðunni **Tilkynningagrunnur** skal velja aðgerðina **Áætlun tilkynninga**.  
5. Á síðunni **Tilkynningaáætlun** í reitnum **Endurtekning** skal velja **Samstundis**.  

## <a name="creating-the-approval-workflow"></a>Stofnun samþykktarverkflæðis

Stofnið samþykktarverkflæði innkaupapöntunar með því að afrita skrefin úr **samþykktarverkflæði** samþykkts innkaupapapöntunarinnar. Hafið fyrirliggjandi verkflæðisþrep óbreyttar og virkið þau síðan í verkflæði.  

> [!TIP]
> Einnig er hægt að bæta við svarskrefi verkflæðis til að tilkynna sendanda þegar beiðni er samþykkt eða henni er hafnað. Frekari upplýsingar eru tilgreindar í [Tilgreinið hvenær og hvernig á að taka á móti tilkynningum](across-how-to-specify-when-and-how-to-receive-notifications.md).

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Til að stofnaog virkja samþykktarverkflæði innkaupapöntunar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **verkflæði** og velja síðan tengdan tengil.  
2. Á síðunni **Verkflæði** skal velja **Aðgerðir** og svo **Nýtt** og svo **Nýtt vinnuflæði úr Sniðmáti** aðgerðina.  
3. Á síðunni **Verkflæðissniðmát** skal velja verkflæðissniðmát með heitinu **Samþykktarverkflæði innkaupapöntunar**.  

   Síðan **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti. Gildið í **reitnum kóti** er útvíkkað með *-01* til að gefa til kynna þetta er fyrsta verkflæði sem búið er til úr sniðmáti fyrir verkflæði **fyrir** innkaupapöntun.  
4. Á Haus **verkflæðissíðunnar** er kveikt á **virkjunni** skipta.  

## <a name="use-the-approval-workflow"></a>Nota samþykktarverkflæðið

Notið nýja samþykktarverkflæðið fyrir innkaupapöntun með því að skrá sig fyrst inn í [!INCLUDE[prod_short](includes/prod_short.md)] Alicia til að biðja um samþykki á innkaupapöntun. Skráðu þig þá inn eins og þér er bent á, Skoðaðu nótuna á hlutverkamiðstöðinni, fylgdu beiðninni á samþykkisbeiðnina og samþykktu síðan beiðnina.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Til að óska eftir samþykki á innkaupapöntun, sem Alicia

1. Skrá inn sem Alicia.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **innkaupapantanir** og veljið síðan tengda tengilinn.  
3. Veljið línuna til að opna *106001* innkaupapöntun.  
4. Á síðunni **Innkaupapöntun** skal velja **Aðgerðir**, svo **Biðja um samþykki** og svo **Senda samþykktarbeiðni** aðgerðina.  

Takið eftir að gildið í reitnum **Staða** hefur breyst í **Bíður samþykktar**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Til að samþykkja innkaupapöntun, sem Sean

1. Skrá inn sem Sean.
2. Á hlutverkamiðstöðinni, á **sjálfu þjónustusvæðinu**, velur **beiðnir til samþykktar**.
3. **Á síðunni beiðnir til samþykktar** skal velja línuna um innkaupapöntunina frá Alicia og velja **síðan samþykkja** aðgerðina.  

Gildið í reitnum **Staða í** innkaupapöntun frá Alicia breytist í **Losað**.  

Nú er búið að setja upp og prófa einfalt samþykktarverkflæði eftir fyrstu tveimur skrefum **samþykktarverkflæðis** innkaupapöntunarinnar. Auðvelt er að víkka þetta verkflæði til að það bóki sjálfkrafa innkaupapöntun Alicia þegar Sean samþykkir hana. Til að gera þetta verður að virkja **verkflæði** innkaupareikins svo svarið við útgefinni innkaupareikningi sé til að bóka það. Fyrst þarf að breyta skilyrðum tilviksins á fyrsta skrefið verkflæði (innkaup) úr **Reikningur** í **Pöntun**.  

Almenn útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur mörg verkflæðissniðmát fyrir áætlanir sem eru studdar af forritskóta. Flest þessara sniðmáta eru fyrir samþykktarverkflæði.  

Afbrigði af verkflæði eru skilgreind með því að fylla út í reiti í verkflæðislínum með því að nota fasta lista yfir tilvik og svargildi sem tákna áætlanir sem kóti forrits styður. Frekari upplýsingar um [Stofna verkflæði](across-how-to-create-workflows.md).  

[!INCLUDE[workflow](includes/workflow.md)]

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/use-approval-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Stofna samþykktarverkflæði](across-how-to-create-workflows.md)  
[Nota Samþykktarverkflæði](across-how-use-approval-workflows.md)  
[Verkflæði](across-workflow.md)  
[Nota Viðskiptamiðað í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
