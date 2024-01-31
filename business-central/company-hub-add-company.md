---
title: Bæta fyrirtækjum við fyrirtækjamiðstöðina
description: Kynnið ykkur hvernig bæta má fyrirtækjum úr öðru umhverfi Business Central við fyrirtækjamiðstöðina svo hægt sé að stjórna vinnu í mörgum umhverfum.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, company hub'
ms.search.form: '1151, 1155, 1166, 1165'
ms.date: 09/28/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Bæta fyrirtækjum við fyrirtækjamiðstöðina

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Með fyrirtækjamiðstöðinni er hægt að fá nálgast vinnuna í gegnum mörg fyrirtæki í mörgum [!INCLUDE [prod_short](includes/prod_short.md)]-umhverfum. Hægt er að bæta umhverfi og fyrirtækjum við handvirkt, ef fyrirtækin birtast ekki sjálfkrafa í fyrirtækjamiðstöðinni.  

Á lendingarsíðu fyrirtækjamiðstöðvar finnur þú valmyndina **Uppsetning** þaðan sem hægt er að opna síðuna **Umhverfistenglar**. Veljið **Nýtt** og fyllið svo inn í viðeigandi svæði. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

> [!NOTE]
> Hægt er að tengja fyrirtækjamiðstöð við eins mörg fyrirtæki og þörf krefur. Hins vegar er aðeins hægt að tengja fyrirtækjamiðstöð við fyrirtæki sem eru hýst á [!INCLUDE [prod_short](includes/prod_short.md)] á netinu.

## Umhverfistenglar

Tengilll á umhverfi er spjald þar sem tilgreint er [!INCLUDE [prod_short](includes/prod_short.md)]-umhverfi sem hýsir eitt eða fleiri fyrirtæki sem notandi starfar í. Gögnin á spjaldi hvers umhverfis fyrir sig eru tilgreind af þér og þú getur breytt þeim að vild. Aftur á móti er reiturinn **Tengill umhverfis** mikilvægur - þannig færð þú aðgang að hverju fyrirtæki fyrir sig í [!INCLUDE [prod_short](includes/prod_short.md)]. Notið aðgerðina **Prófa tenginguna** á borðanum til að sannreyna hvort réttur tengill hafi verið sleginn inn. Tengillinn sem þú verður að færa stig á umhverfi sem hýsir fyrirtækið sem þú ert að bæta við og það verður að fela  Microsoft Entra  auðkenni, eða lénsheiti fyrirtækis þíns. Ef þeir hafa til dæmis tilgreint aðsetur á borð við MyBusiness.com, þá er tengillinn á [!INCLUDE [prod_short](includes/prod_short.md)] þeirra ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Annars mun hann líta einhvern veginn svona út: ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```  

Tengillinn er notaður þegar fyrirtækið er valið í fyrirtækjamiðstöðinni.  

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Aðgerðir fyrir fyrirtæki sem er skráð í fyrirtækjamiðstöðinni.":::

> [!TIP]
> Ef unnið er í ókeypis prufuútgáfunni af [!INCLUDE [prod_short](includes/prod_short.md)], er auðvelt að bæta fyrirtækjum við í leigjandanum. Tengilinn umhverfi er að finna með því að afrita KENNIÐ í  Microsoft Entra  úr  **úrræðaleitarhlutanum**  á hjálp & stuðningssíðu. Heiti umhverfis er líklega sjálfgefið gildi, FRAMLEIÐSLA. Bætið þessum upplýsingum við **Tengil umhverfis**, t.d. ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```, og veljið svo **Prófa tenginguna**. Tilraunafyrirtækinu verður bætt við listann.
>
> Ef þú hefur verið farið yfir í þrjátíu daga tilraunafyrirtæki, Fyrirtækið mitt, geturðu bætt því við listann með því að velja aðgerðina **Endurhlaða / Endurhlaða öllum fyrirtækjum** í listanum.

## Hlaða fyrirtæki

Þegar umhverfunum hefur verið bætt við birtast fyrirtækin sjálfkrafa. Hins vegar ef vitað er að nýju fyrirtæki hefur verið bætt við umhverfi er hægt að velja aðgerðina **Endurhlaða öllum fyrirtækjum** til að endurhlaða listanum. Notið sömu aðgerðina til að endurhlaða gögnum frá öllum fyrirtækjunum.  

> [!TIP]
> Til að uppfæra gögnin í fyrirtækjamiðstöðinni þarf að hafa aðgang að gögnum í fyrirtækjunum sem gögnin koma frá.

## Sjá einnig .

[Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md)  
[Tilföng fyrir Hjálp og notendaþjónustu](product-help-and-support.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
