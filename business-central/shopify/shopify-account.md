---
title: Stofna og setja upp Shopify reikning
description: Læra hvernig á að fá Shopify reikning svo hægt sé að sýna verkflæði til samþættingar Shopify og Business Central.
ms.date: 03/04/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# Stofna og setja upp Shopify reikning



Ef þú íhugar hvort nota Shopify eigi sem e-Commerce lausn og þarft Shopify reikning til að staðfesta samþætt verkflæði þá eru eftirfarandi valkostir:

- Fáðu prufuútgáfu. Þetta er dæmigerður upphafspunktur fyrir notendur.  
- Stofna þróunarbúðir. Þessi nálgun er fyrir félaga sem stunda ítrekaða lýðheilsu, þjálfun og veita stuðning.

## Prufuútgáfa (notandi)

Farðu á vefsíðuna [Shopify](https://www.shopify.com) og notaðu tölvupóstreikninginn þinn fyrir stjórnandareikninginn til að skrá þig fyrir ókeypis prufuútgáfu. Fræðast meira um hvernig á að búa til og sérstilla netverslunina þína í [Shopify hjálparmiðstöðinni](https://help.shopify.com/).

Í stjórnanda **Shopify** búðarinnar sem búin var til skal nota eftirfarandi **stillingar**:

- Valin er áætlun í stillingum áætlunar [**·**](https://www.shopify.com/admin/settings/plan) til að geta prófað útskráningarferlið.

- Íhuga skal að *virkja Sýna innskráningartengil í haus onilne-verslunar og útskráningar* í reikningum í **netverslun og útskráningarhluta**  [**stillinga viðskiptamannareikninga**](https://www.shopify.com/admin/settings/customer_accounts) í **Shopify stjórnandanum**.
- Íhuga skal að *velja Nýjan viðskiptamannareikning* í reikningum  **í netverslun og útskráningarhluta** stillinga viðskiptamannareikninga.
- Íhuga *að virkja sjálfsafgreiðslu skil í hlutanum* Nýir **viðskiptavinareikningar** í stillingum viðskiptamannareikninganna.

- Virkja prufugreiðslur. Tveir valkostir eru í boði. Byrjað er á greiðslustillingum [**·**](https://www.shopify.com/admin/settings/payments) :  
  1. *(til prófunar) Falska hliðið*. Nánari upplýsingar eru [í Virkja svikagátt fyrir prófun](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify greiðslur* í prófunarham. Nánari upplýsingar eru [í Prófun greiðslna Shopify](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Slökktu á valkostinum **Safnvista pöntunina sjálfkrafa** í hlutanum **Úrvinnsla pöntunar** í stillingum fyrir [**Greiðsluferli**](https://www.shopify.com/admin/settings/checkout) í **Shopify stjórnanda**.
- Íhuga skal að *velja Heiti fyrirtækis* - Valfrjálst í hlutanum **Upplýsingar um** viðskiptamenn í útskráningarstillingunum.
- Gera valkostina **Sýna ábendingar virka við útskráningu** í **hlutanum Áþreipanlegur** hluti útskráningarstillinganna ef ætlunin er að sýna ábendingu.

> [!Important]  
> Til að forðast greiðslur, mundu að hætta við réttarhöldin Shopify .

## Þróunarverslun

Byrjað er á því að ganga í félagakerfið [Shopify](https://help.shopify.com/partners/about). Síðan er mælaborð **félaga** notað til að stofna þróunarverslunina. Fræðast meira um [stofnun þróunarversluna](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Þegar búðin hefur verið búin til, í **Shopify Stjórnandi** búðarinnar, skal nota eftirfarandi **stillingar**:

- Íhuga skal að *virkja Sýna innskráningartengil í haus onilne-verslunar og útskráningar* í reikningum í **netverslun og útskráningarhluta**  [**stillinga viðskiptamannareikninga**](https://www.shopify.com/admin/settings/customer_accounts) í **Shopify stjórnandanum**.
- Íhuga skal að *velja Nýjan viðskiptamannareikning* í reikningum  **í netverslun og útskráningarhluta** stillinga viðskiptamannareikninga.
- Íhuga *að virkja sjálfsafgreiðslu skil í hlutanum* Nýir **viðskiptavinareikningar** í stillingum viðskiptamannareikninganna.
  
- Virkja prufugreiðslur. Tveir valkostir eru í boði. Byrja á því að fletta að [**stillingum greiðslna**](https://www.shopify.com/admin/settings/payments) :  
  1. *(til prófunar) Falska hliðið*. Nánari upplýsingar eru [í Virkja svikagátt fyrir prófun](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify greiðslur* í prófunarham. Fá nánari upplýsingar við [prófun Shopify greiðslna](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).
     
- Slökktu á valkostinum **Safnvista pöntunina sjálfkrafa** í hlutanum **Úrvinnsla pöntunar** í stillingum fyrir [**Greiðsluferli**](https://www.shopify.com/admin/settings/checkout) í **Shopify stjórnanda**.
- Íhuga skal að *velja Heiti fyrirtækis* - Valfrjálst í hlutanum **Upplýsingar um** viðskiptamenn í útskráningarstillingunum.
- Ef ætlunin er að sýna ábendingu skal virkja valkostina **Sýna ábendingar við útskráningu** í hlutanum **Ábending** í útskráningarstillingunum.


> [!Note]  
> Þróunarverslanir eru yfirleitt aðgangsorð varnar. Þegar reynt er að opna tiltekna síðu í netversluninni frá [!INCLUDE [prod_short](../includes/prod_short.md)], til dæmis til að fara í tiltekna vöru eða pöntun, þarftu að slá inn aðgangsorðið þitt. Meðan þú ert að prófa, til að forðast að slá inn aðgangsorðið þitt, skrá þig inn í Shopify admin og opna verslunina þaðan. Ekki þarf að færa inn aðgangsorð geymslu fyrr en vafranum er lokað eða lota rennur út.  

## Sjá einnig

[Hafist handa í tengilinu Shopify](get-started.md)  
[Kynning: Uppsetning og notkun Shopify tengis](walkthrough-setting-up-and-using-shopify.md)
