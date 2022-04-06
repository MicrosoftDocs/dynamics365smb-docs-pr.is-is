---
title: Sandkassaumhverfi
description: Kynntu þér hvernig sérhæft umhverfi getur hjálpað þér að skoða, læra, sýna, þróa, úrræðaleita og prófa Business Central á öruggan hátt.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/20/2021
ms.author: solsen
ms.openlocfilehash: 20637dcced16fe695d64c2b4d858483882c64f7a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518286"
---
# <a name="sandbox-environments-in-prod_short"></a>Sandkassaumhverfi í [!INCLUDE[prod_short](includes/prod_short.md)]

Með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu geturðu auðveldlega náð þér í öruggt umhverfi þar sem hægt er að prófa, þjálfa eða leysa úr málum án þess að það trufli verkferla eða viðskiptagögn fyrirtækisins. Slíkt umhverfi sem ekki er hægt að framleiða í er kallað *sandkassi*. Sandkassaumhverfi er staðurinn, ótengdur framleiðslu, þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa þjónustuna í öruggu umhverfi án þess að eiga á hættu að hafa áhrif á gögnin eða stillingarnar í framleiðsluumhverfi þínu.  

> [!TIP]
> Landaði þú á þessari grein eftir að þú valdir nafnið á umhverfi þínu [!INCLUDE [prod_short](includes/prod_short.md)] í Top Bar? Eins er ekki hægt að breyta nafninu eða umhverfinu sem vegur. Þess í stað þarf að biðja kerfisstjóra um að breyta nafninu eða biðja þá um að samnýta tengilinn í annað umhverfi.

Stjórnandi hefur umsjón með sandkassaumhverfum í [stjórnendamiðstöðinni](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Ef þú vilt til dæmis búa til sandkassa sem viðmið getur stjórnandi þinn búið til sérhæft umhverfi í stjórnendamiðstöðinni. Frekari upplýsingar eru í [Vinnslu- og sandkassaumhverfi](/dynamics365/business-central/dev-itpro/administration/environment-types) í þróunar- og stjórnunarefni.  

Einnig er hægt að nota sandkassa til þjálfunar á öruggan hátt, t.d. til að fylgja námsleið úr [Microsoft Learn](/learn/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs) því það er öruggt umhverfi til að gera tilraunir í. Ef eitthvađ fer úrskeiđis eyđir mađur einfaldlega sandkassanum og byrjar upp á nýtt.  

Að því loknu geturðu fjarlægt sandkassann með því að nota stjórnstöðina.  

> [!NOTE]
> Tæknilega séð eru sandkassaumhverfi mjög frábrugðin vinnsluumhverfum. Stjórnandi þinn getur búið til sandkassa sem inniheldur framleiðslugögn en er samt sandkassi og þú getur til dæmis ekki óskað eftir útflutningi gagnagrunns. Frekari upplýsingar eru í [Sandkassaumhverfum](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments) í þróunar- og stjórnunarefni.

Sandkassaumhverfið er ekki síst gagnlegt vegna þess að það felur í sér nokkra handhæga eiginleika:

* [Ítarleg notendaupplifun](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Hönnuður](#designer)  

## <a name="advanced-user-experience"></a>Ítarleg notendaupplifun

Mögulegt er að virkja og prófa fulla virkni af staðalútgáfu [!INCLUDE[prod_short](includes/prod_short.md)] í sandkassa leigjanda með því að stilla svæðið **Upplifun** á síðunni **Upplýsingar um fyrirtæki** á *Premium*. Leitaðu að síðunni **Upplýsingar um fyrirtæki** í :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Stillingatákninu."::: .  

Eftir að þú hefur opnað fyrir notendaupplifunina *Premium*, færðu aðgang að öllum stöðluðu forstillingunum (hlutverkum) og Mitt hlutverk í stöðluðu útgáfunni. Að öðrum kosti er hægt að hafa samskipti við endursöluaðila til að fá sýniútgáfu af þeim eiginleikum. Nánari upplýsingar er að finna í [Hvernig finn ég endursöluaðila?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Ljúka sýnigögnum

Ef þú þarft frekari sýnigögn skaltu ræða við endursöluaðila þinn.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer"></a>Hönnuður

Í sandkassaumhverfi er kveikt á **Hönnuður**. Hægt er að virkja hönnuðinn með því að velja hönnunartáknið ![Hönnuður.](./media/across-sandbox/sandbox-inclient-design-icon.png) á síðu eða með því að velja **Hanna** valmyndaratriðið í stillingavalmyndinni ![Stillingar](media/ui-experience/settings_icon_small.png).  

Nánari upplýsingar eru [í notkun hönnunar](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) í efni forritara og admin (aðeins á ensku).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Sjá einnig

[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Prufuútgáfa og áskrift](across-preview.md)  
[Stjórnun umhverfis í stjórnunarmiðstöð Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Vinnslu- og sandkassaumhverfi](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
