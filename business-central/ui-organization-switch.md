---
title: Skipta yfir í annað fyrirtæki eða umhverfi
description: Ef unnið er fyrir mörg fyrirtæki er fljótlegt að skipta á milli umhverfis og fyrirtækja.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/16/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="switching-to-another-company-or-environment"></a>Skipta yfir í annað fyrirtæki eða umhverfi

[!INCLUDE [prod_short](includes/prod_short.md)] er fáanlegt í mörgum mismunandi löndum/svæðum og styður margar mismunandi gerðir stofnana. Fyrirtækið þitt gæti valið að skipuleggja vinnu í [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum *fyrirtækjum* og *umhverfum*. Þessi grein hjálpar þér að skilja helsta muninn og hvernig á að vinna sig í gegnum hann.

## <a name="about-companies-and-environments"></a>Um fyrirtæki og umhverfi

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Ef skipt er oft á milli fyrirtækj, eða unnið er með [!INCLUDE[prod_short](includes/prod_short.md)] úr öðru forriti á borð við Microsoft Teams, getur verið auðvelt að missa sjónar á því hvar þú ert. Til að auðvelda þér að fylgjast með er hægt að bæta við merki sem birtir heiti fyrirtækisins þannig að þú getir staðfest á skjótan hátt að þú sért á réttum stað. Frekari upplýsingar eru í [Birta upplýsingatákn fyrirtækis](admin-company-information.md#badge).
> 
> Það fer eftir vafranum þínum en þú getur einnig fest mismunandi fyrirtæki við eftirlætisstikuna.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## <a name="features-for-switching-company-or-environment"></a>Eiginleikar til að skipta um fyrirtæki eða umhverfi

Það eru nokkrir eiginleikar sem þú getur notað til að skipta um fyrirtæki eða umhverfi þegar þú vinnur. Eftirfarandi tafla ber saman möguleika eiginleikans, sem eru útskýrðir nánar í næstu hlutum.

|Eiginleiki|Skipa um fyrirtæki|Skipta um umhverfi|Skipta í nýjum vafraglugga| Í boði á staðnum|
|-------|--------------|------------------|-------------------------|----------------------|
|[Skipt um fyrirtæki](#use-the-company-switcher)|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|
|[Forritavalmynd](#use-the-app-launcher)||![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")||
|[Mínar stillingar](#use-my-settings)|![gátmerki](media/check.png "ávísun")|||![gátmerki](media/check.png "ávísun")|
|[Fyrirtækjamiðstöð](#use-company-hub)|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")|![gátmerki](media/check.png "ávísun")||

## <a name="use-the-company-switcher"></a>Nota fyrirtækjaskipti

Að nota fyrirtækjaskiptinn er líklega fljótlegasta og fjölbreyttasta leiðin til að skipta um fyrirtæki. Fyrirtækjaskiptirinn er svæði sem er aðgengilegt á öllum svæði. Svæðið sýnir yfirlit yfir öll fyrirtæki í öllum umhverfum sem þú hefur aðgang að og gerir þér kleift að skipta beint yfir í öll þeirra&mdash;annaðhvort í sama vafraglugganum eða nýjum. Það er sérstaklega gagnlegt þegar unnið er í mörgum fyrirtækjum í mismunandi umhverfi.

1. Efst í hægra horninu, nálægt leitartákninu, sérðu annaðhvort staðlað tákn fyrirtækis, t.d. ![fyrirtækiskóða ræsiforrits](media/ui-experience/company-icon.png "Sýnir tákn fyrirtækjaskiptis sem notað er í einu umhverfi") og ![fjölumhverfi fyrirtækiskóða](media/ui-experience/company-icon-multi-env.png "Sýnir tákn fyrirtækjaskiptis sem notað er í mörgum umhverfum") eða [sérsniðið upplýsingatákn](admin-company-information.md#badge) fyrir fyrirtækið sem þú ert að vinna í. Veldu táknið til að opna svæði fyrirtækjaskiptis.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Sýnir tákn fyrirtækjaskiptis í haus Business Central-biðlarans":::  

   > [!TIP]
   > Einnig er hægt að nota  <kbd>flýtivísunina CRTL</kbd>+<kbd>O</kbd>  til að opna rúðuna.
2. Á svæðinu **Tiltæk fyrirtæki** skaltu velja fyrirtækið sem þú vilt skipta yfir í, velja örina **Skipta**, síðan velja einn af eftirfarandi valkostum:

   |Valkostur|Lýsing|
   |------|-----------|
   |Skipta|Opnar hlutverkamiðstöð fyrir valið fyrirtæki í sama vafraglugga og verið er að vinna í. Fyrirtækið verður sjálfgefna fyrirtækið sem opnast í Business Central, þar til þú skiptir aftur eða breytir fyrirtækinu með því að nota **Mínar stillingar**. |
   |Opna í nýjum flipa|Opnar hlutverkamiðstöð fyrir valið fyrirtæki í nýjum vafraglugga, heldur upprunalega fyrirtækinu opnu í hinum flipanum.|
   |Opna á nýjum flipa og fara á sömu síðu|Þessi valkostur er aðeins virkur á listasíðum, eins og viðskiptamönnum, sölupöntunum eða vörum. Hann opnar sama lista, en fyrir valið fyrirtæki, í nýjum vafraglugga. |

> [!TIP]
> Veljið  <kbd>F5</kbd>  til að endurnýja lista yfir umhverfi og fyrirtæki.

## <a name="use-the-app-launcher"></a>Nota forritavalmyndina

Þegar þú ert skráð(ur) inn á [!INCLUDE[prod_short](includes/prod_short.md)] eru umhverfin sem hægt er að opna aðgengilegt á Office.com.  

1. Veldu táknið **Forritavalmynd** ![Forritavalmynd.](media/app-launcher-icon.png "Forritavalmynd býður upp á aðgang að fleiri eiginleikum").
2. Í svæðinu sem opnast er hægt að leita að og velja [!INCLUDE[prod_short](includes/prod_short.md)]. Ef þú sérð ekki [!INCLUDE[prod_short](includes/prod_short.md)] skaltu velja **Öll forrit** og slá svo inn **Business Central** í reitinn **Leita**.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text="Microsoft 365 forritavalmyndin sem sýnir reit Business Central.":::  

3. Ef það eru fleiri en eitt umhverfi verður þú beðin(n) um að velja umhverfið sem á að opna.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## <a name="use-my-settings"></a>Nota mínar stillingar

Þegar þú ert skráð(ur) inn í [!INCLUDE[prod_short](includes/prod_short.md)] geturðu skipt yfir í annað fyrirtæki á fljótlegan hátt í sama umhverfinu. Þegar búið er að skipta yfir verður fyrirtækið sem þú velur sjálfgefið fyrirtæki og birtist næst þegar þú skráir þig inn.

1. Í efra hægra horninu skaltu velja **Stillingar** táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og velja síðan aðgerðina **Mínar stillingar**.

    > [!TIP]
    > Einnig er hægt að nota  <kbd>flýtiflýtilykla Alt</kbd>+<kbd>T</kbd>  til að opna síðuna stillingar.

2. Á síðunni **Mínar stillingar** á svæðinu **Fyrirtæki** er valið fyrirtæki.  
3. Velja hnappinn **Í lagi**.

> [!TIP]
> Góð aðferð við að fara beint í sjálfgefna fyrirtækið þegar þú skráir þig inn og ekki þurfa að tilgreina umhverfið er að bæta vefslóðinni á eftirlætislistann þinn eftir að þú skráir þig inn.

## <a name="use-company-hub"></a>Nota fyrirtækjamiðstöð

*Fyrirtækjamiðstöð* er mjög sérhæfð hlutverkamiðstöð sem gefur fjárhagslega yfirsýn yfir fyrirtæki og umhverfi. Fyrirtækjamiðstöðin er í boði sem [viðbót](ui-extensions-company-hub.md) og býður upp á stjórnborð með samantektargögnum fyrir hvert fyrirtæki sem þú hefur aðgang að. Heimasíðan sýnir fjármálatengda afkastavísa (KPI) og beinan tengil á stök umhverfi og fyrirtæki. Frekari upplýsingar er að finna í [Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md).

[![Sýnir síðu fyrirtækjamiðstöðvar sem sýnir öll fyrirtæki.](media/company-hub.png)](media/company-hub.png#lightbox)  

## <a name="see-also"></a>Sjá einnig .

[Stofna ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Umhverfi og fyrirtæki (aðeins enska)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Stofngögn](admin-company-information.md)  
[Stjórnunarmiðstöð Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
