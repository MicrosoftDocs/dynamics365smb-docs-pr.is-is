---
title: Skoða og breyta í Excel From Business Central
description: Lærðu hvernig hægt er að opna síðurnar í Microsoft Excel frá Business Central til að fá betri gagnagreiningar.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Skoða og breyta í Excel úr Business Central

Með síðum sem birta lista yfir færslur í línum og dálkum, eins og lista yfir viðskiptavini, sölupantanir eða reikninga, geturðu flutt út listannn í Microsoft Excel og skoðað hann þar. Þú hefur tvo valkosti til að skoða í Excel en það fer eftir síðunni. Báðir valkostirnir eru í boði undir tákninu **Deila** ![Deila síðu í öðru forriti.](media/share-icon.png) efst á síðu. Þú getur annaðhvort valið aðgerina **Opna í Excel** eða aðgerðina **Breyta í Excel** á síðunni. Í þessari grein eru aðgerðirnar tvær útskýrðar.

## Opna í Excel

Með aðgerðinni **Opna í Excel** er hægt að gera breytingar á færslum í Excel, en þú getur ekki birt þær aftur í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú getur aðeins vistað breytingarnar í Excel-skrá án þess að það hafi áhrif á gögn í [!INCLUDE[prod_short](includes/prod_short.md)].

- Með þessari aðgerð tekur Excel allar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar. Excel-vinnubókin mun innihalda sömu línur og dálka sem birtast á síðunni í [!INCLUDE[prod_short](includes/prod_short.md)].

- Þessi aðgerð virkar bæði í Windows og macOS.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

<!-- 
> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default. However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.-->

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> Í Excel hafa heilar tölur í dálkum tugatákn í lokin (eins og tímabil `.` eða kommu `,`) jafnvel þó að tugatáknið sé ekki sýnt í Business Central. Tugastafstáknið fer eftir svæðisstillingum tækisins. Í Business Central gæti til dæmis `10`  birst sem `10.` eða `10,` í Excel. Hægt er að breyta sniði í Excel með því að velja gildin og velja <kbd>síðan Ctrl</kbd>+<kbd>1</kbd>. Nánari upplýsingar um breytingar á númerasniði í Excel fást með því að fara [í Númer sniðs](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).

## Breyta í Excel

Aðgerðin **Breyta í Excel** er í boði í flestum listum en ekki öllum. Með aðgerðinni **Breyta í Excel** gerir þú breytingar á færslum í Excel og birtir síðan breytingarnar aftur í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar Excel opnast sérðu gluggann **Excel-innbót** hægra megin.

- Með þessari aðgerð tekur Excel flestar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar, þannig að Excel-vinnubókin innihaldi nánast sömu færslur og dálka.

- Til að fá nýjustu gögnin úr [!INCLUDE[prod_short](includes/prod_short.md)] skal velja **Uppfæra** í glugga Excel-innbótar.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### Fyrsta innskráning

Aðgerðin **Breyta í Excel** krefst þess að innbót Business Central sé uppsett í Excel. Í sumum tilvikum gæti kerfisstjórinn hafa sett upp innbótina til að setja sjálfkrafa upp fyrir þig. Í þessu tilviki þarftu bara að skrá þig inn í Business Central í glugga **Excel-innbótar** með notandanafni og lykilorði. Annars opnast glugginn **Ný Office-innbót**. Til að setja upp innbótina skal velja **Treysta þessari innbót** sem mun setja upp innbótina beint úr Office-versluninni.

Ef innbótin er ekki sett upp skal annaðhvort hafa samband við stjórnanda eða reyna að setja hana upp handvirkt. Frekari upplýsingar er að finna í [Setja upp innbótina handvirkt til eigin nota](admin-deploy-excel-addin.md#install).

### Vinna í öllum umhverfum og fyrirtækjum

Hægt er að skipta um fyrirtæki sem unnið er með. Til að skipta um fyrirtæki velur þú táknið **Valkostir** ![Valkostir Excel-innbótar.](media/cogwheel.png "Valkostir Excel-innbótar") í glugga Excel-innbótar skal síðan velja fyrirtækið í reitnum **Fyrirtæki**.  

> [!IMPORTANT]
> Þegar skipt er um fyrirtæki skal ganga úr skugga um að reiturinn **Umhverfi** sé ekki auður. Ef svo er skal stilla hann á einn af tiltækum valkostum, annars virkar innbótin ekki sem skyldi.  

Ef verið er að gera breytingar á innbótinni verður að endurhlaða hana til að uppfæra tenginguna. Til að endurhlaða skal nota valmyndina ![Excel-innbót](media/excel-addin-menu.png "Valkostir Excel-innbótar") efst í hægra horni innbótarinnar. Ef ekki er hægt að hlaða innbótinni skal tala við kerfisstjórann. Ef þú ert kerfisstjórinn skaltu skoða [Sækja innbót Business Central fyrir Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Innbótin virkar með Excel fyrir vefinn (á netinu) úr hvaða tæki sem er svo lengi sem þú notar viðurkenndan vafra. Hún virkar einnig með Excel-forritinu fyrir Windows (PC); en ekki fyrir macOS.
>
> Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er aðgerðin **Breyta í Excel** aðeins í boði ef stjórnandi hefur stillt Excel-innbótina og aðeins í boði fyrir vefbiðlara. Ef stjórnendur langar að fræðast betur um hvernig eigi að setja upp Excel-innbótina má finna upplýsingar um það í [Setja upp Excel-innbótina fyrir Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### Takmarkanir á notkun á Excel fyrir vefinn

Þegar **Breyta í Excel** er notað á listasíðum fyrir töflur með mörgum dálkum gæti vinnubókin verið með of marga dálka til að hægt sé að skoða skrána í Excel fyrir vefinn. [!INCLUDE[prod_short](includes/prod_short.md)] takmarkar sjálfkrafa útflutta vinnubók við 100 dálka þegar OneDrive er grunnstillt fyrir kerfiseiginleika. 

<!--## See the differences between the options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]-->

## Sjá einnig .

[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Vinna með Business Central](ui-work-product.md)  
[Endurbætur á Excel-samþættingu í 2019 útgáfu 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
