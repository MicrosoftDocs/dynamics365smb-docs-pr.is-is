---
title: Stöðureitur á skjölum
description: Upplýsingar um stöðuna ' opin ' og ' Útgefin ' í tilboðum, pöntun eða kreditreikningsskjölum.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,
ms.search.form: ''
ms.date: 09/19/2022
ms.author: bholtorf
ms.openlocfilehash: f48f499277155aaf60ae0992199d7895225f1ef5
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728627"
---
# <a name="status-field-on-documents"></a>Stöðureitur á skjölum

Þegar stofnað er tilboð, pöntun eða kreditreikningur er **sjálfgefið að reiturinn Staða** í fylgiskjalshausnum opni **sjálfkrafa stöðuna**.

Þegar búið er að fylla út skjalið er hægt að losa það og [!INCLUDE[prod_short](includes/prod_short.md)] breyta gildinu í **reitnum Staða** til **losunar**. Þessi staða gefur til kynna að pöntunin sé tilbúin fyrir næsta stig vinnslu áður en hún er bókuð.

| Staða | Lýsing |
| ------ | ----------- |
| Opinn   | Hægt að gera breytingar á fylgiskjalinu. |
| Losað | Skjalinu hefur verið sleppt á næsta stig vinnslu og ekki er hægt að gera breytingar á línum af gerðinni *Vara* og *eign*.<br /><br />Hægt er að opna útgefna fylgiskjalið aftur ef breyta á efni þess. Eigi að færa breytt fylgiskjal á næsta stig í meðhöndluninni þarf að gefa það út aftur. |
| Bíður samþykkis   | Fylgiskjalið bíður samþykktar. |
| Bíður fyrirframgreiðslu | Bókaður hefur verið fyrirframgreiðslureikningur fyrir skjalið. |

## <a name="release-process"></a>Úttektarferli

Hægt er að nota úttektarferlið á mismunandi hátt til að auðvelda venjulegt verkflæði, til dæmis til að fylgja ferlum fyrirtækis eftir samþykki eða til að ræsa vöruhúsaaðgerðir.

### <a name="approval-procedures"></a>Samþykktarferli

Fyrirtækið getur notað úttektarferlið til að gefa til kynna að annar notandi hafi samþykkt skjalið eða að utanaðkomandi tengiliður geti mætt lýsingum skjalsins eins og sýnt er í þessum dæmum:

* Aðeins er hægt að gefa út innkaupapöntun þegar lánardrottinninn hefur sýnt fram á að þeir séu reiðubúnir til að uppfylla pöntunina.
* Pöntun er stofnuð og annar notandi verður að samþykkja hana, ef til vill af öryggisástæðum, áður en leyft er að losa hana.
* Framkvæmdastjóri sem ber ábyrgð á að samþykkja allar endurgreiðslur verður að gefa út kreditreikning sem notandi hefur stofnað.

Frekari upplýsingar um samþykktarverkflæði við [notkun verkflæða](across-use-workflows.md).

### <a name="warehouse-activities"></a>Verkþættir í vöruhúsi

Ef pöntunarstaðan er **opin** mun vöruhúsið ekki byrja að undirbúa sendinguna og ekki er búist við að hún berist með vörunum í innkaupapöntun. Þegar pöntunin er frágengin er gefið til kynna að pöntuninni sé lokið og að vöruhúsið geti innihaldið hana í verkþætti hennar.

## <a name="reopen-a-released-order"></a>Opna útgefna pöntun

Hægt er að breyta útgefinni pöntun með því að enduropna hana. Hins vegar er einungis hægt að auka magnið í þeim lína sem þegar er búið að vinna úr í vöruhúsinu.

Þegar breytingarnar eru gerðar og losa pöntunina aftur, [!INCLUDE [prod_short](includes/prod_short.md)] endurreiknar Virðisauki (VAT) og reikningsafsláttur.

Ef gerðar eru breytingar á útgefinni pöntun verður að láta vöruhúsið vita um breytingarnar.

> [!NOTE]
> Ef bóka á eina opna pöntun eða kreditreikning án þess að gefa hana út fyrst, [!INCLUDE [prod_short](includes/prod_short.md)] mun skjalið sjálfkrafa gefa út þegar það er bókað. Ef pantanir eða kreditreikningar eru **bókaðir með keyrslunni** Bóka er hægt að velja að bóka aðeins pantanir eða kreditreikninga sem hafa verið Útgefnir.

## <a name="see-also"></a>Sjá einnig .

[Selja vörur með sölupöntun viðskiptavinar](sales-how-sell-products.md)  
[Skrá innkaup með innkaupareikningum](purchasing-how-record-purchases.md)  
[Senda vörur](warehouse-how-ship-items.md)  
[Móttaka vara](warehouse-how-receive-items.md)  
[Nota Samþykktarverkflæði](across-how-use-approval-workflows.md)  
[Röðun, leit og síun í listum](ui-enter-criteria-filters.md)  
[Safnvista skjöl](across-how-to-archive-documents.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
