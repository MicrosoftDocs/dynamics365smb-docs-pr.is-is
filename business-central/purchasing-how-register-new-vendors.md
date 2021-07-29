---
title: Stofna lánardrottnaspjald til að skrá nýjan lánardrottinn
description: Þetta efnisatriði kynnir hvernig skal stofna lánadrottnaspjald til að skrá nýjan lánardrottin eða birgja og vista lánardrottnaspjöld sem sniðmát.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 2d4943415af6f5cd91ac35c68a9d8433e024b6be
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445377"
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

Til að skrá nýjan lánardrottinn þarf að fylla út lánardrottnaspjald. Hægt er að búa til sniðmát fyrir mismunandi forstillingar lánardrottna eða hægt er að bæta við lánardrottnum án sniðmáta. Einnig er hægt að stofna lánardrottinn úr sniðmáti. Frekari upplýsingar eru í [Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Ef lánardrottnasniðmát er til fyrir mismunandi tegundir lánardrottna, þá birtist síða þegar búið er til nýtt lánardrottnaspjald þar sem hægt er að velja viðeigandi sniðmát. Ef aðeins eitt lánardrottnasniðmát er fyrir hendi, nota ný lánardrottnaspjöld alltaf það sniðmát.  

### <a name="to-create-a-new-vendor-card"></a>Að búa til nýtt lánardrottnaspjald.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.  
2. Á síðunni **Lánardrottnar** skal velja **Nýtt**.

    Ef fleiri en eitt lánardrottnasniðmát er fyrir hendi, þá birtist sjálfkrafa síða með tiltækum lánardrottnasniðmátum. Í því tilviki, fylgið næstu tveimur skrefum.
    1. Á síðunni **Velja sniðmát fyrir nýjan lánardrottin** er valið sniðmátið sem á að nota fyrir nýja lánardrottnaspjaldið.
    2. Velja hnappinn **Í lagi**. Nýtt lánardrottnaspjald opnast þar sem búið er að fylla upplýsingar úr sniðmátinu inn í hluta reitanna.
3. Því næst eru reitir á lánardrottnaspjaldinu færðir inn eða þeim breytt eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > Ef ekki er vitað reikningsaðsetur sem verður notað fyrir hvern reikning frá lánardrottni skal ekki færa í reitinn **Númer lánardrottins**. Þess í stað skal velja borga-lánardrottni númer eftir að hafa sett upp innkaupabeiðni, pöntun eða reikningshaus.

Nú hefur lánardrottinn verið skráður og lánardrottnaspjaldið má nú nota í innkaupaskjölum.

Ef nota á þetta lánardrottnaspjald sem sniðmát þegar ný lánardrottnaspjöld eru búin til, vistið það sem lánardrottnasniðmát. Frekari upplýsingar eru í hlutanum [Að vista lánardrottnaspjaldið sem sniðmát](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-vendor-cards"></a>Eyðir lánardrottnaspjöldum

Ef þú hefur bókað færslu fyrir lánardrottinn er ekki hægt að eyða spjaldinu þar sem hugsanlega þarf að nota fjárhagsfærslurnar í endurskoðun. Til að eyða lánardrottnaspjöldum með fjárhagsfærslum skal hafa samband við samstarfsaðila Microsoft til að gera það með kóða.

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