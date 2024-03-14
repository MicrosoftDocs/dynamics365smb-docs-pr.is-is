---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Ef fyrirtækið starfar í fleiri en einu landi eða svæði er líklega mikilvægt að hægt sé að eiga viðskipti í fleiri en einum gjaldmiðli. Staðbundinn gjaldmiðill (SGM) er skilgreindur á síðunni **Fjárhagsgrunnur** . Síðan er staðarmynt birt sem auður gjaldmiðill í fylgiskjölum og viðskiptum. Þegar reiturinn **Gjaldmiðill** er auður er gjaldmiðillinn SGM.

Eftirfarandi myndskeið útskýrir hvernig staðbundnir gjaldmiðlar eru settir upp.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Því næst þarf að setja upp gjaldmiðilskóða fyrir hvern gjaldmiðil sem er notaður ef keypt er eða selt er í öðrum gjaldmiðlum en staðbundnum gjaldmiðli (SGM). Einnig er hægt að stofna bankareikninga með gjaldmiðlum. Hægt er að skrá fjárhagsfærslur í mismunandi gjaldmiðlum, en fjárhagsfærslan verður ávallt færð í staðbundnum gjaldmiðli (SGM).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM), en þú getur sett hann upp til að einnig nota annan gjaldmiðil með gengi stillt. Með því að auðkenna annan gjaldmiðil sem annan skýrslugjaldmiðil [!INCLUDE[prod_short](prod_short.md)]  skráir kerfið sjálfkrafa upphæðir bæði í SGM og öðrum skýrslugjaldmiðli í fjárhagsfærslu og öðrum færslum, svo sem VSK-færslum. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](../finance-how-setup-additional-currencies.md). Viðbótarskýrslugjaldmiðillinn er oftast notaður til að auðvelda fjárhagsskýrslugerð til eigenda sem búa í löndum/svæðum sem nota annan gjaldmiðil en staðbundinn gjaldmiðill (SGM).  

> [!IMPORTANT]
> Ef þú vilt nota annan skýrslugjaldmiðil fyrir fjárhagsskýrslur skaltu ganga úr skugga um að þú skiljir takmarkanirnar. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Þegar bókað er í fjárhag með erlendum gjaldmiðli [!INCLUDE [prod_short](prod_short.md)]  breytir hreyfingin í SGM með því að nota gengi gjaldmiðilsins fyrir bókunardagsetninguna. Í fjárhagsfærslunni eru ekki upplýsingar um hvaða gjaldmiðill var notaður, aðeins virði hennar í SGM. Til að fylgjast með upphaflegum gjaldmiðli skal nota sölu- og innkaupaskjölin og bankareikninga sem geyma upplýsingar um gjaldmiðil fyrir færslur.
