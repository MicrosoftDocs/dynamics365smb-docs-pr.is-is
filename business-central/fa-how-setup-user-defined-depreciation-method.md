---
title: Uppsetning afskriftaaðferðar eignar sem notandi skilgreinir
description: Í Business Central er hægt að nota afskriftaaðferð sem notandi skilgreinir til að skilgreina afskriftaaðferð eignar á síðu eignaspjalds.
author: jill-kotel-andersson
ms.reviewer: edupont
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: edupont
---

# <a name="set-up-fixed-assets-with-user-defined-depreciation-methods"></a><a name="set-up-fixed-assets-with-user-defined-depreciation-methods"></a>Setja upp eignir með afskriftaaðferðum sem notandi skilgreinir

Hægt er að nota [!INCLUDE[prod_short](includes/prod_short.md)] til að setja upp afskriftaaðferðir sem notandi skilgrenir eins og lýst er hér.

Í hverri aðferð sem notandi skilgreinir sjálfur eru færðar inn afskriftaprósentur fyrir hvert tímabil (mánuð, ársfjórðung, ár eða reikningstímabil) á síðunni **Afskriftatöflur**. Síðan, ef úthlutuð er afskriftabók með notandaskilgreindri aðferð á eign, þarf að stilla reitina **Fyrsta not.skilgr. afskr.dags.** og **Upphafsdags. afskrifta** á síðunni **Eignaafskriftabækur** fyrir tiltekna eign.  

Reiknireglan fyrir útreikning á afskriftaupphæðum er:  

*Afskriftaupphæð = (Beinlínu % x Fjöldi afskr.daga x Afskriftagrunnur) / (100 x 360)*


> [!NOTE]  
> Dagsetningin í reitnum **Fyrsta not.skilgr. afskr.dags** er notuð til að ákvarða tímabilin, en **Upphafsdags. afskrifta** er notuð til að ákvarða fjölda afskriftadaga. Ef **Fyrsta not.skilgr. afskr.dags** kemur á undan **Upphafsdags. afskrifta** verður prósentan fyrir fyrsta tímabilið í afskriftatöflunni aðeins notuð að hluta til þegar forritið reiknar út fyrstu afskriftina. Það þýðir að eignin verður ekki að fullu afskrifuð við lok síðasta tímabilsins.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method"></a><a name="to-assign-a-depreciation-book-to-a-fixed-asset-with-a-user-defined-depreciation-method"></a>Að úthluta afskriftabók á eign með notandaskilgreindri afskriftaaðferð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
2. Valin er eignin sem setja á upp eignaafskriftabók fyrir.
3. Veldu aðgerðina **Tengd** og síðan **Eign** og síðan **Afskriftabækur**. Þá opnast síðan **Eignaafskriftabækur**.

   Sumir reitirnir sem þarf að fylla út samkvæmt leiðbeiningunum hér að neðan eru sjálfgefið faldir og því þarf að sýna þá. Til að gera þetta þarftu að sérstilla síðuna. Frekari upplýsingar eru í [Hefja sérstillingu á síðu með borðanum Sérstilla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).
4. Í reitnum **Afskriftaaðferð** skal velja **Notandaskilgreint**.
5. Í reitnum **Afskriftatöflukóði** skal velja **Afskriftatöfluna** sem á að nota.
6. Í reitnum **Upphafsdags. afskrifta** skal velja upphafsdag fyrir útreikning afskriftar.
7. Þegar þú notar notandaskilgreinda aðferð verður að stilla reitinn **Fyrsta not.skilgr. afskr.dags** á dagsetningu sem er sú sama eða á undan þeirri sem er í reitnum **Upphafsdags. afskrifta**. Ef valið hefur verið gildi í reitnum **Lengd tímabils** í afskriftatöflunni verður dagsetningin í reitnum **Fyrsta not.skilgr. afskr.dags** að vera upphafsdagur reikningstímabilsins.
8. Annaðhvort skal fylla út reitinn **Fjöldi afskriftaára** eða reitinn **Lokadags. afskrifta**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## <a name="to-set-up-user-defined-depreciation-methods"></a><a name="to-set-up-user-defined-depreciation-methods"></a>Uppsetning afskriftaaðferða sem notandi skilgreinir

Á síðunni **Afskriftatöfluspjald** er hægt að setja upp notendaskilgreinda afskriftaaðferðir. Til dæmis er hægt að setja upp afskriftir sem byggjast á fjölda eininga.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afskriftatöflur** og velja síðan viðkomandi tengil.  
2. Á síðunni **listi yfir afskriftartöflur** skal velja aðgerðina **Nýtt**.  
3. Á síðunni **Afskriftatöfluspjald** skal fylla inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Nota skal aðgerðina **Stofna töflu fyrir samtölu talna** til að skilgreina afskriftatöflu sem byggir á aðferðinni *Samtala talna*.

Með aðferðinni *Samtala talna*, ef föst eign er afskrifuð á fjórum árum verða afskriftir fyrir hvert ár reiknaðar svona:

Samtala talna = 1 + 2 + 3 + 4 = 10 Afskrift:

* Ár 1 = 4/10  
* Ár 2 = 3/10  
* Ár 3 = 2/10  
* Ár 4 = 1/10  

### <a name="depreciation-based-on-number-of-units"></a><a name="depreciation-based-on-number-of-units"></a>Afskriftir miðaðar við fjölda eininga

Notandaskilgreindu aðferðina má einnig nota til að afskrifa eftir fjölda eininga, til dæmis vélar sem hafa þekkta framleiðslugetu. Á síðunni **Afskriftatöflu** er hægt að færa inn fjölda eininga sem hægt er að framleiða á hverju tímabili mánuði, ársfjórðungi, ári eða reikningstímabili.  

### <a name="example---user-defined-depreciation"></a><a name="example---user-defined-depreciation"></a>Dæmi - Notandaskilgreindar afskriftaraðferð

Notuð er afskriftaaðferð sem gerir kleift að afskrifa eignir hraðar vegna tekjuskatts.  

Eftirfarandi afskriftaaðferð er notuð á eign með þriggja ára líftíma vegna skatta.  

* 1. ár: 25%  
* 2. ár: 38%  
* 3. ár: 37%  

Stofnkostnaðurinn er SGM 100.000 og afskrifanlegur líftími er fimm ár. Afskriftir eru reiknaðar árlega.  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| --- | --- | --- | --- | --- |
| 01/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta) |100,000.00 |100,000.00 |
| 12/31/20 |Afskrift |360 |-25.000,00 |75,000.00 |
| 12/31/21 |Afskrift |360 |-38.000,00 |37,000.00 |
| 12/31/22 |Afskrift |360 |-37.000,00 |0 |
| 12/31/23 |Afskrift |Engin |Engin |0 |
| 12/31/24 |Afskrift |Engin |Engin |0 |

Í fyrra dæminu yrðu báðir reitirnir **Fyrsta not.skilgr. afskr.dags.** og **Upphafsdags. afskrifta** stilltir á 01/01/20 á síðunni **Eignaafskriftabækur** fyrir tiltekna eign. Ef í reitnum **Fyrsta not.skilgr. afskr.dags.** er þó 01/01/20 og í reitnum **Upphafsdags. afskriftar** er 01/04/20 yrði útkoman:  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| --- | --- | --- | --- | --- |
| 01/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta) |100,000.00 |100,000.00 |
| 12/31/20 |Afskrift |270 |-18.750,00 |81,250.00 |
| 12/31/21 |Afskrift |360 |-38.000,00 |42,250.00 |
| 12/31/22 |Afskrift |360 |-37.000,00 |6,250.00 |
| 12/31/23 |Afskrift |90 |-6.250,00 |0 |
| 12/31/24 |Afskrift |Engin |Engin |0 |


## <a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Setja upp eignaafskriftir](fa-how-setup-depreciation.md)  
[Afskriftaaðferðir fyrir eignir](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
