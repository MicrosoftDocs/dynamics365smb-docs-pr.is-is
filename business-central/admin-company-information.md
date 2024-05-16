---
title: Yfirlit yfir stofngögn
description: 'Síða fyrirtækjaupplýsinga sýnir grunnupplýsingar um viðskiptaeiningu, t.d. nafn, aðsetur og sendingarupplýsingar.'
author: jswymer
ms.topic: conceptual
ms.search.form: 1
ms.date: 04/24/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Yfirlit yfir stofngögn

[!INCLUDE[prod_short](includes/prod_short.md)] skipuleggur viðskiptaeiningar í *fyrirtækjum*. Fyrir hvert fyrirtæki þarf að fylla út nokkrar grunnupplýsingar um fyrirtækið og tilheyrandi upplýsingar á síðunni **Fyrirtækjaupplýsingar**. Upplýsingarnar á síðunni [**Fyrirtækjaupplýsingar**](https://businesscentral.dynamics.com/?page=1) eru notaðar í skjölum eins og fyrirsögnum reikninga. Hægt er að setja upp fleiri en eitt fyrirtæki, s.s. móðurfyrirtæki og dótturfyrirtæki.  

Ef birgðageymslur fyrirtækisins eru á öðrum stað en höfuðstöðvarnar er hægt að fylla út ýmsa sent-til-reiti og reitinn **Staðsetningarkóði** á flipanum **Afhending**. Upplýsingarnar í þessum reitum eru síðan prentaðar á innkaupapantanir, svo að lánardrottnar sendi vörur á réttan stað.  

Fyrir hvert fyrirtæki sem þú setur upp þarftu að fylla út síðuna **Fyrirtækjaupplýsingar** ásamt síðunni **Fjárhagsgrunnur**þ Einnig verður að setja upp hvert svæði fyrir sig í [!INCLUDE [prod_short](includes/prod_short.md)], eins og síðuna **Uppsetning sölugrunns** fyrir hvert fyrirtæki. Frekari upplýsingar eru í [Yfirlit yfir verkefni til að setja upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  

Á **síðunni Stofngögn** eru mismunandi reitir og flýtiflipar, allt eftir landi/svæði notanda. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir algengustu flýtiflipunum.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Þegar upplýsingarnar hafa verið færðar inn er hægt að loka síðunni.  

## Vinna með mörg fyrirtæki

Ef [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur mörg fyrirtæki gætu notendur þínir viljað nota *upplýsingatákn fyrirtækisins* til að sjá strax og halda utan um hvaða fyrirtæki þeir eru að vinna í hverju sinni. Frekari upplýsingar eru í [Birta upplýsingatákn fyrirtækis](#badge).

Nokkrar aðgerðir eru í boði til að skipta milli fyrirtækja um leið og unnið er, eins og rofi fyrirtækisins (<kbd>Ctrl</kbd>+<kbd>O</kbd>). Frekari upplýsingar eru í [Skipta yfir í annað fyrirtæki eða umhverfi](ui-organization-switch.md).

## <a name="badge"></a>Sýna upplýsingatákn fyrirtækis

Þegar fleiri en eitt fyrirtæki eða umhverfi er til staðar sýnir rofi fyrirtækisins efst til hægri á forritastikunni nálægt leitartákninu. Fyrirtækjaskiptirinn notar sjálfgefið staðlað fyrirtækistákn eins og ![ræsiforrit fyrirtækistákns](media/ui-experience/company-icon.png "Sýnir tákn fyrirtækjaskiptis sem notað er í einu umhverfi"). og ![fyrirtækistákn í fjölumhverfi](media/ui-experience/company-icon-multi-env.png "Sýnir tákn fyrirtækjaskiptis sem notað er í mörgum umhverfum").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Sýnir tákn fyrirtækjaskiptis í haus Business Central-biðlarans":::  

Hafist er handa í 2023 útgáfu bylgju 2, útgáfa 23, birtist merki fyrirtækisins í vafraflipanum þegar vefbiðlarinn er notaður. Það er einnig í síðutenglum sem þú [afritar og límir í ríkum](across-share-data-features.md#copying-a-link) textaritlum, eins og Word, Outlook og Teams.

Eftirfarandi myndband sýnir hvernig á að vinna með merki fyrirtækisins.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2PC]
 
### Stilla fyrirtækismerki

Með því að nota síðuna **Fyrirtækjaupplýsingar** geturðu skipt út stöðluðu fyrirtækistákni fyrir sérsniðið upplýsingatákn fyrir hvert fyrirtækis fyrir sig ef upplýsingatáknið auðveldar notendum að bera kennsl á fyrirtækið sem þeir eru að vinna í.

1. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Fyrirtækismerki**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Þegar þessu er lokið er vafrinn endurnýjaður (Ctrl <kbd>F5</kbd>+<kbd>) valið</kbd> til að uppfæra skjöldinn í biðlaranum.  

> [!NOTE]
> Fyrirtækjaskiptirinn var kynntur í 2022 útgáfutímabili 2, útgáfu 21. Í eldri útgáfum er upplýsingatákn fyrirtækisins ekki notað til að skipta á milli fyrirtækja. Það er sýnt efst til hægri á flestum síðum, jafnvel þótt aðeins eitt fyrirtæki sé til staðar. Ef það er valið birtist fullt heiti fyrirtækis og heiti umhverfis.

## Breyta birtingarnafni fyrirtækis

Heiti fyrirtækisins er alltaf birt efst í vinstra horninu og virkar sem aðgerð sem hægt er að velja til að fara til baka í Mitt hlutverk. Þú getur breytt þessu heiti á síðunni **Upplýsingar um fyrirtækið**.

1. Veldu táknið ![Sprocket til að opna stillingavalmyndina.](media/ui-experience/settings_icon_small.png) táknið og veldu síðan aðgerðina **Upplýsingar um fyrirtæki**.
2. Heiti nýja fyrirtækisins er ritað í reitinn **Heiti**.
3. Fara af síðunni. Kerfið endurræsir og sýnir heitið á nýja fyrirtækinu í horninu efst til vinstri.

## Upplifun

Sjálfgefin upplifun notanda í [!INCLUDE [prod_short](includes/prod_short.md)] prufuútgáfunni sýnir ekki alla möguleika. Þú getur kveikt á allri upplifuninni á síðunni **Fyrirtækjaupplýsingar**.  

Nánari upplýsingar eru í [Breyta hvaða eiginleikar eru birtir](ui-experiences.md).  

## Sjá einnig .

[Yfirlit yfir verkefni til að setja upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Stuttur leiðarvísir um fyrirtækjaupplýsingar](quick-start-company-information.md)  
[Setja upp upplýsingar um fyrirtæki á Ítalíu](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Stofna ný fyrirtæki](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
