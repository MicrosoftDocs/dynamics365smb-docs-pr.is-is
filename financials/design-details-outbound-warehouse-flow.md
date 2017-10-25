---
title: "Hönnunarupplýsingar - Vöruhúsaflæði á útleið | Microsoft Docs"
description: "Flæði á útleið í vöruhúsinu hefst með beiðni úr losuðum upprunaskjölum um að flytja vöruna af staðsetningu vörushússins, annað hvort til að flytja hana til þriðja aðila eða á aðra staðsetningu fyrirtækisins. Úr geymslusvæðinu eru vöruhúsaaðgerðir framkvæmdar á mismunandi flækjustigi til að koma vörunum af afhendingarsvæðinu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 54489c23a34e409ccb22faff77da41acdaf065b3
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-outbound-warehouse-flow"></a>Hönnunarupplýsingar: vöruhúsaflæði á innleið
Flæði á útleið í vöruhúsinu hefst með beiðni úr losuðum upprunaskjölum um að flytja vöruna af staðsetningu vörushússins, annað hvort til að flytja hana til þriðja aðila eða á aðra staðsetningu fyrirtækisins. Úr geymslusvæðinu eru vöruhúsaaðgerðir framkvæmdar á mismunandi flækjustigi til að koma vörunum af afhendingarsvæðinu.  

 Hver vara er greint og samsvörun við samsvarandi upprunaskjal inn. Eftirfarandi upprunaskjal á útleið er til:  

- Sölupöntun  
- Flutningspantanir á útleið.  
- Vöruskilapöntun innkaupa  
- Þjónustupöntun  

Að auki eru eftirfarandi innri uppspretta gögn sem virka eins uppruni á útleið:  

- Framleiðslupöntun með íhlutaþörf  
- Samsetningarpöntun með íhlutaþörf  

 Síðustu tvö fylgiskjölin standa fyrir flæði á útleið úr vöruhúsi til innri rekstrarsviða. Frekari upplýsingar um vöruhúsameðhöndlun fyrir innri ferli á innleið og útleið eru í [Hönnunarupplýsingar: Innra vöruhúsaflæði](design-details-internal-warehouse-flows.md).  

 Ferli og notendaviðmótsskjöl í vöruhúsi Á útleið eru ólík á milli grunnvöruhúss og ítarlegs vöruhúss. Aðalmunurinn er sá aðgerðir eru framkvæmdar pöntun fyrir pöntun í grunnvörugeymslu þegar þeim er steypt saman fyrir margfaldar pantanir í ítarlegu vöruhúsi. Nánari upplýsingar um mismunandi vöruhúsaflækjustig eru í [Hönnunarupplýsingar: Vöruhúsayfirlit](design-details-warehouse-setup.md).  

 Í [!INCLUDE[d365fin](includes/d365fin_md.md)], er hægt að framkvæma útleiðarferlið til að tína og afhenda á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Tínsla|Afhendingar|Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka tínslu og afhendingu frá pöntunarlínunni|X|||2|  
|Á|Bóka tínslu og afhendingu frá birgðatínsluskjali||X||3|  
|C|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali|||X|4/5/6|  
|D|Bóka tínslu frá vöruhúsatínsluskjali og bóka afhendingu frá vöruhúsaafhendingarskjali||X|X|4/5/6|  

 Nánari upplýsingar má nálgast á [Hönnunarupplýsingar: vöruhúsaflæði á útleið]()  

 Val á aðferð fer eftir samþykku verklagi fyrirtækisins og flækjustigi. Í pöntun fyrir pöntun umhverfi með einföldum aðferðum og einfaldri hólfaskipan er aðferð A, tiltekt og afhending frá pöntunarlínu viðeigandi. Í öðrum pöntun fyrir pöntun fyrirtækjum þar sem vörur fyrir eina pöntunarlínu geta komið frá fleiri en einu hólfi eða þar sem vöruhúsastarfsmenn geta ekki unnið með pantanaskjöl á notkun aðskilinna tiltektarskjala við, aðferð B. Ef fyrirtæki er með tiltektar og afhendingarferli með magnpantanavinnslu og þarf því meiri stjórn og yfirsýn, getur fyrirtækið valið að nota vöruhúsaafhendingarskjal og vöruhúsatínsluskjal til að aðskilja tiltektar og afhendingarverk, aðferðir C og D.  

 Í aðferðum A, B, og C eru tiltektar- og afhendingaraðgerðir sameinaðar í eitt skref þegar samsvarandi skjal er bókað sem flutt. Í aðferð D er tiltekt fyrst skráð og svo er afhendingin bókuð síðar úr öðru skjali.  

## <a name="basic-warehouse-configurations"></a>Grunngerðir vöruhúss  
 Eftirfarandi skýringarmynd sýnir útflæði í vöruhús eftir skjalagerð grunngerðar vöruhúss. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

 ![Flæði á útleið í grunngerðir vöruhúss](media/design_details_warehouse_management_outbound_basic_flow.png "Hönnunarupplýsingar_vöruhúsastjórn_grunnflæði_á_útleið")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1: Upprunaskjal losunar / Stofna birgðatínsla eða Hreyfing  
 Þegar notandi sem er ábyrgur fyrir Þegar notandi sem er ábyrgur fyrir upprunaskjölum, svo sem sölupantanavinnsla eða framleiðslustjóri, er tilbúinn fyrir vöruhúsastarfsemi á útleið, sleppir hann eða hún upprunaskjalinu til að  láta starfsmenn í vöruhúsi vita að hægt er að sækja seldar vörur eða íhluti og setja í tilgreind hólf. Að öðrum kosti, notandinn býr til birgðatínslu eða hreyfingarskjöl fyrir stakar pöntunarlínur með færslu, byggt á tilgreindum hólfum og magni til meðhöndlunar.  

> [!NOTE]  
>  Birgðahreyfingar eru notaðar til að færa vörur til innri starfssvæði í grunnvörugeymslu, byggt á upprunaskjöl eða á tilfallandi grunni.  

### <a name="2-create-outbound-request"></a>2: stofna á útleið beiðni  
 Þegar upprunaskjal á útleið er losað er stofnuð sjálfkrafa stofnuð vöruhúsabeiðni á útleið. Það inniheldur tilvísanir til upprunaskjalstegund og númeri og er ekki sýnilegt notandanum.  

### <a name="3-create-inventory-pick-or-movement"></a>3: Stofna birgðatínsla eða hreyfingu  
 Í **Birgðatínsla** eða **Birgðahreyfing** glugganum sækir vöruhúsanotandi sem er ábyrgur fyrir móttöku, með aðferðinni tínslur, væntanlegar upprunaskjalslínur byggt á vöruhúsabeiðnum á innleið. Að öðrum kosti er birgðatínslulínur þegar stofnaðar, með ýtingu, af notanda sem er ábyrgur fyrir upprunaskjalinu.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4: Bóka birgðatínslu eða skrá birgðahreyfingu  
 Í hverri línu fyrir vöru sem hefur verið tínd eða færð, að hluta eða fullu, fyllir starfsmaður í vöruhúsi út reitinn **Magn** og bókar svo birgðatínslu eða skráir birgðahreyfingu. Upprunaskjöl sem tengjast  birgðatínslu eru bókuð sem afgreitt eða notað. Upprunaskjöl sem tengjast birgðahreyfingu eru ekki bókuð.  

 Fyrir birgðatínslu eru neikvæðar birgðabókarfærslur stofnaðar, vöruhúsafærslur stofnaðar og tínslubeiðni eytt, ef meðhöndluð að fullu. Til dæmis reiturinn **Magn afgreitt** á upprunaskjalinu á útleið er uppfærður. Bókað afhendingarskjal er stofnað til að til dæmis endurspegla sölupöntunina og afhentar vörur.  

## <a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi  
 Eftirfarandi skýringarmynd sýnir útflæði í vöruhús eftir skjalagerð í grunngerð ítarlegu vöruhúsi. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

 ![Flæði á útleið í grunngerð ítarleg vöruhúsum](media/design_details_warehouse_management_outbound_advanced_flow.png "Hönnunarupplýsingar_vöruhúsastjórn_ítarlegt_flæði_á_útleið")  

### <a name="1-release-source-document"></a>1: Upprunaskjal losunar  
 Þegar notandi sem er ábyrgur fyrir upprunaskjölum, svo sem sölupantanavinnsla eða framleiðslustjóri, er tilbúinn fyrir vöruhúsastarfsemi á útleið, sleppir hann eða hún upprunaskjalinu til að  láta starfsmenn í vöruhúsi vita að hægt er að sækja seldar vörur eða íhluti og setja í tilgreind hólf.  

### <a name="2-create-outbound-request"></a>2: stofna á útleið beiðni  
 Þegar upprunaskjal á innleið er losað er stofnuð sjálfkrafa stofnuð vöruhúsabeiðni á útleið. Það inniheldur tilvísanir til upprunaskjalstegund og númeri og er ekki sýnilegt notandanum.  

### <a name="3-create-warehouse-shipment"></a>3: Stofna vöruhúsaafhendingu  
 Í **Vöruhúsaafhendingu** glugga sækir starfsmaður í afhendingu sem er ábyrgur væntanlegar upprunaskjalalínur byggt á vöruhúsabeiðnum á útleið. Margar línurnar úr upprunaskjölunum er hægt að sameina í eitt Vöruhúsaafhendingarskjal.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4: Losa afhendingu / Stofna vöruhústínslu  
 Afhendingarstarfsmaðurinn sem er ábyrgur losar vöruhússafhendingu til að starfsmenn vöruhússins geti stofnað eða samhæft tiltektir vöruhúss fyrir viðkomandi afhendingu.  

 Að öðrum kosti stofnar notandinn vöruhússtínsluskjal fyrir stakar afhendingarlínur, með ýtingu, samkvæmta tilgreindum hólfum og magni sem á að meðhöndla.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5: Losa innri virkni / Stofna vöruhúsatínslu  
 Notandinn sem er ábyrgur fyrir innri virkni losar innra upprunaskjal, t.d. vöru- og samsetningarpöntun, þannig að starfsmenn vöruhússins geti stofnað eða samhæft tiltektir vöruhúss fyrir viðkomandi innri virkni.  

 Að öðrum kosti stofnar notandinn vöruhússtínsluskjöl fyrir stakar framleiðslu- eða samsetningarpöntun, með ýtingu, samkvæmta tilgreindum hólfum og magni sem á að meðhöndla.  

### <a name="6-create-pick-request"></a>6: Stofna tiltektarbeiðni  
 Þegar upprunaskjal á útleið er losað er sjálfkrafa stofnuð tiltektarbeiðni í vöruhúsi. Það inniheldur tilvísanir til upprunaskjalstegund og númeri og er ekki sýnilegt notandanum. Eftir uppsetningu, notkun frá framleiðslu og samsetningarpöntun þess skapar einnig tiltektarbeiðni til að ná nauðsynlega íhluti frá lager.  

### <a name="7-generate-pick-worksheet-lines"></a>7: Mynda tínsluvinnublaðslínur  
 Notandinn sem er ábyrgur fyrir samræmingu tiltekta sækir tiltektarlínur vöruhúss í **Vinnublað tínslu** byggt á tiltektarbeiðnum úr afhendingum vöruhúss eða innri virkni með notkun íhlutar. Notandinn velur línurnar sem á að taka til og undirbýr tiltektina með því að tilgreina úr hvaða hólfum á að taka, í hvaða hólf á að setja og hversu margar einingar á að meðhöndla. Hólf er hægt að forskilgreina í uppsetningu vöruhússstaðsetningar eða vinnslutilfanga.  

 Notandinn tilgreinir tiltektaraðgerðina fyrir góða vöruhúsameðhöndlun og notar svo aðgerð til að búa til samsvarandi tínsluskjal vöruhúss sem er úthlutað á mismunandi starfsmenn í vöruhúsi sem sjá um tiltekt í vöruhúsi. Þegar öllum tiltektum í vöruhúsi hefur verið úthlutað er línunum **Vinnublaði tínslu** eytt.  

### <a name="8-create-warehouse-pick-documents"></a>8: Stofna tínsluskjöl vöruhúss  
 Starfsmaður í vöruhúsi sem sér um tínslur stofnar tínsluskjal vöruhúss, af gerðinni tínslur, byggt á losnuðu upprunaskjali. Að öðrum kosti er vöruhússtínsluskjalið stofnað og úthlutað á starfsmann í vöruhúsi með ýtingu.  

### <a name="9-register-warehouse-pick"></a>9: Skrá vöruhúsatínslu  
 Í hverri línu fyrir vöru sem hefur verið tínd, að hluta eða fullu, fyllir starfsmaður í vöruhúsi út reitinn **Magn** í glugganum **Vöruhúsatínsla** og skráir svo vöruhústínsluna.  

 Vöruhúsafærslur eru búnar til og vöruhúsatiltektarlínum eytt, ef að fullu meðhöndlaðar. Tínsluskjal vöruhúss er opið þar til allt magn tengdrar sendingar vöruhúss er skráð. Reiturinn **Tínt magn** á afhendingarlínu vöruhússins er uppfærður í samræmi.  

### <a name="10-post-warehouse-shipment"></a>10: Bóka vöruhúsaafhendingu  
 Þegar allar vörur í vöruhúsaafhendingarskjalinu eru skráðar sem teknar til í tilgreind afhendingarhólf bókar starfsmaður afhendingar sem ber ábyrgð vöruhúsaafhendinguna. Neikvæðar birgðafærslur eru stofnaðar. Til dæmis reiturinn **Magn afgreitt** á upprunaskjalinu á útleið er uppfærður.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)

