---
title: Meðhöndla notendur og hlutverk | Microsoft Docs
description: Lærið að meðhöndla notendur og Mitt hlutverk í Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 11/06/2019
ms.author: sgroespe
ms.openlocfilehash: b96b5cbff2ec182ab1a7254ee3384a6d1869e3c4
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775428"
---
# <a name="manage-profiles"></a>Vinna með forstillingar
Öllum notendum [!INCLUDE[d365fin](includes/d365fin_md.md)] er úthlutað forstillingu sem endurspeglar viðskiptahlutverk þeirra, deildina sem þeir vinna í eða aðra flokkun. Forstillingar gera stjórnendum kleift að skilgreina og stjórna því miðlægt hvað mismunandi gerðir notenda geta séð og gert í notendaviðmótinu svo þeir geti framkvæmt verk sín á skilvirkan hátt.

> [!NOTE]
> Dæmigerð notkun forstillingar er hlutverk. Forstilling er því heitið *Forstilling (hlutverk)* í notendaviðmóti.

Kerfisstjóri stofnar og stjórnar forstillingum á síðunni **Forstillingar (hlutverk)**. Hvert snið er með spjald þar sem hægt er að vinna með ýmsar stillingar fyrir tengda hlutverkið, svo sem hlutverksheiti, stillingar notanda og hvaða hlutverkamiðstöð sniðið notar. Frekari upplýsingar um notendastillingar og hlutverkamiðstöðvar er að finna í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

Áður en hægt er að hafa umsjón með forstillingum notenda verða notendur að vera búnir að stofna þær og bæta við í gegnum Office 365 stjórnendamiðstöð. Síðan er hægt að úthluta heimildum á hvern notanda eða notendaflokk til að skilgreina hvaða eiginleika þeir mega skoða og/eða breyta. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Sérsnið síðna
Hægt er að sérsníða síðuútlit fyrir forstillingu þannig að allir notendur sem hafa forstillingin hefur verið úthlutað á sjái sérsniðnar síður. Sem kerfisstjóri sérstillir þú síður með því að nota sömu virkni og notendur gera þegar þeir sérsníða. Frekari upplýsingar er að finna á [Sérsníða síður fyrir forstillingar](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Forstilling stofnuð
Ef ekki er hægt að afrita fyrirliggjandi forstillingu er hægt að stofna nýja handvirkt.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, slá inn **Forstillingar (hlutverk)** og velja svo viðeigandi tengil.  
2. Velja skal síðuna **Forstillingar (hlutverk)** í aðgerðinni **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-a-profile"></a>Til að afrita forstillingu
Til að spara tíma er hægt að búa til nýja forstillingu með því að afrita fyrirliggjandi forstillingu. Afritaðu eina sem er með svipaðar stillingar og sá sem á að búa til.

> [!NOTE]
> Þegar þú afritar forstillingu eru allar sérstillingar sem tengjast síðunni einnig afritaðar, bæði af sem voru búnar til af notandanum og þær sem fengnar eru úr viðbótum.

1. Opnaðu síðuna **Forstillingar (hlutverk)**, veldu línuna fyrir forstillinguna sem þú vilt afrita og veldu svo **Afrita forstillingu** aðgerðina.
2. Fylltu út reitina **Auðkenni forstillingar** og **Birtingarnafn** og veldu síðan hnappinn **Í lagi**.
3. Á **Forstillingar (hlutverk)** síðunni skaltu opna nýstofnaða notandaspjaldið og breyta síðan öðrum reitum eftir þörfum.

## <a name="to-edit-a-profile"></a>Til að breyta forstillingu
Hægt er að breyta forstillingu með því að breyta svæðunum á síðunni **Snið (hlutverk)**. Breytingarnar verða þó ekki sýnilegar notendum sem hefur verið úthlutað á forstillingarnar fyrr en þeir skrá sig út og aftur inn.

> [!Caution]
> Ekki skal endurnefna forstillingu á meðan notendum sem notandasíðunni hefur verið úthlutað á eru skráðir inn þar sem varan kann að frjósa og endurræsing nauðsynleg.

## <a name="to-assign-a-profile-to-a-user"></a>Úthlutun forstillinga á notanda
Notendur geta úthlutað sjálfum sér hlutverki (sem stendur fyrir forstillingu) með því að velja reitinn **Hlutverk** á síðunni **Mínar stillingar**. Kerfisstjóri getur gert það sama í gegnum síðuna **Forstillingar (hlutverk)**.

1. Á síðunni **Forstillingar (hlutverk)** skaltu velja forstillingu sem á að úthluta og síðan velja aðgerðina **Listi yfir sérstillingar notenda**.
2. Á síðunni **Sérstillingar notanda** skal velja notandann sem á að úthluta forstillingunni og síðan velja aðgerðina **Breyta**.
3. Í reitnum **Auðkenni forstillingar** skal velja viðeigandi forstillingu.

> [!NOTE]
> Ef annarri forstillingu er úthlutað á notanda verða allar sérstillingar sem notandinn gerði með fyrra sniðinu varðveittar.

## <a name="to-define-user-settings-for-a-profile"></a>Til að skilgreina notandastillingar fyrir forstillingu
Á síðunni **Mínar stillingar** geta notendur skilgreint grunnhegðun reikningsins síns, svo sem hlutverkamiðstöð, tungumálið og hvaða tilkynningar þeir fá. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

Sem kerfisstjóri er hægt að skilgreina þessar stillingar fyrir forstillingu og nota þannig stillingarnar fyrir alla notendur tengda hlutverkinu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Forstillingar (hlutverk)** og veldu síðan tengda tengilinn.
2. Velja skal línuna fyrir forstillinguna sem á að breyta notandastillingum fyrir, velja aðgerðina **Skoða** og síðan velja aðgerðina **Sérstillingar notanda**.
3. Á síðunni **Sérstillingar notanda** skal opna spjaldið fyrir notandann sem á að breyta stillingum hjá.
4. Á síðunni **Sérstillingaspjald notanda** skal breyta reitunum eftir þörfum.

## <a name="to-activate-a-profile"></a>Til að virkja forstillingu
Þegar forstilling er stofnuð er hægt að velja aðra gátreiti sem skilgreina hvort, hvar og hvernig forstillingin og upplýsingarnar eru gerðar aðgengilegar fyrir notendur.

* Á síðunni **Forstilling (hlutverk)** skal velja eftirfarandi gátreiti:
    - **Virkt** til að tilgreina hvort tengda hlutverkið sé sýnilegt á síðunni **Tiltæk hlutverk** fyrir notendur að velja úr.  
    - **Nota sem sjálfgefna forstillingu** til að tilgreina forstillinguna sem á við notendur sem hafa ekki fengið úthlutað ákveðnu hlutverki.
    - **Óvirkja sérstillingar** til að tilgreina hvort notendur tengdra hlutverka geti sérstillt vinnusvæði.
    - **Sýna í hlutverkaleit** til að tilgreina hvort aðgerðir fyrir viðskiptaeiginleika sem eru hafðar með í forstillingunni sem birtist í eiginleikayfirliti hlutverkaleitar. Nánari upplýsingar er að finna í [Að finna síður með hlutverkaleit](ui-role-explorer.md)

## <a name="to-export-user-created-profiles"></a>Til að flytja út forstillingar búnar til af notendum
Hægt er að flytja út forstillingar sem hafa verið breytt annaðhvort af notanda eða af notendum, eins og gefið er til kynna af **(Búið til af notanda)** í reitnum **Uppruni**. Forstillingin er flutt út í zip-skrá sem inniheldur .al-skrár sem hægt er að endurnýta til að þróa viðbætur. Frekari upplýsingar er að finna í [Nota biðlarann til að stofna forstillingar og sérstillingar á síðunni](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Á **Forstillingar (hlutverk)** síðunni skaltu velja aðgerðina **Flytja út forstillingar búnar til að notendum**.

Zip-skrá með .al-skránum fyrir forstillingar sem nýlega hefur verið bætt við eða breytt er flutt út.

## <a name="to-delete-a-profile"></a>Til að eyða forstillingu
Hægt er að eyða forstillingu með því að velja aðgerðina **Eyða** á **Forstillingar (hlutverk)** síðunni. Eftirfarandi takmarkanir gilda hins vegar:

- Ekki er hægt að eyða forstillingu sem hefur verið úthlutað á notanda eða notendahóp.
- Ekki er hægt að eyða forstillingum sem eiga uppruna sinn í viðbótum. Fyrst verður að fjarlægja viðbótina.
- Aðeins er hægt að eyða einni forstillingu í einu.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Til að eyða öllum sérstillingum sem notandi gerði
Hægt er að eyða öllum breytingum sem notandi hefur gert á síðum sem mynda vinnusvæðið. Þetta getur til dæmis komið sér vel ef starfsmaður hefur breytt hlutverki og þarf ekki lengur sérstillinguna. Með því að eyða sérstillingum fyrir notendur breytist síðuútlitið aftur í það sem er tilgreint í forstillingunni.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sérstillingar notanda** og veldu síðan tengda tengilinn.

    Síðan **Sérstillingar notanda** birtir alla notendur sem hafa gert sérstillingar.

2. Opnaðu spjaldið fyrir notanda sem eyða á sérstillingum hjá.
3. Á síðunni **Sérstillingaspjald notanda** skal velja aðgerðina **Hreinsa sérstilltar síður** og síðan samþykkja skilaboðin sem birtast.

Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.

Einnig er hægt að eyða öllum sérstillingum síðu fyrir forstillingu. Frekari upplýsingar er að finna í [Til að eyða öllum sérstillingum fyrir forstillingu](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Til að eyða sérstillingum fyrir tilteknar síður
Hægt er að eyða öllum sérstillingum sem einn eða fleiri notendur hafa gert á síðum sem mynda vinnusvæði þeirra. Þetta getur komið sér vel, til dæmis ef breytt viðskiptaferli leiðir til þess að notendur muni ekki lengur nota sérstillingar. Með því að eyða sérstillingum fyrir notendur breytist síðuútlitið aftur í það sem er tilgreint í forstillingunni.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sérstillingar notandasíðu** og veldu síðan tengda tengilinn.

    Á síðunni **Sérstillingar notandasíðu** er listi yfir allar síður sem hafa verið sérstilltar og notandinn sem þau tilheyra.

    > [!Note]
    > Gátmerki í **Eldri sérstilling** reitnum gefur til kynna að sérstillingin hafi verið gerð í eldri útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)], sem meðhöndlaði sérstillingu öðruvísi. Notendur sem reyna að sérstilla þessar síður eru útilokaðir frá því að gera það nema þeir velji að opna síðuna. Frekari upplýsingar eru í [Af hverju er síða læst og því ekki hægt að sérsníða hana](ui-personalization-locked.md).

2. Veldu línuna fyrir sérstillingu síðunnar sem á að eyða og veldu síðan aðgerðina **Eyða**.

Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.    

Einnig er hægt að eyða einstaka sérstillingum síðu fyrir forstillingu. Frekari upplýsingar er að finna í [Til að eyða sérstillingum fyrir tilteknar síður fyrir forstillingu](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="see-also"></a>Sjá einnig  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  
