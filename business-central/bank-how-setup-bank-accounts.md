---
title: Upspetning bankareikninga (inniheldur myndskeið)
description: Kynntu þér hvernig bankareikningar eru notaðir í Business Central og hvernig hægt er að stemma af upphæðir með bankanum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 01/24/2022
ms.author: edupont
---
# Bankareikningar settir upp

Þú notar bankareikninga í [!INCLUDE[prod_short](includes/prod_short.md)] til að fylgjast með bankafærslunum þínum. Hægt er að hafa reikninga í SGM eða erlendum gjaldmiðli. Þegar bankareikningar hafa verið settir upp er einnig hægt að nota valkostinn prentskoðun. Bankareikningarnir innihalda aukalega virkni fyrir [afstemmingu greiðslna](receivables-apply-payments-auto-reconcile-bank-accounts.md), [afstemmingu banka](bank-how-reconcile-bank-accounts-separately.md) og inn- og útflutning bankaskráa. Bankareikningarnir geta einnig verið teknir með í færslum í almennum færslubókum. Hver bankareikningur er tengdur við reikning í bókhaldslyklinum í gegnum tilskilinn bókunarflokk bankareiknings. Með því að nota bankareikning í greiðslufærslu verður færsla sjálfkrafa stofnuð bæði á bankareikningi og tengdum fjárhagsreikningi.  

Bankareikningar virka mismunandi eftir því hvort gjaldmiðilskóði er tilgreindur:

- Ef gjaldmiðilskóði er auður

  Allar færslur á bankareikningnum verða í staðbundnum gjaldmiðli (SGM) fyrir núverandi fyrirtæki. Ef færsla fer fram á reikningnum í öðrum gjaldmiðli eru upphæðirnar bókaðar á reikninginn í LCY samkvæmt viðkomandi gengi gjaldmiðils. Allar ávísanir sem eru gefnar út frá þessum reikningi verða að vera gefnar út í SGM. Ef bankareikningurinn er notaður í færslubók verður færslubókarlínan sjálfkrafa hluti af auðum gjaldmiðilskóða.  
  
- Gjaldmiðilskóði er tilgreindur

  Allar færslur sem gerðar eru fyrir og ávísanir gefnar út frá þessum reikningi verða að vera í sama gjaldmiðli og tilgreindur er á reikningnum.

Þú getur sparað þér tíma við gagnafærslu með því að gera bankareikning sjálfgefinn reikning sem á að nota fyrir gjaldmiðilinn sem tilgreindur er fyrir reikninginn. Ef þú gerir það er reikningnum úthlutað á sölu- og þjónustuskjöl sem nota gjaldmiðilinn. Til að gera reikninginn sjálfgefinn fyrir sölu- og þjónustuskjöl, á síðunni **Bankareikningsspjald**, skaltu kveikja á **Nota sem sjálfgefið fyrir gjaldmiðil**. Ef þörf krefur er hægt að velja annan reikning þegar unnið er í skjali.

Bankareikningur er samþættur hluti af [!INCLUDE[prod_short](includes/prod_short.md)] og gegnir hlutverki í mörgum öðrum möguleikum. Eftirfarandi mynd sýnir mikilvægustu tengslin:

![Skýring á tengslum bankareiknings.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Þú sérð að stofnun bankareiknings gerir hann aðgengilegan á öllum stöðum sem sýndir eru hér að ofan ásamt því að vera sýndir á viðkomandi fjárhagsreikningi og á síðunni **Fyrirtækjaupplýsingar**.

Yfirleitt er fylgst með bankareikningi daglega til að ganga úr skugga um að nýjar greiðslur frá viðskiptavinum séu skráðar eins fljótt og hægt er. Þetta hjálpar til við að tryggja að raunveruleg staða viðskiptamanns komi fram í [!INCLUDE[prod_short](includes/prod_short.md)]. Það veitir sölufólki, endurskoðendum og öðrum starfsmönnum aðgang að mikilvægustu og nýjustu upplýsingum svo að þeir forðist að hringja í viðskiptamanninn að óþörfu vegna reikninga á gjalddaga eða tafa á sendingum.  

![Skýring á bankagreiðslu.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Annað verk er að flytja inn gjaldmiðilsgreiðslur lánardrottins með raunverulegu gengi gjaldmiðils til að ganga úr skugga um að raunveruleg staða lánardrottna sé uppfærð. Að nota möguleikann [greiðsluafstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md) er auðveldasta leiðin til að gera þetta. Í **Greiðsluafstemmingarbók** er hægt að flytja inn bankafærslur beint frá netbanka og láta bóka þér meira og minna sjálfkrafa. Færslubókin greinir og bókar sjálfkrafa eftirfarandi:  

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

Á myndinni hér að ofan táknar vinstri hliðin bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)] og hægri hliðin táknar færslurnar sem fluttar eru inn frá bankanum gegnum netbankaforritið. Skýringarmyndin í miðjunni sýnir færslurnar frá báðum hliðum, sem er bankaafstemmingin.

Raunverulegi bankinn ætti að kannast við flestar færslur frá bankareikningnum í [!INCLUDE[prod_short](includes/prod_short.md)]. Þær fáu undantekningar fela í sér eftirfarandi tilvik:  

- Leiðréttingar bókaðar í [!INCLUDE[prod_short](includes/prod_short.md)]  
- Útgefnar ávísanir sem ekki er búið að innleysa 
- Greiðslur lánardrottna sem bankinn hefur ekki enn samþykkt  

Frá raunverulegum reikningi í bankanum berast oft færslur sem greiðsluafstemmingarbókin ber ekki kennsl á, t.d. eftirfarandi:  

- Nýjar áskriftir lánardrottins  
- Greiðslur viðskiptavina án lýsingar
- Bankavextir
- Bankakostnaður
- Kreditkortagjöld sem hafa ekki verið tilkynnt

Því betri sem þú ert í að kortleggja upplýsingar í greiðsluafstemmingarbókinni, því fleiri færslur eru bókaðar sjálfkrafa og þeim mun auðveldari verður reglubundna bankaafstemmingin.

Sjá í myndbandinu hér að neðan grunnskref til að setja upp bankareikning í [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Sumir reitir geta innihaldið viðkvæm gögn eins og reitirnir **Útibúsnúmer banka**, **Bankareikningsnr.**, **SWIFT-kóði** og **IBAN-númer**. Frekari upplýsingar er að finna á [Fylgst með viðkvæmum reitum](across-log-changes.md#monitoring-sensitive-fields).

## Bankareikningar settir upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar**, velja síðan viðkomandi tengil.
2. Á síðunni **bankareikningar** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Dæmi væri reiturinn **Bókunarflokkur bankareiknings** sem tengir bankareikninginn við undirliggjandi fjárhagsreikning í efnahagsreikningnum. Frekari upplýsingar er að finna á [Uppsetning bókunarflokka](finance-posting-groups.md).

> [!TIP]
> Sumir reitir eru faldir þar til þú velur aðgerðina **Sýna fleiri**, yfirleitt vegna þess að þeir eru sjaldan notaðir. Öðrum verður að bæta við með sérstillingu. Frekari upplýsingar er að finna á [Sérstilling verksvæðis](ui-personalization-user.md).

Hægt er að stofna eins marga bankareikninga og þarf fyrir reksturinn. Fyrir hvern bankareikning þarf að tilgreina upplýsingar sem auðkenna bankareikninginn á einkvæman hátt. Þessar upplýsingar fela í sér heimilisfang bankans, númeraraðir fyrir mismunandi færslugerðir, eins og beingreiðslu og kreditfærslur, gjaldmiðilinn sem upphæðar eru gefnar upp í og upplýsingar sem eru notaðar til að flytja inn bankayfirlit. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## Að færa inn opnunarstöðu

Til að fylla út í reitinn **Staða** með opnunarstöðu verður þú að bóka fjárhagsfærslu bankareiknings með upphæðinni. Hægt er að gera þetta með því að framkvæma afstemmingu bankareiknings. Frekari upplýsingar er að finna á [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).  
>
> Einnig er hægt að tiltaka opnunarstöðu sem hluta af almennri gagnamyndun í nýjum fyrirtækjum með því að nota **Flytja viðskiptagögn** leiðbeiningar um uppsetningu með hjálp. Frekari upplýsingar eru í [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).  

> [!IMPORTANT]
> Ekki bóka opnunarstöðuna beint í fjárhaginn. Að vera með færslur í fjárhagsreikningnum sem voru bókaðar beint í hann leiðir yfirleit til þess að ekki sé hægt að afstemma bankareikninginn. Með bankareikningum í erlendum gjaldmiðli leiðir slíkt verklag til þess að mismunur safnast upp eftir því sem þú bókar fleiri bankaafstemmingar. Yfirleitt er opnunarstaða í banka bókuð beint á bankareikninginn og upphæðin endar á fjárhagsreikningnum. Annars geturðu seinna bakfært hana út af fjárhagsreikningnum sem þú notar jafna opnunarstöðu fjárhagsins. Í báðum tilvikum þarf að jafna allar beinar bókanir á fjárhagsreikninginn áður en þú byrjar fyrstu bankaafstemminguna&mdash;sérstaklega ef bankareikningurinn er í erlendum gjaldmiðli.

## Til að setja upp bankareikning þinn til að flytja inn eða flytja út bankaskrár

Reitirnir sem tengjast innflutningi og útflutningi bankastraums og skráa eru í flýtiflipanum **Millifærsla** á síðunni **Bankareikningsspjald**. Frekari upplýsingar er að finna í [Notkun AMC Banking 365 Fundamentals viðbótar](ui-extensions-amc-banking.md) og [Setja upp Envestnet Yodlee Bank Feeds þjónustu](bank-how-setup-bank-statement-service.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar**, velja síðan viðkomandi tengil.
2. Opnaðu spjaldið fyrir bankareikninginn sem þú ætlar að flytja út og inn bankaskrár fyrir.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Flytja**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Mismunandi útflutningsþjónusta skráa og snið þeirra þurfa mismunandi uppsetningargildi á síðunni **Bankareikningsspjald**. Þú færð upplýsingar um röng eða týnd uppsetningargildi þegar þú flytur skrána út. Lestu stuttar lýsingar á reitunum vandlega eða vísaðu til viðkomandi efnisferlis. Til dæmis, við útflutning greiðsluskráar fyrir kortamillifærslu NA (EFT) þarf að fylla út reitina **Síðasta greiðslutilkynningarnúmer** og **Kenninúmer**. Frekari upplýsingar er að finna á [Flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)

Reitirnir í flýtiflipanum **Flutningur** á bankareikningnum þjóna mismunandi tilgangi, eftir því hvort greiðslan er á innleið eða útleið.

Myndin hér að neðan sýnir leið inngreiðslna (tölurnar í lýsingunni samsvara þeim á myndinni):

:::row:::
    :::column:::

1. Færslurnar eru fluttar út af bankareikningnum á annaðhvort læsilegu .csv-sniði eða sniði bankans.
2. *Skilgreining gagnaskipta* varpar upplýsingunum í skránni í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Setja upp gagnaskipti](across-set-up-data-exchange.md)
3. *Uppsetning útflutnings/innflutnings gagna* skilgreinir innflutning eða útflutning og tengir við skilgreiningu gagnaskipta.
4. *Bankayfirlitin á innflutningssniðinu* tengja innflutningsuppsetninguna við bankareikninginn.
5. Greiðslurnar eru fluttar inn gegnum síðuna **Greiðsluafstemmingarbók** eða **Afstemming bankareiknings**.

  :::column-end:::
  :::column:::

        ![Mynd af greiðslum sem berast frá bankanum inn á bankareikninga.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Greiðslur á innleið eru alltaf fluttar inn gegnum síðuna **Greiðsluafstemmingarbók** eða beint á síðuna **Afstemming bankareiknings**. Á hinn bóginn geta greiðslur á útleið komið úr hvaða greiðslubók sem er. Einu forsendurnar eru þær að velja þarf reitinn **Leyfa útflutning greiðslu** í viðkomandi runu greiðslubókar.

Myndin hér að neðan sýnir leið útgreiðslna (tölur í lýsingunni samsvara þeim sem eru á myndinni):

:::row:::
    :::column:::

6. Færslurnar eru fylltar út í greiðslubók sem hefur verið útbúin fyrir útflutning á greiðslum í skrá.
7. *Bankayfirlitin á innflutningssniðinu* tengja innflutningsuppsetninguna við bankareikninginn.
8. *Uppsetning útflutnings/innflutnings gagna* skilgreinir innflutning eða útflutning og tengir við skilgreiningu gagnaskipta.
9. *Skilgreining gagnaskipta* varpar upplýsingunum í skránni í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna á [Setja upp gagnaskipti](across-set-up-data-exchange.md)
10. Greiðslurnar eru fluttar út úr greiðslubókinni og fluttar inn á bankareikninginn.

  :::column-end:::
  :::column:::

        ![Skýring á greiðslum af bankareikningum sem eru sendar til bankans.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa

Reitir á **Flutningur** flýtiflipanum á síðunni **Bankareikningsspjald lánardrottins** eru tengdir útflutningi á bankastraumum og skrám. Frekari upplýsingar er að finna í [Nota AMC Banking 365 Fundamentals viðbót](ui-extensions-amc-banking.md) og [Flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## Bankareikningnum breytt

Til að nota annan bankareikning fyrir reksturinn þarf að stofna nýja bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)]. Mælt er með því að nota ekki upplýsingar um reikninginn sem er nú í notkun vegna þess að það getur leitt til rangra gagna. Til dæmis gæti opnunarstaðan verið röng eða bankagjaldið gæti hætt að virka á réttan hátt. Það er mikilvægt að halda núverandi og nýjum reikningum aðskildum.

Eftir að nýi bankareikningurinn hefur verið stofnaður ættir þú einnig að stofna nýjan bókunarflokk bankans og úthluta honum á nýjan fjárhagslykil. Þú getur endurnotað fyrirliggjandi bókunarflokk bankans og bankafærslur verða bókaðar á sömu fjárhagslyklana eins og hinir bankareikningarnir sem deila bókunarflokki bankans. Hins vegar er mælt með því að stofna nýjan bókunarflokk bankans og fjárhagslykil svo afstemmingarnar verði auðveldari.

> [!NOTE]
> Mundu að upplýsingar um bankareikning á opnum sölureikningum sýna enn upprunalega bankareikninginn. Samkvæmt því er líklegt að greiðslur verði enn bókaðar á þann reikning. Við mælum með því að þú haldir báðum reikningunum virkum í ákveðið langan tíma eftir breytinguna.

Til að fá samþjappaðra yfirlit yfir sjóðsreikninga í fjárhagsskýrslugerð skal nota reikningana **Samtala í upphafi** og **Samtala í lok** í bókhaldslyklinum, línurnar **Samtölur** í fjárhagsskýrslum eða flokkum fjárhagsreikninga. Frekari upplýsingar er að finna í [Viðskiptagreind og Financial Reporting](bi.md) hlutanum.

## Sjá tengda [Microsoft þjálfun](/training/modules/cash-management-dynamics-365-business-central/)

## Sjá einnig .

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
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
