---
title: Samnýtingu gagna
description: Fræðast um mismunandi leiðir til að deila viðskipagögnum úr Viðskiptamiðinu.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 09/21/2022
ms.author: jswymer
ms.openlocfilehash: e54cabd331253a40b160a6cc89b4ab170bd1db89
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607473"
---
# <a name="sharing-business-data-from-business-central"></a>Hlutdeild Viðskipagagna frá Viðskiptamiðinu

Samvinna fólks innan og utan fyrirtækis er óaðskiljanlegur hluti flestra fyrirtækja. [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á nokkra möguleika fyrir samnýtingu viðskipdata, líkt og lista yfir færslur, tilteknar færslur eða skjöl. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Með öllum þessum aðgerðum er aðgangur að gögnum varin með leyfi og heimildir rekstraraðila miðlægu.

## <a name="copying-a-link"></a>Að afrita tengil

![Stutt](media/check.png) Viðskipti miðsvæðis á netinu ![Stutt](media/check.png) Rekstur miðsvæðis innanhúss

Frá hvaða síðu sem er getur þú afritað slóð síðunnar, síðan límt og dreift henni í annars konar miðlum eins og tölvupóstum, teymum spjalli eða textaskilaboðum. Auðveldasta leiðin til að afrita tengil er að með því að velja **Share** > **Copy hlekk** efst á síðunni. Önnur leið er að afrita SLÓÐINA beint úr nafnakassa vafrans.

### <a name="modify-the-page-link"></a>Breyta síðu tengils

Þegar búið er að afrita tengil, áður en það er sent, er hægt að breyta SLÓÐINNI til að vinna úr því sem sést þegar síðan opnast. Til dæmis er hægt að bæta við síum eða tilgreina annað fyrirtæki.

Frekari upplýsingar er að finna [á Vefbiðlaraslóðinni](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### <a name="about-filtered-lists"></a>Um síaða lista

Með því að nota síurúðuna á listasíðum er hægt að nota afmarkanir til að þrengja færslurnar sem sýndar eru á listanum. Ef afritunartengill **er notaður** eða afritað úr vafranum tekur síðutengill ekki með sér breytingar á síðunni. Notendur sem opna tengilinn sjá fullt safn. Leiðin til að geyma síuna á söfnunarsíðu hlekki er að vista síaða síðu sem **Sýn** fyrst. Því næst skaltu opna Úrið og afrita tengilinn þaðan.

Nánari upplýsingar er að finna í [Flokkun, leit og síun](ui-enter-criteria-filters.md).

## <a name="sharing-to-teams"></a>Samnýting á teymum

![Stutt](media/check.png) Viðskipti miðsvæðis á netinu ![Ekki studd](media/x-icon.png) Rekstur miðsvæðis innanhúss

Beint af flestum söfnuninni og upplýsingasíðunum er hægt að senda tengil á síðuna á fólk, flokka spjall eða rásir. Deildu t.d. tengli í afmarkað yfirlit yfir færslurnar þínar. Ef þú hefur sett upp [!INCLUDE[prod_short](includes/prod_short.md)] App fyrir hópana þá stækkar hlekkurinn sjálfkrafa í geisladisk til að þú fylgir með skilaboðunum þínum. Viðtakendur velja síðan tengilinn eða kortið til að opna síðuna í Viðskiptamiðinu.

Frekari upplýsingar [fást í Samnýting færslna og Síðutenglum í teymum](across-working-with-teams.md).

## <a name="sharing-through-onedrive"></a>Hlutdeild í gegnum OneDrive

![Stutt](media/check.png) Viðskipti miðsvæðis á netinu ![Stutt](media/check.png) Rekstur miðsvæðis innanhúss

Viðskiptamiðlæg gerir það auðvelt að geyma, stjórna og samnýta skrár með öðru fólki í gegnum OneDrive fyrir fyrirtæki. Á flestum síðum þar sem skrár eru tiltækar, svo sem í Skýrsluinnhólfinu eða skrám sem tengdar eru færslum, er hægt að **finna opnu í OneDrive** og **samnýta** Aðgerðir. Báðar aðgerðirnar vista afrit af skrá á OneDrive. Þegar inn OneDrive er komið er hægt að nota það fyrir samnýtingu og framlegmöguleika á skránni. Munurinn á aðgerðunum er sá að **OneDrive** opnar skrána í OneDrive. **Deildu** opnar síðu við skulum velja hver á að deila skránni með. Viðtakendur munu fá tilkynningu í tölvupósti um að nálgast skrána frá OneDrive kl.

Frekari upplýsingar fást [í Samnýting skráa í OneDrive](across-share-onedrive.md).

## <a name="opening-in-excel"></a>Opnun í Excel

![Stutt](media/check.png) Viðskipti miðsvæðis á netinu ![Stutt](media/check.png) Rekstur miðsvæðis innanhúss

Ef listasíður og listar eru innfelldir á síðu er hægt að **nota Open í aðgerð í Excel**. Þessi aðgerð flytur lista yfir skráningar í Excel vinnubók (. xlsx File), sem hægt er að samnýta með öðrum. Í vinnubókinni er einnig hægt að nota hlutaaðgerðina sem er hluti af Excel.

Nánari upplýsingar er að finna [í Skoða og breyta í Excel](across-work-with-excel.md).

## <a name="sharing-rows-or-tables"></a>Samnýtingarlínur eða töflur

![Stutt](media/check.png) Viðskipti miðsvæðis á netinu ![Stutt](media/check.png) Rekstur miðsvæðis innanhúss

Hægt er að samnýta eina eða fleiri færslur í lista. Ýttu á flýtivísunina CTRL + C til að afrita á klemmuspjaldið þitt. Límið síðan það sem þú afritaðir í annað forrit með því að ýta á Ctrl + V. Til dæmis, afritun á þremur sölupöntunum og líma sem inn á tölvupóst birtast pöntunum í fallega niðrá töflu.

Frekari upplýsingar [fást í Copy og PASTE FAQ](faq-copy-paste.yml).

## <a name="see-also"></a>Sjá einnig

[Business Central og OneDrive samþætting](across-onedrive-overview.md)  
[Stjórnun OneDrive samþættingar við Business Central](admin-onedrive-integration.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)