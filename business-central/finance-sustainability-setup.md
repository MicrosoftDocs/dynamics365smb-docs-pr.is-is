---
title: Sjálfbærniuppsetning
description: Læra hvernig setja á upp sjálfbærniaðgerðir.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-setup"></a>Sjálfbærniuppsetning

Áður en einingin Sjálfbærni getur unnið rétt þarf að setja upp nokkur grunneftirlit og leiðbeiningar sem tengjast allri virkninni.

Til að setja upp eininguna Sjálfbærni skal fylgja skrefunum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Sjálfbærniuppsetning** og velja síðan viðeigandi tengil.
2. Á flýtiflipanum **Almennt** eru skilgreindir nauðsynlegir reitir sem tengjast einingunni Sjálfbærni.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | **Kóti mælieiningar útblásturs** | Tilgreina mælieiningarkótann sem er notaður til að skrá losun. |
    | **Aukastafir í útblæstri** | Tilgreina fjölda aukastafa sem sýndir eru fyrir útblástursupphæðir. Sjálfgefna stillingin *2:5* merkir að minnst tveir tugastafir og mest fimm tugastafir eru sýndir fyrir allar upphæðir. Einnig er hægt að færa inn fast númer. Ef til dæmis er fært inn *2* birtast tveir aukastafir fyrir allar upphæðir. |
    | **Land/svæði áskilið** | Tilgreina þarf hvort land/svæði er áskilið. Notendur geta stillt lands-/svæðisreitinn í færslubókum jafnvel þótt þessi reitur sé ekki valinn. Hins vegar þarf notendur að stilla lands-/svæðisreitinn áður en bókað er. |
    | **Ábyrgðarstöð áskilin** | Tilgreina þarf hvort ábyrgðarstöðin sé áskilin. Ábyrgðarstöðina er hægt að nota sem aðstöðu til að mæla losun sem byggir á aðstöðu. Notendur geta stillt ábyrgðarstöðina í færslubókum jafnvel þótt ekki sé valinn þessi reitur. En með því að velja hana er þess krafist að notendur stilli reitinn ábyrgðarstöð áður en bókað er. |
    | **Loka breytingu á útreikningi ef færslur eru til** | Tilgreint er hvort breytingar á útreikningsstofni (reiknireglu) á stigi reikningstegundar eru lokaðar þegar sjálfbærnifærslan hefur þegar verið jöfnuð. |
    | **Gera villuprófun bakgrunns virka** | Tilgreina hvort bakgrunnsvilluprófun á sjálfbærnibókarlínum er virk. |

    > [!NOTE]
    > Þegar bakgrunnsvilluprófun hefur verið gerð virk eða gerð virk í færslubókum þarf að skrá sig aftur inn áður en nýja uppsetningin er sett í gang.

3. Á flýtiflipanum **Útreikningar** eru nauðsynlegir reitir sem eru tengdir reiknireglunum sem notaðar eru til að reikna út útblástur.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | **Eldsneyti/rafmagn aukastafir** | Tilgreina fjölda aukastafa sem sýndir eru fyrir upphæðir eldsneytis/rafmagns. Sjálfgefna stillingin *2:5* merkir að minnst tveir tugastafir og mest fimm tugastafir eru sýndir fyrir allar upphæðir. Einnig er hægt að færa inn fast númer. Ef til dæmis er fært inn *2* birtast tveir aukastafir fyrir allar upphæðir. |
    | **Fjarlægð tugastafir** | Tilgreindur er fjöldi aukastafa sem sýndir eru fyrir mælingar á fjarlægð. Sjálfgefna stillingin *2:5* merkir að minnst tveir tugastafir og mest fimm tugastafir eru sýndir fyrir allar upphæðir. Einnig er hægt að færa inn fast númer. Ef til dæmis er fært inn *2* birtast tveir aukastafir fyrir allar upphæðir. |
    | **Sérsniðnir aukastafir í upphæð** | Tilgreina fjölda aukastafa sem sýndir eru fyrir sérsniðnar upphæðir. Sjálfgefna stillingin *2:5* merkir að minnst tveir tugastafir og mest fimm tugastafir eru sýndir fyrir allar upphæðir. Einnig er hægt að færa inn fast númer. Ef til dæmis er fært inn *2* birtast tveir aukastafir fyrir allar upphæðir. |

4. Á flýtiflipanum **Skýrslur** skal ljúka uppsetningunni með því að grunnstilla reitina sem tengjast skýrslugerð til yfirvalda.

    > [!NOTE]
    > Í útgáfu 24.0 [!INCLUDE[prod_short](includes/prod_short.md)]  styður engin yfirvöld skýrslugerð. Þess vegna eru reitir sem eru tengdir grunnstillingu þessarar aðgerðar á flýtiflipanum **Skýrslur** fyrir síðari skýrslugerðarmöguleika. Félagar geta þó einnig notað þessa reiti í staðfærðum útgáfum.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | **Mælieiningarkóti útblástursskýrslu** | Tilgreina skal mælieiningarkótann sem er notaður til að gefa skýrslu um losun þar sem hægt er að nota aðra mælieiningu þegar yfirvöld gefa skýrslu um það. Þessi reitur á ekki við staðlaðar skýrslur. |
    | **Skýrslugerðarstuðull** | Tilgreina skal mælieiningarstuðulinn sem er notaður til að skrá losun ef notuð er önnur mælieining þegar yfirvöld eru send til yfirvalda. |
    | **Útblástur sléttunarnákvæmni** | Tilgreina stærð bilsins sem er notað við sléttun útblástursupphæða þegar skýrslur eru gerðar til yfirvalda. |
    | **Tegund útblásturssléttunar** | Tilgreina hvernig kerfið sléttar losunarupphæðir þegar skýrslur eru gerðar til yfirvalda. Eftirfarandi valkostir eru í boði: **Næst**, **Upp** og **Niður**. |

## <a name="see-also"></a>Sjá einnig .

[Fjármál](finance.md)  
[Sjálfbærnistjórnunaryfirlit](finance-manage-sustainability.md)  
[Bókhaldslykill fyrir sjálfbærni og fjárhag](finance-sustainability-accounts-ledger.md)  
[Skrá sjálfbærnifærslur](finance-sustainability-journal.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
