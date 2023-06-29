---
title: Sameina vörur
description: Læri um saman-til-röð og setja saman verkferla í viðskiptum miðsvæðis.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="assemble-items"></a><a name="assemble-items"></a>Sameina vörur

 **Ef reiturinn Áfyllingarkerfi**  á birgðaspjaldinu inniheldur  **samsetningu** er sjálfgefna aðferðin við að útvega vöruna að setja hana saman samkvæmt samsetningaruppskrift og hugsanlega með tilteknum forða. Frekari upplýsingar í  [vinnu með uppskriftum samsetningar](assembly-how-work-assembly-boms.md). Frekari upplýsingar um uppsetningu samsetningarvöru í  [skilningi setja saman við pöntun og setja saman við birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

Hægt er að setja upp samsetningarvörur fyrir tvö samsetningarferli.

|Ferli  |Description  |
|---------|---------|
|Setja saman á lager     | Hlutir sem þú hefur safnað saman og lager fyrir síðari sölu. T.d. pökkum fyrir komandi söluherferð. Vörurnar eru ekki tengdar sölupöntun, a.m.k. ekki enn sem komið er. Yfirleitt eru þessi atriði ekki sérsniðin að beiðnum viðskiptavina.        |
|Setja saman til að panta     | Vörur sem þú vilt ekki eiga á lager. Til dæmis, þar sem þeir eru sérsniðnir eftir pöntunum viðskiptavina eða til að minnka kostnað á lagerbirgðum. |
  
Í þessari grein er lýst stöðluðum stillingum til að setja saman við birgðir. Það gætu verið aðrar leiðir sem henta þínu fyrirtæki. Lærðu meira á að  [selja birgðavörur í saman-til-Pöntunarstreymi](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)  og  [selja samsettar vörur og birgðavörur saman](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Samsetningaríhlutir eru meðhöndlaðir á sérstakan hátt í grunnskilgreiningum vöruhúss. Frekari upplýsingar á  [afgreiðslunum setja saman við vörur með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## <a name="to-assemble-an-item-to-stock"></a><a name="to-assemble-an-item-to-stock"></a>Vara sett saman til Hlutabréfakaup

Fylgið leiðbeiningum í þessu ferli til að setja vöru á lager. Til að fræðast um að setja saman til að panta er farið í að  [selja vörur saman til að panta](assembly-how-to-sell-items-assembled-to-order.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Samsetningarpantanir** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð. Síðan **Ný samsetningarpöntun** opnast.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í reitnum  **Vörunr.**  skal velja þá vöru sem setja á saman. Hægt er að velja vörur sem settar eru upp fyrir samsetningu og hafa samsetningaruppskrift, eða vörur án samsetningaruppskriftar. Hið síðara er gagnlegt fyrir óáætlaðar samsetningar eða aðstæður þegar nota á endurflokkun og rekja kostnað.  
5. Í reitnum **Magn** er fært inn hversu margar einingar vörunnar setja á saman.  

    > [!NOTE]  
    >  Ef einn eða fleiri þættir eru ekki tiltækir til að uppfylla magn á gjalddaga  **opnast síðan ráðstöfunarsíða**  samsetningar. Síðan sýnir hversu mörg samsetningaratriði er hægt að setja saman út frá þáttframboðum. Lærðu meira á  [Skoða framboð vara](inventory-how-availability-overview.md). Þegar síðunni er lokað er samsetningarröðin stofnuð með ráðstöfunarviðvörunum í línunum fyrir viðkomandi íhluti.  

    Línurnar innihalda efni samsetningaruppskriftarinnar og tilgreinda magnið.  

    > [!NOTE]  
    >   **Ef síðan Samsetningarráðstöfunarsíða**  opnast þegar fyllt er í haus samsetningarpöntunar, inniheldur  **hver lína samsetningarlínu er Já**  í reitnum  **gagn. Viðvörunarsvæði**  með hlekk á ítarlegar ráðstöfunarupplýsingar. <!--check whether this field help is useful For more information, see Check Availability.--> Hægt er að leysa úr íhlutandi úthreyfingu með því að:

    > * Upphafsdagsetningin frestað.
    > * Skipta út íhlut með annarri vöru.
    > * Val á tiltækan staðgengilsheiti ef hún er skilgreind.  

6.  **Í svæðinu Magn til að setja saman**  við skal slá inn hversu margar einingar samsetningarvörunnar á að bóka sem úttak næst þegar samsetningarpöntunin er bókuð. Þetta magn getur verið lægra en gildið í svæðinu **Magn** til að spegla hlutafrálagsbókun.  

    > [!NOTE]  
    >  Til að tryggja að bókun íhlutanotkunar passi við frálagsbókun samsetningarvörunnar eru magnreitirnir í samsetningarpöntunarlínunum sjálfkrafa lagaðir að gildinu sem fært er inn í reitinn **Magn til að setja saman**.  
7. Á samsetningarpöntunarlínum af gerðinni **Vara** eða **Forði**, í reitnum **Magn til notkunar**, tilgreinið hversu margar einingar á að bóka sem notað, næst þegar samsetningarpöntun er bókuð.
8. Þegar komið er að því að bóka að hluta eða í heild er valin aðgerðin **Bóka**.  

    > [!NOTE]  
    >  Ef viðvaranir eru enn til staðar í samsetningarpöntunarlínunum er ekki hægt að bóka pöntunina. Boð birtast um íhlut eða íhluti sem ekki eru í birgðum.  

Eftir að bókun tekst, er samsetningarvaran bókuð sem frálag birgðageymslukótans og hugsanlegs hólfakóta sem eru skilgreindir í samsetningarpöntuninni. Fyrir samsetningarpantanir sem voru stofnaðar handvirkt er hægt að afrita staðsetninguna úr uppsetningarreitnum **Sjálfgefin staðsetning fyrir pantanir**. Fyrir sameiningarpöntunarflæði, er hægt að afrita kóta birgðageymslu úr sölupöntunarlínunni.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
