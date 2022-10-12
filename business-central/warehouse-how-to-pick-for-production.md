---
title: Tínsla fyrir framleiðslu, samsetningu eða vinnslur í Grunnvöruhúsi
description: Þegar vöruhúsið krefst þess að hægt sé að vinna tínslur en ekki afhendingar er síðan nota Birgðatínslusíðuna til að skrá þá íhluti sem voru teknir til.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617877"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Tínsla fyrir framleiðslu, samsetningu eða vinnslur í Grunnvöruvöruhúsi

Hátturinn við frágang tínsluíhluta fyrir framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Tína fyrir framleiðslu með einföldum vörhúsagrunnstillingum

Ef Birgðageymsla krefst tínsluvinnslu en ekki afhendingarvinnslu er hægt að **nota síðuna Birgðatínsla**. Á **síðunni Birgðatínsla** er hægt að skipuleggja tiltekt og skráningu vara sem hafa birgðaskráningaraðferðina stillta á **handvirkt**. Þegar Birgðatínsla er skráð er notkun Tíndu íhlutanna bókuð. Einnig er hægt að nota **birgðahreyfingar** með tilvísun í upprunaskjal til að úthluta íhlutum með Birgðaskráningaraðferð stillt á **handvirkt**, **Velja + áfram**, **taka + afturábak** í framleiðslupöntunum.

Ef framleiðsla er samþætt við vöruhúsaferli í gegnum hólf eða beinan frágang og tínslu eru íhlutir notaðar úr hólfinu á framleiðslupöntunarlínunni. Allar íhlutir sem þörf er á verða að vera tiltækir í því hólfi. Að öðrum kosti er hætt við að Handvirk eða notkun bókunar sé stöðvuð fyrir þann íhlut.

> [!NOTE]  
> Eftirfarandi er mikilvægur munur á birgðatínslu, birgðahreyfingum og vöruhúsatínum:  
>
> - Þegar birgðatínsla er skráð fyrir innri aðgerð, s.s. framleiðslu, er notkun fyrir tínda hluti bókuð samhliða. Þegar birgðahreyfing er skráð fyrir innri aðgerð eða vöruhúsatínslu þarf aðeins að skrá raunverulegan flutning nauðsynlegs íhlutar að hólfi í rekstrarsvæðinu án þess að bóka notkun.  
> - Þegar birgðatínsla er notuð skilgreinir reiturinn **Hólfkóti** á íhlutalínu framleiðslupöntunar hólfið *taka* hvaðan íhlutir eru minnkaðir þegar notkun er bókuð. Þegar birgðahreyfingar eru notaðar í vöruhúsatínslu skilgreinir reiturinn **Hólfkóti** í framleiðslupöntunaríhlutalínum hólfið *setja* í aðgerðasvæðinu þar sem starfsmaður í vöruhúsi verður setja íhlutina.  

Til að taka til eða færa íhluti fyrir upprunaskjöl verður beiðni á útleið í vöruhúsi að tilkynna vöruhúsasvæðið þörfina fyrir íhlutinn. Vöruhúsabeiðni á útleið er stofnuð þegar gert er við eftirfarandi:

- Breyta stöðu framleiðslupöntunar í Útgefin.
- Stofnið útgefna framleiðslupöntun.  

Flúorskolun hefur einnig áhrif á flæði íhluta í framleiðslu. Nánari upplýsingar eru í [Birgðaskrá íhluti samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md). **Ekki er hægt að nota birgðahreyfingar** með tilvísunum í upprunaskjal og **vöruhúsatiltekt** til að velja íhluti með *fram* -og *afturkræflunaraðferðum*. **Ekki er hægt að nota birgðatínslu** til að velja íhluti með Birgðaskráningaraðferð en *handvirkt*. Til að sjá um eftirstandandi íhluti skal nota **Birgðahreyfingu** án tilvísana í upprunaskjal. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Í ítarlegri vöruhúsagrunnstillingu þar sem staðsetningar þarfnast bæði tínslu og afhendingar þarf að nota síðuna **Vöruhúsatínsla** til að færa íhluti með losunaraðferð stillta á *Handvirkt*, *Tína + framvirkt*, *Tína + afturvirkt* yfir í framleiðslupantanir. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Íhlutir tínsluhlutar til framleiðslu og vinnslu í grunnvöruafbrigðum

Í grunnvöruhúsaleiðunum þar sem birgðageymslan er sett upp þannig að hún noti tiltekt, er hægt að velja íhluti fyrir framleiðsluverkþætti og vinnsluráætlanalínur á **síðunni Birgðatínsla**. Frekari upplýsingar, sjá [Tína vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> Getu til að velja íhluti fyrir vinnsluráætlanalínur var bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)] í 2022 út bylgju 2. Ef byrja á að nota getu verður kerfisstjóri að **gera aðgerðina uppfæra: Virkja birgða-og vöruhúsatiltekt frá vinnslum** á **síðunni Feature Management**.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] notar gildið í **reitnum Eftirstöðvar** í verkáætlunarlínunni þegar Birgðatínslur eru stofnaðar. Ef nota á Birgðatínslur fyrir vinnslur verður að kveikja á reitnum **nota Notkunartengil** á **síðunni vinnsluspjald** fyrir vinnsluna. Þetta gerir þér kleift að rekja notkun þína gegn áætlun þinni. Ef ekki er kveikt á skiptiverði er eftirstandandi magn haldið á **0** og Birgðatínsla verður ekki stofnuð. Frekari upplýsingar er að finna [í til að setja upp verknotkunina](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
2. Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
3. Velja íhlutinn og skrá síðan tiltektarupplýsingar í **reitinn Magn til afgreiðslu**.  
4. Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókunin stofnar nauðsynlegar vöruhúsafærslur og bókar notkun varanna.  

Einnig er hægt að stofna **Birgðatínslu** beint úr útgefnu framleiðslupöntuninni. Veljið aðgerðina **Stofna birgðafrágang/-tínslu/-hreyfingu**, veljið gátreitinn **Stofna birgðatínslu** og smellið síðan á hnappinn **Í lagi**.

Auk þess er notuð **birgðahreyfing** með tilvísun í upprunaskjalið til að flytja vörur milli hólfa. Þú þarft að skrá neyslu sérstaklega. Frekari upplýsingar er að finna í [Fjöldabóka framleiðslunotkun](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Tiltekt fyrir samsetningu í grunnstillingum vöruhúss

Notið eftirfarandi síður til að velja fyrir samsetningarpantanir:

- **Síða birgðahreyfingar**.
- Ef birgðageymslan krefst tínslu en ekki afhendingar skal nota **síðuna Birgðatínsla** til að taka saman og senda sölupantanir þar sem vörur verða settar saman áður en hægt er að senda þær. Nánari upplýsingar eru í [Meðhöndlun á vörum samsetningarpöntunar með birgðatínslum](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Í ítarlegri vöruhúsagrunnstillingu þar sem staðsetningar þarfnast bæði tínslu og afhendingar þarf að nota síðuna **Vöruhúsatínsla** til að færa íhluti til samsetningarpantana. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Meðhöndlun setja saman í pöntun íhluta við birgðatínslu

Síðan **Birgðatínsla** er einnig notaður til að tína og senda vegna sölu þar sem vörur verða að vera samsettar áður en hægt er að senda þær. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).

Setja saman vörur til að senda eru ekki taldar til staðar í hólfi fyrr en þær eru settar saman og bókaðar sem Output í hólf í samkomusvæðinu. Því skal velja þessi atriði fyrir sendingu sem fylgir sérstöku áklæði. Starfsmenn í vöruhúsi færa samsetningaríhluti úr hólfi á afhendingarsvæði og bóka síðan birgðatínsluna. Bókaða birgðatínslan bókar svo samsetningarfrálagið, íhlutanotkunina og söluafhendinguna.

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] í búa til birgðahreyfingu sjálfkrafa þegar birgðatínsla fyrir samsetningarvöru er stofnuð. Til að stofna hreyfingar sjálfkrafa skal velja **svæðið Stofna hreyfingar sjálfkrafa** á **síðu samsetningaruppsetningar**. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

[!INCLUDE[prod_short](includes/prod_short.md)] stofnar birgðatínslulínur fyrir söluvörur á annan hátt, allt eftir því hvort ekkert, eða allt magn sölulínanna er sett saman við pöntun.

- Í sölu þar sem Birgðatínsla er notuð til að bóka birgðalokun, [!INCLUDE[prod_short](includes/prod_short.md)] stofnar eina birgðatínslínu fyrir hverja sölupöntunarlínu. Ef varan er sett í önnur hólf verður til fleiri en ein lína. Tínslulínurnar eru byggðar á magninu í **reitnum Magn til sendingar**.
- Í sölu þar sem heildarmagnið á sölupöntunarlínunni er sett saman til pöntunar er ein birgðatínalína stofnuð fyrir magnið. Gildið í reitnum Magn til að setja saman við er það sama og gildið í **svæðinu Magn til sendingar**. **Setja saman í pöntun** reiturinn er valið í línunni.

Ef frálagsflæði samsetningar er sett upp fyrir birgðageymsluna er gildið í **reitunum asam.-to-Pöntunarhólfsh** eða **frá-samsetningarkóti** í þeirri pöntun sett inn í **reitinn hólfskóti** í birgðatínslulínunni.

Ef enginn hólfskóði er gefinn upp í sölupöntunarlínunni og samsetningarfrálagsflæði hefur ekki verið sett upp fyrir birgðageymsluna er reiturinn **Hólfakóði** í birgðatínslulínunni er auður. Starfsmaður í vöruhúsi verður að opna síðuna **Hólfainnihald** og velja hólfið þar sem samsetningarvörurnar eru settar saman.

Þegar hluti af magninu verður að vera settur saman fyrst og annað verður að taka til úr birgðum eru [!INCLUDE[prod_short](includes/prod_short.md)] stofnaðar að minnsta kosti tvær birgðatínslulínur. Ein tínslulína er fyrir sameiningarpöntunarmagnið. Hin tínslulínan fer eftir hvaða hólf geta uppfyllt eftirstöðvar úr birgðum. Hólfkóti á línunum tveimur er fylltur út er á mismunandi hátt eins og lýst er fyrir þessar tvær mismunandi sölutegundir. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Fylla út notkunarhólfið

Þetta flæðirit sýnir hvernig reiturinn **Hólfkóði** í framleiðslupöntunaríhlutalínum er útfylltur samkvæmt uppsetningu staðsetningar.

![Flæðirit hólfs.](media/binflow.png "BinFlow")

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
