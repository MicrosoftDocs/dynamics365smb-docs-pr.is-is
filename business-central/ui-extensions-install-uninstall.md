---
title: Setja upp og fjarlægja forrit
description: Kynntu þér hvernig þú getur sett upp og fjarlægt forrit og viðbætur í Business Central.
author: SusanneWindfeldPedersen
ms.author: solsen
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 20350'
---

# <a name="install-and-uninstall-extensions-apps-in-business-central"></a>Setja upp og fjarlægja viðbætur (forrit) í Business Central

Þú getur breytt [!INCLUDE[prod_short](includes/prod_short.md)] með því að setja upp forrit sem bæta t.d. við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis. Frekari upplýsingar eru í [Sérstilling Business Central með viðbótum](ui-extensions.md).

> [!NOTE]
> Til að setja upp eða fjarlægja forrit úr AppSource eða bæta við forritum fyrir hvern leigjanda fyrir sig þarf að vera með réttar heimildir. Annaðhvort verður þú að vera meðlimur í D365 Extension notendahópnum eða þú verður að hafa FRAMLENGINU. STJÓR. - STJÓRNANDA heimildasamstæða. Ef notandi er kerfisstjóri er hægt að úthluta notendaflokkum og heimildum á aðra notendur í fyrirtækinu. Til að fræðast meira um notendaflokka og heimildir er farið í að  [úthluta heimildum til notenda og hópa](ui-define-granular-permissions.md).
>
> Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.

Til að nota nafnauka þarf að vera úthlutað þeim heimildarstæðum sem fylgja henni.

## <a name="install-an-extension"></a><a name="install"></a>Setja upp viðbót

Þú stjórnar forritum og viðbótum á síðunni **Viðbótastjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Annars geturðu valið **Leita að síðu eða Tilkynna** táknið ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") í efst í hægra horninu skal slá inn  **framlengingu** og velja síðan tengdan tengil.  

Hægt er að fá ný forrit úr markaðstorginu á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Markaðstorgið býður upp á öll tiltæk forrit fyrir [!INCLUDE[prod_short](includes/prod_short.md)] auk forrita og efnispakka fyrir aðrar Microsoft-vörur. Stilltu viðeigandi síur, skoðaðu upplýsingar um hverja viðbót og fáðu viðbót fyrir þinn [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fara í AppSource úr [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **framlengingarstjórnun** geturðu séð forritin sem eru í uppsettri röð og þú getur opnað **Framlengingarmarkað** síðu sem sýnir [!INCLUDE[prod_short](includes/prod_short.md)] forritin sem eru í boði í AppSource. Ef valið er *Fleiri forrit* tengilinn, er farið með þig á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Veldu app til að fræðast um hvað það gerir, og þú getur nálgast app til að fá frekari upplýsingar. Þegar valið er að fá App þarf að samþykkja notkunarskilmála þess. Ef þú færð forritið af AppSource vefsíðunni verður þú skráð(ur) inn í [!INCLUDE[prod_short](includes/prod_short.md)] til að ljúka uppsetningunni.  

Þegar þú hefur sótt forrit gætir þú þurft að setja það upp. Sum forrit krefjast þess að þú veitir upplýsingar áður en þú getur notað þau. Eftir að þú til dæmis setjur upp forritið **PayPal Payments Standard** þarftu að tilgreina netfang eða reikningskenni söluaðila fyrir PayPal-reikninginn þinn. Til að setja upp forrit eða til að finna út hvaða upplýsingar vantar skaltu velja á síðunni **Uppsettar viðbætur** aðgerðina **Setja upp**.  

Önnur forrit bæta einfaldlega reitum við fyrirliggjandi síðu, eða þau bæta við nýjum síðum, til dæmis.

Ef þú fjarlægir forrit og skiptir um skoðun geturðu sett það inn aftur. Þegar þú fjarlægir App sem þú hefur verið að nota er ekki eytt. Gögnin eru tiltæk ef þú setur upp forritið aftur.

Sum forrit eru í boði Microsoft og önnur forrit eru í boði [annarra fyrirtækja](ui-extensions-other.md). Við mælum með að þú lærir meira um App áður en þú kýst að setja það upp.

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

## <a name="set-up-an-app"></a>Setja upp App

Þegar þú hefur sótt forrit gætir þú þurft að setja það upp. Til dæmis þarftu að tilgreina PayPal-reikningin sem á að nota fyrir forritið **PayPal Payments Standard fyrir [!INCLUDE[prod_short](includes/prod_short.md)]**. Ef það er tilfellið, þegar uppsetning lýkur mun [!INCLUDE[prod_short](includes/prod_short.md)] spyrja hvort þú viljir setja forritið upp strax. Uppsetningar geta verið nauðsynlegar til að forritið virki eða valfrjálsar.

Ef þú velur að setja forritið upp strax og það er með nauðsynleg skref mun [!INCLUDE[prod_short](includes/prod_short.md)] opna nauðsynlegu skrefin. Uppsetningin getur verið annaðhvort síða þar sem þú slærð inn upplýsingar eða uppsetningarleiðbeiningar með hjálp sem aðstoða þig í gegnum skrefin. Ef þú lýkur ekki uppsetningunni í einni tilraun geturðu notað síðuna **Uppsetningar fyrir _nafn forrits_**, sem sýnir allar uppsetningar fyrir forritið. Nauðsynlegar stillingar eru auðkenndar með **feitletruðum stöfum**.

## <a name="upload-a-per-tenant-extension-pte"></a>Hlaða upp viðbót fyrir hvern leigjanda (PTE)

Þú hleður upp PTE með því að nota síðuna **Viðbótastjórnun**. Á síðunni **Viðbótastjórnun** skal fara í **Stjórna**, síðan velja **Hlaða upp viðbót**. Á síðunni **Hlaða og setja upp viðbót** skal tilgreina forritsskrána sem á að hlaða upp. Til að halda áfram skal velja hnappinn **Samþykkja** og síðan hnappinn **Nota** sem mun hefja innleiðingarferli PTE.

Ef PTE inniheldur skemabreytingar með þáttaskilum er mögulegt að *þvinga* upphleðslu þess. Til að gera það, í  **Samstillingarham**  skema Veldu  **afl**  valkostinn. Samþykkja þarf staðfestingarglugga sem birtist áður en haldið er áfram.  

## <a name="uninstall-an-app"></a>Fjarlægja forrit

Hægt er að fjarlægja forrit með því að nota síðuna **Viðbótastjórnun**. Til að fjarlægja forrit skaltu velja það á síðunni og velja svo aðgerðina **Fjarlægja**. Ef þú fjarlægir forrit og skiptir síðan um skoðun geturðu sett forritið upp aftur.

Sjálfgefið er að þegar App hefur verið tekið í notkun sé ekki eytt. Ef þú ert viss um að þú munt ekki setja forritið upp aftur og þú getur eytt gögnunum þegar það er fjarlægt. Til að eyða gögnum þegar App er fjarlægt skal kveikja á  **gagnaskipta**  eyðu fyrir endingu. Þú munt fá staðfestingarglugga og þú verður að velja  **Já**  til að kveikja á honum. Þegar kveikt hefur verið á rofanum **Eyða gögnum viðbótar** geturðu fjarlægt forritið og þú verður beðin(n) um að staðfesta aftur að þú viljir fjarlægja forritið og eyða gögnunum.

> [!IMPORTANT]  
> * Það gætu verið forrit sem krefjast eða ráðast á App sem á að fjarlægja. Þessi forrit eru nefnd sem  *háði*. Ekki er hægt að fjarlægja App nema hægt sé að fjarlægja það einnig. Þegar þú fjarlægir App sem er háður háði, birtir svargluggi lista háðs. Til að halda áfram þarftu að velja  **Já**  til að fjarlægja App og háða það.
> * Ef kveikt er á skiptiframað  **gagnaskipta**  skal fjarlægja forritið til að eyða öllum gögnum fyrir App  *plús*  gögn fyrir öll forrit sem eru háð. Ekki er hægt að afturkalla aðgerðina.
> * Sum forrit eru nauðsynleg og ekki er hægt að eyða þeim á  **síðu Framlengingarstjórnunar** .  

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
