---
title: Greiða með umreikningsþjónustu bankagagna eða SEPA-kreditfærslu | Microsoft Docs
description: Meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c1089a48cee57f6e42e48d995ed9c9ae7fd8fd80
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302037"
---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a>Greiða með umreikningsþjónustu bankagagna eða SEPA-kreditfærslu
Á síðunni **Greiðslubók** er hægt að meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning. [!INCLUDE[d365fin](includes/d365fin_md.md)] styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.

Í almenn útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)], er altæk þjónustuveita til að umbreyta bankagögnum í annað skráarsnið sem bankinn krefst að er uppsett og tengt. Í Norður-Ameríku útgáfum má nota sömu þjónustuvöru til að senda greiðslu skrám sem rafrænar millifærslu (EFT) en með ofurlítið annarri vinnslu. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).   

 Til að gera SEPA kredifærslur, verður þú fyrst að setja upp bankareikning, lánardrottin, og almenna bókarkeyrslurunu sem greiðslubók er byggt á. Greiðslur til lánardrottna eru því næst undirbúnar með því að fylla sjálfkrafa út síðuna **Greiðslubók** með gjaldföllnum greiðslum með tilgreindum bókunardagsetningum.  

> [!NOTE]  
>  Þegar þú hefur staðfest að greiðslurnar hafi verið framkvæmdar af bankanum getur þú bókað greiðslubókarlínurnar.  

## <a name="setting-up-the-bank-data-conversion-service"></a>Uppsetning umskráningarþjónustu fyrir bankagögn
Virkjið eiginleikann UUmreikningsþjónusta fyrir bankagögn til að umbreyta hvers kyns bankayfirlitsskrá í snið sem hægt er að flytja inn eða til að umbreyta útfluttum greiðsluskrám í það snið sem bankinn krefst. Nánari upplýsingar er að finna í [Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-statement-service.md).

## <a name="setting-up-sepa-credit-transfer"></a>Uppsetning SEPA-kreditfærslna
Af síðunni **Greiðslubók** er hægt að flytja út greiðslur í skrá til upphals í netbanka til vinnslu á tengdum peningamillifærslum. [!INCLUDE[d365fin](includes/d365fin_md.md)] styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.  

Til að opna fyrir útflutning af skráasniði bankaskrár sem ekki eru studdar af [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að setja upp gagnaskiptaskilgreiningu með því að nota gagnaskiptaumgjörð. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

Áður en þú getur afgreitt greiðslu rafrænt með því að flytja greiðsluskrár í SEPA-kreditfærslusnið, verður þú að framkvæma eftirfarandi uppsetningarskref:  

* Setja upp viðkomandi bankareikning til að meðhöndla SEPA-kreditfærslusnið.  
* Setja upp lánardrottinn spjöld með því að flytja skrár úr í SEPA-kreditmillifærslur sniði.  
* Setja upp viðeigandi bókarkeyrslu til að gera virkan útflutning greiðslu af **Greiðslubók** síðunni  
* Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Að setja upp bankareikning fyrir SEPA-kreditfærslu  
1. Í reitinn **Leita** skal færa inn **Bankareikningar** og velja síðan viðkomandi tengi.  
2. Opnið spjald bankareikningsins sem á að flytja greiðsluskrár úr á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Millifærsla**, í reitnum **Útflutningssvið greiðslu** skal velja **SEPADD**.  
4. Í **SEPA Kreditfærsla skilaboð kenni númeraröð** reitnum skal velja númeraröð sem tölum eru úthlutað úr til SEPA-kreditfærslu.  
5. Gangið úr skugga um að reiturinn **IBAN** sé útfylltur.  

    > [!NOTE]  
    >  Reiturinn **Gjaldmiðilskóði** verður að vera stilltur á **EUR**, því SEPA-kreditmillifærslur er aðeins hægt að gera í evrum.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Að setja upp lánardrottin fyrir SEPA-kreditfærslu  
1. Í reitnum **Leita** skal færa inn **Lánardrottnar** og velja síðan viðkomandi tengi.  
2. Opnið spjald lánardrottins sem á að greiða til rafrænt útflutningi greiðsluskráa á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Greiðsla**, í reitnum **Kóði greiðslumáta** skal velja **BANKI**.  
4. Í **Valinn bankareikningur** reitnum, veldu banka sem fé verður flutt inn á þegar það er unnið með rafrænum bankann þinn.  

     Gildið í reitnum **Valinn bankareikningur** er afritað í reitinn **Móttökubankareikningur** á síðunni **Greiðslubók**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Að stilla greiðslubók upp til að flytja greiðsluskrár  
1. Í reitnum **Leit** skal færa inn **Greiðslubækur** og velja síðan viðkomandi tengil.  
2. Opnið greiðslubókina sem á að nota til vinna greiðslur með því að flytja skrár á SEPA-kreditfærslusniði.  
3. Í reitnum **Heiti keyrslu** er felli\-lista hnappurinn valinn.  
4. Á síðunni **Færslubókarkeyrslur** á flipanum **Heim**, í flokknum **Stjórna**, skal velja **Breyta lista**.  
5. Á línunni fyrir greiðslubókina sem notuð verður til að flytja út greiðslur skal velja gátreitinn **Leyfa greiðsluútflutning**.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.  
1. Í reitnum **Leit** skal færa inn **Greiðsluhættir** og velja síðan viðkomandi tengil.  
2. Á síðunni **Greiðslumáti** skaltu velja greiðslumáta sem er notað til að flytja út greiðslur frá, og þá velja **Greiðsluútflutningur Línuskilgreining** reitinn.  
3. Á síðunni **Greiðsluútflutningur Línuskilgreining** skal velja kóðann sem var tilgreindur í **Kóði** reitnum á **Línuskilgreiningar** flýtiflipanum í skrefi 4 í „Að lýsa sniði lína og dálka í skránni“ hlutanum í [Setja upp gagnaskiptaskilgreiningar](across-how-to-set-up-data-exchange-definitions.md) aðgerðinni.  

Umboðið fyrir beingreiðslur er sjálfkrafa sett inn í **Kenni umboðs fyrir beint debet** reitinn þegar sölureikningur er stofnaður fyrir viðskiptamann sem var valinn í skrefi 2. Nánari upplýsingar er að finna í [Stofna ítrekaðar sölu og innkaupalínur](sales-how-work-standard-lines.md).   

## <a name="preparing-the-payment-journal"></a>Greiðslubók undirbúin
Fyllið út greiðslubókina með línum fyrir greiðslu á gjalddaga til lánardrottna með möguleikanum á að setja inn bókunardagsetningar byggt á gjalddaga tengdra innkaupaskjala. Nánari upplýsingar er að finna í [Stjórna skuldum](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Greiðslur fluttar út í bankaskrá
Þegar þú ert tilbúinn að inna af hendir greiðslur til lánardrottna, eða endurgreiðslur til starfsmanna, er hægt að flytja út skrá með greiðsluupplýsingum á línurnar á síðunni **Greiðslubók**. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning.

Í almennri útgáfu [!INCLUDE[d365fin](includes/d365fin_md.md)] er umskráningarþjónusta fyrir bankagögn sett upp og tengd. Í Norður-Ameríku útgáfum má nota sömu þjónustuvöru til að senda greiðslu skrám sem rafrænar millifærslu (EFT) en með ofurlítið annarri vinnslu. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
>   Áður en hægt er að flytja út greiðsluskrár í greiðslubókina, verður að tiltaka rafrænt sniði bankareikningnum sem við á, og verður að virkja umbreytingarþjónustu fyrir bankagögn. Frekari upplýsingar eru í [Setja á upp bankareikninga](bank-how-setup-bank-accounts.md) og [Setja upp umskráningarþjónusta fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md). Þar að auki þarf að velja **Leyfa útflutning greiðslu** gátreiturinn á síðunni **Almennar Færslubókakeyrslur**. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).  

Síðan **Skráningar kreditmillifærslna** er notuð til að skoða greiðsluskrár sem hafa verið fluttar út úr greiðslubókinni. Á þessari síðu er einnig hægt að endurflytja út greiðsluskrár ef um er að ræða tæknilegar villur eða breytingar á skrá. Þó er bent á að ekki eru sýndir á þessari síðu útfluttar EFT skrár og þær geta ekki verið fluttar út aftur.  

### <a name="to-export-payments-to-a-bank-file"></a>Til að flytja út greiðslur í bankaskrá
Eftirfarandi dæmi sýnir hvernig á að greiða lánardrottni með ávísun. Skrefin eru svipuð og endurgreiðsla til viðskiptamanns með ávísun.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **greiðslubók** og veldu síðan tengda tengilinn.
2. Fyllið út greiðslubókarlínurnar. Nánari upplýsingar eru í [Skrá greiðslur og endurgreiðslur](payables-how-post-payments-refunds.md).

> [!NOTE]  
>   Ef EFT eru notaðar þarf að velja annaðhvort **Rafrænar Greiðslu** eða **Rafrænar Greiðslu – IAT** í reitnum **Tegund Bankagreiðslu** reit. Mismunandi útflutningsþjónustu skráa og snið þeirra krefjast mismunandi uppsetningargildi á **Bankareikningsspjald** og **Bankareikningsspjaldi Lánardrottins** síðum. Þú færð að vita um uppsetningargildi sem eru röng eða sem vantar þegar þú reynir að flytja út skrána.

3. Þegar öllum greiðslubókarlínunum er lokið skal velja aðgerðina **Flytja út**.
4. Á síðunni **Flytja út rafrænar greiðslur** þarf að fylla reitina út eftir þörfum.

    Öll villuboð birtast í **Villur í greiðsluskrá** upplýsingareitnum þar sem þú getur einnig valið villuboð til að sjá ítarlegar upplýsingar. Leysa þarf úr öllum villum áður en hægt er að flytja út greiðsluskrána.

    > [!TIP]  
    >   Þegar þú notar umskráningarþjónustu fyrir bankagögn er algeng villa sú að bankareikningsnúmerið sé ekki með lengdina sem bankinn fer fram á. Til að forðast villuna eða leysa úr henni þarf að fjarlægja gildið á **IBAN** reitnum **Bankareikningsspjald** síðunni og svo, í **Nr. Bankareiknings** reitnum, slá inn bankareikningsnúmer á því sniði sem bankinn fer fram á.

5. Á síðunni **Vista sem** skal tilgreina staðsetninguna þangað sem skráin er flutt út og velja svo **Vista**.

    > [!NOTE]  
    >   Ef þú ertu að nota EFT, vistaðu þá tilbúna lánardrottinn greiðslu formið sem word-skjal eða láta það sent beint til lánardrottins með tölvupósti. Greiðslur eru nú bætt á **Búa til EFT skrá** síðuna þar sem hægt að setja saman fjölgreiðslupantanir til að spara miðlaunarkostnaður. Nánari upplýsingar, sjá eftirfarandi skref.
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
>   Útfluttar EFT skrár ekki eru sýndar á síðunni **Kreditfærsluskrár** og ekki er hægt að flytja þær aftur út.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skráningar kreditmillifærslna** og veldu síðan tengda tengilinn.
2. Veldu greiðsluútflutning sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslu í skrá**.

## <a name="posting-the-payments"></a>Bókun greiðslna
Þegar rafræna greiðslan hefur verið unnin að fullu af bankanum skal bóka greiðslurnar. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).

## <a name="see-also"></a>Sjá einnig  
[Setja upp umskráningarþjónustu fyrir bankagögn](bank-how-setup-bank-statement-service.md)  
[Setja upp SEPA-kreditfærslur](finance-how-to-set-up-sepa-credit-transfer.md)  
[Stjórna skuldum](payables-manage-payables.md)   
[Vinna í færslubókum](ui-work-general-journals.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)   
