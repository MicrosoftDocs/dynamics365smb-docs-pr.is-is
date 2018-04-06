---
title: "Hvernig á að setja upp notendur sem samþykkjendur | Microsoft Docs"
description: "Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Í Uppsetning fyrir samþykki notanda glugganum er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 98dab9ee1d3b6d717d6d7d999785080225592ee3
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-approval-users"></a>Setja upp notendur samþykktar
Áður en hægt er að stofna verkflæði sem fela í sér samþykktarskref verður að setja upp verkflæðisnotendur sem taka þátt í samþykktarferli. Í **Uppsetning fyrir samþykki notanda** glugganum er einnig hægt að stilla takmörk upphæðar fyrir tilteknar gerðir beiðna og skilgreina staðgengilssamþykkjendur sem samþykktarbeiðnir eru sendar til þegar upphaflegur samþykkjandi er fjarverandi.  

> [!NOTE]  
>  Notendur sem samþykkja, bæði samþykkjendur beiðni og samþykkjendur, verða að vera settir upp sem notendur verkflæðis í **Verkflæði notandahópur** glugganum. Frekari upplýsingar eru í [Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md).  

 Þegar notendur samþykkis hafa verið settir upp er hægt að nota uppsetninguna til að stofna verkflæðisviðbrögð fyrir samþykktarverkflæði. Frekari upplýsingar eru í skrefi 9 í [Stofna verkflæði](across-how-to-create-workflows.md).  

> [!NOTE]  
>  Til að skilgreina að samþykktarbeiðni sé ekki samþykkt fyrr en margar samþykkjendur í samþykktarkeðju hafa samþykkt skal setja upp samþykkjendur í stigveldi. Hvað varðar samþykkjendur af gerðinni **Samþykkjandi** skal setja þá upp í glugganum **Uppsetning Samþykkjandi notandi**. Hvað varðar samþykkjendur af gerðinni **Notendaflokkur verkflæðis** skal setja þá upp í glugganum **Notendaflokkar verkflæðis** og skilgreina stigveldið með því að úthluta stighækkandi númerum á hvern samþykkjanda í reitnum **röð nr.**. . Frekari upplýsingar eru í þessu efnisatirði og [Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md).  
>   
>  Til að skilgreina að samþykktarbeiðni sé ekki samþykkt fyrr en margar jafn samþykkjendur hafa samþykkt, án tillits til stigveldi, skal setja upp flatan notendahóp verkflæðis. Hvað varðar samþykkjendur af gerðinni **Notendaflokkur verkflæðis** skal setja þá upp í glugganum **Notendaflokkar verkflæðis** og úthluta sama númeri á hvern samþykkjanda í reitnum **Röð nr.**. . Frekari upplýsingar eru í [Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Uppsetning samþykkts notanda  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning samþykkts notanda** og velja svo viðeigandi tengil.  
2. Í glugganum **Samþykkjandi notandauppsetning** þarf að búa til nýja línu og fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kenni notanda**|Velja skal notandakenni notanda sem tekur þátt í samþykktarferlinu.|  
    |**Kóði sölumanns/innk.aðila**|Tilgreina skal sölumann eða kaupanda kóða sem gildir um notandann í **Sölum./Innk. kóði** reitnum.<br /><br /> Vanalega er reiturinn **Sölum./Innk. kóði** fylltur út ef sölumaður eða kaupandi sem er ábyrgur fyrir viðskiptamanninum eða lánardrottni er einnig aðilinn sem þarf að samþykkja sölu eða innkaupabeiðinina.|  
    |**Notandakenni samþykkjanda**|Velja notandakenni notanda sem verður að samþykkja beiðnir sem gerðar eru af notandanum í reitnum **Notandakenni**.|  
    |**Takmörk samþykktar á sölu**|Tilgreina hámarkssöluupphæð í SGM sem notandi í **Notandakenni** reitnum getur samþykkt.|  
    |**Ótakmörkuð söluheimild**|Tilgreina að notandi í **Notandakenni** reitnum getur samþykkt allar sölubeiðnir saman hver upphæð þeirra er.<br /><br /> Sé þessi gátreitur valinn er ekki hægt að fylla út **Samþykktarmörk söluupphæðar** reitinn.|  
    |**Takmörk samþykktar á innkaupum**|Tilgreina hámarkssöluupphæð í SGM sem notandi í **Notandakenni** reitnum getur samþykkt.|  
    |**Ótakmörkuð innkaupaheimild**|Tilgreina að notandi í **Notandakenni** reitnum getur samþykkt allar sölubeiðnir saman hver upphæð þeirra er.<br /><br /> Sé þessi gátreitur valinn er ekki hægt að fylla út **Samþykktarmörk söluupphæðar** reitinn.|  
    |**Takmörk samþykktar á beiðni**|Tilgreina hámarksupphæð í SGM sem notandi í **Notandakenni** reitnum getur samþykkt fyrir innkaupabeiðni.<br /><br /> Til að nota þennan reit þarf að velja **Keðja samþykkjenda** valkostinn í **Gerð takmarkana fyrir samþykktaraðila** reitnum í **Verkflæðissvörun** glugganum.|  
    |**Ótakmörkuð beiðniheimild**|Tilgreina að notandi í **Notandakenni** reitnum getur samþykkt öll kauptilboð saman hver upphæð þeirra er.<br /><br /> Sé þessi gátreitur valinn er ekki hægt að fylla út **samþykktarmörk pantanaupphæðar** reitinn.|  
    |**Staðgengill**|Velja notandakenni notanda sem verður að samþykkja beiðnir sem gerðar eru af notandanum í reitnum **Notandakenni** ef notandinn í **Samþykktaraðilakenni** reitnum er ekki laus. **Athugið:** Staðgengillinn getur annaðhvort verið notandinn í reitnum **Staðgengill**, beini samþykkjandinn eða samþykktarstjórnandi, í þessari forgangsröð. Frekari upplýsingar eru í [Nota verkflæði samþykktar](across-how-use-approval-workflows.md).|  
    |**Netfang**|Tilgreina netfang notanda í **Notandakenni** reitnum.|  
    |**Samþykktastjórnandi**|Tilgreina notandann sem hefur rétt til að opna fyrir samþykktarverkflæði, t.d. með því að úthluta samþykktarbeiðnum á nýja samþykkjendur og eyða samþykktarbeiðnum sem hafa fallið á tíma.|  

    > [!NOTE]  
    >  Hegðun reitsins **Gerð takmarkana fyrir samþykktaraðila** á aðeins við um þá kerfishluta sem leyfa skilgreiningu marka, það er samþykktir sölu og kaupa. Allar aðrar gerðir af samþykki þar sem mörk eru ekki skilgreind munu alltaf haga sér eins og lýst er fyrir **Beinn samþykktaraðili** valmöguleikann.  

3. Til að prófa uppsetningu samþykkts notanda, skal velja aðgerðina **Uppsetning samþykkts notanda**.  
4. Endurtaka skal þrep 2 til 3 fyrir hvern notanda sem á að stofna sem notanda samþykkis.  

## <a name="see-also"></a>Sjá einnig  
[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)   
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)   
[Búa til verkflæði](across-how-to-create-workflows.md)   
[Uppsetning verkflæðis](across-set-up-workflows.md)   
[Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Verkflæði](across-workflow.md)   

