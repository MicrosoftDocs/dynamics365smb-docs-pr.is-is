---
title: Notkun viðbótar fyrir Myndgreinanda | Microsoft Docs
description: Viðbótin gerir þér kleift að greina myndir af tengiliðum og vörum til að finna eigindir, svo þú getir úthlutað þeim í Business Central á fljótlegan máta.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3957936f7a95ce493443ed86c791ebceee6b56b9
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757243"
---
# <a name="the-image-analyzer-extension"></a>Myndgreiningarviðbót

Viðbótin fyrir Myndgreinandann notar öflugar myndgreiningaraðferðir frá Tölvusjón API for Microsoft Cognitive Services til að greina eigindir á myndunum sem þú flytur inn fyrir vörur og tengiliði, svo þú getir auðveldlega endurskoðað þær og úthlutað þeim. Fyrir vörur, þá geta eigindir sagt til um hvort varan er borð eða bíll, og hvort hún er rauð eða blá. Fyrir tengiliði, þá geta eigindir verið kyn eða aldur.

Myndgreinandinn leggur til eigindir sem byggjast á merkjum sem Tölvusjón API finnur, og áreiðanleikastig. Greinandinn leggur að sjálfgefnu aðeins til eigindir ef 80% vissa, hið minnsta, er fyrir hendi um að eigindin sé rétt. Þú getur still inn annað áreiðanleikastig, ef þörf krefur. Til að læra meira um hvernig merki og áreiðanleikastig eru ákvörðuð, sjá [Tölvusjón API](https://go.microsoft.com/fwlink/?linkid=851476)  

Myndgreinandinn er ókeypis í [!INCLUDE[prod_short](includes/prod_short.md)], en það eru takmörk fyrir því hversu margar vörur þú getur greint yfir ákveðið tímabil. Að sjálfgefnu, geturðu greint 100 myndir á mánuði.

Eftir að þú virkjar viðbótina, keyrist Myndgreinandinn í hvert skipti sem þú flytur inn mynd til vöru eða tengiliðs. Um leið muntu sjá eigindirnar, áreiðanleikastigið og upplýsingarnar og getur ákveðið hvað skal gera við hverja eigind. Ef þú fluttir inn myndir áður en þú virkjaðir Myndgreinanda-viðbótina, þarftu að ná í vöruna eða tengiliðaspjaldið og velja **Greina mynd** aðgerðina.  

## <a name="privacy-notice"></a>Persónuverndaryfirlýsing

Þessi viðbót notar Tölvusjón API frá Microsoft Cognitive Services, sem kann að hafa mismunandi stig skuldbindingar um reglufylgni en [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar þú kveikir á Image Analyzer viðbótinni verða viðskiptamannagögn á borð við tengiliðamynd eða vörumynd send til Tölvusjónar API. Með því að setja upp þessa viðbót samþykkir þú að þetta takmarkaða gagnasafn verði sent til Tölvusjónar API. Athugaðu að þú getur slökkt á, sem og fjarlægt, Image Analyzer viðbótina hvenær sem er til að hætta að nota þessa virkni. Nánari upplýsingar, sjá [Microsoft Öryggismiðstöð](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Kröfur

Myndirnar þurfa að lúta nokkrum skilyrðum:

* Myndasnið: JPEG, PNG, GIF, BMP  
* Hámarks skráarstærð: Minna en 4 MB  
* Stærð myndar: Meira en 50 x 50 pixlar  

## <a name="to-enable-image-analyzer"></a>Að virkja Myndgreinandann

Viðbótin fyrir Myndgreinandann er innbyggð í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú þarft bara að kveikja á því.

> [!NOTE]  
> Aðeins kerfisstjóri getur virkjað viðbótina fyrir Myndgreinandann. Gakktu úr skugga um að þér sé úthlutað **Yfirnotandi** heimildarsamstæðu fyrir notanda.

1. Gert er eitt af eftirfarandi til að virkja viðbótina fyrir myndgreinandann:

* Vöru- eða tengiliðaspjald er opnað. Á tilkynningastikunni skal velja **Greina myndir**, og svo er skrefunum í Uppsetningu með aðstoð fylgt.  
* Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustutengingar** og veldu síðan **Uppsetning myndgreiningar**. Á gátreitnum skal velja **Virkja myndgreinanda**, og svo er skrefunum í Uppsetningu með aðstoð fylgt.  

    > [!TIP]  
    > Á **Uppsetning myndgreiningar** síðunni geturðu líka breytt áreiðanleikastiginu fyrir tillögur um eigindir. Ef þú vilt til dæmis auka áreiðanleikann, þá geturðu slegið inn hærri prósentu.

## <a name="to-analyze-an-image-of-an-item"></a>Að greina mynd af vöru

Eftirfarandi skref lýsa því hvernig skal greina mynd sem var flutt inn áður en þú virkjaðir viðbótina fyrir Myndgreinandann.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.  
2. Veljið vöruna og veljið svo aðgerðina **Greina mynd**.  
3. Síðan **Eigindir myndgreinanda** birtir þær eigindir sem finnast, áreiðanleikastigið og aðrar upplýsingar um eigindina. Nota **Aðgerð til að framkvæma** valkostina til að tilgreina hvað skal gera við eigindina.  

    > [!TIP]  
    > Þú getur bætt nafni eigindarinnar við lýsinguna á vörunni með því að velja **Bæta við vörulýsingu**. Þetta getur t.d. reynst gagnlegt þegar bæta þarf við upplýsingum snögglega.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Greina mynd af tengilið

Eftirfarandi skref lýsa því hvernig skal greina mynd sem var flutt inn áður en þú virkjaðir viðbótina fyrir Myndgreinandann.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn.  
2. Veljið tengiliðinn og veljið svo **Greina mynd** aðgerðina.  
3. Á flýtiflipanum **spurningarlisti fyrir notandasíðu**, skal endurskoða tillögur og leiðrétta ef þarf.  

## <a name="block-suggested-attributes"></a>Loka á eigindir sem mælt er með

Ef greiningin leggur til eigind sem þú vilt ekki sjá, geturðu lokað á þá eigind. Sýndu samt aðgát. Útilokaðar eigindir koma ekki fram í tillögum um aðrar vörur eða tengiliði heldur. Ef þú sérð eftir því að hafa lokað á eigind, geturðu valið **Skoða eigindir á svörtum lista** og svo eytt eigindinni úr listanum.

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Nota þinn eigin aðgang fyrir Tölvusjón API

Þú getur líka notað þinn eigin aðgang fyrir Tölvusjón API, til dæmis ef þú vilt greina fleiri myndir en við leyfum.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning myndgreiningar** og veldu síðan tengda tengilinn.  
2. Færið inn **API URI** og **API lykil** sem þú fékkst fyrir Tölvusjón API.  

    > [!NOTE]  
    > Nauðsynlegt er að bæta **/greina** aftan við API URI ef það er ekki þegar þar. Til dæmis: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Til að sjá hversu margar greiningar þú hefur skilið eftir á núverandi tímabil

Þú getur skoðað hversu margar greiningar þú hefur framkvæmt, og hversu margar þú getur enn gert, á núverandi tímabili.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning myndgreiningar** og veldu síðan tengda tengilinn.  
2. **Gerð marka**, **Gildi marka** og **Framkvæmdar greiningar** veita upplýsingar um notkun.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Hætta að nota viðbót fyrir Myndgreinanda

1. Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustutengingar** og veldu síðan **Uppsetning myndgreiningar**.  
2. Hreinsa **Virkja Myndgreinanda** gátreitinn.  

## <a name="see-also"></a>Sjá einnig

[Vinna með vörueigindir](inventory-how-work-item-attributes.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Hafist handa](product-get-started.md)  
