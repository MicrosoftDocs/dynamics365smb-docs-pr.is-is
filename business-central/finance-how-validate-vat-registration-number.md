---
title: Staðfesta VSK-skráningarnúmer
description: Láta Business Central nota VIES-þjónustu til að villuleita VSK-númer sjálfkrafa.
author: kielkenny
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 80e955e96a64c5a0bd91d0a72297b32d67ff4ab6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750558"
---
# <a name="validate-vat-registration-numbers"></a>Staðfesta VSK-skráningarnúmer

Mikilvægt er að þau VSK-númer sem þú hefur fyrir viðskiptamenn, lánardrottna og tengiliði séu gild. Fyrirtæki breyta til dæmis stundum stöðu skattaskuldar hjá sér, og í sumum lönd gætu skattayfirvöld farið fram á að fá skýrslur, til dæmis skýrsluyfirlit um sölu innan Evrópubandalagsins, sem inniheldur VSK-númerin sem þú ert að nota við í viðskiptum.

Framkvæmdarstjórn Evrópusambandsins býður á vefsíðu sinni þjónustu VIES varðandi VSK Númerastaðfestingu, sem býðst öllum og er án endurgjalds. [!INCLUDE[prod_short](includes/prod_short.md)] getur sparað þér það skref og leyft þér að nota þjónustu VIES til að staðfesta og rekja VSK-númer viðskiptamanna, lánardrottna og tengiliði beint úr spjöldum viðskiptamaður, lánardrottinn og tengiliða. Þjónustan í [!INCLUDE[prod_short](includes/prod_short.md)] kallast **ESB VSK Skrá. Nr. Staðfestingarþjónusta**. Þjónustan er tiltæk í **Þjónustutengingar** síðunni og þú getur hafið notkun strax. Þjónustan er án endurgjalds og skráningar er ekki krafist.

## <a name="to-verify-vat-registration-numbers"></a>Staðfesta VSK-skráningarnúmer

Til að virkja **Sannprófa VSK-skráningarnúmer innan ESB** skal opna færsluna á síðunni **Þjónustutenging**. Þegar á að vera búið að fylla út í reitinn **Endastöð þjónustu**. Ef ekki er hægt að nota aðgerðina **Stilla sjálfgefna endastöð**. Því næst skal stilla reitinn **Virkjað** og þá er allt klárt.

> [!NOTE]
> Til að virkja VSK-skráningarnúmer innan ESB staðfestingarþjónustuna verður þú að hafa kerfisstjóraheimildir.

Þegar þjónustu okkar er notuð, skráum við ferill VSK-númera og VSK-staðfestinga fyrir hvern viðskiptamann, lánadrottinn eða tengiliðar, í reitnum **VSK Skráning Skrá**, þannig að þú getur auðveldlega rekja þá. Skráin á sérstaklega við hvern viðskiptamann. Til dæmis kemur skráin að gagni við að sanna það að þú hafir staðfest að gildandi VSK-númer séu réttar. Þegar VSK-númer er staðfest, mun **Biðja um kennimerki** dálkurinn í skránni endurspegla að þú hafir framkvæmt hlutinn.

Hægt er að skoða VSK-skráning skránna á spjöldunum fyrir viðskiptamann, lánardrottin eða tengilið, á **Reikningsfæra** Flýtiflipanum með því að velja hnappinn uppfletting á **VSK-númer**  

Okkar þjónustu getur einnig sparað þér tíma þegar verið er að stofna viðskiptamann eða lánardrottin. Ef þú veist VSK-númer viðskiptamanns, geturðu fært það inn í reitinn **VSK-númer** á spjöldum viðskiptamanns eða lánardrottins, og við fyllum út nafn viðskiptamanns fyrir þig. Sumar lönd bjóða einnig upp á aðsetur fyrirtækis á skipulögðu sniði. Í þeim löndum, munum við fylla út aðsetur líka.  

Það eru nokkur atriði sem vert er að athuga varðandi þjónustu VIES á VSK-númerastaðfestingu:

* Þjónustan notar http-reglur, sem táknar að gagnaflutningur um þjónustuna er ekki dulkóðaður.  
* Þú getur upplifað óvirkan tíma í þessari þjónustu sem Microsoft er ekki ábyrgt fyrir. Þjónustan er hluti af víðfemu ESB skráningarkerfi VSK-númera.

> [!IMPORTANT]
> Það er á þína ábyrgð að kanna hvort gögnin séu gildi. Af og til er gögnum með villum skilað af VIES sannprófunarþjónustu fyrir VSK-númer. Ef sannprófun tekst ekki, skal sannprófa VSK-númerin á [vefsvæðinu](https://ec.europa.eu/taxation_customs/vies/), prenta út niðurstöðuna eða vista hana á samnýtt svæði og síðan bæta tenglinum við færsluna fyrir viðskiptamanninn, lánardrottin eða tengiliðinn. Frekari upplýsingar er að finna í [Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum](ui-how-add-link-to-record.md).

## <a name="see-also"></a>Sjá einnig

[Setja upp virðisaukaskatt](finance-setup-vat.md)  
[Uppsetning á óinnleystum virðisaukaskatti](finance-setup-unrealized-vat.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Staðbundin virkni í Business Central](about-localization.md)  
