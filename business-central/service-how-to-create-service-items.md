---
title: Hvernig á að stofna Þjónustuvörur
description: 'Lestu um mismunandi leiðir sem hægt er að fara til að búa til þjónustuvörur í Business Central, til dæmis innan þjónustupöntunar eða við sendingu á vörum.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Stofna þjónustuatriði

Í [!INCLUDE[prod_short](includes/prod_short.md)] vísar hugtakið „þjónustuvara“ til búnaðar eða vöru þarfnast þjónustu. Þegar þú stofnar þjónustupöntun, tilgreinirðu vöruna sem þarfnast þjónustu. Í pöntuninni geturðu tengt þjónustuvöru við vöru í birgðum eða þjónustuvöruflokk.

Þegar tekið er við vöru sem þarfnast þjónustu má skrá hana sem þjónustuvöru. Hægt er gera það á nokkra vegu: Þú getur t.d. stofnað þjónustuvöru á **Þjónustuvörur** síðunni, eða sem hluta af öðru ferli, eins og þegar þú vinnur með þjónustupöntun.

## Þjónustuvörur stofnaðar:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuvörur** og svo velja viðeigandi tengil.
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Þjónustuvörur stofnaðar út frá þjónustupöntunum

Þegar tekið er við vöru til þjónustu og þarf að skrá hana sem þjónustuvöru er hægt að stofna þjónustuvöru á síðunum **Þjónustupöntun** eða **Þjónustutilboð**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Veljið aðgerðina **Stofna þjónustuvara**.  

    Númeri er sjálfkrafa úthlutað til þjónustuvörunnar og þjónustuvöruspjald er stofnað. Reiturinn **Nr. þjónustuvöru** er fylltur út með númeri nýju þjónustuvörunnar.

## Þjónustuvörur stofnaðar þegar vörur eru sendar:

Þegar vörur eru sendar, annaðhvort með því að bóka sölupantanir eða sölureikninga eru sendu vörurnar sjálfkrafa skráðar sem þjónustuvörur að uppfylltum eftirfarandi skilyrðum. Varan verður að tilheyra þjónustuvöruflokki með gátmerki í reitnum **Stofna þjónustuvöru**. Ef vörurnar eru með raðnúmer skráð á síðunni **Vörurakningarlínur** eru þessar upplýsingar afritaðar sjálfvirkt í reitinn Raðnr. á þjónustuvöruspjaldinu þegar þjónustuvörur eru stofnaðar.  

Eftirfarandi aðferð sýnir hvernig stofna má þjónustuvöru þegar sölupöntunarvara er send.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Viðeigandi sölupöntun er opnuð.  
3. Veljið aðgerðina **bóka** eða **Bóka og prenta**.  
4. Velja **Afhenda** eða **Afhenda og reikningsfæra** aðgerðina.  
5. Þjónustuvörur eru stofnaðar sjálfkrafa fyrir vörurnar í pöntuninni svo fremi að þær tilheyri þjónustuvöruflokki sem settur hefur verið upp til að stofna þjónustuvörur. Ef sérstök raðnúmer eru skráð á síðunni **Vörurakningarlínur** verður þeim úthlutað til þessum þjónustuvörum eins og við á.  

> [!NOTE]  
> Ef vara er uppskrift og búið er að opna uppskriftina eru vörurnar meðhöndlaðar eins og um venjulegar vörur væri að ræða. Kerfið stofnar þjónustuvörur eftir skilyrðinu um þjónustuvöruflokk, og ef vill, raðnúmer. Ef þjónustuvara er aukinheldur stofnuð fyrir opna uppskrift sem er samsett úr öðrum uppskriftaríhlutum eru vörur sem þjónustuvöruíhluti stofnaðar fyrir opna uppskriftarþjónustuvöru.  
>
> Ef vara er uppskrift og ekki búið að opna uppskriftina eru þjónustuvörur stofnaðar fyrir hana eftir skilyrðinu um þjónustuvöruflokk, og ef vill, raðnúmer.  

## Upphafsgjald vegna þjónustuvöru sett inn:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuverk** og svo velja viðeigandi tengil.
2. Velja aðgerðina **Vöruvinnublað**.
3. Velja þjónustulínuna og síðan **Aðgerðir**, velja **Aðgerðir** og síðan velja **Setja inn upphafsgjald** aðgerðina.  

    Kerfið setur inn þjónustulínu af gerðinni **Kostnaður** með upphafsgjaldinu. Upphafsgjaldið á við þá þjónustuvöru sem valin var.

## Loka vörum, vöruafbrigðum eða tilteknum þjónustuvörum

Hægt er að koma í veg fyrir að vörur, vöruafbrigði eða þjónustuvörur séu notaðar í þjónustukerfisfærslum, svo sem þjónustusamningum, þjónustupöntunum og þjónustureikningum. Þetta getur verið gagnlegt ef takmarka á ráðstöfunarbirgðir sumra vara eða þjónustuvara í þjónustuskyni, til dæmis vegna stuðnings sem hætt er við, takmarkaðra birgða eða samninga um samninga.

Til að loka vöru eða vöruafbrigði sem notað er í þjónustukerfisfærslum skal kveikja á vífærslninu Þjónustulokað á síðunni **Birgðaspjald**, **Vöruafbrigði og** Vöruafbrigðisspjald **·**. **·**  Einnig er hægt að setja þennan reit á síðunni **Vörusniðmát** og hann verður afritaður á vörurnar sem stofnaðar eru úr því sniðmáti.

Þegar lokað er á vöru eða vöruafbrigði er hún ekki tiltæk á eftirfarandi síðum:

- Þjónustulína (fyrir utan þjónustukreditreikninga, þar sem notandi sér tilkynningu um að lokað sé á vöruna eða afbrigðið en leyfilegt er af þessari tegund fylgiskjals)
- Þjónustuvara
- Þjónustusamningslína
- Stöðluð þjónustulína

Ef vörunúmer eða afbrigði sem lokað er á er fært inn handvirkt birtast villuboð sem gefa til kynna: "Í reitnum er gildi sem finnst ekki í tengdu töflunni."

Ef um er að ræða þjónustusamninga, þjónustusamningstilboð eða þjónustupantanir sem innihalda lokaðar þjónustuvörur eða vöruafbrigði er ekki hægt að nota eftirfarandi aðgerðir:

- **Læsa** eða **gera samning** á síðunni **Þjónustusamningstilboð** .
- **Læsa samningi**, **Undirrita samning**, **Stofna samningsþjónustupantanir** eða **Stofna samningsreikninga**  á síðunni **Þjónustusamningur** .
- **Gera pöntun** á síðunni **Þjónustutilboð** .
- **Gefa út til afhendingar** eða **bóka** á síðunni **Þjónustupöntun** .
- **Bóka** á síðunni **Þjónustureikningur** .

### Loka þjónustuvöru

Til að loka fyrir að þjónustuvara sé notuð í þjónustukerfisfærslum skal velja einn af eftirfarandi valkostum á **síðunni Þjónustuvöruspjald** í reitnum **Lokaður** :

- **Þjónustusamningur**: Lokað er á að þjónustuvaran sé notuð í þjónustusamningum og þjónustusamningstilboðum en ekki í þjónustupöntunum eða öðrum þjónustuskjölum.
- **Allt**: Loka skal notkun þjónustuvörunnar í öllum þjónustukerfisfærslum, þar á meðal þjónustusamningum, þjónustupöntunum og öðrum þjónustuskjölum.

Þegar þjónustuvöru er lokað er ekki hægt að velja hana á eftirfarandi síðum:

- Þjónustusamningslína (ef lokað er fyrir þjónustusamning eða allt)
- Þjónustuvörulína (fyrir utan þjónustukreditreikninga, ef öllum er lokað)

Ef þjónustuvörunúmer þjónustuvöru er handvirkt fært inn fyrir lokaða þjónustuvöru birtast villuboð um "Í reitnum er gildi sem finnst ekki í tengdu töflunni."

Ef um er að ræða þjónustusamninga, þjónustusamningstilboð eða þjónustupantanir sem innihalda lokaðar þjónustuvörur er ekki hægt að nota eftirfarandi aðgerðir:

- **Læsa** og **gera samning** á síðunni **Þjónustusamningstilboð** (ef lokað er á þjónustusamning eða allt).
- **Læsa samningi**, **Undirrita samning** eða **Breyta viðskiptamanni** á síðunni **Þjónustusamningur** (ef lokað er á þjónustusamning eða allt).
- **Búa til pöntun** í **þjónustutilboðinu**  (ef allt er lokað).
- **Gefa út til afhendingar**, **Bóka** í **þjónustupöntun (** ef allt er lokað. Ef þjónustupöntunarskjöl innihalda margar þjónustuvörur og sumar eru lokaðar og aðrar ekki er hægt að gefa út og bóka línur sem ekki eru lokaðar. Íhuga skal hvort kveikja eigi á einni **þjónustuvörulínu/pöntunarvíkkun** á síðunni **Þjónustukerfisgrunnur**).
- **Bóka** á síðunni **Þjónustureikningur** (ef öllum er lokað).

Einnig er hægt að skoða lokaðar þjónustuvörur með því að nota afmörkun á eftirfarandi skýrslur:

- Þjónustuvörur (skýrsla 5935)
- Þjónustuvörur úr ábyrgð (skýrsla 5937)
- Framlegð þjónustu (þjónustuvörur) (skýrsla 5938)

### Gagnauppfærsla

Þessi aðgerð krefst ekki frekari uppsetningar. En ef uppfærslan er [!INCLUDE [prod_short](includes/prod_short.md)] uppfærð skal hafa eftirfarandi í huga:

- Ef um er að ræða vörur, vöruafbrigði eða vörusniðmát þar sem **kveikt er á vísbendingunni Sala lokað** er einnig kveikt á reitnum **Þjónustulokað** fyrir þessar færslur við uppfærslu. Þetta tryggir að eldri sölulokunargrunnur gildir einnig um þjónustukerfisfærslur.
- Gagnauppfærsla aðeins ef að minnsta kosti ein þjónustuvara er til í fyrirtækinu, sem þýðir að notandi notar þjónustukerfisaðgerðina og þarfnast gagnauppfærslu. Ef þjónustuvörur eru ekki til er gagnauppfærslunni sleppt og **sjálfgefið er að slökkt sé á vífærinu Þjónustulokuð** fyrir allar vörur, vöruafbrigði og vörusniðmát.

## Sjá einnig .

[Setja upp þjónustuvörur og íhluti þjónustuvara](service-how-setup-service-items.md)  
[Þjónustustýring sett upp](service-setup-service.md)  
[Þjónustukerfi](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
