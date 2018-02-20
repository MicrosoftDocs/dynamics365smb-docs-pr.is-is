---
title: "Hvernig á að tína vörur fyrir vöruhúsaafhendingu | Microsoft Docs"
description: "Þegar staðsetningin er sett þannig upp að það krefjist vöruhúsatínsluvinnslu og vöruhúsaafhendingarvinnslu eru vöruhúsatínsluskjöl notuð til að stofna og sjá um tínsluupplýsingar fyrir bókun vöruhúsaafhendingar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5b73ac2ca4f1aa3bbb8c6514a8aafa39b3c76f99
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="pick-items-for-warehouse-shipment"></a>Tína vörur fyrir vöruhúsaafhendingu
Þegar staðsetningin er sett þannig upp að það krefjist vöruhúsatínsluvinnslu og vöruhúsaafhendingarvinnslu eru vöruhúsatínsluskjöl notuð til að stofna og sjá um tínsluupplýsingar fyrir bókun vöruhúsaafhendingar.  

Ekki er hægt að stofna vöruhúsatínsluskjal frá grunni þar sem í tínsluaðgerð er alltaf hluti af verkflæði, annað hvort sem dráttur eða ýting.  

Hægt er að útbúa vöruhússtínsluskjöl eins og drátt með því að opna autt vöruhúsaafhendingarfylgiskjal, finna upprunaskjöl sem eru send til afhendingar, og síðan stofna vöruhúsatínslulínur fyrir þær afhendingar. Hægt er að nota aðgerðirnar **Sækja upprunaskjöl** eða **Nota afmörkun til að sækja upprunaskjöl** til að finna upprunaskjöl sem eru tilbúin til afhendingar.

Einnig er hægt að nota gluggann **Vinnublað tínslu** til að draga og stofna tínslulínur í runustillingu. Frekari upplýsingar, sjá [Áætla tínslu á vinnublöðum](warehouse-how-to-plan-picks-in-worksheets.md).  

Einnig er hægt að stofna vöruhúsatínsluskjöl í eins og ýtingu í glugganum **Vöruhúsaafhending** með því að velja **Stofna tínslu**.  

> [!NOTE]  
>  Tínsla fyrir vöruhúsaafhendingu vara sem settar eru saman úr sölupöntuninni sem verið er að afenda fylgir sömu aðferð og hefðbundin vöruhúsatínsla fyrir afhendingu eins og lýst er í þessu efnisatriði. Hins vegar gæti fjöldi tínslulína miðað við afhendingarmagn verið af gerðinni n:1 þar sem íhlutar eru tíndir en ekki samsetningarvaran.  
>   
>  Vöruhúsatínslulínurnar eru stofnaðar fyrir gildið í reitnum **Eftirstöðvar** í línum samsetningarpöntunarinnar sem tengist sölupöntunarlínunni sem verið er að afhenda. Þetta tryggir að allir íhlutir eru tíndir í einni aðgerð.  
>   
>  Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við vöruhúsaafhendingu”   
>   
>  Upplýsingar um almenna tínslu íhluta fyrir samsetningarpantanir, þar á meðal þegar samsetningaríhlutur er ekki hluti af söluafhendingu, eru í [Tína fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md).  

## <a name="to-pick-items-for-warehouse-shipment"></a>Til að tína vörur fyrir vöruhúsaafhendingu  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tínsla** og velja svo viðeigandi tengil.  

    Ef nauðsynlegt er að vinna í tiltekinni tínslu, er tínslan valin af lista eða listi afmarkaður til að vinna tínslu sem hafa verið úthlutað notandanum sérstaklega. Tínsluspjaldið er opnað.  
2.  Ef reiturinn **Úthlutað notandakenni** er auður færir notandinn notandakennið inn til að auðkenna sig, ef þess þarf.  
3.  Framkvæma raunverulega tínslu vara.  

    Ef vöruhúsið er sett upp þannig að það noti hólf verða sjálfgefin hólf notuð fyrir ráðleggingar um hvaðan skuli taka vörur. Leiðbeiningarnar birtast sem tvær aðskildar línur, minnst ein fyrir hvort hvora aðgerð, Taka og Setja.  

    Ef vöruhúsið er sett upp þannig að það noti beinan frágang og tínslu verður hólfaflokkun notuð til að reikna út hvaða hólf er best að tína úr og síðan stungið upp á þeim hólfum í tínslulínum. Leiðbeiningarnar birtast sem tvær aðskildar línur, minnst ein fyrir hvort hvora aðgerð, Taka og Setja.  

4.  Þegar tínslan hefur verið framkvæmd og vörurnar settar á afhendingarsvæði eða í afhendingarhólf er smellt á **Skrá tínslu** aðgerðina.  

Sá sem ábyrgur er fyrir afhendingu getur nú komið vörunum að afhendingarhöfn og bókað afhendinguna, þar á meðal tengt upprunaskjal, í glugganum **Vöruhúsaafhending**. Frekari upplýsingar eru í [Senda vörur](warehouse-how-ship-items.md).   

Til viðbótar við tínslu upprunaskjala eins og lýst er í þessu efnisatriði er hægt að taka og færa vörur á milli hólfa án þess að vísa í upprunaskjöl. Frekari upplýsingar, sjá: [Tína og ganga frá án upprunaskjals](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Meðhöndlun íhluta pantanasamsetninga við vöruhúsaafhendingu
Þegar sameinað er í pöntuð er reiturinn **Magn til afhendingar** í vöruhúsaafhendingarlínum notaður til að skrá hversu magar einingar eru settar saman. Tilgreinda magnið er síðan bókað sem samsetningarfrálag þegar vöruhúsaafhendingin er bókuð.

Fyrir aðrar vöruhúsaafhendingarlínur er gildið í reitnum **Magn til afhendingar** núll í upphafi.

Þegar starfsmenn sem bera ábyrgð á samsetningu ljúka við að setja saman magnið sem setja á saman í pöntun að hluta til eða í heild skrá þeir það í reitinn **Magn til afhendingar** í vöruhúsasendingarlínunn og velja svo **Bóka afhend.** aðgerðina. Niðurstaðan er að samsvarandi samsetningarfrálag er bókað, að meðtalinni notkun íhluta. Söluafhending fyrir magnið er bókuð fyrir sölupöntunina.

Í samsetningarpöntun má velja **Setja saman í p. vöruh. send. lína** til sjá vöruhúsaafhendingarlínuna. Þetta er hentugt fyrir starfsmenn sem nota ekki yfirleitt gluggann **Vöruhúsaafhending**.

Eftir að vöruhúsasendingin er bókuð, eru ýmis svæði í sölupöntunarlínunni uppfærð til að sýna vinnslu í vöruhúsinu. Eftirfarandi svæði eru einnig uppfærð til að sýna hversu mikið magn samsetningarpantana á eftir að setja saman og afhenda:

- **Útistandandi magn ATO vöruhúss**
- **Útistandandi magn ATO vöruhúss (stofn)**

> [!NOTE]
> Við blandaðar aðstæður, þar sem fyrst þarf að setja saman hluta magnsins og afhenda þarf annað magn úr birgðum, eru tvær vöruafhendingarlínur búnar til. Ein er fyrir er fyrir samsetningarpöntunarmagn, og ein er fyrir birgðamagn.

> Í því tilfelli er magn samsetningarpöntunarinnar meðhöndlað eins og lýst er í þessu efnisatriði og birgðamagnið eins og hefðbundin vöruhúsaafhendingarlína. Frekari upplýsingar um samsetningaraðstæður eru í [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

