---
title: Úrræðaleit fyrir samstillingu Shopify og Business Central
description: Kynntu þér hvað á að gera ef eitthvað fer úrskeiðis í samstillingu gagna milli Shopify og Business Central
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30118, 30119, 30120, 30101, 30102'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Úrræðaleit fyrir samstillingu Shopify og Business Central

Hægt er að lenda í aðstæðum þar sem þú þarft að úrræðaleita vandamál þegar gögn eru samstillt milli Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi síða skilgreinir skref úrræðaleitar fyrir sumar algengar aðstæður sem gætu komið upp.

## Skrár

Ef samstillingarverkið mistekst er hægt að virkja skráningu með því að kveikja á víxlhnappnum **Virkja skrá** á síðunni **Shopify verslunarkort**. Þá geturðu handvirkt ræst samstillingarverkið og yfirfarið skrár.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Shopify Skráarfærslur** og veldu viðkomandi tengil.
2. Veldu tengda skráningarfærslu og opnaðu síðuna **Shopify skráningarfærsla**.
3. Farðu yfir beiðnina, stöðukóðann og lýsinguna og svargildin.

Síðar skaltu muna að slökkva á skráningu til að forðast neikvæð áhrif á afköst og aukna stærð gagnagrunns.

Á síðunni **Shopify skráarfærslur** geturðu ræst eyðingu á öllum skráarfærslum eða þeim sem eru eldri en sjö daga.

## Gagnataka

Burtséð frá stillingum fyrir **Skrá virkjuð**, eru sum Shopify viðbrögð alltaf skráð svo þú getir skoðað eða sótt þau með síðunni **Listi gagnatöku**.

Veldu aðgerðina **Sótti Shopify gögn** á einni af eftirfarandi síðum:

- **Shopify pöntun**
- **Shopify uppfylling pantana**
- **Sendingarkostnaður Shopify pöntunar**
- **Shopify pöntunarfærslur**
- **Shopify útgreiðslur**
- **Shopify greiðslufærslur**
- **Shopify færslur**

## Endurstilla samstillingu

Til að ná sem bestum árangri flytur tengillinn aðeins inn viðskiptamenn, vörur og pantanir sem búnar eru til eða breytt frá síðustu samstillingu. Á síðunni **Shopify verslunarkort** eru aðgerðir sem breyta dagsetningu/tíma síðustu samstillingar eða endurstilla hana alveg. Þessi aðgerð tryggir að þegar samstilling er keyrð eru öll gögn samstillt frekar en bara breytingarnar frá síðustu samstillingu.

Þessi aðgerð á aðeins við um samstillingar úr Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það getur verið gagnlegt ef þú þarft að endurheimta eydd gögn eins og vörur, viðskiptamenn eða eyddar pantanir.

## Biðja um aðgangslykilinn

Ef [!INCLUDE[prod_short](../includes/prod_short.md)] vill ekki tengjast Shopify reikningnum þínum skaltu prófa að biðja um aðgangslykilinn frá Shopify. Þessi beiðni gæti verið nauðsynleg ef öryggislyklar eru valdir handahófskennt eða breytingar hafa verið gerðar á nauðsynlegum heimildum (umfangi).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **Shopify verslanir** og veldu viðeigandi tengil.
2. Veldu verslunina sem þú vilt aðgangslykilinn fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það.

Víxlhnappurinn **Er með aðgangslykil** verður gerður virkur.

### Staðfesta og virkja heimildir til að leggja fram http-beiðnir þegar keyrt er í öðru umhverfi en framleiðsluumhverfi

Til að allt virki rétt þarf viðbót Shopify tengilsins heimild til að leggja fram http-beiðnir. Þegar prófað er í sandkassa eru http-beiðnir bannaðar fyrir allar viðbætur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **viðbótastjórnun** og veldu síðan viðkomandi tengil.
2. Veldu viðbótina **Shopify tengill**.
3. Veldu aðgerðina **Grunnstilla** til að opna síðuna **Stilling viðbótar**.
4. Gakktu úr skugga um víxlhnappurinn **Leyfa HttpClient-beiðnir** sé virkur.

## Snúðu Shopify aðgangslyklinum

Eftirfarandi ferlar lýsa því hvernig á að snúa aðgangslyklinum sem Shopify tengillinn notar til að komast inn í Shopify netverslunina þína.

### Eftir Shopify

1. Úr **Shopify stjórnandi** skaltu fara í [Forrit](https://www.shopify.com/admin/apps).
2. Veldu **Eyða** í línunni með **Dynamics 365 Business Central** forritinu.
3. Veldu **Eyða** í skilaboðunum sem birtast.

### Eftir [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **Shopify verslanir** og veldu viðeigandi tengil.
2. Veldu verslunina sem þú vilt snúa aðgangslyklinum fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Ef beðið er um það skaltu skrá þig inn á Shopify reikninginn þinn, fara yfir persónuvernd og heimildir og velja svo hnappinn **Setja upp forrit**.

## Þekkt vandamál

### *Almennur viðskiptabókunarflokkur* má ekki vera núll eða auður; það verður að vera gildi í reit viðskiptamannsins.

Á síðunni **Shopify verslunarkort** skal fylla út í reitinn **Sniðmátskóði viðskiptamanns** með sniðmátinu sem er með **Almennur viðskiptabókunarflokkur** útfyllt. Sniðmát viðskiptamanns er notað ekki bara til þess að stofna viðskiptamenn heldur einnig fyrir útreikning á söluverðinu og við stofnun söluskjala.

### Innflutningur gagna í Shopify verslunina þína er ekki virkur. Opnaðu verslunarkortið til að virkja hann

Í glugganum **Shopify verslunarkort** skaltu kveikja á víxlhnappnum **Leyfa gagnasamstillingu í Shopify**. Þessi víxlhnappur á að vernda netverslunina frá því að fá sýnigögn úr [!INCLUDE[prod_short](../includes/prod_short.md)].

### Oauth villa invalid_request: Ekki tókst að finna Shopify API forrit með api_key

Svo virðist sem þú notir [Innleiða forrit](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) þar sem vefslóð biðlara er á sniðinu:`https://[application name].bc.dynamics.com`. Tengillinn Shopify virkar ekki fyrir „Innleiða forrit“. Frekari upplýsingar er að finna í [Hvaða Microsoft-vörur er Shopify tengillinn tiltækur fyrir ](shopify-faq.md#what-microsoft-products-is-the-shopify-connector-available-for).

## Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)
