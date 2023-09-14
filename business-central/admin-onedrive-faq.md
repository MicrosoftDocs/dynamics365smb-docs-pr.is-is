---
title: Algengar spurningar um OneDrive for Business
description: Fáðu svör við dæmigerðum spurningum um OneDrive for Business og Business Central.
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, integration, share, browser'
ms.date: 09/09/2022
ms.author: bholtorf
---
# Algengar spurningar um OneDrive for Business

[!INCLUDE [online_only](includes/online_only.md)]

Þessi grein svarar einhverjum þeirra spurninga sem þú gætir haft um notkun á OneDrive og [!INCLUDE [prod_short](includes/prod_short.md)].

## Virkar þetta fyrir alla [!INCLUDE[prod_short](includes/prod_short.md)] biðlara?

Já. Hægt er að opna skrár í OneDrive úr [!INCLUDE[prod_short](includes/prod_short.md)] farsímaforritum, þegar upplýsingar spjalds eru skoðaðar í Microsoft Teams eða jafnvel í Outlook-innbótinni.  

## Er OneDrive sama og SharePoint fyrir varðveislu skráa?

Sem hluti af Microsoft 365-áskriftinni þinni býður fyrirtækið þitt upp á OneDrive, skráageymsluna þína í skýinu. OneDrive er sjálfgefið til einkanota, þar sem þú skipuleggur efnið þitt og velur hvaða skrár eða möppur á að deila og með hverjum. SharePoint býður hinsvegar upp á gagnageymslu í skýinu fyrir skrár sem deilt er með öðrum í fyrirtækinu.  

## Styður [!INCLUDE[prod_short](includes/prod_short.md)] notanda OneDrive?

Fj. Þessi samþætting er eingöngu ætluð OneDrive for Business og styður aðeins vinnureikninginn þinn. 

## Er allar áskriftarleiðir OneDrive for Business studdar?

[!INCLUDE[prod_short](includes/prod_short.md)] styður ekki sjálfstæðar áskriftarleiðir fyrir OneDrive fyrir viðskipti. OneDrive verður að vera keypt sem hluti af áskriftarleið Microsoft 365 Business eða  Enterprise. Frekari upplýsingar er að finna í [Bera saman verð og áskriftarleiðir OneDrive skýjageymslu](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## Hvar get ég séð OneDrive Service Health?

Stjórnendur geta fengið aðgang að stjórnborði Service Health sem hluti af stjórnendamiðstöð Microsoft 365. Stjórnborðið inniheldur aðgengileika OneDrive þjónustu. Opnið [https://admin.microsoft.com/Adminportal/Home?#/servicehealth](https://admin.microsoft.com/Adminportal/Home?#/servicehealth).
 
## Er OneDrive samþætting í boði fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum?

Já, en ólíkt [!INCLUDE[prod_short](includes/prod_short.md)] á netinu þarf meiri uppsetningu. Frekari upplýsingar er að finna í [Skilgreining Business Central-þjóns innanhúss](admin-onedrive-integration-onpremises.md).  

## Tengist [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við SharePoint Server?

Nr. Þessi samsetning uppsetningar er ekki studd jafnvel þótt SharePoint þjónninn hefur virkjað „Mín svæði“.  

## Tengist [!INCLUDE[prod_short](includes/prod_short.md)] á netinu við SharePoint Server?

Nr. Þessi samsetning uppsetningar er ekki studd jafnvel þótt SharePoint þjónninn hefur virkjað „Mín svæði“.  

## Hvernig virkar þetta í fyrirtæki með mörgum umhverfum?

Samþættingin gerir ráð fyrir að heiti fyrirtækja séu einkvæm milli [!INCLUDE[prod_short](includes/prod_short.md)] umhverfa. Þegar heiti fyrirtækja eru einkvæm í móðurfyrirtækinu mun skrá sem er opnuð í OneDrive afrita skrána í möppu sem heitir eftir núverandi fyrirtæki. Ef heiti fyrirtækja eru ekki einkvæm yfir öll umhverfi gætu skrár úr fyrirtækjum sem bera sama heitið verið settar saman í eina möppu.  

## Við höfum breytt heiti fyrirtækis. Hvað verður um gömlu skrárnar mínar?

[!INCLUDE[prod_short](includes/prod_short.md)] flytur ekki skrár sjálfkrafa sem þú opnaðir áður í OneDrive yfir í nýju möppuna. Eftir að fyrirtækið hefur verið endurnefnt mun aðgerðin Opna í OneDrive afrita skrárnar í möppu sem er með nýja heiti fyrirtækisins.   

## Þegar skrár eru hengdar við [!INCLUDE[prod_short](includes/prod_short.md)] hvernig vel ég skrá úr OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] býður ekki upp á skýjaskráaval. Þú verður að sækja skrána úr OneDrive og yfir í tækið þitt og síðan hlaða henni upp í [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Í staðinn vil ég opna skrár í SharePoint. Hvernig geri ég það?

[!INCLUDE[prod_short](includes/prod_short.md)] býður ekki upp á eiginleika til að afrita skrár í SharePoint og opna þær úr SharePoint safni. Hafðu samband við samstarfsaðila Microsoft til að átta þig á möguleikum þínum eða leitaðu að forritum í AppSource.  

## Hvernig slekk ég á samþættingu í OneDrive?

Keyrðu uppsetningarleiðbeininguna **OneDrive uppsetning** og slökktu á rofunum **Nota OneDrive fyrir forritseiginleika** og **Nota OneDrive fyrir kerfiseiginleika**. 

## Ætti ég að nota SharePoint uppsetningarsíðu tengingar til að tengjast við SharePoint?

Þetta er eldri eiginleiki þar sem allar [!INCLUDE[prod_short](includes/prod_short.md)] skrár frá öllum notendum eru sendar í eina SharePoint möppu. Mælt er með því að grunnstilla ekki flýtiflipa samnýttra skjala á síðunni **Uppsetning SharePoint tengingar** því að þessi síða hefur verið [úrelt](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) og verður fjarlægð í 2023 útgáfutímabili 2, útgáfu 23.0.  Mælt er með því að nota **OneDrive uppsetningu** í staðinn.  

## Hvaða útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] styður OneDrive?

Samþætting við OneDrive varð aðgengileg í 2021 útgáfutímabili 2.  

## <a name="features"></a>Hvaða eiginleikar verða fyrir áhrifum af OneDrive samþættingu?

Í uppsetningarleiðbeiningunni **OneDrive uppsetning** til að setja upp OneDrive samþættingu geturðu kveikt eða slökkt á eiginleikum til að meðhöndla skrár Business Central í OneDrive. Eiginleikarnir skiptast á milli tveggja valkosta:

|Valkostur|Lýsing|
|------|----------|
|**Nota OneDrive fyrir forritseiginleika**|Ef þú kveikir á þessum valkosti eru aðgerðirnar **Opna í OneDrive** og **Deila** gerðar aðgengilegar í skrám í Business Central, eins og skrám sem tengdar eru við skjöl eða í skýrsluinnhólfinu. Þessar aðgerðir gera notendum kleift að afrita, opna og deila skrám í OneDrive. Frekari upplýsingar er að finna í [Opna og deila Business Central-skrám í OneDrive](across-share-onedrive.md).
|**Nota OneDrive fyrir kerfiseiginleika**|Ef kveikt er á þessum valkosti virkjast eftirfarandi eiginleikar:<ul><li> Aðgerðirnar **Opna í Excel** og **Breyta í Excel** á listasíðum munu afrita Excel-skrána sjálfkrafa í OneDrive, síðan opna hana í Excel Online. Frekari upplýsingar er að finna í [Skoða og breyta í Excel](across-work-with-excel.md).</li><li> Að senda skýrslu í Excel- eða Word-skrá mun afrita skrána sjálfkrafa í OneDrive, síðan opna hana í Excel eða Word á netinu. Frekari upplýsingar er að finna í [Skýrsla vistuð í skrá](ui-work-report.md#saving-a-report-to-a-file).|

## Heldur Microsoft áfram að bæta samþættinguna í OneDrive?

Við hjá Microsoft erum stöðugt að hlusta á viðbrögð frá fjölbreyttu samfélagi notenda okkar og vinna með helstu tillögur samfélagsins. Til að fá upplýsingar um hvað er á döfinni varðandi samþættingar við forrit Microsoft 365 skal skoða [Útgáfuáætlun Dynamics 365](/dynamics365-release-plan/2021wave1).  

Ef þú vilt taka þátt í að bæta OneDrive samþættingu eða ert með hugmynd um hvernig skuli bæta skráadeilingu og samstarf í [!INCLUDE[prod_short](includes/prod_short.md)] geturðu bætt við hugmynd eða kosið um fyrirliggjandi hugmyndir á [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## Úrræðaleit

Í þessum hluta koma fram upplýsingar um hvernig á að bera kennsl á og lagfæra vandamál sem kunna að koma upp þegar OneDrive er notað með [!INCLUDE[prod_short](includes/prod_short.md)].  

### Business Central finnur ekki OneDrive

Þegar þessi skilaboð birtast: „Ekki tókst að ákvarða staðsetningu OneDrive for Business. Hafa skal samband við samstarfsaðila til að setja hana upp,“ skal athuga hvort notandinn hafi opnað aðgang sinn að OneDrive að minnsta kosti einu sinni. Ef viðkomandi hefur ekki gert það skaltu biðja hann/hana um að fara á portal.office.com/onedrive til að setja hana upp. Það getur tekið nokkra stund. Ef skilaboðin birtast enn eftir sólarhring skaltu hafa samband við notendaþjónustu.  
 
### Ég á í vandræðum með að deila úr Outlook

Sjá [Get ekki deilt OneDrive skrám frá ](https://support.microsoft.com/en-us/office/can-t-share-onedrive-files-from-outlook-com-05d4cb21-40a2-40e3-b111-82cddb82d22f) Outlook.com í notendaþjónustu Microsoft.

### Það vantar aðgerðirnar opna í OneDrive og deila

Þú getur athugað nokkra hluti:

- Athugaðu hvort kveikt sé á forritseiginleikunum OneDrive í uppsetningarleiðbeiningunni **OneDrive uppsetning**. Sjá [Grunnstilla OneDrive með OneDrive uppsetningu](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup).
- Athugaðu hvort Microsoft OneDrive sé stillt á **Samþykkja** á síðunni **Staða persónuverndartilkynninga**. Sjá [Staða persónuverndartilkynninga](privacy-notices-status.md).

## Sjá einnig

[Business Central og OneDrive samþætting](across-onedrive-overview.md)  
[Stjórnun OneDrive samþættingar við Business Central](admin-onedrive-integration.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
