---
title: Stofna birgðaspjald fyrir vörur eða þjónustu| Microsoft Docs
description: Þú býrð til spjöld fyrir þjónustu sem þú selur sem klukkutíma og fyrir efnislegar vörur eins og t.d. samsetningaríhlutir, fullunnar vörur eða hráefni sem þú selur úr birgðum.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: 506576c6ecbc707dd44ce23294ce7eb8b6e89329
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324151"
---
# <a name="register-new-items"></a>Skrá nýjar vörur
Vörur, ásamt öðrum framleiðsluvörum, eru grundvöllur fyrirtækisins, vörurnar eða þjónustan sem þú stundar viðskipti með. Hver vara verður að vera skráð sem birgðaspjald.

Birgðaspjald inniheldur upplýsingarnar sem þarf til að kaupa, selja, geyma og tilkynna vörur.

Birgðaspjaldið getur verið af gerðinni **Birgðir**, **Þjónusta** eða **Ekki birgðir** til að tilgreina hvort vara er raunbirgðaeining, launatímaeining eða efnisleg eining sem ekki er rakin í birgðum. Nánari upplýsingar er að finna í [Um vörugerðir](inventory-about-item-types.md).

Hlutur getur verið uppbyggður sem yfireining með undirliggjandi undireiningu í uppskrift. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] getur uppskrift verið annað hvort framleiðsluuppskrift eða samsetningaruppskrift, út frá notkun. Nánari upplýsingar er að finna í [Vinna með uppskrift.](inventory-how-work-BOMs.md)

Ef sama varan er keypt frá fleiri en einum lánardrottni, er hægt að tengja þessa lánardrottna við birgðaspjaldið. Lánardrottnarnir munu þá birtast á síðunni **Vörulisti lánardrottins**, þannig að þú getir auðveldlega valið annan lánardrottin.

Vörur sem þú býður viðskiptamönnum þínum en þú vilt ekki stjórna í kerfinu þínu fyrr en þú byrjar að selja þær er hægt að setja upp sem vörulistaatriði. Vörulistaatriðum skal ekki rugla saman við venjulegar vörur af gerðinni **Engar birgðir**. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Ef vörusniðmát er til fyrir mismunandi vörutegundir, þá birtist síða þar sem búið er til nýtt birgðaspjald og hægt er að velja viðeigandi sniðmát. Ef aðeins eitt vörusniðmát er fyrir hendi, nota ný birgðaspjöld alltaf það sniðmát.

Eftirfarandi ferli skýrir hvernig á að búa til birgðaspjald frá grunni. Einnig er hægt að búa til ný birgðaspjöld með því að afrita birgðaspjald sem þegar er til staðar. Frekari upplýsingar er að finna í [Afrita fyrirliggjandi vörur í Búa til nýjar vörur](inventory-how-copy-items.md).<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Að búa til nýtt vöruspjald
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.  
2. Á síðunni **Vörur** skal velja aðgerðina **Nýtt**.

    Ef aðeins eitt vörusniðmát er fyrir hendi, opnast nýtt birgðaspjald með suma af reitunum útfyllta með upplýsingum úr sniðmátinu.
3. Á síðunni **Velja sniðmát fyrir nýja vöru** skal velja sniðmátið sem á að nota fyrir nýja birgðaspjaldið.
4. Velja hnappinn **Í lagi**. Nýtt birgðaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í suma reitina.
5. Því næst skal færa inn eða breyta reitum á birgðaspjaldinu eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Í reitnum **Aðferð kostnaðarútreiknings** seturðu upp hvernig kerfið reiknar út kostnaðarverð með því að áætla vöruflæði fyrirtækisins. Fimm aðferðir kostnaðarútreiknings eru í boði, út frá gerð vörunnar. Nánari upplýsingar eru í [Upplýsingar um hönnun: Kostnaðarútreikningar](design-details-costing-methods.md).
>
> Ef þú velur **Meðaltal** er kostnaðarverð vöru reiknað sem meðaleiningaverð vara á hverjum tímapunkti eftir innkaup. Fyrir verðmat birgða, er gert ráð fyrir að allar birgðir verði seldar á sama tíma. Með þessar stillingar geturðu valið **kostnaðarverð** reitinn á síðunni **Meðalkostnaður útreiknaður yfirlit** til að skoða færslusöguna sem meðalkostnaður er reiknaður út frá.

Þú getur skoðað eða breytt sérstöku verði eða afslætti sem þú veitir, eða sem söluaðili þinn veitir þér, fyrir vöruna Ef tiltekin skilyrði eru uppfyllt, eins og viðskiptavinur, lágmarkspöntun eða lokadagsetning. Þetta er gert með því að velja **Stilla sérverð** eða **Stilla sérstaka afslætti**. Hver lína á, til dæmis á síðunni **Söluverð**, sýnir sértækt verð. Hver dálkur táknar viðmiðun sem verður að uppfylla til að veita viðskiptamanni sérverð sem þú slærð inn í **Einingaverð** reitinn á síðunni **Söluverð**. Frekari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md) eða [Skrá sérstakt söluverð og sérstaka afslætti](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Varan hefur nú verið skráð og birgðaspjaldið má nú nota í skjölum vegna kaupa og sölu.

Ef nota á þetta birgðaspjald sem sniðmát þegar ný birgðaspjöld eru búin til, vistið það sem sniðmát. Nánari upplýsingar eru í eftirfarandi kafla.

### <a name="deleting-item-cards"></a>Eyða birgðaspjöldum
Ef þú hefur bókað færslu fyrir vöru er ekki hægt að eyða spjaldinu þar sem hugsanlega þarf að nota fjárhagsfærslurnar birgðirverðmat eða endurskoðun. Til að eyða birgðaspjöldum með fjárhagsfærslum skaltu hafa samband við samstarfsaðila Microsoft til að gera það í gegnum kóða.

## <a name="to-save-the-item-card-as-a-template"></a>Til að vista birgðaspjald sem sniðmát
1. Á síðunni **Birgðaspjald** skal velja aðgerðina **Vista sem sniðmát**. Síðan **Vörusniðmát** opnast og sýnir birgðaspjaldið sem sniðmát.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir vöruna.
4. Breyta eða færa inn víddarkóta sem munu gilda fyrir ný birgðaspjöld sem stofnuð eru með sniðmátinu.
5. Þegar lokið hefur verið við nýja vörusniðmátið skal velja hnappinn **Í lagi**.

Vörusniðmátinu verður bætt við lista vörusniðmáta þannig að hægt er að nota það til að búa til ný birgðaspjöld.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Margir lánardrottnar settir upp fyrir vörur  
Ef sama varan er keypt frá fleiri en einum lánardrottni þarf að færa inn upplýsingar um hvern lánardrottinn eins og verð, afhendingartími, afsláttur o.s.frv.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.  
2.  Velja skal viðeigandi vöru og síðan aðgerðina **Breyta**.  
3.  Veljið **Lánardrottinn** aðgerðina.  
4.  Velja reitinn **Nr. lánardrottins** og síðan velja þann lánardrottinn sem setja á upp fyrir vöruna.  
5.  Einnig er hægt að fylla inn í þá reiti sem eftir eru.  
6.  Endurtakið skref 2 til 5 fyrir hvern þann lánardrottinn sem þú vilt kaupa vöru af.

Lánardrottnarnir munu nú birtast á síðunni **Vörulisti lánardrottins**, sem þú opnar frá birgðaspjaldinu, þannig að þú getir auðveldlega valið annan lánardrottin.

## <a name="see-also"></a>Sjá einnig
[Birgðir](inventory-manage-inventory.md)  
[Afstemma birgðakostnað í fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Stofnun númeraraða](ui-create-number-series.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
