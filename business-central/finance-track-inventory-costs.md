---
title: Rekja kostnaðarleiðréttingar vöru
description: Fræðast um hvernig rakningarleiðréttingar á vörukostnaði geta hjálpað til við að halda vörukostnaðargögnum réttum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="track-item-cost-adjustments"></a>Rekja kostnaðarleiðréttingar vöru

Brýnt er að halda vörukostnaði nákvæmum og stytta tímann milli þess þegar færsla er bókuð og þegar fjárhagur endurspeglar kostnað hennar. Hægt er að rekja afköst kostnaðarleiðréttinga vegna einstakra leiðréttingarkeyrslna og vara. Ef villur koma upp er hægt að bera kennsl á erfið atriði og gera leiðréttingar. Til dæmis er hægt að útiloka vörurnar frá útreikningum til að tryggja að leiðréttingar séu ekki rofnar vegna annarra vara. Hægt er að leiðrétta kostnað vegna einstakra vara eða stofna vörukeyrslur og leiðrétta þær allar samtímis.

## <a name="start-tracking-cost-adjustments"></a>Hefja rakningu kostnaðarleiðréttinga

Það er auðvelt að byrja. Á síðunni **Birgðagrunnur**  **býður reiturinn** Skráning kostnaðarleiðréttingar nokkra valkosti:

* **Óvirkt** merkir að kostnaðarleiðréttingarkeyrsla er ekki skráð.
* **Villur merkir aðeins** að skrá aðeins keyrslur sem mistókst.
* **Allt** þýðir að skrá allar keyrslur.

> [!NOTE]
> Til að draga úr stærð kladda [!INCLUDE [prod_short](includes/prod_short.md)]  er ekki skráðar breytingar sem gerast sjálfkrafa þegar vara er bókuð.

Einnig verður að setja upp verkraðarfærsluna **Bóka birgðabreytingar (1002).** . Þessi verkraðarfærsla leiðréttir sjálfkrafa kostnað samkvæmt áætlun. Nánari upplýsingar um verkraðarfærslur eru í [Nota verkröð til að tímasetja verk](admin-job-queues-schedule-tasks.md).

## <a name="manage-cost-adjustments"></a>Vinna með kostnaðarleiðréttingar

 **Síðan Leiðrétting birgðakostnaðar** er notuð til að stjórna og fylgjast með kostnaðarleiðréttingarferlinu. Þessi síða birtir vörur ásamt færibreytum kostnaðarútreiknings og stöðu kostnaðarleiðréttingar. Hægt er að afmarka listann til að einbeita sér að vörum sem þarfnast leiðréttingar eða sem eru undanskildar í kostnaðarleiðréttingarferlinu.

### <a name="about-item-batches"></a>Um vörukeyrslur

Hægt er að keyra kostnaðarleiðréttingu á nokkrum vörum með því að flokka þær í keyrslur. Keyrslur auðvelda aðlaga sumar vörur sérstaklega, til dæmis vegna þess að lengri tíma tekur að leiðrétta þær. Keyrslur geta einnig hjálpað til við að auðkenna vörur sem eru með úthreyfingar.

Á síðunni **Leiðrétting** birgðakostnaðar er ein af eftirfarandi gerðum til að stofna keyrslu:

* Vörurnar eru valdar á listanum, kostnaðarleiðrétting **keyrð** og Bæta við keyrslu **valið**.
* Til að stofna runu og keyra kostnaðarleiðréttingu strax skal velja vörurnar á listanum, velja **Keyra kostnaðarleiðréttingu** og velja **svo Bæta við keyrslu og keyra**.
* Velja Skal **Keyra kostnaðarleiðréttingu**, velja **Birgðakeyrslur** og færa svo inn afmörkun í reitinn **Birgðaafmörkun** .
  
> [!TIP]
> Til að stofna á fljótlegan hátt aðra keyrslu fyrir allar vörur sem ekki eru þegar til í keyrslu skal velja **Bæta við vörum**  sem vantar á síðunni **Kostnaðarleiðrétting - Birgðakeyrslur**.

Þegar keyrslu fyrir runu lýkur hefur keyrslan eina af eftirfarandi stöðu á síðunni **Birgðakeyrslur** :

* **Árangur**: Kostnaðarleiðréttingin heppnast.
* **Mistókst**: Ef kostnaðarleiðréttingin mistekst auðkennir [!INCLUDE [prod_short](includes/prod_short.md)]  vöruna sem olli villunni og skiptir núgildandi keyrslu í tvennt. Ein keyrsla með erfiðri vöru og önnur með vörunum sem eftir eru. Endurkeyrsla kostnaðarleiðréttingar fyrir keyrsluna með vörunum sem eftir eru. Ef það mistekst aftur endurtekur ferlið. Hámarksfjöldi skipta er skilgreindur í reitnum **Hámarks tilraunir** til að reyna aftur. Sjálfgefið gildi endurtekninga er 10 en hægt er að færa inn ný takmörkun.
* **Rann út**: Ef kostnaðarleiðréttingin á keyrslu lýkur ekki innan þess tímabils sem tilgreint er í reitnum **Tímamörk (mínútur)** (á milli 1 til 720 mínútna) lýkur lotunni og breytingar eru afturköllaðar. [!INCLUDE [prod_short](includes/prod_short.md)] skiptir núgildandi keyrslu í helmingi og keyrir kostnaðarleiðréttingarferlið aftur fyrir hvern helming. Þetta ferli heldur áfram þar til kostnaðarleiðréttingin heppnast eða nær hámarkstilraunum til endurtekinna tilrauna.

> Það er allt í sósíalistum. Hver keyrsla í sérstakri lotu. Til að fylgjast með framvindu skal nota aðgerðina **Endurnýja** .

### <a name="run-cost-adjustment"></a>Keyra kostnaðarleiðréttingu

Nota síðuna **Leiðrétting birgðakostnaðar** til að gera leiðréttingar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Birgðakostnaðarleiðréttingu** og velja síðan viðeigandi tengil.
1. Eftir því hvað á að gera skal nota einn af eftirfarandi valkostum:

  * Fyrir eina eða fleiri vörur strax skal velja vörurnar á listanum og velja **svo Keyra kostnaðarleiðréttingu**.
  * Fyrir keyrslur er einn af eftirfarandi valkostum notaður:

    * Til að stofna runu og leiðrétta kostnað strax skal velja vörurnar á listanum, velja **Keyra kostnaðarleiðréttingu** og svo **Bæta við keyrslu og keyra**.
    * Til að keyra hana fyrir allar keyrslur skal velja **Keyra kostnaðarleiðréttingu,Birgðakeyrslur** **og** velja **svo Keyra.**
    
    Nánari upplýsingar um keyrslur eru í [Um birgðakeyrslur](#about-item-batches).

### <a name="explore-item-details"></a>Skoða upplýsingar um vöru

Valmyndin **Vara** er notuð til að fá aðgang að upplýsingum um kostnaðarleiðréttingar á tiltekinni vöru.

* **Birgðafærslur**: Birta birgðafærslur fyrir vöruna. Aðgerðin **Mark fyrir leiðréttingu** gerir kleift að knýja fram endurkeyrslu kostnaðarleiðréttingar á vörum beint eða óbeint sem tengjast færslum á innleið sem notandi velur. Það getur verið gagnlegt að þvinga endurkeyrslu ef fyrri keyrslur leiddu til ranga kostnaðar.
* **Virðisfærslur**: Birta virðisfærslur fyrir vöruna.
* **Kostnaðarleiðr.leiðr. Komustaðir**: Glugginn Meðalinnk.verðleiðr. er opnaður **. Komustaðasíða** sem aðallega er notuð til að reikna út meðalinnkaupsverð. Síðan birtir samsetningar vara, birgðageymslna, afbrigða og matsdagsetninga þar sem kostnaðarleiðréttingar eru, eða verða að vera keyrðar.
* **Kostnaðarleiðr.leiðr. Pantanir**: Glugginn Birgðaleiðr.leiðr. er opnaður **. Færsla (Pöntun)** síða þar sem framleiðslu- og samsetningarpantanir eru leiðréttar. Hann sýnir að pantanirnar eru leiðréttar eða þarfnast leiðréttingar.

### <a name="view-the-outcome"></a>Skoða niðurstöðu

Nota skal valmyndina **Skrá eftir** til að skoða niðurstöðu kostnaðarleiðréttinga:

* **Keyra**: Sýna kostnaðarleiðréttingarskrár fyrir hverja keyrslu. Í kladdanum eru gögn um vöruafmörkun, stöðu (Árangur/Mistókst/Tímasett), upphafs- og lokadagsetningu/tímalengd, lengd og kostnaðarmismuninn sem hlaupið framleiðir.
* **Vara**: Sýna nákvæmar upplýsingar um leiðréttingarferlið fyrir völdu vöruna.

### <a name="include-or-exclude-items-from-adjustments"></a>Taka með eða sleppa vörum úr leiðréttingum

Ef ein eða fleiri vörur mistakast er hægt að útiloka vörurnar úr leiðréttingarkeyrslunni og taka þær síðan með í síðari keyrslum. Í valmyndinni **Aðgerðir** er eitt af eftirfarandi valið:

* **Sleppa vöru frá leiðréttingu** og **taka vöru með í leiðréttingu**: Gera tímabundið óvirka og virkja síðan aftur kostnaðarleiðréttingu fyrir valda vöru. Kostnaðarleiðrétting heldur áfram að halda kostnaði nákvæmum fyrir aðrar vörur á meðan mál er rannsakað með tiltekinni vöru.

## <a name="post-adjusted-costs-to-the-general-ledger"></a>Bóka leiðréttan kostnað í fjárhag

Yfirleitt eru nýjar virðisfærslur bókaðar í fjárhag samkvæmt áætluninni **fyrir verkraðarfærsluna Bóka birgðabreytingar (1002)** verkraðarfærslu. Hins vegar er hægt að bóka leiðréttingar á fjárhag strax af síðunni **Leiðrétting birgðakostnaðar** . Í valmyndinni **Aðgerðir** er valið **Bóka birgðabreytingar**.

## <a name="troubleshoot-cost-adjustments"></a>Úrræðaleit vegna kostnaðarleiðréttinga

Eftirfarandi valkostir eru notaðir **í valmyndinni** Greining til að leysa kostnaðarleiðréttingarkeyrslur.

* **Flytja út vörugögn**: Flytja út vörutengd gögn í textaskrá. Hægt er að nota skrána til frekari greiningar í sandkassaumhverfi eða hengja hana við stuðningsbeiðni þegar verið er að rannsaka útreikning kostnaðarútreikninga.
* **Flytja inn vörugögn**: Flytja textaskrá sem áður var flutt inn aftur í gagnagrunninn. Þessi aðgerð er aðeins virk í sandkassaumhverfi eða matsfyrirtækjum.
* **Endurstilla kostnað er leiðrétt**: Endurstilla **kostnaðinn er leiðréttur** vífæra á vörur, framleiðslupantanir eða samsetningarpantanir. Þessi stilling gerir kleift að þvinga endurkeyrslu kostnaðarleiðréttingarinnar fyrir þær.
* **Greiningarskýrsla** kostnaðarútgáfu: Greining dæmigerðra gagnavanda veldur útreikningsvillum í kostnaðarútreikningi. Hún kannar hvort birgðafærslur, virðisfærslur, birgðajöfnunarfærslur og getubókarfærslur séu réttar.
* **Eyða vörugögnum**: Hreinsa allar vörutengdar töflur í gagnagrunninum. Þessi aðgerð er aðeins tiltæk í sandkassaumhverfi eða matsfyrirtækjum.

## <a name="see-also"></a>Sjá einnig .

[Leiðrétta kostnað vara](inventory-how-adjust-item-costs.md)  
[Hönnunarupplýsingar: kostnaðarleiðrétting](design-details-cost-adjustment.md)  
