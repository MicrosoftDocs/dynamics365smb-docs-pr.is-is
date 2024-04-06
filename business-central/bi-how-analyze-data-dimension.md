---
title: Greina gögn eftir víddum
description: Þessi grein lýsir því hvernig hægt er að greina viðskiptagögn eftir víddum til að fá betri innsýn í reksturinn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="analyze-data-by-dimensions"></a>Greining gagna eftir víddum

Í fjárhagsgreiningu er vídd bætt við færslu sem nokkurs konar merki til að flokka færslur með svipaða eiginleika. Til dæmis flokka víddir oft færslur fyrir viðskiptamenn, svæði, vörur og sölumenn. Með hópunum er auðvelt að sækja gögn um þau til greiningar. Hægt er að nota víddir í færslum í færslubókum, fylgiskjölum og áætlunum.

Hver vídd lýsir áherslu greiningar. Tvívíð greining gæti því til dæmis verið sala eftir svæðum. Með því að nota fleiri en tvær víddir þegar færsla er stofnuð er hægt að framkvæma flóknari greiningar. Dæmi um flókna greiningu er að kanna sölu á hverja söluherferð fyrir hvern viðskiptamannaflokk á hvert svæði. Það veitir meiri innsýn í reksturinn, svo sem hversu vel fyrirtækið þitt starfar, hvar það er eða ekki þrífst ekki og hvar þú ættir að ráðstafa meiri fjármunum. Innsýnin hjálpar þér að taka upplýstar viðskiptaákvarðanir. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

> [!TIP]
> Hægt er að greina færslugögn út frá víddum á skjótan hátt með því að afmarka samtölur á bókhaldslyklum (COA) og færslum á öllum **Færslur** síður út frá víddum. Leitaðu að aðgerðinni **Stilla víddarafmörkun**.

> [!NOTE]
> Ef í uppgötvast að rangt víddargildi var notað í bókuðum fjárhagsfærslum er hægt að leiðrétta það og uppfæra greiningaryfirlitin. Til að [fræðast meira er farið í Úrræðaleit og Leiðrétting vídda](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view"></a>Setja upp greiningaryfirlit

Greining eftir víddum notar valda samsetningu af víddum. Þú geymir, sækir og uppfærir þessa vídd með því að búa til **Greiningaryfirlitsspjald**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiningaryfirlit**, velja síðan viðkomandi tengil.  
2. Á síðunni **Listi yfir greiningaryfirlit** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að bæta öðrum víddarkóðum við þá fjóra sem fyrir eru á flýtiflipanum **Víddir** er aðgerðin **Afmörkun** valin, reitirnir fylltir út og síðan er smellt á **Í lagi** hnappinn.  
5. Til að uppfæra yfirlitið er valin aðgerðin **Uppfæra**.

## <a name="analyze-by-dimensions"></a>Greina eftir víddum

Notaðu greiningaryfirlit sem þegar hafa verið sett upp með fylkinu **Greining eftir víddum** til að skoða upphæðirnar í fjárhagnum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiningaryfirlit**, velja síðan viðkomandi tengil.  
2. Velja skal viðeigandi greiningaryfirlit og velja síðan aðgerðina **Greining eftir víddum**.
3. Á síðunni **Greining eftir víddum** skal fylla út reitina til að skilgreina hvaða gögn á að sýna og hvernig.
4. Veljið aðgerðina **Sýna fylki** til að opna fylkissíðuna fyrir greiningaryfirlitið.
5. Til að fá aðgang að upplýsingum um upphæð á fylkissíðunni er upphæðin valin.  

- Í dálkunum vinstra megin eru upplýsingar byggðar á því sem valið er í reitnum **Sýna sem línur** í hausnum.  
- Í dálkunum til hægri eru upplýsingar byggðar á því sem valið er í reitnum **Sýna sem dálka** í hausnum.

> [!IMPORTANT]  
> Ekki er hægt að velja lengd tímabils sem er styttra en tímabilið sem tilgreint er fyrir dagsetningarþjöppunina á spjaldinu **Greiningaryfirlit** . Aðgerðirnar **Næsta safn** og **Fyrra safn** eru ekki tiltækar ef tímabil **hefur verið valið** annaðhvort í reitunum **Sýna sem línur** eða **Sýna sem dálka** .  

> [!NOTE]  
> Hægt er að nota skýrsluna **Víddir - Sundurliðun** til að sýna ítarlega flokkun á notkun vídda í færslum á tilteknu tímabili. Hægt er að nota skýrsluna **Víddir - Heild** til að sýna aðeins heildarupphæðirnar.  

> [!TIP]  
> Einnig er hægt að breyta útlitinu með því að breyta innihaldi reitanna **Sýna sem línur** og **Sýna sem dálka** . Til að snúa við yfirlitsstillingu, skal velja aðgerðina **Snúa við línum og dálkum**.

## <a name="update-an-analysis-view"></a>Uppfæra greiningaryfirlit

Upphæðirnar á síðunni **Greining eftir víddum** gefa mynd af stöðu fyrirtækisins við síðustu uppfærslu. Til að fá núverandi stöðu er uppfærsluaðgerðin keyrð til að uppfæra greiningaryfirlitið.

Notaðu eftirfarandi aðferð til að uppfæra greiningaryfirlit af síðunni **Greining eftir víddum**. Skrefin eru svipuð þeim sem notuð eru við að uppfæra síðurnar **Spjald greiningaryfirlits** og **Listi greiningaryfirlits**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiningaryfirlit**, velja síðan viðkomandi tengil.
2. Velja skal viðeigandi greiningaryfirlit og velja síðan aðgerðina **Greining eftir víddum**.
3. Á síðunni **Greining eftir víddum** skal velja reitinn **Kóði greiningaryfirlits**.  
4. Línan með viðeigandi greiningaryfirliti er valin.  
5. Á síðunni **Greiningaryfirlit** skal velja greiningaryfirlitið, síðan velja aðgerðina **Uppfæra**.  

> [!TIP]  
> Ef gátreiturinn **Uppfæra við bókun er** valinn á greiningaryfirlitsspjaldi uppfærist yfirlitið sjálfkrafa þegar einhver bókar tengda færslu.

> [!NOTE]  
> Sum eða öll greiningaryfirlit eru uppfærð samtímis með því að nota keyrsluna **Uppfæra greiningaryfirlit** .  

## <a name="see-also"></a>Sjá einnig .

[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með víddir](finance-dimensions.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
