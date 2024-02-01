---
title: Innkaupafærslur þriðju aðila ESB
description: Í þessu efnisatriði er útskýrt hvernig eigi að setja upp og nota innkaupafærslur þriðju aðila í Evrópusambandinu.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/07/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Innkaupafærslur þriðju aðila ESB

Samningur við Evrópusambandið (ESB) um viðskipti þriðja aðila þegar tekið er við innkaupareikningi frá viðskiptavini í einu ESB-landi/svæðinu og afurðirnar eru sendar til annars ESB-lands/svæðis án þess að það komi inn í dvalarlandið. Hægt er að auðkenna og skrá færsluupphæðina til samræmis við nokkur ESB-lönd '/svæði fyrir virðisauka (VSK) skýrslugerð og VSK Upplýsingaskiptakerfi (VIES). Microsoft  Dynamics 365 Business Central  virkjar að innkaupafærslur verði settar upp sem þriðja aðila í VIÐSKIPTUM ESB. Bókaðar færslur frá þriðja aðila ESB geta verið afmarkaðar í VSK-skýrslum og útilokaðar upphæðina í  **dálknum**  Sala til viðskiptamanna  **VSK-VIES**  -skýrslu.

Þó að aðgerðin sé foruppsett er hún ekki virkjuð að sjálfgefnu. Fylgdu þessum skrefum til að virkja aðgerðina.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, farið í  **vinnusvæði aðgangsstjórnunar**  og síðan valinn tilheyrandi tengill.
2. Á listanum skal finna og velja  **aðgangsuppfærslu: skipta út fyrirliggjandi innkaupaaðgerðum ESB 3-aðila með NÝJA ESB-3-aðila viðskiptainnkaupanafnaukanum**.
3.  **Í dálkinum virkt fyrir**  dálk skal velja  **alla notendur**.

## Virkja viðskiptaþvingun þriðja aðila ESB fyrir innkaup

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **VSK-uppsetningu** og velja síðan tengda tengilinn.
2. Á uppsetningarsíðu  **VSK, merkið við**  REITINN virkja ESB-3-aðila  **.** 

## Nota ESB-aðgerðir þriðja aðila

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **innkaupareikning**  (eða annað innkaupaskjal) og velja síðan tengda tengilinn.
2. Veljið fyrirliggjandi innkaupareikning eða veljið  **nýtt**  til að stofna nýjan.
3.  **Á flipanum upplýsingar um sundurliðun**  reiknings skal velja  **gátreitinn eu 3-aðila viðskipti** .
4. Veldu  **í lagi**.

## Taka eða útiloka viðskiptafærslur frá þriðja aðila á VSK-yfirliti

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **VSK-yfirlit** og velja síðan tengda tengilinn.
2.  **Á VSK-yfirlitssíðu**  er valinn einn af eftirtöldum valkostum til að sýna viðskiptafærslur þriðju aðila með því að nota  **ESB-3-aðila viðskiptaafmörkunarsvæði** .

    | Valkostur | Heimildasamstæða |
    |--------|-------------|
    | Allt | Sýna allar færslur óháð því hvort merkt er við  **ESB 3-aðila viðskiptasvæðið**  í skjölum. |
    | ESB3 | Sýna aðeins færslur þar sem merkt er við  **viðskiptasvæði**  ESB 3-aðila í skjölum. |
    | Non-EU3 | Sýna aðeins færslur þar sem ekki eru  **merktar viðskiptasvæði**  ESB 3-aðila í skjölum. |


## Sjá einnig .
[Fjármálastjórnun](finance.md)  
[Vinna með Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
