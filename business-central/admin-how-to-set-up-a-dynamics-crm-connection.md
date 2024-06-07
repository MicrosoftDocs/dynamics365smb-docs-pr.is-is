---
title: Tengja við Microsoft Dataverse (inniheldur myndskeið)
description: Settu upp tengingu milli Business Central og Dataverse. Yfirleitt stofna fyrirtæki tenginguna til að samþætta og samstilla gögn við annað Dynamics 365 Business-forrit.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '7200, 7201'
ms.date: 02/28/2024
ms.service: dynamics-365-business-central
---
# <a name="connect-to-microsoft-dataverse"></a>Tengjast við Microsoft Dataverse

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Í þessari grein er því lýst hvernig setja skuli upp tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Yfirleitt stofna fyrirtæki tenginguna til að samþætta og samstilla gögn við annað Dynamics 365 Business-forrit á borð við [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Verður að byrja fyrir

Áður en tengingin er búin til þarf að koma nokkrum upplýsingum á framfæri:  

* Vefslóðin fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] umhverfið sem á að tengjast við. Ef uppsetningarleiðbeiningin **Dataverse Uppsetning tengingar** með hjálp er notuð til að stofna tengingu finnum við umhverfin þín. Einnig er hægt að færa inn vefslóð annars umhverfis í biðlarann.  
* Notandanafn og aðgangsorð reiknings sem er með heimildir stjórnanda í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Ef þú ert með innanhúss [!INCLUDE[prod_short](includes/prod_short.md)] 2020 útgáfubylgju 1, útgáfu 16.5, skaltu lesa greinina [Nokkur þekkt vandamál](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Þú þarft að ljúka við útskýrða hjáleið áður en þú getur stofnað tengingu þína við [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* Staðbundnir gjaldmiðlar sem hvert fyrirtæki notar. [!INCLUDE [prod_short](includes/prod_short.md)] fyrirtæki geta tengst [!INCLUDE [cds_long_md](includes/cds_long_md.md)] umhverfi sem er með grunngjaldmiðil sem er annar en staðbundinn gjaldmiðill. Nánari upplýsingar um hvernig á að meðhöndla marggjaldmiðilsuppsetningar er farið í [Leyfa fyrir mismunandi gjaldmiðla](#allow-for-different-currencies).

> [!IMPORTANT]
>  [!INCLUDE[cds_long_md](includes/cds_long_md.md)] umhverfið má ekki vera í stjórnunarstillingu. Stjórnandastillingin veldur því að tengingin mistekst vegna þess að notandareikningur samþættingar fyrir tenginguna er ekki með heimildir stjórnanda. Frekari upplýsingar eru í [Stjórnunarsnið](/power-platform/admin/admin-mode).

> [!Note]
> Þessi skref útskýra ferlið fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu.
> Ef þú notar [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og notar Microsoft Entra ekki reikning til að tengjast [!INCLUDE [cds_long_md](includes/cds_long_md.md)] verður einnig að tilgreina notandanafn og aðgangsorð notandareiknings fyrir samþættinguna. Þessi reikningur er kallaður reikningur „samþættingarnotanda“. Ef notandi notar Microsoft Entra reikning er ekki krafist samþættingarnotandareikningsins eða hann birtur. Samþættingarnotandinn verður settur upp sjálfkrafa og þarf ekki leyfi.

## <a name="link-your-business-central-and-dataverse-environments"></a>Tengja Business Central og Dataverse umhverfi

Fyrirtæki vilja halda gögnum sínum öruggum og öruggum innan persónuverndarmörkum sínum, og sérstaklega þegar viðskiptastjórnunarforrit þeirra er samþætt öðrum forritum. Með því að [!INCLUDE [prod_short](includes/prod_short.md)] tengja og [!INCLUDE[cds_long_md](includes/cds_long_md.md)] umhverfi nærð þú ekki aðeins þeim sjónarmiðum, heldur veitir stjórnendum þínum einnig auðveldari leið til að búa til og viðhalda samþættingu við önnur Dynamics 365 forrit.

 [!INCLUDE [prod_short](includes/prod_short.md)] Í stjórnunarmiðstöðinni er hægt að tengja umhverfið [!INCLUDE [prod_short](includes/prod_short.md)] við umhverfið [!INCLUDE [cds_long_md](includes/cds_long_md.md)] . [!INCLUDE [prod_short](includes/prod_short.md)] hægt er að nota upplýsingarnar af tenglinum til að auðvelda öryggi og samþættingu við önnur forrit Dynamics 365, svo sem Sölu- og reitaþjónustu. Tengt [!INCLUDE [cds_long_md](includes/cds_long_md.md)] umhverfisfang er til dæmis sjálfgefið tiltækt á síðunni **Dataverse Uppsetning** tengingar og þegar uppsetningarleiðbeiningar með aðstoð tengingar **Dataverse eru keyrðar** .

## <a name="allow-for-different-currencies"></a>Leyfa mismunandi gjaldmiðla

[!INCLUDE [prod_short](includes/prod_short.md)] fyrirtæki geta tengst [!INCLUDE [cds_long_md](includes/cds_long_md.md)] umhverfi sem er með grunngjaldmiðil sem er annar en staðbundinn gjaldmiðill.

> [!NOTE]
> Samstilling margra gjaldmiðla krefst þess að samstilling sé notuð, allt frá [!INCLUDE [prod_short](includes/prod_short.md)]  [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

Til að [!INCLUDE [cds_long_md](includes/cds_long_md.md)] fræðast meira um grunngjaldmiðilinn í er farið í [færslugjaldmiðilseiningu](/powerapps/developer/data-platform/transaction-currency-currency-entity) (gjaldmiðill). 

Til að [!INCLUDE [prod_short](includes/prod_short.md)] fræðast meira um gjaldmiðla í er farið í [Gjaldmiðlar í Business Central](finance-currencies.md).

Ef leyfa á mismunandi gjaldmiðla þarf að ganga úr skugga um að eftirfarandi stillingar hafi verið tilgreindar:

* Gjaldmiðilsstilling grunnviðskipta í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] er með gjaldmiðilskótann sem er tilgreindur á síðunni **Gjaldmiðlar** í [!INCLUDE [prod_short](includes/prod_short.md)].
* Það er að minnsta kosti eitt gengi tilgreint fyrir gjaldmiðilinn á [!INCLUDE [prod_short](includes/prod_short.md)] síðunni **Gengi gjaldmiðils** .

Þegar tenging [!INCLUDE [cds_long_md](includes/cds_long_md.md)] er gerð virk við bætir [!INCLUDE [prod_short](includes/prod_short.md)]  heimagjaldmiðillinn henni við **gjaldmiðilseininguna** . [!INCLUDE [cds_long_md](includes/cds_long_md.md)] Heimagjaldmiðillinn notar gengið úr reitnum **Gengisstuðull** á síðunni **Gengi gjaldmiðils** .

Þar sem samstilling gjaldmiðils er einstefnuleg, frá [!INCLUDE [prod_short](includes/prod_short.md)] til [!INCLUDE [cds_long_md](includes/cds_long_md.md)], umbreyta peningaupphæðir og samstilla á eftirfarandi hátt:

* Ef í grunngjaldmiðlinum [!INCLUDE [cds_long_md](includes/cds_long_md.md)] eru upphæðir umreiknaðar í [!INCLUDE [prod_short](includes/prod_short.md)] staðarmynt byggðar á því gengi sem síðast var samstillt úr [!INCLUDE [prod_short](includes/prod_short.md)].
* Ef í [!INCLUDE [prod_short](includes/prod_short.md)] staðarmynt eru upphæðir samstilltar við [!INCLUDE [prod_short](includes/prod_short.md)] heimagjaldmiðilinn í einum af viðbótargjaldmiðlunum sem ekki eru grunngjaldmiðlar í [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

## <a name="set-up-a-connection-to-"></a>Setja upp tengingu við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

Fyrir allar auðkennisgerðir aðrar en Microsoft 365-auðkenningu, er sett upp tengingin við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] á síðunni **Dataverse Uppsetning tengingar**. Fyrir Microsoft 365 auðkenningu er mælt með að þú notir uppsetningarleiðbeiningar **DataverseUppsetning tengingar** með hjálp. Leiðbeiningarnar auðvelda uppsetningu á tengingu og tilgreina ítarlega eiginleika, t.d. eignarhaldslíkan og upphaflega samstillingu.  

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

Eftirfarandi ferli útskýrir hvernig á að setja upp tenginguna á síðunni **Dataverse Uppsetning tengingar**. Á síðunni **Dataverse Uppsetning tengingar** stjórnar þú stillingum samþættingar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Dataverse Uppsetning tengingar** og velja síðan viðkomandi tengil.
2. Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Svæði|Lýsing|
    |-----|-----|
    |**Vefslóð umhverfis**|Ef þú átt umhverfi í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] finnum við þau fyrir þig þegar þú keyrir uppsetningarleiðbeiningarnar. Ef þú vilt tengjast öðru umhverfi í öðrum leigjanda geturðu slegið inn innskráningarupplýsingar stjórnanda fyrir umhverfið og við finnum það. |
    |**Virk**|Byrjaðu að nota samþættinguna. Ef tengingu er ekki komið á núna munu stillingar tengingar vera vistaðar en notendur geta ekki nálgast [!INCLUDE[cds_long_md](includes/cds_long_md.md)] gögnin frá [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að koma aftur þessa síðu og virkja tenginguna seinna.  |

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
## <a name="show-me-the-process"></a>Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a>Sérstilla samsvörunarmiðaða jöfnun

Frá og með 2021 útgáfutímabili 2 getur stjórnandi slegið inn skilyrði til að tengja færslur út frá samsvörun. Hægt er að ræsa reiknirit fyrir samsvörun færslna frá eftirfarandi stöðum í [!INCLUDE [prod_short](includes/prod_short.md)]:

* Listasíður sem sýna færslur sem eru samstilltar með [!INCLUDE [cds_long_md](includes/cds_long_md.md)], t.d. viðskiptavina- og vörusíður.  

    Veldu margar færslur og veldu síðan aðgerðina **Tengdar**, veldu **Dataverse**, veldu **Tenging** og veldu síðan **Tenging byggð á samsvörun**.

    Þegar byrjað er á tengingarferli sem byggir á samsvörun úr lista yfir aðalgögn er tengingarvinna tímasett eftir að þú hefur tilgreint skilyrði tengingar.  
* Síðan **Dataverse Yfirfara fulla samstillingu**.  

    Þegar heildarsamstillingarferlið greinir aftengdar færslur í [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)] birtist tengill **Velja tengingarskilyrði** fyrir samþættingartöflu.  

    Hægt er að hefja ferlið **Keyra fulla samstillingu** af síðunum **Dataverse Uppsetning tengingar** og **Uppsetning Dynamics 365-tengingar**. Þú getur einnig hafið það í uppsetningarleiðbeiningunni **Setja upp tengingu við Dataverse** þegar þú lýkur uppsetningunni.  

    Þegar þú byrjar tengiferlið sem byggir á samsvörun af síðunni **Dataverse Endurskoðun fullrar samstillingar** er tengingarvinna tímasett eftir að uppsetningunni lýkur.  
* Listinn **Vörpun samþættingartöflu**.  

    Veldu vörpun, veldu aðgerðina **Tenging** og veldu svo **Tenging byggð á samsvörun**.

    Þegar þú byrjar tengiferlið sem byggist á samsvörun úr vörpun samþættingartöflu, keyrir tengingarvinna fyrir allar ótengdar færslur í vörpuninni. Einnig er hægt að velja ótengdar færslur í listanum til að keyra verkið aðeins fyrir þessar færslur.

Í öllum þremur tilvikum opnast síðan **Velja tengingarskilyrði** svo þú getir skilgreint viðeigandi tengingarskilyrði. Á þessari síðu skal sérstilla tenginguna með eftirfarandi verkum:

* Veldu reitina sem á að nota til að samsvara [!INCLUDE [prod_short](includes/prod_short.md)] færslur við [!INCLUDE [cds_long_md](includes/cds_long_md.md)] einingar. Hægt er að tilgreina hvort tekið sé tillit til há- og lágstafa í samsvöruninni.  

* Tilgreindu hvort eigi að samstilla eftir að færslurnar eru tengdar. Ef skrár nota tvíátta vörpun er einnig hægt að tilgreina hvað gerist ef árekstrar eru skráðir á síðunni **Leysa úr uppfærsluárekstrum**.  

* Forgangsraðaðu leit að færslunum með því að tilgreina *forgang samsvörunar* fyrir viðkomandi reitarvörpun. [!INCLUDE [prod_short](includes/prod_short.md)] leitar að samsvörun í hækkandi röð út frá gildinu í reitnum **Forgangur samsvörunar**. Autt gildi í reitnum **Forgangur samsvörunar** jafngildir forgangi 0, sem er hæsti forgangur. Reitir með 0 forgang eru fyrst teknir til greina.  

* Tilgreindu hvort eigi að búa til nýtt tilvik einingar í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] ef engin einkvæm ótengd samsvörun finnst með þessu skilyrði fyrir samsvörun. Til að virkja þennan möguleika skal velja aðgerðina **Stofna nýtt ef ekki tekst að finna samsvörun**.  

### <a name="view-the-results-of-the-coupling-job"></a>Skoða niðurstöður tengingarverksins

Til að skoða niðurstöður tengingarverksins skal opna síðuna **Vörpun samþættingartöflu**, velja viðkomandi vörpun, velja aðgerðina **Tenging** og því næst velja aðgerðina **Verkkladdi fyrir tengingu samþættingar**.  

Ef ekki tókst að tengja færslur er hægt að velja gildið í dálknum **Mistókst** til að opna lista yfir villur sem útskýra hvað gerðist.  

Yfirleitt mistekst tenging af eftirfarandi ástæðum:

* Ekkert samsvörunarskilyrði var skilgreint

    Keyrðu tenginguna sem byggir á samsvörun aftur, en mundu að skilgreina skilyrði tengingarinnar.

* Engin samvörun fannst fyrir reitina sem tilgreindir eru í samsvörunarskilyrðinu

    Endurtaktu tenginguna með því að nota aðra reiti.

* Margar samsvaranir fundust fyrir ýmsar færslur út frá reitunum sem tilgreindir eru í samsvörunarskilyrðinu  

    Endurtaktu tenginguna með því að nota aðra reiti.

* Samsvörun fannst en færslan er þegar tengd við færslu í [!INCLUDE [prod_short](includes/prod_short.md)]  

    Endurtaktu tenginguna með því að nota aðra reiti eða kannaðu hvers vegna þessi [!INCLUDE [cds_long_md](includes/cds_long_md.md)] eining er tengd við færsluna í [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> Til að veita þér betri yfirsýn yfir framvindu tengingarinnar sýnir reiturinn **Tengt við Dataverse** hvort færsla sé tengd við [!INCLUDE [cds_long_md](includes/cds_long_md.md)] einingu. Hægt er að nota reitinn **Tengt við Dataverse** til að sía listann yfir færslur sem verið er að samstilla.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Uppfæra tengingar frá Business Central á netinu til að nota sannvottorð

> [!NOTE]
> Þessi hluti á aðeins við fyrir leigjendur [!INCLUDE[prod_short](includes/prod_short.md)] á netinu sem eru hýstir hjá Microsoft. Það hefur engin áhrif á leigjendur á netinu sem eru hýstir hjá óháðum hugbúnaðarsölum og uppsetningar á staðnum.

Í apríl 2022 mun [!INCLUDE[cds_long_md](includes/cds_long_md.md)] taka úr umferð auðkenningarleið Office365 (notandanafn/lykilorð). Frekari upplýsingar er að finna í [Auðkenningarleið Office365 tekin úr umferð](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). Auk þess mun [!INCLUDE[prod_short](includes/prod_short.md)] í mars 2022 taka úr umferð notkun auðkenningu milli þjónusta sem byggir á leyniorði biðlara fyrir leigjendur á netinu. Þú verður að nota auðkenningu milli þjónusta sem byggir á vottorði fyrir tengingar við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Leigjendur [!INCLUDE[prod_short](includes/prod_short.md)] á netinu sem óháðir hugbúnaðarsalar hýsa og uppsetningar á staðnum geta haldið áfram að nota auðkenningu með leyniorði biðlara.

Til að koma í veg fyrir truflanir á samþættingum _verður að uppfæra_ tenginguna til að nota auðkenningu sem byggir á skilríki. Þó að breytingin sé áætluð mars 2022 mælum við eindregið með því að þú uppfærir eins fljótt og auðið er. Eftirfarandi skref útskýra hvernig á að uppfæra auðkenningu með skilríkjum. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Til að uppfæra nettengingu við Business Central til að nota auðkenningu með skilríkjum

1. Gerðu eitt af eftirfarandi ef þú samþættar við Dynamics 365 Sales:
   * Ef þú gerir það skaltu opna **Microsoft Dynamics Uppsetningarsíðu 365**.
   * Ef ekki skaltu opna **Dataverse Uppsetningarsíðu**.
2. Veldu **Tenging** og síðan **Nota sannvottun vottorðs** til að uppfæra tenginguna til að nota sannvottun sem byggir á vottorði.
3. Skráðu þig inn með innskráningarupplýsingum stjórnanda fyrir Dataverse. Innskráning ætti að taka innan við mínútu.

> [!NOTE]
> Þú verður að endurtaka þessi skref í hverju [!INCLUDE[prod_short](includes/prod_short.md)] umhverfi, þar á meðal bæði framleiðslu- og sandkassaumhverfi, og í hverju fyrirtæki þar sem þú tengist [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Tenging útgáfur innanhúss

Til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] þarf að gefa upp upplýsingar á síðunni **Dataverse Uppsetning tengingar**.

Til að tengjast með reikningi Microsoft Entra verður að skrá forrit í Microsoft Entra kenni. Þú þarft að framvísa auðkenni forritsins, leynilykli lyklageymslu og vefslóð framsendingar sem á að nota. Framsend vefslóð er fyllt út fyrirfram og ætti að virka fyrir flestar uppsetningar. Nauðsynlegt er að setja upp uppsetninguna til að nota HTTPS. Frekari upplýsingar er að finna í [Skilgreining SSL til að tryggja örugga tengingu vefbiðlara Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Ef verið er að setja upp þjóninn til að hafa aðra heimasíðu er hægt að breyta vefslóðinni. Leynilykill biðlara verða vistaður sem dulkóðaður strengur í gagnagrunninum. 

### <a name="to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-dataverse"></a>Til að skrá forrit í Microsoft Entra kenni til tengingar frá Business Central til Dataverse

Eftirfarandi skref gera ráð fyrir því að kenni séu notuð Microsoft Entra til að vinna með auðkenni og aðgang. Nánari upplýsingar um skráningu forrits í auðkenni eru Microsoft Entra í [Quickstart: Skráðu forrit á kennivettvang Microsoft](/azure/active-directory/develop/quickstart-register-app). 

1. Í Azure-gáttinni, undir **Stjórna** á yfirlitssvæðinu, skal velja **Sannvottun**.  
2. Undir **Framsenda vefslóðir** skal bæta við framsendingarvefslóð sem mælt er með á síðunni **Dataverse Uppsetning tengingar** í [!INCLUDE[prod_short](includes/prod_short.md)].
3. Undir **Stjórna** skal velja **API-heimildir**.
4. Undir **Skilgreindar heimildir** skal velja **Bæta við heimild** og síðan bæta við úthlutuðum heimildum í flipanum **Microsoft API** á eftirfarandi hátt:
    * Fyrir Business Central skal bæta við heimildunum **Financials.ReadWrite.All**.
    * Fyrir Dynamics CRM skal bæta við heimildunum **user_impersonation**.  

    > [!NOTE]
    > Heiti Dynamics CRM API gæti breyst.

5. Undir **Stjórna** skal velja **Vottorð og leynilyklar** og síðan stofna nýjan leynilykil fyrir forritið. Leynilykillinn verður notaður annaðhvort í [!INCLUDE[prod_short](includes/prod_short.md)], í reitnum **Leynilykill biðlara** á síðunni **Dataverse Uppsetning tengingar** eða geymdur í öruggri geymslu og hann látinn í té í áskriftartilviki eins og lýst var fyrr í þessu efnisatriði.
6. Veljið **Yfirlit** og finnið svo gildið **Auðkenni forrits (biðlara)**. Þetta auðkenni er biðlarakenni forritsins. Færa verður það inn annaðhvort á síðunni **Dataverse Uppsetning tengingar** í reitnum **Biðlarakenni** eða geyma það í öruggri geymslu og láta það í té í áskriftartilviki.
7. Í [!INCLUDE[prod_short](includes/prod_short.md)], á síðunni **Dataverse Uppsetning tengingar**, í reitnum **Vefslóð umhverfis**, skal færa inn vefslóðina fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-umhverfið.
8. Til að virkja tenginguna við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] þarf að kveikja á víxlhnappnum **Virkjað**.
9. Skráðu þig inn með kerfisstjórareikningnum þínum fyrir Microsoft Entra auðkenni (þessi reikningur verður að hafa gilda leyfi fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og vera stjórnandi í umhverfi þínu [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ). Eftir að þú skráir þig inn verður þú beðinn um að leyfa skráða forritinu þínu að skrá sig inn í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] fyrir hönd fyrirtækisins. Veita þarf samþykki til að ljúka uppsetningunni.

   > [!NOTE]
   > Ef þú ert ekki beðinn um að skrá þig inn með stjórnandareikningnum þínum, er það líklega vegna þess að lokað er fyrir sprettiglugga. Til að skrá þig inn skaltu leyfa sprettiglugga úr `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-"></a>Að aftengjast [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Dataverse Uppsetning tengingar** og velja síðan viðkomandi tengil.
2. Á síðunni **Dataverse Uppsetning CDS-tengingar** skal slökkva á víxlhnappnum **Virkjað**.  

## <a name="see-also"></a>Sjá einnig

[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
