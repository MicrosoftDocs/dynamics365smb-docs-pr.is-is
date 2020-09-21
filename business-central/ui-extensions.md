---
title: Setja upp viðbætur til að sérstilla Business Central | Microsoft Docs
description: Kynntu þér hvernig skal bæta virkni og sérstilla Business Central með því að setja upp viðbætur.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765922"
---
# <a name="customizing-business-central-using-extensions"></a>Sérstilling Business Central með viðbótum

Þú getur breytt [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að setja viðbætur sem bæta við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis.

> [!NOTE]
> Til að setja upp viðbætur frá AppSource eða bæta við viðbótum fyrir hvern leigjanda fyrir sig eru réttar heimildir nauðsynlegar. Annaðhvort verður þú að vera aðili að notendaflokknum D365 EXTENSION MGMT eða vera með heimildasamstæðu D365 EXTENSION MGMT. Ef þú ert stjórnandi geturðu úthlutað notendaflokkum og heimildum til annarra notenda fyrirtækisins.<br /><br />
Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.

> [!IMPORTANT]  
> Uppfærsla viðbóta á leigjanda og uppsetning AppSource viðbóta er ekki studd í gegnum **Viðbótastjórnun** síðu fyrir uppsetningar á forútgáfu.

Þegar þú fyrst ræsir [!INCLUDE[d365fin](includes/d365fin_md.md)], eru nokkrar viðbætur þegar settar upp fyrir þig. Með tímanum verða fleiri viðbætur tiltækar fyrir þig, og þú getur síðan valið hvort þú viljir nota viðbótina eða ekki.

Til dæmis veitir Microsoft viðbót sem veitir samþættingu við PayPal Payments Standard. Þessi viðbót er uppsett sjálfgefið
En ef önnur viðbót er gerð sem veitir samþættingu við aðra greiðsluþjónusta, geturðu sett inn nýja viðbót og síðan valið hvaða af þessum tveimur þjónustum þú notar.  

Þú stjórnar viðbótum á síðunni **viðbótastjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Einnig er hægt að velja **Leita að síðu eða skýrslu** táknið ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") efst í hægra horninu, slá inn **Viðbætur** og velja svo tengda hlekkinn. Nánari upplýsingar eru í [Uppsetning og fjarlæging viðbóta](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Ef þú telur að þú ættir að hafa aðgang að viðbót en finnur ekki virknina sem í henni felst, skaltu athuga síðuna **Viðbótarstjórnun** - ef viðbótin er ekki skráð þar getur þú sett hana upp eins og lýst er í eftirfarandi kafla.  

> [!NOTE]  
> Nýjar viðbætur eru ekki tiltækar í AppSource strax eftir að við tilkynnum um uppfærslu. Þú getur fylgst með viðbótum á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="see-also"></a>Sjá einnig

[Stækka Dynamics 365 Business Central](about-develop-extensions.md)  
[Microsoft Business Central viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[Virkja greiðslur viðskiptamanna gegnum PayPal](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Setja upp GetAddress.io UK Postal Code viðbótina](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Viðbætur frá öðrum veitum](ui-extensions-other.md)  
[Hafist handa](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
