---
title: Algengar spurningar fyrir afstemmingu bankareikninga aðstoða við Copilot (forskoðun)
description: 'Í þessari algengu upplýsingar eru upplýsingar um tækni sem er notuð til að stemma af bankareikninga og yfirlit í Business Central. Í honum eru lykilatriði og upplýsingar um notkun ÓM, hvernig það var prófað og metið og allar sérstakar takmarkanir.'
ms.date: 03/27/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-bank-account-reconciliation-assist-with-copilot-preview"></a>Algengar spurningar fyrir afstemmingu bankareikninga aðstoða við Copilot (forskoðun)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Algengar spurningar (FAQ) lýsa algengum aðstoðum við afstemmingu Microsoft Copilot bankareikninga [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>Hvað er aðstoð við bankaafstemmingu?

Bankaafstemming er sameiginlegt bókhaldsverk þar sem fyrirtæki fara yfir bankareikningsyfirlit sín til að auðkenna færslur sem á að skrá inn [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi verkhluti er til dæmis notaður til að auðkenna reglubundin bankagjöld eða lítil útgjöld starfsmanna.

Bankaafstemming er yfirleitt ferli í mörgum þrepum. Í fyrsta lagi eru bankayfirlit flutt inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Næst eru færslur jafnaðar fjárhagsfærslum. Að lokum eru nýjar færslur bókaðar til að endurspegla afborgunarhreyfingar sem ekki voru áður þekktar í fjárhagnum.

Copilot dregur [!INCLUDE[prod_short](includes/prod_short.md)] úr handvirku átaki með því að samsvara fleiri færslum og leggja til fjárhagsreikninga (fjárhagsreikninga) sem hægt er að bóka á.

## <a name="what-are-the-capabilities-of-bank-reconciliation-assist"></a>Hver er möguleiki á að aðstoða bankaafstemmingu?

Copilot veitir alhliða aðstoð við tvo aðskilda verkhluta:

- Bætt samsvörun færslna með fjárhagsfærslum

    [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á sjálfvirkar reglur sem samsvara sjálfkrafa mörgum bankafærslum og færslum. Þessar reglur eru hins vegar ósveigjanlegar og leiða oft til margra ósamræmdra færslna, sem hver þarfnast handvirkrar skoðunar og samanburðar. Copilot notar AI-tækni til að skoða þessar ósamræmdu færslur og auðkenna fleiri samsvörun, byggt á dagsetningum, upphæðum og lýsingum. Ef viðskiptamaður greiddi til dæmis marga reikninga í einni moldarsamtölu stemmir Copilot af eina bankayfirlitslínu við margar reikningsfærslur.

- Tillögur um fjárhagsreikninga

    Copilot notar AI-tækni til að bera færslulýsinguna saman við heiti fjárhagsreikninga og leggja síðan til líklegustu fjárhagsreikningana til að bóka á fyrir afgöngum bankafærslna sem ekki er hægt að para við færslur. Til dæmis ef ósamræmdar færslur hafa frásagnareldsneyti Stöðvun *24* gæti Copilot lagt til að þær séu bókaðar á *flutningsreikninginn* .

Copilot tengist ekki bankanum þínum til að sækja eða senda færslur. Þetta verk helst að fullu innan stjórnunar. Það er forsenda þess að nota aðstoð Copilot, óháð því hvort færslum er bætt við [!INCLUDE[prod_short](includes/prod_short.md)] með stafrænni bankatengingu, fluttar inn úr bankayfirlitsskrá eða handvirkt færðar inn.

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Hver er tilætluð aðstoð við bankaafstemmingu?

Aðstoð við afstemmingu bankareikninga er hönnuð til að auka nákvæmni fjárhags með því að hjálpa viðskiptamönnum að finna nýjar færslur sem þær eiga að gera grein fyrir í [!INCLUDE[prod_short](includes/prod_short.md)]. Það er ekki ætlað til greiningar á svikum eða til að greina hvort viðskiptavinir greiddu á réttum tíma.

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvernig var aðstoð við bankaafstemmingu metin? Hvaða mælieiningar eru notaðar til að mæla afköst?

Aðstoð við afstemmingu bankareikninga var prófuð með því að nota samsetningar tilbúins bankaviðskiptagagna og svipaðra fjárhagsreikninga og fjárhagsfærslna sem ná yfir dæmigerð frávik og gagnamörk hvers reits og á mismunandi tungumálum. Prófunargögn tákna bæði dæmigerða notkun og notkun slæmra leikara. Afköst voru mæld í samanburði við handvirka afstemmingu sömu gagna.

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-these-limitations-when-they-use-the-system"></a>Hverjar eru takmarkanir á bankaafstemmingu að aðstoða? Hvernig geta notendur minnkað áhrif þessara takmarkana þegar þeir nota kerfið?

Aðstoð við afstemmingu bankareikninga hentar best þegar heiti fjárhagsreikninga, færslulýsingar og lýsingar á bankafærslum eru allar á sama tungumáli. Blönduð tungumál eða blönduð tungumál fyrir færslulýsingar leiða oft til færri samsvörunar og tillagna.

Tillögur um fjárhagsreikninga framkvæma best á einu af studdu tungumálunum (sjá næsta kafla fyrir lista yfir tungumál). Notendur geta upplifað færri færslusamsvörur og færri fjárhagsreikninga sem lagt er til á öðrum tungumálum.

## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>Í hvaða landafræði og tungumálum er bankaafstemming tiltæk?

- Tiltæk landfræði

  Aðstoð við afstemmingu bankareikninga er tiltæk í öllum studdum [Business Central löndum/svæðum](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Fyrir umhverfi viðskiptavina sem staðsett eru í löndum/svæðum þar sem Azure OpenAI þjónusta er ekki virkjuð verða stjórnendur að hafa samþykki til að leyfa gögnum sínum að færast yfir mörk [!INCLUDE [prod_short](includes/prod_short.md)] til að tengjast Azure OpenAI þjónustu. Fræðast meira um [hreyfingu copilot gagna í landfræði](ai-copilot-data-movement.md).

- Tiltæk tungumál

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

Nánari upplýsingar um tungumál eru í fyrri spurningunni um takmarkanir.

## <a name="what-is-expected-of-system-users-when-they-operate-bank-account-reconciliation-assist"></a>Hvað er búist við af kerfisnotendum þegar þeir nota afstemmingu bankareikninga?

### <a name="during-bank-account-reconciliation"></a>Við afstemmingu bankareiknings

Ónýt samsvörun og tillögur gætu stundum verið rangar eða ófullnægjandi. Notendur afstemmingar bankareikninga verða að fara yfir nákvæmni samsvaranna og tillagna sem Copilot gefur áður en þeir velja að halda þeim. Samsvörun copilot og tillögur eru ekki vistaðar í gagnagrunninum [!INCLUDE[prod_short](includes/prod_short.md)] fyrr en þú velur **hnappinn Halda honum** og loka glugganum Copilot. Hægt er að breyta og leiðrétta samsvörun eða tillögur áður en valið er að halda þeim.

### <a name="after-bank-account-reconciliation-is-completed"></a>Eftir að afstemmingu bankareiknings er lokið

Mælt er með því að notendur sannreyni einnig nákvæmni og leiðrétti misræmi eftir að þeir loka glugganum Copilot. Þetta ferli ætti að fela í sér eftirfarandi aðgerðir:

- Farið yfir prófunarskýrslu afstemmingar.
- Tryggja þarf að fyrirtækið sé með viðeigandi endurskoðunar- og endurskoðunarferli á réttum stað.
- Opna aftur bókaðar afstemmingar með aðgerðinni **Afturkalla** .
- Leiðrétta allar rangar fjárhagsfærslur með bakfærðum bókunum á færslum.

## <a name="what-is-expected-of-administrators-and-system-users-when-they-operate-bank-account-reconciliation-assist"></a>Hvað er búist við af stjórnendum og notendum kerfisins þegar þeir stýra afstemmingu bankareikninga?

Kerfisnotendur, t.d. endurskoðendur, gjaldkerar eða aðrir sem vinna við viðskiptabókhald, ættu alltaf að fara yfir nákvæmni samsvarana og tillagna sem Copilot veitir áður en þeir velja að halda þeim. Eftir afstemmingu við Copilot er mælt með því að þessir notendur fari yfir afstemmingarprófunarskýrsluna til að votta nákvæmni og greina misræmi.

Stjórnendur ættu að tryggja að viðeigandi bókhaldsnotendum sé veittur aðgangur að þessari getu.

## <a name="is-copilot-the-only-means-of-completing-bank-account-reconciliation"></a>Er Afrita eini leiðin til að ljúka afstemmingu bankareikninga?

Nr. Notkun Copilot er valfrjáls. [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á hefðbundnar og ónýtar leiðir til að flytja inn bankayfirlit, keyra fyrirfram skilgreindar samsvarandi reglur og nota samsvörunir handvirkt og bóka á viðeigandi fjárhagsreikninga. Bæði hefðbundna aðferð og Copilot er hægt að nota samtímis í skipulagi.

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hvernig gef ég ábendingar um innihald myndaðs efnis?

Í hvert skipti sem Copilot býður upp á samsvörun eða tillögur er hægt að senda ábendingar til Microsoft beint úr glugganum Copilot með því að nota eins og (þumlur upp) og ólíkt (þumlum niður) stýringum. Ábendingar þínar eru nafnlausar og við notum þessi gögn til að bæta gæði þjónustunnar.

## <a name="see-also"></a>Sjá einnig .

[Stemma af bankareikninga við Afrita (forskoðun)](bank-reconciliation-with-copilot.md)
