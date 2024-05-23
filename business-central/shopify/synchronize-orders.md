---
title: Samstilla og uppfylla sölupantanir
description: Setja upp og keyra innflutning og vinnslu sölupantana úr Shopify.
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="synchronize-and-fulfill-sales-orders"></a>Samstilla og uppfylla sölupantanir

Þessi grein lýsir áskildum stillingum og skrefum sem þú verður að ljúka til að samstilla og uppfylla sölupantanir með Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Setja innflutning pantana á Shopify Verslunarkortið

 **Færa skal inn gjaldmiðilskóta** ef netverslunin notar annan gjaldmiðil en staðbundinn gjaldmiðil (SGM). Tilgreindur gjaldmiðill verður að hafa stillt gengi. Ef vefverslunin þín notar sama gjaldmiðil og [!INCLUDE[prod_short](../includes/prod_short.md)] skaltu skilja þennan reit eftir auðan. 

Hægt er að fá aðgang að gjaldmiðili verslunar [í stillingum](https://www.shopify.com/admin/settings/general) upplýsinga í versluninni í Stjórnandanum Shopify . Shopify hægt er að grunnstilla til að samþykkja mismunandi gjaldmiðla. Hins vegar eru fluttar inn pantanir í [!INCLUDE[prod_short](../includes/prod_short.md)] verslunargjaldmiðil.

Venjuleg Shopify pöntun getur falið í sér kostnað til viðbótar við millisamtöluna, svo sem sendingargjöld eða, ef slíkt er virkt, ábendingar. Þessar upphæðir eru bókaðar beint á fjárhagsreikninginn sem nota á fyrir tilteknar viðskiptategundir:

* **Reikningur flutningsgjalda**
* **Seldur gjafakortsreikningur** frekari upplýsingar er að finna á [Gjafakort](synchronize-orders.md#gift-cards)
* **Þjórfésreikningur**  

Virkja sjálfvirkar **Stofna pantanir sjálfkrafa** til að búa til söluskjöl sjálfkrafa [!INCLUDE[prod_short](../includes/prod_short.md)] þegar Shopify pöntunin hefur verið flutt inn.

Ef gefa á söluskjalið út sjálfvirkt er vífært á vífæringuna **Sjálfvirk útgáfa sölupöntunar** .

Ef ekki á að senda sjálfvirkar afhendingastaðfestingar til viðskiptamanna er slökkt á vífærinu **Senda staðfestingu á sendingu** . Það getur komið sér vel að slökkva á stafrænum vörum ef þú selur stafrænar vörur eða vilt nota aðra tilkynningabúnað.

Ef reiturinn **Shopify Pöntunarnr. á skjallínu** er valinn eru [!INCLUDE [prod_short](../includes/prod_short.md)]  sölulínur af tegundinni **Athugasemd** settar inn með pöntunarnúmerinu Shopify .

> [!NOTE]
> Söluskjalið í [!INCLUDE[prod_short](../includes/prod_short.md)] tenglum við pöntunina Shopify og hægt er að bæta við pöntunarnúmerinu **Shopify .** á lista- eða spjaldsíður fyrir sölupantanir, reikninga og afhendingar. Nánari upplýsingar um hvernig reit er bætt við er farið í Hefja sérstillingu með því að [nota sérstillingarstillinguna](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

Í reitnum **Forgangur** skattsvæðis er forgangsraðað hvernig á að velja skattsvæðiskóta fyrir aðsetur í pöntunum. Í Shopify pöntuninni sem fluttar eru inn eru upplýsingar um skatta. Skattar eru endurreiknaðir þegar söluskjöl eru búin til svo mikilvægt er að VSK eða skattstillingar séu réttar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Nánari upplýsingar um skatta er farið í [Setja upp skatta fyrir tenginguna Shopify](setup-taxes.md).

Tilgreina hvernig á að vinna vöruskil og endurgreiðslur:

* **Auður** tilgreinir að vöruskil og endurgreiðslur séu ekki fluttar inn og vinnsla.
* **Aðeins** er flutt inn tilgreint að upplýsingar séu fluttar inn en samsvarandi kreditreikningur er stofnaður handvirkt.
* **Stofna kreditreikning** sjálfvirkt tilgreinir að upplýsingar séu fluttar inn og [!INCLUDE[prod_short](../includes/prod_short.md)] stofnar kreditreikningana sjálfkrafa. Þessi valkostur krefst þess að kveikt sé á vífæringu sjálfvirkrar **sölupöntunar** .

Tilgreina birgðageymslu fyrir vöruskil og fjárhagsreikninga fyrir endurgreiðslur fyrir vörur og aðrar endurgreiðslur.

* **Endurgreiðslureikningur utanbirgðavara** tilgreinir fjárhagsreikningsnr. fyrir vörur þar sem ekki á að leiðrétta birgðir.
* **Reikningur** endurgreiðslu tilgreinir fjárhagsreikning fyrir mismuninn í heildarupphæð endurgreiddrar upphæðar og heildarupphæð varanna.

Nánari upplýsingar um [vöruskil og endurgreiðslur](synchronize-orders.md#returns-and-refunds)

### <a name="shipment-method-mapping"></a>Vörpun afhendingarmáta

**Kóða afhendingarmáta** fyrir söluskjöl innflutt frá Shopify er hægt að fylla út sjálfkrafa. Þú þarft að skilgreina **Vörpun afhendingarmáta**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Veljið þá verslun sem á að skilgreina vörpun fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Vörpun afhendingarmáta**. Þetta býr sjálfkrafa til skrár fyrir sendingarmáta sem skilgreindir eru í stillingum [**Sendingar**](https://www.shopify.com/admin/settings/payments) í **Shopify stjórnandamiðstöðinni**.
4. Í reitnum **Heiti** er hægt að sjá heiti sendingarmáta frá Shopify.
5. Sláðu inn **Kóða sendingarmáta** ásamt samsvarandi sendingarmáta í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Ef mörg flutningsgjöld eru tengd við sölupöntun verður aðeins eitt valið og úthlutað á söluskjalið.

### <a name="location-mapping"></a>Vörpun staðsetningar

Birgðageymsluvörpunin þarf til að fylla út **Birgðageymslukóta** fyrir söluskjalslínur sem fluttar eru inn úr Shopify. Þetta er mikilvægt þegar valkosturinn **Staðsetning áskilin** er virkjuð á **Uppsetning birgða**, annars geturðu ekki búið til söluskjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Veljið verslunina sem á að stilla vörpun staðsetnigna fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Staðsetningar** til að opna **Shopify Staðsetningar verslunar**.
4. Veldu aðgerðina **Sækja Shopify Staðsetningar** til að flytja inn allar staðsetningarnar sem skilgreindar eru í Shopify. Þú finnur þær í stillingunum [**Staðsetningar**](https://www.shopify.com/admin/settings/locations) í stjórnendamiðstöð **Shopify þínu**. 
5. Sláðu inn **Sjálfgefinn staðsetningarkóða** með samsvarandi staðsetningu í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Birgðageymsluvörpun er einnig notuð til að samstilla birgðir. Nánari upplýsingar eru notaðar með því að [fara í Samstilla birgðir í Shopify](synchronize-items.md#sync-inventory-to-shopify).
  
## <a name="run-the-order-synchronization"></a>Keyra samstillingu pöntunar

Eftirfarandi ferli lýsir því hvernig eigi að flytja inn og uppfæra sölupantanir.

> [!NOTE]  
> Ekki er Shopify hægt að flytja inn safnvistaðar pantanir. Ef athuga þarf stöðu pöntunar er pöntunin opnuð á [pantanasíðu](https://www.shopify.com/admin/orders) stjórnborðsins **Shopify** og farið yfir pöntunarupplýsingar.
> 
> Slökktu á valkostinum **Safnvista pöntunina sjálfkrafa** í hlutanum **Úrvinnsla pantana** í stillingum fyrir **Útskráningu** í glugganum **Shopify Stjórnandi** til að tryggja að allar pantanir séu fluttar inn til [!INCLUDE[prod_short](../includes/prod_short.md)]. Ef þú þarft að flytja inn safnvistaðar pantanir skaltu nota aðgerðina **Taka pantanir úr geymslu** á síðunni [Pantanir](https://www.shopify.com/admin/orders) í glugganum **ShopifyStjórnandi**. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Velja verslun sem flytja á inn pantanir fyrir til að opna síðu **Shopify Verslunarkortsins**.
3. Veldu aðgerðina **Pantanir**.
4. Veldu aðgerðina **Samstilla pantanir frá Shopify**.
5. Skilgreina síur á pöntunum eftir þörfum. Til dæmis er hægt að flytja inn fullgreiddar pantanir eða þær sem eru með lága áhættustigið.

   > [!NOTE]  
   > Við afmörkun eftir merki ætti að nota afmörkunartákn `@` og `*`. Eigi t.d. að flytja inn pantanir sem innihalda *merki1*, skal nota `@*tag1*`. `@` tryggir að niðurstaðan sé ónæm en `*` finnur pantanir með mörgum merkjum.

6. Velja hnappinn **Í lagi**.

Einnig er hægt að leita að runuvinnslunni **Samstilla pantanir frá Shopify**.

Hægt er að tímasetja verkið sjálfkrafa. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

### <a name="under-the-hood"></a>Undir húddinu

Tengillinn Shopify flytur inn pantanir í tveimur skrefum:

1. Það flytur pantanahausa inn í töfluna **Shopify Pantanir til að flytja inn** þegar þeir uppfylla ákveðin skilyrði:

   * Þeir eru ekki í skjalasafni. Þetta þýðir að hægt er að taka pantanir með eða útiloka þær með því að geyma þær eða sleppa þeim í stjórnandanum Shopify .
   * Þær voru stofnaðar eða þeim breytt eftir síðustu samstillingu. Þetta þýðir að hægt er að þvinga inn flutning tiltekinnar pöntunar ef henni er breytt, til dæmis með því að bæta við **Athugasemdum** eða **Merki**.

2. Hann flytur Shopify inn pantanir og viðbótarupplýsingar.

   *  Shopify Connector vinnur úr öllum færslum í **Shopify töflunni Pantanir til að flytja inn** sem uppfylla afmörkunarskilyrðin sem tilgreind eru á **samstilltu pöntununum frá Shopify** beiðnisíðunni. Til dæmis merki, rás eða uppfyllingarstaða. Ef engar afmarkanir hafa verið tilgreindar vinnur hún allar færslur.
   * Þegar pöntun Shopify er Shopify flutt inn biður Connector um viðbótarupplýsingar frá Shopify:

     * Pöntunarhaus
     * Pöntunarlínur
     * Upplýsingar um afhendingu og uppfyllingu
     * Færslur
     * Vöruskil og endurgreiðslur, ef það er grunnstillt

Síðan **Shopify Pöntun til innflutnings** er gagnleg fyrir vandamál vegna innflutnings á úrræðaleitarpöntunum. Hægt er að meta pantanirnar sem eru tiltækar og taka næstu skref:

* Athuga hvort villa lokaði á innflutning ákveðinnar pöntunar og kanna upplýsingar villunnar. Villuleit er í reitnum **Villa** .
* Vinna aðeins ákveðnar pantanir. Fylla þarf út reitinn **Verkstæðiskóti**, velja eina eða fleiri pantanir og velja svo aðgerðina **Flytja inn valdar pantanir** .
* Eyða pöntunum af síðunni **Shopify Pöntun til að flytja inn** til að útiloka þær frá samstillingunni.

## <a name="review-imported-orders"></a>Yfirfara innfluttar pantanir

Þegar innflutningi er lokið er hægt að skoða pöntunina Shopify og finna allar tengdar upplýsingar, svo sem greiðslufærslur, sendingarkostnað, áhættustig, pöntunareigindir og seðla, eða uppfyllingar, hafi pöntunin þegar verið uppfyllt Shopify. Þú getur einnig séð allar staðfestingar pöntunar sem hefur verið send til viðskiptavinarins með því að velja aðgerðina **Shopify Stöðusíða**.

> [!NOTE]  
> Þú getur farið beint í gluggann **Shopify Pantanir** og þá birtast pantanir í stöðunni *opnar* í öllum verslunum. Til að fara yfir fullkláraðar pantanir þarf að opna **Shopify síðuna Pantanir** á tilteknu **Shopify síðunni Vinnusalarspjald** .

Áður en söluskjöl eru stofnuð í [!INCLUDE[prod_short](../includes/prod_short.md)] er hægt að nota **Samstilla pöntun úr Shopify** aðgerð á síðunni **Shopify Pöntun** til að færa inn tilteknar pantanir aftur.

Einnig er hægt að merkja pöntun sem greidda sem gagnlegar í B2B-tilviki þar sem greiðslur eru unnar utan Shopify brottfarar. Velja skal aðgerðina Merkja **sem greitt** á **Shopify pöntunarsíðunni** . Einnig er hægt að merkja pöntun sem afturköllun til að hefja endurgreiðsluflæðið í Shopify. Velja skal aðgerðina **Hætta við pöntun** á síðunni **Shopify Pöntun**, fylla út reitina eins og þörf krefur á síðunni **Shopify Hætta við pöntun** og ýta á **Í lagi**. Keyra þarf samstillingu pöntunar til að flytja uppfærslurnar [!INCLUDE[prod_short](../includes/prod_short.md)] inn í.

## <a name="create-sales-documents-in-business-central"></a>Stofna söluskjöl í Business Central

 **Ef vísbendingin Stofna sjálfvirkar pantanir** er virk á **Shopify verkstæðisspjaldinu** [!INCLUDE[prod_short](../includes/prod_short.md)]  reynir að stofna söluskjal eftir að pöntunin hefur verið flutt inn. Ef vandamál koma upp eins og að viðskiptavin eða vöru vantar þarftu að laga vandamálin og búa svo til sölupöntunina aftur.

### <a name="to-create-sales-documents"></a>Til að búa til söluskjöl

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Velja verslun sem á að samstilla pantanir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Pantanir**.
4. Veljið röðina sem stofna á söluskjal fyrir og veljið aðgerðina **Búa til söluskjöl**.
5. Velja **Já**.

Ef Shopify pöntunin krefst uppfyllingar **er Sölupöntun** stofnuð. Fyrir uppfylltar Shopify pantanir, svo sem þær pantanir sem innihalda aðeins gjafakort eða eru þegar meðhöndlaðar í Shopify verslunum, verður stofnaður **Sölureikningur**.

Söluskjal er stofnað og hægt er að stjórna því með stöðluðum [!INCLUDE[prod_short](../includes/prod_short.md)] aðgerðum.

Ef óskað er eftir að endurvinna söluskjal er hægt að nota aðgerðina **Ótengd úrvinnsla skjala** á síðunni **Shopify Pöntun** . Bent er á að þessi aðgerð eyðir ekki söluskjalinu sem þegar hefur verið stofnað. Það þarf að vinna handvirkt.

### <a name="manage-missing-customers"></a>Vinna með viðskiptavini sem vantar

Ef stillingarnar koma í veg fyrir að stofna viðskiptamann sjálfvirkt og samsvarandi viðskiptamaður finnst ekki þarf að úthluta viðskiptamanni pöntuninni Shopify handvirkt. Nokkrar leiðir eru til að úthluta viðskiptamönnum á pantanir:

*  **Selt-til viðskm.nr.** og **Reikn. færist á viðskm.** beint á síðunni **Shopify Pantanir** með því að velja viðskiptavin af listanum yfir núverandi viðskiptavini.
* Velja skal sniðmát viðskiptamanns og stofna síðan og úthluta viðskiptamanninum með aðgerðinni **Stofna nýjan viðskiptamann** á síðunni **Shopify Pantanir** . Viðskiptamaðurinn Shopify verður að hafa að minnsta kosti eitt aðsetur. Pantanir sem búnar eru til í Shopify gegnum sölurás sölustaðar vantar oft aðsetursupplýsingar.
* Varpa viðskiptamanni sem til er á tengdan **Shopify viðskiptamann á síðunni** Viðskiptamenn **Shopify** og velja svo aðgerðina **Finna vörpun** á síðunni **Shopify Pantanir** .

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Hvernig tengillinn velur hvaða viðskiptavin á að nota

Aðgerðin *Flytja inn pöntun frá Shopify* reynir að velja viðskiptavini í eftirfarandi röð:

1. Ef **Sjálfgefið númer viðskiptavinar.** Er skilgreind í Sniðmát viðskiptamanns **Shopify fyrir** Sendist-til - Lands-/svæðiskóti **og síðan reiturinn** Sjálfgefinn viðskm.nr **.** er notað óháð stillingum reitanna **Innflutningur viðskiptavinar frá Shopify** og **Vörpunargerð viðskiptavinar**. Nánari upplýsingar um viðskiptamannssniðmát eftir [landi](synchronize-customers.md#customer-template-per-countryregion).
2. Ef valkosturinn **Innflutningur viðskiptavinar frá Shopify** er stilltur á *Ekkert* og **Sjálfgefið nr. viðskiptavinar.** er skilgreint á síðunni **Shopify Verslunarkort** þá er **Sjálfgefið nr. viðskiptavinar.** er notað.

Næstu skref fara eftir **Tegund vörpunar viðskiptavinar**.

* Ef það er **Alltaf taka sjálfgefna viðskiptavininn**, þá notar tengillinn viðskiptavininn sem er skilgreindur í **Sjálfgefið nr. viðskiptavinar**. reitinn á síðunni **Shopify Verslunarkort**.
* Ef það er með **Eftir netfangi/síma** reynir tengillinn að finna núverandi viðskiptavin fyrst eftir skilríkjum, síðan eftir netfangi og að síðustu eftir símanúmeri. Ef viðskiptavinurinn finnst ekki stofnar tengillinn nýjan viðskiptavin.
* Ef það er **Eftir upplýsingum um „reikningsfæra á“** reynir tengillinn að finna fyrst þann viðskiptavin sem er til staðar með skilríkjum og síðan með upplýsingum um heimilisfang. Ef viðskiptavinurinn finnst ekki stofnar tengillinn nýjan viðskiptavin.

> [!NOTE]  
> Tengillinn notar upplýsingar frá heimilisfanginu sem reikningsfært er á og býr til viðskiptamanninn sem reikningsfært er á í [!INCLUDE[prod_short](../includes/prod_short.md)]. Selt-til - Viðskiptavinur er sami viðskiptavinur og reikningsfært er á.

Fyrir B2B pantanir er flæðið svipað þótt tengillinn noti reitina **Sjálfgefin fyrirtækisnr.**, **Flytja inn frá Shopify** fyrirtæki og **Tegund** fyrirtækisvörpunar á síðunni **Shopify Vinnusalarspjald** . Takið eftir að ekkert **sjálfgefið fyrirtækisnr.** í sniðmáti **Shopify** viðskiptamanns vegna þess að búist er við að viðskiptamenn hafi heitið á B2B.

### <a name="different-processing-rules-for-orders"></a>Mismunandi vinnslureglur fyrir pantanir

Hugsanlega þarf að vinna pantanir öðruvísi út frá reglu. Til dæmis ættu pantanir úr tiltekinni söluleið, líkt og SÖLUPANTANIR, að nota sjálfgefinn viðskiptavin en netverslunin á að hafa raunverulegar upplýsingar um viðskiptamanninn.

Ein leið til að takast á við þessa þörf er að stofna viðbótarverkstæðisspjald Shopify og nota afmarkanir á **samstilltar pantanir á Shopify** beiðnisíðunni.

Dæmi: Þú ert með netverslun og posa Shopify . Nota á fastan viðskiptamann fyrir sölupantanir en fyrir netverslunina á að stofna viðskiptavini í [!INCLUDE[prod_short](../includes/prod_short.md)]. Eftirfarandi ferli sýnir hástigsskrefin. Til að fræðast meira er farið í samsvarandi hjálpargreinar.

1. Búðu til Shopify búð sem heitir *STORE* og tengdu hana við reikninginn þinn Shopify .
1. Grunnstilla samstillingu vöru/vöru svo að verslunin stjórni vöruupplýsingum.
1. Tilgreina að viðskiptavinir séu fluttir inn með pöntunum. Tengillinn ætti að finna viðskiptavini með því að leita að netfangi sínu. Ef það finnur ekki aðsetur notar það viðskiptamannasniðmátið til að stofna nýjan viðskiptamann.
1.  Shopify Búa til búð sem heitir *POS* og tengja hana við sama Shopify reikning.
1. Ganga þarf úr skugga um að samstilling vöru/afurðar sé óvirk.
1. Velja tengið sem notar sjálfgefinn viðskiptavin.
1. Stofna ítrekunarfærslu verkraðar fyrir Samstilltar pantanir **skýrslu 30104 Shopify**. Valið er **STORE** í reitnum **Shopify Vinnusalarkóti** og afmarkanir notaðar til að ná öllum pöntunum nema þeim sem sölurás sölustaðar stofnar. Til dæmis,Sölustaður **<>**
1. Stofna ítrekunarfærslu verkraðar fyrir Samstilltar pantanir **skýrslu 30104 Shopify**. Velja **sölustað** í reitnum **Shopify Vinnusalarkóti** og nota afmarkanir til að ná pöntunum sem sölurás myndar. Til dæmis,Sölustaður **·**.

Hver verkröð mun flytja inn og vinna pantanir innan skilgreindra afmarkana og nota reglurnar á viðeigandi Shopify Verkstæðisspjaldi. Til dæmis stofnar hann sölustað fyrir sjálfgefinn viðskiptamann.

> [!Important]
> Til að forðast árekstra við vinnslu pantana skal nota sama tegund verkraðar fyrir báðar verkraðarfærslur.

### <a name="impact-of-order-editing"></a>Áhrif pöntunarbreytinga

Í Shopify:

|Breyta|Áhrif á Shopify pantanir sem ekki hafa verið unnar í [!INCLUDE[prod_short](../includes/prod_short.md)] | Áhrif á Shopify pantanir sem þegar eru unnar í [!INCLUDE[prod_short](../includes/prod_short.md)] |
|------|-----------|-----------|
|Breyta uppfyllingarstaðsetningu | Staðsetning uppfyllingar er samstillt við [!INCLUDE[prod_short](../includes/prod_short.md)]. | Staðsetning uppfyllingar er samstillt við [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Breyta pöntun og auka magn|Innflutt pöntun notar nýtt magn.| Connector finnur breytinguna og merkir pantanirnar. |
|Breyta pöntun og minnka magn|Innflutt pöntun notar nýtt magn. Shopify Endurgreiðsla með 0 upphæð verður flutt inn sem ekki er hægt að breyta í kreditreikning.| Connector finnur breytinguna og merkir pantanirnar. |
|Breyta pöntun og fjarlægja fyrirliggjandi vöru |Ekki verður flutt inn fjarlægð vara. Shopify Endurgreiðsla með 0 upphæð verður flutt inn sem ekki er hægt að breyta í kreditreikning.| Connector finnur breytinguna og merkir pantanirnar. |
|Breyta pöntun og bæta við nýjum hlut | Upprunalegar og viðbættar vörur verða fluttar inn. | Connector finnur breytinguna og merkir pantanirnar. |
|Vinnslupöntun: uppfylla, uppfæra greiðsluupplýsingar | Pöntunarhaus verður uppfærður. |Pöntunarhaus verður uppfærður. Fullyrðingin verður ekki samstillt við Shopify.|
|Hætta við greidda pöntun | Pantanahaus verður uppfærður, til að vinna sérstaklega |Connector finnur breytinguna og merkir pantanirnar. |
|Hætta við ógreidda pöntun | Ekki verður flutt inn fjarlægð vara. Shopify Endurgreiðsla með 0 upphæð verður flutt inn sem ekki er hægt að breyta í kreditreikning. |Connector finnur breytinguna og merkir pantanirnar. |

Ef pöntun var þegar unnin í [!INCLUDE[prod_short](../includes/prod_short.md)] birtir tengillinn eftirfarandi villuboð: *Pöntunin hefur þegar verið unnin í Business Central, en útgáfa barst frá Shopify. Breytingar voru ekki færðar á vinnslupöntunina í Business Central. Uppfæra unnin skjöl til samræmis við móttekin gögn. Shopify Ef þvinga á samstillinguna skal nota aðgerðina "Samstilla pöntun úr Shopify" á síðunni Shopify Pöntunarspjald.*

Hægt er að framkvæma eftirfarandi aðgerðir eftir stöðu stofnaðs söluskjals:

1. Eyða stofnuðu söluskjali
2. Veljið aðgerðina **Ótengd vinnsluskjöl** til að endurstilla **Vinnslu** vísirinn.
3.  **Velja skal samstillingarpöntun úr Shopify** aðgerð til að uppfæra einstaka pöntun með nýlegum gögnum. Shopify

Í [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Breyta|Áhrif|
|------|-----------|
|Staðsetningu er breytt í aðra birgðageymslu. Bóka afhendingu. | Pöntunin verður merkt sem uppfyllt. Staðsetning uppfyllingar Shopify verður notuð. |
|Minnka magn. Bóka afhendingu. | Shopify Pöntunin verður merkt sem uppfyllt að hluta. |
|Auka magn. Bóka afhendingu. | Fullyrðingin verður ekki samstillt við Shopify. Það er sama hvort uppfyllingunni var skipt í Shopify en unnin sem ein lína í [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Bæta við nýju atriði. Bóka afhendingu. | Shopify Pöntunin verður merkt sem uppfyllt. Ekki verður bætt við nýjum línum. |

## <a name="synchronize-shipments-to-shopify"></a>Samstilla sendingar við Shopify

Þegar sölupöntun sem stofnuð er úr Shopify pöntun send er hægt að samstilla sendingarnar við Shopify.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið slá inn **Samstilla sendingar við Shopify** og velja síðan viðkomandi tengil.
2. Skilgreina síur á sendingum eftir þörfum. Til dæmis er hægt að uppfæra sendingu sem er bókuð á tilteknum degi.
3. Velja **Í lagi**.

Pöntunin Shopify verður merkt sem uppfyllt. Viðskiptavinur fær sjálfkrafa tilkynningu um sendingu með tölvupósti eða textaskilaboðum (SMS). Ef afhendingaraðili og rakningarkóði eru tilgreindir í sendingunni eru rakningsupplýsingarnar innifaldar í tölvupóstinum.

Einnig er hægt að nota aðgerðina **Samstilla afhendingar** á síðunum Shopify Sölupantanir eða Shopify Verslunarsíður.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

> [!Important]
> Birgðageymsla, með auðri birgðageymslu, sem skilgreind er í Bókuð afhendingarlína verður að hafa samsvarandi færslu í birgðageymslunni Shopify . Að öðrum kosti verður þessi lína ekki send aftur til Shopify. Frekari upplýsingar er að finna á [Vörpun staðsetningar](synchronize-orders.md#location-mapping).

Munið að keyra **Samstilla pantanir frá Shopify** til að uppfæra uppfyllingarstöðu pöntunar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Tengivirknin geymir einnig skjalasafn að fullu greitt og uppfylltum pöntunum í báðum Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] að því gefnu að skilyrðum sé fullnægt. 

### <a name="shipping-agents-and-tracking-url"></a>Flutningsaðilar og rakningarvefslóð

Ef skjalið **Bókuð söluafhending** inniheldur **Flutningsaðilakóða** og/eða **Leitarnr. sendingar**, verða þessar upplýsingar sendar til Shopify og til viðskiptavinar í staðfestingarpósti sendingar.

Rakningarfyrirtækið er fyllt út í eftirfarandi röð (frá hæsta til lægsta) miðað við umboðsskrá flutningsaðila:

1. **ShopifyRakningarfyrirtæki**
1. **Heiti**
1. **Kóði**

Ef reiturinn **Rakningarvefslóð sendingar** er fylltur út fyrir skrá flutningsaðila mun staðfesting sendingar einnig innihalda rakningarvefslóð.

## <a name="returns-and-refunds"></a>Vöruskil og endurgreiðslur

Í samþættingu milli Shopify og er mikilvægt að geta samstillt eins mikil viðskiptagögn og [!INCLUDE[prod_short](../includes/prod_short.md)] mögulegt er. Þannig er auðveldara að halda fjárhags- og birgðastigum uppfærðum [!INCLUDE[prod_short](../includes/prod_short.md)]. Gögnin sem hægt er að samstilla fela í sér skil og endurgreiðslur sem voru skráðar í Shopify Stjórnandi eða Shopify Pos.

Vöruskil og endurgreiðslur eru fluttar inn með tengdum pöntunum ef vinnslutegundin á Shopify verkstæðisspjaldinu var gerð virk.

Vöruskil eru aðeins flutt inn í upplýsingaskyni. Enginn vinnslugrunnur er tengdur þeim.

Fjárhagslegar og, ef með þarf, eru birgðafærslur unnar með endurgreiðslum. Endurgreiðslur geta innihaldið vörur eða aðeins upphæðir– til dæmis ef söluaðili ákveður að bæta flutningsgjöldum eða einhverja aðra upphæð.

Hægt er að búa til sölukreditreikninga fyrir endurgreiðslur. Kreditreikningarnir geta haft eftirfarandi tegundir lína:

|Gerð|Nr.|Athugasemd|
|-|-|-|
|Fjárhagur|Seldur gjafakortsreikningur| Nota fyrir endurgreiðslur sem tengjast gjafakortum.|
|Fjárhagur|Reikningur endurgreiðslu sem er ekki á lager | Nota fyrir endurgreiðslur sem tengjast vörum sem ekki voru endurkastaðar. |
|Atriði |Vörunr.| Nota skal endurgreiðslur sem tengjast vörum sem voru endurkaupaðir. Gildir fyrir beina endurgreiðslu eða endurgreiðslur sem tengjast endurgreiðslum. Birgðageymslukótinn í kreditlínunni er stilltur á grundvelli gildsins sem valið var fyrir vöruskilastaðinn.|
|Fjárhagur| Endurgreiðslureikningur | Nota skal fyrir aðrar endurgreiddar upphæðir sem ekki tengjast vörum eða gjafakortum. Til dæmis ábendingar eða ef upphæð til endurgreiðslu var tilgreind handvirkt Shopify. |

> [!Note]
> Birgðageymslur vöruskila, þar á meðal auðar birgðageymslur, sem skilgreindar eru á **Shopify verkstæðisspjaldinu** eru notaðar á stofnaða kreditreikningnum. Kerfið hunsar upprunalegu birgðageymslurnar frá pöntunum eða afhendingum.

## <a name="gift-cards"></a>Gjafakort

Í Shopify versluninni er hægt að selja gjafakort sem hægt er að nota til að greiða fyrir raunverulegar vörur.

Þegar unnið er með gjafakort er mikilvægt að slá inn gildi í reitinn **Seldur gjafakortsreikningur** í glugganum **Shopify Verslunarkort**. Selda gjafakortið verður samstillt ásamt pöntunum í línu. Einnig verður flutt inn notað gjafakort með pöntuninni en nú sem færsla. Taktu eftir að gjafakortið lækkar ekki upphæðina sem á að reikningsfæra.

Til að yfirfara nýja birgðaspjaldið og notuð gjafakort skal velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). táknið og færa inn **Gjafakort** og velja síðan viðkomandi tengil.

## <a name="see-also"></a>Sjá einnig .

[Hafist handa Shopify með Connector](get-started.md)  
