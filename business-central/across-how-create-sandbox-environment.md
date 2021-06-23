---
title: Búa til sandkassaumhverfi
description: Stofna umhverfi þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa úr Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: a76ae33815b8e9368f45b72fd8703bfc47cbd079
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215629"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Búa til sandkassaumhverfi í [!INCLUDE[prod_short](includes/prod_short.md)]

Með [!INCLUDE[prod_short](includes/prod_short.md)] geturðu auðveldlega búið til öruggt hverfi þar sem hægt er að prófa, þjálfa eða leysa úr málum án þess að það trufli verkferla eða viðskiptagögn fyrirtækisins. Slíkt umhverfi sem ekki er hægt að framleiða í er kallað *sandkassi*. Sandkassaumhverfi er staðurinn, ótengdur framleiðslu, þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa þjónustuna í öruggu umhverfi án þess að eiga á hættu að hafa áhrif á gögnin eða stillingarnar í framleiðsluumhverfi þínu.  

Kerfisstjórinn þinn stjórnar sandkassaumhverfi í [Stjórnandamiðstöð](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), en ef þú vilt prófa eitthvað á fljótlegan hátt geturðu búið til sandkassaumhverfi úr [!INCLUDE[prod_short](includes/prod_short.md)]. Að því loknu geturðu fjarlægt sandkassann með því að nota stjórnstöðina.  

> [!NOTE]
> Tæknilega séð eru sandkassaumhverfi mjög frábrugðin framleiðsluumhverfi, jafnvel þótt stjórnandi búi til sandkassa sem inniheldur framleiðslugögn. Til dæmis er ekki hægt að nota sandkassa fyrir viðmið og ekki er hægt að biðja um útflutning á gagnagrunni. Ef þú vilt búa til sandkassa sem viðmið getur stjórnandi þinn búið til sérhæft umhverfi í stjórnunarmiðstöðinni. Frekari upplýsingar eru í [Framleiðslu-og sandkassaumhverfi](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Til að búa til sandkassaumhverfi í [!INCLUDE[prod_short](includes/prod_short.md)]

1. Skráðu þig inn í þitt framleiðslutilvik af [!INCLUDE[prod_short](includes/prod_short.md)].

2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sandkassaumhverfi** og veldu síðan tengda tengilinn.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Veldu hnappinn **Stofna**.  

    Annar flipi með [!INCLUDE[prod_short](includes/prod_short.md)] opnast svo hægt sé að ljúka uppsetningu á sandkassaumhverfi.

    > [!NOTE]  
    >  Ef þú ert með sprettigluggavörn virka í vafranum, skaltu breyta henni þannig að vefslóðir frá *.businesscentral.dynamics.com aðsetrinu verði leyfðar.

Þegar sandkassaumhverfið er tilbúið, verður þér beint inn á leiðsagnarforrit sandkassaumhverfisins.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Þú getur valið hnappinn **Frekari upplýsingar** til að lesa um þróunardæmi sem hægt er að prófa í sandkassaumhverfinu eða veldu hnappinn **Loka** til að halda áfram í Mínu hlutverki í [!INCLUDE[prod_short](includes/prod_short.md)] sandkassatilvikinu þínu.

Efst í Hlutverkamiðstöðinni birtist tilkynning til að upplýsa þig um að þetta sé sandkassaumhverfi. Einnig er hægt að sjá um hvaða gerð af umhverfi er að ræða í titilstiku biðlarans.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Sandkassaumhverfi sem er búið til á þennan hátt inniheldur aðeins sjálfgefin sýnigögn fyrir fyrirtækið CRONUS. Engin gögn eru afrituð eða yfirhöfuð flutt frá framleiðsluumhverfinu.
>
> Einnig er hægt að búa til sandkassaumhverfi byggt á framleiðslugögnum. Þetta þarf að gera í gegnum stjórnendamiðstöðina. Frekari upplýsingar eru í [Stjórnun umhverfa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) í þróunar- og stjórnunarefni.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Stjórnandi eða annar notandi getur að takmarkað eða jafnvel hindrað aðganga sumra notenda að sandkassaumhverfinu. Þetta er hægt að gera með því að nota staðlaða öryggiseiginleika vörunnar, eins og t.d. Notandakort, Notendaflokkar og Heimildasamstæður. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Ítarleg virkni í sandkassaumhverfinu

Sandkassaumhverfið er ekki síst gagnlegt vegna þess að það felur í sér nokkra handhæga eiginleika:

* [Ítarleg notendaupplifun](#advanced-user-experience)  
* [Ljúka sýnigögnum](#complete-sample-data)  
* [Hönnuður](#designer)  

### <a name="advanced-user-experience"></a>Ítarleg notendaupplifun

Mögulegt er að virkja og prófa fulla virkni af staðalútgáfu [!INCLUDE[prod_short](includes/prod_short.md)] í sandkassa leigjanda með því að stilla svæðið **Upplifun** á síðunni **Upplýsingar um fyrirtæki** á *Premium*. Leitaðu að síðunni **Upplýsingar um fyrirtæki** á valmynd :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Stillingartáknsins":::.  

Eftir að þú hefur opnað fyrir notendaupplifunina *Premium*, færðu aðgang að öllum stöðluðu forstillingunum (hlutverkum) og Mitt hlutverk í stöðluðu útgáfunni. Einnig er hægt að stofna matsfyrirtæki sem er að fullu uppsett, með sýnigögnum og aðgangi að ítarlegri svæðum vörunnar. Að öðrum kosti er hægt að hafa samskipti við endursöluaðila til að fá sýniútgáfu af þeim eiginleikum. Nánari upplýsingar er að finna í [Hvernig finn ég endursöluaðila?](/dynamics365/business-central/across-faq.yml#findpartner).  

### <a name="complete-sample-data"></a>Ljúka sýnigögnum

Ef þú þarft frekari sýnigögn skaltu ræða við endursöluaðila þinn.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Til að stofna fyrirtæki með fullkláruð sýnigögn í sandkassa

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fyrirtæki** og veldu síðan tengda tengilinn.  
2. Veldu aðgerðina **Nýtt** og síðan **Stofna nýtt fyrirtæki**.  
3. Á síðunni **Uppsetningarleiðbeiningar fyrir fyrirtæki** skaltu smella á **Áfram**.  
4. Tilgreinið heiti fyrir nýja fyrirtækið og síðan á svæðinu **Veldu gögn og uppsetningu til að hefjast handa** veljið **Ítarlegt mat - Heildarsýnigögn**.  
5. Ljúkið við leiðbeiningar um uppsetningu með hjálp.  

Þegar leiðbeiningum um uppsetningu með hjálp er lokið er hægt að fletta í gegnum nýja fyrirtækið með öllum sýnigögnunum. Nánari upplýsingar eru í [Stofna ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Hönnuður

Í sandkassaumhverfi er kveikt á **Hönnuður**. Hægt er að virkja Hönnuð með því að velja hönnunartáknið ![Hönnuður](./media/across-sandbox/sandbox-inclient-design-icon.png) á síðu eða með því að velja **Hanna** valmyndaratriðið í stillingavalmyndinni ![Stillingar](media/ui-experience/settings_icon_small.png).  

Frekari upplýsingar er að finna í [Notkun hönnuðar](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) í efni hönnuðar og stjórnanda (aðeins á ensku).  

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Sjá einnig

[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Prufuútgáfa og áskrift](across-preview.md)  
[Stjórnun umhverfis í stjórnunarmiðstöð Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
