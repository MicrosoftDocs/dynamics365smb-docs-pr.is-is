---
title: Stofna nýtt fyrirtæki með Skilgreiningarpakka
description: Notaðu RapidStart Services töflur og síður til að stofna nýtt fyrirtæki þar sem framkvæma skal innleiðingu viðskiptamanns.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 2d75c136fdd0dcf2891468d722008ab0bf183cbb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512413"
---
# <a name="create-a-new-company-based-on-configuration-packages"></a>Stofna nýtt fyrirtæki samkvæmt Skilgreiningarpakka

Til að nota RapidStart Services fyrir [!INCLUDE[prod_short](includes/prod_short.md)] skal fyrst stofna nýtt fyrirtæki þar sem framkvæma skal innleiðingu viðskiptamanns. Þegar nýtt fyrirtæki er stofnað eru staðlaðar [!INCLUDE[prod_short](includes/prod_short.md)] töflur og síður búnar til, en engin gögn eru í þeim.

Auk þess er hægt að beita sérstökum uppsetningargögnum fyrir fyrirtækið eftir frumstillingu. Upplýsingarnar koma úr grunnstillingapakka, sem er .rapidstart skrá, sem afhendir innihald á samþjöppuðu formi.  

Grunnstillingarpakkar dæma, þ.á.m. skrár sem miðast við land/svæði eru innifaldar í CRONUS sýnifyrirtækinu. Notið eftirfarandi aðgerð til að nota pakkann með dæmastillingunum með nýju fyrirtæki.  

## <a name="to-use-the-sample-configuration-packages"></a>Til að nota sýnishorn af skilgreiningarpökkum

1. CRONUS Opna sýnifyrirtækið. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Grunnstillingarpakka** og velja síðan viðkomandi tengil.  
3. Viðeigandi pakki er valinn af listanum og síðan er **aðgerðin útflutningur pakkans** valin.  

Notið eftirfarandi ferli til að stofna nýtt fyrirtæki og nota skilgreiningarpakkann sem hluta af ferlinu.  

## <a name="to-create-a-new-company"></a>Til að búa til nýtt fyrirtæki

1. Búa til nýtt fyrirtæki. Nánari upplýsingar eru í [Stofna ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Grunnstillingarpakka** og velja síðan viðkomandi tengil.  
3. **Veldu aðgerðina Flytja inn pakka** og tilgreindu svo. RapidStart-skrána sem á að flytja inn.  

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