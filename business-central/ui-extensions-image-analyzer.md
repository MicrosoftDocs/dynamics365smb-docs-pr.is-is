---
title: Myndgreiningarviðbót
description: Viðbótin gerir þér kleift að greina myndir af tengiliðum og vörum til að finna eigindir, svo þú getir úthlutað þeim í Business Central á fljótlegan máta.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.search.form: 2026, 2027, 2029,
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: 814224ed0ba9453c0e787a673dd03e2817ed666f
ms.sourcegitcommit: 2396dd27e7886918d59c5e8e13b8f7a39a97075d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524628"
---
# <a name="the-image-analyzer-extension"></a>Myndgreiningarviðbót

Viðbótin fyrir Myndgreinandann notar öflugar myndgreiningaraðferðir frá Computer Vision API for Azure Cognitive Services til að greina eigindir á myndunum sem þú flytur inn fyrir vörur og tengiliði, svo þú getir auðveldlega endurskoðað þær og úthlutað þeim. Fyrir vörur, þá geta eigindir sagt til um hvort varan er borð eða bíll, og hvort hún er rauð eða blá. Fyrir tengiliði, þá geta eigindir verið kyn eða aldur.

Myndgreinandinn leggur til eigindir sem byggjast á merkjum sem Tölvusjón API finnur, og áreiðanleikastig. Greinandinn leggur að sjálfgefnu aðeins til eigindir ef 80% vissa, hið minnsta, er fyrir hendi um að eigindin sé rétt. Þú getur still inn annað áreiðanleikastig, ef þörf krefur. Til að læra meira um hvernig merki og áreiðanleikastig eru ákvörðuð, sjá [Tölvusjón API](https://go.microsoft.com/fwlink/?linkid=851476)  

Myndgreinandinn er ókeypis í [!INCLUDE[prod_short](includes/prod_short.md)], en það eru takmörk fyrir því hversu margar vörur þú getur greint yfir ákveðið tímabil. Að sjálfgefnu, geturðu greint 100 myndir á mánuði.

Eftir að þú virkjar viðbótina, keyrist Myndgreinandinn í hvert skipti sem þú flytur inn mynd til vöru eða tengiliðs. Um leið muntu sjá eigindirnar, áreiðanleikastigið og upplýsingarnar og getur ákveðið hvað skal gera við hverja eigind. Ef þú fluttir inn myndir áður en þú virkjaðir Myndgreinanda-viðbótina, þarftu að ná í vöruna eða tengiliðaspjaldið og velja **Greina mynd** aðgerðina.  

## <a name="privacy-notice"></a>Persónuverndaryfirlýsing

Þessi viðbót notar Computer Vision API frá Azure Cognitive Services, sem kann að hafa mismunandi stig skuldbindingar um reglufylgni en [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar þú kveikir á Image Analyzer viðbótinni verða viðskiptamannagögn á borð við tengiliðamynd eða vörumynd send til Tölvusjónar API. Með því að setja upp þessa viðbót samþykkir þú að þetta takmarkaða gagnasafn verði sent til Computer Vision API. Bent er á að hægt er að gera óvirkan, og fjarlægja, með því að nota Myndgreinendingu hvenær sem er til að hætta notkun þessarar virkni. Nánari upplýsingar, sjá [Microsoft Öryggismiðstöð](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Kröfur

Myndirnar þurfa að lúta nokkrum skilyrðum:

* Myndasnið: JPEG, PNG, GIF, BMP  
* Hámarks skráarstærð: Minna en 4 MB  
* Stærð myndar: Meira en 50 x 50 pixlar  

## <a name="switch-on-the-image-analyzer-extension"></a>Rofi á Greindri framlengingarmynd

Viðbót myndgreiningar er innbyggð í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú þarft bara að skipta því út.

> [!NOTE]  
> Aðeins kerfisstjóri getur virkjað viðbótina fyrir Myndgreinandann. Gakktu úr skugga um að þér sé úthlutað **Yfirnotandi** heimildarsamstæðu fyrir notanda. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

Gert er eitt af eftirfarandi til að virkja viðbótina fyrir myndgreiningu:

* Vöru- eða tengiliðaspjald er opnað. Í tilkynningarstikunni skal velja **greina mynd** og fylgja síðan skrefunum í uppsetningarhandbók aðstoðar.  
* Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Þjónustutengingar** og veldu síðan **Uppsetning myndgreiningar**. Á gátreitnum skal velja **Virkja myndgreinanda**, og svo er skrefunum í Uppsetningu með aðstoð fylgt.  

    > [!TIP]  
    > Á **Uppsetning myndgreiningar** síðunni geturðu líka breytt áreiðanleikastiginu fyrir tillögur um eigindir. Ef þú vilt til dæmis auka áreiðanleikann, þá geturðu slegið inn hærri prósentu.

## <a name="analyze-an-item-image"></a>Greina vörumersímynd

Eftirfarandi skref lýsa því hvernig skal greina mynd sem var flutt inn áður en þú virkjaðir viðbótina fyrir Myndgreinandann.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Veljið vöruna og veljið svo aðgerðina **Greina mynd**.  
3. Síðan **Eigindir myndgreinanda** birtir þær eigindir sem finnast, áreiðanleikastigið og aðrar upplýsingar um eigindina. Notaðu **Aðgerð til að framkvæma** valkostinn til að tilgreina hvað skal gera við eigindina eða veljdu **Bæta við vörulýsingu** til að bæta heiti eiginleikans við vörulýsinguna. Þessi aðgerð getur til dæmis gagnast fljótlegra að bæta við smáatriðum.

Í **reitnum aðgerð til að framkvæma** er eftirfarandi valkostir:

| Aðgerð | Lýsing |
| ------ | ----------- |
| *Hunsa* | Engar aðgerðir verða framkvæmdar. |
| *Nota sem eigind* | Gildinu er bætt við eiginleika vörunnar. Frekari upplýsingar í [vinnu með eigindir atriðis](inventory-how-work-item-attributes.md). |
| *Nota sem tegund* | Völdu gildi er bætt við sem flokki. Frekari upplýsingar við [flokkun vara](inventory-how-categorize-items.md). |
| *Bæta við útilokunarlista* | Ef greiningin leggur til eigind sem þú vilt ekki sjá, geturðu lokað á þá eigind. Sýndu samt aðgát. Útilokaðar eigindir koma ekki fram í tillögum um aðrar vörur heldur. Ef þú sérð eftir því að hafa lokað á eigind velurðu **Skoða útilokaðar eigindir** og eyðir svo eigindinni úr listanum. |

> [!NOTE]  
> Sjálfgefið **vörueigindi** birtir eigindir þar sem **traust stig** er yfir **traustum þröskuldi%** skilgreint í **uppsetningu** myndgreiningargreiningar. Til að sjá alla greinda eiginleika skal velja aðgerðina **Skoða alla eiginleika**.

## <a name="analyze-a-contact-person-picture"></a>Greina mynd tengiliðar

Eftirfarandi skref lýsa því hvernig skal greina mynd sem var flutt inn áður en þú virkjaðir viðbótina fyrir Myndgreinandann.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tengiliðir** og velja síðan viðkomandi tengil.  
2. Veljið tengiliðinn og veljið svo **Greina mynd** aðgerðina.  
3. Á flýtiflipanum **spurningarlisti fyrir notandasíðu**, skal endurskoða tillögur og leiðrétta ef þarf. [Frekari upplýsingar um notkun spurningalista lýsingar til að flokka Viðskiptatengiliða](marketing-create-contact-profile-questionnaire.md).  

    > [!NOTE]  
    >
    > Computer Vision API skilar eftirfarandi eiginleikum:
    >
    > * *aldur*
    >
    >     Áætlaður „sýnilegur aldru“ í árum. Það er hversu gamall einstaklingur virðist vera borið saman við raunverulegan líffræðilegan aldur.
    > * *kyn*
    >
    >    Karl eða kona.
    >
    > Tölvuvision API skilar ekki traustu stigi fyrir eigindir aldur og kyn.
  
## <a name="use-your-own-computer-vision-api-account"></a>Notaðu þinn eigin Tölvuvision API lykil

Einnig er hægt að nota eigin reikning fyrir API Tölvuvision, t.d. ef á að greina fleiri myndir en sjálfgefin samþættingartilboð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **uppsetningu** myndgreiningar og veljið síðan tengda tengilinn.
2. Færið inn **API URI** og **API lykil** sem þú fékkst fyrir Tölvusjón API.  

    > [!NOTE]  
    > Nauðsynlegt er að bæta **/greina** aftan við API URI ef það er ekki þegar þar. Til dæmis:```https://cronus.api.cognitive.microsoft.com/vision/v2.0/analyze```.

## <a name="see-how-many-analyses-you-have-left-in-the-current-period"></a>Sjá hversu margar greiningar eru skildar eftir á yfirstandandi tímabili

Þú getur skoðað hversu margar greiningar þú hefur framkvæmt, og hversu margar þú getur enn gert, á núverandi tímabili.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **uppsetningu** myndgreiningar og veljið síðan tengda tengilinn.
2. **Gerð takmöranna,** takmörk marka **og** Greining framkvæmda í framkvæmdum **svæði veita notkunarupplýsingar**.  

## <a name="stop-using-the-image-analyzer-extension"></a>Hætta að nota Myndgreinitendingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Þjónustutengingar** og veldu síðan **Uppsetning myndgreiningar**.  
2. Hreinsið svæðið virkja með **Myndgreindri** mynd.  

Einnig er hægt að fjarlægja viðbótina alveg. Það er alltaf hægt að sækja þetta aftur af AppSource. Frekari upplýsingar er að finna [í setja upp og fjarlægja viðauka í Business Central](ui-extensions-install-uninstall.md#uninstall-an-extension).  

## <a name="see-also"></a>Sjá einnig .

[Vinna með vörueigindir](inventory-how-work-item-attributes.md)  
[Flokka vörur](inventory-how-categorize-items.md)  
[Nota spurningalista forstillingar til að flokka viðskiptatengiliði](marketing-create-contact-profile-questionnaire.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
