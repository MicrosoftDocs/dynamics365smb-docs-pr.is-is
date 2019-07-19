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
ms.date: 06/26/2019
ms.author: solsen
ms.openlocfilehash: 217310522d7e54eeaa9dbd50df4ff89b0d68517d
ms.sourcegitcommit: 5b6dd8d881c0eb65ece6936a94dfda3185574335
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711084"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Búa til sandkassaumhverfi
Sandkassaumhverfi (Forskoðun) er tilvik af [!INCLUDE[d365fin](includes/d365fin_md.md)] ótengt framleiðslu. Sandkassaumhverfi er staðurinn, ótengdur framleiðslu, þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa þjónustuna í öruggu umhverfi án þess að eiga á hættu að hafa áhrif á gögnin eða stillingarnar í framleiðsluumhverfi þínu.

## <a name="to-create-a-sandbox-environment"></a>Búa til sandkassaumhverfi
Notandi verður að hafa áskrift að [!INCLUDE[d365fin](includes/d365fin_md.md)] til að geta búið til sandkassaumhverfi. Aðeins er eitt sandkassaumhverfi í boði fyrir hverja áskrift.

1. Skráðu þig inn í þitt framleiðslutilvik af [!INCLUDE[d365fin](includes/d365fin_md.md)] þjónustunni.

2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sandkassaumhverfi** og veldu síðan tengda tengilinn.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Veldu hnappinn **Stofna**.  

    Annar flipi með [!INCLUDE[d365fin](includes/d365fin_md.md)] opnast svo hægt sé að ljúka uppsetningu á sandkassaumhverfi.

    > [!NOTE]  
    >  Ef þú ert með sprettigluggavörn virka í vafranum, skaltu breyta henni þannig að vefslóðir frá *.businesscentral.dynamics.com aðsetrinu verði leyfðar.

4. Þegar sandkassaumhverfið er tilbúið, verður þér beint inn á leiðsagnarforrit sandkassaumhverfisins.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Veldu hnappinn **Frekari upplýsingar** til að lesa um dæmi sem hægt er að prófa í sandkassaumhverfinu eða veldu hnappinn **Loka** til að halda áfram í Mínu hlutverki í [!INCLUDE[d365fin](includes/d365fin_md.md)] sandkassatilvikinu þínu.

    Efst í Hlutverkamiðstöðinni birtist tilkynning til að upplýsa þig um að þetta sé sandkassaumhverfi. Einnig er hægt að sjá um hvaða gerð af umhverfi er að ræða í titilstiku biðlarans.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

    > [!NOTE]
    > Sandkassaumhverfi sem er búið til á þennan hátt inniheldur aðeins sjálfgefin sýnigögn fyrir fyrirtækið CRONUS. Engin gögn eru afrituð eða yfirhöfuð flutt frá framleiðsluumhverfinu.<br /><br />
    > Einnig er hægt að búa til sandkassaumhverfi sem inniheldur framleiðslugögnin. Þetta þarf að gera í gegnum stjórnendamiðstöðina. Frekari upplýsingar eru í [Stjórnun umhverfa](/business-central/dev-itpro/administration/tenant-admin-center-environments) í þróunar- og IT-pro hjálpinni.

6. Alltaf er hægt að fara til baka á **Sandkassaumhverfi** síðuna og endurstilla sandkassaumhverfið.
    > [!NOTE]  
    >  Endurstilling sandkassaumhverfisins mun eyða því algerlega og síðan stofna það á ný með sjálfgefnum sýnigögnum.  

7. Notaðu Business Central gangsetjara smáforrita til að skipta á milli framleiðslu- og sandkassaumhverfisins.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

8. Það mögulegt fyrir stjórnanda eða annan notanda að takmarka eða jafnvel hindra aðganga sumra notenda að sandkassaumhverfinu. Þetta er hægt að gera með því að nota staðlaða öryggiseiginleika vörunnar, eins og t.d. Notandakort, Notendaflokkar og Heimildasamstæður.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Ítarleg virkni í sandkassaumhverfinu
### <a name="designer"></a>Hönnuður
Í sandkassaumhverfi er kveikt á **Hönnuður**, sem hægt er að virkja með því að velja hönnunartáknið ![Hönnuður](./media/across-sandbox/sandbox-inclient-design-icon.png) á síðu.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Gera ítarlega notandaupplifun virka
Mögulegt er að opna fyrir og prófa ítarlega (fulla) virkni [!INCLUDE[d365fin](includes/d365fin_md.md)] í sandkassa leigjanda með því að stilla **Upplifun** reitinn á **Upplýsingar um fyrirtæki** síðunni.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Eftir að þú hefur opnað fyrir ítarlega virkni í sandkassi leigjandi, færðu aðgang að öllum stöðluðu forstillingunum og hlutverkamiðstöðvunum. Einnig er hægt að stofna matsfyrirtæki sem er að fullu uppsett, með sýnigögnum og aðgangi að ítarlegri svæðum vörunnar.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
