---
title: Birta sérsniðnar Power BI skýrslur
description: Hægt er að nota Power BI upplýsingareit til að sýna Power BI skýrslur og öðlast betri innsýn í færslugögn í mikilvægum listum.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 12/13/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-"></a>Að búa til Power BI skýrslur til að sýna listagögn í [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] inniheldur stjórneiningu Power BI upplýsingareits á mörgum mikilvægum listasíðum. Tilgangurinn með þessum upplýsingareit er að sýna Power BI-skýrslur sem tengjast færslum í listunum sem veita betri innsýn í gögnin. Hugmyndin er að þegar farið er milli lína í listanum uppfærist skýrslan uppfærð fyrir valda færslu.

[!INCLUDE[prod_long](includes/prod_long.md)] kemur tilbúið með sumum þessara skýrslna. Einnig er hægt að búa til eigin sérsniðnar skýrslur sem birtast í þessum upplýsingareit. Þessar skýrslur eru búnar til að svipaðan hátt og aðrar skýrslur. En það eru nokkrar hönnunarreglur sem þú þarft að fylgja til að tryggja að skýrslurnar birtast eins og búist var við. Þessar reglur eru útskýrðar í þessari grein.

> [!NOTE]
> Fyrir almennar upplýsingar um stofnun og birtingu Power BI-skýrslna fyrir Business Central er að finna í [Myndun Power BI-skýrslna til að birta [!INCLUDE [prod_long](includes/prod_long.md)] gögn](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Frumskilyrði

- Power BI-Reikningur.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Use [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a>Búa til skýrslu fyrir listasíðu

1. Ræsið Power BI Desktop.
2. Veljið **Sækja gögn** og veljið gagnagjafann fyrir skýrsluna.

    Tilgreinið listasíður Business Central sem innihalda gögnin sem eiga að koma fram í skýrslunni. Til að stofna til dæmis skýrslu fyrir listann **Sölureikningar** skal taka með síður sem tengjast sölu.

    Til að fá frekari upplýsingar skal fylgja leiðbeiningunum [Bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnagjafa í Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).

3. Stillið afmörkun skýrslunnar.

    Til að gera gagnauppfærslu í valinni færslu á listanum er síu bætt við skýrslu. Sían verður að innihalda reit gagnagjafans sem er notaður til að auðkenna sérstaklega hverja færslu í listanum. Hjá þróunaraðila er þessi reitur *aðallykillinn*. Í flestum tilvikum er aðallykill fyrir lista reiturinn **Nr.** .

    Til að stilla síuna skal gera eftirfarandi:

    1. Í **Síunum** skal velja reit aðallykilsins úr listanum yfir tiltæka reiti.
    2. Dragið reitinn yfir á svæðið **Síur** og sleppið honum í reitinn **Síur á öllum síðum**.
    3. Stillið **Síugerðina** á **Grunnsíun**. Það getur ekki verið síða, sjónrænt eða ítarleg sía.

    ![Afmörkun skýrslu stillt fyrir aðgerðaskráningu sölureikninga.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Hannið útlit skýrslunnar.

    Búið til útlitið með því að draga til reiti og bæta við myndrænum framsetningum. Frekari upplýsingar er að finna í [Vinna með skýrsluyfirlit í Power BI Desktop](/power-bi/create-reports/desktop-report-view) í Power BI-fylgigögnum.

5. Skoðið næstu hluta um hvernig skuli stilla stærð skýrslunnar og nota margar síður.

6. Vistið og gefið skýrslunni heiti.

    Gefa skal skýrslunni heiti sem inniheldur heiti listasíðunnar sem tengist skýrslunni, eins og í biðlaranum. Ekki skiptir hins vegar máli hvort nafnið er skráð með há- eða lágstöfum. Segjum að skýrslan sé fyrir listasíðuna **Sölureikningar**. Í þessu tilviki skal setja orðin **sölureikningar** einhversstaðar í nafnið, eins og **solureikningarnir_minir.pbix** eða **minir_solureikningar.pbix**.

    Þessi nafnavenja er ekki skilyrði. Hins vegar gerir það val á skýrslum í [!INCLUDE[prod_short](includes/prod_short.md)] fljótlegri. Þegar skýrsluvalssíða opnast af listasíðu er hún síuð sjálfkrafa út frá síðuheitinu. Sían er með málskipanina: `@*<caption>*`, eins og `@*Sales Invoices*`. Þessi sía er búin til að takmarka skýrslurnar sem eru birtar. Einnig er hægt að fjarlægja afmörkunina til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.

7. Þegar þessu er lokið skal birta skýrsluna eins og venjulega.

    Frekari upplýsingar er að finna í [Birta skýrslu](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Prófið skýrsluna.

    Þegar skýrslurnar hafa verið birtar á vinnusvæðinu ættu þær að vera aðgengilegar í Power BI-upplýsingareitnum á listasíðunni í [!INCLUDE[prod_short](includes/prod_short.md)].

    Til að prófa hann skal fara í gegnum eftirfarandi skref.

    1. Opnaðu [!INCLUDE[prod_short](includes/prod_short.md)] og farðu á listasíðuna.
    2. Ef Power BI-upplýsingareiturinn sést ekki skal fara á aðgerðarstikuna, síðan velja **Aðgerðir** > **Birta** > **Sýna/fela Power BI skýrslur**.
    3. Í Power BI-upplýsingareitnum skal velja **Velja skýrslur**, velja reitinn **Virkja** fyrir skýrsluna, síðan velja **Í lagi**.

    Skýrslan birtist ef þetta er hannað á réttan hátt.  

## <a name="set-the-report-size-and-color"></a>Stilla stærð og lit skýrslunnar

Stærð skýrslu verður að stilla á 325 sinnum 310 pixla. Þessi stærð býður upp á rétta kvörðun á skýrslu í tiltæku bili í Power BI stjórnun upplýsingareits í [!INCLUDE[prod_short](includes/prod_short.md)]. Til að skilgreina stærð skýrslu skal staðsetja fókus utan svæðis fyrir útlit skýrslu og velja svo tákn fyrir málningarrúllu.

![Breidd og hæð skýrslu stillt fyrir Aðgerðaskráningu sölureikninga.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Hægt er að breyta breidd og hæð skýrslunnar með því að velja **Sérsníða** í reitnum **Tegund**.

Ef bakgrunnur skýringarinnar á að vera með bakgrunnslit Power BI upplýsingareitsins skal stilla bakgrunnslit skýrslu á *#FFFFFF* (hvítur). 

> [!TIP]
> Notið [!INCLUDE [prod_short](includes/prod_short.md)]-þemaskrá til að búa til skýrslur með sama litastíl og [!INCLUDE [prod_short](includes/prod_short.md)]-forritin. Frekari upplýsingar er að finna í [Nota [!INCLUDE [prod_short](includes/prod_short.md)] skýrsluþema notað](across-how-use-financials-data-source-powerbi.md#theme).

## <a name="reports-with-multiple-pages"></a>Skýrslur með mörgum síðum

Með Power BI er hægt að stofna eina skýrslu með mörgum síðum. Hins vegar, fyrir skýrslur sem birtast með listasíðum, mælum við með að þær hafi ekki fleiri en eina síðu. The Power BI FactBox sýnir aðeins fyrstu síðu skýrslunnar þinnar.

## <a name="fixing-problems"></a>Vandamál lagfærð

Í þessum hluta er útskýrt hvernig á að laga vandamál sem gætu komið upp þegar reynt er að skoða Power BI skýrslu fyrir listasíðu í [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a>Ekki er hægt að sjá Power BI-upplýsingareitinn á listasíðu

Sjálfgefið er að Power BI-upplýsingareiturinn sé falinn. Til að sýna upplýsingareitinn á síðu skal á aðgerðastikunni velja **Aðgerðir** > **Birta** > **Sýna/fela Power BI-skýrslur**.

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a>Ekki er hægt að sjá skýrsluna á svæðinu Velja skýrslu

Heiti skýrslunnar inniheldur ekki heiti listasíðunnar sem er sýnd. Hreinsaðu síuna til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Verið er að hlaða skrá en hún er tóm, ekki síuð eða síuð á rangan hátt

Staðfestu að skýrslusían innihaldi réttan aðallykil. Yfirleitt er þessi reitur **Nr.** reitur, en í töflunni **Fjárhagsfærsla**, til dæmis, verður að nota **Færslunr.** reitinn.

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Skýrslu er hlaðið inn, en hún sýnir síðu sem þú bjóst ekki við

Sannprófa verður að skýrslan sem notandi vill að birtist sé fyrsta síðan í skýrslunni.  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Skýrsla birtist með óæskilegum gráum ramma eða hún er of lítill eða of stór

Staðfestið að stærð skýrslu sé stillt á 325 x 310 pixla. Vista skal skýrsluna og síðan endurnýja listasíðuna.  

## <a name="see-also"></a>Sjá einnig .

[Gera viðskiptagögn þín virk fyrir Power BI](admin-powerbi.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármál](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
