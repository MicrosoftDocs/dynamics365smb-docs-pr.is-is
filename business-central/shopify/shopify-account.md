---
title: Stofna og setja upp  Shopify  lykil
description: Lærðu að ná  Shopify  í reikning svo hægt sé að sýna fram á verkflæði fyrir samþættingu  Shopify  og rekstur Central.
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# <a name="create-and-set-up-a-shopify-account"></a>Stofna og setja upp  Shopify  lykil

Ef miðað er við hvort nota  Shopify  eigi e-Commerce lausnina og þörf er  Shopify  á reikningi til að sannreyna samþætt verkflæði eru eftirfarandi valkostir:

- Fá prufuútgáfu. Þetta er dæmigerður byrjunarstaður fyrir endónotendur.  
- Stofna þróunarbúðir. Þessi nálgun er fyrir samstarfsaðila sem sinna endurteknum kynningum, lestraraðferðum og veita stuðning.

## <a name="trial-end-user"></a>Próftími (notandi á enda)

 [Shopify Farðu á vefsvæðið](https://www.shopify.com)  og Notaðu tölvupóstreikninginn þinn fyrir stjórnendareikninginn til að skrá þig í ókeypis prufutíma. Frekari upplýsingar um það hvernig eigi að stofna og sérsníða netverslun eru  [Shopify  í hjálparmiðstöðinni](https://help.shopify.com/).

 **Shopify** Í verslun the stofnaðist, gilda eftirfarandi  **stillingar**:

- Slökktu á valkostinum **Safnvista pöntunina sjálfkrafa** í hlutanum **Úrvinnsla pöntunar** í stillingum fyrir [**Greiðsluferli**](https://www.shopify.com/admin/settings/checkout) í **Shopify stjórnanda**.
- Íhuga skal að  *Virkja tengilinn Sýna innskráningu í Storefront stílsniðinu og útskrift*  í  **hlutanum viðskiptavinarstillingar**  í útskráningarstillingum.
- Íhuga skal að  *Velja nafn fyrirtækis sem er valfrjáls*  valkostur í  **hlutanum upplýsingar**  um viðskiptavin í útstillingum.
-  **Gera valkostinn Sýna tikið virka við**  útskráningu í  **tikið**  hluta útskráningarstillinga ef ætlunin er að sýna tikið.
- Virkja prófunargreiðslur. Þú átt tvo valkosti. Byrja á því að fara í stillingar á  [**greiðslum**](https://www.shopify.com/admin/settings/payments) :  
  1. *(fyrir próf) Bogus gátt*. Sjá  [virkið Bogus Gateway fyrir prófun](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction) fyrir frekari upplýsingar.
  2. *Shopify greiðslur*  í prófunarham. Frekari upplýsingar er að finna  [í prófunargreiðslum Shopify](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Veljið áætlun í  [**stillingum áætlunar**](https://www.shopify.com/admin/settings/plan)  til að hægt sé að prófa útskriftarferlið.

> [!Important]  
> Til að forðast greiðslur skaltu muna að hætta  Shopify  réttarhöldin.

## <a name="development-store"></a>Þróunarsjóður

Byrjaðu á því að ganga frá  [Shopify  Félagakerfinu](https://help.shopify.com/partners/about). Eftirá skal nota  **Stjórnborð**  samstarfsaðila til að stofna þróunarverslunina. Frekari upplýsingar um  [stofnun þróunarstofnunar](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Þegar búið er að stofna verslunina, í  **Shopify**  vefverslun stofnunar, gilda eftirfarandi  **stillingar**:

- Slökktu á valkostinum **Safnvista pöntunina sjálfkrafa** í hlutanum **Úrvinnsla pöntunar** í stillingum fyrir [**Greiðsluferli**](https://www.shopify.com/admin/settings/checkout) í **Shopify stjórnanda**.
- Íhuga skal að  *Virkja tengilinn Sýna innskráningu í Storefront stílsniðinu og útskrift*  í  **hlutanum viðskiptavinarstillingar**  í útskráningarstillingum.
- Íhuga skal að  *Velja nafn fyrirtækis sem er valfrjáls*  valkostur í  **hlutanum upplýsingar**  um viðskiptavin í útstillingum.
- Ef þú ætlar að sýna tikið skaltu virkja  **valkostinn Sýna tikið við**  útskráningu í  **tikið**  hluta af stillingum útskriftar.
- Virkja prófunargreiðslur. Þú átt tvo valkosti. Byrja á því að fletta upp í  [**stillingum greiðslna**](https://www.shopify.com/admin/settings/payments) :  
  1. *(fyrir próf) Bogus gátt*. Sjá  [virkið Bogus Gateway fyrir prófun](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction) fyrir frekari upplýsingar.
  2. *Shopify greiðslur*  í prófunarham. Frekari upplýsingar um  [prófgreiðslur Shopify](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

> [!Note]  
> Þróunarbúðir eru yfirleitt lykilorð varin. Þegar þú reynir að opna tiltekna síðu í netverslun frá  [!INCLUDE [prod_short](../includes/prod_short.md)] t.d. til að fara í ákveðna vöru eða pöntun þarftu að slá inn lykilorðið þitt. Meðan þú ert að prófa, til að forðast að slá inn aðgangsorðið þitt, Skráðu þig inn í  Shopify  admin og Opnaðu verslunina þína þaðan. Þú þarft ekki að færa inn Store aðgangsorðið fyrr en þú lokar vafranum þínum eða setrið rennur út.  

## <a name="see-also"></a>Sjá einnig

[Byrjaðu með  Shopify  tengiflugi](get-started.md)  
[Walkthrough: Uppsetning og notkun  Shopify  tengibúnaðar](walkthrough-setting-up-and-using-shopify.md)
