---
title: Vörpun fyrirtækis- og viðskiptaeiningar | Microsoft Docs
description: Fyrirtæki eru bæði lagalegar og viðskiptalegar einingar og eru notuð til að tryggja í sessi og gefa yfirsýn yfir viðskiptagögn.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'CDS, Dataverse, integration, sync'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="data-ownership-models"></a><a name="data-ownership-models"></a><a name="data-ownership-models"></a>Eignarhaldslíkön gagna


[!INCLUDE[prod_short](includes/cds_long_md.md)] krefst þess að tilgreindur sé eigandi fyrir gögnin sem eru geymd. Frekari upplýsingar eru í [Gerðir af töflum](/powerapps/maker/data-platform/types-of-entities) í Power Apps fylgiskjölum. Þegar samþætting er sett upp á milli [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] þarf að velja **Notandi eða teymi** fyrir færslur sem eru samstilltar. Aðgerðir sem hægt er að framkvæma á þessum færslum er hægt að stjórna á notandastigi. <!--We recommend the Team ownership model because it makes it easier to manage ownership for multiple people.NO LONGER TRUE IN DATAVERSE-->

## <a name="team-ownership"></a><a name="team-ownership"></a><a name="team-ownership"></a>Eignarhald teymis
Í [!INCLUDE[prod_short](includes/prod_short.md)] er fyrirtæki lagaleg og viðskiptaleg tafla sem býður upp á leiðir til að tryggja í sessi og gefa yfirsýn yfir viðskiptagögn. Notendur vinna alltaf í tengslum við fyrirtæki. Það næsta sem [!INCLUDE[prod_short](includes/cds_long_md.md)] kemst að þessu hugtaki er viðskiptaeiningartaflan, sem hefur ekki lagaleg eða viðskiptaleg áhrif.

Vegna þess að fyrirtækiseiningar skortir lagaleg og viðskiptaleg áhrif, er ekki hægt að þvinga einn á móti einum (1:1) vörpun til að samstilla gögn milli fyrirtækis- og viðskiptaeiningar, annaðhvort í aðra eða báðar áttir. Til að gera samstillingu mögulega, þegar samstilling er virkjuð fyrir fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)], gerist eftirfarandi í [!INCLUDE[prod_short](includes/cds_long_md.md)]:

* Við stofnun fyrirtækistöflu sem er jafngildi fyrirtækistöflunnar í [!INCLUDE[prod_short](includes/prod_short.md)]. Heiti fyrirtækisins fær viðskeytið „BC fyrirtækiskenni.“ Til dæmis Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Við stofnum sjálfgefna viðskiptaeiningu sem er með sama heiti og fyrirtækið. Til dæmis Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Við búum til aðskilið eigendateymi með sama heiti og fyrirtækið og tengjum það við viðskiptaeininguna. Heiti teymisins fær forskeytið „BCI -.“ Til dæmis BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Færslur sem eru búnar til og samstilltar við [!INCLUDE[prod_short](includes/cds_long_md.md)] er úthlutað á teymið „BCI-eigandi“ sem er tengt við viðskiptaeininguna.

> [!NOTE]
> Ef þú endurnefnir fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)] er heiti fyrirtækisins, starsemi og teymis sem við búum til sjálfkrafa í [!INCLUDE[prod_short](includes/cds_long_md.md)] ekki uppfærð. Þar sem aðeins auðkenni fyrirtækisins er notað til samþættingar hefur þetta ekki áhrif á samstillingu. Ef þú vilt að heitin passi saman verður þú að uppfæra fyrirtækið, fyrirtækiseininguna og teymið í [!INCLUDE[prod_short](includes/cds_long_md.md)].

Eftirfarandi mynd sýnir dæmi um þessa gagnauppsetningu í [!INCLUDE[prod_short](includes/cds_long_md.md)].

![Rót viðskiptaeiningarinnar er efst, teymin eru í miðjunni og síðan eru fyrirtækin neðst.](media/cds_bu_team_company.png)

Í þessari grunnstillingu eru færslur sem tengjast Cronus US fyrirtækinu í eigu teymis sem tengist CRONUS US  rekstrareiningunni í [!INCLUDE[prod_short](includes/cds_long_md.md)]. Notendur sem hafa aðgang að viðskiptaeiningunni í gegnum öryggishlutverk sem er stillt á sýnileika viðskiptaeiningarstigs í [!INCLUDE[prod_short](includes/cds_long_md.md)] geta nú séð færslurnar. Eftirfarandi dæmi sýnir hvernig á að nota teymi til að veita aðgang að þessum færslum.

* Hlutverki sölustjóra er úthlutað til meðlima í söluteymi Cronus US.
* Notendur sem eru með hlutverk sölustjóra hafa aðgang að reikningsfærslum fyrir meðlimi sömu viðskiptaeiningar.
* Söluteymi Cronus US tengist viðskiptaeiningu Cronus US, sem áður var nefnt. Meðlimir söluteymis Cronus US geta séð alla reikninga sem eru í eigu Cronus US  notanda, sem hefði komið frá fyrirtækistöflu Cronus US í [!INCLUDE[prod_short](includes/prod_short.md)].

Hins vegar er 1:1 vörpunin milli viðskiptaeininga, fyrirtækis og teymis aðeins byrjunarreitur, eins og sést í eftirfarandi mynd.

![Öryggishlutverkið stjórnar sýnileika gagna.](media/cds_bu_team_company_2.png)

Í þessu dæmi er ný EUR (Evrópa) rót viðskiptaeiningar búin til í [!INCLUDE[prod_short](includes/cds_long_md.md)] sem yfireining fyrir bæði Cronus DE (Þýskaland) og Cronus ES (Spánn). EUR viðskiptaeiningin er ekki tengd samstillingu. Hins vegar getur hún gefið meðlimum EUR söluteymis aðgang að reikningsgögnum bæði í Cronus DE og Cronus ES með því að stilla gagnasýnileika á **Yfir-/undirstig viðskiptaeiningar** í tengdu öryggishlutverki í [!INCLUDE[prod_short](includes/cds_long_md.md)].

Samstilling ákvarðar hvaða teymi skal eiga færslur. Þessu er stjórnað af reitnum **Sjálfgefið eigendateymi** í BCI -  línunni. Þegar BCI-færsla er virkjuð fyrir samstillingu búum við sjálfkrafa til tengda viðskiptaeiningu og eigendateymi (ef það er ekki þegar til) og stillum reitinn **Sjálfgefið eigendateymi**. Þegar samstilling er virkjuð fyrir töflu geta stjórnendur breytt eigendateyminu, en alltaf verður að úthluta teymi.

> [!NOTE]
> Færslur verða skrifvarðar eftir að fyrirtæki er bætt við og því skal gæta þess að velja rétt fyrirtæki.

## <a name="choosing-a-different-business-unit"></a><a name="choosing-a-different-business-unit"></a><a name="choosing-a-different-business-unit"></a>Að velja aðra viðskiptaeiningu
Þú getur breytt vali á fyrirtækiseiningu ef þú ert að nota eignarhaldslíkan Teams. Ef þú notar eignarhaldalíkan einstaklings er sjálfgefinn fyrirtækiseining alltaf valin. 

Ef þú velur aðra fyrirtækiseiningu, til dæmis einhverja þú varst bj+óst til áður í [!INCLUDE[prod_short](includes/cds_long_md.md)], mun hún halda upprunalegu heiti sínu. Það verður sem sagt ekki bætt viðskeyti við fyrirtækiskennið. Við búum til teymi sem notast við hefðbundna nafngift.

Þegar fyrirtækiseiningu er breytt er aðeins hægt að velja fyrirtækiseiningar sem eru einu stigi fyrir neðan rótarfyrirtækiseiningu.

## <a name="person-ownership"></a><a name="person-ownership"></a><a name="person-ownership"></a>Eignarhald einstaklings
Ef valið er eignarhaldslíkan einstaklings þarf að tilgreina alla sölumenn sem munu vera með nýjar færslur. Fyrirtækiseiningin og teymið eru útbúin eins og lýst er í hlutanum [Eignarhald teymis](admin-cds-company-concept.md#team-ownership).

Sjálfgefna fyrirtækiseiningin er notuð þegar einstaklingseignarhaldslíkan er valið og ekki er hægt að velja aðra fyrirtækiseiningu. Þessi hópur sem tengist sjálfgefinni fyrirtækistöflu mun fá færslur fyrir algengar töflur, eins og vörutöflu, sem tengist ekki sérstökum sölumönnum.

Þegar sölumenn í [!INCLUDE[prod_short](includes/prod_short.md)] eru tengdir við notendur í [!INCLUDE[prod_short](includes/cds_long_md.md)], mun [!INCLUDE[prod_short](includes/prod_short.md)] bæta notandanum við sjálfgefna hópinn í [!INCLUDE[prod_short](includes/cds_long_md.md)]. Hægt er að staðfesta að notendum hafi verið bætt við með því að skoða dálkinn **Sjálfgefinn hópmeðlimur** á síðunni **Notendur - Common Data Service**. Ef notandanum er ekki bætt við er hægt að bæta honum handvirkt við með því að nota aðgerðina **Bæta tengdum notendum við hóp**. Frekari upplýsingar er að finna í [Samstilling gagna í Business Central við Dataverse](admin-synchronizing-business-central-and-sales.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Um [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-common-data-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
