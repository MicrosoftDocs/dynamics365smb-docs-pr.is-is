---
title: Flytja út greiðslur í rafræna greiðsluskrá| Microsoft Docs
description: Til að framkvæma greiðslur lánardrottins, þarf að virkja umskráningarþjónustu fyrir bankagögn, og hlaða upp skránni á netbankanum þínum til að millifæra fjármunina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 539aac89d2da6b2eb81da7f6df729cdb5bc15cb1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253793"
---
# <a name="export-payments-to-a-bank-file"></a>Flytja út greiðslur í bankaskrá
Þegar þú ert tilbúinn að inna af hendir greiðslur til lánardrottna, eða endurgreiðslur til starfsmanna, er hægt að flytja út skrá með greiðsluupplýsingum á línurnar á síðunni **Greiðslubók**. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning.

Í almenn útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)], er altæk þjónustuveita til að umbreyta bankagögnum í annað skráarsnið sem bankinn krefst að er uppsett og tengt. Í Norður-Ameríku útgáfum má nota sömu þjónustuvöru til að senda greiðslu skrám sem rafrænar millifærslu (EFT) en með ofurlítið annarri vinnslu. Sjá skref 6 í [Til að flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).    

> [!NOTE]  
>   Áður en hægt er að flytja út greiðsluskrár í greiðslubókina, verður að tiltaka rafrænt sniði bankareikningnum sem við á, og verður að virkja umbreytingarþjónustu fyrir bankagögn. Frekari upplýsingar eru í [Setja á upp bankareikninga](bank-how-setup-bank-accounts.md) og [Setja upp umskráningarþjónusta fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md). Þar að auki þarf að velja **Leyfa útflutning greiðslu** gátreiturinn á síðunni **Almennar Færslubókakeyrslur**. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).  

Síðan **Skráningar kreditmillifærslna** er notuð til að skoða greiðsluskrár sem hafa verið fluttar út úr greiðslubókinni. Á þessari síðu er einnig hægt að endurflytja út greiðsluskrár ef um er að ræða tæknilegar villur eða breytingar á skrá. Þó er bent á að ekki eru sýndir á þessari síðu útfluttar EFT skrár og þær geta ekki verið fluttar út aftur.  

## <a name="to-export-payments-to-a-bank-file"></a>Til að flytja út greiðslur í bankaskrá
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

## <a name="to-plan-when-to-post-exported-payments"></a>Til að áætla hvenær á að bóka útfluttar greiðslur
Ef þú vilt ekki bóka greiðslubókarlínu fyrir útflutta greiðslu, t.d. vegna þess að þú ert að bíða eftir staðfestingu á því að færslan hafi verið meðhöndluð af bankanum geturðu einfaldlega eytt línunni. Þegar þú síðar stofnar greiðslubókarlínu til að greiða eftirstandandi upphæð á reikningnum sýnir reiturinn **Heildarupphæð flutt út** hversu mikið af greiðsluupphæðinni hefur þegar verið flutt út. Þú getur einnig fundið ítarlegar upplýsingar um heildarupphæðir sem hafa verið fluttar út með því að velja hnappinn **Skráningarfærslur kreditmillifærslna** til að sjá upplýsingar um útfluttar greiðsluskrár.

Ef fylgt er ferli þar sem ekki á að bóka greiðslur fyrr en staðfesting hefur fengist á því að þær hafa verið unnar í bankanum er hægt að stjórna því á tvo vegu.

* Í greiðslubók með tillögum að greiðslulínum geturðu flokkað með annað hvort dálkinum **Flutt út í greiðsluskrá** eða **Heildarupphæð flutt út** og svo eytt greiðslutillögum fyrir opna reikninga þar sem greiðslur hafa þegar átt sér stað og þú vilt ekki greiða.
* Á síðunni **Greiðslutillögur til lánardrottna** þar sem þú tilgreinir hvaða greiðslur eigi að setja í greiðslubókina, geturðu valið gátreitinn **Sleppa útfluttum greiðslum** ef þú vilt ekki setja inn færslubókarlínur fyrir greiðslur sem hafa þegar verið fluttar út.

Til að sjá upplýsingar um útfluttar greiðslur, veljið aðgerðina **Útflutningsferill greiðslna**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Að endurútflytja greiðslur í bankaskrá
Hægt er að endurútflytja greiðsluskrár af síðunni **Skráningar kreditmillifærslna**. Áður en greiðslubókarlínum er eytt eða þær bókaðar er einnig hægt að endurútflytja greiðsluskrána af síðunni **Greiðslubók** með því að flytja hana einfaldlega út aftur. Ef þú hefur eytt eða bókað greiðslubókarlínurnar eftir að þú hefur flutt þær út getur þú endurútflutt sömu greiðsluskrá af síðunni **Skráningar kreditmillifærslna**. Veldu línuna fyrir runu kreditfærslanna sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslur í bankaskrá**.

> [!NOTE]  
>   Útfluttar EFT skrár ekki eru sýndar á síðunni **Kreditfærsluskrár** og ekki er hægt að flytja þær aftur út.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skráningar kreditmillifærslna** og veldu síðan tengda tengilinn.
2. Veldu greiðsluútflutning sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslu í skrá**.

## <a name="see-also"></a>Sjá einnig
[Framkvæma greiðslur](payables-make-payments.md)  
[Til greiðslu](payables-manage-payables.md)  
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
