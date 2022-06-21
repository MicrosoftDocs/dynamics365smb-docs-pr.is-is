---
title: Úrræðaleit vegna Shopify aðalsamstillingar og viðskipta
description: Lærðu hvað á að gera ef eitthvað er athugavert við samstillingu gagna á milli Shopify og Viðskiptamiðst.
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ff2e4aca52f479e461dab0d9d0f0ce4958d19353
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808865"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Úrræðaleit vegna Shopify Aðalsamstillingar og viðskipta

Það er hægt að keyra inn í aðstæður þar sem leysa þarf vandamál. Þessi síða skilgreinir skref til að leysa úr nokkrum algengum aðstæðum sem kunna að koma upp.

## <a name="logs"></a>Skrár

Ef samstillingarverk mistekst er hægt að virkja innskráningu með því **að** gera kladda virka **Shopify óvirka í verkstæðisspjaldinu**. Ræsa samstillingarverk handvirkt og yfirfara kladda.

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Shopify kladdafærslur** og velja tengdan tengil.
2. Veljið tengda kladdafærslu og Opnið **Shopify gluggann kladdafærsla**.
3. Endurskoðunarbeiðni, Stöðukóði og Lýsing og svar.

Munið að skipta út innskráningu til að forðast neikvæð áhrif á afköst og auka í gagnagrunnsstærð.

**Shopify Í glugganum kladdafærslur** er hægt að kalla fram eyðingu á öllum kladdafærslum eða þeim sem eru eldri en sjö daga.

## <a name="data-capture"></a>Gagnatöku

Án tillits til **stillinga kladda** hafa svör frá Shopify alltaf skráð sig sem hægt er að skoða eða sækja um með því **að nota gluggann gagnatökulisti**.

**Veldu sótt Shopify gagnaaðgerð** á einni af eftirtöldum síðum:

- **Shopify þess**
- **Shopify panta uppfyltun**
- **Shopify panta sendingarkostnað**
- **Shopify pantanafærslur**
- **Shopify gjaldskrá**
- **Shopify greiðslufærslur**
- **Shopify færslur**

## <a name="reset-sync"></a>Endurstilla samstillingu

Fyrir bestan árangur flytur Connector aðeins viðskiptavini, afurðir og pantanir sem eru stofnaðar eða breyttar frá síðustu samstillingu. **Shopify Á verkstæðisspjaldinu** eru aðgerðir tiltækar til að breyta dagsetningu/tíma síðustu samstillingar eða algjörlega endurstilla þær. Þessi aðgerð tryggir að þegar samstilling er keyrð eru öll gögn samstillt og ekki bara breytingarnar frá síðustu samstillingu.

Þessi aðgerð á aðeins að samtengjast frá Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)] og getur verið gagnlegt ef endurheimta þarf Eydd gögn, svo sem afurðir, viðskiptamenn eða eyddar pantanir.

## <a name="update-the-access-token"></a>Uppfæra aðgangsstákn

Ef [!INCLUDE[prod_short](../includes/prod_short.md)] ekki er hægt að Shopify tengjast reikningnum skaltu reyna aftur að endurstilla aðgangstófan.

1. Fara á leitarljósaperu ![sem opnast Segðu mér lögun.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Veljið verslunina sem sækja á aðgangstakið til að opna **Shopify Vinnukortasíðuna**.
3. **Veldu aðgangsaðgerðina** beiðni.
4. Ef beðið er skal skrá sig inn Shopify á reikninginn.

## <a name="see-also"></a>Sjá einnig

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
