---
title: Samþykkja eða hafna skjölum í verkflæðum
description: Fara fram á, hafna eða framselja samþykkt á, til dæmis, innkaupa- eða söluskjali, sem hluta af verkflæði.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.search.form: 654, 662, 1500,
ms.date: 09/12/2022
ms.author: edupont
ms.openlocfilehash: f1d7ef11d97d1643bb52085c13696b8831c169b6
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585541"
---
# <a name="how-to-use-approval-workflows"></a>Hvernig nota á samþykktarverkflæði

Þegar færsla, svo sem innkaupaskjal eða viðskiptamannaspjald sem stofnað hefur verið þarfnast samþykktar aðila innan fyrirtækisins er send samþykktarbeiðni sem hluti af verkflæði. Beiðnin um samþykki færslu verður send til viðeigandi samþykkjanda á grundvelli þess hvernig verkflæðið hefur verið sett upp.

Setja upp samþykktarverkflæði á síðunni **Verkflæði**. Einnig þarf að setja upp samþykktarnotendur, þar á meðal viðeigandi upphæðarmörk á **uppsetningarsíðu** samþykktarnotanda. Frekari upplýsingar um [uppsetningu verkflæðisins eru settar upp](across-set-up-workflows.md).  

Auk samþykktarverkfallverkinna sem lýst er í þessari grein er hægt að framkvæma ýmis önnur verkflæðiverk. Frekari upplýsingar um [samþykktarverkflæði nota](across-use-workflows.md).

Kjarna samþykkisverkflæði fyrir innkaupaskjöl, söluskjöl, greiðslubækur, viðskiptamannaspjöld og birgðaspjöldum eru tilbúin til að byrja sem leiðarvísir. Lærðu meira á [að undirbúa þig fyrir viðskipti](ui-get-ready-business.md).

## <a name="request-a-record-approval"></a>Beiðni um skráningu samþykkis

Eftirfarandi verkið er framkvæmt af samþykktarnotanda.

1. Á síðunni sem táknar færsluna er valið **Senda samþykktarbeiðni** aðgerðin.
2. Til að sjá allar samþykktarbeiðnir þínar skal velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Táknið, færa inn **Samþykktarbeiðafærslur** og velja síðan tengda tengilinn.  

Staða samþykktarfærslunnar er uppfærð úr **Stofnað** í **Opið**. Staða færslunnar, eins og innkaupareikningur, er uppfærð frá **opnu** til **samþykkis** í bið og enn er læst fyrir vinnslu þar til allir samþykkjendur hafa samþykkt færsluna.

Þegar allir nauðsynlegir samþykkjendur hafa samþykkt færsluna breytist staðan í **Útgefin**. Síðan er hægt að halda áfram að vinna með skráninguna.

## <a name="cancel-approval-requests"></a>Hætta við samþykktarbeiðnir

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Viðskiptavinur getur óskað eftir að breyta pöntun eftir að hún hefur verið send til samþykktar. Í þessu tilfelli er hægt að hætta við samþykktarferlið, gera nauðsynlegar breytingar á pöntuninni og biðja um samþykki á ný.

- Á síðunni sem birtir færsluna skal velja aðgerðina hætta á **samþykki**.

Þegar hætt hefur verið við samþykktarbeiðnina uppfærist staðan á samþykktarfærslunni í **Hætt við**. Staða færslunnar er uppfærð úr **Bíður samþykktar** í **Opið**. Á þessu stigi getur samþykktarferlið hafist að nýju.

## <a name="approve-or-reject-approval-requests"></a>Samþykkja eða hafna samþykkisbeiðnum

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Hægt er að vinna samþykktarbeiðnir á **síðunni beiðnir til samþykktar** og þar með samþykkja margar beiðnir í einu. Einnig er hægt að samþykkja einstakar færslur með því að velja tengilinn í tilkynningunni sem berst.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Beiðnir til að samþykkja** og velja síðan viðkomandi tengil.
2. Veljið eina eða fleiri línur af færslunum sem á að samþykkja eða hafna.
3. Valið er **Samþykkja**, **Hafna**, eða **Framselja** aðgerðir.

Þegar færsla hefur verið samþykkt eða hafnað, breytist samþykktarstaðan í **reitnum Staða** í samþykkt **eða** hafnað **, eftir því sem við á.**

Ef stigveldi samþykkjanda er sett upp er **Staða færslunnar í bið samþykkis** þar til allir umbeðna samþykkjendur hafa samþykkt færsluna. Þá breytist staða færslunnar í **Útgefin**.

Á sama tíma breytist samþykktarstaða úr **Stofnað** í **opið** um leið og samþykktarbeiðni fyrir færsla er stofnuð. Ef beiðni er hafnað berytist samþykktarstaða í **Hafnað**. Staðan er áfram **opið** eða **Hafnað** þar til allir samþykkjendur hafa samþykki beiðnina.

## <a name="delegate-approval-requests"></a>Beiðni um samþykki fulltrúa

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Til að koma í veg fyrir að færslur komi upp eða hindri verkflæðið getur samþykkjandinn og samþykktarstjórnandinn framselt samþykkisbeiðni til staðgengils. Staðgengil getur annað hvort verið tilgreindur staðgengill, beinn samþykkjandi eða stjórnandi samþykkis, í þeirri forgangsröð. Þessi aðgerð er vanalega notuð ef samþykkjandi er ekki tiltæk eða getur ekki samþykkt beiðnir fyrir gjalddaga.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **beiðnir til samþykktar** og veljið síðan tengda tengilinn.
2. Velja skal eina eða fleiri beiðnir samþykktarbeiðna sem á að úthluta til samþykkjanda og velja **síðan** staðgengilsaðgerðina.

Tilkynning um að samþykkja beiðnina er send til staðgengilssamþykkjanda.

## <a name="manage-overdue-approval-requests"></a>Stjórna beiðnum um samþykkt vanskila

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Með reglulegu millibili þarf að minna notendur á samþykktarverkflæði vegna vanskila á samþykktabeiðnum; Aðgerðin senda samþykkt Áfallnar tilkynningar **er notuð** til að gera það.

Tilkynningarnar **sem** eru sendar gjaldfallnar virka ávísanir fyrir allar opnar samþykktabeiðnir sem nú eru fallnar. Hver samþykkjandi með minnst eina gjaldfallna samþykktarfærslu fær tilkynningu með listann yfir allar samþykktarbeiðnir þeirra um Vanskil. Afrit af tilkynningu er sent til samþykkjenda þeirra og allra sendenda samþykkta sem fallnar eru á tíma. Þessi Síðasta skref hjálpar til ef samþykkja þarf samþykktarfærslu vanskila í staðgengilsvara.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Samþykktarbeiðnir sem eru fallnar á tíma** og velja síðan viðkomandi tengil.
2. Á síðunni **Samþykktarbeiðnir komin fram yfir á tíma** er valið á **Samþykktarbeiðnir komin fram yfir á tíma Tilkynningar** aðgerð.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/use-approval-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Nota samþykktarverkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  
[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Sala](sales-manage-sales.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
