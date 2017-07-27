---
title: "Stjórna VSK skýrslugjöf til skattayfirvalda| Microsoft Docs"
description: "Kynntu þér hvernig skal undirbúa skýrslu sem telur upp VSK-upphæðir af sölu yfir ákveðið tímabil og senda hana til skattyfirvalda."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Hvernig á að: Gefa VSK skýrslu til skattayfirvalda
Í söluyfirlitsskýrslu Evrópubandalaga (EC) eru listar yfir VSK-upphæðir sem þú hefur safnað upp fyrir sölu innan ESB, svo þú getir skilað VSK upphæðunum inn til skattyfirvalda í gegnum netþjónustu þeirra.

> [!NOTE]  
>   Í Bretlandi þurfa öll fyrirtæki sem selja fyrir meira en tiltekna upphæð á ári hverju til viðskiptavina innan ESB að skila inn rafrænni söluyfirlitsskýrslu Evrópubandalaga (EC) á XML formi í gegnum vefsíðu þarlendra skattayfirvalda (HMRC).

Söluyfirlitsskýrsla Evrópubandalaga (EC) virkar aðeins í löndum innan ESB. Hún tekur til dæmis ekki með VSK á sölu til landa eins og Kína og Bandaríkjanna.

Til að skila VSK til skattayfirvalda á rafrænu formi, þarf að tengja [!INCLUDE[d365fin](includes/d365fin_md.md)] við vefþjónustu skattayfirvalda. Til þess þarf að setja upp reikning hjá þínum skattayfirvöldum. Þegar þú ert komin(n) með reikning, geturðu virkjað þjónustutengingu sem við bjóðum upp á í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í Bretlandi geturðu t.d. notað **GovTalk** þjónustutenginguna.

Skýrslan inniheldur eina línu fyrir hverja tegund af viðskiptum við viðskiptavini, og sýnir heildarupphæð fyrir hverja tegund viðskipta. Hægt er að skrá þrjár gerðir viðskipta í skýrslunni:  
  
* B2B vörur  
* B2B þjónusta  
* B2B Þríhliða vörur  
  
B2B vörur og þjónusta tiltaka hvort þú seldir vörur eða þjónustu, og sért undir stjórn stillingarinnar **ESB Þjónusta** í uppsetningu bókunar á VSK. B2B Þríhliða vörur gefa það til kynna hvort þú stundaðir viðskipti við þriðja aðila og sért undir stjórn stillingarinnar **ESB þríhliða viðskipti** í söluskjölum, eins og sölupantanir, reikningar, kreditreikningar osfrv.  
  
Eftir að þú skilar inn skýrslunni, fylgist [!INCLUDE[d365fin](includes/d365fin_md.md)] með þjónustunni og heldur skrá yfir samskipti þín. Reiturinn **Staða** gefur til kynna hvar skýrslan er stödd í ferlinu. Þegar t.d. yfirvöld fara yfir skýrsluna, breytist staða skýrslunnar yfir í **Heppnaðist**. Ef skattayfirvöld finna mistök í skýrslunni sem þú sendir þeim, mun staða skýrslunnar breytast yfir í **Mistókst**. Þú getur skoðað villur undir **Villur og viðvaranir**, leiðrétt þær og svo sent skýrsluna inn aftur. Til að skoða allar EC söluyfirlitsskýrslur þínar, farðu á **EC söluyfirlitsskýrslur** síðuna.  
  
> [!NOTE]  
>   Ef þú notast við aðra aðferð til að senda skýrsluna inn, t.d. með því að flytja út XML og hlaða því svo upp á vefsíðu skattayfirvalda, geturðu eftir á valið **Merkja sem Búið að skila** til að loka skýrslutímabilinu. Eftir að þú merkir skýrsluna sem Búið að skila, er ekki hægt að breyta henni. Ef breyta þarf skýrslunni eftir að hún hefur verið merkt sem útgefin þarf fyrst að enduropna hana. 
  
Eftir að skattayfirvöld fara yfir skýrsluna, munu þau senda tengilið fyrirtækisins tölvupóst. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er tengiliðurinn tiltekinn á síðunni **Upplýsingar um fyrirtækið**. Áður en þú sendir inn skýrsluna skaltu vera viss um að tengiliður hafi verið valinn. 

<!--> [!NOTE]  
>   EC söluyfirlitsskýrsla getur innihaldið allt að 1000 línur. Ef fleiri línur vantar verður að senda inn aðra skýrslu. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Til að tengjast vefþjónustu skattayfirvalda býður
[!INCLUDE[d365fin](includes/d365fin_md.md)] upp á þjónustutengingar sem tengjast við vefsíður skattayfirvalda. Ef þú ert t.d. í Bretlandi, er nauðsynlegt að virkja **GovTalk** þjónustutenginguna.  

1. Í reitnum **Leita að síðu eða skýrslu** skal slá inn **Þjónustutengingar**, og velja síðan viðeigandi tengil. <!-- remember to get the updated text for this-->  
2. Fylltu út nauðsynlega reiti.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Uppsetning EC söluyfirlitsskýrslu
1. Í reitnum **Leita að síðu eða skýrslu** skal slá inn **VSK skýrsla uppsetning**, og velja síðan viðeigandi tengil.  
2. Ef þú vilt láta notendur breyta og endursenda skýrsluna, veldu þá gátreitinn **Breyta innsendum skýrslum**.  
3. Tiltaktu númeraröðina sem nota á í EC söluyfirlitsskýrslunni.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Að undirbúa og senda inn EC söluyfirlitsskýrslu
1. Í reitnum **Leita að síðu eða skýrslu** skal slá inn **EC söluyfirlit**, og velja síðan viðeigandi tengil.  
2. Veljið **Nýtt** og fyllið svo inn í viðeigandi svæði.  
3. Til að útbúa efni skýrslunnar, veljið aðgerðina **Leggja til línur**.  

    > [!NOTE]  
>   Hægt er að endurskoða viðskiptin sem eru innifalin í línunni áður en þú skilar inn skýrslunni. Til að gera það, skaltu velja línuna og svo aðgerðina **Sýna VSK færslur**.  
4. Til að undirbúa skýrsluna til innsendingar skal velja aðgerðina **Losa**.  
5. Til að senda skýrsluna inn skal velja aðgerðina **Innsending**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] staðfestir hvort skýrslan sé rétt sett upp. Ef staðfestingin mistekst, eru villurnar sýndar í **Villur og viðvaranir** svo hægt sé að gera viðeigandi breytingar.

## <a name="viewing-communications-with-your-tax-authority"></a>Skoða samskipti við skattayfirvöld
Í sumum löndum er skipst á skilaboðum við skattayfirvöld þegar skýrslur eru sendar inn. Hægt er að skoða fyrstu og síðustu skilaboðin sem voru send eða móttekin með því að velja aðgerðirnar **Hala niður innsendingarskilaboðum** og **Hala niður svarskilaboðum**.  

## <a name="configuring-your-own-vat-reports"></a>Grunnstilla þínar eigin VSK skýrslur
Hægt er að nota EC Yfirlitsskýrslu sem kemur tilbúin, en líka er hægt að búa til sína eigin skýrslu. Til þess þarftu að stofna nokkrar kóðaeiningar. Ef þú þarft aðstoð við það, hafðu samband við Microsoft tengilið.  
    
Eftirfarandi tafla lýsir kóðaeiningunum sem þú þarft að stofna fyrir skýrsluna þína.

| Codeunit | Það sem hún þarf að gera |
|----|-----|
|Tillögulínur| Ná í upplýsingar frá VSK færslutöflunni og birta þær í línum VSK skýrslunnar.|
|Efni | Stjórna sniði skýrslunnar. Til dæmis hvort þú notar XML eða JSON. Gerð sniðs sem á að nota fer eftir skilyrðum vefþjónustu skattayfirvalda. |
|Sending | Stjórnaðu því hvernig og hvenær þú sendir inn skýrsluna, með tilliti til skilyrða skattayfirvalda. |
|Svarstjóri | Stýra skilum frá skattayfirvöldum. Þau gætu t.d. sent tengilið fyrirtækisins tölvupóst. |
|Hætta við | Senda inn afturköllun VSK skýrslu sem var send inn áður til skattayfirvalda. |

> [!NOTE]  
>   Þegar stofnaðar eru kóðaeiningar fyrir skýrsluna skal veita athygli gildinu í reitnum **VSK skýrsla útgáfa**. Þessi reitur verður að endurspegla útgáfuna af skýrslunni sem er eða var send til skattayfirvalda. Þú gætir til dæmis fært inn **2017** í reitinn til að gefa til kynna að skýrslan samræmist þeim kröfum sem voru í gildi það ár. Til að finna núgildandi útgáfu skal hafa samband við skattayfirvöld.  

## <a name="see-also"></a>Sjá einnig .
[Uppsetning VSK](finance-setup-vat.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Hvernig er reikningsfært](sales-setup-sales.md)  

