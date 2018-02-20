---
title: "Uppsetning viðbóta til að sérstilla Finance and Operations, Business Edition | Microsoft Docs"
description: "Kynntu þér hvernig skal bæta virkni og sérstilla Finance and Operations, Business Edition með því að setja upp viðbætur."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 07/07/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5deba7ee0f88c47738f3f964b9da912c730a1bd4
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="customizing-finance-and-operations-business-edition-using-extensions"></a>Sérstilling Finance and Operations, Business Edition fyrir með viðbótum
Þú getur breytt [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að setja viðbætur sem bæta við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis.
Þegar þú fyrst ræsir [!INCLUDE[d365fin](includes/d365fin_md.md)], eru nokkrar viðbætur þegar settar upp fyrir þig. Með tímanum verða fleiri viðbætur tiltækar fyrir þig, og þú getur síðan valið hvort þú viljir nota viðbótina eða ekki.

Til dæmis veitir Microsoft viðbót sem veitir samþættingu við PayPal Payments Standard. Þessi viðbót er uppsett sjálfgefið
En ef önnur viðbót er gerð sem veitir samþættingu við aðra greiðsluþjónusta, geturðu sett inn nýja viðbót og síðan valið hvaða af þessum tveimur þjónustum þú notar.  

Þú stjórnar viðbótum í **viðbótastjórnun** glugganum. Hægt er að opna þennan glugga úr heimasvæðinu. Einnig er hægt að velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu") efst í hægra horninu, slá inn **Viðbót** og velja svo tengdan tengil.  

> [!NOTE]  
>   Ef þú telur að þú ættir að hafa aðgang að viðbót en finnur ekki virknina sem í henni felst, skaltu athuga gluggann **Viðbótarstjórnun** - ef viðbótin er ekki skráð þar getur þú sett hana upp eins og lýst er í eftirfarandi kafla.  

## <a name="installing-an-extension"></a>Uppsetning viðbótar
Hér getur þú fengið nýjar viðbætur frá markaðstorginu á [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1). Hér getur þú séð allar tiltækar viðbætur fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], og þú getur fengið forrit, viðbætur og innihaldsefni fyrir aðrar Microsoft vörur. Stilltu viðeigandi síur, skoðaðu upplýsingar um hverja viðbót og fáðu viðbót fyrir þinn [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fá að markaðstorgið úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í **framlengingarstjórnun** geturðu séð eftirnafnin sem eru í uppsettri röð og þú getur opnað **Framlengingarmarkað** síðu sem sýnir [!INCLUDE[d365fin](includes/d365fin_md.md)] viðbætur sem eru í boði í AppSource. Ef valið er *Fleiri öpp* tengilinn, er farið með þig á [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Ef þú velur viðbót geturðu lesið um hvað viðbótin gerir, og þú getur fengið aðgang að hjálp fyrir viðbótinni til að læra meira. Þegar valið er að fá viðbót, verðurðu að samþykkja skilmála um notkun. Ef þú færð framlengingu frá AppSource vefsíðu verður þú skráð (ur) inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að ljúka uppsetningunni.  

Þegar þú setur upp viðbót gætirðu þurft að setja það upp, svo sem að tilgreina reikning til notkunar með **PayPal-greiðslustaðall fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]** framlengingu.
Aðrar viðbætur bæta einfaldlega reitum við fyrirliggjandi síðu, eða þeir bæta við nýjum síðum, til dæmis.   

Ef þú fjarlægir viðbót og skiptir um skoðun geturðu sett hana inn aftur. Þegar þú fjarlægir viðbót sem þú hefur verið að nota, eru gögnin geymd svo að ef þú setur þau upp aftur, eru gögnin þínn enn tiltæk.  

Sumar viðbætur eru veittar af Microsoft, og aðrar viðbætur eru veittar af [öðrum fyrirtækjum.](ui-extensions-other.md) Allar viðbætur eru prófaðar áður en þær eru gerðar tiltækar til þin, en við mælum með að þú farir í gegnum tenglana sem eru veittir með hverri viðbót til að læra meira um viðbótina áður en þú setur hana upp.  

Microsoft veitir eftirfarandi viðbætur:  

* [Dynamics GP Gagnafærsla](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee bankastreymi](ui-extensions-yodlee-bank-feeds.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [QuickBooks gagnaflutningur](ui-extensions-quickbooks-data-migration.md)  
* [Spá um sölu og birgðir](ui-extensions-sales-forecast.md)  
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)  
* [Quickbooks-viðbótin fyrir innflutning á launaskrá](ui-extensions-quickbooks-payroll.md)  
* [WorldPay-greiðslustaðall](ui-extensions-worldpay-payments-standard.md)
* [GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
* [QuickBooks gagnaflutningur á netinu](ui-extensions-quickbooks-online-data-migration.md)
* [Endurskoðandagátt](ui-extensions-accountant-portal.md)  
* [Myndgreinandi](ui-extensions-image-analyzer.md)
* [Greiðslur og afstemmingar (DK)](ui-extensions-payments-reconciliation-formats-dk.md)
* [C5 Gagnaflutningur](ui-extensions-c5-data-migration.md)

> [!NOTE]  
>  Nýjar viðbætur eru ekki tiltækar í AppSource strax eftir að við tilkynnum um uppfærslu. Þú getur fylgst með viðbótum á [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Sjá einnig
[Setja upp Envestnet Yodlee bankastreymisþjónustu](bank-how-setup-bank-statement-service.md)  
[Virkja greiðslur viðskiptamanna gegnum PayPal](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](upload-data.md)  
[Setja upp GetAddress.io UK Postal Code viðbótina](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

