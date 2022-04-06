---
title: Microsoft Dataverse Tengjast (inniheldur Video)
description: Settu upp tengingu milli Business Central og Dataverse. Yfirleitt stofna fyrirtæki tenginguna til að samþætta og samstilla gögn við annað Dynamics 365 Business-forrit.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 7200, 7201
ms.date: 09/30/2021
ms.author: bholtorf
ms.openlocfilehash: 57f8091d81870f9e58af80462259006d4cb822ae
ms.sourcegitcommit: 4a57fb5b88b9ebbb61fdd1b25e1fd4ba0013c8e5
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/25/2022
ms.locfileid: "8485033"
---
# <a name="connect-to-microsoft-dataverse"></a>Tengjast við Microsoft Dataverse



Í þessu efnisatriði er lýst hvernig skal setja upp tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Yfirleitt stofna fyrirtæki tenginguna til að samþætta og samstilla gögn við annað Dynamics 365 Business-forrit á borð við [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Áður en byrjað er

Áður en tengingin er búin til þarf að koma nokkrum upplýsingum á framfæri:  

* Vefslóðin fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] umhverfið sem á að tengjast við. Ef notuð er leiðbeiningar um **Dataverse uppsetningu tengingaraðstoðar** til að stofna tenginguna finnum við umhverfi notanda. Einnig er hægt að slá inn VEFSLÓÐ á annað umhverfi hjá leigjanda.  
* Notandanafn og aðgangsorð reiknings sem er með heimildir stjórnanda í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Ef þú ert með innanhúss [!INCLUDE[prod_short](includes/prod_short.md)] 2020 útgáfubylgju 1, útgáfu 16.5, skaltu lesa greinina [Nokkur þekkt vandamál](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Þú þarft að ljúka við útskýrða hjáleið áður en þú getur stofnað tengingu þína við [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* Staðbundinn gjaldmiðill fyrirtækisins í [!INCLUDE[prod_short](includes/prod_short.md)] verður að vera sá sami og færslugjaldmiðillinn í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Þegar færsla hefur verið gerð í grunngjaldmiðlinum [!INCLUDE[cds_long_md](includes/cds_long_md.md)] er ekki hægt að breyta henni. Frekari upplýsingar eru í [Færslugjaldmiðill (gjaldmiðill) einingunni](/powerapps/developer/data-platform/transaction-currency-currency-entity). Öll [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtæki sem þú tengir við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] stofnun verða að nota sama gjaldmiðil.

> [!IMPORTANT]
>  [!INCLUDE[cds_long_md](includes/cds_long_md.md)] umhverfið má ekki vera í stjórnunarstillingu. Stjórnandastillingin veldur því að tengingin mistekst vegna þess að notandareikningur samþættingar fyrir tenginguna er ekki með heimildir stjórnanda. Frekari upplýsingar eru í [Stjórnunarsnið](/power-platform/admin/admin-mode).

> [!Note]
> Þessi skref útskýra ferlið fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu.
> Ef þú notar [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss og notar Azure Active Directory ekki lykil til að tengjast [!INCLUDE [cds_long_md](includes/cds_long_md.md)], verður þú einnig að tilgreina notandanafn og aðgangsorð notandareiknings fyrir samþættingu. Þessi reikningur er kallaður reikningur „samþættingarnotanda“. Ef þú ert að nota Azure Active Directory lykil er reikningur fyrir samþættingu hvorki nauðsynlegur né birtur. Samþættingarnotandinn verður settur upp sjálfkrafa og þarf ekki leyfi.

## <a name="set-up-a-connection-to-cds_long_md"></a>Uppsetning á tengingu við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

Fyrir allar gerðir Microsoft 365 sannvottunar er Tengingin við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] á **Dataverse síðu tengingaruppsetningar** sett upp. Við sannvottun er mælt með því að Uppsetningarleiðbeiningar fyrir Microsoft 365 tengingaraðstoðarmenn **Dataverse séu notaðar**. Leiðbeiningarnar auðvelda uppsetningu á tengingu og tilgreina ítarlega eiginleika, t.d. eignarhaldslíkan og upphaflega samstillingu.  

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
|**Fylgni ekki uppfyllt**|Gögn eru til í báðum forritum en ekki er hægt að samstilla töfluna, því hún fer eftir röð eða töflu sem engin samstillingartilmæli hefur. Til dæmis, ef Viðskiptavinir geta ekki samstillt, þá eru ekki gögn fyrir tengiliði sem fara eftir viðskiptavinagögnum ekki samstillt annað hvort.|

> [!IMPORTANT]
> Yfirleitt er aðeins hægt að nota fulla samstillingu þegar forritin eru samþætt í fyrsta skipti og aðeins eitt forrit inniheldur gögn. Full samstilling getur reynst gagnleg í sýniumhverfi vegna þess að hún stofnar og tengir færslur sjálfkrafa í hverju forriti fyrir sig, sem flýtir fyrir því að geta hafið vinnu með samstillt gögn. Hinsvegar ætti aðeins að keyra fulla samstillingu ef þú vilt eina línu í [!INCLUDE[prod_short](includes/prod_short.md)] fyrir hverja línu í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] fyrir töfluvarpanirnar. Annars getur það leitt til tvítekinna færslna.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil.
2. Veldu **Setja upp tengingu við Microsoft Dataverse** til að hefja leiðbeiningar um uppsetningu með hjálp.
3. Fyllið inn reitina eftir þörfum.

> [!NOTE]
> Ef notandi er ekki beðinn um að skrá sig inn með stjórnandareikninginn er hann líklega á því að POP-ups sé lokað. Til að skrá þig inn skaltu leyfa sprettiglugga úr `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Að stofna eða vinna með tengingu handvirkt

Eftirfarandi ferli útskýrir hvernig á að setja upp tenginguna á síðunni **Dataverse Uppsetning tengingar**. Síðan tengingaruppsetning **Dataverse er í** Umsjón með samþættingarstillingum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Dataverse Uppsetning tengingar** og velja síðan viðkomandi tengil.
2. Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Svæði|Description|
    |-----|-----|
    |**Vefslóð umhverfis**|Ef þú átt umhverfi í [!INCLUDE[cds_long_md](includes/cds_long_md.md)], finnum þá fyrir þér þegar þú keyrir Uppsetningarleiðbeiningarnar. Ef þú vilt tengjast ólíku umhverfi í öðrum leigjanda getur þú slegið inn skilríki umsjónarmanns fyrir umhverfið og við finnum það. |
    |**Virk**|Byrjaðu að nota samþættinguna. Ef tengingin er ekki virk núna eru tengingarstillingarnar vistaðar en notendur geta ekki fengið aðgang [!INCLUDE[cds_long_md](includes/cds_long_md.md)] að gögnum [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að koma aftur þessa síðu og virkja tenginguna seinna.  |

3. Í reitnum **Eignarhaldslíkan** skaltu velja hvort þú viljir að teymistafla í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] eigi nýjar færslur eða einn eða fleiri tilteknir notendur. Ef valið er **Einstaklingur** þarf að tilgreina hvern notanda fyrir sig. Ef valið er **Teymi** birtist sjálfgefna fyrirtækiseiningin í reitnum **Tengd fyrirtækiseining**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you're using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who don't have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account won't have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Til að prófa stillingar tengingar skal velja **Tenging** og síðan **Prófa tengingu**.  

    > [!NOTE]  
    > Ef dulritun gagna er ekki virkjuð í [!INCLUDE[prod_short](includes/prod_short.md)] verður spurt hvort þú viljir virkja hana. Til að virkja dulritun gagna skal velja **Já** og gefa nauðsynlegar upplýsingar. Annars skal velja **Nei**. Hægt er að virkja dulritun gagna seinna. Nánari upplýsingar eru í [Gögn dulrituð í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) í hjálp þróunaraðila og stjórnenda.  
5. Ef [!INCLUDE[cds_long_md](includes/cds_long_md.md)] samstilling er ekki þegar sett upp verður spurt hvort nota eigi sjálfgefna samstillingaruppsetningu. Velja skal **Já** eða **Nei** á grunni þess hvort halda eigi færslum samræmdum í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a>Sérstilla tengingu byggða á samsvörun

Sem byrjar í 2021 2, kerfisstjóri getur fært inn skilyrði fyrir par-færslur sem byggjast á samstæðum. Hægt er að ræsa algrím fyrir jöfnunarfærslur frá eftirtöldum stöðum í [!INCLUDE [prod_short](includes/prod_short.md)]:

* Listasíður sem sýna færslur sem eru samstilltar með [!INCLUDE [cds_long_md](includes/cds_long_md.md)], t.d. viðskiptavina- og vörusíður.  

    Veldu margar færslur og veldu síðan aðgerðina **Tengdar**, veldu **Dataverse**, veldu **Tenging** og veldu síðan **Tenging byggð á samsvörun**.

    Þegar samsvörsferlið er ræst af aðalgagnalista er afsláttarvinnsluaðferð áætluð eftir að viðmiðling er tilgreind.  
* Síðan **Dataverse Yfirfara fulla samstillingu**.  

    Þegar heildarsamstillingarferlið uppgötvar óunnar færslur í og [!INCLUDE [prod_short](includes/prod_short.md)][!INCLUDE [cds_long_md](includes/cds_long_md.md)] birtist tengill í **samþættingartöflu fyrir velja festling Criteria**.  

    Hægt er að ræsa keyrsluferlið í **fullri samstillingu** út **Dataverse frá Uppsetningarsíðum tengingaruppsetningarinnar** og **Dynamics 365**. Einnig er hægt að ræsa hana í **Uppsetning leiðbeininga um tengingu við Dataverse** aðstoðarmenn þegar uppsetningu er lokið.  

    Þegar samsvörun er hafin, frá því að **Dataverse Full Synch er ræst. Skoða** síðu, festingu vinnsla er áætluð eftir að uppsetningu er lokið.  
* Listinn **Vörpun samþættingartöflu**.  

    Veldu vörpun, veldu aðgerðina **Tenging** og veldu svo **Tenging byggð á samsvörun**.

    Þegar samsvörunarferlið er ræst frá vörpun samþættingartöflu, er festivinnsla keyrð fyrir allar óbyggðar færslur í kortvörpun. Einnig er hægt að velja óunnar færslur í listanum til að keyra vinnsluna aðeins fyrir færslurnar.

Í öllum þremur tilvikum opnast síðan **Velja tengingarskilyrði** svo þú getir skilgreint viðeigandi tengingarskilyrði. Á þessari síðu skal sérstilla tenginguna með eftirfarandi verkum:

* Velja svæðin sem á að nota til að jafna [!INCLUDE [prod_short](includes/prod_short.md)] færslur við [!INCLUDE [cds_long_md](includes/cds_long_md.md)] einingar. Hægt er að tilgreina hvort samsvörun sé Stafrétt.  

* Tilgreinið hvort samstilla eigi eftir par-færslum. Ef færslur nota tvístefnuvörpun er einnig hægt að tilgreina hvað gerist ef árekstrar eru á listanum á **síðunni leysa Uppfærsluárekstra**.  

* Forgangsraðaðu leit að færslunum með því að tilgreina *forgang samsvörunar* fyrir viðkomandi reitarvörpun. [!INCLUDE [prod_short](includes/prod_short.md)] mun leita að samsvörun í hækkandi röð sem byggist á gildinu í **reitnum samsvara forgangi**. Autt gildi í **svæðinu samsvörun forgangs** jafngildir forgangi 0 sem er mesti Forgangur. Reitir með 0 forgangi teljast sem fyrst.  

* Tilgreindu hvort eigi að búa til nýtt tilvik einingar í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] ef engin einkvæm ótengd samsvörun finnst með þessu skilyrði fyrir samsvörun. Til að virkja þennan möguleika skal velja aðgerðina **Stofna nýtt ef ekki tekst að finna samsvörun**.  

### <a name="view-the-results-of-the-coupling-job"></a>Skoða niðurstöður tengingarverksins

Til að skoða niðurstöður tengingarverksins skal opna síðuna **Vörpun samþættingartöflu**, velja viðkomandi vörpun, velja aðgerðina **Tenging** og því næst velja aðgerðina **Verkkladdi fyrir tengingu samþættingar**.  

Ef ekki tókst að fá færslur á par má velja gildið í **dálkinum í brást** til að opna lista yfir villur sem lýsa því hvers vegna það gerðist.  

Yfirleitt bregst festing við eftirfarandi ástæðum:

* Ekkert samsvörunarskilyrði var skilgreint

    Keyra samsvöruna saman aftur en munið að skilgreina afsláttarskilyrði.

* Engin samsvörun fannst fyrir svæðin sem tilgreind voru í jöfnunarskilyrnum

    Endurtakið festingu með mismunandi svæðum.

* Margar samstæður fundust fyrir nokkrum færslum sem byggðar voru á svæðunum sem tilgreind voru í jöfnunarskilyrð-  

    Endurtakið festingu með mismunandi svæðum.

* Samskip fannst en færslan er nú þegar komin á skrá í [!INCLUDE [prod_short](includes/prod_short.md)]  

    Endurtaka skal festingu með mismunandi svæðum eða rannsaka hvers vegna [!INCLUDE [cds_long_md](includes/cds_long_md.md)] Einingin er sett í færsluna í [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> Til að auðvelda þér að fá yfirlit yfir framvindu festivalið **Dataverse** sýnir reiturinn hvort færsla er tengd við [!INCLUDE [cds_long_md](includes/cds_long_md.md)] einingu. Hægt er að nota **Dataverse** reitinn miðskrá til að sía listann yfir færslurnar sem verið er að samstilla.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Uppfæra tengingar frá Business Central Online til að nota auðkenningu sem byggir á skilríki
> [!NOTE]
> Þessi hluti á aðeins við fyrir leigjendur [!INCLUDE[prod_short](includes/prod_short.md)] á netinu sem eru hýstir hjá Microsoft. Það hefur engin áhrif á leigjendur á netinu sem eru hýstir hjá óháðum hugbúnaðarsölum og uppsetningar á staðnum.

Í apríl 2022, [!INCLUDE[cds_long_md](includes/cds_long_md.md)] er afskráð úr Office365 sannvottunargerð (notendanafn/lykilorð). Frekari upplýsingar er að finna í [Auðkenningarleið Office365 tekin úr umferð](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). Til viðbótar, í mars 2022, [!INCLUDE[prod_short](includes/prod_short.md)] er afskráð notkun umbjóðanda leyniþjónustu sem byggir á sannvottun skjólstæðinga á netinu vegna þjónustu við leigjendur. Nota verður sannvottun samkvæmt vottorði frá þjónustuveitu til tenginga [!INCLUDE[cds_long_md](includes/cds_long_md.md)] í. [!INCLUDE[prod_short](includes/prod_short.md)] nettengdir leigjendur sem eru hýstir hjá ISVs, og uppsetningar innanhúss, geta haldið áfram að nota leynibréf viðskiptavinar til sannvottunar.

Til að koma í veg fyrir truflanir á samþættingum _verður að uppfæra_ tenginguna til að nota auðkenningu sem byggir á skilríki. Þó svo að breytingin sé áætluð fyrir mars 2022 mælum við eindregið með að uppfært sé eins fljótt og auðið er. Eftirfarandi skref útskýra hvernig á að uppfæra auðkenningu með skilríkjum. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Til að uppfæra nettengingu við Business Central til að nota auðkenningu með skilríkjum

1. Gerðu eitt af eftirfarandi ef þú samþættar við Dynamics 365 Sales:
   * Ef þú gerir það skaltu opna **Microsoft Dynamics Uppsetningarsíðu 365**.
   * Ef ekki skaltu opna **Dataverse Uppsetningarsíðu**.
2. Veldu **Tenging** og síðan **Nota sannvottun vottorðs** til að uppfæra tenginguna til að nota sannvottun sem byggir á vottorði.
3. Skráðu þig inn með innskráningarupplýsingum stjórnanda fyrir Dataverse. Það ætti að taka minna en mínútu að skrá sig inn.

> [!NOTE]
> Þú verður að endurtaka þessi skref í hverju [!INCLUDE[prod_short](includes/prod_short.md)] umhverfi, þar á meðal bæði framleiðslu- og sandkassaumhverfi, og í hverju fyrirtæki þar sem þú tengist [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Að tengja útgáfur á staðnum

Til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] þarf að gefa upp upplýsingar á síðunni **Dataverse Uppsetning tengingar**.

Til að tengjast með Azure Active Directory (Azure AD) lykli þarf að skrá umsókn í Azure AD. Þú munt þurfa að útvega umsóknarkennið, leynihólf lyklageymslu og beina VEFSLÓÐINA að notkun. Framsend vefslóð er fyllt út fyrirfram og ætti að virka fyrir flestar uppsetningar. Nauðsynlegt er að setja upp uppsetninguna til að nota HTTPS. Frekari upplýsingar er að finna í [Skilgreining SSL til að tryggja örugga tengingu vefbiðlara Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Ef þjónn er settur upp til að geta haft aðra heimasíðu er hægt að breyta SLÓÐINNI. Leynilykill biðlara verða vistaður sem dulkóðaður strengur í gagnagrunninum. 

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
6. Veljið **Yfirlit** og finnið svo gildið **Auðkenni forrits (biðlara)**. Þetta AUÐKENNI er Biðlarakenni forritsins. Færa verður það inn annaðhvort á síðunni **Dataverse Uppsetning tengingar** í reitnum **Biðlarakenni** eða geyma það í öruggri geymslu og láta það í té í áskriftartilviki.
7. Í [!INCLUDE[prod_short](includes/prod_short.md)], á síðunni **Dataverse Uppsetning tengingar**, í reitnum **Vefslóð umhverfis**, skal færa inn vefslóðina fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-umhverfið.
8. Til að virkja tenginguna við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] þarf að kveikja á víxlhnappnum **Virkjað**.
9. Skráðu þig inn með stjórnandareikningnum fyrir Azure Active Directory (þessi reikningur verður að hafa gilt leyfi fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og má vera stjórnandi í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-umhverfinu þínu). Eftir að þú hefur skráð þig inn færðu kvaðningu um að leyfa skráðu þinni umsókn að skrá þig inn fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] hönd samtakanna. Veita þarf samþykki til að ljúka uppsetningunni.

   > [!NOTE]
   > Ef notandi er ekki beðinn um að skrá sig inn með stjórnandareikninginn er hann líklega á því að POP ups sé lokað. Til að skrá þig inn skaltu leyfa sprettiglugga úr `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-cds_long_md"></a>Að aftengjast [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Dataverse Uppsetning tengingar** og velja síðan viðkomandi tengil.
2. Á síðunni **Dataverse Uppsetning CDS-tengingar** skal slökkva á víxlhnappnum **Virkjað**.  

## <a name="see-also"></a>Sjá einnig

[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
