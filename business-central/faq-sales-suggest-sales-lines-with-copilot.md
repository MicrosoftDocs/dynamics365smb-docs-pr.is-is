---
title: Algengar spurningar fyrir tillögur um sölulínur með Afrita
description: Þessi eignaspurning veitir upplýsingar um AI-tæknina sem notuð er í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# <a name="faq-for-sales-line-suggestions-with-copilot-preview"></a>Algengar spurningar fyrir sölulínutillögur með afrita (forskoðun)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Algengar spurningar (FAQ) lýsa algengum áhrifum aðgerða sölulínutillögunnar í [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-sales-line-suggestions-with-copilot"></a>Hvað er sölulínutillögur með afrita?

Sölulínutillaga með Copilot getur aðstoðað við stofnun lína í söluskjölum, svo sem sölutilboðum, pöntunum og reikningum sem byggjast á skipulögðu ílagi eða náttúrulegu tungumáli. Eiginleikinn er ekki almennt spjall, heldur mjög sértæk og samþætt reynsla sem hægt er að nota á söluskjölum. Þessi eiginleiki býður upp á tvær aðskildar hæfni sem hjálpa til við að finna gögn um einstakar vörur eða öll skjölin.

## <a name="what-are-capabilities-of-sales-line-suggestions-with-copilot"></a>Hvað eru möguleikar á sölulínutillögum með Copilot?

* Finna afurðir

  Upplýsingar sem lýsa vörum eru geymdar á mörgum stöðum [!INCLUDE [prod_short](includes/prod_short.md)]. Til dæmis eru vörunúmer og lýsingar geymd í töflunni Vara **, mörg strikamerki geymd í** töflunni Vörutilvísun **og eiginleikar framleiðslu eru geymdir í** töflunni Vörueigindir **.**  Þó að beðið sé um *rauð reiðhjól* gæti sjálf varan verið *Crimson tourer*, þar sem *Reiðhjól* er vöruflokkur og *rauður er eigind* .

* Finna skjal með tilvísun

  Notandi endurtekur oft fyrri pöntun eða notar hana að minnsta kosti sem upphafspunkt. En það gæti verið erfiður að finna rétta pöntun í bunka af pöntunum. Sumt af pöntunarkenninu gæti munað, sem getur verið fyrirtækið sem úthlutaði númeri eða tilvísunarnúmeri frá viðskiptamanni. Ef hægt er að nota kvaðningar eins og *Þörf á síðasta reikningi frá apríl* ætti að hjálpa þér að finna pöntun hraðar.

## <a name="what-is-the-intended-use-of-sales-line-suggestions-with-copilot"></a>Hver er tilætluð notkun sölulínutillögu með Copilot?

* Finna afurðir

  Ætlunin er að svara notendum með kvaðningu um að finna vörur sem byggjast á óljósum, ófullnægjandi eða ónákvæmum lýsingum.

  Þar sem meðalfjöldi vara (vörur/þjónusta) fyrir [!INCLUDE [prod_short](includes/prod_short.md)] viðskiptamenn er 10.000 gæti það verið erfitt að finna réttu vörurnar án fyrri reynslu eða þekkingar. Það auðveldar ekki hvernig gögn geymd í [!INCLUDE [prod_short](includes/prod_short.md)] hlutum auðvelda því að leita þarf að mörgum leitum eða afmarka æfingar á mismunandi síðum sem geyma vörugögn.

  Copilot dregur fram umbeðnar vörur og magn og auðkennir helstu leitarorð og eiginleika, svo hægt sé að færa inn kvaðninguna hraðar. Síðan gerir Copilot ítarlega leit í gegnum margar tengdar töflur, notar samstillt, leiðréttir sniði og metur gæði leitarfrálagsins.

* Finna skjal með tilvísun

  Ætlunin er að svara fyrirspurnum notanda til að finna fyrirliggjandi söluskjöl fyrir tiltekinn viðskiptamann með því að nota hluta- eða nánast upplýsingar.

  Í B2B umhverfi getur fólk oft tekið við ítrekuðum beiðnum og pantanavinnslur fengið fyrirspurnir til að endurtaka fyrra skjal eða að minnsta kosti nota það sem upphafspunkt. En það gæti verið erfiður að finna einn af nokkrum ástæðum:

  - Söluskjal getur þróast frá tilboði til pöntunar í bókaðan reikning eða afhendingu með því að þróast í söluskjal. Einnig er hægt að geyma skjöl.
  - Þú ert kannski með nákvæmt auðkenni en getur ekki sagt til um hvað það táknar. Er það til dæmis pöntunarnúmer, reikningsnúmer eða ytri tilvísun?
  - Stundum er til dagsetning eða tímabil en ekki kenni fylgiskjals.

  Til að finna upprunaskjal handvirkt þarf að opna margar síður og nota leit og afmarka mörgum sinnum. Hins vegar einfaldar Copilot þetta í einum, náttúrulegri fyrirspurn sem gerir þér kleift að tjá það sem þú leitar að á eigin hátt. 

  * *Sækja vörur úr pöntun 103031*
  * *Þurfa vörur frá síðasta reikningi í ágúst*

## <a name="how-was-sales-line-suggestions-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvernig voru sölulínutillögur með Copilot metnar? Hvaða mælieiningar eru notaðar til að mæla afköst?

Aðgerðin gekkst undir umfangsmikla prófun þar sem fjölmargar kvaðningar á bandarískri ensku standa fyrir bæði dæmigerða notkun og notkun slæmra leikara. Prófun var byggð á [!INCLUDE [prod_short](includes/prod_short.md)] gögnum um sýni og stór merktur vörulisti tiltækur sem opinn uppruni.

Þessi eiginleiki er byggður upp samkvæmt staðlinum Ábyrgur AI-staðall Microsoft. [Fræðast meira um ábyrgt ÓM frá Microsoft](https://aka.ms/RAI).

## <a name="what-are-the-limitations-of-sales-line-suggestions-with-copilot-how-can-users-minimize-the-impact-of-the-sales-line-suggestions-with-copilot-limitations-when-using-the-system"></a>Hverjar eru takmarkanir á sölulínutillögum með Copilot? Hvernig geta notendur minnkað áhrif sölulínutillögunnar með takmörkunum Copilot þegar kerfið er notað?

* Finna afurðir
  
  Finna vörur virkar best á ensku. Þó að hægt sé að nota þessa aðgerð á hvaða tungumáli sem er sem er sem [!INCLUDE [prod_short](includes/prod_short.md)] styður gæti vöruleit á öðrum tungumálum verið nákvæm.

Ef iðnaður þinn eða lén skarast við það sem Microsoft telur viðkvæm efnisatriði (eins og dóp, ofbeldi, fullorðinsskemmtun o.s.frv.) Gæti Copilot frestað hlutlausum, læknuðum svörum eða gefið ónákvæm svör.

Sölulínurtillögur færa aðeins inn í reitina **Tegund** sem **Vara**, **Nr.**, og Magn **eins og** lýst var. Aðrir reitir, þar á meðal **Mælieining**, **Ein.verð** og **Birgðageymsla** nota gildandi rökfræði og eru útfylltir annaðhvort byggðir á vörustillingum eða erfðum gildum úr fylgiskjalshausnum.

 **Afbrigðiskótinn** er ekki studdur eins og er. Ef hægt er að senda vöru í tveimur mismunandi litum, til dæmis finnur Copilot vöruna sem þarf en skilur reitinn **Afbrigðiskóti** eftir auðan. Reiturinn þarf að vera fylltur út handvirkt.

Hvernig vörur þínar geta haft áhrif á frálag. Til dæmis getur það dregið úr gæðum dulritunar með dulritunarskammstöfunum samanborið við vinaleg heiti.

Í vörum er listi yfir töflur og reiti sem Copilot leitar í.

|Tafla  |Reitir  |
|---------|---------|
|**Birgðir**     |  *Nei.<br>*Lýsing<br>* Lýsing 2<br>* Leitarlýsing<br>* GTIN<br>* Vörunúmer lánardrottins       |
|**Vöruafbrigði**     | *Kóða<br>*Lýsing<br>* Lýsing 2          |
|**Vörutilvísun**     | * Tilvísun nr.<br>*Lýsing<br>* Lýsing 2        |
|**Eigindir vöru**     | *Heiti<br>*Gildi        |
|**Vöruflokkur**     |  *Kóða<br>*Lýsing<br>* Yfirflokkur - 1 stig           |
|**Birgðatexti**     | *Tungumál<br>*Lýsing<br>* Lýsing 2          |
|**Vörukenni**     |  *Kóða       |
|**Lengd textalína**     |  *Texta      |

* Finna skjöl eftir tilvísun

  Eins og er er hægt að hefja sölulínur tillaga af sölupöntunum, reikningum og tilboðum og leita í eftirfarandi skjölum:

  * Sölupantanir
  * Sölutilboð
  * Sölureikningar
  * Bókaðir sölureikningar
  * Bókaðar söluafhendingar

  Copilot leitar í eftirfarandi reitum

  * Fylgiskjalsnr.
  * Númer ytra fylgiskjals
  * Tilvísun notanda
  * Tilboðsnr.
  * Dagsetning fylgiskjals
  * Nr. selt-til-viðskiptavinar

  Copilot skilar ekki öllum línum af tegundinni Vara. Aðeins vörunúmer, afbrigðiskótar og magn eru flutt. Magni úr upprunaskjalinu er breytt í **Sölumælieining**.

## <a name="in-which-geographies-and-languages-is-sales-lines-suggestions-available"></a>Í hvaða landafræði og tungumáli eru Sölulínur tillögur tiltækar?

Að undanskildum Kanada er þessi eiginleiki tiltækur fyrir öll staðfæring á umhverfis-/svæðum og á öllum studdum tungumálum. Vegna stuðnings við takmarkaðan tungumála verður aðgerðin ekki í upphafi tiltæk kanadískum viðskiptavinum vegna reglubundinnar málsmeðferðar. Til að þessi möguleiki sé tiltækur fyrir umhverfi viðskiptamanna sem staðsett er í löndum/svæðum þar sem Azure OpenAI þjónusta er ekki virk verða stjórnendur fyrst að hafa samþykki til að leyfa gögnum sínum að færast yfir mörk [!INCLUDE [prod_short](includes/prod_short.md)] til að tengjast Azure-þjónustu OpenAI .  

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Hvaða rekstrarþættir og stillingar leyfa skilvirka og ábyrga notkun eiginleikans?

Ónýtar tillögur gætu stundum verið rangar eða ófullnægjandi. Þú ættir alltaf að fara yfir nákvæmni tillagna Copilot áður en þú velur hvort þær skuli geymdar. Tillögur Copilot eru ekki vistaðar í gagnagrunninum [!INCLUDE [prod_short](includes/prod_short.md)] fyrr en þú velur hnappinn **Halda honum** og loka glugganum Copilot. Hægt er að breyta og leiðrétta allar tillögur áður en kosið er að halda þeim eða eftir að þær hafa verið settar inn í söluskjal.

### <a name="what-is-expected-of-administrators-and-end-users-when-using-sales-lines-suggestions"></a>Hvað er búist við af stjórnendum og notendum þegar sölulínur eru notaðar?

Hver notandi velur hvort nota **eigi Sölulínur tillögur** eða ekki. Jafnvel þótt stjórnendur og tiltækir eiginleikar séu virkir er hægt að nota hana alltaf, stundum eða aldrei.  

Stjórnendur taka heildarákvörðun um það hvort nota eigi Copilot getu í [!INCLUDE [prod_short](includes/prod_short.md)]. Ef stjórnendur leyfa Copilot ættu þeir að vera viss um að veita viðeigandi notendum aðgang.   

> Takið eftir, 100.000
> - Við styðjum ekki þessa aðgerð innanhúss [!INCLUDE [prod_short](includes/prod_short.md)] eða í einkaskýi.
> - Félagi getur ekki framlengt þessa aðgerð. Það þýðir að forritarar félaga geta ekki breytt, skipt um eða framlengt hann.

## <a name="is-copilot-the-only-means-to-create-sales-lines"></a>Er Afrita eini leiðin til að stofna sölulínur?

Notkun Copilot er valfrjáls. [!INCLUDE [prod_short](includes/prod_short.md)] býður upp á ónýtar leiðir til að setja inn sölulínur eða afrita skjöl. Fyrirtæki geta notað báðar aðferðir samtímis.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hvernig gef ég ábendingar um innihald myndaðs efnis?

Í hvert sinn sem Copilot leggur fram tillögur er hægt að senda ábendingar til Microsoft beint í glugganum Copilot með því að nota hnappana Like og Dislike. Svörun þín er nafnlaus og við notum þessi gögn til að bæta gæði þjónustunnar.  

## <a name="see-also"></a>Sjá einnig .

[Leggja til línur í sölupöntunum með Afrita](sales-suggest-sales-lines-with-copilot.md)  
[Grunnstilla Copilot- og gervigreindarmöguleika](enable-ai.md)  
[Algengar algengar spurningar fyrir Dynamics 365 Business Central](responsible-ai-overview.md)  
