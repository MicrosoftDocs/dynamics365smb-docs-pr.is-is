---
title: Setja upp notendur samþykktar
description: Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferlinu á uppsetningarsíðu samþykktarnotanda.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 663
ms.date: 09/08/2022
ms.author: edupont
ms.openlocfilehash: 2654dcb68b579d90fe3218bcd0bba3bde4cb5036
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585838"
---
# <a name="set-up-approval-users"></a>Setja upp notendur samþykktar

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Á síðunni **Uppsetning fyrir samþykki notanda** er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi.  

> [!NOTE]  
> Bæði samþykktarbeiðandi og samþykktaraðili verða fyrst að vera settir upp sem notendur verkflæðis á síðunni **Notendahópur verkflæðis**. Frekari upplýsingar má finna í [Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md).  

Þegar notendur samþykkis hafa verið settir upp er hægt að stofna verkflæðisviðbrögð fyrir samþykktarverkflæði. Frekari upplýsingar er að finna í skrefi 9 í [Stofna samþykktarverkflæði](across-how-to-create-workflows.md).  

> [!NOTE]  
> Til að skilgreina að samþykktarbeiðni sé ekki samþykkt fyrr en margir notendur hafa samþykkt hana skal setja upp samþykktaraðila í stigveldi. Hvað varðar samþykkjendur af gerðinni **Samþykkjandi** skal setja þá upp á síðunni **Uppsetning Samþykkjandi notandi**. Hvað varðar samþykkjendur af gerðinni **Notendaflokkur verkflæðis** skal setja þá upp á síðunni **Notendaflokkar verkflæðis** og skilgreina stigveldið með því að úthluta stighækkandi númerum á hvern samþykkjanda í reitnum **röð nr.**. . Frekari upplýsingar má finna hér að neðan og í [Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Uppsetning samþykkts notanda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samþykktarnotanda**, velja síðan viðkomandi tengil.  
2. Á síðunni **Samþykkjandi notandauppsetning** þarf að búa til nýja línu og fylla reitina út eins og lýst er í eftirfarandi töflu.  

   |Svæði|Lýsing|
   |-----|-----------|
   |**Kenni notanda**|Velja skal notandakenni þess sem tekur þátt í samþykktarferlinu.|
   |**Kóði sölumanns/innk.aðila**|Tilgreindu kóða sölumanns eða innkaupaaðila sem gildir um notandann.<br /><br /> Vanalega er reiturinn **Sölum./Innk. kóði** fylltur út ef sölumaður eða kaupandi sem er ábyrgur fyrir viðskiptamanninum eða lánardrottni er einnig aðilinn sem þarf að samþykkja sölu- eða innkaupabeiðnina sem um ræðir.|
   |**Notandakenni samþykkjanda**|Veldu notandakenni þess sem verður að samþykkja beiðnir sem einstaklingurinn í reitnum **Notandakenni** gerir.|
   |**Takmörk samþykktar á sölu**|Tilgreindu hámarkssöluupphæð í staðbundnum gjaldmiðli (SGM) sem einstaklingurinn í reitnum **Notandakenni** getur samþykkt.|
   |**Ótakmörkuð söluheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar sölubeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út reitinn **Samþykktarmörk söluupphæðar**.|
   |**Takmörk samþykktar á innkaupum**|Tilgreindu hámarkssöluupphæð í SGM sem einstaklingurinn í reitnum **Notandakenni** getur samþykkt.|
   |**Ótakmörkuð innkaupaheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar innkaupabeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út reitinn **Samþykktarmörk innkaupaupphæðar**.|
   |**Takmörk samþykktar á beiðni**|Tilgreindu hámarksupphæð í SGM sem einstaklingurinn í reitnum **Notandakenni** getur samþykkt fyrir innkaupabeiðnir.<br /><br /> Til að nota þennan reit þarf að velja **Keðja samþykkjenda** valkostinn í **Gerð takmarkana fyrir samþykktaraðila** reitnum á síðunni **Verkflæðissvörun**.|
   |**Ótakmörkuð samþykktarbeiðniheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar innkaupabeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út reitinn **Samþykktarmörk á upphæð beiðni**.|
   |**Staðgengill**|Veldu notandakenni þess sem verður að samþykkja beiðnir sem einstaklingurinn í reitnum **Notandakenni** gerir ef notandinn í **Kenni samþykkjanda** er ekki tiltækt. <br /><br />**Athugið:** Staðgengillinn getur annaðhvort verið notandinn í reitnum **Staðgengill**, beini samþykkjandinn eða samþykktarstjórnandi, í þessari forgangsröð. Frekari upplýsingar má finna á [Nota Samþykktarverkflæði](across-how-use-approval-workflows.md).|
   |**Netfang**|Tilgreindu netfang einstaklingsins í reitnum **Notandakenni**.|
   |**Samþykktastjórnandi**|Tilgreindu notandann sem hefur rétt til að opna á samþykktarverkflæði, t.d. með því að úthluta samþykktarbeiðnum á nýja samþykktaraðila eða eyða samþykktarbeiðnum sem hafa fallið á tíma.|

   > [!NOTE]
   > Aðeins einn einstaklingur getur verið stjórnandi samþykkis.

3. Til að prófa uppsetningu samþykkts notanda, skal velja aðgerðina **Uppsetning samþykkts notanda**.  
4. Endurtaktu skref 2 til 3 fyrir hvern einstakling sem á að setja upp sem samþykktarnotanda.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
