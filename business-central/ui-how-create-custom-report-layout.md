---
title: Stofna og breyta sérsniðið útlit fyrir skýrslur og skjöl | Microsoft Docs
description: Kynntu þér hvernig skal stofna þitt eigið útlitssnið til að sérsníða útlit skýrslu þegar hún er skoðuð, prentuð eða vistuð.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3d4522a08fe1c313ecf3f7c2f3fb59af62f48d2c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778023"
---
# <a name="create-and-modify-custom-report-layouts"></a>Búa til og breyta sérsniðnum skýrsluútlitum

Sjálfgefið er að skýrsla hafa innbyggt skýrsluútlit, sem getur verið RDLC-skýrsluútlit, Word-skýrsluútlit eða bæði. Ekki er hægt að breyta innbyggðu útliti. Þú getur einnig búið til þitt eigið sérsniðið útlit sem gerir þér kleift að breyta útliti skýrslu þegar hún er skoðuð, prentuð eða vistuð. Hægt er að búa til mörg sérsniðin skýrsluútlit fyrir sömu skýrsluna, og skipta svo á milli útlita fyrir skýrsluna eftir þörfum.

> [!NOTE]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)] táknar hugtakið "skýrsla" einnig utanaðkomandi skjöl, s.s. sölureikninga og pöntunarstaðfestingar sem þú sendir til viðskiptavina sem PDF skjöl.

Til að búa til sérsniðið útlit geturðu búið til afrit af öðru sérsniðið útliti, eða bætt við nýju sérsniðnu útliti, sem í flestum tilfellum er byggt á innbyggða útlitinu. Þegar þú bætir við nýju sérsniðnu útliti geturðu valið að bæta við RDLC-skýrsluútliti, Word-skýrsluútliti eða bæði. Nýja sérsniðna útlitið verður sjálfkrafa byggt á innbyggða útlitinu fyrir skýrsluna ef það er til staðar. Ef ekkert innbyggt útlit fyrir gerðina er til þá er stofnað nýtt autt útlit, sem verður að breyta og hanna frá grunni. Frekari upplýsingar um RDLC- og Word-skýrsluútlit, innbyggð útlit, sérsniðið útlit og fleira eru í [stjórna skýrsluútliti](ui-manage-report-layouts.md).  

> [!TIP]
> Notaðu reikningsáætlanir til að fá innsýn í fjárhagsupplýsingar sem eru geymdar í bókhaldslyklum. Frekari upplýsingar er að finna í [Undirbúa Financial Reporting með fjárhagsskemu og lyklategundum](bi-how-work-account-schedule.md).

Þegar sérsniðið skýrsluútlit er skilgreint er hægt að velja það af úr spjöldum viðskiptamanna og lánardrottna til að tilgreina að valið útlit á að nota fyrir skjöl sem þú býrð til fyrir viðskiptamanninn eða lánardrottinn. Frekari upplýsingar eru í [Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md).

## <a name="to-create-a-custom-layout"></a>Til að búa til sérsniðið útlit

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Val á útliti skýrslu** og veldu síðan tengda tengilinn.

    Síðan **Val á útliti skýrslu** sýnir allar skýrslur sem eru í boði fyrir fyrirtæki sem er tiltekið í reitnum **Heiti fyrirtækis** efst á síðunni.
2. Stilltu reitinn **Fyrirtæki** á fyrirtækið sem búa á til skýrsluútliti fyrir.
3. Veldu röðina fyrir skýrsluna sem þú vilt stofna útlitið fyrir, og veldu svo **Sérsniðið útlit** aðgerðina.  

   Síðan **Sérsniðið skýrsluútlit** birtist og sýnir öll sérsniðin útlit sem eru í boði fyrir völdu skýrsluna.
4. Ef þú vilt búa til afrit af sérsniðnu útliti sem þegar er til velurðu sérsniðið útlitið af listanum og velur svo **Afrita** aðgerðina.  

   Afrit af sérsniðna útlitinu birtist á síðunni **Sérsniðið skýrsluútlit** með orðunum *Afrit af* í **lýsing** reitnum.
5. Ef þú vilt bæta við nýju sérsniðnu útliti sem byggir á innbyggðu útliti skaltu gera eftirfarandi:  
   1. Valið er **Nýtt** aðgerð. Síðan **Setja inn innbyggt útlit fyrir skýrslu** birtist. Reitirnir **Auðkenni** og **Heiti** eru fylltir inn sjálfkrafa.
   2. Til að bæta við sérsniðnu Word-skýrsluútliti skaltu velja **Setja inn Word-útlit** gátreitinn.
   3. Til að bæta við sérsniðnu RDLC-skýrsluútliti skaltu velja **Setja inn RDLC-útlit** gátreitinn.
   4. Velja hnappinn **Í lagi**.  

    Nýja sérsniðna útlitið birtist nú á síðunni **Sérsniðið skýrsluútlit**. Ef nýtt útlit byggir á innbyggðu útliti er það með orðin **Afrit af innbyggðu útiliti** í reitnum **Lýsing**. Ef ekkert innbyggt útlit var til staðar fyrir skýrsluna þá er nýja útlitið með orðin **Nýtt útlit** í reitnum **Lýsing**, sem táknar að sérsniðna útlitið er autt.
6. Reiturinn **Heiti fyrirtækis** er sjálfgefið auður, sem táknar að sérsniðið útlit er í boði fyrir skýrsluna í öllum fyrirtækjum. Til að gera sérsniðið útlit aðeins aðgengilegt fyrir tiltekið fyrirtæki, skal velja **Breyta** og stilla síðan reitinn **Heiti fyrirtækis** á það fyrirtæki sem þú vilt.

Sérsniðna útlitið hefur verið búið til. Þá er hægt að breyta sérsniðna útlitinu eftir þörfum.

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Breyta sérsniðnu útliti

Til að breyta skýrsluútliti úr , þarftu fyrst að flytja út skýrsluútlit sem skrá á staðsetningu í tölvunni þinni eða neti, og svo opna útflutta skjalið í og gera breytingarnar. Þegar þú hefur lokið við að gera breytingarnar flyturðu inn skýrsluútlitið.

### <a name="to-modify-a-custom-layout"></a>Skýrsluútliti sérsniðnu breytt

1.  Þú flytur út sérsniðið útlit á síðunni **sérsniðið skýrsluútlit**. Ef þessi síða er ekki þegar opinn, skal leita að og opna síðuna **Val á skýrsluútliti** og veldu röðina fyrir skýrsluna sem þú vilt breyta útlitið fyrir, og veldu svo **Sérsniðið útlit** aðgerðina.  
2.  Á síðunni **Sérsniðið skýrsluútlit** skal velja útlitið sem þú vilt breyta, veldu **Flytja út útlit** aðgerðina og svo velja **Vista** eða **Vista sem** til að vista skýrsluútlitsskjalið á staðsetningu í tölvunni eða á netkerfi.  

3.  Opnaðu skýrsluútlitsskjalið sem þú vistaðir og gerðu breytingar.

      Ef þú ert að breyta Word útliti, opnaðu útlitsskjalið í Word. Fyrir upplýsingar um breytingar, sjá næsta hluta [Breytingar gerðar á skýrsluútlitinu](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      Breyting RDLC-skýrsluútlits er flóknara en Word-skýrsluútlits. Frekari upplýsingar um það hvernig RDLC-skýrsluútliti er breytt eru í [Hanna RDLC-skýrsluútlit](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Mundu að vista breytingar þegar lokið.

4.  Farið aftur á síðuna **Sérsniðið skýrsluútlit**, veljið skýrsluútlit sem var flutt út og breytt og veljið svo **Flytja inn útlit** aðgerðina.  

5. Í svarglugganum **Flytja inn** skal velja **Velja** til að finna og velja skjalið sem skilgreinir skýrsluútlitið og svo velja **Opna**.

##  <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a>Búa til og breyta sérsniðnum skýrsluútlitum

Til að gera almennar sniðsbreytingar og útlitsbreytingar, t.d. að breyta leturgerð, bæta við og breyta töflu eða að fjarlægja gagnareit, skal einfaldlega nota grunnbreytingarvalkosti Word, líkt og gert er fyrir öll önnur Word skjöl.

Ef þú ert að hanna Word-skýrsluútlit frá grunni eða bæta við nýjum gagnareitum skaltu byrja með því að bæta við töflu sem er með raðir og dálka sem munu að endingu innihalda gagnareitina.

> [!TIP]  
> Sýna hnitanetslínur töflu þannig að jaðrar töfluhólfanna sjáist. Loka skal hnitanetslínum þegar breytingum er lokið. Til að sýna eða fela töfluhnitalínur velurðu töfluna og svo, undir **Útlit** á flipanum **Tafla** velurðu **Skoða hnitalínur**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Innfelling leturgerða í Word Layouts fyrir samræmi

Til að tryggja að skýrslur birtist alltaf og prentist með fyrirhuguðum leturgerðum, óháð hvar notendur opna eða prenta skýrslurnar, geturðu fellt inn leturgerðirnar í Word skjalinu. Hins vegar skaltu hafa í huga að innbyggðar leturgerðir geta verulega aukið stærð Word skjala. Nánari upplýsingar um innfellingu leturgerða í Word, sjá [Fella inn leturgerðir í Word, PowerPoint eða Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a> Merkimiða- og gagnareitir fjarlægðir úr Word-útliti

 Merkimiða- og gagnareitir skýrslu eru í efnisstjórnun í Word. Eftirfarandi mynd sýnir efnisstjórnun þegar hún er valin í Word skjalinu.  

 ![Efnisstjórnun fyrir reit í Word skýrsluútliti](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Heiti merkisins eða heiti gagnareits er birt í efnisstjórnun. Í dæminu er heiti reitsins CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Til að fjarlægja merki eða gagnareit  

1. Hægri-smellir á reitinn sem á að eyða og svo **Fjarlægja efnisstýringu**.  

     Efnisstjórnunin er fjarlægð en reitarheitið er til staðar sem texti.  

2. Eyða skal textanum sem eftir er eftir því sem þörf krefur.  

### <a name="adding-data-fields"></a>Bæta við gagnareitum

Að bæta við gagnareitum úr gagnamengi skýrslu er betri leið og kallar á þekkingu gagnamengis skýrslunnar. Upplýsingar um það hvernig reitum er bætt við fyrir gögn, merkjum, gögnum og myndum er að finna í [Bæta reitum við Word skýrsluútlit](ui-how-add-fields-word-report-layout.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Undirbúa Financial Reporting með fjárhagsskemu og lyklategundum](bi-how-work-account-schedule.md) 
[Business Intelligence](bi.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]