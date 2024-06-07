---
title: Þjónustupöntunarstaða og viðgerðarstaða
description: Þjónustupöntunarstaðan sýnir viðgerðarstöðu allra þjónustuvara í þjónustupöntuninni.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="service-order-status-and-repair-status"></a>Þjónustupöntunarstaða og viðgerðarstaða

Reitirnir **Staða** á síðunni **Þjónustupöntun** og þjónustuvöruviðgerðarstaðan sem vísað er til í reitnum **Viðgerðarstöðukóti** á síðunni **Þjónustupöntun** hafa ákveðið samband í Þjónustukerfi. Þjónustupöntunarstaðan sýnir viðgerðarstöðu allra þjónustuvara í þjónustupöntuninni.  

> [!NOTE]  
> Þessir tveir stöðureitir tengjast ekki reitnum **Losunarstaða** á þjónustupöntunarhausnum, sem ákvarðar hvernig vöruhúsið meðhöndlar þjónustuvörur.  

Í hvert sinn sem viðgerðarstöðu þjónustuvöru er breytt í þjónustupöntun er staða pöntunarinnar uppfærð. Til að forritið sýni stöðuna sem sýnir yfirlit yfir viðgerðarstöðuna hjá einstökum þjónustuvörum verður að tilgreina eftirfarandi:  

* Staða þjónustupöntunar sem allar viðgerðarstöður tengjast.  
* Forgangsröð fyrir hvern valkost þjónustupöntunarstöðu.  

Þegar þjónustutilboði er breytt í þjónustupöntun breytir kerfið viðgerðarstöðu hverrar þjónustuvöru í pöntuninni í **Byrjun** og stöðu þjónustupöntunar í **Í undirbúningi**.  

> [!NOTE]
> Áður en hægt er að búa til þjónustupantanir þarf að setja upp viðgerðarstöðu og forgang þjónustustöðu. Frekari upplýsingar eru í [Setja upp stöður fyrir þjónustupantanir og viðgerðir](service-order-repair-status.md).

## <a name="specifying-service-order-status-for-repair-status"></a>Þjónustupöntunarstaða tilgreind fyrir viðgerðarstöðu

Hver viðgerðarstaða er tengt tiltekinni þjónustupöntunarstöðu. Valkostirnir fyrir þjónustupöntunarstöðuna eru eftirfarandi:

* **Í undirbúningi**
* **Í vinnslu**
* **Bið**
* **Lokið**

Valkostirnir fyrir viðgerðarstöðu eru eftirfarandi:

* **Byrjun**
* **Í vinnslu**
* **Sent áfram**
* **Hluta þjónustu lokið**
* **Tilboði lokið**
* **Beðið eftir viðskiptavini**
* **Íhlutur pantaður**
* **Íhlutur móttekin**
* **Lokið**  

### <a name="pending"></a>Í undirbúningi

Þjónustupöntunarstaðan **Í undirbúningi** gefur til kynna að þjónustan geti hafist eða haldið áfram hvenær sem er. Því er hægt að tengja viðgerðarstöðuvalkostina **Byrjun**, **Verki vísað**, **Hluta þjónustu lokið** og **Varahlutur móttekinn** við þjónustupöntunarstöðuna.  

### <a name="in-process"></a>Í vinnslu

Þjónustupöntunarstaðan **Í vinnslu** gefur til kynna að þjónustan sé í vinnslu. Því er hægt að tengja viðgerðarstöðuvalkostina **Í vinnslu** og **Varahlutur pantaður** við þjónustupöntunarstöðuna. Ef staðan **Varahlutur pantaður** er tengd við þjónustupöntunarstöðuna **Í vinnslu** verður einnig að tengja stöðuna **Varahlutur móttekinn** við þessa þjónustupöntunarstöðu.  

### <a name="on-hold"></a>Bið

Þjónustupöntunarstaðan **Bið** gefur til kynna að þjónustan sé um stundarsakir í bið þar sem beðið sé eftir viðbrögðum frá viðskiptavini eða varahlutum áður en þjónustan getur hafist. Því er hægt að tengja viðgerðarstöðuvalkostina **Tilboði lokið**, **Varahlutur pantaður** og **Beðið eftir viðskiptavini** við þjónustupöntunarstöðuna.  

### <a name="finished"></a>Lokið

Þjónustupöntunarstaðan **Lokið** gefur til kynna að þjónustunni sé lokið. Því er viðgerðarstaðan **Lokið** tengd við þessa stöðu.  

## <a name="assigning-priority-to-service-order-status"></a>Þjónustupöntunarstöðu úthlutað forgangi

Þegar viðgerðarstöðu þjónustuvöru er breytt eru þjónustupöntunarstöðurnar tengdar við viðgerðarstöður allra þjónustuvaranna í pöntuninni. Ef þjónustuvaran tengist einni eða fleiri þjónustupöntunarstöðuvalkostum er þjónustupöntunarstöðuvalkosturinn valinn sem gefur mesta forgangsröð.  

Ákveða þarf hvaða þjónustupöntunarstöðuvalkostur hefur mikilvægustu upplýsingarnar í stöðunni í þjónustupöntuninni og setja þá stöðu efst í forgangsröðina o.s.frv.  

Þegar ný þjónustupöntun er stofnuð og vörum er bætt við hana er reiturinn **Forgangur** í þjónustupöntunarhausnum uppfærður út frá forgangsröðunum á þjónustuvörunum.  

### <a name="example"></a>Dæmi

Dæmigerð úthlutun forgangsraðar gæti verið sem hér segir:  

* Í vinnslu - Mikill  
* Í undirbúningi - Í meðallagi mikill  
* Bið - Í meðallagi lítill  
* Lokið - Lítill  

Ef ein þjónustuvara er til dæmis með viðgerðarstöðuna **Byrjun** tengda við þjónustupöntunarstöðuna **Í undirbúningi**, önnur er með viðgerðarstöðuna **Í vinnslu**, tengda við þjónustupöntunarstöðuna **Í vinnslu** og sú þriðja er með viðgerðarstöðuna **Varahlutur pantaður**, tengda við þjónustupöntunarstöðuna **Bið**, verður útkoman staðan **Í vinnslu** þar sem hún er með mestan forgang.  

## <a name="see-also"></a>Sjá einnig

[Setja upp stöður fyrir þjónustupantanir og viðgerðir](service-order-repair-status.md)  
[Þjónustustýring sett upp](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
