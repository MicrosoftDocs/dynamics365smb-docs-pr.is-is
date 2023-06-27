---
title: Flytja og bóka kostnaðarfærslur
description: Áður en kostnaðarúthlutanir eru skilgreindar þarf að átta sig á hvaðan hinar ýmsu kostnaðarfærslur koma.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1103, 1104, 1108, 1113, 1135'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="transferring-and-posting-cost-entries"></a>Flytja og bóka kostnaðarfærslur

Áður en kostnaðarúthlutanir eru skilgreindar, þarf að átta sig á hvernig kostnaðarfærslur koma úr eftirfarandi uppruna:  

- Sjálfvirkur flutningur á fjárhagsfærslum.  
- Handvirk kostnaðarbókun hreins kostnaðar, innri gjalda og handvirkra úthlutana.  
- Sjálfvirk úthlutun bókana fyrir raunkostnað.  
- Flutningur á áætlunarfærslum í raunverulegar.

## <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur

Mikilvægt er að átta sig á skilyrðum fyrir því að flytja fjárhagsfærslur til kostnaðarfærslna. Meðan á millifærslu stendur notar runuvinnslan **Millifæra fjárhagsfærslu til kostnaðarbókhalds** eftirfarandi skilyrði til að tilgreina hvort og hvernig fjárhagsfærslur eru fluttar.  

Fjárhagsfærslur eru fluttar ef:  

- Færslurnar hafa víddargildi sem samsvara annaðhvort kostnaðarstað eða kostnaðarhlut.  
- Færslurnar hafa víddargildi sem samsvara kostnaðarstað og kostnaðarhlut. Kostnaðarstaðurinn hefur forgang í þessum færslum. Þetta hjálpar til við að forðast aðstæður þar sem kostnaðargerð birtist í bæði kostnaðarhlut og kostnaðarstað og er því talin tvisvar í tölfræðigögnum.  
- Fylgiskjalsnúmerið í færslunum er autt, þannig að það birtist með fylgiskjalsnúmerinu 0000 í kostnaðarfærslunum.  
- Færslurnar eru færðar í kostnaðartegund sem leyfir við blandaðar færslur og þessar færslur eru fluttar sem blönduð færsla, annaðhvort mánaðarlega eða daglega.  

Fjárhagsfærslur eru ekki fluttar ef:  

- Færslurnar hafa víddargildi sem samsvara ekki kostnaðarstað né kostnaðarhlut.  
- Færslurnar hafa upphæð núll.  
- Færslurnar hafa fjárhagsreikning sem hefur verið eytt.  
- Færslurnar hafa fjárhagsreikning sem er ekki af tegundinni **Rekstrarreikningur**.  
- Færslurnar hafa fjárhagsreikning sem er ekki tengdur kostnaðartegund.  
- Færslurnar hafa bókunardagsetningu fyrir **Upphafsdagsetning fjárhagsmillifærslu**.  
- Færslurnar hafa verið bókaðar með lokadagsetningu. Þetta eru yfirleitt færslur sem stilla aftur stöðu rekstrarreiknings við lok hvers árs.

## <a name="transferring-general-ledger-entries-to-cost-entries"></a>Flytja fjárhagsfærslur í kostnaðarfærslur

Hægt er að flytja fjárhagsfærslur í kostnaðarfærslur  

Áður en ferlið til að flytja fjárhagsfærslur til kostnaðarfærslna er keyrt, þarf að undirbúa flutninginn til að forðast handvirka leiðréttingarbókun.  

### <a name="to-prepare-the-transfer"></a>Til að undirbúa færsluna

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning kostnaðarbókahalds** og velja síðan viðkomandi tengil.  
2.  Á síðunni **Uppsetning kostnaðarbókhalds** skal ganga úr skugga um að reiturinn **Upphafsdagur fyrir fjárhagsfærslur** sé stilltur á rétt gildi.  
3.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Myndrit kostnaðargerða** og velja síðan viðkomandi tengil.  
4.  Á síðunni **Kostnaðargerðarspjald** skal ganga úr skugga um að reiturinn **Fjárhagsreikningssvið** sé tengdur rétt þannig að hver kostnaðargerð taki færslur úr fjárhag.  
5.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
6.  Fyrir hvern viðeigandi fjárhagsreikning, á síðunni **Fjárhagsreikningsspjald**, skal sannreyna að reiturinn **Kostnaðargerð nr.** sé rétt tengdur í kostnaðartegund. Nánari upplýsingar er að finna í [Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md).  
7.  Staðfesta að allar viðeigandi fjárhagsfærslur hafa víddargildi sem samsvara kostnaðarstað og kostnaðarhlut.  

### <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Til að færa fjárhagsfærslur yfir í kostnaðarfærslur

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Millifæra fjárhagsfærslur til kostnaðarbókhalds** og velja síðan viðkomandi tengil.  
2.  Velja hnappinn **Já** til að hefja millifærsluna. Ferlið færir allar fjárhagsfærslur sem hafa ekki þegar verið færðar.  

Meðan á millifærslu stendur býr ferlið til tengingar í færslurnar í töflunni **Kostnaðarfærsla** og töflunni **Kostnaðarskráning**. Þannig er hægt að rekja uppruna kostnaðarfærsla.

## <a name="automatic-transfer-and-combined-entries"></a>Sjálfvirkur flutningur og færslur sameinaðar

Í kostnaðarbókhaldi er hægt að flytja fjárhagsfærslur í tegund kostnaðar með því að nota blandaða bókun. Þú getur tilgreint það ef kostnaðargerð fær sameinaðar færslur í reitinn **Sameinaðar færslur** í skilgreiningunni á kostnaðargerð. Eftirfarandi tafla lýsir hinum mismunandi valkostum.  

|Sameina færslur|Description|  
|---------------------|-----------------|  
|Engin|Hver fjárhagsfærsla er flutt sérstaklega í samsvarandi kostnaðartegund.|  
|Dagur|Fjárhagsfærslur með sömu bókunardagsetningu eru fluttar sem ein færsla í samsvarandi tegund kostnaðar.|  
|Mánuður|Allar fjárhagsfærslur í sama almanaksmánuði eru fluttar sem ein færsla í samsvarandi tegund kostnaðar.|  

> [!IMPORTANT]  
>  Ef gátreiturinn **Sjálfvirk færsla úr fjárhag** er valinn af síðunni **Uppsetning kostnaðarbókhalds**, uppfærir [!INCLUDE[prod_short](includes/prod_short.md)] kostnaðarbókhaldið eftir hverja bókun í fjárhag. Sameinaðar færslur eru ekki mögulegar.

## <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Niðurstöður millifærslu fjárhagsfærslna yfir í kostnaðarfærslur

Meðan á millifærslu á fjárhagsfærslum í kostnaðarfærslur stendur, stofnar [!INCLUDE[prod_short](includes/prod_short.md)] tengingar í færslurnar í töflunni **Fjárhagsfærslur**, töflunni **Kostnaðarfærsla** og töflunni **Kostnaðarskráning** svo hægt sé að rekja tengingar milli kostnaðar- og fjárhagsfærslna.  

### <a name="general-ledger-entries"></a>Fjárhagsfærslur

Fyrir hverja fjárhagsfærslu sem er flutt í kostnaðarbókhald, fyllir [!INCLUDE[prod_short](includes/prod_short.md)] út kostnaðinn í reitnum **Færslunr.**  

### <a name="cost-entries"></a>Kostnaðarfærslur

Fyrir sérhverja kostnaðarfærslu, vistar [!INCLUDE[prod_short](includes/prod_short.md)] færslunúmer samsvarandi fjárhagsfærslu í reitnum **Fjárhagsfærsla númer** í töflunni **Kostnaðarfærsla**.  

Fyrir sameinaðar kostnaðarfærslur, vistar [!INCLUDE[prod_short](includes/prod_short.md)] færslunúmer síðustu fjárhagsfærslu, sem er færslan með hæsta færslunúmerið.  

Svæðið **Fjárhagsreikningur** í töflunni **Kostnaðarfærsla** hefur að geyma númer þess almenna fjárhagsreiknings sem kostnaðarfærslan kom frá.  

Fyrir stakar kostnaðarfærslur flytur [!INCLUDE[prod_short](includes/prod_short.md)] bókunartextann úr fjárhagsfærslunni í textareitinn **Lýsing**. Fyrir sameinaðar færslur, sýnir textareiturinn að þessar færslur eru fluttar sem sameinaðar færslur. Ef til dæmis um er að ræða sameinaða færslu vegna októbermánaðar 2013 gæti textinn verið **Sameinaðar færslur, október 2013**.  

### <a name="cost-register"></a>Kostnaðarskráning

Í töflunni **Kostnaðarskráning**, [!INCLUDE[prod_short](includes/prod_short.md)] stofnar færslu með upprunaflutningnum frá fjárhag. Færslan skráir fyrstu og síðustu færslunúmer fjárhagsfærslna sem eru fluttar, til viðbótar við fyrstu og síðustu færslunúmer kostnaðarfærslnanna sem eru stofnaðar.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/transfer-gl-entries-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

 [Um kostnaðarbókhald](finance-about-cost-accounting.md)  
 [Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)  
 [Skilgreina og úthluta kostnaði](finance-define-and-allocate-costs.md)  
 [Kostnaðarreikningur](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
