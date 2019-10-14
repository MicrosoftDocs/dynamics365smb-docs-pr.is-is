---
title: Hvernig á að búa til tilboð með samsetningarpöntun | Microsoft Docs
description: Hægt er að nota samsetningarstjórnun til að sérsníða samsetningaríhlut eftir beiðni viðskiptavinar á meðan söluferlinu stendur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1ca43d43c382d191854e89760479d642edec722a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307709"
---
# <a name="quote-an-assemble-to-order-sale"></a>Búa til tilboð með samsetningarpöntun
Hægt er að nota samsetningarstjórnun til að sérsníða samsetningaríhlut eftir beiðni viðskiptavinar á meðan söluferlinu stendur. Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  

Eins og þegar seld er hvers kyns önnur tegund af vöru, er einnig hægt að stofna sölutilboð fyrir sérsniðna samsetningarvöru áður en henni er umbreytt í sölupöntun. Þetta ferli felur í sér nokkur aukaskref í samanburði við stofnun venjulegs standandi sölutilboðs, og notar afbrigði tengdrar samsetningarpöntunar, sem er samsetningartilboð.

> [!NOTE]  
>  Eins og allar gerðir á tilboðum er magn samsetningartilboða ekki notað til ráðstöfunar, í áætlun eða frátekt.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>Til að stofna sölutilboð fyrir vöru sem setja skal saman í pöntun  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **sölutilboð** og veldu síðan tengda tengilinn.  
2.  Stofna nýja sölupöntunarlínu með eina línu fyrir samsetningaríhlut. Frekari upplýsingar er að finna í [Búa til sölutilboð](sales-how-make-offers.md).  
3.  Í reitnum **Magn til samsetningar til pöntunar** skal færa inn fullt magn.

    > [!NOTE]  
    >  Ekki ætti að gera tilboð í hlutamagn. Því verður að færa inn sama magn og fært var inn í reitinn **Magn** í sölutilboðslínunni.  

4.  Á flýtiflipanum skal velja **Línur**, velja **Lína**, velja **Samsetning til pöntunar** og síðan **Setja saman í pöntunarlínur**. Að öðrum kosti skal velja reitinn **Magn til samsetningar til pöntunar** í línunni.  
5.  Á síðunni **Setja saman í pöntunarlínu** endurskoðið og breytið samsetningu pöntunalína samkvæmt tilboði standandi pöntunar sem viðskiptamaðurinn hefur farið fram á. Ef skoða á nánari upplýsingar skal velja aðgerðina **Sýna fylgiskjal** til að opna tilboð standandi pöntunarinnar. Ekki er hægt að breyta innihaldi i flestum reitum, og ekki er hægt að bóka.  
6.  Þegar búið er að leiðrétta samsetningarpöntunarlínur samkvæmt tilboðinu skal loka síðunni **Sameina-í-pöntun línur** til að fara aftur á síðuna **Sölutilboð** .  
7.  Ef viðskiptamaðurinn samþykkir tilboðið skal stofna sölupöntun fyrir samsetningaríhlut tilboðsins. Frekari upplýsingar er að finna í [Búa til sölutilboð](sales-how-make-offers.md). Tengt samsetningartilboð og allar sérstillingar tengjast við þessa nýju sölupöntun til undirbúnings á samsetningu vöru eða vörum sem á að selja.  

## <a name="see-also"></a>Sjá einnig  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
