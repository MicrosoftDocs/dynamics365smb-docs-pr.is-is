---
title: Hvernig á að umbreyta þjónustusamningum
description: Í þessu efnisatriði er lýst nokkrar öðrum aðferðum sem hægt er að nota til að umbreyta þjónustusamningum sem innihalda VSK-upphæðir.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="convert-service-contracts-that-include-vat-amounts" />Umbreyta þjónustusamningum sem innihalda VSK upphæðir
Þar sem breytingaverkfæri VSK-hlutfalls getur ekki umbreytt þjónustusamningum, verður að umbreyta þessum samningum handvirkt. Í þessu efnisatriði er lýst nokkrar öðrum aðferðum sem hægt er að nota við umbreytingar þjónustusamninga.  

> [!NOTE]  
>  Þetta efnisatriði gefur verkflæði á háu stigi.  

 Eftirfarandi ferli lýsir því hvernig eigi að leiðrétta reikning fyrir fyrirframgreiddan þjónustusamning sem hefur verið stofnaður ár fyrirfram.  

> [!NOTE]  
>  Í þessu dæmi þarf að breyta þarf vinnudagsetningunni í 01.01.2017.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract" />Til að leiðrétta reikning fyrir fyrirframgreiddan þjónustusamning
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Umsjón með samningi** og velja síðan viðkomandi tengil.  
2. Undir **Listar**, skal velja **Þjónustusamningar**.  
3. Stofna nýjan fyrirframgreiddan þjónustusamning. Færa inn upphafsdagsetninguna **01.01.2017** og reikningstímabilsár fyrir viðskiptavin **20000**.  
4. Veldu aðgerðina **Undirritun samnings** til að skrifa undir samninginn.  
5. Stofna þjónustureikning.
6. Reikningurinn er á lista sem óbókaður þjónustureikningur. Til að skoða þjónustureikninginn skal velja aðgerðina **Þjónusta**, velja aðgerðina **Samningakerfi** og smella svo á aðgerðina **Þjónustureikningar**.  
7. Bóka skal þjónustureikninginn.  

> [!NOTE]  
>  Ekki breyta óbókaða þjónustureikningnum. Þar sem þjónustufærslur eru stofnaðar við stofnun reikningsins, munu breytingar á óbókaða reikningnum ekki breyta þjónustufærslum sem þegar hafa verið stofnaðar. Hins vegar verða VSK-færslur stofnaðar við bókun reikningsins. Þetta leyfir þér að breyta almenna bókunarflokknum og GSP vörubókunarflokknum á óbókaða þjónustureikningnum.  

### <a name="to-create-a-credit-memo-for-vat-difference" />Til að setja upp kreditreikning fyrir VSK-mun
Eftirfarandi ferli lýsir því hvernig eigi að stofna kreditreikning sem inniheldur einvörðungu VSK-mismun fyrir það tímabil sem þegar hefur verið reikningsfært og byrjar **01.07.2017**. Í þessu dæmi er vsk-upphæðin aðeins bókuð í fjármálastjórnunarhluta, ekki þjónustustjórnunarhlutanum. VSK-færslur sem tengjast þjónustubókarfærslunni verða ekki leiðréttingar.  

1. Búa til nýjar fjárhagsreikninga fyrir VSK-mismuninn. Þessi lykill verður notaður fyrir beina bókun VSK-leiðréttingar.  
2. Bæta nýrri línu við VSK-bókunargrunninn.  

### <a name="to-create-contract-expiration-dates-in-contract-lines" />Til að stofna gildislokadagsetningar samnings í samningslínum
Eftirfarandi ferli lýsir því hvernig eigi að stofna nýja samninga með því að vinna með fyrningardagsetningar samninga í þjónustusamningslínum.  

1. Á síðunni **Þjónustusamningur** stillið lokadagsetningu samnings á **30.06.2017**.  
2. Velja aðgerðina **Stofna kreditreikn.** til að stofna kreditreikning sjálfkrafa fyrir júlí 2017 til desember 2017.  
3. Þar sem samningurinn er útrunninn er, verður að stofna nýjan samning fyrir tímabilið með nýjum VSK-taxta fyrir 1. júlí, 2017 til 31. desember 2017.  

### <a name="to-create-a-new-credit-memo" />Nýr kreditreikningur stofnaður.
Eftirfarandi ferli lýsir því hvernig eigi að stofna nýjan kreditreikning með keyrslunni **Sækja fyrirfr.gr, samn.færslur**. Færslur sem ekki á að leiðrétta frá janúar 2017 til júní 2017 verður eytt.  

1. Keyra skal breytingarverkfæri VSK-hlutfalls 1. júlí 2017. Almenni vörubókunarflokkurinn eða VSK-vörubókunarflokkurinn breytist. Frekari upplýsingar, sjá [Vinna með VSK í sölu og innkaupum](finance-work-with-vat.md).  
2. Eftir keyrslu breytingaverkfæris VSK-hlutfalls, skal færa inn lokadag samnings fyrir þjónustusamninginn. Nú er hægt að eyða þjónustusamningslínunni og stofna nýja línu sem er eins og sú eldri.  
3. Stofna nýjan reikning fyrir tímabilið frá janúar 2017 til desember 2012 með nýjum VSK-taxta.  
4. Til þess að stofna annan kreditreikning er farið á síðuna **Þjónustukreditreikningar** og aðgerðina **Nýr** valin til að stofna nýjan þjónustukreditreikning.  
5. Velja aðgerðina **Sækja fyrirfr.gr, samn.færslur**.  
6. Þegar umreikninginum er lokið, verða VSK og þjónustufjárhagsfærslur réttar.  

## <a name="see-also" />Sjá einnig
[Vinna með þjónustusamninga og þjónustusamningstilboð](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Fjármál](finance.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
