---
title: "Hvernig á að setja upp Dagatöl verkstæðis | Microsoft Docs"
description: "Dagatal vinnustöðvar tilgreinir vinnudaga og -stundir, vaktir, frídaga og fjarvistir sem hafa áhrif á mögulega heildarafkastagetu, mælda í tíma, með tilliti til tilgreindra gilda skilvirkni og getu. Stofnun og virkjun dagatals vinnustöðvar þarfnast nokkurra undirbúningsskrefa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 55cefad889557df37d8869926ee7e200cd145d03
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-shop-calendars"></a>Setja upp dagatal verkstæðis
Dagatal vinnustöðva eða véla tilgreinir vinnudaga og -stundir, vaktir, frídaga og fjarvistir sem hafa áhrif á mögulega heildarafkastagetu, mælda í tíma, með tilliti til tilgreindra gilda skilvirkni og getu.

Fyrst þarf að setja upp eitt eða fleiri almenn dagatöl verkstæðis, sem grunn fyrir útreikningum á tilteknu dagatali vinnu- eða vélastöðvar. Dagatal verkstæðis tilgreinir venjulega vinnuviku eftir upphafs- og lokatíma vinnudags og vaktaskipulagi. Auk þess tilgreinir dagatal verkstæðis fasta frídaga árs.  

Eftirfarandi lýsir því hvernig á að setja upp dagatöl vinnustöðva. Skrefin eru svipuð þegar sett eru upp dagatöl vélastöðva.  

## <a name="to-create-work-shifts"></a>Vaktir stofnaðar  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaktir** og veldu síðan tengda tengilinn.  
2.  Númer er fært inn í reitinn **Kóti** á auðri línu til að auðkenna vaktina t.d. **1**.  
3.  Vaktinni er lýst í reitnum **Lýsing** t.d. **1. vakt**  
4.  Einnig er hægt að fylla inn í línur fyrir aðra og þriðju vakt.  

Jafnvel þótt vinnustöðvarnar noti ekki vaktaskipulag þarf að færa inn a.m.k. einn vaktakóta.  

## <a name="to-set-up-a-shop-calendar"></a>Dagatal verkstæðis sett upp  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Dagatal verkstæðis** og veldu síðan tengda tengilinn.  
2.  Númer er fært inn í reitinn **Kóti** á auðri línu til að auðkenna dagatal verkstæðis.  
3.  Dagatali verkstæðisins er lýst í reitnum **Lýsing**.  
4.  Velja aðgerðina **vinnudagar**.
5.  Á síðunni **Dagatal verkstæðis vinnudagar**, skal skilgreina heila vinnuviku, með upphafs- og lokatíma fyrir hvern dag.  

    Í reitnum **Vaktakóti** er hægt að velja einn af vöktunum sem áður voru skilgreind. Bæta við línu fyrir hvern vinnudag og hverja vakt. Dæmi:  

    Mánudagur 07:00 15:00 1   
    Þriðjudagur 07:00 15:00 1  

    Ef þörf er á dagatali verkstæðis með tveimur vöktum þarf að fylla inn í hana á þennan hátt:  

    Mánudagur 07:00 15:00 1   
    Mánudagur 15:00 23:00 2  
    Þriðjudagur 07:00 15:00 1  
    Þriðjudagur 15:00 23:00 2  

    Allir vikudagar sem ekki eru tilgreindir í dagatali verkstæðis, t.d. laugardagur og sunnudagur, eru teknir sem frídagar og hafa enga mögulega afkastagetu í dagatali vinnustöðvar.  

    Þegar allir vinnudagar hafa verið skilgreindir má loka síðunni **Vinnudagar í verkstæðisáætlun** og byrja að færa inn frídaga.  

6.  Á síðunni **Dagatöl verkstæðis** veljið dagatal verkstæðisins og veljið síðan **Frídagar** aðgerðina.
7. Á síðunni **Dagatal verkstæðis frídagar** skal skilgreina frídaga ársins með því að slá inn upphafs- og lokadagsetningu/-tíma þeirra og lýsingu á hverjum frídegi í hverja línu fyrir sig. Dæmi:  

    04/07/14 0:00:00 23:59:00 sumarfrí  
    05/07/14 0:00:00 23:59:00 sumarfrí  
    06/07/14 0:00:00 23:59:00 sumarfrí  

Tilgreindir frídagar hafa enga mögulega afkastagetu í dagatali vinnustöðvar.  

Nú er hægt að úthluta dagatali verkstæðis á vinnustöð til útreiknings á dagatali vinnustöðvar sem mun stjórna tímasetningum aðgerða á þeirri vinnustöð.  

## <a name="to-calculate-a-work-center-calendar"></a>Dagatal vinnustöðvar reiknað út  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnustöðvar** og veldu síðan tengda tengilinn.
2. Opna vinnustöðina sem á að uppfæra.  
3. Í reitnum **Dagatalskóti verkstæðis**, er valið hvaða dagatal verkstæði notar sem grunn fyrir dagatal vinnustöðvar.  
4. Veljið aðgerðina **Dagatal**.  
5. Á síðunni **Dagatal vinnustöðvar**, skal velja **Sýna fylki** aðgerðina.  

    Vinstra megin á fylkjasíðunni má sjá uppsettar vinnustöðvar. Hægra megin er dagatal sem birtir tiltæk getugildi fyrir hvern vinnudag í skilgreindri mælieiningu, til dæmis **480** mínútur. Hver lína táknar dagatal einnar vinnustöðvar.  

    > [!NOTE]  
    >  Einnig er hægt að skoða gildi afkastagetu fyrir hverja viku eða mánuð með því að breyta valinu í reitnum **Skoða eftir** á síðunni **Dagatal vinnustöðvar**.  

    Til að sýna nýtt dagatal verkstæðis sem línu á valdri vinnustöð verður það fyrst að vera reiknað.  

6.  Velja aðgerðina **Reikna**.  
7.  Á flýtiflipanum **Vinnustöð** er hægt að setja afmörkun til að reikna einungis fyrir eina vinnustöð. Ef engar afmarkanir eru settar verða öll stofnuð dagatöl vinnustöðva reiknuð.  
8.  Skilgreina upphafs- og lokadagsetningar dagatalstímabilsins sem á að reikna, t.d. eitt ár ; frá 01/01/14 til 31/12/14.
9. Velja hnappinn **Í lagi** til að reikna út afkastaveitu.  

Dagatalsfærslur eru nú búnar til (eða þær uppfærðar) og sýna þær mögulega afkastagetu fyrir hvert tímabil með tilliti til eftirfarandi 3 gerða aðalgagna:  

- Vinnudögum og vöktum sem tilgreind eru í úthlutuðu dagatali verkstæðis.  
- Gildinu í reitnum **Geta** á vinnustöðvarspjaldinu.  
- Gildinu í reitnum **Skilvirkni** á vinnustöðvarspjaldinu.  

Reiknað dagatal vinnustöðvar skilgreinir nú hvenær og hversu mikil afkastageta er til staðar í þessari vinnustöð. Þetta stýrir ítarlegri röðun aðgerða sem framkvæmdar eru í vinnustöðinni.  

## <a name="to-record-work-center-absence"></a>Fjarvistir í vinnustöð skráðar  
1.  Á síðunni **Dagatal vinnustöðvar**, skal velja **Sýna fylki** aðgerðina.
2. Á síðunni **Dagatal vinnustöðvar fylki** er valin vinnustöð sem og sá dagur dagatalsins sem skrá á fjarvistina á og svo er smellt á aðgerðina **Fjarvist**.  
3.  Á síðunni **Fjarvist** er tilgreindur upphafs- og lokatími fjarvistar þessa dags sem og lýsing á henni. Dæmi:  

    25/01/01 08:00 10:00 viðhald  

4.  Velja **Uppfæra** aðgerðina og síðan loka **Fjarvist** síðunni.  

Afkastageta þessa dags hefur nú minnkað í samræmi við skráðan fjarvistartíma.  

## <a name="see-also"></a>Sjá einnig  
[Setja upp grunndagatöl](across-how-to-assign-base-calendars.md)  
[Setja upp vinnu- og vélastöðvar](production-how-to-set-up-work-and-machine-centers.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

