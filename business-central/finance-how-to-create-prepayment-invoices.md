---
title: Stofna fyrirframgreiðslureikninga
description: Takist á við aðstæður þar sem þú eða lánardrottinn þinn krefjast fyrirframgreiðslu. Notið sjálfgefnar prósentur fyrir hverja sölu- og innkaupalínu eða leiðréttið upphæðina eins og með þarf.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 07/23/2024
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
ms.service: dynamics-365-business-central
---
# <a name="create-prepayment-invoices"></a>Stofna fyrirframgreiðslureikninga

Ef þú þarf að fá viðskiptamenn til að greiða fyrir sendingu pöntunar geturðu notað eiginleika fyrirframgreiðslu. Sama gildir ef lánardrottinn þinn krefst þess að þú greiðir áður en hann sendir pöntun til þín.  

Hægt er að hefja fyrirframgreiðsluferlið þegar búið er að stofna sölu- eða innkaupapöntun. Sjálfgefna fyrirframgreiðsluprósentan fyrir vöru í pöntuninni eða fyrir viðskiptamanninn eða lánardrottininn er tekin með í fyrirframgreiðslureikningnum. Einnig er hægt að tilgreina fyrirframgreiðsluprósentuna fyrir allt skjalið.

Þegar búið er að stofna sölu- eða innkaupapöntun er hægt að stofna fyrirframgreiðslureikning fyrir hana. Notið sjálfgefnar prósentur fyrir hverja sölu- og innkaupalínu eða leiðréttið upphæðina. Til dæmis er hægt að tilgreina heildarupphæð fyrir alla pöntunina.  

Eftirfarandi ferli sýnir hvernig skal gefa út fyrirframgreiðslureikning fyrir sölupöntun. Skrefin eru svipuð fyrir innkaupapöntun.  

## <a name="to-create-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofna nýja sölupöntun fyrir viðeigandi viðskiptavin. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  

    Á flýtiflipanum **Fyrirframgreiðsla** tilgreinir svæðið **Fyrirframgreiðsla %** prósentuna sem á að nota til að reikna út fyrirframgreiðsluupphæðina. Ef sjálfgefin fyrirframgreiðsluprósenta er á spjaldi viðskiptavinar er svæðið sjálfkrafa fylltur út. Hægt er að breyta prósentunni. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Veldu svæðið **Þjappa fyrirframgreiðslu** ef óskað er eftir að stofna línur á fyrirframgreiðslureikningnum sem sameinar línur úr sölupöntuninni ef:  

    - Þær eru með sama fjárhagsreikninginn fyrir fyrirframgreiðslur samkvæmt stillingum í almenna bókunargrunninum.  
    - Þeir hafa sömu víddir.  

    Ekki velja svæðið **Þjappa fyrirframgreiðslu** ef þú vilt tilgreina fyrirframgreiðslureikning með einni línu fyrir hverja sölupöntunarlínu sem hefur fyrirframgreiðsluprósentu.  

    Gjalddagi fyrirframgreiðslunnar er sjálfkrafa reiknaður út frá gildinu í reitnum **Greiðsluskilmálakóði fyrirframgr.**.

    > [!NOTE]
    > Þegar sumar línur á reikningi þurfa 100% fyrirframgreiðslu og aðrar línur ekki og VSK er á fyrirframgreiðslureikningnum gæti sléttuðu upphæðin valdið villu þegar fyrirframgreiðslureikningur er stofnaður. Villan kemur upp vegna þess að upphæð fyrirframgreiðslureikningsins er hærri en upphæðirnar í fylgiskjalslínunum. Til að laga vandann skal breyta upphæðunum í einni eða öllum línunum sem krefjast 100% fyrirframgreiðslu. Breytingin endurreiknar VSK-upphæðina sléttun og notar uppsafnaða sléttunarmismunur í síðustu breyttu línu.
    >
    > Tvær leiðir til að laga vandamálið eru:
    >
    > * Stofna sérstakan VSK-vörubókunarflokk og VSK-bókunargrunn með sérstöku VSK-kenni og nota það fyrir vörur eða línur sem krefjast 100% fyrirframgreiðslu. Sléttun er gert fyrir hvert VSK-kenni svo að sérstakar sléttun eru gerðar fyrir vörur sem úthlutað er á VSK-vörubókunarflokkinn.
    > * Nota skal sérstakan reikning fyrir vörurnar eða línurnar sem þarfnast ekki 100% fyrirframgreiðslu.

3. Sölulínurnar eru fylltar út.  

    Ef þú hefur tilgreint sjálfgefna fyrirframgreiðsluprósentuna annað hvort fyrir viðskiptavininn eða á flýtiflipanum **Fyrirframgreiðsla** í þessu skjali, er þetta gildi afritað í hverja línu. Hægt er að breyta innihaldi reitsins **Fyrirframgreiðsla %** í línunni.  

    > [!TIP]
    > Ef þú sérð ekki reitinn **Fyrirframgreiðsla %** geturðu bætt honum við í gegnum sérstillingu.  Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

4. Veldu **Upplýsingar** aðgerðina til að skoða heildarupphæð fyrirframgreiðslu.

    Ef leiðrétta á heildarupphæð fyrirframgreiðslunnar fyrir pöntunina er hægt að breyta innihaldi reitsins **Upphæð fyrirframgreiðslu** á síðunni **Tölfræði sölupöntunar**.  

    Ef reiturinn **Verð ásamt VSK** er valinn er hægt að breyta reitnum **Upphæð fyrirframgreiðslu með VSK**.  

    Ef þú breytir innihaldi reitsins **Fyrirframgreiðsluupphæð**, mun upphæðinni verða dreift hlutfallslega á milli allra lína, nema þeirra sem hafa **0** í reitnum **Fyrirframgreiðsla %**.  

5. Til að prenta prufuskýrslu áður en fyrirframgreiðslureikningurinn er bókaður skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Prufuskýrsla fyrirframgreiðslu**.  
6. Til að bóka fyrirframgreiðslureikningurinn skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Bóka fyrirframgreiðslureikning**.  

    Fyrirframgreiðslureikningur er bókaður og prentaður með því að velja aðgerðina **Bóka og prenta fyrirframgr.reikning**.  

Hægt er að gefa út aðra fyrirframgreiðslureikninga fyrir pöntunina. Til að gefa út annan reikning skaltu hækka upphæð fyrirframgreiðslunnar í einni eða fleiri línum, leiðrétta dagsetningu skjalsins ef þess þarf og bóka fyrirframgreiðslureikninginn. Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðarinnar.  

> [!NOTE]  
> Ef þú ert í Norður Ameríku, geturðu ekki breytt fyrirframgreiðsluprósentunni eftir að fyrirframgreiðslureikningurinn hefur verið bókaður. Í N-amerísku útgáfu [!INCLUDE[prod_short](includes/prod_short.md)] er komið í veg fyrir þetta, því útreikningur söluskatts yrði annars rangur.  

 Þegar hægt er að bóka restina af reikningnum er hann bókaður eins og hver annar reikningur og fyrirframgreiðsluupphæðin er sjálfvirkt dregin frá þeirri upphæð sem greiða á.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Uppfæra stöðu fyrirframgreiddra pantana og reikninga sjálfkrafa

Þú getur flýtt fyrir pöntunar- og reikningsvinnslu með því að setja upp verkraðarfærslur sem uppfæra stöðu þessara skjala sjálfkrafa. Þegar fyrirframgreiðslureikningur er greiddur geta verkraðarfærslurnar sjálfkrafa breytt stöðu skjalsins úr **Bíður fyrirframgreiðslu** í **Útgefið**. Þegar þú setur upp verkraðarfærslurnar eru kóðaeiningarnar sem þú þarft að nota **384 Uppf. fyrirfgr. á sölu í bið** og **384 Uppf. fyrirfgr. á innkaupum í bið**. Mælt er með því að keyra færslurnar reglulega, t.d. á mínútu fresti. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Sjá einnig .

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
