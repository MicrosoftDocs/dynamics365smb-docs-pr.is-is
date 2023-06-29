---
title: Setja upp umskráningu bankagagna
description: 'Hægt er að setja upp bankareikninga til að fylgjast með viðskiptum og flytja bankastreymi inn eða út, eins og t.d. Yodlee.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a><a name="set-up-the-amc-banking-365-fundamentals-extension"></a>Setja upp AMC Banking 365 Fundamentals-viðbótina
Altæk þjónustuveita til að umreikna greiðsluupplýsingar í hvaða gagnaskráarsnið sem bankinn þinn þarf eru uppsett og tilbúið til að vera virkjað í [!INCLUDE[prod_short](includes/prod_short.md)]. Vísað er í þetta í [!INCLUDE[prod_short](includes/prod_short.md)] sem AMC Banking 365 Fundamentals-viðbót.

Hægt er að flytja út greiðslulínur á síðunni **Greiðslubók** í skrá eða gagnastreymi sem þú síðan hleður upp í bankann þinn fyrir sjálfvirka vinnslu svo að þú þarft ekki að gera rafræn greiðsla í sitthvoru lagi. Frekari upplýsingar eru í [Flytja út greiðslur í bankaskrá](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Hægt er að flytja bankayfirlitsskrár inn á síðuna **Greiðsluafstemmingarbók** með því að nota AMC Banking 365 Fundamentals-viðbótina til að umbreyta skrá sem þú færð frá bankanum yfir í gagnaflæði sem [!INCLUDE[prod_short](includes/prod_short.md)] getur flutt inn. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Í staðinn fyrir að flytja inn bankayfirlit með AMC Banking 365 Fundamentals-viðbótinni geturðu notað Envestnet Yodlee Bank Feeds þjónustuna. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).

Til að flytja inn eða flytja út bankaskrár verður þú að setja upp eigin bankareikning og bankareikninga lánardrottna þinna. Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> AMC Banking 365 Fundamentals-viðbótin kann að setja hámark á það hversu margar línur er hægt að flytja út í einni skrá. Ef farið er yfir hámarkið munu koma upp villuboð. Mælt er með því að bankayfirlitsskrár fari ekki yfir 1.000 línur þar sem vinnslutími AMC Banking 365 Fundamentals-viðbótarinnar kann þá að aukast til muna.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a><a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Að skrá fyrirtækið fyrir AMC Banking 365 Fundamentals-viðbótinni
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Þjónustugrunnur bankagagnaumreiknings** og svo velja viðeigandi tengil.  
2. Síðan **Uppsetning umbreytingarþjónustu fyrir bankagögn** opnast með þremur reitum útfylltum með viðeigandi vefslóðum frá veitanda AMC Banking 365 Fundamentals-viðbótarinnar.

    > [!NOTE]  
    >   Í CRONUS International Ltd. sýnigagnagrunninum eru notandanafn og lykilorð reitirnir fylltar með sýnidæmum um innskráningarupplýsingar sem þú verður að skipta út með raunverulegum upplýsingum fyrirtækis þíns þegar þú skráir þig fyrir AMC Banking 365 Fundamentals-viðbótinni.
3. Í **innskráningarvefslóð** reitnum, veldu vafrahnappinn til að opna innskráningarsíðu þjónustuveitunnar.  
4. Á skráningarsíðu þjónustuveitu bankagagna skal slá inn notandanafn og aðgangsorð fyrir áskrift fyrirtækisins að þjónustunni og ljúka svo skráningarferlinu samkvæmt leiðbeiningum þjónustuveitunnar.

    Fyrirtæki þitt er nú skráð fyrir AMC Banking 365 Fundamentals-viðbótinni. Sláið inn notandanafn og aðgangsorð sem tilgreind voru fyrir þjónustuna í tengdum uppsetningarreitum í [!INCLUDE[prod_short](includes/prod_short.md)].

5. Á síðunni **Uppsetning umreikningsþjónustu fyrir bankagögn** í **Notandanafn** reitnum, sláðu inn sama gildi sem þú færðir inn sem innskráningarnafn á síðu þjónustuveitunnar í 4. skrefi.
6. Í reitnum **lykilorð**, sláðu inn sama gildi sem þú færðir inn í reitinn **Aðgangsorð** á síðu þjónustuveitunnar í 4. skrefi.

> [!NOTE]  
> Innskráningargögnin þín eru sjálfkrafa dulrituð.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a><a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Til að skoða eða uppfæra listann yfir studd bankagagnasnið
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Þjónustugrunnur bankagagnaumreiknings** og svo velja viðeigandi tengil.
2. Á síðunni **uppsetning umreikningsþjónustu fyrir bankagögn** , skal velja **Nafn banka – umskráningarlisti gagna** til að opna lista yfir nöfn banka sem standa fyrir bankagagnasnið sem eru studd af umskráningarþjónustunni.
3. Á síðunni **Nafn banka – gagnaumreikningslisti**, veldu aðgerðina **Uppfæra nafnalista banka**.

Listinn yfir bankagagnasnið sem eru studd af AMC Banking 365 Fundamentals-viðbótinni er nú uppfærður. Þetta er listinn yfir nöfn banka, afmörkuð eftir landi/svæði, sem hægt er að velja úr í reitnum **Nafn banka - gagnaumreikningur** á síðunni **Bankareikningsspjald**.

> [!NOTE]  
>   Uppfærsla studdra bankagagnasniða á sér einnig stað þegar gildi er valið eða slegið inn í reitinn **Nafn banka - gagnaumreikningur** á bankareikningnum.

Þú hefur nú skráð þig fyrir AMC Banking 365 Fundamentals-viðbótinni. Halda áfram að endurspegla skráningarupplýsingar í öllum bankareikningum sem nota þjónustuna.

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
