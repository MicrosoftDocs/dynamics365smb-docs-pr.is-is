---
title: "Samþykkja eða hafna skjölum í verkflæði| Microsoft Docs"
description: "Fara fram á, hafna eða framselja samþykkt á, til dæmis, innkaupa- eða söluskjali, sem hluta af verkflæði."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 0b83fbb4ec39a1a7596fd788e5dad985bacb30c2
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="use-approval-workflows"></a>Nota Samþykktarverkflæði
Þegar færsla, svo sem innkaupaskjal eða viðskiptamannaspjald sem stofnað hefur verið þarfnast samþykktar aðila innan fyrirtækisins er send samþykktarbeiðni sem hluti af verkflæði. Beiðnin um samþykki færslu verður send til viðeigandi samþykkjanda á grundvelli þess hvernig verkflæðið hefur verið sett upp.

Setja upp samþykktarverkflæði í **Verkflæði** glugganum. Nánari upplýsingar er að finna í [Uppsetning Verkflæði](across-set-up-workflows.md).

Í viðbót við samþykktarverkflæði sem lýst er í þessu efnisatriði, geturðu framkvæmt ýmis önnur verkflæðisverk. Frekari upplýsingar, [Nota verkflæði](across-use-workflows.md).

Kjarna samþykkisverkflæði fyrir innkaupaskjöl, söluskjöl, greiðslubækur, viðskiptamannaspjöld og birgðaspjöldum eru tilbúin til að byrja sem aðstoð við uppsetningu. Nánari upplýsingar er að finna í [Hafist handa](product-get-started.md).

## <a name="to-request-approval-of-a-record"></a>Til að biðja um samþykki færslu
Eftirfarandi verkið er framkvæmt af samþykktarnotanda.

1. Í glugganum sem táknar færsluna er valið **Senda samþykktarbeiðni** aðgerðin.
2. Til að sjá allar samþykktarbeiðnir skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") táknið, færa inn **Beiðnifærslur samþykktar** og velja síðan viðkomandi tengil.  

Staða samþykktarfærslunnar er uppfærð úr **Stofnað** í **Opið**. Staða færslunnar, til dæmis innkaupareikningur, er uppfærð úr **Opin** í **Bíður samþykkis** og er áfram lokuð fyrir breytngar þar til allir samþykkjendur hafa samþykkt færsluna.

Þegar samþykkjandi hefur samþykkt færslu breytist staðan í **Losuð** Þá er hægt að halda áfram verkefni með færsluna.

## <a name="to-cancel-requests-for-approval"></a>Hætt við beiðnir um samþykki
Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Vera kann að viðskiptavinur vilji breyta pöntun eftir að hún hefur verið lögð fram til samþykktar. Í þessu tilfelli má hætta við samþykktarferlið og gera nauðsynlegar breytingar á pöntuninni áður en beðið er um samþykki aftur.

- Í glugganum sem sýnir færsluna er valið **Hætta við samþykktarbeiðni** aðgerðin.

Þegar hætt hefur verið við samþykktarbeiðnina uppfærist staðan á samþykktarfærslunni í **Hætt við**. Staða færslunnar er uppfærð úr **Bíður samþykktar** í **Opið**. Samþykktarferlið getur þá hafist á ný.

## <a name="to-approve-or-reject-requests-for-approval"></a>Samþykkja eða hafna samþykktum
Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Hægt er að vinna samþykktarbeiðnum í glugganum **Beiðnir til að samþykkja** , til dæmis til að samþykkja margar beiðnum í einu. Einnig er hægt er að vinna hvern beiðni á tengdar færslu, eins og í **Innkaupareikningur** glugganum, með því að velja tengillinn í tilkynningin sem þú tekur á móti.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Beiðnir til að samþykkja** og velja svo viðeigandi tengil.
2. Velja eina eða fleiri línur fyrir færslu eða færslur sem á að samþykkja eða hafna.
3. Valið er **Samþykkja**, **Hafna**, eða **Framselja** aðgerðir.

Þegar færsla hefur verið samþykkt eða henni hafnað breytist samþykktarstaða í reitnum **Staða** í **Samþykkt** eða **Hafnað**.

Ef samþykkjendastigveldi er til staðar mun færslustaða vera **Bíður samþykktar** þar til allir samþykkjendur hafa samþykkt færsluna. Þá mun staða færslunnar breytast í **Losað**.

Á sama tíma breytist samþykktarstaða úr **Stofnað** í **opið** um leið og samþykktarbeiðni fyrir færsla er stofnuð. Ef beiðni er hafnað berytist samþykktarstaða í **Hafnað**. Staðan er áfram **opið** eða **Hafnað** þar til allir samþykkjendur hafa samþykki beiðnina.

## <a name="to-delegate-requests-for-approval"></a>Úthluta beiðnum um samþykki
Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Til að koma í veg fyrir að skjöl safnist upp með öðru móti stífla verkflæði getur sá sem bað um samþykktina eða samþykkjandinn úthlutað samþykktarbeiðni til staðgengilssamþykkjanda. Staðgengil getur annað hvort verið tilgreindur staðgengill, beinn samþykkjandi eða stjórnandi samþykkis, í þeirri forgangsröð. Þessi aðgerð er yfirleitt notuð ef samþykkjandi er ekki við og getur ekki samþykkt beiðnir fyrir lokadaginn.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Beiðnir til að samþykkja** og velja svo viðeigandi tengil.
2. Velja eina eða fleiri línur fyrir samþykktarbeiðni sem á að úthluta á staðgengil til samþykktar, og veldu síðan aðgerðina **framselja**.

Tilkynning um að samþykkja beiðnina er send til staðgengilssamþykkjanda.

## <a name="to-manage-overdue-approval-requests"></a>Til að stjórna samþykktarbeiðnum sem eru komnar fram yfir á tíma
Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Með reglulegu millibili kann að þurfa að minna notendur samþykktarverkflæðis á beiðnir sem eru fallnar á tíma og sem þeir þurfa að bregðast við. Virknin **Senda samþykkistilkynningar sem komnar eru fram yfir á tíma** er notuð fyrir þetta.

Aðgerðin **Senda samþykkistilkynningar sem komnar eru fram yfir á tíma** kannar allar opnar samþykktar færslur sem eru fallnar á tíma. Allir samþykkjendur með a.m.k. eina samþykkt fram yfir á tíma fá tilkynningu með lista yfir þær samþykktarfærslur sem fallnar eru á tíma. Afrit af tilkynningu er sent til samþykkjenda þeirra og allra sendenda samþykkta sem fallnar eru á tíma. Þetta er gagnlegt ef nauðsynlegt er að framselja samþykktarfærslu sem fallin er á tíma til staðgengils.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Samþykktarbeiðnir komnar fram yfir á tíma** og velja svo viðeigandi tengil.
2. Í **Samþykktarbeiðnir komin fram yfir á tíma** glugganum er valið á **Samþykktarbeiðnir komin fram yfir á tíma Tilkynningar** aðgerð.

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)    
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

