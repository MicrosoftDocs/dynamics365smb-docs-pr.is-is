---
title: Setja upp bankareikninga (inniheldur Video)
description: Kynntu þér hvernig bankareikningar eru notaðir í Business Central og hvernig hægt er að stemma af upphæðir með bankanum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.search.form: 370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280
ms.date: 01/24/2022
ms.author: edupont
ms.openlocfilehash: deb1ac60e40306d9a8730b825b038e663bd51166
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605327"
---
# <a name="set-up-bank-accounts"></a>Bankareikningar settir upp

Þú notar bankareikninga í [!INCLUDE[prod_short](includes/prod_short.md)] til að fylgjast með bankafærslunum þínum. Lyklar geta verið útnefni í gjaldmiðli landsins eða í erlendum gjaldmiðli. Þegar bankareikningar hafa verið settir upp er einnig hægt að nota valkostinn prentskoðun. Bankareikningarnir fela í sér aukaaðgerðir fyrir [afstemmingu](receivables-apply-payments-auto-reconcile-bank-accounts.md) greiðslu, [afstemmingu](bank-how-reconcile-bank-accounts-separately.md) banka og innflutnings-og útflutning á bankaskrám. Bankareikningarnir geta einnig verið teknir með í færslum í almennum færslubókum. Hver bankareikningur er tengdur við reikning í bókhaldslyklinum í gegnum tilskilinn bókunarflokk bankareiknings. Með því að nota bankareikning í greiðslufærslu verður til færsla sjálfkrafa stofnuð bæði fyrir bankareikninginn og tengdan fjárhag (Fjárhagsreikningur).  

Bankareikningar virka mismunandi eftir því hvort gjaldmiðilskóði er tilgreindur:

- Ef Gjaldmiðilskóði er auður

  Allar færslur á bankareikninginn eru í gjaldmiðli landsins (ISK) fyrir gildandi fyrirtæki. Ef færsla fer fram á reikningnum í öðrum gjaldmiðli eru upphæðirnar bókaðar á reikninginn í LCY samkvæmt viðkomandi gengi gjaldmiðils. Gefa verður einhverjar ávísanir út úr þessum lykli í ISK. Ef bankareikningurinn er notaður í færslubók verður færslubókarlínan sjálfkrafa hluti af auðum gjaldmiðilskóða.  
  
- Gjaldmiðilskóði er tilgreindur

  Allar færslur sem gerðar eru til og ávísanir sem gefnar eru út á þennan lykil verða að vera í sama gjaldmiðli og tilgreint er á reikningnum.

Hægt er að vista tíma í gagnafærslu með því að gera bankareikning að sjálfgefnum lykli til að nota fyrir gjaldmiðilinn sem tilgreindur er fyrir lykilinn. Ef það er gert er lykillinn tengdur við sölu-og þjónustuskjöl sem nota gjaldmiðilinn. Ef gera á lykilinn sjálfgefið fyrir sölu-og þjónustuskjöl á **Bankareikbankakortu** skal kveikja á **notkun sem sjálfgildi gjaldmiðilsvíxilsins**. Ef þörf krefur er hægt að velja annan lykil þegar verið er að vinna í skjali.

Bankareikningur er óaðskiljanlegur hluti af [!INCLUDE[prod_short](includes/prod_short.md)] og gegnir hlutverki við margvíslega aðra getu. Eftirfarandi mynd sýnir mikilvægustu tengslin:

![Skýring á tengslum bankareiknings.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Hægt er að sjá að stofnun á bankareikningi gerir það aðgengilegt í öllum þeim stöðum sem sýndir eru hér að ofan, auk þess að speglast í viðkomandi fjárhagsreikningi og á **upplýsingasíðu** félagsins.

Bankareikningur er yfirleitt vaktaðir daglega til að ganga úr skugga um að nýjar greiðslur frá viðskiptavinum séu skráðar eins fljótt og auðið er. Þetta hjálpar til við að tryggja að raunveruleg staða viðskiptamanns endurspeglist í [!INCLUDE[prod_short](includes/prod_short.md)]. Sem gefa sölum einstaklingum, bókamönnum og öðrum starfsmönnum aðgang að sem flestum viðeigandi og upp-upplýsingum upplýsingar svo þeir komist hjá því að gera óþarfa símtöl við viðskiptavin varðandi gjaldfallna reikninga eða tafir á sendingum.  

![Skýring á bankagreiðslu.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Annað verkefni er að flytja inn gjaldeyristekjur lánardrottins með innleysta Gengi gjaldmiðils til að ganga úr skugga um að raunveruleg Staða lánardrottna sé upp-til skv. Með því [að nota greiðsluafstemmingargetu](receivables-apply-payments-auto-reconcile-bank-accounts.md) er auðveldasta leiðin að gera það. Í **Greiðsluafstemmingarbók** er hægt að flytja inn bankafærslur beint frá netbanka og láta bóka þér meira og minna sjálfkrafa. Færslubókin greinir og bókar sjálfkrafa eftirfarandi:  

- Beingreiðslur frá viðskiptavinum  
- Greiðslur viðskiptavinar á stökum reikningum  
- Fastagreiðslur frá viðskiptavinum  
- Greiðslur viðskiptavinar í erlendum gjaldmiðlum  
- Greiðslur lánardrottna  
- Greiðslur lánardrottna í erlendum gjaldmiðli  
- Endurteknar greiðslur lánardrottna og áskriftir  
- Bankakostnaður og vextir  

Greiðsluuppgjör gefur verulegan tímasparnað í bókun á innleið og útsendum greiðslum. Hins vegar er ekki tekið tillit til færslna á bankareikningi í [!INCLUDE[prod_short](includes/prod_short.md)] 100% rétt fyrr en bankaafstemmingar eru keyrðar.  

Bankaafstemming er notuð til að ganga úr skugga um að bankareikningurinn í [!INCLUDE[prod_short](includes/prod_short.md)] samsvari ytri reikningnum í bankanum.  

 ![Skýring á afstemming bankareiknings.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

Í skýringarmynd hér að ofan táknar leftside-hliðin bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)] og réttingarhliðin táknar færslur sem fluttar hafa verið inn frá bankanum í gegnum bankaforrit á netinu. Skýringarmyndin í miðjunni sýnir færslurnar frá báðum hliðum, sem er bankaafstemmingin.

Raunverulegi bankinn ætti að kannast við flestar færslur frá bankareikningnum í [!INCLUDE[prod_short](includes/prod_short.md)]. Með fáum undantekningum er m.a. átt við eftirfarandi tilvik:  

- Leiðréttingar bókaðar í [!INCLUDE[prod_short](includes/prod_short.md)]  
- Athuganir sem gefnar eru út sem hafa ekki enn verið gjaldsendar 
- Lánardrottinsgreiðslur sem hafa enn ekki verið samþykktar af bankanum  

Af efnislegum reikningi í bankanum eru færslur sem ekki eru greindar í greiðsluafstemmingarbókinni koma allan tímann, eins og til dæmis eftirfarandi:  

- Nýjar áskriftir lánardrottins  
- Greiðslur viðskiptavina án lýsingar
- Bankavextir
- Bankagjöld
- Gjöld vegna kreditkorta ekki enn tilkynnt

Því betra sem þú ert við vörpun upplýsinga í greiðsluafstemmingarbók, því fleiri færslur bókast sjálfkrafa og auðveldari regluleg bankaafstemming verður.

Sjá í myndbandinu hér að neðan grunnskrefin til að setja upp bankareikning í [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Sumir reitir geta innihaldið viðkvæm gögn eins og reitirnir **Útibúsnúmer banka**, **Bankareikningsnr.**, **SWIFT-kóði** og **IBAN-númer**. Lærðu meira á að [vakta viðkvæm svæði](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Bankareikningar settir upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **bankareikninga** og veljið síðan tengda tengilinn.
2. Á síðunni **bankareikningar** skal velja aðgerðina **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Dæmi um það **væri reiturinn Bankareikn. bókunarflokkur** sem tengir bankareikning við undirliggjandi fjárhagsreikning í efnahagslykil. Frekari upplýsingar um [uppsetningu bókunarflokka](finance-posting-groups.md).

> [!TIP]
> Sum svæði eru falin þar til valið er að **Sýna** Aðgerðir, gjarnan vegna þess að þau eru sjaldan notuð. Öðrum verður að bæta við með sérstillingu. Frekari upplýsingar er að sérsníða á [vinnusvæðinu](ui-personalization-user.md).

Hægt er að stofna eins marga bankareikninga og þarf fyrir reksturinn. Fyrir hvern bankareikning þarf að tilgreina upplýsingar sem auðkenna bankareikninginn á einkvæman hátt. Þessar upplýsingar eru meðal annars landfræðilegs aðseturs bankans; númeraröð fyrir mismunandi gerðir færslna, til dæmis beingreiðslu-og kreditfærslur; gjaldeyrisupphæðir eru tilgreindar í; og upplýsingar notaðar við innflutning á bankauppgjörum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
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

## <a name="to-enter-an-opening-balance"></a>Til að færa inn opnunarstöðu

Til að fylla út **reitinn Staða** í með opnunarstöðu verður að bóka bankareiknings-færslu með upphæðinni sem um ræðir. Hægt er að gera þetta með því að framkvæma afstemmingu bankareiknings. Frekari upplýsingar á [afstemmingu bankareikninga](bank-how-reconcile-bank-accounts-separately.md).  
>
> Einnig er hægt að innleiða opnunarstöðuna sem hluta af almennri gagnastofnun í nýjum fyrirtækjum með því að nota leiðbeiningar um uppsetningu á Viðskipdata **fyrir** aðstoðarmenn yfirfæra. Lærðu meira á [að undirbúa þig fyrir viðskipti](ui-get-ready-business.md).  

> [!IMPORTANT]
> Ekki bóka opnunarstöðuna beint í fjárhag. Ef færslur í fjárhagsreikningnum sem voru bókaðar beint á hann leiðir yfirleitt til þess að ekki er hægt að stemma bankareikninginn af. Með bankareikningum erlendra gjaldmiðla er svo reynd afleiðing mismunar sem safnast upp eftir því sem meiri bankaafstemmingar eru bókaðar. Venjulega er opnunarbankainnistaða bókuð beint á bankareikning og upphæðin endar í fjárhagsreikningnum. Síðar er hægt að bakfæra hana úr fjárhagsreikningnum sem er notaður til að jafna opnunarfjárhagsstöðu. Í öðru tilfelli verður að jafna beina bókun við fjárhagsreikninginn áður en fyrsta bankaafstemming &mdash; hefst, sérstaklega ef bankareikninginn er í erlendum gjaldmiðli.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Til að setja upp bankareikning þinn til að flytja inn eða flytja út bankaskrár

Svæðin sem tengjast inn-og útflutningi á bankastraumum og skrám eru á **flutningi** fastflipa á **síðu bankareikningsreikningsins**. Lærðu meira á [að AMC Banking 365 Fundamentals nota framlengingunni](ui-extensions-amc-banking.md) og [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **bankareikninga** og veljið síðan tengda tengilinn.
2. Opna skal spjald fyrir bankareikninginn sem er að flytja út eða flytja inn bankaskrár fyrir.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Flytja**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Mismunandi útflutningsþjónusta skráa og snið þeirra þurfa mismunandi uppsetningargildi á síðunni **Bankareikningsspjald**. Notandi verður upplýstur um röng eða uppsetningargildi þegar skráin er flutt út. Lestu stuttar lýsingar svæðanna vandlega eða vísaðu í efnisatriði tengda ferlinu. Til dæmis þarf að flytja út greiðsluskrá fyrir Norður-ameríska flutningssjóði (EFIENT) og krefjast þess að **Reitirnir í Síðasta greiðslutilkynningu nr** . og **flutningnr.** verði fylltir út. Frekari upplýsingar við [útflutning greiðslur í Bankarskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Reitirnir í flýtiflipanum **Flutningur** á bankareikningnum þjóna mismunandi tilgangi, eftir því hvort greiðslan er á innleið eða útleið.

Útskýring hér að neðan sýnir leið á inngreiðslum (tölur í lýsingunni samsvara þeim sem eru í útskýringu):

:::row:::
    :::column:::

1. Færslurnar eru fluttar út af bankareikningnum á annaðhvort læsilegu .csv-sniði eða sniði bankans.
2. *Skilgreining gagnaskipta* varpar upplýsingunum í skránni í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar í [Setja upp gagnaskipti](across-set-up-data-exchange.md)
3. *Útflutningur/innflutningsuppsetning* gagna skilgreinir útflutning eða innflutning og tengla í skilgreiningu gagnaskipta.
4. *Bankayfirlitin á innflutningssniðinu* tengja innflutningsuppsetninguna við bankareikninginn.
5. Greiðslurnar eru fluttar inn gegnum síðuna **Greiðsluafstemmingarbók** eða **Afstemming bankareiknings**.

  :::column-end:::
  :::column:::

        ![Mynd af greiðslum sem berast frá bankanum inn á bankareikninga.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Innsendar greiðslur eru alltaf fluttar inn í **Greiðsluafstemmingarbók** eða beint inn á **afstemmingarsíðu** bankareiknings. Á hinn bóginn geta greiðslur á útleið komið úr hvaða greiðslubók sem er. Einu forsendurnar eru þær að velja þarf reitinn **Leyfa útflutning greiðslu** í viðkomandi runu greiðslubókar.

Útskýringamynd hér sýnir leiðina á útleið greiðslur (tölur í lýsingunni samsvara þeim sem eru í útskýringu):

:::row:::
    :::column:::

6. Færslurnar byggja á greiðslubók sem hefur verið útbúin fyrir útflutning á greiðslum í skrá.
7. *Bankayfirlitin á innflutningssniðinu* tengja innflutningsuppsetninguna við bankareikninginn.
8. *Útflutningur/innflutningsuppsetning* gagna skilgreinir útflutning eða innflutning og tengla í skilgreiningu gagnaskipta.
9. *Skilgreining gagnaskipta* varpar upplýsingunum í skránni í reitina í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar í sjá [Setja upp gagnaskipti](across-set-up-data-exchange.md)
10. Greiðslurnar eru fluttar út úr greiðslubókinni og fluttar inn í bankareikninginn.

  :::column-end:::
  :::column:::

        ![Skýring á greiðslum af bankareikningum sem eru sendar til bankans.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa

**Í reitunum flutningur** Fastflipi á **spjaldi** bankareikningssíða lánardrottins tengist útflutningi á bankastraumum og skrám. [Frekari upplýsingar um AMC Banking 365 Fundamentals notkun húsnæðis](ui-extensions-amc-banking.md) -og [Útflutningsgreiðslna á bankarskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account"></a>Bankareikningnum breytt

Ef nota á annan bankareikning fyrir viðskiptin þarf að stofna nýja bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)]. Mælt er með því að nota ekki upplýsingar um reikninginn sem er nú í notkun vegna þess að það getur leitt til rangra gagna. Til dæmis gæti opnunarstaðan verið röng eða bankagjaldið gæti hætt að virka á réttan hátt. Það er mikilvægt að halda núverandi og nýjum reikningum aðskildum.

Eftir að nýi bankareikningurinn hefur verið stofnaður ættir þú einnig að stofna nýjan bókunarflokk bankans og úthluta honum á nýjan fjárhagslykil. Hægt er að endurnota fyrirliggjandi bankabókunarflokk og eru bankafærslur bókaðar á sömu fjárhagslykla og aðra bankareikninga sem aðrir viðskiptabókunarflokkar banka. Hins vegar er mælt með því að stofna nýjan bókunarflokk bankans og fjárhagslykil svo afstemmingarnar verði auðveldari.

> [!NOTE]
> Mundu að upplýsingar um bankareikning á opnum sölureikningum sýna enn upprunalega bankareikninginn. Samkvæmt því er líklegt að greiðslur verði enn bókaðar á þann reikning. Við mælum með því að þú haldir báðum reikningunum virkum í ákveðið langan tíma eftir breytinguna.

Til að fá þéttari Sýn á lausafjárreikningana í fjárhagsskýrslugerð eru notaðir **samtölu-og** endareikningar **í bókhaldslykli,** samantektarlínurnar **í fjárhagsskýrslum eða** fjárhagsreikningstegundir. Frekari upplýsingar er að fá í [viðskiptagreind og Fjárhagsskýrsluhluta](bi.md).

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Uppsetning bókunarflokka](finance-posting-groups.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md)  
[SEPA-beingreiðsla í Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Setja upp bankareikning fyrir SEPA-beingreiðslu](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Setja upp bankareikning fyrir SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Gera skal AMC Banking 365 Fundamentals greiðslur með framlengingu eða SEPA Kreditmillifærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Greiðsluafstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Skilja fjárhag og bókhaldslykil](finance-general-ledger.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
