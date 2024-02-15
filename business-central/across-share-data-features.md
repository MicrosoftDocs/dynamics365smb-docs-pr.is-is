---
title: Deila gögnum
description: Kynntu þér ólíkar leiðir til að deila viðskiptagögnum úr Business Central.
author: jswymer
ms.topic: conceptual
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Deiling viðskiptagagna úr Business Central

Samstarf fólks innan og utan fyrirtækis er ómissandi þáttur í flestum viðskiptum. [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á ýmsa eiginleika til að deila viðskiptagögnum, eins og lista yfir færslur, tilteknar færslur eða skjöl. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Með öllum þessum eiginleikum er aðgangur að gögnum varinn með leyfi og heimildum Business Central.

## Afrita tengil

![Stutt](media/check.png) Business Central Online ![Stutt](media/check.png) Business Central á staðnum

Frá hvaða síðu sem er geturðu afritað vefslóð síðunnar, síðan líma hana og dreifa henni með öðrum miðlum eins og tölvupósti, Teams-spjalli eða textaskilaboðum. Einfaldasta leiðin til að afrita tengil er með því að velja **Deila** > **Afrita tengil** efst á síðunni. Önnur leið er að afrita vefslóðina beint úr veffangareit vafrans.

Þegar þú límir veffangið inn í ríkan texta ritil eins og Word, Outlook eða Teams, í stað þess að birta fulla URL, er tengillinn gefið læsilegra heiti sem gefur greinilega til kynna samhengi marksins. Heitið og mynstrið eru mismunandi eftir því hvaða síðu þú tengist. Huga skal að eftirfarandi dæmum:

|Mynstur|Dæmi um síðu|Heiti tengils|
|-|-|-|
|Listasíður|**Listasíða atriða**  | **Birgðir**|
|Listayfirlit| **Opna** afmarkað yfirlit á **lista sölupantana** |**Sölupantanir - Opnar**|
| Ein færsla|Birgðaspjald sýnir eina færslu|"Birgðaspjald - 1896 ∙ AÞENA skrifborð"|
|Drög að færslum| Nýtt viðskiptamannaspjald|**Nýtt - Viðskiptamannaspjald**|
|Fyrirtæki sem notar skjöld|**Vörulistasíða** fyrirtækis með skjöld **CRONUS**| **Vörur (CRONUS)**|

> [!TIP]
> Svipuð nafnavenja er notuð á flipum vafra.

### Samnýting gagnagreiningar
Ef verið er að skoða síðu eða fyrirspurn í gagnagreiningarstillingunni er hægt að samnýta tiltekinn greiningarflipa með því að velja niðurörina á flipanum og velja **síðan Afrita tengil**. [Fá nánari upplýsingar um gagnagreiningarstillingu](analysis-mode.md). 

### Breyta tengli síðunnar

Þegar þú afritar tengil og áður en þú sendir hann geturðu breytt vefslóðinni til að stýra því hvað er sýnt þegar síðan opnast. Til dæmis er hægt að bæta við síum eða tilgreina annað fyrirtæki.

[Fræðast meira um vefslóð](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) vefbiðlarans.

### Um síaða lista

Með því að nota síusvæðið á listasíðum geturðu notað síur til að þrengja færslurnar sem sýndar eru í listanum. Ef notuð er aðgerðin **Afrita tengil** eða vefslóðin úr vafranum er afrituð mun síðutengillinn ekki innihalda síubreytingarnar þínar. Notendur sem opna tengilinn sjá allt safnið. Besta leiðin til að halda síun á síðutengli safnsins er að vista fyrst síuðu síðuna sem **Yfirlit**. Opnaðu svo yfirlitið og afritaðu tengilinn þaðan.

[Fræðast meira um röðun, leit og afmörkun](ui-enter-criteria-filters.md).

## Deila með Teams

![Stutt](media/check.png) Business Central Online ![Ekki stutt](media/x-icon.png) Business Central á staðnum

Beint úr flestum safnsíðum og upplýsingasíðum geturðu sent tengil á síðuna til einstaklinga, hópspjalls eða rása. Til dæmis deila tengli á síað yfirlit yfir færslurnar þínar. Ef þú hefur sett upp [!INCLUDE[prod_short](includes/prod_short.md)] forritið fyrir Teams mun tengillinn sjálfkrafa stækka í samandregið spjald sem þú getur haft með skilaboðunum. Viðtakendur velja síðan tengilinn eða spjaldið til að opna síðuna í Business Central.

[Fræðast meira um samnýtingu færslna og síðutengla í Teymi](across-working-with-teams.md).

## Samnýting með OneDrive

![Stutt](media/check.png) Business Central Online ![Stutt](media/check.png) Business Central á staðnum

Business Central auðveldar geymslu, umsjón og deilingu skráa með öðrum í gegnum OneDrive fyrir Business. Á flestum síðum þar sem skrár eru tiltækar, svo sem Skýrsluinnhólf eða skrár sem eru tengdar færslum, er að finna **aðgerðirnar Opna inn OneDrive** og **Samnýta** . Báðar aðgerðir vista afrit af skrá á OneDrive. Þegar hún er í OneDrive geturðu notað deilingar- og framlagseiginleika á skrána. Munurinn á aðgerðum er sá að **Opna í OneDrive** opnar skrána í OneDrive. **Deila** opnar síðu sem gerir þér kleift að velja með hverjum þú vilt deila skránni. Viðtakendur fá tilkynningarpóst um aðgang að skránni frá þér OneDrive.

[Fræðast meira um samnýtingu skráa OneDrive](across-share-onedrive.md).

## Opna í Excel

![Stutt](media/check.png) Business Central Online ![Stutt](media/check.png) Business Central á staðnum

Fyrir listasíður og lista sem felldir eru inn á síðu er hægt að nota aðgerðina **Opna í Excel**. Þessi aðgerð flytur út lista yfir færslur í Excel-vinnubók (.xlsx-skrá), sem þú getur deilt með öðrum. Í vinnubókinni er einnig hægt að nota eiginleika deilingar sem er hluti af Excel.

[Fræðast meira um skoðun og breytingu í Excel](across-work-with-excel.md).

## Deila röðum eða töflum

![Stutt](media/check.png) Business Central Online ![Stutt](media/check.png) Business Central á staðnum

Þú getur deilt einni eða fleiri færslum í lista.  <kbd>Veldu ctrl</kbd>+<kbd>C</kbd> lyklaborð flýtivísun til að afrita á klippispjaldið þitt. Líma síðan það sem afritað var í annað forrit með því að styðja <kbd>á Ctrl</kbd>+<kbd>V</kbd>. Til dæmis mun afritun á þremur sölupöntunum og líming þeirra í tölvupóst sýna pantanirnar í snyrtilegri töflu.

[Fræðast meira um afrit og líma íFAQ](faq-copy-paste.yml).

## Sjá einnig .

[Business Central og OneDrive samþætting](across-onedrive-overview.md)  
[Stjórnun OneDrive samþættingar við Business Central](admin-onedrive-integration.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)
