---
title: Samþykkja eða hafna skjölum í verkflæði| Microsoft Docs
description: Fara fram á, hafna eða framselja samþykkt á, til dæmis, innkaupa- eða söluskjali, sem hluta af verkflæði.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 09/28/2021
ms.author: edupont
ms.openlocfilehash: a4dcb5c9f12190a662c4f45bbadcfdddee70fa7f
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129822"
---
# <a name="use-approval-workflows"></a>Nota Samþykktarverkflæði

Þegar færsla, svo sem innkaupaskjal eða viðskiptamannaspjald sem stofnað hefur verið þarfnast samþykktar aðila innan fyrirtækisins er send samþykktarbeiðni sem hluti af verkflæði. Beiðnin um samþykki færslu verður send til viðeigandi samþykkjanda á grundvelli þess hvernig verkflæðið hefur verið sett upp.

Setja upp samþykktarverkflæði á síðunni **Verkflæði**. Einnig verður að setja upp samþykkisnotendur, þar á meðal viðeigandi mörk upphæða, á síðunni **Uppsetning samþykkisnotanda**. Nánari upplýsingar er að finna í [Uppsetning Verkflæði](across-set-up-workflows.md).  

Auk samþykktarverkfallverkða sem lýst er í þessari grein er hægt að framkvæma ýmis önnur verkflæðiverk. Sjá [Use verkflæði](across-use-workflows.md) fyrir frekari upplýsingar.

Kjarna samþykkisverkflæði fyrir innkaupaskjöl, söluskjöl, greiðslubækur, viðskiptamannaspjöld og birgðaspjöldum eru tilbúin til að byrja sem leiðarvísir. Nánari upplýsingar er að finna á [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).

## <a name="to-request-approval-of-a-record"></a>Til að biðja um samþykki færslu

Eftirfarandi verkið er framkvæmt af samþykktarnotanda.

1. Á síðunni sem táknar færsluna er valið **Senda samþykktarbeiðni** aðgerðin.
2. Til að sjá allar samþykktarbeiðnir þínar skal velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). táknið, færa inn **Samþykktarbeiðnifærslur** og velja síðan viðkomandi tengil.  

Staða samþykktarfærslunnar er uppfærð úr **Stofnað** í **Opið**. Staða færslunnar, til dæmis innkaupareikningur, er uppfærður úr **opin** í **Bið eftir samþykkt** og enn er læst fyrir vinnslu þar til allir samþykkjendur hafa samþykkt færsluna.

Þegar allir nauðsynlegir samþykkjendur hafa samþykkt færsluna breytist staðan í **Útgefin**. Þá er hægt að halda áfram verkefni með færsluna.

## <a name="to-cancel-requests-for-approval"></a>Hætt við beiðnir um samþykki

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Vera kann að viðskiptavinur vilji breyta pöntun eftir að hún hefur verið lögð fram til samþykktar. Í þessu tilfelli má hætta við samþykktarferlið og gera nauðsynlegar breytingar á pöntuninni áður en beðið er um samþykki aftur.

- Á síðunni sem sýnir færsluna er valið **Hætta við samþykktarbeiðni** aðgerðin.

Þegar hætt hefur verið við samþykktarbeiðnina uppfærist staðan á samþykktarfærslunni í **Hætt við**. Staða færslunnar er uppfærð úr **Bíður samþykktar** í **Opið**. Samþykktarferlið getur þá hafist á ný.

## <a name="to-approve-or-reject-requests-for-approval"></a>Samþykkja eða hafna samþykktum

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Hægt er að vinna samþykktarbeiðnum á síðunni **Beiðnir til að samþykkja** , til dæmis til að samþykkja margar beiðnum í einu. Einnig er hægt er að vinna hvern beiðni á tengdar færslu, eins og í **Innkaupareikningur** síðunni , með því að velja tengillinn í tilkynningin sem þú tekur á móti.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Beiðnir til að samþykkja** og velja síðan viðkomandi tengil.
2. Velja eina eða fleiri línur fyrir færslu eða færslur sem á að samþykkja eða hafna.
3. Valið er **Samþykkja**, **Hafna**, eða **Framselja** aðgerðir.

Þegar færsla hefur verið samþykkt eða henni hafnað breytist samþykktarstaða í reitnum **Staða** í **Samþykkt** eða **Hafnað**.

Ef samþykkjendastigveldi er til staðar mun færslustaða vera **Bíður samþykktar** þar til allir samþykkjendur hafa samþykkt færsluna. Þá mun staða færslunnar breytast í **Losað**.

Á sama tíma breytist samþykktarstaða úr **Stofnað** í **opið** um leið og samþykktarbeiðni fyrir færsla er stofnuð. Ef beiðni er hafnað berytist samþykktarstaða í **Hafnað**. Staðan er áfram **opið** eða **Hafnað** þar til allir samþykkjendur hafa samþykki beiðnina.

## <a name="to-delegate-requests-for-approval"></a>Úthluta beiðnum um samþykki

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Til að koma í veg fyrir að skjöl safnist upp með öðru móti stífla verkflæði getur sá sem bað um samþykktina eða samþykkjandinn úthlutað samþykktarbeiðni til staðgengilssamþykkjanda. Staðgengil getur annað hvort verið tilgreindur staðgengill, beinn samþykkjandi eða stjórnandi samþykkis, í þeirri forgangsröð. Þessi aðgerð er vanalega notuð ef samþykkjandi er ekki tiltæk eða getur ekki samþykkt beiðnir fyrir gjalddaga.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Beiðnir til að samþykkja** og velja síðan viðkomandi tengil.
2. Velja eina eða fleiri línur fyrir samþykktarbeiðni sem á að úthluta á staðgengil til samþykktar, og veldu síðan aðgerðina **framselja**.

Tilkynning um að samþykkja beiðnina er send til staðgengilssamþykkjanda.

## <a name="to-manage-overdue-approval-requests"></a>Til að stjórna samþykktarbeiðnum sem eru komnar fram yfir á tíma

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Með reglulegu millibili kann að þurfa að minna notendur samþykktarverkflæðis á beiðnir sem eru fallnar á tíma og sem þeir þurfa að bregðast við. Aðgerðin senda samþykkt Áfallnar tilkynningar **er notuð** til að minna notendur á.

Aðgerðin **Senda samþykkistilkynningar sem komnar eru fram yfir á tíma** kannar allar opnar samþykktar færslur sem eru fallnar á tíma. Allir samþykkjendur með a.m.k. eina samþykkt fram yfir á tíma fá tilkynningu með lista yfir þær samþykktarfærslur sem fallnar eru á tíma. Afrit af tilkynningu er sent til samþykkjenda þeirra og allra sendenda samþykkta sem fallnar eru á tíma. Þessi Síðasta skref hjálpar til ef samþykkja þarf samþykktarfærslu vanskila í staðgengilsvara.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Samþykktarbeiðnir sem eru fallnar á tíma** og velja síðan viðkomandi tengil.
2. Á síðunni **Samþykktarbeiðnir komin fram yfir á tíma** er valið á **Samþykktarbeiðnir komin fram yfir á tíma Tilkynningar** aðgerð.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/use-approval-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Sala](sales-manage-sales.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]