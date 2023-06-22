---
title: Staðfesta VSK-skráningarnúmer
description: 'Leyfið Business Central að staðfesta VSK-númer fyrir tengiliði þína, viðskiptamenn og lánardrottna samkvæmt VIES-þjónustu Evrópusambandsins fyrir staðfestingu VSK-númers.'
author: andregu
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '249, 575, 1279'
ms.date: 06/16/2021
ms.author: andregu
---

# <a name="validate-vat-registration-numbers" />Staðfesta VSK-skráningarnúmer

Mikilvægt er að þau VSK-númer sem þú hefur fyrir viðskiptamenn, lánardrottna og tengiliði séu gild ef þú notar [!INCLUDE [prod_short](includes/prod_short.md)] í landi með VSK. Fyrirtæki breyta til dæmis stundum stöðu skattaskuldar hjá sér, og í sumum lönd gætu skattayfirvöld farið fram á að fá skýrslur, til dæmis **EB-söluyfirlitsskýrslu**, sem inniheldur VSK-númerin sem þú ert að nota við í viðskiptum.

Framkvæmdarstjórn Evrópusambandsins býður á vefsíðu sinni þjónustu VIES varðandi VSK Númerastaðfestingu, sem býðst öllum og er án endurgjalds. [!INCLUDE [prod_short](includes/prod_short.md)] getur sparað þér það skref og leyft þér að nota þjónustu VIES til að staðfesta og rekja VSK-númer og aðrar fyrirtækjaupplýsingar fyrir viðskiptamenn, lánardrottna og tengiliði. Þjónustan í [!INCLUDE [prod_short](includes/prod_short.md)] kallast **ESB VSK Skrá. Nr. Staðfestingarþjónusta**. Þjónustan er tiltæk í **Þjónustutengingar** síðunni og þú getur hafið notkun strax. Þjónustutengingin er án endurgjalds og viðbótarskráningar er ekki krafist.

## <a name="configure-the-service-to-verify-vat-registration-numbers-automatically" />Skilgreina þjónustuna til að staðfesta skráningu VSK-númera sjálfkrafa

Til að virkja **Sannprófa VSK-skráningarnúmer innan ESB** skal opna færsluna á síðunni **Þjónustutenging**. Ef reiturinn **Endastöð þjónustu** er ekki þegar fylltur út skal nota aðgerðina **Stilla sjálfgefna endastöð**. Því næst skal stilla reitinn **Virkjað** og þá er allt klárt.  

> [!IMPORTANT]
> Til að virkja staðfestingarþjónustu verður þú að hafa kerfisstjóraheimildir.

Einnig er hægt að setja upp sniðmát fyrir gerðir VSK-tengdra gagna sem ætlunin er að þjónustan athugi líka. Frekari upplýsingar er að finna í hlutanum [Sniðmát fyrir villuleit](#validation-templates).

Þegar þjónustu okkar er notuð, skráum við ferill VSK-númera og VSK-staðfestinga fyrir hvern viðskiptamann, lánadrottinn eða tengiliðar, í reitnum **VSK Skráning Skrá**, þannig að þú getur auðveldlega rekja þá. Skráin á sérstaklega við hvern viðskiptamann. Til dæmis kemur skráin að gagni við að sanna það að þú hafir staðfest að gildandi VSK-númer séu réttar. Þegar VSK-númer er staðfest, mun **Biðja um kennimerki** dálkurinn í skránni endurspegla að þú hafir framkvæmt hlutinn.

Hægt er að skoða VSK-skráning skránna á spjöldunum fyrir viðskiptamann, lánardrottin eða tengilið, á **Reikningsfæra** Flýtiflipanum með því að velja hnappinn uppfletting á **VSK-númer**  

Það eru nokkur atriði sem vert er að athuga varðandi þjónustu VIES á VSK-númerastaðfestingu:

* Þjónustan notar http-reglur, sem táknar að gagnaflutningur um þjónustuna er ekki dulkóðaður.  
* Þú getur upplifað óvirkan tíma í þessari þjónustu sem Microsoft er ekki ábyrgt fyrir. Þjónustan er hluti af víðfemu ESB skráningarkerfi VSK-númera.

> [!IMPORTANT]
> Það er á þína ábyrgð að kanna hvort gögnin séu gildi. Af og til er gögnum með villum skilað af VIES sannprófunarþjónustu fyrir VSK-númer. Ef sannprófun tekst ekki, skal sannprófa VSK-númerin á [vefsvæðinu](https://ec.europa.eu/taxation_customs/vies/), prenta út niðurstöðuna eða vista hana á samnýtt svæði og síðan bæta tenglinum við færsluna fyrir viðskiptamanninn, lánardrottin eða tengiliðinn. Frekari upplýsingar er að finna í [Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum](ui-how-add-link-to-record.md).

## <a name="validation-templates" />Sniðmát fyrir villuleit

Hægt er að nota VIES-þjónustu til að athuga einnig aðrar upplýsingar um fyrirtæki, á borð við heimilisfang sem og skráningu VSK-númers. Á síðunni **Sniðmát fyrir staðfestingu VSK-skráningarnr.** skal stofna færslu fyrir hvert land sem á að fá frekari staðfestingu frá og síðan tilgreina upplýsingarnar sem á að fá sjálfkrafa staðfestar.  

Bætið til dæmis við færslu fyrir Spán þar sem ætlunin er að fá staðfestingu á nafni, götu, borg og póstnúmeri og síðan annarri færslu fyrir Þýskaland þar sem ætlunin er að fá aðeins staðfestingu á póstnúmeri, sem dæmi. Því næst á síðunni **Uppsetning sannprófunarþjónustu fyrir VSK-númer innan ESB** skal tilgreina sjálfgefið sniðmát.  

> [!NOTE]
> Gakktu ávallt úr skugga um að sjálfgefið sniðmát virki fyrir þínar þarfir. Hægt er að breyta sjálfgildi til að uppfylla kröfur, t.d. sannprófa alla reiti eða enga reiti.

Næst þegar VSK-númer er tilgreint mun þjónustan staðfesta númerið og bæta við frekari gögnum eftir því hvað kemur fram í staðfestingarsniðmátunum. Ef tilgreind gildi eru mismunandi frá gildunum sem þjónustan skilar, koma upplýsingarnar fram á síðunni **Upplýsingar um staðfestingu** þar sem hægt er að samþykkja eða endurstilla gildin.  

## <a name="see-also" />Sjá einnig

[Setja upp virðisaukaskatt](finance-setup-vat.md)  
[Uppsetning á óinnleystum virðisaukaskatti](finance-setup-unrealized-vat.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Staðbundin virkni í Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
