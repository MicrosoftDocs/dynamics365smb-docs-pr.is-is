---
title: "Flytja út greiðslur í rafræna greiðsluskrá| Microsoft Docs"
description: "Til að framkvæma greiðslur lánardrottins, þarf að virkja umskráningarþjónustu fyrir bankagögn, og hlaða upp skránni á netbankanum þínum til að millifæra fjármunina."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 706ebc016feae6ec5db40c0efc006a6e6e771c4c
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="export-payments-to-a-bank-file"></a>Flytja út greiðslur í bankaskrá
Þegar þú ert tilbúinn að inna af hendir greiðslur til lánardrottna, eða endurgreiðslur til starfsmanna, er hægt að flytja út skrá með greiðsluupplýsingum á línurnar í glugganum **Greiðslubók**. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning.

Í almenn útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)], er altæk þjónustuveita til að umbreyta bankagögnum í annað skráarsnið sem bankinn krefst að er uppsett og tengt. Í Norður-Ameríku útgáfum má nota sömu þjónustuvöru til að senda greiðslu skrám sem rafrænar millifærslu (EFT) en með ofurlítið annarri vinnslu. Sjá skref 6 í „til Að flytja út greiðslur til bankaskráar“ hlutanum.    

> [!NOTE]  
>   Áður en hægt er að flytja út greiðsluskrár í greiðslubókina, verður að tiltaka rafrænt sniði bankareikningnum sem við á, og verður að virkja umbreytingarþjónustu fyrir bankagögn. Frekari upplýsingar eru í [Setja á upp bankareikninga](bank-how-setup-bank-accounts.md) og [Setja upp umskráningarþjónusta fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md). Þar að auki þarf að velja **Leyfa útflutning greiðslu** gátreiturinn á **Almennar Færslubókakeyrslur** glugganum. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).  

Glugginn **Skráningar kreditmillifærslna** er notaður til að skoða greiðsluskrár sem hafa verið fluttar út úr greiðslubókinni. Í þessum glugga er einnig hægt að endurflytja út greiðsluskrár ef um er að ræða tæknilegar villur eða breytingar á skrá. Þó er bent á að ekki eru sýndir í þessum glugga útflutt EFT skrár og þær geta ekki verið aftur útflutt.  

## <a name="to-export-payments-to-a-bank-file"></a>Til að flytja út greiðslur í bankaskrá
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubækur** og velja svo viðeigandi tengil.
2. Fyllið út greiðslubókarlínur, t.d. með aðgerðinni **Greiðslutillögur til lánardrottna**. Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md).
3. Fyllið út reitina í greiðslubókarlínunum eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Ef EFT eru notaðar þarf að velja annaðhvort **Rafrænar Greiðslu** eða **Rafrænar Greiðslu – IAT** í reitnum **Tegund Bankagreiðslu** reit. Mismunandi útflutningsþjónustu skráa og snið þeirra krefjast mismunandi uppsetningargildi á **Bankareikningsspjald** og **Bankareikningsspjaldi Lánardrottins** gluggum. Þú færð að vita um uppsetningargildi sem eru röng eða sem vantar þegar þú reynir að flytja út skrána.

4. Þegar öllum greiðslubókarlínunum er lokið skal velja **Flytja út** aðgerðina.
5. Í glugganum **Flytja út rafrænar greiðslur** þarf að fylla reitina út eftir þörfum.

    Öll villuboð birtast í **Villur í greiðsluskrá** upplýsingareitnum þar sem þú getur einnig valið villuboð til að sjá ítarlegar upplýsingar. Leysa þarf úr öllum villum áður en hægt er að flytja út greiðsluskrána.

    > [!TIP]  
    >   Þegar þú notar umskráningarþjónustu fyrir bankagögn er algeng villa sú að bankareikningsnúmerið sé ekki með lengdina sem bankinn fer fram á. Til að forðast villuna eða leysa úr henni þarf að fjarlægja gildið í **IBAN** reitnum **Bankareikningsspjald** glugganum og svo, í **Nr. Bankareiknings** reitnum, slá inn bankareikningsnúmer á því sniði sem bankinn fer fram á.

6. Í glugganum **Vista sem** skal tilgreina staðsetninguna þangað sem skráin er flutt út og velja svo **Vista**.

    > [!NOTE]  
    >   Ef þú ertu að nota EFT, vistaðu þá tilbúna lánardrottinn greiðslu formið sem word-skjal eða láta það sent beint til lánardrottins með tölvupósti. Greiðslur eru nú bætt á **Búa til EFT skrá** gluggann, þar sem hægt að setja saman fjölgreiðslupantanir til að spara miðlaunarkostnaður. Nánari upplýsingar, sjá eftirfarandi skref.
7. Í **Greiðslubók** glugga, er valið **Búa til EFT skrá** aðgerðina.

    Í glugganum **Búa til EFT skrá** eru allar greiðslur uppsettar fyrir EFT, sem þú hefur flutt út úr greiðslubókinni fyrir tilgreinda bankareikninga en hefur enn ekki búið til, tilgreindar á **Línur** Flýtiflipanum.
8. Velja **Búa til EFT skrá** aðgerð til að flytja út eina skrá fyrir öll EFT greiðslur.
9. Í glugganum **Vista sem** skal tilgreina staðsetninguna þangað sem skráin er flutt út og velja svo **Vista**.

Bankagreiðsluskráin er flutt út á staðsetningu sem þú tilgreinir, og hægt er að meðhöndla hana til hlaða henni upp á rafrænn bankareikning og framkvæma greiðslurnar. Þá má bóka útflutta greiðslubókarlínur.

## <a name="to-export-payments-that-represent-customer-refunds"></a>Til að flytja út greiðslur sem tákna endurgreiðslum viðskiptamanns
Eftirfarandi lýsir hvernig hægt er að vinna í kringum vandamál varðandi útflutning á rafrænar endurgreiðsla.

> [!CAUTION]  
>   Tilbúin greiðsla færslubókarlínurnar er ekki hægt að bóka, eytt eða ógildur.
1. Setja viðskiptamann upp sem lánardrottinn. Gefið því heitið „Viðskiptamaður X fyrir endurgreiðslur“, til dæmis. Nánari upplýsingar eru í [Skráning nýrra lánardrottna](purchasing-how-register-new-vendors.md).
2. Á greiðslubókarlínuna fyrir viðskiptamanninn, setjið **Reikningstegund** reitinn á **Viðskiptamanns**, og **Skjalategund** reitinn á **Endurgreiðsla**.
3. Framkvæma venjulegur verkstigin til útflutnings greiðslu eins og lýst er í hlutanum „Að flytja út greiðslur til bankaskráar".

## <a name="to-plan-when-to-post-exported-payments"></a>Til að áætla hvenær á að bóka útfluttar greiðslur
Ef þú vilt ekki bóka greiðslubókarlínu fyrir útflutta greiðslu, t.d. vegna þess að þú ert að bíða eftir staðfestingu á því að færslan hafi verið meðhöndluð af bankanum geturðu einfaldlega eytt línunni. Þegar þú síðar stofnar greiðslubókarlínu til að greiða eftirstandandi upphæð á reikningnum sýnir reiturinn **Heildarupphæð flutt út** hversu mikið af greiðsluupphæðinni hefur þegar verið flutt út. Þú getur einnig fundið ítarlegar upplýsingar um heildarupphæðir sem hafa verið fluttar út með því að velja hnappinn **Skráningarfærslur kreditmillifærslna** til að sjá upplýsingar um útfluttar greiðsluskrár.

Ef fylgt er ferli þar sem ekki á að bóka greiðslur fyrr en staðfesting hefur fengist á því að þær hafa verið unnar í bankanum er hægt að stjórna því á tvo vegu.

* Í greiðslubók með tillögum að greiðslulínum geturðu flokkað með annað hvort dálkinum **Flutt út í greiðsluskrá** eða **Heildarupphæð flutt út** og svo eytt greiðslutillögum fyrir opna reikninga þar sem greiðslur hafa þegar átt sér stað og þú vilt ekki greiða.
* Í glugganum **Greiðslutillögur til lánardrottna** þar sem þú tilgreinir hvaða greiðslur eigi að setja í greiðslubókina, geturðu valið gátreitinn **Sleppa útfluttum greiðslum** ef þú vilt ekki setja inn færslubókarlínur fyrir greiðslur sem hafa þegar verið fluttar út.

Til að sjá upplýsingar um útfluttar greiðslur, veljið aðgerðina **Útflutningsferill greiðslna**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Að endurútflytja greiðslur í bankaskrá
Hægt er að endurútflytja greiðsluskrár úr glugganum **Skráningar kreditmillifærslna**. Áður en greiðslubókarlínum er eytt eða þær bókaðar er einnig hægt að endurútflytja greiðsluskrána úr glugganum **Greiðslubók** með því að flytja hana einfaldlega út aftur. Ef þú hefur eytt eða bókað greiðslubókarlínurnar eftir að þú hefur flutt þær út getur þú endurútflutt sömu greiðsluskrá úr glugganum **Skráningar kreditmillifærslna**. Veldu línuna fyrir runu kreditfærslanna sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslur í bankaskrá**.

> [!NOTE]  
>   Útfluttar EFT skrár ekki eru sýndir í glugga **Kreditfærsluskrár** og getur ekki verið aftur útfluttar.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Kreditfærsluskrár** og velja svo viðeigandi tengil.
2. Veldu greiðsluútflutning sem þú vilt endurútflytja og notaðu svo aðgerðina **Endurútflytja greiðslu í skrá**.

## <a name="see-also"></a>Sjá einnig
[Viðskiptaskuldir](payables-manage-payables.md)  
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

