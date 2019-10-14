---
title: Hvernig á að stofna Þjónustupantanir | Microsoft Docs
description: Hægt er að nota síðuna **Þjónustupöntun** til að stofna skjöl þar sem hægt er að færa inn upplýsingar um þjónustu, s.s. viðgerðir og viðhald, á þjónustuvörum að beiðni viðskiptamanns.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2e27844b708982e76ce4dfcf15ec02f7190cd855
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311717"
---
# <a name="create-service-orders"></a>Stofna þjónustupantanir
Hægt er að nota síðuna **Þjónustupöntun** til að stofna skjöl þar sem hægt er að færa inn upplýsingar um þjónustu, s.s. viðgerðir og viðhald, á þjónustuvörum að beiðni viðskiptamanns.  

Þegar stofnuð er þjónustupöntun þarf aðeins að fylla út í örfáa reiti. Sumir reitir eru valkvæðir og margir fyllast út sjálfkrafa þegar tengdir reitir eru fylltir út.  

## <a name="to-create-a-service-order"></a>Þjónustupöntun stofnuð:    
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **þjónustupantanir** og veldu síðan tengda tengilinn.  
2. Ný þjónustupöntun er stofnuð.  
3. Í reitnum **númer** er fært inn númer fyrir þjónustupöntunina.  

     Hafi númeraröð fyrir þjónustupöntun verið sett upp á síðunni **Þjónustukerfisgrunnur** er einnig hægt að styðja á færslulykilinn til að velja næsta lausa þjónustupöntunarnúmer.  

4. Í **Númer viðskiptamanns** reitnum, veljið viðeigandi viðskiptamann af listanum. Fyllt er í viðskiptamannareiti með upplýsingum úr töflunni **Viðskiptamaður**.  

5. Vegna stillinga á flýtiflipanum **Áskildir reitir** á síðunni **Þjónustukerfisgrunnur** þarf kannski að fylla út reitinn **Þjónustupöntunartegund** og reitinn **Kóti sölumanns**.  
6. Aðrir reitir eru fylltir út ef þurfa þykir.  
7. Skrá skal þjónustuvörulínur.  

## <a name="to-create-a-service-order-from-a-contract"></a>Þjónustupantanir stofnaðar út frá samningum  
Hægt er að stofna þjónustupantanir sjálfkrafa til viðhalds þjónustuvöru á grunni þjónustusamnings.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Stofna samningsþjónustupantanir** og veldu síðan tengda tengilinn.  
2. Á flýtiflipanum **Haus þjónustusamnings** eru færðar inn afmarkanirnar sem á að nota.  
3. Farið er á flýtiflipann **Valkostir** og reitirnir **Upphafsdagsetning** og **Lokadagsetning** fylltir út með upphafs- og lokadagsetningu tímabilsins sem stofna á samningsþjónustupantanir fyrir. Keyrslan stofnar þjónustupantanir sem ná einnig til þjónustuvöru í þjónustusamningum með næstu áætluðu þjónustudagsetningum á tímabilinu.  

    > [!NOTE]  
    >  Takmörk eru fyrir þeim dagafjölda sem má vera milli dagsetninga í hvert sinn sem keyrslan er framkvæmd. Þessi mörk eru stillt í reitnum **Hám.dagafj. samn.þjón.pantana** á síðunni **Þjónustukerfisgrunnur**.  

4. Í reitnum **Aðgerð** er valið að **Stofna þjónustupöntun**.  

## <a name="to-convert-a-service-quote-to-a-service-order"></a>Þjónustutilboði breytt í þjónustupöntun:
Þegar viðskiptamaður tekur tilboði um þjónustutilboð er því breytt í þjónustupöntun. Tilboðinu er eytt og ný þjónustupöntun er sett upp með sömu lýsingu og þjónustutilboðið. Svardagsetningin og tími vegna þjónustupöntunar eru endurreiknuð og staðan er stillt á **Í undirbúningi**. Viðgerðarstöðu þjónustuvörunnar í pöntuninni er breytt í **Upphafleg**.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] leitar að úthlutunarfærslum vegna allrar þjónustuvörunnar í þjónustutilboðinu sem er með stöðuna **Virkt**. Ef slík úthlutunarfærsla finnst er staða úthlutunar uppfærð úr Virk í **Þarf að endurúthluta**. Þegar þjónustuvörunni í þjónustupöntuninni er endurúthlutað er stöðu úthlutunarfærslna sem skráðar eru vegna tilboðsins uppfærðar í **Lokið.**   

1. Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustusamningstilboð** og veldu síðan tengda tengilinn.  
2. Veldu Þjónustutilboðið sem breytt á í þjónustupöntun.  
3. Velja **búa til pöntun** aðgerð.  

## <a name="to-check-item-availability-for-one-or-more-orders"></a>Til að athuga hvort vörur séu tiltækar fyrir einn eða fleiri pantanir  
Hægt er aðgæta hvort vara sem þörf er á til að hægt að á anna pöntun sé á lager og ef svo er ekki, hvenær hún kemur á lager. Auk þess er hægt að taka frá vöru sem er tiltæk til að tryggja að nota megi hana síðar. Hægt er að kanna framboð fyrir ákveðna pöntun eða fyrir allar pantanir.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afgreiðslustöð** og veldu síðan tengda tengilinn.  
2. Gert er eitt af eftirfarandi:  

    * Fyrir sérstaka pöntun, velja pöntunina, og síða velja **Yfirlit yfir eftirspurn** aðgerðina.  
    * Fyrir allar pantanir skal velja **Sýna skjal**. Síðan **Þjónustupöntun** opnast.  

3. Í glugganum **Yfirlit yfir eftirspurn** stækkið vöruflokkinn og skoðið upplýsingar um framboð vörunar. Til dæmis er hægt að sjá hversu margar vörur eru í birgðum. Einnig er hægt að sjá hvort og þegar vara verður tiltæk ef hún er í biðpöntun, þ. e. Tegund uppruna = Innkaup, eða hvort hún hafi verið tekin frá.

## <a name="to-reserve-an-item-for-a-service-order"></a>Til að taka frá vöru fyrir þjónustupöntun
Ef þú þarft að vera viss um að vara sé tiltæk fyrir þjónustupöntun, geturðu tekið vöruna frá.

1. Í reitnum **Leita** skal færa inn **Þjónustupantanir** og velja síðan viðkomandi tengi.  
2. Veljið þjónustupöntunina og velja svo **Breyta**.  
3. Velja **Aðgerðir**, velja **Röð** og smella síðan á **Þjónustulínur**.  
4. Á síðunni **Þjónustulínur** skal velja vöruna sem á að taka frá og velja síðan **Taka frá** aðgerðina.  
5. Á síðunni **Frátekning** skal velja **Taka frá í gildandi línu**.

## <a name="to-insert-lines-based-on-standard-service-codes"></a>Setja inn línur byggðar á staðlaðir þjónustukóðar  
Ef staðlaðir þjónustukótar hafa verið settir upp og þeim verið úthlutað fyrir þjónustuvöruflokka er hægt að setja inn staðlaðar línur tengdar stöðluðum þjónustukótum í þjónustuskjölum. Frekari upplýsingar eru í [Setja upp staðlaða þjónustukóða](service-how-setup-service-coding.md).   

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **þjónustupantanir** og veldu síðan tengda tengilinn.  
2. Ný þjónustupöntun er stofnuð.  
3. Fyllið inn í svæðin eftir þörfum.  
4. Fylla út þjónustuvörulínur með nauðsynlegum upplýsingum.  
5. Velja skal línuna með þjónustuvörunni sem á að stofna þjónustulínur fyrir og velja síðan **Sækja staðl. þjónustukóta**. Síðan **Fl.kóti staðl. þjón.vöru** opnast með stöðluðum kótum fyrir þjónustuvöruflokkinn sem tilgreindur er í línunni.  
6. Viðeigandi kóti er valinn og síðan smellt á **Í lagi** hnappinn til þess að færa inn staðlaðar þjónustulínur.  

> [!NOTE]  
>  Ef reiturinn **Þjónustuvöruflokkskóti** í þjónustuskjalinu er auður merkir það að þjónustuvaran tilheyri engum þjónustuvöruflokki. Ef svo er inniheldur síðan **Fl.kótar staðlaðrar þjónustuvöru** lista yfir staðlaða þjónustukóta. Velja þarf af listanum til þess að setja staðlaðar þjónustulínur inn í skjalið. Einnig er hægt að velja af lista staðlaðra þjónustukóta sem úthlutað hefur verið fyrir tilgreindan þjónustuvöruhóp. Til þess að skoða listann er viðeigandi kóti valinn í reitnum **Þjónustuvöruflokkskóti** á síðunni **Fl.kótar staðlaðrar þjónustuvöru**.  

## <a name="to-register-internal-or-public-comments"></a>Skráning á innanhúss eða almennar athugasemdir
Þú getur bætt við athugasemdum sem verða prentaðar á þjónustupantanir og þjónustutilboð til að bjóða upp á viðbótarupplýsingar. Hægt er að færa inn allt að 80 stafi, með bilum. Ef færa á inn viðbótartexta er farið í næstu línu. Til að skrá athugasemd skal velja línu og síðan velja aðgerðina **Athugsemd**.  

## <a name="to-delete-invoiced-service-orders"></a>Reikningsfærðum þjónustupöntunum eytt:  
Pöntunum er yfirleitt eytt sjálfkrafa þegar þær hafa verið reikningsfærðar til fulls. Þegar reikningur er bókaður er samsvarandi færsla stofnuð á síðunni **Bókaðir þjónustureikningar** . Hægt er að skoða bókaða fylgiskjalið á síðunni **Bókaður þjónustureikningur**.  

Forritið eyðir þjónustupöntun ekki sjálfkrafa ef heildarmagn pöntunarinnar hefur verið bókað af síðunni **Þjónustureikningur** en ekki í þjónustupöntuninni sjálfri. Þá þarf að eyða bókuðum pöntunum sem ekki var búið að eyða. Hægt er að gera það með því að nota keyrsluna **Eyða reikningsfærðum þjónustupöntunum**.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða reikningsfærðum þjónustupöntunum** og veldu síðan tengda tengilinn. Síðan sem sýnir beiðni um keyrsluna **Eyða reikningsfærðum þjónustupöntunum** opnast.  
2. Til að velja pantanirnar sem á að eyða geturðu velja afmarkanir í reitunum **Nr.**, **Númer viðskiptamanns.** og **Reikn.færist á viðskm.** Reitir  
3. Velja **Í lagi**.  


## <a name="see-also"></a>Sjá einnig  
[Bókun þjónustu](service-service-posting.md)  
[Þjónustupantanir bókaðar](service-how-to-post-service-orders.md)  
[Þjónustustýring sett upp](service-setup-service.md)  
[Vinna við þjónustuverk](service-how-to-work-on-service-tasks.md)  
[Úthluta forða](service-how-to-allocate-resources.md)  
