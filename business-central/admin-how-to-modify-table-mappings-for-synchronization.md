---
title: Vörpun töflur og reiti til að samstilla
description: Kynntu þér hvernig á að varpa töflum og reitum til að samstilla gögn milli Business Central og Microsoft Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 08/07/2024
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
ms.service: dynamics-365-business-central
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Vörpun töflur og reiti til að samstilla

Grunnurinn að því að samstilla gögn er að varpa töflum og reitum í [!INCLUDE[prod_short](includes/prod_short.md)] við töflur og dálka í [!INCLUDE[prod_short](includes/cds_long_md.md)] þannig að hægt sé að skiptast á gögnum. Vörpun gerist í samþættingartöflum.

## <a name="mapping-integration-tables"></a>Vörpun samþættingartöflum

Samþættingartafla er tafla í gagnagrunninum [!INCLUDE[prod_short](includes/prod_short.md)] sem stendur fyrir töflu í, á borð við lykil, í [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Samþættingartöflur innihalda reiti sem samsvara dálkum í [!INCLUDE[cds_long_md](includes/cds_long_md.md)] töflunni. Til dæmis tengist samþættingartafla lykils við töflu lykils í [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Það verður að vera vörpun samþættingartöflu fyrir hverja töflu í [!INCLUDE[cds_short_md](includes/cds_short_md.md)] sem á að samstilla við gögn í [!INCLUDE[prod_short](includes/prod_short.md)].

Þegar tengingin er stofnuð á milli forrita setur [!INCLUDE[prod_short](includes/prod_short.md)] upp einhverjar sjálfgefnar varpanir. Hægt er að breyta töfluvörpunum ef vilji er fyrir því. Frekari upplýsingar er að finna í [Stöðluð töfluvörpun fyrir samstilling](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Ef sjálfgefnum vörpunum hefur verið breytt og ætlunin er að bakfæra breytingarnar skal, á síðunni **Vörpun samþættingartöflu**, velja **Nota sjálfgefna samstillingaruppsetningu**.

> [!Note]
> Ef verið er að nota staðbundna útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] eru varpanir samþættingartöflu geymdar í töflu 5335 samþættingartöfluvarpanir þar sem hægt er að skoða og breyta vörpunum. Flóknar varpanir og samstillingarreglur eru skilgreina í codeunit 5341.

> [!TIP]
> Þegar paruð færsla breytist samstillir [!INCLUDE [prod_short](includes/prod_short.md)]  gögnin sjálfkrafa við Dataverse. Sjálfvirk samstilling er mikil í flestum tilfellum. Hins vegar geta tíðar breytingar á miklu magni paraðra færslna í töflu hægt á samstillingu gagna.
>
> Til að forðast hæga afköst, á síðunni **vörpun** samþættingartafla er hægt að gera gagnasamstillingu sem byggir á atburðum virka eða óvirka fyrir hvaða töflu sem er. Sjálfgefið er að samstilling sem byggist á tilvikum er kveikt á svo að fyrirliggjandi samþættingar hafi ekki áhrif. Kerfisstjórinn getur kveikt eða slökkt á honum fyrir tilteknar töflur.

### <a name="add-table-and-field-mappings-to-existing-integration-tables"></a>Bæta töflu- og reitavörpunum við fyrirliggjandi samþættingartöflur

Á síðunni **samþættingartafla Vörpun** er hægt að nota aðgerðina Nýtt töfluvörpun til að bæta nýjum töfluvörpunum við samþættingartöflur. Aðgerðin ræsir **leiðbeiningarnar Stofna nýjar samþættingarvörpun** sem hjálpa til við uppsetningu nýrra samþættingartafla og reitavörpunar.

Leiðbeiningarnar gera kleift að varpa töflunum í [!INCLUDE [prod_short](includes/prod_short.md)] með fyrirliggjandi samþættingartöflum í Dataverse. Einnig er hægt að tilgreina einkvæmt kenni töflunnar Dataverse í **samþættingartafla Heiti** reits einkvæms kennis og **samþættingartafla breytt á heiti reits** sem þarf til að gagnasamstilling virki.

> [!NOTE]
> Uppflettingin í töfludálknum sýnir allar [!INCLUDE [prod_short](includes/prod_short.md)] töflur, þar á meðal sérsniðnar töflur, sem enn er ekki búið að varpa. Hún undanskilur þá sem þegar eru til á samþættingartafla vörpunarsíðunni. Uppflettingin í dálknum samþættingartafla sýnir aðeins Dataverse töflur (AL Staðgengilstöflur) sem eru hluti af samþættingum úr úr-reitnum. Til að bæta við viðbótartöflum eða sérsniðnum Dataverse töflum þarftu hjálp frá forritara til að búa til og dreifa þeim með viðbót.

Aðgerðin Ítarlegt opnar viðbótarstillingar töfluvörpun sem hægt er að setja upp. Í hlutanum **Ítarlegt** gerir reiturinn **Töfluafmörkun** kleift að tilgreina afmarkanir fyrir [!INCLUDE [prod_short](includes/prod_short.md)]. Reiturinn **samþættingartafla Afmörkun** er notaður til Dataverse að fá gögn til greina í samstillingu gagna ásamt kótum grunnstillingarsniðmátsins í **Table Config. Sniðmátskóti** og **skilgreiningar á sniðmáti Kóti** til að fyrirframfylla gögn sem vantar þegar ný gögn koma úr öðru hvoru forritinu.

Leiðarvísirinn hjálpar einnig til við að tilgreina reitina sem nýja vörpun á að innihalda. Hægt er að samsvara [!INCLUDE [prod_short](includes/prod_short.md)] reit í dálknum Heiti **reits** og Dataverse heiti reits í dálknum **Heiti** samþættingarreits. Einnig er hægt að tilgreina **Stefna**, hvort reiturinn hafi alltaf sama gildi í dálknum **Fasti** og hvort nota þurfi sannprófanir eða umbreytingar í reitnum vörpun.

> [!NOTE]
> Til að fækka villum er uppflettingin fyrir dálkaafmarkanir **samþættingartafla Reitar** afmarkaðar við lista yfir tiltæka reiti. Ef varpa á reitum sem afmarkanirnar innihalda ekki þarf hjálp frá forritara.
>
> * Svæði verður að vera virkjuð.
> * Ekki er hægt að nota handbókina til að varpa FlowField- og FlowFilter-reitum.
> * Aðeins er hægt að varpa reitum af tegundinni BigInteger, Boolean, Code, Date, Date, DateFormula, DateTime, Decimal, Lengd, GUID, Heiltölur, Valkostur og Texti.

> [!TIP]
> Einnig er hægt að bæta nýjum reitavörpunum við fyrirliggjandi samþættingartafla vörpun með **listasíðunni Vörpun** samþættingarreita sem hægt er að fá aðgang að með því að velja **Reitir** á **samþættingartafla Vörpunarsíðunni** .
>
> Einfaldlega skal velja **Nýr reitur vörpun**  til að opna reitinn vörpun skrefi leiðsagnarforritsins **Stofna nýjar samþættingarvörpanir sem aðstoða** við uppsetningu og haldið svo áfram eins og lýst er í þessari grein.

Ný reitavörpun sem bætt er við fyrirliggjandi töfluvörpun eru í óvirkri stöðu. Hægt er að velja **Breyta lista** til að gera þá virka síðar.

### <a name="synchronization-rules"></a>Samstillingarreglur

Samþætingartöfluvörpun inniheldur einnig reglur sem hafa áhrif á hvernig samstillingarverk samþættingar samstilla færslur í töflunni [!INCLUDE[prod_short](includes/prod_short.md)] og töflu í [!INCLUDE[prod_short](includes/cds_long_md.md)]. Dæmi um reglur um samþættingu við Sala er farið í [Samstillingarreglur](#synchronization-rules).

### <a name="strategies-for-auto-resolving-conflicts"></a>Aðferðir til að leysa sjálfvirka úr árekstrum

Gagnaárekstrar geta auðveldlega átt sér stað þegar viðskiptaforrit skiptast á gögnum með reglulegu millibili. Til dæmis gæti einhver eytt eða breytt línu í einu forritanna eða báðum. Til að draga úr þeim fjölda árekstra sem þarf að leysa handvirkt er hægt að tilgreina úrlausnaraðferðir og [!INCLUDE[prod_short](includes/prod_short.md)] mun sjálfkrafa leysa úr árekstrum samkvæmt reglum aðferðarinnar.

Vörpun samþættingartöflu inniheldur reglur sem stýra því hvernig samstillingarverk samstilla færslur. Á síðunni **Vörpun samþættingartöflu**, í dálkunum **Leysir úr eyðingarárekstrum** og **Leysa úr uppfærsluárekstrum**, er hægt að tilgreina hvernig [!INCLUDE[prod_short](includes/prod_short.md)] leysir úr árekstrum sem koma upp vegna þess að færslum var eytt úr töflum í öðru hvoru viðskiptaforritinu, eða þær uppfærðar. 

Í dálknum **Leysir úr eyðingarárekstrum** er hægt að velja um að láta [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa endurheimta eyddar færslur, fjarlægja tenginguna milli færslna eða gera ekki neitt. Ef ekkert er gert er leyst úr árekstrum handvirkt. 

Í dálknum **Leysa úr uppfærsluárekstrum** er hægt að velja um að láta [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa senda gagnauppfærslu í samþættingartöfluna þegar gögn eru send til [!INCLUDE[prod_short](includes/cds_long_md.md)], eða til að fá gagnauppfærslu úr samþættingartöflunni þegar gögn er sótt úr [!INCLUDE[prod_short](includes/cds_long_md.md)], eða gera ekki neitt. Ef ekkert er gert er leyst úr árekstrum handvirkt.

Þegar búið er að tilgreina aðferðina, á síðunni **Samstillingarvilla í tengdum gögnum**, er hægt að velja aðgerðina **Reyna allt aftur** til að leysa úr árekstrum sjálfkrafa.

## <a name="mapping-integration-fields"></a>Vörpun samþættingarreitum

Vörpun á töflum er aðeins fyrsta skrefið. Einnig þarf að varpa reitunum í töflunum. Vörpun samþættingarreits tengir reiti í [!INCLUDE[prod_short](includes/prod_short.md)] töflum við samsvarandi dálka í [!INCLUDE[prod_short](includes/cds_long_md.md)] og ákvarðar hvort samstilla eigi gögn í hverri töflu. Stöðluð töfluvörpun sem [!INCLUDE[prod_short](includes/prod_short.md)] veitir inniheldur reitavarpanir en hægt er að breyta þeim ef þess er óskað. Frekari upplýsingar eru í [Skoðun töfluvarpana](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Ef notuð er staðbundin útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)] eru varpanir samþættingarreits skilgreindar í töflu 5336 vörpun samþættingarreits.

Hægt er að varpa reitunum handvirkt eða gera ferlið sjálfvirkt með því að varpa mörgum reitum samtímis byggt á skilyrði fyrir samsvörun á gildum þeirra. Frekari upplýsingar er að finna í [Að tengja margar færslur sem byggir á samsvörun reitargilda](admin-how-to-couple-and-synchronize-records-manually.md).

### <a name="handle-differences-in-field-values"></a>Meðhöndla mismun í svæðagildum

Stundum eru önnur gildi í reitunum sem á að varpa. Til dæmis, í [!INCLUDE[crm_md](includes/crm_md.md)] er tungumálakóðinn fyrir Bandaríkin „U.S.“ en í [!INCLUDE[prod_short](includes/prod_short.md)] er hann „US.“ Það þýðir að þú verður að umbreyta gildinu þegar þú samstillir gögn. Þetta gerist í gegnum breytingareglur sem eru skilgreindar fyrir svæðin. Umbreytingarreglur eru skilgreindar á síðunni **Varpanir samþættingartöflu** með því að velja **Vörpun** og síðan **Reitir**. Boðið er upp á forskilgreindar reglur, en einnig má búa til sínar eigin. Frekari upplýsingar er að finna í [Umbreytingarreglur](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handle-missing-option-values"></a>Meðhöndla valkostagildi sem vantar

[!INCLUDE[prod_short](includes/cds_long_md.md)] inniheldur dálka fyrir valkosti sem bjóða upp á gildi sem hægt er að varpa í [!INCLUDE[prod_short](includes/prod_short.md)] reiti af gerðinni **Valkostur** fyrir sjálfvirka samstillingu. Við samstillingu eru óvarpaðir valkostir hunsaðir og valkostina sem vantar er komið fyrir í tengdri [!INCLUDE[prod_short](includes/prod_short.md)] töflu og bætt við kerfistöfluna **Vörpun CDS-valkosta** til að meðhöndla handvirkt seinna. Til dæmis með því að bæta við valkostunum sem vantar í aðrahvora vöruna og síðan uppfæra vörpunina. Frekari upplýsingar er að finna í [Að meðhöndla gildi sem vantar fyrir valkosti](admin-cds-missing-option-values.md).

## <a name="couple-records"></a>Paraskrár

Tenging tengir línur í [!INCLUDE[prod_short](includes/cds_long_md.md)] við færslur í [!INCLUDE[prod_short](includes/prod_short.md)]. Til dæmis eru lyklar í [!INCLUDE[prod_short](includes/cds_long_md.md)] yfirleitt samtengdir við viðskiptavini í [!INCLUDE[prod_short](includes/prod_short.md)]. Að tengja færslur býður upp á eftirfarandi ávinning:

* Það gerir samstillingu mögulega.
* Notendur geta opnað færslur eða línur í einu viðskiptaforriti úr hinu. Þetta krefst þess að forritin séu þegar samþætt.

Hægt er að setja upp tengingar sjálfkrafa með því að nota samstillingarverk eða handvirkt með því að breyta færslunni í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Samstilla gögn í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) og [Tengja og samstilla færslur handvirkt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filter-records-and-rows"></a>Afmarka færslur og línur

Ef ekki á að samstilla allar línur fyrir tiltekna töflu í [!INCLUDE[prod_short](includes/cds_long_md.md)] eða í töflunni [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að setja upp afmarkanir til að takmarka gögnin sem eru samstillt. Afmarkanir eru settar upp á síðunni **Varpanir samþættingartöflu**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.
2. Til að afmarka [!INCLUDE[prod_short](includes/prod_short.md)] skrár er reiturinn **Töfluafmörkun** stilltur.  
3. Til að afmarka [!INCLUDE[prod_short](includes/cds_long_md.md)] línur er reiturinn **Afmörkun samþættingartöflu** stilltur.  

## <a name="create-new-records"></a>Stofna nýjar færslur

Sjálfgefið munu aðeins færslur í [!INCLUDE[prod_short](includes/prod_short.md)] og línur í [!INCLUDE[prod_short](includes/cds_long_md.md)] sem eru tengdar vera samstilltar eftir samstillingarverkum samþættingarinnar. Hægt er að setja upp töfluvarpanir til að nýjar færslur verði stofnaðar á áfangastaðnum (t.d., [!INCLUDE[prod_short](includes/prod_short.md)]) fyrir hverja nýja línu í upprunanum (t.d., [!INCLUDE[prod_short](includes/cds_long_md.md)]) sem ekki er þegar tengd.  

Til dæmis notar samstillingarverkið SÖLUFÓLK – Dynamics 365 Sales samstillingarverk töfluvörpunina SÖLUFÓLK. Samstillingarverkið afritar gögn frá notendum í [!INCLUDE[prod_short](includes/cds_long_md.md)] yfir í sölumenn í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef töfluvörpun er sett upp til að stofna nýjar færslur er, fyrir hvern nýjan notanda í [!INCLUDE[prod_short](includes/cds_long_md.md)] sem er ekki þegar tengdur við sölumann í [!INCLUDE[prod_short](includes/prod_short.md)], stofnuð ný sölumannslína í [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-create-new-records-during-synchronization"></a>Til að stofna nýjar færslur við samstillingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.
2. Í færslu töfluvörpunar í listanum skal hreinsa reitinn **Samst. aðeins tengdar færslur**.  

## <a name="use-configuration-templates-on-table-mappings"></a>Nota skilgreiningarsniðmát í töfluvörpunum

Hægt er að úthluta skilgreiningarsniðmátum á töfluvarpanir til að nota fyrir nýjar línur sem stofnaðar eru í [!INCLUDE[prod_short](includes/prod_short.md)] eða [!INCLUDE[prod_short](includes/cds_long_md.md)]. Fyrir hverja töfluvörpun má tilgreina skilgreiningarsniðmát til að nota fyrir nýjar [!INCLUDE[prod_short](includes/prod_short.md)] færslur og annað sniðmát til að nota fyrir nýjar [!INCLUDE[prod_short](includes/cds_long_md.md)] línur.  

Ef sett er upp sjálfgefinn samstillingargrunnur verða skilgreiningarsniðmátin yfirleitt búin til sjálfkrafa og notuð á töfluvörpun fyrir [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamenn og [!INCLUDE[crm_md](includes/crm_md.md)] lykla: **CDSCUST** og **CDSACCOUNT**.  

* **CDSCUST** stofnar og samstillir nýja viðskiptavini með [!INCLUDE[prod_short](includes/prod_short.md)] hliðsjón af reikningum í [!INCLUDE[crm_md](includes/crm_md.md)].  

     Stofna þetta sniðmát með því að afrita fyrirliggjandi skilgreiningarsniðmát fyrir viðskiptamenn. **CDSCUST** er aðeins búið til ef skilgreiningarsniðmát er fyrirliggjandi og reiturinn **Gjaldmiðilskóði** í því sniðmáti er auður. Ef reitur í skilgreiningarsniðmát inniheldur gildi, verður það gildi notað í stað gildis í varpaða dálkinum í reikningnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Ef dálkurinn **Land/svæði** í reikningi í reikningi í [!INCLUDE[prod_short](includes/cds_long_md.md)]  *inniheldur Til dæmis Bandaríki.* og reiturinn **Land/svæði** í skilgreiningarsniðmátinu er **GB**, þá **er GB** notað sem **Land/svæði** viðskiptamannsins í [!INCLUDE[prod_short](includes/prod_short.md)].  

* **CDSACCOUNT** stofnar og samstillir nýja lykla í [!INCLUDE[prod_short](includes/cds_long_md.md)] sem byggist á lykli í [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Til að tilgreina skilgreiningarsniðmát í töfluvörpunum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörpun samþættingartöflu** og veldu síðan tengda tengilinn.
2. Í færslu töfluvörpunar í listanum, í reitnum **Sniðmátskóði fyrir skilgreiningartöflu**, skal velja skilgreiningarsniðmátið til að nota fyrir nýjar færslur í [!INCLUDE[prod_short](includes/prod_short.md)].  
3. Stilla skal reitinn **Sniðmátskóði fyrir innri skilgreiningartöflu** á skilgreiningarsniðmátið til að nota fyrir nýjar færslur í [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a>Sjá einnig .

[Um samþættingu Dynamics 365 Business Central við [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )  
[Samstilling Business Central og [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
