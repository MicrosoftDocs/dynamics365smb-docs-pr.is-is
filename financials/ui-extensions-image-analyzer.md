---
title: "Notkun viðbótar fyrir Myndgreinanda | Microsoft Docs"
description: "Viðbótin gerir þér kleift að greina myndir af tengiliðum og vörum til að finna eigindir, svo þú getir úthlutað þeim í Dynamics 365 á fljótlegan máta."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/19/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 4329a54114476885285da1d28cd292a4f9684e99
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---

# <a name="the-image-analyzer-extension-for-microsoft-dynamics-365-business-edition"></a>Myndgreinandaviðbótin fyrir Microsoft Dynamics 365 Business edition
Viðbótin fyrir Myndgreinandann notar öflugar myndgreiningaraðferðir frá Tölvusjón API for Microsoft Cognitive Services til að greina eigindir á myndunum sem þú flytur inn fyrir vörur og tengiliði, svo þú getir auðveldlega endurskoðað þær og úthlutað þeim. Fyrir vörur, þá geta eigindir sagt til um hvort varan er borð eða bíll, og hvort hún er rauð eða blá. Fyrir tengiliði, þá geta eigindir verið kyn eða aldur.

Myndgreinandinn leggur til eigindir sem byggjast á merkjum sem Tölvusjón API finnur, og áreiðanleikastig. Greinandinn leggur að sjálfgefnu aðeins til eigindir ef 80% vissa, hið minnsta, er fyrir hendi um að eigindin sé rétt. Þú getur still inn annað áreiðanleikastig, ef þörf krefur. Til að læra meira um hvernig merki og áreiðanleikastig eru ákvörðuð, sjá [Tölvusjón API](https://go.microsoft.com/fwlink/?linkid=851476)  

Myndgreinandinn er ókeypis í [!INCLUDE[d365fin](includes/d365fin_md.md)], en það eru takmörk fyrir því hversu margar vörur þú getur greint yfir ákveðið tímabil. Að sjálfgefnu, geturðu greint 100 myndir á mánuði.

Eftir að þú virkjar viðbótina, keyrist Myndgreinandinn í hvert skipti sem þú flytur inn mynd til vöru eða tengiliðs. Um leið muntu sjá eigindirnar, áreiðanleikastigið og upplýsingarnar og getur ákveðið hvað skal gera við hverja eigind. Ef þú fluttir inn myndir áður en þú virkjaðir Myndgreinanda-viðbótina, þarftu að ná í vöruna eða tengiliðaspjaldið og velja **Greina mynd** aðgerðina.  

>   [!NOTE]  
>   Með því að virkja viðbótina samþykkirðu að Microsoft sé heimilt að geyma gögnin þín og nota þau til að bæta þjónustu Microsoft, t.d. til að gera Tölvusjón API betri. Til að auka persónuvernd, gerum við gögnin þín nafnlaus og höldum þeim öruggum. Við munum ekki birta gögnin þín eða leyfa öðrum að nota þau. Þú getur fjarlægt myndina frá vörunni í [!INCLUDE[d365fin](includes/d365fin_md.md)], en Tölvusjón API mun samt sem áður enn hafa aðgang að myndinni, í dulkóðuðu formi. Nánari upplýsingar, sjá [Microsoft Öryggismiðstöð](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Kröfur
Myndirnar þurfa að lúta nokkrum skilyrðum:

* Myndasnið: JPEG, PNG, GIF, BMP  
* Hámarks skráarstærð: Minna en 4 MB  
* Stærð myndar: Meira en 50 x 50 pixlar  

## <a name="blacklisting-suggested-attributes"></a>Hvaða eigindir skal setja á svartan lista
Ef greiningin leggur til eigind sem þú vilt ekki sjá, geturðu sett þá eigind á svartan lista. Sýndu samt aðgát. Eigindir á svörtum lista koma ekki fram í tillögum um aðrar vörur eða tengiliði heldur. Ef þú sérð eftir því að hafa sett eigind á svartan lista, geturðu valið **Eigindir á svörtum lista** og svo eytt eigindinni af listanum.

## <a name="to-enable-image-analyzer"></a>Að virkja Myndgreinandann
Viðbótin fyrir Myndgreinandann er innbyggð í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þú þarft bara að kveikja á því.

> [!NOTE]  
> Aðeins kerfisstjóri getur virkjað viðbótina fyrir Myndgreinandann. Gakktu úr skugga um að þér sé úthlutað **Yfirnotandi** heimildarsamstæðu fyrir notanda.

1. Gert er eitt af eftirfarandi til að virkja viðbótina fyrir myndgreinandann:

* Vöru- eða tengiliðaspjald er opnað. Á tilkynningastikunni skal velja **Greina myndir**, og svo er skrefunum í Uppsetningu með aðstoð fylgt.  
* Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustutengingar** og velja svo **Uppsetning myndgreiningar** Á gátreitnum skal velja **Virkja myndgreinanda**, og svo er skrefunum í Uppsetningu með aðstoð fylgt.  

>   [!TIP]  
>   Á **Uppsetning myndgreiningar** síðunni geturðu líka breytt áreiðanleikastiginu fyrir tillögur um eigindir. Ef þú vilt til dæmis auka áreiðanleikann, þá geturðu slegið inn hærri prósentu.

## <a name="to-analyze-an-image-of-an-item"></a>Að greina mynd af vöru
Eftirfarandi skref lýsa því hvernig skal greina mynd sem var flutt inn áður en þú virkjaðir viðbótina fyrir Myndgreinandann.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.  
2. Veljið vöruna og veljið svo aðgerðina **Greina mynd**.  
3. Síðan **Eigindir myndgreinanda** birtir þær eigindir sem finnast, áreiðanleikastigið og aðrar upplýsingar um eigindina. Nota **Aðgerð til að framkvæma** valkostina til að tilgreina hvað skal gera við eigindina.  

>   [!TIP]  
>   Þú getur bætt nafni eigindarinnar við lýsinguna á vörunni með því að velja **Bæta við vörulýsingu**. Þetta getur t.d. reynst gagnlegt þegar bæta þarf við upplýsingum snögglega.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Greina mynd af tengilið
Eftirfarandi skref lýsa því hvernig skal greina mynd sem var flutt inn áður en þú virkjaðir viðbótina fyrir Myndgreinandann.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tengiliðir** og velja svo viðeigandi tengil.  
2. Veljið tengiliðinn og veljið svo **Greina mynd** aðgerðina.  
3. Á flýtiflipanum **spurningarlisti fyrir notandasíðu**, skal endurskoða tillögur og leiðrétta ef þarf.  

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Nota þinn eigin aðgang fyrir Tölvusjón API
Þú getur líka notað þinn eigin aðgang fyrir Tölvusjón API, til dæmis ef þú vilt greina fleiri myndir en við leyfum.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning myndagreinanda** og velja svo viðeigandi tengil.  
2. Færið inn **API URI** og **API lykil** sem þú fékkst fyrir Tölvusjón API.  

>   [!NOTE]  
>   Nauðsynlegt er að bæta **/greina** aftan við API URI ef það er ekki þegar þar. Til dæmis: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Til að sjá hversu margar greiningar þú hefur skilið eftir á núverandi tímabil
Þú getur skoðað hversu margar greiningar þú hefur framkvæmt, og hversu margar þú getur enn gert, á núverandi tímabili.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning myndagreinanda** og velja svo viðeigandi tengil.  
2. **Gerð marka**, **Gildi marka** og **Framkvæmdar greiningar** veita upplýsingar um notkun.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Hætta að nota viðbót fyrir Myndgreinanda
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustutengingar** og velja svo **Uppsetning myndgreiningar**.  
2. Hreinsa **Virkja Myndgreinanda** gátreitinn.  

## <a name="see-also"></a>Sjá einnig
[Hvernig á að: Vinna með vörueigindir](inventory-how-work-item-attributes.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

