---
title: Úrræðaleita fyrirtækjamiðstöðina
description: Kynnið ykkur hvernig hægt er að leysa vandamál þegar fyrirtækjamiðstöðin er notuð í Dynamics 365 Business Central til að stjórna vinnu í mörgum fyrirtækjum.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accountant, accounting, troubleshoot'
ms.search.form: 1151
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="troubleshooting-your-company-hub"></a><a name="troubleshooting-your-company-hub"></a><a name="troubleshooting-your-company-hub"></a>Úrræðaleita fyrirtækjamiðstöðina

Það er auðvelt að bæta fyrirtækjum við stjórnborð fyrirtækjamiðstöðvarinnar, en þessi grein fjallar um vandamál sem kunna að koma upp.  

## <a name="check-errors"></a><a name="check-errors"></a><a name="check-errors"></a>Leita að villum

Notið aðgerðina **Villuleit** til að skoða lista yfir nýlegar villur. Hægt er að sjá frekari upplýsingar fyrir hverja villu og hægt er að hreinsa kladdann með því að eyða eldri færslum.  

## <a name="connection-failed"></a><a name="connection-failed"></a><a name="connection-failed"></a>Tenging mistókst

Það geta verið nokkrar ástæður fyrir því af hverju ekki er hægt að tengjast fyrirtæki, þ.m.t. eitt af eftirfarandi:

- Vefslóðin í reitnum **Tengill umhverfis** er ekki gild  

  Farðu á síðuna **Umhverfistenglar**, opnið umhverfið sem ekki er hægt að tengjast við og veljið siðan aðgerðina **Prófa tenginguna**.  
- Fyrirtæki viðskiptamannsins er nú ótengt, til dæmis ef verið er að uppfæra það

  Á yfirlitinu skaltu velja **Verkfæri** valmyndaratriði og svo **Villuleit**. Þetta opnar lista með tæknilegum upplýsingum, svo þú kannt að vilja hafa samband við kerfisstjóra ef þú sérð villur. Til dæmis benda villuskilaboðin „*Netþjónninn hefur hafnað upplýsingum viðskiptamanns*“ til þess að þú hafir ekki aðgang.  
- Þú hefur ekki aðgang að öllum fyrirtækjum í umhverfinu sem reynt er að tengjast við

  Í [!INCLUDE [prod_short](includes/prod_short.md)] getur samsteypa verið með margar fyrirtækiseiningar sem kallast fyrirtæki og hugsanlega ertu ekki með aðgang að öllum fyrirtækjum. Hafðu samband við stjórnandann eða viðskiptavininn til að ganga úr skugga um að þú sért með aðgang að fyrirtækjunum sem þú þarft að vinna í.  

## <a name="data-does-not-refresh"></a><a name="data-does-not-refresh"></a><a name="data-does-not-refresh"></a>Gögn uppfærast ekki

Þegar þú bætir við fyrirtæki eða biður um uppfærslu gagna sækir [!INCLUDE [prod_short](includes/prod_short.md)] gögnin. Þú verður að uppfæra síðuna sjálfur, svo sem að velja aðgerðina **Endurbirta öll fyrirtæki**, uppfæra vafrasíðuna, fara af yfirlitinu og svo aftur í það eða annað svipað.  

Ef þú hefur bætt við fyrirtæki en það birtist ekki á listanum er einnig hægt að nota aðgerðina **Endurhlaða öllum fyrirtækjum** til að uppfæra listann.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Stjórna vinnu yfir mörg fyrirtæki í fyrirtækjamiðstöðinni](company-hub.md)  
[Bæta fyrirtækjum við fyrirtækjamiðstöðina](company-hub-add-company.md)  
[Upplifun endurskoðanda í Business Central](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
