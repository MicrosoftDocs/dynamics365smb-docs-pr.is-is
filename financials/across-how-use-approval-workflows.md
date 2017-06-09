---
title: "Hvernig á að nota Samþykkisverkflæði | Microsoft Docs"
description: "Hvernig á að: Nota samþykktarverkflæði"
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 04/25/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ed08fdb7f78c9f6c338e287cd4ef42d7ce0cb72c
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-approval-workflows"></a>Hvernig á að: Nota samþykktarverkflæði
Þegar færsla, svo sem innkaupaskjal eða viðskiptamannaspjald sem stofnað hefur verið þarfnast samþykktar aðila innan fyrirtækisins er send samþykktarbeiðni sem hluti af verkflæði. Beiðnin um samþykki færslu verður send til viðeigandi samþykkjanda á grundvelli þess hvernig verkflæðið hefur verið sett upp.

Setja upp samþykktarverkflæði í **Verkflæði** glugganum.

Kjarna samþykkisverkflæði fyrir innkaupaskjöl, söluskjöl, greiðslubækur, viðskiptamannaspjöld og birgðaspjöldum eru tilbúin til að byrja sem aðstoð við uppsetningu. Nánari upplýsingar sjá í [Velkomin í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md).

**Athugið**: Þessi virkni krefst að upplifun þín er stilltur á **Pakki**. Nánari upplýsingar, sjá [Sérstilli þína [!INCLUDE[d365fin](includes/d365fin_md.md)]upplifun](ui-experiences.md).

## <a name="to-request-approval-of-a-record"></a>Til að biðja um samþykki færslu
Eftirfarandi verkið er framkvæmt af samþykktarnotanda.

1. Í glugganum sem táknar færsluna er valið **Senda samþykktarbeiðni** aðgerðin.
2. Til að sjá allar samþykktarbeiðnir skal velja **Leit að síðu eða skýrslu** táknið efst í hægra horni ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Beiðnifærslur samþykktar** og velja síðan viðkomandi tengil.

Staða samþykktarfærslunnar er uppfærð úr **Stofnað** í **Opið**. Staða færslunnar, til dæmis innkaupareikningur, er uppfærð úr **Opin** í **Bíður samþykkis** og er áfram lokuð fyrir breytngar þar til allir samþykkjendur hafa samþykkt færsluna.

Þegar samþykkjandi hefur samþykkt færslu breytist staðan í **Losuð** Þá er hægt að halda áfram verkefni með færsluna.

## <a name="to-cancel-requests-for-approval"></a>Hætt við beiðnir um samþykki
Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Vera kann að viðskiptavinur vilji breyta pöntun eftir að hún hefur verið lögð fram til samþykktar. Í þessu tilfelli má hætta við samþykktarferlið og gera nauðsynlegar breytingar á pöntuninni áður en beðið er um samþykki aftur.

- Í glugganum sem sýnir færsluna er valið **Hætta við samþykktarbeiðni** aðgerðin.

Þegar hætt hefur verið við samþykktarbeiðnina uppfærist staðan á samþykktarfærslunni í **Hætt við**. Staða færslunnar er uppfærð úr **Bíður samþykktar** í **Opið**. Samþykktarferlið getur þá hafist á ný.

## <a name="to-make-minor-changes-to-approved-records"></a>Gera smávægilegar breytingar á samþykktum færslum
Ef gera á smávægilega breytinga á færslu eftir að hún hefur verið samþykkt er hægt að enduropna hana, gera breytinguna og samþykkja hana. Fyrir smávægilegar breytingar er þetta gert með hnöppunum **Enduropna** og **Gefa út**.

1. Opna skal gluggann sem sýnir færsluna, t.d. innkaupareikning, og velja síðan **opna aftur** aðgerðina.

    Reitnum **Staða skjals** er breytt í **Opna**.
2. Nauðsynlegar breytingar eru gerðar á færslunni, svo sem heimilisfang lánardrottins.
3. Valið er **Losa** aðgerð.

Þegar frumfærslan er opnuð aftur er staða tengdrar samþykktarfærslu áfram Samþykkt í glugganum **Samþykktarfærslur **.

## <a name="to-approve-or-reject-requests-for-approval"></a>Samþykkja eða hafna samþykktum
Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Hægt er að vinna samþykktarbeiðnum í glugganum **Beiðnir til að samþykkja** , til dæmis til að samþykkja margar beiðnum í einu. Einnig er hægt er að vinna hvern beiðni á tengdar færslu, eins og í **Innkaupareikningur** glugganum, með því að velja tengillinn í tilkynningin sem þú tekur á móti.

1. Efst í hægra horninu skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Beiðnir til að samþykkja** og velja svo tengdan tengil.
2. Velja eina eða fleiri línur fyrir færslu eða færslur sem á að samþykkja eða hafna.
3. Valið er **Samþykkja**, **Hafna**, eða **Framselja** aðgerðir.

Þegar færsla hefur verið samþykkt eða henni hafnað breytist samþykktarstaða í reitnum **Staða** í **Samþykkt** eða **Hafnað**.

Ef samþykkjendastigveldi er til staðar mun færslustaða vera **Bíður samþykktar** þar til allir samþykkjendur hafa samþykkt færsluna. Þá mun staða færslunnar breytast í **Losað**.

Á sama tíma breytist samþykktarstaða úr **Stofnað** í **opið** um leið og samþykktarbeiðni fyrir færsla er stofnuð. Ef beiðni er hafnað berytist samþykktarstaða í **Hafnað**. Staðan er áfram **opið** eða **Hafnað** þar til allir samþykkjendur hafa samþykki beiðnina.

## <a name="to-delegate-requests-for-approval"></a>Úthluta beiðnum um samþykki
Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Til að koma í veg fyrir að skjöl safnist upp með öðru móti stífla verkflæði getur sá sem bað um samþykktina eða samþykkjandinn úthlutað samþykktarbeiðni til staðgengilssamþykkjanda. Staðgengil getur annað hvort verið tilgreindur staðgengill, beinn samþykkjandi eða stjórnandi samþykkis, í þeirri forgangsröð. Þessi aðgerð er yfirleitt notuð ef samþykkjandi er ekki við og getur ekki samþykkt beiðnir fyrir lokadaginn.

1. Efst í hægra horninu skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Beiðnir til að samþykkja** og velja svo tengdan tengil.
2. Velja eina eða fleiri línur fyrir samþykktarbeiðni sem á að úthluta á staðgengil til samþykktar, og veldu síðan aðgerðina **framselja**.

Tilkynning um að samþykkja beiðnina er send til staðgengilssamþykkjanda.

## <a name="to-manage-overdue-approval-requests"></a>Til að stjórna samþykktarbeiðnum sem eru komnar fram yfir á tíma
Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Með reglulegu millibili kann að þurfa að minna notendur samþykktarverkflæðis á beiðnir sem eru fallnar á tíma og sem þeir þurfa að bregðast við. Virknin **Senda samþykkistilkynningar sem komnar eru fram yfir á tíma** er notuð fyrir þetta.

Aðgerðin **Senda samþykkistilkynningar sem komnar eru fram yfir á tíma** kannar allar opnar samþykktar færslur sem eru fallnar á tíma. Allir samþykkjendur með a.m.k. eina samþykkt fram yfir á tíma fá tilkynningu með lista yfir þær samþykktarfærslur sem fallnar eru á tíma. Afrit af tilkynningu er sent til samþykkjenda þeirra og allra sendenda samþykkta sem fallnar eru á tíma. Þetta er gagnlegt ef nauðsynlegt er að framselja samþykktarfærslu sem fallin er á tíma til staðgengils.

1. Efst í hægra horninu skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Gjaldfallnar samþykktarbeiðnir** og velja svo tengdan tengil.
2. Í **Samþykktarbeiðnir komin fram yfir á tíma** glugganum er valið á **Samþykktarbeiðnir komin fram yfir á tíma Tilkynningar** aðgerð.

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)    
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

