---
title: Vinna með Intrastat skýrslugerð
description: Lærðu hvernig á að tilkynna viðskipti við fyrirtæki í öðrum ESB löndum/svæðum með Intrastat kerfinu.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 01/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---
# Vinna með Intrastat skýrslugerð

Öll fyrirtæki í löndum innan Evrópusambandsins (ESB) þurfa að gefa öðrum löndum/svæðum innan sambandsins skýrslur um viðskipti sín. Einnig þarf að gefa hagstofu viðkomandi lands/svæðis mánaðarlega skýrslu um hreyfingu vöru og skýrsluna þarf að afhenda skattayfirvöldum. Intrastat er kerfið til að safna saman tölfræði um vöruviðskipti innan þessara landa/svæða. Þú notar **Intrastat-skýrsla** til að ljúka reglubundinni Intrastat-skýrslugerð (yfirleitt mánaðarlega), söfnun, skráningu og tilkynningu um vöruviðskipti í samræmi við löggjöf á hverjum stað.

Intrastat-skýrslur eru byggðar á grunnreglugerðum ESB sem gilda um öll lönd/svæði; þó í reynd er nokkur munur innan einstakra landa/svæða. Hvert land/svæði hefur sínar reglur um hvað nákvæmlega og hvernig á að tilkynna.

> [!IMPORTANT]  
> Þessi grein lýsir nýju Intrastat-upplifuninni sem er í boði í [!INCLUDE[prod_short](includes/prod_short.md)] frá og með byrjun 2022 útgáfutímabils 2, sem inniheldur stækkaða eiginleika og [verður að vera kveikt á fyrir fyrirliggjandi fyrirtæki](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Hafðu samband við stjórnanda til að kveikja á og setja upp nýju getuna.
>
> Lestu fyrri útgáfu af Intrastat uppsetningar- og notkunargrein á [Setja upp og skrá Intrastat](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]  
> Intrastat upplýsingar eiga ekki við um flutning á þjónustu milli landa/svæða, heldur aðeins vörur (hlutir og fastafjármunir). Ef sveitarfélög krefjast skráningar á flutningi þjónustu milli landa/svæða er hægt að gera það með því að nota **Þjónustuyfirlýsing** eiginleikann.
>
> Sem stendur er gert ráð fyrir að þessi eiginleiki verði í boði frá nóvember 2022 sem forrit hjá [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Á þeim tímapunkti, til að nota það, þarf fyrst að setja það upp á síðunni **Viðbótarstjórnun**.

## Fylltu út Intrastat-skýrsluna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Intrastat-listi** og veldu viðeigandi tengil.
2. Veldu aðgerðina **Ný** til að búa til nýja **Intrastat-skýrslu**.
3. Ef færa þarf inn innri upplýsingar um **Intrastat-skýrsluna** skal fylla út þessar upplýsingar í reitinn **Lýsing**.
4. Í reitnum **Tímabil tölfræði** skal tilgreina mánuðinn sem gefa á upp gögn fyrir. Sláið inn tímabilið sem fjögurra stafa númer án bils eða tákna. Það fer eftir þínu landi/svæði, sláðu inn annað hvort mánuðinn fyrst og síðan árið, eða öfugt. Fært er til dæmis inn annaðhvort á *2206* eða *0622* fyrir júní 2022.
5. Veljið aðgerðina **Leggja til línur**. Reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru þegar komnir með dagsetningarnar sem tilgreindar eru fyrir tölfræðitímabilið í haus Intrastat-skýrslunnar.
6. Hægt er að færa prósentu í reitinn **Kostnaðarregla %** (til að ná yfir flutning og tryggingar). Ef færð er inn prósenta verður efni reitsins **Upplýsingagildi** í færslubókinni hlutfallslega hærra. En ef þú vilt nota þennan eiginleika verður þú að breyta reitnum **Upphæð að meðtöldum kostnaðarauka** í **Já**.
7. Þú getur að lokum sett upp aukastillingar á flýtiflipanum **Viðbót**:
   1. **Slepptu endurútreikningi fyrir núllupphæðir** til að tilgreina að línur án upphæða verði ekki endurreiknaðar meðan á runuvinnslu stendur.
   2. **Slepptu núllupphæðum** til að tilgreina að birgðabókarfærslur án upphæða verði ekki með í runuvinnslunni.
   3. **Slepptu óreikningsfærðum færslum** til að tilgreina hvort birgðabókafærslur sem eru sendar eða mótteknar en ekki reikningsfærðar séu ekki teknar með í ferlinu.
8. Smellt er á **Í lagi** til að hefja keyrsluna.

Keyrslan sækir allar birgðafærslur á upplýsingatímabilinu og setur þær inn í **Intrastatskýrsluna** sem línur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Breyta Intrastat-skýrslunni

Ef þörf krefur er hægt að breyta línunum, en í hvert skipti sem gildi er breytt í línu Intrastat-skýrslunnar verður reiturinn **Leiðrétting** sjálfkrafa merktur sem **Já**. Að lokum geturðu bætt við nýrri línu handvirkt ef ástæða er til. Til að bæta handvirkt við nýrri línu.

1. Á síðunni **Intrastat-skýrsla** skal velja aðgerðina **Ný lína** á flýtiflipanum **Línur**.
2. Veldu valkostinn **Innhreyfing** eða **Sending** í reitnum **Gerð**.
3. Í reitnum **Tegund uppruna** skal velja einn af upprununum: **Birgðafærsla**, **Eignafærsla** eða **Verkfærsla**.
4. Byggt á **Tegund uppruna** í reitnum **Vörunr.** er hægt að velja **Vara** (í báðum tilfellum **Birgðafærsla** eða **Verkfærsla**) eða **Eignir**.
5. Fylltu út í aðra reiti eins og þú þarft fyrir Intrastat-skýrsluna.

> [!NOTE]  
> Þegar nýrri línu er bætt handvirkt við Intrastat-skýrsluna verður reiturinn **Dagsetning** í línunni að vera fyrir innan sviðs **Tölfræðitímabils** sem bætt var við hausinn.

## Staðfesta Intrastat-línur

Þegar þú hefur fyllt út **Intrastat-skýrsluna** geturðu keyrt aðgerðina **Gátlistaskýrsla** til að ganga úr skugga um að allar upplýsingar í **Intrastat-skýrslunni** séu réttar. Áskildir reitir sem þú hefur stillt á síðunni **Gátlisti Intrastat-skýrslu** sem vantar gildi verða sýndir í upplýsingareitnum **Villur og viðvaranir** á síðunni **Intrastat-skýrsla**.

Keyrðu **Intrastat Report Checklist** skýrsluna til að athuga Intrastat línur áður en þær eru fluttar út á tilskilið snið. Athugunin er keyrð í **Intrastat-skýrslunni**.

## Endurútreikningur þyngdar eða viðbótarmælieiningar

Ef þú fékkst villuboðin *'Heildarþyngd' í Intrastat skýrslulínunni má ekki vera auð*, þá er það líklega vegna þess að þú stilltir ekki **net Vægt** reiturinn á notuðum uppruna, hlut eða eign. Í þessu tilviki skaltu leita að vöru- eða eignaspjaldinu og bæta við nauðsynlegum reit. Eftir það þarftu bara að opna **Intrastat-skýrsluna** og fylgja þessum skrefum:

1. Veldu aðgerðina **Endurr. þyngd/viðbótarmælie.** til að endurreikna **Heildarþyngd** og/eða **Viðbótarmagn**.
2. Velja einn valkostanna:

    1. **Þyngd** – til að eingöngu endurreikna **Heildarþyngd** út frá núverandi upplýsingum um **Nettóþyngd** á vöru- og eignaspjöldum.
    2. **Magn viðbótarmælie.** – til að eingöngu endurreikna **Viðbótarmagn** í línu **Intrastat-skýrslu** ef það er til, út frá núverandi upplýsingum um **Viðbótarmælie.** á vöru- eða eignaspjöldum.
    3. **Bæði** – til að endurreikna bæði **Heildarþyngd** og **Viðbótarmagn** út frá núverandi upplýsingum um vöru- og eignaspjöldin.
3. Smellt er á **Í lagi** til að hefja keyrsluna.

## Senda Intrastat-skýrslu sem skrá

Hægt er að senda Intrastat-skýrsluna sem skrá byggða á mismunandi kröfum yfirvalda á staðnum. Áður en skráin er búin til skal keyra **Gátlistaskýrsluna** til að athuga hvort allar línur innihaldi nauðsynlegar og gildar upplýsingar. Til að stofna skrá:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Intrastat-listi** og velja síðan viðkomandi tengil.
2. Veldu **Intrastat-skýrslu** sem á að gefa upp sem skrá.
3. Ef þú hefur ekki þegar gert þetta skaltu fylla út **Intrastat skýrsluna** handvirkt eða velja **Stinga upp á línum** aðgerðinni.
4. Aðgerðin **Stofna Skrá** er valin.
5. Intrastat-skráin verður vistuð á því sniði sem krafist er.

Þegar skráin hefur verið búin til mun [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa fylla út eftirfarandi upplýsingar um skýrslugerðina:

* **Útflutningsdagsetningin** til að tilgreina dagsetninguna þegar skýrslan hefur verið flutt út.
* **Útflutningstíminn** til að tilgreina tímann þegar skýrslan hefur verið flutt út.

> [!NOTE]  
> Næst þegar þú stofnar skrá munu reitirnir **Útflutningsdagsetning** og **Útflutningstími** aðeins halda upplýsingum um síðustu skrána sem var stofnuð.

## Intrastat-reglur

### Flokkunarlínur

Í **Intrastat Report** línum er engin flokkun eftir neinum reitum. Allar færslur eru afritaðar frá upprunanum þannig að þú getur fundið þér fljótt út frá samsetningu **Upprunategundar** og **Upprunafærslunr.**.

Flokkun sem yfirvöld krefjast verða gefnar upp í útfluttu skránni. Grunnstilla þarf þetta í **Skilgreining gagnaskipta**, sem er hægt að stilla frá grunni. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)

### Skýrslugjöf eigna

Eignir verða sýndar í Intrastat-línunum aðeins ef:

* **Eignabókunartegund** í reitnum **VSK-færsla** er **Kaupverð** og ef **Tegund skjals** er **Reikningur** í tilfelli innkaupa og
* **Eignabókunartegund** í reitnum **VSK-færsla** er **Tekjur við afskráningu** og ef **Tegund skjals** er **Reikningur** í tilfelli sölu.

### Stöður Intrastat-skýrslu

Þegar þú vinnur með **Intrastat skýrslu**  muntu sjá **Staða** reitinn á skjalhausnum. Þú getur fundið eftirfarandi stöðu ásamt tengdum reglum:

* **Opið**: Þessi staða er búin til sjálfkrafa þegar þú býrð til nýja Intrastat skýrslu og þú getur gert allar aðgerðir í þessari stöðu.
* **Gefið út**: [!INCLUDE[prod_short](includes/prod_short.md)] breytir stöðunni sjálfkrafa í *Gefin út* þegar þú býrð til skrá. Frá þeirri stundu geturðu ekki breytt **Intrastat skýrslunni þinni**. Ef breyta þarf einhverju og gefa skýrslu á nýjan leik er hægt að nota aðgerðina **Enduropna** til að enduropna Intrastat-skýrsluna. Þegar skjalið hefur verið opnað aftur er hægt að nota aðgerðina **Gefa út** til að gefa út skjalið aftur.
* **Tilkynnt**: Tilgreinir hvort skattayfirvöld hafa þegar fengið skýrslu um færsluna. Þetta er ekki venjuleg staða heldur sjálfstæður reitur, og jafnvel þótt þú opnaðir Intrastat skýrsluna aftur, myndi hún samt sýna að skráin er þegar búin til fyrir þessa skýrslu.

### Staðsetningar í Intrastat skýrslugerð 

[!INCLUDE[prod_short](includes/prod_short.md)] notar alltaf upplýsingarnar í **Lands-/svæðiskóði** reitnum á **Staðsetningarkorti** síðunni sem landið fyrir **senda frá** eða fyrir **móttöku til** vöru. Þegar þessar upplýsingar eru ekki til eða staðsetning var ekki notuð notar kerfið upplýsingarnar frá  **Fyrirtækisupplýsingunum** síðunni.   

> [!NOTE]  
> Ef fyrirtækið starfar frá fleiri en einu landi virkar Intrastat skýrslur ekki fyrir öll lönd þar sem staðsetningar eru stilltar. Skýrslur eru eingöngu byggðar á aðallandinu þar sem ekki er hægt að nota fjölþjóðaskýrslu eins og er.  

### Þríhyrningaviðskipti í Intrastat

Þríhyrningsviðskipti fela í sér viðskipti milli þriggja landa eða svæða þar sem vörur fara framhjá landi tilkynningarfyrirtækisins. Í Business Central er hægt að auðvelda þetta með [Sleppa sendingu](sales-how-drop-shipment.md) virkninni. Til að virkja þennan valkost skaltu virkja reitinn **Include Drop Shipment** í reitnum **Intrastat Report Setup**.  

Þegar þú virkjar þennan valkost notar kerfið eftirfarandi reglur, en aðeins ef þú ert með **Sleppa sendingu** merkt í **sölupöntuninni**: 

| Tekið á móti frá | Að afhenda til | Áætluð Intrastat niðurstöðu |
|----------|------------|----------------------|
| Land eins og í **Fyrirtækisupplýsingunum** | Land eins og í **Fyrirtækisupplýsingunum** | Engar Intrastat línur |  
| Land eins og í **Fyrirtækisupplýsingunum** | ESB-land er annað en landið í **fyrirtækjaupplýsingunum** | Intrastat flutningslína | 
| Land eins og í **Fyrirtækisupplýsingunum** | Land utan ESB | Engar Intrastat línur |   
| ESB-land er annað en landið í **fyrirtækjaupplýsingunum** | Land eins og í **Fyrirtækisupplýsingunum** | Intrastat móttökulína | 
| ESB-land er annað en landið í **fyrirtækjaupplýsingunum** | ESB-land er annað en landið í **fyrirtækjaupplýsingunum** | Engar Intrastat línur |
| ESB-land er annað en landið í **fyrirtækjaupplýsingunum** | Land utan ESB | Engar Intrastat línur | 
| Land utan ESB | Land eins og í **Fyrirtækisupplýsingunum** | Engar Intrastat línur |  
| Land utan ESB | ESB-land er annað en landið í **fyrirtækjaupplýsingunum** | Engar Intrastat línur |
| Land utan ESB | Land utan ESB | Engar Intrastat línur |   

## Sjá einnig .

[Sett upp Intrastat-skýrslur](finance-how-setup-report-intrastat.md)  
[Fjármálastjórnun](finance.md)  
[Sendu sendingu](sales-how-drop-shipment.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
