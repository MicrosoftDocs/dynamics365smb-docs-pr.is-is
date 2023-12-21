---
title: Setja upp notendur samþykktar
description: Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðinotendur sem taka þátt í samþykktarferlum.
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '663,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# Setja upp notendur samþykktar

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp notendurna sem taka samþykktarferli með á  **síðu Samþykktarnotandans** . Einnig er hægt að stilla upphæðamörk fyrir mismunandi gerðir beiðna, skilgreina staðgengilstilkynningar og setja upp tilkynningar.  

Eftir að samþykktarnotendur hafa verið settir upp er hægt að stofna svör verkflæðis fyrir samþykktarverkflæði. Frekari upplýsingar má finna á [Stofna verkflæði samþykktars](across-how-to-create-workflows.md).  

> [!TIP]
> Hægt er að krefjast þess að margir samþykkjendur bregðist við samþykktarbeiðni með því að stofna hóp samþykkjendur á  **síðu verkflæðisnotendaflokksins** . Frekari upplýsingar um  [uppsetningu notendaflokka verkflæðis](across-how-to-set-up-workflow-users.md).  

## Uppsetning samþykkts notanda

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samþykktarnotanda**, velja síðan viðkomandi tengil.  
2. Á síðunni **Samþykkjandi notandauppsetning** þarf að búa til nýja línu og fylla reitina út eins og lýst er í eftirfarandi töflu.  

   |Svæði|Lýsing|
   |-----|-----------|
   |**Kenni notanda**|Velja skal notandakenni þess sem tekur þátt í samþykktarferlinu.|
   |**Kóði sölumanns/innk.aðila**|Tilgreindu kóða sölumanns eða innkaupaaðila sem gildir um notandann.<br /><br /> Yfirleitt er fyllt út í  **salespers./Purch. Kóti**  ef Sölumaður eða innkaupaaðili sem er ábyrgur fyrir viðskiptavini eða lánardrottin er einnig einstaklingurinn sem verður að samþykkja sölu-eða innkaupabeiðni.|
   |**Notandakenni samþykkjanda**|Veljið NOTANDAKENNI einstaklingsins sem á að samþykkja beiðnir gerðar af einstaklingnum sem var tilgreindur í  **reitnum notandakenni** .|
   |**Takmörk samþykktar á sölu**|Tilgreinið hámarks söluupphæð í staðbundnum gjaldmiðli (ISK) sem einstaklingurinn sem valinn er í  **reitnum notandakenni**  getur samþykkt.|
   |**Ótakmörkuð söluheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar sölubeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út  **reitinn samþykkisöluupphæðarmarka** .|
   |**Takmörk samþykktar á innkaupum**|Tilgreindu hámarkssöluupphæð í SGM sem einstaklingurinn í reitnum **Notandakenni** getur samþykkt.|
   |**Ótakmörkuð innkaupaheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar innkaupabeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út  **reitinn samþykktarmörk**  innkaupa.|
   |**Takmörk samþykktar á beiðni**|Tilgreindu hámarksupphæð í SGM sem einstaklingurinn í reitnum **Notandakenni** getur samþykkt fyrir innkaupabeiðnir.<br /><br /> Til að nota þennan reit þarf að velja **Keðja samþykkjenda** valkostinn í **Gerð takmarkana fyrir samþykktaraðila** reitnum á síðunni **Verkflæðissvörun**.|
   |**Ótakmörkuð samþykktarbeiðniheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar innkaupabeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út reitinn samþykkisupphæð samþykktar  **á**  Upphæð beiðninnar.|
   |**Staðgengill**|Veljið notandakenni einstaklingsins sem mun samþykkja beiðnir sem einstaklingurinn hefur auðkennt í  **reitnum notandakenni**  ef notandinn í  **Kenni samþykkis**  er ekki tiltækur. <br /><br />**Athugið:** Staðgengillinn getur annaðhvort verið notandinn í reitnum **Staðgengill**, beini samþykkjandinn eða samþykktarstjórnandi, í þessari forgangsröð. Frekari upplýsingar má finna á [Nota Samþykktarverkflæði](across-how-use-approval-workflows.md).|
   |**Netfang**|Tilgreindu netfang einstaklingsins í reitnum **Notandakenni**.|
   |**Samþykktastjórnandi**|Tilgreinið þann notanda sem hefur heimild til að aflæsa samþykktarverkflæði, t.d. með því að úthluta samþykkisbeiðnum til nýrra staðgengilstilfella eða eyða gjaldföllnum samþykktarbeiðnum.<br /><br />**Ath**  að aðeins einn einstaklingur getur verið samþykkistjórinn.|

3. Til að prófa uppsetningu samþykkts notanda, skal velja aðgerðina **Uppsetning samþykkts notanda**.  
4. Endurtaktu skref 2 til 3 fyrir hvern einstakling sem á að setja upp sem samþykktarnotanda.  

Næsta skref er að tilgreina hvernig  [!INCLUDE [prod_short](includes/prod_short.md)]  eigi að tilkynna fólki að beiðni sé í bið að þeirra athygli. Frekari upplýsingar um  [uppsetningu verkflæðistilkynninga](across-setting-up-workflow-notifications.md).

## Sjá einnig .

[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
