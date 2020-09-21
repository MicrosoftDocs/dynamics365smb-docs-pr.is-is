---
title: Tengja við Common Data Service | Microsoft Docs
description: Notkun annarra forrita með Business Central um Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/24/2020
ms.author: bholtorf
ms.openlocfilehash: 10a257b60aedfb22066148fd48145779cd6d4a62
ms.sourcegitcommit: ac492bff0c87bf2a23fa93113e7571da9d5094c7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2020
ms.locfileid: "3701993"
---
# <a name="connect-to-common-data-service"></a>Tengjast við Common Data Service

Í þessu efnisatriði er lýst hvernig skal setja upp tengingu milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Yfirleitt stofna fyrirtæki tenginguna til að samþætta og samstilla gögn við annað Dynamics 365 Business-forrit á borð við [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Áður en byrjað er

Áður en tengingin er búin til þarf að koma nokkrum upplýsingum á framfæri:  

* Vefslóðin fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] umhverfið sem á að tengjast við. Ef uppsetningarleiðbeiningin **Uppsetning CDS-tengingar** með hjálp er notuð til að stofna tengingu finnum við umhverfin þín, en þú getur einnig slegið inn vefslóð fyrir annað umhverfi í leigjandanum þínum.  
* Notandanafn og aðgangsorð reiknings sem er með heimildir stjórnanda í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

> [!Note]
> Þessi skref lýsa ferlinu fyrir netútgáfuna af [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Ef verið er að nota Business Central á staðnum og ekki er notaður Azure Active Directory-reikningur til að tengjast [!INCLUDE [cds_long_md](includes/cds_long_md.md)], þarf einnig að tilgreina notandanafn og aðgangsorð notandareiknings fyrir samþættinguna. Þessi reikningur er kallaður reikningur „samþættingarnotanda“. Ef notaður er Azure Active Directory-reikningur er reikningur samþættingarnotanda ekki nauðsynlegur eða sýndur. Samþættingarnotandinn verður settur upp sjálfkrafa og þarf ekki leyfi.

## <a name="set-up-a-connection-to-cds_long_md"></a>Uppsetning á tengingu við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

Fyrir allar auðkennisgerðir aðrar en Office 365-auðkenningu, er sett upp tengingin við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] á síðunni **Uppsetning CDS-tengingar**. Fyrir Office 365 auðkenningu er mælt með að þú notir uppsetningarleiðbeiningar **Uppsetning Common Data Service tengingar** með hjálp. Leiðbeiningarnar auðvelda uppsetningu á tengingu og tilgreina ítarlega eiginleika, t.d. eignarhaldslíkan og upphaflega samstillingu.  

> [!IMPORTANT]
> Við uppsetningu tengingarinnar við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] er stjórnandi beðinn um að gefa upp eftirfarandi heimildir til að skrá Azure-forritið sem heitir [!INCLUDE[d365fin](includes/d365fin_md.md)] samþætting við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * **Aðgangur að [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sem þú** heimild er nauðsynleg svo að [!INCLUDE[d365fin](includes/d365fin_md.md)] geti, fyrir hönd stjórnanda, stofnað sjálfkrafa heimildarlausa, ógagnvirka notendur forritsins [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration, úthlutað öryggishlutverkum til þessa notanda og til að nota [!INCLUDE[d365fin](includes/d365fin_md.md)] CDS-grunnsamþættingarlausn í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Þessi heimild er aðeins notuð einu sinni við uppsetningu á tengingu við [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Fá fullan aðgang að Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** heimild er nauðsynleg til að sjálfkrafa stofna samþættingarforritið [!INCLUDE[d365fin](includes/d365fin_md.md)] svo að notandi geti fengið aðgang að [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnum sem verða samstillt.  
> * **Skráðu þig inn og lestu notandaupplýsingarnar þínar** heimild er nauðsynleg til að staðfesta innskráningu notanda, er í raun með öryggishlutverk kerfisstjóra úthlutað í [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Með því að veita samþykki fyrir hönd fyrirtækis er stjórnandinn að leyfa skráðu Azure-forriti sem heitir [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration to [!INCLUDE[cds_long_md](includes/cds_long_md.md)] að samstilla gögn með því að nota sjálfkrafa stofnaðar innskráningarupplýsingar notanda fyrir forritið [!INCLUDE[d365fin](includes/d365fin_md.md)] Integration.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>Að nota uppsetningarleiðbeiningar Common Data Service-tengingar með hjálp

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning með hjálp** og veldu síðan tengda tengilinn.
2. Veldu **Setja upp Common Data Service-tengingu** til að hefja leiðbeiningar um uppsetningu með hjálp.
3. Fyllið inn reitina eftir þörfum.

### <a name="to-create-or-maintain-the-connection-manually"></a>Að stofna eða vinna með tengingu handvirkt

Eftirfarandi ferli útskýrir hvernig á að setja upp tenginguna handvirkt á síðunni **Uppsetning CDS-tengingar**. Þetta er einnig síðan þar sem stillingum fyrir samþættingu er stjórnað.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning CDS-tengingar** og veldu síðan tengda tengilinn.
2. Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Svæði|Description|
    |-----|-----|
    |**Vefslóð umhverfis**|Ef þú átt umhverfi í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] finnum við þau fyrir þig þegar þú keyrir uppsetningarleiðbeiningarnar. Ef þú vilt tengjast öðru umhverfi í öðrum leigjanda geturðu slegið inn innskráningarupplýsingar stjórnanda fyrir umhverfið og við finnum það fyrir þig. |
    |**Virk**|Byrjaðu að nota samþættinguna. Ef tengingu er ekki komið á núna munu stillingar tengingar vera vistaðar en notendur geta ekki tengst [!INCLUDE[cds_long_md](includes/cds_long_md.md)] gögnum frá [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hægt er að koma aftur þessa síðu og virkja tenginguna seinna.  |

3. Í reitnum **Eignarhaldslíkan** skaltu velja hvort þú viljir að teymiseining í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] eigi nýjar færslur eða einn eða fleiri tilteknir notendur. Ef valið er **Einstaklingur** þarf að tilgreina hvern notanda fyrir sig. Ef valið er **Teymi** birtist sjálfgefna fyrirtækiseiningin BCI_Company í reitnum **Tengd fyrirtækiseining**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?-->
    Færðu inn eftirfarandi ítarlegar stillingar.

    |Svæði|Description|
    |-----|-----|
    |**[!INCLUDE[d365fin](includes/d365fin_md.md)] Notendur verða að varpa í CDS-notendur**|Ef eignarhaldslíkan einstaklings er notað, skal tilgreina hvort [!INCLUDE[d365fin](includes/d365fin_md.md)] notandareikningar verða að hafa samsvarandi notandareikninga í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. **Office 365 Sannvottunarnetfang** fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir notandann verður að vera sama og **Aðalnetfang** fyrir [!INCLUDE[crm_md](includes/crm_md.md)] notandann.<br /><br /> Ef þetta gildi er stillt á **Já**, [!INCLUDE[d365fin](includes/d365fin_md.md)] munu notendur sem ekki hafa samsvarandi [!INCLUDE[crm_md](includes/crm_md.md)] notandareikning ekki geta notað [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættingu í notandaviðmótinu. Aðgangur að [!INCLUDE[crm_md](includes/crm_md.md)] gögnum beint úr [!INCLUDE[d365fin](includes/d365fin_md.md)] er veittur fyrir hönd [!INCLUDE[crm_md](includes/crm_md.md)] notandareikningsins.<br /><br /> Ef þetta gildi er stillt á **Nei**, munu allir [!INCLUDE[d365fin](includes/d365fin_md.md)] notendur geta notað [!INCLUDE[crm_md](includes/crm_md.md)] samþættingu í notandaviðmótinu. Aðgangur að [!INCLUDE[crm_md](includes/crm_md.md)] gögnum er veittur fyrir hönd notanda [!INCLUDE[crm_md](includes/crm_md.md)]-tengingar (samþættingar).|
    |**Núverandi sölumaður Business Central er varpað í notanda**|Gefur til kynna hvort notandareikningurinn þinn sé varpað í reikning í [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field-->|

4. Til að prófa stillingar tengingar skal velja **Tenging** og síðan **Prófa tengingu**.  

    > [!NOTE]  
    > Ef dulritun gagna er ekki virkjuð í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður spurt hvort þú viljir virkja hana. Til að virkja dulritun gagna skal velja **Já** og gefa nauðsynlegar upplýsingar. Annars skal velja **Nei**. Hægt er að virkja dulritun gagna seinna. Nánari upplýsingar eru í [Gögn dulrituð í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) í hjálp þróunaraðila og stjórnenda.  

5. Ef [!INCLUDE[cds_long_md](includes/cds_long_md.md)] samstilling er ekki þegar sett upp verður spurt hvort nota eigi sjálfgefna samstillingaruppsetningu. Velja skal **Já** eða **Nei** á grunni þess hvort halda eigi færslum samræmdum í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="show-me-the-process"></a>Sýna mér ferlið

Eftirfarandi myndband sýnir skrefin til að tengja [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

## <a name="connecting-on-premises-versions"></a>Að tengja útgáfur á staðnum

Til að tengja [!INCLUDE[d365fin](includes/d365fin_md.md)] á staðnum við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] þarf að gefa upp upplýsingar á síðunni **Common Data Service Uppsetning tengingar**.

Ef ætlunin er að tengjast með Azure Active Directory (Azure AD) reikningi þarf að skrá forrit í Azure AD og gefa upp auðkenni forritsins, leynilykil lyklageymslu og framsendingarslóðina sem á að nota. Framsend vefslóð er fyllt út fyrirfram og ætti að virka fyrir flestar uppsetningar. Nauðsynlegt er að setja upp uppsetninguna til að nota HTTPS. Frekari upplýsingar er að finna í [Skilgreining SSL til að tryggja örugga tengingu vefbiðlara Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Ef verið er að setja upp þjóninn til að hafa aðra heimasíðu er alltaf hægt að breyta vefslóðinni. Leynilykill biðlara verða vistaður sem dulkóðaður strengur í gagnagrunninum.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Til að skrá forrit í Azure AD fyrir tengingu úr Business Central í Common Data Service

Eftirfarandi skref gera ráð fyrir að nota Azure AD til að stjórna auðkennum og aðgangsheimild. Frekari upplýsingar um skráningu forrits í Azure AD er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app). Ef ekki er notað Azure AD skal skoða [Að nota aðra stýringarþjónustu auðkennis og aðgangsheimildar](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. Í Azure-gáttinni, undir **Stjórna** á yfirlitssvæðinu, skal velja **Sannvottun**.  
2. Undir **Framsenda vefslóðir** skal bæta við framsendingarvefslóð sem mælt er með á síðunni **Common Data Service Uppsetning tengingar** í [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. Undir **Stjórna** skal velja **API-heimildir**.
4. Undir **Skilgreindar heimildir** skal velja **Bæta við heimild** og síðan bæta við úthlutuðum heimildum í flipanum **Microsoft API** á eftirfarandi hátt:
    * Fyrir Business Central skal bæta við heimildunum **Financials.ReadWrite.All**.
    * Fyrir Dynamics CRM skal bæta við heimildunum **user_impersonation**.  

    > [!NOTE]
    > Heiti Dynamics CRM API gæti breyst.

5. Undir **Stjórna** skal velja **Vottorð og leynilyklar** og síðan stofna nýjan leynilykil fyrir forritið. Leynilykillinn verður notaður annaðhvort í [!INCLUDE[d365fin](includes/d365fin_md.md)], í reitnum **Leynilykill biðlara** á síðunni **Common Data Service Uppsetning tengingar** eða geymdur í öruggri geymslu og hann látinn í té í áskriftartilviki eins og lýst var fyrr í þessu efnisatriði.
6. Veljið **Yfirlit** og finnið svo gildið **Auðkenni forrits (biðlara)**. Þetta er biðlarakenni forritsins. Færa verður það inn annaðhvort á síðunni **Common Data Service Uppsetning tengingar** í reitnum **Biðlarakenni** eða geyma það í öruggri geymslu og láta það í té í áskriftartilviki.
7. Í [!INCLUDE[d365fin](includes/d365fin_md.md)], á síðunni **Common Data Service Uppsetning tengingar**, í reitnum **Vefslóð umhverfis**, skal færa inn vefslóðina fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-umhverfið.
8. Til að virkja tenginguna við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] þarf að kveikja á víxlhnappnum **Virkjað**.
9. Skráðu þig inn með stjórnandareikningnum fyrir Azure Active Directory (þessi reikningur verður að hafa gilt leyfi fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og má vera stjórnandi í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-umhverfinu þínu). Eftir að þú skráir þig inn verður þú beðinn um að leyfa skráða forritinu þínu að skrá sig inn í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] fyrir hönd fyrirtækisins. Veita þarf samþykki til að ljúka uppsetningunni.

   > [!NOTE]
   > Ef þú ert ekki beðinn um að skrá þig inn með stjórnandareikningnum þínum, er það líklega vegna þess að lokað er fyrir sprettiglugga. Til að skrá þig inn skaltu leyfa sprettiglugga úr `https://login.microsoftonline.com`.

#### <a name="using-another-identity-and-access-management-service"></a>Að nota annað auðkenni og fá aðgang að stýringarþjónustu

Ef þú ert ekki að nota Azure Active Directory til að stjórna auðkennum og aðgangsheimild Þarftu aðstoð frá þróunaraðila. Ef þú kýst frekar að geyma forritskennið og leynilykilinn á annarri staðsetningu, geturðu skilið reiti biðlarakennis og leynilykils biðlara eftir auða og skrifað viðbót til að sækja auðkennið og leynilykilinn frá staðsetningunni. Hægt er að gefa upp leynilykilinn við keyrslu með því að gerast áskrifandi að tilvikum OnGetCDSConnectionClientId og OnGetCDSConnectionClientSecret í codeunit 7201 „Útfæra CDS samþættingu“.

### <a name="to-disconnect-from-cds_long_md"></a>Að aftengjast [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning CDS-tengingar** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning CDS-tengingar** skal slökkva á víxlhnappnum **Virkjað**.  

## <a name="see-also"></a>Sjá einnig

[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  
