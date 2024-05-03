---
title: Algengar spurningar um tæknilegar upplýsingar
description: Upp+ um innleiðingu sem tengist Shopify tenglinum.
ms.date: 01/24/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="faq-for-technical-details"></a>Algengar spurningar um tæknilegar upplýsingar

Í þessari grein er svarað algengum spurningum um Shopify tengilinn.

## <a name="what-is-shopify"></a>Hvað er Shopify?

Shopify er áskriftarforrit sem gerir öllum kleift að setja upp netverslun og selja vörur. Verkvangurinn Shopify býður smásala á netinu upp á þjónustu fyrir greiðslur, markaðssetningu, afhendingu og þátttöku viðskiptavina.

## <a name="what-is-the-microsoft-dynamics-365-business-central-shopify-connector"></a>Hvað er Microsoft Dynamics 365 Business Central Shopify tengillinn?

Með tengilinn Shopify geta fyrirtæki tengt verslanir sínar Shopify við [!INCLUDE[prod_short](../includes/prod_short.md)] til að hámarka framleiðni fyrirtækisins. Með því Shopify að nota tengið geta þeir nálgast og stjórnað innsýn frá fyrirtæki sínu og netverslun þeirra Shopify sem ein eining.

### <a name="capabilities"></a>Getu

- Stuðningur við fleiri en eina Shopify búð
  - Hver verkstæði hefur sína uppsetningu, þar á meðal safn af vörum og birgðageymslum sem notuð eru til að reikna út birgða- og verðlista.  
- Tvístefnusamstilling vara eða vara
  - Tengið samstillir myndir, vöruafbrigði, strikamerki, vörunúmer lánardrottins, lengdan og markaðssetningartexta og merki.  
  - Flyttu út vörueigindir í Shopify.  
  - Notaðu valda verðflokka og afslætti viðskiptamanna til að skilgreina verð sem flutt eru út í Shopify.
  - Skilgreina verð og afslátt fyrir vörulista sem tengjast B2B-fyrirtækjum.
  - Taktu ákvörðun um hvort hægt sé að stofna vörur sjálfkrafa eða aðeins leyfa uppfærslur á fyrirliggjandi afurðum.
- Samstilling birgðastiga
  - Veldu sumar eða allar tiltækar staðsetningar í [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Uppfærðu birgðastöður á mörgum staðsetningum í Shopify.  
- Tvístefnusamstilling viðskiptavina og fyrirtækja
  - Snjallvarpaðu viðskiptamönnum eftir síma og netfangi.  
  - Nota tiltekin sniðmát lands/svæðis þegar viðskiptamenn eru stofnaðir sem hjálpa til við að tryggja að skattstillingar séu réttar.  
- Flytja inn pantanir frá Shopify
  - Taka með pantanir sem búnar eru til í ýmsum sölurásum, svo sem netverslun, **Shopify  POS** eða **B2B**.
  - Sendingarkostnaður, gjafakort, ábendingar, sendingar- og greiðslumátar, færslur og hætta á svikum.  
  - Við innflutning er hægt að stofna viðskiptamenn sjálfvirkt í [!INCLUDE [prod_short](../includes/prod_short.md)] eða ákveða að stjórna viðskiptamönnum. Shopify  
  - Fáðu greiðsluupplýsingar frá Shopify Payments.
- Rekja upplýsingar um uppfyllingu
  - Það má velja að flytja upplýsingar vörurakningar úr [!INCLUDE [prod_short](../includes/prod_short.md)] í Shopify.
- Höfuðlaus samþætting
  - Virkja sjálfvirka samstillingu afurða, birgða, pantana, uppfyllinga og fleira.

## <a name="why-did-microsoft-and-shopify-form-this-partnership"></a>Af hverju mynduðu Microsoft og Shopify þetta samstarf?

[!INCLUDE[prod_short](../includes/prod_long.md)] er að fara í samstarf við Shopify til að viðskiptamönnum okkar að skapa betri upplifun af verslun. Þó Shopify veitir kaupendur einfaldan viðskiptalausn [!INCLUDE[prod_short](../includes/prod_short.md)]  og býður upp á alhliða viðskiptastjórnun í fjármálum, sölu, þjónustu og rekstrarteymum. Nota óaðfinnanlegu tengingu milli forritanna til að samstilla pantanir, lager- og viðskiptamannaupplýsingar til að uppfylla pantanir hraðar og þjóna viðskiptavinum betur.

## <a name="which-microsoft-products-work-with-the-shopify-connector"></a>Fyrir hvaða vörur Microsoft er Shopify tengillinn tiltækur?

Þessi eiginleiki er aðeins í boði fyrir [!INCLUDE[prod_short](../includes/prod_short.md)] á netinu, frá og með útgáfu 20.1. Hann er ekki í boði fyrir uppsetningar á staðnum. Tengið er foruppsett fyrir nýtt umhverfi. Stofnanir með núverandi umhverfi geta sótt og sett tengið upp frá AppSource. Fyrirtækið verður að hafa bæði [!INCLUDE [prod_short](../includes/prod_short.md)] leyfi og Shopify leyfi til að nota tengið. Nánari upplýsingar um lönd/svæði, tungumál og útgáfur af [!INCLUDE[prod_short](../includes/prod_short.md)] fást með því að [Shopify fara í Connector í glugganum AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Tengið Shopify virkar ekki fyrir [Embed App](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), þar sem veffang biðlarans er með sniðinu `https://[application name].bc.dynamics.com` .

Tengið Shopify vinnur ekki með aðrar vörur í Dynamics 365 eigu.

## <a name="what-support-is-offered-for-the-shopify-connector"></a>Hvaða stuðningur er í boði fyrir Shopify tengilinn?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Shopify tengillinn er dekkaður af núverandi stuðningslíkani. Frekari upplýsingar eru í [Tækniaðstoð](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (aðeins á ensku).

Fáðu hjálp frá ráðgjafa sem þekkir tengið Shopify fyrir [!INCLUDE[prod_short](../includes/prod_short.md)], til að uppfylla einstakar kröfur um viðskiptatengdar kröfur. Leita í [Ráðgjafaþjónustu](https://aka.ms/BCShopifyConsultant).

### <a name="shopify"></a>Shopify

Fáðu hjálp frá Shopify almennu [Shopify hjálparmiðstöðinni](https://help.shopify.com/) eða frá [24/7 stuðningi við verslunina sem Shopify söluaðila](https://help.shopify.com/questions#/).

Þú getur einnig skoðað [markaðssetningu](https://experts.shopify.com/) sérfræðinga til að finna rétta sérfræðinga sem bjóða upp á þjónustu fyrir Shopify kaupendur.

## <a name="currently-unsupported-features-however-were-tracking-them-and-may-consider-adding-them"></a>Aðgerðir sem ekki eru studdar eins og er; hins vegar erum við að rekja þær og gætum íhugað að bæta þeim við

- Markaðir
  - Margar þýðingar á aðalgögnum. Hægt er að velja eitt tungumál sem notað verður við útflutning vöruupplýsinga.
  - Verð eftir landi/svæði. Einn verðlisti er tiltækur fyrir valinn gjaldmiðil. Shopify sér um umbreytingu í aðra gjaldmiðla.
- Uppkast að pöntunum

## <a name="is-the-shopify-connector-extensible"></a>Er Shopify tengillinn stækkanlegur?

Já, Shopify tengið er útbreiðanlegt. Athugaðu GitHub til að fá aðgang [að lista yfir möguleika á punktum](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) og skoða nokkur [dæmi](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify).

## <a name="is-the-shopify-connector-open-for-contribution"></a>Er tengið Shopify opið fyrir framlag?

Já, þessi viðbót er opin fyrir framlög frá samfélaginu okkar. Þú getur fundið [frumkóðann](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) í gagnageymslu viðbóta í Microsoft AL-forritinu.

## <a name="building-your-version-of-the-shopify-connector"></a>Byggja útgáfuna af Shopify Connector

Ef Shopify þú vilt byggja og birta tengiforrit á Shopify markaðnum sem hefur þann megintilgang að flytja eða deila gögnum söluaðila til þriðja aðila ([!INCLUDE [prod_short](../includes/prod_short.md)]) verður þú að hafa skriflegt samþykki frá Shopify. Sem hluta af þessu ferli verður þú að fá samþykki frá Microsoft í "Data Acknowledgement End Acknowledgement". Við þurfum að biðja þig að sjá um málið Shopify vegna þess að Microsoft getur ekki skrifað undir samninga við þriðja aðila.

### <a name="what-to-do"></a>Hvað á að gera

Athugaðu skilyrðin Shopify þar sem þú gætir samt verið fær um að hafa óskráð forrit.

 Shopify Einnig fær Tengið [!INCLUDE [prod_short](../includes/prod_short.md)] stöðugt nýjar aðgerðir og nýja viðskiptamenn. Ef tiltekið bil uppgötvast skal íhuga að senda vörutillögu (https://aka.ms/bcideas) eða kóðaframlag til [!INCLUDE [prod_short](../includes/prod_short.md)]. Ef gera á kröfur sem gætu ekki átt við meirihluta viðskiptamanna og ekki er auðvelt að takast á við gildandi umfangsmódel skal hafa samband við [!INCLUDE [prod_short](../includes/prod_short.md)] þróunarteymið til að ræða notkunarmálin. Við ættum að geta fundið feita lausn.

## <a name="see-also"></a>Sjá einnig

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
