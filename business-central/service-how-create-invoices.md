---
title: Stofna reikninga eða kreditreikninga fyrir þjónustu
description: Læra að búa til reikninga og kreditreikninga fyrir þjónustuna.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Stofna þjónustureikninga eða kreditreikninga

Auðveld reikningsfærsla þjónustupantana er lykileiginleiki [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] þannig að þjónustutæknimaður í reitnum geti stofnað reikning fyrir þjónustu sem ekki er tengd samningi eða pöntun. Einnig er hægt að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að reikningsfæra þjónustusamninga reglulega. Reikningstímabil samnings ræður tíðni reikningsfærslu.

## Að reikningsfæra nokkra þjónustusamninga

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stofna þjónustusamningsreikninga** og velja síðan viðkomandi tengil.  
2. Færa skal inn þær afmarkanir sem á að nota.  
3. Í reitnum **Bókunardags.** er færð inn dagsetningin sem á að nota sem bókunardagsetningu á þjónustureikningum.  
4. Í reitnum **Reikningsfæra til dags.** er færð inn dagsetningin sem á að reikningsfæra samninga til. Í keyrslunni verða samningar með næstu dags. reiknings að þessari dagsetningu.  
5. Í reitnum **Aðgerð** er valið að **Stofna reikninga**.  
6. Smellt er á **Í lagi** til að stofna þjónustureikningana.  
  
Einnig er hægt að reikningsfæra þjónustusamning beint af síðunni **Þjónustusamningur** ef næsta reikningsdags. samningsins er á undan vinnudagsetningunni.

## Til að reikningsfæra þjónustusamning úr síðunni Þjónustusamningur   

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustusamningar** og velja síðan viðkomandi tengil.  
2. Velja skal þjónustusamninginn sem á að reikningsfæra og opna samningsspjaldið.  
3. Veldu aðgerðina **Stofna þjónustureikning**. 
4. Smellt er á **Já** til að stofna þjónustureikningana.  
  
  > [!NOTE]  
  > Ekki er hægt að stofna þjónustureikninga fyrir þjónustusamninginn þegar gildið í reitnum **Breyta stöðu** er **opið**.  

## Bókun reikninga úr þjónustupöntunum  

Eftirfarandi ferli lýsir því hvernig á að skilgreina þann hluta þjónustunnar sem viðskiptamaðurinn á að greiða fyrir.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.  
2. Velja skal þjónustupöntunina sem á að reikningsfæra og opna pöntunarspjaldið.  
3. Veljið aðgerðina **Þjónustulínur**.  
4. Finndu færslurnar sem þörf er á og tilgreindu magnið sem á að skrifa á reikning viðskiptamanns í reitnum **Magn til reikningsf.**   
  
   > [!NOTE]  
   > Hægt er að reikningsfæra á viðskiptamann fyrir skráða þjónustu að hluta til eða til fulls. Ef valið er að reikningsfæra viðskiptamanninn að fullu verður gildið í reitnum **Magn til reikningsf** . að vera það sama og gildið í reitnum **Magn** . Hægt er að bóka fullan reikning með fullri afhendingu og hægt er að bóka fullan reikning fyrir fulla afhendingu sem er ekki reikningsfærð eða notuð.  
   >  
   > Ef reikningur að hluta er bókaður eru tvær leiðir til þess að tilgreina magnið sem á að reikningsfæra. Ef þjónustan er bókuð með **valkostinum Afhenda og reikningsfæra** verður gildið í reitnum **Magn til reikningsf** . að vera það sama og gildið í reitnum **Magn til afhendingar** . Ef reikningsfæra á bókaða afhendingu má magn til reikningsfærslu ekki vera meira en gildið í reitnum **Afhent** magn.  
  
5. Veldu **Bóka**, og svo annað hvort **Reikning** eða **Afhenda og reikningsfæra**. Nánari upplýsingar eru í [Bókun í Þjónustukerfi](service-service-posting.md).  
  
 Þjónustulínan sem valin var er bókuð. Hægt er að bóka nokkrar þjónustulínur samtímis með því að velja þær og **velja Bóka**. Ef það er gert þarf að ganga úr skugga um að allar nauðsynlegar upplýsingar séu færðar inn í línurnar.  
  
 Þegar pöntun er bókuð með valkostinum **Reikningur** er bókaður þjónustureikningur stofnaður ásamt tilheyrandi fjárhagsfærslum og viðkomandi reitir í þjónustulínum pöntunarinnar uppfærðir. Einnig eru áður bókuð afhendingarskjöl uppfærð með reikningsfærðu magni. Ef bókunarmöguleikinn **Afhenda og reikningsfæra** er jafnframt stofnuð bókuð afhending.

## Þjónustureikningar búnir til handvirkt  

Ef þjónustupöntun er bókuð með valkostinum **Reikningur** eða **Afhenda og reikningsfæra** býr forritið sjálfkrafa til bókaða reikningsfærslu. Þó getur þurft að gefa út reikning sem ekki er tengdur þjónustusamningi eða pöntun. Þessi aðgerð útskýrir hvernig gefa á út reikning á sama tíma og viðskiptamaðurinn fær þjónustuna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustureikningar** og velja síðan viðkomandi tengil.  
2. Nýr þjónustureikningur er stofnaður.  
3. Fylla þarf út reitinn **Nr.**. .  
  
    > [!NOTE]  
    >  Ef númeraröð hefur verið sett upp fyrir þjónustureikninga á síðunni **Þjónustukerfisgrunnur** er hægt að velja **Færslulykill** til að velja næsta lausa þjónustureikningsnúmer.  
  
4. Í **Númer viðskiptamanns** reitinn er fært inn númer viðskiptamanns. Veljið viðeigandi viðskiptamann af listanum.  
  
    Fyllt er í viðskiptavinareiti með upplýsingum úr spjaldinu **Viðskiptavinur**.  
  
5. Dagsetning er færð inn í reitinn **Bókunardags.** Þessi dagsetning mun birtast á bókuðum færslum. Þessi dagsetning mun birtast á bókuðum færslum. Þessi reitur sýnir núverandi vinnudagsetningu en dagsetningunni má breyta.  
6. Í reitinn **Dags** . fylgiskjals er færð inn dagsetning sem birtist á prentaða reikningnum og notuð við útreikning gjalddaga.  
7. Fylla inn í þjónustulínur reikningsins. Fylla inn í reitina **Tegund**, **Nr.** og **Magn** til þess að skrá vörur, magn og kostnað sem notað hefur verið í þjónustu.

## Til að stofna reikning sem sameinar bókaðar sendingarlínur úr einni eða fleiri þjónustupöntunum 

Hugsanlega þarf að stofna þjónustureikning fyrir þjónustu sem þegar hefur verið afhent, annaðhvort úr einni eða fleiri þjónustupöntunum, en ekki enn reikningsfærð eða notuð. Hægt er að fylla reikningslínurnar út sjálfkrafa ásamt völdum bókuðum afhendingarlínum fyrir tilgreindan viðskiptamann.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustureikningar** og velja síðan viðkomandi tengil.  
2. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Stofna skal reikningslínur fyrir afhenta þjónustu sem ekki er búið að reikningsfæra. Að öðrum kosti geturðu notað **Sækja afhendingarlínur** aðgerðina til að bæta bókuðum afhendingarlínum við reikninginn.  
4. Bóka skal þjónustureikninginn.  
  
 Bókaði þjónustureikningurinn og samsvarandi fjárhagsfærsla eru stofnuð. Áður bókuð afhendingarskjöl uppfærast með reikningsfærðu magni og magni í þjónustulínum upprunapantananna.  

## Þjónustukreditreikningar búnir til:  

Þjónustukreditreikningsskjal er gjarnan notað þegar viðskiptamaður skilar vöru. Hins vegar er einnig hægt að nota hann til að endurgreiða viðskiptamanni eða leiðrétta reikning sem voru mistök.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustukreditreikningar** og velja síðan viðkomandi tengil.  
2. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Reitirnir **Bókunardagsetning** og **Dagsetning fylgiskjals** sýna vinnudagsetninguna. Hægt er að breyta því ef þörf er á.    
4. Í kreditreikningslínurnar eru færðar upplýsingar um vörurnar sem hefur verið skilað eða hafa verið fjarlægðar, eða söluuppbót sem á að gefa viðskiptamanni.  

## Leiðrétta villur í þjónustureikningum

Hægt er að eyða þjónustureikningum með þjónustufærslum sem tengjast þeim. Þetta þýðir að hægt er að leiðrétta villur eða gera breytingar á þjónustureikningum án þess að festast eða tapa gögnum. Ef gleymist t.d. að úthluta vörubókunarflokki á fjárhagsreikning er hægt að bæta honum við og endurræsa þjónustureikninginn.

Nota aðgerðartáknið :::image type="content" source="media/copilot-delete-trash-can.png" alt-text="Eyða aðgerð tákn"::: Eyða aðgerð til að eyða þjónustureikningi. 

Þegar þjónustureikningi er eytt gerast eftirfarandi hlutir:

* Bóka þjónustufærslu til leiðréttingar
* Endurheimta reikningsfærsludagsetningu og tímabil samningsins sem gerir kleift að stofna reikninginn aftur.

> [!NOTE]
> Hægt er að bakfæra nokkra reikninga en það þarf að gera í röð og byrja á síðasta reikningi.
>
> Ekki er hægt að eyða þjónustureikningi ef sundurliðun þess, t.d. reikningstímabili eða fyrirframgreiddu **vífærslnunum** var breytt í tengdum þjónustusamningi. Ganga þarf úr skugga um að reikningum sé eytt áður en stillingum þjónustusamningsins er breytt.

## Sjá einnig .

[Bóka þjónustureikninga](service-how-to-post-service-orders.md)  
[Þjónustustýring sett upp](service-setup-service.md)  
[Bókun þjónustu](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]