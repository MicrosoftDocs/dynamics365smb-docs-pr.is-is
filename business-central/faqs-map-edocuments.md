---
title: Algengar spurningar um vörpun e-skjala með innkaupapöntunum
description: 'Þessi eignaspurning veitir upplýsingar um AI-tækni sem notuð er í Business Central ásamt lykilatriðum og upplýsingum um notkun AI, hvernig það var prófað og metið og allar sérstakar takmarkanir.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-mapping-e-documents-with-purchase-orders-using-copilot-preview"></a>Algengar spurningar um vörpun e-skjala með innkaupapöntunum með Copilot (forskoðun)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Þessar algengu spurningar (FAQ) lýsa algengum áhrifum **eiginleikans E-documents Matching Assistance** í [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-e-documents-matching-assistance"></a>Hvað er aðstoð við samsvörun tölvupóstskjala?

Rafræn skjöl (e-documents) eru grunnurinn að nútímaviðskiptum. Þeir standa fyrir mikilvæg pappírsvinnu eins og reikninga og móttökur sem flæða í báðar áttir með afhendingu og móttöku. Hægt er að búa til og senda rafræna reikninga stafrænt á skipulögðu sniði sem auðveldar sjálfvirka reikningsvinnslu. Hins vegar getur meðhöndlun stafrænna reikninga á innleið verið bráðskemmtilegri fyrir gjaldfallna hópa reikninga.  

Í litlum og meðalstórum fyrirtækjum (SMB) gegnir gjaldfallið teymi lykilhlutverki í að rekja skuldbindingar lánardrottna nákvæmlega. Aðalábyrgð þeirra er að skrá reikninga á innleið nákvæmlega. Það getur krafist framvindu að ná nákvæmni, sérstaklega þegar þeir stemma af ytri reikninga frá lánardrottnum við fyrirliggjandi innkaupapantanir. Misræmi í kótum, lýsingum og mælieiningum koma oft fram áskoranir þar sem þessir einingar stemma hugsanlega ekki saman í mismunandi kerfum og fyrirtækjum. Einnig gæti óvæntur kostnaður, t.d. flutningsgjöld, birst sem aðskilin línuatriði sem þarfnast handvirkrar leiðréttingar. Bókarar verða einnig að hafa reikningsnúmer og dagsetningar í fylgiskjölunum. Áríðandi er að sambandið milli innkaupapantana og ytri reikninga sé ekki alltaf eins fyrir einn. Hægt er að fá marga ytri reikninga fyrir sömu innkaupapöntun.

Hægt er að [!INCLUDE [prod_short](includes/prod_short.md)]  búa til nýja innkaupareikninga sem byggðir eru á mótteknum rafrænum reikningum. Hins vegar var samsvörun reikninga handvirkt við fyrirliggjandi innkaupapantanir tímafrekt og villuviðkvæmt ferli.

**Samsvörunaraðstoð** við rafræn skjöl notar ÓM til að streyma við þetta ferli með því að gera greiningu á ytri rafrænum reikningum sjálfvirka. Þessi eiginleiki gerir endurskoðendum kleift að biðja Copilot um að passa við línur á innleið rafrænum reikningum með línum á innkaupapöntunum í [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="what-are-capabilities-of-the-e-documents-matching-assistance"></a>Hvað er hægt að gera á samsvörunaraðstoð við tölvupóstskjöl?

Copilot veitir AI-powered aðstoð til að passa við móttekinn stafrænan reikning við fyrirliggjandi innkaupapantanir í [!INCLUDE [prod_short](includes/prod_short.md)]. Copilot passar við línur sem byggjast á eftirfarandi:

- Líkt lýsingum
- Mælieiningar
- Tiltækt magn til reikningsfærslu
- Upphæðir

Copilot auðkennir svipaðar lýsingar ef þær eru með rétta mælieiningu og verð, en einnig er hægt að finna samsvörun í flóknari tilvikum. Hann getur til dæmis tilgreint hvort rafrænn reikningur er með tvær línur með afbrigði af sömu vöru og aðeins eina línu í innkaupapöntuninni; [!INCLUDE [prod_short](includes/prod_short.md)] passar við þessar línur svo lengi sem lýsingarnar eru svipaðar og verðið er það sama.

Copilot tengist ekki endastöðvarþjónustu e-skjala til að sækja eða senda stafræn fylgiskjöl. Þetta verk helst að fullu innan stjórnunar og er forsenda þess að nota aðstoð Copilot. Þetta á við, óháð því hvort stafrænu skjölunum er bætt við með því að [!INCLUDE [prod_short](includes/prod_short.md)] nota tengingu við endastöðvarþjónustu eða færa inn handvirkt.  

## <a name="what-is-the-intended-use-of-the-e-documents-matching-assistance"></a>Hver er tilætluð notkun á aðstoð við samsvörun tölvupóstskjala?

Markmið aðgerðarinnar **Samsvörun** e-skjala er að aðstoða lánardrottnateymið að passa við fyrirliggjandi innkaupapantanir og rafræna reikninga á innleið. Mikið af þessari aðgerð snýst um strengjasamsvörun. [!INCLUDE [prod_short](includes/prod_short.md)] býður upp á eiginleika sem gerir suma af þessari aðgerð sjálfvirka og LLM hafa verið skilgreind sem tækifæri til viðbótar við þann eiginleika og draga enn frekar úr handvirku átaki.  

## <a name="how-was-e-documents-matching-assistance-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvernig var samsvörunaraðstoð í E-skjölum metin? Hvaða mælieiningar eru notaðar til að mæla afköst?

Þessi aðgerð var prófuð með samsetningum af eftirfarandi upplýsingum:

- Ytri vörulýsingar
- Mælieiningar
- Magn og upphæðir
- Staðlaðar vörulýsingar
- Mismunandi tungumál
- Aðrar færibreytur sem ná yfir dæmigerð frávik og gagnatakmörkun fyrir hvern reit 

Prófunargögn tákna bæði dæmigerða notkun og notkun slæmra leikara. Afköst voru mæld samanborið við handvirka samsvörun sömu gagna í rafrænum reikningum og innkaupapöntunum.

## <a name="what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system"></a>Hverjar eru takmarkanir á aðstoð við tölvupóstskjöl? Hvernig geta notendur minnkað áhrif takmarkana e-skjala sem samsvarandi aðstoðar eru notaðar þegar kerfið er notað?

**Aðstoð við** samsvörun tölvupósts hentar best þegar ytri (e-reikningur) og innri ([!INCLUDE [prod_short](includes/prod_short.md)]) vörulýsingar og mælieiningar eru allar á sama tungumáli. Blönduð tungumál eða blandað tungumál vörulýsinga leiðir oft til færri samsvörunar og tillagna.  

Tillögur um samsvörun vara úr tölvupóstreikningum með vörum í innkaupapöntunum henta best á ensku. Þó svo að hægt sé að nota þessa aðgerð á öllum tungumálum sem [!INCLUDE [prod_short](includes/prod_short.md)] styðjast gætu færri leikir á öðrum tungumálum upplifað færri atriði. Nánari upplýsingar um tungumálið eru í [Í hvaða landafræði og tungumálum er E-skjöl Samsvarandi aðstoð tiltæk?](#in-which-geographies-and-languages-is-e-documents-matching-assistance-available).

## <a name="in-which-geographies-and-languages-is-e-documents-matching-assistance-available"></a>Í hvaða landafræði og tungumáli er netskjöl samsvörunaraðstoð tiltæk?

- Tiltæk landfræði

   Þessi Copilot eiginleiki er fáanlegur í öllum studdum [Business Central löndum/svæðum](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Hins vegar, fyrir umhverfi viðskiptamanna sem staðsett er í löndum/svæðum þar sem Azure OpenAI þjónusta er ekki virk verða stjórnendur fyrst að hafa samþykki til að leyfa gögnum sínum að færast yfir mörk [!INCLUDE [prod_short](includes/prod_short.md)] til að tengjast Azure OpenAI þjónustu. Fræðast meira um [hreyfingu copilot gagna í landfræði](ai-copilot-data-movement.md).

- Tiltæk tungumál

   [!INCLUDE[e-docs-matching-language-support](includes/e-docs-matching-language-support.md)]

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Hvaða rekstrarþættir og stillingar leyfa skilvirka og ábyrga notkun eiginleikans?

Copilot bætir við vörpunarreiknireglurnar sem [!INCLUDE [prod_short](includes/prod_short.md)] þegar eru til staðar og varpar línunum sem reiknireglurnar gerðu ekki.

### <a name="what-is-expected-of-users-while-using-e-documents-matching-assistance"></a>Hvers er ætlast til að notendur noti samsvörun tölvupóstskjala?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

Þegar rafrænir reikningar á innleið hafa verið varpaðir með innkaupapöntunum verður að varpa línunum á skjölunum.

Síðan **Vörpun** innkaupapantana sýnir allar línur úr báðum fylgiskjölum. Hér er hægt að gera vörpunina handvirkt sem getur verið erfitt ef margar línur eru til staðar.

Hægt er að nota **aðstoð við samsvörun tölvupóstskjala** til að varpa línum út frá eftirfarandi skilyrðum:

- Líkt og í lýsingum þeirra
- Mælieiningar
- Tiltækt magn til reikningsfærslu
- Upphæðir

Samsvörun Copilot gæti verið röng eða ófullnægjandi. Þú ættir alltaf að fara yfir nákvæmni þeirra áður en þú velur að halda þeim. Samsvörun og tillögur Copilot eru vistaðar [!INCLUDE [prod_short](includes/prod_short.md)] þegar þú velur **Halda henni** og hætta í Copilot. Hægt er að breyta og leiðrétta samsvörun eða tillögur áður en valið er að halda þeim. 

### <a name="what-is-expected-of-administrators-and-users-when-operating-e-documents-matching-assistance"></a>Hvað er búist við af stjórnendum og notendum þegar unnið er með samsvarandi aðstoð við tölvupóstskjöl?

Notendur, t.d. endurskoðendur eða aðrir sem fá tölvupóstreikninga, ættu ávallt að fara yfir nákvæmni samsvörunar og tillagna sem Copilot veitir áður en kosið er að halda þeim. Mælt er með því að innkaupapantanalínurnar séu skoðaðar til að sannreyna nákvæmni þeirra og finna misræmi. Ákveðið er hvort nota eigi **samsvarandi aðstoð** við fylgiskjöl. Jafnvel þótt **aðstoð** við samsvörun tölvupóstskjala sé virk af stjórnendum og tiltæk er samt hægt að nota hana alltaf, stundum eða aldrei.  

Stjórnendur taka heildarákvörðun um það hvort nota eigi Copilot í [!INCLUDE [prod_short](includes/prod_short.md)]. Ef þeir leyfa Copilot ættu stjórnendur að tryggja að þeir veiti viðeigandi aðgang.

> Takið eftir, 100.000
> - Við styðjum ekki eiginleikann á [!INCLUDE [prod_short](includes/prod_short.md)] staðnum eða í einkaskýjum.
> - Félagar geta ekki framlengt þessa aðgerð. Forritarar félaga geta ekki breytt, skipt út eða framlengt þessa aðgerð. 

## <a name="is-copilot-the-only-way-to-match-e-documents-to-purchase-orders"></a>Er Copilot eina leiðin til að passa við e-skjöl við innkaupapantanir?

Nei, hvort þú notar Copilot er undir þér komið. [!INCLUDE [prod_short](includes/prod_short.md)] býður upp á ónýtar leiðir til að passa við vörur frá mótteknum rafrænum reikningi með vörum á innkaupapöntunum í [!INCLUDE [prod_short](includes/prod_short.md)]. Fyrirtæki geta einnig notað báðar aðferðir samtímis.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hvernig gef ég ábendingar um innihald myndaðs efnis?

Í hvert sinn sem Copilot leggur fram samsvörun eða tillögur er hægt að senda ábendingar til Microsoft beint úr glugganum Copilot með því að nota **stillingarnar Like** og **Dislike** . Ábendingar þínar eru nafnlausar og við notum þessi gögn til að bæta gæði þjónustunnar.  

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir rafræn skjöl](finance-edocuments-overview.md)  
[Tengja rafræn við innkaupapöntunarlínur með Copilot](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
