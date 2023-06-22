---
title: Tengja og samstilla (inniheldur myndskeið)
description: Samstilling samþættingartöflu virkjar gagnasamþættingu í öllum færslum í töflu í Business Central og Dynamics 365 Sales töflu sem eru tengdar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
---

# <a name="couple-and-synchronize-records-between-dataverse-and-business-central" />Par og samstilla færslur á milli  Dataverse  og viðskipta miðlægt

Þetta efnisatriði lýsir því hvernig á að tengja eina eða fleiri færslur í [!INCLUDE[prod_short](includes/prod_short.md)] við færslur í Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)]. Að tengja færslur gerir þér kleift að skoða Dataverse upplýsingar úr [!INCLUDE[prod_short](includes/prod_short.md)] og öfugt. Tenging gerir þér einnig að samstilla gögn á milli færslna. Hægt er að tengja fyrirliggjandi færslur eða stofna og tengja nýjar færslur.

> [!NOTE]
> Tenging og samstilling gagna við er aðeins í boði ef kerfisstjórinn hefur búið til tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)]. Fljótleg leið til að athuga þetta er að opna spjaldið **Viðskiptamaður** og leita að aðgerðinni **Setja upp tengingu**. Ef aðgerðin er tiltæk eru forritin tengd.

## <a name="video-example" />Myndbandsdæmi

Þetta myndband sýnir tengingar- og samstillingargögn í samhengi samþættingar við [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record" />Til að tengja færslu

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna spjaldið fyrir færsluna sem á að tengja. Til dæmis viðskiptamanna- eða tengiliðaspjald.  

    Einnig er hægt að opna listasíðu og velja færsluna sem á að tengja.  

2. Veldu aðgerðina **Setja upp tengingu**.  
3. Fylltu út reitina og smelltu síðan á hnappinn **Í lagi**.  

## <a name="to-synchronize-a-single-record" />Til að samstilla staka færslu

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna spjaldið fyrir færsluna sem á að tengja. Til dæmis viðskiptamanna- eða tengiliðaspjald.  
2. Veldu aðgerðina **Samstilla núna**.  
3. Ef hægt er að samstilla færslu í aðra áttina, skal velja valkostinn sem tilgreinir átt gagnauppfærslu og velja síðan **Í lagi**.  

## <a name="to-synchronize-a-single-record-from-includecrmmdincludescrmmdmd" />Að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)]

1. Í [!INCLUDE[crm_md](includes/crm_md.md)] skal opna skjámynd fyrir færsluna sem á að tengja. Til dæmis skjámynd reiknings- eða tengiliðaspjalds.  
2. Veldu aðgerðina **[!INCLUDE[prod_short](includes/prod_short.md)]** í borðanum til að opna og tengja færslu sjálfkrafa.

    > [!Note]
    > Aðeins er hægt að samstilla staka færslu  [!INCLUDE[crm_md](includes/crm_md.md)]  sjálfkrafa við  **samstillingu. Aðeins Afsláttarfærslur**  eru óvirkar og samstillingarstefnan er stillt á  **tvístefnu**  eða  **úr Samþættingartöflu**  á  **vörpunarsíðu**  samþættingar fyrir færsluna. Frekari upplýsingar  [fást með því að varpa í töflur og svæði til að samstilla](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## <a name="to-couple-multiple-records-using-match-based-coupling" />Að tengja margar færslur með því að nota tengi sem byggir á samsvörun

Tilgreina gögnin sem á að samstilla fyrir einingu, eins og viðskiptavin eða tengilið, eftir afsláttarfærslum sem byggjast á samstæðum. Betrumbæta samsvörunina með því að gera leitina viðkvæm og úthluta forgangi fyrir hverja samsvörun. Ef engin samsvörun finnst er einnig hægt að tilgreina að þú viljir stofna eininguna í Dataverse. Nánari upplýsingar er að fara í til að  [Sérsníða samsvörun festinga](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Samsvörun byggir á ferli Sleipnir færslur sem þegar er jafnað. Til að taka þessar færslur með þegar þú keyrir samsvörun, ófáar færslur og reyndu aftur. Ef fræðast á um ónúmeraplötur er farið í  [Ósópandi færslur](#uncoupling-records).

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] er opnuð listasíða fyrir færsluna, t.d. listasíður viðskiptamanna eða tengiliða.
2. Veldu aðgerðina **Tenging byggð á samsvörun**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records" />Til að samstilla margar færslur

1.  [!INCLUDE[prod_short](includes/prod_short.md)] Opnið listasíðuna fyrir færsluna, eins og viðskiptamenn eða tengiliðsíðurnar.  
2. Veldu færslurnar sem á að samstilla og veldu svo aðgerðina **Samstilla núna**.  
3. Ef hægt er að samstilla færslur í eina átt skal velja valkostinn sem tilgreinir stefnuna og velja svo **Í lagi**.  

## <a name="bulk-insert-and-couple-records" />Fjöldainnsetningarfærslur og par

Ef um er að ræða mikinn fjölda  Dataverse  eininga sem samsvara færslum í  [!INCLUDE [prod_short](includes/prod_short.md)] er hægt að setja inn og par í-magn. Til dæmis væri hægt að setja upp biðfærslur og par þegar samstilling er sett upp í fyrsta sinn.

Þú notar  **Leiðsagnarforrit**  gagnainnflutnings í  **Microsoft Power Platform  admin Center**.

Eftirfarandi dæmi lýsir því hvernig á að fjöldasetja inn og par viðskiptavini með lykla í Dataverse. Nota skal sama ferli fyrir aðrar tegundir eininga, svo sem lánardrottna, vörur og forða.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2.  **Velja Open í aðgerð Excel**  til að opna viðskiptavinagögn í Excel. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Til að varpa og flytja gögn  **í lykileiningu**  í  Dataverse er fylgt þeim skrefum sem lýst er í  [innflutningsgögnum (allar færslugerðir) frá mörgum aðilum](/power-platform/admin/import-data-all-record-types).  

    Ef Reikningseiningin er með  **bcbi_companyid**  dálk þegar dálkarnir eru kortaðir er tryggt að innflutningurinn ÚTHLUTAR viðeigandi kenni fyrirtækis í dálknum fyrir hverja innflutta færslu. Eftirfarandi er fundið með því að finna AUÐKENNI fyrirtækis í  [!INCLUDE [prod_short](includes/prod_short.md)] eftirfarandi:

    1.  **Opnið síðuna töfluvörpun**  samþættingar.
    2.  **Veldu vörpun viðskiptavinar**  og veldu  **síðan breyta lista**.
    3. Skrunað er til hægri og valinn hnappurinn aðstoða Edit  :::image type="icon" source="media/assist-edit-icon.png" border="false":::  í  **reitnum Afmörkun**  samþættingar. Þetta sýnir sjálfgefna síu fyrir vörpun viðskiptavinar og í henni er KENNI fyrirtækisins. AUÐKENNI fyrirtækis er fyrsta hluta virðis. Afrita aðeins þann hluta, og hunsa 0s. Eftirfarandi dæmi eru í hámörkun hluta til afritunar.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Sýnir þann hluta fyrirtækjakennis sem á að afrita.":::

    > [!NOTE]
    > Ekki er um að ræða öll nöfn  Dataverse  eininga og miðlægu færslur fyrirtækja. Eftir því hvað verið er að flytja inn skal tvöfalda tékka sem eftirfarandi dálka hafa eftirfarandi gildi eftir innflutning:
    >
    >* Fyrir viðskiptavini  **ætti dálkurinn customertypecode**  að innihalda  **viðskiptavin**.
    >* Fyrir lánardrottna ætti að geyma  **lánardrottna**  í  **customertypecode** dálkinum. 
    >* Til vara  **ætti dálkurinn producttypecode**  að innihalda  **sölubirgðir**.
    >* Fyrir forða  **ætti dálkurinn producttypecode**  að innihalda  **þjónustu**.
 
4. Eftir að gögn  Dataverse  hafa verið flutt inn í umhverfið  [!INCLUDE [prod_short](includes/prod_short.md)], skal fylgja skrefunum  [í nokkrar margar færslur með því að nota samsvörun sem byggð](#to-couple-multiple-records-using-match-based-coupling)  er á tveimur  Dataverse  einingum með  [!INCLUDE [prod_short](includes/prod_short.md)]  færslur. 

## <a name="uncoupling-records" />Aftengja færslur

Hægt er að aftengja eina eða fleiri færslur af listasíðum eða síðunni **Samstillingarvillur í tengdum gögnum** með því að velja eina eða fleiri línu og velja **Eyða tengingu**. Einnig er hægt að fjarlægja allar tengingar fyrir eina eða fleiri töfluvörpun á síðunni **Vörpun samþættingartöflu**.

## <a name="see-also" />Sjá einnig

[Nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
