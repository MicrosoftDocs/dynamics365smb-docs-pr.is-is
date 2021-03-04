---
title: Úrræðaleita vandamál með innskráningu í sjálfsafgreiðslu | Microsoft Docs
description: Kynntu þér algengustu ástæðurnar fyrir því af hverju þú getur hugsanlega ekki klárað innskráningu í Business Central, og hvernig hægt er að vinna í kringum þær.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bbfd647bd2a121d3851ff07bf11e5c3d7f689588
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756668"
---
# <a name="troubleshooting-self-service-sign-up"></a>Úrræðaleit innskráning í sjálfsafgreiðslu
Innskráning fyrir [!INCLUDE[prod_short](includes/prod_short.md)] er auðvelt og er hægt að gera mjög skjótan hátt. Hægt er að stofna reikning án endurgjalds jafnvel þó að þú sért fyrirtæki sem þegar er til. Þessi grein fjallar um vandamál sem gætu komið upp við innskráningu.

## <a name="what-email-address-can-i-use-with-business-central"></a>Hvaða netfang get ég notað með Business Central?
[!INCLUDE[prod_short](includes/prod_short.md)] krefst að notandi noti vinnu eða skóla netfang til að nýskrá. [!INCLUDE[prod_short](includes/prod_short.md)] styður ekki netföng frá tölvupóstfangsveitendum sem þjónusta neytendur eða frá fjarskiptafyrirtækjum. Þetta felur í sér outlook.com, hotmail.com, gmail.com og aðra.

Ef þú reynir að nýskrá með einka tölvupóstfang færðu skilaboð sem gefa til kynna að þú eigir að nota vinnu eða skóla netfang.

## <a name="troubleshooting"></a>Úrræðaleit
Í mörgum tilfellum er innskráning í [!INCLUDE[prod_short](includes/prod_short.md)] möguleg með því að fylgja eftirfarandi innskráningarferli. Hins vegar eru nokkrar ástæður fyrir því að þú getur ekki verið fær um að ljúka sjálfsafgreiðslu innskráningu. Taflan hér að neðan er yfirlit yfir nokkrar af algengustu ástæðum fyrir því að vera ekki fær til að ljúka skráningunni og leiðir sem þú getur farið við að leysa þessi vandamál.

| Einkenni/villuboð:  | Ástæða og leið framhjá |
| --------------------- | -------------------- |
| Fyrir Microsoft 365 tölvupóstföng sem eru ekki skráð í studdu landi færðu skilaboð eins og eftirfarandi við innskráningu:<br /><br />**Þetta gekk ekki, við styðjum ekki land þitt eða svæði enn.** |[!INCLUDE[prod_short](includes/prod_short.md)] styður eins og er aðeins Microsoft 365  tölvupóstföng sem eru skráð á takmörkuðum fjölda markaða. Nánari upplýsingar eru í [Svæði í boði](#regional-availability). |
| Persónulegir tölvupóstfang eins og nancy@gmail.com eru ekki studd. Þú færð skilaboð eins og þessi við innskráningu:<br /><br />**Þú færðir inn einka tölvupóstfang: vinsamlegast færðu inn vinnutölvupóstfang svo við getum geymt gögn fyrirtækis þíns á öruggan hátt.**<br> Eða <br> **Það lítur út eins og persónulegt netfang. Færðu inn póstfang svo við getum tengt þig við aðra í fyrirtækinu. Og ekki hafa áhyggjur. Við munum ekki deila netfanginu þínu með neinum.** |[!INCLUDE[prod_short](includes/prod_short.md)] styður ekki netföng frá tölvupóstfangsveitendum sem þjónusta neytendur eða frá fjarskiptafyrirtækjum. Til að klára innskráninguna, reyndu aftur með því að nota tölvupóstfang sem þér var úthlutað af skólanum eða vinnunni. Ef þú getur enn ekki skrá sig og ert tilbúin/n til að ljúka ítarlegra uppsetningarferli, getur þú skrá sig fyrir nýrri Microsoft 365 prufuáskrift og nota það netfang til að skrá þig inn. |
| .gov eða .mil tölvupóstfang Þú færð skilaboð eins og eftirfarandi við innskráningu:<br /><br />**[!INCLUDE[prod_short](includes/prod_short.md)] ótiltækt: [!INCLUDE[prod_short](includes/prod_short.md)] er ekki tiltækt fyrir notendur með .gov eða .mil tölvupóst eins og stendur. Notaðu annað vinnu tölvupóstfang eða athugaðu aftur seinna.** <br>Eða <br>**Við getum ekki lokið við að skrá þig. Það lítur út fyrir að [!INCLUDE[prod_short](includes/prod_short.md)] er ekki í boði fyrir vinnu þína eða skóla.** |[!INCLUDE[prod_short](includes/prod_short.md)] styður ekki þennan .gov eða .mil póstföng eins og stendur. |
| Sjálfsafgreiðslu innskráning er ekki virkjuð. Þú færð skilaboð eins og þessi við innskráningu:<br /><br />**Við getum ekki lokið við að skrá þig. Tölvudeildin þín hefur slökkt á skráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Hafðu samband við þá til að ljúka skráningu.** <br>Eða <br> **Það lítur út eins og persónulegt netfang. Færðu inn póstfang svo við getum tengt þig við aðra í fyrirtækinu. Og ekki hafa áhyggjur. Við munum ekki deila netfanginu þínu með neinum.** |Þjónustustjóri fyrirtækisins þíns hefur gert sjálfvirka skráningu óvirka fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Til að klára innskráninguna, hafðu samband við tæknistjóra og biddu þá um að fara að leiðbeiningunum á [þessari síðu](/dynamics365/business-central/dev-itpro/developer/devenv-business-central-manage-selfservice-signups) til að leyfa fyrirliggjandi notendum að innskrá sig í [!INCLUDE[prod_short](includes/prod_short.md)] og leyfa nýjum notendum að ganga til liðs við núverandi leigjanda. Þú gætir einnig upplifað þetta vandamál ef þú skráðir þig í Microsoft 365 í gegnum félaga. |
| Tölvupóstfang er ekki Microsoft 365 kenni. Þú færð skilaboð eins og þessi við innskráningu:<br /><br />**Við getum ekki fundið þig á contoso.com. Notarðu annað auðkenni í vinnunni eða skólanum? Prófaðu að skrá þig inn og ef það virkar ekki skaltu hafa samband við tæknideildina þína.** |Fyrirtæki þitt notar kenni til að skrá sig inn í Microsoft 365 og aðrar Microsoft þjónustur, sem eru aðrar en tölvupóstfang þitt. Til dæmis gætu þitt tölvupóstfang verið Nancy.Smith@contoso.com en Notandakenni er nancys@contoso.com. Til að ljúka við innskráningu, notaðu kenni sem fyrirtæki þitt hefur úthlutað til að skrá sig inn í Microsoft 365 eða aðrar Microsoft þjónustur. Ef þú veist ekki hvað það er, hafðu samband við tæknistjórann þinn. Ef þú getur enn ekki skrá sig og getur lokið ítarlegra uppsetningarferli, getur þú skrá sig fyrir nýrri Microsoft 365 prufuáskrift og nota það netfang til að skrá þig inn. |
| Ef Microsoft 365 reikningurinn þinn er skráður í studdu land og þú ert að skrá þig fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á meðan í öðru landi færðu skilaboð eins og eftirfarandi við innskráningu:<br /><br />**Þetta gekk ekki, við styðjum ekki land þitt eða svæði enn.**| Microsoft 365 áskrift fyrirtækis þíns er skráð í tiltekið land í Microsoft 365 stjórnunargáttinni. Upplifun innskráningar fyrir [!INCLUDE[prod_short](includes/prod_short.md)] notar tungumálið og landsstaðalinn sem núverandi vafri notar og þar af leiðandi geturðu fengið villuboðin þótt þú sért í studdu landi. Spurðu kerfisstjóra til að sannreyna land sem er tilgreint í forstillingu fyrirtækis í [Microsoft 365 stjórnunargáttinni](https://portal.office.com/adminportal/home#/companyprofile). Ef til vill þarf að nota annan reikning fyrir [!INCLUDE[prod_short](includes/prod_short.md)].|

## <a name="regional-availability"></a>Svæði í boði

[!INCLUDE[prod_short](includes/prod_short.md)] er í boði í mörgum löndum eða svæðum með staðfæringu frá Microsoft eða samþykktum staðfæringaraðila. Tæmandi listi yfir studd lönd og svæði er að finna í [Framboð eftir löndum/svæðum og studdar þýðingar](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  

Til að sjá yfirlit yfir markaði sem nú eru studdir í Dynamics 365 skal skoða skyggnuna [Alþjóðlegt framboð á Microsoft Dynamics 365](/dynamics365/get-started/availability). Yfirlit yfir staðbundna virkni í [!INCLUDE[prod_short](includes/prod_short.md)] er að finna á lendingarsíðunni [Staðbundin virkni](about-localization.md).  

## <a name="see-also"></a>Sjá einnig

[Velkomin(n) í [!INCLUDE[prod_short](includes/prod_long.md)]](index.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Staðbundin virkni](about-localization.md)  
[Framboð eftir löndum/svæðum og studdar þýðingar](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  
[Alþjóðlegt framboð á Microsoft Dynamics 365](/dynamics365/get-started/availability)  


[!INCLUDE[footer-include](includes/footer-banner.md)]