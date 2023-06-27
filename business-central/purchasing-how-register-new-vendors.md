---
title: Stofna lánardrottnaspjald til að skrá nýjan lánardrottinn (inniheldur myndskeið)
description: Sýnir hvernig skal stofna lánadrottnaspjald til að skrá nýjan lánardrottin eða birgja og vista lánardrottnaspjöld sem sniðmát.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: '26, 27, 34, 461, 786, 1379, 1385, 1386, 1628'
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="register-new-vendors"></a>Skráning nýrra lánardrottna

Lánardrottnar útvega vörurnar sem þú selur. Hver lánardrottinn sem keypt er frá verður að vera skráður með lánardrottnaspjaldi.

Áður en hægt er að skrá nýja lánardrottna þarf að setja upp ýmsa innkaupakóða til að velja úr þegar lánardrottnaspjöl eru fyllt út. Eftir að öll nauðsynleg aðalgögn eru búin til er hægt að bæta við einkvæmum eiginleikum fyrir lánardrottin, t.d. forgagnsraða lánardrottni vegna greiðslna eða birta vörur sem lánardrottinn og aðrir lánardrottnar útvega. Annar flokkur uppsetningarverkhluta fyrir lánardrottna er að skrá samninga varðandi afslætti, verð og greiðsluaðferðir. Frekari upplýsingar er að finna í [Uppsetning innkaupa](purchasing-setup-purchasing.md).

Lánardrottnaspjöld geyma upplýsingarnar sem þarf til að kaupa vörur frá hverjum lánardrottni. Frekari upplýsingar er að finna í [Skrá innkaup](purchasing-how-record-purchases.md) og [Skrá nýjar vörur](inventory-how-register-new-items.md).
<br /><br />  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Nýjum lánardrottnum bætt við

Hægt er að bæta við nýjum lánardrottnum handvirkt með því að fylla út síðuna **Lánardrottnaspjald** eða hægt er að nota sniðmát sem innihalda fyrirframskilgreindar upplýsingar. Til dæmis er hægt að stofna sniðmát fyrir mismunandi forstillingargerðir lánardrottna. Með því að nota sniðmát sparast tími þegar nýjum lánardrottnum er bætt við og það hjálpar til við að tryggja að upplýsingarnar séu réttar hverju sinni.

> [!NOTE]  
> Ef til er sniðmát fyrir mismunandi tegundir lánardrottna, þegar byrjað er að búa til nýtt lánardrottnaspjald, sérðu síðu þar sem hægt er að velja viðeigandi sniðmát. Ef aðeins eitt lánardrottnasniðmát er fyrir hendi, nota ný lánardrottnaspjöld alltaf það sniðmát.

Þegar sniðmát er stofnað geturðu notað aðgerðina **Nota sniðmát** til að nota það í einum eða fleiri lánardrottnum. Til að búa til sniðmát skal fylla inn upplýsingarnar sem þú vilt endurnota á síðunni **Lánardrottnaspjald**, síðan vista hana sem sniðmát. Frekari upplýsingar eru í hlutanum [Að vista lánardrottnaspjaldið sem sniðmát](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Það getur reynst gagnlegt að sérsníða síðuna **Sniðmát lánardrottins** þegar þú stofnar sniðmát. Þú gætir til dæmis viljað bæta reit sem er ekki sýndur við síðuna. Frekari upplýsingar er að finna í hlutanum [Sérsníða vinnusvæðið](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Einnig er hægt að stofna lánardrottinn úr sniðmáti. Frekari upplýsingar eru í hlutanum [Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

Greiðsluaðsetur eru notuð þegar prentaðar eru út ávísanir til að greiða lánardrottnum og lánardrottnar geta verið með mörg greiðsluaðsetur fyrir greiðslur. Til dæmis gæti lánardrottinn útvegað vöru úr dótturfyrirtæki en vill taka á móti greiðslu í höfuðstöðvum. [!INCLUDE [prod_short](includes/prod_short.md)] gerir þér kleift að setja upp mörg póstföng fyrir hvernig lánardrottin og hægt er að nota rétta staðsetningu til að senda greiðslur til, einn reikning í einu.

Þú tilgreinir greiðsluaðsetur á lánardrottnaspjöldin og í flýtiflipanum „Afhendingar og greiðslur“ í innkaupapöntunum og reikningum. Þegar greiðslubókarlínur eru stofnaðar með aðgerðunum „Greiða lánardrottni“ eða „Stofna greiðslu“ á síðu lánardrottnalista eða síðu lánardrottnaspjalds, eða aðgerðinni „Jafna færslur“ í greiðslubók, er greiðslukóðanum í lánardrottnafærslum úthlutað. Hægt er að skrifa yfir þetta gildi.

### <a name="to-create-a-new-vendor"></a>Að búa til nýjan lánardrottinn

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Ef ekki er vitað reikningsaðsetur sem verður notað fyrir hvern reikning frá lánardrottni skal ekki fylla út **Nr.**.  á flýtiflipanum **Almennt**. Þess í stað skal velja borga-lánardrottni númer eftir að hafa sett upp innkaupabeiðni, pöntun eða reikningshaus.

Nú hefur lánardrottinn verið skráður og lánardrottnaspjaldið má nú nota í innkaupaskjölum.

Ef nota á þetta lánardrottnaspjald sem sniðmát þegar ný lánardrottnaspjöld eru búin til, vistið það sem lánardrottnasniðmát. Frekari upplýsingar eru í hlutanum [Að vista lánardrottnaspjaldið sem sniðmát](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Að eyða og breyta lánardrottnaupplýsingum

Hægt er að breyta upplýsingunum á lánardrottnaspjöldum hvenær sem er. Ef þú hefur aftur á móti bókað færslu fyrir lánardrottinn er ekki hægt að eyða spjaldinu þar sem hugsanlega þarf að nota fjárhagsfærslurnar í endurskoðun. Til að eyða lánardrottnaspjöldum með fjárhagsfærslum skal hafa samband við samstarfsaðila Microsoft til að gera það með kóða.

> [!TIP]
> Þú getur breytt IBAN-númerinu (alþjóðlegt bankareikningsnúmer) á bankareikningi lánardrottins án þess að breytingin hafi áhrif á sögulegar skráningarfærslur kreditfærslu. Skráningarfærslur kreditfærslu geyma *IBAN viðtakanda* og *Bankareikningsnúmer viðtakanda* sem tilgreint er í reitunum **Bankareikningur lánardrottins** og **Nafn viðtakanda** af síðunni **Lánardrottnaspjald** þegar færslur eru stofnaðar.

> [!TIP]
> Hægt er að bæta við öðrum aðsetrum á lánardrottnaspjöldin með því að velja aðgerðina **Pöntunaraðsetur**.

## <a name="to-save-the-vendor-card-as-a-template"></a>Að vista lánardrottnaspjaldið sem sniðmát

1. Á síðunni **Lánardrottnaspjald** er valin aðgerðin **Vista sem sniðmát**. Síðan **Lánardrottnasniðmát** opnast og sýnir lánardrottnaspjaldið sem sniðmát.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að endurnota víddir í sniðmátum, veljið aðgerðina **Víddir**. Síðan **Víddarsniðmát** opnast og sýnir alla víddarkóða sem settir eru upp fyrir lánardrottin.
4. Breyttu eða færðu inn víddarkóða sem gilda fyrir ný lánardrottnaspjöld sem stofnuð eru með sniðmátinu.
5. Þegar lokið hefur verið við nýja lánardrottinssniðmátið skal velja **Í lagi**.  
   Lánardrottnasniðmátinu verður bætt við lista lánardrottnasniðmáta þannig að hægt er að nota það til að búa til ný lánardrottnaspjöld.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/trade-master-data-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Sameina tvítekin atriði](sales-how-merge-duplicate-records.md)  
[Stofnun númeraraða](ui-create-number-series.md)  
[Setja upp lánardrottnabankareikninga](purchasing-how-set-up-vendors-bank-accounts.md)  
[Setja upp kaupendur](purchasing-how-setup-purchasers.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Nota kortaþjónustu til að finna staðsetningar og leiðsagnir](across-online-maps.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
