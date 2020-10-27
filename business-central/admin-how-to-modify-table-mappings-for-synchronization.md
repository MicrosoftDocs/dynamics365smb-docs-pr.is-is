---
title: Vörpun á töflum og reitum fyrir samstillingu | Microsoft docs
description: Kynntu þér hvernig á að varpa töflum og reitum til að samstilla gögn milli Business Central og Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 382328e88c828afbf4316eb1f9bab73f6a2b7f95
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911381"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Vörpun á töflum og reitum fyrir samstillingu
Grunnurinn að því að samstilla gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)] við gögn í [!INCLUDE[d365fin](includes/cds_long_md.md)] er að varpa töflum og reitum sem innihalda gögnin í báðar áttir. Vörpun gerist í samþættingartöflum. 

## <a name="mapping-integration-tables"></a>Vörpun samþættingartaflna
Samþættingartafla er tafla í gagnagrunninum [!INCLUDE[d365fin](includes/d365fin_md.md)] sem stendur fyrir einingu í, á borð við lykil, í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Samþættingartöflur innihalda reiti sem samsvara reitum í töflunni fyrir eininguna [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Til dæmis tengist samþættingartafla lykils við einingu lykils í [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Það verður að vera vörpun samþættingartöflu fyrir hverja einingu í [!INCLUDE[cds_short_md](includes/cds_short_md.md)] sem á að samstilla við gögn í [!INCLUDE[prodshort](includes/prodshort.md)].

Þegar tengingin er stofnuð á milli forrita setur [!INCLUDE[d365fin](includes/d365fin_md.md)] upp einhverja sjálfgefna töflu- og reitavörpun. Hægt er að breyta töfluvörpunum ef vilji er fyrir því. Frekari upplýsingar er að finna í [Stöðluð einingavörpun fyrir samstillingu](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization). Ef sjálfgefnum vörpunum hefur verið breytt og ætlunin er að bakfæra breytingarnar skal, á síðunni **[!INCLUDE[d365fin](includes/cds_long_md.md)] Upppsetning tengingar** , velja **Nota sjálfgefna samstillingaruppsetningu** .

> [!Note]
> Ef verið er að nota staðbundna útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)] eru varpanir samþættingartöflu geymdar í töflu 5335 samþættingartöfluvarpanir og hægt er að skoða og breyta henni á síðu 5335 samþættingartöfluvarpanir. Flóknar varpanir og samstillingarreglur eru skilgreina í codeunit 5341. 

### <a name="synchronization-rules"></a>Samstillingarreglur
Samþætingartöfluvörpun inniheldur einnig reglur sem hafa áhrif á hvernig samstillingarverk samþættingar samstilla færslur í töflunni [!INCLUDE[d365fin](includes/d365fin_md.md)] og einingu í [!INCLUDE[d365fin](includes/cds_long_md.md)]. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

### <a name="strategies-for-auto-resolving-conflicts"></a>Aðferðir fyrir sjálfvirka úrlausn árekstra
Gagnaárekstrar geta auðveldlega átt sér stað þegar viðskiptaforrit skiptast á gögnum með reglulegu millibili. Til dæmis gæti einhver eytt eða breytt færslu í öðru forritinu eða báðum. Til að draga úr þeim fjölda árekstra sem þarf að leysa handvirkt er hægt að tilgreina úrlausnaraðferðir og [!INCLUDE[d365fin](includes/d365fin_md.md)] mun sjálfkrafa leysa úr árekstrum samkvæmt reglum aðferðarinnar.

Vörpun samþættingartöflu inniheldur reglur sem stýra því hvernig samstillingarverk samstilla færslur. Á síðunni **Vörpun samþættingartöflu** , í dálkunum **Leysir úr eyðingarárekstrum** og **Leysa úr uppfærsluárekstrum** , er hægt að tilgreina hvernig [!INCLUDE[d365fin](includes/d365fin_md.md)] leysir úr árekstrum sem koma upp vegna þess að færslum var eytt úr töflum í öðru hvoru viðskiptaforritinu, eða þær uppfærðar. 

Í dálknum **Leysir úr eyðingarárekstrum** er hægt að velja um að láta [!INCLUDE[d365fin](includes/d365fin_md.md)] sjálfkrafa endurheimta eyddar færslur, fjarlægja tenginguna milli færslna eða gera ekki neitt. Ef ekkert er gert er leyst úr árekstrum handvirkt. 

Í dálknum **Leysa úr uppfærsluárekstrum** er hægt að velja um að láta [!INCLUDE[d365fin](includes/d365fin_md.md)] sjálfkrafa senda gagnauppfærslu í samþættingartöfluna þegar gögn eru send til [!INCLUDE[d365fin](includes/cds_long_md.md)], eða til að fá gagnauppfærslu úr samþættingartöflunni þegar gögn er sótt úr [!INCLUDE[d365fin](includes/cds_long_md.md)], eða gera ekki neitt. Ef ekkert er gert er leyst úr árekstrum handvirkt.

Þegar búið er að tilgreina aðferðina, á síðunni **Samstillingarvilla í tengdum gögnum** , er hægt að velja aðgerðina **Reyna allt aftur** til að leysa úr árekstrum sjálfkrafa. 

## <a name="mapping-integration-fields"></a>Vörpun samþættingarreita
Vörpun á töflum er aðeins fyrsta skrefið. Einnig þarf að varpa reitunum í töflunum. Vörpun samþættingarreits tengir reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)] töflum við samsvarandi reiti í [!INCLUDE[d365fin](includes/cds_long_md.md)] og ákvarðar hvort samstilla eigi gögn í hverri töflu. Stöðluð töfluvörpun sem [!INCLUDE[d365fin](includes/d365fin_md.md)] veitir inniheldur reitavarpanir en hægt er að breyta þeim ef þess er óskað. Nánari upplýsingar er að finna í [Að skoða vörpunareiningar](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Ef notuð er staðbundin útgáfa af [!INCLUDE[d365fin](includes/d365fin_md.md)] eru varpanir samþættingarreits skilgreindar í töflu 5336 vörpun samþættingarreits.

### <a name="handling-differences-in-field-values"></a>Að meðhöndla mun á reitargildum
Stundum eru önnur gildi í reitunum sem á að varpa. Til dæmis, í [!INCLUDE[crm_md](includes/crm_md.md)] er tungumálakóðinn fyrir Bandaríkin „U.S.“ en í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hann „US.“ Það þýðir að þú verður að umbreyta gildinu þegar þú samstillir gögn. Þetta gerist í gegnum breytingareglur sem eru skilgreindar fyrir svæðin. Umbreytingarreglur eru skilgreindar á síðunni **Varpanir samþættingartöflu** með því að velja **Vörpun** og síðan **Reitir** . Boðið er upp á forskilgreindar reglur, en einnig má búa til sínar eigin. Frekari upplýsingar er að finna í [Umbreytingarreglur](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handling-missing-option-values-in-mapping"></a>Að meðhöndla gildi sem vantar fyrir valkosti í vörpun
[!INCLUDE[d365fin](includes/cds_long_md.md)] inniheldur reiti fyrir valkosti sem bjóða upp á gildi sem hægt er að varpa í [!INCLUDE[d365fin](includes/d365fin_md.md)] reiti af gerðinni **Valkostur** fyrir sjálfvirka samstillingu. Við samstillingu eru óvarpaðir valkostir hunsaðir og valkostina sem vantar er komið fyrir í tengdri [!INCLUDE[d365fin](includes/d365fin_md.md)] töflu og bætt við kerfistöfluna **Vörpun CDS-valkosta** til að meðhöndla handvirkt seinna. Til dæmis með því að bæta við valkostunum sem vantar í aðrahvora vöruna og síðan uppfæra vörpunina. Frekari upplýsingar er að finna í [Að meðhöndla gildi sem vantar fyrir valkosti](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Tengja skrár
Tenging tengir færslur í [!INCLUDE[d365fin](includes/cds_long_md.md)] við færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til dæmis eru lyklar í [!INCLUDE[d365fin](includes/cds_long_md.md)] yfirleitt samtengdir við viðskiptavini í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Að tengja færslur býður upp á eftirfarandi ávinning:

* Það gerir samstillingu mögulega.
* Notendur geta opnað færslur í einu viðskiptaforriti úr hinu. Þetta krefst þess að forritin séu þegar samþætt.

Hægt er að setja upp tengingar sjálfkrafa með því að nota samstillingarverk eða handvirkt með því að breyta færslunni í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar er að finna í [Samstilla gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) og [Tengja og samstilla færslur handvirkt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Afmarka færslur  
Ef þú vilt ekki að samstilla allar færslur fyrir tiltekna einingu í [!INCLUDE[d365fin](includes/cds_long_md.md)] eða töflu í [!INCLUDE[d365fin](includes/d365fin_md.md)], getur þú sett upp síur til að takmarka færslur sem eru samstilltar. Afmarkanir eru settar upp á síðunni **Varpanir samþættingartöflu** .  

#### <a name="to-filter-records-for-synchronization"></a>Til að afmarka færslur fyrir samstillingu  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.

2.  Til að afmarka [!INCLUDE[d365fin](includes/d365fin_md.md)] skrár er reiturinn **Töfluafmörkun** stilltur.  

3.  Til að afmarka [!INCLUDE[d365fin](includes/cds_long_md.md)] skrár er reiturinn **Afmörkun samþættingartöflu** stilltur.  

## <a name="creating-new-records"></a>Nýjar færslur stofnaðar  
Sjálfgefið eru aðeins skrár í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] sem eru tengdar samstilltar eftir heildarsamstillingarverk. Hægt er að setja upp töfluvarpanir til að nýjar færslur verði stofnaðar á áfangastaðnum (t.d., [!INCLUDE[d365fin](includes/d365fin_md.md)]) fyrir hverja nýja færslu í upprunanum (t.d., [!INCLUDE[d365fin](includes/cds_long_md.md)]) sem ekki er þegar tengd.  

Til dæmis notar samstillingarverkið SÖLUFÓLK – Dynamics 365 Sales samstillingarverk töfluvörpunina SÖLUFÓLK. Samstillingarverkið afritar gögn úr notendafærslum í [!INCLUDE[d365fin](includes/cds_long_md.md)] yfir í sölufólksfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef töfluvörpun er sett upp til að stofna nýjar færslur er, fyrir hvern nýjan notanda í [!INCLUDE[d365fin](includes/cds_long_md.md)] sem er ekki þegar tengdur við sölumann í [!INCLUDE[d365fin](includes/d365fin_md.md)], stofnuð ný sölumannsfærsla í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Til að stofna nýjar færslur við samstillingu  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.

2.  Í færslu töfluvörpunar í listanum skal hreinsa reitinn **Samst. aðeins tengdar færslur** .  

## <a name="using-configuration-templates-on-table-mappings"></a>Nota skilgreiningarsniðmát í töfluvörpunum
Hægt er að úthluta skilgreiningarsniðmátum á töfluvarpanir til að nota fyrir nýjar færslur sem stofnaðar eru í [!INCLUDE[d365fin](includes/d365fin_md.md)] eða [!INCLUDE[d365fin](includes/cds_long_md.md)]. Fyrir hverja töfluvörpun má tilgreina skilgreiningarsniðmát til að nota fyrir nýjar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslur og annað sniðmát til að nota fyrir nýjar [!INCLUDE[d365fin](includes/cds_long_md.md)] færslur.  

Ef sett er upp sjálfgefinn samstillingargrunnur verða skilgreiningarsniðmátin yfirleitt búin til sjálfkrafa og notuð á töfluvörpun fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamenn og [!INCLUDE[crm_md](includes/crm_md.md)] lykla: **CDSCUST** og **CDSACCOUNT** .  

-   **CDSCUST** er notað til að stofna og samstilla nýja viðskiptamenn í [!INCLUDE[d365fin](includes/d365fin_md.md)] á grundvelli reikninga í [!INCLUDE[crm_md](includes/crm_md.md)].  

     Þetta sniðmát er búið til með því að afrita núverandi skilgreiningasniðmát fyrir viðskiptamenn í forritinu. **CDSCUST** er aðeins búið til ef skilgreiningarsniðmát er fyrirliggjandi og reiturinn **Gjaldmiðilskóði** í því sniðmáti er auður. Ef reitur í skilgreiningarsniðmát inniheldur gildi, verður það gildi notað í stað gildis í varpaða reitnum í reikningnum [!INCLUDE[d365fin](includes/cds_long_md.md)]. T.d. ef reiturinn **Land/Svæði** í lykli [!INCLUDE[d365fin](includes/cds_long_md.md)] inniheldur *Bandaríkin* og reiturinn **Land/Svæði** í skilgreiningarsniðmátinu er *Bretland* , þá er *Bretland* notað sem **Land/Svæði** fyrir viðskiptamanninn í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CDSACCOUNT** stofnar og samstillir nýja lykla í [!INCLUDE[d365fin](includes/cds_long_md.md)] sem byggist á lykli í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Til að tilgreina skilgreiningarsniðmát í töfluvörpunum  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.

2.  Í færslu töfluvörpunar í listanum, í reitnum **Sniðmátskóði fyrir skilgreiningartöflu** , skal velja skilgreiningarsniðmátið til að nota fyrir nýjar færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Stilla skal reitinn **Sniðmátskóði fyrir innri skilgreiningartöflu** á skilgreiningarsniðmátið til að nota fyrir nýjar færslur í [!INCLUDE[d365fin](includes/cds_long_md.md)].

## <a name="see-also"></a>Sjá einnig  
[Um samstillingu Dynamics 365 Business Central við [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Sérstilling Business Central og [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)   
[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
