---
title: Framkvæma greiðslur með AMC banka (US) eða SEPA-kreditfærslu (ESB)
description: Meðhöndla greiðslur til lánardrottna með því að flytja út skrá (EFT) með greiðsluupplýsingum í færslubókarlínum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 07/17/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Framkvæma greiðslur með AMC-bankakerfinu 365 grundvallarviðbót eða SEPA-kreditfærslu

Á síðunni **Útgreiðslubækur** er hægt að vinna úr greiðslum til lánardrottna með því að flytja út skrá með greiðsluupplýsingum úr færslubókarlínunum. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning. [!INCLUDE[prod_short](includes/prod_short.md)] styður SEPA-kreditflutningssniðið en í þínu landi/svæði gætu önnur snið fyrir rafrænar greiðslur verið tiltæk.

> [!NOTE]
> Í almenn útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)], er altæk þjónustuveita til að umbreyta bankagögnum í annað skráarsnið sem bankinn krefst að er uppsett og tengt. Í norður-amerískum útgáfum má nota sömu þjónustu til að senda greiðsluskrár sem rafræna millifærslu (EFT), t.d. kerfi rafrænnar greiðslumiðlunar sem er oft notuð, en með örlítið öðruvísi leiðum. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Til að gera SEPA kredifærslur, verður þú fyrst að setja upp bankareikning, lánardrottin, og almenna bókarkeyrslurunu sem greiðslubók er byggt á. Þú undirbýrð síðan greiðslur til lánardrottna með því að fylla sjálfkrafa út **síðuna Greiðslubækur** með gjaldfóðrum greiðslum með tilteknum bókunardagsetningum.  

> [!NOTE]  
> Þegar þú hefur staðfest að greiðslurnar hafi verið framkvæmdar af bankanum getur þú bókað greiðslubókarlínurnar.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>Uppsetning AMC Banking 365 Fundamentals viðbótarinnar

Virkið AMC Banking 365 Fundamentals viðbótina til að umbreyta hvers kyns bankayfirlitsskrá í snið sem hægt er að flytja inn eða til að umbreyta útfluttum greiðsluskrám í það snið sem bankinn krefst. Frekari upplýsingar eru í [Nota AMC Banking 365 Fundamentals-viðbótina](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>Uppsetning SEPA-kreditfærslna

Á síðunni **Greiðslubækur** er hægt að flytja greiðslur út í skrá til upphleðslu í rafræna bankann þinn til vinnslu á tengdum peningaflutningum. [!INCLUDE[prod_short](includes/prod_short.md)] styður SEPA-kreditflutningssniðið en í þínu landi/svæði gætu önnur snið fyrir rafrænar greiðslur verið tiltæk.  

Til að virkja útflutning á bankaskrársniði sem ekki er studdur úr reitnum í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að setja upp skilgreiningu gagnaskipta með því að nota gagnaskiptarammann. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

Áður en þú getur afgreitt greiðslu rafrænt með því að flytja greiðsluskrár í SEPA-kreditfærslusnið, verður þú að framkvæma eftirfarandi uppsetningarskref:  

* Setja upp viðkomandi bankareikning til að meðhöndla SEPA-kreditfærslusnið.  
* Setja upp lánardrottinn spjöld með því að flytja skrár úr í SEPA-kreditmillifærslur sniði.  
* Setja upp tengda færslubókarkeyrslu til að virkja greiðsluútflutning af síðunni **Útgreiðslubækur**   
* Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.  

> [!NOTE]
> Business Central styður bæði SEPA snið CT verkja.001.001.03 og CT verkur.001.001.09. Hægt er að velja hvaða snið sem er á síðunni **Bankareikningsspjald** .  
> [!TIP]
> Þessi grein gildir um almenna útgáfu af [!INCLUDE [prod_short](includes/prod_short.md)]. Í þínu landi eða svæði, kann að vera búið að bæta við fleiri áskildum reitum á hinar ýmsu síður. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Að setja upp bankareikning fyrir SEPA-kreditfærslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.  
2. Opna skal spjald bankareikningsins þaðan sem þú munt flytja út greiðsluskrár á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Handhafi** reikninga í reitnum **Útflutningssnið** greiðslu er valið SEPA-sniðið sem á að nota.  
4. Í flipanum **Almennt** í **Númer fyrir skilaboð kreditfærslu** reitnum skal velja númeraröð sem tölum eru úthlutað úr til -SEPA-kreditfærslu.  
5. Gangið úr skugga um að reiturinn **IBAN** sé útfylltur.  

    > [!NOTE]  
    > Reiturinn **Gjaldmiðilskóði** verður að vera stilltur á **EUR**, því SEPA-kreditmillifærslur er aðeins hægt að gera í evrum.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Að setja upp lánardrottin fyrir SEPA-kreditfærslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.  
2. Opnið spjald lánardrottins sem á að greiða til rafrænt útflutningi greiðsluskráa á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Greiðslur** í reitnum **Greiðsluháttarkóti** er banki **valinn**.  
4. Í reitnum **Kjörbanki** skal velja bankann sem peningarnir verða fluttir í þegar rafræni bankinn vinnur hann.  

    Ef ekki hefur enn verið settur upp banki fyrir þennan lánardrottinn er hægt að gera það núna. Frekari upplýsingar eru í [Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). Gildið í reitnum **Valinn bankareikningur** er afritað í reitinn **Móttökubankareikningur** á síðunni **Greiðslubók**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Að stilla greiðslubók upp til að flytja greiðsluskrár

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.  
2. Í reitnum **Heiti keyrslu** er felli\-lista hnappurinn valinn.  
3. Á síðunni **Fh.færslubókakeyrslur** skal velja aðgerðina **Breyta lista**.  
4. Í línunni fyrir útgreiðslubókina sem á að nota til að flytja út greiðslur er gátreiturinn **Heimila greiðsluútflutning** valinn.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslumátar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Greiðslumáti** skaltu velja greiðslumáta sem er notað til að flytja út greiðslur frá, og þá velja **Greiðsluútflutningur Línuskilgreining** reitinn.  
3. Á síðunni **Greiðsluútflutningur Línuskilgreining** skal velja kóðann sem var tilgreindur í **Kóði** reitnum á **Línuskilgreiningar** flýtiflipanum í skrefi 4 í „Að lýsa sniði lína og dálka í skránni“ hlutanum í [Setja upp gagnaskiptaskilgreiningar](across-how-to-set-up-data-exchange-definitions.md) aðgerðinni.  

## <a name="preparing-the-payment-journal"></a>Greiðslubók undirbúin

Fyllið út greiðslubókina með línum fyrir greiðslu á gjalddaga til lánardrottna með möguleikanum á að setja inn bókunardagsetningar byggt á gjalddaga tengdra innkaupaskjala. Nánari upplýsingar er að finna í [Stjórna skuldum](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Greiðslur fluttar út í bankaskrá

Þegar notandi er tilbúinn að greiða lánardrottnum eða endurgreiðslur til starfsmanna er hægt að flytja út skrá með greiðsluupplýsingum í línunum á síðunni **Útgreiðslubækur** . Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning.

Í almennu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] er AMC Banking 365 Fundamentals viðbótin í boði. Í Norður-Ameríku útgáfum má nota sömu viðbót til að senda greiðslu skrám sem rafrænar millifærslu (EFT) en með ofurlítið annarri vinnslu. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Áður en hægt er að flytja út greiðsluskrár í greiðslubókina, verður að tiltaka rafrænt sniði bankareikningnum sem við á, og verður að virkja AMC Banking 365 Fundamentals viðbótina. Frekari upplýsingar er að finna í [Setja upp bankareikninga](bank-how-setup-bank-accounts.md) og [Nota AMC Banking 365 Fundamentals viðbótina](ui-extensions-amc-banking.md). Þar að auki þarf að velja **Leyfa útflutning greiðslu** gátreiturinn á síðunni **Almennar Færslubókakeyrslur**. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

Síðan **Skráningar kreditmillifærslna** er notuð til að skoða greiðsluskrár sem hafa verið fluttar út úr greiðslubókinni. Á þessari síðu er einnig hægt að endurflytja út greiðsluskrár ef um er að ræða tæknilegar villur eða breytingar á skrá. Þó skal athuga að útfluttar EFT-skrár eru ekki sýndar á þessari síðu og ekki er hægt að flytja þær út aftur.  

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
6. Á síðunni **Útgreiðslubækur** skal velja aðgerðina **Búa til EFT-skrá** .

    Á síðunni **Búa til EFT skrá** eru allar greiðslur uppsettar fyrir EFT, sem þú hefur flutt út úr greiðslubókinni fyrir tilgreinda bankareikninga en hefur enn ekki búið til, tilgreindar á **Línur** Flýtiflipanum.
7. Velja **Búa til EFT skrá** aðgerð til að flytja út eina skrá fyrir öll EFT greiðslur.
8. Á síðunni **Vista sem** skal tilgreina staðsetninguna þangað sem skráin er flutt út og velja svo **Vista**.

Bankagreiðsluskráin er flutt út á staðsetningu sem þú tilgreinir, og hægt er að meðhöndla hana til hlaða henni upp á rafrænn bankareikning og framkvæma greiðslurnar. Þá má bóka útflutta greiðslubókarlínur.

### <a name="to-plan-when-to-post-exported-payments"></a>Til að áætla hvenær á að bóka útfluttar greiðslur

Ef ekki á að bóka útgreiðslubókarlínu vegna útfluttra greiðslna, til dæmis vegna þess að beðið er eftir staðfestingu á því að bankinn hafi unnið færsluna er hægt að eyða færslubókarlínunni. Þegar þú síðar stofnar greiðslubókarlínu til að greiða eftirstandandi upphæð á reikningnum sýnir reiturinn **Heildarupphæð flutt út** hversu mikið af greiðsluupphæðinni hefur þegar verið flutt út. Þú getur einnig fundið ítarlegar upplýsingar um heildarupphæðir sem hafa verið fluttar út með því að velja hnappinn **Skráningarfærslur kreditmillifærslna** til að sjá upplýsingar um útfluttar greiðsluskrár.

Ef ferli er fylgt þar sem greiðslur eru ekki bókaðar fyrr en staðfest hefur verið að þær hafi verið unnar í bankanum er hægt að stjórna því á tvennan hátt.

* Í greiðslubók með greiðslulínum sem lagðar eru til er hægt að raða annaðhvort dálknum **Flytja út í greiðsluskrá** eða **Útflutt heildarupphæð** og eyða síðan greiðslutillögum fyrir opna reikninga sem greiðslur hafa þegar verið innt af hendi og ekki á að greiða fyrir.
* Á síðunni **Greiðslutillögur** til lánardr. þar sem tilgreint er hvaða greiðslur á að setja inn í útgreiðslubókina er hægt að velja **gátreitinn Sleppa útfluttum** greiðslum ef ekki á að setja inn færslubókarlínur fyrir greiðslur sem þegar hafa verið fluttar út.

Til að sjá upplýsingar um útfluttar greiðslur, veljið aðgerðina **Útflutningsferill greiðslna**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Að endurútflytja greiðslur í bankaskrá

Hægt er að endurútflytja greiðsluskrár af síðunni **Skráningar kreditmillifærslna**. Áður en greiðslubókarlínum er eytt eða bókað er einnig hægt að flytja greiðsluskrána út aftur á **síðunni Útgreiðslubækur** með því að flytja hana út aftur. Ef greiðslubókarlínum er eytt eða bókað eftir útflutninginn er hægt að flytja sömu greiðsluskrá út aftur af síðunni **Kreditfærsludagbækur** . Veldu línuna fyrir runu kreditfærslanna sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslur í bankaskrá**.

> [!NOTE]  
> Útfluttar EFT skrár ekki eru sýndar á síðunni **Kreditfærsluskrár** og ekki er hægt að flytja þær aftur út.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skráningar kreditfærslna** og velja síðan viðkomandi tengil.
2. Veldu greiðsluútflutning sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslu í skrá**.

## <a name="posting-the-payments"></a>Bókun greiðslna

Þegar rafræna greiðslan hefur verið unnin að fullu af bankanum skal bóka greiðslurnar. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).

## <a name="see-also"></a>Sjá einnig

[Nota AMC Banking 365 Fundamentals viðbótina](ui-extensions-amc-banking.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
