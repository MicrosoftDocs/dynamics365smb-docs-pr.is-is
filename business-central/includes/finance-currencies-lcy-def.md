---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Þar sem fyrirtæki starfa í mörgum löndum/svæðum er nauðsynlegt fyrir þau að geta stundað viðskipti og skráð fjárhagslegar upplýsingar í fleiri en einum gjaldmiðli. Staðbundinn gjaldmiðill (SGM) er skilgreindur á síðunni **Fjárhagsgrunnur** eins og lýst er í greininni [Að skilja fjárhag og bókhaldslykla](../finance-general-ledger.md). Þegar staðbundinn gjaldmiðill hefur verið skilgreindur verður hann tómur gjaldmiðill. Þegar reiturinn **Gjaldmiðill** er auður merkir það að gjaldmiðillinn er SGM.  

Því næst þarf að setja upp gjaldmiðilskóða fyrir hvern gjaldmiðil sem er notaður ef keypt er eða selt er í öðrum gjaldmiðlum en staðbundnum gjaldmiðli (SGM). Einnig er hægt að stofna bankareikninga með gjaldmiðlum. Hægt er að skrá fjárhagsfærslur í mismunandi gjaldmiðlum, en fjárhagsfærslan verður ávallt færð í staðbundnum gjaldmiðli (SGM).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM), en þú getur sett hann upp til að einnig nota annan gjaldmiðil með gengi stillt. Sé öðrum gjaldmiðli gefin svokölluð skilgreining Viðbótarskýrslugjaldmiðill mun [!INCLUDE[prod_short](prod_short.md)] skrá upphæðirnar sjálfkrafa bæði í SGM og þessum viðbótarskýrslugjaldmiðli í hverri fjárhagsfærslu og í öðrum færslum á borð við færslur fyrir VSK. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](../finance-how-setup-additional-currencies.md). Viðbótarskýrslugjaldmiðillinn er oftast notaður til að auðvelda fjárhagsskýrslugerð til eigenda sem búa í löndum/svæðum sem nota annan gjaldmiðil en staðbundinn gjaldmiðill (SGM).  

> [!IMPORTANT]
> Ef þú vilt nota annan skýrslugjaldmiðil fyrir fjárhagsskýrslur skaltu ganga úr skugga um að þú skiljir takmarkanirnar. Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Þegar þú bókar í fjárhag með gjaldmiðilskóða, t.d. til að bóka kostnað í færslubók með gjaldmiðilskóða, er færslan umreiknuð í SGM með gengi gjaldmiðilsins fyrir bókunardagsetninguna. Fjárhagsfærslan mun ekki innihalda upplýsingar um hvaða gjaldmiðill var notaður, aðeins virði hans í SGM. Ef þú vilt halda utan um upprunalegan gjaldmiðil, t.d. fyrir reikning, verður þú að nota sölu- og innkaupskjöl sem og bankareikninga sem geyma upplýsingar um gjaldmiðilskóða fyrir færslurnar.
