---
title: Sameina stöður fyrir fyrirtæki sem er viðskiptamaður og lánardrottinn
description: Lýsir því hvernig á að sameina stöður fyrir viðskiptamann sem er einnig lánardrottinn.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="consolidate-balances-for-a-company-that-is-a-customer-and-a-vendor"></a>Sameina stöður fyrir fyrirtæki sem er viðskiptamaður og lánardrottinn
Fyrirtæki sem þú átt í viðskiptum við gæti verið bæði viðskiptamaður og lánardrottinn. Þegar svo er geturðu forðast að framkvæma ónauðsynlegar greiðslur eða móttökur og hugsanlega sparað í færslugjöldum með því að sameina stöður viðskiptamanns og lánardrottins í fyrirtækinu. Sameining ber saman stöður fyrirtækisins sem lánardrottinn og sem viðskiptamaður og finnur síðan nettóupphæðina þannig að annaðhvort stendur eftir staða viðskiptamanns eða lánardrottins eftir því hvor upphæðin er hærri. 

Til að sameina stöðurnar þarf fyrst að tengja fyrirtæki viðskiptamanns og lánardrottins í gegnum tengilið sem er af gerðinni **Fyrirtæki**. Viðskiptamaður og lánardrottinn geta aðeins verið með einn tengilið af gerðinni **Fyrirtæki**. Frekari upplýsingar eru í [Stofna tengiliði](marketing-create-contact-companies.md).

Eftir að þú hefur tengt fyrirtækin býður síðan **Viðskiptamannaspjald** upp á reitinn **Staða sem lánardrottinn** og síðan **Lánardrottnaspjald** inniheldur reitinn **Staða sem viðskiptamaður**.

Þótt það sé ekki skilyrði eru fyrirtæki viðskiptamanns og lánardrottins yfirleitt sami lögaðilinn. 

## <a name="before-you-start"></a>Verður að byrja fyrir
Áður en þú sameinar stöður skal tilgreina nokkrar stillingar á síðunni **Uppsetning markaðssetningar**. 

* Í flýtiflipanum **Samskipti** þarf að tilgreina kóða viðskiptatengsla í reitunum **Viðskiptamenn** og **Lánardrottnar**. [!INCLUDE[prod_short](includes/prod_short.md)] notar þessar upplýsingar til að ákvarða tegund tengsla sem á að sýna fyrir tengiliði. 
* Valfrjálst: Kveiktu eða slökktu á tvítekinni leit í flýtiflipanum **Tvítekningar**. Kveikt er sjálfgefið á tvítekinni leit. Frekari upplýsingar eru í [Meðhöndlun tvítekninga](#handling-duplicates). 

## <a name="link-an-existing-customer-and-vendor-company-through-a-contact"></a>Tengja fyrirliggjandi fyrirtæki viðskiptamanns og lánardrottins í gegnum tengilið
Eftirfarandi skref lýsa því hvernig á að tengja saman viðskiptamann og lánardrottinn í gegnum tengilið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinur** eða **Lánardrottinn** og velja síðan viðkomandi tengil.
2. Veldu viðskiptamann eða lánardrottinn og veldu síðan aðgerðina **Tengiliður**.
3. Ef reiturinn **Viðskiptatengsl tengiliðar** inniheldur gildi annað en **Engin** þarf að fjarlægja tengslin. Til að gera það skal nota aðgerðina **Viðskiptatengsl** og síðan eyða tengslunum. 
4. Eftir því hvort þú valdir **Viðskiptamann** eða **Lánardrottinn** í skrefi 1 velurðu ![Ljósaperuna sem opnar eiginleika viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið og færir síðan inn gagnstæðan aðila. Það er að segja ef þú valdir **Lánardrottinn** ættir þú að leita að **Viðskiptamanni**.
5. Veldu lánardrottinn eða viðskiptamann og veldu síðan aðgerðina **Tengiliðir**.
6. Veldu aðgerðina **Tengja við fyrirliggjandi** og síðan valkostinn **Viðskiptamaður** eða **Lánardrottinn**.
7. Veldu viðskiptamann eða lánardrottinn.

## <a name="create-a-vendor-from-a-customer-or-vice-versa"></a>Stofnaðu lánardrottinn úr viðskiptamanni eða öfugt
Hægt er að stofna nýjan lánardrottinn úr fyrirliggjandi viðskiptamanni eða nýjan viðskiptamann úr lánardrottni. Á síðunum **Viðskiptamaður** eða **Lánardrottinn** skal opna síðuna **Tengiliður**. Veldu aðgerðina **Stofna sem** og síðan annaðhvort valkostinn **Viðskiptamaður** eða **Lánardrottinn**. 

## <a name="create-a-new-customer-or-vendor-and-link-them-through-a-vendor-or-customer-contact"></a>Stofna nýjan viðskiptamann eða lánardrottin og tengja þá í gegnum tengilið lánardrottins eða viðskiptamanns
1. Stofna nýjan viðskiptavin eða lánardrottinn. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md) eða [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).
2. Þegar viðskiptamaður eða lánardrottinn hefur verið settur upp skal velja aðgerðina **Stofna** og síðan velja annaðhvort valkostinn **Viðskiptamaður** eða **Lánardrottinn**. 

## <a name="to-consolidate-the-customer-and-vendor-balances-for-a-contact-company"></a>Að sameina stöður viðskiptamanns og lánardrottins fyrir fyrirtæki tengiliðar
Á síðunni **Greiðslubók** skal nota aðgerðina **Nettóstöður viðskiptamanns/lánardrottins** til að sameina stöður viðskiptamanns og lánardrottins í eina nettóupphæð. Aðgerðin býr til, en bókar ekki, greiðslubókarlínur sem innihalda nettóstöðurnar.

> [!NOTE]
> Ef stöður viðskiptamanns eða lánardrottins innihalda upphæðir sem eru í öðrum gjaldmiðlum er lína stofnuð fyrir upphæðina í hverju gjaldmiðli.

## <a name="handling-duplicates"></a>Meðhöndlun tvítekninga
Ef þú kveikir á tvítekinni leit í flýtiflipanum **Tvítekningar** á síðunni **Uppsetning markaðssetningar** mun viðvörun birtast þegar þú breytir gildum reita sem eru hluti af uppsetningunni fyrir tvítekna leitarstrengi. Þegar tvítekning finnst er hægt að grípa til eftirfarandi aðgerða:

* Sameinaðu tvítekna tengiliði í einn tengilið sem er sá sami fyrir bæði viðskiptamann og lánardrottin með því að nota möguleikann **Sameina við** á síðunni **Tengiliðaspjald**. Yfirleitt er sameining tengiliða eingöngu gerð þegar viðskiptamaður og lánardrottinn eru sami lögaðilinn. Frekari upplýsingar er að finna í [Sameina tvítekin atriði](sales-how-merge-duplicate-records.md). 
* Eyddu viðskiptatengslum lánardrottins fyrir tengilið lánardrottins eða viðskiptamanns og notaðu síðan aðgerðina **Tengja við fyrirliggjandi** til að tengja við annan tengilið.    

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
