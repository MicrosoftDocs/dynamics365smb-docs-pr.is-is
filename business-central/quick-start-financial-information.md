---
title: Fjárhagslegar upplýsingar Flýtistart
description: Fáðu fyrirtækið þitt tilbúið til viðskipta með því að setja upp fjárhagslegar upplýsingar í Viðskiptamiðinu.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: ''
ms.date: 08/25/2022
ms.author: a-reishima
ms.openlocfilehash: 6d8383015e977acffe94555eec00bfb8f104085d
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9586031"
---
# <a name="financial-information-quick-start"></a>Fjárhagslegar upplýsingar Flýtistart

Eftir að upplýsingar um grunnfyrirtæki hafa verið færðar inn [!INCLUDE[prod_short](includes/prod_short.md)] er eitt af næstu skrefum að ljúka við fjárhaghlutann. Þetta er ekki einungis gert til að taka við eða gera greiðslur, heldur einnig til að stjórna og skrá inn tölur um viðskipti.

## <a name="the-chart-of-accounts"></a>Bókhaldslykilinn

Bókhaldslykillinn (COA) býður upp á Yfirlit um fjármál félagsins, listar upp reikninga í skipulögðum flokkum eins og eignir, skuldir, tekjur, kostnað seldra vara og kostnað. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlað bókhaldslykli sem hægt er að sérsníða að bókhaldsvenjum fyrirtækisins.

## <a name="set-up-the-chart-of-accounts"></a>Uppsetning bókhaldslykla

Eftirfarandi myndband sýnir hvernig bókhaldslykillinn er settur upp í [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts"></a>Bæta reikningi við bókhaldslykla

Ef bæta á við lykli sem er sjálfgefinn í [!INCLUDE[prod_short](includes/prod_short.md)] — til dæmis garðaþjónustu — Fylgdu eftirfarandi leiðbeiningum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **bókhaldslykil** og veljið síðan tengda tengilinn.
2. **Velja nýja** aðgerð til að opna **síðuna fjárhagsreikningspjald**.
3. Færið inn eftirfarandi gögn í samsvarandi svæði á **flipanum Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Svæði | Gögn |
   | --- | --- |
   | **Nr.** | 61250 |
   | **Heiti** | Garðaþjónusta |
   | **Tekjur/staða** | Rekstrarreikningur |
   | **Lykiltegund** | Útgjöld |
   | **Undirflokkur reiknings** | Viðgerða- og viðhaldskostnaður |
   | **Debet/kredit** | Bæði |
   | **Tegund reiknings** | Bóka |

4. **Á bókunarflipanum** festing eru færð inn eftirtalin gögn:

   | Svæði | Gögn |
   | --- | --- |
   | **Alm. bókunargerð** | Innkaup |
   | **Alm. bókunarflokkur** | Innanlands |
   | **Bókunarflokkur framl. bókunar** | Þjónusta |

5. Reitirnir sem eftir eru eru fylltir út á **spjaldinu** fjárhagsreikningur eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts"></a>Fá yfirlit yfir bókhaldslykla

Ef þörf er á fleiri þjöppuð yfirlit yfir bókhaldslykla, án dálka fyrir bókunarflokka, bókunargerð eða tegund kostnaðar, er til dæmis **Listi yfir Yfirlit** bókhaldslykla yfir helstu upplýsingar fyrir hvern lykil í minni töflu. Auk þess er hægt að fella niður eða Útvíkka flokka til að fela reikningana inni í þeim.

Til að birta yfirlitið skal velja **Yfirlit yfir** Aðgerðir bókhaldslykilsins á **síðunni Bókhaldslykill** eða leita að aðgerðinni með því að nota ![ljósapera sem opnar aðgerðina segja aðgerð 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera").

Meiri upplýsingar um bókhaldslykilinn og fjárhag við [að skilja fjárhag og bókhaldslykla](finance-general-ledger.md).

## <a name="set-up-bank-accounts"></a>Setja upp bankareikninga

Bankareikningum í [!INCLUDE[prod_short](includes/prod_short.md)] skrá bankafærslur og eru tengdir við færslur í bókhaldslyklum. Eftirfarandi myndband sýnir hvernig Bankareikningar eru settir upp.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **bankareikninga** og veljið síðan tengda tengilinn.
2. Á síðunni **bankareikningar** skal velja aðgerðina **Nýtt**.
3. Í reitnum **númer** Kenni eins og *B010* kemur sjálfkrafa inn ef það er Tölusettur raðlisti fyrir bankareikninga. Ef ekki, Færið inn einstaka samsetningu.

   Reiturinn er annar en **Bankareikningur nr.** er einnig tiltækur á **flipanum Almennt**.
4. Reitirnir á síðu bankareiknings kortsins **eru** fylltir út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Setja upp bókhaldslykil](finance-setup-chart-accounts.md)  
[Bankareikningar settir upp](bank-how-setup-bank-accounts.md)  
[Keyra og prenta skýrslur](ui-work-report.md)  
[Stuttir leiðarvísar Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
