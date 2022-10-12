---
title: Stöðureitur á skjölum
description: Upplýsingar um stöðuna ' opin ' og ' Útgefin ' í tilboðum, pöntun eða kreditreikningsskjölum.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,
ms.search.form: ''
ms.date: 09/19/2022
ms.author: a-reishima
ms.openlocfilehash: c96909b4ee37673ee7b0c752224478a144ad853e
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608470"
---
# <a name="status-field-on-documents"></a>Stöðureitur á skjölum

Þegar stofnað er tilboð, pöntun eða kreditreikningur er **sjálfgefið að reiturinn Staða** í fylgiskjalshausnum opni **sjálfkrafa stöðuna**.

Þegar búið er að fylla út skjalið er hægt að losa það og [!INCLUDE[prod_short](includes/prod_short.md)] breyta gildinu í **reitnum Staða** til **losunar**. Það gefur til kynna að pöntunin sé tilbúin í næsta vinnsluáfanga áður en hún er bókuð.

| Staða | Lýsing |
| ------ | ----------- |
| Opinn   | Hægt að gera breytingar á fylgiskjalinu. |
| Losað | Skjalið hefur verið losað á næsta stigi vinnslu og ekki er hægt að gera breytingar á línum af gerðinni *Vara* og *eign*.<br /><br />Hægt er að opna útgefna fylgiskjalið aftur ef breyta á efni þess. Eigi að færa breytt fylgiskjal á næsta stig í meðhöndluninni þarf að gefa það út aftur. |
| Bíður samþykkis   | Fylgiskjalið bíður samþykktar. |
| Bíður fyrirframgreiðslu | Bókaður hefur verið fyrirframgreiðslureikningur fyrir skjalið. |

## <a name="releasing"></a>Gefa út

Hægt er að nota úttektarferlið á mismunandi hátt til að auðvelda eðlilegt vinnuflæði, til dæmis til að fylgja ferlum fyrirtækisins um samþykki eða til að ræsa vöruhúsaaðgerðir.

### <a name="approval-procedures"></a>Samþykktarferli

Fyrirtækið getur notað úttektarferlið til að sýna að annar notandi hafi samþykkt skjalið eða að utanaðkomandi tengiliður geti hitt lýsingarnar á skjalinu, eins og sýnt er í þessum dæmum:

* Aðeins er hægt að gefa út innkaupapöntun þegar lánardrottinn hefur gefið til kynna að hann geti uppfyllt pöntunina.
* Þegar búið að er búa til pöntun verður annar notandi að samþykkja hana, ef til vill af öryggisástæðum, áður en hægt er að gefa hana út.
* Kreditreikningur sem búinn hefur verið til verður að vera gefinn út af stjórnandanum sem ber ábyrgð á því að samþykkja allar endurgreiðslur.

Frekari upplýsingar um samþykktarverkflæði við [notkun verkflæða](across-use-workflows.md).

### <a name="warehouse-activities"></a>Verkþættir í vöruhúsi

Ef pöntunarstaðan er **opin** mun vöruhúsið ekki byrja að undirbúa sendinguna og ekki er búist við að hún fái vörurnar í innkaupapöntun. Þegar pöntunin er gefin út er gefið til kynna að pöntunin sé tilbúin og að vöruhúsið geti tekið hana með þeim aðgerðum sem þar fara fram.

## <a name="reopening-a-released-order"></a>Enduropnun á útgefinni pöntun

Hægt er að breyta útgefinni pöntun með því að enduropna hana. Hins vegar er einungis hægt að auka magnið í þeim lína sem þegar er búið að vinna úr í vöruhúsinu.

Þegar breytingar hafa verið gerðar og pöntunin er tekin út aftur er Virðisauki (VSK) og reikningsafsláttur endurreiknaður.

Ef gerðar eru breytingar á útgefinni pöntun verður að láta vöruhúsið vita um breytingarnar.

> [!NOTE]
> Ef bóka á eina opna pöntun eða kreditreikning án þess að gefa hana út fyrst gefur forritið sjálfkrafa út skjalið þegar það er bókað. Ef pantanir eða kreditreikningar eru bókaðir með **keyrslunni** Bóka er aðeins hægt að velja að bóka pantanirnar eða kreditreikningana sem hafa verið Útgefnir.

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
