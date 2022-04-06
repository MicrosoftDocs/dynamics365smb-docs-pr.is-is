---
title: Nota sjálfvirkt gagnatökukerfi (ADCS)
description: Hægt er að nota sjálfvirka gagnatökukerfið (ADCS) til að skrá alla hreyfingu á vörum í vöruhúsinu og skrá sumar færslubókaraðgerðir.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.search.form: 7700, 7703, 7704, 7706, 7707, 7710, 9813, 9814
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: cf0ac9f90efe234b73d4509e50502ca37dcf458e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514700"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Nota sjálfvirkt gagnatökukerfi (ADCS)

> [!NOTE]
> Sjálfvirkt gagnatökukerfi (ADCS) býður upp á leið fyrir [!INCLUDE[prod_short](includes/prod_short.md)] til að eiga samskipti við handtæki í gegnum vefþjónustu. Vinna þarf með Microsoft-samstarfsaðila sem geta gefið tengilinn á milli vefþjónustu og tiltekins handtækis. 

Hægt er að nota sjálfvirka gagnatökukerfið (ADCS) til að skrá alla hreyfingu á vörum í vöruhúsinu og skrá sumar færslubókaraðgerðir, s.s. leiðréttingar á magni í birgðabók vöruhússins og raunbirgðir. ADCS felur venjulega í sér skönnun á strikamerki.

Ef nota á ADCS þarf að gefa öllum vörum í vöruhúsinu vörukenni. Einnig þarf að setja upp smáglugga, handtölvuaðgerðir, gagnaskipti og tilgreina stillingar fyrir svæði sem stýra ADCS Notandinn tilgreinir hvort eigi að nota í ADCS spjaldi birgðageymslunnar vöruhúsi.

Magn upplýsinga sem birtar eru í handtölvunni er skilgreint í smágluggauppsetningu hverrar einstakrar handtölvu í samræmi við þarfir vöruhússins. Eftirfarandi eru dæmi um upplýsingar sem hægt er að birta:  

- Gögn úr töflum innan [!INCLUDE[prod_short](includes/prod_short.md)], til dæmis lista yfir tínsluskjöl sem notandinn valið úr.  
- Textaupplýsingar.  
- Skilaboð til að sýna staðfestingar eða villurnar um verkþætti sem framkvæmdir eru og skráðir af handtölvu notanda.

## <a name="to-enable-web-services-for-adcs"></a>Til að virkja vefþjónustu fyrir ADCS
Tila ð nota sjálfvirkt gagnatökukerfi þarf að virkja ADCS-vefþjónustu.  

## <a name="to-enable-and-publish-the-adcs-web-service"></a>Til að virkja og birta ADCS-vefþjónustuna  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Netþjónusta** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.  
3. Á síðunni **Vefþjónustur** skal færa inn eftirfarandi upplýsingar í nýrri línu:  

    |Svæði|Gildi:|  
    |---------------------------------|-----------|  
    |**Gerð hlutar**|Codeunit|  
    |**Kenni hlutar**|7714|  
    |**Heiti þjónustu**|ADCS **mikilvægt:** þess er krafist að **ADCS** þjónustunni sé gefið heiti.|  

5. Veljið gátreitinn **Útgefið**.  
6. Velja hnappinn **Í lagi**.  

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>að setja vöruhús upp fyrir notkun ADCS  
Ef nota á ADCS verður að tilgreina hvaða birgðageymslur nota tæknina.  

> [!NOTE]  
>  Mælt er með að vöruhús séu ekki sett upp til að nota ADCS ef vöruhúsið hefur einnig hólfagetureglu.

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja viðkomandi tengil.
2.  Veljið vöruhús af listanum sem á að gera ADCS virkt fyrir og veljið svo aðgerðina **Breyta**.
3. Á síðunni **birgðageymsluspjald** veljið **Nota ADCS** gátreitur.  

## <a name="to-specify-an-item-to-use-adcs"></a>Tilgreina vöru til að nota ADCS  
Hver vara í vöruhúsi sem nota á með ADCS verður að fá úthlutaðan auðkenningarkótanum til að tengja skjalið ásamt vörunúmerinu. Til dæmis er hægt að nota strikamerki vörunnar sem auðkenniskóta. Vara getur einnig haft margar auðkenniskóta. Þetta getur komið að gagni í tilfellum þar sem vara er tiltæki í ýmsum mælieiningu, s.s. stykkjum og brettum. Í þessu tilfelli er úthlutað auðkenniskóta fyrir hvern.    

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2.  Veljið vöru af listanum sem er hluti af ADCS-lausninni, og síðan aðgerðina **Breyta**.
3. Á síðunni **Birgðaspjald** skal velja aðgerðina **Kennimerki**.
4. Á síðunni **Vörur Kennimerki** skal velja aðgerðina **Nýtt**.
5. Í reitnum **Kóði** skal tilgreina auðkenni vörunnar. Til dæmis gæti kennið verið strikamerkisnúmer vörunnar.  

    Einnig er hægt að færa inn **Afbrigðiskóti** og **Mælieiningu**.  

6. Ef þörf krefur skal færa inn marga kóta fyrir hverja vöru.
7. Velja hnappinn **Í lagi**.  
8.  Til að fara yfir upplýsingarnar skal velja reitinn **Kennimerkiskóði** til að opna síðuna **Vörukennimerki**.

## <a name="to-add-an-adcs-user"></a>Til að bæta við ADCS notanda  
Hægt er að bæta hvaða notanda við sem notanda sjálfvirks gagnatökukerfis (ADCS). Þegar það er gert verður notandinn einnig að gefa upp aðgangsorð. Einnig er hægt að bjóða upp á tengingu sem auðkennir ADCS-notandann sem starfsmann vöruhúss. Aðgangsorð notanda ADCS getur verið frábrugðið Windows-aðgangsorði notandans. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **ADCS-notendur** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3.  Á svæðinu **Heiti** skal færa inn heiti fyrir notandann. Heitið getur ekki innihaldið meira en 20 stafi, með bilum.  
4.  Í reitnum **Lykilorð** er lykilorð fært inn. Aðgangsorðið er falið.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Til að tilgreina að starfsmaður vöruhúss sé ADCS notandi  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2.  Ef þörf krefur skal bæta við nýjum starfsmanni vöruhúss. Frekari upplýsingar eru í [Setja upp vöruhússtarfsmenn](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Veldu aðgerðina **Breyta lista**.  
4.  Veljið vöruhúsastarfsmann af listanum. Í reitnum **ADCS notandi** er valið felliörina og veljið svo nafnið á ADCS-notanda af listanum.  

> [!NOTE]  
>  Sjálfgefið vöruhús fyrir starfsmanninn ætti að nota ADCS.

## <a name="to-create-and-customize-miniforms"></a>Hvernig á að búa til og sérsníða smáglugga
Smágluggar eru notaðir til að gefa lýsa upplýsingum sem birtar eru á lófatækjum. Til dæmis er hægt að stofna smáglugga til að styðja vöruhúsaaðgerðina að tína vörur. Þegar búið er að stofna smáglugga er hægt að bæta við hann virkni fyrir algengar aðgerðir sem notandinn gerir með handtölvum, eins og flutningur upp eða niður línu.  

> [!NOTE] 
> Til að innleiða eða breyta virkni smágluggaaðgerðar þarf að búa til nýja kóðaeiningu fyrir reitinn **Afgreiðslukóðasafn** til að framkvæma aðgerðina eða svarið. Hægt er að fá frekari upplýsingar um ADCS-virkni með því að skoða kóðaeiningar, svo sem 7705, 7706, 7712 og 7713.  

### <a name="to-create-a-miniform-for-adcs"></a>Til að búa til smáglugga fyrir ADCS  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Smágluggar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3.  Í reitnum **Kóði** er færður inn kóði fyrir smáglugganum. Einnig er hægt að færa gildi inni í alla aðra reiti.  

    Velja skal gátreitinn **Ræsa smáglugga** til að gefa til kynna að smáglugginn sé fyrsta skjámyndin sem notandinn sér við innskráningu.  

4.  Á flýtiflipanum **Línur** skilgreinið svæðin sem birtast á smáglugganum. Röðin sem þú færir inn línur er sú röð sem línurnar birtast í handtölvunni.  

Þegar búið er að búa til smáglugga, eru næstu skref er að stofna aðgerðir og tengja virkni fyrir ýmsan lyklaborðsinnslátt.  

### <a name="to-customize-miniform-functions"></a>Til að sérsníða aðgerðir smáglugga  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Smágluggar** og velja síðan viðkomandi tengil.  
2.  Veljið smáglugga af listanum og veljið svo aðgerðina **Breyta**.  
3.  Velja aðgerðina **Aðgerðir**.  
4.  Í fellilistanum **Aðgerðakóði** skal velja kóða fyrir aðgerð sem á að tengja við smáglugga. Til dæmis er hægt að velja ESC, sem tengir aðgerðir við það að stutt er á ESC-lykilinn.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]