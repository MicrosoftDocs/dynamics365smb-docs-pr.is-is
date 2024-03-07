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
---
# Skilgreina varðveislureglur

Þessi grein lýsir því hvernig stjórnendur geta skilgreint varðveislustefnur til að tilgreina hversu oft á að eyða úreltum gögnum í töflum sem innihalda annálsfærslur og geymsluskrár. Til dæmis, með því að hreinsa upp færslur í annálum getur það auðveldað að vinna með viðeigandi gögn. Reglur geta eytt gögnum á grundvelli fyrningardagsetningar, eða þú getur bætt við síum til að innihalda aðeins ákveðin útrunnið gögn.

## Nauðsynlegar uppsetningar og heimildir

Áður en þú getur búið til varðveislustefnur verður þú að setja upp töflurnar til að innihalda og tíma til að geyma gögn.

|Uppsetning  |Heimildasamstæða  |
|---------|---------|
|**Leyfðar töflur**     |Við bjóðum upp á lista yfir töflur sem þú getur haft með í varðveislureglum. Ef þú vilt bæta töflum úr viðbót við varðveislustefnu verður þróunaraðili að bæta töflunum sínum við listann. Til að fá frekari upplýsingar skaltu fara á [Ta með viðbótina þína í varðveislustefnu](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Varðveislutímar**     |Tilgreina tímabil sem á að halda gögnum í töflunum í reglu. Tímabilin ákvarða hversu oft gögnum er eytt.         |

Að auki verður þú að hafa **SUPER** notendaheimildir eða **uppsetning varðveislustefnu** heimilda. Notendur sem hafa heimildasettið Uppsetning varðveislustefnu geta skilgreint varðveislustefnur fyrir töflur. Það er satt, jafnvel þótt þeir hafi ekki Lestur og Eyða heimildir fyrir borðin. Verkraðarfærslan verður að vera keyrð sem notandi með heimildir til að lesa og eyða gögnunum. Ekki veita heimildasettinu fyrir uppsetningu varðveislustefnu til notenda sem ættu ekki að fá að eyða gögnum.

> [!NOTE]
> Ef þú ert að nota [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og vilt prófa varðveislustefnur í Cronus sýnikennslugagnagrunninum, þá eru nokkur atriði sem þú þarft að gera. Sýningarfyrirtækið inniheldur ekki töflur sem þú getur notað með varðveislustefnu, svo þú þarft að bæta þeim við. Til að gera það skal stofna nýtt, autt fyrirtæki í sýnigagnagrunninum. Í nýja fyrirtækinu skaltu flytja inn RapidStart stillingarpakkann fyrir landið/svæðið þitt sem samsvarar staðalnum NAV17.0.W1.ENU.STANDARD.rapidstart pakkanum. Uppsetningargögnin fyrir varðveislureglur verða tiltækar í nýja fyrirtækinu.

### Búðu til varðveislutímabil

Varðveislutímar geta verið eins langir eða stuttir og þú vilt. Til að búa til varðveislutíma skal á síðunni **Varðveislureglur** nota aðgerðina **Varðveislutími**. Tímabilin sem þú skilgreinir eru tiltæk fyrir allar reglur.

> [!NOTE]
> Af samræmisástæðum höfum við skilgreint lágmarks varðveislutíma fyrir sumar töflur. Ef þú stillir varðveislutíma sem er styttri en lágmarkskröfur birtast skilaboð um skyldutímabilið.

### Setja upp varðveislureglu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Varðveislureglur** og veldu síðan tengda tengilinn.
2. Í reitnum **Kenni töflu** skal velja töflu sem á að taka með í regluna.
3. Í reitnum **Varðveislutími** skal tilgreina tímalengdina sem geyma á gögnin í töflunni.
4. Valfrjálst: Þú getur notað stefnuna á tiltekin gögn í töflu, frekar en allar færslur, með því að sía gögnin fyrir hverja línu. Reglan mun aðeins gilda um þær færslur sem síurnar skila. Til að tilgreina síuviðmiðin skaltu slökkva á **Beita á allar færslur** rofa.  **Stefna um varðveislu gagna** Fastflipi birtist þar sem þú getur stillt síuviðmið. Til að læra meira um hvernig síur virka skaltu fara í [Síun](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Hver lína er með sinn eigin varðveislutíma. Ef þú tilgreinir mismunandi varðveislutíma fyrir sömu gögnin er lengsta tímabilið notað. Einnig innihalda sumar töflur síur sem þú getur ekki breytt eða fjarlægt. Til að hjálpa til við að auðkenna þessar síur birtast þær í ljósari lit.

#### Vídeó leiðsögn

Þetta myndband gefur dæmi um hvernig á að setja upp varðveislustefnu.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## Notaðu varðveislustefnur

Hægt er að nota verkraðarfærslu til að setja á varðveislureglur til að eyða gögnum sjálfkrafa eða setja reglur á handvirkt.

Til að nota varðveislureglu sjálfkrafa skal bara stofna og virkja reglu. Þegar þú virkjar stefnu,, [!INCLUDE [prod_short](includes/prod_short.md)] býr til færslu í vinnuröð sem beitir henni í samræmi við varðveislutíma hennar. Allar varðveislureglur munu nota sömu verkraðarfærsluna. Sjálfgefið er að verkraðarfærslan beiti reglunni á hverjum degi kl. 02:00. Hægt er að breyta sjálfgildinu en ef það er gert mælum við með því að það keyri utan vinnutíma. Til að fá frekari upplýsingar skaltu fara á [Nota vinnuraðir til að skipuleggja verkefni](admin-job-queues-schedule-tasks.md). 

Hægt er að setj á reglu handvirkt með því að nota aðgerðina **Nota handvirkt** á síðunni **Varðveislureglur**. Ef ætlunin er að nota alltaf reglu handvirkt skal kveikja á **Handvirkt**. Verkraðarfærslan hunsar þá regluna þegar hún er keyrð.

## Skoðaðu varðveislustefnuskrárfærslur

Hægt er að skoða verkþætti sem tengjast varðveislureglum á síðunni **Varðveislureglukladdi**. Til dæmis eru færslur búnar til þegar reglu er beitt eða ef villur komu upp.

## Taktu viðbótina þína inn í varðveislustefnu (þarfnast hjálp frá þróunaraðila)

Sjálfgefið er að varðveislureglur ná aðeins til [!INCLUDE[prod_short](includes/prod_short.md)] á listanum sem við bjóðum upp á. Hægt er að fjarlægja sjálfgefnar töflur úr listanum og hægt er að bæta við eigin töflum. Það er, þú getur ekki bætt við töflu sem þú bjóst ekki til sjálfur. Til dæmis geturðu ekki bætt við öðrum borðum frá [!INCLUDE[prod_short](includes/prod_short.md)] eða úr viðbót sem þú hefur keypt.

Til að bæta töflunum þínum við listann yfir leyfilegar töflur verður verktaki að bæta við einhverjum kóða. Til dæmis til uppsetningarkóðaeiningarinnar fyrir viðbótina (kóðaeining með *install* undirgerðinni).

Þegar þróunaraðili bætir við töflu getur hann tilgreint áskildar og sjálfgefnar síur. Ekki er hægt að fjarlægja eða breyta lögboðnum síum síðar þegar þú bætir við töflum til að skilgreina varðveislustefnu. Sjálfgefnar síur eru bara tillögur.

Eftirfarandi eru dæmi um hvernig á að bæta töflu við lista yfir leyfðar töflur með og án áskildra og sjálfgefinna sía. Fyrir flóknara dæmi, farðu í kóðaeiningu 3999 "Reten. Pol. Setja upp - BaseApp“.

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