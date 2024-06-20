---
title: Sérsníða síður fyrir hlutverk
description: Kynntu þér hvernig á að sérsníða notandaviðmótið fyrir forstillingu (hlutverk) þannig að allir notendur þess sjái sérsniðið vinnusvæði.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 06/13/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Sérsníða síður fyrir forstillingar

Business Central býður upp á bæði [sérstillingu](ui-personalization-user.md) fyrir notendur og sérstillingu fyrir stjórnendur. Sérstilling gerir notendum kleift að sníða vinnusvæðið sitt með því að stilla síðuuppsetningar eftir eigin óskum. Kerfisstjórar geta sérsniðið síðuuppsetningar fyrir tiltekna forstillingu, byggt á viðskiptahlutverkum eða deildum, þannig að allir notendur sjái sömu sérsniðnu síðuna. Þegar sérstilling gerir notendum kleift að birta, fela og færa reiti og aðgerðir á síðu býður sérstillingin upp á aukagetu. Til dæmis gerir sérstillingin kleift að birta reiti í upprunatöflu eða viðaukatöflum síðunnar en eru ekki skilgreindir á síðuhlutnum&mdash; sem þetta er ekki mögulegt.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> Dæmigerð notkun forstillingar er hlutverk. Forstilling er því heitið *Forstilling (hlutverk)* í notendaviðmóti.

Sérstilling á síðu hefst á síðunni **Forstillingar (hlutverk)**, upphafspunkt stjórnanda til að stjórna notendaforstillingum á einstökum forstillingarspjöldum. Auk þess að sérsníða síðuútlitið er hægt að breyta ýmsum öðrum stillingum fyrir forstillingar á síðunni **Sérstilling (hlutverk)** fyrir hverja forstillingu. Frekari upplýsingar eru í [Unnið með forstillingar](admin-users-profiles-roles.md).

## Frumskilyrði

- Business Central reikningurinn þinn verður að hafa **D365 ForstillingarMgt.** heimildasafn eða sambærilegar heimildir. 

   Reiturinn **D365 Forstillingarreikningur** heimildasafnið inniheldur keyrsluheimild kerfishlutar **9026 Bæta reit við töflu**. Ef þú hefur ekki þessa heimild hefur þú ekki heimild til að bæta reitum við síðuna nema þeir séu skilgreindir á síðuhlutnum. 

## Sérstilla síður fyrir forstillingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forstillingar (hlutverk)** og velja svo viðeigandi tengil.
2. Velja skal línuna fyrir forstillinguna sem á að sérsníða síður fyrir og síðan velja aðgerðina **Breyta**.
3. Veldu **Sérsníða síður** aðgerðina.

    [!INCLUDE[prod_short](includes/prod_short.md)] opnast í nýjum vafraglugga fyrir valda forstillingu með borðanum **Sérstilla**. Borðinn **Sérsníða** býður upp á sömu virkni og borðinn **Sérstilling** sem er aðgengilegur notendum.

4. Sérstilla síður í samræmi við þarfir hlutverks eða deildarinnar sem um ræðir á sama hátt og notandi myndi gera þegar hann sérstillir. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

    > [!NOTE]
    > Til að fletta í sérstillingunni er <kbd>Ctrl</kbd>+<kbd>Smellt á</kbd> í aðgerð ef örvarhausinn auðkenndir hana.

5. Þegar lokið er við að breyta útlitinu á einni eða fleiri síðum skal velja hnappinn **Lokið** á borðanum **Sérsníða** .
6. Lokið vafraglugganum.

Sérstillingar fyrir síður er nú skráðar fyrir forstillinguna.

## Skoða allar sérsniðnar síður fyrir forstillingu

Hægt er að fá yfirlit yfir hvaða síður eru sérstilltar fyrir forstillingu, til dæmis til að áætla hvaða síður á að sérstilla frekar eða eyða.

- Á síðunni **Forstilling (hlutverk)** er hægt að velja aðgerðina **Stjórna sérstilltum síðum**.

Á síðunni **Sérstilltar síður** er hægt að eyða sérstillingum og hægt er að úrræðaleita með því að skanna eftir mögulegum vandamálum.  

## Eyða öllum sérstillingum fyrir forstillingu

Hægt er að hætta við sérstillingar sem þú hefur gert fyrir forstillingu. Sérstillingum sem birtar eru með viðbótum og sérstillingum sem notandi býr til er ekki eytt. Hægt er að eyða öllum sérstillingum með annarri aðgerð. Frekari upplýsingar er að finna á [Eyða öllum sérstillingum sem notandi hefur gert](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Á síðunni **Forstilling (hlutverk)** fyrir sérstillta forstillingu skal velja aðgerðina **Hreinsa sérstilltar síður**.

Útlitið á síðum fyrir forstillinguna er endurstillt á sjálfgefið útlit.  

## Eyða sérstillingu fyrir tilteknar síður fyrir forstillingu

Hægt er að eyða einstökum sérstillingum síðu sem hafa verið gerðar fyrir forstillingu. Sérstillingum sem birtar eru með viðbótum og sérstillingum sem notandi býr til er ekki eytt. Hægt er að eyða tilteknum sérstillingum síðu með annarri aðgerð. Frekari upplýsingar er að finna á [Eyða sérstillingum fyrir tilteknar síður](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Á síðunni **Forstilling (hlutverk)** er hægt að velja aðgerðina **Stjórna sérstilltum síðum**.
2. Á síðunni **Sérstilltar síður** skal velja eina eða fleiri línur fyrir sérstillingar á síðu sem á að eyða og velja síðan aðgerðina **Eyða**.

Útlitinu á völdum síðum er breytt í breytingar sem gerðar voru.

## Bæta við reit

Reitum er bætt við síðuna úr reitnum **Bæta við síðusvæðið** sem er opnað með því að velja aðgerðina **+ Reitur** þegar hún er í sérsniðsstillingunni. Mikilvægt er að skilja að reiturinn **Bæta við síðusvæðið**  er notaður til að sýna reiti sem eru fyrir hendi&mdash; annaðhvort á síðunni og upprunatöflur hennar,&mdash; en eru falin úr yfirliti eins og er. Ekki er hægt að búa til nýja reiti.

Reiturinn **Bæta við síðusvæðið** birtir alla reiti sem hægt er að birta á síðunni. Reitum er skipt í eftirtalda flokka eins og hún er ákvörðuð með undirliggjandi hönnun síðunnar sjálfrar, upprunatöflu hennar og viðauka:

|Flokkur|Heimildasamstæða|
|-|-|
|Töflureitir ekki á síðuhlutanum|Inniheldur reiti sem eru skilgreindir í grunntöflu eða viðbótatöflum en eru ekki skilgreindir á síðunni. Ábendingin fyrir þessa reiti inniheldur merkið **Skilgreint af töflunni**.<br><br>|
|Síðureitir bundnir við töflu|Inniheldur reiti sem eru skilgreindir í grunntöflunni eða viðbótum við töflu og eru einnig skilgreindir á síðunni sem annaðhvort sýndir eða faldir. Ábendingin fyrir þessa reiti inniheldur merkið **Skilgreint af síðunni**.|
|Síðureitir sem eru ekki bundnir við töflu| Reitir sem aðeins eru skilgreindir á síðunni, ekki í grunntöflu eða viðbótatöflum. Þessir reitir eru gjarnan notaðir við breytilegan útreikning. Ábendingin fyrir þessa reiti inniheldur merkið **Skilgreint af síðunni**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Nota skal afmörkunarhnappinn fyrir ofan listann til að breyta tegund reita sem birtast í reitnum **Bæta við síðusvæðið** .  

:::image type="content" source="media/customization-filter.svg" alt-text="Sýnir afmörkunarhnappinn á svæðinu Bæta við reit í sérsniðsstillingunni.":::
 
### Bæta við töflureit sem er ekki á síðuhlutnum

Ef gera á aðeins töflureit tiltækan á síðu við notendur verður fyrst að bæta honum við síðuna. Þegar reitnum hefur verið bætt við geta notendur valið að sýna eða fela reitinn með sérstillingu. Það eru nokkrar leiðir til að bæta við reit.

- Ein leið er að draga hana úr  **Bæta við reit á síðusvæðið** á viðeigandi stað.
- Önnur leið er að velja reitinn á svæðinu til að birta staðsetninguna sem mælt er með á síðunni. Farið er í staðsetningu reitsins á síðunum og örvarhaus valinn og Bæta við **valið**. 

Þegar reitnum hefur verið bætt við er vísbendingin fyrir reitinn í reitnum  **Bæta við síðusvæði** skipt yfir **í Skilgreint af síðunni**.

> [!NOTE]
> Viðbótarreiturinn er læstur í breytingum og ekki er hægt að aflæsa honum.

## Fjarlægja reit

Ef töflureit sem upphaflega var ekki á síðuhlutnum hefur verið bætt við er hægt að fjarlægja hann aftur. Ef reitur er fjarlægður er annað en að fela hann. Þegar reitur er felinn geta notendur samt sýnt hann á vinnusvæði sínu með sérstillingu. Ef reitur er fjarlægður er reiturinn ekki lengur tiltækur fyrir notendur til að sýna eða fela það. Ef reiturinn er birtur á vinnusvæði notanda hverfur hann af vinnusvæði þeirra þegar hann er fjarlægður. 

Til að fjarlægja reit er örvahausinn valinn á reitnum á síðunni og síðan **fjarlægja**. Ef reiturinn finnst ekki er hann valinn í reitnum **Bæta við síðusvæði** til að sýna falda staðsetningu sína. 

> [!IMPORTANT]
> Ef reitur er fjarlægður eyðir það ekki gögnum sem geymd eru í reitnum eða upprunatöflum þess. Það fjarlægir reitinn bara úr yfirliti. 

## Læsa og aflæsa breytingum

Sérstilling gerir það mögulegt að læsa (leyfa breytingar) eða aflæsa breytingum (koma í veg fyrir breytingar) flestra reita á síðu. Til að læsa eða aflæsa breytingum skal velja reitinn á síðunni, velja örvarhnappinn og velja **svo Læsa breytingu** eða **Aflæsa breytingum**. Mikilvægt er að hafa í huga nokkrar reglur um læsingu og aflæsingarreiti:

- Reitir sem voru upphaflega ekki á síðuhlutnum en var bætt við síðuna með sérstillingu eru alltaf læstir og ekki er hægt að opna með sérstillingu eða sérstillingu.
- Hönnun reitsins getur einnig komið í veg fyrir að honum sé breytt. Ef al-forritarinn stillir breytanlega [eiginleika](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property)  reitsins `false` er hann alltaf læstur og ekki hægt að aflæsa honum.
- Mikilvægt er að hafa í huga að eiginleikinn fyrir læsingu er ætlaður til aðstoðar í nákvæmni, samræmi og áreiðanleika gagna. Ekki er ætlunin að tryggja heiðarleika gagna.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## Mikilvægar upplýsingar og ábendingar

- Ekki er víst að allir töflureitir séu tiltækir til sérstillinga frá reitnum **Bæta við síðusvæði** . Forritari töflu getur valið að koma í veg fyrir að reitur birtist í sérstillingu með því að [stilla eiginleika](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) AllowInCustomization í reitnum `Never`.
- Ekki er hægt að sérstilla síðu sem er í [greiningarstillingu](analysis-mode.md). Rofi **greiningar** er óvirkur. Ef skipt er í sérsniðsham á meðan síðan er í greiningarstillingu er slökkt á greiningarstillingu sjálfkrafa. 
- Sumar síður hafa marga síðureiti sem varpa á sömu upprunatöflu. Reiturinn **Bæta við síðusvæðið** sýnir alla þessa síðureiti sérstaklega. Hægt er að sýna, fela eða færa þessa reiti hvoru í sínu lagi án þess að hafa áhrif á hina.
- Ef hluti eða hópur er falinn er samt hægt að auðkenna falda reiti innan hluta eða hóps en ekki er hægt að bæta við, færa eða birta reiti í hlutanum eða hópnum fyrr en þeir sjást. 
## Sjá einnig .

[Sérstilling verksvæðis](ui-personalization-user.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
