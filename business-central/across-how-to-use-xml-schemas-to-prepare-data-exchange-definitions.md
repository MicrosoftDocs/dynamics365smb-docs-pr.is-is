---
title: XML-skema til að undirbúa skilgreiningar gagnaskipta
description: Notaðu XML-skema til að setja upp gagnaskiptaramma til að skilgreina hvaða gagnaeiningar á að skiptast við.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>Nota XML-skema til að undirbúa skilgreiningar gagnaskipta

Til að virkja innflutningur/útflutningur gagna í skrá í gegnum gagnaskiptaumgjörð í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að nota XML-skema til að tilgreina hvaða gagnastök á að skiptast á við [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi aðgerð er gerð á síðunni **XML-skemaskoðun** með því að hlaða XML-skemaskránni, velja viðeigandi gagnastök og ræsa skilgreiningu gagnaskipta.  

 Þegar búið er að skilgreina hvaða gagnastök á að hafa með er hægt að nota **Mynda skilgreiningu gagnaskipta** aðgerð til að frumstilla gagnaskiptiskilgreiningu byggt á völdum gagnastökum sem síðan er lokið í Data Exchange Framework. Þetta stofnar færslu á síðunni **Bókunarskilgreiningar** þar sem haldið er áfram að skilgreina hvaða einingar í SEPA skráakortinu tengjast hvaða reitum í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

 Þetta efnisatriði inniheldur eftirfarandi ferli:  

- Til að hlaða XML-skemaskrá  

- Að velja eða hreinsa hnúta á XML-skema  

- Að búa til gagnaskiptaskilgreiningu sem byggist á XML-skema  

## <a name="to-load-an-xml-schema-file"></a><a name="to-load-an-xml-schema-file"></a><a name="to-load-an-xml-schema-file"></a>Til að hlaða XML-skemaskrá

1. Ganga úr skugga um að viðeigandi XML-skemaskrá sé í boði. Skráarendingin er .xsd.  

2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **XML-skema** og velja síðan viðkomandi tengil.  

3. Valið er aðgerðin **Nýtt**.  

4. Fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Kóti**|Tilgreina kóða til að greina fyrir XML-skemað.|  
    |**Lýsing**|Tilgreinir lýsingu á XML-skema.|  

     Reiturinn **Marknafnabil** tilgreinir hvaða nafnrými í XML-skemaskrá hefur verið hlaðið fyrir þessa línu.  

5. Veldu aðgerðina **Hlaða skema** og veldu síðan XML-skemaskrána.  

     Þegar skránni er hlaðið eru allir hinir reitirnir á línunni fylltir út með upplýsingum úr skránni og gátreiturinn **Skema er hlaðið** valinn.  

    > [!NOTE]  
    >  Tré hlaðins XML-skema er sjálfkrafa samanfallið. Hver hnútur er stækkaður með því að velja **+** hnappinn á hnútinu. Til að auka alla hnúða er valið **Stækka Allt** á borðanum.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><a name="to-select-or-clear-nodes-in-an-xml-schema"></a><a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Að velja eða hreinsa hnúta á XML-skema

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **XML-skemaskoðun** og velja síðan viðkomandi tengil.  

2. Fylla inn í reitina í hausnum eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**XML-skemakóði**|Tilgreinið XML-skemaskrá sem var hlaðið í skrefi 5 í „Að hlaða inn XML-skemaskrá“ hlutanum.|  
    |**Ný XMLport nr.**|Tilgreinið númer XMLport sem er búin til úr þessu XML-skema þegar þú velur **Mynda XMLport** aðgerðina.|  

     Línurnar eru nú fylltar hnútum sem tákna allar einingar í XML-skema. Hnútar fyrir einingar sem eru áskyldar samkvæmt XML-skemanu eru sjálfgefið valdir.  

3. Á fyrstu línunni, í dálknum **Heiti hnútar**, skal stækka hnútinn **Fylgkskjal** og stækka svo smám saman undirliggjandi hnúta sem á að skoða.  

     Að öðrum kosti skal hægrismella á hnútinn og velja svo **Stækka allt**.  

4. Veldu aðra hvora eftirfarandi aðgerða til að breyta því hvaða hnútar eru birtir.  

    |**Aðgerð**|Lýsing|  
    |----------------|---------------------------------------|  
    |**Sýna allt**|Allir hnútar er sýndir.|  
    |**Fela það sem ekki er áskilið**|Aðeins eru birtir hnútar sem standa fyrir einingar sem krafist samkvæmt XML-skemanu. Þessir tengipunktar eru vanalega táknaðir með **1** í reitnum **MinOccurs**.<br /><br /> Veldu **Sýna alla** að snúa við útsýni.|  
    |**Fela það sem ekki er valið**|Aðeins hnútar þar sem gátreiturinn **Valið** er valinn sjást.<br /><br /> Veldu **Sýna alla** að snúa við útsýni.|  

5. Veldu aðgerðina **Breyta**.  

6. Í **Valið** gátreitnum skal tilgreina fyrir hvern hnút ef stak á að vera stutt í gagnaskiptauppsetningu fyrir viðkomandi SEPA bankaskrá.  

    > [!NOTE]  
    >  Þegar þú velur áskilinn undirhnút eru allir yfirhnútar fyrir ofan undirhnútinn einnig valdir.  

7. Veldu aðgerðina **Velja allar áskildar einingar** til að endurvelja alla hnúta sem tákna einingar sem eru áskildar samkvæmt XML-skema.  

8. Veldu **Afvelja allt** aðgerð til að hreinsa allt val.  

     Reiturinn **Val** tilgreinir að hnúturinn hefur tvo eða fleiri systkinahnúta sem valkosti.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Að búa til gagnaskiptaskilgreiningu sem byggist á XML-skema

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **XML-skema** og velja síðan viðkomandi tengil.  

2. Veldu viðeigandi XML-skema og veldu svo aðgerðina **Opna XML-skemaskoðun**.  

3. Gangið úr skugga um að viðeigandi hnútar séu valdir. Nánari upplýsingar fást í hlutanum „Að velja eða hreinsa hnúta í XML-skema“.  

4. Á síðunni **XML-skemaskoðun** skaltu velja aðgerðina **Mynda skilgreiningu gagnaskipta**.  

 Gagnaskiptaskilgreining er sett upp á síðunni **Bókunarskilgreiningar**, sem hægt er að ljúka með því að tilgreina hvaða stök í skránni varpast í hvaða reiti í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
> Einnig er hægt að nota **Sækja skráaskipan** virknina á **Bókunarskilgreining** síðunni sem notar virkni **XML-skemaskoðun** til að fylla út í flýtiflipann **Dálkaskilgreiningar**.  

> [!NOTE]
> Í 2019 útgáfutímabili 1 og fyrri útgáfum var hægt að búa til XMLport sem byggðist á skemanu og síðan flutt inn í lausnina. Þetta er ekki lengur stutt.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)  
[Flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  
[Um gagnaskiptaramma](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
