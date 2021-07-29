---
title: Tengjast við Microsoft Dataverse
description: Settu upp tengingu milli Business Central og Dataverse. Yfirleitt stofna fyrirtæki tenginguna til að samþætta og samstilla gögn við annað Dynamics 365 Business-forrit.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: a29fb1e0a8e10e91a811914a9188548149d5125a
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441344"
---
# <a name="connect-to-microsoft-dataverse"></a>Tengjast við Microsoft Dataverse

[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Í þessu efnisatriði er lýst hvernig skal setja upp tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Yfirleitt stofna fyrirtæki tenginguna til að samþætta og samstilla gögn við annað Dynamics 365 Business-forrit á borð við [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Áður en byrjað er

Áður en tengingin er búin til þarf að koma nokkrum upplýsingum á framfæri:  

* Vefslóðin fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] umhverfið sem á að tengjast við. Ef uppsetningarleiðbeiningin **Dataverse Uppsetning tengingar** með hjálp er notuð til að stofna tengingu finnum við umhverfin þín, en þú getur einnig slegið inn vefslóð fyrir annað umhverfi í leigjandanum þínum.  
* Notandanafn og aðgangsorð reiknings sem er með heimildir stjórnanda í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Ef þú ert með innanhúss [!INCLUDE[prod_short](includes/prod_short.md)] 2020 útgáfubylgju 1, útgáfu 16.5, skaltu lesa greinina [Nokkur þekkt vandamál](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Þú þarft að ljúka við útskýrða hjáleið áður en þú getur stofnað tengingu þína við [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* Staðbundinn gjaldmiðill fyrirtækisins í [!INCLUDE[prod_short](includes/prod_short.md)] verður að vera sá sami og færslugjaldmiðillinn í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Eftir að grunnfærsla er stillt í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] er ekki hægt að breyta henni. Frekari upplýsingar eru í [Færslugjaldmiðill (gjaldmiðill) einingunni](/powerapps/developer/data-platform/transaction-currency-currency-entity). Það þýðir að öll [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtæki sem þú tengir við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] stofnun verða að nota sama gjaldmiðil.

> [!IMPORTANT]
>  [!INCLUDE[cds_long_md](includes/cds_long_md.md)] umhverfið má ekki vera í stjórnunarstillingu. Stjórnandastillingin veldur því að tengingin mistekst vegna þess að notandareikningur samþættingar fyrir tenginguna er ekki með heimildir stjórnanda. Frekari upplýsingar eru í [Stjórnunarsnið](/power-platform/admin/admin-mode).

> [!Note]
> Þessi skref útskýra ferlið fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu.
> Ef verið er að nota [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og ekki er notaður Azure Active Directory-reikningur til að tengjast [!INCLUDE [cds_long_md](includes/cds_long_md.md)], þarf einnig að tilgreina notandanafn og aðgangsorð notandareiknings fyrir samþættinguna. Þessi reikningur er kallaður reikningur „samþættingarnotanda“. Ef notaður er Azure Active Directory-reikningur er reikningur samþættingarnotanda ekki nauðsynlegur eða sýndur. Samþættingarnotandinn verður settur upp sjálfkrafa og þarf ekki leyfi.

## <a name="set-up-a-connection-to-cds_long_md"></a>Uppsetning á tengingu við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

Fyrir allar auðkennisgerðir aðrar en Microsoft 365-auðkenningu, er sett upp tengingin við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] á síðunni **Dataverse Uppsetning tengingar**. Fyrir Microsoft 365 -auðkenningu er mælt með að þú notir uppsetningarleiðbeiningarnar **Dataverse Uppsetning tengingar** með hjálp. Leiðbeiningarnar auðvelda uppsetningu á tengingu og tilgreina ítarlega eiginleika, t.d. eignarhaldslíkan og upphaflega samstillingu.  

> [!IMPORTANT]
> Við uppsetningu tengingarinnar við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] er stjórnandi beðinn um að gefa upp eftirfarandi heimildir til að skrá Azure-forritið sem heitir [!INCLUDE[prod_short](includes/prod_short.md)] samþætting við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * **Aðgangur að [!INCLUDE[cds_long_md](includes/cds_long_md.md)] sem þú** heimild er nauðsynleg svo að [!INCLUDE[prod_short](includes/prod_short.md)] geti, fyrir hönd stjórnanda, stofnað sjálfkrafa heimildarlausa, ógagnvirka notendur forritsins [!INCLUDE[prod_short](includes/prod_short.md)] Integration, úthlutað öryggishlutverkum til þessa notanda og til að nota [!INCLUDE[prod_short](includes/prod_short.md)] samþættingarlausn í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Þessi heimild er aðeins notuð einu sinni við uppsetningu á tengingu við [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Fá fullan aðgang að Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** heimild er nauðsynleg til að sjálfkrafa stofna samþættingarforritið [!INCLUDE[prod_short](includes/prod_short.md)] svo að notandi geti fengið aðgang að [!INCLUDE[prod_short](includes/prod_short.md)]-gögnum sem verða samstillt.  
> * **Skráðu þig inn og lestu notandaupplýsingarnar þínar** heimild er nauðsynleg til að staðfesta innskráningu notanda, er í raun með öryggishlutverk kerfisstjóra úthlutað í [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Með því að veita samþykki fyrir hönd fyrirtækis er stjórnandinn að leyfa skráðu Azure-forriti sem heitir [!INCLUDE[prod_short](includes/prod_short.md)] Integration to [!INCLUDE[cds_long_md](includes/cds_long_md.md)] að samstilla gögn með því að nota sjálfkrafa stofnaðar innskráningarupplýsingar notanda fyrir forritið [!INCLUDE[prod_short](includes/prod_short.md)] Integration.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>Nota hjálparleiðbeiningar fyrir uppsetningu Dataverse tengingar
Leiðbeiningar um uppsetningu Dataverse tengingar getur auðveldað verkið við að tengja forritin og geta jafnvel hjálpað þér að keyra fyrstu samstillingu. Ef valið er að keyra fyrstu samstillingu mun [!INCLUDE[prod_short](includes/prod_short.md)] fara yfir gögnin í báðum forritum og leggja fram tillögur um hvernig eigi að fara að við fyrstu samstillingu. Eftirfarandi tafla lýsir tillögunum.

|Leiðbeiningar  |Description  |
|---------|---------|
|**Full samstilling**|Gögn eru aðeins í [!INCLUDE[prod_short](includes/prod_short.md)] , eða aðeins í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Lagt er til að samstilla öll gögn frá þjónustunni sem er með þau við hina þjónustuna.|
|**Engin samstilling**|Gögn eru til í báðum forritum og keyrsla samstillingar myndi búa til tvítekin gögn. Lagt er til að tengja færslur.|
|**Fylgni ekki uppfyllt**|Gögn eru til í báðum forritum en ekki er hægt að samstilla línu eða töflu vegna þess að hún veltur á línu eða töflu sem er með tillögu um enga samstillingu. Ef til dæmis ekki er hægt að samstilla viðskiptamenn verður ekki heldur hægt að samstilla gögn fyrir tengiliði sem fylgja viðskiptamannagögnum.|

> [!IMPORTANT]
> Yfirleitt er aðeins hægt að nota fulla samstillingu þegar forritin eru samþætt í fyrsta skipti og aðeins eitt forrit inniheldur gögn. Full samstilling getur reynst gagnleg í sýniumhverfi vegna þess að hún stofnar og tengir færslur sjálfkrafa í hverju forriti fyrir sig, sem flýtir fyrir því að geta hafið vinnu með samstillt gögn. Hinsvegar ætti aðeins að keyra fulla samstillingu ef þú vilt eina línu í [!INCLUDE[prod_short](includes/prod_short.md)] fyrir hverja línu í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] fyrir töfluvarpanirnar. Annars getur það leitt til tvítekinna færslna.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil.
2. Veldu **Setja upp tengingu við Microsoft Dataverse** til að hefja leiðbeiningar um uppsetningu með hjálp.
3. Fyllið inn reitina eftir þörfum.

> [!NOTE]
> Ef þú ert ekki beðin(n) um að skrá þig inn með stjórnandareikningnum þínum er það líklega vegna þess að lokað er fyrir sprettiglugga. Til að skrá þig inn skaltu leyfa sprettiglugga úr `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Að stofna eða vinna með tengingu handvirkt

Eftirfarandi ferli útskýrir hvernig á að setja upp tenginguna á síðunni **Dataverse Uppsetning tengingar**. Þetta er einnig síðan þar sem stillingum fyrir samþættingu er stjórnað.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Dataverse Uppsetning tengingar** og velja síðan viðkomandi tengil.
2. Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Svæði|Description|
    |-----|-----|
    |**Vefslóð umhverfis**|Ef þú átt umhverfi í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] finnum við þau fyrir þig þegar þú keyrir uppsetningarleiðbeiningarnar. Ef þú vilt tengjast öðru umhverfi í öðrum leigjanda geturðu slegið inn innskráningarupplýsingar stjórnanda fyrir umhverfið og við finnum það fyrir þig. |
    |**Virk**|Byrjaðu að nota samþættinguna. Ef tengingu er ekki komið á núna munu stillingar tengingar vera vistaðar en notendur geta ekki tengst [!INCLUDE[cds_long_md](includes/cds_long_md.md)] gögnum frá [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að koma aftur þessa síðu og virkja tenginguna seinna.  |

3. Í reitnum **Eignarhaldslíkan** skaltu velja hvort þú viljir að teymistafla í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] eigi nýjar færslur eða einn eða fleiri tilteknir notendur. Ef valið er **Einstaklingur** þarf að tilgreina hvern notanda fyrir sig. Ef valið er **Teymi** birtist sjálfgefna fyrirtækiseiningin í reitnum **Tengd fyrirtækiseining**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field-->|
4. Til að prófa stillingar tengingar skal velja **Tenging** og síðan **Prófa tengingu**.  

    > [!NOTE]  
    > Ef dulritun gagna er ekki virkjuð í [!INCLUDE[prod_short](includes/prod_short.md)] verður spurt hvort þú viljir virkja hana. Til að virkja dulritun gagna skal velja **Já** og gefa nauðsynlegar upplýsingar. Annars skal velja **Nei**. Hægt er að virkja dulritun gagna seinna. Nánari upplýsingar eru í [Gögn dulrituð í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) í hjálp þróunaraðila og stjórnenda.  
5. Ef [!INCLUDE[cds_long_md](includes/cds_long_md.md)] samstilling er ekki þegar sett upp verður spurt hvort nota eigi sjálfgefna samstillingaruppsetningu. Velja skal **Já** eða **Nei** á grunni þess hvort halda eigi færslum samræmdum í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Uppfæra tengingar frá Business Central Online til að nota auðkenningu sem byggir á skilríki
> [!NOTE]
> Þessi hluti á aðeins við fyrir leigjendur Business Central á netinu sem eru hýstir hjá Microsoft. Það hefur engin áhrif á leigjendur á netinu sem eru hýstir hjá óháðum hugbúnaðarsölum og uppsetningar á staðnum.

Í apríl 2022 mun [!INCLUDE[cds_long_md](includes/cds_long_md.md)] taka úr umferð auðkenningarleið Office365 (notandanafn/lykilorð). Frekari upplýsingar er að finna í [Auðkenningarleið Office365 tekin úr umferð](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). Auk þess mun [!INCLUDE[prod_short](includes/prod_short.md)] í mars 2022 taka úr umferð notkun auðkenningu milli þjónusta sem byggir á leyniorði biðlara fyrir leigjendur á netinu og mun krefjast þess að notuð verði auðkenning milli þjónusta sem byggir á skilríkjum fyrir tengingar við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Leigjendur [!INCLUDE[cds_long_md](includes/cds_long_md.md)] á netinu sem óháðir hugbúnaðarsalar hýsa, og uppsetningar á staðnum, geta haldið áfram að nota auðkenningu Office365 sem samstarfsaðili Microsoft setur upp.

Til að koma í veg fyrir truflanir á samþættingum _verður að uppfæra_ tenginguna til að nota auðkenningu sem byggir á skilríki. Þó að breytingin sé áætluð mars 2022 mælum við eindregið með því að þú uppfærir eins fljótt og auðið er. Eftirfarandi skref útskýra hvernig á að uppfæra auðkenningu með skilríkjum. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Til að uppfæra nettengingu við Business Central til að nota auðkenningu með skilríkjum
> [!NOTE]
> Auðkenning með skilríkjum er í boði í Business Central 2021, útgáfutímabili 1 og nýrri. Ef notuð er eldri útgáfa verður að uppfæra í Business Central 2021 útgáfu 1 fyrir mars 2022. Frekari upplýsingar er að finna í [Uppfærslur áætlaðar](/dynamics365/business-central/dev-itpro/administration/update-rollout-timeline#scheduling-updates). Ef vandamál koma upp skaltu hafa samband við samstarfsaðila eða notendaþjónustu.

1. Í [Business Central administration center]/dynamics365/business-central/dev-itpro/administration/tenant-admin-center) skaltu ganga úr skugga um að þú sért að nota Business Central 2021 útgáfutímabil 1 eða síðar (útgáfa 18 eða síðar).
2. Gerðu eitt af eftirfarandi ef þú samþættar við Dynamics 365 Sales:
   * Ef þú gerir það skaltu opna **Microsoft Dynamics Uppsetningarsíðu 365**.
   * Ef ekki skaltu opna **Dataverse Uppsetningarsíðu**.
3. Veldu **Tenging** og síðan **Nota sannvottun vottorðs** til að uppfæra tenginguna til að nota sannvottun sem byggir á vottorði.
4. Skráðu þig inn með innskráningarupplýsingum stjórnanda fyrir Dataverse. Innskráning ætti að taka innan við mínútu.

> [!NOTE]
> Þú verður að endurtaka þessi skref í hverju [!INCLUDE[prod_short](includes/prod_short.md)] umhverfi, þar á meðal bæði framleiðslu- og sandkassaumhverfi, og í hverju fyrirtæki þar sem þú tengist [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Að tengja útgáfur á staðnum

Til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] þarf að gefa upp upplýsingar á síðunni **Dataverse Uppsetning tengingar**.

Ef ætlunin er að tengjast með Azure Active Directory (Azure AD) reikningi þarf að skrá forrit í Azure AD og gefa upp auðkenni forritsins, leynilykil lyklageymslu og framsendingarslóðina sem á að nota. Framsend vefslóð er fyllt út fyrirfram og ætti að virka fyrir flestar uppsetningar. Nauðsynlegt er að setja upp uppsetninguna til að nota HTTPS. Frekari upplýsingar er að finna í [Skilgreining SSL til að tryggja örugga tengingu vefbiðlara Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Ef verið er að setja upp þjóninn til að hafa aðra heimasíðu er alltaf hægt að breyta vefslóðinni. Leynilykill biðlara verða vistaður sem dulkóðaður strengur í gagnagrunninum. 

### <a name="prerequisites"></a>Frumskilyrði

Dataverse verður að nota eina af eftirfarandi gerðum sannvottunar:

* Office365 (eldra)

  > [!IMPORTANT]
  > Gildir frá apríl 2022, Office365 (eldra) verður ekki lengur stutt. Frekari upplýsingar eru í [Mikilvægar breytingar (afskriftir) væntanlegar í Power Apps, Power Automate og viðskiptavinaforritum](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).
* Office365 (modern, OAuth2 leyniorð biðlara)
* OAuth

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-dataverse"></a>Til að skrá forrit í Azure AD fyrir tengingu úr Business Central í Dataverse

Eftirfarandi skref gera ráð fyrir að nota Azure AD til að stjórna auðkennum og aðgangsheimild. Frekari upplýsingar um skráningu forrits í Azure AD er að finna í [Stuttar leiðbeiningar: Skrá forrit með auðkenningarverkvangi Microsoft](/azure/active-directory/develop/quickstart-register-app). 

1. Í Azure-gáttinni, undir **Stjórna** á yfirlitssvæðinu, skal velja **Sannvottun**.  
2. Undir **Framsenda vefslóðir** skal bæta við framsendingarvefslóð sem mælt er með á síðunni **Dataverse Uppsetning tengingar** í [!INCLUDE[prod_short](includes/prod_short.md)].
3. Undir **Stjórna** skal velja **API-heimildir**.
4. Undir **Skilgreindar heimildir** skal velja **Bæta við heimild** og síðan bæta við úthlutuðum heimildum í flipanum **Microsoft API** á eftirfarandi hátt:
    * Fyrir Business Central skal bæta við heimildunum **Financials.ReadWrite.All**.
    * Fyrir Dynamics CRM skal bæta við heimildunum **user_impersonation**.  

    > [!NOTE]
    > Heiti Dynamics CRM API gæti breyst.

5. Undir **Stjórna** skal velja **Vottorð og leynilyklar** og síðan stofna nýjan leynilykil fyrir forritið. Leynilykillinn verður notaður annaðhvort í [!INCLUDE[prod_short](includes/prod_short.md)], í reitnum **Leynilykill biðlara** á síðunni **Dataverse Uppsetning tengingar** eða geymdur í öruggri geymslu og hann látinn í té í áskriftartilviki eins og lýst var fyrr í þessu efnisatriði.
6. Veljið **Yfirlit** og finnið svo gildið **Auðkenni forrits (biðlara)**. Þetta er biðlarakenni forritsins. Færa verður það inn annaðhvort á síðunni **Dataverse Uppsetning tengingar** í reitnum **Biðlarakenni** eða geyma það í öruggri geymslu og láta það í té í áskriftartilviki.
7. Í [!INCLUDE[prod_short](includes/prod_short.md)], á síðunni **Dataverse Uppsetning tengingar**, í reitnum **Vefslóð umhverfis**, skal færa inn vefslóðina fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-umhverfið.
8. Til að virkja tenginguna við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] þarf að kveikja á víxlhnappnum **Virkjað**.
9. Skráðu þig inn með stjórnandareikningnum fyrir Azure Active Directory (þessi reikningur verður að hafa gilt leyfi fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og má vera stjórnandi í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-umhverfinu þínu). Eftir að þú skráir þig inn verður þú beðinn um að leyfa skráða forritinu þínu að skrá sig inn í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] fyrir hönd fyrirtækisins. Veita þarf samþykki til að ljúka uppsetningunni.

   > [!NOTE]
   > Ef þú ert ekki beðinn um að skrá þig inn með stjórnandareikningnum þínum, er það líklega vegna þess að lokað er fyrir sprettiglugga. Til að skrá þig inn skaltu leyfa sprettiglugga úr `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-cds_long_md"></a>Að aftengjast [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Dataverse Uppsetning tengingar** og velja síðan viðkomandi tengil.
2. Á síðunni **Dataverse Uppsetning CDS-tengingar** skal slökkva á víxlhnappnum **Virkjað**.  

## <a name="see-also"></a>Sjá einnig

[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]