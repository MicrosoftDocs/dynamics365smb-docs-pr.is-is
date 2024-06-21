---
title: Hreinsa gögn með varðveislureglum
description: Hægt er að tilgreina hversu oft á að eyða tilteknum gerðum af gögnum.
author: brentholtorf
ms.topic: conceptual
ms.author: bholtorf
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 12/15/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Skilgreina varðveislureglur

Í þessari grein er því lýst hvernig stjórnendur geta skilgreint varðveitingarstefnu til að tilgreina hversu oft á að eyða úreltum gögnum í töflum sem innihalda skráafærslur og geymdar færslur. Til dæmis er auðveldara að hreinsa skráarfærslur með viðeigandi gögnum. Stefnur geta eytt gögnum sem byggð eru á fyrningardagsetningu eða bætt við afmörkunum til að innihalda aðeins tiltekin útrunnin gögn.

## Nauðsynlegar uppsetningar og heimildir

Áður en hægt er að stofna varðveitingarstefnu þarf að setja upp töflur til að taka með og tímabilin til að geyma gögn.

|Uppsetning  |Heimildasamstæða  |
|---------|---------|
|**Leyfðar töflur**     |Við bjóðum upp á lista yfir töflur sem þú getur innifalið í varðveislustefnum. Ef bæta á töflum úr viðbót við varðveislustefnu verður forritari að bæta töflum sínum við listann. Nánari upplýsingar má fá með því að nota [viðbótina þína í varðveitingarstefnu](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Varðveislutímar**     |Tilgreina tímabil sem á að halda gögnum í töflunum í reglu. Tímabilin ákvarða hversu oft gögnum er eytt.         |

Að auki verður að vera með **SUPER-notandaheimildirnar** eða **heimildina Uppsetning** varðveitingarstefnu. Notendur sem hafa heimild fyrir uppsetningu varðveitingarstefnu geta skilgreint varðveitingarstefnu fyrir töflur. Það er rétt þó að þær hafi ekki Lesa og Eyða heimildum fyrir töflurnar. Verkraðarfærslan verður að vera keyrð sem notandi með heimildir til að lesa og eyða gögnunum. Ekki veita notendum heimild fyrir uppsetningu varðveitingarstefnu stilltir á notendur sem eiga ekki að hafa heimild til að eyða gögnum.

> [!NOTE]
> Ef notað er [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss og prófa á varðveislustefnu í Cronus-sýnigagnagrunninum er þörf á nokkrum hlutum. Sýnifyrirtækið inniheldur ekki töflur sem hægt er að nota með varðveislustefnum svo að bæta þurfi þeim við. Til að gera það skal stofna nýtt, autt fyrirtæki í sýnigagnagrunninum. Í nýja fyrirtækinu skal flytja inn RapidStart grunnstillingarpakkann fyrir landið/svæðið sem samsvarar stöðluðu NAV17.0.W1.ENU.STANDARD.rapidstart-pakkanum. Uppsetningargögnin fyrir varðveislureglur verða tiltækar í nýja fyrirtækinu.

### Stofna varðveitingartímabil

Varðveislutímar geta verið eins langir eða stuttir og þú vilt. Til að búa til varðveislutíma skal á síðunni **Varðveislureglur** nota aðgerðina **Varðveislutími**. Tímabilin sem eru skilgreind eru tiltæk fyrir allar stefnur.

> [!NOTE]
> Af samræmisástæðum höfum við skilgreint lágmarks varðveislutíma fyrir sumar töflur. Ef varðveislutímabil er stillt sem er styttra en lágmarksþörf birtast boð um það tímabil.

### Setja upp varðveislureglu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Varðveislureglur** og veldu síðan tengda tengilinn.
2. Í reitnum **Kenni töflu** skal velja töflu sem á að taka með í regluna.
3. Í reitnum **Varðveislutími** skal tilgreina tímalengdina sem geyma á gögnin í töflunni.
4. Valfrjálst: Hægt er að beita reglunni á tiltekin gögn í töflu frekar en allar færslur, með því að afmarka gögnin fyrir hverja línu. Stefnan gildir aðeins um færslurnar sem afmarkanirnar skila. Til að tilgreina afmörkunarskilyrðin skal slökkva á **vífæra á öllum færslum** . Flýtiflipinn **Varðveitingarstefna** færslu sýnir, þar sem hægt er að setja afmörkunarskilyrði. Nánari upplýsingar um hvernig afmarkanir virka er farið í [Afmörkun](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Hver lína er með sinn eigin varðveislutíma. Ef tilgreind eru mismunandi varðveitingartímabil fyrir sömu gögn er lengsta tímabilið notað. Sumar töflur innihalda einnig afmarkanir sem ekki er hægt að breyta eða fjarlægja. Til að hjálpa til við að auðkenna þessar síur birtast þær í ljósari lit.

#### Vídeóleiðbeiningar

Myndbandið gefur dæmi um hvernig setja á upp varðveislustefnu.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## Beita varðveitingarreglum

Hægt er að nota verkraðarfærslu til að setja á varðveislureglur til að eyða gögnum sjálfkrafa eða setja reglur á handvirkt.

Til að nota varðveislureglu sjálfkrafa skal bara stofna og virkja reglu. Þegar regla er virkjuð [!INCLUDE [prod_short](includes/prod_short.md)]  stofnar verkraðarfærsla sem á við hana samkvæmt varðveitingartímabili hennar. Allar varðveislureglur munu nota sömu verkraðarfærsluna. Sjálfgefið er að verkraðarfærslan beiti reglunni á hverjum degi kl. 02:00. Hægt er að breyta sjálfgildinu en ef það er gert mælum við með því að það keyri utan vinnutíma. Nánari upplýsingar eru notaðar með því að fara í [Nota verkröð til að tímasetja verkhluta](admin-job-queues-schedule-tasks.md). 

Hægt er að setj á reglu handvirkt með því að nota aðgerðina **Nota handvirkt** á síðunni **Varðveislureglur**. Ef ætlunin er að nota alltaf reglu handvirkt skal kveikja á **Handvirkt**. Verkraðarfærslan hunsar þá regluna þegar hún er keyrð.

## Skoða færslur í skrá varðveitingarreglu

Hægt er að skoða verkþætti sem tengjast varðveislureglum á síðunni **Varðveislureglukladdi**. Færslur eru til dæmis stofnaðar þegar reglum er beitt, eða ef villur komu upp.

## Hafa viðbótina með í varðveislustefnu (krefst aðstoðar frá forritara)

Sjálfgefið er að varðveislureglur nái aðeins [!INCLUDE[prod_short](includes/prod_short.md)] yfir þann lista sem við bjóðum upp á. Hægt er að fjarlægja sjálfgefnar töflur úr listanum og hægt er að bæta við eigin töflum. Það er ekki hægt að bæta við töflu sem notandi stofnaði ekki sjálfur. Til dæmis er ekki hægt að bæta við öðrum töflum úr [!INCLUDE[prod_short](includes/prod_short.md)] eða úr viðbót sem keypt hefur verið inn.

Til að bæta töflunum við töflulistann þarf forritari að bæta einhverjum kóta við. Til dæmis til uppsetningarkótaeiningar fyrir viðbótina (codeunit með undirtegund *uppsetningar*).

Þegar þróunaraðili bætir við töflu getur hann tilgreint áskildar og sjálfgefnar síur. Áskildar afmarkanir er ekki hægt að fjarlægja eða breyta síðar þegar töflum er bætt við til að skilgreina varðveitingarstefnu. Sjálfgefnu afmarkanirnar eru bara tillögur.

Eftirfarandi eru dæmi um hvernig á að bæta töflu við lista yfir leyfðar töflur með og án áskildra og sjálfgefinna sía. Til að fá flóknari dæmi er farið í codeunit 3999 "Varðveita. Pol. Setja upp - BaseApp“.

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

## Sjá einnig .

[Greining á fjarmælingu á rakningu varðveislustefnu](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Endurskoðunarbreytingar í Business Central](across-log-changes.md)  
[Afmörkun](ui-enter-criteria-filters.md#filtering)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]