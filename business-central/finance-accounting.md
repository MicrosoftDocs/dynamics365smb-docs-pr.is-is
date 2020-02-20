---
title: Upplifun Business Central endurskoðanda | Microsoft Docs
description: Kynntu þér Endurskoðandagáttina fyrir Business Central og Mitt hlutverk endurskoðandi sem styður við innri og ytri endurskoðandann í fyrirtæki viðskiptamanns.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 01/06/2020
ms.author: edupont
ms.openlocfilehash: 50cc4aba9f3a01b9518d974cf011de3b9b20a4da
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991857"
---
# <a name="accountant-experiences-in-d365fin_long"></a>Endurskoðandi upplifun í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Öll fyrirtæki verða að færa bókhald og staðfesta endurskoðunina. Sum fyrirtæki ráða endurskoðanda utan frá og önnur eru með endurskoðanda á launaskrá hjá sér. Engu skiptir hvernig endurskoðandi þú ert, þú getur nýtt þér **Endurskoðandi** Mitt hlutverk sem þitt Heim í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Héðan hefurðu aðgang að öllum síðum sem þú þarft í vinnunni.  

## <a name="accountant-role-center"></a>Endurskoðandi Mitt hlutverk
Mitt hlutverk er yfirlit með aðgerðarreitum sem sýna þér lykiltölur í rauntíma og veita þér skjótan aðgang að gögnum. Á borðanum efst á síðunni færðu aðgang að fleiri aðgerðum, eins og að opna þær fjárhagsskýrslur og yfirlit sem oftast eru notuð í Excel. Efst uppi á yfirlitsstikunni er hægt að skipt hratt á milli listanna sem þú notar oftast. Hér sérðu önnur svæði eins og **Bókuð fylgiskjöl** með mismunandi tegundum fylgiskjala sem fyrirtækið hefur bókað.  

Ef þú þekkir ekki til [!INCLUDE[d365fin](includes/d365fin_md.md)], geturðu opnað myndbandalista frá Mitt hlutverk. Einnig er hægt að opna **Hafist handa** kynningu sem bendir á lykilsvæði.  

## <a name="inviteaccountant"></a>Bjóða ytri endurskoðanda í þitt [!INCLUDE[d365fin](includes/d365fin_md.md)]
Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, getur kerfisstjórinn þinn boðið þeim í þitt [!INCLUDE[d365fin](includes/d365fin_md.md)] svo þeir geti unnið með þín fjárhagsgögn. [!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur þrjú leyfi af gerðinni External Accountant. Nánari upplýsingar um leyfi er að finna í [Microsoft Dynamics 365 Business Central leiðarvísir](https://go.microsoft.com/fwlink/?LinkId=871590).

Þegar endurskoðandi hefur fengið aðgang að þínu [!INCLUDE[d365fin](includes/d365fin_md.md)], getur hann notað **Endurskoðandi** Mitt hlutverk, sem veitir auðveldan aðgang að þeim síðum sem vinna þarf með.  

Við höfum auðveldað þér að bjóða ytri endurskoðanda. Einfaldlega opnið síðuna **Notendur** og veljið síðan **Bjóða ytri endurskoðanda** aðgerðina í borðanum. Tölvupósturinn er tilbúinn fyrir þig, bættu vinnunetfangi endurskoðandans inn og sendu boðið.  

> [!Note]  
> SMTP tölvupósts verður að vera uppsettur. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).   

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Netfang endurskoðanda verður að vera vinnunetfang sem byggist á Azure Active Directory. Ef endurskoðandinn notar aðra gerð netfangs er ekki hægt að sena boðið. 
> 
> Þetta verk krefst aðgangs til að stjórna notendum og leyfum í Azure Active Directory, og notandinn sem sendir þetta boð verður að vera með hlutverkið **Altækur stjórnandi** eða **Notandastjórnandi** í Office 365 stjórnendamiðstöð. Frekari upplýsingar eru í [Um stjórnandahlutverk](/office365/admin/add-users/about-admin-roles) í Office 365 efni kerfisstjóra.  

### <a name="adding-your-accountant-to-your-office-365-via-azure-portal"></a>Endurskoðanda þínum er bætt við Office 365 í gegnum Azure-gátt

Ef stjórnandi þinn eða endursöluaðili vill ekki nota leiðarvísinn **Bjóða ytri endurskoðanda** geta þeir bætt við ytri notanda í Azure-gáttinni og úthlutað þessum notanda ytri heimild endurskoðanda. Frekari upplýsingar er að finna í [Stutt leiðbeining: Bæta gestanotendum við skráasafnið þitt í Azure-gáttinni](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Til að bæta endurskoðandanum sem gestanotanda

1. Opnið [Azure gáttina](https://portal.azure.com/).
2. Veljið **Azure Active Directory** í vinstra svæðinu.
3. Undir **Stjórna** skal velja **Notendur**.
4. Veljið **Nýr gestanotandi**.
5. Á síðunni **Nýr notandi** skal velja **Bjóða notanda** og bæta svo við upplýsingum um ytri endurskoðandann.  

   Einnig er hægt að bjóða endurskoðandann velkominn með skilaboðum til að láta hann vita að verið sé að bæta honum við [!INCLUDE [prodshort](includes/prodshort.md)].

6. Veljið **Bjóða** til að senda boðið sjálfkrafa. Tilkynning birtist efst til hægri með skilaboðunum **Tókst að bjóða notanda**. 
7. Eftir að boð hefur verið sent er notandareikningi sjálfkrafa bætt við skráasafnið sem gestur.

Næst verður að úthluta nýja gestanotandanum leyfi fyrir [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-give-your-accountant-access-to-your-prodshort"></a>Að gefa endurskoðandanum aðgang að [!INCLUDE [prodshort](includes/prodshort.md)]

1. Í Azure-gáttinni, í notanda sem var nýlega bætt við, skal velja **Forstilling** og síðan velja **Breyta**
2. Uppfærið reitinn **Notkunarstaðsetning** í viðeigandi land og veljið síðan **Vista**.
3. Veljið **Leyfi** og opnið síðan **Úthlutanir**.
4. Veljið leyfið **Dynamics 365 Business Central Ytri endurskoðandi**.  

    Ef þetta leyfi er ekki í boði verður að nota aðgengilegt **Dynamics 365 Business Central fyrir IW** leyfi í staðinn.
5. Vistið verkefnið.

Ef það tekst er leyfinu úthlutað til gestanotanda og gestareikningur er búinn til.

### <a name="importing-the-new-user-into-prodshort"></a>Nýr notandi fluttur inn í [!INCLUDE [prodshort](includes/prodshort.md)]

Endurskoðandinn fær tölvupóst þar sem honum er tilkynnt að hann hafi fengið aðgang að Active Directory. Næst verður að veita þeim aðgang að rétta fyrirtækinu í [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Að bæta endurskoðandanum við rétt fyrirtæki

1. Opnið [!INCLUDE [prodshort](includes/prodshort.md)] fyrirtækið sem gefa á endurskoðandanum aðgang að á [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.  
3. Veldu **Fá nýja notendur úr Office 365** aðgerðina.

Þetta flytur notandareikninginn sem var búinn til í Azure-gáttinni inn í fyrirtækið. Frekari upplýsingar eru í [Að bæta við notanda í Business Central](ui-how-users-permissions.md#to-add-a-user-in-business-central).  

Ef á að veita aðgang að mörgum fyrirtækjum þarf að skrá sig inn í hvert fyrirtæki fyrir sig og endurtaka þetta ferli. Að öðrum kosti er hægt að uppfæra heimildaflokka fyrir notandaforstillingu endurskoðandans í [!INCLUDE [prodshort](includes/prodshort.md)], svo sem með því að úthluta þeim *D365 Bus Premium* notendaflokki. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

## <a name="accountant-hub"></a>Accountant Hub

Ef þú ert endurskoðandi með nokkra viðskiptamenn, geturðu notað [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] til að fá betra yfirlit yfir viðskiptamenn þína. Þaðan hefurðu aðgang að sérhverjum leigjanda viðskiptamanna þinna í [!INCLUDE[d365fin](includes/d365fin_md.md)] og getur notað Endurskoðandi Mitt hlutverk eins og lýst er hér að ofan. Nánari upplýsingar er að finna í [Velkomin í [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] er nú í opinberri útgáfu á takmörkuðum fjölda markaða.

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Unnið með víddir](finance-dimensions.md)  
[Greina fjárhagsskýrslur í Excel](finance-analyze-excel.md).  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Setja upp sjóðstreymisgreiningu](finance-setup-cash-flow-analyses.md)  
[Velkomin(n) í [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 - Accountant Hub á Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
