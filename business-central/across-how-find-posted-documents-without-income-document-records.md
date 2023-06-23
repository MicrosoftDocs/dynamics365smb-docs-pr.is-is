---
title: Finna bókuð fylgiskjöl án skjals á innleið
description: 'Hægt að nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð innkaupa- og söluskjöl sem hafa ekki rafræn skjöl á innleið, eins og t.d. innfluttir reikningar.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="find-posted-documents-without-incoming-document-records" />Finna bókuð fylgiskjöl án færslu skjals á innleið

Á síðunum **Bókhaldslyklar** og **Fjárhagsfærslur** er hægt að nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð innkaupa- og söluskjöl sem hafa ekki færslur fyrir skjöl á innleið og tengjast miðlægt við fyrirliggjandi færslur eða stofna nýjar með viðhengdum skrám.

## <a name="to-find-posted-documents-without-incoming-document-records" />Hvernig á að finna bókuð fylgiskjöl án færslu skjals á innleið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.
2. Veljið línu fyrir þann fjárhagsreikning þar sem skoða á fjárhagsfærslur og bókuð innkaupa- og söluskjöl án færslna fyrir skjöl á innleið og veljið síðan **bókuð skjöl án skjal á innleið**
3. Einnig, Valið er **fjárhagsfærslur** aðgerð.
4. Á síðunni **fjárhagsfærslur**, veljið aðgerðina **bókuð skjöl án skjala á innleið**.

Síðan **Bókuð fylgiskjöl án skjals á innleið** opnast og hún sýnir bókuð innkaupa- og söluskjöl án færslna fyrir skjöl á innleið sem tengjast fjárhagsfærslum á fjárhagsreikningi sem síðan var opnuð fyrir. Síðan getur birt mest 1000 línur í einu. Sjálfgefið inniheldur reiturinn **dagsetningarafmörkun** því síu sem takmarkar línurnar við færslur með bókunardagsetningum frá upphafi bókhaldstímabils til vinnudagsetningar.

## <a name="to-connect-found-documents-to-existing-incoming-document-records" />Til að tengja fundin skjöl við fyrirliggjandi færslur skjala á innleið

1. Á síðunni **Bókuð fylgiskjöl án skjals á innleið** skal velja línu fyrir bókað skjal sem á að tengja við fyrirliggjandi færslu skjals á innleið, og veljið svo aðgerðina velja **skjal á innleið**.
2. Á síðunni **Skjöl á innleið** skal velja færslu fyrir skjal á innleið sem tengja á við bókað skjal sem fannst og velja svo hnappinn **Í lagi**.
3. Á síðunni **Bókuð fylgiskjöl án skjals á innleið** er valin færsla skjals á innleið nú tengt við bókaða skjalið, eins og sjá má í upplýsingakassanum **skrár fyrir skjal á innleið**.

Ef viðkomandi færsla skjals á innleið er ekki til á síðunni **Skjöl á innleið** er hægt að stofna hana. Frekari upplýsingar eru í [Stofna færslur skjala á innleið](across-how-create-income-document-records.md).

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Sjá tengda [Microsoft þjálfun](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Stofna færslur skjala á innleið](across-how-create-income-document-records.md)
[Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md)
[Stofna færslur yfir skjöl á innleið, beint úr skjölum og færslum](across-how-connect-disconnect-income-document-records.md)
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
