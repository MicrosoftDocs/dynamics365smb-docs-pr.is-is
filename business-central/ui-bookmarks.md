---
title: Bókamerkja tengil í síðu eða skýrslu í Mitt hlutverk | Microsoft Docs
description: Kynntu þér hvernig á að bæta tengli við svæðið Mitt hlutverk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7f93d54984106cb0fce2d886f6826ba22b1d8185
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787478"
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Síða eða skýrsla bókamerkt í Mitt hlutverk
Með bókamerkjatákni er hægt að bæta aðgerð sem opnar síðu úr yfirlitsvalmyndinni í Mitt hlutverk. Þetta gerir þér kleift að ná fljótt í eftirlætisefnið eða viðskiptaverkefnin þín. Hægt er að bæta við bókamerkinu frá marksíðunni eða skýrslu, sem merkir að skjárinn sem tengja á í Mitt hlutverk opnast.

Táknið fyrir bókamerki er sýnt efst í hægra horninu á síðu og einnig í **Viðmótsleit** glugga þar sem hægt er að nota bókamerki fyrir margar síður eða skýrslur. Ef bókamerki er þegar til fyrir síðuna, þá er teiknið dimmt og verkfæratáknið segir „bókamerkt“.

## <a name="to-bookmark-the-target-page"></a>Til að bókamerkja marksíðu
1. Opnaðu hvaða síðu sem er sem þú vilt fá tengil fyrir í Mitt hlutverk.
2. Velja táknið ![Bókamerki](media/ui_bookmark_icon.png "Bókamerki").

Aðgerð sem er nefnd eftir síðunni er nú bætt við yfirlitsvalmyndina í Mitt hlutverk.

## <a name="to-bookmark-the-target-report"></a>Til að bókamerkja markskýrslu
1. Opnaðu hvaða síðu skýrslubeiðna sem er sem þú vilt fá aðgerð fyrir Mitt hlutverk.
2. Velja táknið ![Bókamerki](media/ui_bookmark_icon.png "Bókamerki").

Aðgerð sem er nefnd eftir skýrslunni er nú bætt við yfirlitsvalmyndina í Mitt hlutverk.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a>Til að bókamerkja síðu eða skýrslu úr glugganum „Viðmótsleit“
1. Opnaðu **Viðmótsleit** glugga og Sláðu inn, til dæmis **sölupantanirnar**.
2. Farið yfir leitarniðurstöður fyrir **Sölupantanir** síðuna eða skýrslu og táknið ![Bókamerki](media/ui_bookmark_icon.png "Bókamerki") svo valið.

Aðgerð sem er nefnd eftir síðunni eða skýrslunni er nú bætt við yfirlitsvalmyndina í Mitt hlutverk.


## <a name="frequently-asked-questions"></a>Algengar spurningar  

- **Get ég endurskipulagt bókamerkin mín?**  
Já. Hægt er að sérsníða Mitt hlutverk og færa aðgerðir inn í nákvæmari röð eða færa þær inn fyrirliggjandi flokka eða undirflokka.  
Kynntu þér hvernig [Sérstilla verksvæði](ui-personalization-user.md).

- **Hvernig fjarlægi ég bókamerki?**  
Á marksíðunni eða skýrslunni skaltu velja bókamerkjatáknið aftur til að fjarlægja viðkomandi aðgerð úr Mitt hlutverk. Einnig er hægt að sérstilla Mitt hlutverk og fela aðgerðir tímabundið án þess að fjarlægja þær alveg.

- **Hvar finn ég bókamerkið mitt?**  
Þegar bókamerki er bætt við síðu eða skýrslur er nýju aðgerðinni bætt við efst á yfirlitsvalmyndina á núverandi heimaskjá (Mitt hlutverk). Ef þú ert með margar aðgerðir getur þurft að virkja hnappinn **Meira** til að birta þær allar þar sem nýju aðgerðinni er alltaf bætt við í lok þessara aðgerða.
<!-- Should we add a screenshot here? -->

- **Ég er ekki með bókamerkjatákn. Er eitthvað að?**  
Möguleikinn á að bókamerkja síðu eða skýrslu er ein af mörgum sérstillingaraðgerðum í Business Central. Ef bókamerkjatákn er ekki birt er líklegt að stjórnandi hafi slökkt á sérstillingum.

- **Hvers vegna er ekki hægt að bókamerkja ákveðnar síður eða skýrslur?**  
Ekki er hægt að bókamerkja allar síður og skýrslur. Þegar síða eða skýrslur eru keyrðar innan sérstaks samhengis sem viðskiptaforritið stjórnar er bókamerkjatákn ekki birt. Til dæmis munu síður sem finnast ekki í glugganum **Viðmótsleit** en eru ræstar annars staðar ekki birta bókamerkjatákn. Á sama hátt birta síður skýrslubeiðna sem eru aðeins notaðar til að safna síum án þess að keyra skýrsluna ekki bókamerkjatákn.

Sjá tæknilegar upplýsingar um [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) og [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Þegar sérstillingar eru hreinsaðar, verða bókamerkin mín einnig hreinsuð?**  
Já. Bókamerki eru í yfirlitsvalmynd. Ef breytingar á yfirlitsvalmyndinni eru hreinsaðar á einhverri síðu, eða allar sérstillingar í Mitt hlutverk, eru allar nýju aðgerðirnar þínar fjarlægðar varanlega.

- **Hvers vegna heldur bókamerkjatáknið mitt áfram að gefa til kynna að það sé enn ekki bókamerkt?**  
Þegar bókamerki er bætt við er nýju aðgerðinni bætt við yfirlitsvalmyndina á Mitt hlutverk og heimsóknir á síðuna eða skýrsluna eftir það sýna dökkt bókamerkjatákn. Ef þú sérstillir Mitt hlutverk og endurskipuleggur aðgerðir þínar með því að færa þær í hópa, er bókamerkjatáknið ekki lengur dökkt og hægt er að bæta öðru bókamerki við sömu síðu eða skýrslu. Þetta gerir þér kleift að bæta við mörgum aðgerðum á sömu síðu eða skýrslu og flokka þær í mismunandi flokka.

- **Hvers vegna er tengill minn í skýrslu að birta aðra skýrslugerð?**  
Sumum skýrslum kann að vera skipt út fyrir aðrar skýrslur eftir að viðbót hefur verið notuð í Business Central. Þegar staðgengill er notaðu er texti nýju aðgerðarinnar ekki uppfærður og mun halda áfram að birta heiti upprunalegu skýrslunnar, en fara þarf í nýrri skýrsluna. Til að leiðrétta texta nýju aðgerðarinnar er hægt að fjarlægja nýju aðgerðina og bæta henni við aftur.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Er bókamerking í boði fyrir XMLports?**  
Fj. Eins og er ekki hægt að bæta við aðgerðum til að opna XMLports úr notandaviðmótinu.

- **Verða bókamerkin mín þýdd þegar ég breyti tungumáli mínu í Business Central?**  
Þegar nýrri aðgerð er bætt við er öllum þýddum texta sem var tiltækur á þeim tíma notað þegar verið er að bókamerkja. Ef nýjum þýddum texta er bætt við síðar mun nýja aðgerðin ekki innihalda nýrri þýðingarnar.


## <a name="see-also"></a>Sjá einnig
[Sérstilling verksvæðis](ui-personalization-user.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]