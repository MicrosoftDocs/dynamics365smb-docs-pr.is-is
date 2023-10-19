---
title: Kynning á sýnigögnum Contoso Coffee
description: Yfirlit yfir áætlanir um hvernig contoso kaffi sýnishorn gögn geta aðstoðað við að læra hvernig nýta má getu í viðskiptafræði miðlægt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-demo-data"></a>Kynning á sýnigögnum Contoso Coffee

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki.  **Útlaginn kaffiforrit**  til  [!INCLUDE [prod_short](../includes/prod_short.md)]  að bæta við sýnigögnum sem þú getur notað til að læra að nota getunina í [!INCLUDE [prod_short](../includes/prod_short.md)].  

## <a name="set-up-contoso-coffee-data"></a>Setja upp Contoso Coffee gögn

[!INCLUDE [contoso-coffee-app-install](contoso-coffee-app-install.md)].

Þegar apps er uppsett, á  **verkfærareinunni**  contoso demo skal nota  **samskipanaraðgerðina**  til að undirbúa eftirfarandi einingar. Hægt er að velja að setja upp öll tiltæk gögn, þar á meðal uppsett og framleiðslugögn eða uppsetningargögn eingöngu.

 -  **Sameiginleg eining**  til að undirbúa almennar stillingar sem  [!INCLUDE [prod_short](../includes/prod_short.md)]  krefst. Til dæmis, hluti eins og númeraröðin. 

Eftirfarandi tafla lýsir stillingum:  

|Svæði  |Heimildasamstæða  |
|---------|---------|
|**Upphafsár** |Tilgreinir fyrsta árið sem óskað er eftir að notuð séu útsýnandi Kaffisýnigögn. Árið er annað hvort almanaksár eða reikningsár en það fer eftir uppsetningu fyrirtækisins.|
|**Lands-/svæðiskóti**|Tilgreinir lands-/svæðiskóta fyrir innlenda viðskiptavini og lánardrottna.|
|**Tegund fyrirtækis**    |Tilgreinir hvort núverandi fyrirtæki þurfi að tilkynna um virðisaukaskatt eða söluskatt. |
|**Verðstuðull**     |Tilgreinir stuðul til að umbreyta verði úr USD/EUR í staðbundinn gjaldmiðil. *1* þýðir að verðið er sama upphæð í hvaða gjaldmiðli sem er. Hærri tala verður notuð til að fá verðið í staðbundnum gjaldmiðli. |
|**Sléttunarnákvæmni**  |Tilgreinir sléttunarnákvæmni sem sýnigögn eiga að hafa.|

 -  [Framleiðslueiningin](manufacturing/contoso-coffee-manufacturing-intro.md)  til að undirbúa  [framleiðsluaðstæður](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 -  [Vöruhúsaeiningin](warehousing/contoso-coffee-warehousing-intro.md)  til undirbúnings fyrir  [vöruhúsaaðstæður](warehousing/contoso-coffee-warehousing-intro.md#scenarios).
 -  [Þjónustueiningin](service/contoso-coffee-service-intro.md)  sem á að undirbúa fyrir  [þjónustuaðstæður](service/contoso-coffee-service-intro.md#scenarios).

Eftir að þú hefur skilgreint einingarnar sem þú vilt prófa skaltu velja  **aðgerðina búa**  til til að stofna sýnigögn fyrir þau.

## <a name="see-also"></a>Sjá einnig .

[Framleiðsla](../production-manage-manufacturing.md)  
[Vöruhúsum](../warehouse-manage-warehouse.md)  
[Þjónustu](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

