---
title: Samstilling Business Central og Common Data Service | Microsoft Docs
description: Kynntu þér hvernig á að samstilla gögn milli Business Central og Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 07/24/2020
ms.author: bholtorf
ms.openlocfilehash: 7e24351bb7382d01a060326ec8e592af555870a7
ms.sourcegitcommit: edad0d0b129e916c2cfdfa9c4f8d9d83513f4fd1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/24/2020
ms.locfileid: "3619385"
---
# <a name="scheduling-a-synchronization-between-business-central-and-common-data-service"></a>Áætla samstillingu milli Business Central og Common Data Service

Hægt er að samstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)] með áætluðu millibili með því að setja upp verk í verkröðinni. Samstillingarverkin samstilla gögn í [!INCLUDE[d365fin](includes/d365fin_md.md)] færslum og [!INCLUDE[cds_long_md](includes/cds_long_md.md)] færslum sem hafa þegar verið tengdar. Eða fyrir færslur sem eru ekki þegar tengdar, allt eftir stefnu samstillingar og reglum, geta samstillingarverk stofnað og tengd nýjar færslur í lendingarkerfinu. 

Nokkur samstillingarverk eru í boði beint úr kassanum. Verkin eru keyrð í eftirfarandi röð til að koma í veg fyrir tengsl tenginga milli eininga. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](/dynamics365/business-central/admin-job-queues-schedule-tasks.md).

1. GJALDMIÐILL – Common Data Service samstillingarverk.
2. LÁNARDROTTINN - Common Data Service samstillingarverk.
3. TENGILIÐUR - Common Data Service samstillingarverk.
4. VIÐSKIPTAMAÐUR - Common Data Service samstillingarverk.
5. SÖLUFÓLK - Common Data Service samstillingarverk.

Hægt er að skoða verkin á síðunni **Verkraðarfærslur**. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Sjálfgefnar Verkraðarfærslur samstillingar

Eftirfarandi tafla lýsir sjálfgefnu samstillingarverkunum fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Verkraðarfærsla | Description | Stefna | Vörpun samþættingartöflu | Sjálfgefin tíðni samstillinga (mín) | Sjálfgefinn hvíldarstaða vegna aðgerðarleysis (mín.) |
|--|--|--|--|--|--|--|
| TENGILIÐUR - Common Data Service samstillingarverk | Samstillir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] tengiliði við [!INCLUDE[d365fin](includes/d365fin_md.md)] tengiliði. | Í báðar áttir | Tengiliður | 30 | 720 <br>(12 klukkustundir) |
| GJALDMIÐILL – Common Data Service samstillingarverk | Samstillir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] færslugjaldmiðla við [!INCLUDE[d365fin](includes/d365fin_md.md)] gjaldmiðla. | Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | GJALDMIÐLAR | 30 | 720 <br> (12 klst.) |
| VIÐSKIPTAMAÐUR - Common Data Service samstillingarverk | Samstillir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] reikninga við [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamenn. | Í báðar áttir | VIÐSKIPTAMAÐUR | 30 | 720<br> (12 klst.) |
| LÁNARDROTTINN - Common Data Service samstillingarverk | Samstillir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] reikninga við [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamenn. | Í báðar áttir | Lánardrottinn | 30 | 720<br> (12 klst.) |
| SÖLUFÓLK – Common Data Service samstillingarverk | Samstillir [!INCLUDE[d365fin](includes/d365fin_md.md)] sölumenn við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] notendur. | Frá [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)] | SÖLUMENN | 30 | 1440<br> (24 klst.) |

## <a name="synchronization-process"></a>Samstillingarferli

Hvert verkraðarfærsla samstillingarverks notar sértæka vörpun samþættingartöflu sem tilgreinir hvaða [!INCLUDE[d365fin](includes/d365fin_md.md)] töflu og [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einingu á að samstilla. Töfluvarpanir innihalda einnig nokkrar stillingar sem stýra því hvaða færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] töflunni [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einingunni verða samstilltar.  

Til að samstilla gögn verða [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einingafærslur að vera tengdar við [!INCLUDE[d365fin](includes/d365fin_md.md)] færslur. Til dæmis verður [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamaður að vera tengdur við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] reikning. Þú getur sett upp tengi handvirkt, áður en samstillingarverk eru keyrð, eða láta samstillingu störf setja upp tengi sjálfkrafa. Eftirfarandi listi lýsir því hvernig gögn eru samstillt milli Common Data Service og [!INCLUDE[d365fin](includes/d365fin_md.md)] og þegar þú ert að nota verkraðarfærslur samstillingarverka. Frekari upplýsingar er að finna í [Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md).

- **Samstilla aðeins tengdar færslur** gátreiturinn stjórnar því hvort nýjar færslur séu stofnaðar þegar þú samstillir. Sjálfgefið er að gátreiturinn sé valinn, sem merkir að aðeins færslur sem eru tengdar eru samstilltar. Í vörpun samþættingartöflu getur þú breytt töfluvörpun á milli [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einingar og [!INCLUDE[d365fin](includes/d365fin_md.md)] töflu þannig að heildasamstillingarverkin stofni nýjar færslur í endanlegum gagnagrunni fyrir hverja færslu í upprunagagnagrunninum sem ekki var tengd. Frekari upplýsingar eru í [Stofna nýjar færslur](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).

    **Dæmi** Ef þú hreinsar  gátreitinn **Samstilla aðeins tengdar færslur**, þegar þú samstillir viðskiptamenn[!INCLUDE[d365fin](includes/d365fin_md.md)] með reikninga í [!INCLUDE[cds_long_md](includes/cds_long_md.md)], er nýr reikningur búinn til hvern viðskiptamann [!INCLUDE[d365fin](includes/d365fin_md.md)] og hann tengdur sjálfkrafa. Auk þessa, þar sem samstilling í þessu tilfelli er tvíátta, er nýr viðskiptamaður búinn til og tengdur fyrir hvern [!INCLUDE[cds_long_md](includes/cds_long_md.md)] reikning sem er ekki þegar tengdur.  

    > [!NOTE]  
    > Til eru reglur og afmarkanir sem ákvarða hvaða gögn eru samstillt. Frekari upplýsingar eru í [Samstillingarreglur](admin-synchronizing-business-central-and-sales.md).

- Þegar nýjar færslur eru stofnaðar í [!INCLUDE[d365fin](includes/d365fin_md.md)], nota þær annaðhvort sniðmát sem er skilgreint fyrir vörpun samþættingartöflunnar eða sjálfgefna sniðmátið sem tiltækt er fyrir færslugerðina. Reitirnir eru fylltir með gögnum úr [!INCLUDE[d365fin](includes/d365fin_md.md)] eða [!INCLUDE[cds_long_md](includes/cds_long_md.md)], fer eftir samstillingaráttinni. Frekari upplýsingar er að finna í [Breyta töfluvörpunum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Við síðari samstillingar, aðeins skrár sem hafa verið breytt eða bætt við eftir síðustu árangursríka samstillingu starf fyrir aðila verður uppfærður.  

     Nýjum færslum í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] er bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef gögnum í reitum í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] færslum hafa breyst eru gögnin afrituð í samsvarandi reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- Við tvíátta samstillingu er verkið samstillt frá [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], og því næst frá [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="about-inactivity-timeouts"></a>Um tímalokun vegna aðgerðaleysis

Í sumum verkraðarfærslum, eins og þeim sem tímasetja samstillingu á milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)], skaltu nota reitinn **Tímalokun** á verkraðarfærsluspjaldi til að koma í veg fyrir að verkraðarfærslan sé í gangi að óþörfu.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Flæðirit fyrir verkraðarfærslur sem eru settar í bið vegna óvirkni.":::

Þegar gildið í þessum reit er ekki núll og verkröðin fann engar breytingar í síðustu keyrslu, setur [!INCLUDE[d365fin](includes/d365fin_md.md)] verkraðarfærsluna í bið. Þegar það gerist mun reiturinn **Staða verkraðarfærslu** sýna **Í bið vegna aðgerðaleysis** og [!INCLUDE[d365fin](includes/d365fin_md.md)] mun bíða í þann tíma sem hefur verið skilgreindur í **Tímabil lokunar** reitnum áður en hann keyrir verkraðarfærslu aftur.  

Til dæmis er sjálfgefið að GJALDMIÐILL verkraðarfærsla, sem samstillir gjaldmiðla í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] með gengi í [!INCLUDE[d365fin](includes/d365fin_md.md)], leita að breytingum á gengi á 30 mínútna fresti. Ef engar breytingar finnast setur [!INCLUDE[d365fin](includes/d365fin_md.md)] GJALDMIÐILL verkraðarfærslu í bið í 720 mínútur (sex klukkustundir). Ef gengi er breytt í [!INCLUDE[d365fin](includes/d365fin_md.md)] á meðan verkraðarfærslan er í bið mun [!INCLUDE[d365fin](includes/d365fin_md.md)] sjálfkrafa endurvirkja verkraðarfærslu og endurræsa verkröðina. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] mun sjálfkrafa virkja verkraðarfærslur sem eru í bið þegar breytingar verða í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Breytingar í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] munu ekki virkja verkraðarfærslur.

## <a name="to-view-the-synchronization-job-log"></a>Til að skoða kladda samstillingarverks

1. Veldu :::image type="icon" source="media/ui-search/search_small.png" border="false"::: táknið, sláðu inn **Samstillingarkladdi samþættingar** og veldu síðan tengda tengilinn.
2. Ef ein eða fleiri villur koma upp í samstillingarverki birtist fjöldi villna í dálkinum **Mistókst** . Veljið þá tölu til að skoða villur í verkinu.  

    > [!TIP]  
    > Þú getur skoðað allar villur í samstillingaverkum með því að opna villukladda samstillingarverka beint.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Til að skoða kladda samstillingarverks úr töfluvörpunum

1. Veldu :::image type="icon" source="media/ui-search/search_small.png" border="false"::: táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.
2. Á síðunni **Vörpun samþættingartöflu** skal velja færslu og síðan velja **Kladdi fyrir samstillingarverk samþættingar**.  

## <a name="to-view-the-synchronization-error-log"></a>Til að skoða villukladda samstillingar

- Veldu :::image type="icon" source="media/ui-search/search_small.png" border="false"::: táknið, sláðu inn **Villur í samstillingu samþættingar** og veldu síðan tengda tengilinn.

## <a name="see-also"></a>Sjá einnig

[Samstilling gagna í Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Samstilla töfluvarpanir handvirkt](admin-manual-synchronization-of-table-mappings.md)  
[Áætla samstillingu milli Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Um samstillingu Dynamics 365 Business Central við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
