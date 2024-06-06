---
title: Þjónustuvörur og þjónustuvöruhlutar
description: 'Kynntu þér það sem þú verður að setja upp áður en þú getur notað þjónustuvörur, eins og sjálfgefin gildi á borð við svartíma og þjónustuverðflokk.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-service-items-and-service-item-components"></a>Setja upp þjónustuvörur og íhluti þjónustuvara
Áður en þú vinnur með þjónustuvörur verður þú að setja upp eftirfarandi:

* Þjónustuvöruflokkar
* Valfrjálst

## <a name="to-set-up-service-item-groups"></a>Setja upp þjónustuvöruflokka
Þú getur setja upp þjónustuvöruflokka sem tengjast hvað varðar viðgerð og viðhaldi. Skilgreina má sjálfgefin gildi vegna þjónustuvöru í þjónustuvöruflokki, t.d. svartíma, samningsafslátt í prósentum og þjónustuverðflokk. Hægt er að ráða því hvort vara í þjónustuvöruflokki sé sjálfkrafa skráð sem þjónustuvara þegar hún er seld.  

Þjónustuvöruflokkum er úthlutað til vöru á **birgða** spjaldi og þjónustuvöru á **þjónustuvöru** spjaldi.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuvöruflokkar** og svo velja viðeigandi tengil.  
2. Nýr þjónustuvöruflokkur er stofnaður.  
3. Fyllt er í reitina **Kóti** og **Lýsing**.  
4. Í reitinn **Sjálfg. samningsafsláttar %** er færð inn sjálfgefin prósenta samningsafsláttar sem á að eiga við þjónustuvöruna í flokknum.  
5. Í reitinn **Kóti sjálfg. Þjónustuverðfl.** er færður inn kóti sjálfgefins þjónustuverðflokks sem á að eiga við þjónustuvöruna í flokknum.  
6. Í reitinn **Sjálfgefinn svartími (klst.)** er færður inn sjálfgefinn svartími í klukkustundum sem á að gilda um þjónustuvöruna í flokknum.  
7. Ef skrá á vöru í flokknum sem þjónustuvöru þegar hún er seld þarf að velja reitinn **Stofna þjónustuvöru**.  

## <a name="to-set-up-service-item-components"></a>Uppsetning þjónustuvöruíhluta
Í þjónustuvöru geta verið margir íhlutir sem skipta má út með varahlutum þegar varan er í þjónustu. Þessir íhlutir eru uppsettir í síðunni **Þjónustuvara íhlutalisti**. Ef setja á upp íhluta vegna þjónustuvöru sem er uppskrift er hægt að afrita uppskriftarvöruna og stofna hana sem íhluti þjónustuvöru.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuvörur** og svo velja viðeigandi tengil.
2. Opna skal þjónustuvöruna sem á að setja upp íhluti fyrir.  
3. Velja aðgerðina **Íhlutir**. Síðan **Þjónustuvöruíhlutalisti** opnast.  
4. Bæta við nýjum íhlut.  
5. Í reitnum **Tegund** skal velja **Þjónustuvara** ef íhluturinn sjálfur er skráð þjónustuvara. Að öðrum kosti skal velja **Vara**.  
6. Í reitnum **númer** skal velja vöruna eða þjónustuvöruna sem er íhlutur þjónustuvörunnar.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>Uppsetning þjónustuvöruíhluta út frá uppskriftum
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuvörur** og svo velja viðeigandi tengil.  
2. Opna skal þjónustuvöruna sem setja á upp íhluti út frá uppskrift fyrir.  
3. Velja aðgerðina **Íhlutir**. Síðan **Þjónustuvöruíhlutalisti** opnast.  
4. Valið er **Afrita úr uppskrift** aðgerð.  

    Ef varan sem þjónustuvaran tengist er uppskrift stofnuð sjálfkrafa fyrir íhluti fyrir alla vöru í uppskriftinni.  

## <a name="to-set-up-a-service-shelf"></a>Uppsetning þjónustuhillu
Þú getur sett upp þjónustuhillur sem tilgreina hvar þú geymir þjónustuvörur þínar. Þjónustuhillum er úthlutað til þjónustuvöru í síðunum **Þjónustupöntun** og **Þjónustuvörublað**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuhillur** og svo velja viðeigandi tengil.
2. Fyllið inn í reitina eftir þörfum.

## <a name="see-also"></a>Sjá einnig
[Setja upp Kóta fyrir Staðlaða þjónustu](service-how-setup-service-coding.md)   
[Setja upp úrræðaleit](service-how-setup-troubleshooting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
