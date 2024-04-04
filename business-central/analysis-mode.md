---
title: Greindu gögn á listasíðum og fyrirspurnum með því að nota gagnagreiningarham
description: Lærðu hvernig á að nota gagnagreiningarhaminn í Business Central til að greina gögn.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 12/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-page-and-query-data-using-data-analysis-mode"></a>Greindu listasíðu og fyrirspurnargögn með því að nota gagnagreiningarham

> **Á VIÐ:** Opinber forskoðun í Business Central 2023 útgáfubylgju 1 og síðar til að greina listasíður; Almennt fáanlegt í Business Central 2023 útgáfubylgju 2 til að greina gögn frá listasíðum og fyrirspurnum.

Í þessari grein lærir þú hvernig á að greina gögn af listasíðum og fyrirspurnum með því að nota *gagnagreiningarhaminn*. Gagnagreiningarhamurinn gerir þér kleift að greina gögn beint af síðunni, án þess að þurfa að keyra skýrslu eða skipta um annað forrit eins og Excel. Það veitir gagnvirka og fjölhæfa leið til að reikna, draga saman og skoða gögn. Í stað þess að keyra skýrslur með mismunandi valkostum og síum geturðu bætt við mörgum flipa sem tákna mismunandi verkefni eða skoðanir á gögnunum. Dæmi gætu verið „Viðskiptavinir mínir“, „Fylgjast með hlutum“, „Nýlega bættir söluaðilar“, „Sölutölfræði“ eða önnur sýn sem þú getur ímyndað þér.

> [!TIP]
> Það góða við gagnagreiningarhaminn er að hann breytir ekki neinum af undirliggjandi gögnum listasíðu eða fyrirspurnar, eða útliti síðunnar eða fyrirspurnarinnar þegar hún er ekki í gagnagreiningarham. Þannig að besta leiðin til að læra um hvað þú getur gert í gagnagreiningarhamnum er að prófa hlutina.

## <a name="prerequisites"></a>Frumskilyrði

- Ef þú ert að nota Business Central útgáfu 22 er gagnagreiningarhamurinn í forskoðun. Svo, stjórnandi verður að virkja það áður en þú getur notað það. Til að virkja það skaltu fara á **Eiginleikastjórnun** síðuna og kveikja á **Eiginleikauppfærslu: Greiningarhamur, greina gögn fljótt beint í Business Central**. [Frekari upplýsingar um eiginleikastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).
- Í útgáfu 23 og síðar verður reikningnum þínum að vera úthlutað **GAGNAGREINING - EXEC** heimildasettinu eða innihalda framkvæmdaheimild á kerfishlutnum **9640 Leyfa gögn Greiningarham**. Sem stjórnandi geturðu útilokað þessar heimildir notenda sem þú vilt ekki að hafi aðgang að greiningarhamnum.

> [!NOTE]
> Þú gætir tekið eftir einhverjum listasíðum sem innihalda ekki **Analyze** rofinn til að skipta yfir í greiningarhaminn. Ástæðan er sú að forritarar geta slökkt á greiningarham á tilteknum síðum með því að nota [AnalysisModeEnabled eiginleikann](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) í AL.

## <a name="get-started"></a>Hefjast handa

1. Opnaðu listasíðuna eða fyrirspurnina.

   Til dæmis, til að vinna með **Færslur viðskiptavina** síðunnar skaltu velja ![stækkunarglerið sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png) Táknið (<kbd>Alt</kbd>+<kbd>Q</kbd>), sláðu inn *færslur viðskiptamannabókar* og veldu síðan tengdur hlekkur. 

2. Í aðgerðastikunni efst á síðunni skaltu kveikja á **Analyze** rofanum.

    Gagnagreiningarhamur opnar gögnin í upplifun sem er fínstillt fyrir gagnagreiningu.  Í gagnagreiningarham er venjulegri aðgerðastikunni skipt út fyrir sérstaka gagnagreiningarhamsstiku. Eftirfarandi mynd sýnir mismunandi svæði síðu í gagnagreiningarham.

   [![Sýnir yfirlit yfir síðu á gagnagreiningarham](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Hvert svæði er útskýrt í köflum sem fylgja.

3. Notaðu mismunandi svæði til að vinna með, draga saman og greina gögn. Sjá kaflana sem fylgja fyrir nánari upplýsingar.

4. Þegar þú vilt fara úr greiningarhamnum skaltu slökkva á **Analyze** rofanum.

   Greiningarflipar sem þú hefur bætt við eru áfram þar til þú eyðir þeim. Þannig að ef þú ferð aftur í gagnagreiningarhaminn sérðu þau nákvæmlega eins og þú fórst frá þeim.

> [!NOTE]
> Gögnin sem sýnd eru í greiningarham er stjórnað af síunum eða skoðunum sem eru settar á listasíðuna. Þetta gerir þér kleift að forsía gögn áður en þú ferð í greiningarham.

## <a name="work-with-data-analysis-mode"></a>Vinna með gagnagreiningarham

Í gagnagreiningarham er síðunni skipt í tvö svæði:

- Aðalsvæðið, sem samanstendur af gagnasvæðinu (1), yfirlitsstikunni (2) og flipastikunni (5)
- Gagnavinnslusvæðið, sem samanstendur af tveimur rúðum: dálkum (3) og greiningarsíur (4).

### <a name="data-area-1"></a>Gagnasvæði (1)

Gagnasvæðið er þar sem línur og dálkar listasíðufyrirspurnar eru sýndar og gögn eru tekin saman. Gagnasvæðið býður upp á fjölhæfa leið til að stjórna uppsetningu dálka og fljótlega leið til að fá yfirlit yfir gögnin. Fyrir dálka sem innihalda tölugildi er summa allra gilda í dálknum sýnd í síðustu röð, nema þú hafir skilgreint línuhópa. Í þessu tilviki birtast fjárhæðirnar sem meðaltala fyrir hópana.  

![Sýnir yfirlit yfir gagnasvæði á síðu í gagnagreiningarham](media/analysis-mode-data-area.png)

- Til að færa dálk skaltu velja hann og draga hann þangað sem hann er skynsamlegastur í greiningu þinni.
- Til að raða í dálk skaltu velja dálkhausinn. Til að raða í marga dálka skaltu velja og halda inni <kbd>Shift</kbd> lyklinum á meðan þú velur dálkahausana sem þú vilt flokka á.
- Hægrismelltu á dálkinn eða farðu yfir hann og veldu valmyndartáknið ![Sýnir táknið á dálki í gagnagreiningarham sem opnar valmynd með aðgerðum](media/analysis-mode-column-menu-icon.png) Til að fá aðgang að nokkrum aðgerðum sem þú getur gert á dálkum. Dæmi:

  - Til að festa dálk vinstra megin eða hægra megin við gagnasvæðið þannig að hann hreyfist ekki af skjánum þegar þú flettir skaltu velja ![ Sýnir táknið á dálki í gagnagreiningarham sem opnar valmynd með aðgerðum](media/analysis-mode-column-menu-icon.png) > **Festa dálk** > **Pinna til vinstri**  súluhlutinn.
  - Skilgreindu gagnasíur beint á dálkskilgreininguna í stað þess að fara í **Greiningarsíur**  rúður. Þú getur samt kíkt inn á upplýsingar um tengd gögn og fyrir hverja línu og opnað kortið til að læra meira um tiltekna aðila.
- Notaðu gagnasvæðið til að hafa samskipti við gögnin. Fyrir dálka sem innihalda töluleg samantektargildi er hægt að fá lýsandi tölfræði um mengi reita með því að merkja við þá. Tölfræðin birtist í stöðustikunni (2) neðst á síðunni.
- Flytja út gögn á Excel eða csv sniði. Hægrismelltu á gagnasvæðið eða úrval af frumum til að flytja út.

### <a name="summary-bar-2"></a>Yfirlitsstika (2)

Samantektarstikan er neðst á síðunni og sýnir tölfræði um gögnin á listasíðunni eða fyrirspurninni. Þegar þú hefur samskipti við dálka sem hægt er að leggja saman gildi þeirra, eins og að velja margar línur í dálki sem sýnir upphæðir, uppfærast gögnin.

![Sýnir yfirlit yfir yfirlitsstiku á gagnagreiningarhamnum](media/analysis-mode-totals-row.png)

Eftirfarandi tafla lýsir mismunandi tölum sem eru sýndar á heildarsvæðinu:

|Fjöldi|Heimildasamstæða|
|-|-|
|Línur|Fjöldi valinna lína sem hluti af heildarfjölda tiltækra lína. |
|Samtals raðir|Fjöldi lína í ósíuða listanum eða fyrirspurninni.|
|Afmarkað|Fjöldi lína sem birtist vegna síanna sem notaðar eru á listann eða fyrirspurnina.|
|Meðaltal|Meðalgildi í öllum völdum yfirlitsreitum.|
|Talning|Fjöldi valda lína.|
|Lágmark|Lágmarksgildi í öllum völdum yfirlitsreitum.|
|Hámark|Hámarksgildi í öllum völdum samantektarreitum.|
|Samtala|Samtala allra gilda í völdum samantektarreitum.|

### <a name="columns-3"></a>Dálkar (3)

The **Dálkar**  er annar af tveimur rúðum sem vinna saman að því að skilgreina greininguna þína. Hitt svæðið er **Greiningarsíur** rúðan.  **Dálkar** glugginn er notaður til að draga saman gögnin. Notaðu **Dálka** rúðuna til að skilgreina hvaða dálka eigi að vera með í greiningunni.

![Sýnir yfirlit yfir dálkasvæðið í gagnagreiningarham](media/analysis-mode-columns-2.png)

|Svæði|Heimildasamstæða|
|-|-|
|Leitaðu/merktu eða hreinsaðu alla reiti|Leitaðu að dálkum. Veldu gátreitinn til að velja/hreinsa alla dálka.|
|Gátreitir|Þetta svæði inniheldur gátreit fyrir hvern reit í upprunatöflu listans eða fyrirspurnar. Notaðu þetta svæði til að breyta því hvaða dálkar eru sýndir. Veldu gátreit til að sýna dálk fyrir reitinn á síðunni; hreinsaðu gátreitinn til að fela dálkinn. |
|Röð hópar|Notaðu þetta svæði til að flokka og leggja saman gögn eftir einum eða fleiri reitum. Þú getur aðeins haft reiti sem ekki eru tölustafir, eins og texta-, dagsetningar- og tímareitir. Röð hópar eru oft notaðir í snúningsham.|
|Gildi|Notaðu þetta svæði til að tilgreina reiti sem þú vilt heildarupphæð fyrir. Þú getur aðeins haft reiti sem innihalda tölur sem hægt er að leggja saman; til dæmis ekki texta-, dagsetningar- eða tímareitir.|

Til að færa reit frá einu svæði til annars skaltu velja grípa táknið ![Sýnir yfirlit yfir síðu í greiningarhamnum](media/column-grab-icon.png) Við hliðina á dálknum á listanum og dragðu inn á marksvæðið. Þér er komið í veg fyrir að færa akur inn á svæði þar sem það er ekki leyfilegt.

### <a name="analysis-filters-4"></a>Greiningarsíur (4)

 **Greiningarsíur** rúðan gerir þér kleift að stilla frekari gagnasíur á dálka til að takmarka færslur á listanum. Stilltu síur á dálka til að takmarka færslur á listanum og síðari upphæðir við þær færslur sem þú hefur áhuga á út frá forsendum sem þú skilgreinir. Segjum sem svo að þú hafir aðeins áhuga á gögnum fyrir tiltekinn viðskiptavin eða sölupöntunum sem fara yfir tiltekna upphæð. Til að stilla síu, veldu dálkinn, veldu samanburðaraðgerðina af listanum (eins og **Jöfn** eða **Byrjar á**), sláðu síðan inn gildið.

![Sýnir yfirlit yfir síurúðuna í greiningarhamnum](media/analysis-mode-filters.png)

> [!NOTE]
> Viðbótarsíurnar eiga aðeins við um núverandi greiningarflipa. Þetta gerir þér kleift að skilgreina nákvæmlega þær aukagagnasíur sem þarf fyrir tiltekna greiningu.

### <a name="tabs-5"></a>Flipar (5)

Flipasvæðið efst gerir þér kleift að búa til mismunandi stillingar (dálka og greiningarsíur) á aðskildum flipa, þar sem þú getur meðhöndlað gögn á flipunum óháð hver öðrum. Það er alltaf að minnsta kosti einn flipi sem heitir **Greining 1** sjálfgefið. Að bæta við fleiri flipa er gagnlegt til að vista oft notaðar greiningarstillingar á gagnasafni. Til dæmis gætirðu verið með flipa til að greina gögn í snúningsstillingu og aðra flipa sem sía í undirmengi raða. Sumir flipar gætu sýnt ítarlega yfirsýn með mörgum dálkum og aðrir sýna aðeins nokkra lykildálka.

Hér eru nokkrar ábendingar um að vinna með marga greiningarflipa:

- Til að bæta við nýjum flipa skaltu velja stóra **+** merkið við hlið síðasta greiningarflipa.
- Veldu örina niður á flipa til að fá aðgang að lista yfir aðgerðir sem þú getur gert á flipa, eins og endurnefna, afrita, eyða og færa.

   - **Eyða** eyðir flipanum sem þú ert með opinn. **Eyða öllum** eyðir öllum flipum sem þú hefur bætt við, nema sjálfgefna **Greining 1** flipanum.
- Þú getur ekki fjarlægt  **Greining 1** alveg, en þú getur endurnefna hana með því að nota **Endurnefna** aðgerðina og hreinsa breytingarnar sem þú hefur gert með því að nota **Eyða** eða **Eyða öllum**.  

- Greiningarflipar sem þú hefur bætt við og stillt eru áfram þar til þú eyðir þeim. Þannig að ef þú ferð aftur í gagnagreiningarhaminn sérðu þau nákvæmlega eins og þú fórst frá þeim.

   > [!TIP]
   > Fliparnir sem þú setur upp eru aðeins sýnilegir þér. Aðrir notendur munu aðeins sjá flipa sem þeir hafa sett upp.
- Þú getur afritað greiningarflipa. Afritun getur verið gagnlegt ef þú vilt gera tilraunir með að breyta flipa án þess að breyta frumritinu, eða ef þú vilt búa til mismunandi afbrigði af sömu greiningu.


## <a name="date-hierarchies"></a>Dagsetningarstigveldi

Í greiningarham eru dagsetningarreitir gagnasafnsins myndaðir í ár-fjórðungs-mánaðar stigveldi með þremur aðskildum reitum. Þetta stigveldi er byggt á venjulegu dagatali, ekki neinum fjárhagsdagatölum sem eru skilgreind í Business Central.

Aukareitirnir heita _\<field name\> Ár_, _\<field name\> Fjórðungur_ og _\<field name\> mánuður_. Til dæmis, ef gagnasafnið inniheldur reit sem heitir _Bókunardagsetning_, þá samanstendur samsvarandi dagsetningarstigveldi af reitum sem kallast _Bókunardagsetning ár_, _Bókunardagur ársfjórðungur_ og _Bókunardagur mánuður_.

> [!NOTE]
> Dagsetningarstigveldið á sem stendur aðeins við um reiti með dagsetningu tegundar, ekki fyrir reiti af gerðinni dagsetningu.

## <a name="pivot-mode"></a>Pivot mode

Þú getur notað snúningsstillingu til að greina mikið magn af tölulegum gögnum og leggja saman gögn eftir flokkum og undirflokkum. Pivot hamurinn er eins og [pivot töflur í Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Til að kveikja og slökkva á snúningsstillingunni skaltu renna  **snúningsstillingu** rofanum í **dálka** rúðunni (3). Þegar þú kveikir á snúningsstillingunni birtist **Dálkamerki** svæðið í glugganum. Notaðu **dálkamerki** svæðið til að flokka samantölur fyrir línur í flokka. Reitir sem þú bætir við  **dálkamerki** svæðið birtast sem dálkar á gagnasvæðinu (1).

Að byggja upp gagnagreininguna í snúningsham felur í sér að færa reiti inn á þrjú svæði: **Röð hópar**, **Dálkamerki**, og **Gildi**. Eftirfarandi mynd sýnir hvar reitirnir kortast við gagnasvæðið (1), hvar `sum`  er útreiknuð gögn, og valfrjálst **Gildi**.

<table>
<tr><th></th><th>Dálkmerki</th><th></th><th>Dálkmerki</th><th></th></tr>
<tr><th>Röð hópur</th><th>Virði</th><th>Virði</th><th>Virði</th><th>Virði</th></tr>
<tr><td>lína</td><td>Summa</td><td>Summa</td><td>Summa</td><td>Summa</td></tr>
<tr><td>lína</td><td>Summa</td><td>Summa</td><td>Summa</td><td>Summa</td></tr>
<tr><td>lína</td><td>Summa</td><td>Summa</td><td>Summa</td><td>Summa</td></tr>
<tr><td>lína</td><td>Summa</td><td>Summa</td><td>Summa</td><td>Summa</td></tr>
</table>

> [!TIP]
> Dálkar sem hafa aðeins nokkur möguleg gildi eru bestir til að nota í dálki **Gildi**.


## <a name="analyze-large-amounts-of-data"></a>Greindu mikið magn af gögnum

Ef gagnasafnið sem þú vilt greina fer yfir 100.000 línur, er mælt með því að þú farir í greiningarham sem er fínstilltur fyrir stór gagnasöfn. Það eru tvær takmarkanir eins og er ef þú skiptir yfir í þessa stillingu: 

- Snið á reitum af eftirfarandi fjórum gagnagerðum gæti breyst: 

   - gjaldmiðil 
   - Aukastafir (alltaf sýndir með tveimur aukastöfum) 
   - Dagsetningar (alltaf sýndar á sniðinu ÁÁÁÁ-MM-DD)
   - tímabelti
- Reitir sem eru notaðir í snúningsstillingu og bætt við dálkamerki verða að hafa fáan fjölda aðskildra gilda.

   Ef þú kveikir á snúningsstillingu og dregur reit inn á **dálkamerki** svæði, þar sem undirliggjandi gögn fyrir þann reit hafa of mörg aðskilin gildi, þá gæti vafraflipi ekki svarað og mun loksins loka, sem krefst þess að þú byrjir upp á nýtt í nýrri lotu. Í þessu tilviki skaltu annað hvort ekki snúa á þann reit eða setja síu á reitinn áður en honum er bætt við  **dálkamerkingar** svæðið.

## <a name="share-data-analysis"></a>Deildu gagnagreiningu

Eftir að þú hefur undirbúið greiningu á flipa geturðu deilt henni sem tengli með vinnufélögum og öðrum í fyrirtækinu þínu beint frá viðskiptavininum. Aðeins viðtakendur sem hafa leyfi fyrir fyrirtækinu og gögnunum geta notað hlekkinn.

1. Á greiningarflipanum, veldu örvarnar niður og veldu síðan **Afrita tengil**.

   ![Sýnir aðgerðina til að afrita greiningu](media/copy-analysis.svg)

    **Tengill á \<tab name\>**  gluggann opnast.

1. Sjálfgefið er að greiningin sem þú deilir tengir við síðuna eða fyrirspurnina í fyrirtækinu sem þú ert að vinna í, sem er gefið til kynna með `company=<company_name>` í vefslóðarreitnum við hliðina á **Afrita** hnappur. Ef þú vilt senda tengil á greiningu sem er ekki tengd tilteknu fyrirtæki skaltu stilla **Fyrirtæki:** reitinn á **Ekki tengja við a tiltekið fyrirtæki**.

   ![Sýnir afritatenglagluggann fyrir greiningarflipa](media/analysis-link-copied.svg)

1. Veldu **Afrita**.

1. Límdu hlekkinn inn í samskiptamiðilinn að eigin vali, eins og Word, Outlook, Teams, OneNote og svo einn. 

2. Eftir móttöku geta viðtakendur síðan valið hlekkinn og opnað greininguna fyrir síðuna eða fyrirspurnina í Business Central. Þeir eru beðnir um að tilgreina nafn fyrir nýja greiningarflipann sem verður búinn til.  

## <a name="limitations-in-2023-release-wave-1-preview"></a>Takmarkanir í útgáfubylgju 1 fyrir 2023 (sýnishorn)

Opinber forsýning á þessum eiginleika hefur eftirfarandi takmarkanir:

- Yfirlit greiningarhamsins hefur hámark 100.000 línur. Ef þú ferð yfir þessi mörk færðu skilaboð sem segja þér það. Til að vinna í kringum þessa takmörkun eru settar síur á síðunni áður en þú skiptir yfir í greiningarham, ef það er mögulegt. Til dæmis, kannski viltu greina ákveðinn hóp viðskiptavina eða vilt aðeins gögn frá yfirstandandi ári. Þú getur líka valið fyrirfram skilgreint útsýni ef það myndi virka fyrir greiningu þína.
- Deilingargagnagreiningareiginleikinn er ekki tiltækur.
- Getan til að vista valin gagnagreiningarval á listasíðum og vista greiningarvalmyndir á greiningarflipa er ekki tiltæk eins og er.

## <a name="see-also"></a>Sjá einnig .

[Tilfallandi gagnagreining](reports-adhoc-analysis.md)  
[Skoða og breyta í Excel](across-work-with-excel.md)  
