---
title: Greiða með AMC Banking (US) eða SEPA-kreditfærslu (ESB)
description: Meðhöndla greiðslur til lánardrottna með því að flytja út skrá (EFT) með greiðsluupplýsingum í færslubókarlínum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 256, 1205, 1206, 1209, 10810, 10811
ms.date: 07/06/2021
ms.author: bholtorf
ms.openlocfilehash: be2f6e3efdfd34d59c55a3addeefb5646454b3bb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516266"
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Greiða með AMC Banking 365 Fundamentals viðbótinni eða SEPA-kreditfærslu

Á síðunni **Greiðslubók** er hægt að meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning. [!INCLUDE[prod_short](includes/prod_short.md)] styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.

> [!NOTE]
> Í almenn útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)], er altæk þjónustuveita til að umbreyta bankagögnum í annað skráarsnið sem bankinn krefst að er uppsett og tengt. Í norður-amerískum útgáfum má nota sömu þjónustu til að senda greiðsluskrár sem rafræna millifærslu (EFT), t.d. kerfi rafrænnar greiðslumiðlunar sem er oft notuð, en með örlítið öðruvísi leiðum. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Til að gera SEPA kredifærslur, verður þú fyrst að setja upp bankareikning, lánardrottin, og almenna bókarkeyrslurunu sem greiðslubók er byggt á. Greiðslur til lánardrottna eru því næst undirbúnar með því að fylla sjálfkrafa út síðuna **Greiðslubók** með gjaldföllnum greiðslum með tilgreindum bókunardagsetningum.  

> [!NOTE]  
> Þegar þú hefur staðfest að greiðslurnar hafi verið framkvæmdar af bankanum getur þú bókað greiðslubókarlínurnar.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>Uppsetning AMC Banking 365 Fundamentals viðbótarinnar

Virkið AMC Banking 365 Fundamentals viðbótina til að umbreyta hvers kyns bankayfirlitsskrá í snið sem hægt er að flytja inn eða til að umbreyta útfluttum greiðsluskrám í það snið sem bankinn krefst. Frekari upplýsingar [fást með því að AMC Banking 365 Fundamentals nota viðaukann](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>Uppsetning SEPA-kreditfærslna

Af síðunni **Greiðslubók** er hægt að flytja út greiðslur í skrá til upphals í netbanka til vinnslu á tengdum peningamillifærslum. [!INCLUDE[prod_short](includes/prod_short.md)] styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.  

Til að opna fyrir útflutning af skráasniði bankaskrár sem ekki eru studdar af [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að setja upp gagnaskiptaskilgreiningu með því að nota gagnaskiptaumgjörð. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

Áður en þú getur afgreitt greiðslu rafrænt með því að flytja greiðsluskrár í SEPA-kreditfærslusnið, verður þú að framkvæma eftirfarandi uppsetningarskref:  

* Setja upp viðkomandi bankareikning til að meðhöndla SEPA-kreditfærslusnið.  
* Setja upp lánardrottinn spjöld með því að flytja skrár úr í SEPA-kreditmillifærslur sniði.  
* Setja upp viðeigandi bókarkeyrslu til að gera virkan útflutning greiðslu af **Greiðslubók** síðunni  
* Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.  

> [!TIP]
> Þessi grein gildir um almenna útgáfu af [!INCLUDE [prod_short](includes/prod_short.md)]. Í þínu landi eða svæði, kann að vera búið að bæta við fleiri áskildum reitum á hinar ýmsu síður. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Að setja upp bankareikning fyrir SEPA-kreditfærslu

1. Í reitinn **Leita** skal færa inn **Bankareikningar** og velja síðan viðkomandi tengi.  
2. Opnið spjald bankareikningsins sem á að flytja greiðsluskrár úr á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Millifærsla**, í reitnum **Útflutningssvið greiðslu** skal velja **SEPACT**.  
4. Í flipanum **Almennt** í **Númer fyrir skilaboð kreditfærslu** reitnum skal velja númeraröð sem tölum eru úthlutað úr til -SEPA-kreditfærslu.  
5. Gangið úr skugga um að reiturinn **IBAN** sé útfylltur.  

    > [!NOTE]  
    > Reiturinn **Gjaldmiðilskóði** verður að vera stilltur á **EUR**, því SEPA-kreditmillifærslur er aðeins hægt að gera í evrum.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Að setja upp lánardrottin fyrir SEPA-kreditfærslu

1. Í reitnum **Leita** skal færa inn **Lánardrottnar** og velja síðan viðkomandi tengi.  
2. Opnið spjald lánardrottins sem á að greiða til rafrænt útflutningi greiðsluskráa á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Greiðsla**, í reitnum **Kóði greiðslumáta** skal velja **BANKI**.  
4. Í **Valinn bankareikningur** reitnum, veldu banka sem fé verður flutt inn á þegar það er unnið með rafrænum bankann þinn.  

    Ef ekki hefur enn verið settur upp banki fyrir þennan lánardrottinn er hægt að gera það núna. Frekari upplýsingar eru í [Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). Gildið í reitnum **Valinn bankareikningur** er afritað í reitinn **Móttökubankareikningur** á síðunni **Greiðslubók**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Að stilla greiðslubók upp til að flytja greiðsluskrár

1. Í reitnum **Leit** skal færa inn **Greiðslubækur** og velja síðan viðkomandi tengil.  
2. Í reitnum **Heiti keyrslu** er felli\-lista hnappurinn valinn.  
3. Á síðunni **Fh.færslubókakeyrslur** skal velja aðgerðina **Breyta lista**.  
4. Á línunni fyrir greiðslubókina sem notuð verður til að flytja út greiðslur skal velja gátreitinn **Leyfa greiðsluútflutning**.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.

1. Í reitnum **Leit** skal færa inn **Greiðsluhættir** og velja síðan viðkomandi tengil.  
2. Á síðunni **Greiðslumáti** skaltu velja greiðslumáta sem er notað til að flytja út greiðslur frá, og þá velja **Greiðsluútflutningur Línuskilgreining** reitinn.  
3. Á síðunni **Greiðsluútflutningur Línuskilgreining** skal velja kóðann sem var tilgreindur í **Kóði** reitnum á **Línuskilgreiningar** flýtiflipanum í skrefi 4 í „Að lýsa sniði lína og dálka í skránni“ hlutanum í [Setja upp gagnaskiptaskilgreiningar](across-how-to-set-up-data-exchange-definitions.md) aðgerðinni.  

## <a name="preparing-the-payment-journal"></a>Greiðslubók undirbúin

Fyllið út greiðslubókina með línum fyrir greiðslu á gjalddaga til lánardrottna með möguleikanum á að setja inn bókunardagsetningar byggt á gjalddaga tengdra innkaupaskjala. Nánari upplýsingar er að finna í [Stjórna skuldum](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Greiðslur fluttar út í bankaskrá

Þegar þú ert tilbúinn að inna af hendir greiðslur til lánardrottna, eða endurgreiðslur til starfsmanna, er hægt að flytja út skrá með greiðsluupplýsingum á línurnar á síðunni **Greiðslubók**. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning.

Í almennu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] er AMC Banking 365 Fundamentals viðbótin í boði. Í Norður-Ameríku útgáfum má nota sömu viðbót til að senda greiðslu skrám sem rafrænar millifærslu (EFT) en með ofurlítið annarri vinnslu. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Áður en hægt er að flytja út greiðsluskrár í greiðslubókina, verður að tiltaka rafrænt sniði bankareikningnum sem við á, og verður að virkja AMC Banking 365 Fundamentals viðbótina. Frekari upplýsingar er að finna [í](bank-how-setup-bank-accounts.md) Setja upp bankareikninga [og AMC Banking 365 Fundamentals nota viðaukann](ui-extensions-amc-banking.md). Þar að auki þarf að velja **Leyfa útflutning greiðslu** gátreiturinn á síðunni **Almennar Færslubókakeyrslur**. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

Síðan **Skráningar kreditmillifærslna** er notuð til að skoða greiðsluskrár sem hafa verið fluttar út úr greiðslubókinni. Á þessari síðu er einnig hægt að endurflytja út greiðsluskrár ef um er að ræða tæknilegar villur eða breytingar á skrá. Þó er bent á að ekki eru sýndir á þessari síðu útfluttar EFT skrár og þær geta ekki verið fluttar út aftur.  

### <a name="to-export-payments-to-a-bank-file"></a>Til að flytja út greiðslur í bankaskrá

Eftirfarandi dæmi sýnir hvernig á að greiða lánardrottni með ávísun. Skrefin eru svipuð og endurgreiðsla til viðskiptamanns með ávísun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.
2. Fyllið út greiðslubókarlínurnar. Nánari upplýsingar eru í [Skrá greiðslur og endurgreiðslur](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Ef EFT eru notaðar þarf að velja annaðhvort **Rafrænar Greiðslu** eða **Rafrænar Greiðslu – IAT** í reitnum **Tegund Bankagreiðslu** reit. Mismunandi útflutningsþjónusta skráa og snið þeirra þurfa mismunandi uppsetningargildi á síðunum **Bankareikningsspjald** og **Bankareikn.spjald lánardr.**. Þú færð að vita um uppsetningargildi sem eru röng eða sem vantar þegar þú reynir að flytja út skrána.
    >
    > Aðeins hægt að nota EFT-eiginleikann fyrir bankareikninga í innlendum gjaldmiðli. Ekki er hægt að nota hann með erlendum gjaldmiðli, sem gefinn er til kynna með gildinu á svæðinu **Gjaldmiðilskóði**. (Auður reitur þýðir innlendur gjaldmiðill.)

3. Þegar öllum greiðslubókarlínunum er lokið skal velja aðgerðina **Flytja út**.
4. Á síðunni **Flytja út rafrænar greiðslur** þarf að fylla reitina út eftir þörfum.

    Öll villuboð birtast í **Villur í greiðsluskrá** upplýsingareitnum þar sem þú getur einnig valið villuboð til að sjá ítarlegar upplýsingar. Leysa þarf úr öllum villum áður en hægt er að flytja út greiðsluskrána.

    > [!TIP]  
    > Þegar þú notar AMC Banking 365 Fundamentals viðbótina er algeng villa sú að bankareikningsnúmerið sé ekki með lengdina sem bankinn fer fram á. Til að forðast villuna eða leysa úr henni þarf að fjarlægja gildið á **IBAN** reitnum **Bankareikningsspjald** síðunni og svo, í **Nr. Bankareiknings** reitnum, slá inn bankareikningsnúmer á því sniði sem bankinn fer fram á.

5. Á síðunni **Vista sem** skal tilgreina staðsetninguna þangað sem skráin er flutt út og velja svo **Vista**.

    > [!NOTE]  
    > Ef þú ertu að nota EFT, vistaðu þá tilbúna lánardrottinn greiðslu formið sem word-skjal eða láta það sent beint til lánardrottins með tölvupósti. Greiðslur eru nú bætt á **Búa til EFT skrá** síðuna þar sem hægt að setja saman fjölgreiðslupantanir til að spara miðlaunarkostnaður. Nánari upplýsingar, sjá eftirfarandi skref.
6. Á síðunni **Greiðslubók** er aðgerðin **Búa til EFT skrá** valin.

    Á síðunni **Búa til EFT skrá** eru allar greiðslur uppsettar fyrir EFT, sem þú hefur flutt út úr greiðslubókinni fyrir tilgreinda bankareikninga en hefur enn ekki búið til, tilgreindar á **Línur** Flýtiflipanum.
7. Velja **Búa til EFT skrá** aðgerð til að flytja út eina skrá fyrir öll EFT greiðslur.
8. Á síðunni **Vista sem** skal tilgreina staðsetninguna þangað sem skráin er flutt út og velja svo **Vista**.

Bankagreiðsluskráin er flutt út á staðsetningu sem þú tilgreinir, og hægt er að meðhöndla hana til hlaða henni upp á rafrænn bankareikning og framkvæma greiðslurnar. Þá má bóka útflutta greiðslubókarlínur.

### <a name="to-plan-when-to-post-exported-payments"></a>Til að áætla hvenær á að bóka útfluttar greiðslur

Ef þú vilt ekki bóka greiðslubókarlínu fyrir útflutta greiðslu, t.d. vegna þess að þú ert að bíða eftir staðfestingu á því að færslan hafi verið meðhöndluð af bankanum geturðu einfaldlega eytt línunni. Þegar þú síðar stofnar greiðslubókarlínu til að greiða eftirstandandi upphæð á reikningnum sýnir reiturinn **Heildarupphæð flutt út** hversu mikið af greiðsluupphæðinni hefur þegar verið flutt út. Þú getur einnig fundið ítarlegar upplýsingar um heildarupphæðir sem hafa verið fluttar út með því að velja hnappinn **Skráningarfærslur kreditmillifærslna** til að sjá upplýsingar um útfluttar greiðsluskrár.

Ef fylgt er ferli þar sem ekki á að bóka greiðslur fyrr en staðfesting hefur fengist á því að þær hafa verið unnar í bankanum er hægt að stjórna því á tvo vegu.

* Í greiðslubók með tillögum að greiðslulínum geturðu flokkað með annað hvort dálkinum **Flutt út í greiðsluskrá** eða **Heildarupphæð flutt út** og svo eytt greiðslutillögum fyrir opna reikninga þar sem greiðslur hafa þegar átt sér stað og þú vilt ekki greiða.
* Á síðunni **Greiðslutillögur til lánardrottna** þar sem þú tilgreinir hvaða greiðslur eigi að setja í greiðslubókina, geturðu valið gátreitinn **Sleppa útfluttum greiðslum** ef þú vilt ekki setja inn færslubókarlínur fyrir greiðslur sem hafa þegar verið fluttar út.

Til að sjá upplýsingar um útfluttar greiðslur, veljið aðgerðina **Útflutningsferill greiðslna**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Að endurútflytja greiðslur í bankaskrá

Hægt er að endurútflytja greiðsluskrár af síðunni **Skráningar kreditmillifærslna**. Áður en greiðslubókarlínum er eytt eða þær bókaðar er einnig hægt að endurútflytja greiðsluskrána af síðunni **Greiðslubók** með því að flytja hana einfaldlega út aftur. Ef þú hefur eytt eða bókað greiðslubókarlínurnar eftir að þú hefur flutt þær út getur þú endurútflutt sömu greiðsluskrá af síðunni **Skráningar kreditmillifærslna**. Veldu línuna fyrir runu kreditfærslanna sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslur í bankaskrá**.

> [!NOTE]  
> Útfluttar EFT skrár ekki eru sýndar á síðunni **Kreditfærsluskrár** og ekki er hægt að flytja þær aftur út.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skráningar kreditfærslna** og velja síðan viðkomandi tengil.
2. Veldu greiðsluútflutning sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslu í skrá**.

## <a name="posting-the-payments"></a>Bókun greiðslna

Þegar rafræna greiðslan hefur verið unnin að fullu af bankanum skal bóka greiðslurnar. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).

## <a name="see-also"></a>Sjá einnig

[AMC Banking 365 Fundamentals Nota viðaukann](ui-extensions-amc-banking.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Vinna við Almennar færslubækur](ui-work-general-journals.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]