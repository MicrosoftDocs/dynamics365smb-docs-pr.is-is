---
title: Yfirlit yfir Fyrirtækjaupplýsingar
description: 'Síða fyrirtækjaupplýsinga sýnir grunnupplýsingar um viðskiptaeiningu, t.d. nafn, aðsetur og sendingarupplýsingar.'
author: jswymer
ms.topic: conceptual
ms.search.form: 1
ms.date: 09/24/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="company-information-overview"></a>Yfirlit yfir Fyrirtækjaupplýsingar

[!INCLUDE[prod_short](includes/prod_short.md)] skipuleggur viðskiptaeiningar í *fyrirtækjum*. Fyrir hvert fyrirtæki þarf að fylla út nokkrar grunnupplýsingar um fyrirtækið og tilheyrandi upplýsingar á síðunni **Fyrirtækjaupplýsingar**. Upplýsingarnar á síðunni [**Fyrirtækjaupplýsingar**](https://businesscentral.dynamics.com/?page=1) eru notaðar í skjölum eins og fyrirsögnum reikninga. Hægt er að setja upp fleiri en eitt fyrirtæki, s.s. móðurfyrirtæki og dótturfyrirtæki.  

Ef birgðageymslur fyrirtækisins eru á öðrum stað en höfuðstöðvarnar er hægt að fylla út ýmsa sent-til-reiti og reitinn **Staðsetningarkóði** á flipanum **Afhending**. Síðan eru upplýsingarnar í þessum reitum til dæmis prentaðar á innkaupapantanir svo að lánardrottnar sendi vöru á réttan stað.  

Fyrir hvert fyrirtæki sem þú setur upp þarftu að fylla út síðuna **Fyrirtækjaupplýsingar** ásamt síðunni **Fjárhagsgrunnur**þ Einnig verður að setja upp hvert svæði fyrir sig í [!INCLUDE [prod_short](includes/prod_short.md)], eins og síðuna **Uppsetning sölugrunns** fyrir hvert fyrirtæki. Frekari upplýsingar eru í [Yfirlit yfir verkefni til að setja upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  

Á  **upplýsingasíðu**  fyrirtækisins eru mismunandi reitir og fastflipar eftir þínu landi/svæði. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir algengustu flýtiflipunum.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Þegar þú hefur lokið við að fylla út upplýsingarnar máttu loka síðunni.  

## <a name="working-with-multiple-companies"></a>Vinna með mörg fyrirtæki

Ef [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur mörg fyrirtæki gætu notendur þínir viljað nota *upplýsingatákn fyrirtækisins* til að sjá strax og halda utan um hvaða fyrirtæki þeir eru að vinna í hverju sinni. Frekari upplýsingar eru í [Birta upplýsingatákn fyrirtækis](#badge).

Það eru örfáir Eiginleikar sem þú getur notað til að skipta á milli fyrirtækja eftir því sem þú vinnur, líkt og fyrirtækið skipari (<kbd>CTRL</kbd>+<kbd>O</kbd>). Frekari upplýsingar eru í [Skipta yfir í annað fyrirtæki eða umhverfi](ui-organization-switch.md).

## <a name="display-a-company-badge"></a><a name="badge"></a>Sýna upplýsingatákn fyrirtækis

Þegar fleiri en eitt fyrirtæki eða umhverfi er til staðar sérðu fyrirtækjaskiptinn efst til hægri á forritastikunni nálægt leitartákninu á forritastikunni. Fyrirtækjaskiptirinn notar sjálfgefið staðlað fyrirtækistákn eins og ![ræsiforrit fyrirtækistákns](media/ui-experience/company-icon.png "Sýnir tákn fyrirtækjaskiptis sem notað er í einu umhverfi"). og ![fyrirtækistákn í fjölumhverfi](media/ui-experience/company-icon-multi-env.png "Sýnir tákn fyrirtækjaskiptis sem notað er í mörgum umhverfum").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Sýnir tákn fyrirtækjaskiptis í haus Business Central-biðlarans":::  

Byrjað í 2023 2, útgáfa 23, merki fyrirtækisins birtist í vafraflipanum þegar vefbiðlarinn er notaður. Það er einnig innifalið í síðutenglum sem þú  [afritar og klífur](across-share-data-features.md#copying-a-link)  í ritstýrður textar, eins og Word, Outlook og hópefli.
 
### <a name="set-the-company-badge"></a>Setja fyrirtækinu merki

Með því að nota síðuna **Fyrirtækjaupplýsingar** geturðu skipt út stöðluðu fyrirtækistákni fyrir sérsniðið upplýsingatákn fyrir hvert fyrirtækis fyrir sig ef upplýsingatáknið auðveldar notendum að bera kennsl á fyrirtækið sem þeir eru að vinna í.

1. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Fyrirtækismerki**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Við gerð skal endurnýja vafra (velja  <kbd>CTRL</kbd>+<kbd>F5</kbd>) til að uppfæra skjölin í biðlaranum.  

> [!NOTE]
> Fyrirtækjaskiptirinn var kynntur í 2022 útgáfutímabili 2, útgáfu 21. Í eldri útgáfum er upplýsingatákn fyrirtækisins ekki notað til að skipta á milli fyrirtækja. Það er sýnt efst til hægri á flestum síðum, jafnvel þótt aðeins eitt fyrirtæki sé til staðar. Ef það er valið birtist fullt heiti fyrirtækis og heiti umhverfis.

## <a name="change-company-display-name"></a>Breyta birtingarnafni fyrirtækis

Heiti fyrirtækisins er alltaf birt efst í vinstra horninu og virkar sem aðgerð sem hægt er að velja til að fara til baka í Mitt hlutverk. Þú getur breytt þessu heiti á síðunni **Upplýsingar um fyrirtækið**.

1. Veldu táknið ![Sprocket til að opna stillingavalmyndina.](media/ui-experience/settings_icon_small.png) táknið og veldu síðan aðgerðina **Upplýsingar um fyrirtæki**.
2. Heiti nýja fyrirtækisins er ritað í reitinn **Heiti**.
3. Fara af síðunni. Kerfið endurræsir og sýnir heitið á nýja fyrirtækinu í horninu efst til vinstri.

## <a name="experience"></a>Upplifun

Sjálfgefin upplifun notanda í [!INCLUDE [prod_short](includes/prod_short.md)] prufuútgáfunni sýnir ekki alla möguleika. Þú getur kveikt á allri upplifuninni á síðunni **Fyrirtækjaupplýsingar**. Frekari upplýsingar er að finna í [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).  

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir verkefni til að setja upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Stuttur leiðarvísir um fyrirtækjaupplýsingar](quick-start-company-information.md)  
[Setja upp upplýsingar um fyrirtæki á Ítalíu](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Stofna ný fyrirtæki](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
