---
title: Uppsetning staðsetningarspjalds og skilgreining flutningsleiða (inniheldur myndskeið)
description: 'Ef þú kaupir, geymir eða selur hluti á fleiri en einum stað getur þú sett hvern stað upp sem staðsetningu.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 03/25/2023
ms.author: bholtorf
---
# <a name="set-up-locations" />Uppsetning birgðageymsla

Staðsetningar eru staðir eins og vöruhús þar sem vörur eru keyptar, geymdar eða seldar. [!INCLUDE [prod_short](includes/prod_short.md)] notar staðsetningar til að hjálpa til við að fylgjast með birgðum í bæði einföldum og flóknum vöruhúsaferlum.

Síðan er hægt að búa til skjalalínur fyrir tilgreinda staðsetningu, skoða tiltækileika eftir staðsetningu og flytja birgðir milli staða. Til að fá frekari upplýsingar er farið í að  [stjórna birgðum](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards" />Staðsetningarspjöld

Upplýsingar um staðsetningu eins og vöruhús eða dreifingarmiðstöð eru tilgreindar á síðunni **Birgðageymsluspjald**. Hver geymsla fær heiti og kóða. Hægt er að færa birgðageymslukóðann inn annars staðar í forritinu þegar skrá þarf færslur vegna tiltekinnar birgðageymslu.  

Hægt er að færa inn upplýsingar um hólf og um skipan vöruhússins fyrir hverja staðsetningu. Það fer eftir vöruhúsareglunum þínum, en hægt er að nota valkostina í flýtiflipanum **Hólf** til að tilgreina hólfin sem á að nota sjálfgefið fyrir færslur. Ef notaður er beinn frágangur og tínsla gera valkostirnir í flýtiflipanum **Hólfareglur** þér kleift að nota ítarlega eiginleika vöruhúsavinnu.  

Sumir valreitir eru háðir stillingum á síðunni **Birgðageymsluspjald** til að takmarka óstuddar samsetningar uppsetningar.  

Veldu **Svæði** eða **Hólf** aðgerðirnar til að skoða upplýsingar um svæði og hólf sem gætu verið skilgreint fyrir birgðageymsluna.

### <a name="to-set-up-a-location" />Uppsetning birgðageymslna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Endurtakið skref 2 og 3 fyrir hverja staðsetningu þar sem á að halda utan um birgðir.

> [!NOTE]  
> Margir reitir á síðu birgðageymsluspjalsins vísa til meðhöndlunar vara í vöruhúsaferli á inn- og útleið. Þessir reitir skipta ekki máli fyrir fyrirtæki sem þurfa ekki flókna vöruhúsavirkni. Til að fá frekari upplýsingar er farið í að  [Setja upp vöruhúsastjórnun](warehouse-setup-warehouse.md).

Hægt er að breyta grunnstillingu staðsetningar svo lengi sem hún er ekki með birgðabókafærslur.  

Hægt er að skilgreina flutningsleiðir milli staða ef margir staðir eru til staðar. Til að fræðast meira um flutningsleiðir er farið í  [til að stofna flutningsleið](inventory-how-setup-locations.md#to-create-a-transfer-route).

### <a name="to-create-a-transfer-route" />Flutningsleið búin til

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningsleiðir** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
4. Á síðunni **Staðsetningarspjald** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nú er hægt að flytja birgðavörur milli tveggja staða. Til að fræðast meira um flutninga er farið í að  [flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md).

## <a name="bins" />Hólf

Hólf tákna grunnskipulag vöruhúss og geta gefið til kynna hvar eigi að setja vörur. Hólfin geta verið með efni eða verið fljótandi hólf án tiltekins efnis.

Til að nota hólfavirknina á staðsetningu, á síðunni **Birgðageymsluspjald**, í flýtiflipanum **Vöruhús**, skal kveikja á **Hólf áskilið**. Þú getur hannað vöruflæðið á staðsetningunni með því að tilgreina hólfakóða í reitnum fyrir vöruhúsaferlin í flýtiflipunum **Hólf** og **Hólfareglur**.

> [!NOTE]
> Áður en hægt er að tilgreina hólfakóða á staðsetningu þarf að búa til hólfakóða. Frekari upplýsingar um hólfin er að fá með því að  [stofna hólf](warehouse-how-to-create-individual-bins.md)  og  [Setja upp hólfagerðir](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones" />Svæði

Ef stofna á hólfin á svæðum má gera það á síðunni **Svæði**. Þegar svæðum er úthlutað á hólf afritar [!INCLUDE [prod_short](includes/prod_short.md)] upplýsingar af svæðinu og í hólfin. Einnig er hægt að velja að setja upp eitt svæði og nota hólf út af fyrir sig til að skipuleggja vöruhúsið. Til að fræðast meira um svæði er farið í að  [Setja upp vöruhúsastjórnun](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations" />Sjálfgefnar víddir fyrir birgðageymslur

Víddir eru gildi sem flokka færslur svo hægt sé að rekja þær og greina þær með ýmsum skýrslugerðarverkfærum. Víddir geta til dæmis gefið til kynna deildina eða verkið sem færslan kom frá. Með sjálfgefinni vídd hjálpar fólki að forðast mistök og þarf að færa inn víddir handvirkt á færslustiginu ef allar vörur koma frá einu stað og deild.

Þú velur sjálfgefnar víddir fyrir birgðageymslu á síðunni **Birgðageymsluspjald** með því að velja **Víddir**. Eftir sem áður er sjálfgefnum víddum staðsetningar úthlutað á eftirfarandi skjöl þegar valin er birgðageymslan í línu.

* Flutningspöntunum
* Efnislegar birgðapantanir
* Birgðaafhendingar
* Innhreyfingar birgða
* Birgðabækur

Ef þörf krefur er hægt að eyða eða breyta víddinni í línunni. Í reitnum **Virðisbókun** er hægt að krefja fólk um að tilgreina víddir fyrir birgðageymslur áður en það getur bókað færslu. Ef leyfa á fólki að velja aðeins eitt ákveðið víddargildi er hægt að tilgreina gildin í reitnum **Sía fyrir leyfileg gildi**. Einnig er hægt að hafa með víddargildi birgðageymslu á síðunni **Forgangur sjálfgefinnar víddar** og fyrir samsetningar á forgangi og víddarreglum á síðunni **Víddasamsetningar**.

Þar sem gögn um flutning pöntunar og Endurflokkunarbækur fást á fleiri en einum stað er röðin sem færð er inn mikilvæg. Sjálfgefnar víddir eru afritaðar úr Síðasta birgðageymslusvæði (innsendingarstaðsetningin er hunsuð).

### <a name="example-of-default-dimensions-on-locations" />Dæmi sjálfgefinnar víddar á birgðageymslum

Eftirfarandi dæmi sýna hvernig sjálfgefna víddin er notuð.

Eftirfarandi víddarstillingum er fylgt:

* Staðsetning AUSTAST. Deild vídd er ADM
* Staðsetning VESTAST. Vídd deildar er PROD

Staðsetningin í millisendingarröð er tilgreind á eftirfarandi hátt:

1. Frá stað = AUSTUR
2. Til staðar = VESTFIRÐIR

Hæddarvíddin verður afrituð úr VESTMANNA.

Reitirnir í öfugri röð eru fylltir út á eftirfarandi hátt:

1. Til staðar = VESTFIRÐIR
2. Frá stað = AUSTUR

ADM-víddin verður afrituð úr stað AUSTUR.

## <a name="see-related-training-at-microsoft-learnlearnmodulestrade-set-up-dynamics-365-business-central" />Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/trade-set-up-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Stjórna birgðum](inventory-manage-inventory.md)  
[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  
[Stofna hólf](warehouse-how-to-create-individual-bins.md)  
[Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
