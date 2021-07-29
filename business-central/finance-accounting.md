---
title: Upplifun endurskoðanda í Business Central
description: Kynnið ykkur hlutverkamiðstöð endurskoðanda og fyrirtækjamiðstöðina sem styður innri og ytri endurskoðendur í fyrirtæki viðskiptavinar.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8e988e0b23f29f4b9969a9682eac2e2e91a30fcc
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442801"
---
# <a name="accountant-experiences-in-prod_long"></a>Endurskoðandi upplifun í [!INCLUDE[prod_long](includes/prod_long.md)]

Öll fyrirtæki verða að færa bókhald og staðfesta endurskoðunina. Sum fyrirtæki ráða endurskoðanda utan frá og önnur eru með endurskoðanda á launaskrá hjá sér. Engu skiptir hvernig endurskoðandi þú ert, þú getur nýtt þér **Endurskoðandi** Mitt hlutverk sem þitt Heim í [!INCLUDE[prod_short](includes/prod_short.md)]. Héðan hefurðu aðgang að öllum síðum sem þú þarft í vinnunni.  

## <a name="accountant-role-center"></a>Endurskoðandi Mitt hlutverk

Mitt hlutverk er yfirlit með aðgerðarreitum sem sýna þér lykiltölur í rauntíma og veita þér skjótan aðgang að gögnum. Á borðanum efst á síðunni færðu aðgang að fleiri aðgerðum, eins og að opna þær fjárhagsskýrslur og yfirlit sem oftast eru notuð í Excel. Efst uppi á yfirlitsstikunni er hægt að skipt hratt á milli listanna sem þú notar oftast. Hér sérðu önnur svæði eins og **Bókuð fylgiskjöl** með mismunandi tegundum fylgiskjala sem fyrirtækið hefur bókað.  

Ef þú þekkir ekki til [!INCLUDE[prod_short](includes/prod_short.md)], geturðu opnað myndbandalista frá Mitt hlutverk. Einnig er hægt að opna **Hafist handa** kynningu sem bendir á lykilsvæði.  

## <a name="company-hub"></a>Fyrirtækjamiðstöð

Ef unnið er í mörgum [!INCLUDE [prod_short](includes/prod_short.md)] fyrirtækjum gæti það hentað þér að nota síðuna **Fyrirtækjamiðstöð** til að fylgjast með vinnu.  Frekari upplýsingar er að finna í [Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-prod_short"></a><a name="inviteaccountant"></a>Bjóða ytri endurskoðanda í þitt [!INCLUDE[prod_short](includes/prod_short.md)]

Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, getur kerfisstjórinn þinn boðið þeim í þitt [!INCLUDE[prod_short](includes/prod_short.md)] svo þeir geti unnið með þín fjárhagsgögn. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur þrjú leyfi af gerðinni External Accountant. Nánari upplýsingar um leyfi er að finna í [Microsoft Dynamics 365 Business Central leyfishandbók](https://go.microsoft.com/fwlink/?LinkId=871590).

Þegar endurskoðandi hefur fengið aðgang að þínu [!INCLUDE[prod_short](includes/prod_short.md)], getur hann notað **Endurskoðandi** Mitt hlutverk, sem veitir auðveldan aðgang að þeim síðum sem vinna þarf með. Hann getur einnig notað fyrirtækjamiðstöðina í eigin [!INCLUDE [prod_short](includes/prod_short.md)] til að stjórna vinnu sinni. Frekari upplýsingar er að finna í [Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Við höfum auðveldað þér að bjóða ytri endurskoðanda. Einfaldlega opnið síðuna **Notendur** og veljið síðan **Bjóða ytri endurskoðanda** aðgerðina í borðanum. Tölvupósturinn er tilbúinn fyrir þig, bættu vinnunetfangi endurskoðandans inn og sendu boðið.  

> [!Note]  
> SMTP tölvupósts verður að vera uppsettur. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Netfang endurskoðanda verður að vera vinnunetfang sem byggist á Azure Active Directory. Ef endurskoðandinn notar aðra gerð netfangs er ekki hægt að sena boðið.
>
> Þetta verk þarfnast aðgang til að stjórna notendum og leyfum í Azure Active Directory. Notandinn sem sendir þetta boð verður að vera með hlutverkið **Altækur stjórnandi** eða **Notandastjórnandi** í Microsoft 365 stjórnendamiðstöð. Frekari upplýsingar er að finna í [Um stjórnandahlutverk](/microsoft-365/admin/add-users/about-admin-roles) í stjórnandaefni Microsoft 365.  

### <a name="adding-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Endurskoðanda þínum er bætt við Microsoft 365 í gegnum Azure-gátt

Ef stjórnandi þinn eða endursöluaðili vill ekki nota leiðarvísinn **Bjóða ytri endurskoðanda** geta þeir bætt við ytri notanda í Azure-gáttinni og úthlutað þessum notanda heimild *Ytri endurskoðanda*. Frekari upplýsingar er að finna í [Stutt leiðbeining: Bæta gestanotendum við skráasafnið þitt í Azure-gáttinni](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Til að bæta endurskoðandanum sem gestanotanda

1. Opnið [Azure gáttina](https://portal.azure.com/).
2. Veljið **Azure Active Directory** í vinstra svæðinu.
3. Undir **Stjórna** skal velja **Notendur**.
4. Veljið **Nýr gestanotandi**.
5. Á síðunni **Nýr notandi** skal velja **Bjóða notanda** og bæta svo við upplýsingum um ytri endurskoðandann.  

   Einnig er hægt að bjóða endurskoðandann velkominn með skilaboðum til að láta hann vita að verið sé að bæta honum við [!INCLUDE[prod_short](includes/prod_short.md)].

6. Veljið **Bjóða** til að senda boðið sjálfkrafa. Tilkynning birtist efst til hægri með skilaboðunum **Tókst að bjóða notanda**. 
7. Eftir að boð hefur verið sent er notandareikningi sjálfkrafa bætt við skráasafnið sem gestur.

Næst verður að úthluta nýja gestanotandanum leyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-give-your-accountant-access-to-your-prod_short"></a>Að gefa endurskoðandanum aðgang að [!INCLUDE[prod_short](includes/prod_short.md)]

1. Í Azure-gáttinni, í notanda sem var nýlega bætt við, skal velja **Forstilling** og síðan velja **Breyta**
2. Uppfærið reitinn **Notkunarstaðsetning** í viðeigandi land og veljið síðan **Vista**.
3. Veljið **Leyfi** og opnið síðan **Úthlutanir**.
4. Veljið leyfið **Dynamics 365 Business Central Ytri endurskoðandi**.  
    
    Ef þetta leyfi er ekki í boði skal leita aðstoðar hjá endursöluaðila til að bæta leyfi við áskriftina.

    Fyrir mat er í prufuleigjanda er hægt að nota **Dynamics 365 Business Central fyrir IWs** leyfið í staðinn. Hins vegar er ekki hægt að nota þessa gerð leyfis ef [!INCLUDE[prod_short](includes/prod_short.md)] hefur verið keypt. 
5. Vistið verkefnið.

Ef það tekst er leyfinu úthlutað til gestanotanda og gestareikningur er búinn til.

### <a name="importing-the-new-user-into-prod_short"></a>Nýr notandi fluttur inn í [!INCLUDE[prod_short](includes/prod_short.md)]

Endurskoðandinn fær tölvupóst þar sem honum er tilkynnt að hann hafi fengið aðgang að Active Directory. Næst verður að veita þeim aðgang að rétta fyrirtækinu í [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Að bæta endurskoðandanum við rétt fyrirtæki

1. Opnið [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtækið sem gefa á endurskoðandanum aðgang að á [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Notendur** og veldu síðan tengda tengilinn.  
3. Veldu **Fá nýja notendur úr Microsoft 365** aðgerðina.

Þetta flytur notandareikninginn sem var búinn til í Azure-gáttinni inn í fyrirtækið. Frekari upplýsingar eru í [Að bæta við notanda í Business Central](ui-how-users-permissions.md#adduser).  

Ef á að veita aðgang að mörgum fyrirtækjum þarf að skrá sig inn í hvert fyrirtæki fyrir sig og endurtaka þetta ferli. Að öðrum kosti er hægt að uppfæra heimildaflokka fyrir notandaforstillingu endurskoðandans í [!INCLUDE[prod_short](includes/prod_short.md)], svo sem með því að úthluta þeim *D365 Bus Premium* notendaflokki. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Unnið með víddir](finance-dimensions.md)  
[Greina fjárhagsskýrslur í Excel](finance-analyze-excel.md)  
[Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Setja upp sjóðstreymisgreiningu](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]