---
title: Hönnunarupplýsingar - vöruhúsaflæði inn
description: Læra að taka á móti vörum í vöruhúsinu og skrá þær og passa við upprunaskjöl á innleið.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: warehouse
ms.date: 09/18/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-inbound-warehouse-flow"></a>Hönnunarupplýsingar: Vöruhúsaflæði á innleið

Flæðiá innleið í vöruhús byrjar þegar vörurnar koma í vöruhús á staðsetningu fyrirtækis, annað hvort frá utanaðkomandi aðila eða frá annarri staðsetningu fyrirtækis. Hægt er að taka á móti efnislegum og óbirgðum vörum. Nánari upplýsingar um móttöku vara sem ekki eru í birgðum fást með því að fara í [Bóka vörur sem ekki eru í birgðum](#post-non-inventory-items).

Ferlið við móttöku pantana á innleið samanstendur af tveimur aðgerðum:

* Taka á móti vörum við bryggjuna, auðkenna þær, passa þær við upprunaskjal og skrá móttekið magn.
* Gengið er frá vörum á lager og þær skráðar.

Upprunaskjölin fyrir vöruhúsaflæði á innleið eru:

* Innkaupapantanir  
* Millifærslupantanir á innleið  
* Vöruskilapantanir sölu  

> [!NOTE]
> Framleiðsla og samsetningarfrálag tákna einnig upprunaskjöl á innleið. Fræðast meira um meðhöndlun framleiðslu og samsetningar frálags innanhúss í [Hönnunarupplýsingar: Vöruhúsaflæði innanhúss](design-details-internal-warehouse-flows.md).  

Vörur [!INCLUDE[prod_short](includes/prod_short.md)] eru mótteknar og gengið frá þeim með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast móttöku|Krefjast frágangs|Flóknarastig (Fræðast meira um [vöruhúsakerfisyfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: Pöntun-fyrir-pöntun.|  
|U|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Bókuð móttaka/sending í mörgum pöntunum.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Val á nálgun ræðst af starfshætti fyrirtækisins og flækjustigi stjórnunar. Eftirfarandi eru nokkur dæmi sem gætu hjálpað þér að ákveða.

* Í umhverfi fyrir pöntun fyrir pöntun, þar sem flest starfsfólk vöruhússins vinnur beint með pöntunarskjöl, er hægt að nota aðferðina A. 
* Vöruhús fyrir pantanir sem er með flóknari frágangsvinnslu eða þar sem starfsfólk vöruhúss skilur frágangsaðgerðir sínar frá pöntunarskjalinu, gæti notað aðferð B.
* Fyrirtækjum sem þarf að áætla meðhöndlun margra pantana getur verið gagnlegt að nota vöruhúsamóttökuskjöl, aðferðir C og D.  

Í aðferðum A, B og C er móttaka og frágangur sameinað í einu þrepi þegar skjöl eru bókuð sem móttekin. Þegar D-aðferð er móttakan bókuð fyrst til að skrá aukningu birgða og að vörur séu tiltækar til sölu. Starfsmaður vöruhússins skráir síðan fráganginn til að gera vörurnar tiltækar fyrir tínslu fyrir pantanir á útleið. 

> [!NOTE]
> Á meðan vöruhúsafrágangur og birgðafrágangur hljóma svipað eru þau mismunandi skjöl og notuð í mismunandi ferlum.
> * Birgðafrágangurinn sem notaður er í aðferð B, ásamt skráningu frágangsupplýsinga, bókar einnig móttöku upprunaskjalsins.
> * Ekki er hægt að bóka vöruhúsafráganginn sem notaður er í aðferð D og skráir aðeins fráganginn. Skráningin gerir vörurnar tiltækar til frekari vinnslu en bókar ekki móttökuna. Í innleiðarflæðinu þarf vöruhúsafrágangurinn vöruhúsamóttöku.

## <a name="no-dedicated-warehouse-activity"></a>Engin sérstök vöruhúsaaðgerð

Eftirfarandi greinar veita upplýsingar um hvernig á að vinna móttökur upprunaskjala ef ekki er tilteknar vöruhúsaaðgerðir.

* [Skrá innkaup](purchasing-how-record-purchases.md)
* [Millifærslupantanir](inventory-how-transfer-between-locations.md)
* [Vinna söluvöruskilapantanir](sales-how-process-sales-returns-orders.md)

## <a name="basic-warehouse-configurations"></a>Einfaldar vöruhúsaskilgreiningar

Kveikt er á krefjast frágangsvíkkunar **í grunnstillingu** vöruhúss en **slökkt er á vífærinu Krefjast móttöku** á **síðunni Birgðageymsluspjald** fyrir birgðageymsluna.

Eftirfarandi skýringarmynd sýnir innflæði í vöruhús eftir skjalagerð grunngerðar vöruhúss. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Grunnflæði á innleið í vöruhúsi.":::

### <a name="1-release-a-source-document-to-create-a-request-for-an-inventory-put-away"></a>1: Gefa út upprunaskjal til að stofna beiðni um birgðafrágang

Þegar vörur eru mótteknar er upprunaskjalið gefið út, t.d. innkaupapöntun eða millifærslupöntun á innleið. Ef fylgiskjalinu er sleppt er hægt að ganga frá vörunum. Einnig er hægt að stofna birgðafrágangsskjöl fyrir einstakar pöntunarlínur á tísku á grundvelli hólfa og magns sem á að meðhöndla.  

### <a name="2-create-an-inventory-put-away"></a>2: Stofna birgðafrágang

Á síðunni **Birgðafrágangur**, á toga í tísku, er hægt að sækja upprunaskjalslínur í undirbúningi samkvæmt vöruhúsabeiðnum á innleið. Á tísku er einnig hægt að stofna birgðafrágangslínur þegar upprunaskjalið er stofnað.  

### <a name="3-post-an-inventory-put-away"></a>3: Bóka birgðafrágang

Í hverri línu fyrir vörur sem gengið hefur verið frá, að hluta eða til fulls er reiturinn **Magn fylltur** út og birgðafrágangurinn síðan bókaður. Upprunaskjöl sem tengjast birgðafrágangi eru bókuð sem móttekin.  

* Jákvæðar birgðafærslur eru stofnaðar.
* Vöruhúsafærslur eru stofnaðar fyrir birgðageymslur sem krefjast hólfkóta í öllum birgðafærslum.
* Frágangsbeiðninni er eytt ef hún er meðhöndluð að fullu. Til dæmis reiturinn **Móttekið magn** á upprunaskjallínu á innleið er uppfærður.
* Bókað móttökuskjal er stofnað til að til dæmis endurspegla innkaupapöntunina og mótteknar vörur.  

## <a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi

Til að nota ítarlega vöruhúsaskilgreiningu er kveikt á vífærslunni **Krefjast móttöku** á síðunni Birgðageymsluspjald fyrir birgðageymsluna. Krefjast **frágangsvíkkunar** er valfrjáls.

Eftirfarandi skýringarmynd sýnir vöruhúsaflæði inn eftir skjalategund. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Ítarlegt flæði á innleið í vöruhúsi.":::

### <a name="1-release-the-source-document"></a>1: Gefa út upprunaskjalið

Þegar vörur eru mótteknar er upprunaskjalið gefið út, t.d. innkaupapöntun eða millifærslupöntun á innleið. Ef fylgiskjalinu er sleppt er hægt að ganga frá vörunum. Frágangurinn felur í sér vísanir í upprunaskjalstegund og númer.

### <a name="2-create-a-warehouse-receipt"></a>2: Stofna vöruhúsamóttöku

Á síðunni **Vöruhúsamóttaka** eru upprunaskjalslínur á innleið sóttar. Hægt er að sameina nokkrar upprunaskjalslínur í eitt vöruhúsamóttökuskjal. Reiturinn **Magn til afgreiðslu** er fylltur út og svæðið og hólfið sem þarf valið, ef þörf krefur.  

### <a name="3-post-the-warehouse-receipt"></a>3: Bóka vöruhúsamóttökuna

Bóka vöruhúsamóttökuna til að búa til jákvæðar birgðafærslur. Reiturinn **Móttekið** magn í upprunaskjalslínunni á innleið er uppfærður.  

 **Ef krefjast frágangsvíkkunar** er ekki kveikt á birgðageymsluspjaldinu stöðvar ferlið hér. Annars er hægt að bóka upprunaskjal á innleið sem hægt er að ganga frá. Frágangurinn felur í sér upprunaskjalstegund og númer.  

### <a name="4-optional-generate-put-away-worksheet-lines"></a>4: (Valfrjálst) Mynda línur frágangsvinnublaðs

Sækja frágangslínur vöruhúss á **vinnublaði** frágangs á grundvelli bókaðra vöruhúsamóttaka eða aðgerða sem framleiða frálag. Á línunum sem gengið er frá eru eftirfarandi upplýsingar tilgreindar:

* Hólfin sem taka á vörur úr.
* Hólfin sem setja á vörur í.
* Hve margar einingar á að meðhöndla.

Hólfin geta verið fyrirfram skilgreind með uppsetningu vöruhúsastaðsetningarinnar eða forðanum sem framkvæmdi aðgerðina.  

Þegar allur frágangur er áætlaður og tengdur starfsmönnum vöruhúss eru vöruhúsafrágangsskjölin mynduð. Fullúthlutuðum frágangslínum er eytt af **vinnublaði** frágangs.  

> [!NOTE]  
>  **Ef vísbendingin Nota vinnublað** frágangs er ekki kveikt á birgðageymsluspjaldinu eru vöruhúsafrágangsskjöl stofnuð beint á grundvelli bókaðra vöruhúsamóttaka. Í því tilviki er ekki þörf á þessu skrefi.  

### <a name="5-create-a-warehouse-put-away-document"></a>5: Stofna frágangsskjal vöruhúss

Stofna vöruhúsafrágangsskjal á toga í tísku sem byggð er á bókuðu vöruhúsamóttökunni. Einnig er hægt að stofna frágangsskjal vöruhúss og úthluta því á starfsmann vöruhúss á tísku.  

### <a name="6-register-a-warehouse-put-away"></a>6: Skrá vöruhúsafrágang

Í **hverri línu fyrir vörur sem gengið hefur verið frá, að hluta eða til fulls er reiturinn Magn fylltur** út á síðunni **Vöruhúsafrágangur** og vöruhúsafrágangurinn skráður.  

* Vöruhúsafærslur eru stofnaðar fyrir birgðageymslur sem krefjast hólfkóta í öllum birgðafærslum.
* Vöruhúsafrágangslínunum er eytt ef þær eru meðhöndlaðar að fullu.
* Vöruhúsafrágangsskjalið er áfram opið þar til allt magn tengdrar bókuðu vöruhúsamóttökunnar er skráð.
* Reiturinn **Frágangur** magns á bókuðum móttökupöntunarlínum vöruhúss er uppfærður.

## <a name="related-tasks"></a>Tengd verkefni

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|  
|Taka á móti vörum á vöruhúsastöðum með vöruhúsamóttöku fyrir fullkomlega eða sjálfvirka vöruhúsavinnslu.|[Móttaka vara](warehouse-how-receive-items.md)|
|Gengið frá vörum á grundvellinum pöntun-fyrir-pöntun og móttakan bókuð í einni aðgerð í einfaldri grunnstillingu vöruhúss.|[Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Ganga frá vörum sem mótteknar eru frá mörgum innkaupum, söluvöruskilum, flytur pantanir í ítarlegri vöruhúsaskilgreiningu.|[Ganga frá vörum með vöruhúsafrágangi](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  

## <a name="post-non-inventory-items"></a>Bóka vörur sem eru ekki í birgðum

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## <a name="see-also"></a>Sjá einnig .

[!INCLUDE[footer-include](includes/footer-banner.md)]
