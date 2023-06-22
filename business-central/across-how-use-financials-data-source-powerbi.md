---
title: Byggja skýrslur á Power BI Desktop til að birta Business Central Data | Microsoft docs
description: Notandi getur gert gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 09/07/2022
ms.author: jswymer
---

# <a name="building-power-bi-reports-to-display-include-prodlongincludesprodlongmd-data" />Búa til Power BI skýrslur til að birta [!INCLUDE [prod_long](includes/prod_long.md)] -gögn

Notandi getur gert [!INCLUDE[prod_long](includes/prod_long.md)]-gögnin sín aðgengileg sem gagnaveitu í Power BI Desktop og byggt upp öflugar skýrslur um stöðu síns reksturs.

Þessi grein lýsir því hvernig hafist er handa við að nota Power BI Desktop til að búa til skýrslur sem birta [!INCLUDE[prod_long](includes/prod_long.md)] gögn.  Þegar búið er að stofna skýrslur er hægt að birta þær í Power BI þjónustunni eða deila þeim með öllum notendum í fyrirtækinu. Þegar þessar skýrslur eru í Power BI þjónustunni geta notendur sem eru settir upp í henni skoðað skýrslurnar í [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready" />Vertu með allt á tæru

- Skráðu þig fyrir nýju Power BI þjónustuna.

  Ef þú hefur ekki þegar skráð þig skaltu fara á [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Þegar þú skráir þig skaltu nota vinnunetfang og aðgangsorð.

- Sækja [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop er ókeypis forrit sem þú setur upp á staðbundinni tölvu. Frekari upplýsingar er að finna í [Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Ganga skal úr skugga um að gögnin sem óskað er eftir í þessari skýrslu séu tiltæk sem API-síða eða birt sem vefþjónusta.

  Frekari upplýsingar er að finna í [Birta gögn í gegnum API-síður eða OData-vefþjónustur](admin-powerbi-setup.md#exposedata).

- Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum skal fá eftirfarandi upplýsingar:

  - OData-vefslóð fyrir [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Yfirleitt er þessi vefslóð með sniðinu `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, til dæmis, `https://localhost:7048/BC190/ODataV4`. Ef um er að ræða virkjun með margleigjanda skal hafa leigjanda á vefslóðinni, til dæmis, `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Notandanafn og aðgangslykill vefþjónustu af [!INCLUDE[prod_short](includes/prod_short.md)] -reikningi.

    Til að sækja gögn úr [!INCLUDE[prod_short](includes/prod_short.md)] notar Power BI grunnsannvottun. Svo þarftu að fá notandanafn og aðgangslykil vefþjónustu til að tengjast. Reikningurinn gæti verið þinn eigin notandareikningur eða fyrirtækið kann að hafa sérstakan reikning í þeim tilgangi.

- Hlaða niður [!INCLUDE [prod_short](includes/prod_short.md)] skýrsluþema (valfrjálst).

  Frekari upplýsingar er að finna í [Nota [!INCLUDE [prod_short](includes/prod_short.md)] skýrsluþema](#theme) í þessari grein.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="a-namegetdataaadd-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop" /><a name="getdata"></a>Bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnaveitu í Power BI Desktop

Fyrsta verk í stofnun skýrslna er að bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnagjafa á Power BI Desktop. Þegar það er tengt er hægt að byrja að búa til skýrslu.

1. Ræsið Power BI Desktop.
2. Velja **Fá-gögn**.

    Ef þú sérð ekki **Sækja gögn** skaltu velja **Skrá** valmyndina og síðan **Sækja gögn**.
3. Á síðunni **Sækja gögn** skaltu velja **Netþjónusta**.
4. Gerið eitt af eftirfarandi skrefum í svæðinu **Netþjónusta**:

    - Til að tengjast [!INCLUDE [prod_short](includes/prod_short.md)] á netinu skal velja **Dynamics 365 Business Central** og síðan **Tengjast**.
    - Til að tengjast [!INCLUDE [prod_short](includes/prod_short.md)] á staðnum skal velja **Dynamics 365 Business Central (á staðnum)** og svo **Tengjast**.

5. Skráðu þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] (aðeins í eitt skipti).

    Ef þú hefur ekki skráð þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] úr Power BI skjáborðinu verður þú beðin(n) um að skrá þig inn.

    - Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu skal velja **Innskráning** og síðan velja réttan reikning. Notaðu sama reikning og þú skráir þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] með. Þegar því er lokið velur þú **Tengjast**.

    - Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á staðnum skal fyrst færa inn OData-vefslóðina fyrir [!INCLUDE[prod_short](includes/prod_short.md)] og síðan velja **Í lagi**. Síðan skal færa inn notandanafn og aðgangsorð reikningsins sem á að nota til að tengjast við [!INCLUDE[prod_short](includes/prod_short.md)] þegar beðið er um það. Færa skal inn aðgangslykil vefþjónustunnar í reitinn **Aðgangsorð**. Þegar því er lokið velur þú **Tengjast**.

    > [!NOTE]  
    > Þegar þú hefur tengst við [!INCLUDE[prod_short](includes/prod_short.md)] verð þú ekki beðinn aftur um að skrá þig inn. [Hvernig breyti ég eða hreinsa reikninginn sem ég nota núna til að tengjast Business Central frá Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Þegar þú hefur tengst, Power BI tengiliðir við Business Central-þjónustuna. Glugginn **Skoðun** birtist og sýnir tiltæka gagnagjafa til að búa til skýrslur. Veldu möppu til að stækka hana og sjá tiltæka gagnagjafa. 

   Þessi gagnagjafar standa fyrir allar vefþjónusturnar og API-síðurnar sem eru gefnar út fyrir [!INCLUDE [prod_short](includes/prod_short.md)]. Gagnagjöfunum er flokkað eftir umhverfum og fyrirtækjum Business Central. Með Business Central á netinu hefur **Skoðari** eftirfarandi skipulag:

    - **Heiti umhverfis**
      - **Nafn fyrirtækis**
        - **Ítarlegt API**

          Þessi mappa sýnir ítarlegar API-síður sem Microsoft gefur út, t.d. [API Business Central-sjálfvirkni](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) og [sérsniðnar API-síður fyrir Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Sérsniðnar API-síður eru ennfremur flokkaðar í möppur eftir eiginleikunum [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property) af upprunakóða API-síðunnar.

        - **Staðlað API v2.0**

          Þessi mappa sýnir API-síðurnar sem [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) birtir.

        - **Vefþjónustur \(eldra efni)**

          Þessi mappa sýnir síður, kóðaeiningar og fyrirspurnir sem eru gefna út sem vefþjónustur í Business Central.

    > [!NOTE]
    > Skipulagið fyrir Business Central á staðnum er öðruvísi vegna þess að það styður ekki API-síður.

7. Veldu gagnagjafana eða upprunastaðina sem þú vilt bæta við gagnalíkanið þitt og veldu svo hnappinn **Hlaða**.
8. Ef þú vilt síðar bæta við frekari gögnum Business Central er hægt að endurtaka fyrri skref.

Þegar gögnum hefur verið hlaðið er hægt að sjá þau á hægra yfirlitssvæði síðunnar. Þér tókst að tengjast gögnum þínum í [!INCLUDE[prod_short](includes/prod_short.md)] og getur byrjað að byggja upp Power BI-skýrsluna þína.  

> [!TIP]
> Frekari upplýsingar um notkun Power BI Desktop eru í [Hafist handa með Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports" />Stofnun aðgengisskýrslna

Mikilvægt er að gera skýrslurnar nothæfar fyrir eins marga og mögulegt er. Reynið að hanna skýrslur þannig að þær þurfi enga sérstaka aðlögun til að mæta sérþörfum mismunandi notenda. Gangið úr skugga um að hönnunin geri notendum kleift að nýta hefðbundin hjálpartækni á borð við skjálesara. Power BI inniheldur ýmsa aðgengiseiginleika, verkfæri og leiðbeiningar sem hjálpa þér að ná þessu markmiði. Frekari upplýsingar um [Power BI Hönnunarskýrslur um aðgengi](/power-bi/create-reports/desktop-accessibility-creating-reports) eru í Power BI skjölunum.

## <a name="creating-reports-to-display-data-associated-with-a-list" />Stofnun skýrslna til að birta gögn sem tengjast lista

Hægt er að búa til skýrslur sem birtast í upplýsingareit á [!INCLUDE [prod_short](includes/prod_short.md)]-listasíðu. Í skýrslunum má finna gögn um færslurnar sem eru valdar á listanum. Að búa til þessar skýrslur er svipað og í öðrum skýrslum, fyrir utan að það eru nokkrir hlutir sem þarf að gera til að ganga úr skugga um að skýrslurnar birtist eins og þær eiga að gera. Frekari upplýsingar er að finna í [´Búa Power BI skýrslur til að birta listagögn í [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="a-namethemeausing-the-include-prodshortincludesprodshortmd-report-theme-optional" /><a name="theme"></a>Notkun [!INCLUDE [prod_short](includes/prod_short.md)] skýrsluþema (valfrjálst)

Áður en þú býrð til skýrsluna mælum við með að þú sækir og flytjir inn [!INCLUDE [prod_short](includes/prod_short.md)] þemaskrána. Þemaskráin býr til litaspjald þannig að þú getir búið til skýrslur í sama litastíl og [!INCLUDE [prod_short](includes/prod_short.md)] forrit án þess að þurfa að skilgreina sérsniðna liti fyrir hvert myndefni.

> [!NOTE]
> Þetta verk er valfrjálst. Alltaf er hægt að stofna skýrslurnar og sækja síðan og nota stílsniðmátið síðar.

### <a name="download-the-theme" />Sækja þema

Þemaskráin er í boði sem json-skrá á Microsoft Power BI Community Themes Gallery. Til að hlaða niður þemaskránni skal gera eftirfarandi:

1. Farðu á [Microsoft Power BI Community Themes Gallery fyrir Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Veldu að hlaða niður viðhenginu **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report" />Flytja inn þemað í skýrslu

Þegar búið er að hlaða niður [!INCLUDE [prod_short](includes/prod_short.md)]-skýrsluþema er hægt að flytja það inn í skýrslur. Til að flytja inn þemað skal velja **Skoða** > **Þemu** > **Skoða fyrir þemað**. Frekari upplýsingar er að finna í [Power BI Desktop - Flytja inn sérstillt skýrsluþema](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports" />Birta skýrslur

Þegar búið er að stofna eða breyta skýrslu er hægt að birta skýrsluna í Power BI þjónustunni og einnig deila henni með öðrum í fyrirtækinu. Þegar þetta er birt muntu sjá skýrsluna í Power BI. Þessi skýrsla verður einnig tiltæk fyrir val í [!INCLUDE[prod_short](includes/prod_short.md)].

Til að birta skýrslu skal velja **Birta** á flipanum **Heim** á borðanum eða úr valmyndinni **Skrá** . Ef þú ert skráð (ur) inn á Power BI þjónustuna er skýrslan gefin út á þessari þjónustu. Annars ertu beðin(n) um að skrá þig inn. 

## <a name="distribute-or-share-a-report" />Dreifa eða deila skýrslu

Það eru nokkrar leiðir til að sækja skýrslur samstarfsstarfsmanna og annarra:

- Dreifa skýrslum sem .pbix-skrám.

    Skýrslur eru geymdar í tölvunni sem .pbix-skrár. Hægt er að dreifa þessari skýrslu sem .pbix-skrá til notenda, eins og hverri annarri skrá. Þá geta notendur hlaðið upp skránni á Power BI þjónustuna. Sjá [Hlaða upp skýrslum úr skrám](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Með því að dreifa skýrslum á þennan hátt eru gögn skýrslna uppfærð af hverjum notanda. Þessi staða gæti haft áhrif á [!INCLUDE[prod_short](includes/prod_short.md)] frammistöðu.

- Deila skýrslum úr Power BI þjónustu

    Ef um er að ræða Power BI Pro-leyfi er hægt að deila skýrslunni til annarra, beint úr Power BI-þjónustunni. Frekari upplýsingar er að finna á [Power BI - Deila stjórnborði eða skýrslu](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="fixing-problems" />Vandamál lagfærð

### <a name="cannot-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page" />Ekki er hægt að setja inn færslu. Núverandi tenging er „Ritvarinn“. villa við að tengjast sérsniðinni API-síðu

> **GILDIR UM:** Business Central Online

Frá og með febrúar 2022 munu nýjar skýrslur sem nota Business Central-gögn sjálfgefið tengjast ritvarinni eftirmynd af gagnagrunni Business Central. Í mjög sjaldgæfum tilfellum, eftir því hver síðuhönnunin er, færðu villu þegar þú reynir að tengjast og fá gögn af síðunni.

1. Ræsið Power BI Desktop.
2. Á borðanum skaltu velja **Sækja gögn** > **Netþjónusta**.
3. Á svæðinu **Netþjónusta** skaltu velja**Dynamics 365 Business Central** og síðan **Tengja**.
4. Í glugganum **Skoðari** skaltu velja API-endastöð sem þú vilt hlaða gögnum úr.
5. Á forskoðunarsvæðinu hægra megin sérðu eftirfarandi villu:

   *Dynamics365BusinessCentral: Beiðni mistókst: Fjartengdur þjónn skilaði villu: (400) Villa í beiðni. (Ekki er hægt að setja inn færslu. Núverandi tenging er ritvarin. CorrelationId: [...])".*

6. Veldu **Umbreyta gögnum** í staðinn fyrir **Hlaða** eins og myndir venjulega gera.
7. Í **Power Query ritill** skaltu velja **Ítarlegur ritill** af borðanum.
8. Í línunni sem hefst á **Uppruni =** skal skipta út eftirfarandi texta:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   með:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Velja **Ekkert**.
10. Veldu **Loka og nota** af borðanum til að vista breytingar og loka Power Query ritlinum.

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics--business-centralindex" />Sjá tengda [Microsoft þjálfun](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Sjá einnig

[Gera viðskiptagögn þín virk fyrir Power BI](admin-powerbi.md)  
[Viðskiptaupplýsingar](bi.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármál](finance.md)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
