---
title: Greina gögn á listasíðum og fyrirspurnum með gagnagreiningarstillingu
description: Læra að nota gagnagreiningarhaminn í Business central til að greina gögn.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/15/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Greina listasíðu og fyrirspurnargögn með gagnagreiningarstillingu

> **GILDIR UM:** Opinber forskoðun í Business Central 2023 gefa út bylgju 1 og síðar til að greina listasíður; Almennt fáanlegt í Business Central 2023 gefa út bylgju 2 til að greina gögn frá listasíðum og fyrirspurnum.

Í þessari grein lærir notandinn hvernig á að greina gögn frá listasíðum og fyrirspurnum í *gagnagreiningarstillingunni*. Með gagnagreiningarstillingunni er hægt að greina gögn beint frá síðunni án þess að þurfa að keyra skýrslu eða skipta um annað forrit eins og Excel. Hún veitir gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Í stað þess að keyra skýrslur með mismunandi valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða yfirlit á gögnunum. Dæmi: "Viðskiptamenn mínir", "Fylgja eftir vörum", "Lánardrottnum hefur nýlega verið bætt við", "Sölutölur", eða öll önnur yfirlit sem hægt er að ímynda sér.

> [!TIP]
> Gott við greiningarham gagna er að hann breytir engum undirliggjandi gögnum á listasíðu eða fyrirspurn, eða uppsetningu síðunnar eða fyrirspurnarinnar þegar hún er ekki í gagnagreiningarstillingu. Besta leiðin til að fræðast um það sem hægt er að gera í gagnagreiningarstillingunni er að prófa hlutina.

## Frumskilyrði 

- Ef Business Central útgáfa 22 er notuð er gagnagreiningarstillingin í forskoðun. Stjórnandi verður því að gera það virkt áður en hægt er að nota það. Til að gera hana virka er farið á síðuna **Eiginleikastjórnun** og kveikt á **Aðgerðauppfærslu: Greiningarstilling, greining á gögnum á fljótlegan hátt í Business Central**. [Fræðast meira um Eiginleikastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).
- Í útgáfu 23 og síðari útgáfu verður að úthluta reikningnum **gagnagreiningu - EXEC** heimildarsafninu eða hafa keyrsluheimild fyrir kerfishlutnum **9640 Leyfa gagnagreiningarstillingu**. Sem stjórnandi er hægt að útiloka þessar heimildir fyrir notendur sem ekki eiga að hafa aðgang að greiningarstillingunni.

> [!NOTE]
> Ef til vill sjást nokkrar listasíður sem ekki innihalda **rofa greiningar** til að breyta í greiningarstillinguna. Ástæðan er sú að forritarar geta gert greiningarham óvirkan á tilteknum síðum með því að nota eiginleikann [AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) í AL.

## Hefjast handa

Ljúka skal þessum skrefum til að byrja að greina gögn með greiningarstillingunni.

>[!TIP]
> Í greiningarstillingunni er einnig Copilot-aðgerð sem kallast *greiningaraðstoð* sem hjálpar til við að hefjast handa. [Fræðast meira um greiningaraðstoð við Copilot](analysis-assist.md).

1. Opna listasíðu eða fyrirspurn.

   Til dæmis, til að vinna með **síðuna Viðskm.færslur** skal velja ![stækkunarglerið sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png) Tákn (<kbd>Alt</kbd>+<kbd>Q</kbd>), slá inn *viðskiptamannafærslur* og velja síðan viðeigandi tengil. 

2. Á aðgerðastikunni efst á síðunni er smellt á Hnappurinn **Færa inn greiningarham** ![Sýnir hnappinn til að kveikja á hnappinum Greiningarhamur](media/analysis-mode-icon.png) .

    Gagnagreiningarhamur opnar gögnin sem eru bjartsýni á gagnagreiningu.  Í gagnagreiningarstillingu er venjulegu aðgerðastikunni skipt út fyrir sérstaka gagnagreiningarhamsstiku. Eftirfarandi mynd sýnir mismunandi svæði síðu í gagnagreiningarstillingunni.

   [![Birtir yfirlit yfir síðu í gagnagreiningarstillingunni](media/analysis-mode-overview-3.png)](media/analysis-mode-overview-3.png#lightbox)

   Hvert svæði er útskýrt í köflunum sem fylgja.

3. Nota mismunandi svæði til að vinna með, taka saman og greina gögn. Sjá hlutana sem fylgja með nánari upplýsingum.

4. Þegar á að stöðva greiningarstillinguna er hnappurinn **Skilja eftir greiningarhamur** ![birtur til að slökkva á greiningarham](media/analysis-mode-exit-icon.png) 

   Greiningarfliparnir sem bætt hefur verið við eru þar til þeim er eytt. Ef farið er aftur í gagnagreiningarstillinguna sést það nákvæmlega eins og það var eftir.

> [!NOTE]
> Gögnunum sem birtast í greiningarstillingu er stýrt af afmörkunum eða yfirlitum sem eru stillt á listasíðunni. Þannig er hægt að forsíu gögn áður en greiningarstilling er færð inn.

## Vinna með gagnagreiningarham

Í gagnagreiningarstillingunni er síðunni skipt í tvö svæði:

- Aðalsvæðið, sem samanstendur af gagnasvæði (1), yfirlitsstika (2) og flipastiku (5)
- Gagnaskipulagssvæðið, sem samanstendur af tveimur svæðum: dálkum (3) og greiningarafmörkunum (4).

### Gagnasvæði (1)

Gagnasvæðið er þar sem línurnar og dálkarnir í fyrirspurn listasíðunnar eru birtir og gögn tekin saman. Gagnasvæðið býður upp á fjölhæfa leið til að stjórna uppsetningu dálka og fljótlegri leið til að fá samantekt á gögnunum. Fyrir dálka sem innihalda töluleg gildi er samtala allra gilda í dálknum sýnd í síðustu línu nema línuflokkar hafi verið skilgreindir. Í þessu tilviki birtast samtölurnar sem millisamtala fyrir hópana.  

![Birtir yfirlit yfir gagnasvæði á síðu í gagnagreiningarstillingunni](media/analysis-mode-data-area.png)

- Dálkur er færður með því að velja hann og draga hann þangað sem þeir eru skynsamlegastir í greiningunni.
- Dálkhaus er valinn til að raða eftir dálki. Til að raða í mörgum dálkum er Shift-lyklinum <kbd>haldið niðri</kbd> með því að velja dálkhausana sem á að raða.
- Hægrismellt er á dálkinn eða sveifa yfir hann og valið valmyndartáknið ![Sýnir táknið í dálki í gagnagreiningarstillingu sem opnar valmynd aðgerða](media/analysis-mode-column-menu-icon.png) Til að fá aðgang að nokkrum aðgerðum sem hægt er að gera í dálkum. Dæmi:

  - Til að festa dálk vinstra eða hægra megin við gagnasvæðið svo að hann færist ekki af skjánum þegar skrunað er skal velja ![Sýnir táknið á dálki í gagnagreiningarstillingu sem opnar valmynd aðgerða Pin-dálkpinna](media/analysis-mode-column-menu-icon.png) > **·** > **vinstra megin** við dálkhlutann.
  - Skilgreina gagnaafmarkanir beint á dálkaskilgreininguna í stað þess að fara á **svæðin Greiningarafmarkanir** . Enn er hægt að gæta að upplýsingum um tengd gögn og fyrir hverja línu og opna kortið til að fræðast meira um tiltekna einingu.
- Gagnasvæðið er notað til að hafa samskipti við gögnin. Fyrir dálka sem innihalda töluleg, samantekin gildi er hægt að fá lýsandi upplýsingar í safni reita með því að merkja þær. Upplýsingarnar birtast á stöðulínunni (2) neðst á síðunni.
- Flytja út gögn á Excel eða csv-sniði. Hægrismellt er á gagnasvæðið eða úrval af reitum til að flytja út.

### Yfirlitsstika (2)

Yfirlitsstikan er neðst á síðunni og birtir tölfræðilegar upplýsingar um gögnin á listasíðunni eða fyrirspurninni. Þegar samskipti eru gerð við dálka þar sem hægt er að leggja saman gildi, eins og að velja margar línur í dálki sem sýnir upphæðir, uppfærast gögnin.

![Birtir yfirlit yfir yfirlitsstika í gagnagreiningarstillingunni](media/analysis-mode-totals-row.png)

Eftirfarandi tafla lýsir mismunandi tölum sem sýndar eru í samtölusvæðinu:

|Fjöldi|Heimildasamstæða|
|-|-|
|Línur|Fjöldi valinna lína sem hluti af heildarfjölda tiltækra lína. |
|Heildarlínur|Fjöldi lína á óafmarkaða listanum eða fyrirspurninni.|
|Afmarkað|Fjöldi lína sem birtast vegna afmarkana sem notaðar eru á listanum eða fyrirspurninni.|
|Meðaltal|Meðalgildi í öllum völdum samantektarreitum.|
|Talning|Fjöldi valinna lína.|
|Lágmark|Lágmarksgildi í öllum völdum samantektarreitum.|
|Hámark|Hámarksgildið í öllum völdum samanteknum reitum.|
|Samtala|Samtala allra gilda í völdum samantektarreitum.|

### Dálkar (3)

Dálkarnir **er** annað af tveimur svæðum sem vinna saman til að skilgreina greiningu. Hitt svæði er **svæðið Greiningarafmarkanir** . Svæðið **Dálkar** er notað til að taka saman gögn.  **Nota svæðið Dálkar** til að skilgreina hvaða dálka skuli taka með í greiningunni.

![Birtir yfirlit yfir dálkasvæði í gagnagreiningarstillingunni](media/analysis-mode-columns-3.png)

|Svæði|Heimildasamstæða|
|-|-|
|Leita að/athuga eða hreinsa alla reiti|Leita að dálkum. Veljið gátreitinn til að velja/hreinsa alla dálka.|
|Gátreitina|Á þessu svæði er gátreitur fyrir hvern reit í upprunatöflu listans eða fyrirspurnarinnar. Þessi reitur er notaður til að breyta því hvaða dálkar eru sýndir. Veljið gátreit til að sýna dálk fyrir svæðið á síðunni; gátreitinn til að fela dálkinn. |
|Línuflokkar|Þetta svæði er notað til að flokka og leggja saman gögn eftir einum eða fleiri reitum. Aðeins er hægt að hafa reiti sem ekki eru tölulegir, eins og texti, dagsetningar- og tímareitir. Línuflokkar eru oft notaðir í veltistillingu.|
|Gildi|Þessi reitur er notaður til að tilgreina reiti sem samtala á að ná yfir. Aðeins er hægt að taka með reiti sem innihalda númer sem hægt er að bæta saman; til dæmis, ekki texta-, dagsetningar- eða tímareiti.|

Til að færa reit milli svæða skal velja grípa táknið ![Birtir yfirlit yfir síðu í greiningarstillingunni](media/column-grab-icon.png) Við hliðina á dálknum á listanum og draga inn í marksvæðið. Komið er í veg fyrir að reitur sé færður yfir á svæði þar sem hann er ekki leyfður.

### Greiningarafmarkanir (4)

Á **svæðinu Greiningarafmarkanir** er hægt að setja frekari gagnaafmarkanir á dálka til að takmarka færslurnar í listanum. Afmarkanir eru settar á dálka til að takmarka færslurnar á listanum og samtölur sem á eftir koma aðeins þeim færslum sem notandi hefur áhuga á samkvæmt skilyrðum sem notandi skilgreinir. Gert er ráð fyrir að notandi hafi aðeins áhuga á gögnum fyrir tiltekinn viðskiptamann eða sölupantanir sem fara yfir tiltekna upphæð. Til að stilla afmörkun skal velja dálkinn, velja samanburðaraðgerð af listanum (eins og **Jafnt** og eða **Byrja með**) og færa inn gildið.

![Birtir yfirlit yfir afmörkunarsvæðið í greiningarstillingunni](media/analysis-mode-filters-2.png)

> [!NOTE]
> Viðbótarafmarkanirnar eiga aðeins við um gildandi greiningarflipa. Þannig er hægt að skilgreina nákvæmlega þá aukagagnaafmarkanir sem þarf við tiltekna greiningu.

### Flipar (5)

Flipasvæðið efst gerir kleift að stofna mismunandi grunnstillingar (dálka og greiningarafmarkanir) á sérstökum flipum þar sem hægt er að vinna með gögn á flipunum óháð hvort öðru. Alltaf er alltaf til minnst einn flipi sem er sjálfgefið kallaður **Greining 1** . Að bæta við fleiri flipum er gagnlegt til að vista oft notaðar greiningarskilgreiningar í gagnamengi. Til dæmis gætu flipar verið til að greina gögn í veltistillingunni og aðrir flipar sem afmarka við hlutmengi lína. Sumir flipar sýna nákvæmt yfirlit með mörgum dálkum og aðrir sýna aðeins nokkra lykildálka.

Hér er bent á að vinna með marga greiningarflipa:

- Til að bæta við nýjum flipa er stóra **+** táknið valið næst síðasta greiningarflipanum.
- Ör niður á flipa er valin til að fá aðgang að lista yfir aðgerðir sem hægt er að gera á flipanum eins og endurnefningu, tvítekningu, eyða og færa.

   - **Eyða** eyðir flipanum sem er opinn. **Eyða öllum** flipum sem hefur verið bætt við, nema sjálfgefni **flipinn Greining 1** .
- Ekki er hægt að fjarlægja **greiningu 1** alveg en hægt er að endurnefna hana með því að nota aðgerðina **Endurnefna** og hreinsa breytingarnar sem gerðar hafa verið með því að nota **Eyða eða** Eyða **öllu**.  

- Greiningarfliparnir sem hefur verið bætt við og grunnstilltir eru þar til þeim er eytt. Ef farið er aftur í gagnagreiningarstillinguna sést það nákvæmlega eins og það var eftir.

   > [!TIP]
   > Fliparnir sem settir eru upp sjást aðeins. Aðrir notendur sjá aðeins flipa sem þeir hafa sett upp.
- Hægt er að afrita greiningarflipa. Afritun getur verið gagnleg ef gera á tilraunir með að breyta flipa án þess að breyta frumritinu eða ef búa á til mismunandi frávik í sömu greiningu.


## Dagsetningastigveldi

Í greiningarstillingu eru dagsetningarreitir gagnasafnsins myndaðir í ársfjórðungs-mánaðarstigveldi þriggja aðskilinna reita. Þetta stigveldi er byggt á venjulegu dagatali en ekki fjárhagsdagatölum sem skilgreind eru í Business Central.

Viðbótarreitirnir eru nefndir _\<field name\> Ársfjórðungur_, _\<field name\>  Ársfjórðungur_ og _\<field name\> Mánuður_. Ef gagnasafnið inniheldur til dæmis reit sem kallast _Bókunardagsetning_ samanstendur samsvarandi dagsetningarstigveldi af reitum sem kallast _Bókunardags.ár_, _Bókunardags.ársfjórðungur_ og _Bókunardags.mánuður_.

> [!NOTE]
> Dagsetningastigveldið á aðeins við um reiti af gerðinni dagsetning, ekki fyrir reiti af gerðinni dagsetningartími.

## Veltihamur

Nota má veltistillingu til að greina mikið magn tölulegra gagna, millisamtölugögn eftir flokkum og undirflokkum. Veltihamurinn er eins og [veltitöflur í Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Til að kveikja og slökkva á veltistillingunni skal renna **rofa veltistillingarinnar** á **dálkasvæðinu** (3). Þegar kveikt er á veltistillingunni **birtist svæðið Dálkmerki** á svæðinu.  **Nota svæðið Dálkmerki** til að flokka samtölur lína í flokka. Reitir sem bætt er við **svæðið Dálkmerki** sýna sem dálka á gagnasvæðinu (1).

Með því að byggja gagnagreiningu í veltistillingu eru færðir reitir í svæðin þrjú: **línuflokkar**, **dálkamerki** og **gildi**. Eftirfarandi mynd sýnir hvar reitirnir varpast á gagnasvæði (1), hvar `sum` eru útreiknuð gögn og gildi ef **vill**.

<table>
<tr><th></th><th>Dálkmerki</th><th></th><th>Dálkmerki</th><th></th></tr>
<tr><th>Línuflokkur</th><th>Virði</th><th>Virði</th><th>Virði</th><th>Virði</th></tr>
<tr><td>lína</td><td>Samtala</td><td>Samtala</td><td>Samtala</td><td>Samtala</td></tr>
<tr><td>lína</td><td>Samtala</td><td>Samtala</td><td>Samtala</td><td>Samtala</td></tr>
<tr><td>lína</td><td>Samtala</td><td>Samtala</td><td>Samtala</td><td>Samtala</td></tr>
<tr><td>lína</td><td>Samtala</td><td>Samtala</td><td>Samtala</td><td>Samtala</td></tr>
</table>

> [!TIP]
> Dálkar sem hafa aðeins nokkur möguleg gildi eru bestu umsækjendur sem nota á í **dálkgildum**.


## Greina mikið magn gagna

Ef gagnasafnið sem á að greina er meiri en 100.000 línur er lagt til að færður sé inn greiningarhamur sem er bestur fyrir stór gagnasöfn. Tvær takmarkanir eru í gangi ef skipt er í þessa stillingu: 

- Snið reita af fjórum gagnategundum gæti breyst: 

   - Gjaldmiðli 
   - Aukastöfum (alltaf sýnt með tveimur aukastöfum) 
   - Dagsetningar (alltaf sýnt á sniði ÁÁÁ-MM-DD)
   - tímareitur
- Reitir sem notaðir eru í veltistillingu og bætt við dálkmerki verða að hafa lágan fjölda greinilegra gilda.

   Ef veltistilling er gerð virk og reitur dreginn inn í **svæði dálkmerkja** þar sem undirliggjandi gögn fyrir þann reit hafa of mörg einstök gildi gæti flipinn vafrinn orðið óábyrgur og lokar á endanum og þarfnast þess að byrja upp á nýtt. Í þessu tilviki skal annaðhvort ekki velta á þeim reit eða setja afmörkun á reitinn áður en honum **er bætt við svæðið Dálkmerki** .

## Samnýting gagnagreiningar

Þegar greining hefur verið gerð á flipa er hægt að deila honum sem tengli með samstarfsfólki og öðrum innan fyrirtækisins beint frá biðlaranum. Aðeins viðtakendur sem hafa heimild til fyrirtækisins og gögnin geta notað tengilinn.

1. Á greiningarflipanum er örvarhaus niður valinn og Afrita tengil **síðan valinn**.

   ![Sýnir aðgerðina til að afrita greiningu](media/analysis-mode-copy.png)

   Svarglugginn **Tengja við \<tab name\>** opnast.

1. Sjálfgefið er að greiningin sem er samnýtt tengir við síðuna eða fyrirspurnina í fyrirtækinu sem verið er að vinna í, sem er gefið til kynna með `company=<company_name>` í reitnum URL við hliðina á hnappnum **Afrita** . Ef senda á tengil í greiningu sem ekki tengist tilteknu fyrirtæki **er reiturinn Fyrirtæki:** á **Ekki tengja við tiltekið fyrirtæki**.

   ![Sýnir afritunartengilsglugga fyrir greiningarflipa](media/analysis-link-copied.svg)

1. Valið er **Afrit**.

1. Líma tengilinn í samskiptamiðla að eigin vali, eins og Word, Outlook, Teymi OneNote, og svo einn. 

2. Þegar búið er að taka á móti geta viðtakendur síðan valið tengilinn og opnað greiningu á síðunni eða fyrirspurninni í Business Central. Beðið er um að tilgreina heiti á nýja greiningarflipanum sem verður stofnaður.  

## Takmarkanir á útgáfubylgju 2023 (forskoðun)

Opinbert forskoðun á þessari aðgerð hefur eftirfarandi takmarkanir:

- Greiningarhamsyfirlitið hefur takmörk á 100.000 línum. Ef þú fer yfir þessi takmörk færðu skilaboð sem segja þér það. Til að vinna utan um þessa takmörkun eru settar afmarkanir á síðuna áður en skipt er yfir í greiningarstillingu, ef það er mögulegt. Til dæmis ef til vill á að greina tiltekinn flokk viðskiptamanna eða aðeins að gögnum frá yfirstandandi ári. Einnig er hægt að velja fyrirfram skilgreint yfirlit ef það myndi virka í greiningu.
- Eiginleikinn samnýtt gagnagreining er ekki tiltækur.
- Geta til að vista val á greiningarvali gagna á listasíðum og vista greiningarvalmyndir á hverjum greiningarflipa eru ekki tiltækar eins og er.

## Sjá einnig .

[Tilfallandi gagnagreining](reports-adhoc-analysis.md)  
[Skoða og breyta í Excel](across-work-with-excel.md)  
