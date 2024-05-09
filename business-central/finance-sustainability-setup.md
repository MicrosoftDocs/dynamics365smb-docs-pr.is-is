---
title: Sjálfbærniuppsetning
description: Læra hvernig setja á upp sjálfbærniaðgerðir.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="sustainability-setup"></a>Sjálfbærniuppsetning

Til að sjálfbærnieiningin vinni rétt þarf fyrst að setja upp nokkur grunneftirlit og leiðbeiningar sem tengjast allri virkni.  

Til að setja upp sjálfbærnieiningu skal fylgja næstu skrefum:  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **sjálfbærniuppsetningu** og velja síðan viðeigandi tengil.  
2. Á flýtiflipanum **Almennt** skal grunnstilla nauðsynlega reiti sem tengjast þessari kerfiseiningu:   

|  Svæði  |  Heimildasamstæða  |  
|--------|--------------| 
| **Kóti mælieiningar útblásturs** | Tilgreinir kóða mælieiningar sem notaður er til að skrá losun. |
| **Aukastafir í útblæstri** | Tilgreinir fjölda aukastafa sem sýndir eru fyrir útblástursupphæðir. Sjálfgefna stillingin 2:5 tilgreinir að allar upphæðir séu sýndar með minnst 2 aukastöfum og mest 5 aukastöfum. Einnig er hægt að færa inn fasta tölu, t.d. 2, sem þýðir einnig að upphæðir eru sýndar með tveimur aukastöfum. |
| **Land/svæði áskilið** | Tilgreinir hvort land / svæði sé áskilið. Hægt er að nota þennan reit í færslubókum án þess að stilla þetta en hægt er að velja hann ef framfylgja á notendum til að fylla út reitinn fyrir bókun. |
| **Ábyrgðarstöð áskilin** | Tilgreinir hvort ábyrgðarstöð sé áskilin þar sem hægt er að nota ábyrgðarstöðina sem aðstöðu til að mæla facilty-undirstaða losun. Hægt er að nota þennan reit í færslubókum án þess að stilla þetta en hægt er að velja hann ef framfylgja á notendum til að fylla út reitinn fyrir bókun. |
| **Loka breytingu á útreikningi ef færslur eru til** | Tilgreinir hvort breytingu á útreikningsgrunni í reikningsflokki er lokað á tíma sjálfbærnifærslu, sem þýðir að þessi reikniregla hefur þegar verið jöfnuð. |
| **Gera villuprófun bakgrunns virka** | Tilgreinir hvort bakgrunnsvilluathugun á línum sjálfbærnibókar sé virk. |

3.  Á flýtiflipanum **Útreikningar** eru skilgreindir nauðsynlegir reitir sem tengjast reiknireglum sem notaðar eru við útreikninga á útblæstri:  

|  Svæði  |  Heimildasamstæða  |  
|--------|--------------| 
| **Eldsneyti/rafmagn aukastafir** | Tilgreinir fjölda aukastafa sem sýndir eru fyrir upphæðir eldsneytis/rafmagns. Sjálfgefna stillingin 2:5 tilgreinir að allar upphæðir séu sýndar með minnst 2 aukastöfum og mest 5 aukastöfum. Einnig er hægt að færa inn fasta tölu, t.d. 2, sem þýðir einnig að upphæðir eru sýndar með tveimur aukastöfum. |
| **Fjarlægð tugastafir** | Tilgreinir þann fjölda aukastafa sem sýndir eru fyrir mælingar á fjarlægð. Sjálfgefna stillingin 2:5 tilgreinir að allar upphæðir séu sýndar með minnst 2 aukastöfum og mest 5 aukastöfum. Einnig er hægt að færa inn fasta tölu, t.d. 2, sem þýðir einnig að upphæðir eru sýndar með tveimur aukastöfum. |
| **Sérsniðnir aukastafir í upphæð** | Tilgreinir fjölda aukastafa sem sýndir eru fyrir sérsniðnar upphæðir. Sjálfgefna stillingin 2:5 tilgreinir að allar upphæðir séu sýndar með minnst 2 aukastöfum og mest 5 aukastöfum. Einnig er hægt að færa inn fasta tölu, t.d. 2, sem þýðir einnig að upphæðir eru sýndar með tveimur aukastöfum. |

4.  Ljúka skal uppsetningunni á flýtiflipanum **Skýrslur** sem tengjast skýrslugerð fyrir yfirvöld:   

|  Svæði  |  Heimildasamstæða  |  
|--------|--------------| 
| **Mælieiningarkóti útblástursskýrslu** | Tilgreinir mælieiningarkótann sem er notaður til að gefa skýrslu um losun, þar sem hægt er að nota mismunandi mælieiningu við skýrslugerð til yfirvalda. Þessi reitur á ekki við staðlaðar skýrslur. |
| **Skýrslugerðarstuðull** | Tilgreinir mælieiningarstuðulinn sem er notaður til að skrá losun ef mismunandi mælieining er notuð við skýrslugerð til yfirvalda. |
| **Útblástur sléttunarnákvæmni** | Tilgreinir stærð bilsins sem á að nota við sléttun losunarupphæða við skýrslugerð til yfirvalda. |
| **Tegund útblásturssléttunar** | Tilgreinir hvernig kerfið sléttar losunarupphæð við skýrslugerð til yfirvalda, með því að nota valkosti: Næst, Upp eða Niður. |

>[!NOTE]
> Í útgáfu 24.0 [!INCLUDE[prod_short](includes/prod_short.md)]  styður engin yfirvöld skýrslugerð. Reitur sem tengist grunnstillingu á flýtiflipanum **Skýrslur** verður notaður fyrir síðari skýrslugerðarmöguleika en einnig er hægt að nota hann af samstarfsaðilum í staðfærðum útgáfum.

## <a name="see-also"></a>Sjá einnig .
[Fjármál](finance.md)    
[Yfirlit yfir](finance-manage-sustainability.md)
[sjálfbærnistjórnun bókhaldslykill sjálfbærni og fjárhagur](finance-sustainability-accounts-ledger.md)
[Hvernig á að skrá losun](finance-sustainability-journal.md)
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
