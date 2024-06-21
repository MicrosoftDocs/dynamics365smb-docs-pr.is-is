---
title: Tenging og samstilling
description: Samstilling samþættingartöflu virkjar gagnasamþættingu í öllum færslum í töflu í Business Central og Dynamics 365 Sales töflu sem eru tengdar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
ms.service: dynamics-365-business-central
---

# <a name="couple-and-synchronize-records-between-dataverse-and-business-central"></a>Par og samstilla færslur milli Dataverse og Business Central

Þetta efnisatriði lýsir því hvernig á að tengja eina eða fleiri færslur í [!INCLUDE[prod_short](includes/prod_short.md)] við færslur í Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)]. Að tengja færslur gerir þér kleift að skoða Dataverse upplýsingar úr [!INCLUDE[prod_short](includes/prod_short.md)] og öfugt. Tenging gerir þér einnig að samstilla gögn á milli færslna. Hægt er að tengja fyrirliggjandi færslur eða stofna og tengja nýjar færslur.

> [!NOTE]
> Tenging og samstilling gagna við er aðeins í boði ef kerfisstjórinn hefur búið til tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)]. Fljótleg leið til að athuga þetta er að opna spjaldið **Viðskiptamaður** og leita að aðgerðinni **Setja upp tengingu**. Ef aðgerðin er tiltæk eru forritin tengd.

## <a name="video-example"></a>Myndbandsdæmi

Þetta myndband sýnir tengingar- og samstillingargögn í samhengi samþættingar við [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Til að tengja færslu

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna spjaldið fyrir færsluna sem á að tengja. Til dæmis viðskiptamanna- eða tengiliðaspjald.  

    Einnig er hægt að opna listasíðu og velja færsluna sem á að tengja.  

2. Veldu aðgerðina **Setja upp tengingu**.  
3. Fylltu út reitina og smelltu síðan á hnappinn **Í lagi**.  

## <a name="to-synchronize-a-single-record"></a>Til að samstilla staka færslu

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna spjaldið fyrir færsluna sem á að tengja. Til dæmis viðskiptamanna- eða tengiliðaspjald.  
2. Veldu aðgerðina **Samstilla núna**.  
3. Ef hægt er að samstilla færslu í aðra áttina, skal velja valkostinn sem tilgreinir átt gagnauppfærslu og velja síðan **Í lagi**.  

## <a name="to-synchronize-a-single-record-from-"></a>Að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)]

1. Í [!INCLUDE[crm_md](includes/crm_md.md)] skal opna skjámynd fyrir færsluna sem á að tengja. Til dæmis skjámynd reiknings- eða tengiliðaspjalds.  
2. Veldu aðgerðina **[!INCLUDE[prod_short](includes/prod_short.md)]** í borðanum til að opna og tengja færslu sjálfkrafa.

    > [!Note]
    > Aðeins er hægt að samstilla eina færslu sjálfkrafa [!INCLUDE[crm_md](includes/crm_md.md)] þegar **samstilla á Aðeins paraðar færslur** eru óvirkar og samstillingarstefnan er stillt **á Tvíátta** eða **Úr samþættingartöflu** á síðunni **Vörpun** samþættingartöflu fyrir færsluna. Nánari upplýsingar [eru í Varpað á töflur og reiti til að samstilla](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Að tengja margar færslur með því að nota tengi sem byggir á samsvörun

Tilgreina gögn til að samstilla fyrir einingu, t.d. viðskiptamann eða tengilið, með því að tengja færslur byggðar á samsvörunum. Fínstilla samsvörunina með því að gera leitarmálin viðkvæm og úthluta forgangi fyrir hverja samsvörun. Ef engin samsvörun finnst er einnig hægt að tilgreina að þú viljir stofna eininguna í Dataverse. Nánari upplýsingar eru í Sérstilla [samsvörunarjöfnun](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Samsvörunarferlið sleppir færslum sem þegar hafa verið jafnaðar. Til að taka þær færslur með þegar keyrð er samsvörun fyrir festingu skal afskrá færslurnar og reyna aftur. Til að [fræðast meira um afskráningu færslna er farið í Afskráningarfærslna](#uncoupling-records).

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] er opnuð listasíða fyrir færsluna, t.d. listasíður viðskiptamanna eða tengiliða.
2. Veldu aðgerðina **Tenging byggð á samsvörun**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Til að samstilla margar færslur

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna listasíðuna fyrir færsluna, t.d. síðurnar Viðskiptamenn eða Tengiliðir.  
2. Veldu færslurnar sem á að samstilla og veldu svo aðgerðina **Samstilla núna**.  
3. Ef hægt er að samstilla færslur í eina átt skal velja valkostinn sem tilgreinir stefnuna og velja svo **Í lagi**.  

## <a name="bulk-insert-and-couple-records"></a>Magn-setja inn og par færslur

Ef um er að ræða margar Dataverse einingar sem samsvara færslum [!INCLUDE [prod_short](includes/prod_short.md)] er hægt að skjóta þeim inn og taka saman í magni. Til dæmis gæti þurft að setja inn fjöldainnsetningu og nokkrar færslur þegar samstilling er sett upp í fyrsta skipti.

Leiðsagnarforritið **Gagnainnflutningur** verður notað í **Microsoft Power Platform stjórnunarstöðinni**.

Eftirfarandi dæmi lýsir því hvernig á að setja inn og para viðskiptamenn með reikninga í Dataverse. Nota sama ferli fyrir aðrar gerðir eininga, svo sem lánardrottna, vara og forða.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Opna í Excel** til að opna gögn viðskiptavina í Excel. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Til að varpa og flytja gögn inn í reikningseininguna **í** Dataverse skal fylgja skrefunum sem lýst er í [Flytja inn gögn (allar færslutegundir) úr mörgum](/power-platform/admin/import-data-all-record-types) uppruna.  

    Ef reikningseiningin er með **bcbi_companyid** dálka ganga þeir úr skugga um að innflutningurinn úthlutar viðeigandi kenni fyrirtækis í dálknum fyrir allar innfluttar færslur. Til að finna kenni fyrirtækis er [!INCLUDE [prod_short](includes/prod_short.md)] eftirfarandi skrefum fylgt:

    1. Opna skal síðuna **Vörpun** samþættingartöflu.
    2. Vörpun viðskiptamanns er **valin og Breyta lista**  síðan valið **.**
    3. Skrunið til hægri og veljið assist edit :::image type="icon" source="media/assist-edit-icon.png" border="false"::: hnappinn í reitnum **Afmörkun** samþættingartöflu. Þetta sýnir sjálfgefna afmörkun fyrir viðskiptamannavörpun og í honum er kenni fyrirtækisins. Fyrirtækiskennið er fyrsti hluti gildsins. Afritaðu aðeins þann hluta og hunsaðu 0s. Eftirfarandi dæmi sýnir þann hluta sem á að afrita.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Sýnir þann hluta fyrirtækiskennisins sem á að afrita.":::

    > [!NOTE]
    > Ekki eru öll nöfn Dataverse eininga og Business Central-færslna samsvörun. Eftir því hvað verið er að flytja inn skal athuga hvort eftirtaldir dálkar hafi eftirfarandi gildi eftir innflutning:
    >
    >* Í dálknum **CustomerTypeCode** ætti að vera **Viðskiptamaður fyrir viðskiptamenn**.
    >* Í dálknum **CustomerTypeCode** ætti að vera **Lánardrottnar fyrir lánardrottna**. 
    >* Í dálknum **ProductTypeCode** ætti að vera **Sölubirgðir** fyrir vörur.
    >* Í dálknum **ProductTypeCode** ætti að vera **þjónusta** fyrir forða.
 
4. Eftir að gögn hafa verið flutt inn í umhverfið Dataverse , í [!INCLUDE [prod_short](includes/prod_short.md)], skal fylgja skrefunum [Til að para margar færslur með því að nota samsvörunarjöfnun](#to-couple-multiple-records-using-match-based-coupling) til að para Dataverse einingarnar með [!INCLUDE [prod_short](includes/prod_short.md)] færslum. 

## <a name="uncoupling-records"></a>Aftengja færslur

Hægt er að aftengja eina eða fleiri færslur af listasíðum eða síðunni **Samstillingarvillur í tengdum gögnum** með því að velja eina eða fleiri línu og velja **Eyða tengingu**. Einnig er hægt að fjarlægja allar tengingar fyrir eina eða fleiri töfluvörpun á síðunni **Vörpun samþættingartöflu**.

## <a name="see-also"></a>Sjá einnig

[Nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
