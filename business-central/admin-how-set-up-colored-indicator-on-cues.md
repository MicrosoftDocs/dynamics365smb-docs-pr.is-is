---
title: Setja upp sérstillta litavísa fyrir verkþátt bendingar
description: Sem stjórnandi geturðu sett upp bendingar sem birtast í Mitt hlutverk notenda þannig að það innihaldi vísi sem breytir um lit eftir gagnagildi í bendingum.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9701, 9702'
ms.date: 04/01/2021
ms.author: jswymer
---
# Setja upp litaðan vísi á bunka fyrir fyrirtækið eða einstaka notendur

Sem stjórnandi geturðu sett upp bendingar sem birtast í Mitt hlutverk notenda þannig að það innihaldi vísi sem breytir um lit eftir gagnagildi í bendingum.  

Vísirinn birtist sem stika efst í ramma bendingarinnar. Veitir sjónrænt merki um virknistöðu bendingarinnar sem getur táknað hagstæð eða óhagstæð skilyrði sem kalla á viðbrögð frá notanda. Ef bunki birtir til dæmis viðvarandi sölureikninga er hægt að stilla vísinn á að vera grænn (jákvætt) þegar heildarfjöldi viðvarandi sölureikninga er undir 10 og rauður (óæskilegt) þegar samtalan er yfir 20.  

Á síðunni **uppsetning bunka** seturðu setja upp vísa fyrir allar bendingar sem eru tiltækar í gagnagrunni fyrirtækisins. Hægt er að setja upp vísa sem eru notaðir fyrir alla notendur í fyrirtækinu eða einstakan starfsmann. Vísisstillingarnar á síðunni **Uppsetning bunka** virka sem sjálfgefnar vísisstillingar. Ef síðan **Uppsetning bendingar notandi** er gerð tiltæk fyrir notendur geta þeir sérsniðið vísastillingarnar sem eru skilgreindar á síðunni **Uppsetning bendingar**.  

Til að setja upp vísi tilgreinirðu allt að tvö þröskuldsgildi sem tilgreina þrjú svið gagnagilda (lágt, miðlungs og hátt) sem hægt er að nota annan lit (eða stíl) við.  

### Til að setja upp litaða vísa í bendingum  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning raðar** og velja síðan viðkomandi tengil.  

     Síðan **Uppsetning bunka** birtist. Síðan birtir vísa sem nú eru uppsettir í bendingum. Vísar sem eiga við alla notendur í fyrirtækinu eru með auðan **Notandanafn** reit. Vísar sem gilda um tiltekinn notanda innhalda notandanafnið í **Notandanafn** reitnum.  

    > [!NOTE]  
    >  Ef þú setur upp vísi fyrir allt fyrirtækið og notandi breytir vísinum síðar þá er önnur færsla fyrir vísinn birtist fyrir þann notanda.  

2. Veldu aðgerðina **Breyta lista**.  
3. Til að setja upp vísir fyrir bendingar sem er ekki listaður á síðunni velurðu **Nýtt** og fyllir svo inn reitina líkt og lýst er í eftirfarandi. Ef þú vilt breyta vísi sem þegar er til skaltu fara á næsta skref.  

    |  Svæði  |  Description  |    
    |---------|---------------|  
    |**Notandanafn**|Ef þú vilt setja upp vísi fyrir allir notendur skaltu hafa þennan reit auðan.<br /><br /> Ef þú vilt setja upp vísi fyrir tiltekinn notanda skaltu stilla þennan reit á notandanafn.|  
    |**Nr. töflu**|Tilgreinir auðkenni töfluhlutarins sem inniheldur bunkann. Notaðu fellilistann til að finna töfluna. Fellilistinn inniheldur allar bendingartöflur í gagnagrunni fyrirtækisins.<br /><br /> **Nafn töflu** reiturinn er sjálfvirkt útfylltur byggt á vali þínu.|  
    |**Reitur nr.**|Tilgreinir auðkenni bendingarinnar sem á að setja upp vísi fyrir. Notaðu fellilistann til að finna bendinguna sem þú vilt. **Athugið:** Auðkenni bendingar samsvarar reitanúmerinu sem er úthlutað á bendingum í töflunni. <br /><br /> **Heiti reitar** reiturinn er sjálfvirkt útfylltur byggt á vali þínu|  

4. Til að setja upp vísi fyrir bendingu velurðu reitina líkt og lýst er í eftirfarandi töflu.  

    |  Svæði  |  Description  |    
    |---------|---------------|  
    |**LágtSnið**|Tilgreinir lit vísisins þegar gildi bunka er minna en gildið í reitnum **Þröskuldur 1**.|  
    |**LágurÞröskuldur**|Tilgreinir gildið þar sem vísirinn breytir um lit sé hann fyrir ofan það, líkt og tilgreint er í reitnum **Stíll miðsviðs**.|  
    |**MiðlungsSnið**|Tilgreinir lit vísisins þegar gildi bunka er meira eða jafnt og gildið í reitnum **Þröskuldur 1** en minna en eða jafnt og gildið í reitnum **Þröskuldur 2**.|  
    |**HárÞröskuldur**|Tilgreinir gildið þar sem vísirinn breytir um lit sé hann fyrir ofan það, líkt og tilgreint er í reitnum **Stíll hás sviðs**.|  
    |**HáttSnið**|Tilgreinir lit vísisins sem nota á þegar gildi bunka er meira en gildið í reitnum **Þröskuldur 2**.|  

     Eftirfarandi tafla sýnir litin sem samsvara valkostum **LágtSnið**, **MiðlungsSnið** og **HáttSnið** reitanna.  

    |  Valkostur  |  Litur  |  
    |----------|---------|  
    |**Ekkert**|Enginn litur (sami litur og í bunkareit)|  
    |**Hagstæð**|Grænt|  
    |**Slæmt**|Rautt|  
    |**Tvírætt**|Gult|  
    |**Undirstig**|Grár|  

## Sjá einnig


[!INCLUDE[footer-include](includes/footer-banner.md)]