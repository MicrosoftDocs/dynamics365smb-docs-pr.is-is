---
title: Skipta yfir í annað fyrirtæki eða umhverfi
description: Ef unnið er fyrir mörg fyrirtæki er fljótlegt að skipta á milli umhverfis og fyrirtækja.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: environments, companies, tenants, organization
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 08/16/2022
ms.author: bholtorf
ms.openlocfilehash: 0cc18a4a84e24ce58d486275442ba686ed559047
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605955"
---
# <a name="switching-to-another-company-or-environment"></a>Skipta yfir í annað fyrirtæki eða umhverfi

[!INCLUDE [prod_short](includes/prod_short.md)] er fáanlegt í mörgum mismunandi löndum og styður við margar mismunandi gerðir stofnana. Fyrirtækið kann að velja að skipuleggja vinnu í [!INCLUDE [prod_short](includes/prod_short.md)] mörgum *fyrirtækjum* og *umhverfi*. Þessi grein hjálpar til við að skilja lykilmuninn og hvernig unnið er þvert á þá.

## <a name="about-companies-and-environments"></a>Um fyrirtæki og umhverfi

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Ef skipt er oft á milli fyrirtækj, eða unnið er með [!INCLUDE[prod_short](includes/prod_short.md)] úr öðru forriti á borð við Microsoft Teams, getur verið auðvelt að missa sjónar á því hvar þú ert. Til að auðvelda þér að fylgjast með er hægt að bæta við merki sem birtir heiti fyrirtækisins þannig að þú getir staðfest á skjótan hátt að þú sért á réttum stað. Nánari upplýsingar er að finna [í Display fyrirtækjamerkis](admin-company-information.md#badge).
> 
> Allt frá vafra er einnig hægt að pinna mismunandi fyrirtæki í eftirlætisstiku.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## <a name="features-for-switching-company-or-environment"></a>Aðgerðir til að skipta um fyrirtæki eða umhverfi

Það eru til örfáir Eiginleikar sem þú getur notað til að skipta fyrirtækinu eða umhverfinu sem þú vinnur. Eftirfarandi tafla ber saman möguleika á lögun, sem útskýrð er nánar í köflum sem fylgja.

|Eiginleiki|Skipta um fyrirtæki|Skipta um umhverfi|Skiptiborð í nýjum vafraflipa| Aðgengilegt innanhúss|
|-------|--------------|------------------|-------------------------|----------------------|
|[Skipafélagið rofi](#use-the-company-switcher)|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|
|[App-ræsing](#use-the-app-launcher)||![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")||
|[Mínar stillingar](#use-my-settings)|![gátmerki](media/check.png "ávísun")|||![gátmerki](media/check.png "ávísun")|
|[Fyrirtækjnöf](#use-company-hub)|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")||

## <a name="use-the-company-switcher"></a>Nota skiptifyrirtækið

Að nota fyrirtækið skipari er líklega fljótasta og mest fjölhæfur leið til að skipta um fyrirtæki. Fyrirtækið skipari er rúðuþurrkur sem eru fúslega fáanlegar frá hvaða síðu sem er. Rúðan gefur yfirlit yfir öll fyrirtæki í öllu umhverfi sem notandi hefur aðgang að og skiptir sér beint í &mdash; það sem er annað hvort á sama vafraflipanum eða nýtt. Það hentar sérstaklega vel þegar unnið er í mörgum fyrirtækjum yfir mismunandi umhverfi.

1. Í efra hægra horninu, nálægt leitartákninu, sérðu annað hvort táknið fyrir venjulegt fyrirtæki eins og ![skotteiknið fyrir fyrirtæki.](media/ui-experience/company-icon.png "Birtir sundurtákn fyrirtækisins sem notað er þegar eitt umhverfi er til staðar") Og ![Company-Icon-mult-Env](media/ui-experience/company-icon-multi-env.png "Birtir sundurtákn fyrirtækisins sem notað er þegar mörg umhverfi eru til staðar"), eða [sérsniðinn Skjöldur](admin-company-information.md#badge) fyrir fyrirtækið sem þú starfar hjá. Velja táknið til að opna sundurvirka rúðuna fyrirtækisins.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Sýnir tákn fyrirtækisins í fyrirsögn Viðskiptamiðis viðskiptavinar.":::  

   > [!TIP]
   > Einnig er hægt að nota flýtivísunina CRTL + O til að opna rúðuna.
2. **Í rúðunni tiltæk fyrirtæki** skal velja fyrirtækið sem á að skipta yfir í, velja **skiptiörina** og velja svo einn af eftirfarandi valkostum:

   |Valkostur|Lýsing|
   |------|-----------|
   |Skipta|Opnar hlutverkamiðstöð valins fyrirtækis í sama vafraflipa sem verið er að vinna í. Fyrirtækið verður sjálfgefið fyrirtæki sem opnast í Aðalviðskiptum þar til skipt er á ný eða fyrirtækinu breytt með því að nota **stillingarnar**. |
   |Opna í nýjum flipa|Opnar hlutverkamiðstöð valins fyrirtækis í nýjum vafraflipa með því að halda upprunalegu fyrirtæki opinni á öðrum flipanum.|
   |Opna í nýjum flipa og fara á sömu síðu|Þessi valkostur er aðeins virkur á listasíðum, eins og viðskiptavinum, sölupöntunum eða vörum. Það opnar sama lista en fyrir valið fyrirtæki í nýjum vafraflipa. |

> [!TIP]
> Stutt er á F5 til að endurnýja lista yfir umhverfi og fyrirtæki.

## <a name="use-the-app-launcher"></a>Nota forritið App

Þegar þú ert skráð(ur) inn á [!INCLUDE[prod_short](includes/prod_short.md)] eru umhverfin sem hægt er að opna aðgengilegt á Office.com.  

1. Veldu teiknið fyrir forritstáknið á **forritinu** . ![.](media/app-launcher-icon.png "Forritavalmynd býður upp á aðgang að fleiri eiginleikum")
2. Í rúðunni sem opnast, leita að og velja [!INCLUDE[prod_short](includes/prod_short.md)]. Ef þú sérð [!INCLUDE[prod_short](includes/prod_short.md)] ekki, Veldu **öll forrit**, þá færðu inn **miðlægt** í **leitargluggann**.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text="Microsoft 365 App-kynnirinn sem sýnir Viðskiptamiðað tiln.":::  

3. Ef fleiri en eitt umhverfi eru til staðar er beðið um að velja umhverfið til að komast að.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## <a name="use-my-settings"></a>Nota mínar stillingar

Þegar þú ert skráður inn á [!INCLUDE[prod_short](includes/prod_short.md)], getur þú á einfaldan hátt skipt yfir í annað fyrirtæki í sama umhverfi. Þegar búið er að gera skiptin er fyrirtækið sem þú velur að verða sjálfgefið fyrirtæki og opnar það næst þegar þú skráir þig inn.

1. Í horninu efst til hægri eru stillingar teiknartákns **valdar**![.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og velja **síðan aðgerðina stillingar**.

    > [!TIP]
    > Einnig er hægt að nota flýtilykilinn Alt+T til að opna síðuna Mínar stillingar á skjótan hátt.

2. Á síðunni **Mínar stillingar** á svæðinu **Fyrirtæki** er valið fyrirtæki.  
3. Velja hnappinn **Í lagi**.

> [!TIP]
> Góð aðferð við að fara beint í sjálfgefna fyrirtækið þegar þú skráir þig inn og ekki þurfa að tilgreina umhverfið er að bæta vefslóðinni á eftirlætislistann þinn eftir að þú skráir þig inn.

## <a name="use-company-hub"></a>Nota nöf fyrirtækis

*Fyrirtækjnöf* er mjög sérhæfð hlutverkamiðstöð sem gefur fjárhagslegt yfirlit yfir fyrirtæki og umhverfi. Fáanlegt sem [framlenging](ui-extensions-company-hub.md), fyrirtækið Hub útvegar Mælaborð með safngögnum fyrir hvert fyrirtæki sem þú hefur aðgang að. Heimasíðan birtir fjárhagslega afkastavísa og bein tengsl við einstök umhverfi og fyrirtæki. Frekari upplýsingar er að finna í [Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md).

[![Sýnir fyrirtækjahub-síðuna sem skráir öll fyrirtæki.](media/company-hub.png)](media/company-hub.png#lightbox)  

## <a name="see-also"></a>Sjá einnig .

[Stofna ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Umhverfi og fyrirtæki (eingöngu á ensku)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Upplýsingar um fyrirtæki](admin-company-information.md)  
[Stjórnunarmiðstöð Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
