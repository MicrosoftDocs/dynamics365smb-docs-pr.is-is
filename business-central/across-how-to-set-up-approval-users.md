---
title: Setja upp notendur samþykktar
description: Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðinotendur sem taka þátt í samþykktarferlum á síðu Samþykktarnotanda.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: e4bb6345a55eedabdf433dbb84a7bf0c7f64d215
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129795"
---
# <a name="set-up-approval-users"></a>Setja upp notendur samþykktar

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Á síðunni **Uppsetning fyrir samþykki notanda** er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi.  

> [!NOTE]  
> Notendur sem samþykkja, bæði samþykkjendur beiðni og samþykkjendur, verða fyrst að vera settir upp sem notendur verkflæðis á síðunni **Verkflæði notandahópur**. Frekari upplýsingar eru í [Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md).  

 Þegar notendur samþykkis hafa verið settir upp er hægt að nota uppsetninguna til að stofna verkflæðisviðbrögð fyrir samþykktarverkflæði. Frekari upplýsingar eru í skrefi 9 í [Stofna verkflæði](across-how-to-create-workflows.md).  

> [!NOTE]  
> Til að skilgreina að samþykktarbeiðni sé ekki samþykkt fyrr en margar samþykkjendur í samþykktarkeðju hafa samþykkt skal setja upp samþykkjendur í stigveldi. Hvað varðar samþykkjendur af gerðinni **Samþykkjandi** skal setja þá upp á síðunni **Uppsetning Samþykkjandi notandi**. Hvað varðar samþykkjendur af gerðinni **Notendaflokkur verkflæðis** skal setja þá upp á síðunni **Notendaflokkar verkflæðis** og skilgreina stigveldið með því að úthluta stighækkandi númerum á hvern samþykkjanda í reitnum **röð nr.**. . Frekari upplýsingar eru í þessu efnisatirði og [Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Uppsetning samþykkts notanda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Uppsetning á notanda samþykktar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Samþykkjandi notandauppsetning** þarf að búa til nýja línu og fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kenni notanda**|Velja skal notandakenni notanda sem tekur þátt í samþykktarferlinu.|  
    |**Kóði sölumanns/innk.aðila**|Tilgreina skal sölumann eða kaupanda kóða sem gildir um notandann í **Sölum./Innk. kóði** reitnum.<br /><br /> Vanalega er reiturinn **Sölum./Innk. kóði** fylltur út ef sölumaður eða kaupandi sem er ábyrgur fyrir viðskiptamanninum eða lánardrottni er einnig aðilinn sem þarf að samþykkja sölu eða innkaupabeiðinina.|  
    |**Notandakenni samþykkjanda**|Velja notandakenni notanda sem verður að samþykkja beiðnir sem gerðar eru af notandanum í reitnum **Notandakenni**.|  
    |**Takmörk samþykktar á sölu**|Tilgreina hámarkssöluupphæð í SGM sem notandi í **Notandakenni** reitnum getur samþykkt.|  
    |**Ótakmörkuð söluheimild**|Tilgreina að notandi í **Notandakenni** reitnum getur samþykkt allar sölubeiðnir saman hver upphæð þeirra er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að **fylla út reitinn samþykkisöluupphæðarmörk** sölu.|  
    |**Takmörk samþykktar á innkaupum**|Tilgreina hámarkssöluupphæð í SGM sem notandi í **Notandakenni** reitnum getur samþykkt.|  
    |**Ótakmörkuð innkaupaheimild**|Tilgreina að notandi í **Notandakenni** reitnum getur samþykkt allar sölubeiðnir saman hver upphæð þeirra er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að **fylla út reitinn samþykkisöluupphæðarmörk** sölu.|  
    |**Takmörk samþykktar á beiðni**|Tilgreina hámarksupphæð í SGM sem notandi í **Notandakenni** reitnum getur samþykkt fyrir innkaupabeiðni.<br /><br /> Til að nota þennan reit þarf að velja **Keðja samþykkjenda** valkostinn í **Gerð takmarkana fyrir samþykktaraðila** reitnum á síðunni **Verkflæðissvörun**.|  
    |**Ótakmörkuð samþykktarbeiðniheimild**|Tilgreina að notandi í **Notandakenni** reitnum getur samþykkt öll kauptilboð saman hver upphæð þeirra er.<br /><br /> Ef þessi gátreitur er valinn, þá er ekki hægt að **fylla út reitinn samþykkisupphæð beiðni um samþykki**.|  
    |**Staðgengill**|Veljið NOTANDAKENNI notandans sem þarf að samþykkja beiðnir frá notandanum í **reitnum notandakenni** ef notandinn í **Kenni samþykkis** er ekki tiltækur. <br /><br />**Athugið:** Staðgengillinn getur annaðhvort verið notandinn í reitnum **Staðgengill**, beini samþykkjandinn eða samþykktarstjórnandi, í þessari forgangsröð. Frekari upplýsingar eru í [Nota verkflæði samþykktar](across-how-use-approval-workflows.md).|  
    |**Netfang**|Tilgreina netfang notanda í **Notandakenni** reitnum.|  
    |**Samþykktastjórnandi**|Tilgreinið notandann sem hefur réttindi til að loka ólæsa samþykktarverkflæði. D. með því að ráðstafa samþykkisbeiðnum til nýrra staðgengilsvara og eyða gjaldföllnum samþykkisbeiðnum.|

    > [!Note]
    > Aðeins einn einstaklingur getur verið stjórnandi samþykkis.

3. Til að prófa uppsetningu samþykkts notanda, skal velja aðgerðina **Uppsetning samþykkts notanda**.  
4. Endurtaka skal þrep 2 til 3 fyrir hvern notanda sem á að stofna sem notanda samþykkis.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Búa til verkflæði](across-how-to-create-workflows.md)  
[Uppsetning verkflæðis](across-set-up-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]