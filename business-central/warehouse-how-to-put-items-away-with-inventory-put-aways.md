---
title: Hvernig á að ganga frá vörum með birgðafrágangi
description: Lærðu að nota birgðafrágangsskjöl til að skrá og bóka frágangs-og móttökuupplýsingar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/19/2023
ms.custom: bap-template
ms.search.forms: '7375,'
---
# Ganga frá vörum með birgðafrágangi

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru vörur afhentar og þær síðan notaðar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast kvittana|Krefjandi frágangur|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: pöntun-eftir pöntun.|  
|U|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Frekari upplýsingar um vöruflæði á  [innleið](design-details-inbound-warehouse-flow.md).

Í þessari grein er átt við aðferð B í töflunni.

Þegar birgðageymslan er sett upp þannig að þörf sé á frágangsvinnslu en ekki vinnslu skal nota  **birgðafrágangsskjal**  til að skrá og bóka frágangs-og móttökuupplýsingar fyrir upprunaskjölin. Upprunaskjöl á innleið geta verið innkaupapantanir, söluvöruskilapantanir og flutningspantanir á innleið.

> [!NOTE]
> Framleiðsla og samsetningarframleiðsla standa einnig fyrir upprunaskjöl á innleið. Frekari upplýsingar um meðhöndlun framleiðslu og samsetningu samsetningar fyrir innri vinnslur í  [Hönnunarupplýsingum: innra vöruhús flæðir](design-details-internal-warehouse-flows.md).

Þú getur búið til birgðafrágang á þrjá vegu:  

* Frágangurinn er stofnaður í upprunaskjalinu sjálfu.  
* Stofnið birgðafrágang fyrir nokkur upprunaskjöl á sama tíma með því að nota runuvinnslu.  
* Stofna frágang í tveimur skrefum með því að gefa fyrst út upprunaskjal til að ganga frá þeim atriðum sem hægt er að ganga frá. Hægt er að stofna birgðafráganginn út frá upprunaskjalinu með því að  **nota síðuna birgðafrágangssíða** .  

## Birgðafrágangur stofnaður úr upprunaskjali:

1. Í upprunaskjalinu, sem getur verið innkaupapöntun, Söluvöruskilapöntun eða flutningspöntun á innleið, skal velja  **aðgerðina stofna birgðafrágang/tínslu** .  
2.  **Veljið stofna Ívt.** Gátgluggi frágangs.
3. Velja hnappinn **Í lagi**. Nýr birgðafrágangur er stofnaður.

## Fleiri en ein birgðafrágangur stofnuð með keyrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **stofna birgðafrágang/tínslu/hreyfingar** og velja síðan tengda tengilinn. 
2.  **Á flipanum vöruhúsabeiðni**, Notið  **upprunaskjalið**  og  **upprunnr.** svæði til að sía á ákveðnar gerðir skjala eða sviða af fylgiskjalsnúmerum. Til dæmis er hægt að stofna frágang aðeins fyrir innkaupapantanir.
3.  **Á flipanum Valkostir**  er gátreiturinn Stofna ívt valinn  **.** Gátgluggi frágangs.
4. Velja hnappinn **Í lagi**. Tiltekinn birgðafrágangar eru stofnaðar.

## Að útbúa fráganginn í tveimur skrefum

### Til að biðja um birgðafrágang með því að gefa út upprunaskjalið

Þegar verið er að gefa út innkaupapantanir, söluvöruskilapantanir og flutningspantanir á innleið verða vörurnar á pantanunum tiltækar til frágangs. Eftirfarandi skref lýsa því hvernig á að gera vörurnar í innkaupapöntun tilbúnar til frágangs.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.
2. Valin er innkaupapöntun sem á að gefa út og velja síðan aðgerðina **Gefa út**.  

### Birgðafrágangur stofnaður á grundvelli upprunaskjals:

Starfsmaður í vöruhúsi getur stofnað nýjan frágang í frágangi á grundvelli útgefins upprunaskjals.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðafrágangur** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Í reitnum **Upprunaskjal** er valin sú tegund upprunaskjalsins sem verið er að ganga frá fyrir.  
4. Í reitnum **Forðanr.** er forðaskjal valið.  
5. Að öðrum kosti, skal velja **Sækja upprunaskjal** aðgerðina til að velja fylgiskjal úr lista yfir upprunaskjöl á innleið sem eru tilbúin til frágangs í birgðageymslu.  
6. Velja hnappinn **Í lagi** til að fylla út frágangslínur í samræmi við valið upprunaskjal.  

## Skrá Birgðafráganginn

1.  **Á síðunni Birgðafrágangur**  er opnaður áður stofnaða frágangsskjal.  
2.  **Í reitnum Hólfkóti**  í frágangslínunum eru hólfin þar sem vörurnar verða að vera lagðar til samkvæmt sjálfgefnu hólfi varanna. Hægt er að skipta um hólf ef með þarf.  
3. Framkvæmið fráganginn og Færið inn raunverulegt magn sem gengið var frá í  **reitinn Magn til afgreiðslu** .

    Ef setja þarf vörur einnar línu í fleiri en eitt hólf, til dæmis þar sem merkt er við fullt, er aðgerðin Skipta Línuaðgerð  **á**  fastflipanum línur  **notaðar** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.  
4. Eftir að vörurnar hafa verið settar í gang skal velja  **aðgerðina Bóka** .  

    * Bóka móttöku upprunaskjalslínurnar sem gengið hefur verið frá
    * Ef birgðageymslan notar hólf mun bókun einnig stofna vöruhúsafærslur til að bóka breytingar á magni hólfs.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Sjá einnig .

[Warehouse Management Overview](design-details-warehouse-management.md)
[Inventory](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
