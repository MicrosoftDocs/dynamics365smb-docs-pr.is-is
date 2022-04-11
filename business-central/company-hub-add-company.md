---
title: Bæta fyrirtækjum við fyrirtækjamiðstöðina
description: Kynnið ykkur hvernig bæta má fyrirtækjum úr öðru umhverfi Business Central við fyrirtækjamiðstöðina svo hægt sé að stjórna vinnu í mörgum umhverfum.
author: edupont04
ms.topic: conceptual
ms.search.keywords: accountant, accounting, company hub
ms.search.form: 1151, 1155, 1166, 1165
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c6cc06c45856f1e7c10b1ac82382dae799aef409
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8139808"
---
# <a name="add-companies-to-your-company-hub"></a>Bæta fyrirtækjum við fyrirtækjamiðstöðina

Með fyrirtækjamiðstöðinni er hægt að fá nálgast vinnuna í gegnum mörg fyrirtæki í mörgum [!INCLUDE [prod_short](includes/prod_short.md)]-umhverfum. Hægt er að bæta umhverfi og fyrirtækjum við handvirkt, ef fyrirtækin birtast ekki sjálfkrafa í fyrirtækjamiðstöðinni.  

Á lendingarsíðu fyrirtækjamiðstöðvar finnur þú valmyndina **Uppsetning** þaðan sem hægt er að opna síðuna **Umhverfistenglar**. Veljið **Nýtt** og fyllið svo inn í viðeigandi svæði. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

> [!NOTE]
> Hægt er að tengja fyrirtækjamiðstöð við eins mörg fyrirtæki og þörf krefur. Hins vegar er aðeins hægt að tengja fyrirtækjamiðstöð við fyrirtæki sem eru hýst á [!INCLUDE [prod_short](includes/prod_short.md)] á netinu.

## <a name="environment-links"></a>Umhverfistenglar

Tengilll á umhverfi er spjald þar sem tilgreint er [!INCLUDE [prod_short](includes/prod_short.md)]-umhverfi sem hýsir eitt eða fleiri fyrirtæki sem notandi starfar í. Gögnin á spjaldi hvers umhverfis fyrir sig eru tilgreind af þér og þú getur breytt þeim að vild. Aftur á móti er reiturinn **Tengill umhverfis** mikilvægur - þannig færð þú aðgang að hverju fyrirtæki fyrir sig í [!INCLUDE [prod_short](includes/prod_short.md)]. Notið aðgerðina **Prófa tenginguna** á borðanum til að sannreyna hvort réttur tengill hafi verið sleginn inn. Tengilinn sem þarf að færa inn bendir á umhverfi sem hýsir fyrirtækið sem verið er að bæta við og hann verður að innihalda kennið fyrir Azure Active Directory (Azure AD) eða lénsheiti fyrirtækisins. Ef þeir hafa til dæmis tilgreint aðsetur á borð við MyBusiness.com, þá er tengillinn á [!INCLUDE [prod_short](includes/prod_short.md)] þeirra ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Annars mun hann líta einhvern veginn svona út: ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```  

Tengillinn er notaður þegar fyrirtækið er valið í fyrirtækjamiðstöðinni.  

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Aðgerðir fyrir fyrirtæki sem er skráð í fyrirtækjamiðstöðinni.":::

> [!TIP]
> Ef unnið er í ókeypis prufuútgáfunni af [!INCLUDE [prod_short](includes/prod_short.md)], er auðvelt að bæta fyrirtækjum við í leigjandanum. Hægt er að finna tengil umhverfis með því að afrita Azure Active Directory-kennið úr hlutanum **Úrræðaleit** á síðu hjálpar og notendaþjónustu. Heiti umhverfis er líklega sjálfgefið gildi, FRAMLEIÐSLA. Bætið þessum upplýsingum við **Tengil umhverfis**, t.d. ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```, og veljið svo **Prófa tenginguna**. Tilraunafyrirtækinu verður bætt við listann.
>
> Ef þú hefur verið farið yfir í þrjátíu daga tilraunafyrirtæki, Fyrirtækið mitt, geturðu bætt því við listann með því að velja aðgerðina **Endurhlaða / Endurhlaða öllum fyrirtækjum** í listanum.

## <a name="load-companies"></a>Hlaða fyrirtæki

Þegar umhverfunum hefur verið bætt við birtast fyrirtækin sjálfkrafa. Hins vegar ef vitað er að nýju fyrirtæki hefur verið bætt við umhverfi er hægt að velja aðgerðina **Endurhlaða öllum fyrirtækjum** til að endurhlaða listanum. Notið sömu aðgerðina til að endurhlaða gögnum frá öllum fyrirtækjunum.  

> [!TIP]
> Til að uppfæra gögnin í fyrirtækjamiðstöðinni þarf að hafa aðgang að gögnum í fyrirtækjunum sem gögnin koma frá.

## <a name="see-also"></a>Sjá einnig .

[Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md)  
[Tilföng fyrir Hjálp og notendaþjónustu](product-help-and-support.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]