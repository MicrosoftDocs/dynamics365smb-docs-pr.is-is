---
title: Greina gögn í listum með hjálp frá Copilot (forskoðun)
description: Læra að nota Copilot í Business central til að greina gögn.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/14/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-data-in-lists-with-help-from-copilot-preview"></a>Greina gögn í listum með hjálp frá Copilot (forskoðun)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Þessi grein útskýrir hvernig á að nota *greiningaraðstoðina* til að aðstoða við greiningu gagna á listasíðum.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-analysis-assist"></a>Um greiningaraðstoð

Greiningaraðstoð er Copilot fyrir [greiningarhaminn](analysis-mode.md) á listasíðum í Business Central. Greiningarstillingin býður upp á gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Til að greina gögn í greiningarstillingunni er búinn *til greiningarflipi* þar sem gögnum er umbreytt til að birta uppsöfnun og samantektir. Til dæmis er reitum raðað í línum og dálkum, afmarkanir tilgreindar, raðað dálkum og velt á reitum. Með greiningaraðstoð, í stað þess að gera þetta verk handvirkt, verður mikið af sama&mdash; eða minnsta byrjun&mdash; með því að nota orð. Með því að tjá uppbygginguna sem óskað er eftir á náttúrumáli, eins og "raða eftir magni frá minnstu til stærstu" eða "sýna meðalinnkaupsverð á hvern flokk", notar greiningaraðstoðin ÓM til að búa til tillöguútlit á greiningarflipa.


<!-- 

 However, the data analysis mode requires some understanding of how to structure fields to meet the desired aggregations and summarizations. It requires you to move fields around to the appropriate areas within analysis mode pane which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals. Analysis assist minimizes these requirments by enabling you to express the desired layout in words. , like "group which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals
--> 
## <a name="prerequisites"></a>Frumskilyrði

- Greiningaraðstoð er virk og notandi hefur heimild til að nota hana. Stjórnandi framkvæmir yfirleitt þennan verkhluta. [Fræðast meira um grunnstillingu stjórnunargetu og afkastagetu](enable-ai.md) Stjórnunargetu.
- Birtingartungumálið í Business Central er stillt á eitt af eftirfarandi enskum heimamönnum: en-AU, en-CA, en-GB, en-IE, en-Í-NZ, en-PH, en-SG, en-US, en-ZA. [Fræðast meira um að breyta tungumálinu](ui-change-basic-settings.md#language).
- Business Central umhverfið þitt er í neinu landi/svæði nema Kanada (þessi eiginleiki er ekki enn tiltækur í Kanada).

<!--
> [!NOTE]
> You may notice some list pages that don't include the **Analyze** switch for changing to the analysis mode. The reason is that developers can disable analysis mode on specific pages by using the [AnalysisModeEnabled property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) in AL.-->

## <a name="get-started"></a>Hefjast handa

1. Opna skal listasíðuna sem á að greina.

   Til dæmis, til að vinna með **síðuna Vörur** skal velja ![stækkunarglerið sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png) Táknmynd (<kbd>Alt</kbd>+<kbd>Q</kbd>), slá inn *vörur* og velja síðan viðeigandi tengil.

1. Hægt er að byrja að greina gögn með Copilot beint af listasíðunni eða með því að færa greiningarhaminn fyrst inn. Hafist er handa með því að gera eitt af eftirfarandi skrefum:

    - Í aðgerðaslánni efst á síðunni skal velja ![Sýnir copilot táknið](media/copilot-icon.png) **Copilot** > **Analyze listann**.
    - Á aðgerðaslánni efst á síðunni skal velja ![Sýna táknið](media/analysis-mode-icon.png) **Færa inn greiningarham** og velja ![síðan Sýna copilot táknið](media/copilot-icon.png) **Copilot** > **Create nýja greiningu**.

1.  **Í glugganum Greining** með Copilot er færð inn lýsing á útlitinu sem óskað er eftir. Lýsingin er þekkt sem *kvaðning*.

    ![Sýnir greiningaraðstoðina Afrita](media/analysis-assist.png)

    > [!TIP]
    > Til að fá hjálp við að skrifa kvaðningu skal velja ![Sýna leiðbeiningar](media/prompt-guide-icon.png) **um kvaðningu** og velja einn af kostunum til að hefjast handa. Textinn í sniðum `[ ]` er aðeins sýndur sem dæmi og er ekki innifalinn í glugganum Copilot.

1. Veljið **Búa til** og bíðið á meðan Copilot býr til uppsetninguna á nýjum greiningarflipa.
1. Niðurstöðurnar eru skoðaðar á nýja greiningarflipanum.

   > [!NOTE]
   > Ef flett er burt frá nýja greiningarflipanum (eins og að fara á annan flipa eða síðu) eða gera breytingar á útliti á flipanum (svo sem röðunardálkar eða breytingar á stillingum í **flipunum Dálkar** og **Greiningarafmarkanir**) er nýi greiningarflipinn sjálfkrafa vistaður og Copilot lokast sjálfkrafa.

1. Ef breyta á myndaðri greiningu er hægt að gera eitt af skrefunum:

   - Til að byggja á fyrri leiðbeiningum skal færa upplýsingarnar inn í reitinn **Bæta við nánari upplýsingum um greiningarreitinn** og velja ![síðan Sýna leiðréttu örina](media/analysis-assist-adjust-button.png) **Leiðrétta** ör. Copilot man eftir fyrri leiðbeiningum og notar þær til að gera leiðréttingar.

   - Til að byrja frá grunni með því að bæta við nýjum leiðbeiningum skal velja ![Sýna kvaðningartáknið](media/edit-pencil.png) **Breyta kvaðningu:**, bæta upplýsingum við kvaðninguna og velja **síðan Mynda**.

1. Ef vista á greiningarflipann er hann **valinn**. Ef ekki á að vista það skal velja **Fleygja**.

## <a name="prompt-tips-and-examples"></a>Hvetja ráðleggingar og dæmi

Nauðsynlegt er að búa til skilvirkar kvaðningar fyrir Copilot til að fá nákvæmar og viðeigandi greiningartillögur. Einnig eru leiðir til að draga úr texta sem bætt er við með kvaðningum til að hraðar verði slegið inn þegar það er slegið inn. Hér eru nokkrar ábendingar og leiðbeiningar sem fylgt er í nokkrum dæmum:

- Vertu nákvæmur og forðastu langar setningar eða margar setningar.
- Ganga þarf úr skugga um að reitaheiti sem notuð eru í kvaðningum séu nokkuð nálægt raunverulegum reitaheitum á síðunni.
- Nota náttúrulegt tungumál, tjá gagnabyggingu sem óskað er eftir á vingjarnlegan og samræðulegan hátt.
- Nota algeng leitarorð, orðasamband og hugtök sem notuð eru við greiningu gagna, eins `group by` og, `sum` `sort by`, o.s.frv.
- Ef upphafssvarið er ekki það sem óskað er eftir skal bæta við leiðbeiningum um eftirfylgni eða endurorða síðustu leiðbeiningar.
- Algengar skammstafanir eru viðunandi.
- Bréfmálið skiptir ekki máli.

### <a name="examples"></a>Dæmi

Eftirfarandi kvaðningardæmi nota greiningaraðstoð við **vörulistann** . Á vörusíðunni eru þrír samanteknir reitir fyrir greiningu: **Tiltækt magn,Kostn.verð,Ein.verð** **·** **·**.

Hvetja: `Show items by brand and unit of measure`

Þessi kvaðning reynir að sýna samtölur allra samantekinna reita, flokkaðar eftir vörumerkjum og **grunnmælieiningu** . En í þessu tilfelli passar "vörumerki" ekki við neitt reitarheiti, þannig að Copilot finnur líklega ekki samsvarandi reit svo að hann biður þig að endurorða kvaðninguna og reyna aftur.

Hvetja: `Show items by type and uom`

Þessi kvaðning sýnir samtölur allra samantekinna reita, flokkaðar eftir reitunum **Tegund** og **Grunnmælieining** . En í stað þess að skrifa út "mælieiningu", er skammstöfunin `uom` notuð.

Hvetja: `Show total quantity per type per UoM`

Þessi kvaðning býr til veltitöflu í reitnum Tiltækt magn á grunnmælieiningu **á** tegund **·** . **·**

## <a name="see-also"></a>Sjá einnig .

[Ábyrg algengar spurningar fyrir greiningaraðstoð](faqs-analysis-assist.md)  
[Greining á tilfalöngum gögnum](reports-adhoc-analysis.md)  