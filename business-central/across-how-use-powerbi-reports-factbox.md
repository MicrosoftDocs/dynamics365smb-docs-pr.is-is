---
title: Birta venjulegar Power BI skýrslur| Microsoft Docs
description: Hægt er að nota Power BI skýrslur til að öðlast frekari innsýn í gögnum í listum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: a8acad8d0be760f567902587acada49ab68e740f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304932"
---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Skoða listagögn í Power BI skýrslum í Business Central

[!INCLUDE[prodlong](includes/prodlong.md)] inniheldur stjórneiningu fyrir upplýsingakassa á mörgum veigamiklum listasíðum sem veita frekari innsýn í gögnin í listanum. Þegar farið er milli lína í listanum er skýrslan uppfærð og síuð fyrir valda færslu. Notandi getur stofnað sérsniðnar skýrslur til að birta í þessum stjórntakka en hér eru nokkrar grunnreglur sem fylgja skal við stofnun skýrslnanna til að tryggja að þær virki sem skyldi.  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power BI. Til að búa til sérsniðnar skýrslur verður þú einnig að hala niður [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Frekari upplýsingar, sjá [Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Gagnamengi skýrslu
Þegar skýrslan er stofnuð í Power BI Desktop skal tilgreina gagnaveitu eða vefþjónustu sem inniheldur gögnin sem tengjast listanum sem á að tengja skýrsluna við. Til dæmis ef notandi vill stofna skýrslu fyrir sölulista skal tryggja að gagnamengið innihaldi upplýsingar sem tengjast sölu.  

Til að afmarka gögn í skýrslum á grundvelli færslunnar sem valin var á listasíðunni verður að nota aðallykil sem skýrslusíu. Aðallykillinn verður að vera hluti af gagnamenginu til að skýrslan verði rétt afmörkuð. Í flestum tilvikum er aðallykill fyrir lista reiturinn **Nr.** .  

## <a name="defining-the-report-filter"></a>Skilgreining á afmörkun skýrslu
Skýrslan þarf að vera með grunnafmörkun skýrslu (ekki síðu eða myndræna afmörkun og ekki ítarlega afmörkun) til að vera rétt afmörkuð í stjórntakka upplýsingakassa í Power BI. Afmörkunin sem er flutt yfir í Power BI skýrsluna af hverri listasíðu byggir á aðallyklinum, eins og lýst er í fyrri hluta.  

Til að skilgreina afmörkun í skýrslunni er aðallykill af listanum yfir tiltæki reitir valinn og síðan er sá reitur dregill og sleppt yfir í hlutann **Afmörkun skýrslu**.  

![Afmörkun skýslu stillt fyrir Aðgerðaskráningu sölureikninga](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Stærð og litur skýrslu
Stærð skýrslu verður að stilla á 325 sinnum 310 pixla. Þetta er áskilið til að kvörðun skýrslunnar verði rétt í því rými sem stjórntakki upplýsingakassa fyrir Power BI leyfir. Til að skilgreina stærð skýrslu skal staðsetja fókus utan svæðis fyrir útlit skýrslu og velja svo tákn fyrir málningarrúllu.

![Breidd og hæð skýrslu stillt fyrir Aðgerðaskráningu sölureikninga](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Hægt er að breyta breidd og hæð skýrslunnar með því að velja **Sérsníða** í reitnum **Tegund**.

Sömuleiðis, ef óskað er að bakgrunnur skýrslunnar renni saman við bakgrunnslit stjórntakka upplýsingakassa Power BI skal skilgreina bakgrunnslit sem *E5E5E5*. Þetta er valfrjálst.  

## <a name="reports-with-multiple-pages"></a>Skýrslur með mörgum síðum
Með Power BI er hægt að stofna eina skýrslu með mörgum síðum. Myndrænir þættir sem notandi vill sjá í listasíðum [!INCLUDE[d365fin](includes/d365fin_md.md)] verða að vera á fyrstu síðu skýrslunnar í Power BI.  

> [!NOTE]  
> Upplýsingakassi fyrir Power BI getur aðeins sýnt fyrstu síðuna í skýrslunni. Ef notandi vill sjá fleiri síður verður að víkka skýrsluna og nota flipana neðst í skýrslunni til að fletta á aðrar síður.  

## <a name="saving-your-report"></a>Vistar skýrsluna

Þegar skýrslan er vistuð er gott verklag að skýrsluheitið innihaldi heiti listasíðunnar sem notandi vill birta skýrsluna á. Til dæmis verður orðið *Lánardrottinn* að koma fyrir einhvers staðar í skýrsluheiti fyrir skýrslur sem notandi vill að verði tiltækar á lista yfir lánardrottna.  

Þetta er ekki skilyrði en mun flýta fyrir ferlinu þegar skýrslur eru valdar. Þegar síða fyrir val á skýrslum er opnuð af listasíðu setjum við inn afmörkun byggða á síðuheitinu til að takmarka hversu margar skýrslur verða birtar.  Hægt er að fjarlægja afmörkunina til að birta heildarlista yfir skýrslur sem eru tiltækar notanda í Power BI.  

## <a name="troubleshooting"></a>Úrræðaleit
Þessi hluti veitir hjáleið fyrir flest dæmigerð vandamál sem komið geta upp þegar Power BI-skýrsla er búin til.  

**Notandi sér enga skýrslu á síðunni Velja skýrslu sem hann vill velja.** Ef notandi getur ekki valið skýrslu er hugsanlega hægt að staðfesta heiti skýrslunnar til að tryggja að heitið innihaldi heiti listasíðunnar. Einnig er hægt að fjarlægja afmörkunina til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.  

**Skýrslan er sótt en er auð, ekki afmörkuð eða afmörkuð með röngum hætti** Sannprófa verður að skýrsluafmörkunin innihaldi réttan aðallykil. Yfirleitt er þetta **Nr.** reitur, en í töflunni **Fjárhagsfærsla**, til dæmis, verður að nota **Færslunr.** reitinn.

**Skýrslunni er hlaðið upp en sýnir síðu sem notandi átti ekki von á að sjá** Sannprófa verður að skýrslan sem notandi vill að birtist sé fyrsta síðan í skýrslunni.  

**Skýrsla er birt með óæskilegum gráum jöðrum, er of lítil eða of stór**

Staðfestið að stærð skýrslu sé stillt á 325 x 310 pixla. Vista skal skýrsluna og síðan endurnýja listasíðuna.  

## <a name="see-also"></a>Sjá einnig

[Gera viðskiptagögn þín virk fyrir Power BI](admin-powerbi.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Hafist handa](product-get-started.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
