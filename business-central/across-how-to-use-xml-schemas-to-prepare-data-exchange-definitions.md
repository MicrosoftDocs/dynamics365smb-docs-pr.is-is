---
title: Búa til XMLports út frá XML-skemum | Microsoft Docs
description: Notaðu XML skjöl til að setja upp ramma skjalaskipta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 91f21f3b6382aee410ea1de51f371999ac86281c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800428"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>Nota XML-skema til að undirbúa skilgreiningar gagnaskipta
Til að virkja innflutningur/útflutningur gagna í skrá í gegnum gagnaskiptaumgjörð í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að nota XML-skema til að tilgreina hvaða gagnastök á að skiptast á við [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessi aðgerð er gerð á síðunni **XML-skemaskoðun** með því að hlaða XML-skemaskránni, velja viðeigandi gagnastök og ræsa því næst annað hvort skilgreiningu gagnaskipta eða XMLport.  

 Þegar búið er að skilgreina hvaða gagnastök á að hafa með, samkvæmt XML-skema, má nota aðgerðina **Mynda XMLport** til að stofna XMLport-hlutinn.  

 Einnig er hægt að nota **Mynda gagnaskiptiskilgreiningu** aðgerð til að frumstilla gagnaskiptiskilgreiningu byggt á völdum gagnastökum sem síðan er lokið í Data Exchange Framework. Þetta stofnar færslu á síðunni **Bókunarskilgreiningar** þar sem haldið er áfram að skilgreina hvaða einingar í SEPA skráakortinu tengjast hvaða reitum í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

 Þetta efnisatriði inniheldur eftirfarandi ferli:  

-   Til að hlaða XML-skemaskrá  

-   Að velja eða hreinsa hnúta á XML-skema  

-   Að búa til gagnaskiptaskilgreiningu sem byggist á XML-skema  

-   Að búa til XMLport fyrir skrá sem byggir á XML-skema  

-   Að flytja inn XMLport í hlutahönnuð  

### <a name="to-load-an-xml-schema-file"></a>Til að hlaða XML-skemaskrá  

1.  Ganga úr skugga um að viðeigandi XML-skemaskrá sé í boði. Skráarendingin er .xsd.  

2.  Í reitnum **Leita** skal færa inn **XML-skema** og velja síðan viðkomandi tengi.  

3.  Á flipanum **Heim** í flokknum **Nýtt** skal velja **Nýtt**.  

4.  Fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Kóti**|Tilgreina kóða til að greina fyrir XML-skemað.|  
    |**Lýsing**|Tilgreinir lýsingu á XML-skema.|  

     Reiturinn **Marknafnabil** tilgreinir hvaða nafnrými í XML-skemaskrá hefur verið hlaðið fyrir þessa línu.  

5.  Á flipanum **Heim** í flokknum **Vinna** skal velja **Hlaða skema** og velja síðan XML-skemaskrána.  

     Þegar skránni er hlaðið eru allir hinir reitirnir á línunni fylltir út með upplýsingum úr skránni og gátreiturinn **Skema er hlaðið** valinn.  

    > [!NOTE]  
    >  Tré hlaðins XML-skema er sjálfkrafa samanfallið. Hver hnútur er stækkaður með því að velja **+** hnappinn á hnútinu. Til að auka alla hnúða er valið **Stækka Allt** á borðanum.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Að velja eða hreinsa hnúta á XML-skema  

1.  Í reitnum **Leita** skal færa inn **XML-skemaskoðun** og velja síðan viðkomandi tengi.  

2.  Fylla inn í reitina í hausnum eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**XML-skemakóði**|Tilgreiniað XML-skemaskrá sem var hlaðið í skrefi 5 í „Að hlaða inn XML-skemaskrá“ hlutanum.|  
    |**Ný XMLport nr.**|Tilgreinið númer XMLport sem er búin til úr þessu XML-skema þegar þú velur **Mynda XMLport** aðgerðina.|  

     Línurnar eru nú fylltar hnútum sem tákna allar einingar í XML-skema. Hnútar fyrir einingar sem eru áskyldar samkvæmt XML-skemanu eru sjálfgefið valdir.  

3.  Á fyrstu línunni, í dálknum **Heiti hnútar**, skal stækka hnútinn **Fylgkskjal** og stækka svo smám saman undirliggjandi hnúta sem á að skoða.  

     Að öðrum kosti skal hægrismella á hnútinn og velja svo **Stækka allt**.  

4.  Á flipanum **Heim**, í flokknum **Skoða**, skal velja aðra hvora eftirfarandi aðgerða til að breyta því hvaða hnútar eru birtir.  

    |**Aðgerð**|Lýsing|  
    |----------------|---------------------------------------|  
    |**Sýna allt**|Allir hnútar er sýndir.|  
    |**Fela það sem ekki er áskilið**|Aðeins eru birtir hnútar sem standa fyrir einingar sem krafist samkvæmt XML-skemanu. Þessir tengipunktar eru vanalega táknaðir með **1** í reitnum **MinOccurs**.<br /><br /> Veldu **Sýna alla** að snúa við útsýni.|  
    |**Fela það sem ekki er valið**|Aðeins hnútar þar sem gátreiturinn **Valið** er valinn sjást.<br /><br /> Veldu **Sýna alla** að snúa við útsýni.|  

5.  Á flipanum **Heim** í flokknum **Stjórna** skal velja **Breyta**.  

6.  Í **Valið** gátreitnum skal tilgreina fyrir hvern hnút ef stak á að vera stutt í gagnaskiptauppsetningu fyrir viðkomandi SEPA bankaskrá.  

    > [!NOTE]  
    >  Þegar þú velur áskilinn undirhnút eru allir yfirhnútar fyrir ofan undirhnútinn einnig valdir.  

7.  Veldu aðgerðina **Velja allar áskildar einingar** til að endurvelja alla hnúta sem tákna einingar sem eru áskildar samkvæmt XML-skema.  

8.  Veldu **Afvelja allt** aðgerð til að hreinsa allt val.  

     Reiturinn **Val** tilgreinir að hnúturinn hefur tvo eða fleiri systkinahnúta sem valkosti.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Að búa til gagnaskiptaskilgreiningu sem byggist á XML-skema  

1.  Í reitnum **Leita** skal færa inn **XML-skema** og velja síðan viðkomandi tengi.  

2.  Veljið viðkomandi XML-skema og veljið því næst á flipanum **Heima** í **Ferli** hópnum valkostinn **Opna XML skemaskoðun**.  

3.  Gangið úr skugga um að viðeigandi hnútar séu valdir. Nánari upplýsingar fást í hlutanum „Að velja eða hreinsa hnúta í XML-skema“.  

4.  Á síðunni **XML-skemaskoðun** í flipanum **Heim** í flokknum **Ferli** veljið **Mynda gagnaskiptaskilgreiningu**.  

 Gagnaskiptaskilgreining er sett upp á síðunni **Bókunarskilgreiningar**, sem hægt er að ljúka með því að tilgreina hvaða stök í skránni varpast í hvaða reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  Einnig er hægt að nota **Sækja skráaskipan** virknina á **Bókunarskilgreining** síðunni sem notar virkni **XML-skemaskoðun** til að fylla út í flýtiflipann **Dálkaskilgreiningar**.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Að búa til XMLport sem byggir á XML-skema  

1.  Í reitnum **Leita** skal færa inn **XML-skema** og velja síðan viðkomandi tengi.  

2.  Veljið viðkomandi XML-skema og veljið því næst á flipanum **Heima** í **Ferli** hópnum valkostinn **Opna XML skemaskoðun**.  

3.  Í **Ný XMLport nr.** reitnum skal tilgreina númer sem nýja XMLport-hlutnum verður gefið þegar hann er myndaður.  

4.  Gangið úr skugga um að viðeigandi hnútar séu valdir. Nánari upplýsingar fást í hlutanum „Að velja eða hreinsa hnúta í XML-skema“.  

5.  Á flipanum **Heim**, í flokknum **Vinna**, skal velja **Mynda XMLport** og vista svo hlutinn sem .txt-skrá á viðeigandi stað.  

6. Flytja skal nýja XMLport í [!INCLUDE[d365fin](includes/d365fin_md.md)] þróunarumhverfið og þýða hana.

## <a name="see-also"></a>Sjá einnig  
[Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)   
[Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md)   
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)   
[Um gagnaskiptaramma](across-about-the-data-exchange-framework.md)
