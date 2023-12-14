---
title: Stofna birgðaspjald fyrir vörur eða þjónustu (inniheldur myndskeið)
description: Þú býrð til birgðaspjöld fyrir þjónustu sem þú selur sem klukkutíma og fyrir efnislegar vörur. Sem dæmi má nefna samsetningaríhluti og fullbúnar vörur sem þú selur úr birgðum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 11/02/2022
ms.author: bholtorf
---
# <a name="register-new-items"></a>Skrá nýjar vörur

Vörur, ásamt öðrum framleiðsluvörum, eru grundvöllur fyrirtækisins, vörurnar eða þjónustan sem þú stundar viðskipti með. Hver vara verður að vera skráð sem birgðaspjald.

Birgðaspjald inniheldur upplýsingarnar sem þarf til að kaupa, selja, geyma og tilkynna vörur.

Birgðaspjaldið getur verið af gerðinni **Birgðir**, **Þjónusta** eða **Ekki birgðir** til að tilgreina hvort vara er raunbirgðaeining, launatímaeining eða efnisleg eining sem ekki er rakin í birgðum. Nánari upplýsingar er að finna í [Um vörugerðir](inventory-about-item-types.md).

Hlutur getur verið uppbyggður sem yfireining með undirliggjandi undireiningu í uppskrift. Frekari upplýsingar um samsetningaruppskriftir og framleiðsluuppskriftir er að finna í [Vinna með uppskriftir](inventory-how-work-BOMs.md).

Ef sama varan er keypt frá fleiri en einum lánardrottni, er hægt að tengja þessa lánardrottna við birgðaspjaldið. Síðan **Vörusölulisti**  sýnir lánardrottnana, þannig að þú getur auðveldlega valið annan söluaðila.

*Vörulistaatriði* eru vörur sem þú býður viðskiptamönnum þínum en þú vilt ekki hafa umsjón með þeim í kerfinu fyrr en þú byrjar að selja þær. Vörulistaatriði eru ekki venjulega vörur af gerðinni **Ekki í birgðum**. Frekari upplýsingar eru í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Ef vörusniðmát er til fyrir mismunandi vörutegundir, þá birtist síða þar sem búið er til nýtt birgðaspjald og hægt er að velja viðeigandi sniðmát. Ef aðeins eitt vörusniðmát er fyrir hendi, nota ný birgðaspjöld alltaf það sniðmát.

Eftirfarandi ferli skýrir hvernig á að búa til birgðaspjald frá grunni. Einnig er hægt að búa til ný birgðaspjöld með því að afrita birgðaspjald sem þegar er til staðar. Frekari upplýsingar er að finna í [Afrita fyrirliggjandi vörur í Búa til nýjar vörur](inventory-how-copy-items.md).  

<br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Að búa til nýtt vöruspjald

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> Í reitnum **Aðferð kostnaðarútreiknings** seturðu upp hvernig kerfið reiknar út kostnaðarverð með því að áætla vöruflæði fyrirtækisins. Fimm aðferðir kostnaðarútreiknings eru í boði, út frá gerð vörunnar. Nánari upplýsingar eru í [Upplýsingar um hönnun: Kostnaðarútreikningar](design-details-costing-methods.md).
>
> Ef þú velur **Meðaltal** er kostnaðarverð vöru reiknað sem meðaleiningaverð vara á hverjum tímapunkti eftir innkaup. Fyrir verðmat birgða, er gert ráð fyrir að allar birgðir verði seldar á sama tíma. Með þessar stillingar geturðu valið **kostnaðarverð** reitinn á síðunni **Meðalkostnaður útreiknaður yfirlit** til að skoða færslusöguna sem meðalkostnaður er reiknaður út frá.

Þú getur skoðað eða breytt sérstöku verði eða afslætti sem þú veitir, eða sem söluaðili þinn veitir þér, fyrir vöruna Ef tiltekin skilyrði eru uppfyllt, eins og viðskiptavinur, lágmarkspöntun eða lokadagsetning. Þetta er gert með því að velja **Stilla sérverð** eða **Stilla sérstaka afslætti**. Hver lína á, til dæmis á síðunni **Söluverð**, sýnir sértækt verð. Hver dálkur táknar viðmiðun sem verður að uppfylla til að veita viðskiptamanni sérverð sem þú slærð inn í **Einingaverð** reitinn á síðunni **Söluverð**. Frekari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md) eða [Skrá sérstakt söluverð og sérstaka afslætti](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Varan hefur nú verið skráð og birgðaspjaldið má nú nota í skjölum vegna kaupa og sölu.

Ef nota á þetta birgðaspjald sem sniðmát þegar ný birgðaspjöld eru búin til, vistið það sem sniðmát. Nánari upplýsingar eru í eftirfarandi kafla.  

### <a name="to-save-the-item-card-as-a-template"></a>Til að vista birgðaspjald sem sniðmát

1. Á síðunni **Birgðaspjald** skal velja aðgerðina **Vista sem sniðmát**. Síðan **Vörusniðmát** opnast og sýnir birgðaspjaldið sem sniðmát.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir vöruna.
4. Breyttu eða sláðu inn víddarkóða sem eiga við um ný vöruspjöld búin til með því að nota sniðmátið.
5. Þegar þú hefur lokið við nýja vörusniðmátið skaltu velja **OK** hnappinn.

Vörusniðmátinu verður bætt við lista vörusniðmáta þannig að hægt er að nota það til að búa til ný birgðaspjöld.

### <a name="items-used-in-production-orders"></a>Vörur notaðar í framleiðslupöntunum

Ef skrá á vörur sem eru notaðar í framleiðslupöntunum er áfyllingarkerfið tilgreint sem *Framl. pöntun* á flipanum **Áfylling**. Frekari upplýsingar eru í [Um framleiðslupantanir](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Margir lánardrottnar settir upp fyrir vörur

Ef sama varan er keypt frá fleiri en einum lánardrottni þarf að færa inn upplýsingar um hvern lánardrottinn eins og verð, afhendingartími, afsláttur o.s.frv.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Velja skal viðeigandi vöru og síðan aðgerðina **Breyta**.  
3. Veljið **Lánardrottinn** aðgerðina.  
4. Velja reitinn **Nr. lánardrottins** og síðan velja þann lánardrottinn sem setja á upp fyrir vöruna.  
5. Einnig er hægt að fylla inn í þá reiti sem eftir eru.  
6. Endurtakið skref 2 til 5 fyrir hvern þann lánardrottinn sem þú vilt kaupa vöru af.

Lánardrottnar birtast á síðunni **Vörusölulista**, sem þú opnar af vöruspjaldinu, þannig að þú getur auðveldlega valið annan söluaðila.

## <a name="set-up-item-substitutions"></a>Setja upp staðgengilsvörur

Þú getur sett upp vörur til að vera með staðgengla, svo sem aðrar vörur sem hægt er að nota í staðinn fyrir upprunalegu vöruna.

### <a name="to-make-an-item-substitution"></a>Til að búa til staðgengilsvöru:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Finndu viðeigandi vöru og veldu síðan **Vörunúmer** til að opna birgðaspjaldið.  
3. Veljið aðgerðina **Tengt**, síðan **Vara** og svo **Staðgenglar** að opna aðgerðina á síðu **staðgengilsvörufærslu**.  
4. Veljið **Nr. staðgengilsvöru** og svo skiptivöru af listanum.
5. Fylla út eða breyta öðrum reitum á síðunni eftir þörfum.

Þegar umbeðið vörumagn fer yfir magnið sem er í boði í birgðum þá birtast skilaboð sem að tilkynna að staðgengilsvörur séu til.

> [!NOTE]  
> Athugaðu að staðgengilsvörur valda ekki sjálfkrafa því að vöru sé skipt út fyrir aðra vöru, til dæmis þegar sölupöntun er stofnuð eða í uppskrift. Þess í stað verður þér gert viðvart um að staðgengilsvara standi til boða.

## <a name="categories-attributes-and-variants"></a>Flokkar, eigindir og afbrigði

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Frekari upplýsingar um afbrigði er að finna í [Stjórna afurðarafbrigðum](inventory-item-variants.md).  

## <a name="delete-item-cards"></a>Eyða vöruspjöldum

Ef þú bókar færslu fyrir vöru er ekki hægt að eyða kortinu vegna þess að fjárhagsfærslurnar gætu verið nauðsynlegar fyrir birgðamat eða endurskoðun. Til að eyða birgðaspjöldum með fjárhagsfærslum skaltu hafa samband við samstarfsaðila Microsoft til að gera það í gegnum kóða.  

## <a name="manage-inventory-in-warehouses"></a>Stjórna birgðum í vöruhúsum

Þegar þú skráir nýja vöru sérðu reiti sem tengjast vöruhúsastjórnun, sérstaklega á **Vöruhús** Flýtaflipanum. Ef fyrirtækið notar ekki möguleika vöruhúsakerfisins í [!INCLUDE [prod_short](includes/prod_short.md)], þá má sleppa þessum reitum.  

Ef fyrirtækið setur síðar upp vöruhúsakerfi er mælt með því að ganga úr skugga um að sérhver fyrirliggjandi vara sé með réttar upplýsingar í hinum ýmsu reitum. Þannig geta vöruhúsaferlin gengið eins og til er ætlast. Upplýsingarnar geta falið í sér reiti á borð við **Kóði vöruhúsaflokks** eða **Kóði frágangssniðmáts**. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

## <a name="planning"></a>Áætlun

Þegar fyrirtækið þitt notar viðkomandi verkferla við áætlun framboðs í [!INCLUDE [prod_short](includes/prod_short.md)] þarf að fylla út í viðkomandi reiti í flýtiflipanum **Áætlanagerð**. Fyrir kynningu á svæði áætlunar skal skoða [Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md).  

Til að sjá dæmi um hvernig hægt er að nota reitina í flýtiflipanum **Áætlanagerð** skal skoða [Uppsetning bestu venja: Færibreytur áætlanagerðar](setup-best-practices-planning-parameters.md).  

## <a name="see-also"></a>Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Setja upp mælieiningar](inventory-how-setup-units-of-measure.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Setja upp Intrastat skýrslugerð](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Afstemma birgðakostnað í fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Stofnun númeraraða](ui-create-number-series.md)  
[Uppsetning bókunarflokka](finance-posting-groups.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Um áætlunaraðgerðir](production-about-planning-functionality.md)  
[Uppsetning bestu venjur: Áætla færibreytur](setup-best-practices-planning-parameters.md)  
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  
[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
