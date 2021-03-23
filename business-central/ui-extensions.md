---
title: Setja upp viðbætur til að sérstilla Business Central
description: Kynntu þér hvernig skal bæta virkni og sérstilla Business Central með því að setja upp viðbætur.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 03/02/2021
ms.author: edupont
ms.openlocfilehash: d92fbe7c21da74c7818be4f249cdb373ed73539f
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493279"
---
# <a name="customizing-business-central-online-using-extensions"></a>Business Central Online sérstillt með viðbótum

Þú getur breytt [!INCLUDE[prod_short](includes/prod_short.md)] Online með því að setja viðbætur sem bæta við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis.

> [!NOTE]
> Til að setja upp viðbætur frá AppSource eða bæta við viðbótum fyrir hvern leigjanda fyrir sig eru réttar heimildir nauðsynlegar. Annaðhvort verður þú að vera meðlimur notendaflokksins D365 EXTENSION MGT eða vera með heimildasamstæðu D365 EXTENSION MGT. Ef þú ert stjórnandi geturðu úthlutað notendaflokkum og heimildum til annarra notenda fyrirtækisins.

Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.

> [!IMPORTANT]  
> Uppfærsla viðbóta á leigjanda og uppsetning AppSource viðbóta er ekki studd í gegnum **Viðbótastjórnun** síðu fyrir uppsetningar á forútgáfu. Ekki er hægt að setja upp viðbætur AppSource á staðnum, þar á meðal hýsingartengdar uppsetningar.

Þegar þú fyrst ræsir [!INCLUDE[prod_short](includes/prod_short.md)], eru nokkrar viðbætur þegar settar upp fyrir þig. Með tímanum verða fleiri viðbætur tiltækar fyrir þig, og þú getur síðan valið hvort þú viljir nota viðbótina eða ekki.

Til dæmis veitir Microsoft viðbót sem veitir samþættingu við PayPal Payments Standard. Þessi viðbót er uppsett sjálfgefið
En ef önnur viðbót er gerð sem veitir samþættingu við aðra greiðsluþjónusta, geturðu sett inn nýja viðbót og síðan valið hvaða af þessum tveimur þjónustum þú notar.  

Þú stjórnar viðbótum á síðunni **viðbótastjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Einnig er hægt að velja **Leita að síðu eða skýrslu** táknið ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") efst í hægra horninu, slá inn **Viðbætur** og velja svo tengda hlekkinn. Nánari upplýsingar eru í [Uppsetning og fjarlæging viðbóta](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Ef þú telur að þú ættir að hafa aðgang að viðbót en finnur ekki virknina sem í henni felst, skaltu athuga síðuna **Viðbótarstjórnun** - ef viðbótin er ekki skráð þar getur þú sett hana upp eins og lýst er í eftirfarandi kafla.  

> [!NOTE]  
> Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[prod_short](includes/prod_short.md)] Online. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fá að markaðstorgið úr [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **framlengingarstjórnun** geturðu séð eftirnöfnin sem eru í uppsettri röð og þú getur opnað **Framlengingarmarkað** síðu sem sýnir [!INCLUDE[prod_short](includes/prod_short.md)] viðbætur sem eru í boði í AppSource. Ef valið er *Fleiri öpp* tengilinn, er farið með þig á [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Ef þú velur viðbót geturðu lesið um hvað viðbótin gerir, og þú getur fengið aðgang að hjálp fyrir viðbótinni til að læra meira. Þegar valið er að fá viðbót, verðurðu að samþykkja skilmála um notkun. Ef þú færð viðbótina frá AppSource vefsíðu verður þú skráð (ur) inn í [!INCLUDE[prod_short](includes/prod_short.md)] til að ljúka uppsetningunni.  

Þegar þú setur upp viðbót gætirðu þurft að setja það upp, svo sem að tilgreina reikning til notkunar með **PayPal-greiðslustaðall fyrir [!INCLUDE[prod_short](includes/prod_short.md)]** framlengingu.
Aðrar viðbætur bæta einfaldlega reitum við fyrirliggjandi síðu, eða þeir bæta við nýjum síðum, til dæmis.   

Ef þú fjarlægir viðbót og skiptir um skoðun geturðu sett hana inn aftur. Þegar þú fjarlægir viðbót sem þú hefur verið að nota, eru gögnin geymd svo að ef þú setur þau upp aftur, eru gögnin þínn enn tiltæk. Einhverjar viðbætur eru nauðsynlegar. Þú ert að koma í veg fyrir að þetta sé fjarlægt af síðunni **Viðbótastjórnun**. Ef þú prófar birtast villuboð.  

Sumar viðbætur eru veittar af Microsoft, og aðrar viðbætur eru veittar af [öðrum fyrirtækjum.](ui-extensions-other.md) Allar viðbætur eru prófaðar áður en þær eru gerðar tiltækar til þin, en við mælum með að þú farir í gegnum tenglana sem eru veittir með hverri viðbót til að læra meira um viðbótina áður en þú setur hana upp.  

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

> [!NOTE]  
> Hægt er að fylgjast með nýjum viðbótum frá Microsoft og öðrum birgjum á [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="see-also"></a>Sjá einnig

[Sérstilla Business Central](ui-customizing-overview.md)  
[Microsoft Business Central viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[Virkja greiðslur viðskiptamanna gegnum PayPal](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Setja upp GetAddress.io UK Postal Code viðbótina](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Hafist handa](product-get-started.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
