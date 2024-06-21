---
title: Bankareikningar settir upp
description: Kynntu þér hvernig bankareikningar eru notaðir í Business Central og hvernig hægt er að stemma af upphæðir með bankanum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 05/24/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-bank-accounts"></a>Bankareikningar settir upp

Nota bankareikninga í [!INCLUDE[prod_short](includes/prod_short.md)] til að fylgjast með bankafærslum. Hægt er að hafa reikninga í SGM eða erlendum gjaldmiðli. Þegar bankareikningar hafa verið settir upp er einnig hægt að prenta tékka. Bankareikningar bjóða einnig upp á aðgerðir fyrir [greiðsluafstemmingu](receivables-apply-payments-auto-reconcile-bank-accounts.md), [bankaafstemmingu](bank-how-reconcile-bank-accounts-separately.md) og inn- og útflutning á bankaskrám.

Hægt er að hafa bankareikninga með í færslum í færslubók. Sérhver bankareikningur tengir reikning í bókhaldslykli í gegnum úthlutaðan bókunarflokk bankareikninga. Ef bankareikningur er notaður í greiðslufærslu býr sjálfkrafa til færsla bæði í bankareikningi og tengdum fjárhag (fjárhagsreikningi).  

Bankareikningar virka mismunandi eftir því hvort gjaldmiðilskóði er tilgreindur:

- Ef gjaldmiðilskóti er ekki tilgreindur eru allar færslur á bankareikningnum í SGM (SGM) gildandi fyrirtækis. Ef viðskipti eru gerð fyrir reikninginn í öðrum gjaldmiðli bóka upphæðirnar á reikninginn í SGM á grundvelli gengis gjaldmiðilsins. Allir tékkar sem gefnir eru út af þessum reikningi verða að vera í SGM. Ef bankareikningurinn er notaður í færslubók notar færslubókarlínan sjálfkrafa auðan gjaldmiðilskóta.  
  
- Ef gjaldmiðilskóti er tilgreindur verða allar færslur sem gerðar eru á þessum reikningi og allar tékka sem gefnir hafa verið út af honum að nota sama gjaldmiðil og reikningurinn.

Þú getur sparað þér tíma við gagnafærslu með því að gera bankareikning sjálfgefinn reikning sem á að nota fyrir gjaldmiðilinn sem tilgreindur er fyrir reikninginn. Ef þú gerir það er reikningnum úthlutað á sölu- og þjónustuskjöl sem nota gjaldmiðilinn. Til að gera reikninginn sjálfgefinn fyrir sölu- og þjónustuskjöl, á síðunni **Bankareikningsspjald**, skaltu kveikja á **Nota sem sjálfgefið fyrir gjaldmiðil**. Ef þörf krefur er hægt að velja annan reikning þegar unnið er í skjali.

Bankareikningur er samþættur hluti af [!INCLUDE[prod_short](includes/prod_short.md)] og gegnir hlutverki í mörgum öðrum möguleikum. Eftirfarandi mynd sýnir mikilvægustu tengslin:

![Skýring á tengslum bankareiknings.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Þegar bankareikningur er stofnaður er hann tiltækur á öllum stöðum sem sýndir eru í útskýringunni og speglast í fjárhagsreikningi og á síðunni **Stofngögn** .

Oft er fylgst með bankareikningum daglega til að tryggja að nýjar greiðslur frá viðskiptamönnum séu skráðar eins fljótt og unnt er. Með því að skrá greiðslur er fljótlegt að tryggja að raunveruleg staða viðskiptamanns birtist [!INCLUDE[prod_short](includes/prod_short.md)]. Með því að halda stöðu greiðslna viðskiptamanna hjálpar sölufólk, bókarar og aðrir starfsmenn að hringja óþarfa símtöl varðandi gjaldfallna reikninga eða seinkun á afhendingum.  

![Skýring á bankagreiðslu.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Annað verk er að flytja inn gjaldmiðilsgreiðslur lánardrottins með raunverulegu gengi gjaldmiðils til að ganga úr skugga um að raunveruleg staða lánardrottna sé uppfærð. Að nota möguleikann [greiðsluafstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md) er auðveldasta leiðin til að gera þetta. Í greiðsluafstemmingarbók **er** hægt að flytja bankafærslur beint inn úr netbankajöfnun og bóka þær sjálfkrafa eða minna. Færslubókin auðkennir og bókar sjálfkrafa eftirfarandi færslur:  

- Beinar debetgreiðslur frá viðskiptamönnum.  
- Greiðslur viðskiptavina á einum reikningum.  
- Molta-samtala greiðslna frá viðskiptamönnum.  
- Greiðslur viðskiptavina í erlendri mynt.  
- Greiðslur lánardrottna.  
- Greiðslur lánardrottins í erlendum gjaldmiðli.  
- Lánardrottnagreiðslur og áskriftir sem eru ítrekunar.  
- Bankagjöld og vextir.  

Greiðsluafstemming sparar umtalsverðan tíma við bókun á greiðslum á innleið og útleið. Færslurnar á bankareikningnum í [!INCLUDE[prod_short](includes/prod_short.md)] eru þó ekki taldar 100% réttar fyrr en bankaafstemming er keyrð.  

Bankaafstemming er notuð til að ganga úr skugga um að bankareikningurinn í [!INCLUDE[prod_short](includes/prod_short.md)] samsvari ytri reikningnum í bankanum.  

 ![Skýring á afstemming bankareiknings.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

Vinstri hliðin táknar bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)] og hægra megin táknar færslur sem fluttar eru frá bankanum í gegnum netbankaforritið. Skýringarmyndin sýnir færslur frá báðum hliðum sem mynda bankaafstemminguna.

Raunverulegi bankinn ætti að kannast við flestar færslur frá bankareikningnum í [!INCLUDE[prod_short](includes/prod_short.md)]. Þær fáu undantekningar fela í sér eftirfarandi tilvik:  

- Leiðréttingar bókaðar í [!INCLUDE[prod_short](includes/prod_short.md)].  
- Ávísanir sem hafa verið gefnar út sem eru ekki í reiðufé.
- Lánardrottnagreiðslur sem ekki hafa verið samþykktar af bankanum.  

Færslur sem ekki eru auðkenndar í greiðsluafstemmingarbók berast alltaf, svo sem eftirfarandi færslur:  

- Nýjar áskriftir lánardrottins  
- Greiðslur viðskiptavina án lýsingar
- Bankavextir
- Bankakostnaður
- Kreditkortagjöld sem hafa ekki verið tilkynnt

Því betri sem þú ert í að kortleggja upplýsingar í greiðsluafstemmingarbókinni, því fleiri færslur eru bókaðar sjálfkrafa og þeim mun auðveldari verður reglubundna bankaafstemmingin.

Eftirfarandi myndband sýnir grunnskrefin til að setja upp bankareikning í [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Sumir reitir geta innihaldið viðkvæm gögn eins og reitirnir **Útibúsnúmer banka**, **Bankareikningsnr.**, **SWIFT-kóði** og **IBAN-númer**. Nánari upplýsingar eru í [reitunum Skjár sem viðkvæmir eru](across-log-changes.md#monitor-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Bankareikningar settir upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar**, velja síðan viðkomandi tengil.
2. Á síðunni **bankareikningar** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Dæmi um það er reiturinn **Bókunarflokkur** bankareikninga sem tengir bankareikninginn við undirliggjandi fjárhagsreikning á efnahagsreikningi. Frekari upplýsingar er að finna á [Uppsetning bókunarflokka](finance-posting-groups.md).

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

## <a name="to-enter-an-opening-balance"></a>Að færa inn opnunarstöðu

Til að fylla út í reitinn **Staða** með onunarstöðu verður þú að bóka fjárhagsfærslu bankareiknings með upphæðinni. Færslan er bókuð með afstemmingu bankareiknings. Frekari upplýsingar er að finna á [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).  
>
> Einnig er hægt að tiltaka opnunarstöðu sem hluta af almennri gagnamyndun í nýjum fyrirtækjum með því að nota **Flytja viðskiptagögn** leiðbeiningar um uppsetningu með hjálp. Frekari upplýsingar eru í [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).  

> [!IMPORTANT]
> Ekki bóka opnunarstöðuna beint í fjárhag. Færslur í fjárhagsreikningi sem bókaðar voru beint á hann koma yfirleitt í veg fyrir að bankareikningur sé stemmdur af. Með bankareikningum í erlendum gjaldmiðli leiðir bein bókun af mismuni sem safnast upp eftir því sem fleiri bankaafstemmingar eru bókaðar. Yfirleitt er opnunarstaða banka bókuð beint á bankareikninginn og upphæðin endar á fjárhagsreikningnum. Annars geturðu seinna bakfært hana út af fjárhagsreikningnum sem þú notar jafna opnunarstöðu fjárhagsins. Í báðum tilvikum þarf að jafna allar beinar bókanir á fjárhagsreikninginn áður en þú byrjar fyrstu bankaafstemminguna&mdash;sérstaklega ef bankareikningurinn er í erlendum gjaldmiðli.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Til að setja upp bankareikning þinn til að flytja inn eða flytja út bankaskrár

Reitirnir sem tengjast innflutningi og útflutningi bankastraums og skráa eru í flýtiflipanum **Millifærsla** á síðunni **Bankareikningsspjald**. Frekari upplýsingar er að finna í [Notkun AMC Banking 365 Fundamentals viðbótar](ui-extensions-amc-banking.md) og [Setja upp Envestnet Yodlee Bank Feeds þjónustu](bank-how-setup-bank-statement-service.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar**, velja síðan viðkomandi tengil.
2. Opna skal spjald bankareikningsins til að flytja inn eða flytja inn bankaskrár fyrir.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Flytja**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Mismunandi útflutningsþjónusta skráa og snið þeirra þurfa mismunandi uppsetningargildi á síðunni **Bankareikningsspjald**. Þú færð upplýsingar um röng eða týnd uppsetningargildi þegar þú flytur skrána út. Lestu stuttar lýsingar á reitunum vandlega eða vísaðu til viðkomandi efnisferlis. Til dæmis, við útflutning greiðsluskráar fyrir kortamillifærslu NA (EFT) þarf að fylla út reitina **Síðasta greiðslutilkynningarnúmer** og **Kenninúmer**. Frekari upplýsingar er að finna á [Flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)

Reitirnir í flýtiflipanum **Flutningur** á bankareikningnum þjóna mismunandi tilgangi, eftir því hvort greiðslan er á innleið eða útleið.

Eftirfarandi mynd sýnir leið greiðslna á innleið. Tölurnar í lýsingunni samsvara tölunum í myndinni.

:::row:::
    :::column:::

1. Færslurnar eru fluttar út af bankareikningnum á annaðhvort læsilegu .csv-sniði eða sniði bankans.
2. Skilgreining gagnaskipta varpar upplýsingunum í skránni í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Setja upp gagnaskipti](across-set-up-data-exchange.md)
3. Uppsetning gagnaútflutnings/innflutnings skilgreinir útflutning eða innflutning og tengist skilgreiningu gagnaskipta.
4. Innflutningssnið bankayfirlita tengir uppsetningu innflutnings við bankareikninginn.
5. Greiðslurnar eru fluttar inn gegnum síðuna **Greiðsluafstemmingarbók** eða **Afstemming bankareiknings**.

  :::column-end:::
  :::column:::

        ![Mynd af greiðslum sem berast frá bankanum inn á bankareikninga.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Greiðslur á innleið eru alltaf fluttar inn gegnum síðuna **Greiðsluafstemmingarbók** eða beint á síðuna **Afstemming bankareiknings**. Á hinn bóginn geta greiðslur á útleið komið úr hvaða greiðslubók sem er. Einu forsendurnar eru þær að velja þarf reitinn **Leyfa útflutning greiðslu** í viðkomandi runu greiðslubókar.

Eftirfarandi mynd sýnir leið greiðslna á útleið. Tölurnar í lýsingunni samsvara tölunum í myndinni.

:::row:::
    :::column:::

6. Færslurnar eru útfylltar í greiðslubók sem var tilbúin til útflutnings á greiðslum í skrá.
7. Innflutningssnið bankayfirlita tengir uppsetningu innflutnings við bankareikninginn.
8. Uppsetning gagnaútflutnings/innflutnings skilgreinir útflutning eða innflutning og tengist skilgreiningu gagnaskipta.
9. Skilgreining gagnaskipta varpar upplýsingunum í skránni í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna á [Setja upp gagnaskipti](across-set-up-data-exchange.md)
10. Greiðslurnar eru fluttar út úr greiðslubókinni og fluttar inn á bankareikninginn.

  :::column-end:::
  :::column:::

        ![Skýring á greiðslum af bankareikningum sem eru sendar til bankans.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa

Reitir á **Flutningur** flýtiflipanum á síðunni **Bankareikningsspjald lánardrottins** eru tengdir útflutningi á bankastraumum og skrám. Frekari upplýsingar er að finna í [Nota AMC Banking 365 Fundamentals viðbót](ui-extensions-amc-banking.md) og [Flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account"></a>Bankareikningnum breytt

Til að nota annan bankareikning fyrir reksturinn þarf að stofna nýja bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)]. Mælt er með því að þú skiptir ekki bara um upplýsingar um reikninginn sem þú notar þar sem það getur valdið röngum gögnum. Til dæmis gæti opnunarstaðan verið röng eða bankagjaldið gæti hætt að virka á réttan hátt. Það er mikilvægt að halda núverandi og nýjum reikningum aðskildum.

Eftir að nýi bankareikningurinn hefur verið stofnaður ættir þú einnig að stofna nýjan bókunarflokk bankans og úthluta honum á nýjan fjárhagslykil. Hægt er að endurnota bankabókunarflokk og bankafærslur eru bókaðar á sömu fjárhagsreikninga og aðrir bankareikningar sem deila þeim bankabókunarflokki. Hins vegar er mælt með því að stofna nýjan bókunarflokk bankans og fjárhagslykil svo afstemmingarnar verði auðveldari.

> [!NOTE]
> Mundu að upplýsingar um bankareikning á opnum sölureikningum sýna enn upprunalega bankareikninginn. Samkvæmt því er líklegt að greiðslur verði enn bókaðar á þann reikning. Við mælum með því að þú haldir báðum reikningunum virkum í ákveðið langan tíma eftir breytinguna.

Til að fá samþjappaðra yfirlit yfir sjóðsreikninga í fjárhagsskýrslugerð skal nota reikningana **Samtala í upphafi** og **Samtala í lok** í bókhaldslyklinum, línurnar **Samtölur** í fjárhagsskýrslum eða flokkum fjárhagsreikninga. Frekari upplýsingar er að finna í [Viðskiptagreind og Financial Reporting](bi.md) hlutanum.

## <a name="see-also"></a>Sjá einnig .

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
