---
title: Samræma og uppfylla sölupantanir
description: Setja upp og keyra innflutning og vinnslu sölupöntunar frá Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
---

# <a name="synchronize-and-fulfill-sales-orders"></a>Samræma og uppfylla sölupantanir

Þessi grein lýsir áskildum stillingum og skrefum sem þú verður að ljúka til að samstilla og uppfylla sölupantanir með Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Setja innflutning pantana á Shopify Verslunarkortið

 **Færið inn gjaldmiðilskóða**  ef vefverslunin notar annan gjaldmiðil en staðbundinn GJALDMIÐIL (ISK). Tilgreindur gjaldmiðill verður að hafa stillt gengi. Ef vefverslunin þín notar sama gjaldmiðil og [!INCLUDE[prod_short](../includes/prod_short.md)] skaltu skilja þennan reit eftir auðan. 

Hægt er að fá aðgang að gjaldmiðli verslunarinnar í  [upplýsingastillingum](https://www.shopify.com/admin/settings/general)  verslunarinnar í  Shopify  admin.  Shopify hægt að skilgreina til að samþykkja mismunandi gjaldmiðla, annars vegar innfluttar pantanir í  [!INCLUDE[prod_short](../includes/prod_short.md)]  notkun verslunargjaldmiðils.

Venjuleg Shopify pöntun getur falið í sér kostnað til viðbótar við millisamtöluna, svo sem sendingargjöld eða, ef slíkt er virkt, ábendingar. Þessar upphæðir eru settar beint á fjárhag sem þú vilt nota fyrir tilteknar tegundir færslna:

* **Reikningur sendingargjalda**
* **Seldur gjafakortsreikningur** frekari upplýsingar er að finna á [Gjafakort](synchronize-orders.md#gift-cards)
* **Þjórfésreikningur**  

Virkja sjálfvirkar **Stofna pantanir sjálfkrafa** til að búa til söluskjöl sjálfkrafa [!INCLUDE[prod_short](../includes/prod_short.md)] þegar Shopify pöntunin hefur verið flutt inn.

Ef gefa á söluskjal sjálfkrafa út skal kveikja á víxlun Söltunarinnar  **í**  sjálfvirka losun.

Söluskjalið í  [!INCLUDE[prod_short](../includes/prod_short.md)]  tenglum við  Shopify  pöntunina og þá er hægt að bæta við reit sem er ekki þegar birtur á síðunni. Frekari upplýsingar um að bæta við reit er farið í  [til að ræsa sérsníða síðu í gegnum  **fylgiritið**  Sérsníða](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner). Ef hakað er í  **Shopify  reitinn Pöntunarnr. í Doc. línu**  eru þessar upplýsingar endurteknar í sölulínur af gerðinni  **comment**.

 **Í reitnum Forgangur**  skattsvæðis er hægt að stilla forgang að því hvernig velja á skattsvæðiskóta á aðsetur í pöntun. Í innfluttu  Shopify  pöntuninni eru upplýsingar um skatta. Skattar eru endurreiknaðir þegar söluskjal er stofnað þannig að mikilvægt er að VSK-/skattstillingarnar séu réttar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Frekari upplýsingar um skatta er að finna í [Setja upp skatta Setja upp skatta fyrir Shopify tenginguna](setup-taxes.md).

Tilgreinið hvernig á að vinna skil og endurgreiðslur:

* **Auður**  Tilgreinir að ekki sé verið að flytja inn og vinna úr skilum og endurgreiðslum.
* **Innflutningur aðeins**  Tilgreinir að upplýsingar um innflutning eru fluttar inn en samsvarandi kreditreikningur er handvirkt stofnaður.
* **Sjálfvirk stofnun kreditreiknings**  Tilgreinir að flytja eigi inn upplýsingar og  [!INCLUDE[prod_short](../includes/prod_short.md)]  stofnar sjálfkrafa kreditreikningana. Þessi valkostur krefst þess að kveikt sé á  **skiptilínu**  sjálfstofnunar sölupöntunar.

Tilgreinið staðsetningu fyrir skil og fjárhagsreikninga til endurgreiðslu fyrir vörur og aðrar endurgreiðslur.

* **Endurgreiðslulykill non-endurbirgðavara**  -tilgreinir í reitnum Fjárhagsreikningur nr. fyrir vörur þar sem ekki á að hafa leiðréttingu á birgðum.
* **Endurgreiðslureikningur**  -Tilgreinir fjárhagsreikning fyrir mismuninn í heildarupphæð endurgreidda upphæðar og heildarupphæð varanna.

Frekari upplýsingar um  [skil og endurgreiðslur](synchronize-orders.md#returns-and-refunds)

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

Vörpun staðsetningar er nauðsynleg í þrenns konar tilgangi:

* Til að samstilla birgðir, til að fá frekari upplýsingar, sjá [Samstilla birgðir við Shopify](synchronize-items.md#sync-inventory-to-shopify)
* Til að fylla inn **Staðsetningarkóði** fyrir söluskjöl flutt inn úr Shopify. Þetta er mikilvægt þegar valkosturinn **Staðsetning áskilin** er virkjuð á **Uppsetning birgða**, annars geturðu ekki búið til söluskjöl.
* Til að uppfæra Shopify pöntunina með upplýsingum um uppfyllingu sem byggjast á síðunni **Bókuð söluafhending**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Veljið verslunina sem á að stilla vörpun staðsetnigna fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Staðsetningar** til að opna **Shopify Staðsetningar verslunar**.
4. Veldu aðgerðina **Sækja Shopify Staðsetningar** til að flytja inn allar staðsetningarnar sem skilgreindar eru í Shopify. Þú finnur þær í stillingunum [**Staðsetningar**](https://www.shopify.com/admin/settings/locations) í stjórnendamiðstöð **Shopify þínu**. Athugaðu að staðsetningin sem merkt er sem *Sjálfgefin* verður notuð þegar óuppfylltar Shopify pantanir eru fluttar inn.
5. Sláðu inn **Sjálfgefinn staðsetningarkóða** með samsvarandi staðsetningu í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="run-the-order-synchronization"></a>Keyra samstillingu pöntunar

Eftirfarandi ferli lýsir því hvernig eigi að flytja inn og uppfæra sölupantanir.

> [!NOTE]  
> Ekki er Shopify hægt að flytja inn safnvistaðar pantanir. Slökktu á valkostinum **Safnvista pöntunina sjálfkrafa** í hlutanum **Úrvinnsla pantana** í stillingum fyrir **Útskráningu** í glugganum **Shopify Stjórnandi** til að tryggja að allar pantanir séu fluttar inn til [!INCLUDE[prod_short](../includes/prod_short.md)]. Ef þú þarft að flytja inn safnvistaðar pantanir skaltu nota aðgerðina **Taka pantanir úr geymslu** á síðunni [Pantanir](https://www.shopify.com/admin/orders) í glugganum **ShopifyStjórnandi**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Velja verslun sem flytja á inn pantanir fyrir til að opna síðu **Shopify Verslunarkortsins**.
3. Veldu aðgerðina **Pantanir**.
4. Veldu aðgerðina **Samstilla pantanir frá Shopify**.
5. Skilgreina síur á pöntunum eftir þörfum. Til dæmis er hægt að flytja inn pantanir sem hafa verið greiddar að fullu eða þær sem eru með lágt áhættustig.

> [!NOTE]  
> Þegar sía eftir merki ætti að nota síutákn  `@`  og `*`. Til dæmis ef flytja á inn pantanir sem innihalda  *tag1*, nota `@*tag1*`. `@` vilja tryggja að niðurstaða sé mál óviðkvæm, en  `*`  finna pantanir með mörgum merkjum.

6. Velja hnappinn **Í lagi**.

Einnig er hægt að leita að runuvinnslunni **Samstilla pantanir frá Shopify**.

Hægt er að áætla verkið sem á að framkvæma sjálfkrafa. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

### <a name="under-the-hood"></a>Undir hetta

 Shopify Tengivirkið flytur pantanir í tveimur skrefum:

1.  Það flytur inn pöntunarhausa í  **Shopify  pantanirnar sem á að flytja inn**  þegar þær samsvara ákveðnum skilyrðum:
    
* Þeir eru ekki í geymslu.
* Þær voru stofnaðar eða þeim breytt eftir síðustu samstillingu.

2.  Hann flytur inn  Shopify  pantanir og viðbótarupplýsingar.
*  Shopify Tengitengið vinnur úr öllum færslum í  **Shopify  pöntunum í innflutningstöflu**  sem samsvara afmörkunarskilyrðaviðmiðinu sem tilgreint er á  **samstillingarpöntunum frá  Shopify**  beiðni. T.d. merki, rás eða uppfyltslustöðu. Ef engar afmarkanir hafa verið tilgreindar eru allar færslur í henni vinnur úr þeim.
* Við innflutning á shopify pöntun biður Connector um  Shopify  viðbótarupplýsingar frá Shopify:

    * Pöntunarhaus
    * Pöntunarlínur
    * Upplýsingar um sendingu og uppfylgun
    * Færslur
    * Skilagreinar og endurgreiðslur, ef samskipað

 **Shopify Pöntunin til að flytja inn**  síðu er gagnleg til að leysa innflutningsmál pöntunar. Hægt er að meta þær pantanir sem eru tiltækar og rífa næstu skref:

* Athugaðu hvort Villa útilokaði innflutning tiltekinnar pöntunar og Kannaðu nánar villur. Reiturinn Villa er í  **reitnum villuleitað** .
* Vinna aðeins tilteknar pantanir. Þú þarft að fylla út í reitinn verkstæðiskóti  **, velja eina eða fleiri pantanir og velja**  svo aðgerðina Flytja inn valdar pantanir  **.** 
* Eyða pöntunum úr  **Shopify  pöntuninni til að flytja inn**  síðu til að útiloka þær úr samkeyrslu.

## <a name="review-imported-orders"></a>Yfirfara innfluttar pantanir

Þegar innflutningi er lokið er hægt að kanna  Shopify  pöntunina og finna allar tengdar upplýsingar, svo sem greiðslufærslur, sendingarkostnað, hættustig, eigindir pöntunar og merki eða uppfyllum, ef pöntunin var þegar uppfyllt Shopify. Þú getur einnig séð allar staðfestingar pöntunar sem hefur verið send til viðskiptavinarins með því að velja aðgerðina **Shopify Stöðusíða**.

> [!NOTE]  
> Þú getur farið beint í gluggann **Shopify Pantanir** og þá birtast pantanir í stöðunni *opnar* í öllum verslunum. Til að fara yfir pantanir sem er lokið verður að opna síðuna**Shopify Pantanir** í sérstökum glugga **Shopify Verslunarkort**.

## <a name="create-sales-documents-in-business-central"></a>Stofna söluskjöl í Business Central

 **Ef Sjálfvirk pantanavíxla**  eru virkjuð á  **Shopify  verkstæðisspjaldinu** [!INCLUDE[prod_short](../includes/prod_short.md)]  er reynt að stofna söluskjal eftir að pöntunin hefur verið flutt inn. Ef vandamál koma upp eins og að viðskiptavin eða vöru vantar þarftu að laga vandamálin og búa svo til sölupöntunina aftur.

### <a name="to-create-sales-documents"></a>Til að búa til söluskjöl

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Velja verslun sem á að samstilla pantanir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Pantanir**.
4. Veljið röðina sem stofna á söluskjal fyrir og veljið aðgerðina **Búa til söluskjöl**.
5. Velja **Já**.

Ef Shopify pöntunin krefst uppfyllingar **er Sölupöntun** stofnuð. Fyrir uppfylltar Shopify pantanir, svo sem þær pantanir sem innihalda aðeins gjafakort eða eru þegar meðhöndlaðar í Shopify verslunum, verður stofnaður **Sölureikningur**.

Söluskjal er nú búið til og hægt er að stjórna því með því að nota hefðbundna [!INCLUDE[prod_short](../includes/prod_short.md)] virkni.

### <a name="manage-missing-customers"></a>Vinna með viðskiptavini sem vantar

Ef stillingarnar þínar koma í veg fyrir að viðskiptavinur sé stofnaður sjálfkrafa og réttur viðskiptavinur finnst ekki þarftu að úthluta viðskiptavini í Shopify pöntunina handvirkt. Nokkrar leiðir eru til að gera þetta:

* Þú getur úthlutað **Selt-til viðskm.nr.** og **Reikn. færist á viðskm.** beint á síðunni **Shopify Pantanir** með því að velja viðskiptavin af listanum yfir núverandi viðskiptavini.
* Hægt er að velja sniðmátskóða fyrir viðskiptavini, búa síðan til og úthluta viðskiptavini í gegnum aðgerðina **Búa til nýjan viðskiptavin** á síðunni **Shopify Pantanir**. Taktu eftir að Shopify viðskiptamaðurinn verður að vera með minnst eitt aðsetur. Oft eru upplýsingar um aðsetursskipanir stofnaðar með  Shopify  sölurásum sölustaða.
* Þú getur varpað núverandi viðskiptavin við tengdan **Shopify Viðskiptavin** í glugganum **Shopify Viðskiptavinir** og valið síðan aðgerðina **Leita að vörpun** á síðunni **Shopify Pantanir**.

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Hvernig tengillinn velur hvaða viðskiptavin á að nota

Aðgerðin *Flytja inn pöntun frá Shopify* reynir að velja viðskiptavini í eftirfarandi röð:

1. Ef **Sjálfgefið númer viðskiptavinar.** Er skilgreindur í  **Shopify  Viðskiptavinarsniðmátinu**  fyrir  **Sendist-til lands-/svæðiskótann, þá** sjálfgefna viðskiptavinarnúmer  **.** er notað óháð stillingum reitanna **Innflutningur viðskiptavinar frá Shopify** og **Vörpunargerð viðskiptavinar**. Frekari upplýsingar um  [sniðmát viðskiptavinar fyrir hvert land](synchronize-customers.md#customer-template-per-countryregion).
2. Ef valkosturinn **Innflutningur viðskiptavinar frá Shopify** er stilltur á *Ekkert* og **Sjálfgefið nr. viðskiptavinar.** er skilgreint á síðunni **Shopify Verslunarkort** þá er **Sjálfgefið nr. viðskiptavinar.** er notað.

Næstu skref fara eftir **Tegund vörpunar viðskiptavinar**.

* Ef það er **Alltaf taka sjálfgefna viðskiptavininn**, þá notar tengillinn viðskiptavininn sem er skilgreindur í **Sjálfgefið nr. viðskiptavinar**. reitinn á síðunni **Shopify Verslunarkort**.
* Ef það er með **Eftir netfangi/síma** reynir tengillinn að finna núverandi viðskiptavin fyrst eftir skilríkjum, síðan eftir netfangi og að síðustu eftir símanúmeri. Ef viðskiptavinurinn finnst ekki stofnar tengillinn nýjan viðskiptavin.
* Ef það er **Eftir upplýsingum um „reikningsfæra á“** reynir tengillinn að finna fyrst þann viðskiptavin sem er til staðar með skilríkjum og síðan með upplýsingum um heimilisfang. Ef viðskiptavinurinn finnst ekki stofnar tengillinn nýjan viðskiptavin.

> [!NOTE]  
> Tengillinn notar upplýsingar frá heimilisfanginu sem reikningsfært er á og býr til viðskiptamanninn sem reikningsfært er á í [!INCLUDE[prod_short](../includes/prod_short.md)]. Selt-til - Viðskiptavinur er sami viðskiptavinur og reikningsfært er á.

### <a name="different-processing-rules-for-orders"></a>Mismunandi vinnslureglur fyrir pantanir

Þú gætir viljað vinna pantanir á annan hátt samkvæmt reglu. Til dæmis ættu pantanir frá tiltekinni sölurás, eins og POS, að nota sjálfgefinn viðskiptavin en óskað er eftir að vefverslunin hafi raunverulegar upplýsingar um viðskiptavininn.

Ein leið til að takast á þessi krafa er að búa til viðbótar  Shopify  vinnuspjald og nota síur í  **Samkeyrslupantanunum frá  Shopify**  beiðssíðu.

Dæmi: þú ert með netverslun sem  Shopify  og sölustaði. Fyrir SÖLUSTAÐINA er æskilegt að nota fasta viðskiptavini en fyrir netverslun er ætlunin að stofna viðskiptavini í [!INCLUDE[prod_short](../includes/prod_short.md)]. Hér á eftir er stigið háskref í þessu ferli. Til að fá frekari upplýsingar er farið í samsvarandi hjálpargreinar.

1. Búðu til búð sem  Shopify  heitir  *Store*  og tengir hana við þinn  Shopify  reikning.
2. Samskipa samstillingu vöru/afurðar þannig að þessi verslun hafi umsjón með upplýsingum um afurð.
3. Tilgreinið að Viðskiptavinir séu fluttir inn með pöntunum. Tengivirkið ætti að finna viðskiptavini með því að leita að netfangi þeirra. Ef hann finnur ekki aðsetur notar það viðskiptamannssniðmát til að stofna nýjan viðskiptavin.
4.  Shopify Stofna verkstæði sem heitir  *POS*  og tengja það við sama  Shopify  lykil.
6. Ganga þarf úr skugga um að samstilling vara/afurða sé óvirk.
7. Velja skal tengibúnað sem notar sjálfgefinn viðskiptavin.
8. Stofna færslu endurtekinnar vinnslu fyrir verk í skýrslu 30104  **Samstilla pantanir úr Shopify**. Valið  **er að geyma**  í  **Shopify  reitnum verkstæðiskóti**  og nota afmarkanir til að grípa allar pantanir nema þær sem sölurásin í sölurás býr til. Sem dæmi má  **nefna að < > sölustað**
9. Stofna færslu endurtekinnar vinnslu fyrir skýrsluna 30104  **Samstilla pantanir frá Shopify**. Velja  **skal sölustaði**  í  **Shopify  reitnum verkstæðiskóti**  og nota afmarkanir til að grípa til pantana sem myndaðar eru af söluleið sölustaðar.  **T.d. bent á sölu**.

Hver vinnsluröð mun flytja inn og vinna úr pöntunum innan skilgreinds afmörkunar og nota reglurnar af viðkomandi  Shopify  vinnuspjaldi. Til dæmis eru þeir stofnaðir sem benda á sölupantanir fyrir sjálfgefinn viðskiptavin.

>! Mikilvægt Til að forðast árekstra við vinnslu pantana þarf að muna að nota sama vinnsluraðarflokk fyrir báðar vinnsluraðarfærslur.

### <a name="impact-of-order-editing"></a>Áhrif pöntunarbreytinga

Í Shopify:

|Breyta|Áhrif fyrir pöntun sem þegar er flutt inn|Áhrif til þess að panta sem fær innflutta í fyrsta sinn|
|------|-----------|-----------|
|Breyta uppfyllingarstaðsetningu | Upprunaleg staðsetning er í línum | Staðsetning uppfyllingar er samsýnd [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Breyta pöntun og auka magn| Pöntunarhaus og fylgitöflur verða uppfærðar í  [!INCLUDE[prod_short](../includes/prod_short.md)], línur verða ekki.| Innflutt pöntun mun nota nýtt magn|
|Breyta pöntun og minnka magn| Pöntunarhaus og fylgitöflur verða uppfærðar í  [!INCLUDE[prod_short](../includes/prod_short.md)], línur verða ekki.| Ef innflutt pöntun mun nota upprunalegt magn mun svæðið Uppfyllegt magn innihalda nýtt gildi.|
|Breyta pöntun og fjarlægja fyrirliggjandi vöru | Pöntunarhaus og fylgitöflur verða uppfærðar í  [!INCLUDE[prod_short](../includes/prod_short.md)], línur verða ekki.| Fjarlægð vöru verður enn flutt inn, svæðið í Uppfylanlegu magni mun innihalda núll. |
|Breyta pöntun og bæta við nýjum hlut | Haus pöntunar verður uppfærður, línur breytast ekki. | Upprunaleg og bætt vara verður flutt inn. |
|Vinna pöntun: uppfylla, uppfæra greiðsluupplýsingar | Pöntunarhaus verður uppfærður en línurnar ekki. |Breyting hefur engin áhrif á það hvernig pöntunin er flutt inn.|
|Hætta við pöntun | Pöntunarhaus verður uppfærður en línurnar ekki. |Afturkölluð pöntun er ekki flutt inn |

Í [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Breyta|Áhrif|
|------|-----------|
|Breyta staðsetningu í aðra staðsetningu, varpað yfir í Shopify staðsetningar. Bóka afhendingu. | Pöntun verður merkt sem fuflilli. Upprunaleg staðsetning verður notuð. |
|Breyta staðsetningu í aðra staðsetningu, ekki varpaða í Shopify staðsetningar. Bóka afhendingu. | Fullyrðingin verður ekki samstillt við Shopify. |
|Minnka magn. Bóka afhendingu. | Shopify Pöntunin verður merkt sem uppfyllt að hluta. |
|Auka magn. Bóka afhendingu. | Fullyrðingin verður ekki samstillt við Shopify. |
|Bæta við nýju atriði. Bóka afhendingu. | Shopify Pöntunin verður merkt sem uppfyllt. Línur verða ekki uppfærðar. |

## <a name="synchronize-shipments-to-shopify"></a>Samstilla sendingar við Shopify

Þegar sölupöntun sem stofnuð er úr Shopify pöntun send er hægt að samstilla sendingarnar við Shopify.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið slá inn **Samstilla sendingar við Shopify** og velja síðan viðkomandi tengil.
2. Skilgreina síur á sendingum eftir þörfum. Til dæmis er hægt að uppfæra sendingu sem er bókuð á tilteknum degi.
3. Velja hnappinn **Í lagi**.

Pöntunin Shopify verður merkt sem uppfyllt. Viðskiptavinur fær sjálfkrafa tilkynningu um sendingu með tölvupósti eða textaskilaboðum (SMS). Ef afhendingaraðili og rakningarkóði eru tilgreindir í sendingunni eru rakningsupplýsingarnar innifaldar í tölvupóstinum.

Einnig er hægt að nota aðgerðina **Samstilla afhendingar** á síðunum Shopify Sölupantanir eða Shopify Verslunarsíður.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

>[!Important]
>Staðsetningin, þar á meðal auður Birgðageymsla, sem er skilgreind í bókuðu afhendingarlínunni verður að hafa samsvarandi færslu í  Shopify  birgðageymslunni. Að öðrum kosti verður þessi lína ekki send aftur til Shopify. Frekari upplýsingar er að finna á [Vörpun staðsetningar](synchronize-orders.md#location-mapping).

Munið að keyra **Samstilla pantanir frá Shopify** til að uppfæra uppfyllingarstöðu pöntunar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Virkni tengilsins safnvistar einnig að fullu greiddar og uppfylltar pantanir bæði í Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] að því gefnu að skilyrðin séu uppfyllt.

### <a name="shipping-agents-and-tracking-url"></a>Flutningsaðilar og rakningarvefslóð

Ef skjalið **Bókuð söluafhending** inniheldur **Flutningsaðilakóða** og/eða **Leitarnr. sendingar**, verða þessar upplýsingar sendar til Shopify og til viðskiptavinar í staðfestingarpósti sendingar.

Rakningarfyrirtækið er fyllt út í eftirfarandi röð (frá hæsta til lægsta) miðað við umboðsskrá flutningsaðila:

* **ShopifyRakningarfyrirtæki**
* **Heiti**
* **Kóði**

Ef reiturinn **Rakningarvefslóð sendingar** er fylltur út fyrir skrá flutningsaðila mun staðfesting sendingar einnig innihalda rakningarvefslóð.

## <a name="returns-and-refunds"></a>Skilagreinar og endurgreiðsla

Í samþættingu á milli  Shopify  og  [!INCLUDE[prod_short](../includes/prod_short.md)] er því mikilvægt að geta samstillt eins mikið af viðskipagögnum og mögulegt er. Auðveldara er að halda fjármálum og birgðastikunni í [!INCLUDE[prod_short](../includes/prod_short.md)]... Gögnin sem þú getur samstillt eru skil og endurgreiðslur sem voru skráðar í  Shopify  admin eða  Shopify  POS.

Skilagreinar og endurgreiðslur eru fluttar inn með tengdum pöntunum þeirra ef vinnslugerðin er virkjuð á  Shopify  Verkstæðisspjaldinu.

Skilagreinar eru eingöngu fluttar inn til upplýsinga. Engin vinnsluröksemd er í tengslum við þau.

Fjárhagsleg og, ef þörf krefur, birgðafærslur eru unnar í gegnum endurgreiðslur. Endurgreiðsla getur innihaldið vörur eða bara upphæðir, til dæmis ef seljandi hefur ákveðið að bæta aðflutningsgjöld eða einhverja aðra upphæð við.
Hægt er að stofna sölukreditreikninga fyrir endurgreiðslur. Kreditreikningar geta haft eftirfarandi línur:

|Gerð|Nr.|Athugasemd|
|-|-|-|
|Fjárhagur|Seldur gjafakortsreikningur| Nota fyrir endurgreiðslur sem tengjast gjafakortum.|
|Fjárhagur|Endurgreiðslureikningur ekki Hlutabréfakaup | Nota fyrir endurgreiðslur tengdar afurðum sem ekki voru endurverðbréfaðar. |
|Atriði |Vörunr.| Nota fyrir endurgreiðslur tengdar afurðum sem voru endurverðbréfaðar. Gildir um beinar endurgreiðslur eða endurgreiðslur sem tengjast endurgreiðslum. Birgðageymslukótinn fyrir kreditlínu er stilltur á grundvelli gildis sem er valið fyrir skilastaðinn.|
|Fjárhagur| Endurgreiðslureikningur | Notið fyrir aðrar endurgreiddar upphæðir sem ekki eru tengdar vörum eða gjafakortum. Til dæmis ábendingar eða ef tiltekin upphæð er handvirkt endurgreidd Shopify. |

>[!Note]
>Skilastaðsetningin, þar á meðal auðir staðir, skilgreindir í  **Shopify  verkstæðisspjaldinu**  á stofnaða kreditreikningnum. Kerfið hunsar upprunalegar staðsetningar frá pöntunum eða sendingum.

## <a name="gift-cards"></a>Gjafakort

Í Shopify versluninni er hægt að selja gjafakort sem hægt er að nota til að greiða fyrir raunverulegar vörur.

Þegar unnið er með gjafakort er mikilvægt að slá inn gildi í reitinn **Seldur gjafakortsreikningur** í glugganum **Shopify Verslunarkort**. Selda gjafakortið verður samstillt ásamt pöntunum í línu. Einnig verður flutt inn notað gjafakort með pöntuninni en nú sem færsla. Taktu eftir að gjafakortið lækkar ekki upphæðina sem á að reikningsfæra.

Til að yfirfara nýja birgðaspjaldið og notuð gjafakort skal velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). táknið og færa inn **Gjafakort** og velja síðan viðkomandi tengil.

## <a name="see-also"></a>Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
