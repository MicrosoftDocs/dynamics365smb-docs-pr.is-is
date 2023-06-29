---
title: Yfirlit vöruhúsaferli á útleið
description: Þessi grein lýsir verkflæði út-vöruhúss á útleið.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes"></a><a name="outbound-warehouse-processes"></a>Ferli vöruhúss á útleið

Ferlar á útleið í vöruhúsum byrja þegar upprunaskjal er losað til að taka vörur úr vöruhúsastað. Til dæmis annað hvort að senda vörurnar einhversstaðar eða til að flytja þær í aðra staðsetningu fyrirtækisins. Í grundvallaratriðum samanstendur ferlið út frá pöntunum á tveimur verkþáttum:

* Tínsla vörur úr hillum.
* Sendingu vara út úr vöruhúsinu.

Upprunaskjöl fyrir flæði á útleið eru:  

* Sölupöntun  
* Flutningspantanir á útleið.  
* Vöruskilapöntun innkaupa  
* Þjónustupöntun  

> [!NOTE]
> Framleiðslu-og samsetningarpantanir með íhlutaþarfir tákna einnig upprunaskjöl á útleið. Framleiðslu-og samsetningarskipanir eru svolítið ólíkar því þær eru gjarnan innri ferlar sem ekki flækja skipurit. Þess í stað eru þeir notaðir við frágang á framleiddum vörum eða flutt þá íhluti sem þarf til að setja vöru upp í samsetningarsvæði. Frekari upplýsingar um þessi ferli í  [Hönnunarupplýsingum: innanhúss-vöruhús flæða](design-details-internal-warehouse-flows.md).  

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru tínsla og sendingarvara notuð með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínslu og sendingu úr pöntunarlínu|||Engin sérstök vöruhúsaaðgerð.|  
|B|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: pöntun-eftir pöntun.|  
|N|Bóka tínslu og sendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bókið tínsluna úr vöruhúsatínsluskjali og bókið sendinguna úr afhendingarskjali vöruhúss|Kveikt|Kveikt|Ítarlegt|  

Nálgunin sem velja á veltur á vöruhúsastarfsháttum og stigi skipulags. Eftirfarandi eru nokkur dæmi sem gætu hjálpað við að ákveða.

* Í pöntunar-og söluumhverfi með einföldum ferlum og einfaldri hólfaskipan er aðferðin A, tiltekt og sendingu úr pöntunarlínunni rétt.
* Ef vörur fyrir pöntunarlínu koma úr fleiri en einu hólfi eða ef vöruhúsastarfsmenn geta ekki unnið með pöntunarskjölum er notkun sérstakra tínsluskjala viðeigandi, aðferð B.
* Ef tiltektar-og sendingarferlar fela í sér margar pantanir og krefjast meiri eftirlits og yfirlits er hugsanlegt að nota vöruhúsaafhendingarskjal og vöruhúsatínsluskjal til að aðskilja tiltektar-og Sendingarverk, aðferðir C og D.  

Í aðferðum A, B og C, eru tiltektar-og sendingarverkþættir sameinaðir í eitt þrep þegar skjal er bókað sem afhent. Í aðferð D skráir þú fyrst tínsluna og bókar síðan sendinguna seinna úr öðru skjali.

> [!NOTE]
> Meðan vörugeymslur og Birgðatínsla hljóma svipað eru þau ólík skjölum og eru notuð í mismunandi ferlum.
> * Birgðatínslan sem notuð er í Aðferðarb, ásamt því að skrá tiltektarupplýsingar, bókar einnig afhendingu á súece-skjalinu.
> * Vöruhúsatínslan sem notuð er í aðferðard er ekki hægt að bóka og aðeins skráir tínsluna. Skráningin gerir vörurnar tiltækar fyrir vöruhúsaafhendinguna en bókar ekki sendinguna. Vöruhúsatínslu krefst vöruhúsaafhendingar í útstreymissengi.

## <a name="no-dedicated-warehouse-activity"></a><a name="no-dedicated-warehouse-activity"></a>Engin sérhæfð vöruhúsastarfsemi

Eftirfarandi greinar veita upplýsingar um hvernig á að vinna innhreyfingar fyrir upprunaskjöl ef ekki er búið að tileinka sér vöruhúsaaðgerðir.

* [Selja vöru](sales-how-sell-products.md)
* [Flutningspöntunum](inventory-how-transfer-between-locations.md)
* [Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md)
* [Stofna þjónustupantanir](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations"></a><a name="basic-warehouse-configurations"></a>Afbrigði grunnvöruhúsa

Eftirfarandi skýringarmynd sýnir ferla á útleið í vöruhúsi fyrir mismunandi gerðir skjala í grunnvöruhúsafbrigðum. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Sýnir þrep í grunnstreymi út í vöruhús.":::

### <a name="1-release-a-source-document"></a><a name="1-release-a-source-document"></a>1: gefa út upprunaskjal

Þegar úttektaraðgerðin  **er notuð**  á upprunaskjali, til dæmis sölu-eða flutningspöntun, eru vörurnar á skjalinu tilbúnar til flutnings í vöruhúsinu. Til dæmis tekið til og sett í hólfið sem tilgreint er á skjalinu. Einnig er hægt að stofna birgðatínsluskjöl fyrir einstakar línur á pöntunum, á þrýstihátt, samkvæmt tilgreindum hólfum og magni sem á að afgreiða.  

### <a name="2-create-an-inventory-pick"></a><a name="2-create-an-inventory-pick"></a>2: stofna birgðatínslu

 **Á síðunni Birgðatínsla**  sækir starfsmaðurinn vöruhúsastarfsmanninn, í draga tísku, í upprunaskjalslínurnar. Að öðrum kosti er birgðatínslulínur þegar stofnaðar, með ýtingu, af notanda sem er ábyrgur fyrir upprunaskjalinu.  

### <a name="3-post-an-inventory-pick"></a><a name="3-post-an-inventory-pick"></a>3: bóka birgðatínslu

Í  **hverri línu fyrir vörur sem hafa verið tíndar eða færðar, að hluta til eða fullu, er reiturinn Magn**  fylltur út og síðan er birgðatínslan bókuð. Upprunaskjöl sem tengjast  birgðatínslu eru bókuð sem afgreitt eða notað.  

Fyrir birgðatínslu eru neikvæðar birgðabókarfærslur stofnaðar, vöruhúsafærslur stofnaðar og tínslubeiðni eytt, ef meðhöndluð að fullu. Til dæmis reiturinn **Magn afgreitt** á upprunaskjalinu á útleið er uppfærður. Bókað afhendingarskjal er stofnað til að til dæmis endurspegla sölupöntunina og afhentar vörur.  

## <a name="advanced-warehouse-configurations"></a><a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi

Eftirfarandi skýringarmynd sýnir ferla á útleið í vöruhúsi fyrir mismunandi gerðir skjala í ítarlegum vöruhúsafbrigðum. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Sýnir skrefin í ítarlegu vöruflæði á útleið.":::

### <a name="1-release-a-source-document-1"></a><a name="1-release-a-source-document-1"></a>1: gefa út upprunaskjal

Gefa út upprunaskjal í ítarlegum skilgreiningum gildir það sama og um grunnskilgreiningar. Vörurnar verða fáanlegar til afgreiðslu í vöruhúsinu. Þær geta til dæmis verið innifaldar í sendingu.  

### <a name="2-create-a-warehouse-shipment"></a><a name="2-create-a-warehouse-shipment"></a>2: vöruhúsaafhending stofnuð

 **Á síðunni vöruhúsaafhending**  fást línurnar úr útgefnu upprunaskjali. Hægt er að sameina línur úr nokkrum upprunaskjali í eina vöruhúsaafhendingu.  

### <a name="3-create-a-warehouse-pick"></a><a name="3-create-a-warehouse-pick"></a>3: Vöruhúsatínsla stofnuð

 **Á síðunni vöruhúsaafhending**, Stofnið vöruhúsatínsluaðgerðir fyrir vöruhúsaafhendingar á tvo vegu:

- Á þrýstihátt, þar sem þú notar  **aðgerðina stofna tínslu** . Velja línurnar sem á að tína og undirbúa tínslur með því að tilgreina, til dæmis, hvaða hólf eigi að taka af og á í og hversu margar einingar eigi að afgreiða. Hólfin geta verið fyrirfram skilgreind fyrir vöruhúsastaðinn eða forðinn.
- Á togtísku, þar sem notuð  **er úttektaraðgerð** .  **Á síðunni tínsluvinnublað**  geta starfsmenn vöruhúss notað  **aðgerðina Sækja vöruhúsaskjöl**  til að fá úthlutaða tínslur. Þegar vöruhúsatínslan er fullskráð er línunum á  **tínsluvinnublaðinu**  eytt.

### <a name="4-register-a-warehouse-pick"></a><a name="4-register-a-warehouse-pick"></a>4: Vöruhúsatínsla skráð

 **Í Vöruhúsafærslusíðunni**  fyllir  **reiturinn Magn**  út fyrir hverja línu sem þeir hafa tekið til eða að hluta til og skráir tínsluna síðan.

Vöruhúsafærslur eru stofnaðar og vöruhúsatínslulínunum er eytt ef fullt magn var tekið til. Vöruhúsatínsluskjalið er áfram opið þar til heildarmagn vöruhúsaafhendingarinnar er skráð. Reiturinn **Tínt magn** á afhendingarlínu vöruhússins er uppfærður í samræmi.  

### <a name="5-post-the-warehouse-shipment"></a><a name="5-post-the-warehouse-shipment"></a>5: bóka vöruhúsaafhendinguna

Þegar allar vörur á vöruhúsaafhendingskjalinu eru skráðar sem tínslur, bókar vöruhúsastarfsmaðurinn afhendinguna. Bókun uppfærir birgðafærslurnar sem á að endurspegla minnkun birgða. Til dæmis reiturinn **Magn afgreitt** á upprunaskjalinu á útleið er uppfærður.  

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Stjórnun vöruhúss](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
