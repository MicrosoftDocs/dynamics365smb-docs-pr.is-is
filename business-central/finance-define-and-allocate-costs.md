---
title: Skilgreina og úthluta kostnaði
description: 'Kostnaðarúthlutun færir kostnað og tekjur milli kostnaðargerða, kostnaðarstaða og kostnaðhluta. Hægt er að tilgreina eins margar línur og þörf krefur.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1102, 1105, 1106, 1107, 1109, 1114'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="defining-and-allocating-costs"></a><a name="defining-and-allocating-costs"></a>Skilgreina og úthluta kostnaði

Kostnaðarúthlutun færir kostnað og tekjur milli kostnaðargerða, kostnaðarstaða og kostnaðhluta. Hægt er að tilgreina eins margar línur og þörf krefur. Hver úthlutun samanstendur af:  

- Úthlutunaruppruni.  
- Eitt eða fleiri úthlutunarmörk.  

Úthlutunaruppruninn kveður á um hvaða kostnaði verður að úthluta, og úthlutunarmörk skilgreina hvert kostnaðinum skuli úthlutað. Til dæmis getur úthlutunaruppruninn verið kostnaðurinn fyrir kostnaðartegundina Rafmagn og hiti. Öllum rafmagns- og hitakostnaði er úthlutað á þrjá kostnaðarstaði: Verkstæði, Framleiðslu og Sölu. Þessir kostnaðarstaðir eru það sem úthluta skal á.  

Fyrir hvern úthlutunaruppruna skilgreinir notandi úthlutunarstig, gildistímabil og afbrigði sem flokkunarkenni. Hægt er að nota keyrslu til að setja afmarkanir til að velja úthlutunarskilgreiningar og keyra síðan kostnaðarúthlutun . sjálfkrafa.  

Fyrir hvert úthlutunarmarki skilgreinir notandi úthlutunarstofninn. Úthlutunarstofn getur annað hvort verið fastur eða kvikur.  

- Fastir úthlutunargrunnar eru byggðir á tilteknu gildi, s.s. ferfetum eða skilgreindu úthlutunarhlutfalli, s.s. 5:2:4.  
- Kvik úthlutun fer eftir breytanlegum gildum, eins og fjölda starfsmanna í kostnaðarstöð eða sölutekjum kostnaðarliðar á tilteknu tímabili.  

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

## <a name="setting-up-allocation-source-and-targets"></a><a name="setting-up-allocation-source-and-targets"></a>Uppsetning uppruna og markhópa úthlutanna

Hver úthlutun samanstendur af úthlutunaruppruna og einu eða fleiri úthlutunarmörkum. Úthlutunaruppruninn skilgreinir hvaða kostnaði skal úthlutað. Úthlutunarmörkin ákvarða hvert kostnaði verður úthlutað.  

### <a name="to-set-up-cost-allocations"></a><a name="to-set-up-cost-allocations"></a>Til að setja upp kostnaðarúthlutanir

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Kostnaðarúthlutun** og veldu síðan tengda tengilinn.  
2. Á síðunni **Kostnaðarúthlutun** skal velja reitinn **Breyta**.  
3. Færið inn kenni fyrir úthlutunaruppsprettu í reitnum **Kenni**.  
4. Skilgreina stig sem tölu á bilinu 1 til 99 í reitnum **Stig**. Úthlutunarbókunin mun fylgja röð stiganna.  
5. Færa inn kostnaðartegund til að skilgreina hvaða kostnaðartegundum verður úthlutað í reitinn **Svið kostnaðartegundar**. Ef öllum kostnaði kostnaðartegundar hefur verið úthlutað er ekkert svið skilgreint.  
6. Færa inn kostnaðarstað ásamt kostnaði sem á að úthluta í reitinn **Kostnaðarstaðarkóði**.  
7. Færa inn kostnaðarhlut ásamt kostnaði sem á að úthluta í reitinn **Kostnaðarhlutakóði**. Reiturinn er oftast áfram auður vegna þess að kostnaðarhlutir eru sjaldnast úthlutaðir á aðra kostnaðarhluti.  
8. Færa inn kostnaðargerð í reitinn **Kreditfært í kostnaðartegund**. Kostnaður sem er úthlutað verður kreditfærður í upprunakostnaðartegund. Kreditbókunin verður bókuð á þá kostnaðartegund sem uppgefin er hér.  
9. Á flýtiflipanum **Línur** skal skilgreina úthlutunarmörk. Í fyrstu línunni skal færa inn kostnaðartegund í reitinn **Markkostnaðartegund**. Skilgreinir hvaða kostnaðartegund úthlutunin er skuldfærð á.  
10. Í fyrstu línunni skal færa inn fyrsta úthlutunar markið í reitinn **Markkostnaðarstaður** eða reitinn **Markkostnaðarhlutur** . Þessir tveir reitir skilgreina hvaða kostnaðarstað eða kostnaðarhlut úthlutunin er skuldfærð á. Aðeins er hægt að færa inn í gildi annars hvors þessara reita, en ekki bæði.  
11. Endurtaka skal sömu skref í annarri línu til að setja upp fleiri úthlutunarmörk.  
12. Þegar búið er að setja upp úthlutunarmarkmið og -uppruna, skal velja aðgerðina **Reikna úthlutunarlykil** til að reikna samtölu hlutdeildargilda.  

> [!NOTE]  
> Veljið gátreitinn **Útilokað** til að gera úthlutunaruppsetningu óvirka.

## <a name="setting-filters-for-dynamic-allocation-bases"></a><a name="setting-filters-for-dynamic-allocation-bases"></a>Uppsetning afmarkanir fyrir Kvik úthlutunargrunnar.

Kvika úthlutunaraðferðin byggist á breytanlegum gildum. Til dæmis fjöldi starfsmenn í kostnaðarstöð eða seldar vörur af kostnaðarhlut á tilteknu tímabili. Níu forskilgreindir úthlutunargrunnar og tólf kvik dagsetningarsvið eru í boði. Mismunandi afmarkanir eru settar á grundvelli úthlutunargrunns.  

### <a name="setting-filters"></a><a name="setting-filters"></a>Afmarkanir stilltar

Eftirfarandi tafla sýnir hvaða afmarkanir eru mögulegar fyrir mismunandi úthlutunargrunna og hvaða gildi eru leyfileg í reitunum **Nr. afmörkunar** og **Afmörkun hóps**. Veljið  <kbd>F1</kbd>  í  **reitnum Dagsetningarafmörkunarkóti**  til að lesa nákvæmar lýsingar.  

|**Grunnur**|**Númersafmörkun**|**Kóti gagnaafmörkunar**|**Afmörkun kostnaðarstaðar**|**Afmörkun kostnaðarhlutar**|**Afmörkun hópa**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Fjárhagsfærslur|Fjárhagsreikningur|Já|Já|Já|Á ekki við|  
|Fjárhagsáætl.færslur|Fjárhagsreikningur|Já|Já|Já|Heiti fjárhagsáætl.|  
|Kostnaðartegundarfærslur|Tegund kostnaðar|Já|Já|Já|Á ekki við|  
|Færslur kostnaðaráætlana|Tegund kostnaðar|Já|Já|Já|Heiti áætlunar|  
|Fjöldi starfsmanna|Á ekki við|Já|Já|Já|Á ekki við|  
|Seldar vörur (magn )|Vörunr.|Já|Já|Já|Birgðabókunarflokkur|  
|Keyptar vörur (magn)|Vörunr.|Já|Já|Já|Birgðabókunarflokkur|  
|Seldar vörur (upphæð )|Vörunr.|Já|Já|Já|Birgðabókunarflokkur|  
|Keyptar vörur (upphæð)|Vörunr.|Já|Já|Já|Birgðabókunarflokkur|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a><a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a>Sýnishorn 1: Skilgreining fastrar úthlutunar á grundvelli úthlutunarhlutfalls

Föst úthlutunaraðferð er byggð á tilteknu gildi, s.s. fermetrum í notkun eða skilgreindu úthlutunarhlutfalli, s.s. 5:2:4.  

Í þessu efnisatriði er lýst hvernig á að skilgreina þrjá nýja kostnaðarhluti úthlutunarmarks fyrir kostnaðarstað úthlutunarupprunans FRAML með fyrirliggjandi úthlutunarhlutfallinu 5:2:4. Kostnaðarhlutirnir þrír eru ACCESSO, PAINT og FITTINGS.  

> [!NOTE]  
> Í dæminu er notast við sýnigögnin í [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Til að skilgreina PROD kostnaðarstað úthlutunarveitu á flýtiflipanum Almennt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Kostnaðarúthlutun** og velja síðan viðkomandi tengil.  
2. Á síðunni **Kostnaðarúthlutun** skal velja aðgerðina **Nýtt**.  
3.  **Í reitinn Kenni**  skal velja  <kbd>Færa</kbd>  inn eða færa inn kenni.  
4. Í reitinn **Stig**, sláið inn **1**.  
5. Í reitnum **Gildir frá** og **Gildir til** eru viðeigandi dagsetningar færðar inn.  
6. Í reitinn **Kóði kostnaðarstaðar** er slegið inn **SALA**.  
7. Í **Kreditfært í kostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Til að skilgreina kostnaðarhluti úthlutunarmarks á flýtiflipanum Línur

1. Í fyrstu línunni í reitnum **Markkostnaðartegund** sláið inn **9903**.  
2. Í fyrstu línunni í reitnum **Markkostnaðarhlutur** veljið **ACCESSO**.  
3. Í fyrstu línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.  
4. Í fyrstu línunni í reitnum **Grunnur** veljið **Fast** til að nota fasta úthlutunaraðferð.  
5. Í fyrstu línuna í reitnum **Deila** setjið inn úthlutunarhlutfallið **5**.  
6. Í aðra línuna í reitnum **Markkostnaðartegund** sláið inn **9903**.  
7. Í annarri línunni, í reitnum **Markkostnaðarhlutur** er valið **MÁLNING**.  
8. Í annarri línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.  
9. Í annarri línunni, í reitnum **Grunnur**, er valið **Föst** til að nota fasta úthlutunaraðferð.  
10. Í annarri línunni, í reitnum **Deila**, er sett inn úthlutunarhlutfallið **2**.  
11. Í þriðju línuna í reitnum **Markkostnaðartegund** sláið inn **9903**.  
12. Í þriðju línunni í reitnum **Markkostnaðarhlutur**, er slegið inn **TENGIHLUTIR**.  
13. Í þriðju línunni í reitnum **„Gerð úthlutunarmarka** veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.  
14. Í þriðju línunni í reitnum **Grunnur**, er valið **Föst** til að nota fasta úthlutunaraðferð.  
15. Í þriðju línunni, í reitnum **Deila**, er sett inn úthlutunarhlutfallið **4**.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] reiknar sjálfkrafa reitinn **Prósenta** með því að nota prósentuhlutfall sem er háð öllum þremur úthlutunarhlutföllum sem færð eru inn í reitinn **Deila** í öllum þremur línunum.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a><a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a>Sýnishorn 2: Skilgreining kvikrar úthlutunar á grundvelli seldra vara

Þetta efnisatriði sýnir dæmi um hvernig á að skilgreina úthlutanir með því að nota kvika úthlutunaraðferð. Í dæminu er kvika úthlutun af kostnaði fyrir kostnaðarstað breytt til að styðja nýjan kostnaðarhlut IT EQUIPMENT. IT EQUIPMENT pakkar hafa vörunúmer frá 8904-W til 8924-W. Sölutölur fyrra árs eru notaðar til að reikna út hlutdeild. Úthlutunin er bókuð í aukakostnaðartegund 9903.  

> [!NOTE]  
> Í dæminu er notast við sýnigögnin í [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Til að skilgreina kvikar úthlutanir sem byggja á vörum sem seldar voru á síðasta ári

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Kostnaðarúthlutanir** og velja síðan viðkomandi tengil.  
2. Á síðunni **Kostnaðarúthlutun** skal velja aðgerðina **Nýtt**.  
3.  **Í reitinn Kenni**  skal velja  <kbd>Færa</kbd>  inn eða færa inn kenni.  
4. Í reitinn **Stig**, sláið inn **1**.  
5. Í reitnum **Gildir frá** og **Gildir til** eru viðeigandi dagsetningar færðar inn.  
6. Í reitinn **Kóði kostnaðarstaðar** er slegið inn **SALA**.  
7. Í **Kreditfært í kostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.  
8. Í **Markkostnaðartegund** reitinn er slegin inn kostnaðargerðin **9903**.  
9. Í reitnum **Markkostnaðarhlutur** veljið **Nýtt** til að stofna nýja kostnaðarhlutinn IT EQUIPMENT og fyllt er í reitina eftir þörfum. Veljið **IT EQUIPMENT**. Reiturinn **Markkostnaðarstaður** er hafður auður.  
10. Í reitnum **Gerð úthlutunarmarka**, veljið **Allur kostnaður** til að tilgreina hvernig öllum uppsöfnuðum kostnaði er úthlutað.  
11. Í reitnum **Grunnur** veljið úthlutunarstofninn **Seldar vörur (upphæð)**.  
12. Í retinn **Númersafmörkun** er fært inn **8904-W..8924-W**.  
13. Í reitinn **Kóði gagnaafmörkunar** er fært inn **Síðasta ár**.  
14. Veljið **Reikna úthlutunarlykil** aðgerðina til að reikna út hlutinn.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] notar sölutölur fyrri ára til að reikna hlut 1596.50 SGM með 100 prósentum fyrir pakka IT EQUIPMENT. Þetta merkir að öllum seldum vörum síðasta árs verður úthlutað á kostnaðarhlutinn IT EQUIPMENT.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/allocate-costs-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

 [Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)  
 [Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md)  
 [Kostnaðarreikningur](finance-manage-cost-accounting.md)  
 [Orðalisti í kostnaðarbókhaldi](finance-terminology-in-cost-accounting.md)  
 [Um kostnaðarbókhald](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
