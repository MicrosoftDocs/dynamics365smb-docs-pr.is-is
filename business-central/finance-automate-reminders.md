---
title: Áminningar sjálfvirkar í söfnum
description: 'Spara tíma í söfnum með því að gera vinnslur við stofnun, útgáfu og sendingu innheimtubréfa til viðskiptamanna sjálfvirka.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="automate-reminders-in-collections"></a>Áminningar sjálfvirkar í söfnum

Gera söfnin virkari með því að gera stofnun, útgáfu og sendingu innheimtubréfa til viðskiptamanna. Sjálfvirkni getur dregið verulega úr þeim tíma sem eytt er í söfn, veitt betri yfirsýn yfir ferlið og veitt fulla stjórn á hverju þrepi.

Á síðunni **Sjálfvirkni** innheimtubréfs eru tilgreindar einstakar aðgerðir (þrep). Hægt er að sameina skrefin til að stofna, senda og senda áminningar eða stofna sérstaka sjálfvirkni fyrir hvert skref ef það er betra fyrir söfnunarferlið. Sjálfvirkni byggist á áminningarskilmálum og áminningarstigum. Nánari upplýsingar eru settar upp með því að fara í [Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md). Hægt er að setja afmarkanir á áminningarskilmála fyrir sjálfvirkni í heild og setja afmarkanir fyrir hverja aðgerð í sjálfvirkninni. Þú getur einnig hengt útistandandi reikninga við tölvupóst sem PDF skrár.

Sjálfvirkni gerist í gegnum verkraðarfærslu. Þegar sjálfvirkni er sett upp er reiturinn **Cadence** notaður til að tilgreina hvernig og hvenær hún er keyrð. Ef valið er **Handvirkt** keyrir sjálfvirknin einu sinni þegar aðgerðin **Hefja** er notuð. Einnig er hægt að velja **Vikulega**, **Mánaðarlega** eða velja **Sérsnið** til að setja upp nákvæmari cadence. Ef Valið er **Sérstilla** verður að færa inn dagsetningarreiknireglu. Nánari upplýsingar um hvernig dagsetningarreikniregla er færð inn er farið í [Nota dagsetningarreiknireglur](ui-enter-date-ranges.md#use-date-formulas). Þegar annar valkostur en **Handfært** er valinn keyrir sjálfvirknin þar til hlé er gert til að setja hana í bið. Ef þörf er á enn nákvæmari um það hvenær hún er keyrð skal nota aðgerðina **Verkraðarfærslur** til að opna **síðuna Verkraðarfærslur** og leiðrétta endurtekninguna, til dæmis á daglegan eða tiltekinn virkan dag.

## <a name="automate-the-reminders-flow"></a>Gera áminningarflæði sjálfvirkt

Eftirfarandi hlutar lýsa því hvernig á að setja upp áminningar til að stofna, senda og senda sjálfkrafa.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **sjálfvirkni** innheimtubréfa og velja síðan viðeigandi tengil.
1. Velja Nýtt **og** fylla síðan út reitina á flýtiflipanum **Almennt** .
1. Í reitnum **Skilmálaafmörkun** innheimtubréfa er valið skilmálar innheimtubréfs eða skilmálar sem þessi sjálfvirkni á við.
1. Í reitnum **Cadence** er valið hversu oft sjálfvirknin keyrir.
1. Á flýtiflipanum **Aðgerðir** skal velja **Nýtt** og velja svo hvort sjálfvirknin stofnar, sendir eða sendir áminningar. Velja **Í lagi**.
1. Eftir því hver tegund aðgerðarinnar sjálfvirknin framkvæmir þarf að fylla út reitina eins og þörf krefur á uppsetningarsíðunni. Nánari upplýsingar um stillingarnar eru í [Stillingar fyrir áminningaraðgerðir](#settings-for-reminder-actions).
1. Þegar aðgerðirnar fyrir sjálfvirknina hafa verið settar upp er hægt að nota **aðgerðirnar Færa upp** og **Færa niður** til að aðlaga í hvaða röð þær eru keyrðar.

## <a name="settings-for-reminder-actions"></a>Stillingar fyrir áminningaraðgerðir

Uppsetningarstillingarnar eru mismunandi fyrir aðgerðirnar Stofna, Senda og Senda áminningu. Hér á eftir er því lýst hvernig á að nota þá.

### <a name="create"></a>Stofna

* Velja hæsta stigið í öllum innheimtubréfslínum.  
* Stofna áminningar fyrir færslur sem eru í bið. Þessi stilling er til dæmis gagnleg ef deilt er um það við viðskiptamann og vill að þær sjái stóru myndina.
* Stofna áminningar fyrir alla ógreidda reikninga, en ekki bara reikninga sem eru gjaldfallnir. Skýrslan birtir gjaldfallna reikninga og reikninga sem eru ógreiddir en ekki gjaldfallnir í sérstökum hlutum.
* Afmarkanir eru settar til að gera innheimtubréfið nánar.

### <a name="issue"></a>Útgáfa

Þegar innheimtubréf er sent eru stofnaðar færslur í viðskiptamannabók með bókunardagsetningu og skattdagsetningu. Nota skal stillingarnar á síðunni **Uppsetning** innheimtubréfa til að tilgreina hvort skipta eigi þeim upplýsingum á innheimtubréfi út með upplýsingum úr því innheimtubréfi sem stofnað var. Ef innheimtubréf var til dæmis stofnað í gær og það var sent í dag færist gjalddaginn einn dagur.

### <a name="send"></a>Senda

> [!NOTE]
> Sjálfvirkni sendingar krefst þess að tölvupóstur sé settur upp. [!INCLUDE [prod_short](includes/prod_short.md)] Til að fá nánari upplýsingar um uppsetningu tölvupósts er farið í [Setja upp tölvupóst](admin-how-setup-email.md).

Efni tölvupóstsins, svo sem viðhengi, texti í meginmáli tölvupósts og tungumál koma úr uppsetningu áminningartímabilsins. Nánari upplýsingar um stillingar tölvupósts fást í [Setja upp áminningarskilmála og stig](finance-setup-reminders.md).

Nota skal stillingarnar á síðunni **Uppsetning** innheimtubréfa með eftirfarandi:

* Almennar stillingar, t.d. lýsing, og hversu oft sama innheimtubréf er sent.
* Stillingar fyrir það sem á að taka með í innheimtubréfi.
* Stillingar til að rekja áminningarnar sem sendar eru með því að stofna samskipti, hvort sem áminning er prentuð eða send með tölvupósti og hvort ætlunin sé eingöngu að hengja við gjaldfallna reikninga, alla reikninga eða enga reikninga. 

## <a name="access-the-history-of-a-reminder"></a>Aðgangur að sögu áminningar

[!INCLUDE [prod_short](includes/prod_short.md)] helst utan um í hvert sinn sem sjálfvirkni er keyrð. Hægt er að komast í ferilinn með því að velja **kladdafærslur** . Einnig er hægt að nota aðgerðina **Send innheimtubréf** til að fá aðgang að lista yfir þau innheimtubréf sem send hafa verið.

## <a name="handle-errors"></a>Meðhöndla villur

Á flýtiflipanum **Aðgerðir** er hægt að tilgreina fyrir hverja aðgerð hvort sjálfvirknin eigi að stöðvast ef villa er í aðgerðinni. Ef það er gert vinnur sjálfvirknin ekki aðgerðirnar sem koma á eftir. Til að kveikja eða slökkva á þessari aðgerð skal nota **Stilla stöðvun á villu** eða **Hreinsa stöðvun á villuaðgerðum** .

## <a name="change-action-settings-for-an-automation"></a>Breyta aðgerðastillingum sjálfvirkni

Hægt er að breyta stillingum sjálfvirkni hvenær sem er. Á flýtiflipanum **Aðgerðir** skal velja **Uppsetning** og gera síðan breytingarnar.

## <a name="see-also"></a>Sjá einnig .

[Setja upp skilmála og stig innheimtubréfa](finance-setup-reminders.md)  
[Senda innheimtubréf vegna útistandandi stöðu](receivables-send-reminders.md)  
