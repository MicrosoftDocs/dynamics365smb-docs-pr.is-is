---
title: Stjórna notendum og hlutverkum
description: Læra að stjórna notendasniðum í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.form: '9171,'
---
# <a name="manage-user-profiles"></a>Stjórna forstillingum notenda

Úthluta öllum notendum á forstillingar sem endurspegla:

* Viðskiptahlutverk þeirra
* Deildin sem þeir vinna í
* Önnur tegund flokkunar

Forstillingar gera stjórnendum kleift að skilgreina miðlægt og stjórna því hvaða mismunandi gerðir notenda hafa aðgang að í Business Central.

Dæmigerð notkun forstillingar er hlutverk. Forstilling er því heitið *Forstilling (hlutverk)* í notendaviðmóti.

Kerfisstjóri stofnar og stjórnar forstillingum á síðunni **Forstillingar (hlutverk)**. Hver forstilling er með spjaldi þar sem stillingum tengda hlutverksins er stjórnað. Á spjaldinu eru eftirfarandi upplýsingar:

* Heiti hlutverksins
* Notandastillingar
* Mitt hlutverk sem forstillingin notar

Frekari upplýsingar um notendastillingar og hlutverkamiðstöðvar er að finna í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

Áður en hægt er að stjórna notendaforstillingum þarf að stofna og bæta notendum við í gegnum Microsoft 365 stjórnunarmiðstöðina. Síðan er hægt að úthluta heimildum á hvern notanda eða notendaflokk. Heimildir skilgreina eiginleikana sem notendur hafa aðgang að. Nánari upplýsingar um heimildastillingar eru [í Úthluta heimildum til notenda og hópa](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Sérstilling síðu

Hægt er að sérsníða síðuuppsetningar fyrir forstillingu svo að allir notendur sem forstillingunni hefur verið úthlutað sjá sérsniðnu síðurnar. Sem kerfisstjóri sérstillir þú síður með því að nota sömu virkni og notendur gera þegar þeir sérsníða. Nánari upplýsingar um uppsetningu síðu [eru í Sérstilla síður fyrir forstillingar](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Forstilling stofnuð

Ef ekki er hægt að afrita fyrirliggjandi forstillingu er hægt að búa til nýja handvirkt.

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Forstillingar (hlutverk)** og velja svo viðeigandi tengil.  
2. Velja skal síðuna **Forstillingar (hlutverk)** í aðgerðinni **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Ef þú vilt að tiltekið notandasíða sé aðeins í boði fyrir mjög sértæka notendur getur þú stillt reitinn **Lýsing** á `Navigation menu only.`. Þannig er notandasíðan útilokuð frá listanum yfir tiltæk hlutverk í **Mínar stillingar**.

## <a name="to-copy-a-profile"></a>Til að afrita forstillingu

Til að spara tíma er hægt að búa til nýja forstillingu með því að afrita fyrirliggjandi forstillingu. Afritaðu eina sem er með svipaðar stillingar og sá sem á að búa til.

Þegar þú afritar forstillingu eru allar sérstillingar sem tengjast síðunni einnig afritaðar, bæði af sem voru búnar til af notandanum og þær sem fengnar eru úr viðbótum.

1. Opnaðu síðuna **Forstillingar (hlutverk)**, veldu línuna fyrir forstillinguna sem þú vilt afrita og veldu svo **Afrita forstillingu** aðgerðina.
2. Fylltu út reitina **Auðkenni forstillingar** og **Birtingarnafn** og veldu síðan hnappinn **Í lagi**.
3. Á **Forstillingar (hlutverk)** síðunni skaltu opna nýstofnaða notandaspjaldið og breyta síðan öðrum reitum eftir þörfum.

## <a name="to-edit-a-profile"></a>Til að breyta forstillingu

Hægt er að breyta forstillingu með því að breyta reitunum á síðunni **Forstillingar (hlutverk).**). Breytingarnar sjást hins vegar ekki notandanum sem úthlutaði forstillingunni fyrr en þær skrá sig út og aftur.

> [!Caution]
> Ekki skal endurnefna forstillingu á meðan notendum sem notandasíðunni hefur verið úthlutað á eru skráðir inn þar sem varan kann að frjósa og endurræsing nauðsynleg.

## <a name="to-assign-a-profile-to-a-user"></a>Úthlutun forstillinga á notanda

Notendur geta úthlutað sjálfum sér hlutverki (sem stendur fyrir forstillingu) með því að velja reitinn **Hlutverk** á síðunni **Mínar stillingar**. Kerfisstjóri getur gert það sama í gegnum síðuna **Forstillingar (hlutverk)**.

1. Á síðunni **Forstillingar (hlutverk)** skaltu velja forstillingu sem á að úthluta og síðan velja aðgerðina **Listi yfir sérstillingar notenda**.
2. Á síðunni **Sérstillingar notanda** skal velja notandann sem á að úthluta forstillingunni og síðan velja aðgerðina **Breyta**.
3. Í reitnum **Auðkenni forstillingar** skal velja viðeigandi forstillingu.

Ef annarri forstillingu er úthlutað á notanda verða allar sérstillingar sem notandinn gerði með fyrra sniðinu varðveittar.

## <a name="to-define-user-settings-for-a-profile"></a>Til að skilgreina notandastillingar fyrir forstillingu

Á síðunni **Mínar stillingar** geta notendur skilgreint grunnhegðun reikningsins síns, svo sem hlutverkamiðstöð, tungumálið og hvaða tilkynningar þeir fá. Nánari upplýsingar um notendastillingar eru [í Breyta grunnstillingum](ui-change-basic-settings.md).

Sem stjórnandi getur notandi skilgreint stillingar fyrir forstillingu. Stillingarnar eiga við um alla notendur sem hafa verið tengdir hlutverkinu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forstillingar (hlutverk)** og velja svo viðeigandi tengil.
2. Velja skal línuna fyrir forstillinguna sem á að breyta notandastillingum fyrir og síðan velja aðgerðina **Listi sérstillingar notanda**.
3. Á síðunni **Sérstillingar notanda** skal opna spjaldið fyrir notandann sem á að breyta stillingum hjá.
4. Á síðunni **Sérstillingaspjald notanda** skal breyta reitunum eftir þörfum.

## <a name="to-activate-a-profile"></a>Til að virkja forstillingu

Þegar forstilling er búin til er hægt að skilgreina hvort, hvar og hvernig forstillingin og upplýsingarnar hennar eru tiltækar notendum.

Á síðunni **Forstillingar (hlutverk)** eru eftirfarandi gátreitir valdir:

* **Virkt** til að tilgreina hvort tengda hlutverkið sé sýnilegt á síðunni **Tiltæk hlutverk** fyrir notendur að velja úr.  
* **Nota sem sjálfgefna forstillingu** til að tilgreina forstillinguna sem á við notendur sem ekki hafa úthlutað tilteknu hlutverki.
* **Óvirkja sérstillingar** til að tilgreina hvort notendur tengdra hlutverka geti sérstillt vinnusvæði.
* **Sýna í hlutverkaleit** til að tilgreina hvort aðgerðir fyrir viðskiptaeiginleika sem eru hafðar með í forstillingunni sem birtist í eiginleikayfirliti hlutverkaleitar. Nánari upplýsingar um hlutverkavafra eru [í Finna síður með hlutverkavafranum](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Flytja út forstillingar

Hægt er að flytja forstillingar út úr [!INCLUDE[prod_short](includes/prod_short.md)] og endurnota þær aftur í öðrum leigjanda. Forstillingarnar eru fluttar út í zip-skrá sem inniheldur Al-tungumálaskrár forritsins. Hægt er að endurnota AL-skrár til að þróa viðbætur. Nánari upplýsingar um útflutning forstillinga eru [í Biðlarinn til að stofna forstillingar og síðusnið](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Á síðunni **Forstillingar (hlutverk)** skal velja aðgerðina **Flytja út forstillingar**.

    Þessi aðgerð flytur út zip-skrá með AL-skrám fyrir allar forstillingar.

## <a name="to-import-profiles"></a>Flytja inn forstillingar

Hægt er að flytja inn forstillingar sem eru fluttar út frá Business Central. Skrefin eru meira eða minna þau sömu og við útflutning forstillinga nema í hina áttina.

1. Á síðunni **Forstillingar (hlutverk)** skal velja aðgerðina **Flytja inn forstillingar**.
1. Fylgdu skrefunum í leiðsögninni **Flytja inn forstillingar**.

    Ef aðeins á að flytja inn valdar forstillingar er gátreiturinn **Valið notaður** til að gefa til kynna hvaða á að flytja inn.
1. Hnappurinn **Flytja inn valið er valinn** .

    Þessi aðgerð flytur inn zip-skrá sem inniheldur AL-skrár fyrir valdar forstillingar.

## <a name="to-delete-a-profile"></a>Til að eyða forstillingu

Hægt er að eyða forstillingu með því að velja aðgerðina **Eyða** á **Forstillingar (hlutverk)** síðunni. Eftirfarandi takmarkanir gilda hins vegar:

* Ekki er hægt að eyða forstillingu sem er úthlutað á notanda eða notendahóp.
* Ekki er hægt að eyða forstillingum sem eru upprunnin úr viðbótum. Fyrst verður að fjarlægja viðbótina.
* Aðeins er hægt að eyða einni forstillingu í einu.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Til að eyða öllum sérstillingum sem notandi gerði

Hægt er að eyða öllum breytingum sem notandi gerir á síðum. Breytingar geta til dæmis verið gagnlegar ef starfsmaður breytir hlutverki og þarfnast þeirra ekki lengur. Forstillingin skilgreinir síðuuppsetningu og eyðingar sem endurheimta hana aftur í þá skilgreiningu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sérstillingar notanda** og velja síðan viðkomandi tengil.

    Síðan **Sérstillingar** notanda sýnir lista yfir alla notendur sem sérstilla sig.

2. Opnaðu spjaldið fyrir notanda sem eyða á sérstillingum hjá.
3. Á síðunni **Sérstillingaspjald notanda** skal velja aðgerðina **Hreinsa sérstilltar síður** og síðan samþykkja skilaboðin sem birtast.

Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.

Einnig er hægt að eyða öllum sérstillingum síðu fyrir forstillingu. Nánari upplýsingar eru [í Til að eyða öllum sérstillingum fyrir forstillingu](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Til að eyða sérstillingum fyrir tilteknar síður

Hægt er að eyða sérstillingum sem einn eða fleiri notendur gera á tilteknum síðum. Sérstillingar geta til dæmis verið gagnlegar ef breyting á viðskiptaferli merkir að ekki er hægt að nota sérstillingu. Eyðir endurheimta síðuuppsetninguna aftur til þess sem forstillingin skilgreinir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sérstillingar notandasíðu** og velja síðan viðkomandi tengil.

    Sérstillingar **notendasíðu** birtast allar síður sem eru sérstilltar og notandinn sem þær tilheyra.

    Gátmerki í reitnum **Sérstilling eldri sérstillinga** gefur til kynna að sérstillingin hafi verið gerð í eldri útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] sérstillingunni á mismunandi hátt. Notendur sem reyna að sérstilla þessar síður eru útilokaðir frá því að gera það nema þeir velji að opna síðuna.

2. Veldu línuna fyrir sérstillingu síðunnar sem á að eyða og veldu síðan aðgerðina **Eyða**.

Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.  

Einnig er hægt að eyða einstaka sérstillingum síðu fyrir forstillingu. Nánari upplýsingar eru [í Til að eyða sérstillingu tiltekinna síðna fyrir forstillingu](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Stjórna lotum notenda

Sem kerfisstjóri á [!INCLUDE[prod_short](includes/prod_short.md)] ánetinu er hægt að stjórna notandalotum í stjórnunarstöðinni. Nánari upplýsingar [eru í Unnið með lotur][def] í stjórnunarefninu.  

Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er t.d. hægt að stjórna lotum með því að nota SQL Server Management Studio. Frekari upplýsingar er að finna í [tæknileg fylgiskjöl SQL Server](/sql/sql-server).  

## <a name="see-also"></a>Sjá einnig .

[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions
