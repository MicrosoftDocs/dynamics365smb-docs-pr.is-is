---
title: Hönnunarupplýsingar - bókunarstrúktúr vörurakningar
description: Lærðu hvernig nota skal birgðabókarfærslur sem aðalflutningsaðili vörurakningarnúmera í bókunarskipulagi vörurakningar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-item-tracking-posting-structure"></a>Hönnunarupplýsingar: bókunarstrúktúr vörurakningar
Til að jafna með birgðakostnaðarvirkni og til að fá einfaldari og öflugri lausn, erubirgðabókarfærslur notaðar sem aðalflutningsaðili vörurakningarnúmera.  
  
Vörurakningarnúmer í rekstrareiningum innan og utan pöntunarnets eru tilgreind í töflunni **Frátekningarfærsla** (T337). Vörurakningarnúmer sem tengjast sögulegum upplýsingum eru sótt beint úr birgðahöfuðbókarfærslum sem tengjast viðkomandi færslu. Þetta þýðir að birgðahöfuðbókarfærslur endurspegla vörurakningarforskrift á bókaðri pöntunarlínu.  
  
Síðan fyrir **vörurakningarlínur** endurheimtir upplýsingar úr T337 og úr birgðafærslum og sýnir þær í bráðabirgðatöflunni **Rakningarlýsing** (T336). T336 heldur einnig tímabundnum gögnum á **Síðu vörurakningarlína** fyrir vörurakningarmagn sem á eftir að reikningsfæra.  
  
## <a name="one-to-many-relation"></a>Tengsl eins í marga
Taflan **Birgðafærslutengsl**, sem skal nota til að tengja bókaða fylgiskjalslínu við tengdar birgðafærslur, samanstendur af tveimur meginhlutum:  
  
* Bendill á bókuðu skjalalínuna, reiturinn **Pöntunarlínunr.** .  
* Færslunúmer bendir til birgðahöfuðbókarfærslu, reitsins **Birgðafærslunr.**.  
  
Virkni núverandi **Færslunr.** reitar, sem tengir birgðafærslu við bókaða skjalalínu, meðhöndlar dæmigerð tengsl tveggja eininga þegar engin vörurakningarnúmer eru til staðar á bókuðu skjalalínunni. Ef vörurakningarnúmer eru til er reiturinn **Færslunr.** skilinn eftir auður, og tengslin einn-á-móti-mörgum eru meðhöndluð af töflunni **Tengsl birgðafærslu**. Ef bókaða skjalalínan er með vörurakningarnúmer en tengist aðeins einni birgðafærslu sér reiturinn **Færslunr.** um tengslin og engin færsla er skráð í töflunni **Tengsl birgðafærslu**.  
  
## <a name="codeunits-80-sales-post--and-90-purch-post"></a>Codeunit 80 (Sölubók) og 90 (Innk.bókun)
Til að skipta birgðahöfuðbókarfærslum við bókun, er kóðinn í kóðaeiningu 80 og kóðaeiningu 90, er með lykkjum sem keyra í gegnum altæka tímabundnar færslubreytur. Þessi kóði kallar á kóðaeiningu 22 með birgðarbókarlínu. Þessar breytur eru frumstilltar þegar vörurakningarnúmer eru til fyrir skjalalínuna. Til að halda kóðann einfalt, þessi lykkjuuppbyggingu er alltaf notuð. Ef engin vörurakningarnúmer eru til staðar fyrir skjalalínuna er ein færsla sett inn og lykkjan er einungis unnin einu sinni.  
  
## <a name="posting-the-item-journal"></a>Birgðabókin bókuð
Vörurakningarnúmer eru flutt í gegnum frátekningarfærslurnar sem tengjast birgðafærslunni og lykkjan gegnum vörurakningarnúmerin á sér stað í codeunit 22 (Birgðabókarlína). Þessi hugmynd virkar á sama hátt þegar birgðafærslulína er notuð óbeint til að bóka sölu eða innkaupapöntun og þegar birgðafærslulína er notuð beint. Þegar birgðabók er notuð beint er vísar reiturinn **uuppsprettulínuauðkenni** beint á sjálfa birgðabókarlínuna.  
  
## <a name="code-unit-22--item-jnl-post-line"></a>Kóti 22 (Birgðabókarlína)
Codeunit 80 (Sölubók) og 90 (Innk.bókun) lykkja símtalið við codeunit 22 (Birgðabókunarlína) við reikningsbókun vörurakningarnúmera og við reikningsfærslu fyrirliggjandi afhendinga eða móttöku.  
  
Við magnbókun vörurakningarnúmera sækir codeunit 22 (Birgðabókunarlína) vörurakningarnúmer úr færslunum í T337 (frátekningarfærsla) sem tengjast bókuninni. Þessar færslur eru settar beint á birgðabókarlínuna.  
  
Codeunit 22 (Birgðabókarlína) lykkur í gegnum vörurakningarnúmerin og skiptir bókuninni í viðeigandi birgðafærslur sem hafa vörurakningarnúmerin. Upplýsingum um hvaða birgðafærslur eru stofnaðar er skilað til T337 (Frátekningarfærsla)með því að nota Bráðabirgða T336-færslu sem kallast ferli í codeunit 22. Þessi aðferð er kölluð fram þegar kóðaeining 22 hefur lokið þess að keyra vegna á þeim tímapunkti kóðaeining 22 hluturinn inniheldur upplýsingar. Þegar tímabundin færsla T336 er sótt stofna codeunit 80 (Sölubók) og 90 (Innk.bókun) færslur í **töflunni Birgðafærslutengsl** til að tengja stofnaðar birgðafærslur í stofnuðu afhendingar- eða móttökulínuna. Codeunit 80 (Sales-Post) og 90 (Innkaup-Post) breytir síðan bráðabirgða færslunum T336 (Rakningarlýsing) í raunverulegar T336 (Rakningarlýsing) færslur sem tengjast viðkomandi línu. Hins vegar eiga þessi viðskipti sér aðeins stað aðeins ef bókuðu skjalalínunni er ekki eytt, vegna þess að hún er aðeins bókuð að hluta til.  
  
## <a name="see-also"></a>Sjá einnig
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)   
[Hönnunarupplýsingarn: vörurakning hönnun](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
