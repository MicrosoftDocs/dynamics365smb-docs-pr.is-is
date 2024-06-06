---
title: Setja upp upplýsingar um almennar eignir (eignir)
description: 'Áður en þú getur byrjað að stjórna eignum, verður þú að setja upp sjálfgefna fjárhagsreikninga, bókunarflokka, úthlutunarlykla, færslubókasniðmát og keyrslur, og flokkskóða.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-general-fixed-assets-information"></a>Setja upp upplýsingar um almennar eignir

Áður en hægt er að stjórna eignum (eign) verður að setja upp sjálfgefna fjárhagsreikninga, úthlutunarlykla og bókarsniðmát og keyrslur til að bóka og endurflokka eignir. Einnig þarf að skilgreina flokkunarstigveldi (flokka og undirflokka) til að skipuleggja eignirnar og skilgreina staðsetningarnar þar sem eignir eru geymdar ef með þarf.

## <a name="to-set-up-general-behavior-for-fixed-assets-functionality"></a>Til að setja upp almenna virkni eigna

Skilgreina almenna hegðun eignaaðgerðarinnar og númeraröð fylgiskjala á síðunni **Eignagrunnur** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning eigna** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Setja upp bókunarflokka eigna

Bókunarflokkar eru notaðir til þess að skilgreina flokka eigna. Færslur fyrir þessa bókunarflokka bóka á sömu fjárhagsreikninga.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignabókunarflokkar** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.
3. Á síðunni **eignabókunarflokkaspjald** þarf að fylla reitina út eftir þörfum.

    > [!NOTE]  
    >   Til að ganga úr skugga um að mótreikningar fyrir mismunandi eignabókanir eru sjálfkrafa settir inn þegar þú velur **Setja inn mótreikning eigna** aðgerð í færslubókarlínum, fylgja skal næsta skref, í samræmi við uppfærslubókun.
4. Á flýtiflipi **Mótreikningur** í reitnum **mótreikningur uppfærslu** er valinn fjárhagsreikningurinn sem þú vilt bóka mótfærslur í fyrir uppfærslu.

Nánari upplýsingar um aðgerðina **Setja inn mótreikn** . eigna í eignafjárhagsbókarlínum [eru í Endurmeta eignir](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-journal-templates"></a>Setja upp sniðmát eignabóka

Sniðmát er fyrirfram skilgreind uppsetning á færslubók. Í sniðmáti eru upplýsingar um ferilskóta, skýrslur og númeraraðir. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] stofnar sjálfkrafa eignabókarsniðmát í fyrsta skipti sem síðan Eignabók **er opnuð**, en hægt er að setja upp önnur bókarsniðmát.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát eignabókar** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

## <a name="to-set-up-fixed-asset-class-and-subclass-codes"></a>Uppsetning eignaflokka og undirflokkskóta

Í eignum er hægt að skilgreina flokkunarstigveldi sem hægt er að nota til að flokka eignir. Stigveldið hefur tvö stig: flokka og undirflokka.

### <a name="fixed-asset-class-codes"></a>Eignaflokkskóðar

Eignaflokkar eru efsta stigs færslur í flokkunarstigveldinu sem eignir eru flokkaðar í. Til dæmis má nota flokka til að skipta eignum í áþreifanlegar eða óáþreifanlegar eignir. Stofna verður að minnsta kosti einn eignaflokk í uppsetningunni.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignaflokkar** og velja síðan viðkomandi tengil.
2. Færðir eru inn kótar og heiti á eignaflokkunum sem á að stofna.

### <a name="fixed-asset-subclass-codes"></a>Undirflokkskótar eigna

Eignaundirflokkar eru á öðru stigs færslum í flokkunarstigveldinu sem eignir eru flokkaðar í. Hver undirflokkur vísar á efsta stigs flokk. Nota eignaundirflokkskóta til að flokka eignir í nákvæmari flokkum, svo sem byggingar, ökutæki, húsbúnað eða vélbúnað. Stofna verður að minnsta kosti einn eignaundirflokk í uppsetningunni.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignaundirflokkar** og velja síðan viðkomandi tengil.
2. Færðir eru inn kótar og heiti á eignaundirflokknum sem á að stofna.

## <a name="start-to-register-assets"></a>Byrjað er að skrá eignir

Ef eignirnar eru notaðar í [!INCLUDE[prod_short](includes/prod_short.md)] fyrsta skipti verður að setja upp kerfishlutann Fjárhagur áður en eignir eru settar upp. Hvernig það er gert fer eftir því hvort eignir eru samþættar við fjárhag.  

Eftirfarandi aðferð er notuð ef bóka á eignafærslur í fjárhag.  

1. Ljúka grunnuppsetningum eigna.  
2. Fyllt er út eignaspjald fyrir hverja eign sem til er.  
3. Stofna eigna-/afskriftabók fyrir hvern afskriftartilgang (til dæmis fyrir skattinn og fjárhagsskýrslur). Skilmálar og skilyrði eru skilgreind fyrir hverja afskriftabók, svo sem samþætting við fjárhag.

    Virkja fjárhagssamþættingu með því að fylgja næstu skrefum. Í fyrsta lagi skal tryggja að fjárhagsheildun sé ekki virk fyrir allar afskriftabækur, bóka síðan opnunarfærslurnar og að lokum skal kveikja á fjárhagsheildun.  
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afskriftabækur** og velja síðan viðkomandi tengil.  
5. Veldu viðeigandi afskriftabók og síðan aðgerðina **Breyta** til að opna síðuna **Afskriftabókarspjald**.
6. Á flýtiflipanum **Samþætting** skal slökkva á öllum vífærunum. Ef um er að ræða fleiri en eina afskriftabók er þetta skref endurtekið fyrir hverja þeirra.  
7. Í eignabókinni eru færðar eftirfarandi línur fyrir hverja eign:
   * Færð er inn lína með stofnkostnaðinum.
   * Lína með uppsafnaðar afskriftir til loka fyrra fjárhagsárs.
   * Lína með uppsafnaðar afskriftir frá upphafi yfirstandandi reikningsárs til dagsetningarinnar sem [!INCLUDE[prod_short](includes/prod_short.md)] er stillt á og setur af stað útreikning á afskriftunum.

    Ef aðrar mótfærslur eru opnar eru einnig hægt að færa þær inn núna, til dæmis niðurfærsla og uppfærsla.  
8. Þegar færslubókarlínur fyrir hverja eign hafa verið færðar inn og bókaðar er kveikt á fjárhagsheildun í afskriftabókunum.

Ef eignirnar eru ekki samþættar fjárhag er þrepum 6 og átta sleppt.

## <a name="to-set-up-fixed-asset-location-codes-optional"></a>Uppsetning staðsetningarkóta eigna (valfrjálst)

Staðsetningarkótar eigna skilgreina kenni þar sem hægt er að setja eignir eins og söludeild, móttöku, stjórnunardeild, framleiðsludeild eða vöruhús. Hægt er að nota þær til að skrá staðsetningu eignar. Þessar upplýsingar koma að gagni við vátryggingar og birgðir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetning eigna** og velja síðan viðkomandi tengil.
2. Færðir eru inn kóðar og heiti á staðsetningum eigna sem búa á til.

## <a name="to-set-up-fixed-asset-allocation-keys-optional"></a>Uppsetning eignaúthlutunarlykla (valfrjálst)

Nota úthlutunarlykla til að úthluta færslum á ýmsar deildir eða verkefni. Til dæmis er hægt að setja upp úthlutunarlykil til að úthluta afskriftum ökutækja með 35 prósentum á stjórnunardeildina og 65 prósent á söludeildina. Frekari upplýsingar eru í [Úthluta kostnaði og tekjum](year-allocate-costs-income.md).

Úthlutunarlyklar gilda um eignaflokka en ekki um stakar eignir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignabókunarflokkar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Eignabókunarflokkar** skal velja aðgerðina **Úthlutanir** og velja síðan bókunarflokk.
3. Á síðunni **eignaúthlutanir** þarf að fylla reitina út eftir þörfum.
4. Endurtaktu skref 2 og 3 fyrir hverja bókunargerð sem ætlunin er að skilgreina úthlutunarlykla fyrir.

## <a name="to-set-up-fixed-asset-journal-batches-optional"></a>Uppsetning eignabókarkeyrslna (valfrjálst)

Hægt er að setja upp margar bókarkeyrslur sem eru sérstakar færslubækur fyrir hvert færslubókarsniðmát. Starfsmenn geta til dæmis verið með eigin bókarkeyrslur sem nota upphafsstafi starfsmannsins sem heiti bókarkeyrslu. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát eignabókar** og velja síðan viðkomandi tengil.  
2. Valin er viðeigandi sniðmát færslubókar og veldu svo **keyrslur** aðgerðina.
3. Á síðunni **eignabókarkeyrslur** þarf að fylla reitina út eftir þörfum.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates-optional"></a>Uppsetning sniðmáta fyrir endurflokkunarbók eigna (valfrjálst)

Nota sérstakar endurflokkunarbækur til að flytja, skipta eða sameina eignir. [!INCLUDE[prod_short](includes/prod_short.md)] stofnar sjálfkrafa eignaendurflokkunarbókarsniðmát í fyrsta skipti sem glugginn Eignaendurflokkunarbók er opnaður **. Færslubókarsíða**, en hægt er að setja upp önnur sniðmát endurflokkunarbóka. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát færslubókar fyrir eignaendurflokkun** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches-optional"></a>Uppsetning eignaendurflokkunarbókarkeyrslna (valfrjálst)

Hægt er að setja upp margar bókarkeyrslur sem eru sérstakar færslubækur fyrir hvert sniðmát endurflokkunarbókar. Starfsmenn geta til dæmis verið með eigin endurflokkunarbókarkeyrslur sem nota upphafsstafi starfsmannsins sem heiti bókarkeyrslu. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát færslubókar fyrir eignaendurflokkun** og velja síðan viðkomandi tengil.  
2. Valin er viðeigandi sniðmát færslubókar og veldu svo **keyrslur** aðgerðina.
3. Á síðunni **keyrslur eignaendurflokkunarbókar** þarf að fylla reitina út eftir þörfum.

## <a name="see-also"></a>Sjá einnig .

[Uppsetning eigna](fa-setup.md)  
[Yfirlit yfir eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
