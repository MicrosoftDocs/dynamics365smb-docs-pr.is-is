---
title: Kynning - Útreikningur verks í vinnslu fyrir verk
description: 'Fræðast um hvernig rekja má notkun vinnustunda starfsmanna, vélastundir, birgðavörur og aðrar gerðir notkunar eftir því sem verk er framvinda.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 12/13/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Kynning: Útreikningur verks í vinnslu fyrir verk

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Með verkefninu er hægt að tímasetja notkun á forða fyrirtækisins og fylgjast með ýmsum kostnaði sem tengist notkun forða í tilteknu verkefni. Verkefnið felur í sér notkun á vinnutíma starfsmanna, vélastundir, birgðavörur og aðrar gerðir notkunar sem þarf að rekja sem verkferla. Ef verk er keyrt yfir langt tímabil gæti þurft að flytja þann kostnað yfir á VÍV-reikning verks (VÍV) á efnahagsreikningi á meðan verkinu er lokið. Síðan er hægt að samþykkta kostnað og sölu á rekstrarreikningi þegar það á við.  

## Um kynninguna

 Þessi kynning fjallar um eftirfarandi verk:  

-   Útreikning á VÍV.  
-   Val á VÍV-útreikningsaðferð.  
-   Að undanskildum verkhluta frá VÍV.  
-   Bókun VÍV í fjárhag.  
-   Bakfærslu á VÍV-bókun.  

 Hvert skref í ferlinu reiknar út virðið og færir verkfærslurnar í fjárhaginn. Útreikningur og bókun eru aðskilin svo hægt sé að fara yfir gögn og gera breytingar áður en bókað er í fjárhaginn. Þess vegna þarf að ganga úr skugga um að allar upplýsingar séu réttar eftir að útreikningskeyrslur eru keyrðar og áður en bókunarkeyrslur eru keyrðar.  

## Hlutverk

 Þessi kynning notar Tinnu sem meðlim verkefnateymisins.  

## Frumskilyrði

 Áður en hægt er að framkvæma verk hér í kynningunni þarf að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] í tölvunni.  

## Ferill

 Þessi kynning einblínir á fyrirtækið CRONUS International Ltd., hönnunar- og ráðgjafafyrirtæki sem hannar og setur upp nýja innviði á borð við ráðstefnusali og skrifstofur, með húsgögn, aukahluti og geymslueiningar. Mest af vinnunni CRONUS er verkefnabundin og Tinna, meðlimur verkefnishóps, notar verkefnið til að hafa yfirlit yfir hvert verk sem CRONUS er hafið og einnig verkefnið sem er að ljúka. Sumt af verkefninu getur verið löng og getur keyrt í rúma mánuði. Tinna getur notað VÍV-reikning til að skrá verk í vinnslu og rekja kostnað alls staðar í verkefninu.  

## Útreikningur á VÍV

 CRONUS hefur tekið að sér langt verk sem nær yfir nokkur bókhaldstímabil. Tinna, meðlimur verkefnateymis, reiknar út verk í vinnslu (VÍV) til að ganga úr skugga um að ársreikningur fyrirtækisins sé réttur.  

 Tinna velur tiltekinn hóp verkhluta sem tekin eru með í VÍV-útreikninginn. Á síðunni **Verkhlutalínur** verkefnis getur Tinna tilgreint þessar línur í dálknum **VÍV-samtala** .  

 Eftirfarandi tafla lýsir valkostunum þremur.  

|Svæði|Heimildasamstæða|  
|-------------------------------------|---------------------------------------|  
|**\<blank\>**|Hafðu autt ef verkhlutinn er hluti af hópi verkhluta.|  
|**Samtals**|Skilgreinir svið eða hóp verkhluta sem eru innifaldir í VÍV og samþykkisútreikningi. Innan flokksins eru allir verkhlutar með **verkhlutategund verks** sem stilltir eru á **Bókun** teknir með í VÍV-samtöluna, nema VÍV-samtala **þess** sé stillt á **Undanskilin**.|  
|**Útilokað**|Á aðeins við um verk með **verkhlutategund** verks **·**. Verkið er ekki tekið með þegar VÍV og samþykki eru reiknuð.|  

 Í eftirfarandi kynningu notar Tinna kostnaðarvirðisaðferðina, staðal fyrirtækis þeirra, til að reikna VÍV. Tinna tilgreinir þann hluta verksins sem á að taka með í VÍV-útreikninginn með því að úthluta VÍV-samtölugildum til ýmissa verkhlutalína.  

### Útreikningur VÍV  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja svo viðeigandi tengil.  
2. Á listanum **Verkefni** skal velja **Deerfield-verkefnið** og velja svo aðgerðina **Breyta** . Þá opnast Verkefnaspjaldið í breytingastillingu.  

     Hægt er að reikna VÍV eftir Kostnaðarvirði, Söluvirði, Sölukostnaði, Prósentum lokið eða Samningi lokið. Í þessu dæmi, notar CRONUS aðferðina kostnaðarvirði.  

3. Á flýtiflipanum **Bókun** í reitnum **VÍV-aðferð** og síðan valið **Kostnaðarvirði**.  
4. Veljið aðgerðina **Verkhlutalínur** verks og stillið eftirfarandi gildi í reitnum **VÍV-samtala** .  

     Eftirfarandi tafla lýsir gildunum.  

    |Nr. verkhluta verkefnis|VÍV-samtala|  
    |------------------|----------------------|  
    |1130|Útilokað|  
    |1190|Samtala|  
    |1210|Útilokað|  
    |1310|Útilokað|  

5. Veljið aðgerðina **VÍV** og svo aðgerðina **Reikna VÍV**.  
6. Á síðunni **Verk - Reikna VÍV** er valið verk til að reikna VÍV fyrir. Á flýtiflipanum **Verkefni** er Deerfield **valið** í reitnum **Nr.** .  
7. Í reitnum **Bókunardags.** færið inn dagsetningu sem er síðar en vinnudagsetningu.
8. Fært er inn **1** í reitinn **Númer fylgiskjals**. Þetta stofnar skjal sem síðar er hægt að vísa í fyrir rekjanleika.  
9. Veldu hnappinn **Í lagi** til að ræsa keyrsluna. Skilaboð birtast. Velja hnappinn **Í lagi** til að halda áfram. Síðunni Verkhlutalínur **verkefnis** er lokað.  

    > [!NOTE]  
    >  Skilaboðin tilgreina að um viðvaranir sé að ræða sem tengjast VÍV-útreikningnum. Fara þarf yfir viðvaranirnar í næsta ferli.  

10. Á síðunni **Verkspjald** er flýtiflipinn **VÍV og Samþykki** stækkaður til að sjá útreiknuð gildi. Einnig er hægt að sjá **Bókunardagsetning VÍV** og gildin sem hafa verið bókuð í fjárhag, ef einhver eru.  

 Athugið að gildið fyrir **Samþ. kostnaðarupphæð** er 215.60 í dálknum **Til að bóka**. Þetta endurspeglar heildarkostnað tveggja varanna í flokki verkhluta 1110 – 1130. Þriðja varan var stillt á **Undanskilin** og er því ekki tekin með í VÍV-útreikningi.  

### Til að fara yfir viðvaranir VÍV  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **VÍV-stjórnklefa** verkefnis og velja síðan viðeigandi tengil.  
2.   **Velja skal Deerfield-verkefnið** og velja svo aðgerðina **Sýna viðvaranir** .  
3.  Á síðunni **VÍV-viðvaranir verks** skal fara yfir viðvörunina sem tengist verkefninu.  

 Eftir bókhaldstímabilið þarf Tinna að endurreikna VÍV til að taka með þá vinnu sem unnin hefur verið.  

### VÍV endurreiknað  

1. Á síðunni **Verkspjald** skal velja aðgerðina **VÍV-færslur** til að skoða VÍV-útreikninginn.  

     Síðan **VÍV-færslur verks** sýnir VÍV-færslurnar sem síðast voru reiknaðar í verki, jafnvel þótt VÍV hafi ekki enn verið bókað í fjárhag.  

2. Hægt er að fylgja skrefunum í leiðbeiningunum sem útskýrir hvernig reikna á VÍV til að endurreikna VÍV. Í hvert sinn sem VÍV er reiknað er færsla stofnuð á síðunni **VÍV-færslur verks** .  
3. Loka síðunni.  

> [!NOTE]  
> VÍV og samþykki eru reiknuð en eru ekki bókuð í fjárhag. Til að gera það verður að keyra **keyrsluna Bóka VÍV í fjárhag** eftir að VÍV og samþykki hafa verið reiknuð.

## Bókun VÍV í fjárhag

 Nú þegar Tinna hefur reiknað VÍV fyrir þetta verkefni geta þeir bókað það í fjárhaginn.  

### VÍV bókað í fjárhag  

1. Af listanum **Verkefni** er Deerfield-verkefnið **valið**.  
2. Veljið aðgerðina **VÍV** og svo aðgerðina **Bóka VÍV í fjárhag**.  
3. Á síðunni **Verk - Bóka VÍV í fjárhag** á flýtiflipanum **Verkefni** er Deerfield **valið** í reitnum **Nr.** .  
4. Á flýtiflipanum **Valkostir** í reitnum **Fylgiskjalsnr. bakfærslu** er **1** fært inn.  
5. Velja hnappinn **Í lagi** til að bóka VÍV í fjárhag.  
6. Velja hnappinn **Í lagi** til að loka staðfestingarsíðunni.  

     Eftir að gengið hefur verið frá bókun er hægt að skoða upplýsingar um bókun á síðunni **Fjárhagsfærslur VÍV**.  

7.  Á listanum Projets **skal velja** Deerfield-verkefnið **og velja svo VÍV-fjárhagsfærslur aðgerðina**  **.**   

     Á síðunni **VÍV-fjárhagsfærslur verks** er gengið úr skugga um að VÍV hafi verið bókað í fjárhag.  

8. Loka síðunni.  
9. Opna síðuna **Verkspjald** fyrir **Deerfield-verkefnið** .  
10. Á flýtiflipanum **VÍV og samþykki** skal athuga að í dálkinum **Bókað** er reiturinn **Samþ. fjárhagsupph. kostnaðar** nú útfylltur, sem þýðir að það tókst að bóka VÍV í fjárhag.  
11. Velja hnappinn **Í lagi** til að loka spjaldinu.  

## Bakfærsla VÍV-bókunar

 Tinna ákveður að verkhlutarnir sem voru undanskildir útreikningi VÍV hefðu átt að reiknast í VÍV. Tinna getur bakfært rangar bókanir án þess að bóka nýjar VÍV-bókanir.  

### Bakfærsla VÍV-bókunar  

1. Af listanum **Verkefni** er Deerfield-verkefnið **valið**.  
2. Veljið aðgerðina **VÍV** og svo aðgerðina **Bóka VÍV í fjárhag**.  
3. Á síðunni **Verkbóka VÍV í fjárhag** á flýtiflipanum **Verkefni** skal velja **Deerfield** í reitnum **Nr.** .  
4. Á flýtiflipanum **Valkostir** í reitnum **Fylgiskjalsnr. bakfærslu** er **1** fært inn.  
5. Í reitnum **Bókunardags. bakfærslu** er færð inn upprunaleg bókunardagsetningu. Það ætti að vera sama dagsetning og notuð var til að reikna VÍV í fyrsta sinn.  
6. Gátreiturinn **Eingöngu** bakfæra er valinn. Þetta bakfærir áður bókað VÍV, en bókar ekki nýtt VÍV í fjárhag.  
7. Velja hnappinn **Í lagi** til að keyra runuvinnsluna og velja svo **Í lagi** til að loka staðfestingarsíðunni.  
8. Opna síðuna **Verkspjald** fyrir **Deerfield**.  
9. Á flýtiflipanum **VÍV og samþykki** skal staðfesta að engar bókaðar VÍV-færslur séu til staðar.  
10. Loka þessari síðu.  
11. Á listanum **Verkefni** skal velja **Deerfield-verkefnið**, velja **VÍV** aðgerðina og velja svo aðgerðina **VÍV-fjárhagsfærslur** . VÍV-færslur hafa gátreitinn **Bakfært** valið.  
12. Loka þessari síðu.  
13. Opna verkhlutalínur **verkefnisins**, taka með þá hluta verksins sem á að vera í VÍV-útreikningi og endurreikna og bóka nýja gildið í fjárhaginn.  

    > [!NOTE]  
    >  Segjum svo að Tinna hafi reiknað og bókað VÍV fyrir verkefni með röngum dagsetningum. Eftir aðferðina sem rædd var áður getur Trausti bakfært rangar bókanir, leiðrétt dagsetningarnar og endurbókað í fjárhaginn.  

## Næstu skref

 Í þessari kynningu var farið yfir skrefin í útreikningi á VÍV í [!INCLUDE[prod_short](includes/prod_short.md)]. Í stærri verkefnum getur verið gagnlegt að flytja kostnaðinn í VÍV-reikning með reglulegu millibili á meðan verkefninu er lokið. Í kynningunni var sýnt hvernig á að undanskilja verkhlutalínur frá útreikningi. Sýnir einnig hvenær þörf er á endurreikningi. Og að lokum, þessi kynning sýnir hvernig á að bóka VÍV í fjárhag. Dæmi um bakfærslu VÍV-bókunar í fjárhag er einnig tekin með.  

## Sjá einnig .

 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Kynning: Stjórnun verkefna](walkthrough-managing-projects-with-jobs.md)  
 [Að skilja VÍV-aðferðir](projects-understanding-wip.md)  
 [Fylgst með framvindu og afköstum](projects-how-monitor-progress-performance.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
