---
title: Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur
description: 'MF-færslur sem þú færð frá félögunum eru skráðar í MF-innhólfinu, þar sem þær eru í vinnslu handvirkt eða sjálfvirkt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.service: dynamics-365-business-central
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur

MF-færslurnar sem þú færð frá félögunum eru skráðar á  **síðuna MF-Innhólf** . Til að fræðast um hvernig á að vinna úr samstæðufærslum er farið í að  [vinna úr færslum milli fyrirtækja](#process-incoming-intercompany-transactions). MF-færslurnar sem sendar eru til samstarfsaðila eru á lista á  **síðunni um Milliútg** . Til að læra hvernig á að vinna færslur milli samstæðufærslna er farið í  [til að vinna úr MF-færslum](#to-process-outgoing-intercompany-transactions).

Eftir uppsetningu samstæðunnar eru sumar færslur Afgreiddar sjálfkrafa. Hægt er að setja upp upprunafyrirtæki og samstarfsfyrirtæki til að stofna sjálfkrafa skjöl og færslubækur sem samsvara færslum sem aðilar bóka í gegnum almenna færslubók innan samstæðu. Til að fræðast um notkun samstæðubóka er farið í að  [fylla út og bóka MF-færslubók](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox"></a>Innhólfinu raðað

Hægt er að nota afmörkunarreitina efst á innhólfinu til að ákvarða hvaða færslur eru sýndar á síðunni. Til dæmis, ef aðeins á að kanna færslur sem tiltekinn samstarfsaðili stofnaði, nota  **uppruna**  og  **kótaafmarkanir Færslufélagakóða**  innan samstæðu.  

### <a name="transaction-source"></a>Uppruni færslu

Það sem hægt er að gera við færslu fer eftir því hvort hún var:  

* Stofnuð af Millifyrirtækjafélaga  
* Hafnað af MF-félaga og send til baka  

 **Notið svæðið Sýna upprunakátt**  færslu til að afmarka  **síðuna síða MF-innhólfsfærslna**  þannig að hún birti eina af þessum færslugerðum. Einnig er hægt að afmarka eftir MF-félaga, eða efni  **reitsins Línuaðgerð** .  

#### <a name="created-by-intercompany-partner"></a>Stofnað af samstæðufélaga

 Þegar ný færsla berst sem var stofnuð af félaga er hægt að velja að:

* Samþykkja færsluna  
* Hafna færslunni (skila til samstarfsaðila)  
* Hætta við færsluna (eyða færslunni og skila henni ekki til félaganna)  

#### <a name="returned-from-intercompany-partner"></a>Skilað frá samstæðufélaga

Ef MF-félaginn hafnar færslu verður að hætta við færsluna í innhólfinu og stofna síðan leiðréttingarlínur eða bakfæra færslubókina eða skjalið.  

## <a name="recreating-inbox-entries"></a>Endurbúa innhólfsfærslur

Ef færsla var samþykkt í innhólfinu en fylgiskjalinu eða færslubókinni var síðan eytt án þess að bóka hana er hægt að stofna innhólfsfærsluna aftur og samþykkja hana aftur.  

## <a name="get-an-overview-of-intercompany-transactions-for-a-period"></a>Fá yfirlit yfir færslur milli fyrirtækja á tímabili

Hægt er að fá yfirlit yfir allar færslur milli fyrirtækja sem tekið var við og hafa verið sendar á tilteknu tímabili. Í skýrslunni **Millifyrirtækjafærslur** koma fram allar fjárhagsfærslur, viðskiptamannafærslur og lánardrottnafærslur milli fyrirtækja.

> [!NOTE]  
> Ef samstæðufélagarnir eru í sama gagnagrunni geta samstarfsaðilar sjálfkrafa tekið við viðskiptum. Farið beint  **í Afgreiddar MF-innhólfsfærslur**  og  **meðhöndlað færslur MF-úthólfsfærslna** . Frekari upplýsingar um sjálfvirka samþykkt færslna má fá með því að fara í  [sjálfvirkar færslur frá samstæðufélögum](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * Fyrir samstillingarfélagana, á  **síðu Samstæðuuppsetningar**, er kveikt á  **Auto. senda færslur**  skipta.
> * Ef um er að ræða samstarfsfyrirtæki, á  **síðu félaga**  innan samstæðunnar, skal kveikja á Auto. taka til  **skipta á færslum** .  

## <a name="import-intercompany-transactions-from-a-file"></a>Flytja færslur milli fyrirtækja inn úr skrá

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Ef fyrirtækið er með milli-fyrirtækjafélaga sem er ekki í sama gagnagrunni og fyrirtækið er hægt að taka á móti færslum milli fyrirtækja frá félaganum í XML-skrá. Síðan þarf að flytja færslurnar inn í innhólfið.  

1. Vistaðu skrána á staðinn sem tilgreindur var í reitnum **Upplýsingar um samstæðuinnhólf** þegar samstæðan er sett upp.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-innhólfsfærslur** og velja síðan viðkomandi tengil.
3. Á síðunni **Færslur í innboxi millifyrirtækis** skal velja **Flytja inn færsluskrá** aðgerðina.  
4. á síðunni sem birtist er XML-skráin með færslunum valin og síðan smellt á hnappinn **Opna**.  

Færslurnar eru fluttar inn í innhólfið og nú er hægt að vinna með þær.

## <a name="process-incoming-intercompany-transactions"></a>Vinna úr innsendum samstæðufærslum

Þegar milli-fyrirtækjafélagar senda færslur milli fyrirtækja enda færslurnar í milli-fyrirtækjainnhólfinu. Meta þarf hverja færslu í pósthólfinu og bregðast við því.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-innhólfsfærslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Færslur í innhólfi millifyrirtækis** skal velja línu og síðan aðgerð, eins og t.d. **Samþykkja** til að setja línuna í ferli.
3. Á síðunni **Lokið MF-innhólf aðgerð** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velja hnappinn **Í lagi**.  

Fyrir línur sem samþykktar eru eru fylgiskjals-eða færslubókarlínurnar stofnaðar í fyrirtækinu. Opna skal hvert fylgiskjal eða færslubók, gera nauðsynlegar breytingar og bóka.  

Línum sem þú hafnar og skila á félaginn fara í MF-úthólfið, þar sem þú getur sent félaginn.

Fyrir línur sem félagi hefur verið hafnað og skilað til þín þarf að bóka leiðréttingu á upphaflegu færslunni sem þú bókaðir í fyrirtækinu.

## <a name="to-process-outgoing-intercompany-transactions"></a>Vinna færslur milli fyrirtækja á útleið

Þegar bókuð er MF-færslubók eða-fylgiskjal eða send staðfesting samstæðupöntunar, fara færslurnar í MF-Úthólf notanda. Til að senda til MF-félaga skaltu opna úthólfið og vinna úr þeim.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-úthólfsfærslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Færslur í úthólfi millifyrirtækis** skal velja línu og síðan aðgerð, eins og t.d. **Fara aftur í innhólf** til að setja línuna í ferli.

 **Notið aðgerðina senda til MF-félaga**  til að senda línur í innhólf viðkomandi félaga.

Nota skal  **aðgerðina endursenda til innhólfsaðgerð**  til að flytja línur í innhólfið, þar sem hægt er að samþykkja þær til að stofna skjöl eða færslubókarlínur í fyrirtækinu.  

Ef hætt er við að  **nota aðgerðina Hætta**  við verður að bóka leiðréttingu á færsluna sem upphaflega var bókuð hjá fyrirtækinu.  

## <a name="recreate-intercompany-inbox-transactions"></a>Endurgera færslur í MF-innhólfi

Þú gætir viljað endurstofna færslu í innhólfinu eða úthólfinu. Ef t.d. færsla var samþykkt í innhólfinu en fylgiskjalinu eða færslubókinni var síðan eytt án þess að bóka hana er hægt að stofna innhólfsfærsluna aftur og samþykkja hana aftur.  

Eftirfarandi ferli lýsir hvernig eigi að endurstofna innhólfsfærslur, en sömu skref eiga einnig við um úthólfið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afgreiddar MF-innhólfsfærslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Afgreiddar MF-innhólfsfærslur** veljið línuna með færslunni sem á að stofna aftur í innhólfinu, og veljið svo **Endurstofna innhólfsfærslu** aðgerðina.  

## <a name="see-also"></a>Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
