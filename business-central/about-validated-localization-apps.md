---
title: Þróun staðfestra forrita fyrir staðfæringu
description: Samræmast kröfum reglugerða í Dynamics 365 Business Central sem staðfest staðfæringarforrit.
author: altotovi
ms.date: 06/04/2024
ms.reviewer: bholtorf
ms.topic: conceptual
ms.author: altotovi
---

# Þróun staðfestra forrita fyrir staðfæringu

Þessi grein lýsir kröfum og leiðbeiningum um þróun staðfests staðfæringarforrits fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

## Hvað er staðfest staðfæringarforrit?

[!INCLUDE[prod_short](includes/prod_short.md)] er í boði [á heimsvísu á 170+ mörkuðum](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json). Á markaðnum vinnur Microsoft með samstarfsaðilum ISV til að staðfæra með forritum sem nálgast [!INCLUDE[prod_short](includes/prod_short.md)] má staðfæringu á [Microsoft AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Fyrir þessi svæði er hægt að nálgast staðfæringar með forritinu sem hentar kjörstaðsetningu. Forritið sem kýs staðfæringarforrit þekkir forritin sem eru byggð samkvæmt tilteknum leiðbeiningum Microsoft um gæði. ISV samstarfsaðilar sem uppfylla þessar kerfiskröfur og leiðbeiningar geta gagnast tæknilega og í viðskiptalegum tilburðum til að þjónusta sölumenn og viðskiptamenn.  

Í eftirfarandi hlutum má finna kröfur og leiðbeiningar. Þú getur haft samband við kerfið teymið ef þú vilt taka þátt í þessu forriti og uppfylla kröfur sem hér að neðan eru gerðar með því að hafa samband við okkur í gegnum [staðfæringarteymi Microsoft](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> Frumkvæði [!INCLUDE[prod_short](includes/prod_short.md)] staðfestrar staðfæringarforrits er nú verið að taka út sem verkefnisforrit. Hér á eftir koma kröfur og hlunnindi sem byggjast á ábendingum félagans og viðskiptavina.  

Forrit í staðfestri staðfæringarflugmannskerfinu innihalda safn aðgerða sem takast á við staðbundnar kröfur reglugerða sem eru innan eins af flokkunum í eftirfarandi lista.  

- **Reglubundnar kröfur** - staðbundnar aðgerðir sem hjálpa fyrirtækjum að uppfylla lagalegar kröfur sínar, svo sem skattskýrslugerð, staðbundið E-reikningsfærslusnið, staðbundið GAAP og aðrar kröfur um eftirlit.
- **Kröfur**  um innlenda staðla – staðbundnar aðgerðir sem taka til staðbundinna staðla, svo sem aðseturssnið, landsbankasnið eða staðbundnar túlkanir á altækum stöðlum.
- **Staðbundið tungumál** - tungumál í staðfæringarforritinu en einnig fyrir grunnforrit ef tungumálið er ekki á lista yfir [studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

> [!NOTE]
> Staðbundnar kröfur um markaðsþarfir eða iðnað ætti ekki að vera innifalin í kjörforritum fyrir staðfæringu. Ef forrit innihalda þessar aðgerðir er ekki hægt að samþykkja forritin sem Staðfest staðfæringarforrit.

> [!NOTE]
> Staðbundnar aðgerðir eru gagnlegar fyrir framleiðniviðskipti í landi og bæta þar með við viðskiptum en eru ekki nauðsynlegar frá sjónarhóli reglubundins sjónarhorns, t.d. tilteknum banka- og greiðslusniðum, útgjaldaskýrslum, aðgerðum í hraðbanka, launagreiðslum og álíka smærri eða stærri og gott að hafa aðgerðirnar í öðrum forritum. Ef forrit innihalda þessar aðgerðir er þeim ekki samþykkt sem Staðfest staðfæringarforrit.   

## Prófaðar viðskiptakröfur fyrir staðfæringu forrits  

- Sannprófuð staðfæringarforritaveita uppfyllir allar kröfur til að vera CSP óbeinn veitandi.  
- Staðfest staðfæringarforrit veitir markaðssetningu að lágmarki tilboð í fimm löndum/svæðum, sem búna Dynamics 365 Business Central til með staðfestu staðfæringarforriti. 
- Staðfest staðfæringarforritaveitan hefur að lágmarki 10 [!INCLUDE[prod_short](includes/prod_short.md)] netviðskiptamenn með framleiðsluumhverfi sem eru virkir með því að nota staðfesta staðfæringarforritið. 
- Forritið Staðfest staðfæring sendir viðskiptaáætlun árlega til forritsins v-teymis. Þar með talið eru áætlaðar markaðssetningar- og undirbúningsaðgerðir til að kynna búnt tilboðsins með CSP óbeinum endurseljendum í viðeigandi löndum/svæðum. Hægt er að senda áætlun í upphafi hvers ársfjórðungs til [staðfæringarteymis](mailto:d365bcloc@microsoft.com) Microsoft.  
- Staðfest staðfæringarforrit eru gerð tiltæk öllum viðskiptamönnum og samstarfsaðilum sem vilja njóta góðs af því.     
- Staðfest staðfæringarforritaveitan tekur þátt í ítrekuðum vinnugrunni við Microsoft.

## Virkni og tæknilegar kröfur um staðfæringu  

### Virkniþarfir   

Fyrir utan að uppfylla tæknilegar kröfur fyrir staðfæringarforritið sem hentar best er að lágmarks hagkvæmt vöruumfang kjörforrits:  

- Staðbundnar reglur:   
  - Lagaskilyrði.   
  - Opinberlega skyldubundnar aðgerðir. 
  - Aðeins láréttir eiginleikar (ekki sértækir iðnaður).  
  - Á við í flestum fyrirtækjum.  
  - Innan eftirfarandi teikningar:   
    - Svæði algengustu lagabreytinganna. 
    - Þegar rakið sem staðfæring í staðfæringum Microsoft. 
    - Meðmælavísanir aðgerða – sjaldan nýjar.  
    - Engin snið fyrir tiltekin lánardrottin/banka, laun eða svipuð. 
    - Engir altækir eiginleikar ef þeir eru ekki byggðir upp af Microsoft. 
- Þýðingar: 
  - Þýðing á staðfæringarforriti yfir í staðbundin tungumál. 
  - Þýðing á grunnforriti yfir í staðbundin tungumál – ef tungumálið er ekki þegar [studt](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  
  - Þýðing á fylgiskjölum staðfæringarforritsins yfir í staðbundin tungumál. 
- Jafnvel þó þeir séu báðir hluti staðfæringar er mælt með því að National Standard Aðgerðir (staðbundnir hluti) séu byggðir sem sérstök forrit frá Staðbundnum reglugerðareiginleikum. 
- Sýnigögn á tungumáli landsins sem eiga við um tiltekinn markað.   
- Allar aðgerðir verður að hanna til að halda einfölduðu notandaviðmóti, athuga skal að þeir eru fyrst og fremst ætlaðir á SMB markaðinn.  
- Forðast skal að byggja nýjar aðgerðir ef sömu eða svipaðar aðgerðir eru þegar til í grunnforritinu, svo sem rafræna reikningsfærslu, útflutning endurskoðunar, VSK-eiginleika, gagnaskipti og aðrar þar sem flestar aðgerðir eru sameiginlegar öllum löndum/svæðum en nokkrar staðbundnar reglur eða viðskiptasnið eru sem eru viðbætur við altæka ramma eða snið. Í stað þess að byggja nýjar aðgerðir skal framlengja þær sem fyrir eru.  
- Útbúa leiðsagnarforrit fyrir uppsetningu (leiðsagnarforrit) fyrir svæði sem eru flókin til að setja upp til að hjálpa notendum að virkja, uppgötva og hafa góða reynslu af notkun staðfæringarforritsins.  
- Samstarfsaðilar verða að útvega hagnýt fylgigögn fyrir alla þætti staðfæringar þeirra.  

### Tæknilegar kröfur  

Hér á eftir er að finna lista yfir þarfir sem þarf að uppfylla áður en forritið Staðfest staðfæring er sent sem viðbót við staðfestingu. Þessi listi breytir [ekki tæknilegu villuleitarlistanum](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) og nær aðeins yfir kröfur þaðan.  

- Forritaveiturnar staðfest staðfæring verða að byggja upp staðfest staðfæringarforrit byggt á W1 grunnforritinu.  
- Forritaveitur fyrir staðfesta staðfæringu verða að fylgja líftíma og stuðningsreglum Microsoft.   
- Áskilin sjálfvirkni verður að ná lágmarks 80% af kóta og öll viðskiptaferli sem breytast með forritinu Staðfest staðfæring verður að ná yfir með sjálfvirkniprófun.  
- Staðfest staðfæringarforritaveiturnar verða að uppfæra og/eða prófa það er Staðfest staðfæringarforrit áður en opinber ræsing nýrrar útgáfu (að lágmarki með RC fyrir nýja útgáfu) til að staðfesta að engin vandamál séu í gangi. 
- Allir hlutir í kóta staðfestrar staðfæringarforrits verða að vera á ensku.   
- Staðfestar staðfæringarforritaveitur verða að fylgja stefnu Microsoft um úrelta hluti og brjóta breytingar og bestu venjur til að afskrifa AL-kótann.  
- Forritaveiturnar fyrir staðfesta staðfæringu ættu að bæta við nýjum atburðum ef það er krafist af markaði (öðrum framkvæmdaaðilum eða viðskiptamönnum) ef það er skynsamlegt í viðskiptum, í kjölfar stefnu og starfs í Microsoft. Annars verða staðfestar staðfæringarforritaveitur að gefa svar við slíkum fyrirspurnum með réttri réttri stillingu á því hvers vegna það er ekki skynsamlegt að bæta við. 
- Forritaveiturnar Staðfest staðfæring verða að útvega skriflegar prófunaraðstæður á ensku og gera Microsoft kleift að gera handvirka prófun ef Microsoft krefst þess.  
- Ef staðfest staðfæringarforrit auka gagnalíkanið [!INCLUDE[prod_short](includes/prod_short.md)] með nýjum töflum og/eða reitum verður forritið Staðfest staðfæring að stilla **eiginleika DataClassification** rétt.

> [!NOTE]  
> Einnig er hægt að búa til samþættingu ef þér finnst hún gagnleg til að hafa einhverja virkni setta utan umhverfisins [!INCLUDE[prod_short](includes/prod_short.md)] og tengjast þess í stað til að nota til [!INCLUDE[prod_short](includes/prod_short.md)] dæmis API eða vefþjónustu.

## Sjá einnig .

[Tæknileg prófun](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Þróun staðlaðrar staðfæringarlausnar](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Lönd/svæði í boði og studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Hvað er staðbundnar aðgerðir í Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]?](about-localization.md)  
[Alþjóðlegt framboð á Microsoft Dynamics 365](/dynamics365/get-started/availability)  
[Yfirlit yfir reglufylgni](compliance/compliance-overview.md)  
[Landfræðilegt til ráðstöfunar fyrir Dynamics 365](https://dynamics.microsoft.com/en-us/availability-reports/georeport/)  
