---
title: Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur
description: Færslur milli fyrirtækja sem berast þér rafrænt frá MF-félögum eru taldar upp í MF-innhólfinu, þar sem þú vinnur þær sjálfvirkt eða handvirkt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: 600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611
ms.date: 03/09/2022
ms.author: edupont
ms.openlocfilehash: 868f07b2b56ccaefb4c56e26be72c27b941d950c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522119"
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur
Allar færslur milli fyrirtækja sem berast þér rafrænt frá MF-félögum eru taldar upp í MF-innhólfinu.  

Hins vegar eftir því hvernig samstæðufyrirtæki eru sett upp fyrir fyrirtækið eru sumar færslur sjálfkrafa endureftirsettar á viðkomandi samstæðufélaga. Þegar byrjað er á 2022 1 er hægt að setja upp fyrirtækið fyrir sjálfvirka stofnun samstæðufærslna frá samstæðufélögum, bókað í gegnum almenna færslubók innan samstæðu. Frekari upplýsingar er að finna [til að fylla út og bóka samstæðufærslubók](intercompany-how-work-documents-journals.md#to-fill-in-and-post-an-intercompany-journal).  

## <a name="organizing-the-inbox"></a>Innhólfinu raðað  
 Hægt er að nota afmörkunarreitina efst í innhólfsglugganum til að ákvarða hvaða færslur eru birtar á síðunni. Til dæmis, ef aðeins á skoða færslur sem tiltekinn félagi stofnaði er hægt að færa inn afmarkanir í afmörkununum **Uppruni færslu** og **MF-félagakóti**.  

### <a name="transaction-source"></a>Uppruni færslu  
Það sem hægt er að gera við færslu fer eftir því hvort hún var:  

- Stofnuð af Millifyrirtækjafélaga  
- Hafnað af MF-félaga og send til baka  

Hægt er að nota reitinn **Sýna uppruna færslu** til að afmarka síðuna **MF-innhólfsfærslur** þannig að í honum birtist aðeins önnur af þessum færslutegundum. (Einnig er hægt að afmarka eftir MF-félaga eða eftir efni reitarins **Línuaðgerð**.)  

#### <a name="created-by-intercompany-partner"></a>Stofnuð af Millifyrirtækjafélaga  
 Þegar ný færsla berst sem var stofnuð af félaga er hægt að velja að:

- Samþykkja færsluna  
- Hafna færslunni (endursenda til félaga)  
- Ógilda færsluna (eyða færslunni en senda hana ekki aftur til félaga)  

#### <a name="returned-from-intercompany-partner"></a>Skilað af Millifyrirtækjafélaga  
 Ef færslunni var hafnað af Millifyrirtækja-félaga er eina valið að ógilda færsluna í innhólfinu. Síðan þarf að stofna leiðréttingarlínur eða bakfæra færslubókina eða fylgiskjalið í fyrirtækinu.  

## <a name="recreating-inbox-entries"></a>Innhólfsfærslur stofnaðar aftur  
 Ef færsla var samþykkt í innhólfinu en fylgiskjalinu eða færslubókinni var síðan eytt án þess að bóka hana er hægt að stofna innhólfsfærsluna aftur og samþykkja hana aftur.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Yfirlit yfir færslur milli fyrirtækja á tímabili  
 Hægt er að fá yfirlit yfir allar færslur milli fyrirtækja sem tekið var við og hafa verið sendar á tilteknu tímabili. Í skýrslunni **Millifyrirtækjafærslur** koma fram allar fjárhagsfærslur, viðskiptamannafærslur og lánardrottnafærslur milli fyrirtækja.

 > [!NOTE]  
 > Ef millifyrirtækjafélagar eru í sama gagnagrunni, eru færslur framkvæmdar án þess að nota þurfi skrá eða tölvupóst. Sjá **Færslugerð** reitinn á síðunni **Millifyrirtækjafélagi**. <br /><br />
Í því tilfelli, geturðu sett upp kerfi til að tengja fram hjá innhólfinu og úthólfinu með því að velja **Samþykkja færslur sjálfvirkt** gátreitinn á síðunni **Millifyrirtækjafélagi** og **Senda færslur sjálfvirkt** gátreitinn á síðunni **Uppsetning millifyrirtækis**. Aðeins er hægt að samþykkja utanaðkomandi samstæðufærslur ef verkáætlun er virkjuð. Frekari upplýsingar er að finna [í samskipun Verkáætlunarstillinga fyrir miðlægu Viðskiptaþjón](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task).

## <a name="to-import-intercompany-transactions-from-a-file"></a>Færslur milli fyrirtækja fluttar inn úr skrá:

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Ef fyrirtækið er með milli-fyrirtækjafélaga sem er ekki í sama gagnagrunni og fyrirtækið er hægt að taka á móti færslum milli fyrirtækja frá félaganum í XML-skrá. Síðan þarf að flytja færslurnar inn í innhólfið.  

1. Vistið skrána á birgðageymsluna sem tilgreind var í reitnum upplýsingar **um** MF-Innhólf þegar sett er upp Samstæða.  
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-innhólfsfærslur** og velja síðan viðkomandi tengil.
3. Á síðunni **Færslur í innboxi millifyrirtækis** skal velja **Flytja inn færsluskrá** aðgerðina.  
4. á síðunni sem birtist er XML-skráin með færslunum valin og síðan smellt á hnappinn **Opna**.  

Færslurnar eru fluttar inn í innhólfið og nú er hægt að vinna með þær.

## <a name="to-process-incoming-intercompany-transactions"></a>Vinna færslur milli fyrirtækja á innleið  
Þegar milli-fyrirtækjafélagar senda færslur milli fyrirtækja enda færslurnar í milli-fyrirtækjainnhólfinu. Meta þarf hverja færslu í innhólfinu og bregðast við henni.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-innhólfsfærslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Færslur í innhólfi millifyrirtækis** skal velja línu og síðan aðgerð, eins og t.d. **Samþykkja** til að setja línuna í ferli.
3. Á síðunni **Lokið MF-innhólf aðgerð** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velja hnappinn **Í lagi**.  

Fyrir línur sem þú setur í ferli með **Samþykkja** aðgerðinni, verða fylgiskjöl eða færslubókarlínur síðan stofnaðar í fyrirtækinu. Opna skal hvert fylgiskjal eða færslubók, gera nauðsynlegar breytingar og bóka.  

Línur sem þú vannst með **Skila til félaga** aðgerðinni verða settar í úthólfið þaðan sem þú getur síðan sent þær til félaga þíns.

Fyrir línur sem þú vannst með aðgerðinni **Skilað af félaga** verður nú að bóka leiðréttingu á upphaflegu færslunni sem bókuð var í fyrirtækinu.

## <a name="to-process-outgoing-intercompany-transactions"></a>Vinna færslur milli fyrirtækja á útleið  
Þegar færslubók eða fylgiskjal milli fyrirtækja er bókað eða pantanastaðfesting milli fyrirtækja er send fara færslurnar í milli-fyrirtækja úthólfið. Til að þær verði sendar til milli-fyrirtækjafélaga þarf að opna úthólfið og vinna úr þeim.  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-úthólfsfærslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Færslur í úthólfi millifyrirtækis** skal velja línu og síðan aðgerð, eins og t.d. **Fara aftur í innhólf** til að setja línuna í ferli.

Línur sem þú vannst með aðgerðinni **Senda til millifyrirtækjafélaga** verða sendar í innhólf viðeigandi félaga.

Línur sem þú vannst með **Skila til félaga** aðgerðinni verða settar í innhólfið þar sem þú getur síðan samþykkt þær til að búa til skjöl eða færslubókarlínur í fyrirtækinu.  

Fyrir línur sem þú vannst með aðgerðinni **Hætta við** verður nú að bóka leiðréttingu á upphaflegu færslunni sem bókuð var í fyrirtækinu.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Innhólfsfærslur milli fyrirtækja endurstofnaðar  
Einstaka sinnum gæti verið ráðlegt að stofna aftur viðskipti í innhólfinu eða úthólfinu. Ef t.d. færsla var samþykkt í innhólfinu en fylgiskjalinu eða færslubókinni var síðan eytt án þess að bóka hana er hægt að stofna innhólfsfærsluna aftur og samþykkja hana aftur.  

Eftirfarandi ferli lýsir hvernig eigi að endurstofna innhólfsfærslur, en sömu skref eiga einnig við um úthólfið.

  1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afgreiddar MF-innhólfsfærslur** og velja síðan viðkomandi tengil.  

  2.  Á síðunni **Afgreiddar MF-innhólfsfærslur** veljið línuna með færslunni sem á að stofna aftur í innhólfinu, og veljið svo **Endurstofna innhólfsfærslu** aðgerðina.  

## <a name="see-also"></a>Sjá einnig
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna við Almennar færslubækur](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
