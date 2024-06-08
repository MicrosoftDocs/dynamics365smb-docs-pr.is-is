---
title: Algengar spurningar fyrir greiningaraðstoð (forskoðun)
description: 'Þessi algenga spurning veitir upplýsingar um AI-tæknina sem notuð er til að greina gögn á síðum í Business Central. Í honum eru lykilatriði og upplýsingar um notkun ÓM, hvernig það var prófað og metið og allar sérstakar takmarkanir.'
ms.date: 02/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# Algengar spurningar fyrir greiningaraðstoð (forskoðun)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Algengar spurningar (FAQ) lýsa algengum áhrifum greiningaraðstoðaraðgerðarinnar í [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Hvað er greiningaraðstoð?

Greiningaraðstoð er Afritari sem veitir aðstoð til að vinna með [gagnagreiningarhaminn](analysis-mode.md) í Business Central. Með gagnagreiningarstillingunni er hægt að skipuleggja, leggja saman og taka saman gögn á síðum og fyrirspurnum til að gera það hentugara að greina og draga út mikilvæga innsýn. Með greiningaraðstoð er hægt að búa sjálfkrafa til yfirlit yfir gögnin sem á að greina með því að tjá þarfir notanda á einföldum, náttúrulegum tungumálum, eins og "sýna lánardrottna eftir birgðageymslum sem raðað er eftir fjölda innkaupa." Greiningaraðstoð auðveldar vinnu við gögn án flókinnar tæknifærni.

## Hvað eru möguleikar á greiningaraðstoð?

Greiningaraðstoð er byggð á verkfærum fyrir Copilot í Business Central. Hann notar Azure Open Ai Azure OpenAI til að breyta óskipulögðum leiðbeiningum í skipulagða hönnun til að birta gögn í greiningarstillingunni, án þess að stofna, breyta eða uppfæra viðskiptagögn sjálfir.

## Hver er tilætluð notkun greiningaraðstoðar?

Fyrirhuguð notkun greiningaraðstoðar er að hjálpa við að stofna greiningarflipa í gagnagreiningarstillingunni til að birta gögn á þann hátt sem auðveldar útdrætti. Hins vegar er mikilvægt að athuga að greiningaraðstoðin veitir ekki beina innsýn eða niðurstöður varðandi gögnin. Það er verkfæri sem hjálpar notendum að skipuleggja og skoða gögn sín. Hins vegar er það allt til notandans að draga úr aðgerðanlegum upplýsingum, uppgötva þróun og taka upplýstar ákvarðanir um akstur viðskiptavirði.

## Hvernig var greiningaraðstoð metin? Hvaða mælieiningar eru notaðar til að mæla afköst?

- Aðgerðin gómaði umfangsmikla prófun byggða á [!INCLUDE[prod_short](includes/prod_short.md)] gögnum um sýni og öðrum hugsuðum vörulistum. Copilot var gefið fjölda kvaðninga í studdum enskum heimamönnum. Í kvaðningunum er fjallað um víðtækt svið gagnagreiningarleiðbeininga og stíla sem lýsa ásetningi. Niðurstaðan var metin gegn nákvæmni, vægi og öryggi.

- Eiginleikinn er byggður upp samkvæmt staðlinum Ábyrgur AI-staðall Microsoft. [Fræðast meira um ábyrgt ÓM frá Microsoft](https://aka.ms/RAI).

## Hvernig fylgist Microsoft með gæðum myndaðs efnis?

Microsoft hefur mismunandi kerfi til að tryggja að efni sem Copilot myndar sé í hæsta gæðaráði, finni fyrir misnotkun og tryggi öryggi fyrir viðskiptavini okkar og gögn þeirra.

Notendur geta veitt endurgjöf við öllum svörum copilot og gefið skýrslu um ónákvæmt eða óviðeigandi efni til að gera Microsoft kleift að endurbæta þessa aðgerð.

- Ef óviðeigandi myndað efni kemur upp skal tilkynna það til Microsoft með því að nota þetta svarglugga: [Tilkynna misnotkun](https://go.microsoft.com/fwlink/?linkid=2249810).

- Við greinum og nýtum endurgjöf notenda á þeim eiginleika til að hjálpa okkur að bæta svörun.

  Notandi veitir svörun með því að nota táknið like (þumlur upp) eða mislíkar (þumlur niður) á **Copilot** svæðinu á [!INCLUDE[prod_short](includes/prod_short.md)].

- Microsoft gæti slökkva á copilot-knúnum aðgerðum fyrir tilgreinda viðskiptamenn ef misnotkun á virkninni finnst.

## Hverjar eru takmarkanir á greiningaraðstoð? Hvernig geta notendur minnkað áhrif takmörkunar greiningaraðstoðar þegar kerfið er notað?

- Almennar AI takmarkanir

  Al-kerfi eru verðmæt verkfæri, en þau eru óákægð. Hugsanlegt er að efnið sem það býr til sé ekki nákvæmt. Svo er mikilvægt að nota dómgreind þína til að fara yfir og staðfesta viðbrögð Copilot áður en ákvarðanir sem gætu haft áhrif á hagsmunaaðila eins og viðskiptamenn og samstarfsaðila.

- Tungumál og landfræðilegar takmarkanir:

  - Greiningaraðstoð er aðeins studd á ensku fyrir eftirfarandi heimamenn: en-AU, en-CA, en-GB, en-IE, en-Í-NZ, en-PH, en-SG, en-US, en-ZA.

    Ef skjátungumálið í Business Central er ekki eitt af skráðum staðbundnum er eiginleikinn ekki tiltækur.

  - Gæði svaranna geta verið lægri ef:
    - Tungumálastaðurinn í Business Central er eitthvað annað en en en-US.
    - Tungumálastilling notandans í Business Central er frábrugðin aðaltungumáli viðskiptagagna í gagnagrunninum [!INCLUDE[prod_short](includes/prod_short.md)] .
  
  - Landfræðileg takmörkun:
  
    Aðgerðin er tiltæk í öllum studdum [Business Central löndum/svæðum](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) nema í Kanada, vegna reglubundinnar málsmeðferðar. Aðgerðin notar Microsoft Azure OpenAI þó Þjónustu sem er tiltæk fyrir Business Central í sumum landsvæðum. Ef umhverfið þitt er staðsett í landi/svæði þar sem Azure OpenAI þjónusta er ekki tiltæk verða stjórnendur að leyfa gögnum að færast yfir landfræði. [Fræðast meira](/dynamics365/business-central/ai-copilot-data-movement).

- Ákveðinn iðnaður, vara og efnistakmörkun:

  Fyrirtæki sem starfa í sumum viðskiptaumdæmum, svo sem læknisfræði, lyf, lögleg og vopn, gætu upplifað lægri þjónustugæði.

## Hvaða gögnum safnar greining og hvernig hún er notuð

Greiningaraðstoðin safnar lágmarksgögnum sem Business Central krefst til að veita þjónustuna. Microsoft notar ekki gögn fyrirtækisins, þar á meðal textann sem sendur er til Copilot, til að þjálfa grunnlíkönin til hagsbóta fyrir aðra. Nánari upplýsingar eru í [Dynamics 365 terms for Azure-powered OpenAI eiginleikar](https://go.microsoft.com/fwlink/?linkid=2236010).

Hún safnar einnig gögnum frá svörunarnotendum getur veitt notkun eins og (þumalputta upp) eða mislíki táknmynda (þumlur niður) í greiningaraðstoðinni **Copilot** page. Gögnin eru nafnlaus og felur í sér val á líku og eða mislíki, mislíkindaástæður ef það er kveðið á um og copilot aðgerðin sem svörunin gildir fyrir.

## Sjá einnig .

[Greina gögn með copilot (forskoðun)](analysis-assist.md)
