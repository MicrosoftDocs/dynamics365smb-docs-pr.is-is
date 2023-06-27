---
title: Samþykkja eða hafna skjölum í verkflæði
description: 'Fara fram á, hafna eða framselja samþykkt á, til dæmis, innkaupa- eða söluskjali, sem hluta af verkflæði.'
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '654, 662, 1500,'
ms.date: 09/12/2022
ms.author: edupont
---
# <a name="how-to-use-approval-workflows" />Hvernig á að nota samþykktarverkflæði

Þegar færsla, svo sem innkaupaskjal eða viðskiptamannaspjald sem stofnað hefur verið þarfnast samþykktar aðila innan fyrirtækisins er send samþykktarbeiðni sem hluti af verkflæði. Beiðnin um samþykki færslu verður send til viðeigandi samþykkjanda á grundvelli þess hvernig verkflæðið hefur verið sett upp.

Setja upp samþykktarverkflæði á síðunni **Verkflæði**. Einnig verður að setja upp samþykkisnotendur, þar á meðal viðeigandi mörk upphæða, á síðunni **Uppsetning samþykkisnotanda**. Frekari upplýsingar má finna á [Setja upp verkflæði samþykktar](across-set-up-workflows.md).  

Í viðbót við samþykktarverkflæði sem lýst er í þessari grein geturðu framkvæmt ýmis önnur verkflæðisverk. Frekari upplýsingar má finna á [Nota Samþykktarverkflæði](across-use-workflows.md).

Kjarna samþykkisverkflæði fyrir innkaupaskjöl, söluskjöl, greiðslubækur, viðskiptamannaspjöld og birgðaspjöldum eru tilbúin til að byrja sem leiðarvísir. Frekari upplýsingar eru í [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).

## <a name="request-a-record-approval" />Biðja um samþykki á færslu

Eftirfarandi verkið er framkvæmt af samþykktarnotanda.

1. Á síðunni sem táknar færsluna er valið **Senda samþykktarbeiðni** aðgerðin.
2. Til að sjá allar samþykktarbeiðnir þínar skal velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). táknið, fara í **Færslur samþykktarbeiðni**, velja síðan viðkomandi tengil.  

Staða samþykktarfærslunnar er uppfærð úr **Stofnað** í **Opið**. Staða færslunnar, til dæmis innkaupareiknings, er uppfærð úr **Opin** í **Bíður samþykkis** og er áfram lokuð fyrir úrvinnslu þar til allir samþykktaraðilar hafa samþykkt færsluna.

Þegar allir nauðsynlegir samþykktaraðilar hafa samþykkt færsluna breytist staðan í **Útgefin**. Þá er hægt að halda áfram að vinna með færsluna.

## <a name="cancel-approval-requests" />Hætta við samþykktarbeiðnir

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Viðskiptamaður kann að vilja breyta pöntun eftir að hún hefur verið lögð fram til samþykktar. Í slíku tilfelli má hætta við samþykktarferlið og gera nauðsynlegar breytingar á pöntuninni og síðan biðja aftur um samþykki.

- Á síðunni sem sýnir færsluna skal velja aðgerðina **Hætta við samþykktarbeiðni**.

Þegar hætt hefur verið við samþykktarbeiðnina uppfærist staðan á samþykktarfærslunni í **Hætt við**. Staða færslunnar er uppfærð úr **Bíður samþykktar** í **Opið**. Nú getur samþykktarferlið hafist að nýju.

## <a name="approve-or-reject-approval-requests" />Samþykkja eða hafna samþykktarbeiðnum

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Hægt er að vinna úr samþykktarbeiðnum á síðunni **Beiðnir til að samþykkja**, þ.m.t. að samþykkja margar beiðnum í einu. Að öðrum kosti er hægt að samþykkja einstakar færslur með því að velja tengilinn í tilkynningunni sem þú færð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Beiðnir til að samþykkja** og velja síðan viðkomandi tengil.
2. Veldu eina eða fleiri línur í færslunni/færslunum sem á að samþykkja eða hafna.
3. Valið er **Samþykkja**, **Hafna**, eða **Framselja** aðgerðir.

Þegar færsla hefur verið samþykkt eða henni hafnað breytist samþykktarstaða í reitnum **Staða** í **Samþykkt** eða **Hafnað**.

Ef stigveldi samþykktaraðila er uppsett er færslustaðan **Bíður samþykktar** þar til allir samþykktaraðilar hafa samþykkt færsluna. Þá mun staða færslunnar breytast í **Útgefið**.

Á sama tíma breytist samþykktarstaða úr **Stofnað** í **opið** um leið og samþykktarbeiðni fyrir færsla er stofnuð. Ef beiðni er hafnað berytist samþykktarstaða í **Hafnað**. Staðan er áfram **opið** eða **Hafnað** þar til allir samþykkjendur hafa samþykki beiðnina.

## <a name="delegate-approval-requests" />Framselja samþykktarbeiðnir

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Til að koma í veg fyrir að færslur safnist upp eða stífla verkflæðið á annan hátt getur samþykktaraðili og samþykktarstjórnandi úthlutað samþykktarbeiðni á staðgengil samþykktaraðila. Staðgengil getur annað hvort verið tilgreindur staðgengill, beinn samþykkjandi eða stjórnandi samþykkis, í þeirri forgangsröð. Þessi aðgerð er yfirleitt notuð ef samþykktaraðili er ekki við eða getur ekki samþykkt beiðnir fyrir lokadaginn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Beiðnir til að samþykkja**, velja síðan viðkomandi tengil.
2. Veldu eina eða fleiri línur fyrir samþykktarbeiðnir sem á að úthluta á staðgengil samþykktaraðila og veldu síðan aðgerðina **Úthluta**.

Tilkynning um að samþykkja beiðnina er send til staðgengilssamþykkjanda.

## <a name="manage-overdue-approval-requests" />Stjórna samþykktarbeiðnum sem eru komnar fram yfir á tíma

Eftirfarandi verkið er framkvæmt af samþykktarnotanda með samþykktarheimildir.

Með reglulegu millibili þarftu að minna notendur samþykktarverkflæðis á samþykktarbeiðnir sem komnar eru fram yfir tímann; þú notar aðgerðina **Senda samþykktartilkynningar sem komnar eru fram yfir tíma** til að gera það.

Aðgerðin **Senda samþykktartilkynningar sem komnar eru fram yfir tíma** kannar allar opnar samþykktar beiðnir sem eru fallnar á tíma. Allir samþykkjendur með a.m.k. eina samþykkt fram yfir á tíma fá tilkynningu með lista yfir þær samþykktarfærslur sem fallnar eru á tíma. Afrit af tilkynningu er sent til samþykkjenda þeirra og allra sendenda samþykkta sem fallnar eru á tíma. Þetta síðasta skref er gagnlegt ef úthluta þarf samþykktarfærslu sem komin er fram yfir tíma á staðgengil.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Samþykktarbeiðnir sem eru fallnar á tíma** og velja síðan viðkomandi tengil.
2. Á síðunni **Samþykktarbeiðnir komin fram yfir á tíma** er valið á **Samþykktarbeiðnir komin fram yfir á tíma Tilkynningar** aðgerð.

## <a name="see-related-microsoft-training" />Sjá tengda [Microsoft þjálfun](/training/modules/use-approval-workflows/)

## <a name="see-also" />Sjá einnig .

[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  
[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Sala](sales-manage-sales.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
