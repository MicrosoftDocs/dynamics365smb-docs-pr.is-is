---
title: Nota AMC Banking 365 Fundamentals viðbótina
description: Kynntu þér hvernig á að skiptast á gögnum við bankann á greiðlegan hátt með því að umbreyta gögnum í það snið sem krafist er.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank, format, data'
ms.search.form: '20100, 20101, 20102, 20105, 20106, 20107, 20109,'
ms.date: 09/20/2022
ms.author: bholtorf
---

# Nota AMC Banking 365 Fundamentals viðbótina

AMC Banking 365 Fundamentals viðbótin gerir það auðveldar sendingu gagna til bankans þíns og eykur áreiðanlega þeirra. Viðbótin tengir [!INCLUDE[prod_short](includes/prod_short.md)] við AMC Banking 365 Fundamentals fyrir Microsoft Dynamics 365 Business Central þjónustu sem getur breytt bankagögnum úr [!INCLUDE[prod_short](includes/prod_short.md)] í snið sem yfir 600 bankar í heiminum krefjast. Þannig er til dæmis auðveldara að millifæra greiðslur og kreditfærslur til lánardrottna með því að slá greiðslurnar inn í [!INCLUDE[prod_short](includes/prod_short.md)] og hlaða þeim svo upp í bankann þinn. Sniðin geta einnig jafnað út bankaafstemmingarferli. Frekari upplýsingar er að finna í [AMC Banking fyrir Microsoft Dynamics 365 Business Central](https://www.amcbanking.com/bc-fundamentals/).

> [!NOTE]
> AMC Banking hefur byggt aukalegar viðbætur sem virka með [!INCLUDE[prod_short](includes/prod_short.md)]. Þetta efnisatriði lýsir aðeins Fundamental-viðbótinni.

> [!NOTE]
> Í almenn útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)], er altæk þjónustuveita til að umbreyta bankagögnum í annað skráarsnið sem bankinn krefst að er uppsett og tengt. Í norður-amerískum útgáfum má nota sömu þjónustu til að senda greiðsluskrár sem rafræna millifærslu (EFT), t.d. kerfi rafrænnar greiðslumiðlunar sem er oft notuð, en með örlítið öðruvísi leiðum.

## Nota sýnireikning okkar

[!INCLUDE[prod_short](includes/prod_short.md)] fylgir með sýnireikningi sem gerir þér kleift að prófa AMC Banking 365 Fundamentals-viðbótina. Við bjóðum upp á sjálfgefnar stillingar fyrir tengingu við AMC Banking, þar sem bankareikningar eru tilgreindir til að sækja gögn frá [!INCLUDE[prod_short](includes/prod_short.md)], auk nokkurra gagnaskiptaskilgreininga. Þú getur skoðað tengingarstillingarnar á síðunni **AMC Banking Uppsetning**. Fyrir bankareikninga bætir viðbótin gildum í reitina **Heiti banka**, **Nr. á skilaboðum kreditfærslu**, **Innflutningssnið bankayfirlits** og **Greiðsluútflutningssnið** á bankareikningspjöldum.

Við veitum stillingarnar en til að prófa viðbótina verður þú að keyra leiðbeiningar um uppsetningu með hjálp til að nota þær. Til að keyra leiðarvísinn, á síðunni **AMC Banking Uppsetning**, skaltu velja aðgerðina **Uppsetning með hjálp**.

> [!NOTE]
> Einhverjar takmarkanir eru á sýnireikningnum. Til dæmis þegar greiðslum er umbreytt mun upphæðin í umbreyttu skránni ekki passa við raunverulegu upphæðina. Í staðin verður upphæðin alltaf fimm einingar af gjaldmiðlinum sem þú notar fyrir greiðslur.  

## Uppsetning viðbótarinnar

Að hefjast handa felur aðeins í sér nokkur einföld skref og leiðbeiningar um uppsetningu með hjálp munu koma á tengingunni og kveikja á viðbótinni. Leiðbeiningin mun gera hluti eins og að setja upp gagnaskiptaskilgreiningar fyrir uppsetningar á útflutningi/innflutningi bankayfirlits og byrja á númeraröðum sem eru notaðar fyrir skilaboð kreditfærslna.  

### Til að setja upp áskildar heimildasamstæður

Áður en hægt er að nota þessa viðbót verður stjórnandi að afrita eftirfarandi heimildasamstæður, breyta þeim og síðan úthluta nýjum heimildasamstæðum til notenda í staðinn fyrir þær upprunalegu:

* **D365 Grunnútgáfa**
* **D365-teymismeðlimur**
* **D365-upplýsingar**
* **IntelligentCloudBC**

Nánari upplýsingar er að finna í [Til að afrita heimildasamstæðu](ui-define-granular-permissions.md#to-copy-a-permission-set).

Fyrir hverja nýja heimildasamstæðu skal aðeins veita heimildina **Lesa** fyrir **AMC Banking Uppsetningartafla (20101)**. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildum handvirkt](ui-define-granular-permissions.md#to-create-a-permission-set).

### Til að tengja viðbótina við AMC Banking

1. Fá einingu og þjónustuáætlun fyrir AMC Banking. Til að gera það skaltu fara á [AMC leyfissíðuna](https://license.amcbanking.com/register).
2. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **AMC Banking Uppsetning** og velja síðan viðkomandi tengil.  
3. Á síðunni **AMC Banking Uppsetning**, skaltu velja aðgerðina **Uppsetning með hjálp**.
4. Ljúka skal skrefunum í leiðbeiningum um uppsetningu með hjálp.

### Til að tengja bankareikninga við viðbótina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Opnaðu spjaldið fyrir bankareikninginn sem þú vilt tengja við þjónustuna.
3. Í reitnum **Heiti banka** skaltu velja sniðið sem bankinn krefst.  

   Sniðin eru síuð til að sýna aðeins þau sem skipta máli fyrir landið/svæðið sem er tilgreint fyrir bankareikninginn.
4. Í reitnum **Númer fyrir skilaboð kreditfærslu** skaltu velja númeraröðina sem nota á fyrir skilaboð sem fylgja greiðslum.
5. Í reitunum **Innflutningssnið bankayfirlits** og **Greiðsluútflutningssnið** skal velja þær gagnaskiptaskilgreiningar sem bankinn krefst.

## Nota viðbótina

Ef þú notar þessa viðbót þarf aðeins að flytja út gögn á síðunni **Greiðslubækur** og síðan hlaða þeim upp á vefþjónustu bankans. Nánari upplýsingar er að finna í [Greiða með umreikningsþjónustu bankagagna eða SEPA kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!NOTE]
> Þú verður að fylla út reitina **SWIFT kóði** og **IBAN** fyrir hvern bankareikning.

### Til að flytja út gögn og senda þau í bankann þinn

> [!CAUTION]  
> Þegar þú flytur út gögn með AMC Banking 365 Fundamentals viðbótinni, mun sá sem veitir þjónustuna geta séð eitthvað af gögnunum. Þjónustuveita, AMC Consult A/S, er ábyrg fyrir persónuvernd gagnanna. Nánari upplýsingar er að finna í [AMC-persónuverndarstefnu](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.
2. Stofna skal færslubókarlínurnar sem á að flytja út.  

   > [!NOTE]
   > Fyrir hverja línu skaltu muna að velja **Rafræn greiðsla** í reitnum **Tegund bankagreiðslu**.
3. Veldu **Export** aðgerðina.

### Til að flytja inn og nota umbreyttu skrána

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluafstemmingarbók** og velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Flytja inn bankafærslur** og svo umbreyttu skrána.  

   [!INCLUDE[prod_short](includes/prod_short.md)] stofnar nýja greiðsluafstemmingarbók sem inniheldur gögnin í skránni. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## Sjá einnig .

[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
