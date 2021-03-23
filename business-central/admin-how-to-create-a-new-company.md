---
title: Hvernig á að búa til nýtt fyrirtæki | Microsoft Docs
description: Til að nota RapidStart Services eru stofnaðar töflur og síður en engin gögn eru í þeim.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 703b70a608bd6b25b9a3218eb59e8666fcd6a0ab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378324"
---
# <a name="create-a-new-company"></a>Búa til nýtt fyrirtæki
Til að nota RapidStart Services fyrir [!INCLUDE[prod_short](includes/prod_short.md)] skal fyrst stofna nýtt fyrirtæki þar sem framkvæma skal innleiðingu viðskiptamanns. Þegar nýtt fyrirtæki er stofnað eru staðlaðar [!INCLUDE[prod_short](includes/prod_short.md)] töflur og síður búnar til, en engin gögn eru í þeim.

Auk þess er hægt að beita sérstökum uppsetningargögnum fyrir fyrirtækið eftir frumstillingu. Upplýsingarnar koma úr grunnstillingapakka, sem er .rapidstart skrá, sem afhendir innihald á samþjöppuðu formi.  

Grunnstillingarpakkar dæma, þ.á.m. skrár sem miðast við land/svæði eru innifaldar í CRONUS sýnifyrirtækinu. Notið eftirfarandi aðgerð til að nota pakkann með dæmastillingunum með nýju fyrirtæki.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Til að nota dæmið um BASICCONFIG grunnstillingarpakkann  
1. Opna fyrirtækið CRONUS International Ltd. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).
2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingapakkar** og veldu síðan tengda tengilinn.  
3. Velja skal BASICCONFIG-pakkann af listanum og síðan velja aðgerðina **Flytja út pakka**.  

Notið eftirfarandi aðgerð til að búa til nýtt fyrirtæki og nota BASICCONFIC pakkann sem hluta ferlisins.  

## <a name="to-create-a-new-company"></a>Til að búa til nýtt fyrirtæki  
1. Búa til nýtt fyrirtæki. Nánari upplýsingar eru í [Stofna ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).
2. Frá Mitt hlutverk RapidStart Services innleiðara er hægt að flytja inn grunnstillingarpakkann sem hefur verið fluttur úr fyrirtækinu CRONUS International Ltd.

Þegar búið er að stofna nýtt fyrirtæki, eru sumar töflur sjálfkrafa fylltar út, jafnvel þótt fyrirtækissniðmát sé ekki notað. Til dæmis má sjá stöðluðu kótana fyrir bókun og runufærslur á síðunni **Forðakóði**. Ef þú veitir staðbundna útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] ættir þú að fara yfir þessa töflu og íhuga hugsanleg vandamál fyrir viðkomandi tungumál.

## <a name="about-data-tables"></a>Um gagnatöflur
[!INCLUDE[prod_short](includes/prod_short.md)] gagnatöflur eru til í tveim grunntegundum: Aðaltafla og uppsetning. Þegar verið er að setja upp fyrirtækjaskilgreiningu er hægt að nota þessar gerðir til að skerpa á skilgreiningaráætluninni.  

### <a name="master-data-tables"></a>Töflur aðalgagna  
Eftirfarandi tafla sýnir sumar aðalgagnatöflurnar. Þegar nýtt fyrirtæki er frumstillt eru þessar töflur auðar.  

|Tafla nr.|Töfluheiti|  
|-------------------|--------------------|  
|15|Fjárhagsreikningur|  
|18|Viðskiptavinur|  
|23|Lánardrottinn|  
|27|Atriði|  
|5050|Tengiliður|  

### <a name="setup-data-tables"></a>Gagnatöflur uppsetningar  
Í eftirfarandi töflu koma fram sumar uppsetningargagnatöflur þar sem uppsetningarupplýsingar eru fangaðar í grunnstillingarspurningalistanum. Þessar töflur innihalda grunnlínuupplýsingar þegar fyrirtækið er stofnað.  

|Tafla nr.|Töfluheiti|  
|-------------------|--------------------|  
|98|Uppsetning fjárhags|  
|311|Sölugrunnur|  
|312|Innkaupagrunnur|  
|313|Birgðagrunnur|  

Auk uppsetningargagnataflna inniheldur [!INCLUDE[prod_short](includes/prod_short.md)] einnig gögn uppsetningargerðar sem sýna grunnupplýsingar um fyrirtækið og viðskiptaferla þess. Eftirfarandi tafla sýnir nokkrar af þeim.  

|Tafla nr.|Töfluheiti|  
|-------------------|--------------------|  
|3|Greiðsluskilmálar|  
|4|Gjaldmiðill|  
|6|Verðflokkar viðskm.|  
|5700|Birgðahaldseining|

  

## <a name="see-also"></a>Sjá einnig  
[Nota skilgreiningu á ný fyrirtæki](admin-apply-configuration-to-new-companies.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]