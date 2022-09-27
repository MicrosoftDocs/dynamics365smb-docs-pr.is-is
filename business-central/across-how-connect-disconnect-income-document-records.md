---
title: Stofna færslur skjala á innleið úr skjölum
description: Hægt er að vista ytri viðskiptaskjöl með því að hengja skjöl við tengdar færslur skjala á innleið.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/14/2022
ms.author: edupont
ms.openlocfilehash: 81dc6b8cff380e6eb9cf2fd6ef01be140914bc06
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532242"
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Stofna færslur yfir Skjöl á innleið, beint úr Skjöl og Færslur

Hægt er að vista ytri viðskiptaskjöl í [!INCLUDE[prod_short](includes/prod_short.md)] með því að hengja skjöl við tengdar færslur skjala á innleið. Ef skjalið, eins og innkaupareikningur, fann ekki tilvist þess sem færslu skjals er enn hægt að stofna og tengja komandi skjalaskráningu við það síðar. Einnig er hægt að hengja skjöl á innleið við bókuð innkaupa- og söluskjöl og við færslur lánardrottins, viðskiptamanns og fjárhagsfærslur með því að nota upplýsingakassann **Skjöl á innleið** á til dæmis síðunum **Bókaðir innkaupareikningar** og **Lánardrottnabók**.

**Í bókhaldslykilinn og** **á síðum bókhaldanna** er hægt að nota Leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð innkaupa-og söluskjöl sem hafa ekki færslur á innleið og svo tengja þær við eldri færslur eða stofna nýjar með viðhengdar skjalaskrár. Nánari upplýsingar er að finna í [Finna bókuð skjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md).

Eftirfarandi ferli sýna hvernig á að tengja skrá við lánardrottnafærslu eða innkaupareikning sem fyrir er sem ekki var stofnaður úr skjalafærslu á innleið. Að festa viðhengi við bókað innkaupa- eða söluskjal fer fram á svipaðan hátt.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Að stofna og tengja færslu skjals á innleið úr innkaupareikningi

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Veljið línu fyrir innkaupareikning sem á að hengja skrá við og veljið síðan aðgerðina **Búa til skjal á innleið úr skrá**.
3. Einnig er hægt að velja línu fyrir innkaupareikning sem á að hengja skrá við og velja svo aðgerðina **Hengja skrá við**.
4. Á síðunni **Setja inn skrá** skal velja skrána sem táknar skjalið á innleið og svo hnappinn **Opna**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Að stofna og tengja færslu skjals á innleið úr fjárhagsfærsla lánardrottins

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Lánardrottnafærslur** og veldu síðan tengda tengilinn.
2. Veljið línu fyrir lánardrottnafærslu sem á að hengja skrá við og veljið síðan aðgerðina **Búa til skjal á innleið úr skrá**.
3. Einnig er hægt að velja línu fyrir lánardrottnafærslu sem á að hengja skrá við og velja svo aðgerðina **Hengja skrá við**.
4. Á síðunni **Setja inn skrá** skal velja skrána sem táknar skjalið á innleið og svo hnappinn **Opna**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Til að fjarlægja tengingu á milli færslu fyrir skjal á innleið og bókaðs skjals

Hægt er að fjarlægja viðhengi skjals úr óbókuðum skjölum hvenær sem er með því að eyða tengdum færslum fyrir skjöl á innleið. Ef skjalið er bókað verður fyrst að fjarlægja tengingu úr færslu fyrir skjal á innleið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Veljið línu fyrir færslu skjals á innleið sem tengist bókaða fylgiskjalinu sem á að fjarlægja og veljið svo aðgerðina **Fjarlægja tilvísun í skrá**.

Tengingin við bókað skjal var var fjarlægt. Nú er hægt að halda áfram að tengja aðra færslu skjals við bókaða skjalið eins og lýst er í þessari grein.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Stofna komandi skjalaskrár](across-how-create-income-document-records.md)[
 nota OCR til að kveikja PDF-og myndskrár inn í rafræn skjöl 
](across-how-use-ocr-pdf-images-files.md)[finna bókuð skjöl án þess að skjalaskrár](across-how-find-posted-documents-without-income-document-records.md)
[á innleið séu stofnaðar](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
