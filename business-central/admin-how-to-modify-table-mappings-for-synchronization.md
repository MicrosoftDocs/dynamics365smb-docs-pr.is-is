---
title: Breyta töfluvörpunum fyrir samstillingu | Microsoft Docs
description: Kynntu þér hvernig á að breyta töfluvörpunum sem eru notaðar þegar gögn eru samstillt milli Business Central og Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: de924baa494ae00c09dcb7657c050f2d9ae3ba87
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "940206"
---
# <a name="modify-table-mappings-for-synchronization"></a>Breyta töfluvörpunum fyrir samstillingu
Vörpun samþættingartöflu tengir töflu í [!INCLUDE[d365fin](includes/d365fin_md.md)] við samþættingartöflu fyrir eininguna [!INCLUDE[crm_md](includes/crm_md.md)]. Fyrir hverja einingu í [!INCLUDE[crm_md](includes/crm_md.md)] sem á að samstilla við samsvarandi gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)]], verður að vera samsvarandi vörpun samþættingartöflu. Vörpun samþættingartöflu felur í sér nokkrar stillingar sem gera kleift að stjórna hvernig færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]-töflu og [!INCLUDE[crm_md](includes/crm_md.md)]-einingu eru samstilltar af samsvarandi heildarsamþættingarverkum.  

## <a name="filtering-records"></a>Afmarka færslur  
 Ef þú vilt ekki að samstilla allar færslur fyrir tiltekna einingu í [!INCLUDE[crm_md](includes/crm_md.md)] eða töflu í [!INCLUDE[d365fin](includes/d365fin_md.md)], getur þú sett upp síur til að takmarka færslur sem eru samstilltar. Afmarkanir eru settar upp á síðunni **Varpanir samþættingartöflu**.  

#### <a name="to-filter-records-for-synchronization"></a>Til að afmarka færslur fyrir samstillingu  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Varpanir samþættingartöflu** og veldu síðan viðeigandi tengil.

2.  Til að afmarka [!INCLUDE[d365fin](includes/d365fin_md.md)] skrár er reiturinn **Töfluafmörkun** stilltur.  

3.  Til að afmarka [!INCLUDE[crm_md](includes/crm_md.md)] skrár er reiturinn **Afmörkun samþættingartöflu** stilltur.  

## <a name="creating-new-records"></a>Nýjar færslur stofnaðar  
 Sjálfgefið eru aðeins skrár í [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] sem eru tengdar samstilltar eftir heildarsamstillingarverk. Hægt er að setja upp töfluvarpanir til að nýjar færslur verði stofnaðar á áfangastaðnum (t.d., [!INCLUDE[d365fin](includes/d365fin_md.md)]) fyrir hverja nýja færslu í upprunanum (t.d., [!INCLUDE[crm_md](includes/crm_md.md)]) sem ekki er þegar tengd.  

 Til dæmis notar samstillingarverkið SÖLUFÓLK – Dynamics 365 for Sales samstillingarverk fyrir Dynamics CRM töfluvörpunina SÖLUFÓLK. Samstillingarverkið afritar gögn úr notendafærslum í [!INCLUDE[crm_md](includes/crm_md.md)] yfir í sölufólksfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef töfluvörpun er sett upp til að stofna nýjar færslur er, fyrir hvern nýjan notanda í [!INCLUDE[crm_md](includes/crm_md.md)] sem er ekki þegar tengdur við sölumann í [!INCLUDE[d365fin](includes/d365fin_md.md)], stofnuð ný sölumannsfærsla í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Til að stofna nýjar færslur við samstillingu  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Varpanir samþættingartöflu** og veldu síðan viðeigandi tengil.

2.  Í færslu töfluvörpunar í listanum skal hreinsa reitinn **Samst. aðeins tengdar færslur**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Nota skilgreiningarsniðmát í töfluvörpunum
Hægt er að úthluta skilgreiningarsniðmátum á töfluvarpanir til að nota fyrir nýjar færslur sem stofnaðar eru í [!INCLUDE[d365fin](includes/d365fin_md.md)] eða [!INCLUDE[crm_md](includes/crm_md.md)]. Fyrir hverja töfluvörpun má tilgreina skilgreiningarsniðmát til að nota fyrir nýjar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslur og annað sniðmát til að nota fyrir nýjar [!INCLUDE[crm_md](includes/crm_md.md)] færslur.  

Ef sett er upp sjálfgefinn samstillingargrunnur verða skilgreiningarsniðmátin yfirleitt búin til sjálfkrafa og notuð á töfluvörpun fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamenn og [!INCLUDE[crm_md](includes/crm_md.md)] lykla: **CRMCUST** og **CRMACCOUNT**.  

-   **CRMCUST** er notað til að stofna og samstilla nýja viðskiptamenn í [!INCLUDE[d365fin](includes/d365fin_md.md)] á grundvelli reikninga í [!INCLUDE[crm_md](includes/crm_md.md)].  

     Þetta sniðmát er búið til með því að afrita núverandi skilgreiningasniðmát fyrir viðskiptamenn í forritinu. **CRMCUST** er aðeins búið til ef skilgreiningarsniðmát er fyrirliggjandi og reiturinn **Gjaldmiðilskóði** í því sniðmáti er auður. Ef reitur í skilgreiningarsniðmát inniheldur gildi, verður það gildi notað í stað gildis í varpaða reitnum í reikningnum [!INCLUDE[crm_md](includes/crm_md.md)]. T.d. ef reiturinn **Land/Svæði** í lykli [!INCLUDE[crm_md](includes/crm_md.md)] inniheldur *Bandaríkin* og reiturinn **Land/Svæði** í skilgreiningarsniðmátinu er *Bretland*, þá er *Bretland* notað sem **Land/Svæði** fyrir viðskiptamanninn í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** stofnar og samstillir nýja lykla í [!INCLUDE[crm_md](includes/crm_md.md)] sem byggist á lykli í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Til að tilgreina skilgreiningarsniðmát í töfluvörpunum  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Varpanir samþættingartöflu** og veldu síðan viðeigandi tengil.

2.  Í færslu töfluvörpunar í listanum, í reitnum **Sniðmátskóði fyrir skilgreiningartöflu**, skal velja skilgreiningarsniðmátið til að nota fyrir nýjar færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Stilla skal reitinn **Sniðmátskóði fyrir innri skilgreiningartöflu** á skilgreiningarsniðmátið til að nota fyrir nýjar færslur í [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Sjá einnig  
[Um samstillingu Dynamics 365 Business Central við Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Sérstilling Business Central og Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
