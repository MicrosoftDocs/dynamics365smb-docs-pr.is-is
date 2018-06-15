---
title: "Úthluta eða breyta notendaheimild | Microsoft Docs"
description: "Lýsir því hvernig skal bæta Office 365 notendum við Business Central, og svo úthluta heimildum, aðgangsréttindum og öryggisstillingum."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 05/24/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: 443c04799e9aa2b9aa4ede15006ecb5e9773ce6b
ms.contentlocale: is-is
ms.lasthandoff: 05/28/2018

---
# <a name="manage-users-and-permissions"></a>Vinna með notendur og heimildir
Til að bæta notendum í [!INCLUDE[d365fin](includes/d365fin_md.md)], verður kerfisstjóri Office 365 í fyrirtækinu fyrst að stofna notendur í stjórnstöð Office 365. Frekari upplýsingar, sjá [Bæta notendum við Office 365 fyrir fyrirtæki](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Þegar notendur hafa verið stofnaðir í Office 365 er hægt að flytja þá inn í gluggann **notendur** með því að velja aðgerðina **Sækja notendur úr Office 365** Notendum er úthlutað heimildarsöfnum samkvæmt áætlun sem notandanum er úthlutað í Office 365.

Má því næst úthluta notendum heimildarsöfnum til að skilgreina hvaða hluti úr gagnagrunni, og þar með hvaða einingar Viðmótsins, þeir hafa aðgang að og í hvaða fyrirtækjum. Þú getur bætt notendum við notendahópa. Þannig er auðveldara að úthluta sama heimildarsöfn á mörgum notendum.

Heimildasafn er safn heimildir fyrir tiltekna hluti í gagnagrunninum. Öllum notendum verða að hafa verið úthlutað eitt eða fleiri heimildasöfn áður en þeir geta opnað [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nokkur fyrirfram skilgreind heimildasöfn eru veitt sjálfvirkt.  

Stjórnendur geta notað **Notandauppsetningu** gluggann til að skilgreina tímabil þegar tilgreindir notendur geta bókað, og geta einnig tilgreint hvort kerfið skrái tímann sem notandinn er skráður inn.

Annað kerfi sem skilgreinir hvað notendur geta nálgast er upplifunarstillingin. Frekari upplýsingar, sjá [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Að úthluta notanda heimild
1. Velja skal táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Notendur** og velja svo viðeigandi tengil.
2. Veldu notandann sem á að úthluta á þessum viðskiptamanni til.
Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu **breyta** aðgerðina til að opna gluggann **Notandapjald** .
4. Á flýtiflipanum **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Til hópnotenda í notandaflokkum
Þú getur sett upp notendahópa til að hjálpa þér að stjórna heimildasamstæðum fyrir hópa notenda í fyrirtæki þínu.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notandaflokkar** og velja svo viðeigandi tengil.
2. Einnig, í glugganum **Notendur**, veldu aðgerðina **Notandaflokkar**.
3. Í glugganum **Notandaflokkur** er valin aðgerðin **Meðlimir notandaflokks**.
6. Í glugganum **Meðlimir notandaflokks** er valin aðgerðin **Bæta við notendum**.
7. Til að bæta nýjum eða fleiri heimildarsöfnum, velurðu í glugganum **Notandahópar** aðgerðina **Heimildarsöfn notandahóps**.
8. Í glugganum **Heimildarsöfn notandahópa** er í nýrri línu fyllt í reitina eftir þörfum með því að velja úr heimildarsöfnum sem þegar eru til staðar.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Til að afrita notendaflokk og öll heimildarsöfn
Til að fljótt skilgreina nýja notendaflokka geturðu afritað öll heimildarsöfn frá núgildandi notendaflokki yfir í nýjan notendaflokk.

Meðlimir úr notendaflokki eru ekki afritaðar í nýja notendaflokkinn. Þú verður að bæta þeim við handvirkt eftir á.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notandaflokkar** og velja svo viðeigandi tengil.
2. Veldu notendaflokkinn sem þú vilt afrita og veldu síðan aðgerðina **Afrita notendaflokk**.
3. Í reitinn **Nýr kóði notendaflokks** skal færa inn heiti fyrir flokkinn og velja síðan hnappinn **Í lagi**.

Nýja notendaflokknum er bætt við gluggann **Notendaflokkar**. Halda áfram að bæta við notendum. Nánari upplýsingar er að finna í kaflanum „Að flokka notendur í notendaflokka“.

## <a name="to-set-up-user-time-constraints"></a>Til að setja upp tímaskorður notanda
Stjórnendur geta skilgreint tímabil þegar tilgreindir notendur geta bókað, og geta einnig tilgreint hvort kerfið skrái tímann sem notandinn er skráður inn. Stjórnendur geta einnig úthlutað ábyrgðarstöðvum á notendur. Frekari upplýsingar eru í [Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md).

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notandauppsetning** og velja svo viðeigandi tengil.
2. Í glugganum **Notandauppsetning** opnast, skal velja **Nýtt** aðgerð.
3. Í reitnum **Kenni notanda**, skal færa inn kenni notanda, eða velja reitinn til að sjá alla núverandi Windows notendur innan kerfisins.
4. Fyllið inn í reitina eftir þörfum.

## <a name="see-also"></a>Sjá einnig
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Hafist handa](product-get-started.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

