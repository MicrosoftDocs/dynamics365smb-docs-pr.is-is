---
title: "Notkun greiðslna og afstemmingar (DK) viðbótarinnar | Microsoft Docs"
description: "Þessi viðbót gerir það auðvelt að flytja út skrár sem eru forstilltar til að uppfylla kröfur banka um rafræna skráningu."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 09/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c2daa9854f371660dd9096c54d85812466dfe46e
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="the-payments-and-reconciliations-dk-extension-for-microsoft-dynamics-for-finance-and-operations-business-edition"></a>Greiðslur og afstemmingar (DK) viðbótin fyrir Microsoft Dynamics for Finance and Operations, Business Edition
Greiddu hratt og án mistaka með því að flytja út skrár sem eru sérstaklega sniðnar fyrir millifærslur með lánardrottni eða banka. Þessar skrár flýta fyrir greiðslu- og afstemmingum og útrýma villum sem geta komið upp þegar upplýsingar eru slegnar inn á bankasíðu.  
  
Þessi viðbót styður skráarsnið fyrir nokkra danska banka. Þegar þú flytur út greiðsluupplýsingar í skrá pakkar viðbótin gögnunum inn í sniðið sem bankinn fer fram á. Dæmi um þetta eru sniðin Bankdata-V3, BEC, SDC og FIK, sem margir mismunandi bankar nota, og sum sem eru sérhæfðari fyrir tiltekna banka á borð við Danske Bank og Nordea. Viðbótin inniheldur einnig nokkur snið til að flytja inn og afstemma bankareikninga.  
  
> [!Note]
> Til að nota viðbótina er nauðsynlegt að vita hvaða snið bankinn eða lánardrottinn krefst. Sumir bankar eða lánardrottnar veita þessar upplýsingar á vefsvæðum sínum: Hins vegar gætirðu þurft að hafa samband við þjónustudeild þeirra til að fá upplýsingarnar.  
  
## <a name="supported-bank-formats"></a>Studd bankasnið
Þessi viðbót getur notað eftirfarandi skráarsnið fyrir greiðsluskrár:  
  
* BANKDATA-V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK-CMKV  
* DANSKEBANK-CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CSV  

## <a name="to-set-up-the-extension"></a>Til að setja upp viðbótina
Nokkur skref eru nauðsynleg í upphafi.  
  
* Leyfa útflutning greiðslugagna. Til að vernda gögnin þín er þetta ekki í boði.  
* Setja upp innkaup og viðskiptaskuldir þannig að þú þurfir ekki utanaðkomandi skjalanúmer á reikningum. Ef þess er þörf geturðu notað tilvísunarnúmerið til að vísa til tiltekins reiknings.  
* Tilgreina greiðslumáta fyrir hvern lánardrottininn. Greiðslumátar skilgreina hvernig þú borgar reikninga frá lánardrottninum. Til dæmis Banki, Staðgreiðsla, Ávísun eða Reikningur.  
* Tilgreina gerð sniðsins sem á að nota fyrir hvern bankareikning. Til dæmis NORDEA, DANSKEBANK, SDC og svo framvegis.  
  
Að auki þarftu að úthluta lánardrottnum á staðbundinn **Alm. viðsk.bókunarflokkur** og **Bókunarflokk lánardrottins**. Stilling fyrir land/svæði fyrir lánardrottinn verður að vera Danmörk (DK). Nánari upplýsingar er að finna í [Uppsetning Bókunarflokka](finance-posting-groups.md).  
  
### <a name="to-allow-included365finincludesd365finmdmd-to-export-payment-data"></a>Til að leyfa [!INCLUDE[d365fin](includes/d365fin_md.md)] að flytja út greiðslugögn
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubók** og velja svo viðeigandi tengil.  
2. Í glugganum **Breyta greiðslubók** er valið **Banki**.  
3. Veljið gátreitinn **Leyfa greiðsluútflutning**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Til að tilgreina greiðslumáta lánardrottins
Eftirfarandi tafla sýnir sambland FIK og GIRO greiðslumáta sem [!INCLUDE[d365fin](includes/d365fin_md.md)] styður.

||Gerð 01 | Gerð 04 | Gerð 71 | Gerð 73 |
|----|---|---|---|---|
|Númer gíróreiknings eða FIK-lánardrottins? | Númer gíróreiknings | Númer gíróreiknings | Númer FIK-lánardrottins | Númer FIK-lánardrottins|
|Leyfja skilaboð til viðtakanda? | Já |Nei |Nei | Já |
|Inniheldur greiðslutilvísunarnúmer? | Nei | Já, 16 stafir. | Já, 15 stafir. | Nei|

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **lánardrottnar** og velja svo viðeigandi tengil.  
2. Opnaðu kortið, víkkaðu **Greiðslur** flipann, í **Greiðslumáti** veldu greiðslumáta.  
3. Nauðsynlegt er að ljúka öðrum reitum, allt eftir valinu. Lýsing samsetninga er að finna í töflunni hér að ofan.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Til að tilgreina sniðið sem á að nota fyrir bankareikning
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bankareikningar** og velja svo viðeigandi tengil.  
2. Opna spjaldið fyrir bankareikninginn.  
3. Á **Útflutningssnið greiðslu** skal velja sniðið fyrir útflutningsskrána.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Velja FIK eða Gírógreiðsluupplýsingar fyrir reikninga lánardrottins
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.
2. Veljið lánardrottinn. Munið að þetta verður að vera danskur lánardrottinn með heimilisfang í Danmörku.
3. Búa til reikning. Reitirnir **Greiðslumáti** og **Númer lánardrottins** eru fylltir út samkvæmt stillingum á lánardrottnaspjaldinu. Hægt er að breyta þeim ef óskað er.
4. Í **Greiðslutilvísun** skal slá inn 15 stafa númerið á reikningi lánardrottins.  
  
    > [!Tip]
    > Þú verður aðeins að bæta við síðustu 11 tölustöfum í númerinu. [!INCLUDE[d365fin](includes/d365fin_md.md)] mun bæta fjórum núllum við upphaf númersins.  
  
5. Bóka skal reikninginn.

## <a name="to-use-the-extension-to-export-payment-data"></a>Til að nota viðbótina til að flytja út greiðslugögn
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubækur** og velja svo viðeigandi tengil.  
2. Velja **Stinga upp á greiðslubókum lánardrottins** aðgerðina.  
  
    > [!Tip]
    > Ef þú vilt aðeins flytja út tilteknar greiðslur skaltu nota afmörkunarvalkosti gagna.  
  
3. Ef það er nauðsynlegt er hægt að bæta við afmörkunum til að flytja aðeins tilteknar greiðslur.  
4. Í reitnum **Tegund bankagreiðslu** skal velja **Rafræn greiðsla**.  
5. Veldu **Export** aðgerðina.  

## <a name="see-also"></a>Sjá einnig .
[Sérstilling Finance and Operations, Business Edition fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] Notkun viðbóta](ui-extensions.md)  
[Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[Setja upp SEPA-beingreiðslur](finance-how-to-set-up-sepa-direct-debit.md)  
[Bóka SEPA-greiðslukvittanir beingreiðslna](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  





