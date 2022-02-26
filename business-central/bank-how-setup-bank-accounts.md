---
title: Setja upp bankareikninga (inniheldur Video)
description: Kynntu þér hvernig bankareikningar eru notaðir í Business Central og hvernig hægt er að stemma af upphæðir með bankanum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: 816b46e859fb4125c93346243f57f88b5f941a70
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029275"
---
# <a name="set-up-bank-accounts"></a>Bankareikningar settir upp

Þú notar bankareikninga í [!INCLUDE[prod_short](includes/prod_short.md)] til að fylgjast með bankafærslunum þínum. Hægt er að hafa reikninga í SGM eða erlendum gjaldmiðli. Þegar bankareikningar hafa verið settir upp er einnig hægt að nota valkostinn prentskoðun. Bankareikningarnir innihalda aukalega virkni fyrir [afstemmingu greiðslna](receivables-apply-payments-auto-reconcile-bank-accounts.md), [afstemmingu banka](bank-how-reconcile-bank-accounts-separately.md) og inn- og útflutning bankaskráa. Bankareikningarnir geta einnig verið teknir með í færslum í almennum færslubókum. Hver bankareikningur er tengdur við reikning í bókhaldslyklinum í gegnum tilskilinn bókunarflokk bankareiknings. Með því að nota bankareikning í greiðslufærslu verður færsla sjálfkrafa stofnuð bæði á bankareikningi og tengdum fjárhagsreikningi.  

Bankareikningar virka mismunandi eftir því hvort gjaldmiðilskóði er tilgreindur:

- Gjaldmiðilskóði er auður

  Allar færslur á bankareikningnum verða í staðbundnum gjaldmiðli (LCY) fyrir núverandi fyrirtæki. Ef færsla fer fram á reikningnum í öðrum gjaldmiðli eru upphæðirnar bókaðar á reikninginn í LCY samkvæmt viðkomandi gengi gjaldmiðils. Allar ávísanir sem eru gefnar út frá þessum reikningi verða að vera gefnar út í LCY. Ef bankareikningurinn er notaður í færslubók verður færslubókarlínan sjálfkrafa hluti af auðum gjaldmiðilskóða.  
- Gjaldmiðilskóði er tilgreindur

  Allar færslur sem eru gerðar á þennan reikning verða að vera í sama gjaldmiðli og tilgreindur er á reikningnum. Allar ávísanir sem eru gefnar út af þessum reikningi verða einnig að hafa þennan gjaldmiðil.  

Bankareikningur er samþættur hluti af [!INCLUDE[prod_short](includes/prod_short.md)] og gegnir hlutverki í mörgum öðrum möguleikum. Eftirfarandi mynd sýnir mikilvægustu tengslin:

![Skýring á tengslum bankareiknings.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Það þýðir að stofnun bankareiknings gerir hann aðgengilegan á öllum stöðum sem sýndir eru hér að ofan ásamt því að vera sýndir á viðkomandi fjárhagsreikningi og á síðunni **Fyrirtækjaupplýsingar**.

Yfirleitt er fylgst með bankareikningi daglega til að ganga úr skugga um að nýjar greiðslur frá viðskiptavinum séu skráðar eins fljótt og hægt er. Þetta tryggir að raunveruleg staða viðskiptavina endurspeglist í [!INCLUDE[prod_short](includes/prod_short.md)] þannig að sölufólk, endurskoðendur og aðrir starfsmenn hafi aðgang að viðeigandi og nýjustu upplýsingum. Þannig koma þeir í veg fyrir óþarfa hringingar til viðskiptavinar varðandi gjaldfallna reikninga eða seinkun á sendingum.  

![Skýring á bankagreiðslu.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Annað verk er að flytja inn gjaldmiðilsgreiðslur lánardrottins með raunverulegu gengi gjaldmiðils til að ganga úr skugga um að raunveruleg staða lánardrottna sé uppfærð. Auðveldasta leiðin til að tryggja að bankareikningurinn sé uppfærður er að nota möguleika [greiðsluafstemmingar](receivables-apply-payments-auto-reconcile-bank-accounts.md). Í **Greiðsluafstemmingarbók** er hægt að flytja inn bankafærslur beint frá netbanka og láta bóka þér meira og minna sjálfkrafa. Færslubókin greinir og bókar sjálfkrafa eftirfarandi:  

- Beingreiðslur frá viðskiptavinum  
- Greiðslur viðskiptavinar á stökum reikningum  
- Fastagreiðslur frá viðskiptavinum  
- Greiðslur viðskiptavinar í erlendum gjaldmiðlum  
- Greiðslur lánardrottna  
- Greiðslur lánardrottna í erlendum gjaldmiðli  
- Endurteknar greiðslur lánardrottna og áskriftir  
- Bankakostnaður og vextir  

Greiðsluafstemming sparar umtalsverðan tíma við bókun á greiðslum á innleið og útleið. Færslurnar á bankareikningnum í [!INCLUDE[prod_short](includes/prod_short.md)] eru hinsvegar ekki álitnar 100% réttar fyrr en bankaafstemming er keyrð.  

Bankaafstemming er notuð til að ganga úr skugga um að bankareikningurinn í [!INCLUDE[prod_short](includes/prod_short.md)] samsvari ytri reikningnum í bankanum.  

 ![Skýring á afstemming bankareiknings.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

Á myndinni hér að ofan táknar vinstri hliðin bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)] og hægri hliðin táknar færslurnar sem fluttar eru inn frá bankanum gegnum netbankann. Skýringarmyndin í miðjunni sýnir færslurnar frá báðum hliðum, sem er bankaafstemmingin.

Raunverulegi bankinn ætti að kannast við flestar færslur frá bankareikningnum í [!INCLUDE[prod_short](includes/prod_short.md)]. Einu undantekningarnar fela í sér eftirfarandi mál:  

- Leiðréttingar bókaðar í [!INCLUDE[prod_short](includes/prod_short.md)]  
- Útgefnar ávísanir sem ekki er búið að innleysa  
- Greiðslur lánardrottna sem bankinn hefur enn ekki samþykkt  

Frá raunverulegum reikningi í bankanum berast oft óþekktar færslur sem greiðsluafstemmingarbókin ber ekki kennsl á, t.d. eftirfarandi:  

- Nýjar áskriftir lánardrottins  
- Greiðslur viðskiptavina án lýsingar
- Bankavextir
- Bankakostnaður
- Kreditkortagjöld sem enn hafa ekki verið tilkynnt

Því betri sem kortlagning upplýsinga er í greiðsluafstemmingarbókinni, því fleiri færslur eru bókaðar sjálfkrafa og þeim mun auðveldari verður reglubundna bankaafstemmingin.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Sumir reitir geta innihaldið viðkvæm gögn eins og reitirnir **Útibúsnúmer banka**, **Bankareikningsnr.**, **SWIFT-kóði** og **IBAN-númer**. Frekari upplýsingar er að finna í [Fylgjast með viðkvæmum reitum](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Bankareikningar settir upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Á síðunni **bankareikningar** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Til dæmis tengir Bankareikn **reikningsflokkinn** bankareikninginn við undirliggjandi fjárhagsreikning í efnahagsreikningi. Frekari upplýsingar er að finna í [Setja upp bókunarflokka](finance-posting-groups.md).

> [!TIP]
> Sumir reitir eru faldir þar til þú velur aðgerðina **Sýna fleiri**, yfirleitt vegna þess að þeir eru sjaldan notaðir. Öðrum verður að bæta við með sérstillingu. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

Hægt er að stofna eins marga bankareikninga og þarf fyrir reksturinn. Fyrir hvern bankareikning þarf að tilgreina upplýsingar sem auðkenna bankareikninginn á einkvæman hátt. Þessar upplýsingar fela í sér heimilisfang bankans, númeraraðir fyrir mismunandi færslugerðir, eins og beingreiðslu og kreditfærslur, gjaldmiðilinn sem upphæðar eru gefnar upp í og upplýsingar sem eru notaðar til að flytja inn bankayfirlit. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->
> [!NOTE]
> Til að fylla út í reitinn **Staða** með onunarstöðu verður þú að bóka fjárhagsfærslu bankareiknings með upphæðinni. Hægt er að gera þetta með því að framkvæma afstemmingu bankareiknings. Frekari upplýsingar er að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).  
>
> Einnig er hægt að tiltaka opnunarstöðu sem hluta af almennri gagnamyndun í nýjum fyrirtækjum með því að nota **Flytja viðskiptagögn** leiðbeiningar um uppsetningu með hjálp. Nánari upplýsingar er að finna á [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).  

> [!IMPORTANT]
> Mikilvægt er að opnunarstaðan sé ekki bókuð beint í fjárhag. Ef færslur í fjárhagsreikningnum sem eru bókaðar beint á fjárhagsreikninginn leiða yfirleitt til þess að ekki er hægt að stemma bankareikninginn af, eða ef um er að ræða bankareikninga á erlendum gjaldmiðli, leiðir mismunur til þess að þú bókar meiri bankaafstemmingar. Oft er opnunarbankainnistaða bókuð beint á bankareikning og upphæðin endar síðan í fjárhagsreikningnum. Einnig er hægt að bakfæra hana síðar á móti tilgreindum fjárhagsreikningi sem notaður var til að jafna stöðu opnunarfjárhags. Í báðum tilvikum þarf að jafna beina bókun við fjárhagsreikninginn áður en fyrsta bankaafstemming hefst, og þá sérstaklega svo ef bankareikninginn er í erlendum gjaldmiðli.  

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Til að setja upp bankareikning þinn til að flytja inn eða flytja út bankaskrár

Reitir á **Flutningur** flýtiflipanum á síðunni **Bankareikningsspjald** eru tengdir innflutningi og útflutningi á bankastraumum og skrám. Nánari upplýsingar um það eru í [Notkun AMC Banking 365 Fundamentals viðbótarinnar](ui-extensions-amc-banking.md) og [Uppsetning Envestnet Yodlee Bank Feeds þjónustunnar](bank-how-setup-bank-statement-service.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Opnaðu kortið fyrir bankareikning sem þú vilt flytja út eða flytja inn bankaskrár fyrir.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Flytja**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Mismunandi útflutningsþjónusta skráa og snið þeirra þurfa mismunandi uppsetningargildi á síðunni **Bankareikningsspjald**. Þú færð að vita um uppsetningargildi sem eru röng eða sem vantar þegar þú reynir að flytja út skrána. Svo lestu stuttar lýsingar á reitunum vandlega eða vísaðu til viðkomandi efnisferlis. Til dæmis, við útflutning greiðsluskráar fyrir kortamillifærslu NA (EFT) þarf að fylla út reitina **Síðasta greiðslutilkynningarnúmer** og **Kenninúmer**. Frekari upplýsingar eru í [Flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Reitirnir í flýtiflipanum **Flutningur** á bankareikningnum þjóna mismunandi tilgangi, eftir því hvort greiðslan er á innleið eða útleið.

Myndin sýnir leið greiðslan á innleið:

:::row:::
    :::column:::
        1. Færslurnar eru fluttar út af bankareikningnum á annaðhvort læsilegu .csv-sniði eða sniði bankans.
        <br><br>
2. *Skilgreining gagnaskipta* varpar upplýsingunum í skránni í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Setja upp gagnaskipti](across-set-up-data-exchange.md)
<br><br>
3. *Uppsetning útflutnings/innflutnings gagna* skilgreinir innflutning eða útflutning og tengir hann við skilgreiningu gagnaskipta.
<br><br>
4. *Bankayfirlitin á innflutningssniðinu* tengja innflutningsuppsetninguna við bankareikninginn.
<br><br>
5. Greiðslurnar eru fluttar inn gegnum síðuna **Greiðsluafstemmingarbók** eða **Afstemming bankareiknings**.
    :::column-end:::
    :::column:::
        ![Mynd af greiðslum sem berast frá bankanum inn á bankareikninga.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

Greiðslur á innleið eru alltaf fluttar inn gegnum síðuna **Greiðsluafstemmingarbók** eða beint á síðuna **Afstemming bankareiknings**. Á hinn bóginn geta greiðslur á útleið komið úr hvaða greiðslubók sem er. Einu forsendurnar eru þær að velja þarf reitinn **Leyfa útflutning greiðslu** í viðkomandi runu greiðslubókar.

Myndin sýnir leið greiðslan á útleið:

:::row:::
    :::column:::
        6. Færslurnar eru fylltar út í greiðslubók sem hefur verið útbúin fyrir útflutning á greiðslum í skrá.
        <br><br>
        7. *Bankayfirlitin á innflutningssniðinu* tengja innflutningsuppsetninguna við bankareikninginn
        <br><br>
        8. *Uppsetning útflutnings/innflutnings gagna* skilgreinir innflutning eða útflutning og tengir við skilgreiningu gagnaskipta.
        <br><br>
        9. *Skilgreining gagnaskipta* varpar upplýsingunum í skránni í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Setja upp gagnaskipti](across-set-up-data-exchange.md)
        <br><br>
        10. Greiðslurnar eru fluttar út úr greiðslubókinni og fluttar inn á bankareikninginn
    :::column-end:::
    :::column:::
        ![Skýring á greiðslum af bankareikningum sem eru sendar til bankans.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa

Reitir á **Flutningur** flýtiflipanum á síðunni **Bankareikningsspjald lánardrottins** eru tengdir útflutningi á bankastraumum og skrám. Nánari upplýsingar um það eru í [Notkun AMC Banking 365 Fundamentals viðbótarinnar](ui-extensions-amc-banking.md) og [Flytja Greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Opnaðu kortið fyrir lánardrottinn með bankareikning sem þú sendir út greiðslubankaskrár til.
3. Veldu aðgerðina **Bankareikningar**.
4. Af **Lista yfir reikninga lánardrottins** skal velja viðeigandi bankareikning eða bæta við nýjum bankareikningi.  
5. Á síðunni **Bankareikn.spjald lánardr** á flipanum **Flutningur** fylltu inn reitina eftir því sem þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!WARNING]
> Sumir reitir í bankareikningi lánardrottins innihalda viðkvæm gögn eins og reitirnir **Útibúsnúmer banka**, **Bankareikningsnr.**, **SWIFT-kóði** og **IBAN-númer**. Frekari upplýsingar er að finna í [Fylgjast með viðkvæmum reitum](across-log-changes.md#monitoring-sensitive-fields).

## <a name="changing-your-bank-account"></a>Bankareikningnum breytt

Ef nota á annan bankareikning fyrir reksturinn þarf að stofna nýja bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)]. Mælt er með því að nota ekki upplýsingar um reikninginn sem er nú í notkun vegna þess að það getur leitt til rangra gagna. Til dæmis gæti opnunarstaðan verið röng eða bankagjaldið gæti hætt að virka á réttan hátt. Það er mikilvægt að halda núverandi og nýjum reikningum aðskildum.

Eftir að nýi bankareikningurinn hefur verið stofnaður ættir þú einnig að stofna nýjan bókunarflokk bankans og úthluta honum á nýjan fjárhagslykil. Þú getur endurnotað fyrirliggjandi bókunarflokk bankans og bankafærslur verða bókaðar á sömu fjárhagslyklana eins og hinir bankareikningarnir sem deila bókunarflokki bankans. Hins vegar er mælt með því að stofna nýjan bókunarflokk bankans og fjárhagslykil svo afstemmingarnar verði auðveldari.

> [!NOTE]
> Mundu að upplýsingar um bankareikning á opnum sölureikningum sýna enn upprunalega bankareikninginn. Samkvæmt því er líklegt að greiðslur verði enn bókaðar á þann reikning. Við mælum með því að þú haldir báðum reikningunum virkum í ákveðið langan tíma eftir breytinguna.

Til að fá samþjappaðra yfirlit yfir sjóðsreikninga í fjárhagsskýrslugerð skal nota reikningana **Samtala í upphafi** og **Samtala í lok** í bókhaldslyklinum, línurnar **Samtölur** í fjárhagsskemum eða flokkum fjárhagsreikninga. Frekari upplýsingar er að finna í hlutanum [Viðskiptagreind og Financial Reporting](bi.md).

## <a name="see-also"></a>Sjá einnig

[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Uppsetning bókunarflokka](finance-posting-groups.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[SEPA-beingreiðsla í Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Setja upp bankareikning fyrir SEPA-beingreiðslu](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Setja upp bankareikning fyrir SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Greiða með AMC Banking 365 Fundamentals viðbótinni eða SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Greiðsluafstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Skilja fjárhag og bókhaldslykil](finance-general-ledger.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
