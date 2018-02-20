---
title: "Haldið utan um fjarveru starfsmanna | Microsoft Docs"
description: "Lýsir því hvernig á að skrá fjarveru starfsmanna og greina upplýsingar um fjarveru."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/08/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 13461418fd89c8eb743b88b5a2ed98f24a520571
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="manage-employee-absence"></a>Haldið utan um fjarvistir starfsmanna
Til að geta haldið utan um fjarvistir starfsmanns er nauðsynlegt að skrá fjarveru í gluggann **Skráning fjarvista**. Þá er hægt að skoða þær á ýmsan hátt eins og þarf til greiningar og skráningar.

Hægt er að skoða fjarvistir starfsmanna í tveimur ólíkum gluggum:

* Glugganum **Fjarvistaskráning**, þar sem allar fjarvistir starfsmanna eru skráðar í eina línu fyrir hverja fjarvist.
* Í glugganum **Fjarvist starfsmanns** eru einungis birtar fjarvistir eins starfsmanns. Þetta eru upplýsingarnar sem voru færðar inn í glugganum **Skráning fjarvista**, afmarkaðar við þennan tiltekna starfsmann.

Til að fá nothæfar tölur ætti ávallt að gæta þess að nota ætíð sömu mælieiningu (klukkustund eða dag) þegar fjarvera starfsmanna er skráð.

## <a name="to-register-employee-absence"></a>Skráning fjarvistar starfsmanna
Hægt er að skrá fjarvistir starfsmanna daglega eða á einhverjum öðru tímabili sem hentar þörfum fyrirtækisins.

1. Í efra hægra horni, veljið táknið **leita að síðu eða skýrslu**, færið inn **Skráning fjarvistar** og veljið síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fylla þarf út línu fyrir hverja fjarvist starfsmanns sem óskað er eftir að skrá.
4. Glugganum er lokað.

    > [!Tip]
    > Til að fá nothæfar tölur verður að gæta þess að nota ætíð sömu mælieiningu (klst eða dag) þegar fjarvera starfsmanna er skráð.

## <a name="to-view-an-individual-employees-absence"></a>Til að skoða fjarvistir staks starfsmanns
1. Í efra hægra horni, veljið táknið **leita að síðu eða skýrslu**, færið inn **Starfsmenn** og veljið síðan viðkomandi tengil.
2. Veljið viðeigandi starfsmann og smellið því næst á aðgerðina **Fjarvistir**.

    Glugginn **Fjarvistir starfsmanna** opnast og þar birtist listi yfir allar fjarvistirnar og dagsetninguna sem þær hófust og lauk.

## <a name="to-view-an-employees-absence-by-categories"></a>Til að skoða fjarvistir starfsmanns eftir flokkum
1. Í efra hægra horni, veljið táknið **leita að síðu eða skýrslu**, færið inn **Starfsmenn** og veljið síðan viðkomandi tengil.
2. Veljið viðeigandi starfsmann og smellið því næst á aðgerðina **Fjarvistir eftir flokkum**.
3. Í glugganum **Fjarvistir starfsm. e. flokkum** skal fylla inn í síureitina eins og á þarf að halda og velja svo aðgerðina **Sýna fylki**.

    Glugginn **Fjarvistir starfs. e. fl. - fylki** opnast og sýnir allar fjarvistir, sem flokkaðar eru niður eftir ástæðum fjarvistar.

## <a name="to-view-all-employee-absences-by-category"></a>Til að skoða allar fjarvistir starfsmanna eftir tegund
1. Í efra hægra horni, veljið táknið **leita að síðu eða skýrslu**, færið inn **Skráning fjarvistar** og veljið síðan viðkomandi tengil.
2. Í glugganum **Fjarvistaskráning** skal velja aðgerðina **Yfirlit eftir flokkum**.
3. Í glugganum **Yfirlit fjarvista eftir flokkum** skal setja takmörkun í reitinn **Afmörkun á starfsmannanr.** til að skoða fjarvistir fyrir einstakan starfsmann eða skilgreindan hóp starfsmanna.
4. Veljið aðgerðina **Sýna fylki**.

    Glugginn **Yfirlit fjarvista e. flokkum - fylki** opnast og birtir lista yfir allar fjarvistir starfsmanna flokkað eftir ástæðu fjarvistar.

## <a name="to-view-all-employee-absences-by-period"></a>Til að skoða allar fjarvistir starfsmanna eftir tímabili
1. Í efra hægra horni, veljið táknið **leita að síðu eða skýrslu**, færið inn **Skráning fjarvistar** og veljið síðan viðkomandi tengil.
   Í glugganum **Fjarvistaskráning** skal velja aðgerðina **Yfirlit eftir tímabilum**.
2. Í glugganum **Yfirlit fjarvista e. tímabilum** skal setja takmörkun í reitinn **Ástæða fjarvistar - Afmörkun** til að skoða fjarvistir starfsmanna fyrir tiltekna ástæðu fjarvistar.
3. Veljið aðgerðina **Sýna fylki**.

    Glugginn **Yfirlit fjarvista e. tímabilum** opnast og birtir lista yfir fjarvistir starfsmanna flokkað eftir tímabilum.

## <a name="see-also"></a>Sjá einnig
[Hafa umsjón með mannauði](hr-manage-human-resources.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sérstillir þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).

