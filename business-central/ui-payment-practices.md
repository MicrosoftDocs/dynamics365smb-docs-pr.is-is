---
title: Skýrsla um greiðsluaðferðir
description: Læra auðveldlega að búa til skýrslu um greiðsluaðferðir fyrir lánardrottna og viðskiptamenn.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment, practices, vendor, customer, report'
ms.search.form: '686, 687, 689'
ms.date: 04/23/2024
ms.author: altotovi
--- 

# <a name="payment-practices-report"></a>Skýrsla um greiðsluaðferðir

Sum lönd/svæði krefjast þess að fyrirtæki tilkynni greiðslutíma fyrir lánardrottna sína eins og þau eru skilgreind af bæjaryfirvöldum. Skýrslugerðin getur byggst á mismunandi uppruna og getur raðað lánardrottnum eftir stærð þeirra eða skilgreindum greiðsluskilmálum, sem veitir lánardrottnum skýrslur fyrir eftirfarandi eins og krafist er af bæjaryfirvöldum:  

- Meðaltal umsamins greiðslutímabils.  
- Meðaltal raunverulegs greiðsluskilmála.   
- Hlutfall reikninga sem greiddir eru eftir lok umsamins greiðslutímabils. 

Notendur geta valið tímabilið sem hann á að keyra útreikning á og til að finna upplýsingar byggðar á flokkun sem er valin. Hægt er að finna upprunafærslur fyrir hvern flokkunarflokk. 

> [!NOTE]
> Þessa skýrslugerð er svo langt krafist í sumum löndum, en þetta er altækur eiginleiki og hægt er að nota hana alls staðar. Eins og er þurfa sænsk fyrirtæki með 250 og fleiri starfsmenn að gefa skýrslu til sænskra fyrirtækja skráningarskrifstofu um hvaða greiðslutíma þau hafa fyrir innkaup frá fyrirtækjum sem eru smærri en sjálf. Svipuð athöfn er til í Bretlandi, Ástralíu og Nýja-Sjálandi.  

## <a name="generate-the-report"></a>Mynda skýrsluna

Eftirfarandi skref eru notuð til að keyra skýrsluna **Greiðsluvenjur** :

1. Velja skal eiginleikann ![Lightbulb sem opna Tell Me.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **greiðsluhætti** og velja síðan viðeigandi tengil. 
2. Valið er **Nýtt**.
3. Á flýtiflipanum **Almennt** eru gildi færð inn í eftirfarandi reiti:

   | Svæði | Heimildasamstæða |
   |---------|-----------------------------------|
   | Nr. | Tilgreina númer færslu eða færslu fyrir skýrsluna. |
   | Uppsöfnunargerð | Tilgreina hvernig gögn eru samanlögð. Ef skýrslan Tímabil er valin **verður byggð á mismunandi tímabilum en ef skýrslan Stærð** fyrirtækis er valin **er stofnuð á grundvelli stærða fyrirtækis sem grunnstilltar eru í** reitnum Stærðarkóti **stærðar fyrirtækis á** spjaldinu Lánardrottinn **.**  |
   | Hausagerð | Tilgreinir uppruna færslna í greiðsluferlinu og hægt er að velja Lánardrottnar, Viðskiptamenn eða hvort tveggja. |
   | Upphafsdagur | Tilgreinir upphafsdagsetningu greiðsluháttar. |
   | Lokadagur | Tilgreinir lokadagsetningu greiðsluháttar. |

> [!NOTE]
> Ef ákveðið er að nota valkostinn **Stærð** fyrirtækis þarf fyrst að stofna færslur á síðunni **Stærðir fyrirtækis** og bæta þeim við alla lánardrottna sem á að rekja með þessari aðferð.

4. Þegar allir reitir eru útfylltir í hausnum þarf að keyra aðgerðina **Búa til að mynda** gögn í línum og tölum fyrir valda gerð skýrslugerðar.
5. Á grundvelli tegundar **ágústmánaðar** fást mismunandi línur. Hægt er að breyta sumum gildum handvirkt, en í þessu tilviki verður hver lína og öll skýrslan merkt sem **breytt handvirkt**.
6. Í öllum reiknuðum reitum er hægt að fara dýpra til að sjá hvernig þessi niðurstaða hefur verið reiknuð og opna **síðuna Gagnalisti** greiðsluvenna.
7. Ef prenta á fylgiskjalið er hægt að gera það með því að keyra aðgerðina **Prenta** .

## <a name="see-also"></a>Sjá einnig .

[Fjárhagsskýrslur](finance-reports.md)  
[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Skýrslur og greiningar viðskiptakrafna](receivables-reports.md)  
[Skýrslur og greiningar viðskiptaskulda](payables-reports.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjármál](finance.md)  
[Yfirlit yfir staðbundna virkni](about-localization.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
