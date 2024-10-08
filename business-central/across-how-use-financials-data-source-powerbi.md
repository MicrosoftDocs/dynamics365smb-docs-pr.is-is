---
title: Byggingarskýrslur í Power BI Desktop til að birta Business Central data
description: Notandi getur gert gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 06/12/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="building-power-bi-reports-to-display--data"></a>Byggingarskýrslur Power BI til að birta [!INCLUDE [prod_long](includes/prod_long.md)] gögn

Þú getur gert gögnin þín [!INCLUDE[prod_long](includes/prod_long.md)] tiltæk sem gagnagjafa í Power BI Desktop og byggt upp öflugar skýrslur um stöðu fyrirtækisins.

Þessi grein lýsir því hvernig byrja skal að nota Power BI Desktop til að stofna skýrslur sem birta [!INCLUDE[prod_long](includes/prod_long.md)] gögn. Þegar búið er að stofna skýrslur er hægt að birta þær í Power BI þjónustunni eða deila þeim með öllum notendum í fyrirtækinu. Þegar skýrslurnar eru í þjónustunni Power BI geta notendur sem settir eru upp fyrir hana skoðað skýrslurnar í [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Vertu með allt á tæru

- Skráðu þig fyrir nýju Power BI þjónustuna.

  Ef þú ert ekki skráð(ur) farðu þá til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Þegar þú skráir þig skaltu nota vinnunetfang og aðgangsorð.

- Sækja [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop er ókeypis forrit sem þú setur upp á staðbundinni tölvu. Frekari upplýsingar er að finna í [Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Ganga skal úr skugga um að gögnin sem óskað er eftir í þessari skýrslu séu tiltæk sem API-síða eða birt sem vefþjónusta. Frekari upplýsingar er að finna í [Birta gögn í gegnum API-síður eða OData-vefþjónustur](admin-powerbi-setup.md#exposedata).

<!--- For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, get the following information:

  - The OData URL for [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Typically, this URL has the format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, for example, `https://localhost:7048/BC190/ODataV4`. If you have a multi-tenant deployment, include the tenant in the URL, for example, `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - A user name and web service access key of a [!INCLUDE[prod_short](includes/prod_short.md)] account.

    To get data from [!INCLUDE[prod_short](includes/prod_short.md)], Power BI uses basic authentication. So, you'll need a user name and web service access key to connect. The account might be your own user account, or your organization may have specific account for this purpose.-->

- Hlaða niður [!INCLUDE [prod_short](includes/prod_short.md)] skýrsluþema (valfrjálst).

  Frekari upplýsingar er að finna í [Nota [!INCLUDE [prod_short](includes/prod_short.md)] skýrsluþema](#theme) í þessari grein.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnaveitu í Power BI Desktop

Fyrsta verk í stofnun skýrslna er að bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnagjafa á Power BI Desktop. Þegar það er tengt er hægt að byrja að búa til skýrslu.

1. Ræsið Power BI Desktop.
2. Velja **Fá-gögn**.

    Ef þú sérð ekki **Sækja gögn** skaltu velja **Skrá** valmyndina og síðan **Sækja gögn**.
3. Á síðunni **Sækja gögn** skaltu velja **Netþjónusta**.
4. Gerið eitt af eftirfarandi skrefum í svæðinu **Netþjónusta**:

    - Til að tengjast [!INCLUDE [prod_short](includes/prod_short.md)] á netinu skal velja **Dynamics 365 Business Central** og síðan **Tengjast**.
    <!--- To connect to  [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, select **Dynamics 365 Business Central (on-premises)**, then **Connect**.-->

5. Skráðu þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] (aðeins í eitt skipti).

    Ef notandi er ekki skráður inn [!INCLUDE [prod_short](includes/prod_short.md)]  Power BI á skjáborðið birtist kvaðning um innskráningu.

    - Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu skal velja **Innskráning** og síðan velja réttan reikning. Notaðu sama reikning og þú skráir þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] með. Þegar því er lokið velur þú **Tengjast**.

    <!--- For [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, first enter the OData URL for [!INCLUDE[prod_short](includes/prod_short.md)], then select **OK**. When prompted, enter the user name and password of the account to use for connecting to [!INCLUDE[prod_short](includes/prod_short.md)]. In the **Password** box, enter the web service access key. When done, select **Connect**.-->

    > [!NOTE]  
    > Þegar tengst hefur verið við [!INCLUDE[prod_short](includes/prod_short.md)] birtist ekki kvaðning aftur um innskráningu. [Hvernig breyti ég eða hreinsa reikninginn sem ég nota núna til að tengjast Business Central frá Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Þegar tengst er tengiliðum Power BI  við þjónustuna [!INCLUDE [prod_short](includes/prod_short.md)] . Glugginn **Navigator** birtir gagnagjafa sem tiltækir eru til að byggja skýrslur. Velja möppu til að stækka hana og sýna tiltæka gagnagjafa.

   Þessar gagnaveitur standa fyrir allar vefþjónustur og API-síður sem birtar eru fyrir, flokkaðar eftir umhverfi og fyrirtækjum [!INCLUDE [prod_short](includes/prod_short.md)]. Með [!INCLUDE [prod_short](includes/prod_short.md)] online, **Navigator** hefur eftirfarandi skipulag:

    - **Heiti umhverfis**
      - **Nafn fyrirtækis**
        - **Ítarlegt API**

          Þessi mappa sýnir ítarlegar API-síður sem Microsoft gefur út, t.d. [API Business Central-sjálfvirkni](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) og [sérsniðnar API-síður fyrir Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Sérsniðnar API-síður eru flokkaðar frekar í möppur samkvæmt [eiginleikum APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property) í upprunakóta API-síðunnar.

        - **Staðlað API v2.0**

          Þessi mappa sýnir API-síðurnar sem [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) birtir.

        - **Vefþjónustur \(eldra efni)**

          Þessi mappa sýnir síður, kóðaeiningar og fyrirspurnir sem eru gefna út sem vefþjónustur í Business Central.

    <!--
    > [!NOTE]
    > The structure for Business Central on-premises is different because it doesn't support API pages.-->

7. Veldu gagnagjafana eða upprunastaðina sem þú vilt bæta við gagnalíkanið þitt og veldu svo hnappinn **Hlaða**.
8. Ef þú vilt síðar bæta við frekari gögnum Business Central er hægt að endurtaka fyrri skref.

Þegar gögnum hefur verið hlaðið er hægt að sjá þau á hægra yfirlitssvæði síðunnar. Þá tengist þú gögnunum þínum [!INCLUDE[prod_short](includes/prod_short.md)] og getur byrjað að byggja skýrsluna Power BI .  

> [!TIP]
> Frekari upplýsingar um notkun Power BI Desktop eru í [Hafist handa með Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports"></a>Stofnun aðgengisskýrslna

Mikilvægt er að gera skýrslurnar nothæfar fyrir eins marga og mögulegt er. Reynið að hanna skýrslur þannig að þær þurfi enga sérstaka aðlögun til að mæta sérþörfum mismunandi notenda. Gangið úr skugga um að hönnunin geri notendum kleift að nýta hefðbundin hjálpartækni á borð við skjálesara. Power BI inniheldur ýmsa aðgengiseiginleika, verkfæri og leiðbeiningar sem hjálpa þér að ná þessu markmiði. Frekari upplýsingar um [Power BI Hönnunarskýrslur um aðgengi](/power-bi/create-reports/desktop-accessibility-creating-reports) eru í Power BI skjölunum.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Stofnun skýrslna til að birta gögn sem tengjast lista

Hægt er að búa til skýrslur sem birtast í upplýsingareit á [!INCLUDE [prod_short](includes/prod_short.md)]-listasíðu. Í skýrslunum má finna gögn um færslurnar sem eru valdar á listanum. Stofnun þessara skýrslna svipar til annarra skýrslna, nema ýmislegt er hægt að gera til að tryggja að skýrslurnar birtist eins og væntanlegt er. Frekari upplýsingar er að finna í [´Búa Power BI skýrslur til að birta listagögn í [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the--report-theme-optional"></a><a name="theme"></a>Notkun [!INCLUDE [prod_short](includes/prod_short.md)] skýrsluþema (valfrjálst)

Áður en þú býrð til skýrsluna mælum við með að þú sækir og flytjir inn [!INCLUDE [prod_short](includes/prod_short.md)] þemaskrána. Þemaskráin býr til litaspjald þannig að þú getir búið til skýrslur í sama litastíl og [!INCLUDE [prod_short](includes/prod_short.md)] forrit án þess að þurfa að skilgreina sérsniðna liti fyrir hvert myndefni.

> [!NOTE]
> Þetta verk er valfrjálst. Alltaf er hægt að stofna skýrslurnar og sækja síðan og nota stílsniðmátið síðar.

### <a name="download-the-theme"></a>Sækja þema

Þemaskráin er í boði sem json-skrá á Microsoft Power BI Community Themes Gallery. Til að hlaða niður þemaskránni skal gera eftirfarandi:

1. Farðu á [Microsoft Power BI Community Themes Gallery fyrir Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Veldu að hlaða niður viðhenginu **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Flytja inn þemað í skýrslu

Þegar skýrsluþemað hefur [!INCLUDE [prod_short](includes/prod_short.md)] verið sótt er hægt að flytja það inn í skýrslurnar. Til að flytja inn þemað skal velja **Skoða** > **Þemu** > **Skoða fyrir þemað**. Frekari upplýsingar er að finna í [Power BI Desktop - Flytja inn sérstillt skýrsluþema](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Birta skýrslur

Þegar skýrsla hefur verið stofnuð eða henni breytt er hægt að birta skýrsluna til þjónustunnar Power BI og deila henni einnig með öðrum innan fyrirtækisins. Þegar skýrsla hefur verið gefin út er hún tiltæk í Power BI. Þessi skýrsla verður einnig tiltæk fyrir val í [!INCLUDE[prod_short](includes/prod_short.md)].

Til að birta skýrslu skal velja **Birta** á flipanum **Heim** á borðanum eða úr valmyndinni **Skrá** . Ef þú ert skráð (ur) inn á Power BI þjónustuna er skýrslan gefin út á þessari þjónustu. Annars ertu beðin(n) um að skrá þig inn. 

## <a name="distribute-or-share-a-report"></a>Dreifa eða deila skýrslu

Það eru nokkrar leiðir til að sækja skýrslur samstarfsstarfsmanna og annarra:

- Dreifa skýrslum sem .pbix-skrám.

    Skýrslur eru geymdar í tölvunni sem .pbix-skrár. Hægt er að dreifa þessari skýrslu sem .pbix-skrá til notenda, eins og hverri annarri skrá. Þá geta notendur hlaðið upp skránni á Power BI þjónustuna. Sjá [Hlaða inn skýrslum úr skrám](across-working-with-powerbi.md#upload).

    > [!NOTE]
    > Með því að dreifa skýrslum á þennan hátt eru gögn skýrslna uppfærð af hverjum notanda. Þessi staða gæti haft áhrif á [!INCLUDE[prod_short](includes/prod_short.md)] frammistöðu.

- Deila skýrslum úr Power BI þjónustu

    Ef um er að ræða Power BI Pro-leyfi er hægt að deila skýrslunni til annarra, beint úr Power BI-þjónustunni. Frekari upplýsingar er að finna á [Power BI - Deila stjórnborði eða skýrslu](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="how-to-develop-cross-company-or-cross-environment-power-bi-reports"></a>Hvernig á að þróa skýrslur milli fyrirtækja eða þvert á umhverfi Power BI

API-endastöðvarnar [!INCLUDE[prod_short](includes/prod_short.md)] hafa allir forskeytið `https://api.businesscentral.dynamics.com/v2.0/<environment_name>/api/v2.0` fylgt (`/companies({company_id})/accounts({id})` hér notum `accounts` við API sem myndskýringu). Hægt er að nota þessa uppbyggingu til að stofna PowerQuery fyrirspurnir sem hlaða gögnum fyrir mörg fyrirtæki eða mörg umhverfi ef notandinn sem les gögnin hefur aðgang að þeim.

Til að setja upp fyrirspurn til að hlaða inn gögnum fyrir mörg fyrirtæki skal fylgja eftirfarandi skrefum:

1. Taka PowerQuery fyrirspurnina sem hleður inn gögnum fyrir eitt fyrirtæki. Breyta því í sérsniðna Power Query aðgerð sem tekur fyrirtækiskennið (eða umhverfisheitið) sem færibreytur. Nánari upplýsingar eru notaðar með því að [fara í Notkun sérsniðinna Power Query aðgerða](/power-query/custom-function).
1. Nú skal nota nýju sérsniðnu aðgerðina í PowerQuery fyrirspurn þar sem aðgerðinni er varpað yfir lista yfir fyrirtæki og svo eru gagnasöfnin sameinuð með aðgerðinni [Table.Combine](/powerquery-m/table-combine) Power Query .

## <a name="fixing-problems"></a>Vandamál lagfærð

### <a name="cant-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page"></a>"Ég get ekki sett inn færslu. Núverandi tenging er „Ritvarinn“. villa við að tengjast sérsniðinni API-síðu

> **GILDIR UM:** Business Central Online

Í febrúar 2022 hefjast nýjar skýrslur sem nota [!INCLUDE [prod_short](includes/prod_short.md)] sjálfgefið gagnatengingu við ritvarið eftirlíkingu gagnagrunnsins [!INCLUDE [prod_short](includes/prod_short.md)] . Í sjaldgæfum tilvikum gæti komið upp villa eftir síðuhönnun þegar reynt er að tengjast og sækja gögn af síðunni.

1. Ræsið Power BI Desktop.
2. Á borðanum skaltu velja **Sækja gögn** > **Netþjónusta**.
3. Á svæðinu **Netþjónusta** skaltu velja**Dynamics 365 Business Central** og síðan **Tengja**.
4. Í glugganum **Skoðari** skaltu velja API-endastöð sem þú vilt hlaða gögnum úr.
5. Forskoðunarsvæðið sýnir eftirfarandi villu:

   *Dynamics365BusinessCentral: Beiðni mistókst: Fjarþjónninn skilaði villu: (400) Slæm beiðni. (Ekki er hægt að setja inn færslu. Núgildandi ásetningur tengingar er ritvarinn. CorrelationId: [...])".*

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

## <a name="see-also"></a>Sjá einnig

[Virkjun viðskiptagagna fyrir Power BI](admin-powerbi-setup.md)  
[Viðskiptaupplýsingar](bi.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármál](finance.md)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
