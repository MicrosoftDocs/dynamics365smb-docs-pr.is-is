---
title: Uppsetning og fjarlæging viðbóta í Business Central  | Microsoft Docs
description: Frekari upplýsingar um uppsetningu og fjarlægingu viðbóta í Business Central.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.date: 09/04/2020
ms.author: solsen
ms.openlocfilehash: da6e53a314438ef7ce5063febf8ece1d18c69f7b
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766092"
---
# <a name="installing-and-uninstalling-extensions-in-business-central"></a>Uppsetning og fjarlæging viðbóta í Business Central

Þú getur breytt [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að setja viðbætur sem bæta t.d. við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis. Frekari upplýsingar eru í [Sérstilling Business Central með viðbótum](ui-extensions.md).

> [!NOTE]
> Til að setja upp viðbætur frá AppSource eða bæta við viðbótum fyrir hvern leigjanda fyrir sig eru réttar heimildir nauðsynlegar. Annaðhvort verður þú að vera aðili að notendaflokknum D365 EXTENSION MGMT eða vera með heimildasamstæðu D365 EXTENSION MGMT. Ef þú ert stjórnandi geturðu úthlutað notendaflokkum og heimildum til annarra notenda fyrirtækisins.<br /><br />
Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.

## <a name="installing-an-extension"></a>Uppsetning viðbótar

Þú stjórnar viðbótum á síðunni **Viðbótastjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Einnig er hægt að velja **Leita að síðu eða skýrslu** táknið ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") efst í hægra horninu, slá inn **Viðbætur** og velja svo tengda hlekkinn.  

Hægt er að fá nýjar viðbætur úr markaðstorginu á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Hér getur þú séð allar tiltækar viðbætur fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)], og þú getur fengið forrit, viðbætur og innihaldsefni fyrir aðrar Microsoft vörur. Stilltu viðeigandi síur, skoðaðu upplýsingar um hverja viðbót og fáðu viðbót fyrir þinn [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
> Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fá að markaðstorgið úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Á síðunni **framlengingarstjórnun** geturðu séð eftirnöfnin sem eru í uppsettri röð og þú getur opnað **Framlengingarmarkað** síðu sem sýnir [!INCLUDE[d365fin](includes/d365fin_md.md)] viðbætur sem eru í boði í AppSource. Ef valið er *Fleiri öpp* tengilinn, er farið með þig á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Ef þú velur viðbót geturðu lesið um hvað viðbótin gerir, og þú getur fengið aðgang að hjálp fyrir viðbótinni til að læra meira. Þegar valið er að fá viðbót, verðurðu að samþykkja skilmála um notkun. Ef þú færð viðbótina frá AppSource vefsíðu verður þú skráð (ur) inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að ljúka uppsetningunni.  

Þegar þú setur upp viðbót gætirðu þurft að setja það upp, svo sem að tilgreina reikning til notkunar með **PayPal-greiðslustaðall fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]** framlengingu.
Aðrar viðbætur bæta einfaldlega reitum við fyrirliggjandi síðu, eða þeir bæta við nýjum síðum, til dæmis.

Ef þú fjarlægir viðbót og skiptir um skoðun geturðu sett hana inn aftur. Þegar þú fjarlægir viðbót sem þú hefur verið að nota, eru gögnin geymd svo að ef þú setur þau upp aftur, eru gögnin þínn enn tiltæk. Einhverjar viðbætur eru nauðsynlegar. Þú ert að koma í veg fyrir að þetta sé fjarlægt af síðunni **Viðbótastjórnun**. Ef þú prófar birtast villuboð.

Sumar viðbætur eru veittar af Microsoft, og aðrar viðbætur eru veittar af [öðrum fyrirtækjum.](ui-extensions-other.md) Allar viðbætur eru prófaðar áður en þær eru gerðar tiltækar til þin, en við mælum með að þú farir í gegnum tenglana sem eru veittir með hverri viðbót til að læra meira um viðbótina áður en þú setur hana upp.

Microsoft veitir eftirfarandi viðbætur:

* [Endurskoðandagátt fyrir Business Central](ui-extensions-accountant-portal.md)  
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md) 
* [Dynamics GP Gagnafærsla](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md) 
* [Essential viðskiptainnsýn](ui-extensions-essential-business-insights.md)   
* [Myndgreinandi](ui-extensions-image-analyzer.md) 
* [Snjallský](ui-extensions-data-replication.md)    
* [Grunnur snjallskýs](ui-extensions-intelligent-cloud.md)  
* [Greiðsludráttarspár](ui-extensions-late-payment-prediction.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md) 
* [QuickBooks gagnaflutningur](ui-extensions-quickbooks-data-migration.md)   
* [QuickBooks Online Gagnaflutningur](ui-extensions-quickbooks-online-data-migration.md) 
* [Quickbooks-viðbótin fyrir innflutning á launaskrá](ui-extensions-quickbooks-payroll.md) 
* [Sölu- og birgðaspár](ui-extensions-sales-forecast.md)   
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md) 
* [AMC Banking 365 Fundamentals Viðbót](ui-extensions-amc-banking.md)    
* [DK - C5 gagnaflutningur](ui-extensions-c5-data-migration.md)  
* [DK - Greiðslur og afstemmingar](ui-extensions-payments-reconciliation-formats-dk.md)  
* [DK - Skráarsnið skatts](ui-extensions-tax-file-formats-dk.md) 
* [UK - GetAddress.io UK póstnúmer](ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Senda greiðslutilkynningu](ui-extensions-send-remittance-advice.md) 
* [Microsoft Business Central viðbætur frá öðrum veitum](ui-extensions-other.md)

## <a name="uninstalling-an-extension"></a>Fjarlæging viðbótar

Hægt er að fjarlægja viðbót með því að nota **Viðbótastjórnun**. Ef þú fjarlægir viðbót og skiptir um skoðun geturðu sett viðbótina inn aftur. Þegar þú fjarlægir viðbót sem þú hefur verið að nota eru gögnin sjálfkrafa geymd svo ef þú vilt setja upp viðbótina aftur. Hægt er að velja að eyða gögnunum með viðbótinni. Þessu er stjórnað af gátreitnum **Eyða gögnum viðbótar**. Sjálfgefið er að þessi gátreitur sé *ekki virkur*.

> [!IMPORTANT]  
> Ef **Eyða gögnum viðbótar** er valið birtist staðfestingargluggi og þú verður að velja **Í lagi**. Ef hakað er í **Eyða gögnum viðbótar** er hægt að fjarlægja viðbótina og beðið er um staðfestingu á því að þú viljir fjarlægja viðbótina og eyða gögnunum. Ekki er hægt að afturkalla þessa aðgerð.
Sumar viðbætur eru nauðsynlegar. Þú ert að koma í veg fyrir að þetta sé fjarlægt af síðunni **Viðbótastjórnun**. Ef þú prófar birtast villuboð.  


## <a name="see-also"></a>Sjá einnig
[Stækka Dynamics 365 Business Central](about-develop-extensions.md)  
[Microsoft Business Central viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[Virkja greiðslur viðskiptamanna gegnum PayPal](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Setja upp GetAddress.io UK Postal Code viðbótina](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Hafist handa](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  