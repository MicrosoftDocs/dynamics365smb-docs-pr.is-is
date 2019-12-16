---
title: Úthluta sérstöku skjalaútliti til viðskiptavina eða lánardrottna| Microsoft-skjöl
description: Þegar sérsniðið skýrsluútlit er skilgreint er hægt að velja það af úr spjöldum viðskiptamanna og lánardrottna til að tilgreina að valið útlit á að nota fyrir skjöl sem þú býrð til fyrir viðskiptamanninn eða lánardrottinn.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: 23c4573c3121a660b8263c3bc9bb2c6ac8b1d331
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809400"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna
Þegar sérsniðið skýrsluútlit er skilgreint er hægt að velja það af úr spjöldum viðskiptamanna og lánardrottna til að tilgreina hvaða útlit á að nota fyrir mismunandi tegundir skjala sem þú býrð til fyrir viðskiptamanninn eða lánardrottinn. Gildið í reitnum **Notkun** skilgreinir fyrir hvaða ferli skjalaútlitið verður notað, eins og **Áminning**, **Afhending** og **Staðfesting**.

Auk þess að setja upp hvaða útlit á að nota fyrir hvaða skjal er hægt að spara tíma þegar skjöl eru send til mismunandi viðskiptamanna eða tengiliði lánardrottins með því að setja upp sérstök netföng fyrir tiltekna aðila sem nota á með sérstökum skjölum. Til dæmis verða yfirlit viðskiptamanns sendar til tengiliða í bókhaldi, sölupantanir til innkaupaaðila viðskiptavina og innkaupapantanir til sölumanna eða bókahaldara lánardrottins.

Þegar skjalaútlit er skilgreint fyrir viðskiptamann eða lánardrottin er einnig hægt að tilgreina netfang tengiliðar sem verður að fá skjalið. Þú getur gert þetta á fljótlegan hátt með aðgerðinni **Velja netfang úr tengiliðum**, sem afmarkar sjálfkrafa tengiliðanetföngin fyrir viðskiptamanninn eða lánardrottinn.

Áður en hægt er að skilgreina hvaða skjalaútlit á að nota fyrir hvaða ferli, og til hvaða tengiliðar á að senda skjalið, verður að hlaða öllum tiltækum skýrslum (skjölum) af síðunni **Skýrsluval** . Þú getur gert þetta á fljótlegan hátt með aðgerðinni **Afrita úr skýrsluvali**.

Eftirfarandi sýnir hvernig skilgreina á útlit söluskjals af viðskiptamannaspjaldi. Skrefin eru svipuð fyrir útlit innkaupaskjala af lánardrottnaspjaldi.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Til að virkja öll tiltæk söluskjöl fyrir viðskiptamann
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Opnaðu spjald viðskiptamannsins sem þú vilt skilgreina útlit skjals fyrir í hverju viðskiptaferli.
3. Á síðunni **Viðskiptamannaspjald** skal velja aðgerðina **Útlit fylgiskjals**.
4. Á síðunni **Útlit fylgiskjals** skal velja aðgerðina **Afrita úr skýrsluvali**.

Síðan **Útlit fylgiskjals** fyrir viðkomandi viðskiptamann er fyllt með öllu útliti skýrslu fyrir sölur sem eru til staðar í kerfinu. Nánari upplýsingar um stofnun er að finna í [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md).

Nú er hægt að halda áfram að stilla listann með sérsniðnum skýrsluútlitum eða netföngum fyrir tengiliðina sem senda verður skjölin til.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Til að velja sérsniðið skýrsluútlit sem á að nota fyrir útlit söluskjals
Ef eitt eða fleiri af skýrsluútlit sem eru skilgreind á síðunni **Útlit fylgiskjals** fyrir viðskiptamanninn eru ekki með sérsniðið skýrsluútlit skilgreint er hægt að gera það á fljótlegan hátt.

1. Á síðunni **Útlit fylgiskjals**, á línunni fyrir skýrsluútlit sem á að nota skal nota sérsniðið útlit fyrir skal velja reitinn **Lýsing á sérstilltu útliti**. Reiturinn er fylltur út ef útlit viðskiptavinar er þegar valið en annars auður.
2. Á síðunni **Sérsniðið skýrsluútlit** skal velja sérsniðna skýrsluútlitið sem á að nota fyrir gerð söluskjalsins. Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Til að setja upp hvaða tengiliður fær þetta skjalaútlit fyrir viðskiptavin
Þú getur sparað tíma þegar skjöl eru send til annarra viðskiptamanna eða tengiliða lánardrottins með því að tilgreina netföng tengiliða á mismunandi línum á síðunni **Útlit fylgiskjals** . Til dæmis er hægt að senda yfirlit viðskiptamanns til tengiliða í bókhaldi, sölupantanir til innkaupaaðila viðskiptavina og innkaupapantanir til sölumanna eða bókahaldara lánardrottins.

1. Á síðunni **Útlit fylgiskjals**, á línunni fyrir skýrsluútlit sem á að senda á tiltekinn tengilið fyrir viðskiptamanninn skal velja aðgerðina **Velja netfang úr tengiliðum**.
2. Á síðunni **Tengiliðir** skal velja línuna fyrir tengiliðinn og svo hnappinn **Í lagi**.

Netfang tengiliðarins er nú sett inn í línu skjalauppsetningar þannig að söluskjalið sem um ræðir, til dæmis áminningar, er alltaf sent til þess tengiliðar í fyrirtæki viðskiptavinarins.

## <a name="see-also"></a>Sjá einnig  
[Uppfæra sérsniðið skýrsluútlit](ui-update-report-layouts.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
