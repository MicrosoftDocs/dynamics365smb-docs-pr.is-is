---
title: Úthluta kostnaði til millifyrirtækjafélaga | Microsoft Docs
description: Kynntu þér hvernig VSK-stillingar fyrir viðskiptamenn og lánardrottna stjórna því hvort og hvernig virðisaukaskattur er reiknaður.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocate-costs-to-intercompany-partners"></a>Úthluta kostnaði til millifyrirtækjafélaga
Þegar bókanir milli fyrirtækja eru notaðar til að flytja skjöl milli samstarfsfyrirtækja, þá stjórna VSK-tengdar stillingar (sérstaklega VSK-viðskiptabókunarflokkurinn) sem úthlutað er til viðskipamanna- eða lánardrottnalykla (sem tengjast millifyrirtækjafélagi) því hvort og hvernig virðisaukaskattur er reiknaður og skráður. Einnig er hægt að gera kostnaðardreifingu beint í innkaupapöntunum til samstarfsfyrirtækja. Til dæmis ef skráður er innkaupareikningur frá ytri lánardrottni og ætlunin er að dreifa einhverjum eða öllum kostnaði á eitt eða fleiri millifyrirtækjafélög.

Hægt er að úthluta kostnaði á eitt eða fleiri millifyrirtækjafélög með því að nota eftirfarandi:

* **MF-færslubækur** - Þessar færslubækur eru gagnlegar þegar þjónusta er keypt. Til dæmis þegar móðurfyrirtæki kaupir þjónustu til að setja upp tölvukerfi í tveimur dótturfélögum. Reikningurinn er sendur til móðurfyrirtækisins, en kostnaðinum er úthlutað á millifyrirtækjafélögin. Frekari upplýsingar eru í [Unnið með samstæðuskjöl og færslubækur](intercompany-how-work-documents-journals.md).
* Innkaupapantanir og reikningar - Notkun innkaupaskjala er gagnleg þegar innkaupaaðgerðir á til dæmis rekstrargjöldum eru miðstýrðar í einu fyrirtæki og síðan úthlutað á millifyrirtækjafélög.

## <a name="to-allocate-costs-using-an-intercompany-general-journal"></a>Að úthluta kostnaði með MF-færslubók
Til að færa inn línu í MF-færslubók skal fylgja þessum skrefum. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubók milli fyrirtækja** og velja síðan viðkomandi tengil.
2. Ef nauðsynlegt, skal í reitinn **Númer ytra skjals** færa inn skjalanúmer reiknings frá lánardrottninum.
3. Í reitnum **Gerð skjals** skal velja **Reikningur**.
4. Í reitnum **Gerð reiknings** skal velja **Lánardrottinn**.
5. Í svæðinu **Bankareikningsnúmer** skal velja lánardrottinn.
6. Í reitinn **Upphæð** skal færa inn neikvæða upphæð sem samsvarar upphæð reikningsins.
7. Í reitnum **Tegund mótreiknings** skal velja **Fjárhagsreikningur**.
8. Í reitnum **Nr. mótreiknings** skal velja mótreikninginn sem á að nota.
9. Til að úthluta kostnaði á millifyrirtækjafélaga skal fylgja þessum skrefum:
   1. Stofnið nýja línu.
   2. Skiljið eftir reitinn **Gerð skjals**, veljið valkostinn sem skilur hann eftir auðan.
   3. Í reitinn **Nr. skjals** skal færa inn númer sem er ólíkt númerinu í reitnum **Nr. ytra skjals**. Litið er á kostnaðarúthlutunina sem aðra færslu.
   4. Í reitnum **Gerð reiknings** skal velja **MF-félagi**.
   5. Í reitnum **Reikningsnúmer** skal velja millifyrirtækjafélaga sem úthluta á kostnaði til.
   6. Í reitnum **Gerð mótreiknings** skal velja **Fjárhagsreikningur**.
   7. Í reitnum **Nr. mótreiknings** skal velja fjárhagsreikninginn þar sem bóka á upphæðina sem er móttekin frá millifyrirtækjafélaga.
   1. Í reitinn **Upphæð** skal færa inn upphæð reikningsins sem á að úthluta á millifyrirtækjafélaga.
   1. Í reitnum **Fjárhagsreikningsnr. MF-félaga** skal velja fjárhagsreikninginn sem á að bóka upphæðina á fyrir millifyrirtækjafélagann. 
   1. Fyllið inn í eftirstandandi reiti eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Endurtakið þessi skref fyrir hvert samstæðufyrirtæki sem á að deila kostnaðinum.
1. Til að bóka skjalið og úthluta kostnaði skal velja **Bóka**.  

## <a name="to-allocate-costs-using-a-purchase-document"></a>Að úthluta kostnaði með innkaupaskjali
Eftirfarandi ferli lýsir því hvernig á að úthluta kostnaði með því að nota innkaupareikning. Skrefin eru þau sömu fyrir innkaupapantanir.

> [!NOTE]
> Til að ljúka þessum skrefum verður að sérsníða síðuna **Innkaupareikningur** með því að bæta við reitunum **MF-félagakóði**, **Tilvísunarteg. MF-félaga** og **MF-félagi**. Frekari upplýsingar eru í [Hefja sérstillingu á síðu með borðanum Sérstilla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningur** og velja síðan viðkomandi tengil.
2. Í reitnum **Gerð** skal velja **Fjárhagsreikningur**.
   
   Fjárhagsreikningur er eini valkosturinn sem hægt er að nota til að úthluta kostnaði.  
1. Í reitnum **númer** skal velja fjárhagsreikninginn sem á að bóka á.
1. Í reitnum **MF-félagakóði** skal velja millifyrirtækjafélaga sem úthluta á kostnaði til.
1. Í **Tilvísunarteg. MF-félaga** skal velja fjárhagsreikning til að nota fyrir úthlutunina. Þessi lykill mun varpa kostnaðinum í lykil í bókhaldslykli millifyrirtækjafélaga.
1. Í reitnum **Magn** skal tilgreina fjölda eininga sem rukka á millifyrirtækjafélagann um.
1. Í reitinn **Innkaupsverð án VSK (eða með VSK)** skal færa inn kostnað á hverri vöru sem rukka á millifyrirtækjafélagann um.
1. Fyllið inn í eftirstandandi reiti eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Til að bóka innkaupapöntunina skal velja **Bóka**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners"></a>Að senda úthlutaðan kostnað til millifyrirtækjafélaga
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-úthólfsfærslur** og velja síðan viðkomandi tengil.
2. Velja skal línu til að senda og velja síðan aðgerðina **Senda til MF-félaga**. 
3. Til að úthluta kostnaði skal velja aðgerðina **Ljúka línuaðgerðum**.

## <a name="calculating-vat-for-cost-distributions"></a>Útreikningur virðisaukaskatts fyrir kostnaðardreifingar
Þegar skjal er notað til að dreifa kostnaði á millifyrirtækjafélaga skal hafa í huga tvær VSK-stillingar: 
* Stillingar á fjárhagsreikningnum fyrir útgjöld:
   * Ef almenni viðskiptabókunarflokkurinn eða VSK-viðskiptabókunarflokkurinn er settur upp í fjárhagsreikningnum, þá fer útreikningurinn eftir flokkunum og afurðahópunum í skjalalínunni.
   * Ef almenni viðskiptabókunarflokkurinn eða VSK-viðskiptabókunarflokkurinn er ekki tilgreindir í fjárhagsreikningnum, þá fer útreikningurinn eftir eftirfarandi:
* Stillingar bókunarflokks í millifyrirtækjafélaga
   * Hvort millifyrirtækjafélagi er úthlutaður á númer viðskiptamanns sem er ekki með almennan viðskiptabókunarflokk eða VSK-viðskiptabókunarflokk tilgreindan.
   * Ekkert viðskiptamannanúmer er tengt millifyrirtækjafélaganum. Þá er almenni viðskiptabókunarflokkurinn eða VSK-viðskiptabókunarflokkurinn auður og línan í VSK-bókunargrunni notuð, sem er yfirleitt flokkur þar sem 0% VSK er tilgreindur.

> [!NOTE]
> Mikilvægt er að staðfesta bæði uppsetningu millifyrirtækjafélaga og uppsetningu fjárhagsreiknings (fyrir kostnaðarreikninginn sem notaður er fyrir kostnaðardreifingu) áður en kostnaði er úthlutað til millifyrirtækjafélaga.

## <a name="see-also"></a>Sjá einnig
[Uppsetning milli fyrirtækja](intercompany-how-setup.md)  
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
