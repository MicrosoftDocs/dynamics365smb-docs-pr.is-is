---
title: Setja upp notendur samþykktar
description: Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendurna sem taka þátt í samþykktarferlunum.
author: brentholtorf
ms.topic: how-to
ms.devlang: al
ms.search.form: '663,'
ms.date: 05/31/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-approval-users"></a>Setja upp notendur samþykktar

Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp notendurna sem taka þátt í samþykktarferlum á síðunni **Notandauppsetning samþykktar** . Einnig er hægt að setja takmarkanir á upphæðir fyrir mismunandi gerðir beiðna, skilgreina staðgengilssamþykkjendur og setja upp tilkynningar.  

Þegar notendur samþykktar hafa verið settir upp er hægt að stofna verkflæðissvar fyrir samþykktarverkflæði. Frekari upplýsingar má finna á [Stofna verkflæði samþykktars](across-how-to-create-workflows.md).  

> [!TIP]
> Hægt er að krefjast þess að margir samþykkjendur bregði sér í samþykktarbeiðni með því að stofna flokk samþykkjenda á síðunni **Notendaflokkur** verkflæðis. Nánari upplýsingar um [uppsetningu notendahópa verkflæðis](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Uppsetning samþykkts notanda

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning samþykktarnotanda**, velja síðan viðkomandi tengil.  
2. Á síðunni **Samþykkjandi notandauppsetning** þarf að búa til nýja línu og fylla reitina út eins og lýst er í eftirfarandi töflu.  

   |Svæði|Lýsing|
   |-----|-----------|
   |**Kenni notanda**|Velja skal notandakenni þess sem tekur þátt í samþykktarferlinu.|
   |**Kóði sölumanns/innk.aðila**|Tilgreindu kóða sölumanns eða innkaupaaðila sem gildir um notandann.<br /><br /> Fylla þarf út reitinn **Sölumenn/Innk.aðilar. Reiturinn Kóti** ef sölumaðurinn eða innkaupaaðili sem ber ábyrgð á viðskiptamanni eða lánardrottni er einnig sá sem verður að samþykkja sölu- eða innkaupabeiðni.|
   |**Notandakenni samþykkjanda**|Velja notandakenni þess sem þarf að samþykkja beiðnir frá einstaklingnum sem tilgreindur er í reitnum **Notandakenni** .|
   |**Takmörk samþykktar á sölu**|Tilgreina hámarksupphæð sölu í staðarmynt (SGM) sem einstaklingurinn sem valinn er í reitnum **Kenni notanda** getur samþykkt.|
   |**Ótakmörkuð söluheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar sölubeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út reitinn **Samþykktarmörk** söluupphæðar.|
   |**Takmörk samþykktar á innkaupum**|Tilgreindu hámarkssöluupphæð í SGM sem einstaklingurinn í reitnum **Notandakenni** getur samþykkt.|
   |**Ótakmörkuð innkaupaheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar innkaupabeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út reitinn **Samþykktarmörk** innkaupaupphæðar.|
   |**Takmörk samþykktar á beiðni**|Tilgreindu hámarksupphæð í SGM sem einstaklingurinn í reitnum **Notandakenni** getur samþykkt fyrir innkaupabeiðnir.<br /><br /> Til að nota þennan reit þarf að velja **Keðja samþykkjenda** valkostinn í **Gerð takmarkana fyrir samþykktaraðila** reitnum á síðunni **Verkflæðissvörun**.|
   |**Ótakmörkuð samþykktarbeiðniheimild**|Tilgreindu að einstaklingurinn í reitnum **Notandakenni** geti samþykkt allar innkaupabeiðnir sama hver upphæðin er.<br /><br /> Ef þessi gátreitur er valinn er ekki hægt að fylla út reitinn **Samþykktarmörk** beiðniupphæðar.|
   |**Staðgengill**|Velja skal notandakenni þess sem samþykkir **beiðnir sem einstaklingurinn tilgreinir í reitnum** Notandakenni **ef notandinn í** kenni samþykkjanda er ekki tiltækur. <br /><br />**Athugið:** Staðgengillinn getur annaðhvort verið notandinn í reitnum **Staðgengill**, beini samþykkjandinn eða samþykktarstjórnandi, í þessari forgangsröð. Frekari upplýsingar má finna á [Nota Samþykktarverkflæði](across-how-use-approval-workflows.md).|
   |**Netfang**|Tilgreindu netfang einstaklingsins í reitnum **Notandakenni**.|
   |**Samþykktastjórnandi**|Tilgreina notandann sem hefur heimild til að opna samþykktarverkflæði, t.d. með því að dreifa samþykktarbeiðnum til nýrra staðgengilssamþykkjenda eða eyða samþykktarbeiðnum sem komnar eru fram yfir tíma.<br /><br />**Aðeins** einn einstaklingur getur verið samþykktarstjóri.|

3. Til að prófa uppsetningu samþykkts notanda, skal velja aðgerðina **Uppsetning samþykkts notanda**.  
4. Endurtaktu skref 2 til 3 fyrir hvern einstakling sem á að setja upp sem samþykktarnotanda.  

Næsta skref er að tilgreina hvernig [!INCLUDE [prod_short](includes/prod_short.md)] eigi að tilkynna fólki að beiðni bíði athygli þeirra. Nánari [upplýsingar um uppsetningu verkflæðistilkynninga](across-setting-up-workflow-notifications.md).

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  
[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
