---
title: Kynning á contoso Coffee
description: Yfirlit yfir Aðstæður fyrir hvernig contoso kaffi sýnikennsla getur auðveldað þér að læra hvernig hægt er að nýta vöruhúsaggetu í viðskiptum miðsvæðis.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-warehousing"></a><a name="introduction-to-contoso-coffee-warehousing"></a><a name="introduction-to-contoso-coffee-warehousing"></a>Kynning á contoso Coffee Vöruhúsnæðinu

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki.  **Útinnandi kaffiforrit**  fyrir fyrirtæki seðlabankar bæta við sýnigögnum sem nota má til að læra hvernig hægt er að nýta sér Vöruhúsagetu í viðskiptum miðsvæðis. Hægt er að skilgreina vöruhúsaaðgerðir á ýmsa vegu, sjá  [Yfirlit yfir mismunandi skilgreiningarvalkosti](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Í App eru þrjár staðsetningar sem eru bestar fyrir mismunandi atburðarás:

- **SILFUR**  

  Þessi staðsetning samskipar að nota hólf. Auðvelt getur verið að skilgreina hann til að styðja undirstöðu eða Ítarlegt. 

- **GULT**  

  Þessi staðsetning notar ítarlegri skilgreiningu vöruhúss en notar ekki hólf. Hægt er að endurskilgreina hana til að styðja grunnskilgreiningar.

- **HVÍTT**  

  Þessi staðsetning notar ítarlega samstillingu vöruhússins með beinum frágangi og tínslu, sem gerir ítarlegri reglur um hvernig vörur eru færðar í öllu vöruhúsi.

## <a name="set-up-contoso-coffee-warehousing-data"></a><a name="set-up-contoso-coffee-warehousing-data"></a><a name="set-up-contoso-coffee-warehousing-data"></a>Setja upp contoso Coffee Vöruhúsgagnagerð

Til að nota contoso Coffee Vöruhúsgögnunum sýnigögnin þarf að setja upp tvö forrit í viðkomandi fyrirtæki í [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Gagnamengi Contoso Coffee**  

    Þetta forrit afhendir sýnigögn fyrir grunnforritið.  
- **Sýnigagnamengi Contoso Coffee (auðkenni lands)**  

    Þetta forrit bætir landsbundnu efni við efst í grunnforritið.

Bættu forritunum við autt fyrirtæki í greiddri áskrift eða sem hluti af prufuáskrift. Stofnaðu til dæmis nýtt fyrirtæki með engin sýnigögn úr uppsetningarleiðbeiningunni **Stofna nýtt fyrirtæki** sem hægt er að opna úr listanum **Fyrirtæki**. Bættu þá appinu við af  [markaðstorginu](../../ui-extensions-install-uninstall.md#install)  ef þær eru ekki þegar á skrá á  **síðu framlengingarstjórnunar** .  

Þegar viðeigandi forrit eru sett upp skal fara á  [síðuna contoso Coffee Vöruhúsavöruvöruhúss](https://businesscentral.dynamics.com/?page=4761)  í  [!INCLUDE [prod_short](../../includes/prod_short.md)] og breyta sjálfgefnum stillingum sem henta þínum þörfum. Eftirfarandi tafla lýsir stillingum:  

|Svæði  |Description  |
|---------|---------|
|**Upphafsár** |Tilgreinir fyrsta árið sem óskað er eftir að notuð séu útsýnandi Kaffisýnigögn. Árið er annað hvort almanaksár eða reikningsár en það fer eftir uppsetningu fyrirtækisins.|
|**Birgðageymsla bí**  |Staðsetning til nota fyrir helstu aðstæður á staðnum.|
|**Staðsetning adv. Logistics**  |Staðsetningin til að nota við að einfalda vörustjórnunaraðstæður.|
|**Staðsetning beinn frágangur og tínsla**  |Staðsetningin til að nota fyrir ítarlegar aðstæður vörustjórnunar.|
|**Staðsetning í flutningi**  |Staðsetning til að nota fyrir innsendingarstað í flutningsáætlunum.|
|**Viðskiptamaður nr**.  |Viðskiptavininn til að nota til grundvallar og einfaldrar atburðarásar í söluaðgerðum.|
|**Nr. lánardrottins**  |Lánardrottinn sem nota á fyrir allar áætlanir í innkaupaaðgerðum.|
|**Aðalatriði nr**.  |Varan sem nota á fyrir allar aðstæður í söluaðgerðum.|
|**Liður 1 nr**.  |Aðalatriðið til að nota við allar aðstæður.|
|**Liður 2 nr**.  |Aukavaran sem nota á fyrir allar aðstæður.|
|**Bókunarflokkur viðskm**.|Tilgreinir viðskiptakóta fyrir innlenda viðskiptamenn. Viðskiptakóðarnir eru notaðir þegar færslur eru bókaðar. |
|**Almennir viðskiptabókunarflokkar viðskiptavina**|Tilgreinir viðskiptakóta fyrir innlenda viðskiptamenn. Viðskiptakóðarnir eru notaðir þegar færslur eru bókaðar. |
|**Bókunarflokkur lánardrottins**|Tilgreinir viðskiptakóða fyrir innlenda viðskiptavini og lánardrottna. Viðskiptakóðarnir eru notaðir þegar færslur eru bókaðar. |
|**Almennur viðskiptabókunarflokkur lánardrottins**|Tilgreinir viðskiptakóða fyrir innlenda viðskiptavini og lánardrottna. Viðskiptakóðarnir eru notaðir þegar færslur eru bókaðar. |
|**Innlendur-VSK-viðskiptabókunarflokkur**|Tilgreinir VSK-viðskiptakóða fyrir viðskiptavini og lánardrottna til bókunar á VSK ef VSK er virkjaður.|
|**Endursölu-Birgðabókunarflokkur**    |Tilgreinir kóta fyrir vörur sem þarf að nota til að bóka endursölu.|
|**Smásala – almennur vörubókunarflokkur**    |Tilgreinir kóta fyrir vörur sem þarf að nota til að bóka smásölu.|
|**VSK-vörubókunarflokk**    |Tilgreinir VSK-afurðarkóta fyrir vörur fyrir bókun VSK ef VSK er virkjaður.|
|**Verðstuðull**     |Tilgreinir stuðul til að umbreyta verði úr USD/EUR í staðbundinn gjaldmiðil. *1* þýðir að verðið er sama upphæð í hvaða gjaldmiðli sem er. Hærri tala verður notuð til að fá verðið í staðbundnum gjaldmiðli. |
|**Sléttunarnákvæmni**  |Skilgreinir hvernig reiknað notkunarmagn er sléttað þegar það er fært inn á notkunarbókarlínur. Magn undir 0,5 verður sléttað niður Magn sem er 0,5 eða meira verður sléttað upp.|

Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

> [!IMPORTANT]
> Ef verið er að keyra atburðarásina kann að vera hægt að sannreyna að notandanum hafi verið bætt við hana á völdum stöðum. Frekari upplýsingar er að finna  [í setja upp starfsmenn](../../warehouse-how-to-set-up-warehouse-employees.md) vöruhúss.

## <a name="scenarios"></a><a name="scenarios"></a><a name="scenarios"></a>Dæmi

Contoso Coffee vöruhúsgögnunum sýnigögn sem nú styðja við eftirfarandi Aðstæður til prófs og þjálfunar:

1.  [Ganga frá innflæði á innleið og útleið í grunnstillingum vöruhúss](warehouse-basic-flow-putaway-pick.md)
2.  [Vasaljós á inn-og útrennsli í Blönduðum Vöruhúsaleiðingum](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Ganga frá inn-og útstreymissútflæði í ítarlegri samskipan vöruhúss með beinan frágang og tínslu](warehouse-directed-flow.md)

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Uppsetning birgða](../../inventory-setup-inventory.md) 
[hvernig setja á upp staðsetningar](../../inventory-how-setup-locations.md) 
[yrir upplýsingar um](../../warehouse-manage-warehouse.md) 
[hönnun vöruhúsa](../../design-details-warehouse-overview.md) 
