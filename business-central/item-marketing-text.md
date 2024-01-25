---
title: Bættu markaðstexta við hluti
description: Skrifaðu markaðstexta fyrir hluti í Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 12/13/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# Bættu markaðstexta við hluti

Fyrir hvaða hlut sem er skráður í Business Central geturðu skrifað *markaðstexta* um hlutinn. Þó að markaðstexti sé eins konar lýsing er hann öðruvísi en  **Lýsing** reit hlutarins. Reiturinn **Lýsing**  er venjulega notaður sem hnitmiðað nafn til að auðkenna vöruna fljótt. Markaðstextinn er hins vegar ríkari og lýsandi texti. Tilgangur þess er að bæta við markaðs- og kynningarefni, einnig þekkt sem *copy*. Þennan texta er síðan hægt að birta með hlutnum ef hann er birtur á vefverslun, eins og Shopify, eða límdur í tölvupóst eða önnur samskipti við viðskiptavini þína.

Það eru tvær leiðir til að búa til markaðstextann. Auðveldasta leiðin til að byrja er að nota Copilot, sem stingur upp á gervigreindum texta fyrir þig. Hin leiðin er að byrja frá grunni. 

## <a name=copilot></a> Fáðu tillögur um markaðstexta með Copilot

Með Copilot færðu fljótt textatillögu sem er sjálfkrafa búin til fyrir þig. AI-myndaður texti er sniðinn að hlutnum og gefur góðan upphafspunkt. Textinn er að hluta til byggður á eftirfarandi upplýsingum:

- Eiginleikar sem eru skilgreindir fyrir hlutinn&mdash; til dæmis lýsingin, liturinn, mál, efni og svo framvegis. [Frekari upplýsingar um eiginleika vöru](inventory-how-work-item-attributes.md).
-  **Lýsing** reitur hlutarins.
- Vöruflokkurinn. [Frekari upplýsingar um að flokka hluti](inventory-how-categorize-items.md).
- Valanlegar stílstillingar eins og raddblær, snið og lengd.

Copilot er hannað til að spara þér tíma og hjálpa þér að skrifa skapandi og grípandi texta sem endurspeglar vörumerkið þitt og er í samræmi í vörulínunni þinni. Byrjaðu á því að búa til tillögu og breyttu síðan textatillögunni eftir þörfum.

### Frumskilyrði

- Eiginleiki markaðstextatillögur er virkur og virkur í umhverfi þínu. Þetta verkefni er venjulega gert af stjórnanda. Fyrir frekari upplýsingar, farðu í [Stilling Copilot og AI getu](enable-ai.md).
- Þú ert að nota eitt af tungumálunum sem eru studdar af markaðstextatillögunum.

  [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Til að breyta tungumálinu skaltu velja **Stillingar** táknið ![Stillingar í efra hægra horninu.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") > **Stillingar mínar** > **Tungumál**. Fyrir frekari upplýsingar, farðu í [Breyta grunnstillingum](ui-change-basic-settings.md#language).
- Skoðaðu [algengar spurningar fyrir tillögur um markaðstexta](faqs-marketing-text.md) til að læra hvernig gervigreind er beitt.

### Búðu til fyrstu drög með Copilot

Ljúktu við eftirfarandi skref til að bæta markaðstexta við fyrirliggjandi hlut. Til að læra hvernig á að búa til nýjan hlut skaltu fara á [Skráðu nýja hluti](inventory-how-register-new-items.md).

1. Í Business Central, opnaðu hlutinn sem þú vilt breyta með því að ljúka eftirfarandi skrefum:

   - Í efra hægra horninu skaltu velja ![peruna sem opnar Segðu mér eiginleikann 22.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Items** og veldu síðan tengda tengilinn til að sýna lista yfir tiltæka hluti.

   - Tvísmelltu á hlutinn eða veldu gildi þess í **No.** dálki.

   [![Sýnir vöruspjald með markaðstexta glugganum](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

2. Frá vöruspjaldinu eru tvær leiðir til að byrja að skrifa markaðstexta með Copilot. Framkvæmdu eitt af eftirfarandi skrefum:

   - Í **Markaðstexta** rúðunni í staðreyndaboxinu hægra megin á síðunni skaltu velja **Draft with Copilot**. 
   
     Copilot byrjar að semja markaðstextann. 

   - Efst á síðunni velurðu **Markaðstexta** aðgerðina, veldu síðan **Draft with Copilot** á **Breyta markaðstexta** glugganum.   **Draft Marketing Text with Copilot** gluggarnir birtast og listar upp allar tiltækar eiginleikar fyrir hlutinn.
   
     ![Sýnir textabreytingargluggann](media/marketing-text-copilot-attributes.svg)

     Veldu eiginleikana sem þú vilt að Copilot base tillögur um, veldu síðan **Búa til**. Þú getur breytt völdum eiginleikum og öðrum valkostum síðar. Copilot byrjar að semja markaðstextann. 
     
3. Þegar Copilot klárar uppkastið birtist textinn í Copilot ritstjóraglugganum sem þú getur skoðað og breytt. 

   [![Sýnir búa til með Copilot gluggum](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Þú getur nú fengið fleiri tillögur, reynt að bæta tillögurnar sem þú færð, breytt texta og fleira. Farðu í [Skoðaðu, breyttu og vistaðu](#review-edit-and-save-text) til að fá frekari upplýsingar.


### Skoðaðu, breyttu og vistaðu texta

Þegar þú hefur fyrstu drögin verður þú að fara yfir þau og gera breytingar á textanum til að gera hann tilbúinn til birtingar. Þessi vinna er unnin úr Copilot ritlinum, sem gerir þér kleift að fá fleiri tillögur, breyta kjörstillingum til að hafa áhrif á tillögurnar og gera breytingar handvirkt og stíla textann.

> [!IMPORTANT]
> AI-myndaður texti frá Copilot er aðeins tillaga og það getur verið mistök. Það krefst mannlegrar eftirlits og endurskoðunar til að tryggja að það sé rétt og viðeigandi. Farðu yfir hvaða textatillögu sem er og breyttu eftir þörfum áður en þú vistar hann og birtir hann til almenningsneyslu.

Notaðu eftirfarandi leiðbeiningar til að ganga frá og vista markaðstextann.

1. Gerðu breytingar á texta beint í textareitnum. Notaðu tækjastikuna neðst í reitnum til að forsníða og stíla texta, bæta við tenglum og fleira.
2. Til að fá nýja tillögu skaltu velja **Regenerate**.
3. Ef þú ert ekki ánægður með tillögurnar skaltu bæta textatillögurnar með því að nota **Tónn**, **Snið**, og **Áherslur**  valmöguleikar.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   Til að fá leiðbeiningar um að bæta tillögur, farðu í [Bæta og sníða textatillögur](#improve-and-tailor-text-suggestions).

4. Til að fara fram og til baka í gegnum tillögur, notaðu fyrri og næstu hlekk efst á síðunni (*x* **af** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Skoðaðu textann vandlega með tilliti til nákvæmni og viðeigandi:

   - Ef þú vilt vista textann skaltu velja **Halda honum**. 
   - Ef þú vilt ekki vista skaltu velja fleygjahnappinn (ruslatunna) ![Sýnir ruslatunnutáknið til að eyða öllum Copilot tillögunum um afstemmingu bankareiknings](media/copilot-delete-trash-can.png).

### Bæta og sérsníða textatillögur

Það eru nokkur skref sem þú getur gert til að bæta textatillögurnar og fínstilla þær til að henta persónulegum óskum þínum eða fyrirtækis.

1. Breyttu eiginleikum vörunnar sem Copilot notar.

   Tillögur aðstoðarflugmanns eru að hluta til byggðar á eiginleikum sem hlutnum er úthlutað. Til að skoða tiltæka eiginleika og núverandi stillingar skaltu velja edit ![Sýnir edit táknið á Copilot glugganum til að breyta eiginleikum](media/edit-pencil.png) tákninu í efra vinstra horninu. Á síðunni **Eiginleikar vöru**  skaltu velja þá eiginleika sem passa best við þá eiginleika sem þú vilt kynna. Því meira viðeigandi eiginleika sem þú tekur með, því ríkari verður útkoman. Ef þér finnst vanta nokkra lykileiginleika skaltu bæta við fleiri. Fyrir frekari upplýsingar um eiginleika, farðu í [Vinna með eiginleika vöru](inventory-how-work-item-attributes.md)
1. Breyttu stillingum þínum fyrir  **Tón**, **Format** og **Áhersla** valkostir.

   |Valkostur|Heimildasamstæða|
   |-|-|
   |Tónn |Notaðu þennan valmöguleika til að hafa áhrif á hvers konar orð, orðasambönd og greinarmerki eru notuð til að ná til markhópsins. Þú getur valið úr nokkrum fyrirfram skilgreindum raddstónum, allt frá **Formlegu** (sem leiðir af sér viðskiptatón) til **Creative** (sem leiðir af sér óformlegan tón). |
   |Snið og lengd|Notaðu þennan valmöguleika til að stjórna almennri uppbyggingu textans, sem samanstendur af þremur hlutum sem falla undir fjóra mismunandi valkosti: <ul><li>**Tagline** - Grípandi setning eða stutt setning sem auðkennir hlutinn eða vörumerkið.</li><li>**Málsgrein** - Ein málsgrein með reiprennandi og margorðum texta, sem samanstendur af nokkrum heilum setningum.</li><li>**Merki + málsgrein** - Merkiorð á eftir með málsgrein</li><li>**Stutt** - Inngangssetning, líkt og tagline, fylgt eftir með punktalista yfir helstu áhugaverða staði.</li></ul> |
   |Áhersla|Notaðu þennan valkost til að velja úr lista yfir fyrirfram skilgreinda eiginleika sem þú vilt leggja áherslu á í textanum. Veldu gæði sem passar best við tegund hlutarins sem þú ert að skrifa um. Eiginleikarnir samsvara ekki eiginleikum, lýsingu eða flokki hlutarins beint. Til dæmis gæti **Gæði**  verið góður kostur fyrir bæði hjól eða skrifborð, en **Hraði** myndi henta hjóli, en ekki skrifborð.|

1. Bættu **Lýsing** reitinn á vöruspjaldinu.

   Textinn í reitnum **Lýsing** er notaður eins og hann er á mörgum stöðum í textatillögunni, svo það er mikilvægt að lýsingin sýni sem best hvernig þú vilt að hluturinn sé vísað til í markaðssetningunni. texti. 

1. Gakktu úr skugga um að **Vöruflokkakóði** reiturinn á vöruspjaldinu sé stilltur á réttan flokk.

   Copilot finnur orð og orðasambönd sem tengjast flokknum og vinnur þau inn í textatillöguna.

### Að vinna með mörg tungumál 

Texti er alltaf búinn til á því tungumáli sem er skilgreint af  [stillingum notanda](ui-change-basic-settings.md#language). Ef fyrirtækið þitt starfar og setur gögn inn í Business Central á öðru tungumáli, eða ef Business Central er tengt við netverslunina þína eins og með Shopify gæti það leitt til birtingar efnis sem passar ekki við svipað markaðsefni.

## Búðu til texta frá grunni

1. Í Business Central, opnaðu hlutinn sem þú vilt breyta á eftirfarandi hátt:

    1. Í efra hægra horninu skaltu velja ![peruna sem opnar Segðu mér eiginleikann 22.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Items** og veldu síðan tengda tengilinn til að sýna lista yfir tiltæka hluti.
    2. Til að opna hlutinn skaltu tvísmella á hann eða velja númer hans í   **No.** .

2. Framkvæmdu eitt af eftirfarandi skrefum:

   - Í **Markaðstexta** rúðunni í staðreyndaboxinu hægra megin á síðunni skaltu velja **Breyta**.
   - Veldu aðgerðina **Markaðstexti** .
3. Gerðu breytingar á texta beint í **Markaðstexta** reitnum. Notaðu tækjastikuna neðst í reitnum til að forsníða og stíla texta, bæta við tenglum og fleira.
4. Veldu **Í lagi** þegar því er lokið til að vista textann.

## Sjá einnig .

[Yfirlit yfir tillögur að markaðstexta](ai-overview.md)  
[Villuleita Copilot- og gervigreindarmöguleika](ai-copilot-troubleshooting.md)  
[Algengar spurningar um tillögur að markaðstexta](faqs-marketing-text.md)  
[Grunnstilla Copilot- og gervigreindarmöguleika](enable-ai.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
