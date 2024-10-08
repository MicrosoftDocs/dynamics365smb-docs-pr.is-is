---
title: Upplifun endurskoðanda í Business Central
description: Kynnið ykkur hlutverkamiðstöð endurskoðanda og fyrirtækjamiðstöðina sem styður innri og ytri endurskoðendur í fyrirtæki viðskiptavinar.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 06/12/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="accountant-experiences-in-"></a>Endurskoðandi upplifir sig í [!INCLUDE[prod_long](includes/prod_long.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Öll fyrirtæki verða að færa bókhald og staðfesta endurskoðunina. Sum fyrirtæki ráða endurskoðanda utan frá og önnur eru með endurskoðanda á launaskrá hjá sér. Í hvaða tegund endurskoðanda þú ert þá er hægt að nota **Mitt hlutverk endurskoðanda** sem heimili notanda [!INCLUDE[prod_short](includes/prod_short.md)]. Héðan hefurðu aðgang að öllum síðum sem þú þarft í vinnunni.  

## <a name="accountant-role-center"></a>Endurskoðandi Mitt hlutverk

Mitt hlutverk er yfirlit með aðgerðarreitum sem sýna þér lykiltölur í rauntíma og veita þér skjótan aðgang að gögnum. Borðinn efst á síðunni veitir aðgang að fleiri aðgerðum. Til dæmis til að opna fjárhagsskýrslur og yfirlit í Excel. Efst uppi á yfirlitsstikunni er hægt að skipt hratt á milli listanna sem þú notar oftast. Hér sjást önnur svæði, svo sem **Bókuð fylgiskjöl** með ýmsum tegundum fylgiskjala sem fyrirtækið bókaði.  

Ef notandi er nýr í er hægt að [!INCLUDE[prod_short](includes/prod_short.md)] opna lista yfir myndbönd beint frá Mitt hlutverk. Einnig er hægt að opna **Hafist handa** kynningu sem bendir á lykilsvæði.  

## <a name="company-hub"></a>Fyrirtækjamiðstöð

Ef unnið er í mörgum [!INCLUDE [prod_short](includes/prod_short.md)] fyrirtækjum gæti það hentað þér að nota síðuna **Fyrirtækjamiðstöð** til að fylgjast með vinnu. Frekari upplýsingar er að finna í [Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-"></a><a name="inviteaccountant"></a>Bjóða ytri endurskoðanda í þitt [!INCLUDE[prod_short](includes/prod_short.md)]

Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, getur kerfisstjórinn þinn boðið þeim í þitt [!INCLUDE[prod_short](includes/prod_short.md)] svo þeir geti unnið með þín fjárhagsgögn. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur þrjú leyfi af gerðinni External Accountant. Nánari upplýsingar um leyfisveitingar fást með því að ná í [Microsoft Dynamics 365 Business Central Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).

Þegar endurskoðandi hefur aðgang að notandanum [!INCLUDE[prod_short](includes/prod_short.md)] geta þeir notað **Mitt hlutverk endurskoðanda** til að fá greiðan aðgang að síðum fyrir vinnu sína. Hann getur einnig notað fyrirtækjamiðstöðina í eigin [!INCLUDE [prod_short](includes/prod_short.md)] til að stjórna vinnu sinni. Frekari upplýsingar er að finna í [Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Auðvelt er að bjóða ytri endurskoðanda. Opna skal síðuna **Notendur** og velja svo aðgerðina **Bjóða ytri endurskoðanda** í borðanum. Tölvupósturinn er tilbúinn fyrir þig, bættu vinnunetfangi endurskoðandans inn og sendu boðið.  

> [!Note]  
> SMTP tölvupósts verður að vera uppsettur. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Netfang endurskoðanda verður að vera vinnuaðsetur sem byggir á Microsoft Entra skilríki. Ef endurskoðandinn notar aðra gerð netfangs er ekki hægt að sena boðið.
>
> Þetta verk krefst aðgangs að stjórnun notenda og leyfis í Microsoft Entra kenni. Notandanum sem sendir fundarboðið verður að vera úthlutað að minnsta kosti [hlutverki notandastjóra](/entra/identity/role-based-access-control/permissions-reference#user-administrator) í Microsoft 365 stjórnunarmiðstöðinni. Frekari upplýsingar eru í [Um stjórnandahlutverk](/microsoft-365/admin/add-users/about-admin-roles) í Microsoft 365 efni kerfisstjóra.  

### <a name="add-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Bæta endurskoðandanum þínum Microsoft 365 í Azure-gáttina

Ef kerfisstjóri eða endurseljandi vill ekki nota **leiðarvísinn Bjóða ytri endurskoðanda** getur hann bætt við ytri notanda í Azure-gáttinni og úthlutað þessum notanda *ytri endurskoðanda* leyfi. Frekari upplýsingar er að finna í [Stutt leiðbeining: Bæta gestanotendum við skráasafnið þitt í Azure-gáttinni](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Til að bæta endurskoðandanum sem gestanotanda

1. Opnið [Azure gáttina](https://portal.azure.com/).
2. Á vinstri svæðinu skal velja **Microsoft Entra kenni**.
3. Undir **Stjórna** skal velja **Notendur**.
4. Veljið **Nýr gestanotandi**.
5. Á síðunni **Nýr notandi** skal velja **Bjóða notanda** og bæta svo við upplýsingum um ytri endurskoðandann.  

   Valfrjálst skal innihalda persónuleg móttökuskilaboð til endurskoðenda til að láta þá vita að þú bætir þeim við þig [!INCLUDE[prod_short](includes/prod_short.md)].

6. Veljið **Bjóða** til að senda boðið sjálfkrafa. Tilkynning birtist efst til hægri með skilaboðunum **Tókst að bjóða notanda**. 
7. Eftir að boð hefur verið sent er notandareikningi sjálfkrafa bætt við skráasafnið sem gestur.

Næst verður að úthluta nýja gestanotandanum leyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-give-your-accountant-access-to-your-"></a>Að gefa endurskoðandanum aðgang að [!INCLUDE[prod_short](includes/prod_short.md)]

1. Í Azure-gáttinni, í notanda sem var nýlega bætt við, skal velja **Forstilling** og síðan velja **Breyta**
2. Reiturinn **Notkunarstaður** er uppfærður í viðeigandi land/svæði og Vista **valið**.
3. Veljið **Leyfi** og opnið síðan **Úthlutanir**.
4. Veljið leyfið **Dynamics 365 Business Central Ytri endurskoðandi**.  
    
    Ef þetta leyfi er ekki tiltækt skal hafa samband við söluaðila til að bæta leyfinu við áskriftina.

    Fyrir mat er í prufuleigjanda er hægt að nota **Dynamics 365 Business Central fyrir IWs** leyfið í staðinn. Hins vegar er ekki hægt að nota þessa tegund leyfis ef þú hefur þegar keypt [!INCLUDE[prod_short](includes/prod_short.md)]. 
5. Vistið verkefnið.

Ef það tekst er leyfinu úthlutað til gestanotanda og gestareikningur er búinn til.

### <a name="import-the-new-user-into-"></a>Flytja nýja notandann inn í [!INCLUDE[prod_short](includes/prod_short.md)]

Endurskoðandi fær tölvupóst sem tilkynnir þeim að hann hafi aðgang að skilyrðum þínum Microsoft Entra . Næst verður að veita þeim aðgang að rétta fyrirtækinu í [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Að bæta endurskoðandanum við rétt fyrirtæki

1. Opnið [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtækið sem gefa á endurskoðandanum aðgang að á [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Notendur** og veldu síðan tengda tengilinn.  
3. Veldu **Fá nýja notendur úr Microsoft 365** aðgerðina.

Þessi aðgerð flytur inn notandareikninginn sem stofnaður var í Azure-gáttinni yfir í fyrirtækið. Frekari upplýsingar eru í [Að bæta við notanda í Business Central](ui-how-users-permissions.md#adduser).  

Ef á að veita aðgang að mörgum fyrirtækjum þarf að skrá sig inn í hvert fyrirtæki fyrir sig og endurtaka þetta ferli. Að öðrum kosti er hægt að uppfæra heimildaflokka fyrir notandaforstillingu endurskoðandans í [!INCLUDE[prod_short](includes/prod_short.md)], svo sem með því að úthluta þeim *D365 Bus Premium* notendaflokki. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

## <a name="see-also"></a>Sjá einnig .

[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Vinna með víddir](finance-dimensions.md)  
[Greina fjárhagsskýrslur í Excel](finance-analyze-excel.md)  
[Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Setja upp sjóðstreymisgreiningu](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
