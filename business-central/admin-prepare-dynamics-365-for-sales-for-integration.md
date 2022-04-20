---
title: Samþætting við Dynamics 365 Sales
description: Kynntu þér hvernig þú sækir Dynamics 365 Business Central tilbúið til að samþætta við Dynamics 365 Sales.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 86ca61b19495269d90597e7f050c92bb935099e1
ms.sourcegitcommit: 55f42d2407e109b4924218cb22129467b53deb08
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557276"
---
# <a name="integrating-with-dynamics-365-sales"></a>Samþætting við Dynamics 365 Sales

Hlutverk sölumannsins er oft talið sýnilegasti hlutinn í viðskiptum. Hins vegar getur það gagnast sölumönnum að geta fengið innsýn í viðskiptin og séð hvað er að gerast á bak við tjöldin. Með því að samþætta [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] er hægt að gefa sölufólki þínu þessi innsýn. Sameining mun láta fólk Skoða upplýsingar í á [!INCLUDE[prod_short](includes/prod_short.md)] meðan þeir eru að vinna í [!INCLUDE[crm_md](includes/crm_md.md)]. Þegar sölutilboð er undirbúið getur það til dæmis verið gagnlegt að vita hvort nægar birgðir séu til staðar til að uppfylla pöntunina. Frekari upplýsingar [fást í use Dynamics 365 Sala frá Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Þetta efnisatriði útskýrir ferlið við samþættingu á vefútgáfum af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar um grunnstillingu á staðnum er að finna í [Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-dataverse"></a>Samþætting í gegnum Dataverse
Til að auðvelda tengingu og samstillingu gagna með öðrum Dynamics 365 er [!INCLUDE[prod_short](includes/prod_short.md)] einnig samþætt [!INCLUDE[prod_short](includes/cds_long_md.md)]. Þú getur til dæmis tengst við [!INCLUDE[crm_md](includes/crm_md.md)], eða jafnvel apps sem þú smíðar sjálfur. Ef þú ert að samþætta í fyrsta sinn þarf að gera það í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Dataverse](admin-common-data-service.md).

Ef þú hefur þegar samþætt [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að halda áfram að samstilla gögn með uppsetningarforritinu. Ef þú hins vegar uppfærir eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)] til að kveikja á henni aftur. Frekari upplýsingar er að finna í [Uppfærsla samþættingar við Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Endurtenging um [!INCLUDE[prod_short](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar. Til dæmis verða sjálfgefnar töfluvarpanir notaðar.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Stillingar samþættingar sem eiga sérstaklega við um [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingu
Samþætting með [!INCLUDE[prod_short](includes/prod_short.md)] gerist [!INCLUDE[prod_short](includes/cds_long_md.md)] og margar staðlaðar stillingar og töflur eru gefnar upp. Ásamt stöðluðum stillingum, eru nokkrar sem eiga sérstaklega við um [!INCLUDE[crm_md](includes/crm_md.md)]. Í eftirfarandi köflum er listi yfir þessar stillingar.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Heimildir og öryggishlutverk fyrir notandareikninga í Sales
Þegar samþættingarlausnin er sett upp eru heimildir fyrir notandareikning samþættingar grunnstilltar. Ef þeim heimildum er breytt gæti þurft að endurstilla þær. Hægt er að gera það með því að setja samþættingarlausnina upp aftur eða velja **Endurvirkja samþættingarlausn** á síðunni **Uppsetning Dynamics 365-tengingar**. Eftirfarandi öryggishlutverk eru virkjuð:

* Dynamics 365 Business Central Samþættingarstjórnandi
* Dynamics 365 Business Central Samþættingarnotandi
* Dynamics 365 Business Central Notandi afurðaframboðs

### <a name="connection-settings-in-the-setup-guide"></a>Tengingarstillingar í uppsetningarleiðbeiningum
Hægt er að nota uppsetningarleiðbeiningar með hjálp til að setja upp tenginguna á fljótvirkan hátt og tilgreina ítarlega eiginleika, t.d. tengingu milli færslna.

1. Veldu **Uppsetning og viðbætur** og veldu síðan **Uppsetning með hjálp**.
2. Veldu **Setja upp Dynamics 365 Sales tengingu** til að hefja leiðbeiningar um uppsetningu með hjálp.
3. Fyllið inn reitina eftir þörfum.
4. Að öðrum kosti eru ítarlegar stillingar sem auka öryggi og virkja meiri getu. Eftirfarandi tafla lýsir ítarlegum stillingum.  

| Svæði | Lýsing |
|--|--|
| **Flytja inn Dynamics 365 Sales Solution** | Setja upp og samskipa samþættingarlausnina í [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Samstilla vöruframboð sjálfkrafa**|Tilgreinir að raða verði vinnslubiðröð vöru. Vinnsluröðin keyrir á 30 mínútna fresti og uppfærir framkomnar vörur á afsláttarmiðuðum vörum.|
| **Virkja samþættingu sölupöntunar** | Þegar fólk stofnar sölupantanir í [!INCLUDE[crm_md](includes/crm_md.md)] og fullnægir pöntunum í [!INCLUDE[prod_short](includes/prod_short.md)] er þessi stilling samþætt ferlinu í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna á [Virkja sölupöntunarferli samþættingar](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Nauðsynlegt er að gefa upp skilríki fyrir notandareikning stjórnanda í [!INCLUDE[crm_md](includes/crm_md.md)]. Nánari upplýsingar er að finna í [Meðhöndlun á gögnum sölupöntunar](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
|**Virkja Dynamics 365 Sales Connection** | Virkja tenginguna við [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Dynamics 365 SDK útgáfa** | Þetta á aðeins við ef samþætt er innanhússútgáfa af [!INCLUDE[crm_md](includes/crm_md.md)]. Þessi SDK er Dynamics 365 hugbúnaðarþróunarkit (einnig nefnt Xrm) sem þú notar til að tengjast [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[crm_md](includes/crm_md.md)]. Útgáfan verður að vera samhæf SDK-útgáfunni sem notuð er af [!INCLUDE[crm_md](includes/crm_md.md)] og sú sama eða nýrri og útgáfan sem er notuð af [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Stillingar tengingar á Uppsetning tengingar  Microsoft Dynamics 365

Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)].

| Svæði | Lýsing |
|--|--|
|**Dynamics 365 Sales vefslóð**|Vefslóð fyrir [!INCLUDE[crm_md](includes/crm_md.md)]-tilvikið þitt. Þessi stilling leyfir notendum að opna færslurnar í [!INCLUDE[prod_short](includes/prod_short.md)] sem samsvara færslum í [!INCLUDE[crm_md](includes/crm_md.md)]. Til dæmis lykil eða afurð. [!INCLUDE[prod_short](includes/prod_short.md)]-færslur opnast í [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Samstilla vöruframboð sjálfkrafa**|Tilgreinir að raða verði vinnslubiðröð vöru. Vinnsluröðin keyrir á 30 mínútna fresti og uppfærir framkomnar vörur á afsláttarmiðuðum vörum.|
|**Dynamics 365 SDK útgáfa**|Ef þú ert að samþætta með innanhússútgáfu af [!INCLUDE[crm_md](includes/crm_md.md)] er þetta Dynamics 365 hugbúnaðarþróunarkit (einnig nefnt Xrm) sem þú notar til að tengjast [!INCLUDE[prod_short](includes/prod_short.md)][!INCLUDE[crm_md](includes/crm_md.md)] við. Útgáfan sem var valin verður að vera samhæf SDK-útgáfunni sem notuð er af [!INCLUDE[crm_md](includes/crm_md.md)]. Þessi útgáfa sem er til jafns á við eða nýrri en útgáfan sem er notuð af [!INCLUDE[crm_md](includes/crm_md.md)].|

Auk ofangreindra stillinga skal færa inn eftirfarandi stillingar fyrir [!INCLUDE[crm_md](includes/crm_md.md)].

| Svæði | Description |
|--|--|
| **Kveikt er á samþættingu sölupöntunar** | Gerðu notendum kleift að senda inn sölupantanir og virkjuð tilboð í [!INCLUDE[crm_md](includes/crm_md.md)] og síðan skoða og vinna úr þeim í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi stilling samþætir ferlinu í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna á [Virkja sölupöntunarferli samþættingar](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Stofna sölupantanir sjálfvirkt** | Stofna sölupöntun í [!INCLUDE[prod_short](includes/prod_short.md)] þegar notandi stofnar og sendir inn eina í [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Vinna sölutilboð sjálfkrafa** | Vinna úr sölutilboði í [!INCLUDE[prod_short](includes/prod_short.md)] þegar notandi stofnar og virkjar eitt slíkt í [!INCLUDE[crm_md](includes/crm_md.md)]. Nánari upplýsingar er að finna í [Meðhöndlun á gögnum sölutilboðs](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Samhæfa Synch sölupantana**|Samstilla sölupantanir í báðar áttir. Ef viðskiptavinur breytir til dæmis hugarfari sínu um vöruna eða magnið sem þeir pöntuðu í [!INCLUDE[crm_md](includes/crm_md.md)] er hægt að útvista söluskjalið og stofna nýtt í [!INCLUDE[prod_short](includes/prod_short.md)]. Sama gildir um breytingar skv [!INCLUDE[prod_short](includes/prod_short.md)]. Til dæmis, þegar verð, skattaupphæðir eða áætlaðar sendingardagsetningar breytast breytist breytingarnar sjálfkrafa í [!INCLUDE[crm_md](includes/crm_md.md)]. Með tvískipaðri samstillingu halda seljendur upp á nýjustu breytingar og stöðu tilboða og pantana.|

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Stöðluð einingavörpun Sales fyrir samstillingu

Einingar í [!INCLUDE[crm_md](includes/crm_md.md)], t.d. pantanir, eru samþættar við jafngildar gerðir af töflunum í [!INCLUDE[prod_short](includes/prod_short.md)], t.d. sölupantanir. Til að vinna með [!INCLUDE[crm_md](includes/crm_md.md)]-gögn eru tenglar settir upp, kallast tengingar, milli tafla í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

Eftirfarandi töflur birta staðlaða vörpun milli tafla í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] sem [!INCLUDE[prod_short](includes/prod_short.md)] veitir.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Stefna samstillingar | Sjálfgefin sía |
|--|--|--|--|
| Mælieining | Einingarflokkur | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Vara | Vara | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Tengiliðasía Sales: **Gerð afurðar** er **Birgðir Sales** |
| Forði | Vara | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Tengiliðasía Sales: **Gerð afurðar** er **Þjónusta** |
| Mælieiningarstuðull vöru | CRM UOM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Mælieining forða | CRM UOM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Einingarflokkur | CRM Uomschedule | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Verðflokkur viðskiptamanna | Verðlisti | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Söluverð | Verðlisti vöru | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] Afmörkun tengiliðar: **kóti** sölu er ekki auður, **Tegund** sölu er **Verðflokkur viðskiptamanna** |
| Tækifæri | Tækifæri | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Sölureikningshaus | Reikningsfæra | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Sölureikningslína | Reikningsfæra vöru | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Sölupöntunarhaus | Sölupöntun | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Ef samstilla á í báðar áttir verður að kveikja á **Tvískipaðri Synch-Sölupöntunarsölupöntunum** á **síðunni Dynamics 365-tengingaruppsetningarsíðu**.| [!INCLUDE[prod_short](includes/prod_short.md)] Sía söluhauss: **Gerð skjals** er Pöntun, **Staða** er útgefin |
| Athugasemdir sölupöntunar | Athugasemdir sölupöntunar | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Varpanir fyrir mælieiningu vöru, mælieiningu tilfangs og töflur einingahóps eru aðeins í boði ef stjórnandinn hefur kveikt á eiginleikanum **Eiginleikauppfærsla: margar einingar til að mæla samstillingu með Dynamics 365 Sales** á síðunni **Eiginleikastjórnun**. Frekari upplýsingar er að finna í [Vörur og tilföng samstillt við afurðir í öðrum mælieiningum](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronizing-items-and-resources-with-products-with-different-units-of-measure).

## <a name="synchronizing-items-and-resources-with-products-with-different-units-of-measure"></a>Vörur og tilföng samstillt við afurðir með öðrum mælieiningum
Fyrirtæki framleiða oft eða kaupa vörurnar í einni mælieiningu og selja þær svo í öðrum. Til að samstilla vörur sem nota margar mælieiningar þarf að kveikja á eiginleikanum **Eiginleikauppfærsla: margar einingar til að mæla samstillingu með Dynamics 365 Sales** á síðunni **Eiginleikastjórnun**. 

Þegar kveikt er á aðgerðinni uppfæra er Taflan ný Einingaflokkur stofnuð og úthlutuð hverri vöru og tilfang í [!INCLUDE[prod_short](includes/prod_short.md)]. Í töflunum er hægt að varpa einingaflokki, mælieiningu vöru, og mælieiningatöflum í [!INCLUDE[prod_short](includes/prod_short.md)] í Dynamics 365 flokk sölueiningarinnar í [!INCLUDE[crm_md](includes/crm_md.md)]. Eftirfarandi mynd sýnir varpanir.

:::image type="content" source="media/unit group 1.png" alt-text="Töfluvarpanir fyrir einingahópa":::

Hægt er að búa til margar mælieiningar fyrir hvern einingahóp og úthluta hópunum á afurðir í [!INCLUDE[crm_md](includes/crm_md.md)]. Þar á eftir geturðu samstillt afurðirnar við vörur og tilföng í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að tengja mælieiningar vöru eða tilfangs við einingahóp. Þegar það er gert, ef einingaflokkur fyrir vöruna eða tilfang er ekki miðaðir við einingaflokk í [!INCLUDE[crm_md](includes/crm_md.md)], til dæmis vegna þess að einingaflokkur var ekki til, [!INCLUDE[prod_short](includes/prod_short.md)] stofnar sjálfkrafa einingarflokkinn í [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="mapping-items-and-resources-to-products"></a>Varpa vörum og tilföngum í afurðir
Þegar kveikt er á eiginleikanum **Eiginleikauppfærsla: margar einingar til að mæla samstillingu með Dynamics 365 Sales** gerist eftirfarandi:

* Nýjar varpanir eru búnar til fyrir vörur og tilföng.
* Fyrirliggjandi vörpunum er eytt. <!--which mappings?-->
* Gagnauppfærsla býr til einingahópa fyrir vörur og tilföng.

Til að nota nýju varpanirnar þarf að samstilla einingahópa, mælieiningu vöru og mælieiningu tilfangs. Einnig þarf að endursamstilla vörur og tilföng. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] leyfir þér ekki að breyta einingahópi fyrir afurð. Þess vegna þarf að taka afurðirnar úr umferð og aftengja vörur og tilföng og síðan samstilla með því að búa til nýjar afurðir í [!INCLUDE[crm_md](includes/crm_md.md)]. 

Eftirfarandi skref lýsa skrefunum til að hefja vörpun einingahópa:

1. Gætið þess að vörur [!INCLUDE[crm_md](includes/crm_md.md)] sem eru ekki afsláttarvörur eða tilföng séu í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef þær eru skal fara á **síðurnar** og/eða **forða** og nota síuvalkosti til að velja kostnaðarsömu færslur. Veldu **síðan Dynamics 365 söluaðgerðina** og veldu **afpar**. Þessi aðgerð raðar bakvinnslu á ófáar færslur. Á meðan verkið er í gangi er hægt að athuga stöðu þess með því að nota aðgerðina **Samstillingarkladdi**. Frekari upplýsingar er að finna í [Tenging og samstilling](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Þar sem nýjar afurðir verða stofnaðar í [!INCLUDE[crm_md](includes/crm_md.md)] með nýjum einingarflokkum, til að forðast tvíteknar heiti, skal gera eina af eftirfarandi skrefum:
    
    * Endurnefndu afurðirnar og taka þær svo úr umferð í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Taka afurðir úr umferð (sölumiðstöð)](/dynamics365/sales-enterprise/retire-product). Til að magnbreyta afurðum notanda inn Microsoft Excel, skrá Power Apps þær inn, velja umhverfi, fara í **afurðatöflu** og velja **svo flipann gögn** . hreinsa síur sem er beitt. Í hópnum **Gögn** skal velja aðgerðina **Breyta gögnum í Excel**. Bættu forskeyti eða viðskeyti við tengdar afurðir og taktu þær svo úr umferð.
    * Taktu afurðirnar úr umferð og eyddu þeim. 

3. Fylgdu þessum skrefum til að samstilla **Einingahópa**, **Mælieiningar**, **Vörur** og **Tilföng**:
    1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna síðuna **Uppsetning tengingar fyrir Dynamics 365 Sales**.
    2. Notaðu aðgerðina **Keyra fulla samstillingu** til að opna síðuna **Dataverse Yfirfara fulla samstillingu**.
    3. Fyrir varpanirnar **VARA UOM**, **TILFANG UOM** OG **EININGAHÓPUR** skal velja aðgerðina **Ráðleggja fulla samstillingu**.
    4. Veldu aðgerðina **Samstilla allt**.

    > [!NOTE]
    > Þessi aðgerð mun samstilla að fullu þær varpanir sem hafa ekki verið samstilltar að fullu hingað til. Til að koma í veg fyrir að þessar varpanir verði samstilltar skal eyða vörpunum af síðunni. Þetta fjarlægir þær aðeins úr núverandi fullri samstillingu og eyðir ekki vörpununum.
    
5. Veldu vörpunina **VARA-AFURÐ** og síðan aðgerðina **Endurræsa**. Endurræsingu stofnar nýjar afurðir úr vörunum í [!INCLUDE[crm_md](includes/crm_md.md)] og úthlutar nýjum einingaflokki sem er tiltekinn fyrir vöruna.
6. Veldu vörpunina **TILFANG-AFURÐ** og síðan aðgerðina **Endurræsa**. Endurræst stofnar nýjar afurðir úr tilföngum í [!INCLUDE[crm_md](includes/crm_md.md)] og úthlutar nýjum einingaflokki sem er sérstaklega fyrir tilföng.

### <a name="synchronization-rules"></a>Samstillingarreglur

Í eftirfarandi töflu eru taldar upp reglurnar sem stjórna samstillingu milli [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)]. Þessar reglur eru auk reglna skilgreindar fyrir Dataverse, sem einnig gilda. Frekari upplýsingar er að finna í [Stöðluð einingavörpun](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Breytingar á gögnum í  sem voru gerðar af notandareikningi samþættingar eru ekki samstilltar. Mælt er með því að gögnum sé ekki breytt á meðan reikningurinn er notaður. Nánari upplýsingar er að finna í [Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tafla|Regla|
|-----|----|
|Mælieiningar|Mælieiningar eru samstillar við einingahópa í [!INCLUDE[crm_md](includes/crm_md.md)]. Aðeins er hægt að skilgreina eina mælieiningu í einingahópnum.|
|Birgðir|Þegar vörur eru samstilltar við [!INCLUDE[crm_md](includes/crm_md.md)]-vörur mun [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa stofna verðlista í [!INCLUDE[crm_md](includes/crm_md.md)]. Til að forðast Samstillingarvillur ætti ekki að breyta þessari Verðskrá handvirkt.|
|Forðar|Tilföng eru samstillt við vörur [!INCLUDE[crm_md](includes/crm_md.md)] sem hafa þjónustu sem vörugerðina.|
|Verðflokkar viðskm.|Verðflokkar viðskiptavinar eru samstilltir við verðlista Sales.|
|Söluverð|Söluverð sem eru með verðflokk viðskiptavinar sem sölugerð og eru með skilgreindan sölukóða eru samstillt við verðlistalínur [!INCLUDE[crm_md](includes/crm_md.md)]|
|Tækifæri|Tækifæri eru samstillt við tækifæri [!INCLUDE[crm_md](includes/crm_md.md)]. Gildið á kóða sölumanns skilgreinir eiganda tengdu töflunnar í [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bókaðir sölureikningar|Bókaðir sölureikningar eru samstilltir við sölureikninga. Áður en hægt er að samstilla reikning er betra að samstilla allar aðrar töflur sem geta tekið þátt í reikningnum, frá sölumannalista yfir í verðlistum. Gildið á kóða sölumanns í fyrirsögn reiknings skilgreinir eiganda tengdu töflunnar í Sales.|
|Sölupantanir|Þegar sölupöntun er virkjuð verða sölupantanir í [!INCLUDE[prod_short](includes/prod_short.md)] sem eru stofnaðar úr sendum sölupöntunum [!INCLUDE[crm_md](includes/crm_md.md)] samstilltar með sölupöntunum í [!INCLUDE[crm_md](includes/crm_md.md)] þegar þær eru losaðar. Áður en þú samstillir pantanir mælum við með að þú samstillir fyrst allar töflurnar sem koma við sögu í pöntuninni, t.d. sölufólk og verðlistar. Kóðareitur sölumanns í pöntunarhaus skilgreinir eiganda tengdu töflunnar í [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Samstillingarverk fyrir samþættingu Sales

Verkin eru keyrð í eftirfarandi röð til að koma í veg fyrir tengsl tenginga milli taflanna. Fleiri störf eru í boði frá Dataverse kl. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](./admin-job-queues-schedule-tasks.md).

1. UNITOFMEASURE-samstillingarvinnsla Dynamics 365 Sales  
2. TILFÖNG-AFURÐ fyrir samstillingarvinnslu Dynamics 365 Sales  
3. ITEM-PRODUCT - Dynamics 365 Sales samstillingarverk  
4. CUSTPRCGRP-VERÐ í samstillingarvinnslu Dynamics 365 Sales.
5. SALESPRC-PRODPRICE - Dynamics 365 Sales samstillingarvinnsla.
6. POSTEDSALESINV-INV - Dynamics 365 Sales samstillingarvinnsla.

### <a name="default-synchronization-job-queue-entries"></a>Sjálfgefnar Verkraðarfærslur samstillingar

Eftirfarandi tafla lýsir sjálfgefnu samstillingarverkunum fyrir Sales.  

|Verkraðarfærsla|Description|Stefna|Vörpun samþættingartöflu|Sjálfgefin tíðni samstillinga (mín)|Sjálfgefinn hvíldarstaða vegna aðgerðarleysis (mín.)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|UNITOFMEASURE-samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] einingahópa við [!INCLUDE[prod_short](includes/prod_short.md)] mælieiningar.|Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÆLIEINING|30|720<br> (12 klst.)|
|TILFÖNG-AFURÐ fyrir samstillingarvinnslu Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] vörur við [!INCLUDE[prod_short](includes/prod_short.md)] tilföng.|Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|TILFÖNG-VARA|30|720<br> (12 klst.)|
|VARA-AFURÐ- samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] vörur við [!INCLUDE[prod_short](includes/prod_short.md)] atriði.|Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|ATRIÐI-VARA|30|1440<br> (24 klst.)|
|CUSTPRCGRP-VERÐ í samstillingarvinnslu Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] söluverðlista við [!INCLUDE[prod_short](includes/prod_short.md)] verðflokka viðskiptamanns.| |VERÐFLOKKAR VIÐSKIPTAMANNS-LISTAR SÖLUVERÐS|30|1440<br> (24 klst.)|
|SALESPRC-PRODUCTPRICE-samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] afurðarverð við [!INCLUDE[prod_short](includes/prod_short.md)] söluverð.||AFURÐARVERÐ-SÖLUVERÐ|30|1440<br> (24 klst.)|
|POSTEDSALESINV-INV-Dynamics 365 Sales samstillingarvinnsla|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga við [!INCLUDE[prod_short](includes/prod_short.md)] bókaða sölureikninga.|Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|REIKNINGAR-BÓKAÐIR SÖLUREIKNINGAR|30|1440<br> (24 klst.)|
|Talnagögn viðskiptavinar - samstillingarvinnsla Dynamics 365 Sales|Uppfærir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga með nýjustu [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamannagögnunum. Í [!INCLUDE[crm_md](includes/crm_md.md)] birtast upplýsingarnar í **Tölfræði fyrir Business Central-reikning** skjámynd flýtiyfirlits yfir reikninga sem eru tengdir við [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamenn.<br /><br /> Einnig er hægt að uppfæra þessi gögn handvirkt úr hverri viðskiptamannafærslu. Frekari upplýsingar er að finna í [Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Athugið:** Þessi verkraðarfærsla á aðeins við ef [!INCLUDE[prod_short](includes/prod_short.md)] samþættingarlausnin er sett upp í [!INCLUDE[crm_md](includes/crm_md.md)]. |Á ekki við|Á ekki við|30|Á ekki við| 

## <a name="connecting-to-on-premises-versions-of-business-central-2019-release-wave-1-and-microsoft-dynamics-nav-2018"></a>Tenging við staðbundnar útgáfur af Business Central 2019 útgáfutímabil 1 og Microsoft Dynamics NAV 2018
Microsoft Power Platform Teymið hefur [tilkynnt](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) að það sé að afskrifa Office365-sannvottunargerðina. Ef þú ert að nota útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss sem er á undan en Business Central 2019 út Wave 1, verður að nota sannvottunargerðina OAuth til að tengjast [!INCLUDE[crm_md](includes/crm_md.md)] netinu. Skrefin í þessum hluta lýsa því hvernig á að tengjast eftirfarandi útgáfum af vöru:

* Útgáfutímabil 1 af Business Central 2019
* Microsoft Dynamics NAV 2018

### <a name="prerequisites"></a>Frumskilyrði

- Nauðsynlegt er að vera með Microsoft Azure-áskrift. Prufureikningur virkar fyrir forritsskráningu.
- [!INCLUDE[crm_md](includes/crm_md.md)] er grunnstillt til að nota eina af eftirfarandi sannvottunargerðum:

   - Office365 (eldra)

     > [!IMPORTANT]
     > Gildir frá apríl 2022, Office365 (eldra) verður ekki lengur stutt. Frekari upplýsingar eru í [Mikilvægar breytingar (afskriftir) væntanlegar í Power Apps, Power Automate og viðskiptavinaforritum](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   - OAuth

### <a name="to-connect-business-central-2019-release-wave-1-and-dynamics-nav-2018"></a>Til að tengja Business Central 2019 útgáfutímabil 1 og Dynamics NAV 2018

1. Flytjið samþættingarlausn Microsoft Dynamics 365 Business Central inn í [!INCLUDE[crm_md](includes/crm_md.md)]-umhverfið. Samþættingarlausnin er í boði í möppunni CrmCustomization á DVD-uppsetningardisknum fyrir [!INCLUDE[prod_short](includes/prod_short.md)] eða Dynamics NAV 2018. Innflutningur er ein af eftirfarandi lausnum, allt eftir útgáfu afurðar:

   * Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur mappan DynamicsNAVIntegrationSolution_v9 og DynamicsNAVIntegrationSolution_v91. lausnir. Lausnin sem þú ættir að flytja inn veltur á þeirri útgáfu af [!INCLUDE[crm_md](includes/crm_md.md)] sem verið er að tengjast. [!INCLUDE[crm_md](includes/crm_md.md)] á netinu þarf samþættingarlausnina DynamicsNAVIntegrationSolution_v91.
   * Fyrir Dynamics NAV 2018 skal setja upp DynamicsNAVIntegrationSolution-lausnina.

2. Stofnið ógagnvirkan samþættingarnotanda í [!INCLUDE[crm_md](includes/crm_md.md)]-umhverfinu og úthlutið notandanum eftirfarandi öryggishlutverkum. Frekari upplýsingar er að finna í [Stofna ógagnvirkan notandareikning](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central Samþættingarstjórnandi
   * Dynamics 365 Business Central Samþættingarnotandi

   > [!Important]
   > Þessi notandi má ekki hafa öryggishlutverk kerfisstjóra. Einnig er ekki hægt að nota reikning kerfisstjóra sem samþættingarnotanda.

3.  Í Azure-gáttinni skal búa til forritsskráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Skrá forrit í Azure Active Directory](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Mælt er með að forrið sé skráð í sama leigjanda og Dataverse-umhverfið þannig að ekki þurfi að samþykkja aðgang forritsins að umhverfinu. Ef þú skráir forritið í öðru umhverfi þarf að skrá sig inn í Azure AD með stjórnandareikningnum fyrir Dataverse-umhverfið og veita samþykki.
   >
   > Auk þess má forritið sem þú skráir ekki vera með leynilykil. Að tengja forrit með leynilykli við Dataverse er aðeins í boði í Business Central 2020 útgáfutímabili 1 og síðar.
  
4. Gerið eina af eftirfarandi skrefum, allt eftir vöruútgáfunni:

    * Í [!INCLUDE[prod_short](includes/prod_short.md)] skal leita að **Microsoft Dynamics 365 uppsetning tengingar** og síðan velja viðkomandi tengil. 
    * Í Dynamics NAV 2018 skal leita að **Microsoft Dynamics 365 for Sales Uppsetning tengingar** og síðan velja viðkomandi tengil.

5. Í reitnum **Sannvottunargerð**, skal velja valkostinn fyrir OAuth. 
6. Veljið SDK-útgáfu CRM sem samsvarar úrlausnarútgáfu sem flutt var inn í skrefi 1.

   > [!NOTE]
   > Þetta skref á aðeins við fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

7. Sláið inn vefslóð [!INCLUDE[crm_md](includes/crm_md.md)]-umhverfisins og sláið síðan inn notandanafn og aðgangsorð fyrir samþættingarnotandann. 

   * Í [!INCLUDE[prod_short](includes/prod_short.md)] skal nota reitinn **Vistfang þjóns**.
   * Í Dynamics NAV 2018 skal nota reitinn **Vefslóð Dynamics 365 Sales**.

8. Í reitinn **Tengistrengur** skal tilgreina auðkenni forritsskráningarinnar. Þessi reitur er með tveimur merkjum þar sem tilgreina þarf kenni forrits.

   |Tákn           |Description  |
   |----------------|-------------|
   |**AppId**       |Stillið forritskennið.      |
   |**RedirectUri** |Stillið forritskennið, en bætið við **app://** forskeytinu.         |

    **Dæmi** Eftirfarandi dæmi sýnir tengistreng.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Virkjaðu tenginguna.

> [!Note]
> Ef þú vilt skilgreina tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]-tilvik með tiltekinni gerð sannvottunar skaltu fylla út reitina á flýtiflipanum **Upplýsingar um sannvottunargerð**. Frekari upplýsingar eru í [Sannvottun með Microsoft Dataverse vefþjónustu](/powerapps/developer/data-platform/authentication). Ekki er krafist þessa skrefs þegar tengd er netútgáfa af [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Sjá einnig

[Uppsetning á notendareikningum fyrir samþættingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sérstilling Business Central og [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
