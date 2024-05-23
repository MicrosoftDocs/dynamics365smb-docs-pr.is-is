---
title: Kynning á sýnigögnum Contoso Coffee
description: Yfirlit yfir atburðarásir um hvernig Gögn Contoso-kaffisins geta hjálpað þér að læra að nota getuna í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# Kynning á sýnigögnum Contoso Coffee

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki. Contoso-kaffiforritin **til** [!INCLUDE [prod_short](../includes/prod_short.md)] að bæta við kynningu á gögnum sem hægt er að nota til að læra að nota getuna í [!INCLUDE [prod_short](../includes/prod_short.md)].  

## Setja upp Contoso Coffee gögn

[!INCLUDE [contoso-coffee-app-install](../includes/contoso-coffee-app-install.md)]

Þegar forritin eru sett upp, á síðunni **Contoso Demo Tool**, skal nota Grunnstillingu **aðgerðina** til að undirbúa eftirfarandi einingar. Hægt er að velja um að setja upp öll tiltæk gögn, sem fela eingöngu í sér uppsetningar- og framleiðslugögn, eða uppsetningargögn.

 - Sameiginleg **eining** til að undirbúa almennar stillingar sem [!INCLUDE [prod_short](../includes/prod_short.md)] þarf. Hluti eins og númeraraðir, til dæmis. Bent er á að **Sameiginleg eining** inniheldur aðeins viðbótargögn fyrir vöruhúsið, Framleiðsla, Þjónustuaðstæður. Ekki er mælt með því að keyra hana í einangrun.

Eftirfarandi tafla lýsir stillingunum:  

|Svæði  |Heimildasamstæða  |
|---------|---------|
|**Upphafsár** |Tilgreinir fyrsta árið sem nota á fyrir sýnigögn Contoso-kaffisins. Árið er annað hvort almanaksár eða reikningsár en það fer eftir uppsetningu fyrirtækisins.|
|**Lands-/svæðiskóti**|Tilgreinir lands-/svæðiskóta fyrir innlenda viðskiptamenn og lánardrottna.|
|**Tegund fyrirtækis**    |Tilgreinir hvort núverandi fyrirtæki þurfi að tilkynna um virðisaukaskatt eða söluskatt. |
|**Verðstuðull**     |Tilgreinir stuðul til að umbreyta verði úr USD/EUR í staðbundinn gjaldmiðil. *1* þýðir að verðið er sama upphæð í hvaða gjaldmiðli sem er. Hærri tala verður notuð til að fá verðið í staðbundnum gjaldmiðli. |
|**Sléttunarnákvæmni**  |Tilgreinir sléttunarnákvæmni sem sýnigögn eiga að hafa.|

 - Framleiðslueiningin [til](manufacturing/contoso-coffee-manufacturing-intro.md) að undirbúa [framleiðsluaðstæður](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 - Birgðahaldseiningin [til](warehousing/contoso-coffee-warehousing-intro.md) að undirbúa [fyrir húsnæðisaðstæður](warehousing/contoso-coffee-warehousing-intro.md#scenarios).
 - Þjónustueiningin [sem](service/contoso-coffee-service-intro.md) undirbúa á fyrir [þjónustuaðstæður](service/contoso-coffee-service-intro.md#scenarios).

Þegar einingarnar sem á að prófa hafa verið grunnstilltar skal velja aðgerðina **Mynda** til að stofna sýnigögn fyrir þær.

## Sjá einnig .

[Framleiðsla](../production-manage-manufacturing.md)  
[Aðvörun](../warehouse-manage-warehouse.md)  
[Þjónusta](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

