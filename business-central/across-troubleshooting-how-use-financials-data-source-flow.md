---
title: "Úrræðaleit samþættingar við Microsoft Flow | Microsoft Docs"
description: "Notandi getur leitað úrræða um það hvernig hann getur gert Financials-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 60ce05760251da39280eb8a4884cb80586c2ab62
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Úrræðaleit samþættingar við Microsoft Flow - Umbeðin slóð of löng
Notandi getur notað [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín sem hluta af verkflæði í Microsoft Flow.  

> [!NOTE]  
>   Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Flæði.  

Ef verið er að búa til Microsoft Flow með [!INCLUDE[d365fin](includes/d365fin_md.md)] tengi kunna að birtast villuboð um að umbeðna slóðin sé of löng eftir að flæðið hefur verið búið til, á borð við: **RequestUriTooLong**.

## <a name="cause"></a>Stofnar
Til að flæði fari af stað leitar það að breytingum í gögnum. Við ákvörðun á því hvort gögn hafi breyst ber tengið saman gögn í skyndiminni við ný gögn sem beðið er um frá uppruna.  

Ef gagnafyrirspurnin býr til vefslóð sem er of löng mistekst hún. Algengar ástæður kunna að vera:
- Allar upprunatöflur yfir 250 línur
- Upprunatafla inniheldur þúsundir færslna

## <a name="workaround"></a>Hjáleið
Fylgið eftirfarandir skrefum til að leysa vandamálið.
1. Velja að breyta flæði sem mistekst.
2. Víkkið **Sýna ítarlega valkosti** á flæðiskveikjunni.
3. Í reitnum **Sleppa talningu** skal slá inn fjölda færslna sem á að sleppa.  
Ef taflan sem er verið að nota er til dæmis með gagnaveitu sem inniheldur 4.000 færslur skal slá inn 4.000 sem fjöldanns em á að sleppa.
4. Uppfærið flæðið.

> [!NOTE]  
> Tengið er í beta-útgáfu. Uppfærist í það hvernig unnið er úr gagnabreytingum í framtíðarútgáfum.


## <a name="see-also"></a>Sjá einnig
[Notkun [!INCLUDE[d365fin](includes/d365fin_md.md)] í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  

