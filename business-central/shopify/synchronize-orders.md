---
title: Samræma og uppfylla sölupantanir
description: Setja upp og keyra innflutning og vinnslu sölupöntunar frá Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Samræma og uppfylla sölupantanir

Þessi grein lýsir áskildum stillingum og skrefum sem þú verður að ljúka til að samstilla og uppfylla sölupantanir með Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)].

## Setja innflutning pantana á Shopify Verslunarkortið

 **Færið inn gjaldmiðilskóða**  ef vefverslunin notar annan gjaldmiðil en staðbundinn GJALDMIÐIL (ISK). Tilgreindur gjaldmiðill verður að hafa stillt gengi. Ef vefverslunin þín notar sama gjaldmiðil og [!INCLUDE[prod_short](../includes/prod_short.md)] skaltu skilja þennan reit eftir auðan. 

Hægt er að sjá Store-gjaldmiðil í  [upplýsingastillingum](https://www.shopify.com/admin/settings/general)  verslunarinnar í  Shopify  admin. Shopify  hægt að skilgreina til að samþykkja mismunandi gjaldmiðla, annars vegar innfluttar pantanir í  [!INCLUDE[prod_short](../includes/prod_short.md)]  notkun verslunargjaldmiðils.

Venjuleg Shopify pöntun getur falið í sér kostnað til viðbótar við millisamtöluna, svo sem sendingargjöld eða, ef slíkt er virkt, ábendingar. Þessar upphæðir eru settar beint á fjárhag sem þú vilt nota fyrir tilteknar tegundir færslna:

* **Reikningur sendingargjalda**
* **Seldur gjafakortsreikningur** frekari upplýsingar er að finna á [Gjafakort](synchronize-orders.md#gift-cards)
* **Þjórfésreikningur**  

Virkja sjálfvirkar **Stofna pantanir sjálfkrafa** til að búa til söluskjöl sjálfkrafa [!INCLUDE[prod_short](../includes/prod_short.md)] þegar Shopify pöntunin hefur verið flutt inn.

Söluskjalið í [!INCLUDE[prod_short](../includes/prod_short.md)] inniheldur tengil á Shopify pöntunina. Ef valið er reiturinn **Shopify Pöntunarnr. í skjalalínu**, þessar upplýsingar eru endurteknar í sölulínum af gerðinni *Athugasemd*.

Í reitnum **Uppruni skattsvæðis** er hægt að setja forgang um hvernig velja á skattsvæðiskóða eða VSK-viðskiptabókunarflokk miðað við heimilisfang. Innflutt Shopify pöntun inniheldur upplýsingar um skatta en skattarnir eru endurreiknaðir þegar söluskjalið er stofnað og því er mikilvægt að stillingar VSK/skatta séu réttar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Frekari upplýsingar um skatta er að finna í [Setja upp skatta Setja upp skatta fyrir Shopify tenginguna](setup-taxes.md).

### Vörpun afhendingarmáta

**Kóða afhendingarmáta** fyrir söluskjöl innflutt frá Shopify er hægt að fylla út sjálfkrafa. Þú þarft að skilgreina **Vörpun afhendingarmáta**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Veljið þá verslun sem á að skilgreina vörpun fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Vörpun afhendingarmáta**. Þetta býr sjálfkrafa til skrár fyrir sendingarmáta sem skilgreindir eru í stillingum [**Sendingar**](https://www.shopify.com/admin/settings/payments) í **Shopify stjórnandamiðstöðinni**.
4. Í reitnum **Heiti** er hægt að sjá heiti sendingarmáta frá Shopify.
5. Sláðu inn **Kóða sendingarmáta** ásamt samsvarandi sendingarmáta í [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Ef mörg flutningsgjöld eru tengd við sölupöntun verður aðeins eitt valið og úthlutað á söluskjalið.

### Vörpun staðsetningar

Vörpun staðsetningar er nauðsynleg í þrenns konar tilgangi:

* Til að samstilla birgðir, til að fá frekari upplýsingar, sjá [Samstilla birgðir við Shopify](synchronize-items.md#sync-inventory-to-shopify)
* Til að fylla inn **Staðsetningarkóði** fyrir söluskjöl flutt inn úr Shopify. Þetta er mikilvægt þegar valkosturinn **Staðsetning áskilin** er virkjuð á **Uppsetning birgða**, annars geturðu ekki búið til söluskjöl.
* Til að uppfæra Shopify pöntunina með upplýsingum um uppfyllingu sem byggjast á síðunni **Bókuð söluafhending**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Veljið verslunina sem á að stilla vörpun staðsetnigna fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Staðsetningar** til að opna **Shopify Staðsetningar verslunar**.
4. Veldu aðgerðina **Sækja Shopify Staðsetningar** til að flytja inn allar staðsetningarnar sem skilgreindar eru í Shopify. Þú finnur þær í stillingunum [**Staðsetningar**](https://www.shopify.com/admin/settings/locations) í stjórnendamiðstöð **Shopify þínu**. Athugaðu að staðsetningin sem merkt er sem *Sjálfgefin* verður notuð þegar óuppfylltar Shopify pantanir eru fluttar inn.
5. Sláðu inn **Sjálfgefinn staðsetningarkóða** með samsvarandi staðsetningu í [!INCLUDE[prod_short](../includes/prod_short.md)].

## Keyra samstillingu pöntunar

Eftirfarandi ferli lýsir því hvernig eigi að flytja inn og uppfæra sölupantanir.

> [!NOTE]  
> Ekki er Shopify hægt að flytja inn safnvistaðar pantanir. Slökktu á valkostinum **Safnvista pöntunina sjálfkrafa** í hlutanum **Úrvinnsla pantana** í stillingum fyrir **Útskráningu** í glugganum **Shopify Stjórnandi** til að tryggja að allar pantanir séu fluttar inn til [!INCLUDE[prod_short](../includes/prod_short.md)]. Ef þú þarft að flytja inn safnvistaðar pantanir skaltu nota aðgerðina **Taka pantanir úr geymslu** á síðunni [Pantanir](https://www.shopify.com/admin/orders) í glugganum **ShopifyStjórnandi**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Velja verslun sem flytja á inn pantanir fyrir til að opna síðu **Shopify Verslunarkortsins**.
3. Veldu aðgerðina **Pantanir**.
4. Veldu aðgerðina **Samstilla pantanir frá Shopify**.
5. Skilgreina síur á pöntunum eftir þörfum. Til dæmis er hægt að flytja inn pantanir sem hafa verið greiddar að fullu eða þær sem eru með lágt áhættustig.

> [!NOTE]  
> Þegar sía eftir merki ætti að nota síutákn  `@`  og `*`. Til dæmis ef flytja á inn pantanir sem innihalda  *tag1*, nota `@*tag1*`. `@` vilja tryggja að niðurstaða sé viðurkennd, en  `*`  finna má pantanir með mörgum merkjum.

7. Velja hnappinn **Í lagi**.

Einnig er hægt að leita að runuvinnslunni **Samstilla pantanir frá Shopify**.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

## Yfirfara innfluttar pantanir

Þegar innflutningi er lokið er hægt að kanna  Shopify  pöntunina og finna allar tengdar upplýsingar, svo sem greiðslufærslur, sendingarkostnað, hættustig, eigindir pöntunar og merki eða uppfyllum, ef pöntunin var þegar uppfyllt Shopify. Þú getur einnig séð allar staðfestingar pöntunar sem hefur verið send til viðskiptavinarins með því að velja aðgerðina **Shopify Stöðusíða**.

> [!NOTE]  
> Þú getur farið beint í gluggann **Shopify Pantanir** og þá birtast pantanir í stöðunni *opnar* í öllum verslunum. Til að fara yfir pantanir sem er lokið verður að opna síðuna**Shopify Pantanir** í sérstökum glugga **Shopify Verslunarkort**.

## Stofna söluskjöl í Business Central

Ef valkosturinn **Stofna pantanir sjálfkrafa** er virkur á **Shopify Verslunarkortinu**, [!INCLUDE[prod_short](../includes/prod_short.md)]reynir það að búa til söluskjal þegar pöntunin hefur verið flutt inn. Ef vandamál koma upp eins og að viðskiptavin eða vöru vantar þarftu að laga vandamálin og búa svo til sölupöntunina aftur.

### Til að búa til söluskjöl

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Shopify Verslanir** og velja síðan viðkomandi tengil.
2. Velja verslun sem á að samstilla pantanir fyrir til að opna síðuna **Shopify Verslunarkort**.
3. Veldu aðgerðina **Pantanir**.
4. Veljið röðina sem stofna á söluskjal fyrir og veljið aðgerðina **Búa til söluskjöl**.
5. Velja **Já**.

Ef Shopify pöntunin krefst uppfyllingar **er Sölupöntun** stofnuð. Fyrir uppfylltar Shopify pantanir, svo sem þær pantanir sem innihalda aðeins gjafakort eða eru þegar meðhöndlaðar í Shopify verslunum, verður stofnaður **Sölureikningur**.

Söluskjal er nú búið til og hægt er að stjórna því með því að nota hefðbundna [!INCLUDE[prod_short](../includes/prod_short.md)] virkni.

### Vinna með viðskiptavini sem vantar

Ef stillingarnar þínar koma í veg fyrir að viðskiptavinur sé stofnaður sjálfkrafa og réttur viðskiptavinur finnst ekki þarftu að úthluta viðskiptavini í Shopify pöntunina handvirkt. Nokkrar leiðir eru til að gera þetta:

* Þú getur úthlutað **Selt-til viðskm.nr.** og **Reikn. færist á viðskm.** beint á síðunni **Shopify Pantanir** með því að velja viðskiptavin af listanum yfir núverandi viðskiptavini.
* Hægt er að velja sniðmátskóða fyrir viðskiptavini, búa síðan til og úthluta viðskiptavini í gegnum aðgerðina **Búa til nýjan viðskiptavin** á síðunni **Shopify Pantanir**. Taktu eftir að Shopify viðskiptamaðurinn verður að vera með minnst eitt aðsetur. Oft eru upplýsingar um aðsetursskipanir stofnaðar með  Shopify  sölurásum sölustaða.
* Þú getur varpað núverandi viðskiptavin við tengdan **Shopify Viðskiptavin** í glugganum **Shopify Viðskiptavinir** og valið síðan aðgerðina **Leita að vörpun** á síðunni **Shopify Pantanir**.

### Hvernig tengillinn velur hvaða viðskiptavin á að nota

Aðgerðin *Flytja inn pöntun frá Shopify* reynir að velja viðskiptavini í eftirfarandi röð:

1. Ef **Sjálfgefið númer viðskiptavinar.** reiturinn er skilgreindur í **Shopify Sniðmát viðskiptavinar** fyrir samsvarandi land og svo **Sjálfgefið nr. viðskiptavinar.** er notað óháð stillingum reitanna **Innflutningur viðskiptavinar frá Shopify** og **Vörpunargerð viðskiptavinar**. Frekari upplýsingar eru á [Sniðmát viðskiptavinar eftir landi](synchronize-customers.md#customer-template-per-country).
2. Ef valkosturinn **Innflutningur viðskiptavinar frá Shopify** er stilltur á *Ekkert* og **Sjálfgefið nr. viðskiptavinar.** er skilgreint á síðunni **Shopify Verslunarkort** þá er **Sjálfgefið nr. viðskiptavinar.** er notað.

Næstu skref fara eftir **Tegund vörpunar viðskiptavinar**.

* Ef það er **Alltaf taka sjálfgefna viðskiptavininn**, þá notar tengillinn viðskiptavininn sem er skilgreindur í **Sjálfgefið nr. viðskiptavinar**. reitinn á síðunni **Shopify Verslunarkort**.
* Ef það er með **Eftir netfangi/síma** reynir tengillinn að finna núverandi viðskiptavin fyrst eftir skilríkjum, síðan eftir netfangi og að síðustu eftir símanúmeri. Ef viðskiptavinurinn finnst ekki stofnar tengillinn nýjan viðskiptavin.
* Ef það er **Eftir upplýsingum um „reikningsfæra á“** reynir tengillinn að finna fyrst þann viðskiptavin sem er til staðar með skilríkjum og síðan með upplýsingum um heimilisfang. Ef viðskiptavinurinn finnst ekki stofnar tengillinn nýjan viðskiptavin.

> [!NOTE]  
> Tengillinn notar upplýsingar frá heimilisfanginu sem reikningsfært er á og býr til viðskiptamanninn sem reikningsfært er á í [!INCLUDE[prod_short](../includes/prod_short.md)]. Selt-til - Viðskiptavinur er sami viðskiptavinur og reikningsfært er á.

### Áhrif pöntunarbreytinga

Í Shopify:

|Breyta|Áhrif|
|------|-----------|
|Breyta uppfyllingarstaðsetningu | Upphafleg staðsetning verður samstillt við [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Breyta uppfyllingu staðsetningar og skrá uppfyllingu í Shopify| Ef pöntun var þegar flutt inn verða línurnar ekki uppfærðar. Annars mun innflutt pöntun nota Uppfyllingarstaðsetningu. |
|Breyta pöntun og breyta magni| Haus pöntunar og viðbótartöflur verða uppfærðar í [!INCLUDE[prod_short](../includes/prod_short.md)], línur breytast ekki. |
|Breyta pöntun og bæta við nýjum hlut | Haus pöntunar verður uppfærður, línur breytast ekki. |

Í [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Breyta|Áhrif|
|------|-----------|
|Breyta staðsetningu í aðra staðsetningu, varpað yfir í Shopify staðsetningar. Bóka afhendingu. | Eftir að búið er að samstilla uppfyllinguna verður staðsetningin uppfærð í Shopify. |
|Breyta staðsetningu í aðra staðsetningu, ekki varpaða í Shopify staðsetningar. Bóka afhendingu. | Fullyrðingin verður ekki samstillt við Shopify. |
|Breyta eða minnka magn. Bóka afhendingu. | Shopify Pöntunin verður merkt sem uppfyllt að hluta. |
|Bæta við nýju atriði. Bóka afhendingu. | Shopify Pöntunin verður merkt sem uppfyllt. Línur verða ekki uppfærðar. |

## Samstilla sendingar við Shopify

Þegar sölupöntun sem stofnuð er úr Shopify pöntun send er hægt að samstilla sendingarnar við Shopify.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið slá inn **Samstilla sendingar við Shopify** og velja síðan viðkomandi tengil.
2. Skilgreina síur á sendingum eftir þörfum. Til dæmis er hægt að uppfæra sendingu sem er bókuð á tilteknum degi.
3. Velja hnappinn **Í lagi**.

Pöntunin Shopify verður merkt sem uppfyllt. Viðskiptavinur fær sjálfkrafa tilkynningu um sendingu með tölvupósti eða textaskilaboðum (SMS). Ef afhendingaraðili og rakningarkóði eru tilgreindir í sendingunni eru rakningsupplýsingarnar innifaldar í tölvupóstinum.

Einnig er hægt að nota aðgerðina **Samstilla afhendingar** á síðunum Shopify Sölupantanir eða Shopify Verslunarsíður.

Þú getur skipulagt verkið sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar er að finna á [Tímasetja endurtekin verk](background.md#to-schedule-recurring-tasks).

>[Mikilvægt] Staðsetningin, þar á meðal auða staðsetningin, sem skilgreind er í Bókaðri afhendingarlínu, verður að hafa samsvarandi færslu í Shopify staðsetningunni. Að öðrum kosti verður þessi lína ekki send aftur til Shopify. Frekari upplýsingar er að finna á [Vörpun staðsetningar](synchronize-orders.md#location-mapping).

Munið að keyra **Samstilla pantanir frá Shopify** til að uppfæra uppfyllingarstöðu pöntunar í [!INCLUDE[prod_short](../includes/prod_short.md)]. Virkni tengilsins safnvistar einnig að fullu greiddar og uppfylltar pantanir bæði í Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] að því gefnu að skilyrðin séu uppfyllt.

### Flutningsaðilar og rakningarvefslóð

Ef skjalið **Bókuð söluafhending** inniheldur **Flutningsaðilakóða** og/eða **Leitarnr. sendingar**, verða þessar upplýsingar sendar til Shopify og til viðskiptavinar í staðfestingarpósti sendingar.

Rakningarfyrirtækið er fyllt út í eftirfarandi röð (frá hæsta til lægsta) miðað við umboðsskrá flutningsaðila:

* **ShopifyRakningarfyrirtæki**
* **Heiti**
* **Kóði**

Ef reiturinn **Rakningarvefslóð sendingar** er fylltur út fyrir skrá flutningsaðila mun staðfesting sendingar einnig innihalda rakningarvefslóð.

## Gjafakort

Í Shopify versluninni er hægt að selja gjafakort sem hægt er að nota til að greiða fyrir raunverulegar vörur.

Þegar unnið er með gjafakort er mikilvægt að slá inn gildi í reitinn **Seldur gjafakortsreikningur** í glugganum **Shopify Verslunarkort**. Selda gjafakortið verður samstillt ásamt pöntunum í línu. Einnig verður flutt inn notað gjafakort með pöntuninni en nú sem færsla. Taktu eftir að gjafakortið lækkar ekki upphæðina sem á að reikningsfæra.

Til að yfirfara nýja birgðaspjaldið og notuð gjafakort skal velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). táknið og færa inn **Gjafakort** og velja síðan viðkomandi tengil.

## Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
