---
title: Vinna með fjárhagsyfirlit í Excel
description: Lærðu hvernig hægt er að opna fjárhagsskýrslurnar í Microsoft Excel frá Business Central til að fá betri greiningar.
author: edupont04
ms.topic: overview
ms.search.keywords: accountant, accounting, financial report
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: edupont
ms.openlocfilehash: 43b5a4181b50da65f25be3f3fc73a0e01fd885af
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361762"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Greina fjárhagsskýrslur í Excel Microsoft Excel.

[!INCLUDE [prod_short](includes/prod_short.md)] útvegar afkastavísa og fá yfirskoðanir á fjármálum fyrirtækisins. Hér á eftir eru dæmi um leiðir til að greina afkastavísa og yfirflettingar í Excel:

* Opna lista í Excel og greina gögnin. 
* Flytja út þunga ársreikninga eins og efnahag eða rekstrarreikning í Excel, greina gögnin og prenta skýrslurnar.  

> [!TIP]
> Sjálfgefið er að skýrslurnar sem hægt er að skoða í Excel séu hannaðar til að hjálpa til við að greina yfirstandandi ár. Í rekstrarreikningi er undantekning þó. Þessi skýrsla gerir kleift að sía gögnin þannig að þau taki fyrri ár í greiningu.

## <a name="getting-the-overview-and-the-details-in-excel"></a>Fá yfirlit og upplýsingar í Excel

Í hlutverkamiðstöðvum Viðskiptastjóra og Accountant er **skýrsluaðgerðin** gerir kleift að velja ársreikninginn til skoðunar í Excel. Þegar þú velur skýrslu, mun hún opnast í Excel eða Excel Online. Innbót tengir gögnin við [!INCLUDE [prod_short](includes/prod_short.md)]. Þú þarft samt sem áður að skrá þig inn með sama aðgangi og þú notar með [!INCLUDE [prod_short](includes/prod_short.md)] Í eftirfarandi töflu er listi yfir skýrslurnar og hvar þær eru tiltækar.  


|Skýrsla  |Mitt hlutverk  |
|---------|---------|
|Efnahagsreikningur                 | Viðskiptastjóri, endurskoðandi |
|Rekstrarreikningur              | Viðskiptastjóri, endurskoðandi |
|Sjóðstreymisyfirlit       | Viðskiptastjóri, endurskoðandi |
|Yfirlit yfir óráðstafað eigið fé| Viðskiptastjóri, endurskoðandi |
|Innheimtur söluskattur         | Viðskiptastjóri, endurskoðandi |
|Yfirlit viðskiptamanns           | Viðskiptastjóri, endurskoðandi |
|Aldursgreind skuld         | Endurskoðandi |
|Aldursgreind krafa      | Endurskoðandi |

Segjum sem svo að þú viljir grafa dýpra í sjóðstreymi þitt. Frá hlutverkamiðstöð Viðskiptastjóra eða bókhaldara, getur þú opnað **yfirlitið yfir Sjóðstreymissskýrslu** í Excel en það sem í raun gerist er að við útförum viðkomandi gögn fyrir þig og Búðu til Excel-vinnubók byggð á fyrirfram ákveðnu sniðmáti. Þú gætir verið minnt(ur) á að opna eða vista vinnubókina, það fer eftir tegund vafrans.  

Í Excel má sjá glugga þar sem gögnin eru sett upp fyrir þig á fyrstu vinnubókinni. Öll gögnin sem voru flutt út eru líka aðgengileg á öðrum vinnublöðum ef þú þarft á þeim að halda. Þú getur prentað út skýrsluna undir eins, eða breytt henni þar til þú hefur yfirlitið og upplýsingarnar sem þú sækist eftir. Notaðu [!INCLUDE [prod_short](includes/prod_short.md)] Excel-innbótina til að afmarka og greina frekar gögn.  

### <a name="understanding-the-excel-templates"></a>Að skilja Excel-sniðmátin

Fyrirframskilgreindar Excel-skýrslur eru byggðar á gögnum í núverandi fyrirtæki. Til dæmis hefur sýnifyrirtækið sett upp bókhaldslykilinn til að skrá þrjá sjóðsreikninga undir *Núverandi eignir*: 10100 **Ávísanareikningur**, 10200 **Sparireikningur**, og 10300 **Kassasjóður**. Lyklarnir eru með reitinn **Undirflokkur reiknings** stilltan á *Reiðufé* og samtals upphæð þeirra er sýnd sem *Reiðufé* í Excel-skýrslunni **Efnahagsreikningur**.  

Önnur blöð í vinnubók Excel Sýna gögnin að baki skýrslunni. Til að komast að því hvað er bak við flokkanir í Excel skýrslum gæti þurft að sía listana í [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="the-prod_short-excel-add-in"></a>[!INCLUDE [prod_short](includes/prod_short.md)] Excel-innbótin

[!INCLUDE [prod_short](includes/prod_short.md)] Upplifun þín inniheldur innbót fyrir Excel. Eftir áskriftina skráir þú þig inn sjálfkrafa, eða þú verður að láta þig fá upplýsingar um innskráningu fyrir kl [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Skoða og breyta í Excel úr Business Central](across-work-with-excel.md).  

Viðbótin gerir þér kleift að fá fersk gögn úr [!INCLUDE [prod_short](includes/prod_short.md)] og þú getur ýtt breytingum aftur í [!INCLUDE [prod_short](includes/prod_short.md)]. Möguleikinn til að ýta gögnum til baka í gagnagrunn er hins vegar ekki fyrir hendi vegna þeirra fjárhagslegu skýrslna sem hægt er að skoða í Excel.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Skoða og breyta í Excel From Business Central](across-work-with-excel.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með Viðskiptaseðla-](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]