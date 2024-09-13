---
title: Framkvæma greiðslur með AMC banka (US) eða SEPA-kreditfærslu (ESB)
description: Meðhöndla greiðslur til lánardrottna með því að flytja út skrá (EFT) með greiðsluupplýsingum í færslubókarlínum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 08/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Framkvæma greiðslur með AMC-bankakerfinu 365 grundvallarviðbót eða SEPA-kreditfærslu

Á síðunni **Útgreiðslubækur** er hægt að vinna úr greiðslum til lánardrottna með því að flytja út skrá með greiðsluupplýsingum úr færslubókarlínunum. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning. [!INCLUDE[prod_short](includes/prod_short.md)] styður SEPA-kreditflutningssniðið en í þínu landi/svæði gætu önnur snið fyrir rafrænar greiðslur verið tiltæk.

> [!NOTE]
> Í almenn útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)], er altæk þjónustuveita til að umbreyta bankagögnum í annað skráarsnið sem bankinn krefst að er uppsett og tengt. Í norður-amerískum útgáfum má nota sömu þjónustu til að senda greiðsluskrár sem rafræna millifærslu (EFT), t.d. kerfi rafrænnar greiðslumiðlunar sem er oft notuð, en með örlítið öðruvísi leiðum. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Til að gera SEPA kredifærslur, verður þú fyrst að setja upp bankareikning, lánardrottin, og almenna bókarkeyrslurunu sem greiðslubók er byggt á. Þú undirbýrð síðan greiðslur til lánardrottna með því að fylla sjálfkrafa út **síðuna Greiðslubækur** með gjaldfóðrum greiðslum með tilteknum bókunardagsetningum.  

Þegar gengið hefur verið úr skugga um að bankinn hafi unnið úr greiðslunum er hægt að bóka útgreiðslubókarlínurnar.  

## Uppsetning viðbótarinnar AMC Banking 365 Fundamentals 

Virkja viðaukann AMC Banking 365 Fundamentals til að:

* Breyta bankayfirlitsskrám í snið sem hægt er að flytja inn.
* Umbreyta útfluttum greiðsluskrám í það snið sem bankinn krefst.

Frekari upplýsingar eru í [Nota AMC Banking 365 Fundamentals-viðbótina](ui-extensions-amc-banking.md).

## Uppsetning SEPA-kreditfærslu

Á síðunni **Greiðslubækur** er hægt að flytja greiðslur út í skrá til upphleðslu í rafræna bankann þinn til vinnslu á tengdum peningaflutningum. [!INCLUDE[prod_short](includes/prod_short.md)] styður SEPA-kreditflutningssniðið en í þínu landi/svæði gætu önnur snið fyrir rafrænar greiðslur verið tiltæk.  

Hægt er að flytja út bankaskrársnið sem ekki er studd úr reitnum í [!INCLUDE[prod_short](includes/prod_short.md)] með því að setja upp skilgreiningu gagnaskipta. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

Áður en þú getur afgreitt greiðslu rafrænt með því að flytja greiðsluskrár í SEPA-kreditfærslusnið, verður þú að framkvæma eftirfarandi uppsetningarskref:  

* Setja upp viðkomandi bankareikning til að meðhöndla SEPA-kreditfærslusnið.  
* Setja upp lánardrottinn spjöld með því að flytja skrár úr í SEPA-kreditmillifærslur sniði.  
* Setja upp tengda færslubókarkeyrslu til að virkja greiðsluútflutning af síðunni **Útgreiðslubækur**   
* Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.  

> [!NOTE]
> Business Central styður bæði SEPA snið CT verkja.001.001.03 og CT verkur.001.001.09. Hægt er að velja hvaða snið sem er á síðunni **Bankareikningsspjald** .  

> [!TIP]
> Þessi grein gildir um almenna útgáfu af [!INCLUDE [prod_short](includes/prod_short.md)]. Í þínu landi eða svæði, kann að vera búið að bæta við fleiri áskildum reitum á hinar ýmsu síður. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### Að setja upp bankareikning fyrir SEPA-kreditfærslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.  
2. Velja skal bankareikninginn þaðan sem greiðsluskrár eru fluttar út á SEPA-kreditfærslusniði.
3. Í flipanum **Almennt** í **Númer fyrir skilaboð kreditfærslu** reitnum skal velja númeraröð sem tölum eru úthlutað úr til -SEPA-kreditfærslu.
4. Á flýtiflipanum **Samskipti** skal færa inn aðsetur og tengiliðaupplýsingar fyrir bankann. 

   > [!NOTE]
   > Fylla verður út reitinn **Lands-/svæðiskóti** . Ef reiturinn er auður er ekki hægt að flytja út greiðslur fyrir reikninginn. Einnig þarf landið/svæðið að hafa gildan ISO-kóta.

5. Á flýtiflipanum **Bókun** í reitnum **Gjaldmiðilskóti** er tilgreindur gjaldmiðill bankareikningsins.  

   > [!NOTE]  
   > Reiturinn **Gjaldmiðilskóði** verður að vera stilltur á **EUR**, því SEPA-kreditmillifærslur er aðeins hægt að gera í evrum.  

6. Á flýtiflipanum **Millifærsla** í reitnum **Útflutningssnið** greiðslu er valið SEPA-sniðið sem á að nota.  
7. Í reitnum **IBAN** skal tilgreina alþjóðlegt bankareikningsnúmer fyrir reikninginn.  

### Að setja upp lánardrottin fyrir SEPA-kreditfærslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.  
2. Opna skal spjald lánardrottins sem greitt er rafrænt með því að flytja út greiðsluskrár á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Greiðslur** í reitnum **Greiðsluháttarkóti** er banki **valinn**.  
4. Í reitnum **Kjörbanki** skal velja bankann sem peningarnir millifærast í þegar unnið er úr þeim í rafræna bankanum.  

    Ef þú ert ekki með banka lyklasafn upp fyrir þennan lánardrottinn getur þú gert það núna. Frekari upplýsingar eru í [Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). Gildið í reitnum **Valinn bankareikningur** er afritað í reitinn **Móttökubankareikningur** á síðunni **Greiðslubók**.  

### Að stilla greiðslubók upp til að flytja greiðsluskrár

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.  
2. Í reitnum **Heiti keyrslu** er felli\-lista hnappurinn valinn.  
3. Á síðunni **Fh.færslubókakeyrslur** skal velja aðgerðina **Breyta lista**.  
4. Í línunni fyrir útgreiðslubókina sem er notuð til að flytja út greiðslur er gátreiturinn **Heimila greiðsluútflutning** valinn.  

### Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslumátar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Greiðslumáti** skaltu velja greiðslumáta sem er notað til að flytja út greiðslur frá, og þá velja **Greiðsluútflutningur Línuskilgreining** reitinn.  
3. Á síðunni **Greiðsluútflutningur Línuskilgreining** skal velja kóðann sem var tilgreindur í **Kóði** reitnum á **Línuskilgreiningar** flýtiflipanum í skrefi 4 í „Að lýsa sniði lína og dálka í skránni“ hlutanum í [Setja upp gagnaskiptaskilgreiningar](across-how-to-set-up-data-exchange-definitions.md) aðgerðinni.  

## Greiðslubók undirbúin

Fyllið út greiðslubókina með línum fyrir greiðslu á gjalddaga til lánardrottna með möguleikanum á að setja inn bókunardagsetningar byggt á gjalddaga tengdra innkaupaskjala. Nánari upplýsingar er að finna í [Stjórna skuldum](payables-manage-payables.md).

## Útflutningur greiðslna í bankaskrá

Þegar notandi er tilbúinn að greiða lánardrottnum eða endurgreiðslur til starfsmanna er hægt að flytja út skrá með greiðsluupplýsingum í línunum á síðunni **Útgreiðslubækur** . Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning.

Í almennu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] er AMC Banking 365 Fundamentals viðbótin í boði. Í Norður-Ameríku útgáfum má nota sömu viðbót til að senda greiðslu skrám sem rafrænar millifærslu (EFT) en með ofurlítið annarri vinnslu. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Áður en hægt er að flytja út greiðsluskrár í greiðslubókina, verður að tiltaka rafrænt sniði bankareikningnum sem við á, og verður að virkja AMC Banking 365 Fundamentals viðbótina. Frekari upplýsingar er að finna í [Setja upp bankareikninga](bank-how-setup-bank-accounts.md) og [Nota AMC Banking 365 Fundamentals viðbótina](ui-extensions-amc-banking.md). Þar að auki þarf að velja **Leyfa útflutning greiðslu** gátreiturinn á síðunni **Almennar Færslubókakeyrslur**. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

Notaðu síðuna **Kreditfærsludagbækur** til að skoða greiðsluskrárnar sem fluttar voru út úr útgreiðslubókinni. Á þessari síðu er einnig hægt að endurútflutta greiðsluskrár ef tæknilegar villur eða skráarbreytingar urðu. Þó skal athuga að útfluttar EFT-skrár eru ekki sýndar á þessari síðu og ekki er hægt að flytja þær út aftur.  

### Til að flytja út greiðslur í bankaskrá

Eftirfarandi skref útskýra hvernig á að greiða lánardrottni með ávísun. Skrefin eru svipuð og endurgreiðsla til viðskiptamanns með ávísun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.
2. Fyllið út greiðslubókarlínurnar. Nánari upplýsingar eru í [Skrá greiðslur og endurgreiðslur](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Ef EFT eru notaðar þarf að velja annaðhvort **Rafrænar Greiðslu** eða **Rafrænar Greiðslu – IAT** í reitnum **Tegund Bankagreiðslu** reit. Mismunandi útflutningsþjónusta skráa og snið þeirra þurfa mismunandi uppsetningargildi á síðunum **Bankareikningsspjald** og **Bankareikn.spjald lánardr.**. Þú færð að vita um uppsetningargildi sem eru röng eða sem vantar þegar þú reynir að flytja út skrána.
    >
    > Aðeins hægt að nota EFT-eiginleikann fyrir bankareikninga í innlendum gjaldmiðli. Ekki er hægt að nota hann með erlendum gjaldmiðli, sem gefinn er til kynna með gildinu á svæðinu **Gjaldmiðilskóði**. (Auður reitur þýðir innlendur gjaldmiðill.)

3. Þegar búið er að fylla út allar útgreiðslubókarlínur skal velja aðgerðina **Flytja út** .
4. Á síðunni **Flytja út rafrænar greiðslur** þarf að fylla reitina út eftir þörfum.

    Villuboð birtast í upplýsingakassanum **Villur** greiðsluskrár þar sem einnig er hægt að velja villuboð til að fá nánari upplýsingar. Leysa verður allar villur áður en hægt er að flytja út greiðsluskrána.

    > [!TIP]  
    > Þegar þú notar AMC Banking 365 Fundamentals viðbótina er algeng villa sú að bankareikningsnúmerið sé ekki með lengdina sem bankinn fer fram á. Til að forðast villuna eða leysa úr henni þarf að fjarlægja gildið á **IBAN** reitnum **Bankareikningsspjald** síðunni og svo, í **Nr. Bankareiknings** reitnum, slá inn bankareikningsnúmer á því sniði sem bankinn fer fram á.

5. Á síðunni **Vista sem** skal tilgreina staðsetninguna þangað sem skráin er flutt út og velja svo **Vista**.

    > [!NOTE]  
    > Ef þú ertu að nota EFT, vistaðu þá tilbúna lánardrottinn greiðslu formið sem word-skjal eða láta það sent beint til lánardrottins með tölvupósti. Greiðslur eru nú bætt á **Búa til EFT skrá** síðuna þar sem hægt að setja saman fjölgreiðslupantanir til að spara miðlaunarkostnaður. Nánari upplýsingar, sjá eftirfarandi skref.
6. Á síðunni **Útgreiðslubækur** skal velja aðgerðina **Búa til EFT-skrá** .

    Á síðunni **Mynda EFT-skrá** sýnir flýtiflipinn **Línur** allar EFT-greiðslur sem fluttar voru út úr greiðslubók fyrir bankareikning en hafa ekki enn verið búnar til.
7. Velja **Búa til EFT skrá** aðgerð til að flytja út eina skrá fyrir öll EFT greiðslur.
8. Á síðunni **Vista sem** skal tilgreina staðsetninguna þangað sem skráin er flutt út og velja svo **Vista**.

Bankagreiðsluskráin er flutt út á tilgreindan stað. Þú getur hlaðið honum upp á rafræna bankareikninginn þinn og innt af hendi raunverulegar greiðslur. Þá má bóka útflutta greiðslubókarlínur.

### Til að áætla hvenær á að bóka útfluttar greiðslur

Ef ekki á að bóka útgreiðslubókarlínu vegna útfluttra greiðslna er bara hægt að eyða færslubókarlínunni. Til dæmis vegna þess að beðið er eftir staðfestingu á því að bankinn hafi unnið færsluna. Seinna, þegar útgreiðslubókarlína er stofnuð til að greiða eftirstandandi upphæð sýnir reiturinn **Útflutt heildarupphæð** hversu mikið af greiðsluupphæðinni var þegar útflutt. Þú getur einnig fundið ítarlegar upplýsingar um heildarupphæðir sem hafa verið fluttar út með því að velja hnappinn **Skráningarfærslur kreditmillifærslna** til að sjá upplýsingar um útfluttar greiðsluskrár.

Ef ekki á að bóka greiðslur fyrr en bankinn staðfestir að þær séu unnar er hægt að:

* Í greiðslubók með greiðslulínum sem lagðar eru til er hægt að raða annaðhvort dálknum **Flytja út í greiðsluskrá** eða **Útflutt heildarupphæð** og eyða síðan greiðslutillögum fyrir opna reikninga þar sem greiðslur voru þegar innt af hendi.
* Á síðunni **Greiðslutillögur** til lánardr. þar sem tilgreint er hvaða greiðslur á að setja inn í útgreiðslubókina er hægt að velja **gátreitinn Sleppa útfluttum** greiðslum ef ekki á að setja inn færslubókarlínur fyrir greiðslur sem þegar voru fluttar út.

Til að sjá upplýsingar um útfluttar greiðslur, veljið aðgerðina **Útflutningsferill greiðslna**.

### Að endurútflytja greiðslur í bankaskrá

Hægt er að endurútflytja greiðsluskrár af síðunni **Skráningar kreditmillifærslna**. Áður en greiðslubókarlínum er eytt eða bókað er einnig hægt að flytja greiðsluskrána út aftur á **síðunni Útgreiðslubækur** með því að flytja hana út aftur. Ef greiðslubókarlínum er eytt eða bókað eftir útflutninginn er hægt að flytja sömu greiðsluskrá út aftur af síðunni **Kreditfærsludagbækur** . Veldu línuna fyrir runu kreditfærslanna sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslur í bankaskrá**.

> [!NOTE]  
> Útfluttar EFT skrár ekki eru sýndar á síðunni **Kreditfærsluskrár** og ekki er hægt að flytja þær aftur út.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skráningar kreditfærslna** og velja síðan viðkomandi tengil.
2. Veldu greiðsluútflutning sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslu í skrá**.

## Bókun greiðslna

Þegar bankinn vinnur úr rafrænu greiðslunni skal bóka greiðslurnar. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).

## Sjá einnig .

[Nota AMC Banking 365 Fundamentals viðbótina](ui-extensions-amc-banking.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
