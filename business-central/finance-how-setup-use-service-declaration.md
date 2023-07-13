---
title: Setja upp og nota viðauka Þjónustuskýrslu
description: Lærðu að setja upp og nota Þjónustuskýrslu (Intrastat for Services) aðgerðir til að skrá þjónustuviðskipti við fyrirtæki í öðrum ESB-löndum/-svæðum.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# <a name="the-service-declaration-extension"></a>Framlenging á Þjónustuskýrslu

Í sumum ESB-löndum/svæðum krefjast yfirvöld þess að fyrirtæki geri skýrslu um útflutning þjónustu í öðrum ESB-löndum/-svæðum. Með  **viðauka Þjónustuskýrslunnar**  er hægt að safna upplýsingum um þjónustuviðskipti innan ESB og tilkynna það yfirvöldum. Þrátt fyrir að hún sé nefnd  **Þjónustuskýrsla**, er einnig hægt að nota hana sem  **Intrastat fyrir þjónustu**. Þessi framlenging er fáanleg fyrir öll ESB löndin/svæðin sem W1 gáfu og það er hægt að nota as-is í Belgíu. Fyrir önnur lönd/svæði verður að krefjast nafnauka á grundvelli lands/svæðis. Ef land/svæði þarf aðeins annað snið er hægt að nota skýrsluskilgreininguna í  **Rammaskrárgengi**  til að breyta sniðinu.

## <a name="enable-the-service-declaration-extension"></a>Gera viðauka Þjónustuskýrslu virka

Þegar búið er að setja upp endingu í umhverfi þarf að virkja hann.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **aðgangsstjórnun** og veljið síðan tengda tengilinn.
2. Finna  **eiginleika: leyfa notkun Þjónustuskýrslu (Intrastat fyrir þjónustur)** og í  **reitnum virkt fyrir**  svæðið skal velja  **alla notendur**. Frekari upplýsingar um eiginleikastjórnun hjá [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management) í efni fyrir stjórnendur.
3. Þegar aðgerðin er gerð virk ætti að fylgja skrefum í uppsetningarforritinu í gegnum uppsetningarforritið. Sjálfgefin svæði eru sjálfkrafa skilgreind.
4. Bæta aðeins  **við gerðir**  þjónustufærslna í seinna skrefinu með því að  **Velja opna síðuna þjónustufærslugerðirnar til að tilgreina valkostalistann** .
5. Áður en hafist er handa er athugað með  **heildarfjölda kóða**  til að skilja hversu margar gerðir þjónustufærslna hafa þegar verið tilgreindar.
6. Velja  **Ljúka**  í síðasta skrefi til að ljúka skilgreiningunni.

## <a name="set-up-the-service-declaration-extension"></a>Setja upp viðauka Þjónustuskýrslu

Hægt er að setja upp viðauka handvirkt eða með því að nota skýrslugerðarskrá í skilgreiningum á gögnum.

### <a name="to-set-up-service-declaration-manually"></a>Að setja upp Þjónustuskýrslu handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **uppsetningu** þjónustuskýrslu og veljið síðan tengda tengilinn.
2.  **Á flipanum Almennt**  skal skilgreina svæðin sem lýst er í eftirfarandi töflu:

    |Svæði  |Heimildasamstæða  |
    |---------|---------|
    |**Röð í skýrslu nr.**     | Tilgreinir númeraröðina sem nota á til að úthluta kennum á nýjar færslur.        |
    |**Kostnaðargjöld skýrslu**  | Tilgreinir hvort tilkynna verður kostnaðarauka. Ef virkjað,  [!INCLUDE [prod_short](includes/prod_short.md)]  athugar þjónustufærslukóðann fyrir kostnaðarauka og tekur þá með í þjónustuskýrslum.        |
    |**Viðskm. reikn.**     | Tilgreinir viðskiptamanninn sem á að nota til að bera saman landskóta sinn við landakóða á  **upplýsingasíðu**  fyrirtækisins. Aðeins skjöl þar sem þessir tveir kótar eru mismunandi verða teknir með í þjónustuskýrslu.<br><br>* **Frumvarp til.: nota landskóta úr** Reikn-til viðskm  **.**  < br<br>* **Selt-til.** : Notið landskóta frá  **Selt-til-viðskiptavininum**.        |
    |**Afh. aðila/borgun-nr.**  | Tilgreinir hvaða lánardrottinn á að nota til að bera saman landskóta sinn við landskóta á  **síðu fyrirtækjaupplýsinga** . Aðeins skjöl þar sem þessir tveir kótar eru mismunandi verða teknir með í þjónustuskýrslu.<br><br> * **Afh.** aðila: nota skal landskóta frá  **lánardrottni** afh. <br><br> * **Borgun.** : nota skal landskótann úr  **Launadrottinn**.         |
    |**Skilgreiningarkóði gagnaskipta**  | Tilgreinir skilgreiningarkóða gagnaskipta sem er notaður til að mynda útfluttu skrána fyrir þjónustuyfirlýsinguna.        |
    |**Virkja skattskráningu nr.**     |  Tilgreinir hvort  **skattskráningarnúmer** er virkjaður fyrir þjónustuskýrsluna.       |

3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Þjónustufærslugerðir** og velja síðan tengda tengilinn.
4. Í línunum eru tilgreindir  **kótar**  og  **lýsingar**  á þjónustufærslugerðunum sem eru notaðar.

### <a name="set-up-a-reporting-file"></a>Setja upp skýrsluskrá

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **upplýsingar um Gengisskilgreiningar** og velja síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3.  **Á flipanum Almennt**  skal lýsa gagnaskiptaskilgreiningu með því að tilgreina gerð gagnaskráa, skiltákn í tengslum við kódeunits,  XMLport og fylla út hina reitina.
4. Á flýtiflipanum **Línuskilgreiningar** skal lýsa sniði lína í gagnaskránni með því að fylla út reitina sem byggðir eru reitnum **Línugerð** og þar þarf að skilgreina fjölda dálka fyrir þessa línu.
5. Á flýtiflipanum **Dálkskilgreiningar** er fyllt út í línuna fyrir hvern fyrirhugaðan dálk.
6. Veldu aðgerðina **Reitavörpun** á flýtiflipanum **Línuskilgreiningar** til að opna síðuna **Reitavörpun**.
7. Stofnið nýja færslu og á  **flipanum Almennt**  skal velja  **töflukennið**  (fyrir  **þjónustuskýrslu**, velja  **5024**) og fyllið síðan út reitina á eftirfarandi hátt:
   1.  **Í reitnum Lyklavísitala**  skal tilgreina lyklavísi til að raða upprunafærslunum eftir á fyrir útflutning.
   2.  **Veljið vörpun Kódeseiningar**.
8.  **Á flipanum Flýtivörpun**  í svæðið skal bæta við dálkunum sem áður voru skilgreindir í  **fastflipa Dálkaskilgreininganna**  og bæta svo eftirfarandi við:
   1. Tilgreinið **Auðkenni reitar** fyrir hvern dálk.
   2.  **Tilgreinið umbreytingarregluna**  fyrir hvern dálk eftir þörfum. Reglan umbreytir innfluttum texta í studd gildi áður en hægt er að tengja hann við tiltekið svæði í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar gildi er valið í þessum reit er nákvæmar gildi slegið inn í reitinn **Umbreytingarregla** í töflunni **Biðminni vörpunar gagnaskiptareits** Borð, og öfugt.
9. Til að flokka færslur út frá dálkum, á  **flipanum svæði flokkun**, veljið þá reiti sem nota á við flokkun.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] kemur með fyrirframskilgreinda gagnaskiptaskilgreiningu fyrir  **Þjónustuskýrslu**  fyrir öll staðbundin lönd/regioins. Frekari upplýsingar um stofnun nýrra Gagnaskiptaskilgreininga á að setja upp skilgreiningar  [á](across-how-to-set-up-data-exchange-definitions.md) gagnaskiptum.

## <a name="other-related-configurations"></a>Aðrar tengdar stillingar

Áður en notuð er framlenging á Þjónustuskýrslu skal samskipa nokkur svæði fyrir vörur, forða og Vörugjöld.

### <a name="items"></a>Vörur

Setja upp upplýsingar sem tengjast Þjónustuskýrslu á Vöruspjaldssíðum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Veldu vöru til að stilla.
3.  **Útvíkkið vöruflipann**  og Skilgreinið eftirfarandi reiti:
   1.  **Í reitnum Tegund**  er valin  **þjónusta**.
   2.  **Í reitnum kóti**  þjónustufærslu er tilgreindur kóti  **þjónustufærslugerðar**.
   3. Ef ekki á að taka þessa þjónustuvöru með í þjónustuskýrslum er reiturinn útiloka frá Þjónustuskýrslu  **valinn** .

### <a name="resources"></a>Forðar

Setja upp upplýsingar sem tengjast Þjónustuskýrslu á Forðaspjaldssíðum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **tilföng** og velja síðan tengda tengilinn.
2. Velja skal tilfang sem á að samskipa.
3.  **Útvíkkið almenna**  fastflipann og Skilgreinið eftirfarandi reiti:
   1.  **Í reitnum kóti**  þjónustufærslu er tilgreindur kóti  **þjónustufærslugerðar**.
   2. Ef ekki á að taka þennan forða með í þjónustuskýrslum er reiturinn útiloka frá Þjónustuskýrslu  **valinn** .

### <a name="item-charges"></a>Kostnaðaraukar

Setja upp upplýsingar sem tengjast Þjónustuskýrslu fyrir Vörugjöld:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **kostnaðarauka** og velja síðan tengda tengilinn.
2. Velja þann kostnaðarauka sem á að samskipa.
3.  **Í reitnum kóti**  þjónustufærslu er tilgreindur kóti  **þjónustufærslugerðar**.
4. Ef ekki á að taka þennan kostnaðarauka með í þjónustuskýrslum er reiturinn útiloka frá Þjónustuskýrslu  **valinn** .

## <a name="create-new-service-declaration"></a>Stofna nýja þjónustuskýrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **þjónustuskýrslur** og veljið síðan tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.
3.  **Á flipanum Almennt**  skal fylla út eftirfarandi reiti:
    1.  **Í Config.** Er tilgreindur Skilgreiningarkóði sem notaður er til að leggja línur og stofna skrár. Þú þarft að velja eina sem  **Þjónustuskýrslu**.
    2.  **Í reitunum Upphafsdagsetning**  og  **Lokadagsetning**  er upphafs-og lokadagsetningar tímabilsins sem á að hafa með í þjónustuskýrslu tilgreindar.
4. Velja skal  **aðgerðina leggja til línur**  til að ræsa runuvinnslu sem safnar línum úr skjölum og fyllir út línur í þjónustuskýrslu.

Keyrslan sækir allar færslur í viðeigandi innkaupa-og söluskjölum á tímabilinu sem þarf og bætir þeim við í þjónustunúmeralínunum. Sveima yfir reiti í línum til að lesa stutta lýsingu.

## <a name="modify-a-service-declaration"></a>Breyta þjónustuskýrslu

Ef þörf krefur er hægt að breyta línunum eða bæta við nýjum.

1.  **Á síðunni Þjónustuskýrsla**  skal velja  **nýju línuaðgerðina**  í  **fastflipanum línur** .
2.  **Í reitnum Tegund**  fylgiskjals er valinn valkosturinn sem tengist fylgiskjalinu sem nota á.
3.  **Á grundvelli skjalgerðarinnar** er fyllt út í reitinn  **Fylgiskjal nr.** sviði.
4. Eftirstandandi reitir eru fylltir út.

## <a name="overview-the-service-declaration-lines"></a>Yfirlit yfir línur þjónustuskýrslu

Eftir að þjónustuskýrsla hefur verið stofnuð er aðgerðin Yfirlit  **notuð**  til að fá yfirlit yfir þjónustulínur. Hægt er að flokka og draga saman línurnar á sama hátt og útfluttu skrána. Einnig er hægt að opna línurnar í Excel.

## <a name="report-service-declaration-in-a-file"></a>Skýrsluþjónustuskýrsla í skrá

Hægt er að senda þjónustuskýrsluna sem skrá sem byggir á mismunandi þörfum sveitarfélaga. Til að stofna skrá:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn  **Þjónustuskýrslur** og velja síðan tengda tengilinn.
2. Velja skal þá þjónustuskýrslu sem á að skrá í skrána.
3. Ef þú hefur ekki þegar gert það, fylltu þá út þjónustuskýrsluna handvirkt eða veldu  **aðgerðina leggja til línur** .
4. Aðgerðin **Stofna Skrá** er valin.
5. Þjónustuskýrsluna verður vistað með tilskildum sniði.

## <a name="other-considerations"></a>Önnur atriði

Þegar þú ert að nota  **viðauka Þjónustuskýrslunnar**  þá er ýmislegt sem þarf að huga að. Það er til dæmis mikilvægt að hóparnir njóti þarfa frá yfirvöldum. Það er einnig mikilvægt að þjónustur séu rétt settar á sölu-og innkaupaskjöl.

### <a name="grouping-lines"></a>Flokkunarlínur

Í þjónustuskýrslu er engin flokkun eftir neinu svæði. Allar færslur eru afritaðar úr upprunalega skjalinu sem Uppruni.

Flokkun sem yfirvöld krefjast verða gefnar upp í útfluttu skránni. Skilgreina þarf flokkana í  **Gagnaskiptaskilgreiningunni** sem er fyllilega skilgreinanleg. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)

### <a name="using-services-in-document-lines"></a>Notkun þjónustu í skjalalínum

Þegar stofnuð er innkaupa-, sölu-eða Þjónustureikningur er hægt að finna tvo reiti sem tengjast þjónustuskýrslum í línunum sínum. Bæði svæðin eru fyllt út með sjálfgefnum gildum úr vöru-, forða-eða vörugjaldi sem stillt er á ups.

- **Kóti**  þjónustufærslugerðar-Tilgreinir kóta fyrir gerð þjónustufærslu.
- **Á við um Þjónustuskýrslu**  -Tilgreinir hvort vara eða Forði eigi við þjónustuskýrslu.

Hægt er að breyta gildunum í þessum reitum en ef valið er svæðið sem  **á við fyrir Þjónustuskýrslu**  þarf að tilgreina gildi í  **reitnum kóti**  þjónustufærslu. Ef ekki, þá er ekki hægt að bóka skjalið.

Ef tilgreint er gildi í  **reitnum kóti**  þjónustufærslu en ekki á  **við valið fyrir reitinn þjónustuskýrsla**  er hægt að bóka skjalið en línan verður ekki reiknuð þegar það er gert.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Set Up Intrastat Reporting](finance-how-setup-report-intrastat.md)
[Intrastat Reporting in Business Central](finance-how-report-intrastat.md)  
[Fjármálastjórnun](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
