---
title: Hvernig á að taka vörur frá
description: 'Fræðast um frátekningu vara fyrir sölupantanir, innkaupapantanir og framleiðslupantanir.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 05/14/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="reserve-items"></a>Taka vörur frá

Hægt er að taka vörur frá fyrir sölu-, innkaupa-, þjónustu, samsetningarpantanir, flutningspantanir og framleiðslupantanir. Einnig er hægt að taka frá vörur í birgðum eða á innleið í opnum skjalalínum eða færslubókarlínum. Þetta er gert á síðunni **Frátekning**.

Hver lína sem er opnuð til að taka frá vörur á síðunni **Frátekning** sýnir upplýsingar um eina tegund línu (í sölu, innkaupum eða færslubók) eða birgðafærslu. Línurnar lýsa því hver margar vörur er hægt að taka frá fyrir hverja tegund línu eða færslu.

> [!TIP]
> Það fer eftir magninu sem hefur verið frátekið í birgðum og [!INCLUDE [prod_short](includes/prod_short.md)]  birtir stöðu á skjölunum þannig að fljótlegt er að átta sig á næsta skrefi. Til dæmis er hægt að senda sölupöntun eða byrja að vinna við verkefni, samsetningu eða framleiðslupöntun. Staðan hjálpar einnig til við að draga úr hættu á hlutaafhendingum eða birgðahaldi vegna birgðahalds í framleiðslu- og samsetningarpöntunum sem vantar.
>
> Reiturinn **Frátekið úr birgðaskrá** hjálpar til við að átta sig á því hvort hægt er að afhenda eða tína fyrir tiltekna pöntun eða pöntunarlínu. Í línum er reiturinn Frátekið frá birgðaskrá tiltækur í upplýsingakössum. Til að fá aðgang að upplýsingunum fyrir alla pöntunina er reiturinn á **upplýsingasíðunni**.

## <a name="reserve-items-for-sales"></a>Taka frá vörur fyrir sölu

Eftirfarandi ferli lýsir því hvernig skal taka frá vörur í sölupöntun. Skrefin eru svipuð fyrir innkaupa-, þjónustu- og flutnings- og samsetningarpöntun.
  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir**, velja síðan viðkomandi tengil.  
2. Loka sölupöntuninni.
3. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**. Síðan **Frátekning** opnast.  
4. Smellt er á línuna þar sem taka á vörurnar frá.  
5. Ein af eftirfarandi aðgerðum er valinn.  

    |**Virkni**|**Lýsing**|
    |------------------|---------------------|  
    |**Sjálfvirk frátekning**|Vörur teknar sjálfkrafa frá á síðunni **Frátekning**.|  
    |**Taka frá í gildandi línu**|Vörur teknar frá úr skjalinu á línunni sem hefur verið valin.|  
    |**Hætta við frátekningu í gildandi línu**|Að hætta við bókun á atriðum í skjalinu í línunni sem hefur verið valin.|

> [!NOTE]  
> Ef vörurakningarlínur eru til vegna sölupöntunarinnar leiðir frátekningarkerfið notandann í gegnum nokkrar séraðgerðir. Frekari upplýsingar er að finna í hlutanum [Að taka frá tiltekið rað- eða lotunúmer](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## <a name="reserve-an-item-for-a-production-order-line"></a>Taka frá vörur fyrir framleiðslupöntunarlínur

Hægt er að taka vörur frá fyrir framleiðslupantanir. Greina þarf á milli framleiðslupöntunarlína, það er yfirvaran, og framleiðslupöntunaríhluta.

Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er notuð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fastáætluð framl.pöntun**, velja síðan viðkomandi tengil.  
2. Opna fastáætluðu framleiðslupöntunina sem taka á frá yfirvörur fyrir.  
3. Viðkomandi framleiðslupöntunarlína er valin.  
4. Á flýtiflipanum **Línur** í flokknum **Aðgerðir** skal velja aðgerðina **Taka frá** .
5. Á síðunni **Frátekning** skal velja Sölulína, Pöntunarlína og velja **síðan Taka frá úr gildandi línu** aðgerð.  

Magnið sem fært var inn í fastáætluðu framleiðslupöntunarlínuna hefur verið frátekið.

## <a name="reserve-items-for-production-order-components"></a>Taka frá vörur fyrir íhluti framleiðslupöntunar

Hægt er að taka vörur frá fyrir framleiðslupantanir. Greina þarf á milli framleiðslupöntunarlína, það er yfirvaran, og framleiðslupöntunaríhluta.

Eftirfarandi aðferð sýnir hvernig fastáætluð framl.pöntun er notuð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fastáætluð framl.pöntun**, velja síðan viðkomandi tengil.  
2. Opna fastáætluðu framleiðslupöntunina sem taka á frá íhlutavörur fyrir.  
3. Viðkomandi framleiðslupöntunarlína er valin.  
4. Í flýtiflipanum **Línur** skal velja **Lína** og velja svo **Íhlutir**.  
5. Viðeigandi íhlutarlínu er valin.  
6. Á flýtiflipanum **Línur** veljið aðgerðina **Taka frá**.  
7. Á síðunni **Frátekning** skal velja línu og síðan velja aðgerðina **Taka frá úr gildandi línu**.  

Magnið sem fært var inn í fastáætluðu framleiðsluíhlutalínuna hefur verið frátekið.

## <a name="reserve-items-in-bulk"></a>Taka vörur frá í lausu

Nota síðuna **Frátekningarvinnublað** til að taka frá og úthluta innsendum vörum í lausu. Til dæmis getur magnfrátekningar hjálpað til við að tryggja að magn sé tiltækt fyrir sölu- og framleiðslupantanir. Hægt er að hafa margar keyrslur í mismunandi tilgangi. Til dæmis er hægt að úthluta framleiðslupöntunum vikulega en taka daglega frá fyrir sölu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Frátekningarvinnublað** og velja síðan viðeigandi tengja.  
2. Veljið aðgerðina **Sækja eftirspurn** . Síðan **Sækja eftirspurn til frátekninga** opnast.
1. Á síðunni **Sækja eftirspurn til frátekningar** skal tilgreina þá tegund eftirspurnar sem taka á frá úr tiltækum birgðum.
1. Afmarkanirnar eru fylltar út eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
1. Valfrjálst: Ef úthluta á vörunum strax skal velja aðgerðina **Úthluta** .
1. Á síðunni **Úthlutunarstefna** skal velja stefnu fyrir hvert skref.

   |Úthlutunarregla  |Heimildasamstæða  |
   |---------|---------|
   |Grunnur (engir árekstrar)     | Úthlutar eftirspurn í birgðum ef engir árekstrar verða og hægt er að ná yfir eftirspurnina að fullu. Til dæmis er sölupöntun A með magnið 10 og verk með magnið 7. Ef um er að ræða 20 í birgðum fær bæði eftirspurn fullt magn. Ef birgðir eru 12 er birgðunum ekki úthlutað. Magninu verður að vera úthlutað handvirkt.        |
   |Jafnt    | Dreifir tiltækum birgðum til eftirspurnar jafnt. Sölupöntun er til dæmis með magnið 10 og verk með magnið 7. Ef birgðastigið er 20 fær báðar eftirspurnirnar fullt magn. Ef birgðir þínar eru 12 þá fá báðir kröfur 6.        |
   |Eftir forgangsröðun viðskiptamanna|Skipting eftir reitnum **Forgangur** á síðunni **Viðskiptamannaspjald** . Þegar um er að ræða lágt birgðamagn birgðir birgðir Business Central fyrst hærri forgangsröðun viðskiptamanna.|

6. Til að taka frá allar línur þar sem **kveikt er á Samþykkja** skal velja aðgerðina **Gera frátekningu** .
    
## <a name="change-a-reservation"></a>Breyta frátekningu

Hægt er að breyta frátekningu á vöru.

1. Í skjalalínunni þar sem frátekningin var gerð, í flýtiflipanum **Línur**, skal velja aðgerðina **Taka frá**.  
2. Á síðunni **Frátekning** skal velja aðgerðina **Frátekningarfærslur**.
3. Á **Frátekningarfærslur**, uppfærðu reitinn **Magn** í línunni sem á að breyta.
4. Staðfesta eftirfarandi skilaboð með því að velja hnappinn **Í lagi**.

## <a name="cancel-a-reservation"></a>Hætta við frátekningu

Hægt er að hætta við frátekningu á vöru.

1. Úr fylgiskjalslínunni þar sem á að hætta við frátekningu, á flýtiflipanum **Línur** skal velja aðgerðina **Taka frá**.  
2. Á síðunni **Frátekningar** er aðgerðin **Frátekningarfærslur** valin á flýtiflipanum **Línur** .  
3. Á síðunni **Frátekningarfærslur** er valin aðgerðin **Hætta við frátekningu**.  
4. Staðfestu eftirfarandi skilaboð með því að velja hnappinn **Já**.  

## <a name="reserve-a-specific-serial-or-lot-number"></a>Taka frá tiltekið rað- eða lotunúmer

Hægt að taka frá tiltekin raðnúmer eða lotunúmer í útleiðarskjölum fyrir vörur með línurakningu, svo sem sölupantanir eða framleiðsluíhlutalista. Til dæmis getur verið gagnlegt að taka frá tiltekin rað- eða lotunúmer við eftirfarandi aðstæður:

* Ef þörf er á framleiðsluíhlutum úr tiltekinni lotu til að tryggja samræmi við eldri framleiðslukeyrslur.
* Þar sem viðskiptamaður hefur beðið um tiltekið raðnúmer. 

Frekari upplýsingar eru í [Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).

Þessi venja er vísað til ákveðinnar frátekningar vegna þess að tekið er frá úr magni vöru X sem tilheyrir lotu X. Aftur á móti, ef aðeins er tekið frá úr magni af vöru X, þá er það einfaldlega venjulegt, ósértækt, frátekning. Frekari upplýsingar eru í [Hönnunarupplýsingar: vörurakning og frátekningar](design-details-item-tracking-and-reservations.md).

Eftirfarandi ferli byggist á sölupöntun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofna sölupöntunarlínu fyrir vörurakta vöru.  
3. Úthluta rað- og lotunúmerum í sölupöntunarlínuna. Frekari upplýsingar eru í [Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).
4. Velja **Taka frá** aðgerðina í sölupöntunarlínunni.  
5. Velja hnappinn **Já** til að taka frá tiltekin rað- eða lotunúmer.  
6. Á síðunni **Vörurakningarlisti** skal velja samsetningu rað- og lotunúmers sem þú ert með úthlutaða.  
7. Veldu hnappinn **Í lagi** til að opna síðuna **Frátekning** sem sýnir aðeins framboð með tiltekna vörurakningarnúmerinu. Ef ósértækar frátekningar eru í vörurakningarnúmeri sem tilgreint hefur verið fyrir þessa línu er tilkynnt um hve mikið magn hefur þegar verið frátekið.  
8. Veldu annaðhvort aðgerðina **Sjálfvirk frátekning** eða **Taka frá í gildandi línu** til að búa til frátekningu á tilgreindum vörurakningarnúmerum.

## <a name="see-also"></a>Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: Pöntun, pöntunarrakning og stöðuboð](design-details-reservation-order-tracking-and-action-messaging.md)  
[Hönnunarupplýsingar: vörurakning og frátekningar](design-details-item-tracking-and-reservations.md)  
[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
