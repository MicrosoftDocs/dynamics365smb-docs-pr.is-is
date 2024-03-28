---
title: Sérstilling Business Central Online með forritum
description: Kynntu þér allt um hvernig skal bæta við aðgerðum og sérstilla Business Central með því að setja upp forrit í þessari grein.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 09/27/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="customizing-business-central-online-with-apps"></a>Sérstilling Business Central Online með forritum

Þú getur breytt [!INCLUDE[prod_short](includes/prod_short.md)] Online með því að setja forrit sem bæta við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis. Þessi forrit eru einnig kölluð *viðbætur* vegna þess að þau *bæta við* [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="manage-apps"></a>Stjórna forritum

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Þegar þú opnar [!INCLUDE[prod_short](includes/prod_short.md)] í fyrsta skipti eru nokkur forrit þegar sett upp fyrir þig. Með tímanum verða fleiri forrit í boði fyrir þig og þú getur síðan valið hvort þú viljir nota forritið eða ekki.

Til dæmis býður Microsoft upp á forrit sem veitir samþættingu við PayPal Payments Standard. Þessi viðbót er uppsett sjálfgefið En ef önnur viðbót er gerð sem veitir samþættingu við aðra greiðsluþjónusta, geturðu sett inn nýja viðbót og síðan valið hvaða af þessum tveimur þjónustum þú notar.  

Til að nota virkni sem forrit býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti forritsins.

Til að setja upp eða fjarlægja forrit úr AppSource eða bæta við viðbótum fyrir hvern leigjanda fyrir sig þarf að vera með réttar heimildir. Annaðhvort verður þú að vera meðlimur í notendaflokknum **D365 Viðbótastjórnun** eða vera sérstaklega með heimildasamstæðuna **VIÐB.STJ. - STJÓRNANDI**. Ef þú ert stjórnandi geturðu úthlutað notendaflokkum og heimildum til annarra notenda fyrirtækisins. Nánari upplýsingar er að finna í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  

> [!IMPORTANT]  
> Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á staðnum er ekki hægt að hlaða upp viðbótum fyrir hvern leigjanda fyrir sig eða setja upp AppSource forrit í gegnum síðuna **Viðbótastjórnun**. Ekki er hægt að setja upp AppSource forrit á staðnum, þ.m.t. hýsingartengdar uppsetningar.

Þú stjórnar forritunum á síðunni **Viðbótastjórnun**. Hægt er að opna þessa síðu úr heimasvæðinu. Einnig er hægt að velja **Leita að síðu eða skýrslu** táknið ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") efst í hægra horninu, slá inn **Viðbætur** og velja svo tengda hlekkinn. Frekari upplýsingar er að finna í [Setja upp og fjarlægja forrit](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Ef þú telur að þú eigir að hafa aðgang að forriti en finnur ekki virknina sem í því felst, skaltu athuga síðuna **Viðbótarstjórnun** - ef forritið er ekki skráð þar getur þú sett það upp eins og lýst er í eftirfarandi kafla.  

> [!NOTE]  
> Skráðu þig inn á [AppSource.microsoft.com](https://appsource.microsoft.com/) með því að nota netfangið sem þú notar fyrir [!INCLUDE[prod_short](includes/prod_short.md)] Online. Nota sama tölvupóstreikning fyrir aðra þjónustu og vörur fyrir er hnökralausa upplifun.  

Einnig er hægt að fá að markaðstorgið úr [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **framlengingarstjórnun** geturðu séð forritin sem eru í uppsettri röð og þú getur opnað **Framlengingarmarkað** síðu sem sýnir [!INCLUDE[prod_short](includes/prod_short.md)] forritin sem eru í boði í AppSource. Ef valið er *Fleiri öpp* tengilinn, er farið með þig á [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Ef þú velur forrit geturðu lesið um hvað forritið gerir og þú getur fengið aðgang að hjálp fyrir forritið til að læra meira. Þegar valið er að fá forrit, verðurðu að samþykkja skilmála um notkun þess. Ef þú færð forritið af AppSource vefsvæðinu verður þú skráð(ur) inn í [!INCLUDE[prod_short](includes/prod_short.md)] til að ljúka uppsetningunni.  

Þegar þú setur upp forrit gætirðu þurft að setja það upp, svo sem að tilgreina reikning til notkunar með **PayPal Payments Standard fyrir [!INCLUDE[prod_short](includes/prod_short.md)]** framlengingu.
Önnur forrit bæta einfaldlega reitum við fyrirliggjandi síðu, eða þau bæta við nýjum síðum, til dæmis.   

Ef þú fjarlægir forrit og skiptir um skoðun geturðu sett það inn aftur. Þegar þú fjarlægir forrit sem þú hefur verið að nota, eru gögnin geymd svo að ef þú setur það upp aftur, eru gögnin þín enn tiltæk. Sum forrit eru nauðsynleg. Þú ert að koma í veg fyrir að þetta sé fjarlægt af síðunni **Viðbótastjórnun**. Ef þú prófar birtast villuboð.  

Sum forrit eru í boði Microsoft og önnur forrit eru í boði [annarra fyrirtækja](ui-extensions-other.md). Öll forrit eru prófuð áður en þau eru gerðar tiltæk fyrir þig, en við mælum með að þú farir í gegnum tenglana sem eru veittir með hverju forriti til að læra meira um forritið áður en þú setur það upp.  

> [!NOTE]  
> Hægt er að fylgjast með nýjum forritum frá Microsoft og öðrum birgjum á [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer"></a>Forrit og gagnaflutningur

Þar sem eftirfarandi forrit eru í samskiptum við aðra þjónustu gætu þau flutt gögn út úr landfræðilegri staðsetningu á [!INCLUDE[prod_short](includes/prod_short.md)] umhverfinu:

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

Frá og með 2022, útgáfutímabili 2, geta umhverfi [!INCLUDE [prod_short](includes/prod_short.md)] á netinu sýnt eitt eða fleiri forrit á síðunum **Tengiforrit** og **Bankaforrit**. Þessi forrit geta tengt fyrirtækið við utanaðkomandi þjónustu sem eykur framleiðni með því að sjálfvirknivæða ferla. Til dæmis er hægt að tengjast bönkunum og flytja inn bankafærslur sjálfkrafa. Auðvelt er að setja forritin upp og setja þau upp beint af þessari síðu. Veldu forrit til að fá frekari upplýsingar um möguleika og verð.  

Skoðaðu lista yfir forrit sem mælt er með með því að velja aðgerðina **Tengiforrit** á síðunni **Viðbótastjórnun**.  

> [!NOTE]
> Fyrsti aðilinn til að opna síðuna **Tengiforrit** verður að leyfa viðbótinni að tengjast við ytri þjónustu. Leyfa tenginguna einu sinni eða alltaf. Ef þú velur að loka á tenginguna verður þú að finna tilheyrandi forrit í AppSource.

Þessi ytri þjónusta útbýr lista yfir viðeigandi forrit út frá landinu þínu eða svæði.

## <a name="recommended-apps"></a>Ráðlögð forrit

Samstarfsaðilar og endursöluaðilar Microsoft geta búið til forrit sem þeir geta notað til að setja saman lista yfir forrit sem þeir mæla oft með fyrir viðskiptavini sína. Ef þeir gera það og hafa innleitt forrit í leigjandanum þínum verða forritin aðgengileg á síðunni **Ráðlögð forrit**. Þar er hægt að lesa sér til um hvert forrit og ákveða hvort eigi að setja þau upp.

> [!NOTE]
> Ef þú ert samstarfsaðili eða endursöluaðili Microsoft og hefur áhuga á að bjóða upp á lista yfir forrit sem mælt er með skaltu skoða [Mæla með forritum frá AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) í efni stjórnanda.

## <a name="see-also"></a>Sjá einnig .

[Setja upp og fjarlægja forrit](ui-extensions-install-uninstall.md)  
[Sérstilla Business Central](ui-customizing-overview.md)  
[Business Central-forrit frá öðrum veitum](ui-extensions-other.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[Virkja greiðslur viðskiptamanna um greiðsluþjónustur](sales-how-enable-payment-service-extensions.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Setja upp GetAddress.io UK Postal Code viðbótina](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] forrit frá öðrum veitum](ui-extensions-other.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
