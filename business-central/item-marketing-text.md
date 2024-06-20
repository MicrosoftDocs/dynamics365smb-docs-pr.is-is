---
title: Bæta markaðssetningartexta við vörur
description: Skrifa markaðssetningartexta fyrir vörur í Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# Bæta markaðssetningartexta við vörur

Fyrir allar vörur sem skráðar eru í Business Central er hægt að skrifa *markaðssetningartexta* um vöruna. Þótt markaðssetningatexti sé eins konar lýsing er hún öðruvísi en lýsingarreitur **vörunnar** . Reiturinn **Lýsing** er gjarnan notaður sem nákvæmt birtingarheiti til að auðkenna vöruna á fljótlegan hátt. Markaðssetningartextinn er hins vegar ríkari og lýsandi texti. Tilgangur hennar er að bæta við markaðssetningu og kynningarefni, einnig þekkt sem *afrit*. Þá er hægt að birta þennan texta með vörunni ef hún er birt á vefverslun, eins Shopify og eða límd í tölvupóst eða önnur samskipti við viðskiptavini þína.

Það eru tvær leiðir til að búa til markaðssetningartextann. Auðveldast að hefjast handa er að nota Copilot, sem leggur til EI-myndaðan texta fyrir þig. Hin leiðin er að byrja frá grunni. 

## <a name=copilot></a> Fá markaðssetningatextatillögur með Copilot

Með Copilot færðu fljótt textatillögu sem býr til sjálfkrafa fyrir þig. AI-mynda textinn er sniðinn að vörunni og gefur góðan upphafspunkt. Textinn er byggður að hluta á eftirfarandi upplýsingum:

- Eigindir sem skilgreindar eru fyrir vöruna&mdash;, til dæmis lýsing, litur, víddir, efni og svo framvegis. [Fræðast meira um vörueigindir](inventory-how-work-item-attributes.md).
- Reiturinn Lýsing **vörunnar** .
- Vörutegundin. [Fá nánari upplýsingar um flokkun vara](inventory-how-categorize-items.md).
- Valkostir stíls eins og tónn raddar, sniðs og lengdar.

Copilot er hannað til að spara þér tíma og hjálpa þér að skrifa skapandi og taka þátt í texta sem endurspeglar vörumerkið þitt og er í samræmi við vörulínuna þína. Byrjað er á því að búa til tillögu og textanum sem lagt er til breytt eftir þörfum.

### Tiltæk tungumál

[!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

### Frumskilyrði

Eiginleikinn Textatillögur markaðssetningar er virkur í umhverfinu. Stjórnandi framkvæmir yfirleitt þennan verkhluta. Nánari upplýsingar eru í [Grunnstilling copilot og AI](enable-ai.md).

### Búa til fyrstu uppkast með Copilot

Ljúka skal eftirfarandi skrefum til að bæta markaðssetningartexta við fyrirliggjandi vöru. Til að læra hvernig á að stofna nýja vöru er farið í [Skrá nýjar vörur](inventory-how-register-new-items.md).

1. Í Business Central er atriðið sem á að breyta opnað með því að ljúka eftirfarandi skrefum:

   - Í efra hægra horni ![skal velja Lightbulb sem opnar Tell Me aðgerð 22.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vörur** og velja svo tengdan tengil til að sýna lista yfir tiltækar vörur.

   - Tvísmellt er á vöruna eða gildi hennar valið í reitnum **Nr.** súla.

1. Á birgðaspjaldinu eru tvær leiðir til að byrja að skrifa markaðstexta með Copilot: í **upplýsingakassa markaðssetningar** eða með því að nota textaaðgerðina **Markaðssetning**. Þessar aðferðir eru gefnar til kynna í eftirfarandi mynd af birgðaspjaldi.  

   [![Sýnir birgðaspjald með markaðssetningartextasvæði](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

   Fyrsta drög að vöru eru stofnuð með því að gera eitt af eftirfarandi skrefum:

   - Á rúðunni **Markaðssetningartexti**  **í upplýsingakassanum hægra megin á síðunni skal velja** Uppkast með Afrita. 

     Copilot byrjar að draga texta markaðssetningarinnar.

   - Efst á síðunni skal velja aðgerðina **Markaðssetningartexti** og velja **síðan Drög með copilot í** glugganum Breyta **markaðssetningartexta** .  Uppkast **að markaðssetningartexta með gluggum Copilot** birtist og birtir lista yfir allar tiltækar eigindir vörunnar.
1. Velja skal eiginleikana sem copilot grunntillögurnar eiga að koma í, svo er Mynda **valið**. Hægt er að breyta völdum eigindum og öðrum valkostum síðar. Copilot byrjar að draga texta markaðssetningarinnar. 

   ![Sýnir gluggann breyta markaðssetningartexta](media/marketing-text-copilot-attributes.svg)

1. Þegar Copilot lýkur uppkastinu birtist textinn í glugganum Copilot-ritillglugginn til að skoða og breyta.

   [![Sýnir stofnun með Copilot gluggum](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Nú er hægt að fá fleiri tillögur, reyna að bæta tillögurnar, breyta texta og fleira.  [Fara á Skoða, breyta og vista](#review-edit-and-save-text) fyrir upplýsingar.

### Skoða, breyta og vista texta

Þegar búið er að fá fyrstu uppkast þarf að fara yfir það og gera breytingar á textanum til að fá hana tilbúna til útgáfu. Þetta verk er unnið úr copilot-ritlinum, sem gerir þér kleift að fá fleiri tillögur, breyta kjörstillingum til að hafa áhrif á tillögurnar og gera handvirkt breytingar og stíl textans.

> [!IMPORTANT]
> Eiginlega textinn frá Copilot er aðeins tillaga og hann getur haft mistök. Það krefst yfirsjónar manna og endurskoðunar til að tryggja að það sé nákvæmt og viðeigandi. Skoða hvaða texta sem lagt er til og breyta eftir þörfum áður en hann er vistaður og birtur til opinberrar notkunar.

Nota skal eftirfarandi leiðbeiningar til að ljúka og vista texta markaðssetningar.

1. Breyta texta beint í textareitnum. Nota verkfærastikuna neðst í kassanum til að sníða og stíltexta, bæta við tenglum og fleira.
2. Til að fá nýja tillögu skal velja **Endurgera**.
3. Ef tillögurnar eru ekki fullnægjandi þarf að bæta textatillögunum **við með valkostunum** Tónn **,** Snið **og** Áhersla.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   Til að fá leiðbeiningar um bættar tillögur er farið í [tillögurnar Endurbætt og sniðið textatillögurnar](#improve-and-tailor-text-suggestions).

4. Til að fara fram og til baka með tillögum skal nota fyrri og næstu tengla efst á síðunni (*x* **af** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Farið vandlega yfir textann fyrir nákvæmni og nákvæmni:

   - Ef vista á textann skal velja **Halda honum**. 
   - Ef þú vilt ekki vista skaltu velja fleyghnappinn (ruslið) ![Sýnir ruslið getur táknið til að eyða öllum Stjórnunartillögum fyrir afstemmingu bankareikninga](media/copilot-delete-trash-can.png).

### Bæta og sníða textatillögur

Þú getur gert nokkur þrep til að bæta textatillögurnar og kveikja í þeim til að henta persónulegum eða óskum fyrirtækisins.

1. Breyta vörueigindum sem Copilot notar.

   Stjórnunartillögur eru byggðar að hluta til á eigindum vörunnar. Til að skoða tiltækar eigindir og núgildandi stillingar skal velja breytingartáknið ![Sýna breytingatáknið í glugganum Copilot til að breyta eigindatákni](media/edit-pencil.png) í vinstra horni uppi. Á síðunni **Vörueigindir** skal velja þá eiginleika sem best samræmast þeim eiginleikum sem á að kynna. Eftir því sem viðeigandi eigindir eru taldar, þeim mun ríkari verður útkoman. Ef þér finnst vanta einhverjar lykileigindir, bætið við fleirum. Nánari upplýsingar um eigindir eru í [Vinna með vörueigindir](inventory-how-work-item-attributes.md)
1. Breyta kjörstillingum fyrir  **tón-,** snið **og** **áhersluvalkosti** .

   |Valkostur|Heimildasamstæða|
   |-|-|
   |Tónn |Þessi kostur er notaður til að hafa áhrif á hvers konar orð, orðasambönd og greinargerð eru notuð til að taka þátt í markhópnum. Hægt er að velja úr nokkrum fyrirfram skilgreindum röddum, allt frá **Formal**  (sem leiðir af sér viðskiptatón) til **Creative**  (sem leiðir af sér óformlegan tón). |
   |Snið og lengd|Þessi kostur er notaður til að stýra almennri uppbyggingu textans, sem samanstendur af þremur hlutum, sem fjórir mismunandi valkostir taka til: <ul><li>**Tagline** - Grípandi orðasambandi eða stutt setning sem auðkennir vöruna eða vörumerkið.</li><li>**Málsgrein** - Ein málsgrein flautu- og verbose texta, sem samanstendur af nokkrum heildarsetningum.</li><li>**Tagline + Málsgrein** - A tagline fylgdi málsgrein</li><li>**Stutt** - Kynningasetning, svipuð taglínu og á eftir skotheldum lista yfir lykilatriði vaxta.</li></ul> |
   |Áhersla|Þessi kostur er notaður til að velja úr lista yfir fyrirfram skilgreinda eiginleika sem á að leggja áherslu á í textanum. Veldu gæði sem eru best samstillt við tegund vörunnar sem þú skrifar um. Eiginleikarnir samsvara ekki beint eigindum vörunnar, lýsingu eða tegund. Gæði **gætu til dæmis**  verið góður kostur fyrir bæði hjól eða skrifborð, en **Speed** myndi henta hjóli en ekki skrifborði.|

1. Reiturinn **Lýsing** er bættur á birgðaspjaldinu.

   Textinn í reitnum **Lýsing** er notaður sem-er á mörgum stöðum í textanum sem lagður er til og því er mikilvægt að lýsingin eigi besta mynd af því hvernig vísað er í vöruna í markaðssetningartextanum. 

1. Ganga þarf úr skugga um að reiturinn **Vöruflokkskóti** á birgðaspjaldinu sé stilltur á réttan flokk.

   Copilot finnur orð og orðasamband sem tengjast flokknum og vinnur þau inn í textann sem lagður er til.

### Unnið með mörg tungumál 

Texti er alltaf myndaður á því tungumáli sem skilgreint er af [notandastillingum](ui-change-basic-settings.md#language). Ef fyrirtækið rekur og færir gögn inn í Business Central á öðru tungumáli eða ef Business Central er tengt netverslun þinni, svo sem með Shopify, gæti það leitt til útgáfuefnis sem passar ekki við svipað markaðsefni.

## Stofna texta frá grunni

1. Í Business Central er varan sem á að breyta opnuð á eftirfarandi hátt:

    1. Í efra hægra horni ![skal velja Lightbulb sem opnar Tell Me aðgerð 22.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vörur** og velja svo tengdan tengil til að sýna lista yfir tiltækar vörur.
    2. Til að opna vöruna er tvísmellt á hana eða númerið valið í reitnum  **Nr.** .

2. Framkvæmdu eitt af eftirfarandi skrefum:

   -  **Á glugganum Texti** markaðssetningar í upplýsingakassanum hægra megin á síðunni er Breyta **valið**.
   - Veljið aðgerðina **Markaðssetningartexti** .
3. Breyta texta beint í reitnum **Texti** markaðssetningar. Nota verkfærastikuna neðst í kassanum til að sníða og stíltexta, bæta við tenglum og fleira.
4. Velja skal **Í lagi** þegar það er gert til að vista textann.

## Sjá einnig .

[Yfirlit yfir tillögur að markaðstexta](ai-overview.md)  
[Úrræðaleit fyrir Copilot- og AI-eiginleika](ai-copilot-troubleshooting.md)  
[Algengar spurningar um tillögur að markaðstexta](faqs-marketing-text.md)  
[Grunnstilla Copilot- og gervigreindarmöguleika](enable-ai.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
