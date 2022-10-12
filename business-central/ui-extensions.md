---
title: Sérsníða viðskipti miðlægt á netinu með notkun apps
description: Lærðu allt um að bæta við aðgerðum og sérsníða Business Central með því að setja upp forrit í þessari grein.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.search.form: 2500, 2502, 20350, 20353
ms.date: 09/27/2022
ms.author: edupont
ms.openlocfilehash: 5b0744394201e11534f19c25999af0da0944ec9b
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605685"
---
# <a name="customizing-business-central-online-with-apps"></a>Sérsníða viðskipti miðlægt á netinu með apps

Þú getur breytt [!INCLUDE[prod_short](includes/prod_short.md)] netinu með því að setja upp forrit sem bæta við aðgerðum, breyta hegðun eða veita þér aðgang að nýjum þjónustum á netinu. Þessi forrit eru einnig kölluð *viðaukabréf* þar sem þau *lengja*[!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="manage-apps"></a>Stjórna forritum

Þegar fyrsta ræsing [!INCLUDE[prod_short](includes/prod_short.md)] er hafin eru sum forrit uppsett fyrir þig. Með tímanum verða fleiri forrit gerð aðgengileg þér og þú getur svo valið hvort þú viljir nota App eða ekki.

Til dæmis býður Microsoft upp á App sem veitir samþættingu við PayPal greiðslur. Þessi viðbót er uppsett sjálfgefið En ef önnur viðbót er gerð sem veitir samþættingu við aðra greiðsluþjónusta, geturðu sett inn nýja viðbót og síðan valið hvaða af þessum tveimur þjónustum þú notar.  

Ef nota á aðgerðina sem App fyrir forrit eins og að opna síður, keyra skýrslur, velja aðgerðir og þess háttar, verður að vera hægt að úthluta heimilunum sem eru settar upp sem hluti af forritinu.

Til að setja upp eða fjarlægja forrit úr AppSource eða bæta við dagrennum fyrir hvern leigjanda þarf að hafa réttar heimildir. Annaðhvort þarf að vera meðlimur **í D365 Extension Mgt.** Notendaflokkur eða þá verður að hafa **exten.-admin** heimild sett skýrt fram. Ef þú ert stjórnandi geturðu úthlutað notendaflokkum og heimildum til annarra notenda fyrirtækisins. Nánari upplýsingar er að finna í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  

> [!IMPORTANT]  
> Fyrir innanhúss er ekki hægt að [!INCLUDE [prod_short](includes/prod_short.md)] hlaða inn viðaukum fyrir AppSource hvern leigjanda eða setja upp **forrit í gegnum framlengingarsíðuna**. Ekki er hægt að setja upp AppSource forrit innanhúss, m.a. í virkjun sem byggir á Docker.

Þú stjórnar appinu á **síðunni um Framlengingarstjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Einnig er hægt að velja **Leita að síðu eða skýrslu** táknið ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") efst í hægra horninu, slá inn **Viðbætur** og velja svo tengda hlekkinn. Frekari upplýsingar er að finna [í setja upp og fjarlægja apps](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Ef þú telur að þú ættir að hafa aðgang að App en finnur ekki virkni þess, Leitaðu á **síðu Framlengingarstjórnunar** -ef forritið er ekki skráð þar geturðu sett það upp eins og lýst er í eftirfarandi kafla.  

> [!NOTE]  
> Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[prod_short](includes/prod_short.md)] Online. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fá að markaðstorgið úr [!INCLUDE[prod_short](includes/prod_short.md)]. **Á síðunni um Framlengingarstjórnun** má sjá appið sem nú er uppsett og hægt er að opna síðu um **framlengingarmarkaðinn** sem sýnir [!INCLUDE[prod_short](includes/prod_short.md)] appið sem nú er aðgengilegt í AppSource. Ef valið er *Fleiri öpp* tengilinn, er farið með þig á [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Ef þú velur App getur þú lesið þér til um hvað forritið gerir og þú getur nálgast Hjálp fyrir app til að fræðast meira. Þegar valið er að fá App þarf að samþykkja notkunarskilmála. Ef þú færð App af AppSource vefsvæðinu þá skráir þú þig inn til [!INCLUDE[prod_short](includes/prod_short.md)] að klára uppsetninguna.  

Þegar þú setur upp App gætir þú þurft að setja það upp, svo sem að tilgreina lykil til að nota með **PayPal greiðslum stöðluðum fyrir [!INCLUDE[prod_short](includes/prod_short.md)]** framlengingu.
Önnur forrit bæta einfaldlega reitum við síðu sem fyrir er, eða þau bæta við nýrri síðu, td.   

Ef þú fjarlægir App og skiptir um skoðun getur þú sett það upp aftur. Þegar þú fjarlægir App sem þú hefur verið að nota, eru gögnin varðveitt þannig að ef þú setur upp forritið aftur, þá er gögnin þín enn tiltæk. Til eru nokkur forrit sem eru nauðsynleg. Þú ert að koma í veg fyrir að þetta sé fjarlægt af síðunni **Viðbótastjórnun**. Ef þú prófar birtast villuboð.  

Sum forrit eru veitt af Microsoft, og önnur forrit eru veitt af [öðrum fyrirtækjum](ui-extensions-other.md). Öll forrit eru prófuð áður en þau eru gerð aðgengileg þér, en við mælum með að þú fáir aðgang að þeim tenglum sem fylgja með hverju viðauka fyrir sig til að fá frekari upplýsingar um App áður en þú velur að setja það upp.  

> [!NOTE]  
> Hægt er að hafa auga með nýjum forritum frá Microsoft og öðrum birgjum á [AppSource . microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer"></a>Apps og Gagnaflutningur

Þar sem eftirfarandi forrit eiga samskipti við aðra þjónustu gætu þau flutt gögn úr landafræði [!INCLUDE[prod_short](includes/prod_short.md)] umhverfisins:

* AMC Banking 365 Fundamentals Viðbót
* Myndgreinandi
* Greiðsludráttarspá
* PayPal Payments Standard
* Sölu- og birgðaspár
* WorldPay Payments Standard

Þetta á einnig við um suma virkni í grunnforritinu, svo sem eftirfarandi eiginleika:

* Sjóðstreymisspá
* Skjalaskiptaþjónusta
* Dataverse tengingar
* Stafakennslaþjónusta
* Kortaþjónusta
* VSK-skráningarnúmer innan ESB. Þjónusta

## <a name="connect-your-business"></a>Tengdu fyrirtækið þitt

Sem byrjar í 2022 2, [!INCLUDE [prod_short](includes/prod_short.md)] netumhverfi getur nýtt eitt eða fleiri forrit á **vefsíðum tengingar** og **forritun** forrita. Þessi forrit geta tengt fyrirtæki þitt við utanaðkomandi þjónustu sem eykur framleiðni með því að gera ferla sjálfvirka. Til dæmis er hægt að tengjast bankanum og flytja sjálfkrafa inn bankaviðskipti. Appinn er auðveldur í uppsetningu og settur upp beint af þessari síðu. Veldu app til að fræðast meira um getu og verðlagningu.  

Skoðið lista yfir leiðbeinandi apps með því að velja aðgerðir fyrir **tengingar** á síðu um **framlengingarstjórnun**.  

> [!NOTE]
> Fyrsti einstaklingurinn til að opna **tengipunkta tengingar** verður að leyfa viðaukanum að tengjast við utanaðkomandi þjónustu. Leyfa tenginguna einu sinni eða alltaf. Ef valið er að loka á tenginguna þarf að finna viðkomandi forrit á AppSource.

Þessi utanaðkomandi þjónusta mun mynda lista yfir viðeigandi forrit út frá þínu landi eða svæði

## <a name="recommended-apps"></a>Ráðleggingar apps

Microsoft-samstarfsaðilar og endurseljendur geta stofnað App sem þeir geta notað til að þýða lista yfir forrit sem þau mæla oft með við viðskiptavini sína. Ef þeir gera það, og hefur virkjað app til leigjanda, verður appið fáanlegt á **síðunni ráðleggingar apps**. Þar er hægt að lesa sér til um hvert forrit og ákveða hvort eigi að setja þau upp.

> [!NOTE]
> Ef þú ert samstarfsaðili samstarfsaðila í Microsoft eða endursöluaðila og hefur áhuga á að bjóða upp á lista með ráðlögðum forritum, sjá [meðmæli með forritum úr AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) stjórnunarefninu.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/customize-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp og fjarlægja forrit](ui-extensions-install-uninstall.md)  
[Sérstilla Business Central](ui-customizing-overview.md)  
[Viðskipti miðlæg apps eftir öðrum Veituveitum](ui-extensions-other.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[Virkja greiðslur viðskiptamanna um greiðsluþjónustur](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra Viðskipdata frá öðrum Fjármálakerfum](across-import-data-configuration-packages.md)  
[Setja upp GetAddress.io framlengingarkóta póstnúmers](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] apps eftir öðrum veitum](ui-extensions-other.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
