---
title: Hönnunarupplýsingar - bókunarstrúktúr vörurakningar
description: Lærðu hvernig nota skal birgðabókarfærslur sem aðalflutningsaðili vörurakningarnúmera í bókunarskipulagi vörurakningar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item tracking, posting, inventory
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: b568e62a71b907e8d2f9cbc8eba43773be655b44
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136323"
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
  
## <a name="codeunits-80-and-90"></a>Kóðaeiningar 80 og 90  
Til að skipta birgðahöfuðbókarfærslum við bókun, er kóðinn í kóðaeiningu 80 og kóðaeiningu 90, er með lykkjum sem keyra í gegnum altæka tímabundnar færslubreytur. Þessi kóði kallar á kóðaeiningu 22 með birgðarbókarlínu. Þessar breytur eru frumstilltar þegar vörurakningarnúmer eru til fyrir skjalalínuna. Til að halda kóðann einfalt, þessi lykkjuuppbyggingu er alltaf notuð. Ef engin vörurakningarnúmer eru til staðar fyrir skjalalínuna er ein færsla sett inn og lykkjan er einungis unnin einu sinni.  
  
## <a name="posting-the-item-journal"></a>Birgðabókin bókuð  
Vörurakningarnúmer eru flutt fyrir milligöngu frátekningarfærslna sem tengjast birgðafærslunni og lykkjumyndum gegnum vörurakningarnúmer á sér stað í kóðaeiningu 22. Þessi hugmynd virkar á sama hátt þegar birgðafærslulína er notuð óbeint til að bóka sölu eða innkaupapöntun og þegar birgðafærslulína er notuð beint. Þegar birgðabók er notuð beint er vísar reiturinn **uuppsprettulínuauðkenni** beint á sjálfa birgðabókarlínuna.  
  
## <a name="code-unit-22"></a>Kóðaeining 22  
Kóðaeiningar 80 og 90 lykkja hringingu frá kóðaeiningu 22 við bókun reiknings fyrir vörurakningarnúmer og við reikningsfræslu á fyrirliggjandi sendingum eða móttökum.  
  
Við magnbókun vörurakningarnúmera, sækir kóðaeining 22 vörurakningarnúmer úr færslum í T337 sem tengjast bókuninni. Þessar færslur eru settar beint á birgðabókarlínuna.  
  
Kóðaeining 22 lykkjast gegnum vörurakningarnúmer og skiptir bókuninni í þær birgðabókarfærslur sem bera þau vörurakningarnúmer. Upplýsingar um hvaða birgðabókarfærslur eru búnar til er skilað til T337 með tímabundna T336 skrá, sem kennt er við ferli í kóðaeiningu 22. Þessi aðferð er kölluð fram þegar kóðaeining 22 hefur lokið þess að keyra vegna á þeim tímapunkti kóðaeining 22 hluturinn inniheldur upplýsingar. Þegar tímabundinT336 færsla er endurheimt, stofna kóðaeiningar 80 og 90 færslur í töflunni **Birgðafærslutengsl** til að tengja stofnuðu birðgabókarfærslurnar við stofnuðu sendingarlínuna eða inngreiðslulínuna. Kóðaeiningar 80 eða 90 umbreyta síðan tímabundum skrám T336 í raunfærslur T336 sem eru tengdar við línu sem um ræðir. Hins vegar eiga þessi viðskipti sér aðeins stað aðeins ef bókuðu skjalalínunni er ekki eytt, vegna þess að hún er aðeins bókuð að hluta til.  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)   
[Hönnunarupplýsingarn: vörurakning hönnun](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]