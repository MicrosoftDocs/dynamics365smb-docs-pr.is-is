---
title: Bæta við viðhengjum, tenglum og athugasemdum á færslum | Microsoft Docs
description: Setja tengil í skjal eða vefsíðu á tiltekna skrá, s.s. viðskiptavin eða fylgiskjal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 84d58193fa7ee272b372403d63702348fbfb1f77
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315277"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum

Í upplýsingareitnum á flestum spjöldum og skjölum er hægt að hengja við skrár, bæta við tenglum og skrifa athugasemdir. Einnig er hægt að gera þetta á listasíðunni með því að velja tengda línu fyrir tengla og athugasemd.

Til að skoða eða breyta einhverjum þessara tengdu upplýsingargerða verður fyrst að opna flipann **Viðhengi** í upplýsingareitnum. Talan fyrir aftan dálktitilinn gefur til kynna hversu margar viðhengdar skrár, tenglar eða upplýsingar eru til staðar fyrir kortið eða skjalið.

Viðhengi, tenglar og athugasemdirnar eru hengd við sem spjaldið eða skjalið er unnið úr í öðrum stöðum, t.d. frá yfirstandandi sölupöntun á bókuðum sölureikningi. Athugið hins vegar að engin af viðhengisgerðunum er úttak úr kerfinu, til dæmis við prentun eða þegar verið er að vista í skrá.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Til að hengja skrá við innkaupareikning
Hægt er að tengja allar gerðir skráa, sem innihalda texta, mynd eða myndskeið við spjald eða skjal. Þetta er til dæmis gagnlegt þegar óskað er eftir að vista reikning lánardrottins sem PDF-skrá á tengdum innkaupareikningi í [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Skrár sem eru hengdar við eiginleikann skjöl á innleið eru ekki teknar með á flipanum **Viðhengi**. Frekari upplýsingar er að finna í [Skjöl á innleið](across-income-documents.md).

Eftirfarandi ferli byggist á sölupöntun. Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.
2. Opnaðu sölupöntunina sem á að hengja skrá við.
3. Í upplýsingareitnum skal opna flipann **Viðhengi**.
4. Veljið gildið fyrir aftan reitinn **Skjöl**, eins og „0“.
5. Á síðunni **Skjöl í viðhengi** í reitnum **Viðhengi** skal velja hnappinn **Velja skrá**.
5. Veldu skrá frá hvaða staðsetningu sem er og veldu svo hnappinn **Opna**.

Skráin er nú hengd við innkaupareikninginn.

## <a name="to-add-a-link-from-an-item-card"></a>Til að bæta við tengli af birgðaspjaldi
Hægt er að bæta við tengli af korti eða skjali á einhverja vefslóð eða slóð. Þetta er gagnlegt, til dæmis þegar tengja á birgðaspjald við vörulista birgis.

Eftirfarandi aðferð er byggð á birgðaspjaldi. Skrefin eru svipuð fyrir öll önnur studd kort og skjöl.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda hlekkinn.
2. Veldu vöruna sem þú vilt bæta við tengli úr og veldu svo flipann **Viðhengi** í upplýsingareitnum.
3. Í **Tenglar** skal velja **+** táknið.
4. Í svæðinu **Veffang tengils** skal slá inn tengilinn.

    - Til að tengja skrá á þinni tölvu eða neti, skaltu færa inn fulla slóð og skráarheiti, eins og t.d. **C:\My Documents\invoice1.doc**.
    - Til að tengja á vefsíðu, færa inn vefslóðina (URL) eins og t.d. **www.microsoft.com**.
    - Til að tengja forrit, færa inn tilgreindan streng til að opna forritið. Til að opna t.d. Outlook með nýjum tómum tölvupósti til tiltekins viðtakanda skal færa inn **mailto:testalias**.  

5. Í reitinn **Lýsing** skal færa inn upplýsingar um tengilinn.  
6. Velja hnappinn **Í lagi**.

Tengillinn er nú tengdur við birgðaspjaldið.  

## <a name="to-write-a-note-on-a-sales-order"></a>Til að skrifa athugasemd á sölupöntun
Hægt er að skrifa athugasemd á skjal eða kort, til dæmis til að skrifa sérstakar leiðbeiningar fyrir aðra notendur skjalsins eða kortsins. Hægt er að hafa skráartengla og vefslóðir með í athugasemdum.

> [!NOTE]
> Athugasemdirnar á flipanum **Viðhengi** eru ekki tengdar virkni innri athugasemda, sem eru aðallega notaðar til að eiga samskipti á milli notenda verkflæðis. Nánari upplýsingar er að finna í [Uppsetning Verkflæði Tilkynningar](across-setting-up-workflow-notifications.md).

Eftirfarandi ferli byggist á sölupöntun. Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.
2. Veljið sölupöntunina sem á að afskrifa athugasemd við og veljið svo flipann **Viðhengi** í upplýsingareitnum.
3. Í hlutanum **Athugasemdir** skal velja **+** táknið.
4. Í reitinn **Athugasemd** skal færa inn hvaða texta sem er, t.d. „Þetta er áríðandi pöntun“.
5. Velja hnappinn **Í lagi**.

Athugasemdin er nú hengd við sölupöntunina.

## <a name="see-also"></a>Sjá einnig  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Skjöl á innleið](across-income-documents.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
