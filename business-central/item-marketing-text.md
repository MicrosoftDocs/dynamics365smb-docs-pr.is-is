---
title: Bæta markaðstexta við vörur
description: Skrifa markaðstexta fyrir vörur í Viðskiptamiðinu
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Bæta markaðstexta við vörur

Ef um er að ræða vöru sem er skráð í Business Central er hægt að skrifa  *markaðstexta*  um vöruna. Þrátt fyrir að markaðstexti sé nokkurs konar Lýsing er það mismunandi eftir lýsingarsviði  **vöru** .  **Reiturinn Lýsing**  er vanalega notaður sem Birtingarheiti þess að nota fljótt til að auðkenna afurðin. Markaðstextinn er hins vegar fremur ríkur og lýsandi texti. Tilgangur þess er m.a. að bæta markaðsefni og kynningarefni, einnig þekkt sem  *eintak*. Þennan texta er síðan hægt að birta með vörunni ef hann er birtur á vefbúð, Like Shopify.

Það eru tvær leiðir til að búa til markaðstexta. Auðveldasta leiðin til að komast af stað er að nota Copilot, sem stingur upp á AI-myndaðan texta fyrir þig. Hin leiðin er að byrja frá grunni. 

## <a name=copilot></a> Stofna markaðstexta með AI-myndaða (Forskoðun) með Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Með Copilot færðu fljótt textatillögu sem er mynduð sjálfkrafa fyrir þig. Uppbúin texti er sniðgenginn í atriðið og gefur þeim góðan upphafsstað. Textinn er byggður að hluta á eftirfarandi upplýsingum:

- Eigindir sem eru skilgreindar fyrir vöruna, til dæmis, eins og lýsingin, litur, víddir, efni o. frv.
- Kjörborðstíll valinnar eins og tónn í rödd, sniði og lengd.

Copilot er hönnuð til að spara þér tíma og hjálpa þér að skrifa skapandi og þátt texta sem endurspeglar vörumerki þitt og er í samræmi yfir vörulínu þinni. Byrja á því að mynda tillögu, breyta síðan leiðbeinandi texta eftir þörfum.

### Frumskilyrði

- Þú notar  [forskoðunarútgáfu](ai-preview-getstarted.md)  af Business Central sem er virkjaður fyrir Copilot. Virkjun Copilot er unnin af admin. Frekari upplýsingar er að fara í til að  [samskipa texta fyrir MARKAÐSSETNINGU AI-vara með Copilot](enable-ai.md).

-  [SKOÐAÐU spurningar](ai-faq.md)  um copilot til að fá meiri upplýsingar um AI-myndaðar texta tillögur frá copilot og hvernig þú átt að nota þær.

### Búa til fyrstu drög með Copilot

1. Í Business Central er varan sem á að breyta opnuð. Til að opna vöru skal gera eftirfarandi skref:

   1. Í efra hægra horninu skaltu velja þá ljósaperu  ![sem opnast Segðu mér lögun 22](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Teiknið, Færið inn  **atriði** og veljið síðan tengda tengilinn til að sýna lista yfir tiltækar vörur.
   2. Til að opna atriðið er tvísmellt á það eða gildi þess valið í reitnum   **Nr**. dálki.

   Upplýsingar um það hvernig eigi að stofna vöru er að fara í til að  [skrá nýjar vörur](inventory-how-register-new-items.md).

   [![Sýning og birgðaspjald með Markaðstextarúðu](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. Á birgðaspjaldinu eru tvær leiðir til að byrja að skrifa markaðstexta með Copilot:

   - Ein leið er að nota  **rúðu Markaðstextans**  í upplýsingakassa hægra megin á síðunni. Fylgdu þessum leiðbeiningum:

      1.  **Í rúðunni markaðssetning texta**  er valið  **Búa til með copilot**.

         Textinn sem er leiðbeinandi birtist í rúðunni.
      2. Ef óskað er eftir annarri tillögu er valið  **Búa til með Copilot**  aftur. Ef þú vilt ekki tillögu skaltu velja  **sleppa**  því að hreinsa rúðuna.

         Þú getur gert þetta skrefi ofar og þangað til þú færð uppástungu heldurðu að það sé nógu góður byrjunarpunktur. En hafið í huga að núverandi tillaga verður yfirskrift og þið megið ekki endilega fá hana aftur. Þannig að ef þú líkar við núverandi tillögu, Farðu þá í næsta skref. Þú munt samt hafa tækifæri til að fá fleiri tillögur, og jafnvel bæta tillögurnar, ef þér líkar síðar.
      3. Velja  **skal yfirfara og vista tillögu**  eða  **Breyta**  til að yfirfara, breyta og vista textann.

         Þetta skref tekur þig  **í póst með Copilot**  -síðunni. Fara í næsta kafla.

         > [!NOTE]
         > Textinn verður ekki vistaður fyrr en þú gerir þetta skref.

   - Önnur leið er að velja markaðsaðgerðinn  **·**  sem er efst á síðunni Vöruspjald til að fara beint  **á Create með copilot**   síðunni.

      **Frá stofnun með copilot**  síðunni, Veldu  **Búa til með copilot**  til að fá fyrstu uppákomu. Þú getur svo fengið fleiri tillögur, reynt að bæta tillögurnar sem þú færð, breytt texta og fleira.  [Farðu í yfirfara, breyta og vista](#review-edit-and-save-text)  fyrir nánari upplýsingar.

   > [!TIP]
   > [Hvaðan kemur tillagan?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### Yfirfara, breyta og vista texta

Þegar búið er að taka fyrstu uppkastið þarf að fara yfir það og gera breytingar á textanum til að fá hana tilbúna til birtingar. Þessi vinna er unnin úr  **stofunum með Copilot**  -síðunni. Núgildandi texti birtist í  **reitnum markaðssetning texta** . Síðan gerir þér kleift að fá fleiri tillögur, breyta kjörum til að hafa áhrif á tillögurnar og gera handvirkt breytingar og stíla á textann.

[![Sýnir að búið er að búa til glugga með Copilot](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> Uppbúin texti frá Copilot er aðeins uppákoma og það geta verið mistök. Það þarf að manna yfirsjón og yfirsjónir til að tryggja það réttmætt og viðeigandi. Fara yfir hvaða leiðbeinandi texta og breyta eftir þörfum áður en hann er vistaður og gefa hann út til opinberrar notkunar.

Notaðu eftirfarandi leiðbeiningar til að ganga frá og vista markaðstexta.

1. Gera breytingar á texta beint í  **markaðskextextareitinn** . Notaðu Verkfærasláin meðfram botni kasssins til að sníða og stíla texta, bæta við tenglum og fleira.
2. Til að fá nýja tillögu er valið  **Búa til drög**.
3. Ef þú ert ekki sáttur við tillögur, auka tillögur um texta út frá þínum óskum.

   Velja  **skal fleiri stillingar**, breyta valkostum sem birtast undir  **Velja hvernig copilot stofnar tillögur**, velja  **síðan búa til drög**  til að fá nýja tillögu.

   Til viðmiðunar við að bæta við tillögum er farið í að bæta og sníða tillögur  [að](#improve-and-tailor-text-suggestions) texta.

4. Ef fara á aftur í fyrri tillögu skal velja  **afturkalla**.
5. Skoðið vandlega textann fyrir nákvæmni og viðeigandi texta og veljið  **síðan í lagi**  til að vista hann.

### Bæta og sníða tillögur að texta

Það eru nokkur skref sem þú getur gert til að bæta tillögur í texta og klikka þá á því að henta þínum persónum eða fyrirtækjum.

1. Notaðu valkostina efst á  **Stofna með Copilot**  -síðu til að hafa áhrif á útkomu í TEXTANUM í AI-mynduðu: 

   |Valkostur|Description|
   |-|-|
   |Eigindir sem eiga að fylgja með|Notið þennan valkost til að byggja tillögurnar, að hluta á eigindum sem er úthlutað á vöruna. Velja eigindin sem best skal samræma við þau einkenni sem ætlunin er að efla. Því fleiri viðeigandi eigindir sem þú ert með, þeim mun ríkari verður útkoman. Ef þér finnst þú vanta einhverja lykileiginleika Bættu fleiri við. Frekari upplýsingar um eiginleika er að fara í  [vinnu með vörueigindum](inventory-how-work-item-attributes.md) |
   |Leggja áherslu á gæði|Þessi valkostur er notaður til að velja af lista yfir fyrirfram skilgreinda eiginleika sem á að leggja áherslu á í textanum. Veldu gæði bestu alvöruna með þeirri tegund vöru sem þú ert að skrifa um vöru. Eiginleikar samsvara ekki beint við eigindir vörunnar, lýsingu eða tegund. Gæði  **gætu til dæmis**  verið góður kostur fyrir bæði reiðhjól eða afgreiðsluborð,  **en hraði**  myndi henta á reiðhjól en ekki afgreiðsluborð.|
   |Raddblær|Notaðu þennan valkost til að hafa áhrif á hvers konar orð, orðasambönd og greinarmerki eru notuð til að taka þátt í að sinna markhópnum. Hægt er að velja úr nokkrum fyrirfram skilgreindum tónum raddarinnar, allt frá  **formlegum**  (sem leiðir af sér mestan viðskiptatón Valmöguleikarnir) til  **skapandi**  greina (sem leiðir í senn óformlegan tón um valið). |
   |Snið og lengd|Þessi valkostur er notaður til að stýra almennu skipulagi textans sem samanstendur af þremur hlutum og fjallað um fjóra valkosti: <ul><li>**Tagline**  -grípandi orðasambönd eða stutt setning sem auðkennir atriðið eða vörumerki.</li><li>**Málsgrein**  -stök málsgrein af flúent og orðtexta, sem samanstendur af nokkrum fullsetnum setningum.</li><li>**Tagínu + lið**  -tagína eftir efnisgrein</li><li>**Stutt**  -inngangsorð, líkt og tagína, fylgir með Deplar-listi yfir helstu vaxtaratriði.</li></ul> |

2.  **Bæta lýsingarsvæðið**  á birgðaspjaldinu.

   Textinn í  **reitnum Lýsing**  verður notaður sem-er á maí-stöðum í leiðbeinandi textanum þannig að mikilvægt er að lýsingin komi best að þeirri lýsingu sem vísað er í markaðstexta vörunnar. 

3. Ganga þarf úr skugga um  **að reiturinn tegundarkóti**  á birgðaspjaldinu sé stilltur á réttan flokk.

   Í copilot er að finna orð og orðasambönd sem tengjast flokknum og vinna þau inn í leiðbeinandi texta.

## Búa til markaðstexta frá grunni

1. Í Business Central er varan opnuð sem á að breyta á eftirfarandi hátt:

    1. Í efra hægra horninu skaltu velja þá ljósaperu  ![sem opnast Segðu mér lögun 22](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Teiknið, Færið inn  **atriði** og veljið síðan tengda tengilinn til að sýna lista yfir tiltækar vörur.
    2. Til að opna atriðið er tvísmellt á það eða númer þess valið í reitnum   **Nr**. .

2. Framkvæmdu eitt af eftirfarandi skrefum:

   - Í  **Markaðsstextarúðu**  upplýsingakassa hægra megin á síðunni velurðu  **Edit**.
   -  **Veljið aðgerðina markaðssetning texta** .
3. Gera breytingar á texta beint í  **markaðskextextareitinn** . Notaðu Verkfærasláin meðfram botni kasssins til að sníða og stíla texta, bæta við tenglum og fleira.
4. Valið  **er í lagi**  þegar gert er til að vista textann.

## Sjá einnig .

[Yfirlit um markaðssetningu á AI-knúinn vöru með Copilot](ai-overview.md)  
[Grunnstilla hluta markaðstexta gervigreindar með Copilot](enable-ai.md)  
[Textahöfundur Markaðsupplýsingar með Copilot-FAQ vöru](ai-faq.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  