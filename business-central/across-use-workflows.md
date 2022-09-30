---
title: Notkun Samþykktarverkflæða
description: Hægt er að setja upp og nota verkflæði til að tengja verk-ferla eins og sjálfvirka bókun eða biðja um og veita samþykki fyrir nýjum færslum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 1500, 1501, 1503, 1504, 1505
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 4b4a46071173c7371a306570227be5fffebd36d6
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585784"
---
# <a name="use-approval-workflows"></a>Nota Samþykktarverkflæði

Verkflæði er röð verka sem ræst er af aðgerð, skilyrði eða reglu. Verkflæði er vanalega útfært til að samþætta viðskiptagrunn við stofnun, eins og aðskilnað á skyldum, samvinnsluferlum eða beita bestu venjum.

Verkflæðinu getur verið ætlað að skapa beiðnir um samþykki á færslu breytinga á færslusvæði við að halda gömlum gögnum Ef beiðnin er ekki samþykkt. Nýja gildið verður ekki útfært fyrr en Síðasta beiðni er samþykkt.

Viðskiptagrunninn gæti verið samþykkur um:

- Ný aðalgögn eins og Fjárhagur (fjárhags-) reikningar, viðskiptamenn, Lánardrottnar eða vörur.
- Breytist í svæði í færslum sem til eru með skynsamlegum upplýsingum, eins og **bankareikning** lánardrottins, eða **lánamark viðskiptamanns**.
- Breytingar á reitum í færslum sem til eru sem innihalda viðskiptaupplýsingar, svo sem **söluverð vöru**.
- Nýrra notenda eða breytinga á notendaleyfi.
- Innkaupaskjölum.
- Söluskjöl.
- Utanaðkomandi skjöl.
- Fjármagna færslubækur áður en bókað er.

Eftirfarandi mynd er dæmi um verkflæði með raðsamþykkt af notanda. Með því að setja verkflæðið af stað verður samþykktarbeiðni búin til fyrir fyrsta samþykkjandann.  

![Mynd af verkflæði með samþykktarröð.](media/Workflows/approval-flow.png)

Þú sérð á skýringarmynd hér fyrir ofan hvernig beiðni þarf að vera samþykkt af fyrsta samþykkjanda áður en hún er send á þann næsta. Ef beiðnin er ekki samþykkt af fyrsta samþykkjanda, skal beiðnin aldrei fara á næsta.

Leiðin sem farin er frá upphaflegri ræsingu verkflæðisins getur verið breytileg eftir því hvers eðlis samþykktin er.  

Eftirfarandi mynd sýnir samhliða samþykkt notanda. Samhliða samþykkt merkir samþykkisbeiðnin send til allra samþykkjendur samtímis.  

![Mynd af verkflæði með samhliða samþykki.](media/Workflows/approval-flow-2.png)

Verkflæðinu er hins vegar ekki lokið fyrr en allar beiðnir hafa verið samþykktar, eins og sýnt er á eftirfarandi mynd:  

![Mynd af höfnuðu verkflæði með samhliða samþykki.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Fyrir verkflæði með marga samþykkjendur verður að samþykkja hvert skref áður en verkflæðið getur farið fram á næsta viðburði. Samþykkið frá bara einum samþykkjanda flytur ekki verkflæðið áfram.

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Það er líka hægt að stofna sama verkflæði oftar en einu sinni. Hægt er að kveikja á hverju verkflæði með mismunandi síum. Þetta er gagnlegt ef samþykkja þarf samþykktarbeiðni fyrir eina deild með einum samþykkjanda, en annar samþykkjandans verður að samþykkja hana. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Áður en hægt er að byrja að nota verkflæði þarf að setja upp verkflæðisnotendur, Stofna verkflæði (hugsanlega fyrir sérsnið eftir kóta) og tilgreina hvernig notendur taka á móti tilkynningum. Frekari upplýsingar um [uppsetningu verkflæðis](across-set-up-workflows.md).

> [!NOTE]  
> Dæmigerðar verkflæðisskref fela í sér að notendur biðja um samþykki á verkum og samþykkjendur samþykkja eða hafna samþykktarbeiðnum. Þess vegna eru mörg efnisatriði um það hvernig verkflæði er notað vísa í samþykki.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.  

| **Til að** | **Sjá** |
|--|--|
| Setja upp samþykktarverkflæði sem á að byrja þegar fyrsti tilfærslupunkturinn á sér stað. | [Virkja samþykktarverkflæði](across-how-to-enable-workflows.md) |
| Beiðni um samþykki á verki; sem samþykkjandi, samþykkja, hafna eða ráðstafa samþykktum sínum; og senda eða skoða samþykktar tilkynningar. | [Hvernig nota á samþykktarverkflæði](across-how-use-approval-workflows.md) |
| Stofna verkflæðisskref sem takmarka ákveðna færslugerð úr notkun áður en tiltekinn atburður á sér stað, til dæmis, samþykki fyrir færslunni. | [Takmarka og heimila notkun á færslu](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Skoða tilvik verkflæðisskrefa með **stöðuna Lokið**. | [Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md) |
| Eyða samþykktarverkflæði sem ekki er lengur notað. | [Eyða samþykktarverkflæði](across-how-to-delete-workflows.md) |

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Uppsetning Samþykktarverkflæðis](across-set-up-workflows.md)  
[Verkflæði](across-workflow.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
