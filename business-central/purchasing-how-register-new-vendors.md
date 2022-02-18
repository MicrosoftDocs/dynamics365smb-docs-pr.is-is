---
title: Stofna spjald lánardrottins til að skrá nýjan lánardrottin (inniheldur Video)
description: Þetta efnisatriði kynnir hvernig skal stofna lánadrottnaspjald til að skrá nýjan lánardrottin eða birgja og vista lánardrottnaspjöld sem sniðmát.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: 26, 27, 34, 461, 786, 1379, 1385, 1386, 1628
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 1cbdf85f08939aa05c013901239bbd390400f3e1
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115503"
---
# <a name="register-new-vendors"></a>Skráning nýrra lánardrottna

Lánardrottnar veita vörurnar sem selja á. Hver lánardrottinn sem keypt er frá verður að vera skráður sem lánardrottnaspjald.

Áður en hægt er að skrá nýja lánardrottna þarf að setja upp ýmsar innkaupakóða sem hægt er að velja úr þegar fyllt eru út lánardrottnaspjöld. Þegar búið er að setja inn öll nauðsynleg höfuðgögn er hægt að grunnstilla lánardrottininn frekar, s.s. að forgangsraða lánardrottninum vegna greiðslna og gera lista yfir vörur sem lánardrottinninn og aðrir lánardrottnar geta útvegað. Annar flokkur uppsetningarverkhluta fyrir lánardrottna er að skrá samninga varðandi afslætti, verð og greiðsluaðferðir. Nánari upplýsingar er að finna í [Uppsetning innkaupa](purchasing-setup-purchasing.md).

Lánardrottnaspjöld geyma upplýsingarnar sem þarf til að kaupa vörur frá lánardrottninum. Frekari upplýsingar eru í [Skrá innkaup](purchasing-how-record-purchases.md) og [Skrá nýja hluti](inventory-how-register-new-items.md).

> [!NOTE]  
> Ef lánardrottnasniðmát er til fyrir mismunandi tegundir lánardrottna, þá birtist síða þegar búið er til nýtt lánardrottnaspjald þar sem hægt er að velja viðeigandi sniðmát. Ef aðeins eitt lánardrottnasniðmát er fyrir hendi, nota ný lánardrottnaspjöld alltaf það sniðmát.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Nýjum lánardrottnum bætt við
Hægt er að bæta við nýjum lánardrottnum handvirkt með því að fylla út reitina á síðunni **Lánardrottnaspjald** eða hægt er að nota sniðmát sem innihalda fyrirframskilgreindar upplýsingar. Til dæmis er hægt að stofna sniðmát fyrir mismunandi forstillingargerðir lánardrottna. Með því að nota sniðmát sparast tími þegar nýjum lánardrottnum er bætt við og það hjálpar til við að tryggja að upplýsingarnar séu réttar hverju sinni. Ef þú stofnar sniðmát fyrir fleiri en eina gerð af lánardrottni geturðu valið sniðmátið sem á að nota þegar þú bætir við lánardrottni. Ef þú býrð aðeins til eitt sniðmát verður það notað fyrir alla nýja lánardrottna. Þegar sniðmát er stofnað geturðu notað aðgerðina **Nota sniðmát** til að nota það í einum eða fleiri lánardrottnum. Til að búa til sniðmát fyllir þú inn upplýsingarnar sem þú vilt endurnota á síðu lánardrottnaspjaldsins og vistar það síðan sem sniðmát. Frekari upplýsingar er að finna í [Að vista lánardrottnaspjaldið sem sniðmát](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Það getur reynst gagnlegt að sérsníða síðuna **Sniðmát lánardrottins** þegar þú stofnar sniðmát. Þú gætir til dæmis viljað bæta reit sem er ekki sýndur við síðuna. Frekari upplýsingar eru í [Sérstilling verksvæðis](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Einnig er hægt að stofna lánardrottinn úr sniðmáti. Frekari upplýsingar eru í [Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>Að búa til nýjan lánardrottinn

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Ef ekki er vitað reikningsaðsetur sem verður notað fyrir hvern reikning frá lánardrottni skal ekki færa í reitinn **Númer lánardrottins**. Þess í stað skal velja borga-lánardrottni númer eftir að hafa sett upp innkaupabeiðni, pöntun eða reikningshaus.

Nú hefur lánardrottinn verið skráður og lánardrottnaspjaldið má nú nota í innkaupaskjölum.

Ef nota á þetta lánardrottnaspjald sem sniðmát þegar ný lánardrottnaspjöld eru búin til, vistið það sem lánardrottnasniðmát. Frekari upplýsingar eru í hlutanum [Að vista lánardrottnaspjaldið sem sniðmát](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Að eyða og breyta lánardrottnaupplýsingum

Hægt er að breyta upplýsingunum á lánardrottnaspjöldum hvenær sem er. Ef þú hefur aftur á móti bókað færslu fyrir lánardrottinn er ekki hægt að eyða spjaldinu þar sem hugsanlega þarf að nota fjárhagsfærslurnar í endurskoðun. Til að eyða lánardrottnaspjöldum með fjárhagsfærslum skal hafa samband við samstarfsaðila Microsoft til að gera það með kóða.

> [!TIP]
> Þú getur breytt IBAN-númerinu á bankareikningi lánardrottins án þess að breytingin hafi áhrif á sögulegar skráningarfærslur kreditfærslu. Skráning kreditfærslu geymir reiti fyrir IBAN-númer viðtakanda, bankareikningsnúmer viðtakanda sem var gefið upp í bankareikningi lánardrottins og nafn viðtakanda af lánardrottnaspjaldinu þegar færslurnar voru stofnaðar.


## <a name="to-save-the-vendor-card-as-a-template"></a>Að vista lánardrottnaspjaldið sem sniðmát

1. Á síðunni **Lánardrottnaspjald** er valin aðgerðin **Vista sem sniðmát**. Síðan **Lánardrottnasniðmát** opnast og sýnir lánardrottnaspjaldið sem sniðmát.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir lánardrottin.
4. Breyta eða færa inn víddarkóða sem munu gilda fyrir ný lánardrottnaspjöld sem stofnuð eru með sniðmátinu.
5. Þegar lokið hefur verið við nýja lánardrottnasniðmátið skal velja hnappinn **Í lagi**.  
   Lánardrottnasniðmátinu verður bætt við lista lánardrottnasniðmáta þannig að hægt er að nota það til að búa til ný lánardrottnaspjöld.

## <a name="see-also"></a>Sjá einnig

[Sameina tvítekin atriði](sales-how-merge-duplicate-records.md)  
[Stofnun númeraraða](ui-create-number-series.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]