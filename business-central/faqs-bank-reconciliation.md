---
title: Algengar spurningar fyrir afstemmingu bankareikninga (forskoðun) með Copilot
description: 'Í þessari algengu upplýsingar eru upplýsingar um tækni sem er notuð til að stemma af bankareikninga og yfirlit Business Central. Í honum eru lykilatriði og upplýsingar um notkun ÓM, hvernig það var prófað og metið og allar sérstakar takmarkanir.'
ms.date: 11/07/2023
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

# Algengar spurningar fyrir afstemmingu bankareikninga (forskoðun) með Copilot

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Þessar algengu spurningar (FAQ) lýsa algengum áhrifum stjórnunaraðstoðar við afstemmingu bankareikninga í [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Hvað er aðstoð við bankaafstemmingu?

Bankaafstemming er sameiginlegt bókhaldsverk þar sem fyrirtæki fara yfir bankareikningsyfirlit sín til að auðkenna færslur sem á að skrá inn [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi verkhluti væri til dæmis notaður til að bera kennsl á reglubundin bankagjöld eða lítil útgjöld starfsmanna. Þessi verkhluti er yfirleitt margþrepa ferli sem byrjar á að flytja bankayfirlit inn í [!INCLUDE[prod_short](includes/prod_short.md)] ásamt því að samsvara færslum og fjárhagsfærslum og bóka nýjar færslur til að endurspegla afgangsfærslur sem ekki voru áður þekktar við fjárhaginn. Copilot dregur [!INCLUDE[prod_short](includes/prod_short.md)] úr handvirku átaki með því að passa við fleiri færslur og leggja til fjárhagsreikninga sem hægt er að bóka á. 

## Hvað er hægt að aðstoða við bankaafstemmingu?

Copilot veitir alhliða aðstoð við tvo aðskilda verkhluta: 

- Bætt samsvörun færslna með fjárhagsfærslum 

   [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á sjálfvirkar reglur sem samsvara sjálfkrafa mörgum bankafærslum og færslum. Þessar reglur eru hins vegar ósveigjanlegar og hafa oft í för með sér margar ósamræmdar færslur sem hver krefst handvirkrar skoðunar og samanburðar. Copilot notar tækni viðmóts til að skoða eftirstandandi færslur og auðkenna fleiri samsvörun, byggt á dagsetningum, upphæðum og lýsingum. Ef til dæmis margir reikningar voru greiddir sem ein moldarsamtala af viðskiptamanni stemmir Copilot af eina bankayfirlitslínu við margar reikningsfærslur. 
 
- Tillögur um fjárhagsreikninga 

   Copilot notar AI-tækni til að bera færslulýsinguna saman við heiti fjárhagsreikninga og leggur til líklegustu fjárhagsreikningana til að bóka á fyrir afviknar bankafærslur. Til dæmis gæti Copilot lagt til að færsla með frásögninni "Eldsneytisstöð24" verði bókuð á "flutningsreikninginn". 

Copilot tengist ekki bankanum þínum til að sækja eða senda færslur. Þessi verk helst að fullu innan eftirlits og er forsenda þess að byrja á aðstoð Copilot, hvort þeim færslum er bætt við [!INCLUDE[prod_short](includes/prod_short.md)] með stafrænni bankatengingu, fluttar inn úr bankayfirlitsskrá eða handfærðar. 

## Hver er tilætluð aðstoð við bankaafstemmingu?

Aðstoð við afstemmingu bankareikninga er hönnuð til að auðkenna nýjar færslur sem viðskiptamenn eiga að gera grein fyrir í [!INCLUDE[prod_short](includes/prod_short.md)], til að auka nákvæmni fjárhags sinna. Þessi aðgerð er ekki ætluð til greiningar á svikum eða greiningu á því hvort viðskiptavinir hafa greitt tímanlega.   

## Hvernig var aðstoð við bankaafstemmingu metin? Hvaða mælieiningar eru notaðar til að mæla afköst?

Þessi aðgerð var prófuð með því að nota samsetningar tilbúinna bankaviðskiptagagna og svipaðra fjárhagsreikninga og fjárhagsfærslna sem ná til dæmigerðra frávika og gagnatakmarkana fyrir hvern reit og á mismunandi tungumálum. Prófunargögn tákna bæði dæmigerða notkun og notkun slæmra leikara. Afköst voru mæld í samanburði við handvirka afstemmingu sömu gagna. 

## Hverjar eru takmarkanir á bankaafstemmingu að aðstoða? Hvernig geta notendur minnkað áhrif takmarkana á bankaafstemmingu þegar kerfið er notað?

Aðstoð við afstemmingu bankareikninga hentar best þegar heiti fjárhagsreikninga, færslulýsingar og lýsingar á bankafærslum eru allar á sama tungumáli. Blönduð tungumál eða blandað tungumál færslulýsinga leiða oft til færri samsvörunar og tillagna. 

Tillögur um fjárhagsreikninga henta best á ensku. Þó að hægt sé að nota þessa aðgerð á einhverju tiltæku [!INCLUDE[prod_short](includes/prod_short.md)] tungumáli gætu notendur upplifað færri færslusamsvörur og færri fjárhagsreikninga sem lagt er til á öðrum tungumálum. 
<!--

## What operational factors and settings allow for effective and responsible use of the feature?


-->
## Í hvaða landafræði og tungumálum er bankaafstemming tiltæk? 

Þessi möguleiki er tiltækur fyrir hvaða umhverfisland/svæði sem er og á hvaða tungumáli sem er. Fyrir umhverfi viðskiptavina sem staðsett eru í löndum/svæðum þar sem Azure OpenAI þjónusta er ekki virkjuð verða stjórnendur fyrst að hafa samþykki til að leyfa hreyfingu gagna þvert á mörk [!INCLUDE[prod_short](includes/prod_short.md)] til að tengjast Azure OpenAI þjónustu og til að þessi möguleiki sé tiltækur. 

Nánari upplýsingar um tungumál eru í fyrri spurningu um takmarkanir.  

## Hvers er búist við afstemmingu bankareikninga við afstemmingu bankareikninga? 

### Afstemming bankareikninga notuð 

Ónýt samsvörun og tillögur gætu stundum verið rangar eða ófullnægjandi. Notendur afstemmingar bankareikninga verða að fara yfir nákvæmni samsvörunar og tillagna Copilot áður en kosið er að halda þeim. Samsvörun og tillögur Copilot eru ekki vistaðar í gagnagrunninum [!INCLUDE[prod_short](includes/prod_short.md)] fyrr en þú velur hnappinn Halda honum og loka glugganum Copilot. Einnig er hægt að breyta og leiðrétta samsvörun eða tillögur áður en valið er að halda honum. 

### Eftir að afstemmingu bankareiknings hefur verið lokið 

Mælt er með því að notendur sannreyni einnig nákvæmni og leiðrétti misræmi eftir að farið er út úr glugganum Copilot, þar á meðal eftirfarandi aðgerðir: 

- Farið yfir prófunarskýrslu afstemmingar. 
- Tryggja að fyrirtækið sé með viðeigandi endurskoðunar- og endurskoðunarferli. 
- Opna aftur bókaðar afstemmingar með aðgerðinni Afturkalla. 
- Leiðrétta allar rangar fjárhagsfærslur með bakfærðum bókunum á færslum. 

## Til hvers er vænst af stjórnendum og notendum við afstemmingu bankareikninga? 

Notendur eins og endurskoðendur, gjaldkerar eða aðrir sem vinna við viðskiptabókhald ættu ávallt að fara yfir nákvæmni samsvöruna og tillögur sem Copilot gefur áður en valið er að halda þeim. Þegar copilot hefur verið stemmt af er mælt með því að fara yfir prófunarskýrslu afstemmingar til að sannreyna nákvæmni og greina misræmi. 

Stjórnendur ættu að tryggja að viðkomandi bókhaldsnotendum hafi verið veittur aðgangur að þessari getu. 

## Er Afrita eini leiðin til að ljúka afstemmingu bankareikninga? 

Engin – notkun Copilot er valfrjáls. [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á hefðbundnar og ónýtar leiðir til að flytja inn bankayfirlit, keyra fyrirfram skilgreindar samsvarandi reglur og nota samsvörunir handvirkt og bóka á viðeigandi fjárhagsreikninga. Bæði hefðbundna aðferð og Copilot er hægt að nota samtímis innan fyrirtækis. 

## Hvernig gef ég ábendingar um innihald myndaðs efnis?

Í hvert sinn sem Copilot leggur fram samsvörun eða tillögur er hægt að senda ábendingar til Microsoft beint í glugganum Copilot með því að nota eins og mislíkindi. Svörun þín er nafnlaus og við notum þessi gögn til að bæta gæði þjónustunnar.


## Sjá einnig .

[Stemma af bankareikninga með aðstoð bankaafstemmingar (forskoðun)](bank-reconciliation-with-copilot.md)
