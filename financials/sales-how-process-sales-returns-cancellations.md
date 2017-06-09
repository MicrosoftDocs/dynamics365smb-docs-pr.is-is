---
title: "Meðhöndlun söluvöruskila eða afturkallana | Microsoft Docs"
description: "Meðhöndlun söluvöruskila eða afturkallana"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: cf471e0c3a13a954ab7604a8b1d0f715f664722d
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-sales-returns-or-cancellations"></a>Meðhöndlun söluvöruskila eða afturkallana
Ef viðskiptavinur vill skila eða endurgreiða fyrir vörur eða þjónustu sem þú hefur selt og fengið greiðslu fyrir verður þú að búa til og senda inn söluskuldbindingar sem tilgreinir umbeðnar breytingar. Til að geta tekið upp réttar upplýsingar um sölureikninga geturðu búið til söluskuldbindinguna frá uppgefnu sölureikningi eða notað afritaaðgerð.  

**Til athugunar:** Ef staða sölureiknings hefur ekki verið greiddur þá geturðu notað **Rétt** eða **Hætta við** störf á staða sölureikning til að snúa við viðskiptum. Þessar aðgerðir virka aðeins fyrir ógreiddar reikningar og styðja ekki hluta skilar eða afpöntunar. Nánari upplýsingar er að finna [hvernig á að: Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md)

Auk upprunalega bókaðs sölureiknings, er hægt að jafna sölukreditreikning öðrum söluskjölum, t.d. aðra bókað sölureikninga, þar sem viðskiptamaðurinn er einnig að skila vörum sem voru afhentar með viðkomandi reikningi.

Skil eða endurgreiðsla getur átt við um aðeins hluta af vörum eða þjónustum á upprunalega sölureikningnum. Í því tilviki þarf að breyta upplýsingum í línunum á sölukreditreikningnum. Við bókun sölukreditreiknings eru þau söluskjöl sem eru breytingin hefur áhrif á bakfærð og hægt er að stofna endurgreiðslu til viðskiptamannsins.  

Hægt er að senda bókaða sölukreditreikninga til viðskiptamannsins til að staðfesta vöruskil eða afturköllun og miðla því að virðið verði endurgreitt, til dæmis þegar vörum er skilað.  

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Að stofna nýjan sölukreditreikning úr bókuðum sölureikningi.
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið") færa **Bókaðir sölureikningar**, og velja síðan viðeigandi tengil.  
2. Í glugganum **Bókaðir sölureikningar** skal velja þá bókuðu sölureikninga sem á að bakfæra og veljið síðan aðgerðina **Stofna leiðréttan kreditreikning**.

    Minnispunktur fyrir sölureikninginn inniheldur nokkrar upplýsingar frá staða sölureikningsins. Hægt er að breyta þessu, til dæmis með nýjar upplýsingar sem endurspegla endursenda samkomulagið.  
3. Breyttu upplýsingum um línurnar í samræmi við samninginn, svo sem fjölda skilaðra hluta eða fjárhæðin sem endurgreiða.
4. Valið er **Jafna Færslur** aðgerð.
5. Í glugganum **Jafna viðskm.færslur** skal velja línuna með bókaða söluskjalinu sem á að jafna sölukreditreikninginn við og veljið síðan aðgerðina **Kenni jöfnunar**.

    Kennimerki söluskuldbindinga birtist á **kenni jöfnunar**.
6. Sláðu inn **Upphæð til að jafna** sem þú vilt sækja um í upphæðin sem á að sækja um ef hún er minni en upphafleg upphæð.  

    Neðst á glugganum **Jafna viðskm.færslur** er hægt að skoða heildarupphæðina sem á að nota til að bakfæra allar færslur, nefnilega þegar gildið í reitnum **Staða** er núll.
7. Velja hnappinn **Í lagi**. Þegar þú sendir inn sölutilboðið, þá er það sótt á staða söluskráanna.

    Eftir að þú hefur stofnað línur fyrir sölukreditreikningana eða breytt þeim og ein eða fleiri jöfnun tilgreind, er hægt að bóka sölukreditreikninginn.   
8. Veljið aðgerðina **Bóka og senda**.  

Í **Bóka og Senda staðfestingu** svargluggi opnast og sýnir notuð valda sendingaraðferð fyrir viðskiptamanninn. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn í reitnum **Senda skjal** til. Frekari upplýsingar er að finna á [Hvernig á að: Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md)  

Bókuðu söluskjölin sem jafnað var við kreditreikninginn eru nú bakfærðir og endurgreiðslu má nú búa til fyrir viðskiptamanninn. Sölukreditreikningurinn er fjarlægður og skipt út fyrir nýtt fylgiskjal á lista bókaðra sölukreditreikninga.

## <a name="to-create-a-sales-credit-memo-from-scratch"></a>Að búa til sölukreditreikning frá grunni
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Bókaðir sölureikningar**, og velja síðan viðeigandi tengil.
2. Veljið aðgerðina **Nýtt** til að opna nýjan auðan sölukreditreikning.
3. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.
4. Valið er **Afrita fylgiskjal** aðgerð.
5. Í glugganum **Afrita söluskjal** í reitnum **Gerð skjals** skal velja **Bókaður reikningur**.
6. Veljið **skjalanúmer** reitinn til að opna gluggann **Bókaðir sölureikningar** og velið síðan bókaða sölureikninginn sem inniheldur línur sem þú vilt bakfæra.
7. Veljið gátreitinn **Endurreikna línur**, ef bókaða sölureikningslínan sem var afrituð á að uppfærast með breytingum á vöruverði og kostnaðarverði síðan reikningurinn var bókaður.
8. Velja hnappinn **Í lagi**. Afrituðu reikningslínurnar eru settar inn í sölukreditreikninginn.
9. Sölukreditreikningnum er lokið eins og útskýrt er í hlutanum "Að stofna sölukreditreikning úr bókuðum sölureikningi" í þessu efnisatriði.

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Hvernig á að: Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

