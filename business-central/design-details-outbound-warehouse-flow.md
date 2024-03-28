---
title: Yfirlit yfir vöruhúsaferli á útleið
description: Þessi grein lýsir verkflæði vöruhúss á útleið.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 02/05/2024
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes"></a>Vöruhúsaferli á útleið

Ferli á útleið í vöruhúsum hefst þegar upprunaskjal er gefið út til að taka vörur úr vöruhúsi. Til dæmis, annaðhvort til að senda vörurnar einhvers staðar eða flytja þær á annan stað fyrirtækis. Hægt er að afhenda raunbirgðavörur og vörur sem ekki eru í birgðum. Nánari upplýsingar um móttöku vara sem ekki eru í birgðum fást með því að fara í [Bóka vörur sem ekki eru í birgðum](#post-non-inventory-items). 

Ferli pantana á útleið samanstendur af tveimur aðgerðum:

* Vörur tíndar úr hillum.
* Afhending vara úr vöruhúsinu.

Upprunaskjölin fyrir vöruhúsaflæði á útleið eru:  

* Sölupöntun  
* Flutningspantanir á útleið.  
* Vöruskilapöntun innkaupa  
* Þjónustupöntun  

> [!NOTE]
> Framleiðslu- og samsetningarpantanir með íhlutaþörf tákna einnig upprunaskjöl á útleið. Framleiðslu- og samsetningarpantanir eru lítið annað því þær eru yfirleitt innri vinnslur sem tengjast ekki afhendingu. Þess í stað eru þeir notaðir til að ganga frá framleiddum vörum eða færa íhluti sem þarf til að setja vöru saman í samsetningarsvæði. Nánari upplýsingar um þessi ferli í [Hönnunarupplýsingar: Vöruhúsaflæði innanhúss](design-details-internal-warehouse-flows.md).  

Vörur [!INCLUDE[prod_short](includes/prod_short.md)] eru tíndar og afhentar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flóknarastig (Fræðast meira um [vöruhúsakerfisyfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínsluna og afhendinguna úr pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: Pöntun-fyrir-pöntun.|  
|U|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Bókuð móttaka/sending í mörgum pöntunum.|  
|D|Tínslan er bókuð úr vöruhúsatínsluskjali og afhendingin bókuð úr vöruhúsaafhendingarskjali|Kveikt|Kveikt|Ítarlegt|  

Nálgunin til að velja fer eftir vinnubrögðum vöruhússins og flækjustigi stjórnunar. Eftirfarandi eru nokkur dæmi sem gætu hjálpað þér að ákveða.

* Í pantanaumhverfi með einföldum ferlum og einfaldri hólfauppbyggingu er viðeigandi aðferð A, tínsla og afhending úr pöntunarlínunni.
* Ef vörur í pöntunarlínu eru úr fleiri en einu hólfi, eða ef starfsmenn vöruhússins geta ekki unnið með pantanaskjöl, er notkun á sérstökum tínsluskjölum viðeigandi er aðferð B rétt.
* Ef vinnslur tínslu og afhendingar fela í sér margar pantanir og krefjast meiri stjórnunar og yfirlits er hægt að velja að nota vöruhúsaafhendingarskjal og vöruhúsatínsluskjal til að aðgreina tínslu- og afhendingarverkhluta, aðferðir C og D.  

Í aðferðum A, B og C eru tínslu- og afhendingaraðgerðir sameinaðar í einu skrefi þegar skjalið er bókað sem afhent. Aðferð D er tínslan fyrst skráð og síðan er afhendingin bókuð síðar úr öðru skjali.

> [!NOTE]
> Á meðan vöruhúsatínsla og birgðatínsla hljóma svipuð eru þau mismunandi skjöl og notuð í mismunandi ferlum.
> * Birgðatínslan sem notuð er í aðferð B, ásamt því að skrá tínsluupplýsingar, bókar einnig afhendingu upprunaskjalsins.
> * Ekki er hægt að bóka vöruhúsatínsluna sem notuð er í D-aðferð og skráir tínsluna aðeins. Skráningin gerir vörurnar tiltækar fyrir vöruhúsaafhendinguna en bókar ekki afhendinguna. Í útleiðarflæðinu þarf vöruhúsatínsluna vöruhúsaafhendingu.

## <a name="no-dedicated-warehouse-activity"></a>Engin sérstök vöruhúsaaðgerð

Eftirfarandi greinar veita upplýsingar um hvernig á að vinna móttökur upprunaskjala ef ekki er tilteknar vöruhúsaaðgerðir.

* [Selja vöru](sales-how-sell-products.md)
* [Millifærslupantanir](inventory-how-transfer-between-locations.md)
* [Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md)
* [Stofna þjónustupantanir](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations"></a>Einfaldar vöruhúsaskilgreiningar

Eftirfarandi skýringarmynd lýsir vöruhúsaferlum á útleið fyrir mismunandi tegundir skjala í grunnskilgreiningum vöruhúsa. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Sýnir verkstigin í grunnflæði út í vöruhúsi.":::

### <a name="1-release-a-source-document"></a>1: Gefa út upprunaskjal

Þegar aðgerðin **Gefa út** er notuð á upprunaskjali, t.d. sölu- eða millifærslupöntun, eru vörurnar á skjalinu tilbúnar til afgreiðslu í vöruhúsinu. Til dæmis tínt og sett í hólfið sem tilgreint er á fylgiskjalinu. Einnig er hægt að stofna birgðatínsluskjöl fyrir einstakar línur í pöntunum, á tísku, byggt á tilteknum hólfum og magni sem á að meðhöndla.  

### <a name="2-create-an-inventory-pick"></a>2: Stofna birgðatínslu

Á síðunni Birgðatínsla **sækir** starfsmaður vöruhússins, á toga í upprunaskjalslínurnar. Að öðrum kosti er birgðatínslulínur þegar stofnaðar, með ýtingu, af notanda sem er ábyrgur fyrir upprunaskjalinu.  

### <a name="3-post-an-inventory-pick"></a>3: Bóka birgðatínslu

Í hverri línu fyrir vörur sem hafa verið tíndar eða færðar að hluta eða til fulls er reiturinn **Magn fylltur** út og birgðatínslan síðan bókuð. Upprunaskjöl sem tengjast  birgðatínslu eru bókuð sem afgreitt eða notað.  

Fyrir birgðatínslu eru neikvæðar birgðabókarfærslur stofnaðar, vöruhúsafærslur stofnaðar og tínslubeiðni eytt, ef meðhöndluð að fullu. Til dæmis reiturinn **Magn afgreitt** á upprunaskjalinu á útleið er uppfærður. Bókað afhendingarskjal er stofnað til að til dæmis endurspegla sölupöntunina og afhentar vörur.  

## <a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi

Eftirfarandi skýringarmynd sýnir ferli útleiðarvöruhúsa fyrir mismunandi gerðir skjala í ítarlegri vöruhúsgrunnstillingu. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Sýnir þrepin í ítarlegu vöruhúsaflæði á útleið.":::

### <a name="1-release-a-source-document-1"></a>1: Gefa út upprunaskjal

Það sama og þegar upprunaskjali er lokað í ítarlegum grunnstillingum er það sama og fyrir grunnstillingar. Vörurnar verða tiltækar til meðhöndlunar í vöruhúsinu. Þau geta til dæmis verið talin með í afhendingu.  

### <a name="2-create-a-warehouse-shipment"></a>2: Stofna vöruhúsaafhendingu

Á síðunni **Vöruhúsaafhending** eru línurnar sóttar í útgefna upprunaskjalið. Hægt er að sameina línur úr nokkrum upprunaskjalum í einni vöruhúsaafhendingu.  

### <a name="3-create-a-warehouse-pick"></a>3: Stofna vöruhúsatínslu

Á síðunni **Vöruhúsaafhending** er hægt að stofna vöruhúsatínsluaðgerðir fyrir vöruhúsaafhendingar á tvo vegu:

- Á tísku þar sem aðgerðin **Stofna tínslu** er notuð. Línurnar sem á að tína eru valdar og tínslan undirbúin með því að tilgreina, til dæmis hvaða hólf á að taka úr og setja í og hversu margar einingar á að meðhöndla. Hægt er að forskilgreina hólfin fyrir vöruhúsastaðinn eða forðann.
- Á toga í tísku, þar sem aðgerðin **Gefa út** er notuð. Á síðunni **Vinnublað** tínslu geta starfsmenn vöruhússins notað aðgerðina **Sækja vöruhúsaskjöl** til að fá úthlutaðar tínslur sínar. Þegar vöruhúsatínslan er fullkomlega skráð eyðast línurnar á vinnublaði **tínslu**.

### <a name="4-register-a-warehouse-pick"></a>4: Skrá vöruhúsatínslu

Á síðunni **Vöruhúsatínsla** fyllir starfsmaður vöruhúss út reitinn **Magn** fyrir hverja línu sem hann hefur tínt að fullu eða að hluta og skráir síðan tínsluna.

Vöruhúsafærslur eru stofnaðar og vöruhúsatínslulínunum er eytt ef allt magnið var tínt. Vöruhúsatínsluskjalið er opið þar til allt magn vöruhúsaafhendingarinnar er skráð. Reiturinn **Tínt magn** á afhendingarlínu vöruhússins er uppfærður í samræmi.  

### <a name="5-post-the-warehouse-shipment"></a>5: Bóka vöruhúsaafhendinguna

Þegar allar vörur í vöruhúsaafhendingarskjalinu eru skráðar sem tíndar bókar starfsmaður vöruhússins afhendinguna. Bókun uppfærir birgðafærslurnar til að endurspegla birgðaminnkunina. Til dæmis reiturinn **Magn afgreitt** á upprunaskjalinu á útleið er uppfærður.  

## <a name="post-non-inventory-items"></a>Bóka vörur sem eru ekki í birgðum

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsakerfi](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
