---
title: Sameina vörur
description: Fræðast um samsetningu eftir pöntunum og samsetningu birgðaferla í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# Sameina vörur

Ef reiturinn **Áfyllingarkerfið** á birgðaspjaldinu inniheldur **samsetningu** er sjálfgefin aðferð við að útvega vöruna til að setja hana saman í samræmi við samsetningaruppskrift og hugsanlega af tilteknum forða. Nánari upplýsingar um [vinnu í samsetningaruppskriftum](assembly-how-work-assembly-boms.md). Nánari upplýsingar um hvernig samsetningarvara er sett upp í Skilningur settur [saman í pöntun og settur saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

Hægt er að setja upp samsetningarvörur fyrir tvær samsetningarvinnslur.

|Ferli  |Heimildasamstæða  |
|---------|---------|
|Setja saman á lager     | Vörur sem settar eru saman og settar saman í framtíðarsölu. Til dæmis pössum fyrir komandi söluherferð. Vörurnar tengjast ekki sölupöntun, að minnsta kosti ekki ennþá. Þessar vörur eru yfirleitt ekki sérsniðnar fyrir beiðnir viðskiptamanna.        |
|Setja saman í pöntun     | Vörur sem ekki á að setja á lager. Til dæmis vegna þess að þær eru sérsniðnar á grundvelli pantana viðskiptamanna eða til að draga úr kostnaði við lagerbirgðir. |
  
Þessi grein lýsir stöðluðum stillingum fyrir samsetningu lagerbirgða. Það gætu verið aðrar leiðir sem henta fyrirtækinu betur. Nánari upplýsingar um [selja birgðir í flæði](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) samsetningar í pöntun og [selja samsetningarvörur og vörur í birgðum saman](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Samsetningaríhlutir eru meðhöndlaðir á sérstakan hátt í grunnskilgreiningum vöruhúss. Fræðast meira um [samsetningarvörur í pöntun með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## Til að setja vöru saman á lager

Fylgja skal skrefunum í þessu ferli til að setja vöru saman í birgðir. Til að fræðast um samsetningu pöntunar er farið í [Selja vörur sem settar eru saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Samsetningarpantanir** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð. Síðan **Ný samsetningarpöntun** opnast.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í reitnum Vörunr **.** er valin varan sem á að setja saman. Hægt er að velja vörur sem eru settar upp fyrir samsetningar og hafa samsetningaruppskrift eða vörur án samsetningaruppskrifta. Hið síðarnefnda er gagnlegt fyrir óáætlaðar samsetningar eða aðstæður þegar nota á endurflokkunar- og rakningarkostnað vöru.  
5. Í reitnum **Magn** er fært inn hversu margar einingar vörunnar setja á saman.  

    > [!NOTE]  
    >  Ef einn eða fleiri íhlutir eru ekki tiltækir til að uppfylla magn á skiladegi **opnast síðan Samsetning til ráðstöfunar** . Síðan sýnir hversu margar samsetningarvörur er hægt að setja saman út frá ráðstöfunarmagni íhluta. Nánari upplýsingar um [tiltækar vörur](inventory-how-availability-overview.md) eru skoðaðar. Þegar síðunni er lokað er samsetningarpöntunin stofnuð með til ráðstöfunarviðvaranir í línunum fyrir viðkomandi íhluti.  

    Í línunum er innihald samsetningaruppskriftarinnar og það magn sem tiltekið er.  

    > [!NOTE]  
    >   **Ef síðan Samsetning til ráðstöfunar** opnast þegar samsetningarpöntunarhausinn var fylltur út er **Já í hverri samsetningarpöntunarlínu sem hefur áhrif á Já** í reitnum **Til ráðstöfunar. Viðvörunarreitur** með tengil á nákvæmar ráðstöfunarupplýsingar. <!--check whether this field help is useful For more information, see Check Availability.--> Hægt er að leysa úthreyfingu á íhlutum til ráðstöfunar með því að:

    > * Upphafsdagsetningu frestað.
    > * Skipt um íhlut með annarri vöru.
    > * Tiltæk staðgengill valinn ef hún er skilgreind.  

6. Í reitinn **Magn til samsetningar** er fært inn hversu margar einingar af samsetningarvörunni á að bóka sem frálag næst þegar samsetningarpöntunin er bókuð. Þetta magn getur verið lægra en gildið í svæðinu **Magn** til að spegla hlutafrálagsbókun.  

    > [!NOTE]  
    >  Til að tryggja að bókun íhlutanotkunar passi við frálagsbókun samsetningarvörunnar eru magnreitirnir í samsetningarpöntunarlínunum sjálfkrafa lagaðir að gildinu sem fært er inn í reitinn **Magn til að setja saman**.  
7. Á samsetningarpöntunarlínum af gerðinni **Vara** eða **Forði**, í reitnum **Magn til notkunar**, tilgreinið hversu margar einingar á að bóka sem notað, næst þegar samsetningarpöntun er bókuð.
8. Þegar komið er að því að bóka að hluta eða í heild er valin aðgerðin **Bóka**.  

    > [!NOTE]  
    >  Ef viðvaranir eru enn til staðar í samsetningarpöntunarlínunum er ekki hægt að bóka pöntunina. Skilaboð sýna íhlutina eða íhlutina sem eru ekki í birgðum.  

Eftir að bókun tekst, er samsetningarvaran bókuð sem frálag birgðageymslukótans og hugsanlegs hólfakóta sem eru skilgreindir í samsetningarpöntuninni. Fyrir samsetningarpantanir sem voru stofnaðar handvirkt er hægt að afrita staðsetninguna úr uppsetningarreitnum **Sjálfgefin staðsetning fyrir pantanir**. Fyrir sameiningarpöntunarflæði, er hægt að afrita kóta birgðageymslu úr sölupöntunarlínunni.  

## Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
