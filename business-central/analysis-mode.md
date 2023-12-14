---
title: Greina gögn í listasíðum og fyrirspurnum með gagnamagnagreiningarstillingu
description: Lærðu að nota greiningarmáta gagnagreiningarinnar í miðborg til að greina gögn.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/05/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Greina listasíðu og Fyrirspurnargögn með gagnagreiningum

> **Á við:**  almenn Forskráning í Business mið 2023 út bylgju 1 og síðar til að greina listasíður; Almennt fáanleg í Business Mið 2023 út Wave 2 fyrir greiningu gagna úr listasíðum og fyrirspurnum.

Í þessari grein er hægt að fræðast um hvernig á að greina gögn af listasíðum og fyrirspurnum með  *gagnagagnagreiningarham*. Gagnagreiningarhamurinn gerir kleift að greina gögn beint af síðunni, án þess að láta keyra skýrslu eða skipta öðru forriti eins og Excel. Hún veitir gagnvirka og fjölhæfur leið til að reikna, leggja saman og skoða gögn. Í stað þess að keyra skýrslur með mismunandi valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða Yfirlit á gögnunum. Dæmi gætu verið "mínir Viðskiptavinir", "fylgja eftir vörum", "Nýlega bættust Lánardrottnar", "sölutölur", eða hvaða aðra Sýn sem þú getur ímyndað þér.

> [!TIP]
> Gott um gagnagreiningsham er að hún breytir engum af undirliggjandi gögnum af listasíðu eða fyrirspurn eða útliti síðunnar eða fyrirspurn þegar hún er ekki í gagnagreiningarham. Svo er besta leiðin til að fræðast um hvað hægt er að gera í gagnagreiningunni er að prófa hlutina út.

## Frumskilyrði 

- Ef notast er við aðalútgáfu Viðskiptaseðla 22 er greiningarháttur gagnanna í forskoðun. Admin verður að virkja það áður en hægt er að nota það. Ef gera á hana virka er farið á  **síðuna Feature Management**  og kveikt á  **Uppfærsluuppfærslu: greiningarhamur, greina skal fljótt gögn beint í Business Central**. [Frekari upplýsingar um aðgangsstýringu](/dynamics365/business-central/dev-itpro/administration/feature-management).
- Í útgáfu 23 og síðar verður lykillinn að því  **að fá úthlutað gagnagreiningu-EXEC**  -leyfi eða hafa keyrsluheimild í kerfihlutnum  **9640 leyfa gagnagreinastilling**. Sem admin getur þú útilokað þessar heimildir á notendur sem þú vilt ekki hafa aðgang að í greiningarstillingu.

> [!NOTE]
> Ef til vill er hægt að taka eftir sumum listasíðum sem innihalda  **ekki greina**  Switch fyrir breytingu á greiningarstillingu. Ástæðan er sú að hönnuðir geta gert greiningarhami á tilteknum síðum með því að nota  [eiginleikinn](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property)  analysismodevirkjuð í Al.

## Hefjast handa

1. Opna listasíðuna eða fyrirspurnina.

   Til dæmis, til að vinna með  **síðuna viðskiptamannafærslur**, veljið  ![ stækkunarglerið sem opnar aðgerðina segja mér.](media/ui-search/search_small.png) Táknið (<kbd>Alt</kbd>+<kbd>Q</kbd>), færa inn  *viðskiptamannafærslur* og velja síðan tengda tengilinn. 

2. Í aðgerðstiku efst á síðunni skal kveikja á  **skiptirofa greina** .

    Gagnagreiningarhamur opnar gögnin í upplifun sem bjartsýni er kominn á við greiningu gagna.  Í gagnagreiningu er venjuleg aðgerðrein gerð í stað sérstakrar gagnagreinðarstiku. Eftirfarandi tala sýnir mismunandi svæði á síðu í gagnagreiningunni.

   [![Sýnir yfirlit á síðu á gagnagreiningunni](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Hvert svæði er útskýrt á köflum sem fylgja.

3. Notaðu mismunandi svæði til að vinna úr, leggja saman og greina gögn. Sjá kafla sem fylgja nánari upplýsingum.

4. Ef hætta á við greinistillingu skal slökkva á  **skiptirofanum greina** .

   Fliparnir sem bætt hefur verið við verða að vera þar til þeim er eytt. Svo ef þú skilar gagnagreiningunni aftur þá Sérðu þær nákvæmlega eins og þú skildir þær.

> [!NOTE]
> Gögnin sem birtast í greiningarham stjórnast af afmörkunum eða yfirlitum sem sett eru á listasíðunni. Þannig er hægt að forsía gögn áður en greiningarhamur er færður inn.

## Vinna við gagnagreiningarham

Í gagnagreiningarham er síðunni skipt upp í tvö svið:

- Meginsvæðið, sem samanstendur af gagnasvæði (1), safnrein (2), og flippandi stikum (5)
- Gagnahandleiðslusvæði, sem samanstendur af tveimur rúðum: dálkum (3) og greiningarsíum (4).

### Gagnasvæði (1)

Gagnasvæðið er þar sem raðir og dálkar listasíðufyrirspurnar eru sýnd og gögn eru tekin saman. Gagnasvæðið veitir fjölhæfur hátt til stýringar á útliti dálka og flýtir leið til að fá fram samantekt á gögnunum. Í dálkum sem innihalda tölugildi er Samtala allra gilda í dálkinum sýnd í síðustu röð, nema þegar búið er að skilgreina línuflokka. Í þessu tilfelli birtast samtölur sem Millisamtala fyrir flokkana.  

![Sýnir yfirlit yfir gagnasvæði á síðu í gagnaggreiningarham](media/analysis-mode-data-area.png)

- Til að hreyfa dálk skaltu velja hann og draga hann að þar sem þeir gera vit í greinunum.
- Hægrismelltu á dálkinn eða sveininn yfir honum og veldu valmyndartáknið ![Sýnir táknið í dálki í gagnaggreiningarham sem opnar valmynd fyrir aðgerðir](media/analysis-mode-column-menu-icon.png) Til að fá aðgang að nokkrum aðgerðum sem hægt er að gera í dálkum. Dæmi:

  - Til að pinna dálk vinstra eða hægra megin við Gagnasvæðið þannig að hann fari ekki af skjánum þegar Skrunað er velurðu  ![ sýnir táknið á dálki í gagnaggreiningarham sem opnar valmynd fyrir aðgerðir ](media/analysis-mode-column-menu-icon.png) > **pinna dálkapin** > **vinstri**  dálkahluta.
  - Skilgreinið gagnasíur beint á dálkskilgreininguna í stað þess að fara í  **Greiningarsíurúður** . Enn er hægt að gægjast inn í upplýsingar um tengd gögn og hverja línu og opna spjald til að fræðast nánar um gefna einingu.
- Nota Gagnasvæðið til samskipta við gögnin. Í dálkum sem innihalda tölulegt, samantekt gildi er hægt að fá lýsandi tölfræði um mengi reita með því að merkja þau. Tölfræðin birtist í stöðulínum (2) ásamt neðst á síðunni.
- Flytja út gögn í Excel eða CSV sniði. Hægrismellið á Gagnasvæðið eða úrval af frumum til að flytja út.

### Safnstika (2)

Samantektarstikunni er meðfram neðst á síðunni og birtir tölulegar upplýsingar um gögnin á listasíðunni eða fyrirspurninni. Þegar þú hefur samskipti við dálka sem hægt er að leggja saman gildi eins og að velja margar raðir í dálki sem sýna upphæðir, uppfærsla á gögnum.

![Sýnir yfirlit yfir yfirlitstikuna á greiningarstillingu gagnanna](media/analysis-mode-totals-row.png)

Eftirfarandi tafla lýsir þeim mismunandi tölum sem sýndar eru í svæðinu samtölur:

|Fjöldi|Heimildasamstæða|
|-|-|
|Línur|Fjöldi valinna lína sem hluti af heildarfjölda tiltækra raða. |
|Heildarlínur|Númer lína í ósíaða listanum eða fyrirspurninni.|
|Afmarkað|Fjöldi lína sem birtar eru í kjölfar afmörkunar sem beitt var á listann eða fyrirspurnina.|
|Meðaltal|Meðaltalsgildið í öllum völdu samantektanlegu svæðunum.|
|Talning|Fjöldi valinna lína.|
|Lágmark|Lágmarksgildið í öllum völdu samanbrjótanlegur svæðunum.|
|Hámark|Hámarksgildið í öllum völdu samantektanlegu svæðunum.|
|Samtala|Samtala allra gilda í völdu samanbrjótanlegur-svæðunum.|

### Dálkar (3)

 **Dálkarnir**  eru annað af tveimur rúðum sem vinna saman að því að skilgreina greinina. Hitt svæðið er í  **greiningarsíuúðunni** .  **Dálkarnir**  rúða eru notaðir til að draga saman gögn.  **Notið rúðuna dálkar**  til að skilgreina hvaða dálkar eigi að taka með í greiningunni.

![Sýnir yfirlit yfir dálka rúðu í gagnagreinarstillingu](media/analysis-mode-columns-2.png)

|Svæði|Heimildasamstæða|
|-|-|
|Leita/tékka eða hreinsa alla reiti|Leita í dálkum. Veljið gátreitinn til að velja/hreinsa alla dálka.|
|Gátreiti|Þetta svæði inniheldur gátreit fyrir hvert svæði í upprunatöflu listans eða fyrirspurnar. Notið þetta svæði til að breyta hvaða dálkar eru sýndir. Veljið gátreitinn til að Sýna dálk fyrir svæðið á síðunni; Hreinsið gátreitinn til að hylja dálkinn. |
|Línuflokka|Nota þetta svæði til að flokka og samtölugögn við eitt eða fleiri svæði. Aðeins er hægt að taka með svæði sem ekki eru töluverð, líkt og texti, dagsetningar og tími. Línuflokkar eru oft notaðir í Pivot ham.|
|Gildi|Notið þetta svæði til að tilgreina svæði sem óskað er samtölu fyrir. Aðeins er hægt að taka reiti sem innihalda tölur sem hægt er að bæta saman; til dæmis ekki texta, dagsetningu eða tímasvæði.|

Til að færa svæði af einu svæði yfir á annað þarf að velja graf-teiknið ![Sýnir yfirlit á síðu á greiningarhamnum](media/column-grab-icon.png) Næst dálkinum í listanum og draga inn í marksvæðið. Þú ert hindraður í að flytja svæði inn á svæði þar sem ekki er leyfilegt.

### Greiningarafmarkanir (4)

Í  **rúðunni greiningarafmarkanir**  er hægt að setja frekari gögn afmarkanir á dálka til að takmarka færslur á listanum. Setja afmarkanir á dálka til að takmarka færslur á listanum og síðari samtölur við aðeins þær færslur sem notandi hefur áhuga á samkvæmt forsendum sem notandi skilgreinir. Til dæmis, Segjum að þú hafir aðeins áhuga á gögnum fyrir tiltekinn viðskiptavin eða sölupantanir sem fara yfir ákveðna upphæð. Til að setja afmörkun skal velja dálkinn, velja samanburðaraðgerðina úr listanum (eins og  **jafnan**  eða  **byrja** á) og færa síðan inn gildið.

![Sýnir yfirlit afmörkunar rúðu í greiningarhamnum](media/analysis-mode-filters.png)

> [!NOTE]
> Viðbótarafmarkanir eiga aðeins við um gildandi greiningarflipa. Þannig er hægt að skilgreina nákvæmlega þær aukagögurnar sem þarf til tiltekinnar greiningar.

### Fliparnir (5)

Svæðið á flipunum efst gerir kleift að stofna mismunandi afbrigði (dálka og greiningarsíur) á öðrum flipum, þar sem hægt er að vinna gögn á flipunum óháð hvort öðru. Það er alltaf minnst einn flipi, sem heitir  **Greining 1**, sjálfgefið. Þegar fleiri flipar eru notaðir er gagnlegt að vista notaðar skilgreiningar á gagnammengi. Til dæmis gætu verið flipar til að greina gögn í Pivot-hamnum og öðrum flipum sem afmarka að hlutmengi raða. Sumir flipar gætu sýnt nákvæmt yfirlit með mörgum dálkum og aðrir birta aðeins nokkra lykildálka.

Hér er bent á að vinna með marga greiningarflipa:

- Ef bæta á við nýjum flipa er stóra  **+**  táknið valið næst á flipanum Síðasta Greining.
- Veljið örhveið á flipanum til að fá aðgang að lista yfir aðgerðir sem hægt er að gera á flipanum, eins og endurnefna, afrita, eyða og færa.

   - **Eyða**  eyðir flipanum sem opin er núna. **Eyða öllum**  eyðir öllum flipum sem bætt hefur verið við, nema flipann sjálfgefinn  **greiningar1** .
- Þú getur ekki alveg fjarlægt  **greininguna 1**, en þú getur endurnefnt hana með því að  **nota endurnefna**  aðgerð og hreinsað breytingarnar sem þú hefur gert með því að nota  **DELETE**  eða  **Eyða öllu**.  

- Fliparnir sem bætt hefur verið við og samskipaðir verða þar til þeim er eytt. Svo ef þú skilar gagnagreiningunni aftur þá Sérðu þær nákvæmlega eins og þú skildir þær.

   > [!TIP]
   > Fliparnir sem þú setur upp eru aðeins sýnilegir þér. Aðrir notendur munu aðeins sjá flipa sem þeir hafa sett upp.
- Hægt er að afrita greiningarflipa. Afritun getur verið gagnleg ef gera á tilraunir með að breyta um flipa án þess að breyta upprunalegu, eða ef stofna á mismunandi afbrigði sömu greiningar.


## Stigveldi dagsetningar

Í greiningarham eru dagsetningarreitir gagnagreiningarinnar myndaðar í Fjórðungsþrepum þriggja mánaða í þremur aðskildum reitum. Þetta stigveldi er byggt á venjulegri dagbók, ekki neinum fjárhagsdagatölum sem skilgreindir eru í Viðskiptamiðinu.

Auksvæðin eru nefnd  _\<field name\>  ár_,  _\<field name\>  ársfjórðungur_ og  _\<field name\>  mánuður_. Ef DataSet inniheldur til dæmis svæði sem heitir  _Bókunardagsetning_ er samsvarandi dagsetningastigveldi samsett úr reitum sem kallast  _bókunardagsetning, ár_,  _Dagsetningardagur_ og  _Bókunardagsetning mánuður_.

> [!NOTE]
> Dagsetningastigveldið eins og gildir aðeins um svæði af gerðinni dagsetning, ekki fyrir svæði af gerðinni DateTime.

## Völvustilling

Hægt er að nota Pivot ham til að greina mikið magn tölulegra gagna, undirsamantekt gagna eftir flokkum og undirflokkum. Völvuhamurinn er eins og  [veltitöflur í Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Ef snúa á völvustillingu á og af skal Skyggnið  **á Pivot Mode**  rofna í  **dálka**  rúðunni (3). Þegar kveikt er á völvustillunni  **birtist dálkmerkin**  á svæðinu í rúðunni.  **Notaðu svæðið dálkmerki**  til að flokka samtölur fyrir línur í flokka. Reitir sem bætt  **er á svæði dálkamerkinga**  Sýna sem dálka í gagnasvæði (1).

Að byggja upp gagnagreiningu í Pivot ham felst að færa reiti inn á þrjú svið:  **röð flokka**,  **dálka merki** og  **gildi**. Eftirfarandi mynd sýnir hvar Reitirnir eru í gagnasvæðinu (1), þar sem  `sum`  eru útreiknuðu gögnin, og valfrjálst  **gildi**.

<table>
<tr><th></th><th>Dálksmerki</th><th></th><th>Dálksmerki</th><th></th></tr>
<tr><th>Línuflokki</th><th>Virði</th><th>Virði</th><th>Virði</th><th>Virði</th></tr>
<tr><td>lína</td><td>Summar</td><td>Summar</td><td>Summar</td><td>Summar</td></tr>
<tr><td>lína</td><td>Summar</td><td>Summar</td><td>Summar</td><td>Summar</td></tr>
<tr><td>lína</td><td>Summar</td><td>Summar</td><td>Summar</td><td>Summar</td></tr>
<tr><td>lína</td><td>Summar</td><td>Summar</td><td>Summar</td><td>Summar</td></tr>
</table>

> [!TIP]
> Dálkar sem aðeins hafa nokkur hugsanleg gildi eru bestu frambjóðendur fyrir notkun í **dálkagildunum**.


## Greina mikið gagnamagn

Ef gagnasettið sem óskað er eftir að greina fer yfir 100.000 línur er lagt til að greiningarhamurinn verði færður inn sem bjartsýni á mikið gagnasafn. Nú eru tvær takmarkanir Ef skipt er í þennan ham: 

- Snið reita af eftirfarandi fjórum gagnagerðum gætu breyst: 

   - gjaldmiðli 
   - Aukastöfum (alltaf sýnt með tveimur aukastöfum) 
   - Dagsetningar (alltaf sýndar í sniðinu YYYY-MM-DD)
   - tímabeltum
- Reitir sem eru notaðir í Pivot stillingu og bætast við dálkamerkingar verða að hafa lágan fjölda aðgreinra gilda.

   Ef Pivot ham er gerð virk og svæði er virkjað í  **svæði dálkanna**, þar sem undirliggjandi gögn í reitnum eru með of mörgum greinargóðum gildum, gæti vafraflipinn í vafranum orðið óraunvirkur og hann lokast, sem krefst þess að byrjað sé á nýrri lotu. Í þessu tilfelli á annaðhvort ekki að velkja á þeim reit eða setja afmörkun á svæðið áður en þeim er bætt  **á svæði fyrir dálkamerkingar** .

## Deila gagnagreiningu

Þegar búið er að útbúa greiningu á flipanum er hægt að samnýta hana sem tengil með starfsmönnum og öðrum í fyrirtækinu beint af biðlaranum. Einungis viðtakendur sem hafa leyfi til fyrirtækisins og gögnin geta nýtt sér tengilinn.

1. Á flipanum greining er gátreiturinn Down arrowhead valinn og síðan er valið  **Afrita tengill**.

   ![Sýnir aðgerðina til að afrita greiningu](media/copy-analysis.svg)

    **Hlekkurinn í  \<tab name\>**  svargluggann opnast.

1. Sjálfgefið er að greiningin sem þú deilir með því að tengja síðuna eða fyrirspurnina í fyrirtækinu sem þú ert að vinna í, sem er tilgreind með því  `company=<company_name>`  að í REITNUM vefslóð er við hliðina  **á hnappnum afrita** . Ef senda á tengil í greiningu sem er ekki tengt tilteknu fyrirtæki, Stillið  **fyrirtæki:**  svæðið á  **ekki að tengjast tilteknu fyrirtæki**.

   ![Sýnir svarglugga afritunartengils á flipanum Greining](media/analysis-link-copied.svg)

1. Velja  **eintak**.

1. Líma tengilinn inn á samskiptamiðlana að eigin vali, eins og Word, Outlook, teymið,  OneNote og svo eitt. 

2. Þegar það er móttekið geta viðtakendur síðan valið tengilinn og opnað greinina fyrir síðuna eða fyrirspurn í aðalvefsíðu. Beðið er um að tilgreina heiti fyrir nýja greiningarflipann sem verður stofnaður.  

## Takmarkanir í 2023 losun öldu 1 (Forskoðun)

Með almennu forskotinu hefur eftirfarandi takmörkunum verið fylgt:

- Greiningarhamsyfirlitið hefur takmörk á 100.000 raðir. Ef þú fer yfir þessi mörk færðu skilaboð um að segja þér það. Ef vinna á þessa takmörkun er sett sía á síðuna áður en skipt er yfir í greiningarham, ef það er mögulegt. Til dæmis er kannski ætlunin að greina ákveðinn hóp viðskiptavina eða aðeins gögn frá yfirstandandi ári. Einnig er hægt að velja fyrirfram skilgreint úrtak ef það myndi vinna greinina.
- Aðgerðin Samnýting gagnagreininga er ekki tiltæk.
- Möguleikinn á að vista æskilegan valmöguleika gagnagreiningar á listasíðum og vista greiningarvalmynd á greiningarflipa er ekki tiltækur.

## Sjá einnig .

[Tilfallandi gagnagreining](reports-adhoc-analysis.md)  
[Skoða og breyta í Excel](across-work-with-excel.md)  
