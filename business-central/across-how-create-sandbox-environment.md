---
title: Stofna sandkassaumhverfi| Microsoft Docs
description: Stofna umhverfi þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 04/01/2020
ms.author: solsen
ms.openlocfilehash: 59b659ca458e6cfe7c13ef5094dbbf80a144c369
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188565"
---
# <a name="creating-a-sandbox-environment-in-prodshort"></a>Búa til sandkassaumhverfi í [!INCLUDE [prodshort](includes/prodshort.md)]

Með [!INCLUDE [prodshort](includes/prodshort.md)] geturðu auðveldlega búið til öruggt hverfi þar sem hægt er að prófa, þjálfa eða leysa úr málum án þess að það trufli verkferla eða viðskiptagögn fyrirtækisins. Slíkt umhverfi sem ekki er hægt að framleiða í er kallað *sandkassi*. Sandkassaumhverfi er staðurinn, ótengdur framleiðslu, þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa þjónustuna í öruggu umhverfi án þess að eiga á hættu að hafa áhrif á gögnin eða stillingarnar í framleiðsluumhverfi þínu.  

Kerfisstjórinn þinn getur búið til sandkassaumhverfi í [Stjórnandamiðstöð](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), en ef þú vilt prófa eitthvað á fljótlegan hátt geturðu búið til sandkassaumhverfi úr [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Tæknilega séð eru sandkassaumhverfi mjög frábrugðin framleiðsluumhverfi, jafnvel þótt stjórnandi búi til sandkassa sem inniheldur framleiðslugögn. Til dæmis er ekki hægt að nota sandkassa fyrir viðmið og ekki er hægt að biðja um útflutning á gagnagrunni. Ef þú vilt búa til sandkassa sem viðmið getur stjórnandi þinn búið til sérhæft framleiðsluumhverfi í stjórnunarmiðstöðinni. Frekari upplýsingar er að finna á [Gerðir umhverfis](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-prodshort"></a>Til að búa til sandkassaumhverfi í [!INCLUDE [prodshort](includes/prodshort.md)]

1. Skráðu þig inn í þitt framleiðslutilvik af [!INCLUDE[d365fin](includes/d365fin_md.md)].

2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sandkassaumhverfi** og veldu síðan tengda tengilinn.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Veldu hnappinn **Stofna**.  

    Annar flipi með [!INCLUDE[d365fin](includes/d365fin_md.md)] opnast svo hægt sé að ljúka uppsetningu á sandkassaumhverfi.

    > [!NOTE]  
    >  Ef þú ert með sprettigluggavörn virka í vafranum, skaltu breyta henni þannig að vefslóðir frá *.businesscentral.dynamics.com aðsetrinu verði leyfðar.

Þegar sandkassaumhverfið er tilbúið, verður þér beint inn á leiðsagnarforrit sandkassaumhverfisins.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Þú getur valið hnappinn **Frekari upplýsingar** til að lesa um þróunardæmi sem hægt er að prófa í sandkassaumhverfinu eða veldu hnappinn **Loka** til að halda áfram í Mínu hlutverki í [!INCLUDE[d365fin](includes/d365fin_md.md)] sandkassatilvikinu þínu.

Efst í Hlutverkamiðstöðinni birtist tilkynning til að upplýsa þig um að þetta sé sandkassaumhverfi. Einnig er hægt að sjá um hvaða gerð af umhverfi er að ræða í titilstiku biðlarans.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Sandkassaumhverfi sem er búið til á þennan hátt inniheldur aðeins sjálfgefin sýnigögn fyrir fyrirtækið CRONUS. Engin gögn eru afrituð eða yfirhöfuð flutt frá framleiðsluumhverfinu.<br /><br />
> Einnig er hægt að búa til sandkassaumhverfi sem inniheldur framleiðslugögnin. Þetta þarf að gera í gegnum stjórnendamiðstöðina. Frekari upplýsingar eru í [Stjórnun umhverfa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) í þróunar- og IT-pro hjálpinni.

Alltaf er hægt að fara til baka á **Sandkassaumhverfi** síðuna og endurstilla sandkassaumhverfið.

> [!NOTE]  
> Endurstilling sandkassaumhverfisins mun eyða því algerlega og síðan stofna það á ný með sjálfgefnum sýnigögnum.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Stjórnandi eða annar notandi getur að takmarkað eða jafnvel hindrað aðganga sumra notenda að sandkassaumhverfinu. Þetta er hægt að gera með því að nota staðlaða öryggiseiginleika vörunnar, eins og t.d. Notandakort, Notendaflokkar og Heimildasamstæður. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Ítarleg virkni í sandkassaumhverfinu

Sandkassaumhverfið er ekki síst gagnlegt vegna þess að það felur í sér nokkra handhægan eiginleika.

### <a name="designer"></a>Hönnuður

Í sandkassaumhverfi er kveikt á **Hönnuður**. Hægt er að virkja Hönnuð með því að velja hönnunartáknið ![Hönnuður](./media/across-sandbox/sandbox-inclient-design-icon.png) á síðu eða með því að velja **Hanna** valmyndaratriðið í stillingavalmyndinni ![Stillingar](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Gera ítarlega notandaupplifun virka
Mögulegt er að opna fyrir og prófa fulla virkni af staðalútgáfu [!INCLUDE[d365fin](includes/d365fin_md.md)] í sandkassa leigjanda með því að stilla **Upplifun** reitinn á **Upplýsingar um fyrirtæki** síðunni.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Eftir að þú hefur opnað fyrir notendaupplifunina *Premium*, færðu aðgang að öllum stöðluðu forstillingunum (hlutverkum) og Mitt hlutverk í stöðluðu útgáfunni. Einnig er hægt að stofna matsfyrirtæki sem er að fullu uppsett, með sýnigögnum og aðgangi að ítarlegri svæðum vörunnar. Að öðrum kosti er hægt að hafa samskipti við endursöluaðila til að fá sýniútgáfu af þeim eiginleikum. Nánari upplýsingar er að finna í [Hvernig finn ég endursöluaðila?](across-faq.md#findpartner).  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a>Sjá einnig

[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Prufuútgáfa og áskrift](across-preview.md)  
[Stjórnun umhverfis í stjórnunarmiðstöð Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
