---
title: Setja upp tölvupóstskráningu | Microsoft Docs
description: Kynntu þér hvernig tölvupóstsamskipti milli sölufólks og viðskiptavina geta skapað alvöru sölutækifærum.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 2abc0406fa8e86646d2382a4c7bbb1e228439728
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148409"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða

Fáðu meira út úr samskiptum sölumanna við núverandi eða mögulega viðskiptavini þína með því að rekja tölvupóstsamskipti og breyta þeim síðan í möguleg tækifæri. [!INCLUDE[prod_short](includes/prod_short.md)] getur unnið með Exchange Online til að halda skrá yfir skilaboð á inn- og útleið. Þú getur skoðað og greint innihald skilaboða á síðunni **Samskiptaskráningarfærslur**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Setja upp almenningsmöppur og reglur fyrir tölvupóstsskráningu á Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Næst tengir þú [!INCLUDE[prod_short](includes/prod_short.md)] við Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)] til að skrá tölvupóstskilaboð

Hafist handa með tölvupóstskráningu í tveimur einföldum skrefum:

1. Tengjast [!INCLUDE[prod_short](includes/prod_short.md)] við Exchange Online áskriftina þína Microsoft 365. Exchange Online sér um tölvupóstskilaboðin þín. Við höfum einfaldað þetta skref með því að bjóða upp á uppsetningarleiðbeiningar. Þú þarft bara að hafa kerfisstjóra-skilríkin fyrir kerfisstjóra lykilinn í Microsoft 365. Til að hefja leiðsögnina skaltu opna síðuna **Uppsetning með hjálp** og velja síðan **Setja upp tölvupóstskráningu**.  

2. Gakktu úr skugga um að gild netföng hafi verið slegin inn í [!INCLUDE[prod_short](includes/prod_short.md)] fyrir sölufólk og tengiliði, sem er háð því hvort um sé að ræða mögulega eða núverandi viðskiptavini. Til að gera það fyrir hvern viðskiptavin eða sölumann skal opna spjaldið **Tengiliður** eða **Sölumaður/innkaupaaðili** og kíkja í reitinn **Netfang**.

> [!Tip]
> Eftir að þú hefur lokið skrefum leiðsagnarinnar geturðu athugað hvort tengingin hafi borið árangur. Leitaðu að **Uppsetning markaðssetningar** og veldu **Aðgangur**, síðan **Aðgerðir** og að lokum **Staðfesta uppsetningu tölvupóstskráningar**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Að skoða tölvupóstsamskipti í samskiptaskránni

[!INCLUDE[prod_short](includes/prod_short.md)] býr til færslu á síðunni **Samskiptaskrá** í hvert skipti sem sölumaður og tengiliður skiptast á tölvupóstskilaboðum. Til að skoða samskiptaskrána skaltu opna spjaldið **Tengiliður** fyrir einstaklinginn og velja síðan **Tengt**, **Ferill** og að lokum velja **Samskiptaskráningarfærslur**. Við getum gert nokkra hluti við hverja færslu í skránni, til dæmis:

- Skoðaðu innihald tölvupóstsins sem var sendur á milli með því að velja **Vinna** og svo **Sýna viðhengi**.
- Breyttu tölvupóstsamskiptum í sölutækifæri - Þú getur skapað tækifæri úr færslu sem lofar góðu og náð sölu út úr henni. Þetta er gert með því að velja færsluna og velja síðan **Vinna** og síðan **Búa til tækifæri**. Nánari upplýsingar er að finna í [Umsjón sölutækifæra](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Að tengja útgáfur á staðnum við Microsoft Exchange

Hægt er að tengja [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss við Exchange innanhúss eða Exchange Online fyrir tölvupóstsskráningu. Fyrir báðar útgáfur af Exchange eru stillingar fyrir tenginguna í boði á síðunni **Uppsetning markaðssetningar**. Fyrir Exchange Online er einnig hægt að nota uppsetningarleiðbeiningar með hjálp.

### <a name="connecting-to-exchange-on-premises"></a>Að tengjast við Exchange innanhúss

Til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss við Exchange innanhúss er hægt á síðunni **Uppsetning markaðssetningar** að nota **Grunnútfærsla** sem **Sannvottunargerð** og síðan slá inn innskráningarupplýsingar fyrir notandareikninginn fyrir Exchange innanhúss. Því næst skal kveikja á **Virkja** til að hefja skráningu á tölvupósti.

### <a name="connecting-to-exchange-online"></a>Tengist við Exchange Online

Til að tengjast við Exchange Online þarf að nota **OAuth2** sem **Sannvottunargerð**. Einnig þarf að skrá forrit í Azure Active Directory og gefa upp auðkenni forrits, leynilykil lyklageymslu og framsendingarslóð sem á að nota. Framsend vefslóð er fyllt út fyrirfram og ætti að virka fyrir flestar uppsetningar. Frekari upplýsingar eru í Til að skrá forrit í Azure AD fyrir tengingu úr Business Central í Exchange Online.

Nauðsynlegt er að setja upp uppsetninguna til að nota HTTPS. Frekari upplýsingar er að finna í [Skilgreining SSL til að tryggja örugga tengingu vefbiðlara Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Ef verið er að setja upp þjóninn til að hafa aðra heimasíðu er hægt að breyta vefslóðinni. Leynilykill biðlara verða vistaður sem dulkóðaður strengur í gagnagrunninum.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Til að skrá forrit í Azure AD fyrir tengingu úr Business Central í Exchange Online

Eftirfarandi skref gera ráð fyrir að nota Azure Active Directory til að stjórna auðkennum og aðgangsheimild. Frekari upplýsingar er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app). Ef ekki er notað Azure Active Directory skal skoða [Að nota aðra stýringarþjónustu auðkennis og aðgangsheimildar](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

1. Í Azure-gáttinni, undir **Stjórna**, skal velja **Sannvottun**.
2. Undir **Framsendingarvefslóð** skal bæta við framsendingarvefslóðinni sem mælt er með á síðunni **Uppsetning markaðssetningar** í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef framsendingarslóðin á uppsetningarsíðu markaðssetningar er tóm skal finna ráðlagða framsendingarslóð á síðunni **Uppsetning tölvupóstsskráningar með hjálp**.

    > [!NOTE]
    > Ef framsendingarslóðin er ekki tilgreind er hægt að gera það seinna með því að velja **Bæta við verkvangi** og síðan velja **Vef** til að bæta við vefforritinu og framsendingarvefslóðinni. 

3. Undir **Stjórna** skal velja **Skrá**.
4. Finnið eiginleikann **requiredResourceAccess** í skránni og bætið við eftirfarandi kóða innan hornklofanna ([]) til að bæta við áskildum heimildum. Frekari upplýsingar er að finna í [Skrá forritið](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Velja **Vista**.
6. Undir **Stjórna** skal velja **API-heimildir** og síðan ganga úr skugga um að eftirfarandi heimildir komi fram:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Undir **Stjórna** skal velja **Vottorð og leynilyklar** og síðan stofna nýjan leynilykil fyrir forritið. Leynilykillinn verður notaður annaðhvort í [!INCLUDE[prod_short](includes/prod_short.md)], í reitnum **Leynilykill biðlara** á síðunni **Uppsetning markaðssetningar** eða geymdur í öruggri geymslu og hann látinn í té í áskriftartilviki.
8. Veljið **Yfirlit** og finnið svo gildið **Auðkenni forrits (biðlara)**. Þetta er biðlarakenni forritsins. Færa verður það inn annaðhvort á síðunni **Uppsetning markaðssetningar** í reitnum **Biðlarakenni** eða geyma það í öruggri geymslu og láta það í té í áskriftartilviki.
9. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal setja upp tölvupóstsskráningu á síðunni **Uppsetning markaðssetningar** eða nota leiðbeininguna **Uppsetning tölvupóstsskráningar með hjálp** til að fá aðstoð við ferlið.
    * Gefið upp tölvupóstsreikning notandans fyrir hönd þess sem áætlað verk mun tengjast við Exchange Online og vinna úr tölvupósti. Notandinn verður að hafa gilt leyfi fyrir Exchange Online.
    * Gefðu upp vefslóðina fyrir Exchange Online. Yfirleitt er þetta lénið sem tilgreint var í netfangi notandans.
    * Gefið upp **Slóð biðraðarmöppu** og **Slóð geymslumöppu**.
10. Kveikið á **Virkja** til að hefja skráningu á tölvupósti.
11. Skráðu þig inn með stjórnandareikningnum fyrir Azure Active Directory (þessi reikningur verður að hafa gilt leyfi fyrir Exchange og má vera stjórnandi í Exchange Online þínu). Eftir að þú skráir þig inn verður þú beðinn um að leyfa skráða forritinu þínu að skrá sig inn í Exchange Online fyrir hönd fyrirtækisins. Veita þarf samþykki til að ljúka uppsetningunni.

   > [!NOTE]
   > Ef ekki er beðið um innskráningu með stjórnandareikningnum er það líklega vegna þess að lokað er fyrir sprettiglugga. Til að skrá þig inn skaltu leyfa sprettiglugga úr https://login.microsoftonline.com.

### <a name="using-another-identity-and-access-management-service"></a>Að nota annað auðkenni og fá aðgang að stýringarþjónustu
Ef þú ert ekki að nota Azure Active Directory til að stjórna auðkennum og aðgangsheimild Þarftu aðstoð frá þróunaraðila. Ef þú kýst frekar að geyma forritskennið og leynilykilinn á annarri staðsetningu, geturðu skilið reiti biðlarakennis og leynilykils biðlara eftir auða og skrifað viðbót til að sækja auðkennið og leynilykilinn frá staðsetningunni. Hægt er að gefa upp leynilykilinn við keyrslu með því að gerast áskrifandi að tilvikum OnGetEmailLoggingClientId og OnGetEmailLoggingClientSecret tilvikum í codeunit 1641 „Uppsetning tölvupóstskráningar“.

### <a name="to-stop-logging-email"></a>Að hætta að skrá tölvupóst
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning markaðssetningar** og velja síðan viðkomandi tengil.
2. Slökkva skal á víxlhnappnum **Virkjað**.

## <a name="see-also"></a>Sjá einnig
[Stjórnun tengsla](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]