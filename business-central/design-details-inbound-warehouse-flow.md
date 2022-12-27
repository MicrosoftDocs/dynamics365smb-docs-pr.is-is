---
title: Hönnunarupplýsingar - vöruhúsaflæði inn
description: Vöruhúsaflæði á innleið hefst þegar vörur koma á staðsetningu vöruhúss. Vörur eru skráðar og að lokum jafnaðar við upprunaskjöl á innleið.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: de7a468377f454c01d45742f4510cb9978340ae6
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132004"
---
# <a name="design-details-inbound-warehouse-flow"></a>Hönnunarupplýsingar: vöruhúsaflæði inn
Flæðiá innleið í vöruhús byrjar þegar vörurnar koma í vöruhús á staðsetningu fyrirtækis, annað hvort frá utanaðkomandi aðila eða frá annarri staðsetningu fyrirtækis. Starfsmaður skráir vörurnar, yfirleitt með því að skanna strikamerki. Úr móttökusvæðinu eru vöruhúsaaðgerðir framkvæmdar á mismunandi flækjustigi til að koma vörunum inn á geymslusvæðið.  

 Hver vara er greint og samsvörun við samsvarandi upprunaskjal inn. Eftirfarandi upprunaskjal á innleið er til:  

- Innkaupapöntun  
- Flutningspöntun á innleið  
- Vöruskilapöntun sölu  

Að auki eru eftirfarandi innri upprunaskjal sem virka eins og uppruni á innleið:  

- Framleiðslupöntun með bókun frálags  
- Samsetningarpöntun með frálagsbókun  

Síðustu tvö standa fyrir flæði á innleið úr vöruhúsi til innri rekstrarsviða. Frekari upplýsingar um vöruhúsameðhöndlun fyrir innri ferli á innleið og útleið eru í [Hönnunarupplýsingar: Innra vöruhúsaflæði](design-details-internal-warehouse-flows.md).  

Ferli og notendaviðmótsskjöl í vöruhúsi á innleið eru ólík á milli grunnvöruhúss og ítarlegs vöruhúss. Aðalmunurinn er sá aðgerðir eru framkvæmdar pöntun fyrir pöntun í grunnvörugeymslu þegar þeim er steypt saman fyrir margfaldar pantanir í ítarlegu vöruhúsi. Nánari upplýsingar um mismunandi vöruhúsaflækjustig eru í [Hönnunarupplýsingar: Vöruhúsayfirlit](design-details-warehouse-setup.md).  

Í [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Móttökur|Frágangur|Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|X|||2|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali|||X|3|  
|C|Bóka móttöku og frágang frá vöruhúsamóttökuskjali||X||4/5/6|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali||X|X|4/5/6|  

Val á aðferð fer eftir samþykku verklagi fyrirtækisins og flækjustigi. Í pöntun fyrir pöntun vöruhúsaumhverfi, þar sem flestir af lagerstarfsfólki vinnur beint með pöntunarskjöl, getur fyrirtæki ákveðið að nota aðferð A. Pöntun fyrir pöntun vöruhús sem hefur flóknari frágangsferli eða þar sem er sérstakt starfsfólk til að framkvæma vöruhúsaaðgerðir, gæti ákveðið að skilja að frágangsaðgerðir frá pöntunarskjalinu, aðferð B. Auk þess fyrirtæki sem þurfa að skipuleggja meðhöndlun margra pantanir getur fundið það gagnlegt að nota skjöl vöruhúsamóttöku, aðferðir C og D.  

Í aðferðum A, B, og C eru aðgerðirnar móttaka og frágangur sameinaðar í eitt skref þegar samsvarandi skjal eru bókuð sem móttekið. Í aðferð D er móttaka bókuð fyrst til að staðfesta birgðahækkun og að vörur séu tiltækar til sölu. Starfsmaður í vöruhúsi skráir svo fráganginn til að gera vörur tilbúnar fyrir tínslu.  

## <a name="basic-warehouse-configurations"></a>Grunngerðir vöruhúss  
Eftirfarandi skýringarmynd sýnir innflæði í vöruhús eftir skjalagerð grunngerðar vöruhúss. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

![Flæði á innleið í grunnskilgreiningum vöruhúss.](media/design_details_warehouse_management_inbound_basic_flow.png "Flæði á innleið í grunngerðir vöruhúss")  

### <a name="1-release-source-document--create-inventory-put-away"></a>1: Upprunaskjal losunar / Stofna Birgðafrágang  
Þegar vörur berast í vöruhús, gefur notandi sem er ábyrgur fyrir móttöku út upprunaskjaliið, svo sem innkaupapöntun eða flutningspöntun á innleið, til að láta starfsmenn í vöruhúsi vita að mótteknar vörur megi ganga frá í birgðum. Að öðrum kosti stofnar notandinn birgðafrágangsskjöl fyrir stakar pantanalínur, með ýtingu, samkvæmta tilgreindum hólfum og magni sem á að meðhöndla.  

### <a name="2-create-inbound-request"></a>2: Stofna innleiðarbeiðni  
Þegar upprunaskjal á innleið er losað er stofnuð sjálfkrafa stofnuð vöruhúsabeiðni á innleið. Það inniheldur tilvísanir til upprunaskjalstegund og númeri og er ekki sýnilegt notandanum.  

### <a name="3-create-inventory-put-away"></a>3: Birgðafrágangur búinn til  
Á síðunni **Birgðafrágangur** sækir vöruhúsanotandi sem er ábyrgur fyrir móttöku, með aðferðinni tínslur, væntanlegt upprunaskjalslínur byggt á vöruhúsabeiðnum á innleið. Að öðrum kosti er birgðafrágangslínur þegar stofnaðar, með ýtingu, af notanda sem er ábyrgur fyrir upprunaskjalinu.  

### <a name="4-post-inventory-put-away"></a>4: Birgðafrágangur  
Í hverri línu fyrir vöru sem hefur verið gegnið frá, að hluta eða fullu, fyllir starfsmaður í vöruhúsi út reitinn **Magn** og skráir svo birgðafráganginn. Upprunaskjöl sem tengjast birgðafrágangi eru bókuð sem móttekin.  

Jákvæðar birgðahöfuðbókarfærslur eru stofnaðar, vöruhúsafærslur eru stofnaðar og frágangsbeiðni er eytt, ef hún er að fullu meðhöndluð. Til dæmis reiturinn **Móttekið magn** á upprunaskjallínu á innleið er uppfærður. Bókað móttökuskjal er stofnað til að til dæmis endurspegla innkaupapöntunina og mótteknar vörur.  

## <a name="advanced-warehouse-configurations"></a>Grunngerðir í ítarlegu vöruhúsi  
Eftirfarandi skýringarmynd sýnir innflæði í vöruhús eftir skjalagerð í grunngerð ítarlegs vöruhúss. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

![Flæði á innleið í ítarlegum skilgreiningum vöruhúss.](media/design_details_warehouse_management_inbound_advanced_flow.png "Flæði á innleið í grunngerð ítarlegs vöruhúss")  

### <a name="1-release-source-document"></a>1: Upprunaskjal losunar  
Þegar vörur berast í vöruhús, gefur notandi sem er ábyrgur fyrir móttöku út upprunaskjaliið, svo sem innkaupapöntun eða flutningspöntun á innleið, til að láta starfsmenn í vöruhúsi vita að mótteknar vörur megi ganga frá í birgðum.  

### <a name="2-create-inbound-request"></a>2: Stofna innleiðarbeiðni  
Þegar upprunaskjal á innleið er losað er stofnuð sjálfkrafa stofnuð vöruhúsabeiðni á innleið. Það inniheldur tilvísanir til upprunaskjalstegund og númeri og er ekki sýnilegt notandanum.  

### <a name="3-create-warehouse-receipt"></a>3: Stofna vöruhúsamóttöku  
Á síðunni **Vöruhúsamóttaka** sækir notandi sem er ábyrgur fyrir móttöku væntanlegra upprunaskjalalína byggt á vöruhúsabeiðnum á innleið. Margar línurnar úr upprunaskjölunum er hægt að sameina í eitt Vöruhúsamóttökuskjal.  

Notandinn fyllir út **Magn til afgreiðslu** reitinn og velur móttökusvæðið og hólf, ef nauðsynlegt er.  

### <a name="4-post-warehouse-receipt"></a>4: Bóka vöruhúsamóttöku  
Notandinn bókar vöruhúsamóttökuna. Jákvæðar birgðafærslur eru stofnaðar. Til dæmis reiturinn **Móttekið magn** á upprunaskjallínu á innleið er uppfærður.  

### <a name="5-create-warehouse-internal-put-away"></a>5: Innanhússfrágangar vöruhúss - framleiðsla  
Notandinn sem er ábyrgur fyrir frágangi úr innri virkni stofnar innri frágang vöruhússins fyrir vörur sem ganga þarf frá í vöruhúsinu, s.s. vöru eða samsetningarúttak. Notandinn tilgreinir magn, svæði og hólf þar sem frágangur fer fram, hugsanlega með aðgerðinni **Sækja innihald hólfs**. Notandinn losar innri frágang vöruhússins, sem stofnar innbundna vöruhúsabeiðni þannig að hægt er að sækja verkið í frágangsskjölum vöruhússins eða í frágangsvinnublaðinu.  

### <a name="6-create-put-away-request"></a>6: Stofna frágangsbeiðni  
Þegar upprunaskjal á innleið er bókað er stofnuð sjálfkrafa beiðni um frágang í vöruhúsi. Það inniheldur tilvísanir til upprunaskjalstegund og númeri og er ekki sýnilegt notandanum. Eftir uppsetningu, framleiðsla úr framleiðslupöntun skapar einnig frágangsbeiðni til að setja fullunnar vörur burtu í birgðum.  

### <a name="7-generate-put-away-worksheet-lines-optional"></a>7: Mynda frágangsvinnublaðslínur (valkvæmt)  
Notandinn sem er ábyrgur fyrir samræmingu frágangs sækir frágangslínur vöruhúss í **Birgðafrágangur vinnublað** byggt á bókuðum innhreyfingum vöruhúss eða innri virkni með úttaki. Notandinn velur línurnar sem á að ganga frá og undirbýr fráganginn með því að tilgreina úr hvaða hólfum á að taka, í hvaða hólf á að setja og hversu margar einingar á að meðhöndla. Hólf er hægt að forskilgreina í uppsetningu vöruhússstaðsetningar eða vinnslutilfanga.  

Þegar allur frágangur er bókaður og úthluta á vöruhúsastarfsmenn notandinn býr til frágangsskjöl vöruhús. Fullúthlutaðar frágangslínum er eytt úr **Birgðafrágangur vinnublað**.  

> [!NOTE]  
>  Ef reiturinn **Nota Birgðafrágangur vinnublað** er ekki valinn á staðsetningarkortinu eru frágangsskjöl vöruhúss búin til beint á grunni bókaðra vöruhúsamóttakna. Í því tilfelli, er skref 7 sleppt.  

### <a name="8-create-warehouse-put-away-document"></a>8: Stofna frágangsskjal vöruhúss  
Starfsmaður í vöruhúsi sem sér um frágang stofnar frágangsskjal vöruhúss, af gerðinni tínslur, byggt á bókaðri innhreyfingu vöruhúss. Að öðrum kosti er vöruhússfrágangsskjalið stofnað og úthlutað á starfsmann í vöruhúsi með ýtingu.  

### <a name="9-register-warehouse-put-away"></a>9: Skrá frágang í vöruhúsi  
Í hverri línu fyrir vöru sem hefur verið gegnið frá, að hluta eða fullu, fyllir starfsmaður í vöruhúsi út reitinn **Magn** á síðunni **Vöruhúsafrágangur** og skráir svo vöruhúsfráganginn.  

Vöruhúsafærslur eru búnar til og vöruhúsafrágangslínum eytt, ef að fullu meðhöndlaðar. Frágangsskjal vöruhúss er opið þar til allt magn tengdrar móttöku vöruhúss er skráð. Reiturinn **Magn frágangur** á pöntunarlínum vöruhúsamóttöku er uppfærður.  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]