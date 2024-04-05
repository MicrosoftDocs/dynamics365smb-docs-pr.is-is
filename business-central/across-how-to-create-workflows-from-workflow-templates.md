---
title: Hvernig á að Búa til verkflæði úr verkflæðissniðmátum
description: Til að spara tíma þegar nýtt samþykktarverkflæði er stofnað er hægt að búa til verkflæði úr verkflæðissniðmátum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dajoo
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Stofna verkflæði úr verkflæðissniðmátum

Á síðunni **Verkflæði** er búið til verkflæði með því að stofna röð verkflæðisskrefa í línunum. Hvert skref samanstendur af verkflæðistilviki (When Event), í meðallagi eftir atvikaskilyrðum (Á skilyrði) og verkflæðissvari (Þá Svar), í meðallagi svarvalkostum. Reitirnir í verkflæðislínunum bjóða upp á fasta lista yfir atburða- og svargildi sem tákna aðstæðurnar sem [!INCLUDE [prod_short](includes/prod_short.md)] styðja. Frekari upplýsingar eru á [Búa til verkflæði](across-how-to-create-workflows.md).

Til að spara tíma þegar samþykktarverkflæði eru stofnuð veitir [!INCLUDE [prod_short](includes/prod_short.md)]  sniðmát verkflæðis. Sniðmátin eru tiltæk á síðunni **Sniðmát** verkflæðis. Hægt er að nota sniðmátin eins og þau eru eða sérsníða þau eftir þörfum. Kótar fyrir verkflæðissniðmátin frá Microsoft eru forskeytinu með **MS-**.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Ef verkflæðissniðmáti er breytt, en síðar sést eftir breytingunni, skal nota aðgerðina **Endurstilla Microsoft-sniðmát** til að snúa aftur í upprunalegu stillinguna fyrir verkflæðið.

> [!CAUTION]
> Aðgerðin **Endurstilla** Microsoft-sniðmát endurstillir öll verkflæðissniðmát Microsoft. Ekki er hægt að endurstilla eitt sniðmát.  

Önnur leið til að stofna verkflæði á fljótlegan hátt er að flytja það inn, til dæmis ef það var flutt út frá öðru tilviki. [!INCLUDE[prod_short](includes/prod_short.md)] Frekari upplýsingar eru í [Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md).  

## Að búa til verkflæði úr verkflæðissniðmáti

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Nýtt verkflæði úr sniðmáti**. Síðan **Sniðmát verkflæðis** opnast.  
3. Veldu verkflæðissniðmát, veldu síðan **Í lagi**.  

   Síðan **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti. Við gildið í reitnum **Kóði** er bætt við t.d. „-01“ til að gefa til kynna að þetta sé fyrsta verkflæðið sem er stofnað úr verkflæðissniðmátinu.  
4. Til að sérstilla verkflæðið skal breyta verkflæðisskrefunum eða bæta við nýjum skrefum. Frekari upplýsingar eru á [Búa til verkflæði](across-how-to-create-workflows.md).  

## Sjá einnig .

[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)  
[Flytja samþykktarverkflæði inn og út](across-how-to-export-and-import-workflows.md)  
[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)  
[Eyða samþykktarverkflæðum](across-how-to-delete-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
