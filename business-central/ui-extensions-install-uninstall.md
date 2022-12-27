---
title: Setja upp og fjarlægja forrit
description: Kynntu þér hvernig þú getur sett upp og fjarlægt forrit og viðbætur í Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500, 20350
ms.date: 09/22/2022
ms.author: solsen
ms.openlocfilehash: db08c13d5e6a5dd29cf9a32b56ab3b5fa9ce77f9
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605982"
---
# <a name="install-and-uninstall-extensions-apps-in-business-central"></a>Setja upp og fjarlægja viðbætur (forrit) í Business Central

Þú getur breytt [!INCLUDE[prod_short](includes/prod_short.md)] með því að setja upp forrit sem bæta t.d. við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis. Frekari upplýsingar eru í [Sérstilling Business Central með viðbótum](ui-extensions.md).

> [!NOTE]
> Til að setja upp eða fjarlægja forrit úr AppSource eða bæta við forritum fyrir hvern leigjanda fyrir sig þarf að vera með réttar heimildir. Þú verður að vera meðlimur í EXTEND. STJÓR. - STJÓRNANDA Notendahópur eða þú verður að hafa EXTEND. STJÓR. - STJÓRNANDA heimildasamstæða. Ef þú ert stjórnandi geturðu úthlutað notendaflokkum og heimildum til annarra notenda fyrirtækisins.
>
> Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.

Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.

## <a name="install-an-extension"></a><a name="install"></a>Setja upp viðbót

Þú stjórnar forritum og viðbótum á síðunni **Viðbótastjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Annars geturðu valið **Leita að síðu eða Tilkynna** táknið ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") efst í hægra horninu skal velja **Viðbót** og síðan velja viðkomandi tengil.  

Hægt er að fá ný forrit úr markaðstorginu á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Markaðstorgið býður upp á öll tiltæk forrit fyrir [!INCLUDE[prod_short](includes/prod_short.md)] auk forrita og efnispakka fyrir aðrar Microsoft-vörur. Stilltu viðeigandi síur, skoðaðu upplýsingar um hverja viðbót og fáðu viðbót fyrir þinn [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fara í AppSource úr [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **framlengingarstjórnun** geturðu séð forritin sem eru í uppsettri röð og þú getur opnað **Framlengingarmarkað** síðu sem sýnir [!INCLUDE[prod_short](includes/prod_short.md)] forritin sem eru í boði í AppSource. Ef valið er *Fleiri forrit* tengilinn, er farið með þig á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Ef þú velur forrit geturðu lesið um hvað forritið gerir og þú getur fengið aðgang að hjálp fyrir forritið til að læra meira. Þegar valið er að fá forrit, verðurðu að samþykkja skilmála um notkun þess. Ef þú færð forritið af AppSource vefsíðunni verður þú skráð(ur) inn í [!INCLUDE[prod_short](includes/prod_short.md)] til að ljúka uppsetningunni.  

Þegar þú hefur sótt forrit gætir þú þurft að setja það upp. Sum forrit krefjast þess að þú veitir upplýsingar áður en þú getur notað þau. Eftir að þú til dæmis setjur upp forritið **PayPal Payments Standard** þarftu að tilgreina netfang eða reikningskenni söluaðila fyrir PayPal-reikninginn þinn. Til að setja upp forrit eða til að finna út hvaða upplýsingar vantar skaltu velja á síðunni **Uppsettar viðbætur** aðgerðina **Setja upp**.  

Önnur forrit bæta einfaldlega reitum við fyrirliggjandi síðu, eða þau bæta við nýjum síðum, til dæmis.

Ef þú fjarlægir forrit og skiptir um skoðun geturðu sett það inn aftur. Þegar þú fjarlægir forrit sem þú hefur verið að nota, eru gögnin geymd svo að ef þú setur það upp aftur, eru gögnin þín enn tiltæk. Sum forrit eru nauðsynleg. Þú ert að koma í veg fyrir að þessi forrit séu fjarlægð af síðunni **Viðbótastjórnun**. Ef þú prófar birtast villuboð.

Sum forrit eru í boði Microsoft og önnur forrit eru í boði [annarra fyrirtækja](ui-extensions-other.md). Öll forrit eru prófuð áður en þau eru gerð tiltæk fyrir þig, en við mælum með að þú farir í gegnum tenglana sem fylgja hverju forriti til að kynna þér forritið betur áður en þú setur það upp.

Microsoft veitir eftirfarandi forrit:

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

## <a name="set-up-an-extension"></a>Setja upp viðbót
Þegar þú hefur sótt forrit gætir þú þurft að setja það upp. Til dæmis þarftu að tilgreina PayPal-reikningin sem á að nota fyrir forritið **PayPal Payments Standard fyrir [!INCLUDE[prod_short](includes/prod_short.md)]**. Ef það er tilfellið, þegar uppsetning lýkur mun [!INCLUDE[prod_short](includes/prod_short.md)] spyrja hvort þú viljir setja forritið upp strax. Uppsetningar geta verið nauðsynlegar til að forritið virki eða valfrjálsar.

Ef þú velur að setja forritið upp strax og það er með nauðsynleg skref mun [!INCLUDE[prod_short](includes/prod_short.md)] opna nauðsynlegu skrefin. Uppsetningin getur verið annaðhvort síða þar sem þú slærð inn upplýsingar eða uppsetningarleiðbeiningar með hjálp sem aðstoða þig í gegnum skrefin. Ef þú lýkur ekki uppsetningunni í einni tilraun geturðu notað síðuna **Uppsetningar fyrir _nafn forrits_**, sem sýnir allar uppsetningar fyrir forritið. Nauðsynlegar stillingar eru auðkenndar með **feitletruðum stöfum**.

## <a name="upload-a-per-tenant-extension-pte"></a>Hlaða upp viðbót fyrir hvern leigjanda (PTE)

Þú hleður upp PTE með því að nota síðuna **Viðbótastjórnun**. Á síðunni **Viðbótastjórnun** skal fara í **Stjórna**, síðan velja **Hlaða upp viðbót**. Á síðunni **Hlaða og setja upp viðbót** skal tilgreina forritsskrána sem á að hlaða upp. Til að halda áfram skal velja hnappinn **Samþykkja** og síðan hnappinn **Nota** sem mun hefja innleiðingarferli PTE.

Ef PTE inniheldur skemabreytingar með þáttaskilum er mögulegt að *þvinga* upphleðslu þess. Til að gera það skal í **Samstilling skema** velja valkostinn **Þvinga**. Samþykkja þarf staðfestingarglugga sem birtist áður en haldið er áfram.  

## <a name="uninstall-an-app"></a>Fjarlægja forrit

Hægt er að fjarlægja forrit með því að nota síðuna **Viðbótastjórnun**. Til að fjarlægja forrit skaltu velja það á síðunni og velja svo aðgerðina **Fjarlægja**. Ef þú fjarlægir forrit og skiptir síðan um skoðun geturðu sett forritið upp aftur.

Þegar þú fjarlægir forrit sem þú hefur verið að nota eru gögn sjálfgefið geymd ef þú skyldir setja forritið upp aftur. Hægt er að velja að eyða gögnunum með forritinu. Þessari aðgerð er stjórnað með rofanum **Eyða gögnum viðbótar**. Það er sjálfgefið að **Slökkt** sé á þessum rofa. Þegar þú reynir að kveikja á rofanum **Eyða gögnum viðbótar** fyrir forritið færðu upp staðfestingarglugga og þú þarft að velja **Já** til að kveikja á honum. Þegar kveikt hefur verið á rofanum **Eyða gögnum viðbótar** geturðu fjarlægt forritið og þú verður beðin(n) um að staðfesta aftur að þú viljir fjarlægja forritið og eyða gögnunum.

> [!IMPORTANT]  
> - Það gætu verið önnur forrit sem krefjast þess eða eru háð forritinu sem þú vilt fjarlægja til þess að virka. Vísað er í þessi forrit sem *háð*. Ekki er hægt að fjarlægja forrit nema háðu forritin séu einnig fjarlægð.
> - Þegar þú velur að fjarlægja forrit sem er með eitt eða fleiri háð forrit færðu staðfestingarglugga sem sýnir háðu forritin og spyr hvort þú viljir fjarlægja forritið og öll háð forrit. Þú þarft að velja **Já** til að halda áfram.
> - Ef þú kveikir á rofanum **Eyða gögnum viðbótar** mun eyðing forritsins eyða öllum gögnum fyrir forritið **ásamt** gögnum fyrir öll háð forrit. Ekki er hægt að afturkalla þessa aðgerð.
> - Sum forrit eru nauðsynleg. Þú ert að koma í veg fyrir að þetta sé fjarlægt af síðunni **Viðbótastjórnun**. Ef þú prófar birtast villuboð.  

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