---
title: Setja upp umskráningu bankagagna| Microsoft Docs
description: Hægt er að setja upp bankareikninga til að fylgjast með viðskiptum og flytja bankastreymi inn eða út, eins og t.d. Yodlee.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 10/02/2018
ms.author: sgroespe
ms.openlocfilehash: 48fb943e03e2dff3d1ed583872cb989944495f7f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800482"
---
# <a name="set-up-the-bank-data-conversion-service"></a>Setja upp umskráningarþjónustu fyrir bankagögn
Altæk þjónustuveita til að umreikna greiðsluupplýsingar í hvaða gagnaskráarsnið sem bankinn þinn þarf eru uppsett og tilbúið til að vera virkjað í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta er vísað til í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem umskráningarþjónusta fyrir bankagögn.

Hægt er að flytja út greiðslulínur á síðunni **Greiðslubók** í skrá eða gagnastreymi sem þú síðan hleður upp í bankann þinn fyrir sjálfvirka vinnslu svo að þú þarft ekki að gera rafræn greiðsla í sitthvoru lagi. Frekari upplýsingar eru í [Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md).

Þú getur flutt inn bankareikningsskrár á síðuna **Greiðsluafstemmingarbók** með því að nota umskráningarþjónusta fyrir bankagögn til að umbreyta skrá sem þú færð frá bankanum í gagnastraum sem [!INCLUDE[d365fin](includes/d365fin_md.md)] getur flutt inn. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Í staðinn fyrir að flytja inn bankayfirlit með gagnagrunnþjónustu bankans geturðu notað Envestnet Yodlee Bank Feeds þjónustuna. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee bankastreymisþjónustu](bank-how-setup-bank-statement-service.md).

Til að flytja inn eða flytja út bankaskrár verður þú að setja upp eigin bankareikning og bankareikninga lánardrottna þinna. Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> Umskráningarþjónusta fyrir bankagögn kann að setja hámark á það hversu margar línur má flytja út í einni skrá. Ef farið er yfir hámarkið munu koma upp villuboð. Mælt er með því að bankayfirlitsskrár fari ekki yfir 1.000 línur þar sem vinnslutími umreikningsþjónusta bankagagna kann þá að aukast til muna.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Að skrá fyrirtækið fyrir umreikningsþjónustu bankagagna
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **uppsetning umreikningsþjónustu fyrir bankagögn** og veldu síðan tengda tengilinn.  
2. Síðan **Uppsetning Umreikningsþjónusta fyrir bankagögn** opnast með þremur reitum útfylltum með viðeigandi vefslóðir frá veitanda umreikningsþjónustu fyrir bankagögn.

    > [!NOTE]  
    >   Í CRONUS International Ltd. Sýnigagnagrunninum eru notandanafn og lykilorð reitirnir fylltar með sýnidæmum um innskráningarupplýsingar sem þú verður að skipta út með raunverulegum upplýsingum fyrirtækis þíns þegar þú skráir þig fyrir umreikningsþjónustu bankagagna.
3. Í **innskráningarvefslóð** reitnum, veldu vafrahnappinn til að opna innskráningarsíðu þjónustuveitunnar.  
4. Á skráningarsíðu þjónustuveitu bankagagna skal slá inn notandanafn og aðgangsorð fyrir áskrift fyrirtækisins að þjónustunni og ljúka svo skráningarferlinu samkvæmt leiðbeiningum þjónustuveitunnar.

    Fyrirtæki þitt er nú skráð fyrir umreikningsþjónustu bankagagna. Sláið inn notandanafn og aðgangsorð sem tilgreind voru fyrir þjónustuna í tengdum uppsetningarreitum í [!INCLUDE[d365fin](includes/d365fin_md.md)].

5. Á síðunni **Uppsetning umreikningsþjónustu fyrir bankagögn** í **Notandanafn** reitnum, sláðu inn sama gildi sem þú færðir inn sem innskráningarnafn á síðu þjónustuveitunnar í 4. skrefi.
6. Í reitnum **lykilorð**, sláðu inn sama gildi sem þú færðir inn í reitinn **Aðgangsorð** á síðu þjónustuveitunnar í 4. skrefi.

> [!NOTE]  
> Innskráningargögnin þín eru sjálfkrafa dulrituð.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Til að skoða eða uppfæra listann yfir studd bankagagnasnið
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **uppsetning umreikningsþjónustu fyrir bankagögn** og veldu síðan tengda tengilinn.
2. Á síðunni **uppsetning umreikningsþjónustu fyrir bankagögn** , skal velja **Nafn banka – umskráningarlisti gagna** til að opna lista yfir nöfn banka sem standa fyrir bankagagnasnið sem eru studd af umskráningarþjónustunni.
3. Á síðunni **Nafn banka – gagnaumreikningslisti**, veldu aðgerðina **Uppfæra nafnalista banka**.

Listi yfir bankagagnasnið sem eru studd af umreikningsþjónustunni fyrir bankagögn er nú uppfærður. Þetta er listinn yfir nöfn banka, afmörkuð eftir landi/svæði, sem hægt er að velja úr í reitnum **Nafn banka - gagnaumreikningur** á síðunni **Bankareikningsspjald**.

> [!NOTE]  
>   Uppfærsla studdra bankagagnasniða á sér einnig stað þegar gildi er valið eða slegið inn í reitinn **Nafn banka - gagnaumreikningur** á bankareikningnum.

Þú hefur nú skráð þig fyrir umreikningsþjónustu bankagagna. Halda áfram að endurspegla skráningarupplýsingar í öllum bankareikningum sem nota þjónustuna.

## <a name="see-also"></a>Sjá einnig
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Stjórna bankareikningum](bank-manage-bank-accounts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
