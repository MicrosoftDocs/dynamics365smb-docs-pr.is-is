---
title: 'Kynning: Framkvæmd söluherferðar'
description: Herferð er hver sú aðgerð sem hefur með marga tengiliði að gera. Mikilvægur þáttur í uppsetningu herferðar hefur með val á markhópi hennar að gera. Í þessum tilgangi er búinn til í Business Central hluti eða hópur tengiliða með afmörkunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/25/2021
ms.author: edupont
ms.openlocfilehash: 653638cd056313c6f4bdb830f0b0ec32fa5e8cbf
ms.sourcegitcommit: cce6bacca46d489423a9538d410d2d9371de0ddf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102434"
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Kynning: Framkvæmd söluherferðar

Herferð er hver sú aðgerð sem hefur með marga tengiliði að gera. Mikilvægur þáttur í uppsetningu herferðar hefur með val á markhópi hennar að gera. Í þessum tilgangi er búinn til í [!INCLUDE[prod_short](includes/prod_short.md)] hluti eða hópur tengiliða með afmörkunum.  

 Þetta er notað í Sölu og markaðssetningu til að skipuleggja markaðsaðgerðir nákvæmlega og til að vinna með samskipti við tengiliði og viðskiptamenn. Hægt er að stofna herferðir og setja upp hluta tengiliða á póstlista og aðrar gerðir samskipta við tengiliði og hugsanlega viðskiptamenn.  

 Valkostirnir Herferð og Hluti, og sjálfvirkar vinnslur þeirra, gera notandanum kleift að áætla, skipuleggja og rekja markaðssetningu. Þetta eykur líkurnar á að ná í nýja viðskiptamenn og að halda gömlum viðskiptamönnum.  

## <a name="about-this-walkthrough"></a>Um kynninguna

 Þessi kynning sýnir ferlið á bak við eftirfylgni við sölusýningu og miðun á hugsanlega viðskiptamenn (tengiliði) í eftirfylgniherferðinni.  

 Í kynningunni eru herferðar- og hlutavalkostirnir í Sölu og markaðssetningu kynntir. Þessi kynning fjallar um eftirfarandi verk:  

- Gögnin undirbúin.
- Uppsetning herferðar.  
- Val á markhópi.  
- Gagnaskoðun.  
- Bréfasendingar til tengiliða.  
- Skráning svara við herferð.  

## <a name="roles"></a>Hlutverk

 Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Markaðs- eða sölustjóri  
- Starfsmaður markaðsdeildar  

## <a name="prerequisites"></a>Frumskilyrði

 Áður en hægt er að framkvæma verk hér í kynningunni þarf að setja upp [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="story"></a>Ferill

 Markaðsstjóri söludeildar CRONUS er ábyrgur fyrir skipulagningu og framkvæmd herferða. Hann tekur einnig ákvarðanir um hvaða sölusýningum á að taka þátt í, auk þess að meta framvindu herferða.  

 Starfsmaður markaðsdeildarinnar sér um framleiðslu, dreifingu og birtingu markaðsefnis.  

 Fyrirtækið er nýbúið að setja á markað nýja vöru sem er kölluð Rome Guest Chair. Varan var nýlega kynnt á sölusýningunni Office Futurus. Margir viðskiptamenn sýndu vörunni mikinn áhuga og í kynningarherferð var viðskiptamönnum boðin Rome Guest Chair varan á sérstöku kynningarherferðarverði.  

 Eitt af verkefnum starfsmanns markaðsdeildar eftir sölusýninguna er að færa alla hugsanlega viðskiptamenn sem tengiliði.  

 Markaðsstjórinn setur upp herferð, stofnar hluta sem inniheldur alla nýju tengiliðina og skoðar gögn um þá til að velja markhóp herferðarinnar.  

 Starfsmaðurinn sendir út þakkarbréf til allra tengiliða sem skildu eftir nafnspjald á sölubásnum og markaðsstjórinn skráir öll svör sem hugsanlegir viðskiptamenn senda.  

## <a name="setting-up-a-campaign"></a>Uppsetning herferðar

 Þegar starfsmaðurinn hefur slegið inn upplýsingar af nafnspjöldunum sem söfnuðust á sölusýningunni setur markaðsstjórinn upp herferðarspjald til að vinna með herferðina.  

### <a name="to-set-up-a-campaign"></a>Uppsetning herferðar  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Herferðir** og veldu síðan tengda tengilinn.  
2. Til að búa til nýja herferð skal velja aðgerðina **Nýtt**. Á söluherferðarspjaldinu er stutt á **Færslulykilinn** til að söluherferðarnúmer verði sjálfkrafa sett inn.  
3. Í reitinn **Lýsing** er færð inn lýsing á herferðinni, t.d. **Office Futurus - sölusýning**.  
4. Veljið reitinn **Stöðukóði** og veljið stöðukóðann „1-PLAN“. 
5. Reitirnir **Upphafsdags.** og **Lokadags.** í herferðinni eru fylltir út eins og með þarf.  

## <a name="selecting-the-target-audience"></a>Val á markhópi

 Markaðsstjórinn stofnar hluta til að velja tengiliðina sem hann vill hafa samskipti við.  
 
 Þegar hluti er stofnaður er hægt að nota ýmis viðmið til að velja tengiliðina sem verða að vera markmið hlutans. Til dæmis er hægt að velja tengiliði sem vinna við innkaup hjá fyrirtæki viðskiptamanns eða hugsanlegs viðskiptamanns. Afmarkanir eru notaðar til að bæta við tengiliðum samkvæmt þeim skilyrðunum sem best henta. T.d er hægt að velja að afmarka við ábyrgðarstöðu tengiliðar, viðskiptatengsl tengiliðarfyrirtækisins eða iðnaðinn sem það tilheyrir. Í þessari kynningu er afmörkunin **Starfsábyrgð** valin til að velja tengiliði.

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Stofnun hluta með viðeigandi tengiliðum  

1. Veljið aðgerðina **Skoða** og velja svo **Hlutar**.  
2. Til að búa til nýjan hluta skal velja aðgerðina **Nýtt**. Á hlutaspjaldinu er **Færslulykilinn** valinn til að hlutanúmer verði sjálfkrafa sett inn.  
3. Í flýtiflipann **Almennt** í reitnum **Lýsing** er t.d. skrifað *Gestir á Office Futurus sölusýningunni*.
4. Veljið **Bæta við tengiliðum** aðgerðina til að opna **Bæta við tengiliðum** afmörkunina.  
5. Flettið niður að **Starfsábyrgð tengiliðar** er afmörkunin **Innkaup** valin sem **Starfsábyrgðarkóti** og svo er smellt á **Í lagi**.  

Síðan **Hluti** inniheldur nú lista yfir tengiliði sem valdir voru samkvæmt valinni afmörkun. Á flýtifliðanum **Almennt** í reitnum **Fjöldi lína** er hægt að skoða á einu augabraði fjölda tengiliða sem uppfylla þessi skilyrði.  

> [!NOTE]  
> Hægt er að vista hlutaskilyrði til notkunar síðar.

### <a name="to-save-your-segmentation-criteria"></a>Til að vista hlutaviðmiðin

1. Á síðunni **Hluti** skal velja **Aðgerðir**.
2. Veldu **Aðgerðir**, síðan **Hluti** og síðan aðgerðina **Vista skilyrði**.  
3. Á síðunni **Vista hlutaskilyrði** er færður inn kóti fyrir hlutann. Í reitinn **Lýsing** er færð inn lýsing á hlutaskilyrðunum.
4. Velja hnappinn **Í lagi**.  

## <a name="mining-the-data"></a>Gagnaskoðun

 Markaðsstjórinn skoðar hlutaða tengiliðalistann betur og áttar sig á því að hann er alltof langur. Hann ákveður að grisja listann niður í raunverulega hugsanlega viðskiptamenn til að miðað sé á réttan markhóp. Þetta ferli endurskoðunar og samdráttar á gögnum er einnig kallað gagnaskoðun.  

### <a name="to-remove-contacts-from-the-segment"></a>Tengiliðir fjarlægðir úr hluta  

1. Á síðunni **Hluti** skal velja **Aðgerðir**.
2. Í valmyndastikunni hér að neðan skal velja **Aðgerðir**, velja **Tengiliðir** og svo **Fækka tengiliðum**.  

  Glugginn **Fjarlægja tengiliði – Fækka** opnast.  
4. Á flýtiflipanum **Viðskiptatengsl tengiliðar** er afmörkunin **SÉRS** valin sem **Viðskiptatengslakóti** og svo er hnappurinn **Í lagi** valinn.

 Síðan **Hluti** inniheldur nú styttan lista yfir tengiliði og í reitnum **Fjöldi lína** er hægt að sjá fjölda tengiliða sem uppfyllir nýju skilyrðin.  

 > [!NOTE]  
 > Ef það þarf að afturkalla þessa fækkun á tengiliðum er aðgerðin **Til baka** valin. Með öðrum orðum er hægt að afturkalla síðustu hlutun.  

### <a name="to-bring-back-the-removed-contacts"></a>Til að sækja fjarlægða tengiliði

1. Á síðunni **Hluti** skal velja aðgerðina **Hluti**.
2. Veljið aðgerðina **Til baka**.

Tengiliðunum sem voru rétt í þessu fjarlægðir er aftur bætt á tengiliðalistann.

## <a name="linking-a-segment-to-a-campaign"></a>Hluti tengdur við herferð

Markaðsstjórinn ákveður að ekki þurfi að stytta listann frekar þar sem hann inniheldur þá tengiliði sem henta herferðinni. Því tengir hann þennan hluta við herferðina FUTURUS - sölusýning.  

### <a name="to-link-a-segment-to-the-campaign"></a>Tenging hluta við herferð  

1. Á síðunni **Hluti** á flýtiflipanum **Herferð** er reiturinn **Herferð** valinn til að velja herferðina sem tengja á við hlutann, t.d. **CP0001**.
2. Velja skal **Já**.  
3. Þar sem hlutinn er markhópur herferðarinnar er gátreiturinn **Markhópur söluherferðar** valinn og svo **Já**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Sending bréfa og tölvupósts til tengiliða

 Starfsmaður markaðssetningar aðstoðar markaðsstjórann við að senda út bréf til mögulegra viðskiptamanna, þar sem þeim er þakkað fyrir heimsóknina á sölusýningunni.

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Til að nota hluta til að senda bréf á tengilið  

> [!NOTE]  
> Í þessari aðferð þarftu að hengja við Word-skjal. Þú getur bætt við viðhengjum á hvaða tungumáli sem er.

> [!NOTE]  
> Smelltu á táknið **Breyta blýanti** til að opna síðuna í breytingastillingu ef þörf krefur.

1. Spjaldið **Hluti** er opnað fyrir **Gestir á sölusýningunni FUTURUS**.  
2. Á flýtiflipanum **Samskipti** í reitnum **Kóði samskiptasniðmáts** er sniðmátið Viðskiptabréf, kóði **VIÐ** valinn og svo **Já**.
3. Velja reitinn **Tungumálakóði sjálfgefinn** til að opna síðuna **Tungumál hlutasamskipta**. Veljið **Tungumálakóði** og smellið á hnappinn **Í lagi**.
4. Ganga þarf úr skugga um að **Tegund samskipta (sjálfgildi)** sé stillt á **Sendibréf**.
5. Í **Viðhengi** reitnum velurðu reitinn **Úrfellingarmerki**. Þetta opnar skjámyndina Flytja inn viðhengi.
    1. Veldu **Velja** hnappinn til að velja skrána þína.
    1. Finndu skrána og veldu hnappinn **Opna** til að hengja hana við.
6. Í reitinn **Efni (sjálfgefið)** skal slá inn eftirfarandi textadæmi: **Takk fyrir heimsóknina á sölusýningunni**. Ýttu á dálkalykilinn til að yfirgefa reitinn og veldu hnappinn **Já**.
7. Renndu **Senda Word-skjöl sem viðhengi** á kveikt og veldu hnappinn **Já**.
8. Velu aðgerina **Kladdi**. Í sprettiglugganum fyrir Skrá hluta er virkjað: **Stofna eftirfylgnihluta**
9. Velja hnappinn **Í lagi** til að hefja **Skrá hluta runuvinnsluna**.  

Viðhengi hafa verið send. Þegar ferlinu er lokið skal velja hnappinn **Í lagi** fyrir skilaboðin sem tilkynna að hlutinn hafi verið skráður.  

 Bókstafir eru sjálfkrafa prentaðir og hlutinn er skráður. Þar sem hlutinn hefur verið skráður, er hann ekki lengur í lista yfir hluti en er fluttur í lista yfir skráða hluti. Til að sjá þann lista velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera")táknið, sláðu inn **Skráðir hlutar** og veldu síðan tengda tengilinn.  

Eftir að hlutinn er skráður, er hvert bréf sem er sent skráð sem samskipti, sem sjá má í kladdanum.  

Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslur í samskiptaskráningu** og veldu síðan tengda tengilinn. Til er færsla fyrir hvern sendan staf.  

### <a name="to-send-an-email-message-to-a-contact"></a>Til að senda tölvupóstskeyti á tengilið  

1. Á flýtiflipanum **Samskipti** í reitnum **Kóti samskiptasniðmáts** er sniðmátið Viðskiptabréf, kóti **FBR** valið.  
2. Í reitinn **Efni (sjálfgefið)** skal slá inn eftirfarandi textadæmi: **Takk fyrir heimsóknina á sölusýningunni**.  
3. Í reitnum **Tegund samskipta** veljið **Tölvupóstur**.  
4. Tilgreinið tungumálastillingar og hengið Word-skjal við eins og í síðustu aðgerð.  
5. Veldu aðgerðina **kladdi**. Síðan **Skrá hluta** opnast.  
6. Velja gátreitinn **Senda viðhengi** til að láta senda viðhengin í tölvupósti.  
7. Velja gátreitinn **Stofna eftirfylgnihluta**.  
8. Velja hnappinn **Í lagi**.  

 Bókstafir eru sjálfkrafa sendir með tölvupósti og hlutinn er skráður. Þar sem hlutinn hefur verið skráður, er hann ekki lengur í lista yfir hluti en er vistaður í lista yfir skráða hluti. Til að sjá þann lista velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skráðir hlutar** og veldu síðan tengda tengilinn.  

## <a name="registering-campaign-responses"></a>Skráning svara við herferð

 Næstu vikur svara hugsanlegir viðskiptamenn bréfinu. Markaðsstjórinn vill fylgjast með svörunum og skrá samskiptin.  

 Til þess er settur upp hluti fyrir þá tengiliði sem hafa svarað bréfinu.  

### <a name="to-register-campaign-responses"></a>Skráning svara við herferð  

1. Á síðunni **Hluti** á flýtiflipanum **Samskipti** er reiturinn **Kóði samskiptasniðmáts** valinn.  

 Það er ekki til samskiptasniðmát fyrir skráningu svara við herferð. Því skal búa til nýtt sniðmát.  

2. Á fellilistanum **Samskiptasniðmát** skaltu velja aðgerðina **Nýtt**.  
3. Í reitinn **Kóti** er **SVÖR** fært inn og í reitinn **Lýsing** er **Svör við herferð** fært inn.  
4. Velja hnappinn **Í lagi**.
5. Veldu **Já** til að staðfesta að nota eigi þetta samskiptasniðmát fyrir allar hlutalínur.
6. Á flýtiflipanum **Söluherferð** skaltu velja reitinn **Svörun söluherferðar**. Veldu **Já** til að staðfesta skilaboðin *Þú hefur breytt svörun söluherferðar*.  
7. Á síðunni **Hluti** skal velja aðgerðina **Skrá**.  
8. Á síðunni **Skrá hluta** er gátreiturinn **Senda viðhengi** afvalinn. Veldu svo hnappinn **Í lagi** til að staðfesta skilaboðin um að hluti hafi verið skráður.  
  
## <a name="see-also"></a>Sjá einnig  
[Umsjón með venslum](marketing-relationship-management.md)  
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
