---
title: Stöðureitur á skjölum
description: 'Kynntu þér „Opna“ og „Útgefna“ stöðu á tilboðs-, pöntunar- eða kreditreikningsskjölum.'
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="status-field-on-documents"></a>Stöðureitur á skjölum

Þegar búið er til tilboð, pöntun eða kreditreikningur er **Staða** í stöðureitnum í skjalhausnum sjálfgefin **Opið**.

Þegar skjalið er fyllt út má gefa það út og [!INCLUDE[prod_short](includes/prod_short.md)] mun breyta gildinu í reitnum **Staða** í **Útgefið**. Þessi staða gefur til kynna að pöntunin sé tilbúin í næsta vinnsluáfanga áður en hún er bókuð.

| Staða | Lýsing |
| ------ | ----------- |
| Opinn   | Hægt að gera breytingar á fylgiskjalinu. |
| Losað | Fylgiskjalið hefur verið gefið út fyrir næsta stig í ferlinu og ekki er hægt að gera breytingar á línum af gerðinni *Vara* og *Eign*.<br /><br />Hægt er að opna útgefna fylgiskjalið aftur ef breyta á efni þess. Eigi að færa breytt fylgiskjal á næsta stig í meðhöndluninni þarf að gefa það út aftur. |
| Bíður samþykkis   | Fylgiskjalið bíður samþykktar. |
| Bíður fyrirframgreiðslu | Bókaður hefur verið fyrirframgreiðslureikningur fyrir skjalið. |

## <a name="release-process"></a>Útgáfuferli

Hægt er að nota útgáfuferlið á mismunandi vegu til að liðka fyrir venjulegu verkflæði, til dæmis til að fylgja ferlum fyrirtækis hvað varðar samþykktir eða stöðu vöruhúsaaðgerða.

### <a name="approval-procedures"></a>Samþykktarferli

Hægt er að nota útgáfuferlið til að gefa til kynna að annar notandi hafi samþykkt skjalið eða að utanaðkomandi tengiliður geti mætt skilgreiningunum skjalsins eins og eftirfarandi dæmi sýna:

* Aðeins er hægt að gefa út innkaupapöntun þegar lánardrottinn hefur gefið til kynna að hann geti uppfyllt pöntunina.
* Þegar búið að er búa til pöntun verður annar notandi að samþykkja hana, ef til vill af öryggisástæðum, áður en hægt er að gefa hana út.
* Stjórnandinn sem ber ábyrgð á því að samþykkja allar endurgreiðslur verður að gefa út kreditreikning sem þú hefur búið til.

Frekari upplýsingar um samþykktarferli er að finna undir [Nota vinnuferli](across-use-workflows.md).

### <a name="warehouse-activities"></a>Vöruhúsaaðgerðir

Ef pöntunarstaðan er **Opin** er ekki hafist handa við að undirbúa sendinguna í vöruhúsinu né heldur er búist við því að fá vörurnar sem eru í innkaupapöntuninni. Þegar pöntunin er gefin út er gefið til kynna að pöntunin sé tilbúin og að vöruhúsið geti tekið hana með þeim aðgerðum sem þar fara fram.

## <a name="reopen-a-released-order"></a>Enduropna útgefna pöntun

Hægt er að breyta útgefinni pöntun með því að enduropna hana. Hins vegar er einungis hægt að auka magnið í þeim lína sem þegar er búið að vinna úr í vöruhúsinu.

Þegar breytingarnar eru gerðar og pöntunin er gefin út aftur mun [!INCLUDE [prod_short](includes/prod_short.md)] reikna aftur út VSK og reikningsafsláttinn.

Ef gerðar eru breytingar á útgefinni pöntun verður að láta vöruhúsið vita um breytingarnar.

> [!NOTE]
> Ef bóka á eina opna pöntun eða kreditreikning án þess að gefa hana út fyrst gefur [!INCLUDE [prod_short](includes/prod_short.md)] sjálfkrafa út skjalið þegar það er bókað. Ef pantanirnar eða kreditreikningarnir eru bókaðir með því að nota aðgerðina **Bóka runu** er hægt að velja að bóka aðeins pantanir eða kreditreikninga sem búið er að gefa út.

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
