---
title: "Kynning - Framkvæmd söluherferðar | Microsoft Docs"
description: "Herferð er hver sú aðgerð sem hefur með marga tengiliði að gera. Mikilvægur þáttur í uppsetningu herferðar hefur með val á markhópi hennar að gera. Í þessum tilgangi í [!INCLUDE[d365fin](includes/d365fin_md.md)], er búinn til í  hluti eða hópur tengiliða með afmörkunum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e9eb96fb0f9669a9ddac5e4ea6e973fd64388b87
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Kynning: Framkvæmd söluherferðar
Herferð er hver sú aðgerð sem hefur með marga tengiliði að gera. Mikilvægur þáttur í uppsetningu herferðar hefur með val á markhópi hennar að gera. Í þessum tilgangi er búinn til í [!INCLUDE[d365fin](includes/d365fin_md.md)] hluti eða hópur tengiliða með afmörkunum.  

 Þetta er notað í Sölu og markaðssetningu til að skipuleggja markaðsaðgerðir nákvæmlega og til að vinna með samskipti við tengiliði og viðskiptamenn. Hægt er að stofna herferðir og setja upp hluta tengiliða á póstlista og aðrar gerðir samskipta við tengiliði og hugsanlega viðskiptamenn.  

 Valkostirnir Herferð og Hluti, og sjálfvirkar vinnslur þeirra, gera notandanum kleift að áætla, skipuleggja og rekja markaðssetningu. Þetta eykur líkurnar á að ná í nýja viðskiptamenn og að halda gömlum viðskiptamönnum.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
 Þessi kynning sýnir ferlið á bak við eftirfylgni við sölusýningu og miðun á hugsanlega viðskiptamenn (tengiliði) í eftirfylgniherferðinni.  

 Í kynningunni eru herferðar- og hlutavalkostirnir í Sölu og markaðssetningu kynntir. Þessi kynning fjallar um eftirfarandi verk:  

-   Uppsetning herferðar.  
-   Val á markhópi.  
-   Gagnaskoðun.  
-   Bréfasendingar til tengiliða.  
-   Skráning svara við herferð.  

## <a name="roles"></a>Hlutverk  
 Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

-   Markaðs- eða sölustjóri  
-   Starfsmaður markaðsdeildar  

## <a name="prerequisites"></a>Frumskilyrði  
 Áður en hægt er að framkvæma verk hér í kynningunni þarf að setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="story"></a>Ferill  
 Markaðsstjóri söludeildar CRONUS Ísland hf. er ábyrgur fyrir skipulagningu og framkvæmd herferða. Hann tekur einnig ákvarðanir um hvaða sölusýningum á að taka þátt í, auk þess að meta framvindu herferða.  

 Starfsmaður markaðsdeildarinnar sér um framleiðslu, dreifingu og birtingu markaðsefnis.  

 Fyrirtækið er nýbúið að setja á markað nýja vöru sem er kölluð Millennium Server. Varan var nýlega kynnt á sölusýningunni Computer Futurus. Margir viðskiptamenn sýndu vörunni mikinn áhuga og í kynningarherferð var viðskiptamönnum boðin varan á sérstöku kynningarherferðarverði.  

 Eitt af verkefnum starfsmanns markaðsdeildar eftir sölusýninguna er að færa alla hugsanlega viðskiptamenn sem tengiliði.  

 Markaðsstjórinn setur upp herferð, stofnar hluta sem inniheldur alla nýju tengiliðina og skoðar gögn um þá til að velja markhóp herferðarinnar.  

 Starfsmaðurinn sendir út þakkarbréf til allra tengiliða sem skildu eftir nafnspjald á sölubásnum og markaðsstjórinn skráir öll svör sem hugsanlegir viðskiptamenn senda.  

## <a name="setting-up-a-campaign"></a>Uppsetning herferðar  
 Þegar starfsmaðurinn hefur slegið inn upplýsingar af nafnspjöldunum sem söfnuðust á sölusýningunni setur markaðsstjórinn upp herferðarspjald til að vinna með herferðina.  

### <a name="to-set-up-a-campaign"></a>Uppsetning herferðar  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Herferðir** og velja svo viðeigandi tengil.  
2.  Til að búa til nýja herferð skal velja aðgerðina **Nýtt**. Á söluherferðarspjaldinu er stutt á Færslulykilinn til að söluherferðarnúmer verði sjálfkrafa sett inn.  
3.  Í reitinn **Lýsing** er færð inn lýsing á herferðinni, t.d. **FUTURUS - sölusýning**.  
4.  Veldu reitinn **Stöðukóti** og veldu stöðukóta af listanum sem opnast í glugganum **Staða söluherferðar**.  
5.  Reitirnir **Upphafsdags.** og **Lokadags.** í herferðinni eru fylltir út eins og með þarf.  

## <a name="selecting-the-target-audience"></a>Val á markhópi  
 Markaðsstjórinn stofnar hluta til að velja tengiliði sem hafa á samskipti við.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Stofnun hluta með viðeigandi tengiliðum  

1.  Skal velja **Hluti** aðgerð.  
2.  Til að búa til nýjan hluta skal velja aðgerðina **Nýtt**. Á hlutaspjaldinu er stutt á Færslulykilinn til að hlutanúmer verði sjálfkrafa sett inn.  
3.  Í flýtiflipann **Almennt** í reitnum **Lýsing** er t.d. skrifað **Gestir á sölusýningunni FUTURUS**.  

     Þegar almennar upplýsingar um hlutann hafa verið færðar inn eru tengiliðir valdir fyrir hann.  

     Hægt er að velja þá eftir ýmsum skilyrðum, t.d. tengiliði sem vinna við innkaup hjá fyrirtæki viðskiptamanns eða hugsanlegs viðskiptamanns.  

     Afmarkanir eru notaðar til að bæta við tengiliðum samkvæmt þeim skilyrðunum sem best henta. T.d er hægt að velja að afmarka við ábyrgðarstöðu tengiliðar, viðskiptatengsl tengiliðarfyrirtækisins eða iðnaðinn sem það tilheyrir. Í þessari kynningu er afmörkunin **Starfsábyrgð** valin til að velja tengiliði.  

4.  Í glugganum **Hluti** skal velja **Bæta við tengiliðum** aðgerðina til að opna **Bæta við tengiliðum** afmörkunina.  
5.  Á flýtiflipanum **Starfsábyrgð** er afmörkunin **Innkaup** valin sem **Starfsábyrgðarkóti** og svo er smellt á **Í lagi**.  

     Glugginn **Hluti** inniheldur nú lista yfir tengiliði sem valdir voru samkvæmt valinni afmörkun. Á flýtifliðanum **Almennt** í reitnum **Fjöldi lína** er hægt að skoða á einu augabraði fjölda tengiliða sem uppfylla þessi skilyrði.  

    > [!NOTE]  
    >  Hægt er að vista hlutaskilyrði til notkunar síðar.

    1.  Í glugganum **Hluti** skal velja aðgerðina **Hluti** og síðan velja aðgerðina **Vista skilyrði**.  
    2.  Í glugganum **Vista hlutaskilyrði** er færður inn kóti fyrir hlutann. Í reitinn **Lýsing** er færð inn lýsing á hlutaskilyrðunum.
    3.  Velja hnappinn **Í lagi**.  

## <a name="mining-the-data"></a>Gagnaskoðun  
 Markaðsstjórinn skoðar hlutaða tengiliðalistann betur og áttar sig á því að hann er alltof langur. Hann ákveður að grisja listann niður í raunverulega hugsanlega viðskiptamenn til að miðað sé á réttan markhóp. Þetta ferli endurskoðunar og samdráttar á gögnum er einnig kallað gagnaskoðun.  

### <a name="to-remove-contacts-from-the-segment"></a>Tengiliðir fjarlægðir úr hluta  

1.  Í glugganum **Hluti** skal velja aðgerðina **Tengiliðir** og síðan velja aðgerðina **Fækka tengiliðum** til að opna gluggann **Eyða tengiliðum - Fækka**.  
2.  Á flýtiflipanum **Viðskiptatengsl** er afmörkunin **VIÐF** valin sem **Viðskiptatengslakóti** og svo er hnappurinn **Í lagi** valinn.  

     Glugginn **Hluti** inniheldur nú styttan lista yfir tengiliði og í reitnum **Fjöldi lína** er hægt að sjá fjölda tengiliða sem uppfyllir nýju skilyrðin.  

    > [!NOTE]  
    >  Ef það þarf að afturkalla þessa fækkun á tengiliðum er aðgerðin **Til baka** valin. Með öðrum orðum er hægt að afturkalla síðustu hlutun.  
    >   
    >  Í glugganum **Hluti** skal velja aðgerðina **Hluti** og síðan velja aðgerðina **Fara til baka**.  
    >   
    >  Tengiliðunum sem voru rétt í þessu fjarlægðir er aftur bætt á tengiliðalistann.  

## <a name="linking-a-segment-to-a-campaign"></a>Hluti tengdur við herferð  
 Markaðsstjórinn ákveður að ekki þurfi að stytta listann frekar, á honum séu þeir tengiliðir sem henta herferðinni. Næsta skref er því að tengja þennan hluta við herferðina FUTURUS - sölusýning.  

### <a name="to-link-a-segment-to-the-campaign"></a>Tenging hluta við herferð  

1.  Í glugganum **Hluti** á flýtiflipanum **Herferð** er reiturinn **Herferð**  valinn til að velja herferðina sem tengja á við hlutann, t.d. **CP0001**.  
2.  Þar sem hlutinn er markhópur herferðarinnar er gátreiturinn **Markhópur söluherferðar** valinn.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Sending bréfa og tölvupósts til tengiliða  
 Starfsmaður markaðssetningar aðstoðar markaðsstjórann við að senda út bréf til mögulegra viðskiptamanna, þar sem þeim er þakkað fyrir heimsóknina á sölusýningunni.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Til að nota hluta til að senda bréf á tengilið  

1.  Spjaldið **Hluti** er opnað fyrir **Gestir á sölusýningunni FUTURUS**.  
2.  Á flýtiflipanum **Samskipti** í reitnum **Kóti samskiptasniðmáts** er sniðmátið Viðskiptabréf, kóti **FBR** valið.  
3.  Í reitinn **Efni (sjálfgefið)** skal slá inn eftirfarandi textadæmi: **Takk fyrir heimsóknina á sölusýningunni**.  

    > [!NOTE]  
    >  Þetta sniðmát er tengt fleiri en einu viðhengdu skjali, sem hvert fyrir sig er skrifað á mismunandi tungumáli. Tungumál í þessu dæmi eru m.a. enska og danska.  

4.  Velja reitinn **Tungumálakóti (sjálfgefinn)** til að opna gluggann **Tungumál hlutasamskipta**. Veljið tungumálakóta og smellið á hnappinn **Í lagi**.  
5.  Hægt er að birta skjalið á völdu tungumáli. Veljið aðgerðina **Viðhengi** og svo aðgerðina **Opna**.  

     Til að bregðast við þessum boðum sem biðja um leyfi til að ræsa Word skal velja valkostinn **Leyfa fyrir þessa biðlarasetu**.  

     Við það opnast tengda Word skjalið svo hægt sé að skoða það. Einnig er hægt að nota tækifærið til að breyta og breyta stafnum. Loka Word þegar því er lokið.  

6.  Efni bréfsins er fært inn í reitinn **Efni** á því tungumáli sem er valið fyrir sniðmátið.  
7.  Veldu aðgerðina **kladdi**.
8.  Velja gátreitinn **Senda viðhengi** til að láta prenta viðhengin.  

    1. Velja gátreitinn **Stofna eftirfylgnihluta**.  
    2. Velja hnappinn **Í lagi** til að hefja runuvinnsluna **Skrá hluta**.  

9. Viðhengi hafa verið send. Þegar ferlinu er lokið skal velja hnappinn **Í lagi** fyrir skilaboðin sem tilkynna að hlutinn hafi verið skráður.  

     Bókstafir eru sjálfkrafa prentaðir og hlutinn er skráður. Þar sem hlutinn hefur verið skráður, er hann ekki lengur í lista yfir hluti en er fluttur í lista yfir skráða hluti. Til að sjá þann lista, velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Skráðir Hlutar** og velja svo viðeigandi tengil.  

10. Eftir að hlutinn er skráður, er hvert bréf sem er sent skráð sem samskipti, sem sjá má í kladdanum.  

     Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Samskiptaskrá færslur** og velja svo viðeigandi tengil. Til er færsla fyrir hvern sendan staf.  

### <a name="to-send-an-email-message-to-a-contact"></a>Til að senda tölvupóstskeyti á tengilið  

1.  Á flýtiflipanum **Samskipti** í reitnum **Kóti samskiptasniðmáts** er sniðmátið Viðskiptabréf, kóti **FBR** valið.  
2.  Í reitinn **Efni (sjálfgefið)** skal slá inn eftirfarandi textadæmi: **Takk fyrir heimsóknina á sölusýningunni**.  
3.  Í reitnum **Tegund samskipta** veljið **Tölvupóstur**.  
4.  Tilgreinið tungumálastillingar eins og í síðustu aðgerð.  
5.  Veldu aðgerðina **kladdi**. Glugginn **Skrá hluta** opnast.  
6.  Velja gátreitinn **Senda viðhengi** til að láta senda viðhengin í tölvupósti.  
7.  Velja gátreitinn **Stofna eftirfylgnihluta**.  
8.  Velja hnappinn **Í lagi**.  

     Bókstafir eru sjálfkrafa sendir með tölvupósti og hlutinn er skráður. Þar sem hlutinn hefur verið skráður, er hann ekki lengur í lista yfir hluti en er vistaður í lista yfir skráða hluti. Til að sjá þann lista, velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Skráðir Hlutar** og velja svo viðeigandi tengil.  

## <a name="registering-campaign-responses"></a>Skráning svara við herferð  
 Næstu vikur svara hugsanlegir viðskiptamenn bréfinu. Markaðsstjórinn vill fylgjast með svörunum og skrá samskiptin.  

 Til þess er settur upp hluti fyrir þá tengiliði sem hafa svarað bréfinu.  

### <a name="to-register-campaign-responses"></a>Skráning svara við herferð  

1.  Í glugganum **Hluti** skal stækka flýtiflipann **Samskipti**  
2.  Velja reitinn **Kóti samskiptasniðmáts**.  

     Það er ekki til samskiptasniðmát fyrir skráningu svara við herferð. Því skal búa til nýtt sniðmát.  

3.  Í glugganum **Samskiptasniðmát** skal velja aðgerðina **Nýtt**.  
4.  Í reitinn **Kóti** er **SVÖR** fært inn og í reitinn **Lýsing** er **Svör við herferð** fært inn.  
5.  Velja hnappinn **Í lagi**.  
6.  Þetta samskiptasniðmát er valið í reitnum **Kóti samskiptasniðmáts** og skilaboðin sem spyrja hvort uppfæra eigi hlutalínurnar með sama kóta samskiptasniðmáts eru samþykkt.  

     Nú er hægt að tilgreina að þessir tengiliðir hafi svarað herferðinni:  
7.  Á flýtiflipanum **Söluherferð** á reitnum **Söluherferð nr.** , veljið söluherferðina.  
8.  Yfirgefðu **Söluherferð nr.** og skilaboðin sem spyrja hvort uppfæra eigi hlutalínurnar með sama kóða samskiptasniðmáts eru samþykkt.  
9. Reiturinn **Svörun söluherferðar** er valinn og fylgjandi skilaboð samþykkt.  

     Hlutinn er skráður til að tryggja að samskiptin séu skráð.  
10. Í glugganum **Hluti** veldu aðgerðina **kladdi**.  
11. Í glugganum **Skrá hluta** er gátreiturinn **Senda viðhengi** afvalinn og svo er hnappurinn **Í lagi** valinn og skilaboðin sem fylgja samþykkt.  

     Um leið og hlutinn er skráður er sjálfkrafa stofnuð færsla fyrir herferðina til að skrá þessa aðgerð í gluggann **Söluherferðarfærslur**.  

## <a name="see-also"></a>Sjá einnig  
[Umsjón með venslum](marketing-relationship-management.md)  
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

