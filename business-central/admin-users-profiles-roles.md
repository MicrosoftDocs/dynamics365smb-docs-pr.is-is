---
title: Stjórna notendum og hlutverkum
description: Kynntu þér hvernig á að stjórna notandasíðum og hlutverkamiðstöðvum í Business Central. Notandasíður gera stjórnendum kleift að skilgreina og stjórna hvað notendur geta séð og gert á miðlægan hátt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/11/2023
ms.custom: bap-template
ms.search.form: 9171
---
# Stjórna notandasíðum

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Úthluta öllum notendum á forstillingar sem endurspegla:

* Viðskiptahlutverk þeirra
* Deildina sem þeir vinna í
* Annars konar flokkun

Forstillingar gera stjórnendum kleift að skilgreina miðlægt og stýra því hvaða mismunandi tegundir notendur geta fengið aðgang að í [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Dæmigerð notkun forstillingar er hlutverk. Forstilling er því heitið *Forstilling (hlutverk)* í notendaviðmóti.

Kerfisstjóri stofnar og stjórnar forstillingum á síðunni **Forstillingar (hlutverk)**. Hvert snið er með spjald þar sem hægt er að stjórna stillingum tengda hlutverkinu. Á spjaldinu eru til dæmis eftirfarandi upplýsingar:

* Heiti hlutverks
* Notandastillingar
* Hlutverkamiðstöðin sem sniðið notar

Frekari upplýsingar um notendastillingar og hlutverkamiðstöðvar er að finna í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

Áður en hægt er að stjórna notendaforstillingum verður að stofna og bæta við notendum í gegnum  Microsoft 365  stjórnstöðina. Síðan er hægt að úthluta heimildum á hvern notanda eða notendaflokk. Heimildir skilgreina aðgerðirnar sem notendur geta fengið aðgang að. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

## Sérsnið síðna

Hægt er að sérsníða síðuútlit fyrir forstillingu þannig að allir notendur sem hafa forstillingin hefur verið úthlutað á sjái sérsniðnar síður. Sem kerfisstjóri sérstillir þú síður með því að nota sömu virkni og notendur gera þegar þeir sérsníða. Frekari upplýsingar er að finna á [Sérsníða síður fyrir forstillingar](ui-personalization-manage.md).

## Forstilling stofnuð

Ef ekki er hægt að afrita fyrirliggjandi forstillingu er hægt að stofna nýja handvirkt.

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Forstillingar (hlutverk)** og velja svo viðeigandi tengil.  
2. Velja skal síðuna **Forstillingar (hlutverk)** í aðgerðinni **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Ef þú vilt að tiltekið notandasíða sé aðeins í boði fyrir mjög sértæka notendur getur þú stillt reitinn **Lýsing** á `Navigation menu only.`. Þannig er notandasíðan útilokuð frá listanum yfir tiltæk hlutverk í **Mínar stillingar**.

## Til að afrita forstillingu

Til að spara tíma er hægt að búa til nýja forstillingu með því að afrita fyrirliggjandi forstillingu. Afritaðu eina sem er með svipaðar stillingar og sá sem á að búa til.

> [!NOTE]
> Þegar þú afritar forstillingu eru allar sérstillingar sem tengjast síðunni einnig afritaðar, bæði af sem voru búnar til af notandanum og þær sem fengnar eru úr viðbótum.

1. Opnaðu síðuna **Forstillingar (hlutverk)**, veldu línuna fyrir forstillinguna sem þú vilt afrita og veldu svo **Afrita forstillingu** aðgerðina.
2. Fylltu út reitina **Auðkenni forstillingar** og **Birtingarnafn** og veldu síðan hnappinn **Í lagi**.
3. Á **Forstillingar (hlutverk)** síðunni skaltu opna nýstofnaða notandaspjaldið og breyta síðan öðrum reitum eftir þörfum.

## Til að breyta forstillingu

Hægt er að breyta forstillingu með því að breyta svæðunum á síðunni **Snið (hlutverk)**. Breytingarnar verða þó ekki sýnilegar notendum sem hefur verið úthlutað á forstillingarnar fyrr en þeir skrá sig út og aftur inn.

> [!Caution]
> Ekki skal endurnefna forstillingu á meðan notendum sem notandasíðunni hefur verið úthlutað á eru skráðir inn þar sem varan kann að frjósa og endurræsing nauðsynleg.

## Úthlutun forstillinga á notanda

Notendur geta úthlutað sjálfum sér hlutverki (sem stendur fyrir forstillingu) með því að velja reitinn **Hlutverk** á síðunni **Mínar stillingar**. Kerfisstjóri getur gert það sama í gegnum síðuna **Forstillingar (hlutverk)**.

1. Á síðunni **Forstillingar (hlutverk)** skaltu velja forstillingu sem á að úthluta og síðan velja aðgerðina **Listi yfir sérstillingar notenda**.
2. Á síðunni **Sérstillingar notanda** skal velja notandann sem á að úthluta forstillingunni og síðan velja aðgerðina **Breyta**.
3. Í reitnum **Auðkenni forstillingar** skal velja viðeigandi forstillingu.

> [!NOTE]
> Ef annarri forstillingu er úthlutað á notanda verða allar sérstillingar sem notandinn gerði með fyrra sniðinu varðveittar.

## Til að skilgreina notandastillingar fyrir forstillingu

Á síðunni **Mínar stillingar** geta notendur skilgreint grunnhegðun reikningsins síns, svo sem hlutverkamiðstöð, tungumálið og hvaða tilkynningar þeir fá. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

Kerfisstjóri getur skilgreint stillingar fyrir forstillingu. Stillingarnar gilda um alla notendur sem úthlutað er á hlutverkið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forstillingar (hlutverk)** og velja svo viðeigandi tengil.
2. Velja skal línuna fyrir forstillinguna sem á að breyta notandastillingum fyrir og síðan velja aðgerðina **Listi sérstillingar notanda**.
3. Á síðunni **Sérstillingar notanda** skal opna spjaldið fyrir notandann sem á að breyta stillingum hjá.
4. Á síðunni **Sérstillingaspjald notanda** skal breyta reitunum eftir þörfum.

## Til að virkja forstillingu

Þegar forstilling er stofnuð er hægt að skilgreina hvort, hvar og hvernig forstillingin og upplýsingarnar eru aðgengilegar fyrir notendur.

 **Á síðunni forstillingar (hlutverk)**  skal velja eftirtalda gátreiti:

* **Virkt** til að tilgreina hvort tengda hlutverkið sé sýnilegt á síðunni **Tiltæk hlutverk** fyrir notendur að velja úr.  
* **Nota sem sjálfgefna forstillingu** til að tilgreina forstillinguna sem á við notendur sem hafa ekki fengið úthlutað ákveðnu hlutverki.
* **Óvirkja sérstillingar** til að tilgreina hvort notendur tengdra hlutverka geti sérstillt vinnusvæði.
* **Sýna í hlutverkaleit** til að tilgreina hvort aðgerðir fyrir viðskiptaeiginleika sem eru hafðar með í forstillingunni sem birtist í eiginleikayfirliti hlutverkaleitar. Nánari upplýsingar er að finna í [Að finna síður með hlutverkaleit](ui-role-explorer.md)

## Flytja út forstillingar

Hægt er að flytja út forstillingar úr [!INCLUDE[prod_short](includes/prod_short.md)], til dæmis til að endurnýta þær í öðrum leigjanda. Forstillingarnar eru fluttar út í zip-skrá sem inniheldur AL-skrár. Hægt er að endurnýta AL skrárnar til að þróa viðaukaskrár. Frekari upplýsingar er að finna í [Nota biðlarann til að stofna notandasíður og sérstillingar á síðunni](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Á síðunni **Forstillingar (hlutverk)** skal velja aðgerðina **Flytja út forstillingar**.

    Þessi aðgerð flytur zip-skrá sem inniheldur AL-skrár fyrir allar forstillingar.

## Flytja inn forstillingar

Hægt er að flytja inn forstillingar sem hafa verið fluttar út úr [!INCLUDE[prod_short](includes/prod_short.md)]. Skrefin eru meira eða minna þau sömu og við útflutning forstillinga nema í hina áttina. Frekari upplýsingar er að finna í [Flytja út forstillingar](admin-users-profiles-roles.md#to-export-profiles).

1. Á síðunni **Forstillingar (hlutverk)** skal velja aðgerðina **Flytja inn forstillingar**.
2. Fylgdu skrefunum í leiðsögninni **Flytja inn forstillingar**.

    Ef aðeins á að flytja inn valdar forstillingar skal nota gátreitinn **Valið** til að gefa til kynna hverjar á að flytja inn.
3. Velja skal hnappinn **Flytja inn valið**.

    Þessi aðgerð flytur inn zip-skrá sem inniheldur AL-skrár fyrir valdar forstillingar.

## Til að eyða forstillingu

Hægt er að eyða forstillingu með því að velja aðgerðina **Eyða** á **Forstillingar (hlutverk)** síðunni. Eftirfarandi takmarkanir gilda hins vegar:

* Ekki er hægt að eyða forstillingu sem hefur verið úthlutað á notanda eða notendahóp.
*-* Ekki er hægt að eyða forstillingum sem eru í viðaukum. Fyrst verður að fjarlægja viðbótina.
*-* Aðeins er hægt að eyða einni forstillingu í einu.

## Til að eyða öllum sérstillingum sem notandi gerði

Hægt er að eyða öllum breytingum sem notandinn hefur gert á síðum. Eyðing breytinga getur verið gagnleg, t.d. ef starfsmaður hefur breytt um hlutverk og þarf þess ekki lengur. Deletions snúa útliti síðunnar aftur við það sem sniðið er skilgreint.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sérstillingar notanda** og velja síðan viðkomandi tengil.

    Síðan **Sérstillingar notanda** birtir alla notendur sem hafa gert sérstillingar.

2. Opnaðu spjaldið fyrir notanda sem eyða á sérstillingum hjá.
3. Á síðunni **Sérstillingaspjald notanda** skal velja aðgerðina **Hreinsa sérstilltar síður** og síðan samþykkja skilaboðin sem birtast.

Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.

Einnig er hægt að eyða öllum sérstillingum síðu fyrir forstillingu. Frekari upplýsingar er að finna  [í til að eyða öllum sérstillingum fyrir forstillingu](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

## Til að eyða sérstillingum fyrir tilteknar síður

Hægt er að eyða sérsniðnum stillingum sem einn eða fleiri notendur hafa gert á tilteknar síður. Ef sérstillingum er eytt getur það til dæmis verið gagnlegt ef viðskiptaferli breytist vegna þess að ekki er hægt að nota sérsnið. Deletions snúa útliti síðunnar aftur við það sem sniðið er skilgreint.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sérstillingar notandasíðu** og velja síðan viðkomandi tengil.

    Á síðunni **Sérstillingar notandasíðu** er listi yfir allar síður sem hafa verið sérstilltar og notandinn sem þau tilheyra.

    > [!Note]
    > Gátmerki í **Eldri sérstilling** reitnum gefur til kynna að sérstillingin hafi verið gerð í eldri útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)], sem meðhöndlaði sérstillingu öðruvísi. Notendur sem reyna að sérstilla þessar síður eru útilokaðir frá því að gera það nema þeir velji að opna síðuna. Frekari upplýsingar eru í [Af hverju er síða læst og því ekki hægt að sérsníða hana](ui-personalization-locked.md).

2. Veldu línuna fyrir sérstillingu síðunnar sem á að eyða og veldu síðan aðgerðina **Eyða**.

Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.  

Einnig er hægt að eyða einstaka sérstillingum síðu fyrir forstillingu. Frekari upplýsingar er að finna  [í til að eyða sérstökum síðum fyrir forstillingu](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## Stjórna lotum notenda

Sem kerfisstjóri á [!INCLUDE[prod_short](includes/prod_short.md)] ánetinu er hægt að stjórna notandalotum í stjórnunarstöðinni. Frekari upplýsingar er að finna  [í umsjón með setum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions)  í innihaldi stjórnunar.  

Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er t.d. hægt að stjórna lotum með því að nota SQL Server Management Studio. Frekari upplýsingar er að finna í [tæknileg fylgiskjöl SQL Server](/sql/sql-server).  

## Sjá einnig .

[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
