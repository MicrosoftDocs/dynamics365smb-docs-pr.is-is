---
title: Kynning á Contoso Coffee Project Management
description: Þessi grein kynnir þig á Consoso Coffee sýnigagna fyrir verk og verkefnastjórnun.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="introduction-to-contoso-coffee-jobs-and-project-management"></a>Kynning á Contoso Kaffiverkum og verkefnastjórnun

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki. Contoso-kaffiforritin **fyrir** Business Central bæta við kynningargögnum sem hægt er að nota til að læra hvernig á að nota getu verka og verkefnastjórnunar í Business Central.

Í forritinu eru nokkrir þættir sem notaðir eru í aðalkynningunum:

- Forði með úthlutaða þekkingu og svæði
- Vörur sem eru grunnstilltar til að stofna þjónustuvörur

> [!IMPORTANT]
> Áður en þú keyrir einhverjar aðstæður fyrir Contoso Coffee skaltu bóka allar birgðabókarlínur með opnunarstöðum. Nánari kröfur má finna í hlutanum [Setja upp Contoso-kaffigögn](#set-up-contoso-coffee-jobs-and-project-management-data) .
>
> 
## <a name="set-up-contoso-coffee-jobs-and-project-management-data"></a>Uppsetning Contoso-kaffiverka og verkefnastjórnunargagna

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Þegar viðkomandi forrit hafa verið sett upp er farið á [síðuna Contoso Coffee Jobs Demo Data í](https://businesscentral.dynamics.com/?page=4767)  [!INCLUDE [prod_short](../../includes/prod_short.md)] og sjálfgefnum stillingum breytt eftir þörfum. Eftirfarandi töflur lýsa stillingunum.  

|Svæði  |Lýsing  |
|---------|---------|
|**Upphafsár** |Tilgreinir fyrsta árið sem á að nota fyrir sýnigögn Contoso Coffee. Árið er annað hvort almanaksár eða reikningsár en það fer eftir uppsetningu fyrirtækisins.|
|**Númer viðskiptamanns**  |Viðskiptavinurinn sem á að nota í dæmum í söluaðgerðum.|
|**Vara 1 nr.**  |Varan sem á að nota í tilfellum samnings.|
|**Vörunr.**  |Varan sem á að nota í brotskeytisaðstæðum.|
|**Staðbundið forðanúmer 1**  |Forðinn sem á að nota í tilfellum samninga.|
|**Forðanúmer 1**  |Forðinn sem á að nota fyrir brotskeyti.|
|**Bókunarflokkur viðskm.**|Tilgreinir viðskiptakóta fyrir innlenda viðskiptamenn. Viðskiptakóðarnir eru notaðir þegar færslur eru bókaðar. |
|**Almennur viðskiptabókunarflokkur viðskm.**|Tilgreinir viðskiptakóta fyrir innlenda viðskiptamenn. Viðskiptakóðarnir eru notaðir þegar færslur eru bókaðar. |
|**Innlendur – almennur viðskiptabókunarflokkur**|Tilgreinir viðskiptakóða fyrir innlenda viðskiptavini og lánardrottna. Viðskiptakóðarnir eru notaðir þegar færslur eru bókaðar. |
|**Endursala - Birgðabókunarflokkur**    |Tilgreinir kóta fyrir vörur sem nota verður til að bóka endursölu.|
|**Smásala – almennur vörubókunarflokkur**    |Tilgreinir kóða fyrir vörur sem verður að nota til að bóka smásölu.|
|**VSK-vörubókunarflokkur**    |Tilgreinir VSK-vörukóta fyrir vörur til að bóka VSK ef VSK er virkjaður.|
|**Verðstuðull**     |Tilgreinir stuðul til að umbreyta verði úr USD/EUR í staðbundinn gjaldmiðil. *1* þýðir að verðið er sama upphæð í hvaða gjaldmiðli sem er. Hærri tala verður notuð til að fá verðið í staðbundnum gjaldmiðli. |
|**Sléttunarnákvæmni**  |Skilgreinir hvernig reiknað notkunarmagn er sléttað þegar það er fært inn á notkunarbókarlínur. Magn undir 0,5 verður sléttað niður Magn sem er 0,5 eða meira verður sléttað upp.|

Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

## <a name="see-also"></a>Sjá einnig .
