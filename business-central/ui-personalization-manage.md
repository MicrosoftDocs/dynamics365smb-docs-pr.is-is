---
title: Sérsníða síður fyrir hlutverk
description: Kynntu þér hvernig á að sérsníða notandaviðmótið fyrir forstillingu (hlutverk) þannig að allir notendur þess sjái sérsniðið vinnusvæði.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# Sérsníða síður fyrir forstillingar

Á Aðalaðalfundi eru bæði  [sérstillingar](ui-personalization-user.md)  fyrir notendur og sérsnið fyrir stjórnendur. Sérsnið gerir notendum kleift að sníða vinnusvæðið sitt með því að leiðrétta síðuskipan sem hentar þeirra óskum. Kerfisstjórar geta sérsniðið síðuskipan fyrir ákveðna forstillingu, byggða á hlutverkum eða deildum stjórnenda, þannig að allir úthlutuðu notendur sjái sömu sérsniðnu síðuna. Meðan sérsnið gerir notendum kleift að sýna, fela og færa svæði og aðgerðir á síðu, er boðið upp á auka getu. Til dæmis gerir sérsnið kleift að sýna svæði sem eru í upprunatöflu síðunnar eða viðaukatöflum en eru ekki skilgreind á síðunni Object &mdash; þetta eru ekki mögulegar sérstillingar.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> Dæmigerð notkun forstillingar er hlutverk. Forstilling er því heitið *Forstilling (hlutverk)* í notendaviðmóti.

Sérstilling á síðu hefst á síðunni **Forstillingar (hlutverk)**, upphafspunkt stjórnanda til að stjórna notendaforstillingum á einstökum forstillingarspjöldum. Auk þess að sérsníða síðuútlitið er hægt að breyta ýmsum öðrum stillingum fyrir forstillingar á síðunni **Sérstilling (hlutverk)** fyrir hverja forstillingu. Frekari upplýsingar eru í [Unnið með forstillingar](admin-users-profiles-roles.md).

## Frumskilyrði

- Aðalreikningur fyrirtækisins verður að hafa  **D365 Profile Mgt.** leyfi sett eða sambærilegar heimildir. 

    **D365 Profile Mgt.** heimildasafn inniheldur keyrsluheimildina í kerfinu Object  **9026 bæta við svæði í töflu**. Hafir þú ekki þessa heimild ertu ekki að bæta við reitum á síðunni nema þeir séu skilgreindir á síðuhlutnum. 

## Sérsníða síður fyrir forstillingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forstillingar (hlutverk)** og velja svo viðeigandi tengil.
2. Velja skal línuna fyrir forstillinguna sem á að sérsníða síður fyrir og síðan velja aðgerðina **Breyta**.
3. Veldu **Sérsníða síður** aðgerðina.

    [!INCLUDE[prod_short](includes/prod_short.md)] opnast í nýjum vafraglugga fyrir valda forstillingu með borðanum **Sérstilla**. Borðinn **Sérsníða** býður upp á sömu virkni og borðinn **Sérstilling** sem er aðgengilegur notendum.

4. Sérstilla síður í samræmi við þarfir hlutverks eða deildarinnar sem um ræðir á sama hátt og notandi myndi gera þegar hann sérstillir. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

    > [!NOTE]
    > Til að vafra á meðan á sérprentun stendur skal nota  <kbd>CTRL</kbd>+<kbd>smella</kbd>  á aðgerð ef hún er auðkennd með arrowhead.

5. Þegar lokið er við að breyta útlitinu á einni eða fleiri síðum skal velja hnappinn **Lokið** á borðanum **Sérsníða** .
6. Lokið vafraglugganum.

Sérstillingar fyrir síður er nú skráðar fyrir forstillinguna.

## Skoða allar sérsniðnar síður fyrir forstillingu

Hægt er að fá yfirlit yfir hvaða síður eru sérsniðnar fyrir forstillingu, til dæmis til að áætla hvaða síður á að sérsníða frekar eða eyða.

- Á síðunni **Forstilling (hlutverk)** er hægt að velja aðgerðina **Stjórna sérstilltum síðum**.

Á síðunni **Sérstilltar síður** er hægt að eyða sérstillingum og hægt er að úrræðaleita með því að skanna eftir mögulegum vandamálum.  

## Eyða öllum sérstillingum fyrir forstillingu

Hægt er að hætta við sérstillingar sem þú hefur gert fyrir forstillingu. Sérsnið kynnt með viðaukagerð og sérstillingum notanda er ekki eytt. Hægt er að eyða öllum sérstillingum með annarri aðgerð. Frekari upplýsingar er að finna á [Eyða öllum sérstillingum sem notandi hefur gert](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Á síðunni **Forstilling (hlutverk)** fyrir sérstillta forstillingu skal velja aðgerðina **Hreinsa sérstilltar síður**.

Útlitið á síðum fyrir forstillinguna er endurstillt á sjálfgefið útlit.  

## Eyða sérsniðssíðum fyrir forstillingu

Hægt er að eyða einstökum sérstillingum síðu sem hafa verið gerðar fyrir forstillingu. Sérsnið kynnt með viðaukagerð og sérstillingum notanda er ekki eytt. Hægt er að eyða tilteknum sérstillingum síðu með annarri aðgerð. Frekari upplýsingar er að finna á [Eyða sérstillingum fyrir tilteknar síður](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Á síðunni **Forstilling (hlutverk)** er hægt að velja aðgerðina **Stjórna sérstilltum síðum**.
2. Á síðunni **Sérstilltar síður** skal velja eina eða fleiri línur fyrir sérstillingar á síðu sem á að eyða og velja síðan aðgerðina **Eyða**.

Útlitinu á völdum síðum er breytt í breytingar sem gerðar voru.

## Bæta við reit

Reitum er bætt við síðuna úr  **rúðunni bæta við svæði í síðurúðu**  sem er opnaður með því að velja  **aðgerðina + reitur**  við sérsniðsstillingu. Mikilvægt er að skilja að  **svæðið bæta við svæði við síðurúðuna**   er notað til að sýna svæði sem eru þegar til &mdash; bæði á síðunni og upprunatöflum &mdash; þess en eru nú falin úr yfirliti. Ekki er hægt að stofna ný svæði.

 **Reiturinn bæta við síðurúða**  birtir alla reiti sem hægt er að sýna á síðunni. Svæðum er skipt í eftirfarandi flokka, eins og það er ákvarðað með undirliggjandi hönnun síðunnar sjálfrar, upprunatöflu hennar og viðaukum:

|Flokkur|Heimildasamstæða|
|-|-|
|Töflureitir ekki á síðuhlutanum|Inniheldur svæði sem eru skilgreind í grunntöflu eða viðaukatöflum, en eru ekki skilgreind á síðunni. Snertiskjárinn fyrir þessi svæði inniheldur merkið  **sem tilgreint er í töflunni**.<br><br>|
|Síðureitir bundnir við töflu|Inniheldur svæði sem eru skilgreind í grunntöflu eða töfluviðaukum og eru einnig skilgreind á síðunni sem annað hvort sýnd eða falin. Snertiskjárinn fyrir þessi svæði inniheldur merkið  **sem er skilgreint af síðunni**.|
|Síðureitir sem ekki eru bundnir við töflu| Svæði sem eru aðeins skilgreind á síðunni, hvorki í grunntöflu eða viðaukatöflum. Þessi svæði eru yfirleitt notuð við breytu eða útreikninga. Snertiskjárinn fyrir þessi svæði inniheldur merkið  **sem er skilgreint af síðunni**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Nota skal síuhnappinn fyrir ofan listann til að breyta því í hvaða flokki reita er sýndur  **reiturinn bæta við síðurúða** .  

:::image type="content" source="media/customization-filter.svg" alt-text="Sýnir síuhnappinn í svæðinu Bæta við reitarúðu í sérsniðsstillingunni.":::
 
### Bæta við töflusvæði sem ekki er á síðuhlut

Ef þú vilt gera töfluaðeins sem er tiltækur á síðu til notenda þá þarftu fyrst að bæta honum á síðuna. Þegar svæðinu hefur verið bætt við geta notendur valið að sýna eða fela svæðið að vild með sérstillingar. Tvær leiðir eru til að bæta við reit.

- Ein leið er að draga það frá   **til að bæta svæði við síðurúðu**  í æskilega stöðu.
- Önnur leið er að velja svæðið í rúðunni til að birta ráðlagða staðsetningu á síðunni. Síðan er farið á svæðastað á síðunum, valið örhveið og síðan valið  **Add**. 

Þegar svæðinu hefur verið bætt við er verkfærtip fyrir svæðið í   **reitnum bæta við síðurúðu**  skipt yfir í  **skilgreint af síðunni**. Reiturinn bætt er lokaður frá breyta og ekki er hægt að opna hann.

## Fjarlægja svæði

Ef bætt hefur verið við töflureit sem upphaflega var ekki á síðuhlutnum er hægt að fjarlægja hann að nýju. Að fjarlægja svæði er annað sem felur það í sér. Þegar svæði er hulið geta notendur enn sýnt það á vinnusvæði sínu í gegnum sérstillingar. Hins vegar er svæðið ekki lengur tiltækt fyrir notendur til að sýna eða fela sig fyrir það efni. Ef reiturinn er nú sem birtist á vinnusvæði notanda hverfur hann af vinnusvæði sínu þegar hann er fjarlægður. 

Svæði er fjarlægt með því að velja örhveið á svæðinu í síðunni og fjarlægja  **það síðan**. Ef ekki er hægt að finna svæðið skal velja það í  **reitnum bæta við síðu**  til að tilgreina falda staðsetningu hans. 

> [!IMPORTANT]
> Þegar svæði er fjarlægt er ekki eyða gögnum sem geymd eru í svæðinu eða upprunatöflum. Það fjarlægir bara svæðið frá útsýni. 

## Læsa og opna breytingar

Sérsnið gerir kleift að læsa (leyfa breytingar) eða aflæsa breytingum (koma í veg fyrir breytingar) af flestum svæðum á síðu. Til að læsa eða aflæsa breytingum skal velja svæðið á síðunni, velja örhvead og velja  **svo breytingar**  á lás eða  **aflæsa**. Mikilvægt er að hafa í huga nokkrar reglur um læsisstefnu og ólæsa reiti:

- Field ' ' sem upprunalega var ekki á síðuhlutnum en var bætt við síðuna með því að sérsníða er alltaf læst og ekki hægt að opna með því að nota sérsnið eða sérsnið.
- Hönnun vallarins getur einnig komið í veg fyrir að henni sé breytt. Sé AL verktaki settur breytanlegur eiginleiki  [svæðis](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property)  að  `false` þá er hann alltaf læstur og ekki hægt að aflæsa.
- Mikilvægt er að hafa í huga að breytingaraðgerðinni Læsa er ætlað að aðstoð við nákvæmni, samræmi og áreiðanleika gagna. Það er ekki ætlað til að tryggja heilindi gagna.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## Mikilvægar upplýsingar og ábendingar 

- Ekki er víst að öll töflusvæði séu tiltæk til að sérsníða úr  **rúðunni bæta við síðu** . Forritaraverktaki í töflu getur valið að koma í veg fyrir að svæði birtist í sérsnið með því að  [setja eiginleikinn](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property)  fjárheimild svæðisins  `false` í.
- Ekki er hægt að sérsníða síðu sem er í  [greiningarham](analysis-mode.md).  **Rofinn greina**  er óvirkur. Ef skipt er í sérsniðsham á meðan síðan er í greiningarham er slökkt á stillingunni sjálfvirkt. 
- Sumar síður eru með marga síðureiti sem varpa sömu upprunatöflu.  **Í reitnum bæta við síðu**  birtast allir síðureitir óháð staðsetningu. Hægt er að sýna, fela eða færa þessi svæði sjálfstætt án þess að það hafi áhrif á hina.
- Ef hluti eða flokkur er falinn er enn hægt að auðkenna falda reiti innan hlutans eða flokks, en ekki má bæta við, færa eða sýna reiti í hlutanum eða flokka fyrr en þeir eru gerðir sýnilegir. 
## Sjá einnig .

[Sérstilling verksvæðis](ui-personalization-user.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
