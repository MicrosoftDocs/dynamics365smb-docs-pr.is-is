---
title: Sameina stöður fyrir fyrirtæki sem er Viðskiptamaður og lánardrottinn
description: Lýsir því hvernig á að sameina stöður fyrir viðskiptavin sem er einnig lánardrottinn.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.search.form: 5052, 21, 5050
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 66e97780c2f8d4cd771c774fa306fd8197d36c95
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521021"
---
# <a name="consolidate-balances-for-a-company-that-is-a-customer-and-a-vendor"></a>Sameina stöður fyrir fyrirtæki sem er Viðskiptamaður og lánardrottinn
Fyrirtæki sem þú átt viðskipti við gætu bæði verið viðskiptamaður og lánardrottinn. Þegar það er tilfellið er hægt að komast hjá því að gera óþarfar greiðslur eða kvittanir og ef til vill spara á Færslugjöld, með því að styrkja stöður viðskiptavina og lánardrottna fyrirtækisins. Samstæða tengir saman stöður fyrirtækisins sem lánardrottinn og sem viðskiptavin og heldur nets þeirri upphæð þannig að annað hvort staða viðskiptamanns eða lánardrottins er eftir því hvaða upphæð var hærri. 

Til að sameina stöðuna þarf fyrst að tengja viðskiptamanninn og lánardrottnafyrirtækin í gegnum tengilið sem er með gerðinni **fyrirtæki**. Viðskiptavinur eða lánardrottinn getur aðeins haft einn tengilið af gerðinni **fyrirtæki**. Frekari upplýsingar eru í [Stofna tengiliði](marketing-create-contact-companies.md).

Þegar búið er að tengja fyrirtækin þá **býður viðskiptamannaspilið** upp á **stöðuna sem lánardrottinn** og **lánardrottnaspjaldið** **hefur stöðuna sem viðskiptavinur**.

Þó er það ekki krafa, að viðskiptamenn og lánardrottnafyrirtæki séu yfirleitt sami Lögaðili. 

## <a name="before-you-start"></a>Verður að byrja fyrir
Áður en stöður eru sameinaðar skal tilgreina nokkrar stillingar á **síðu markaðsuppsetningarsíðunnar**. 

* **Á flipanum samskipti** þarf að tilgreina viðskiptatengslakóta í **svæðunum viðskiptamenn** og **Lánardrottnar**. [!INCLUDE[prod_short](includes/prod_short.md)] notar þessar upplýsingar til að ákvarða tegund tengsla sem á að birta fyrir tengiliði. 
* Valfrjálst: á **flipanum tvítekningar er leit á tvítekningum** snúið við eða slökkt á henni. Leit er sjálfkrafa kveikt í tvítekningu. Sjá [handling tvítekningar](#handling-duplicates) fyrir frekari upplýsingar. 

## <a name="link-an-existing-customer-and-vendor-company-thorough-a-contact"></a>Tengja tengilið og fyrirtæki sem þegar er til Ítarlegt
Eftirfarandi skref lýsa því hvernig á að tengja viðskiptavin og lánardrottin í gegnum tengilið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinur** eða **Lánardrottinn** og velja síðan viðkomandi tengil.
2. Velja skal viðskiptavin eða lánardrottinn og velja **síðan aðgerðina tengiliður**.
3. Ef annað er ekki í **reitnum viðskiptatengsl** en **enginn** verður að fjarlægja tengslin. Til að gera það skaltu nota **aðgerðina viðskiptatengsl** og eyða síðan venslunum. 
4. Eftir því hvort viðskiptavinur eða lánardrottinn **er** valinn í skrefi 1 skal velja þá **ljósaperu sem** opnar aðgerðina segja. ![...](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd og síðan inn í andstæðan teig. Það er, ef lánardrottinn er valinn **, ætti að leita til** viðskiptamanns **.**
5. Velja skal lánardrottinn eða viðskiptavin og velja **síðan Tengiliðir**.
6. Velja skal **tengilinn með fyrirliggjandi** aðgerð og svo **valkostinn Viðskiptamaður** eða **Lánardrottinn**.
7. Veljið viðskiptavin eða lánardrottinn.

## <a name="create-a-vendor-from-a-customer-or-vice-versa"></a>Stofna lánardrottin úr viðskiptamanni, eða öfugt
Hægt er að stofna nýjan lánardrottinn úr fyrirliggjandi viðskiptamanni, eða nýjum viðskiptamanni frá lánardrottni. **Opnið** tengiliðasíðuna **á síðunum Viðskiptamaður** eða **Lánardrottinn**. **Velja aðgerðina stofna sem** aðgerð og síðan annað hvort valkosti fyrir **viðskiptavin** eða **lánardrottna**. 

## <a name="create-a-new-customer-or-vendor-and-link-them-through-a-vendor-or-customer-contact"></a>Stofna nýjan viðskiptavin eða lánardrottinn og tengja þá við tengilið lánardrottins eða viðskiptavinar
1. Stofna nýjan viðskiptavin eða lánardrottinn. Frekari upplýsingar er að finna [í skrá nýja viðskiptamenn](sales-how-register-new-customers.md) eða [skrá nýja viðskiptamenn](sales-how-register-new-customers.md).
2. Þegar viðskiptamaður eða lánardrottinn er settur upp skal velja **aðgerðina stofna** og velja **síðan valkosti viðskiptavinar** eða **lánardrottins**. 

## <a name="to-consolidate-the-customer-and-vendor-balances-for-a-contact-company"></a>Til að sameina stöður viðskiptamanna og lánardrottna fyrir tengiliðafyrirtæki
**Á síðunni greiðslubók** er aðgerðin nettó-viðskiptamanna-/lánardrottnastaða **notuð** til að sameina stöður viðskiptamanna og lánardrottna í eina nettóupphæð. Aðgerðin stofnar en bókar ekki greiðslubókarlínur sem innihalda nettóstöðu.

> [!NOTE]
> Ef viðskiptamanna-eða lánardrottnastöður innihalda upphæðir sem eru í mismunandi gjaldmiðlum er stofnuð lína fyrir upphæðina í hverjum gjaldmiðli.

## <a name="handling-duplicates"></a>Meðhöndlun tvítekningum
Ef kveikt er á tvítekningu á **flipanum tvítekningar** á **uppsetningarsíðu** markaðssetningar birtist viðvörun þegar gildum reita sem eru hluti uppsetningarinnar fyrir tvíteknum leitarstrengjum er breytt. Þegar Tvítekning finnst er hægt að grípa til eftirfarandi aðgerða:

* Sameinið tvítekna tengiliði í einum tengilið sem er sá sami fyrir bæði viðskiptavininn og lánardrottininn með því að nota **blöndunartækin** á **síðunni tengiliðaspjald**. Yfirleitt er aðeins aðeins gert við sameinaða tengiliði þegar viðskiptamaður og lánardrottinn eru sami Lögaðili. Frekari upplýsingar er að finna í [Sameina tvítekin atriði](sales-how-merge-duplicate-records.md). 
* Eyða viðskiptatengslum lánardrottins eða tengiliða lánardrottins og nota **síðan tengilinn við fyrirliggjandi** aðgerð til að tengja við annan tengilið.    

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  
