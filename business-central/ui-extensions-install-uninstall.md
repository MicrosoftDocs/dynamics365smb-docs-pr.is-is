---
title: Setja upp og fjarlægja viðauka
description: Frekari upplýsingar um uppsetningu og fjarlægingu viðbóta í Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500
ms.date: 05/24/2022
ms.author: solsen
ms.openlocfilehash: a70ea442ffb9d6e5f131e4d720da57f033474e16
ms.sourcegitcommit: 6eeac924d8e211080316ce5068e3d4fb5a2d5ed9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804657"
---
# <a name="install-and-uninstall-extensions-in-business-central"></a>Setja upp og fjarlægja viðauka í Viðskiptamiðinu

Þú getur breytt [!INCLUDE[prod_short](includes/prod_short.md)] með því að setja viðbætur sem bæta t.d. við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis. Frekari upplýsingar eru í [Sérstilling Business Central með viðbótum](ui-extensions.md).

> [!NOTE]
> Til að setja upp eða fjarlægja viðbætur frá AppSource eða bæta við viðbótum fyrir hvern leigjanda fyrir sig eru réttar heimildir nauðsynlegar. Þú verður að vera meðlimur í EXTEND. STJÓR. - STJÓRNANDA Notendahópur eða þú verður að hafa EXTEND. STJÓR. - STJÓRNANDA heimildasamstæða. Ef þú ert stjórnandi geturðu úthlutað notendaflokkum og heimildum til annarra notenda fyrirtækisins.
>
> Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.

> [!NOTE]  
> Heimildasamstæðan **VIÐBÓTARSTJÓRNUN - STJÓRNANDI** var kynnt til sögunnar í Business Central 2021 útgáfutímabili 1 sem staðgengill fyrir **D365 VIÐBÓTASTJÓRNUN** heimildasamstæðuna í eldri útgáfum.

## <a name="install-an-extension"></a><a name="install"></a> Setja upp framlengingu

Þú stjórnar viðbótum á síðunni **Viðbótastjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Annars geturðu valið **Leita að síðu eða Tilkynna** táknið ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") efst í hægra horninu skal velja **Viðbót** og síðan velja viðkomandi tengil.  

Hægt er að fá nýjar viðbætur úr markaðstorginu á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Hér getur þú séð allar tiltækar viðbætur fyrir [!INCLUDE[prod_short](includes/prod_short.md)], og þú getur fengið forrit, viðbætur og innihaldsefni fyrir aðrar Microsoft vörur. Stilltu viðeigandi síur, skoðaðu upplýsingar um hverja viðbót og fáðu viðbót fyrir þinn [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fá að markaðstorgið úr [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **framlengingarstjórnun** geturðu séð eftirnöfnin sem eru í uppsettri röð og þú getur opnað **Framlengingarmarkað** síðu sem sýnir [!INCLUDE[prod_short](includes/prod_short.md)] viðbætur sem eru í boði í AppSource. Ef þú velur *fleiri apps* tengil þá ert þú að taka til [AppSource . microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Ef þú velur viðbót geturðu lesið um hvað viðbótin gerir, og þú getur fengið aðgang að hjálp fyrir viðbótinni til að læra meira. Þegar valið er að fá viðbót, verðurðu að samþykkja skilmála um notkun. Ef þú færð framlengingu af AppSource heimasíðu þá skráir þú þig inn til [!INCLUDE[prod_short](includes/prod_short.md)] að klára uppsetninguna.  

Þegar þú setur upp viðbót gætirðu þurft að setja það upp, svo sem að tilgreina reikning til notkunar með **PayPal-greiðslustaðall fyrir [!INCLUDE[prod_short](includes/prod_short.md)]** framlengingu.
Aðrar viðbætur bæta einfaldlega reitum við fyrirliggjandi síðu, eða þeir bæta við nýjum síðum, til dæmis.

Ef þú fjarlægir viðbót og skiptir um skoðun geturðu sett hana inn aftur. Þegar þú fjarlægir viðbót sem þú hefur verið að nota, eru gögnin geymd svo að ef þú setur þau upp aftur, eru gögnin þínn enn tiltæk. Einhverjar viðbætur eru nauðsynlegar. Þú ert hindraður í að fjarlægja þessa viðauka af síðunni um **Framlengingarstjórnun**. Ef þú prófar birtast villuboð.

Sumar viðbætur eru veittar af Microsoft, og aðrar viðbætur eru veittar af [öðrum fyrirtækjum.](ui-extensions-other.md) Allir Viðaukar eru prófaðir áður en þeir eru gerðir aðgengilegir, en mælt er með því að nálgast þau tengsl sem bjóðast við hverja framlengingu til að fá frekari upplýsingar um framlengingu áður en valið er að setja það upp.

Microsoft veitir eftirfarandi viðbætur:

* [AMC Banking 365 Fundamentals Viðbót](ui-extensions-amc-banking.md)
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)
* [Fyrirtækjamiðstöð](ui-extensions-company-hub.md)  
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
* [VSK-flokkur](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK - C5 gagnaflutningur](ui-extensions-c5-data-migration.md)
* [DK - Greiðslur og afstemmingar](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK - Skráarsnið skatts](ui-extensions-tax-file-formats-dk.md)
* [Viðbótin GetAddress.io UK Postcodes](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA - Senda greiðslutilkynningu](ui-extensions-send-remittance-advice.md)

## <a name="upload-a-per-tenant-extension-pte"></a>Sækja um framlengingu á leigjanda (PTE)

Þú hleður upp PTE með því að nota síðuna **Viðbótastjórnun**. Á síðunni **Viðbótastjórnun** skal fara í **Stjórna**, síðan velja **Hlaða upp viðbót**. Á síðunni **Hlaða og setja upp viðbót** skal tilgreina forritsskrána sem á að hlaða upp. Til að halda áfram skal velja **hnappinn Samþykkja** og síðan **Virkja hnappinn, sem mun hefja ferlið á því að nota** Pte.

Ef PTE inniheldur breytingar á grindarverki er mögulegt að *knýja* fram upphleðslu þess. Til að gera það skal í **Samstilling skema** velja valkostinn **Þvinga**. Þú færð staðfestingarglugga til að samþykkja áður en haldið er áfram.  

## <a name="uninstall-an-extension"></a>Fjarlægja nafnauka

Hægt er að fjarlægja viðbót með því að nota **Viðbótastjórnun**. Til að fjarlægja nafnauka er það valið á síðunni og síðan er **fjarlægingaraðgerðin** valin. Ef þú fjarlægir viðbót og skiptir um skoðun geturðu sett viðbótina inn aftur.

Þegar búið er að fjarlægja framlengingu sem þú hefur notað, er sjálfgefið að gögn séu varðveitt ef framlenging er sett upp aftur. Hægt er að velja að eyða gögnunum með viðbótinni. Þessari aðgerð er stjórnað af Gagnatrofann **með því að** Eyða framlenginu. Sjálfgefið er að slökkt **sé** á þessum rofa. Þegar reynt er að kveikja á **Skiptigagnagögnum** eyðu-Framlengingar fyrir framlengingu færðu staðfestingarglugga og þú verður að velja **Já** til að kveikja á honum. **Eftir að kveikt er á Framlengingargagnagögnum** er hægt að fjarlægja eftirnafn og biðja um staðfestingu á að þú viljir fjarlægja eftirnafn og eyða gögnunum.

> [!IMPORTANT]  
> - Það geta verið aðrir Viðaukar sem krefjast eða fara eftir viðaukanum sem á að fjarlægja til þess að vinna. Um aðra viðauka vísast til *háðs*. Ekki er hægt að fjarlægja framlengingu nema háði þeirra sé einnig tekinn niður.
> - Þegar valið er að fjarlægja nafnauka sem hefur einn eða fleiri háðan þá fær maður staðfestingarglugga sem er listi háðs og spyr hvort þú viljir fjarlægja eftirnafn og allan hans háða. Þú verður að velja **Já** til að halda áfram.
> - Ef kveikt er á gagnarofi til að **Eyða framlengingu eyða öll gögn fyrir viðaukanum** auk **gögnum fyrir alla háða** viðauka. Ekki er hægt að afturkalla þessa aðgerð.
> - Sumar viðbætur eru nauðsynlegar. Þú ert að koma í veg fyrir að þetta sé fjarlægt af síðunni **Viðbótastjórnun**. Ef þú prófar birtast villuboð.  

## <a name="see-also"></a>Sjá einnig

[Sérstilla Business Central](ui-customizing-overview.md)  
[Microsoft Business Central viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[Virkja greiðslur viðskiptamanna gegnum PayPal](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Setja upp GetAddress.io UK Postal Code viðbótina](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]