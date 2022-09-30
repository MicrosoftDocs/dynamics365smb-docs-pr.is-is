---
title: Setja upp notendur samþykktar
description: Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðinotendur sem taka þátt í samþykktarferlum á síðu Samþykktarnotanda.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585838"
---
# <a name="set-up-approval-users"></a>Setja upp notendur samþykktar

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Á síðunni **Uppsetning fyrir samþykki notanda** er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi.  

> [!NOTE]  
> Bæði samþykktaraðilar og samþykkjendur verða fyrst að setja upp verkflæðinotendur á **síðunni verkflæðisnotendaflokkur**. Frekari upplýsingar um uppsetningu á [Verkflæðisnotendum](across-how-to-set-up-workflow-users.md).  

Þegar samþykktarnotendur hafa verið settir upp er hægt að stofna svör verkflæðis fyrir samþykktarverkflæði. Frekari upplýsingar úr skrefi 9 í [Stofna samþykktarverkflæði](across-how-to-create-workflows.md).  

> [!NOTE]  
> Ef skilgreina á samþykktarbeiðni sem ekki samþykkt fyrr en margir notendur hafa samþykkt hana er sett samþykkjendur upp í stigveldi. Hvað varðar samþykkjendur af gerðinni **Samþykkjandi** skal setja þá upp á síðunni **Uppsetning Samþykkjandi notandi**. Notendaflokkur **verkflæðis fyrir samþykkjanda** er stilltur, stilla samþykkjendur á **síðunni verkflæði notendaflokka** og skilgreina stigveldið með því að úthluta stigvaxandi númerum á hvern samþykkjanda í reitnum **Raðnúmer nr.** . Frekari upplýsingar að neðan og at [Setja upp Verkflæðisnotendum](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Uppsetning samþykkts notanda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **notendauppsetningu** samþykkisins, velja síðan tengda tengilinn.  
2. Stofnið nýja línu á **síðunni Samþykktarnotandauppsetning** og fyllið þá reitina eins og lýst er í eftirfarandi töflu.  

   |Svæði|Lýsing|
   |-----|-----------|
   |**Kenni notanda**|Veljið NOTANDAKENNI einstaklingsins sem á við samþykktarferlið.|
   |**Kóði sölumanns/innk.aðila**|Tilgreinið sölumanninn eða innkaupaaðila kóta sem á við notandann.<br /><br /> Yfirleitt er fyllt út í **salespers./Purch. Kóti** ef Sölumaður eða innkaupaaðili sem er ábyrgur fyrir viðskiptavini eða lánardrottinn er einnig sá sem á að samþykkja sölu-eða innkaupabeiðnina.|
   |**Notandakenni samþykkjanda**|Veljið NOTANDAKENNI einstaklingsins sem á að samþykkja beiðnir sem einstaklingurinn hefur auðkennt í **reitnum notandakenni**.|
   |**Takmörk samþykktar á sölu**|Tilgreinið hámarks söluupphæð í staðbundnum gjaldmiðli (ISK) sem einstaklingurinn sem auðkenndur er í **reitnum notandakenni** getur samþykkt.|
   |**Ótakmörkuð söluheimild**|Tilgreinið að einstaklingurinn sem auðkenndur er **í reitnum notandakenni** geti samþykkt allar sölubeiðnir sem eru án upphæðarinnar.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út **reitinn samþykkisöluupphæðarmarka**.|
   |**Takmörk samþykktar á innkaupum**|Tilgreinið hámarks innkaupsupphæð í ISK sem einstaklingurinn sem auðkenndur er í **reitnum notandakenni** getur samþykkt.|
   |**Ótakmörkuð innkaupaheimild**|Tilgreinið að einstaklingurinn sem auðkenndur er **í reitnum notandakenni** geti samþykkt allar innkaupabeiðnir án tillits til upphæðar.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út **reitinn samþykktarmörk** innkaupa.|
   |**Takmörk samþykktar á beiðni**|Tilgreinið Hámarksupphæð í ISK sem einstaklingurinn sem auðkenndur er í **reitnum notandakenni** getur samþykkt fyrir innkaupatilboð.<br /><br /> Til að nota þennan reit þarf að velja **Keðja samþykkjenda** valkostinn í **Gerð takmarkana fyrir samþykktaraðila** reitnum á síðunni **Verkflæðissvörun**.|
   |**Ótakmörkuð samþykktarbeiðniheimild**|Tilgreinið að einstaklingurinn sem auðkenndur er **í reitnum notandakenni** geti samþykkt allar innkaupabeiðnir óháð upphæðinni.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út reitinn samþykkisupphæð samþykktar **á** Upphæð beiðninnar.|
   |**Staðgengill**|Veljið notandakenni þess sem mun samþykkja beiðnir frá einstaklingnum sem er auðkenndur í **reitnum notandakenni**, ef notandinn í **Kenni** samþykkjanda er ekki tiltækur. <br /><br />**Athugið:** Staðgengillinn getur annaðhvort verið notandinn í reitnum **Staðgengill**, beini samþykkjandinn eða samþykktarstjórnandi, í þessari forgangsröð. Frekari upplýsingar um [samþykktarverkflæði](across-how-use-approval-workflows.md) nota.|
   |**Netfang**|Tilgreinið netfang einstaklingsins í **reitnum notandakenni**.|
   |**Samþykktastjórnandi**|Tilgreinið notandann með réttindum til að aflæsa samþykktarverkflæði, svo sem með því að úthluta samþykkisbeiðnum til nýrra staðgengilstilfella eða eyða gjaldföllnum samþykktarbeiðnum.|

   > [!NOTE]
   > Aðeins einn einstaklingur getur verið stjórnandi samþykkis.

3. Til að prófa uppsetningu samþykkts notanda, skal velja aðgerðina **Uppsetning samþykkts notanda**.  
4. Endurtaka skal þrep 2 til 3 fyrir hvern þann sem á að setja upp sem samþykkinotanda.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Stofna samþykktarverkflæði](across-how-to-create-workflows.md)  
[Uppsetning Samþykktarverkflæðis](across-set-up-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
