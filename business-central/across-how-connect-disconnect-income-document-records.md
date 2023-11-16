---
title: Stofna færslur skjala á innleið úr skjölum
description: Hægt er að vista ytri viðskiptaskjöl með því að hengja skjöl við tengdar færslur skjala á innleið.
author: jswymer
ms.topic: how-to
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 02/23/2023
ms.author: jswymer
ms.reviewer: jswymer
ms-service: dynamics365-business-central
ms.custom: bap-template
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Stofna skjalaskrár sem berast beint úr skjölum og færslum

Hægt er að vista ytri viðskiptaskjöl í [!INCLUDE[prod_short](includes/prod_short.md)] með því að hengja skjöl við tengdar færslur skjala á innleið. Ef skjalið, s.s. innkaupareikningur, var upprunlega ekki færsla skjals á innleið, er samt hægt að stofna og tengja færslur skjals á innleið við það síðar. Einnig er hægt að hengja skjöl á innleið við bókuð innkaupa- og söluskjöl og við færslur lánardrottins, viðskiptamanns og fjárhagsfærslur með því að nota upplýsingakassann **Skjöl á innleið** á til dæmis síðunum **Bókaðir innkaupareikningar** og **Lánardrottnabók**.

Á síðunum **Bókhaldslyklar** og **Fjárhagsfærslur** er hægt að nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð innkaupa- og söluskjöl sem hafa ekki færslur fyrir skjöl á innleið og tengjast miðlægt við fyrirliggjandi færslur eða stofna nýjar með viðhengdum skrám. Nánari upplýsingar er að finna í [Finna bókuð skjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md).

Eftirfarandi ferli sýna hvernig á að hengja skrá við lánardrottnafærslu eða fyrirliggjandi innkaupareikning sem var ekki stofnaður úr færslu skjals á innleið. Að festa viðhengi við bókað innkaupa- eða söluskjal fer fram á svipaðan hátt.

## <a name="create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Stofna og tengja komandi skjalfærslu úr innkaupareikningi

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Veljið línu fyrir innkaupareikning sem á að hengja skrá við og veljið síðan aðgerðina **Búa til skjal á innleið úr skrá**.
3. Einnig er hægt að velja línu fyrir innkaupareikning sem á að hengja skrá við og velja svo aðgerðina **Hengja skrá við**.
4.  **Á síðunni INSERT-skrá**  skal gera einn af eftirtöldum skrefum til að hengja upp skrá sem táknar skjalið sem um er að ræða:

   [!INCLUDE[file-upload](includes/file-upload.md)]


## <a name="create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Stofna og tengja komandi skjalafærslu úr lánardrottnafærslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Lánardrottnafærslur** og veldu síðan tengda tengilinn.
2. Veljið línu fyrir lánardrottnafærslu sem á að hengja skrá við og veljið síðan aðgerðina **Búa til skjal á innleið úr skrá**.
3. Einnig er hægt að velja línu fyrir lánardrottnafærslu sem á að hengja skrá við og velja svo aðgerðina **Hengja skrá við**.
4.  **Á síðunni INSERT-skrá**  skal gera einn af eftirtöldum skrefum til að hengja upp skrá sem táknar skjalið sem um er að ræða:

   [!INCLUDE[file-upload](includes/file-upload.md)]


## <a name="remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Fjarlægja tengingu úr skjalfærslu skjals yfir í bókað skjal

Hægt er að fjarlægja viðhengi skjals úr óbókuðum skjölum hvenær sem er með því að eyða tengdum færslum fyrir skjöl á innleið. Ef skjalið er bókað verður fyrst að fjarlægja tengingu úr færslu fyrir skjal á innleið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Veljið línu fyrir færslu skjals á innleið sem tengist bókaða fylgiskjalinu sem á að fjarlægja og veljið svo aðgerðina **Fjarlægja tilvísun í skrá**.

Tengingin við bókað skjal var var fjarlægt. Nú er hægt að tengja aðra færslu skjals á innleið við bókað skjal eins og lýst er í þessari grein.

## <a name="see-also"></a>Sjá einnig .

[Stofna færslur skjala á innleið](across-how-create-income-document-records.md)
[Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md)
[Finna bókuð fylgiskjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md)
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
