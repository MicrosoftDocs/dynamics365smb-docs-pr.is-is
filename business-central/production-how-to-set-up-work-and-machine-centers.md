---
title: Hvernig á að setja upp vinnu- og vélastöðvar | Microsoft Docs
description: '**Vinnustöðvarspjald** skipuleggur föst gildi og þarfir viðkomandi framleiðsluforða og stjórnar þannig afköstum framleiðslu þeirrar vinnustöðvar.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b247cdc220ad522fe42085528df8a25200d6dd48
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440304"
---
# <a name="set-up-work-centers-and-machine-centers"></a>Setja upp vinnu- og vélastöðvar

Forritið greinir á milli þrennskonar afkastagetu. Henni er raðað eftir stigveldi: Á hverju stigi eru undirstig.  

Efsta stigið er vinnustöðvarflokkurinn. Vinnustöðvum er úthlutað á vinnustöðvaflokkana. Hver vinnustöð getur aðeins tilheyrt einum vinnustöðvarflokki.

Hægt er að úthluta ýmsum vélastöðvum á hverja vinnustöð. Aðeins ein vélastöð getur tilheyrt hverri vinnustöð.  

Áætluð afkastageta vinnustöðvarinnar samanstendur af tiltækileika samsvarandi vélastöðva og áætlaðrar aukaafkastagetu vinnustöðvarinnar. Áætlaður tiltækileiki vinnustöðvarflokksins er því samtala alls samsvarandi tiltækileika véla- og vinnustöðva.  

Það sem er til ráðstöfunar er geymt í dagatalsfærslum.  

> [!IMPORTANT]
> Áður en þú setur upp vinnu- eða vélastöðvar, þarftu að setja upp dagatal verkstæðis. Nánari upplýsingar eru í [Búa til dagatal verkstæðis](production-how-to-create-work-center-calendars.md).

## <a name="to-set-up-a-work-center"></a>Vinnustöð sett upp

Eftirfarandi lýsir fyrst og fremst því hvernig vinnustöð er sett upp. Skrefin í uppsetningu dagatals vélastöðva eru svipuð, fyrir utan flýtiflipann **Uppsetning leiða**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnustöðvar** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í reitnum **Vinnustöðvarhópur** skal velja efra-stigs forðaflokkun sem vinnustöðin er flokkuð undir, ef það á við. Valið er **Nýtt** aðgerðin í felllilistanum.  
5. Veljið reitinn **Lokaður** til að koma í veg fyrir að vinnustöðin verði notuð í vinnslu. Þetta þýðir að frálag er ekki hægt að bóka fyrir vörur sem er framleidd í vinnustöðinni. Frekari upplýsingar eru í [Bóka framleiðslufrálag](production-how-to-post-output-quantity.md).
6. Í reitinn **Innk.verð** er færður inn kostnaður við að framleiða eina mælieiningu í þessari vinnustöð, án annarra kostnaðarliða. Þessi kostnaður er oft kallaður *beinn vinnutaxti*.  
7. Í reitinn **Óbein kostnaðar %** er færður inn almennur aðgerðakostnaður við notkun vinnustöðvarinnar sem hlutfall af Innkaupsverði. Þessari hlutfallslegu upphæð er bætt við beinan kostnað í útreikningum á kostnaðarverði.  
8. Í reitinn **Hlutf. sameiginl. kostn.** er færður inn kostnaður vegna vinnustöðvar sem ekki kemur aðgerðum beint við, s.s. viðhaldskostnað, sem algilda tölu.  

    Reiturinn **Kostn.verð** inniheldur reiknað kostnaðarverð einnar mælieiningar, með öllum kostnaðarliðum, í þessari vinnustöð, sem hér segir:  

    Kostnaðarverð = Innkaupsverð + (Innkaupsverð x Óbein kostnaðar %) + Hlutfall sameiginlegs kostnaðar.  

9. Í reitnum **Útreikningur kostn.verðs** er tilgreint hvort útreikningurinn hér að ofan sé byggður á tímafjölda:  **Tími**; eða fjölda framleiddra eininga:  **Einingar**.  
10. Veljið reitinn **Tiltekinn einingarkostnaður** ef á að skilgreina einingarkostnað vinnustöðvar í leiðarlínunni þar sem hann er notaður. Slíkt kann að eiga við aðgerðir með verulegan mismun í kostnaði afkastagetu miðað við það sem er venjulega unnið í vinnustöðinni.  
11. Í reitnum **Birgðaskráningaraðferð** er valið hvort reikna á og bóka frálagsbókun á þessari vinnustöð handvirkt eða sjálfvirkt með annarri hvorri eftirfarandi aðferð.

    |Valkostur|Description|
    |------|-----------|
    |**Handvirkt**|Notkun er bókuð handvirkt í frálagsbókinni eða framleiðslubókinni.|
    |**Framvirkt**|Notkun er reiknuð og bókuð sjálfvirkt þegar framleiðslupöntun er gefin út.|
    |**Afturvirkt**|Notkun er reiknuð og bókuð sjálfvirkt þegar framleiðslupöntun er lokið.|

    > [!NOTE]
    > Ef nauðsyn krefur er hægt að hundsa birgðaskráningaraðferðina sem er valin hér og á spjaldinu **Vara** í einstökum aðgerðum með því að breyta stillingunum á leiðarlínum

12. Í reitinn **Mælieiningarkóði** er færð inn tímaeiningin þar sem þessi kostnaðarútreikningur og afkastagetuáætlun vinnustöðvar eru gerð.
    Til að geta fylgst stöðugt með notkun verður fyrst að setja upp mæliaðferð. Einingarnar sem eru færðar inn eru grunneiningar. Vinnslutíminn er til dæmis mældur í klukkustundum og mínútum.

    > [!NOTE]  
    > Ef valið er að nota Dagar Skal hafa það í huga að 1 dagur = 24 klukkustundir - en ekki 8 (vinnustundir).

13. Í reitnum **Geta** er tilgreint hvort vinnustöð er með fleiri en einn einstakling við vinnu og eina vél í vinnslu á sama tíma. Ef uppsetning [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur ekki Vélastöðvaraðgerð verður gildið í þessum reit að vera **1**.  
14. Í reitinn **Skilvirkni** er fært inn hlutfall áætlaðra staðlaðra afkasta sem þessi vinnustöð afkastar í raun. Ef fært er inn **100** þýðir það að raunveruleg afköst vinnustöðvarinnar eru þau sömu og staðlaða afkastagetan.  
15. Velja skal **Sameinað dagatal** gátreitinn ef þú ert líka að nota vélstöðvar. Þetta tryggir að dagatalsfærslur verði settar saman frá vélastöðva dagatölum.  
16. Í reitnum **Dagatalskóti verkstæðis** veljið dagatal verkstæðis. Nánari upplýsingar eru í [Búa til dagatal verkstæðis](production-how-to-create-work-center-calendars.md).  
17. Í reitnum **Biðraðartími** er tilgreindur fastur tími sem þarf að líða áður en úthlutað verk er hafið á þessari vinnustöð. 

> [!NOTE]
> Nota skal biðtíma til að veita smá tíma á milli þess þegar íhluturinn kemur á vél eða vinnustöð og þegar aðgerðin hefst í raun. Ef til dæmis hlutur er afhentur vélastöð klukkan 10:00 en það tekur klukkustund að festa hann við vél hefst aðgerðin ekki fyrr en 11:00. Biðtíminn yrði þá ein klukkustund. Gildið úr reitnum **Biðraðartími** á véla- eða Vinnustöðvarspjaldi plús samtala gildanna í reitunum **Uppsetningartími**, **Keyrslutími**, **Biðtími** og **Flutningstími** í vöruleiðarlínunni gefa afgreiðslutímann í framleiðslu vörunnar. Þetta hjálpar til við að gefa upp nákvæman framleiðslutíma alls.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Dæmi - Mismunandi vélastöðvum úthlutað á vinnustöð

Mikilvægt er að áætla nauðsynlega heildarafkastagetu við uppsetningu véla- og vinnustöðva.

Ef mismunandi vélastöðvum (t.d. 210 Pökkunarborð 1, 310 Málningarklefi) er úthlutað á vinnustöð þarf að taka með í reikninginn afkastagetu vélastöðvanna þar sem bilun í einni vinnustöð getur tafið allan ferilinn. Hægt er að færa inn vélarhópana samkvæmt getu þeirra en ekki má taka tillit til þeirra í áætluninni. Með því að gera reitinn **Sameinað dagatal** óvirkan er afkastagetu vinnustöðvarinnar en ekki vélastöðvarinnar úthlutað í áætluninni.

Ef hins vegar sams konar vélastöðvar (t.d. 210 Pökkunarborð 1 og 220 Pökkunarborð 2) eru sameinaðar í eina vinnustöð er það vinnustöðin sem samtala úthlutaðra vélastöðva sem skiptir höfuðmáli. Því yrði vinnustöðin skráð með enga getu. Með því að virkja reitinn **Sameinað dagatal** er sameiginlegri afkastagetu úthlutað á vinnustöðina.

Ef ekki á að taka með afkastagetu vinnustöðva í heildarafkastagetunni má stilla skilvirkni = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Vinnu- eða vélastöð með takmarkaða afkastagetu sett upp

Setja þarf upp framleiðsluforða sem talinn er mikilvægur og merkja hann þannig að hann samþykki takmarkað álag í staðinn fyrir sjálfgefið, ótakmarkað álag sem annar framleiðsluforði samþykkir. Tilfang með takmarkaða afkastagetu getur verið vinnu- eða vélastöð sem þú hefur greint sem flöskuháls og vilt setja takmarkað álag á.

[!INCLUDE[prod_short](includes/prod_short.md)] styður ekki sundurliðaða vinnusalsstýringu. Hún áætlar gerlega nýtingu tilfanga með því að leggja fram grófa áætlun en stofnar ekki og viðheldur sjálfkrafa ítarlegum áætlunum, byggðum á reglum um forgangsröðun eða bestun.

Á síðunni **Tilföng með takmarkaða afkastagetu**, geturðu búið til uppsetning sem forðast yfirálag á tilgreind tilföng og tryggir að engin afkastageta sé án úthlutunar ef úthlutun á henni gæti aukið viðdvalartíma framleiðslupöntunar. Í reitnum **Hömlur (% af heildar afkastagetu)** má bæta við hömlutíma á tilföng til að draga úr skiptingu aðgerðar. Þetta gerir kerfinu kleift að áætla hleðslu á síðasta mögulega dag með því auka álagsprósentuna lítillega ef það er hægt að minnka fjölda virkni sem er skipt.

Við áætlum á tilföngum með takmarkaða getu tryggir kerfið að engin tilföng séu hlaðin yfir skilgreina getu (hættumörk) Þetta er gert með því að úthluta hverri virkni á næsta tiltekna tímabil. Ef tímabilið er ekki nógu langt til að hægt sé að ljúka allri aðgerðinni verður aðgerðinni skipt í tvo eða fleiri hluta á næstu tiltæku tímabilum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng takmarkaðrar afkastagetu** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn í reitina eftir þörfum.

> [!NOTE]
> Aðgerðir á vinnustöðvum eða vélastöðvum sem settar eru upp sem takmarkaður forði verða alltaf áætlaðar í röð. Það þýðir að jafnvel ef takmarkaður forði er með margar afkastagetur þá eru aðgerðir sem þessar getur framkvæma aðeins áætlaðar í röð, ekki samhliða, eins og yrði gert ef vélastöðin var ekki sett upp sem takmarkaður forði. Reiturinn Geta í vinnu- eða vélastöð er hærri en 1 fyrir takmarkaðan forða

> Í tilviki uppskiptingar starfssemi er uppsetningartíma aðeins  úthlutað einu sinni vegna þess að það er gert ráð fyrir að sumir handvirk jöfnun sé gerð til að hámarka áætlun.

## <a name="see-also"></a>Sjá einnig

[Stofna dagatal verkstæðis](production-how-to-create-work-center-calendars.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]