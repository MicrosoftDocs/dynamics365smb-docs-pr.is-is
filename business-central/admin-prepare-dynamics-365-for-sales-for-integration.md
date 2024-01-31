---
title: Samþætting við Dynamics 365 Sales
description: Kynntu þér hvernig þú sækir Dynamics 365 Business Central tilbúið til að samþætta við Dynamics 365 Sales.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 12/15/2023
ms.author: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Samþætting við Dynamics 365 Sales

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Hlutverk sölumannsins er oft talið sýnilegasti hlutinn í viðskiptum. Hins vegar getur það gagnast sölumönnum að geta fengið innsýn í viðskiptin og séð hvað er að gerast á bak við tjöldin. Með því að samþætta [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] geturðu veitt sölumönnum þínum þessa innsýn. Samþættingin gerir fólki kleift að skoða upplýsingar í [!INCLUDE[prod_short](includes/prod_short.md)] á meðan það er að vinna í [!INCLUDE[crm_md](includes/crm_md.md)]. Þegar sölutilboð er undirbúið getur það til dæmis verið gagnlegt að vita hvort nægar birgðir séu til staðar til að uppfylla pöntunina. Frekari upplýsingar er að finna í [Nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Þetta efnisatriði útskýrir ferlið við samþættingu á vefútgáfum af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar um grunnstillingu á staðnum er að finna í [Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## Samþætta í gegnum Dataverse

Til að auðvelda tengingu og samstillingu gagna við önnur Dynamics 365-forrit samþættist [!INCLUDE[prod_short](includes/prod_short.md)] einnig við [!INCLUDE[prod_short](includes/cds_long_md.md)]. Til dæmis er hægt að tengjast [!INCLUDE[crm_md](includes/crm_md.md)] eða jafnvel forritum sem þú smíðar sjálf(ur). Ef þú ert að samþætta í fyrsta skipti verður þú að gera það í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Dataverse](admin-common-data-service.md).

Ef þegar er búið að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að halda áfram að samstilla gögn með uppsetningunni. Ef þú hins vegar uppfærir eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)] til að kveikja á henni aftur. Frekari upplýsingar er að finna í [Uppfærsla samþættingar við Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Endurtenging um [!INCLUDE[prod_short](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar. Til dæmis verða sjálfgefnar töfluvarpanir notaðar.

## Samþættingarstillingar sem eru sértækar fyrir [!INCLUDE[crm_md](includes/crm_md.md)] samþættingu

Samþætting við [!INCLUDE[prod_short](includes/prod_short.md)] gerist í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)] og margar staðlaðar stillingar og töflur eru í boði. Ásamt stöðluðum stillingum, eru nokkrar sem eiga sérstaklega við um [!INCLUDE[crm_md](includes/crm_md.md)]. Stillingarnar eru taldar upp í eftirfarandi hlutum.

## Heimildir og öryggishlutverk fyrir notendareikninga í sölu

Þegar samþættingarlausnin er sett upp eru heimildir fyrir notandareikning samþættingar grunnstilltar. Ef þessum heimildum er breytt þarf mögulega að endurstilla þær. Hægt er að gera það með því að setja samþættingarlausnina upp aftur eða velja **Endurvirkja samþættingarlausn** á síðunni **Uppsetning Dynamics 365-tengingar**. Eftirfarandi öryggishlutverk eru virkjuð:

* Dynamics 365 Business Central Samþættingarstjórnandi
* Dynamics 365 Business Central Samþættingarnotandi
* Dynamics 365 Business Central Notandi afurðaframboðs

### Tengistillingar í uppsetningarhandbókinni

Hægt er að nota uppsetningarleiðbeiningar með hjálp til að setja upp tenginguna á fljótvirkan hátt og tilgreina ítarlega eiginleika, t.d. tengingu milli færslna.

1. Veldu **Uppsetning og viðbætur** og veldu síðan **Uppsetning með hjálp**.
2. Veldu **Setja upp Dynamics 365 Sales tengingu** til að hefja leiðbeiningar um uppsetningu með hjálp.
3. Fyllið inn reitina eftir þörfum.
4. Einnig eru ítarlegar stillingar sem geta aukið öryggi og virkjað fleiri möguleika. Eftirfarandi tafla lýsir ítarlegum stillingum.  

| Svæði | Lýsing |
|--|--|
| **Flytja inn Dynamics 365 Sales Solution** | Setja upp og grunnstilla samþættingarlausnina í [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Samstilla vörur til ráðstöfunar sjálfkrafa**|Tilgreinir að verkröð vöruráðstöfunar verði að vera tímasett. Verkröðin keyrir á 30 mínútna fresti og uppfærir stöðu tengdra vara.|
| **Virkja samþættingu eldri sölupöntuna** | Þegar fólk býr til sölupantanir í [!INCLUDE[crm_md](includes/crm_md.md)] og uppfyllir pantanir í [!INCLUDE[prod_short](includes/prod_short.md)] samþættar þessi stilling ferlið í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna á [Virkja sölupöntunarferli samþættingar](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).<br><br>**Athugið:** Þú getur ekki notað þennan valkost ef þú notar **Tvíátta samstillingu sölupantana** valkostinn. Stillingarnar tvær útiloka hvorn annan. Til að læra meira um þennan valkost skaltu fara í [Ein og tvíátta samstilling sölupantana](#single-and-bi-directional-synchronization-of-sales-orders). |
|**Virkja Dynamics 365 Sales Connection** | Virkja tenginguna við [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Dynamics 365 SDK útgáfa** | Þetta á aðeins við ef verið er að samþætta við útgáfu á staðnum af [!INCLUDE[crm_md](includes/crm_md.md)]. Þetta SDK er hugbúnaðarþróunarpakki Dynamics 365 (einnig vísað í sem Xrm) sem er notaður til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[crm_md](includes/crm_md.md)]. Útgáfan verður að vera samhæf SDK-útgáfunni sem notuð er af [!INCLUDE[crm_md](includes/crm_md.md)] og sú sama eða nýrri og útgáfan sem er notuð af [!INCLUDE[crm_md](includes/crm_md.md)]. |
|**Tvíátta samstilling sölupantana**|Samstilltu sölupantanir í báðar áttir. Til að læra meira um þennan valkost skaltu fara  [Ein og tvíátta samstilling á sölupöntunum](#single-and-bi-directional-synchronization-of-sales-orders).<br><br>**Athugið:** Þú getur ekki notað þennan valkost ef þú notar **Virkja eldri sölupöntunarsamþættingu** valkostinn. Stillingarnar tvær útiloka hvorn annan.|

### Tengistillingar á síðunni Microsoft Dynamics 365 Connection Setup

Færðu inn eftirfarandi upplýsingar fyrri tenginguna frá [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)].

| Svæði | Lýsing |
|--|--|
|**Dynamics 365 Sales vefslóð**|Vefslóð fyrir [!INCLUDE[crm_md](includes/crm_md.md)]-tilvikið þitt. Þessi stilling gerir notendum kleift að opna færslurnar í [!INCLUDE[prod_short](includes/prod_short.md)] sem samsvara færslum í [!INCLUDE[crm_md](includes/crm_md.md)]. Til dæmis reikning eða vöru. [!INCLUDE[prod_short](includes/prod_short.md)]-færslur opnast í [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Samstilla vörur til ráðstöfunar sjálfkrafa**|Tilgreinir að verkröð vöruráðstöfunar verði að vera tímasett. Verkröðin keyrir á 30 mínútna fresti og uppfærir stöðu tengdra vara.|
|**Dynamics 365 SDK útgáfa**|Ef verið er að samþætta við útgáfu á staðnum af [!INCLUDE[crm_md](includes/crm_md.md)], er þetta hugbúnaðarþróunarpakki Dynamics 365 (einnig vísað í sem Xrm) sem er notaður til að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[crm_md](includes/crm_md.md)]. Útgáfan sem var valin verður að vera samhæf SDK-útgáfunni sem notuð er af [!INCLUDE[crm_md](includes/crm_md.md)]. Þessi útgáfa sem er til jafns á við eða nýrri en útgáfan sem er notuð af [!INCLUDE[crm_md](includes/crm_md.md)].|

Auk ofangreindra stillinga skal færa inn eftirfarandi stillingar fyrir [!INCLUDE[crm_md](includes/crm_md.md)].

| Svæði | Description |
|--|--|
| **Kveikt er á samþættingu sölupöntunar** | Gerðu notendum kleift að senda inn sölupantanir og virkjuð tilboð í [!INCLUDE[crm_md](includes/crm_md.md)] og síðan skoða og vinna úr þeim í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi stilling samþættir ferlið í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna á [Virkja sölupöntunarferli samþættingar](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Stofna sölupantanir sjálfvirkt** | Stofna sölupöntun í [!INCLUDE[prod_short](includes/prod_short.md)] þegar notandi stofnar og sendir inn eina í [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Vinna sölutilboð sjálfkrafa** | Vinna úr sölutilboði í [!INCLUDE[prod_short](includes/prod_short.md)] þegar notandi stofnar og virkjar eitt slíkt í [!INCLUDE[crm_md](includes/crm_md.md)]. Nánari upplýsingar er að finna í [Meðhöndlun á gögnum sölutilboðs](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Tvíátta samstilling sölupantana**|Samstilltu sölupantanir í báðar áttir. Til að læra meira um þennan valkost skaltu fara í [Ein og tvíátta samstilling sölupantana](#single-and-bi-directional-synchronization-of-sales-orders).|
<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->
### Einstök og tvíátta samstilling sölupantana

Þegar þú setur upp samþættingu þína, annað hvort í uppsetningarhandbókinni eða á síðunni Microsoft Dynamics 365 Connection Setup, eru valkostir sem stjórna í hvaða átt þú samstillir sölupantanir og hvernig þú sendir þær inn.

 **Tvíátta samstilling sölupantana** valkosturinn gerir þér kleift að samstilla sölupantanir frá sölu til [!INCLUDE [prod_short](includes/prod_short.md)] og öfugt. Ef viðskiptamaður skiptir til dæmis um skoðun á vörunni eða magninu sem hann pantaði í [!INCLUDE[crm_md](includes/crm_md.md)] geturðu safnvistað söluskjalinu og stofnað nýtt í [!INCLUDE[prod_short](includes/prod_short.md)]. Það sama á við um breytingar á [!INCLUDE[prod_short](includes/prod_short.md)]. Til dæmis, þegar verð, skattupphæðir eða væntanlegir sendingardagar breytast, samstillast breytingarnar við [!INCLUDE[crm_md](includes/crm_md.md)]. Tvíátta samstilling hjálpar til við að halda seljendum þínum uppfærðum með nýjustu breytingarnar og stöðu sölupantana.

Fyrir tvíátta samstillingu gerirðu sölupantanir tiltækar fyrir samstillingu þegar þú breytir stöðu þeirra í **Sent fram** í sölu. Þegar þú stillir þá stöðu geturðu ekki lengur breytt upplýsingum á línum pöntunarinnar. Þegar þú samstillir er pöntunin færð yfir á [!INCLUDE [prod_short](includes/prod_short.md)] með stöðunni **Loft**. Ef mistök eru, geturðu snúið pöntuninni aftur í **Opið** (í [!INCLUDE [prod_short](includes/prod_short.md)]) eða **Virkt** (í sölu), og bættu síðan við eða eyddu línum til að leiðrétta mistökin og sendu pöntunina aftur.

> [!TIP]
> Þegar þú virkjar **Tvíátta samstilling sölupantana** valkostsins, býr  [!INCLUDE [prod_short](includes/prod_short.md)] skrá í **sölupöntunarsafninu** síðu þegar þú birtir eða breytir upplýsingum um pöntun. Til dæmis geta geymdar útgáfur verið gagnlegar til að kanna sögu pöntunar.

Valkosturinn **Virkja eldri sölupöntunarsamþættingu** samstillingar aðeins frá sölu til [!INCLUDE [prod_short](includes/prod_short.md)]. Fyrir þennan valkost notarðu **Senda** aðgerðina í Sales til að gera pantanir aðgengilegar fyrir samstillingu. Þegar þú gerir það geturðu ekki lengur breytt neinum upplýsingum um pöntunina. Þegar þú samstillir er pöntunin færð yfir á [!INCLUDE [prod_short](includes/prod_short.md)] með stöðunni **Loft**.

Til að nota þennan valkost verður þú að gefa upp skilríki fyrir notandareikning stjórnanda í [!INCLUDE[crm_md](includes/crm_md.md)]. Til að fá frekari upplýsingar, sjá [Meðhöndlun sölupöntunargagna](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!NOTE]
> Valmöguleikarnir **Tvíátta samstilling sölupantana** og **Virkja samþættingu eldri sölupöntuna**  útiloka hvorn annan. Þú getur ekki notað báða valkostina á sama tíma.

Fyrir báða valkostina sýnir [!INCLUDE [prod_short](includes/prod_short.md)] allar sölupantanir með  **Sendið** stöðuna á  **pantunum - Microsoft Dynamics 365 Sölu** síða.

### Venjuleg kortlagning sölueiningar fyrir samstillingu

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
| Söluverð | Verðlisti vöru | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] tengiliðasía: **Sölukóði** er ekki auður, **Sölutegund** er **Verðflokkur viðskiptamanns** |
| Tækifæri | Tækifæri | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Sölureikningshaus | Reikningsfæra | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Sölureikningslína | Reikningsfæra vöru | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Sölupöntunarhaus | Sölupöntun | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Til að samstilla í báðar áttir verður þú að kveikja á **Tvíátta samstilling sölupantana** á síðunni **Uppsetning Dynamics 365-tengingar**.| [!INCLUDE[prod_short](includes/prod_short.md)] Sía söluhauss: **Gerð skjals** er Pöntun, **Staða** er útgefin |
| Athugasemdir sölupöntunar | Athugasemdir sölupöntunar | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Varpirnar fyrir töflurnar Mælieining vöru, Tilföng mælieiningu og Einingarhópa eru aðeins tiltækar ef stjórnandi þinn hefur kveikt á **Einingahópsvörpun** rofi á **Microsoft Dynamics 365 tengingaruppsetning** síða. Til að læra meira, farðu í [Samstilla hluti og tilföng við vörur í mismunandi mælieiningum](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronize-items-and-resources-with-products-with-different-units-of-measure).

## Samstilltu hluti og tilföng við vörur með mismunandi mælieiningar

Fyrirtæki framleiða oft eða kaupa vörurnar í einni mælieiningu og selja þær svo í öðrum. Til að samstilla hluti sem nota margar mælieiningar, verður þú að kveikja á **einingahópsvörpun** rofi á **Microsoft Dynamics 365 tengingaruppsetningu** síðu. 

Þegar kveikt er á eiginleikauppfærslunni er ný tafla einingahóps búin til og henni úhlutað á hverja vöru og tilfang í [!INCLUDE[prod_short](includes/prod_short.md)]. Töflurnar gera þér kleift að varpa töflum einingahóps, mælieiningar vöru og mælieiningar tilfangs úr [!INCLUDE[prod_short](includes/prod_short.md)] í einingahóp Dynamics 365 Sales í [!INCLUDE[crm_md](includes/crm_md.md)]. Eftirfarandi mynd sýnir varpanir.

:::image type="content" source="media/unit group 1.png" alt-text="Töfluvarpanir fyrir einingahópa":::

Hægt er að búa til margar mælieiningar fyrir hvern einingahóp og úthluta hópunum á afurðir í [!INCLUDE[crm_md](includes/crm_md.md)]. Þar á eftir geturðu samstillt afurðirnar við vörur og tilföng í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að tengja mælieiningar vöru eða tilfangs við einingahóp. Þegar það er gert, ef til að mynda einingahópur vöru eða tilfangs er ekki tengdur við einingahóp í [!INCLUDE[crm_md](includes/crm_md.md)] vegna þess að einingahópurinn var ekki til, mun [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa búa til einingahóp í [!INCLUDE[crm_md](includes/crm_md.md)].

### Kortaðu hluti og tilföng við vörur

Þegar þú kveikir á **Unit Group Mapping** rofi á síðunni **Microsoft Dynamics 365 Connection Setup**, gerist eftirfarandi:

* Nýjar varpanir eru búnar til fyrir vörur og tilföng.
* Fyrirliggjandi vörpunum er eytt. <!--which mappings?-->
* Gagnauppfærsla býr til einingahópa fyrir vörur og tilföng.

Til að nota nýju varpanirnar þarf að samstilla einingahópa, mælieiningu vöru og mælieiningu tilfangs. Einnig þarf að endursamstilla vörur og tilföng. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] leyfir þér ekki að breyta einingahópi fyrir afurð. Þess vegna þarf að taka afurðirnar úr umferð og aftengja vörur og tilföng og síðan samstilla með því að búa til nýjar afurðir í [!INCLUDE[crm_md](includes/crm_md.md)]. 

Eftirfarandi skref lýsa skrefunum til að hefja vörpun einingahópa:

1. Gættu þess að afurðir í [!INCLUDE[crm_md](includes/crm_md.md)] séu ekki tengdar við vörur eða tilföng í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef svo er skal fara á síðurnar **Vörur** og/eða **Tilföng**, nota síuvalkostina til að velja tengdar færslur. Veldu svo aðgerðina **Dynamics 365 Sales** og veldu **Aftengja**. Þessi aðgerð tímasetur bakgrunnsvinnslu til að aftengja færslurnar. Á meðan verkið er í gangi er hægt að athuga stöðu þess með því að nota aðgerðina **Samstillingarkladdi**. Frekari upplýsingar er að finna í [Tenging og samstilling](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Þar sem nýjar afurðir verða búnar til í [!INCLUDE[crm_md](includes/crm_md.md)] með nýjum einingahópum skal gera eitt af eftirfarandi til að forðast tvítekningu heita:
    
  * Endurnefndu afurðirnar og taka þær svo úr umferð í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Taka afurðir úr umferð (sölumiðstöð)](/dynamics365/sales-enterprise/retire-product). Til að breyta mörgum afurðum í einu í Microsoft Excel skal skrá sig inn í Power Apps, velja umhverfið, fara í töfluna **Afurð** og velja flipann **Gögn**. Hreinsaðu allar síur sem eru notaðar. Í hópnum **Gögn** skal velja aðgerðina **Breyta gögnum í Excel**. Bættu forskeyti eða viðskeyti við tengdar afurðir og taktu þær svo úr umferð.
    * Taktu afurðirnar úr umferð og eyddu þeim. 

3. Fylgdu þessum skrefum til að samstilla **Einingahópa**, **Mælieiningar**, **Vörur** og **Tilföng**:
    1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna síðuna **Uppsetning tengingar fyrir Dynamics 365 Sales**.
    2. Notaðu aðgerðina **Keyra fulla samstillingu** til að opna síðuna **Dataverse Yfirfara fulla samstillingu**.
    3. Fyrir varpanirnar **VARA UOM**, **TILFANG UOM** OG **EININGAHÓPUR** skal velja aðgerðina **Ráðleggja fulla samstillingu**.
    4. Veldu aðgerðina **Samstilla allt**.

    > [!NOTE]
    > Þessi aðgerð mun samstilla að fullu þær varpanir sem hafa ekki verið samstilltar að fullu hingað til. Til að koma í veg fyrir að þessar varpanir verði samstilltar skal eyða vörpunum af síðunni. Þetta fjarlægir þær aðeins úr núverandi fullri samstillingu og eyðir ekki vörpununum.
    
5. Veldu vörpunina **VARA-AFURÐ** og síðan aðgerðina **Endurræsa**. Endurræsing býr til nýjar afurðir úr vörunum í [!INCLUDE[crm_md](includes/crm_md.md)] og úthlutar nýjum einingahópi sem á við um vöruna.
6. Veldu vörpunina **TILFANG-AFURÐ** og síðan aðgerðina **Endurræsa**. Endurræsing býr til nýjar afurðir úr tilföngunum í [!INCLUDE[crm_md](includes/crm_md.md)] og úthlutar nýjum einingahópi sem á við um tilföngin.

### Samstillingarreglur

Í eftirfarandi töflu eru taldar upp reglurnar sem stjórna samstillingu milli [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)]. Þesar reglur eru viðbót við reglur sem skilgreindar eru fyrir Dataverse, sem eiga einnig við. Frekari upplýsingar er að finna í [Stöðluð einingavörpun](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Breytingar á gögnum í  sem voru gerðar af notandareikningi samþættingar eru ekki samstilltar. Mælt er með því að gögnum sé ekki breytt á meðan reikningurinn er notaður. Nánari upplýsingar er að finna í [Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tafla|Regla|
|-----|----|
|Mælieiningar|Mælieiningar eru samstillar við einingahópa í [!INCLUDE[crm_md](includes/crm_md.md)]. Aðeins er hægt að skilgreina eina mælieiningu í einingahópnum.|
|Birgðir|Þegar vörur eru samstilltar við [!INCLUDE[crm_md](includes/crm_md.md)]-vörur mun [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa stofna verðlista í [!INCLUDE[crm_md](includes/crm_md.md)]. Til að forðast samstillingarvillur ætti ekki að breyta þessum verðlista handvirkt.|
|Forðar|Tilföng eru samstillt við vörur [!INCLUDE[crm_md](includes/crm_md.md)] sem hafa þjónustu sem vörugerðina.|
|Verðflokkar viðskm.|Verðflokkar viðskiptavinar eru samstilltir við verðlista Sales.|
|Söluverð|Söluverð sem eru með verðflokk viðskiptavinar sem sölugerð og eru með skilgreindan sölukóða eru samstillt við verðlistalínur [!INCLUDE[crm_md](includes/crm_md.md)]|
|Tækifæri|Tækifæri eru samstillt við tækifæri [!INCLUDE[crm_md](includes/crm_md.md)]. Gildið á kóða sölumanns skilgreinir eiganda tengdu töflunnar í [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bókaðir sölureikningar|Bókaðir sölureikningar eru samstilltir við sölureikninga. Áður en hægt er að samstilla reikning er betra að samstilla allar aðrar töflur sem geta verið hluti af reikningnum, frá sölumanni til verðlista. Gildið á kóða sölumanns í fyrirsögn reiknings skilgreinir eiganda tengdu töflunnar í Sales.|
|Sölupantanir|Þegar samþætting sölupöntunar er virkjuð eru sölupantanir í [!INCLUDE[prod_short](includes/prod_short.md)] sem eru búnar til úr innsendum sölupöntunum í [!INCLUDE[crm_md](includes/crm_md.md)] samstilltar við sölupantanir í [!INCLUDE[crm_md](includes/crm_md.md)] þegar þær eru gefnar út. Áður en þú samstillir pantanir mælum við með að þú samstillir fyrst allar töflurnar sem koma við sögu í pöntuninni, t.d. sölufólk og verðlistar. Kóðareitur sölumanns í pöntunarhaus skilgreinir eiganda tengdu töflunnar í [!INCLUDE[crm_md](includes/crm_md.md)].|

### Samstillingarstörf fyrir sölusamþættingu

Verkin eru keyrð í eftirfarandi röð til að koma í veg fyrir tengsl tenginga milli taflanna. Fleiri verk eru í boði úr Dataverse. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](./admin-job-queues-schedule-tasks.md).

1. UNITOFMEASURE-samstillingarvinnsla Dynamics 365 Sales  
2. TILFÖNG-AFURÐ fyrir samstillingarvinnslu Dynamics 365 Sales  
3. ITEM-PRODUCT - Dynamics 365 Sales samstillingarverk  
4. CUSTPRCGRP-VERÐ í samstillingarvinnslu Dynamics 365 Sales.
5. SALESPRC-PRODPRICE - Dynamics 365 Sales samstillingarvinnsla.
6. POSTEDSALESINV-INV - Dynamics 365 Sales samstillingarvinnsla.

### Sjálfgefin færslur í vinnuröð fyrir samstillingu

Eftirfarandi tafla lýsir sjálfgefnum samstillingarverkum fyrir [!INCLUDE[crm_md](includes/crm_md.md)].  

|Verkraðarfærsla|Description|Stefna|Vörpun samþættingartöflu|Sjálfgefin tíðni samstillinga (mín)|Sjálfgefinn hvíldarstaða vegna aðgerðarleysis (mín.)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|UNITOFMEASURE-samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] einingahópa við [!INCLUDE[prod_short](includes/prod_short.md)] mælieiningar.|Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÆLIEINING|30|720<br> (12 klst.)|
|TILFÖNG-AFURÐ fyrir samstillingarvinnslu Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] vörur við [!INCLUDE[prod_short](includes/prod_short.md)] tilföng.|Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|TILFÖNG-VARA|30|720<br> (12 klst.)|
|VARA-AFURÐ- samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] vörur við [!INCLUDE[prod_short](includes/prod_short.md)] atriði.|Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|ATRIÐI-VARA|30|1440<br> (24 klst.)|
|CUSTPRCGRP-VERÐ í samstillingarvinnslu Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] söluverðlista við [!INCLUDE[prod_short](includes/prod_short.md)] verðflokka viðskiptamanns.| |VERÐFLOKKAR VIÐSKIPTAMANNS-LISTAR SÖLUVERÐS|30|1440<br> (24 klst.)|
|SALESPRC-PRODUCTPRICE-samstillingarvinnsla Dynamics 365 Sales|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] afurðarverð við [!INCLUDE[prod_short](includes/prod_short.md)] söluverð.||AFURÐARVERÐ-SÖLUVERÐ|30|1440<br> (24 klst.)|
|POSTEDSALESINV-INV-Dynamics 365 Sales samstillingarvinnsla|Samstillir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga við [!INCLUDE[prod_short](includes/prod_short.md)] bókaða sölureikninga.|Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|REIKNINGAR-BÓKAÐIR SÖLUREIKNINGAR|30|1440<br> (24 klst.)|
|Talnagögn viðskiptavinar - samstillingarvinnsla Dynamics 365 Sales|Uppfærir [!INCLUDE[crm_md](includes/crm_md.md)] reikninga með nýjustu [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamannagögnunum. Í [!INCLUDE[crm_md](includes/crm_md.md)] birtast upplýsingarnar í **Tölfræði fyrir Business Central-reikning** skjámynd flýtiyfirlits yfir reikninga sem eru tengdir við [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamenn.<br /><br /> Einnig er hægt að uppfæra þessi gögn handvirkt úr hverri viðskiptamannafærslu. Frekari upplýsingar er að finna í [Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Athugið:** Þessi verkraðarfærsla á aðeins við ef [!INCLUDE[prod_short](includes/prod_short.md)] samþættingarlausnin er sett upp í [!INCLUDE[crm_md](includes/crm_md.md)]. |Á ekki við|Á ekki við|30|Á ekki við| 

## Tengstu við staðbundnar útgáfur af Business Central 2019 útgáfubylgju 1 og Microsoft Dynamics NAV 2018

Microsoft Power Platform hópurinn hefur [tilkynnt](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) að hann ætli að úrelda sannvottunargerð Office365. Ef notað er útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum sem er eldra en útgáfutímabil 1 af Business Central 2019 þarf að nota sannvottunargerð OAuth til að tengjast [!INCLUDE[crm_md](includes/crm_md.md)] á netinu. Skrefin í þessum hluta lýsa því hvernig á að tengjast eftirfarandi útgáfum af vöru:

* Útgáfutímabil 1 af Business Central 2019
* Microsoft Dynamics NAV 2018

### Frumskilyrði

* Nauðsynlegt er að vera með Microsoft Azure-áskrift. Prufureikningur virkar fyrir forritsskráningu.
* [!INCLUDE[crm_md](includes/crm_md.md)] er grunnstillt til að nota eina af eftirfarandi sannvottunargerðum:

   * Office365 (eldra)

     > [!IMPORTANT]
     > Gildir frá apríl 2022, Office365 (eldra) verður ekki lengur stutt. Frekari upplýsingar eru í [Mikilvægar breytingar (afskriftir) væntanlegar í Power Apps, Power Automate og viðskiptavinaforritum](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   * OAuth

### Connect Business Central 2019 útgáfubylgja 1 og Dynamics NAV 2018

1. Flytjið samþættingarlausn Microsoft Dynamics 365 Business Central inn í [!INCLUDE[crm_md](includes/crm_md.md)]-umhverfið. Samþættingarlausnin er í boði í möppunni CrmCustomization á DVD-uppsetningardisknum fyrir [!INCLUDE[prod_short](includes/prod_short.md)] eða Dynamics NAV 2018. Flytjið inn eitt af eina af eftirfarandi lausnum eftir því hver útgáfa vörunnar er:

   * Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur mappan DynamicsNAVIntegrationSolution_v9 og DynamicsNAVIntegrationSolution_v91. lausnir. Lausnin sem þú ættir að flytja inn veltur á þeirri útgáfu af [!INCLUDE[crm_md](includes/crm_md.md)] sem verið er að tengjast. [!INCLUDE[crm_md](includes/crm_md.md)] á netinu þarf samþættingarlausnina DynamicsNAVIntegrationSolution_v91.
   * Fyrir Dynamics NAV 2018 skal setja upp DynamicsNAVIntegrationSolution-lausnina.

2. Stofnið ógagnvirkan samþættingarnotanda í [!INCLUDE[crm_md](includes/crm_md.md)]-umhverfinu og úthlutið notandanum eftirfarandi öryggishlutverkum. Frekari upplýsingar er að finna í [Stofna ógagnvirkan notandareikning](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central Samþættingarstjórnandi
   * Dynamics 365 Business Central Samþættingarnotandi

   > [!Important]
   > Þessi notandi má ekki hafa öryggishlutverk kerfisstjóra. Einnig er ekki hægt að nota reikning kerfisstjóra sem samþættingarnotanda.

3. Í Azure-gáttinni skal búa til forritsskráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Fyrir frekari upplýsingar, sjá [Skráðu umsókn í Microsoft Entra ID](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Mælt er með að forrið sé skráð í sama leigjanda og Dataverse-umhverfið þannig að ekki þurfi að samþykkja aðgang forritsins að umhverfinu. Ef þú skráir appið í öðru umhverfi verður þú að skrá þig inn á Microsoft Entra ID með því að nota stjórnandareikninginn fyrir Dataverse umhverfið þitt og gefa samþykki.
   >
   > Auk þess má forritið sem þú skráir ekki vera með leynilykil. Að tengja forrit með leynilykli við Dataverse er aðeins í boði í Business Central 2020 útgáfutímabili 1 og síðar.
  
4. Framkvæmið eitt af eftirfarandi skrefum eftir því hver útgáfa vörunnar er:

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

## Sjá einnig .

[Uppsetning á notendareikningum fyrir samþættingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sérstilling Business Central og [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
