---
title: Stjórna notendum og hlutverkum
description: Læra að stjórna notendasniðum í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 07/26/2024
ms.custom: bap-template
ms.search.form: '9171,'
---
# Stjórna forstillingum notenda

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

Áður en hægt er að stjórna notendaforstillingum þarf að stofna og bæta notendum við í gegnum Microsoft 365 stjórnunarmiðstöðina. Síðan er hægt að úthluta hverjum notanda heimildum eða notendaflokkur. Heimildir skilgreina eiginleikana sem notendur hafa aðgang að. Nánari upplýsingar um heimildastillingar eru [í Úthluta heimildum til notenda og hópa](ui-define-granular-permissions.md).

## Sérstilling síðu

Hægt er að sérsníða síðuuppsetningar fyrir forstillingu svo að allir notendur sem forstillingunni hefur verið úthlutað sjá sérsniðnu síðurnar. Sem kerfisstjóri sérstillir þú síður með því að nota sömu virkni og notendur gera þegar þeir sérsníða. Nánari upplýsingar um uppsetningu síðu [eru í Sérstilla síður fyrir forstillingar](ui-personalization-manage.md).

## Stofna forstillingu

Ef ekki er hægt að afrita fyrirliggjandi forstillingu er hægt að búa til nýja handvirkt.

1. Velja skal Leit að ![síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") Táknmynd, færa inn **Forstillingar (Hlutverk)** og velja síðan viðeigandi tengja.  
2. Á síðunni **Forstillingar (hlutverk)** skal velja aðgerðina **Nýtt** .  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Ef þú vilt að tiltekið notandasíða sé aðeins í boði fyrir mjög sértæka notendur getur þú stillt reitinn **Lýsing** á `Navigation menu only.`. Þannig er notandasíðan útilokuð frá listanum yfir tiltæk hlutverk í **Mínar stillingar**.

## Afrita forstillingu

Til að spara tíma er hægt að búa til nýja forstillingu með því að afrita fyrirliggjandi forstillingu. Afritaðu eina sem er með svipaðar stillingar og sá sem á að búa til.

Þegar þú afritar forstillingu eru allar sérstillingar sem tengjast síðunni einnig afritaðar, bæði af sem voru búnar til af notandanum og þær sem fengnar eru úr viðbótum.

1. Á síðunni **Forstillingar (hlutverk)** skal velja línuna fyrir forstillinguna sem á að afrita og velja svo aðgerðina **Afrita forstillingu** .
2. Reitirnir **Kenni** forstillingar og **Birta heiti** eru fylltir út og hnappurinn **Í lagi** valinn.
3. Á **Forstillingar (hlutverk)** síðunni skaltu opna nýstofnaða notandaspjaldið og breyta síðan öðrum reitum eftir þörfum.

## Breyta forstillingu

Hægt er að breyta forstillingu með því að breyta reitunum á síðunni **Forstillingar (hlutverk).**). Breytingarnar sjást hins vegar ekki notandanum sem úthlutaði forstillingunni fyrr en þær skrá sig út og aftur.

> [!Caution]
> Ekki skal endurnefna forstillingu á meðan notendum sem notandasíðunni hefur verið úthlutað á eru skráðir inn þar sem varan kann að frjósa og endurræsing nauðsynleg.

## Úthluta notanda forstillingu

Notendur geta úthlutað sjálfum sér hlutverki (sem stendur fyrir forstillingu) með því að velja reitinn **Hlutverk** á síðunni **Mínar stillingar**. Kerfisstjóri getur gert það sama í gegnum síðuna **Forstillingar (hlutverk)**.

1. Á síðunni **Forstillingar (hlutverk)** skal velja forstillinguna sem á að úthluta og svo skal velja aðgerðina **Sérstillingalisti** notanda.
2. Á síðunni **Stillingar** notanda er notandinn sem á að úthluta forstillingunni valinn og aðgerðin **Breyta** valin.
3. Í reitnum **Auðkenni forstillingar** skal velja viðeigandi forstillingu.

Ef annarri forstillingu er úthlutað á notanda verða allar sérstillingar sem notandinn gerði með fyrra sniðinu varðveittar.

## Skilgreina notendastillingar fyrir forstillingu

Á síðunni **Mínar stillingar** geta notendur skilgreint grunnhegðun reikningsins síns, svo sem hlutverkamiðstöð, tungumálið og hvaða tilkynningar þeir fá. Nánari upplýsingar um notendastillingar eru [í Breyta grunnstillingum](ui-change-basic-settings.md).

Sem stjórnandi getur notandi skilgreint stillingar fyrir forstillingu. Stillingarnar eiga við um alla notendur sem hafa verið tengdir hlutverkinu.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Forstillingar (Hlutverk)** og velja síðan viðeigandi tengja.
2. Línan fyrir forstillinguna sem breyta á notendastillingum fyrir er valin og svo skal velja aðgerðina **Sérstillingalisti** notanda.
3. Á síðunni **Sérstillingar notanda** skal opna spjaldið fyrir notandann sem á að breyta stillingum hjá.
4. Á síðunni **Sérstillingaspjald notanda** skal breyta reitunum eftir þörfum.

## Virkja forstillingu

Þegar forstilling er búin til er hægt að skilgreina hvort, hvar og hvernig forstillingin og upplýsingarnar hennar eru tiltækar notendum.

Á síðunni **Forstillingar (hlutverk)** eru eftirfarandi gátreitir valdir:

* **Virkt** til að tilgreina hvort tengda hlutverkið sé sýnilegt á síðunni **Tiltæk hlutverk** fyrir notendur að velja úr.  
* **Nota sem sjálfgefna forstillingu** til að tilgreina forstillinguna sem á við notendur sem ekki hafa úthlutað tilteknu hlutverki.
* **Óvirkja sérstillingar** til að tilgreina hvort notendur tengdra hlutverka geti sérstillt vinnusvæði.
* **Sýna í hlutverkaleit** til að tilgreina hvort aðgerðir fyrir viðskiptaeiginleika sem eru hafðar með í forstillingunni sem birtist í eiginleikayfirliti hlutverkaleitar. Nánari upplýsingar um hlutverkavafra eru [í Finna síður með hlutverkavafranum](ui-role-explorer.md).

## Flytja út forstillingar

Hægt er að flytja forstillingar út úr [!INCLUDE[prod_short](includes/prod_short.md)] og endurnota þær aftur í öðrum leigjanda. Forstillingarnar eru fluttar út í zip-skrá sem inniheldur Al-tungumálaskrár forritsins. Hægt er að endurnota AL-skrár til að þróa viðbætur. Nánari upplýsingar um útflutning forstillinga eru [í Biðlarinn til að stofna forstillingar og síðusnið](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Á síðunni **Forstillingar (hlutverk)** skal velja aðgerðina **Flytja út forstillingar** .

    Þessi aðgerð flytur út zip-skrá með AL-skrám fyrir allar forstillingar.

## Flytja inn forstillingar

Hægt er að flytja inn forstillingar sem eru fluttar út frá Business Central. Skrefin eru meira eða minna þau sömu og við útflutning forstillinga nema í hina áttina.

1. Á síðunni **Forstillingar (hlutverk)** skal velja aðgerðina **Flytja inn forstillingar** .
1. Fylgdu skrefunum í leiðsögninni **Flytja inn forstillingar**.

    Ef aðeins á að flytja inn valdar forstillingar er gátreiturinn **Valið notaður** til að gefa til kynna hvaða á að flytja inn.
1. Hnappurinn **Flytja inn valið er valinn** .

    Þessi aðgerð flytur inn zip-skrá sem inniheldur AL-skrár fyrir valdar forstillingar.

## Eyða forstillingu

Hægt er að eyða forstillingu með því að velja aðgerðina **Eyða** á **Forstillingar (hlutverk)** síðunni. Eftirfarandi takmarkanir gilda hins vegar:

* Ekki er hægt að eyða forstillingu sem er úthlutað á notanda eða notendaflokkur.
* Ekki er hægt að eyða forstillingum sem eru upprunnin úr viðbótum. Fyrst verður að fjarlægja viðbótina.
* Aðeins er hægt að eyða einni forstillingu í einu.

## Eyða sérstillingum

### Eyða öllum sérstillingum sem tiltekinn notandi hefur gert

Hægt er að eyða öllum breytingum sem notandi gerir á hvaða síðu sem er, sem bakfærir síðurnar í upphaflega útlitið. Sérstillingar eru ekki tengdar við forstillingu (hlutverk). Ef notandi sérstillir síðu finnur hann sérstillingar á síðunni sama hvaða hlutverki hann notar.<!--Deleting changes can be useful, for example, if an employee changes role and no longer needs them. The profile defines the page layout and deletions restore it back to that definition.--> 

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Notandastillingar** og velja síðan viðeigandi tengja.

    Síðan **Stillingar** notanda sýnir lista yfir alla notendur<!--who make personalizations-->.

2. Velja skal notandann sem á að eyða sérstillingum fyrir.
3. Á síðunni **Stillingar** notanda skal velja aðgerðina **Hreinsa sérsniðnar síður** og samþykkja síðan skilaboðin sem birtast.

Notandinn sér breytingarnar næst þegar hann skráir sig inn.

Einnig er hægt að eyða öllum sérstillingum síðu fyrir forstillingu. Nánari upplýsingar eru [í Til að eyða öllum sérstillingum fyrir forstillingu](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

### Eyða sérstillingum fyrir tilteknar síður

Hægt er að eyða sérstillingum sem einn eða fleiri notendur gera á tilteknum síðum. Sérstillingar geta til dæmis verið gagnlegar ef breyting á viðskiptaferli merkir að ekki er hægt að nota sérstillingu. Eyðir endurheimta síðuuppsetninguna aftur til þess sem forstillingin skilgreinir.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **sérsniðnar síður** og velja síðan viðeigandi tengja.

    Síðan **Sérsniðnar síður** birtir lista yfir allar síður sem eru sérstilltar og notandinn sem þær tilheyra.

    <!--A checkmark in the **Legacy Personalization** field indicates that the personalization was done in an older version of [!INCLUDE[prod_short](includes/prod_short.md)], which handled personalization differently. Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.-->

2. Línan fyrir sérstillingu síðunnar sem á að eyða er valin og svo er aðgerðin **Eyða** valin.

Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.  

Einnig er hægt að eyða einstaka sérstillingum síðu fyrir forstillingu. Nánari upplýsingar eru [í Til að eyða sérstillingu tiltekinna síðna fyrir forstillingu](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## Stjórna lotum notenda

Sem kerfisstjóri á [!INCLUDE[prod_short](includes/prod_short.md)] ánetinu er hægt að stjórna notandalotum í stjórnunarstöðinni. Nánari upplýsingar [eru í Unnið með lotur][def] í stjórnunarefninu.  

Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er t.d. hægt að stjórna lotum með því að nota SQL Server Management Studio. Frekari upplýsingar er að finna í [tæknileg fylgiskjöl SQL Server](/sql/sql-server).  

## Sjá einnig .

[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions
