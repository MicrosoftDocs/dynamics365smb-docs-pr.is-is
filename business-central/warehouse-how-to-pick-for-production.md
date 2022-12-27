---
title: Tínsla fyrir framleiðslu, samsetningu eða verk í einföldu vöruhúsi
description: Þegar vöruhúsið þitt krefst þess að þú vinnir úr tínslum en ekki sendum skaltu nota birgðatínslusíðuna til að skrá að íhlutir hafi verið tíndir.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617877"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Tínsla fyrir framleiðslu, samsetningu eða verk í einfaldri vöruhúsagrunnstillingu

Hátturinn við frágang tínsluíhluta fyrir framleiðslu fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Tína fyrir framleiðslu með einföldum vörhúsagrunnstillingum

Ef staðsetning krefst tínsluvinnslu en ekki úrvinnslu sendingar geturðu notað síðuna **Birgðatínsla**. Síðan **Birgðatínsla** gerir þér kleift að skipuleggja og skrá tínslu á vörum sem er með birgðaskráningaaðferðina stillta á **Handvirkt**. Þegar þú skráir birgðatínslu er notkun tíndra íhluta bókuð. Einnig er hægt að nota **Birgðahreyfingar** með tilvísun í upprunaskjal til að úthluta íhlutum með birgðaskráningaaðferð stillta á **Handvirkt**, **Tína + framvirkt**, **Tína + afturvirkt** yfir í framleiðslupantanir.

Ef framleiðsla er samþætt við vöruhúsaferli í gegnum hólf eða beinan frágang og tínslur eru íhlutir notaðir úr hólfinu í framleiðslupöntunarlínunni. Allar íhlutir sem þörf er á verða að vera tiltækir í því hólfi. Annars er handvirk eða sjálfvirk notkunarbókun stöðvuð fyrir íhlutinn.

> [!NOTE]  
> Eftirfarandi er mikilvægur munur milli birgðatínslu, birgðahreyfingu og vöruhúsatínslu:  
>
> - Þegar birgðatínsla er skráð fyrir innri aðgerð, s.s. framleiðslu, er notkun fyrir tínda hluti bókuð samhliða. Þegar birgðahreyfing er skráð fyrir innri aðgerð eða vöruhúsatínslu þarf aðeins að skrá raunverulegan flutning nauðsynlegs íhlutar að hólfi í rekstrarsvæðinu án þess að bóka notkun.  
> - Þegar birgðatínsla er notuð skilgreinir reiturinn **Hólfkóti** á íhlutalínu framleiðslupöntunar hólfið *taka* hvaðan íhlutir eru minnkaðir þegar notkun er bókuð. Þegar birgðahreyfingar eru notaðar í vöruhúsatínslu skilgreinir reiturinn **Hólfkóti** í framleiðslupöntunaríhlutalínum hólfið *setja* í aðgerðasvæðinu þar sem starfsmaður í vöruhúsi verður setja íhlutina.  

Til að tína eða færa íhúti fyrir upprunaskjöl þarf vöruhúsabeiðni á útleið að tilkynna vöruhúsasvæði um þörfina á íhlutnum. Vöruhúsabeiðni á útleið er búin til þegar þú gerir eftirfarandi:

- Breyttu stöðu framleiðslupöntunar í útgefna.
- Stofna útgefna afurð.  

Losunaraðferðir hafa einnig áhrif á flæði íhluta í framleiðslu. Nánari upplýsingar eru í [Birgðaskrá íhluti samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md). **Birgðahreyfing** með tilvísanir í upprunaskjalið og **Vöruhúsatínslu** er ekki hægt að nota til að tína íhluti með birgðaskráningaaðferðunum *Framvirkt* og *Afturvirkt*. Ekki er hægt að nota **Birgðatínsla** til að tína íhluti með neinni losunaraðferð nema *Handvirkt*. Til að sjá um eftirstandandi íhluti skal nota **Birgðahreyfingu** án tilvísana í upprunaskjal. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Í ítarlegri vöruhúsagrunnstillingu þar sem staðsetningar þarfnast bæði tínslu og afhendingar þarf að nota síðuna **Vöruhúsatínsla** til að færa íhluti með losunaraðferð stillta á *Handvirkt*, *Tína + framvirkt*, *Tína + afturvirkt* yfir í framleiðslupantanir. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Að tína íhluti fyrir framleiðslu og verk í einfaldri vöruhúsagrunnstillingu

Í einfaldri vöruhúsagrunnstillingu þar sem staðsetningin er sett upp til að nota eingöngu tínslu, eru íhlutir tíndir fyrir framleiðsluaðgerðir og verkáætlunarlínur á síðunni **Birgðatínsla**. Frekari upplýsingar, sjá [Tína vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> Getan til að tína íhluti fyrir veráætlunarlínur var bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)] í 2022 útgáfutímabili 2. Til að byrja að nota möguleikann verður stjórnandi að kveikja á **Eiginleikastjórnun: Virkja birgða- og vöruhúsatínslu úr verkum** á síðunni **Eiginleikastjórnun**.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] notar gildið í reitnum **Eftirstöðvar** á verkáætlunarlínunni þegar það býr til birgðatínslur. Til að nota birgðatínslur fyrir verk þarftu að kveikja á **Nota notkunartengil** á síðunni **Verkspjald** fyrir verkið. Þetta gerir þér kleift að fylgjast með notkun miðað við áætlun þína. Ef þú kveikir ekki á víxlhnappnum verða eftirstöðvarnar í **0** og birgðatínslan verður ekki búin til. Nánari upplýsingar eru í [Til að setja upp notkunarrakningu verka](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
2. Til að komast í íhluti framleiðslupöntunarinnar, veldu aðgerðina **Sækja upprunaskjöl** og síðan er útgefna framleiðslupöntunin valin.  
3. Veldu íhlutinn og skráðu svo tínsluupplýsingarnar í reitinn **Magn til afgreiðslu**.  
4. Þegar línurnar eru tilbúnar til bókunar er smellt á aðgerðina **Bóka**. Bókunin stofnar nauðsynlegar vöruhúsafærslur og bókar notkun varanna.  

Einnig er hægt að stofna **Birgðatínslu** beint úr útgefnu framleiðslupöntuninni. Veljið aðgerðina **Stofna birgðafrágang/-tínslu/-hreyfingu**, veljið gátreitinn **Stofna birgðatínslu** og smellið síðan á hnappinn **Í lagi**.

Annars er hægt að nota **Birgðahreyfingu** með tilvísun í upprunaskjalið til að færa vörur á milli hólfa. Notkun þarf að skrá notkun sér. Frekari upplýsingar er að finna í [Fjöldabóka framleiðslunotkun](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Tiltekt fyrir samsetningu í grunnstillingum vöruhúss

Notaðu eftirfarandi síður til að velja fyrir samsetningarpantanir:

- **Birgðahreyfing** síðan.
- Ef staðsetningin krefst tínslu en ekki sendingar skal nota síðuna **Birgðatínsla** til að tína, taka saman og senda fyrir sölupantanir þar sem vörur verða að vera settar saman áður en hægt er að senda þær. Nánari upplýsingar eru í [Meðhöndlun á vörum samsetningarpöntunar með birgðatínslum](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Í ítarlegri vöruhúsagrunnstillingu þar sem staðsetningar þarfnast bæði tínslu og afhendingar þarf að nota síðuna **Vöruhúsatínsla** til að færa íhluti til samsetningarpantana. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Meðhöndlun setja saman í pöntun íhluta við birgðatínslu

Síðan **Birgðatínsla** er einnig notaður til að tína og senda vegna sölu þar sem vörur verða að vera samsettar áður en hægt er að senda þær. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).

Vörur sem á að senda í samsetningarpöntun eru ekki taldar til staðar í hólfi fyrr en þær eru teknar saman og bókaðar sem úttak í hólf á samsetningarsvæðinu. Tínsla á þessum vörum fyrir sendingu fylgir þar af leiðandi sérstöku flæði. Starfsmenn í vöruhúsi færa samsetningaríhluti úr hólfi á afhendingarsvæði og bóka síðan birgðatínsluna. Bókaða birgðatínslan bókar svo samsetningarfrálagið, íhlutanotkunina og söluafhendinguna.

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] í búa til birgðahreyfingu sjálfkrafa þegar birgðatínsla fyrir samsetningarvöru er stofnuð. Til að búa til hreyfingar sjálfkrafa skal velja reitinn **Stofna hreyfingar sjálfkrafa** á síðunni **Uppsetning samsetningar**. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

[!INCLUDE[prod_short](includes/prod_short.md)] stofnar birgðatínslulínur fyrir söluvörur á mismunandi hátt eftir því hvort ekkert, sumt eða allt magn sölulínu er safnað í pöntun.

- Í sölu þar sem þú notar birgðatínslu til að bóka birgðasendingu stofnar [!INCLUDE[prod_short](includes/prod_short.md)] eina birgðatínslulínu fyrir hverja sölupöntunarlínu. Ef varan er sett í mismunandi hólf verða fleiri en ein lína búnar til. Tínslulínurnar byggja á magninu í reitnum **Magn til afhendingar**.
- Í sölu þar sem fullt magn í sölupöntunarlínu er samsetningarpöntun er ein birgðatínslulína stofnuð fyrir magnið. Gildið í reitnum Magn til samsetningar er það sama og gildið í reitnum **Magn til afhendingar** . **Setja saman í pöntun** reiturinn er valið í línunni.

Ef samsetningarfrálagsflæði er sett upp fyrir birgðageymsluna er gildið í reitnum **Setja saman í pöntun hólfakóði** eða gildið í reitnum **Frá samsetningu hólfakóði**, í þeirri röð, sett inn í reitinn **Hólfakóði** í birgðatínslulínunni.

Ef enginn hólfskóði er gefinn upp í sölupöntunarlínunni og samsetningarfrálagsflæði hefur ekki verið sett upp fyrir birgðageymsluna er reiturinn **Hólfakóði** í birgðatínslulínunni er auður. Starfsmaður í vöruhúsi verður að opna síðuna **Hólfainnihald** og velja hólfið þar sem samsetningarvörurnar eru settar saman.

Þegar hluti magnsins verður að vera settur saman fyrst og annar verður að vera tíndur úr birgðum, stofnar [!INCLUDE[prod_short](includes/prod_short.md)] að minnsta kosti tvær birgðatínslulínur. Ein tínslulína er fyrir sameiningarpöntunarmagnið. Hin tínslulínan fer eftir hvaða hólf geta uppfyllt eftirstöðvar úr birgðum. Hólfkóti á línunum tveimur er fylltur út er á mismunandi hátt eins og lýst er fyrir þessar tvær mismunandi sölutegundir. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Fylla út notkunarhólfið

Þetta flæðirit sýnir hvernig reiturinn **Hólfkóði** í framleiðslupöntunaríhlutalínum er útfylltur samkvæmt uppsetningu staðsetningar.

![Flæðirit hólfs.](media/binflow.png "BinFlow")

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
