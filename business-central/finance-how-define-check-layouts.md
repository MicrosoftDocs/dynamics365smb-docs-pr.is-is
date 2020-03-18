---
title: Tiltaka útlit ávísunar| Microsoft Docs
description: Þú getur hannað og prentað þínar ávísanir á mismunandi sniði til að vera í samræmi við staðla.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 02/20/2020
ms.author: edupont
ms.openlocfilehash: df141f15eda20b1c3ce17e12e726f79a20532915
ms.sourcegitcommit: 35552b250b37c97772129d1cb9fd9e2537c83824
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2020
ms.locfileid: "3097745"
---
# <a name="select-a-check-layout"></a>Velja útlit ávísunar
Hægt er að hanna tékka til þess að uppfylla staðla sem staðaryfirvöld setja. Hægt er að prenta tékkamyndir á Enska, frönsku eða Spænsku.

Tékkar eru hannaðir til að vera prentaðir bæði í Bandrískum og kanadískum tékkamyndsniðum annað á sniðinu tékki-svunta-tékki  eða á sniðinu svunta-svunta-tékki.

## <a name="to-select-a-check-layout"></a>Útlit ávísunar valið
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bankareikningur skýrsluvals** og veldu síðan tengda tengilinn.
2. Á síðunni **Skýrsluval - Bankareikningur** í reitnum **Notkun** skal velja **Reikningur**.
3. Eitt af eftirfarandi skýrslukennum er valið:

| Kenni skýrslu | Skýrsluheiti | Description |
| --- | --- | --- |
| 1401 |Tékki |Þetta er sjálfgefin skýrsla. |
| 10411 |Tékki (Svunta/Svunta/tékki) |þessari skýrslu er hannaðar til að prenta tékka á sniðinu svunta/svunta/tékki. |
| 10412 |Tékki (Svunta/tékki/svunta) |Þessari skýrslu er hannaðar til að prenta tékka á sniðinu svunta/tékki/svunta. |
| 10413 |Þrjár athuganir á hverri síðu |Þessi skýrsla er hönnuð til að prenta þrjá tékka á hverri síðu. |

Þegar settar hafa verið upp útlit tékka er hægt að prenta tékka af síðunni **greiðslubók** . Nánari upplýsingar eru í [Vinna með tékka](payables-how-work-checks.md).

Til að breyta einum af þessum sjálfgefnu útlitum ávísunar skal annaðhvort nota Word- eða RDLC-samþættingu. Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).

## <a name="using-micr-and-security-fonts"></a>Nota MICR og öryggisletur
Netútgáfan af [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur foruppsettar leturgerðir á netþjónum sem hægt er að nota þegar útlit ávísana er skilgreint. Eftirfarandi lýsir því hvaða leturgerðir eru í boði og inniheldur tengla á ítarlegar upplýsingar þriðju aðila í leturgerðum.

> [!Important]
> MICR og öryggisleturgerðir ávísana í Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] eru leyfisveitt í leturgerðarpakka frá IDAutomation.com, Inc. Aðeins má nota þessar vörur sem hluta af og í tengslum við Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].

Í uppfærslu 15.3 og nýrri eru Magnetic Ink Character Recognition (MICR) leturgerðir uppsettar og tilbúnar til notkunar. Bæði E-13B og CMC-7 staðallinn eru studdir. Auk MICR-leturgerða eru sérstakar öryggisleturgerðir í boði til að búa til texta, heiti, upphæðir og gjaldmiðilstáknin dollara, evrur, pund, og Yen, sem erfitt er að breyta þegar búið er að prenta ávísunina.

> [!NOTE]
> Af öryggis-og lagaástæðum er ekki hægt að hlaða upp sérstilltum leturgerðum í [!INCLUDE[d365fin](includes/d365fin_md.md)] umhverfinu.

### <a name="micr-e-13b-specifications"></a>MICR E-13B lýsingar
Eftirfarandi er samantekt skilgreininga fyrir MICR E-13B leturgerðir sem kunna að vera gagnlegar þegar leturgerðir eru kvarðaðar fyrir ávísunarútliti með tilteknum MICR-prenturum.

![MICR E-13B lýsingar](media/font_MICR_E-13B_Specifications.png "MICR E-13B lýsingar")

Hægt er að finna alla lýsinguna á leturgerðum MICR E-13B í fylgiskjölum birgis hér: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>MICR CMC-7 lýsingar
Eftirfarandi CMC-7 letur er tiltækt á [!INCLUDE[d365fin](includes/d365fin_md.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
-   IDAutomationCMC7n40

Eftirfarandi er samantekt skilgreininga fyrir MICR CMC-7 leturgerðir sem kunna að vera gagnlegar þegar leturgerðir eru kvarðaðar fyrir ávísunarútliti með tilteknum MICR-prenturum.

![MICR CMC-7 lýsingar](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 lýsingar")

Hægt er að finna alla lýsinguna á leturgerðum MICR CMC-7 í fylgiskjölum birgis hér: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Lýsingar á öruggu letri
Eftirfarandi er samantekt skilgreininga fyrir öryggisleturgerðir ávísana sem kunna að vera gagnlegar þegar leturgerðir eru kvarðaðar fyrir ávísunarútliti með tilteknum MICR-prenturum.

![Skoða lýsingar á öryggisletri](media/font_check-security-font_Specifications.png "Skoða lýsingar á öryggisletri")

Hægt er að finna alla lýsinguna á öryggisleturgerðum ávísana í fylgiskjölum birgis hér: (https://www.idautomation.com/security-fonts/).

Leturgerðir í öðrum tilgangi má einnig finna í [!INCLUDE[prodshort](includes/prodshort.md)]. Frekari upplýsingar er að finna á [Leturgerðir í boði](ui-fonts.md)

## <a name="see-also"></a>Sjá einnig
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Leturgerðir í Business Central](ui-fonts.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)   
[Að klára Ferli í lok tímabila](year-how-complete-period-end-processes.md)  
[Unnið með [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)
