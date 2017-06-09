---
title: "Sérsníða Dynamics 365 for Financials með því að nota viðbætur | Microsoft Docs"
description: "Aðlaga Dynamics 365 for Financials með því að nota eftirnafn"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1de01d9944489f862dfc6db145c1542c3d0dd2e3
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="customizing-dynamics-365-for-financials-using-extensions"></a>Aðlaga Dynamics 365 for Financials með því að nota eftirnafn
Þú getur breytt [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að setja viðbætur sem bæta við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis.
Þegar þú fyrst ræsir [!INCLUDE[d365fin](includes/d365fin_md.md)], eru nokkrar viðbætur þegar settar upp fyrir þig. Með tímanum verða fleiri viðbætur tiltækar fyrir þig, og þú getur síðan valið hvort þú viljir nota viðbótina eða ekki.

Til dæmis veitir Microsoft viðbót sem veitir samþættingu við PayPal Payments Standard. Þessi viðbót er uppsett sjálfgefið
En ef önnur viðbót er gerð sem veitir samþættingu við aðra greiðsluþjónusta, geturðu sett inn nýja viðbót og síðan valið hvaða af þessum tveimur þjónustum þú notar.  

Þú stjórnar viðbótum í **viðbótastjórnun** glugganum. Hægt er að opna þennan glugga úr heimasvæðinu. Einnig er hægt að velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu") efst í hægra horninu, slá inn **Viðbót** og velja svo tengdan tengil.  

**Athugaðu**: Ef þú telur að þú ættir að hafa aðgang að framlengingu en þú finnur ekki virkni sína skaltu athuga gluggann **Viðbótarstjórnun** ef framlengingin er ekki skráð þar getur þú sett hana upp eins og lýst er í eftirfarandi kafla.  

## <a name="installing-an-extension"></a>Uppsetning viðbótar
Hægt er að fá nýja viðbætur úr markaðstorginu á [AppSource.microsoft.com](https://appsource.microsoft.com/). Hér getur þú séð allar tiltækar viðbætur fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], og þú getur fengið forrit, viðbætur og innihaldsefni fyrir aðrar Microsoft vörur. Stilltu viðeigandi síur, skoðaðu upplýsingar um hverja viðbót og fáðu viðbót fyrir þinn [!INCLUDE[d365fin](includes/d365fin_md.md)].  
**Athugaðu**: Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fá að markaðstorgið úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í **framlengingarstjórnun** geturðu séð eftirnafnin sem eru í uppsettri röð og þú getur opnað **Framlengingarmarkað** síðu sem sýnir [!INCLUDE[d365fin](includes/d365fin_md.md)] viðbætur sem eru í boði í AppSource. Ef valið er *Fleiri öpp* tengilinn, er farið með þig á [AppSource.microsoft.com](https://appsource.microsoft.com/).  

Ef þú velur viðbót geturðu lesið um hvað viðbótin gerir, og þú getur fengið aðgang að hjálp fyrir viðbótinni til að læra meira. Þegar valið er að fá viðbót, verðurðu að samþykkja skilmála um notkun. Ef þú færð framlengingu frá AppSource vefsíðu verður þú skráð (ur) inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að ljúka uppsetningunni.  

Þegar þú setur upp viðbót gætirðu þurft að setja það upp, svo sem að tilgreina reikning til notkunar með **PayPal-greiðslustaðall fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]** framlengingu.
Aðrar viðbætur bæta einfaldlega reitum við fyrirliggjandi síðu, eða þeir bæta við nýjum síðum, til dæmis.   

Ef þú fjarlægir viðbót og skiptir um skoðun geturðu sett hana inn aftur. Þegar þú fjarlægir viðbót sem þú hefur verið að nota, eru gögnin geymd svo að ef þú setur þau upp aftur, eru gögnin þínn enn tiltæk.  

Sumar viðbætur eru veittar af Microsoft, og aðrar viðbætur eru veittar af [öðrum fyrirtækjum.](ui-extensions-other.md) Allar viðbætur eru prófaðar áður en þær eru gerðar tiltækar til þin, en við mælum með að þú farir í gegnum tenglana sem eru veittir með hverri viðbót til að læra meira um viðbótina áður en þú setur hana upp.  

Microsoft veitir eftirfarandi viðbætur:  

* [Dynamics GP Gagnafærsla](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee bankastreymi](ui-extensions-yodlee-bank-feeds.md)  
* [PayPal-greiðslustaðall](ui-extensions-paypal-payments-standard.md)  
* [QuickBooks gagnaflutningur](ui-extensions-quickbooks-data-migration.md)  
* [Spá um sölu og birgðir](ui-extensions-sales-forecast.md)  
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)  
* [Quickbooks-viðbótin fyrir innflutning á launaskrá](ui-extensions-quickbooks-payroll.md)  
* [WorldPay-greiðslustaðall](ui-extensions-worldpay-payments-standard.md)
* [GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)

## <a name="see-also"></a>Sjá einnig
[Hvernig á að: Setja upp Envestnet Yodlee bankastreymisþjónustu](bank-how-setup-bank-statement-service.md)  
[Hvernig á að: Virkja greiðslur viðskiptamanna gegnum PayPal](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](upload-data.md)  
[Setja upp GetAddress.io UK Postal Code viðbótina](uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Viðbætur frá öðrum veitum](ui-extensions-other.md).  
[Velkomin í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]] (index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
