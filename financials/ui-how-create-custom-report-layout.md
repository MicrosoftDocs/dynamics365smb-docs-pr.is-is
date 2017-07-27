---
title: "Stofna sérsniðið útlit fyrir skýrslur og skjöl | Microsoft Docs"
description: "Kynntu þér hvernig skal stofna þitt eigið útlitssnið til að sérsníða útlit skýrslu þegar hún er skoðuð, prentuð eða vistuð."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 551e838c2896470f9ee620f4ca09a6af3377b458
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-a-custom-report-or-document-layout"></a>Hvernig á að: Búa til sérsniðið skýrsluútlit eða skjalaútlit
Sjálfgefið er að skýrsla hafa innbyggt skýrsluútlit, sem getur verið RDLC-skýrsluútlit, Word-skýrsluútlit eða bæði. Ekki er hægt að breyta innbyggðu útliti. Þú getur einnig búið til þitt eigið sérsniðið útlit sem gerir þér kleift að breyta útliti skýrslu þegar hún er skoðuð, prentuð eða vistuð. Hægt er að búa til mörg sérsniðin skýrsluútlit fyrir sömu skýrsluna, og skipta svo á milli útlita fyrir skýrsluna eftir þörfum.

> [!NOTE]  
>   Í [!INCLUDE[d365fin](includes/d365fin_md.md)] táknar hugtakið "skýrsla" einnig utanaðkomandi skjöl, s.s. sölureikninga og pöntunarstaðfestingar sem þú sendir til viðskiptavina sem PDF skjöl.

Til að búa til sérsniðið útlit geturðu búið til afrit af öðru sérsniðið útliti, eða bætt við nýju sérsniðnu útliti, sem í flestum tilfellum er byggt á innbyggða útlitinu. Þegar þú bætir við nýju sérsniðnu útliti geturðu valið að bæta við RDLC-skýrsluútliti, Word-skýrsluútliti eða bæði. Nýja sérsniðna útlitið verður sjálfkrafa byggt á innbyggða útlitinu fyrir skýrsluna ef það er til staðar. Ef ekkert innbyggt útlit fyrir gerðina er til þá er stofnað nýtt autt útlit, sem verður að breyta og hanna frá grunni. Frekari upplýsingar um RDLC- og Word-skýrsluútlit, innbyggð útlit, sérsniðið útlit og fleira eru í [stjórna skýrsluútliti](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Til að búa til sérsniðið útlit
1. Velja skal ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Search for Page or Report icon"), slá inn **Val á útliti skýrslu**, og velja síðan viðeigandi tengil.  
   Valmyndin ** Skýrslusnið val** birtir allar skýrslur sem eru í boði í fyrirtækinu sem er tilgreint í reitnum Fyrirtæki efst í glugganum.
2. Stilltu reitinn **Fyrirtæki** á fyrirtækið sem búa á til skýrsluútliti fyrir.
3. Veldu röðina fyrir skýrsluna sem þú vilt stofna útlitið fyrir, og veldu svo **Sérsniðið útlit**.  
   Glugginn **Sérsniðið skýrsluútlit** birtist og sýnir öll sérsniðin útlit sem eru í boði fyrir völdu skýrsluna.
4. Ef þú vilt búa til afrit af sérsniðnu útliti sem þegar er til velurðu sérsniðið útlitið af listanum og velur svo **Afrita**.  
   Afrit af sérsniðna útlitinu birtist í glugganum **Sérsniðið skýrsluútlit** með orðunum Afrit í reitnum Lýsing.
5. Ef þú vilt bæta við nýju sérsniðnu útliti sem byggir á innbyggðu útliti skaltu gera eftirfarandi:  
   1. Velja **Nýtt**. Glugginn **Setja inn innbyggt útlit fyrir skýrslu** birtist. Reitirnir **Auðkenni** og **Heiti** eru fylltir inn sjálfkrafa.
   2. Til að bæta við sérsniðnu Word-skýrsluútliti fyrir skýrsluna skaltu velja **Setja inn Word-útlit** gátreitinn.
   3. Til að bæta við sérsniðnu RDLC-skýrsluútliti skaltu velja **Setja inn RDLC-útlit** gátreitinn.
   4. Velja hnappinn **Í lagi**.  
      Nýja sérsniðna útlitið birtist í glugganum **Sérsniðið skýrsluútlit**. Ef nýtt útlit byggir á innbyggðu útliti er það með orðin **Afrit af innbyggðu útiliti** í reitnum **Lýsing**. Ef ekkert innbyggt útlit var til staðar fyrir skýrsluna þá er nýja útlitið með orðin **Nýtt útlit** í reitnum **Lýsing**, sem táknar að sérsniðna útlitið er autt.
6. Reiturinn **Heiti fyrirtækis** er sjálfgefið auður, sem táknar að sérsniðið útlit er í boði fyrir skýrsluna í öllum fyrirtækjum. Til að gera sérsniðið útlit aðeins aðgengilegt fyrir tiltekið fyrirtæki, skal velja **Breyta** og stilla síðan reitinn **Heiti fyrirtækis** á það fyrirtæki sem þú vilt.

## <a name="see-also"></a>Sjá einnig
[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Hvernig á að: Breyta hvaða útlit er nú notað í skýrslu](ui-how-change-layout-currently-used-report.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

