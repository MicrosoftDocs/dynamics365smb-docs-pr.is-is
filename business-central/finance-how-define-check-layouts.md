---
title: Tiltaka útlit ávísunar
description: Þú getur hannað og prentað þínar ávísanir á mismunandi sniði til að vera í samræmi við staðla sem yfirvöld á staðnum setja.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.search.form: 374, 404
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4278cb474440e8746bcc423c3dd10dbc209fdb9a
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971666"
---
# <a name="select-a-check-layout"></a>Velja útlit ávísunar

Hægt er að hanna tékka til þess að uppfylla staðla sem staðaryfirvöld setja. Hægt er að prenta tékkamyndir á Enska, frönsku eða Spænsku.

Tékkar eru hannaðir til að vera prentaðir bæði í Bandrískum og kanadískum tékkamyndsniðum annað á sniðinu tékki-svunta-tékki  eða á sniðinu svunta-svunta-tékki.

## <a name="to-select-a-check-layout"></a>Útlit ávísunar valið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningur skýrsluvals** og velja síðan viðkomandi tengil.
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

Netútgáfan af [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur foruppsettar leturgerðir á netþjónum sem hægt er að nota þegar útlit ávísana er skilgreint. Eftirfarandi lýsir því hvaða leturgerðir eru í boði og inniheldur tengla á ítarlegar upplýsingar þriðju aðila í leturgerðum.

> [!Important]
> MICR og öryggisleturgerðir ávísana í Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] eru leyfisveitt í leturgerðarpakka frá IDAutomation.com, Inc. Aðeins má nota þessar vörur sem hluta af og í tengslum við Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].

Í uppfærslu 15.3 og nýrri eru Magnetic Ink Character Recognition (MICR) leturgerðir uppsettar og tilbúnar til notkunar. Bæði E-13B og CMC-7 staðallinn eru studdir. Auk MICR-leturgerða eru sérstakar öryggisleturgerðir í boði til að búa til texta, heiti, upphæðir og gjaldmiðilstáknin dollara, evrur, pund, og Yen, sem erfitt er að breyta þegar búið er að prenta ávísunina.

> [!NOTE]
> Af öryggis-og lagaástæðum er ekki hægt að hlaða upp sérstilltum leturgerðum í [!INCLUDE[prod_short](includes/prod_short.md)] umhverfinu.

### <a name="micr-e-13b-specifications"></a>MICR E-13B lýsingar

Eftirfarandi er samantekt skilgreininga fyrir MICR E-13B leturgerðir sem kunna að vera gagnlegar þegar leturgerðir eru kvarðaðar fyrir ávísunarútliti með tilteknum MICR-prenturum.

![MICR E-13B lýsingar.](media/font_MICR_E-13B_Specifications.png "MICR E-13B lýsingar")

### <a name="delimiter-characters"></a>Skiltákn

![Skiltákn.](media/font-micr-letters.png "Skiltákn")

Hægt er að finna alla lýsinguna á leturgerðum MICR E-13B í fylgiskjölum birgis hér: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>MICR CMC-7 lýsingar

Eftirfarandi CMC-7 letur er tiltækt á [!INCLUDE[prod_short](includes/prod_short.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
- IDAutomationCMC7n40

Eftirfarandi er samantekt skilgreininga fyrir MICR CMC-7 leturgerðir sem kunna að vera gagnlegar þegar leturgerðir eru kvarðaðar fyrir ávísunarútliti með tilteknum MICR-prenturum.

![MICR CMC-7 lýsingar.](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 lýsingar")

### <a name="delimiter-characters"></a>Skiltákn

![Skiltákn fyrir CMC-7.](media/font-cmc7-letters.png "Skiltákn fyrir CMC-7")

Hægt er að finna alla lýsinguna á leturgerðum MICR CMC-7 í fylgiskjölum birgis hér: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Lýsingar á öruggu letri

Eftirfarandi er samantekt skilgreininga fyrir öryggisleturgerðir ávísana sem kunna að vera gagnlegar þegar leturgerðir eru kvarðaðar fyrir ávísunarútliti með tilteknum MICR-prenturum.

![Skoða lýsingar á öryggisletri.](media/font_check-security-font_Specifications.png "Skoða lýsingar á öryggisletri")

Hægt er að finna alla lýsinguna á öryggisleturgerðum ávísana í fylgiskjölum birgis hér: (https://www.idautomation.com/security-fonts/).

Leturgerðir í öðrum tilgangi má einnig finna í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna á [Leturgerðir í boði](ui-fonts.md)

## <a name="see-also"></a>Sjá einnig

[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Leturgerðir í Business Central](ui-fonts.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)   
[Að klára Ferli í lok tímabila](year-how-complete-period-end-processes.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]