---
title: "Velja notandaupplifun til að sýna eða fela ítarlegri eiginleika | Microsoft Docs"
description: "Kynntu þér hvað notandaupplifunin Basic og Essential þýða fyrir notandaviðmótið, kerfishlutana og fyrirtækið þitt."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 07/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: f8dd92a5a7398ddce64dd4fce0ce9323014a29a0
ms.contentlocale: is-is
ms.lasthandoff: 08/06/2018

---
# <a name="changing-which-features-are-displayed"></a>Breyta því hvaða eiginleikar eru sýndir
[!INCLUDE[d365fin](includes/d365fin_md.md)] er hannað til að hjálpa þér að reka fyrirtækið þitt, óháð því í hvaða geira þú ert. Í kjarna [!INCLUDE[d365fin](includes/d365fin_md.md)] að finna fjárhagsskýrslu og sölu og innkaupaferli. Þú bætir við reynslu í samræmi við þarfir fyrirtækis þíns með því að bæta við viðbótum frá AppSource eða með því að breyta upplifunarstillingum fyrir fyrirtækið þitt. Frekari upplýsingar eru í [Sérstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] Nota viðbætur](ui-extensions.md), eða kaflanum „Velja notandaupplifun til að sýna og fela eiginleika“ hér fyrir neðan.

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Velja upplifun notanda eða Sýna eða Fela eiginleika
Notandi reynsla ákvarðar hversu mikið af kjarna virkni er í boði þegar þú og samstarfsmenn þínir nota [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þú getur valið reynslu notenda fyrir fyrirtækið þitt í **Fyrirtækjaupplýsingar**, í reitnum **Reynsla**.

> [!NOTE]  
> Þessi stilling á við allir notendur í fyrirtækinu. Notendur geta sérstillt eigin upplifun enn frekar með því að breyta útliti síðu og efni. Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns og síðna](ui-personalization-user.md).  

Eftirfarandi tafla lýsir þeim reynslu sem nú er að finna.

| Upplifun | Áhrif á viðmótið |
| --- | --- |
| **Grunnatriði** |Sýnir aðeins kjarnaaðgerðir og svið fyrir kjarnastarfsemi fyrirtæki, svo sem sölu, innkaup, fjármál og birgðahald. |
| **Grunnþættir** |Sýnir allar aðgerðir og svið fyrir allar algengustu viðskiptavirknir.|
| **Úrvals** |Sýnir allar aðgerðir og svið fyrir alla viðskiptavirkni, þ.á.m. framleiðslu- og þjónustukerfi.|

> [!NOTE]  
> Upplifunin sem hægt er að velja úr [!INCLUDE[d365fin](includes/d365fin_md.md)] fer eftir leyfinu, sem kallast áætlun. Fyrir upplýsingar um **Grundvallar** og **Úrvals** áætlanir, sjá [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) á markaðssvæði Microsoft Dynamics 365. Sjá einnig [[!INCLUDE[d365fin](includes/d365fin_md.md)] Leyfisleiðbeiningar](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409).

> [!IMPORTANT]  
> Allir reglulegir notendur í lausn verða að sömu áætluninni úthlutað, grunn- eða úrvalsáskrift, áður en hægt er að velja þá upplifun fyrir fyrirtækið. Samkvæmt því getur einn notandi ekki fengið aðgang að eiginleikum úrvalsáskriftar ef einn eða fleiri aðrir notendur geta aðeins fengið aðgang að eiginleikum grunnáskriftar. Þetta á ekki við fyrir óreglulega notendur af gerðinni Team Member, innri stjórnandi, ytri endurskoðandi og úthlutaður stjórnandi, sem hver getur fengið annarri áætlun úthlutað en hinir notendurnir í lausninni.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Virkjar eiginleika úrvalsáskriftar eftir uppfærslu á áætlun
Áætlunum er úthlutað til notenda í stjórnendamiðstöðinni Office 365 í tengslum við almennu vinnuna til að búa til notendur Business Central. Frekari upplýsingar, sjá [Bæta notendum við Office 365 fyrir fyrirtæki](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Þú getur síðan skilgreint hvaða sérstakar aðgerðir og gluggar innan þeirrar upplifunar sem notendur geta fengið aðgang að með því að veita heimildasamstæður. Frekari upplýsingar eru í [Stjórna notendum og heimildum](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Til að uppfæra breytingar á áætlunum í flokkum notenda
Þegar þú hefur gert breytingu á áætlunum notenda í stjórnendamiðstöðinni Office 365, á borð við að úthluta fleiri notendum á úrvalsáskriftina, verður þú að endurspegla breytinguna í [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Skráðu þig inn sem stjórnanda.
2. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notendur** og velja svo viðeigandi tengil.
3. Í glugganum **Notendur** skaltu velja aðgerðina **Endurhlaða alla notendaflokka**.

Allar nýjar upplýsingar um áætlanir notenda og úthlutuðum notendaflokkum þeirra hafa nú verið uppfærðar samkvæmt breytingum áætlunarinnar.

### <a name="to-select-the-premium-experience"></a>Til að velja úrvalsupplifunina
Nú er hægt að halda áfram til að velja nýju upplifunina.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fyrirtækjaupplýsingar** og velja svo viðeigandi tengil.
2. Í glugganum **Fyrirtækjaupplýsingar** í flýtiflipanum **Notandaupplifun** skal velja úrvalsáskrift í reitnum **Upplifun**.

## <a name="see-also"></a>Sjá einnig .
[Stofna ný fyrirtæki](about-new-company.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Leyfishandbók](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

