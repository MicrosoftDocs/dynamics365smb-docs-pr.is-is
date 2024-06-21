---
title: Stofna birgðaspjöld fyrir vörur eða þjónustu
description: Þú býrð til birgðaspjöld fyrir þjónustu sem þú selur sem klukkutíma og fyrir efnislegar vörur. Sem dæmi má nefna samsetningaríhluti og fullbúnar vörur sem þú selur úr birgðum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="register-new-items"></a>Skrá nýjar vörur

Vörur eru vörurnar eða þjónustan sem keypt er, geymt, selt, afhent og reikningsfært fyrir.  **Síðan Birgðaspjald** er notuð til að skrá upplýsingar um eftirfarandi tegundir atriða:

* **Í birgðum** er tilgreint að varan sé efnisleg eining sem hægt er að stjórna og rekja í birgðum.
* **Óbirgðir** eru efnislegar einingar sem ekki er stjórnað eða raktar í birgðum.
* **Þjónustuvörur** eru vinnutímaeining, gjarnan notuð í þjónustukerfi.

Nánari upplýsingar um þessar vörur eru í [Um vörutegundir](inventory-about-item-types.md).

> [!TIP]
> Einnig eru vörulistavörur sem líkjast vörum sem ekki eru í birgðum að því leyti að þær eru vörur sem boðnar eru viðskiptamönnum en stjórna ekki fyrr en þær eru selt. Til að fá nánari upplýsingar er farið í [Vinna við vörulistaatriði](inventory-how-work-nonstock-items.md).  

## <a name="primary-and-alternate-vendors"></a>Aðal- og aðrir lánardrottnar

Ef sama varan er keypt frá fleiri en einum lánardrottni er hægt að tengja þá lánardrottna við vöruna. Nota aðgerðina **Lánardrottnar** á síðunni **Birgðaspjald** til að opna **síðuna Vörulisti** lánardrottins. Síðan sýnir þá lánardrottna sem keypt er frá, þannig að auðvelt er að stofna eða velja annan lánardrottin þegar innkaupapöntun er stofnuð.

## <a name="use-item-templates"></a>Nota vörusniðmát

Til að endurnota stillingar fyrir mismunandi tegundir vara þegar nýjar vörur eru stofnaðar er hægt að vista vörur sem vörusniðmát. Vörusniðmát hraða við að bæta við nýjum vörum og auka samkvæmni í vörugögnum. Þegar ný vara er skráð birtist síða sem gerir kleift að velja sniðmát. Þegar sniðmát hefur verið valið eru stillingar þess fylltar út fyrir vöruna sem verið er að stofna. Ef aðeins eitt vörusniðmát er fyrir hendi nota nýjar vörur alltaf það sniðmát. Til að fræðast um hvernig setja á upp vörusniðmát er farið í [Vista birgðaspjald sem vörusniðmát](#save-an-item-card-as-an-item-template).

## <a name="include-items-in-bills-of-materials"></a>Taka vörur með í uppskriftum

Hægt er að skipuleggja stigveldi með aðalvöru með undirliggjandi íhlutavörur í samsetningar- og framleiðsluuppskriftum. Hægt er að fræðast meira um uppskriftir með því að fara í [Vinna með uppskriftir](inventory-how-work-BOMs.md).

## <a name="to-create-a-new-item-card"></a>Að búa til nýtt vöruspjald

Eftirfarandi myndband sýnir hvernig vara er sett upp á síðunni Birgðaspjald. Einnig er hægt að setja upp nýjar vörur með því að afrita fyrirliggjandi vörur. Nánari upplýsingar eru notaðar með því að fara í [Afrita fyrirliggjandi vörur til að stofna nýjar vörur](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> Í reitnum **Aðferð kostnaðarútreiknings** seturðu upp hvernig kerfið reiknar út kostnaðarverð með því að áætla vöruflæði fyrirtækisins. Fimm aðferðir kostnaðarútreiknings eru í boði, út frá gerð vörunnar. Nánari upplýsingar um kostnað eru í [Hönnunarupplýsingar: Aðferðir kostnaðarútreiknings](design-details-costing-methods.md).
>
> Ef meðalinnkaupsverð **er valið** er kostnaðarverð vörunnar reiknað sem meðalinnkaupaverð á hverjum tímapunkti eftir innkaup. Fyrir verðmat birgða, er gert ráð fyrir að allar birgðir verði seldar á sama tíma. Með þessari stillingu er hægt að velja reitinn **Kostn.verð** á síðunni **Útreikn.yfirlit** meðalinnkaupsverðs til að skoða færslurnar sem voru notaðar til að reikna út meðalinnkaupaverðið.

Hægt er að nota sérverð eða afslátt sem notandi eða lánardrottinn veita fyrir vöruna samkvæmt ákveðnum skilyrðum. Skilyrði innihalda til dæmis viðskiptamanninn, lágmarksmagn pöntunar eða lokadagsetningu. Sérstök verð eru sett upp með því að velja Aðgerðirnar **Setja sérverð** eða **Setja sérstakan** afslátt. Hver lína á, til dæmis á síðunni **Söluverð**, sýnir sértækt verð. Hver dálkur táknar viðmiðun sem verður að uppfylla til að veita viðskiptamanni sérverð sem þú slærð inn í **Einingaverð** reitinn á síðunni **Söluverð**. Nánari upplýsingar um verðlagningu fást með því að fara í [Skrá söluverð, afslátt og Greiðslusamninga](sales-how-record-sales-price-discount-payment-agreements.md) eða [skrá sérstakt innkaupaverð og afslátt](purchasing-how-record-purchase-price-discount-payment-agreements.md).

### <a name="save-an-item-card-as-an-item-template"></a>Vista birgðaspjald sem vörusniðmát

1. Á síðunni **Birgðaspjald** skal velja aðgerðina **Vista sem sniðmát**. Síðan **Birgðasniðmát** sýnir birgðaspjaldið sem sniðmát.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Einnig er hægt að endurnota víddir fyrir vörur. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Síðan **Víddarsniðmát** sýnir víddirnar sem eru settar upp fyrir vöruna. Breyta eða bæta við víddum sem eiga við nýjar vörur sem stofnaðar eru úr sniðmátinu.

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

Lánardrottnarnir birtast á síðunni **Vörulisti** lánardrottins sem opnaður er á birgðaspjaldinu, svo auðvelt sé að velja annan lánardrottin.

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

## <a name="delete-item-cards"></a>Eyða birgðaspjöldum

Ef bókuð eru viðskipti vegna vöru er ekki hægt að eyða spjaldinu vegna þess að bókarfærslur gætu verið nauðsynlegar við verðmætamat birgða eða endurskoðun. Til að eyða birgðaspjöldum með fjárhagsfærslum skaltu hafa samband við samstarfsaðila Microsoft til að gera það í gegnum kóða.  

## <a name="manage-inventory-in-warehouses"></a>Stjórna birgðum í vöruhúsum

Þegar ný vara er skráð sjást reitir sem tengjast vöruhúsakerfinu, sérstaklega á flýtiflipanum **Vöruhús** . Ef fyrirtækið notar ekki möguleika vöruhúsakerfisins í [!INCLUDE [prod_short](includes/prod_short.md)], þá má sleppa þessum reitum.  

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
