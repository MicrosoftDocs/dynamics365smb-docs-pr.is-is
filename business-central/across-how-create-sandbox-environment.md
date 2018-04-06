---
title: Stofna sandkassaumhverfi| Microsoft Docs
description: "Stofna umhverfi þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8451e456d03c9429ff2e04f4e0664ae240f872c2
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="create-a-sandbox-environment"></a>Búa til sandkassaumhverfi
Sandkassaumhverfi (Forskoðun) er tilvik af [!INCLUDE[d365fin](includes/d365fin_md.md)] ótengt framleiðslu. Sandkassaumhverfi er staðurinn, ótengdur framleiðslu, þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa þjónustuna í öruggu umhverfi án þess að eiga á hættu að hafa áhrif á gögnin eða stillingarnar í framleiðsluumhverfi þínu.

## <a name="to-create-a-sandbox-environment"></a>Búa til sandkassaumhverfi
Notandi verður að hafa áskrift að [!INCLUDE[d365fin](includes/d365fin_md.md)] til að geta búið til sandkassaumhverfi. Aðeins er eitt sandkassaumhverfi í boði fyrir hverja áskrift.

1. Skráðu þig inn í þitt framleiðslutilvik af [!INCLUDE[d365fin](includes/d365fin_md.md)] þjónustunni.
2. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sandkassaumhverfi** og velja svo viðeigandi tengil.
![Sandkassaumhverfi Uppsetning](./media/across-sandbox/sandbox-environment-setup.png)
3. Velja **Stofna**.  
  Annar flipi í vafranum mun opnast til að hægt sé að ljúka uppsetningunni á sandakassaumhverfinu.
> [!NOTE]  
>  Ef þú ert með sprettiglugga-lokara virkan í vafranum, skaltu breyta honum þannig að vefslóðir frá *.financials.dynamics.com aðsetrinu verði leyfðar.   

4. Þegar sandkassaumhverfið er tilbúið, verður þér beint inn á leiðsagnarforrit sandkassaumhverfisins.
![Sandkassi Velkomin(n) Leiðsagnarforrit](./media/across-sandbox/sandbox-wizard.png)

5. Veldu **Læra meira** til að lesa um dæmi sem hægt er að prófa í sandkassaumhverfinu. Eða veldu **Loka** til að halda áfram í Hlutverkamiðstöð í [!INCLUDE[d365fin](includes/d365fin_md.md)] sandkassatilvikinu þínu.
6. Efst í Hlutverkamiðstöðinni birtist tilkynning til að upplýsa þig um að þetta sé sandkassaumhverfi. Einnig er hægt að sjá um hvaða gerð af umhverfi er að ræða í titilstiku biðlarans.
![Sandkassi Hlutverkamiðstöð Tilkynning](./media/across-sandbox/sandbox-rolecenter-notification.png)  
Búinn hefur verið til glænýr leigjandi í sandkassaumhverfinu. Þessi leigjandi er uppfullur af sjálfgefnum sýnigögnum fyrir CRONUS fyrirtækið. Engin gögn eru afrituð eða yfirhöfuð flutt frá framleiðsluumhverfinu á meðan stofnun sandkassans stendur.
7.  Alltaf er hægt að fara til baka á **Sandkassaumhverfi** síðuna og endurstilla sandkassaumhverfið.
> [!NOTE]  
>  Endurstilling sandkassaumhverfisins mun eyða því algerlega og síðan stofna það á ný með sjálfgefnum sýnigögnum.  

8.  Notaðu Business Central gangsetjara smáforrita til að skipta á milli framleiðslu- og sandkassaumhverfisins.
![Sandkassi  Dynamics365 Valmynd](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Það mögulegt fyrir stjórnanda eða annan notanda að takmarka eða jafnvel hindra aðganga sumra notenda að sandkassaumhverfinu. Þetta er hægt að gera með því að nota staðlaða öryggiseiginleika vörunnar, eins og t.d. Notandakort, Notendaflokkar og Heimildasamstæður.

![Heimildasamstæður sandkassa](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Ítarleg virkni í sandkassaumhverfinu
### <a name="the-in-client-designer"></a>Hönnunarviðmót í-biðlara
Í sandkassaumhverfi er í boði eiginleikinn hönnunarviðmót í-biðlara, sem þú getur virkjað með því að velja hönnunartáknið ![Hönnuður](./media/across-sandbox/sandbox-inclient-design-icon.png) á síðu.

![Hönnunarviðmót í-biðlara](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>Gera ítarlega notandaupplifun virka
Mögulegt er að opna fyrir og prófa ítarlega (fulla) virkni [!INCLUDE[d365fin](includes/d365fin_md.md)] í sandkassa leigjanda með því að stilla **Upplifun** reitinn á **Upplýsingar um fyrirtæki** síðunni.

![Sandkassaumhverfi Ítarlegt](./media/across-sandbox/sandbox-advanced.png)

![Sandkassi Framleiðsla](./media/across-sandbox/sandbox-production.png)

Eftir að þú hefur opnað fyrir ítarlega virkni í sandkassi leigjandi, færðu aðgang að öllum stöðluðu forstillingunum og hlutverkamiðstöðvunum. Einnig er hægt að stofna matsfyrirtæki sem er að fullu uppsett, með sýnigögnum og aðgangi að ítarlegri svæðum vörunnar.

![Sandkassi nýtt fyrirtæki](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

