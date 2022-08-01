---
title: Nota verkflæði
description: Hægt er að setja upp og nota verkflæði sem tengja verk viðskiptaferla eins og sjálfvirka bókun eða beiðni og samþykki samþykktar fyrir nýjar færslur.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 4f66b334df678ff27e094858dd0cec44c1bb8e75
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130227"
---
# <a name="use-workflows"></a>Nota verkflæði

Verkflæði er röð verka sem aðgerð, skilyrði eða regla setur af stað. Verkflæði eru yfirleitt innleidd til að samþætta viðskiptagrunn við fyrirtæki, t.d. aðskilnað aðgangsheimilda, sameiningu ferla eða til að auka traust og ábyrgð.  

Verkflæðinu er ætlað að skapa beiðnir um samþykki á nýju gildi en halda gömlu gildi sínu Ef beiðnin er ekki samþykkt. Nýja gildið verður ekki útfært fyrr en Síðasta beiðni er samþykkt.  

Viðskiptagrunnurinn gæti verið samþykki á:

- Nýjum aðalgögnum eins og fjárhagsreikningum, viðskiptavinum, lánardrottnum eða vörum
- Breytingar á reitum í fyrirliggjandi færslum innihalda viðkvæmar upplýsingar á borð við **Bankareikningsnúmer lánardrottins** eða **Lánamark viðskiptavinar**
- Breytingar á reitum í fyrirliggjandi færslum sem innihalda mikilvægar upplýsingar um viðskipti á borð við **Söluverð vöru**
- Nýir notendur eða breytingar á notendaheimildum
- Innkaupaskjöl
- Söluskjöl
- Skjöl á innleið
- Fjármálabækur á undan bókun

Eftirfarandi skýringarmynd sýnir dæmi um verkflæði með samþykktarröð sem notandi setur í gang. Með því að setja verkflæðið af stað verður samþykktarbeiðni búin til fyrir fyrsta samþykkjandann.  

![Mynd af verkflæði með samþykktarröð.](media/Workflows/approval-flow.png)

Í þessu dæmi verður fyrsti samþykktaraðilinn að samþykkja beiðnina áður en beiðnin er send á næsta samþykktaraðilann. Ef beiðnin er ekki samþykkt af fyrsta samþykkjanda, fer beiðnin aldrei til næsta samþykkjanda.  

Leiðin sem farin er frá upphaflegri ræsingu verkflæðisins getur verið breytileg eftir því hvers eðlis samþykktin er.  

Eftirfarandi mynd sýnir samhliða samþykki sem notandi setur af stað. Með því að setja verkflæðið í gang er beiðni um samþykkt send á alla samþykktaraðilana samtímis.  

![Mynd af verkflæði með samhliða samþykki.](media/Workflows/approval-flow-2.png)

Hins vegar er verkfall ekki samþykkt fyrr en allar beiðnir hafa verið samþykktar af samþykkjendum, eins og sést á eftirfarandi mynd:  

![Mynd af höfnuðu verkflæði með samhliða samþykki.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Ekki er hægt að búa til verkflæði með mörgum samþykktaraðilum og ætlast til þess að allt verkflæðið verði samþykkt eftir að fyrsta beiðnin hefur verið samþykkt. Samþykkja þarf allar beiðnir svo að verkflæðið verði samþykkt.

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Það er líka hægt að stofna sama verkflæði oftar en einu sinni. Hægt er að kveikja á hverju verkflæði með mismunandi síum. Þetta er gagnlegt ef samþykkja þarf samþykkisbeiðni í einni deild með einum samþykkjanda, á meðan samþykkisbeiðnir á öðrum deildum verða að vera samþykktar af öðrum samþykkjanda. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Áður en hægt er að byrja að nota verkflæði verður að setja upp notendur verkflæðis, stofna verkflæði, hugsanlega eftir að hafa sérsniðið kóða og tilgreina hvernig notendur fá tilkynningar. Nánari upplýsingar er að finna í [Uppsetning Verkflæði](across-set-up-workflows.md).  

> [!NOTE]  
> Dæmigerð verkflæðisskref eru um notendur sem biðja um samþykki verka og samþykkjendur sem samþykkja eða hafna samþykktarbeiðnum. Því vísa mörg efni um hvernig nota eigi verkflæði til Samþykktir.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Stilla verkflæði á að hefjast þegar fyrsta færslupunktstilvik á sér stað.|[Virkja verkflæði](across-how-to-enable-workflows.md)|  
|Samþykktarbeiðni fyrir verk, sem samþykktaraðili samþykkirðu, hafnarðu eða úthlutar samþykktum, og sendir eða ferð yfir samþykktartilkynningar.|[Nota Samþykktarverkflæði](across-how-use-approval-workflows.md)|  
|Stofna verkflæðisskreft sem takmarka sérstakri færslugerð sé notuð áður en tiltekið tilvik á sér stað, til dæmis að færsla sé samþykkt.|[Takmarka og heimila notkun á færslu](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Skoða skref verkflæðis fyrir stöðuna **lokið**.|[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)|  
|Eyða verkflæði sem þú ert örugglega ekki lengur að nota.|[Eyða verkflæðum](across-how-to-delete-workflows.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Uppsetning verkflæðis](across-set-up-workflows.md)  
[Verkflæði](across-workflow.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]