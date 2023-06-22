---
title: Sérstilling Business Central og Dataverse
description: Kynntu þér hvernig á að samstilla gögn milli Business Central og Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
---

# <a name="scheduling-a-synchronization-between-business-central-and-dataverse" />Áætla samstillingu milli Business Central og Dataverse

Hægt er að samstilla [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)] með áætluðu millibili með því að setja upp verk í verkröðinni. Samstillingarvinnslur samstilla gögn í  [!INCLUDE[prod_short](includes/prod_short.md)]  færslum og  [!INCLUDE[cds_long_md](includes/cds_long_md.md)]  færslum sem eru samkeyrðar. Fyrir færslur sem eru ekki þegar í samræmi við stefnu og reglur er hægt að stofna samstillingarvinnslur og nokkrar nýjar færslur í viðtökukerfinu.

Nokkur samstillingarverk eru í boði beint úr kassanum. Verkin eru keyrð í eftirfarandi röð til að koma í veg fyrir tengsl tenginga milli taflanna. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

1. GJALDMIÐILL – Common Data Service samstillingarverk.
2. LÁNARDROTTINN - Common Data Service samstillingarverk.
3. TENGILIÐUR - Common Data Service samstillingarverk.
4. VIÐSKIPTAMAÐUR - Common Data Service samstillingarverk.
5. SÖLUFÓLK - Common Data Service samstillingarverk.

Hægt er að skoða verkin á síðunni **Verkraðarfærslur**. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries" />Sjálfgefnar færslur vinnsluraðar vinnslu

Eftirfarandi tafla lýsir sjálfgefnu samstillingarverkunum fyrir [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Verkraðarfærsla | Description | Stefna | Vörpun samþættingartöflu | Sjálfgefin tíðni samstillinga (mín) | Sjálfgefinn hvíldarstaða vegna aðgerðarleysis (mín.) |
|--|--|--|--|--|--|--|
| TENGILIÐUR - Common Data Service samstillingarverk | Samstillir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] tengiliði við [!INCLUDE[prod_short](includes/prod_short.md)] tengiliði. | Í báðar áttir | Tengiliður | 30 | 720 <br>(12 klukkustundir) |
| GJALDMIÐILL – Common Data Service samstillingarverk | Samstillir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] færslugjaldmiðla við [!INCLUDE[prod_short](includes/prod_short.md)] gjaldmiðla. | Frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | GJALDMIÐLAR | 30 | 720 <br> (12 klst.) |
| VIÐSKIPTAMAÐUR - Common Data Service samstillingarverk | Samstillir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] reikninga við [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamenn. | Í báðar áttir | VIÐSKIPTAMAÐUR | 30 | 720<br> (12 klst.) |
| LÁNARDROTTINN - Common Data Service samstillingarverk | Samstillir [!INCLUDE[cds_long_md](includes/cds_long_md.md)] reikninga við [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamenn. | Í báðar áttir | Lánardrottinn | 30 | 720<br> (12 klst.) |
| SÖLUFÓLK – Common Data Service samstillingarverk | Samstillir [!INCLUDE[prod_short](includes/prod_short.md)] sölumenn við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] notendur. | Frá [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] | SÖLUMENN | 30 | 1440<br> (24 klst.) |

## <a name="synchronization-process" />Samstillingarferli

Hvert verkraðarfærsla samstillingarverks notar sértæka vörpun samþættingartöflu sem tilgreinir hvaða [!INCLUDE[prod_short](includes/prod_short.md)] töflu og [!INCLUDE[cds_long_md](includes/cds_long_md.md)] töflu á að samstilla. Töfluvarpanir innihalda einnig nokkrar stillingar sem stýra því hvaða færslur í [!INCLUDE[prod_short](includes/prod_short.md)] töflunni [!INCLUDE[cds_long_md](includes/cds_long_md.md)] töflunni verða samstilltar.  

Til að samstilla gögn verða [!INCLUDE[cds_long_md](includes/cds_long_md.md)] töflur að vera tengdar við [!INCLUDE[prod_short](includes/prod_short.md)] færslur. Til dæmis verður [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamaður að vera tengdur við [!INCLUDE[cds_long_md](includes/cds_long_md.md)] reikning. Þú getur sett upp tengi handvirkt, áður en samstillingarverk eru keyrð, eða láta samstillingu störf setja upp tengi sjálfkrafa. Eftirfarandi listi lýsir því hvernig gögn eru samstillt milli [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] og þegar þú ert að nota verkraðarfærslur samstillingarverka. Frekari upplýsingar er að finna í [Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md).

- **Samstilla aðeins tengdar færslur** gátreiturinn stjórnar því hvort nýjar færslur séu stofnaðar þegar þú samstillir. Sjálfgefið er að gátreiturinn sé valinn, sem merkir að aðeins færslur sem eru tengdar eru samstilltar. Í vörpun samþættingartöflu getur þú breytt töfluvörpun á milli [!INCLUDE[cds_long_md](includes/cds_long_md.md)] töflu og [!INCLUDE[prod_short](includes/prod_short.md)] töflu þannig að heildasamstillingarverkin stofni nýjar færslur í endanlegum gagnagrunni fyrir hverja línu í upprunagagnagrunninum sem ekki var tengd. Frekari upplýsingar er að finna  [í stofnun nýrrar skráningar](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Dæmi** Ef þú hreinsar  gátreitinn **Samstilla aðeins tengdar færslur**, þegar þú samstillir viðskiptamenn[!INCLUDE[prod_short](includes/prod_short.md)] með reikninga í [!INCLUDE[cds_long_md](includes/cds_long_md.md)], er nýr reikningur búinn til hvern viðskiptamann [!INCLUDE[prod_short](includes/prod_short.md)] og hann tengdur sjálfkrafa. Auk þessa, þar sem samstilling í þessu tilfelli er tvíátta, er nýr viðskiptamaður búinn til og tengdur fyrir hvern [!INCLUDE[cds_long_md](includes/cds_long_md.md)] reikning sem er ekki þegar tengdur.  

    > [!NOTE]  
    > Til eru reglur og afmarkanir sem ákvarða hvaða gögn eru samstillt. Frekari upplýsingar er að fara í  [samstillingarreglur](admin-synchronizing-business-central-and-sales.md).

- Þegar nýjar færslur eru stofnaðar í [!INCLUDE[prod_short](includes/prod_short.md)], nota þær annaðhvort sniðmát sem er skilgreint fyrir vörpun samþættingartöflunnar eða sjálfgefna sniðmátið sem tiltækt er fyrir línugerðina. Reitirnir eru fylltir með gögnum úr [!INCLUDE[prod_short](includes/prod_short.md)] eða [!INCLUDE[cds_long_md](includes/cds_long_md.md)], fer eftir samstillingaráttinni. Frekari upplýsingar er að finna í [Breyta töfluvörpunum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Við síðari samstillingar verða aðeins færslur sem hafa verið breytt eða bætt við eftir síðasta árangursríka samstillingarverk fyrir töflu uppfærðar.  

     Nýjum færslum í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] er bætt við [!INCLUDE[prod_short](includes/prod_short.md)]. Ef gögnum í reitum í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] færslum hafa breyst eru gögnin afrituð í samsvarandi reiti í [!INCLUDE[prod_short](includes/prod_short.md)].  

- Við tvíátta samstillingu er verkið samstillt frá [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], og því næst frá [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts" />Um tímafrekari tímalóvirkni

Í sumum verkraðarfærslum, eins og þeim sem tímasetja samstillingu á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)], skaltu nota reitinn **Tímalokun** á SÍÐU verkraðarfærslu til að koma í veg fyrir að verkraðarfærslan sé í gangi að óþörfu.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Flæðirit fyrir verkraðarfærslur sem eru settar í bið vegna óvirkni.":::

Þegar gildið í þessum reit er ekki núll og verkröðin fann engar breytingar í síðustu keyrslu, setur [!INCLUDE[prod_short](includes/prod_short.md)] verkraðarfærsluna í bið. Þegar það gerist mun reiturinn **Staða verkraðarfærslu** sýna **Í bið vegna aðgerðaleysis** og [!INCLUDE[prod_short](includes/prod_short.md)] mun bíða í þann tíma sem hefur verið skilgreindur í **Tímabil lokunar** reitnum áður en hann keyrir verkraðarfærslu aftur.  

Til dæmis er sjálfgefið að GJALDMIÐILL verkraðarfærsla, sem samstillir gjaldmiðla í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] með gengi í [!INCLUDE[prod_short](includes/prod_short.md)], leita að breytingum á gengi á 30 mínútna fresti. Ef engar breytingar finnast setur [!INCLUDE[prod_short](includes/prod_short.md)] GJALDMIÐILL verkraðarfærslu í bið í 720 mínútur (tólf klukkustundir). Ef gengi er breytt í [!INCLUDE[prod_short](includes/prod_short.md)] á meðan verkraðarfærslan er í bið mun [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa endurvirkja verkraðarfærslu og endurræsa verkröðina. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] mun sjálfkrafa virkja verkraðarfærslur sem eru í bið þegar breytingar verða í [!INCLUDE[prod_short](includes/prod_short.md)]. Breytingar í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] munu ekki virkja verkraðarfærslur.

## <a name="to-view-the-synchronization-job-log" />Til að skoða kladda samstillingarverks

1. Veldu :::image type="icon" source="media/ui-search/search_small.png" border="false"::: táknið, sláðu inn **Samstillingarkladdi samþættingar** og veldu síðan tengda tengilinn.
2. Ef ein eða fleiri villur koma upp í samstillingarverki birtist fjöldi villna í dálkinum **Mistókst** . Veljið þá tölu til að skoða villur í verkinu.  

    > [!TIP]  
    > Þú getur skoðað allar villur í samstillingaverkum með því að opna villukladda samstillingarverka beint.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings" />Til að skoða kladda samstillingarverks úr töfluvörpunum

1. Veldu :::image type="icon" source="media/ui-search/search_small.png" border="false"::: táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.
2. Á síðunni **Vörpun samþættingartöflu** skal velja færslu og síðan velja **Kladdi fyrir samstillingarverk samþættingar**.  

## <a name="to-view-the-synchronization-error-log" />Til að skoða villukladda samstillingar

- Veldu :::image type="icon" source="media/ui-search/search_small.png" border="false"::: táknið, sláðu inn **Villur í samstillingu samþættingar** og veldu síðan tengda tengilinn.

## <a name="see-also" />Sjá einnig .

[Samstilling gagna í Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Samstilla töfluvarpanir handvirkt](admin-manual-synchronization-of-table-mappings.md)  
[Áætla samstillingu milli Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Um samstillingu Dynamics 365 Business Central við [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
