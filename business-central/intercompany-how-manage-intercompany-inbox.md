---
title: Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur
description: Millifyrirtækjafærslur sem berast frá félögum eru taldar upp í MF-innhólfinu þar sem þær eru unnar handvirkt eða sjálfvirkt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.service: dynamics-365-business-central
---
# Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur

Millifyrirtækjafærslurnar sem berast frá félögum eru taldar upp á síðunni **MF-innhólf** . Til að læra hvernig á að vinna færslur milli fyrirtækja á innleið er farið [í Vinna færslur milli fyrirtækja á innleið](#process-incoming-intercompany-transactions). Millifyrirtækjafærslurnar sem sendar eru félögum eru taldar upp á síðunni **MF-úthólf** . Til að læra hvernig á að vinna færslur milli fyrirtækja á útleið er farið í Til að [vinna færslur milli fyrirtækja á útleið](#to-process-outgoing-intercompany-transactions).

Sumar færslur eru þó sjálfkrafa afgreiddar eftir uppsetningu milli fyrirtækja. Hægt er að setja upp upprunafyrirtæki og samstarfsfyrirtæki til að stofna sjálfkrafa skjöl og færslubækur sem samsvara færslum sem félagar bóka í gegnum færslubók milli fyrirtækja. Til að [fræðast um notkun MF-færslubóka er farið í Fylla út og bóka MF-færslubók](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## Innhólfinu raðað  

Hægt er að nota afmörkunarreitina efst á innhólfssíðunni til að ákvarða hvaða færslur eru birtar á síðunni. Eigi t.d. aðeins að skoða færslur sem tiltekinn félagi stofnaði skal nota **afmarkanirnar Uppruni** færslu og **MF-félagakóti** .  

### Uppruni færslu  

Það sem hægt er að gera við færslu fer eftir því hvort hún var:  

* Stofnuð af Millifyrirtækjafélaga  
* Hafnað af MF-félaga og send til baka  

Reiturinn **Sýna uppruna** færslu er notaður til að afmarka **síðuna MF-innhólfsfærslur** þannig að hún birtir aðeins eina af þessum færslutegundum. Einnig er hægt að afmarka eftir MF-félaga eða eftir efni reitsins **Línuaðgerð** .  

#### Stofnað af MF-félaga  

 Þegar ný færsla berst sem var stofnuð af félaga er hægt að velja að:

* Samþykkja færsluna  
* Hafna færslunni (fara aftur til félaga)  
* Hætta við færsluna (eyða færslunni og skila henni ekki til félagans)  

#### Skilað frá MF-félaga  

Ef MF-félaginn hafnar færslu verður að hætta við færsluna í innhólfinu og stofna síðan leiðréttingarlínur eða bakfæra færslubókina eða fylgiskjalið.  

## Innhólfsfærslur endurteknar  

Ef færsla var samþykkt í innhólfinu en fylgiskjalinu eða færslubókinni var síðan eytt án þess að bóka hana er hægt að stofna innhólfsfærsluna aftur og samþykkja hana aftur.  

## Fá yfirlit yfir færslur milli fyrirtækja á tilteknu tímabili  

Hægt er að fá yfirlit yfir allar færslur milli fyrirtækja sem tekið var við og hafa verið sendar á tilteknu tímabili. Í skýrslunni **Millifyrirtækjafærslur** koma fram allar fjárhagsfærslur, viðskiptamannafærslur og lánardrottnafærslur milli fyrirtækja.

> [!NOTE]  
> Ef félagar milli fyrirtækja eru í sama gagnagrunni geta félagarnir samþykkt færslurnar sjálfkrafa. Fara beint á síðurnar **Afgreiddar MF-innhólfsfærslur** og **Afgreiddar MF-úthólfsfærslur** . Til að fá nánari upplýsingar um sjálfvirka samþykkt færslna er farið í [Sjálfvirk viðskipti frá milli-fyrirtækjafélögum](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * Fyrir samstillingarfélagann á síðunni **Uppsetning** milli fyrirtækja er kveikt á víxlinu **Sjálfvirk sending færslna** .
> * Á síðunni **Millifyrirtækjafélagar** er kveikt á víxlinu **Sjálfvirkt. Samþykkja færslur** .  

## Flytja inn færslur milli fyrirtækja úr skrá

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Ef fyrirtækið er með milli-fyrirtækjafélaga sem er ekki í sama gagnagrunni og fyrirtækið er hægt að taka á móti færslum milli fyrirtækja frá félaganum í XML-skrá. Síðan þarf að flytja færslurnar inn í innhólfið.  

1. Vistaðu skrána á staðinn sem tilgreindur var í reitnum **Upplýsingar um samstæðuinnhólf** þegar samstæðan er sett upp.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-innhólfsfærslur** og velja síðan viðkomandi tengil.
3. Á síðunni **Færslur í innboxi millifyrirtækis** skal velja **Flytja inn færsluskrá** aðgerðina.  
4. á síðunni sem birtist er XML-skráin með færslunum valin og síðan smellt á hnappinn **Opna**.  

Færslurnar eru fluttar inn í innhólfið og nú er hægt að vinna með þær.

## Vinna færslur milli fyrirtækja á innleið  

Þegar milli-fyrirtækjafélagar senda færslur milli fyrirtækja enda færslurnar í milli-fyrirtækjainnhólfinu. Meta verður hverja færslu í innhólfinu og bregðast við henni.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-innhólfsfærslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Færslur í innhólfi millifyrirtækis** skal velja línu og síðan aðgerð, eins og t.d. **Samþykkja** til að setja línuna í ferli.
3. Á síðunni **Lokið MF-innhólf aðgerð** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velja hnappinn **Í lagi**.  

Fyrir línur sem notandi samþykkir eru fylgiskjals- eða færslubókarlínur stofnaðar í fyrirtækinu. Opna skal hvert fylgiskjal eða færslubók, gera nauðsynlegar breytingar og bóka.  

Línur sem hafnað er og fara aftur til félagans fara í MF-úthólfið þar sem hægt er að senda þær til félagans.

Fyrir línur sem félagi hafnaði og skilaði til notanda verður að bóka leiðréttingu á upphaflegu færslunni sem bókuð var í fyrirtækinu.

## Vinna færslur milli fyrirtækja á útleið  

Þegar færslubók eða fylgiskjal milli fyrirtækja er bókað eða pantanastaðfesting milli fyrirtækja er send fara færslurnar í MF-úthólfið. Til að senda þeim til MF-félaga er úthólfið opnað og unnið úr þeim.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-úthólfsfærslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Færslur í úthólfi millifyrirtækis** skal velja línu og síðan aðgerð, eins og t.d. **Fara aftur í innhólf** til að setja línuna í ferli.

Nota aðgerðina **Senda til MF-félaga** til að senda línur í innhólf viðkomandi félaga.

Nota aðgerðina **Skila í innhólf** til að færa línur í innhólfið þar sem hægt er að samþykkja þær til að stofna skjöl eða færslubókarlínur í fyrirtækinu.  

Ef aðgerðin **Hætta við** er notuð verður að bóka leiðréttingu á færslunni sem upphaflega var bókuð í fyrirtækinu.  

## Endurstefna innhólfsfærslur milli fyrirtækja  

Hugsanlega þarf að stofna aftur færslu í innhólfinu eða úthólfinu. Ef t.d. færsla var samþykkt í innhólfinu en fylgiskjalinu eða færslubókinni var síðan eytt án þess að bóka hana er hægt að stofna innhólfsfærsluna aftur og samþykkja hana aftur.  

Eftirfarandi ferli lýsir hvernig eigi að endurstofna innhólfsfærslur, en sömu skref eiga einnig við um úthólfið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afgreiddar MF-innhólfsfærslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Afgreiddar MF-innhólfsfærslur** veljið línuna með færslunni sem á að stofna aftur í innhólfinu, og veljið svo **Endurstofna innhólfsfærslu** aðgerðina.  

## Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
