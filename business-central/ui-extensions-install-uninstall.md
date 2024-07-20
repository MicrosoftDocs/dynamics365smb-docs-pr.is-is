---
title: Setja upp og fjarlægja forrit
description: Kynntu þér hvernig þú getur sett upp og fjarlægt forrit og viðbætur í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: solsen
ms.topic: conceptual
ms.date: 06/26/2024
ms.custom: bap-template
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 2514, 20350'
ms.service: dynamics-365-business-central
---

# Setja upp og fjarlægja viðbætur (forrit) í Business Central

Þú getur breytt [!INCLUDE[prod_short](includes/prod_short.md)] með því að setja upp forrit sem bæta t.d. við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis. Frekari upplýsingar eru í [Sérstilling Business Central með viðbótum](ui-extensions.md).

> [!NOTE]
> Til að setja upp eða fjarlægja forrit úr AppSource eða bæta við forritum fyrir hvern leigjanda fyrir sig þarf að vera með réttar heimildir. Annaðhvort verður að vera meðlimur í D365 Extension MGT notendaflokkur eða þá að hann verður að vera með FRAMLENGINGuna. STJÓR. - STJÓRNANDA heimildasamstæða. Ef notandi er kerfisstjóri er hægt að úthluta notendaflokkum og heimildum til annarra notenda í fyrirtækinu. Til að [fá nánari upplýsingar um notendaflokka og heimildir er farið í Úthluta heimildum til notenda og hópa](ui-define-granular-permissions.md).
>
> Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.

Ef nota á viðbót verður að úthluta heimildarsamstæðunum sem því fylgja.

## <a name="install"></a>Setja upp viðbót

Þú stjórnar forritum og viðbótum á síðunni **Viðbótastjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Annars geturðu valið **Leita að síðu eða Tilkynna** táknið ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") í efra hægra horni skal færa inn **Nafnauka** og velja síðan viðeigandi tengja.  

Hægt er að fá ný forrit úr markaðstorginu á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Markaðstorgið býður upp á öll tiltæk forrit fyrir [!INCLUDE[prod_short](includes/prod_short.md)] auk forrita og efnispakka fyrir aðrar Microsoft-vörur. Stilltu viðeigandi síur, skoðaðu upplýsingar um hverja viðbót og fáðu viðbót fyrir þinn [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fara í AppSource úr [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **Viðbótastjórnunargrunnur** getur þú séð forritin sem eru uppsett og þú getur opnað **Microsoft AppSource síðuna Forrit** sem sýnir forritin [!INCLUDE[prod_short](includes/prod_short.md)] sem eru tiltæk í AppSource. Ef aðgerðin **Skoða AppSource** er valin er farið [AppSource í.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Frekari upplýsingar [eru í Manage AppSource apps](admin-manage-appsource-apps.md).  

Veldu forrit til að fræðast um hvað það gerir og þú getur opnað Hjálp fyrir forritið til að fá nánari upplýsingar. Þegar þú velur að fá forrit verður þú að samþykkja notkunarskilmála þess. Ef þú færð forritið af AppSource vefsíðunni verður þú skráð(ur) inn í [!INCLUDE[prod_short](includes/prod_short.md)] til að ljúka uppsetningunni.  

Þegar þú hefur sótt forrit gætir þú þurft að setja það upp. Sum forrit krefjast þess að þú veitir upplýsingar áður en þú getur notað þau. Eftir að þú til dæmis setjur upp forritið **PayPal Payments Standard** þarftu að tilgreina netfang eða reikningskenni söluaðila fyrir PayPal-reikninginn þinn. Til að setja upp forrit eða til að finna út hvaða upplýsingar vantar skaltu velja á síðunni **Uppsettar viðbætur** aðgerðina **Setja upp**.  

Önnur forrit bæta einfaldlega reitum við fyrirliggjandi síðu, eða þau bæta við nýjum síðum, til dæmis.

Ef þú fjarlægir forrit og skiptir um skoðun geturðu sett það inn aftur. Þegar þú fjarlægir forrit sem þú hefur verið að nota gögnin þín eyðist ekki. Gögnin eru tiltæk ef forritið er sett upp aftur.

Sum forrit eru í boði Microsoft og önnur forrit eru í boði [annarra fyrirtækja](ui-extensions-other.md). Mælt er með að þú lærir meira um forritið áður en þú velur að setja það upp.

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

## Setja upp forrit

Þegar þú hefur sótt forrit gætir þú þurft að setja það upp. Til dæmis þarftu að tilgreina PayPal-reikningin sem á að nota fyrir forritið **PayPal Payments Standard fyrir [!INCLUDE[prod_short](includes/prod_short.md)]**. Ef það er tilfellið, þegar uppsetning lýkur mun [!INCLUDE[prod_short](includes/prod_short.md)] spyrja hvort þú viljir setja forritið upp strax. Uppsetningar geta verið nauðsynlegar til að forritið virki eða valfrjálsar.

Ef þú velur að setja forritið upp strax og það er með nauðsynleg skref mun [!INCLUDE[prod_short](includes/prod_short.md)] opna nauðsynlegu skrefin. Uppsetningin getur verið annaðhvort síða þar sem þú slærð inn upplýsingar eða uppsetningarleiðbeiningar með hjálp sem aðstoða þig í gegnum skrefin. Ef þú lýkur ekki uppsetningunni í einni tilraun geturðu notað síðuna **Uppsetningar fyrir _nafn forrits_**, sem sýnir allar uppsetningar fyrir forritið. Nauðsynlegar stillingar eru auðkenndar með **feitletruðum stöfum**.

## Hlaða upp viðbót fyrir hvern leigjanda (PTE)

Þú hleður upp PTE með því að nota síðuna **Viðbótastjórnun**. Á síðunni **Viðbótastjórnun** skal fara í **Stjórna**, síðan velja **Hlaða upp viðbót**. Á síðunni **Hlaða og setja upp viðbót** skal tilgreina forritsskrána sem á að hlaða upp. Til að halda áfram skal velja hnappinn **Samþykkja** og síðan hnappinn **Nota** sem mun hefja innleiðingarferli PTE.

Ef PTE inniheldur skemabreytingar með þáttaskilum er mögulegt að *þvinga* upphleðslu þess. Til að gera það skal velja valkostinn Samstilla afköst **í** samstillingu **skema**. Samþykkja þarf staðfestingarglugga sem birtist áður en haldið er áfram.  

## Fjarlægja forrit

Hægt er að fjarlægja forrit með því að nota síðuna **Viðbótastjórnun**. Til að fjarlægja forrit skaltu velja það á síðunni og velja svo aðgerðina **Fjarlægja**. Ef þú fjarlægir forrit og skiptir síðan um skoðun geturðu sett forritið upp aftur.

Sjálfgefið er að þegar forrit sem þú hefur verið að nota gögnin þín er sjálfgefið eytt. Ef þú ert viss um að þú setjir forritið ekki upp aftur og eytt gögnunum þegar þú fjarlægir það. Til að eyða gögnum þegar forrit er fjarlægt skal kveikja á víxlinu **Eyða viðbótagögnum** . Þú munt fá staðfestingarsvarglugga og þú verður að velja **Já** til að kveikja á honum. Þegar kveikt hefur verið á rofanum **Eyða gögnum viðbótar** geturðu fjarlægt forritið og þú verður beðin(n) um að staðfesta aftur að þú viljir fjarlægja forritið og eyða gögnunum.

> [!IMPORTANT]  
> * Það gætu verið forrit sem krefjast þess eða ráðast af því forriti sem þú vilt fjarlægja. Þessi forrit eru nefnd háð *forritum*. Ekki er hægt að fjarlægja forrit nema það sé ekki fjarlægt. Þegar forrit sem er ósjálfstætt er fjarlægt birtir svargluggi yfir það sem er háð. Til að halda áfram verður þú að velja **Já** til að fjarlægja forritið og það er háð því.
> * Ef kveikt er á **víxluninni Eyða viðbótagögnum** eyðir það öllum gögnum forritsins *að viðbættum* gögnum fyrir öll ósjálfstæð forrit. Ekki er hægt að afturkalla aðgerðina.
> * Sum forrit eru nauðsynleg og ekki er hægt að eyða þeim á síðunni **Viðbótastjórnun** .  

Ef þú vilt halda gögnum fyrir forrit sem hefur verið fjarlægt getur þú eytt gögnunum síðar. Síðan **Eyða munaðarlausu viðbótagögnunum** birtir forritin sem þú ert enn með gögn fyrir. Til að eyða gögnunum skal velja forritið og velja **svo Eyða gögnum**. 

## Sjá einnig

[Sérstilla Business Central](ui-customizing-overview.md)  
[Microsoft Business Central viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Stjórna AppSource forritum](admin-manage-appsource-apps.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[Virkja greiðslur viðskiptamanna gegnum PayPal](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Setja upp GetAddress.io UK Postal Code viðbótina](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
