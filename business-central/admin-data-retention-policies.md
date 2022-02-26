---
title: Hreinsa gögn með Varðveislustefnu
description: Hægt er að tilgreina hversu oft á að eyða tilteknum gerðum af gögnum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delete, data, retention, policy, policies
ms.search.form: 3903, 3901
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: ab16aacb7689287eac259658a8ef6bb355f04842
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012394"
---
# <a name="define-retention-policies"></a>Skilgreina varðveislureglur
Stjórnendur geta skilgreint varðveislureglur til að tilgreina hversu oft þeir vilja að [!INCLUDE[prod_short](includes/prod_short.md)] eyði úreltum gögnum í töflum sem innihalda kladdafærslur og safnvistaðar færslur. Til dæmis getur hreinsun á kladdafærslum gert auðveldara um vik að vinna með gögnin sem eiga við. Reglur geta innihaldið öll gögn í töflunum sem eru komin fram yfir lokadagsetninguna eða hægt er að bæta við síuskilyrðum sem innihalda aðeins tiltekin útrunnin gögn í reglunni. 

## <a name="required-setups-and-permissions"></a>Áskildar uppsetningar og heimildir
Áður en hægt er að búa til varðveislureglur þarf að setja upp eftirfarandi.

|Uppsetning  |Description  |
|---------|---------|
|**Leyfðar töflur**     |Við bjóðum upp á lista yfir töflur sem hafa má með í varðveislureglum. Hins vegar, ef ætlunin er að bæta töflum úr viðbót við varðveislureglu þarf þróunaraðili að bæta töflum notanda við listann. Frekari upplýsingar er að finna í [Viðbótin höfð með í varðveislureglu](admin-data-retention-policies.md#including-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Varðveislutímar**     |Tilgreina tímabil sem á að halda gögnum í töflunum í reglu. Tímabilin ákveða hversu oft gögnum verður eytt.         |

Þar að auki þarf að vera með heimildir yfirnotanda eða heimildasamstæðu fyrir uppsetningu varðveislureglu. Notendur sem fá heimildasamstæðuna fyrir uppsetningu varðveislureglu geta skilgreint varðveislureglur fyrir töflur, jafnvel þótt þeir hafi ekki heimildir til að lesa og eyða heimildum fyrir þessar töflur. Verkraðarfærslan verður að vera keyrð sem notandi með heimildir til að lesa og eyða gögnunum. Ráðlagt er að veita ekki heimildasamstæðu fyrir uppsetningu varðveislureglu til notenda sem ættu ekki að fá leyfi til að eyða gögnum.

> [!NOTE]
> Ef verið er að nota [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og ætlunin er að prófa varðveislureglur í Cronus-sýnigagnagrunninum, eru nokkrir hlutir sem þarf að gera. Sýnifyrirtækið inniheldur ekki töflur sem hægt er að nota með varðveislureglum og því þarf að bæta þeim við. Til að gera það skal stofna nýtt, autt fyrirtæki í sýnigagnagrunninum. Í nýja fyrirtækinu skal flytja inn grunnstillingapakkann RapidStart fyrir landið þitt sem samræmist staðlaða pakkanum NAV17.0.W1.ENU.STANDARD.rapidstart. Uppsetningargögnin fyrir varðveislureglur verða tiltækar í nýja fyrirtækinu.

### <a name="to-create-retention-periods"></a>Varðveislutímar búnir til
Varðveislutímar geta verið eins langir eða stuttir og þú vilt. Til að búa til varðveislutíma skal á síðunni **Varðveislureglur** nota aðgerðina **Varðveislutími**. Tímabilin sem eru skilgreind verða tiltæk fyrir allar reglur.

> [!NOTE]
> Af samræmisástæðum höfum við skilgreint lágmarks varðveislutíma fyrir sumar töflur. Ef varðveislutími er stilltur sem er styttri en lágmark sem krafist er, birtast skilaboð um áskilda tímabilið.

### <a name="set-up-a-retention-policy"></a>Setja upp varðveislureglu
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Varðveislureglur** og veldu síðan tengda tengilinn.
2. Í reitnum **Kenni töflu** skal velja töflu sem á að taka með í regluna.
3. Í reitnum **Varðveislutími** skal tilgreina tímalengdina sem geyma á gögnin í töflunni.
4. Valfrjálst: Til að nota regluna fyrir tiltekin gögn í töflu skal slökkva á Nota fyrir allar færslur. Flýtiflipinn Skrá varðveislureglu birtist þar sem hægt er að stilla síur til að búa til undirsafn af gögnum fyrir hverja línu. Frekari upplýsingar er að finna í [Síun](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Hver lína er með sinn eigin varðveislutíma. Ef annar varðveislutími er tilgreindur fyrir sömu gögnin, verður lengsti tíminn notaður. Sumar töflur innihalda líka síur sem ekki er hægt að breyta eða fjarlægja. Til að hjálpa til við að auðkenna þessar síur birtast þær í ljósari lit.

## <a name="applying-retention-policies"></a>Varðveislureglur settar á
Hægt er að nota verkraðarfærslu til að setja á varðveislureglur til að eyða gögnum sjálfkrafa eða setja reglur á handvirkt.

Til að nota varðveislureglu sjálfkrafa skal bara stofna og virkja reglu. Þegar regla er gerð virk búum við til verkraðarfærslu sem setur á varðveislureglur samkvæmt varðveislutímanum sem er tilgreindur. Allar varðveislureglur munu nota sömu verkraðarfærsluna. Sjálfgefið er að verkraðarfærslan beiti reglunni á hverjum degi kl. 02:00. Hægt er að breyta sjálfgildinu en ef það er gert mælum við með því að það keyri utan vinnutíma. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md). 

Hægt er að setj á reglu handvirkt með því að nota aðgerðina **Nota handvirkt** á síðunni **Varðveislureglur**. Ef ætlunin er að nota alltaf reglu handvirkt skal kveikja á **Handvirkt**. Verkraðarfærslan hunsar þá regluna þegar hún er keyrð.

## <a name="viewing-retention-policy-log-entries"></a>Kladdafærslur varðveislureglu skoðaðar
Hægt er að skoða verkþætti sem tengjast varðveislureglum á síðunni **Varðveislureglukladdi**. Til dæmis eru færslur búnar til þegar regla er notuð, eða ef villur komu upp þegar það var gert. 

## <a name="including-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Hafa með viðbótina í varðveislureglu (krefst aðstoðar frá þróunaraðila)
Að sjálfgefnu ná varðveislureglur aðeins yfir töflur sem eru teknar með í listanum yfir [!INCLUDE[prod_short](includes/prod_short.md)]-töflur sem við bjóðum upp á. Hægt er að fjarlægja sjálfgefnar töflur úr listanum og hægt er að bæta við eigin töflum. Það er sem sagt ekki hægt að bæta við töflu sem þú bjóst ekki til. Til dæmis er ekki hægt að bæta við öðrum töflum úr [!INCLUDE[prod_short](includes/prod_short.md)] eða úr viðbót sem hefur verið keypt.

Til að bæta töflum við listann yfir leyfðar töflur þarf þróunaraðili að bæta við kóða, til dæmis til að codeunit-uppsetningarforritið fyrir viðbótina (kóðaeining með undirgerðina *uppsetning*). 

Þegar þróunaraðili bætir við töflu getur hann tilgreint áskildar og sjálfgefnar síur. Ekki er hægt að fjarlægja áskildar síur eða breyta þeim síðar þegar töflum er bætt við til að skilgreina varðveislureglu. Sjálfgefnar síur eru bara vinalegar tillögur.

Eftirfarandi eru dæmi um hvernig á að bæta töflu við lista yfir leyfðar töflur með og án áskildra og sjálfgefinna sía. Fyrir flóknara dæmi skal skoða codeunit 3999 „Reten. Pol. Setja upp - BaseApp“. 

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

Eftirfarandi dæmi inniheldur áskilda síu.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Þegar þróunaraðili hefur bætt töflum við listann, getur stjórnandi haft þær með í varðveislureglu. 

## <a name="see-also"></a>Sjá einnig

[Greining á fjarmælingu á rakningu varðveislustefnu](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Endurskoðunarbreytingar í Business Central](across-log-changes.md)  
[Afmörkun](ui-enter-criteria-filters.md#filtering)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]