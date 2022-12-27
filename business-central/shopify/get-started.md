---
title: Hafist handa með tengli fyrir Shopify
description: Fyrstu skrefin við að grunnstilla tengingu milli Business Central og Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: b79691660ca84309057c3abab3d3a3df47271f58
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728411"
---
# <a name="get-started-with-the-shopify-connector"></a>Hafist handa með Shopify tengli

Tengdu Shopify verslunina þína (eða verslanir) við [!INCLUDE [prod_short](../includes/prod_short.md)] og hámarkaðu afköst viðskiptanna. Stjórnaðu og skoðaðu innsýn í viðskiptin og Shopify verslunina þína í einni einingu.

Shopify tengillinn felur í sér eftirfarandi möguleika:

- Stuðningur við fleiri en eina Shopify verslun.
  - Hver verslun er með sína eigin uppsetningu, þar á meðal safn af vörum, staðsetningar sem notaðar eru til að reikna birgðir og verðlista.  
- Tvíátta samstilling á vörum og afurðum.
  - Tengillinn mun samstilla myndir, vöruafbrigði, strikamerki, vörunúmer lánardrottna, lengri texta og merki.  
  - Flyttu út vörueigindir í Shopify.  
  - Notaðu valda verðflokka og afslætti viðskiptamanna til að skilgreina verð sem flutt eru út í Shopify.  
  - Taktu ákvörðun um hvort hægt sé að stofna vörur sjálfkrafa eða aðeins leyfa uppfærslur á fyrirliggjandi afurðum.  
- Samstilling birgðastöðu.
  - Veldu sumar eða allar tiltækar staðsetningar í [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Uppfærðu birgðastöður á mörgum staðsetningum í Shopify.  
- Tvíátta samstilling viðskiptamanna.
  - Snjallvarpaðu viðskiptamönnum eftir síma og netfangi.  
  - Notaðu landsbundin sniðmát þegar viðskiptamenn eru stofnaðir, sem hjálpar til við að tryggja að stillingar skatta séu réttar.  
- Flytja inn pantanir frá Shopify.
  - Meðan á innflutningi stendur geturðu sjálfkrafa stofnað viðskiptamenn í [!INCLUDE [prod_short](../includes/prod_short.md)] eða ákveðið að stjórna viðskiptamönnum í Shopify.  
  - Taktu með pantanir sem stofnaðar eru í öðrum rásum eins og Shopify sölustað eða Amazon.  
  - Sendingarkostnaður, gjafakort, ábendingar, sendingar- og greiðslumátar, færslur og hætta á svikum.  
  - Fáðu greiðsluupplýsingar frá Shopify Payments.  
- Rektu upplýsingar um uppfyllingu.
  - Það má velja að flytja upplýsingar vörurakningar úr [!INCLUDE [prod_short](../includes/prod_short.md)] í Shopify.  

Til að nota Shopify með [!INCLUDE [prod_short](../includes/prod_short.md)] þarft fyrst að gera nokkra hluti. Þessi grein þjónar hlutverki leiðsagnar til að samþætta Shopify verslun við [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forkröfur fyrir Shopify

Þú verður að vera með:

- Shopify-Reikningur.
- Shopify netverslun.

Til að stofna nýjan Shopify reikning eða nýskrá þig fyrir 14 daga prufuáskrift skaltu fara á [Shopify.com](https://www.shopify.com/). Frekari upplýsingar um hvernig á að búa til og sérsníða netverslunina er að finna í [Shopify hjálparmiðstöð](https://help.shopify.com/).
  
Aðrar sölurásir eru studdar, til dæmis Shopify sölustaður.

### <a name="recommended-settings"></a>Ráðlagðar stillingar

- Slökktu á valkostinum **Safnvista pöntunina sjálfkrafa** í hlutanum **Úrvinnsla pöntunar** í stillingum fyrir [**Greiðsluferli**](https://www.shopify.com/admin/settings/checkout) í **Shopify stjórnanda**.

Frekari upplýsingar um Shopify stillingar fyrir sýniútgáfur og prufuaðstæður á [Prufu- og þjálfunaraðstæður](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Skilyrði fyrir Business Central

- Gakktu úr skugga um að forritið **[Shopify tengill](https://go.microsoft.com/fwlink/?linkid=2196238)** sé uppsett.

Forritið er foruppsett fyrir allar nýskráningar og prufuáskriftir. Frekari upplýsingar um uppsetningu forrit úr AppSource eru í [Uppsetning og fjarlæging viðbóta](../ui-extensions-install-uninstall.md#install). Fylgdu skrefunum sem talin eru upp hér að neðan ef þú ert ekki [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Settu Dynamics 365 Business Central forritið upp í Shopify netverslunina þína

Fyrir núverandi [!INCLUDE[prod_short](../includes/prod_short.md)] er þetta skref valfrjálst og hægt er að sleppa því.

1. Finndu [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) forritið í [Shopify AppStore](https://apps.shopify.com/)
2. Veldu hnappinn **Bæta við forriti**. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það. Veldu nauðsynlega netverslun ef þú ert með fleiri en eina.
3. Þegar búið er að fara yfir persónuvernd og heimildir skaltu velja hnappinn **Setja upp forrit**.

   Þú getur fundið og opnað uppsett **Dynamics 365 Business Central** forrit í hlutanum **Forrit** á hliðarstikunni á síðunni **Shopify stjórnandi**.
4. Veldu **Nýskrá núna** til að hefja [!INCLUDE[prod_short](../includes/prod_short.md)] prufuáskriftina eða **Skrá inn** ef þú ert þegar með [!INCLUDE[prod_short](../includes/prod_short.md)]. Þér verður beint á síðuna [Business Central](https://businesscentral.dynamics.com).
5. Næstu skref skal gera í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connect-business-central-to-the-shopify-online-store"></a>Tengja Business Central við Shopify netverslunina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.  
3. Í reitinn **Kóði** skal færa inn kóðann sem auðveldar þér að finna í [!INCLUDE[prod_short](../includes/prod_short.md)]. Til dæmis getur heiti endurspeglað það sem verslun selur, til dæmis „Húsgögn“ eða „Kaffi“, eða landið eða svæðið sem hún þjónustar.
4. Í reitinn **Shopify vefslóð** skal færa inn vefslóð netverslunar sem á að tengja. Notaðu eftirfarandi snið: `https://{shop}.myshopify.com/`.
5. Virkjaðu víxlhnappinn **Virkjað**, farðu yfir og samþykktu skilmálana.
6. Ef beðið er um það skaltu skrá þig inn á Shopify reikninginn þinn, fara yfir persónuverndarskilmálana og heimildirnar, síðan velja hnappinn **Setja upp forrit**.

Endurtaktu skref 2-6 fyrir allar netverslanir sem þú vilt tengjast.

> [!NOTE]
> Gakktu úr skugga um að vafrinn loki ekki á sprettiglugga. Þegar þú virkjar víxlhnappinn **Virkjað** opnar kerfið síðuna **Bíður eftir svari - ekki loka þessari síðu** sem bíður eftir aðgangslykli frá Shopify, ef þessi síða er lokuð eða lokað fyrir hana - þú getur ekki tengst við Shopify. Frekari upplýsingar er að finna í [Biðja um aðgangslykilinn](troubleshoot.md#request-the-access-token).

### <a name="next-steps"></a>Næstu skref

Nú er netverslunin þín tengd við [!INCLUDE[prod_short](../includes/prod_short.md)]. Í næstu skrefum skilgreinir þú hvernig og hvað á að samstilla.

- [Samstilla vörur](synchronize-items.md)
- [Samstilla viðskiptavini](synchronize-customers.md)
- [Samstilla pantanir](synchronize-orders.md)

## <a name="see-also"></a>Sjá einnig .

[Prófunar- og þjálfunaraðstæður](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).
