---
title: Sameina tvítekinn viðskiptamann eða lánardrottnafærslur | Microsoft Docs
description: Lýsir því hvernig skal stofna viðskiptamannaspjald til að skrá upplýsingar um alla nýja viðskiptamenn eða biðlara sem selt er til.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 04034406154dddfabe44a9fd62e0a793981e7f69
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748359"
---
# <a name="merge-duplicate-records"></a>Sameina tvíteknar færslur
Með tímanum stofna ýmsir notendur nýjan viðskiptamann, lánardrottin eða tengiliðaspjöld, eða nýju færslurnar eru stofnaðar sjálfkrafa við flutning, og því getur gerst að viðskiptamaður, lánardrottinn eða tengiliður komi fram í kerfinu í fleiri en einni færslu. Í slíkum tilfellum er hægt að nota síðuna **Sameina tvítekið atriði** úr spjaldinu með færslunni sem á að halda í. Síðan veitir yfirlit yfir tvítekin reitargildi og býður upp á virkni til að velja hvaða gildum skuli halda eða fleygja þegar tvær færslur eru sameinaðar sem ein.

> [!NOTE]
> Eingöngu notendur með heimildasamstæðuna SAMEINA TVÍTEKNINGAR geta notað þessa virkni.

> [!TIP]
> Síðan **Sameina tvítekið atriði** sýnir alla reiti þar sem gildin eru ólík fyrir færslurnar tvær sem bornar eru saman. Þar af leiðandi eru tvítekningar gefnar til kynna á síðu sem sýnir fáa reiti. Ef síðan sýnir hins vegar marga reiti þá er færslan líklega ekki tvítekin.

Eftirfarandi ferli byggist á viðskiptamannaspjaldi. Skrefin eru svipuð fyrir lánardrottin og tengiliðaspjöld.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamenn** og veldu síðan tengda tengilinn.
2. Veldu viðskiptamanninn sem þú veist eða grunar að sé með tvítekna færslu og veldu síðan aðgerðina **Breyta**.
3. Á síðunni **Viðskiptamannaspjald** skal velja aðgerðina **Sameina við**.
4. Á síðunni **Sameina tvítekið atriði**, í reitnum **Sameina við**, skal velja viðskiptamanninn sem þú telur að sé tvítekinn af þeim sem eru opnir, sem gefið er upp í reitnum **Núverandi**.

    Flýtiflipinn **Reitir** birtir reiti þar sem gildin eru mismunandi fyrir viðskiptamennina tvo. Þetta þýðir að ef valinn viðskiptamaður er í raun tvítekinn munu aðeins fáir reitir birtast, t.d. innsláttarvillur og önnur mistök við gagnaskráningu.

    Flýtiflipinn **Tengdar töflur** birtir töflur þar sem eru reitir sem tengjast báðum viðskiptamönnunum. Reitirnir **Núverandi fjöldi** og **Tvítekinn fjöldi** sýna fjölda reita í tengdum töflum þar sem **Nr.** gildið fyrir bæði núverandi og tvítekinn viðskiptamann er notað. Á síðunni **Sameina tvítekið atriði**, þessi hluti er eingöngu til upplýsinga, ef hins vegar árekstrar sameiningar eru til, leysir þú úr þeim á síðunni **Sameina árekstra tvítekninga**. Sjá skref 8 til 12.   

5. Fyrir hvern reit þar sem þú vilt nota annað gildi en núverandi gildi skal velja gátreitinn **Hnekkja**. Gildið í reitnum **Annað gildi** verður þá flutt í núverandi færslu þegar ferlinu er lokið.
6. Þegar þú hefur lokið við að velja hvaða gildum eigi að halda eða hnekkja, skaltu velja aðgerðina **Sameina**.

    Kerfið athugar hvort sameining gilda fyrir tvítekinn viðskiptamann yfir í núverandi viðskiptamann valdi einhverjum árekstrum. Árekstur á sér stað ef gildi í að minnsta kosti einum lykilreit er það sama fyrir báða viðskiptamenn á meðan gildið í reitnum **Nr** er ólíkt fyrir viðskiptamennina tvo.

7. Ef engir árekstrar finnast skal velja hnappinn **Já** í glugga staðfestingarboða.

    Tvítekinn viðskiptamaður er endurnefndur þannig að öll notkun á **Nr.** gildinu í öllum reitum með tengsl við töflu viðskiptamanns verður skipt út fyrir **Nr.** gildið á núverandi viðskiptamanni.
8. Ef árekstur á sér stað skal velja **Leysa úr (xx) árekstrum á undan sameiningu.** aðgerðina í flýtiflipanum **Árekstrar** sem mun birtast ef árekstrar eiga sér stað.
9. Á síðunni **Sameina árekstra tvítekninga** skal velja línuna fyrir tengda töflu með árekstri og því næst velja aðgerðina **Skoða upplýsingar**.

    Síðan **Sameina tvítekið atriði** sýnir nú reitina í valdri töflu sem valda árekstri milli færslna viðskiptamannanna tveggja. Taktu eftir að samantekin gildi í reitunum **Núverandi** og **Árekstrar við** og í línunum þar sem að minnsta kosti einn lykilreitur er sá sami fyrir báða viðskiptamennina og gildið á **Nr.** reitnum er ólíkt fyrir viðskiptamennina tvo.   
10. Ef þú vilt ekki geyma tvítekna færslu viðskiptamanns skaltu velja aðgerðina **Fjarlægja tvítekið atriði** og því næst velja hnappinn **Loka**.

    Eins reitargildi, önnur en gildið í **Nr.** reitnum, eru fjarlægð úr tvítekinni færslu og sett inn í núverandi færslu.
11. Ef þú vilt geyma tvítekna færslu viðskiptamanns eftir sameiningu skaltu velja **Endurnefna tvítekið atriði**.
12. Í línum, ekki fyrir **Nr.** reitinn, þar sem reiturinn er með sama gildi í báðum færslum, skal breyta gildinu í reitnum **Annað gildi** og síðan velja hnappinn **Loka**.

    Reitargildið með árekstra er uppfært í tvítekinni færslu svo hægt sé að sameina það við núverandi færslu. Tvítekin færsla heldur áfram að vera til eftir sameiningu.
13. Endurtaktu skref 8 til 12 þar til leyst hefur verið úr öllum árekstrum. Flýtiflipinn **Árekstrar** hverfur.
14. Á síðunni **Sameina tvítekið atriði** skal velja aðgerðina **Sameina** og síðan velja hnappinn **Já** í glugga staðfestingarboða.

> [!NOTE]
> Fyrir tengiliði er hægt að nota virkni til að finna tvítekna tengiliði áður en síðan **Sameina tvítekið atriði** er notuð. Frekari upplýsingar er að finna í [Leita að tvíteknum tengiliðum](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Uppsetning tengiliða](marketing-setup-contacts.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]