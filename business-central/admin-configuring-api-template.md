---
title: "Grunnstilling API-sniðmáta | Microsoft Docs"
description: "Lýsir skrefunum sem þú verður að taka til að grunnstilla API sniðmát fyrir Dynamics 365 Business Central."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 05/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 1695a6950dabc1b2f0a2f85ad9e0c565012c92e1
ms.contentlocale: is-is
ms.lasthandoff: 05/17/2018

---

# <a name="configuring-api-templates"></a>Grunnstilling API-sniðmáta
API-safnið fyrir [!INCLUDE[d365fin_md](includes/d365fin_md.md)] gefur einfaldaða framsetningu á undirliggjandi einingum. Allir eiginleikarnir í forritinu fara ekki í gegnum tengt API. Glugginn **API-uppsetning** gerir þér kleift að skilgreina sniðmát sem eru notuð til að fylla í tóma eiginleika í einingu þegar þú býrð til POST-aðgerð í gegnum API. 

Til dæmis, ef grunnstillingarsniðmát er skilgreint fyrir vörueininguna, þegar ný vörufærsla er stofnuð í gegnum vörur API, verður fyllt í alla eiginleika nýju vörunnar sem ekki eru skilgreindir í API-kallinu út frá valda sniðmátinu. Ef til dæmis ekkert gildi er skilgreint fyrir reitinn **Alm. vörubókunarflokkur** í gegnum API, en gildi er skilgreint í valda sniðmátinu, þá verður gildi bókunarflokksins sem er skilgreint í sniðmátinu notað fyrir nýju vöruna. 

## <a name="setting-up-the-entity-template"></a>Uppsetning sniðmátseiningar
Til að nota sniðmát með API-safninu verður þú fyrst að setja upp og skilgreina eiginleika fyrir sniðmátið. Hægt er að setja upp þessi sniðmát í glugganum **Grunnstillingarsniðmát**. Frekari upplýsingar eru í [Undirbúa flutning á gögnum viðskiptamanns](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Úthluta sniðmátinu á API

Til að úthluta API sniðmáti verður þú að fara í gegnum eftirfarandi skref.

1. Veljið táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), sláið inn **API-uppsetning** og veljið viðeigandi tengil.
2. Veljið **Nýtt** og veljið síðan gildið á **Röðun** fyrir færsluna.  
Ef fleiri en eitt sniðmát er valið fyrir API (síðukenni) eru sniðmátin notuð í þeirri röð sem er skilgreind í dálknum **Röðun**.   
Þegar hvert sniðmát er notað eru reitargildum sem eru skilgreind í sniðmátinu aðeins beitt á reiti sem hafa ekki enn fengið gildi skilgreint, annaðhvort sérstaklega í API eða í sniðmáti sem notað var áður í röðinni. 
3. Veljið gildi fyrir **Síðukenni**.  
Þetta er síðan fyrir API sem sniðmátið verður beitt á. Uppflettingin **Síðukenni** býður upp á lista af öllum API sem eru í boði í safninu.
4. Veljið gildi í reitnum **Sniðmátskóði**.  
Sniðmátskóðinn er kóðinn fyrir sniðmátið sem var skilgreint í glugganum **Grunnstillingarsniðmát**. Skilgreindum sniðmátsgildum er beitt á API. 
5. Í reitnum **Skilyrði** skal tilgreina hvaða sniðmátum eigi að beita.  
Skilgreindu sniðmáti er beitt á nýja færslu sem er stofnuð í gegnum API, en eingöngu ef skilyrðin sem eru skilgreind í reitnum **Skilyrði** eru uppfyllt af gildunum sem þegar eru skilgreind fyrir nýja tilvikið af einingunni.

## <a name="see-also"></a>Sjá einnig
[Fylgiskjöl API](/dynamics-nav/fin-graph)  
[Þróun á tengiforritum fyrir [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Virkja API](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Endastöðvar fyrir API](/dynamics-nav/endpoints-apis-for-dynamics)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)