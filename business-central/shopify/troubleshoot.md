---
title: Úrræðaleit vegna Shopify Aðalsamstillingar og viðskipta
description: Læra hvað á að gera ef eitthvað fer úrskeiðis við samstillingu gagna á milli Shopify og viðskipta-seðlabankar
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30118, 30119, 30120,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 37fb8069f6149cc89c1c53f671eafe3788f54ccf
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728357"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Úrræðaleit vegna Shopify Aðalsamstillingar og viðskipta

Mögulegt er að keyra inn í aðstæður þar sem leysa þarf vandamál þegar samstillt er við gögn á milli Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi síða skilgreinir villuleitarskref fyrir nokkrar algengar aðstæður sem kunna að koma upp.

## <a name="logs"></a>Skrár

Ef samstillingarverk mistekst er hægt að virkja innskráningu með því að **Virkja skráningu virkja** skipta á **Shopify vinnukortasíðunni**. Þá er hægt að kveikja handvirkt á samstillingarverkinu og yfirfara kladda.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Shopify kladdafærslur** og velja tengdan tengil.
2. Veljið tengda kladdafærslu og Opnið **Shopify síðuna kladdafærsla**.
3. Farið yfir beiðnina, stöðukóðann og lýsinguna og svargildin.

Síðar þarf að muna að skipta um innskráningu til að forðast neikvæð áhrif afkasta og aukningu í gagnagrunnsstærð.

**Shopify Á síðunni kladdafærslur** er hægt að kalla fram eyðingu á öllum kladdafærslum eða þeim sem eru eldri en sjö daga.

## <a name="data-capture"></a>Gagnatöku

Án tillits til **stillinga kladda sem virkjaður** eru fá sum Shopify svör alltaf skráð svo hægt sé að skoða þau eða sækja þau með **listasíðu** gagnatökunar.

**Veldu sótt Shopify gagnaaðgerð** á einni af eftirtöldum síðum:

- **Shopify þess**
- **Shopify panta uppfyltun**
- **Shopify panta sendingarkostnað**
- **Shopify pantanafærslur**
- **Shopify gjaldskrá**
- **Shopify greiðslufærslur**
- **Shopify færslur**

## <a name="reset-sync"></a>Endurstilla samstillingu

Fyrir bestan árangur flytur Connector aðeins viðskiptavini, afurðir og pantanir sem eru stofnaðar eða breyttar frá síðustu samstillingu. **Shopify Á Vinnukortssíðunni** eru aðgerðir sem breyta dagsetningu/tíma síðustu samstillingu eða algjörlega endurstilla hana. Þessi aðgerð tryggir að þegar samstilling er keyrð eru öll gögn samstillt frekar en breytingarnar síðan síðast var samstillt.

Þessi aðgerð á aðeins að samtengjast frá Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)]. Það getur komið sér vel ef endurheimta þarf Eydd gögn, svo sem afurðir, viðskiptamenn eða eyddar pantanir.

## <a name="request-the-access-token"></a>Beiðni um aðgangsstákn

Ef [!INCLUDE[prod_short](../includes/prod_short.md)] mun ekki tengjast Shopify reikningnum skaltu reyna að biðja um aðgangstófan Shopify. Þessa beiðni gæti verið þörf ef til staðar eru snúningar Öryggislyklar eða breytingar á nauðsynlegum heimildum (umfang).

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu tengdan tengil.
2. Veljið verslunina sem sækja á aðgangstakið til að opna **Shopify Vinnukortasíðuna**.
3. **Veldu aðgangsaðgerðina** beiðni.
4. Ef beðið er skal skrá sig inn Shopify á reikninginn.

**Víxl með AccessKey** -víxli verða virkjuð.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Sannprófa og leyfa heimildir til að gera HTTP-beiðnir þegar keyrðar eru í umhverfi sem ekki er í framleiðslu

Til að vinna rétt Shopify þarf tengivirkið leyfi til að gera HTTP beiðnir. Við prófun í sandkassa er http-beiðnirnar bannaðar öllum viðaukum.

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **framlengingarstjórnun** og veljið tengdan tengil.
2. **Shopify Veljið Connector** Extension.
3. Velja skal **samskipanaraðgerð** til að opna **síðuna framlengingarstilling**.
4. Ganga þarf úr skugga um að **Leyfa Beiðnabeiðingar** HTTPClient séu virkar.

## <a name="rotate-the-shopify-access-token"></a>Shopify Snúa aðgangsákefð

Eftirfarandi ferli lýsa því hvernig aðgangstákn sem notað er Shopify sem Connector eru notuð til að komast Shopify í vefverslunina.

### <a name="in-shopify"></a>Í Shopify

1. **Shopify Frá admin**, Farðu í [apps](https://www.shopify.com/admin/apps).
2. Veldu **Eyða** í röðinni með **Dynamics 365 Business Central** App.
3. Veljið **Eyða** í skilaboðunum sem birtast.

### <a name="in-prod_short"></a>Í [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikni, Sláðu inn **Shopify verslanir** og veldu tengdan tengil.
2. Veljið verkstæðið sem á að snúa aðgangstakið við til að opna **Shopify Vinnukortasíðuna**.
3. **Veldu aðgangsaðgerðina** beiðni.
4. Ef beðið er, Skráðu þig inn á reikninginn þinn Shopify, farðu yfir persónuvernd og heimildir og veldu **síðan hnappinn setja upp App**.

## <a name="known-issues"></a>Þekkt atriði

### <a name="the-gen-bus-posting-group-cannot-be-zero-or-empty-there-must-be-a-value-in-the-customer-field"></a>*Alm. viðsk. bókunarflokkurinn* má ekki vera núll eða tómur; gildi verður í viðskiptamannasvæðinu

**Shopify Á vinnukortasíðunni** er reiturinn sniðmát **viðskiptamanns fylltur út** með sniðmátinu sem hefur **Alm. útfylling bókunarflokks**. Viðskiptamannssniðmátið er eingöngu notað fyrir stofnun viðskiptamanna heldur einnig fyrir útreikning söluverðs og við stofnun söluskjala.

### <a name="importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Innflutningur á gögnum til Shopify verkstæðis er ekki virkjaður. Fara í verkstæðisspjaldið til að virkja það

**Shopify Í glugganum verkstæðisspjald** er kveikt á reitnum **Leyfa samkeyrslu til að Shopify** skipta. Þessari víxlun er ætlað að vernda vefverslunina með því að sækja kynningu á gögnum [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Oauth Villa invalid_request: Ekki tókst að finna Shopify API-forrit með api_key

Það virðist vera notað [App](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), þar sem BIÐLARASLÓÐIN hefur sniðið:`https://[application name].bc.dynamics.com`. Shopify Connector virkar ekki fyrir Emblu apps. Frekari upplýsingar er að finna [í því hvað Microsoft-vörur eru tengivirkið sem Shopify er tiltækt](shopify-faq.md#what-microsoft-products-is-the-shopify-connector-available-for).

## <a name="see-also"></a>Sjá einnig .

[Byrjaðu með Tengimynt fyrir Shopify](get-started.md)
