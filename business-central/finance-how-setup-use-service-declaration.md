---
title: Setja upp og nota viðbót við þjónustuskýrslu
description: Læra hvernig á að setja upp og nota aðgerðir þjónustuskýrslu (Intrastat for Services) til að tilkynna þjónustuviðskipti við fyrirtæki í öðrum ESB-löndum/svæðum.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# <a name="the-service-declaration-extension"></a>Viðauki þjónustuskýrslu

Í sumum ESB-löndum/svæðum krefjast yfirvöld þess að fyrirtæki tilkynni útflutning þjónustu til annarra ESB-landa/svæða. Viðbót **við þjónustuskýrslu** gerir kleift að safna upplýsingum um þjónustuviðskipti í ESB og tilkynna það stjórnvöldum. Þótt hún sé nefnd þjónustuyfirlýsing **er** einnig hægt að nota hana sem **Intrastat fyrir þjónustu**. Þessi viðauki er tiltækur fyrir öll lönd/svæði í ESB sem W1-útgáfu og hana má nota sem-er í Belgíu. Í öðrum löndum/svæðum þarf að framlengingu sem byggð er á landi/svæði. Ef land/svæði þarf aðeins annað snið er hægt að nota skýrsluskilgreininguna í **Data Exchange Framework** til að breyta sniði.

## <a name="enable-the-service-declaration-extension"></a>Gera þjónustuskýrslu viðbót virka

Þegar viðbótin hefur verið sett upp í umhverfinu þarf að gera hana virka.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Eiginleikastjórnun** og velja síðan viðeigandi tengil.
2. Finna **eiginleika: Gera virka notkun þjónustuskýrslu (Intrastat for Services)** og í reitnum **Virkt fyrir** skal velja **Alla notendur**. Frekari upplýsingar um eiginleikastjórnun hjá [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management) í efni fyrir stjórnendur.
3. Þegar aðgerðin er gerð virk ætti að fylgja skrefum í uppsetningarferlinu í gegnum uppsetningarforritið. Flestir reitir eru sjálfgefið grunnstilltir.
4. Bæta aðeins **við tegundum** þjónustuviðskipta í öðru þrepinu **með því að velja síðuna Opna síðuna Opna þjónustuviðskiptategundir til að tilgreina lista yfir kótavalkosti** .
5. Áður en byrjað er að athuga **heildarfjölda** kóta til að skilja hversu margar þjónustuviðskiptategundir hafa þegar verið tilgreindar.
6. Veljið **Ljúka** í síðasta skrefi til að ljúka skilgreiningunni.

## <a name="set-up-the-service-declaration-extension"></a>Setja upp viðbót við þjónustuskýrslu

Hægt er að setja viðbótina upp handvirkt eða með því að nota skýrsluskrá í Data Exchange skilgreiningum.

### <a name="to-set-up-service-declaration-manually"></a>Þjónustuskýrslur settar upp handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **þjónustuskýrslugrunn og** velja síðan viðeigandi tengil.
2. Á flýtiflipanum **Almennt** eru reitirnir sem lýst er í eftirfarandi töflu grunnstilltir:

    |Svæði  |Heimildasamstæða  |
    |---------|---------|
    |**Skýrslunr. Röð**     | Tilgreinir númeraröðina sem á að nota til að úthluta kenni á nýjar færslur.        |
    |**Kostnaðarauki skýrslu**  | Tilgreinir hvort tilkynna þurfi kostnaðarauka. Ef það er virkt athugar [!INCLUDE [prod_short](includes/prod_short.md)]  þjónustuviðskiptakótinn fyrir kostnaðarauka og tekur þá með í þjónustuskýrslum.        |
    |**Selt-til/Reikn.færist á viðskm.**     | Tilgreinir viðskiptamanninn sem á að nota til að bera landskótann saman við landskótann á síðunni **Stofngögn** . Aðeins fylgiskjöl þar sem þessir tveir kótar eru mismunandi verða tekin með í þjónustuskýrslunni.<br><br>* **Reikningsfærslu:** Landskótinn er notaður úr **reikningsfærsluviðskiptamaðurinn** <br.<br>* **Selt-til.**: Landskótinn er notaður úr **selt-til viðskm**.        |
    |**Nr. afh.aðila/Greiðist lánardr. nr.**  | Tilgreinir hvaða lánardrottinn á að nota til að bera landskótann saman við landskótann á síðunni **Stofngögn** . Aðeins fylgiskjöl þar sem þessir tveir kótar eru mismunandi verða tekin með í þjónustuskýrslunni.<br><br> * **Afh.aðila: Landskótinn er notaður frá lánardrottni** afh.aðila **·**. <br><br> * **Borgunarnr.**: Landskótinn er notaður úr Greiðist **lánardr**.         |
    |**Skilgreiningarkóði gagnaskipta**  | Tilgreinir skilgreiningarkóða gagnaskipta sem er notaður til að mynda útfluttu skrána fyrir þjónustuyfirlýsinguna.        |
    |**Gera skattskráningarnúmer virkt**     |  Tilgreinir hvort skattskráningarnúmerið er tilgreint **.** er virk fyrir þjónustuskýrsluna.       |

3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **tegundir** þjónustuviðskipta og velja síðan viðeigandi tengil.
4. Í línunum eru tilgreindir **kótar** og **lýsingar** á þeim þjónustuviðskiptategundum sem á að nota.

### <a name="set-up-a-reporting-file"></a>Setja upp skýrsluskrá

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **skilgreiningar** gagnaskipta og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Á flýtiflipanum **Almennt** skal lýsa skilgreiningu gagnaskipta með því að tilgreina gagnaskrártegund, dálkskiltákn, tengd codeunit XMLport og fylla út aðra reiti.
4. Á flýtiflipanum **Línuskilgreiningar** skal lýsa sniði lína í gagnaskránni með því að fylla út reitina sem byggðir eru reitnum **Línugerð** og þar þarf að skilgreina fjölda dálka fyrir þessa línu.
5. Á flýtiflipanum **Dálkskilgreiningar** er fyllt út í línuna fyrir hvern fyrirhugaðan dálk.
6. Veldu aðgerðina **Reitavörpun** á flýtiflipanum **Línuskilgreiningar** til að opna síðuna **Reitavörpun**.
7. Ný færsla er stofnuð og á flýtiflipanum **Almennt** skal velja **Kenni töflu**  (fyrir **þjónustuskýrslulínu**, velja **5024**) og fylla svo út reitina sem hér segir:
   1. Í reitnum **Lykillykill** er tilgreindur vísir til að raða upprunafærslum áður en flutt er út.
   2.  **Velja skal Vörpunarkótaunit**.
8. Á flýtiflipanum **Reitavörpun** skal bæta við dálkunum sem áður voru grunnstilltir á flýtiflipanum **Dálkskilgreiningar** og bæta síðan við eftirfarandi:
   1. Tilgreinið **Auðkenni reitar** fyrir hvern dálk.
   2. Tilgreinið **umbreytingarregluna** fyrir hvern dálk eftir þörfum. Reglan umbreytir innleiddum texta í studd gildi áður en hægt er að varpa henni í tilgreindan reit í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar gildi er valið í þessum reit er nákvæmar gildi slegið inn í reitinn **Umbreytingarregla** í töflunni **Biðminni vörpunar gagnaskiptareits** Og öfugt.
9. Til að flokka færslur eftir dálkum á flýtiflipanum **Reitaflokkun** skal velja reitina sem nota á til að flokka.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] Með fyrirframskilgreindri skilgreiningu gagnaskipta fyrir **þjónustuskýrslur** fyrir öll staðfærð lönd/reglugerðir. Fá nánari upplýsingar um stofnun nýrrar gagnaskiptaskilgreiningar í Setja upp skilgreiningar á [gagnaskiptum](across-how-to-set-up-data-exchange-definitions.md).

## <a name="other-related-configurations"></a>Aðrar tengdar stillingar

Áður en þjónustuskýrsluviðbótin er notuð skal grunnstilla suma reiti fyrir vörur, forða og kostnaðarauka.

### <a name="items"></a>Vörur

Setja upp upplýsingar sem tengjast þjónustuskýrslu á birgðaspjaldssíðum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Veldu vöru til að stilla.
3. Stækka **skal flýtiflipann Vara** og grunnstilla eftirfarandi reiti:
   1. Í reitnum **Tegund** skal velja **Þjónusta**.
   2. Í reitnum **Tegund þjónustuviðskipta er** tilgreindur kóti fyrir tegund **þjónustuviðskipta**.
   3. Ef ekki á að taka þessa þjónustuvöru með í þjónustuskýrslum skal velja reitinn **Sleppa þjónustuskýrslu** .

### <a name="resources"></a>Forðar

Setja upp upplýsingar sem tengjast þjónustuskýrslu á forðaspjaldssíðum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Forði** og velja síðan viðeigandi tengil.
2. Valinn er forðinn sem á að grunnstilla.
3. Stækka **skal flýtiflipann Almennt** og grunnstilla eftirfarandi reiti:
   1. Í reitnum **Tegund þjónustuviðskipta er** tilgreindur kóti fyrir tegund **þjónustuviðskipta**.
   2. Ef ekki á að taka þennan forða með í þjónustuskýrslum skal velja reitinn **Sleppa þjónustuskýrslu** .

### <a name="item-charges"></a>Kostnaðaraukar

Setja upp upplýsingar sem tengjast þjónustuskýrslu fyrir kostnaðarauka:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **kostnaðarauka** og velja síðan viðeigandi tengil.
2. Kostnaðaraukinn sem á að grunnstilla er valinn.
3. Í reitnum **Tegund þjónustuviðskipta er** tilgreindur kóti fyrir tegund **þjónustuviðskipta**.
4. Ef ekki á að taka þennan kostnaðarauka með í þjónustuskýrslum er reiturinn **Sleppa þjónustuskýrslu** valinn.

## <a name="create-new-service-declaration"></a>Stofna nýja þjónustuskýrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **þjónustuskýrslur** og velja síðan viðeigandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Á flýtiflipanum **Almennt** eru eftirfarandi reitir fylltir út:
    1. Í glugganum **Skilgreiningargr. Í reitnum Kóti** skal tilgreina grunnstillingarkótann sem er notaður til að leggja til línur og stofna skrár. Velja þarf eina sem **þjónustuskýrslu**.
    2. Í reitunum **Upphafsdagsetning** og **Lokadagsetning** eru tilgreindar upphafs- og lokadagsetningar tímabilsins sem taka á með í þjónustuskýrslunni.
4. Veljið aðgerðina **Leggja til línur** til að hefja keyrslu sem safnar línum úr skjölum og fyllir út þjónustuskýrslulínurnar.

Keyrslan sækir allar færslur úr viðeigandi innkaupa- og söluskjölum á tilskildu tímabili og bætir þeim við þjónustuskýrslulínurnar. Setja yfir reiti í línum til að lesa stutta lýsingu.

## <a name="modify-a-service-declaration"></a>Breyta þjónustuskýrslu

Ef þörf krefur er hægt að breyta línunum eða bæta nýjum við.

1. Á síðunni **Þjónustuskýrsla** skal velja aðgerðina **Ný lína** á flýtiflipanum **Línur** .
2. Í reitnum **Tegund** fylgiskjals er valinn kosturinn sem tengist fylgiskjalinu sem á að nota.
3. Fyllt er út í reitinn **Númer fylgiskjals á grundvelli tegundar** fylgiskjals **.** Ef reiturinn er auður er
4. Eftirstandandi reitir eru fylltir út.

## <a name="overview-the-service-declaration-lines"></a>Yfirlit yfir þjónustuskýrslulínurnar

Þegar þjónustuskýrsla hefur verið stofnuð skal nota yfirlitsaðgerðina **til** að fá yfirlit yfir þjónustuskýrslulínurnar. Hægt er að flokka og taka saman línurnar á sama hátt og útflutta skrá. Einnig er hægt að opna línurnar í Excel.

## <a name="report-service-declaration-in-a-file"></a>Skýrsla þjónustuskýrslu í skrá

Hægt er að senda þjónustuskýrsluna sem skrá sem byggð er á þörfum sveitarfélaga. Til að stofna skrá:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **þjónustuskýrslur** og velja síðan viðeigandi tengil.
2. Velja skal þjónustuskýrsluna sem á að skrá sem skrá.
3. Ef það hefur ekki verið gert er þjónustuskýrslan fyllt út handvirkt eða aðgerðin **Leggja til línur** valin.
4. Aðgerðin **Stofna Skrá** er valin.
5. Þjónustuskýrsluskráin verður vistuð á nauðsynlegu sniði.

## <a name="other-considerations"></a>Önnur atriði

Þegar viðauki þjónustuskýrslunnar **er notaður** þarf að íhuga ýmislegt fleira. Til dæmis er mikilvægt að hóparnir uppfylli kröfur frá yfirvöldum. Einnig er mikilvægt að þjónusta fylgi rétt með sölu- og innkaupaskjölum.

### <a name="grouping-lines"></a>Flokkunarlínur

Í þjónustuskýrslulínum er enginn flokkaður eftir neinum reitum. Allar færslur eru afritaðar úr upprunalega skjalinu sem uppruni.

Flokkun sem yfirvöld krefjast verða gefnar upp í útfluttu skránni. Grunnstilla verður flokkana í skilgreiningu **gagnaskipta** sem er fullkomlega stillanleg. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)

### <a name="using-services-in-document-lines"></a>Notkun þjónustu í skjalalínum

Þegar búinn er til innkaupa-, sölu- eða þjónustureikningur finnur notandi tvo reiti sem tengjast þjónustuskýrslum í línum þeirra. Í báða reitina eru sjálfgildin úr vörunni, forðanum eða kostnaðaraukanum sem sett hafa verið upp.

- **Kóti**  þjónustuviðskiptategundar- Tilgreinir kóta þjónustuviðskiptategundar.
- **Við þjónustuskýrslu** - Tilgreinir hvort vara eða forði eigi við þjónustuskýrslu.

Hægt er að breyta gildum í þessum reitum en ef reiturinn **Jafna þjónustuskýrslu** er valinn þarf að tilgreina gildi í reitnum **Tegund þjónustutegundar** . Ef það er ekki gert er ekki hægt að bóka fylgiskjalið.

Ef tilgreint er gildi í reitnum **Tegundarkóti** þjónustuviðskipta en reiturinn **Tiltækt fyrir þjónustuskýrslu** er ekki valinn er hægt að bóka fylgiskjalið en línan verður ekki reiknuð þegar það er gert.

## <a name="see-also"></a>Sjá einnig .

[Setja upp Intrastat-skýrslugerð](finance-how-setup-report-intrastat.md)
[Intrastat skýrslugerð í Business Central](finance-how-report-intrastat.md)  
[Fjármálastjórnun](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
