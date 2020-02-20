---
title: Flytja gögn frá Dynamics GP með Gagnaflutningaviðbótinni | Microsoft Docs
description: Notaðu Dynamics GP-Gagnaflutningaviðbótina til að flytja viðskiptamenn, lánardrottna, birgðavörur, fjárhagsreikninga, opnar viðskiptaskuldir og opnar viðskiptakröfur færslur frá Dynamics GP til Business Central.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 01/16/2020
ms.author: edupont
ms.openlocfilehash: b05959eea09289db7878145347362786ab336de8
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992146"
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Dynamics GP-Gagnaflutningaviðbótin 
Þessi viðbót gerir það auðvelt að flytja viðskiptamenn, lánardrottna, birgðavörur, fjárhagsreikninga, opnar viðskiptaskuldir og færslur opinna viðskiptakrafna frá Dynamics GP til [!INCLUDE[prodshort](includes/prodshort.md)]. Ef fyrirtækið þitt notar Dynamics GP í dag getur þú flutt út viðeigandi skrár og síðan opnað leiðbeiningar um uppsetningu með hjálp til að bæta gögnunum við [!INCLUDE[prodshort](includes/prodshort.md)]. Flutningsviðbótin virkar fyrir allar studdar útgáfur af Microsoft Dynamics GP. Nánari upplýsingar eru í [Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md).

> [!NOTE]
>  Viðbótin verður úrelt í uppfærslu 15.3. Mælt er með því að notendur sem vilja flytja úr Dynamics GP byrji að nota leiðsagnarforritið **Flutningur í ský** í staðinn. Viðbótin **Flutningur í ský** er með öflugri virkni og færir meiri gögn í Business Central úr Dynamics GP.

## <a name="exporting-data-from-dynamics-gp"></a>Flytja út gögn úr Dynamics GP
Þú verður að hafa flutt út nokkra eða alla núverandi viðskiptamenn, lánardrottna, birgðavörur, og fjárhagsreikninga með því að nota gagnaútflutningsvirkni innan Dynamics GP. Þegar þú velur gögnin til að flytja út, er hægt að velja eftirfarandi gerðir:

* Reikningur  
* Viðskiptavinur  
* Atriði  
* Lánardrottinn  

Þegar útflutningsskráin er búin til verður þú með zip-skrá sem inniheldur nokkra txt-skrár sem verða ákvörðuð af því sem þú valdir í útflutningsgagnaferlinu.  Það verður einnig fleiri txt-skrár sem eru búnar til, sem innihalda stuðningsupplýsingar sem eru nauðsynlegar við uppsetningu innan nýju [!INCLUDE[prodshort](includes/prodshort.md)] fyrirtækisins þíns.

Dynamics GP Data Migration viðbót varpar sjálfkrafa útfluttm gögn þannig að þú hafir skjótan aðgang að gögnunum þínum í nýja [!INCLUDE[prodshort](includes/prodshort.md)] fyrirtækinu.

## <a name="whats-new-in-the-october-2018-release"></a>Hvað er nýtt í útgáfu október 2018

Í þessari útgáfu, höfum við stækkað gagnamagnið sem við setjum inn í [!INCLUDE[prodshort](includes/prodshort.md)] frá Dynamics GP.

Í leiðsagnarforriti fyrir flutning getur þú valið hvernig þú vilt flytja Dynamics GP bókhaldslykilinn. Þú getur flutt fyrirliggjandi bókhaldslykil eða þú getur búið til nýtt bókhaldslykil sem byggjast á fyrirliggjandi bókhaldslykil.  

Ef þú velur að nota fyrirliggjandi bókhaldslykil verður reikningarnir settir upp sem aðalreikningshluti frá Dynamics GP og viðbótarhlutarnir verða settar upp sem víddir innan [!INCLUDE[prodshort](includes/prodshort.md)].  

Ef þú velur að búa til nýtt bókhaldslykil færðu viðbótarsíðu með reikningsupplýsingar í leiðsagnarforritinu svo þú getir sótt vinnubókina, gert viðeigandi breytingar og síðan flutt vinnubókin aftur til að breyta reikningunum þínum.  

Þú verður að hlaða niður Excel-vinnubókinni og tengja nýjan reikningsnúmer við sérhvert reikningsnúmer í Excel-töflureikninum. Hver reikningur verður að hafa sitt eigið númer eða flutningurinn tekst ekki. Þegar þú hefur lokið vörpuninni getur þú haldið áfram í gegnum leiðsagnarforritið fyrir flutning með því að flytja inn Excel-vinnubókina sem þú hefur nýlega uppfært. Leiðsagnarforritið staðfestir að hverja röð hafi sérstakt reikningsnúmer og að engar raðir séu með tómt nýtt reikningsnúmer í þeim.  

Með breytingunni á valkostum fyrir vörpun bókhaldslykils, munt þú einnig taka eftir breytingu á gerð gagna sem koma yfir í færslubókina fyrir reikningsnúmerin.  

- Ef þú velur að nota núverandi reikningsnúmer munum við færa upphafsstöðu aðalhlutans (nýtt reikningsnúmer) sem samantekt á aðalreikningsnúmeri þegar flutningur fer fram.  
- Ef þú velur að búa til ný reikningsnúmer, munum við færa samantektarupplýsingar um samsvarandi tvö reikningsár miðað við reikningsskilatímabilið sem þú hefur sett upp í Dynamics GP.

Í fyrri útgáfum af [!INCLUDE[prodshort](includes/prodshort.md)] flutti leiðsagnarforritið yfirlitsfærslu fyrir viðskiptamenn/lánardrottinn stöðuna í Dynamics GP. Nú færum við inn ítarlegar opnar færslur fyrir viðskiptamenn og lánardrottna þegar flutningur fer fram. Hvað þýðir það? Ef viðskiptamaður þinn hefur 3 útistandandi færslur sem eru skráðir í kerfiseiningu viðskiptakrafna, færir leiðsagnarforritið þessar færslur inn í [!INCLUDE[prodshort](includes/prodshort.md)] með útistandandi upphæð sem upphæð í skjali. Þetta er það sama fyrir kerfiseiningu viðskiptaskulda fyrir lánardrottna.  

Birgðavörur eru fluttar inn með kostnaðarmatsaðferðinni sem var valin þegar leiðsagnarforrit uppsetningar fyrirtækisins var keyrður. Þjónustuvörum er sjálfkrafa úthlutað FIFO-matsaðferðinni. Sem stendur færum við inn Magn á lager fyrir vörurnar þegar flutningur fer fram.  Þetta magn er fært inn í auða birgðageymsluna.  

Síðasti valkosturinn sem þú sérð í leiðsagnarforriti fyrir gagnaflutning í Dynamics GP er eiginleikinn að tilgreina bókunarvalkostinn þinn. Þessi stilling tilgreinir hvort þú viljir sjálfkrafa bóka allar færslur í færslubækurnar um leið og flutningurinn færir gögnin inn í [!INCLUDE[prodshort](includes/prodshort.md)] eða ef þú vilt bóka handvirkt þannig að allar færslur muni sitja í runum á færslubókarsíðunni, svo þú getir staðfest upplýsingarnar áður en þú bókar. Þessi valkostur er sýnilegur á síðunni sem inniheldur valkosti fyrir Bókhaldslykla.


## <a name="see-also"></a>Sjá einnig
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Sérstilling [!INCLUDE[prodshort](includes/prodshort.md)] með viðbótum ](ui-extensions.md)  
