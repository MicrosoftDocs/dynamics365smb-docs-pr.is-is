---
title: Úrræðaleit vegna Shopify aðalsamstillingar og viðskipta
description: Lærðu hvað á að gera ef eitthvað fór úrskeiðis við samstillingu gagna á milli Shopify og Viðskiptamiðst
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 4ccbe8ac97eba568ff82d965f24b86ab58c95f81
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317246"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Úrræðaleit vegna Shopify Aðalsamstillingar og viðskipta

Mögulegt er að keyra inn í aðstæður þar sem leysa þarf vandamál þegar samstillt er við gögn á milli Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi síða skilgreinir skref til að leysa úr nokkrum algengum aðstæðum sem kunna að koma upp.

## <a name="logs"></a>Skrár

Ef samstillingarverk mistekst er hægt að virkja innskráningu með því að **Virkja skráningu virkja** skipta á **Shopify verkstæðisspjaldinu**. Kveikja handvirkt á samstillingarverkinu og yfirfara kladda.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, slá inn **Shopify kladdafærslur** og velja síðan tengda tengilinn.
2. Veljið tengda kladdafærslu og Opnið **Shopify gluggann kladdafærsla**.
3. Farið yfir beiðnina, stöðukóðann og lýsinguna og svarið.

Munið að skipta síðar um skráningu til að forðast neikvæð áhrif á afköst og aukningu í gagnagrunnsstærð.

**Shopify Í glugganum kladdafærslur** er hægt að kalla fram eyðingu allra kladdafærslna eða þeirra sem eru eldri en sjö daga.

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

## <a name="request-the-access-token"></a>Beiðni um aðgangsstákn

Ef [!INCLUDE[prod_short](../includes/prod_short.md)] ekki er hægt að tengjast Shopify reikningnum skaltu reyna að biðja um aðgangstófan Shopify. Þessa beiðni gæti verið þörf ef til staðar eru snúningar Öryggislyklar eða breytingar á nauðsynlegum heimildum (umfang).

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verslunina sem sækja á aðgangstakið til að opna **Shopify Vinnukortasíðuna**.
3. **Veldu aðgangsaðgerðina** beiðni.
4. Ef beðið er skal skrá sig inn Shopify á reikninginn.

**Víxl með AccessKey** -víxli verða virkjuð.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Sannprófa og leyfa heimildir til að gera HTTP-beiðnir þegar keyrðar eru í umhverfi sem ekki er í framleiðslu

Til þess að vinna rétt Shopify þarf tengivirkið leyfi til að gera HTTP beiðnir. Við prófanir í Sandkössum eru HTTP beiðnir um að allir Viðaukar séu bannaðir.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Framlengingarstjórnun** og velja síðan tengda tengilinn.
2. *Shopify Veljið Connector* Extension.
3. Velja skal **samskipanaraðgerð** til að opna **síðuna framlengingarstilling**.
4. Ganga þarf úr skugga um að **Leyfa Beiðnabeiðingar** HTTPClient séu virkar.

## <a name="rotate-the-shopify-access-key"></a>Shopify Snúa aðgangslyklinum

Eftirfarandi ferli lýsa hvernig á að snúa aðgangstáknum Shopify sem Connector notar Shopify til að fá aðgang að vefversluninni.

### <a name="in-shopify"></a>Í Shopify

1. **Shopify Frá admin**, Farðu í [apps](https://www.shopify.com/admin/apps).
2. Í röðinni með **Dynamics 365 Business Central** App skal velja **DELETE**.
3. Í skilaboðunum sem birtist velurðu **Eyða**.

### <a name="in-prod_short"></a>Í [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify verslanir** og veljið síðan tengda tengilinn.
2. Veljið verkstæðið sem á að snúa aðgangstakið við til að opna **Shopify Vinnukortasíðuna**.
3. **Veldu aðgangsaðgerðina** beiðni.
4. Ef beðið er, Skráðu þig inn í reikninginn þinn Shopify, farðu yfir persónuvernd og heimildir og veldu **síðan hnappinn setja upp App**.

## <a name="known-issues"></a>Þekkt atriði

### <a name="gen-bus-posting-group-must-have-a-value-in-customer-it-cannot-be-zero-or-empty"></a>Almenn Strætisvagn. bókunarflokkur verður að hafa gildi í viðsk. Það má ekki vera núll eða autt.

Reiturinn **Kóti viðskiptamannssniðmáts er fylltur út í glugganum Spjald-gluggi með sniðmátinu sem hefur** gen. viðsk. bókunarflokks **Shopify .** **·** Viðskiptamannssniðmátið er ekki eingöngu notað fyrir stofnun viðskiptamanna heldur einnig útreikning söluverðs og við stofnun söluskjala.

### <a name="importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Innflutningur á gögnum til Shopify verkstæðis er ekki virkjaður. Fara í verkstæðisspjaldið til að gera það virkt.

**Shopify Í glugganum verkstæðisspjald** er kveikt á reitnum **Leyfa samkeyrslu til að Shopify** skipta.  Þessari víxlun er ætlað að vernda vefverslunina með því að sækja kynningu á gögnum [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)  
