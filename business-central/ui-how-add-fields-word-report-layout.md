---
title: Hvernig á að bæta reitum við Word-skýrsluútlit
description: Þetta efnisatriði lýsir ferlinu við að bæta reitum í gagnasafni skýrslu við fyrirliggjandi Word-skýrsluútlit fyrir skýrslu.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/25/2021
ms.author: jswymer
---

# <a name="work-with-word-layouts" />Vinna með Word-útlit

Word-skýrsluútlit ákvarðar efni og snið skýrslunnar þegar hún er forskoðuð og prentuð úr Business Central. Þú býrð til og breytir þessum útlitum með Microsoft Word.

[![Dæmi um skjal word-skýrsluútlits fyrir Business Central.](media/word-layout.png)](media/word-layout.png#lightbox) 

Þegar þú breytir Word-skýrsluútliti tilgreinir þú reiti í gagnasafni skýrslunnar sem eiga að vera í skýrslu og hvernig reitunum er raðað. Þú skilgreinir líka almennt snið skýrslunnar, t.d. leturgerð og stærð texta, spássíu og bakgrunnsmyndir. Þú raðar yfirleitt efni skýrslunnar með því að bæta töflum við útlitið.

Til að gera almennar sniðsbreytingar og útlitsbreytingar, t.d. að breyta leturgerð, bæta við og breyta töflu eða að fjarlægja gagnareit, skal einfaldlega nota grunnbreytingarvalkosti Word, líkt og gert er fyrir öll önnur Word skjöl.

Ef þú ert að hanna Word-skýrsluútlit frá grunni eða bæta við nýjum gagnareitum skaltu byrja með því að bæta við töflu sem er með raðir og dálka sem munu að endingu innihalda gagnareitina.

> [!TIP]  
> Sýna hnitanetslínur töflu þannig að jaðrar töfluhólfanna sjáist. Mundu að fela hnitanetslínurnar þegar breytingum er lokið. Til að sýna eða fela töfluhnitalínur velurðu töfluna og svo, undir **Útlit** á flipanum **Tafla** velurðu **Skoða hnitalínur**.

## <a name="embedding-fonts-in-word-layouts-for-consistency" />Innfelling leturgerða í Word Layouts fyrir samræmi

Til að tryggja að skýrslur birtist alltaf og prentist með fyrirhuguðum leturgerðum, óháð því hvar notendur opna eða prenta skýrslurnar, geturðu fellt inn leturgerðirnar í Word skjalinu. Hins vegar geta innfelldar leturgerðir aukið stærð Word-skrá umtalsvert. Nánari upplýsingar um innfellingu leturgerða í Word, sjá [Fella inn leturgerðir í Word, PowerPoint eða Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

## <a name="adding-data-fields" />Bæta við gagnareitum

Gagnasafn skýrslu getur samanstaðið af reitum sem birta merki, gögn og myndir. Þetta efnisatriði lýsir ferlinu við að bæta reitum í gagnasafni skýrslu við fyrirliggjandi Word-skýrsluútlit fyrir skýrslu. Reitum er bætt við með því að nota Word sérsniðinn XML-hluta fyrir skýrsluna og bæta við efnisstjórnun sem varpar í reiti gagnamengis skýrslunnar. Bæting reita þarfnast einhverrar þekkingar á gagnamengi skýrslunnar þannig að hægt er að bera kennsl á reitina sem á að bæta við útlitið.  
  
> [!NOTE]  
>  Ekki er hægt að breyta innbyggðu skýrsluútliti<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

### <a name="to-open-the-custom-xml-part-for-the-report-in-word" /><a name="OpenXMLPart"></a>Til að opna sérsniðinn XML-hluta fyrir skýrsluna í Word
  
1. Ef það er ekki þegar opið skal opna Word-sniðmátsskjal fyrir skýrslu í Word.  
  
     Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md).  
  
2. Sýna flipann **Hönnuður** á borða Microsoft Word.  
  
     Sjálfgefið er að **Hönnuður** er ekki sýnilegur í borðanum. Frekari upplýsingar eru í [Sýna flipann Hönnuður á borðanum](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3. Á flipanum **Developer** skal velja **XML-vörpunarsvæði**.  
  
4. Á svæðinu **XML-vörpun**, á fellilistanum **Sérsniðinn XML-hluti** velurðu sérsniðinn XML-hluta fyrir [!INCLUDE[prod_short](includes/prod_short.md)]-skýrslu, sem er vanalega síðast á listanum. Heiti sérstillta XML-hlutans er á eftirfarandi sniði:  
  
     `urn:microsoft-dynamics-nav/reports/<report_name>/<ID>`  

     `<report_name>` er heitið sem er úthlutað á skýrsluna. 

     `<ID>` er kenninúmer skýrslunnar.  
  
     Eftir að þú velur sérsniðna XML-hlutann sýnir XML-vörpunarglugginn merki og reitastjórnun sem er í boði fyrir skýrsluna.  
  
### <a name="to-add-a-label-or-data-field" />Til að bæta við merki eða gagnareit
  
1. Setja skal bendilinn á skjalið þar sem þú vilt setja inn stjórnhnapp.  
  
2. Á svæðinu **XML-vörpun** skal hægrismella á stjórnhnappinn sem á að bæta við, velja **Fella inn í efnisstjórnun** og velja svo **Ósniðinn texti**.  
  
    > [!NOTE]  
    >  Ekki er hægt að bæta við reit með því að slá handvirkt inn heiti gagnamengisreits í efnisstjórnun. Þú verður að nota **XML-vörpun** svæðið til að varpa reitunum.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list" />Til að bæta við endurteknum línum gagnareita til að búa til lista
  
1. Í töflunni skal bæta við töflulínu sem inniheldur dálk fyrir hvern reit sem á að endurtaka.  
  
   Þessi lína virkar sem staðgengill fyrir endurtekna reiti.  
  
2. Veldu alla röðina.  
  
3. Á svæðinu **XML-vörpun** skal hægrismella á stjórnhnappinn sem samsvarar skýrslugagnaatriðinu sem inniheldur reitina sem á að endurtaka, velja **Fella inn í efnisstjórnun** og velja svo **Endurtaka**.  
  
4. Bættu endurtekna reitinum við röð svona:  
  
    1. Bendillinn er settur á dálk.  
  
    2. Á svæðinu **XML-vörpun** skal hægrismella á stjórnhnappinn sem á að bæta við, velja **Fella inn í efnisstjórnun** og velja svo **Ósniðinn texti**.  
  
    3. Endurtakið skref a og b fyrir hvern reit.  
  
## <a name="adding-image-fields" />Bæta við myndareitum

Gagnasafn skýrslu getur innihaldið reit sem inniheldur mynd, t.d. fyrirtækjamerki eða mynd af hlut. Til að bæta við mynd úr skýrslugagnamenginu er sett inn efnisstjórnunin **Mynd**.  
  
Myndir birtast efst í hægra horni efnisstýringar og laga stærð sína sjálfvirkt þannig að þær passi við mörk efnisstjórnunar.  
  
> [!IMPORTANT]  
> Aðeins er hægt að bæta við myndum á sniði sem Word styður, t.d. .bmp, .jpeg, og .png skráargerðir. Ef þú bætir við mynd á sniði sem Word styður ekki færðu villu þegar þú keyrir skýrsluna úr [!INCLUDE[prod_short](includes/prod_short.md)] biðlaranum.  
  
### <a name="to-add-an-image" />Til að bæta við mynd
  
1. Setja skal bendilinn á skjalið þar sem þú vilt setja inn stjórnhnapp.  
  
2. Á svæðinu **XML-vörpun** skal hægrismella á stjórnhnappinn sem á að bæta við, velja **Fella inn í efnisstjórnun** og velja svo **Mynd**.  
  
3. Til að auka eða minnka myndastærðina dregurðu stærðarhandfang frá eða að miðju efnisstjórnunar.  

## <a name="removing-label-and-data-fields" /><a name="RemoveField"></a> Merkja- og gagnareitir fjarlægðir

Merkimiða- og gagnareitir skýrslu eru í efnisstjórnun í Word. Eftirfarandi mynd sýnir efnisstýringu þegar hún er valin í Word-skjalinu.  

![Efnisstýring fyrir reit í Word-skýrsluútliti.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

Heiti merkisins eða heiti gagnareits er birt í efnisstjórnun. Í dæminu er heiti reitsins CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field" />Til að fjarlægja merki eða gagnareit

1. Hægri-smellir á reitinn sem á að eyða og svo **Fjarlægja efnisstýringu**.  

     Efnisstjórnunin er fjarlægð en reitarheitið er til staðar sem texti.  

2. Eyða skal textanum sem eftir er eftir því sem þörf krefur.

## <a name="custom-xml-part-overview" />Sérsniðinn XML-hluti yfirlit

Word-skýrsluútlit byggja á *sérsniðnum XML-hlutum*. Sérsniðinn XML-hluti fyrir skýrslu samanstendur af þáttum sem samsvara gagnahlutum, dálkum og merkingum sem saman mynda gagnamengi skýrslunnar. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Sérsniðinn XML-hluti er notaður til að varpa gögnunum í skýrslu þegar skýrslan er keyrð.

### <a name="xml-structure-of-custom-xml-part" />XML bygging sérsniðins XML-hluta

Eftirfarandi tafla sýnir einfaldað yfirlit yfir XML af sérsniðnum XML-hluta.  
  
|XML-einingar|Description|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Haus|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|XML nafnbil tilgreint. `<reportname>` er heitið sem er úthlutað á skýrsluna. `<id>` er auðkennið sem tengt er úthlutað á skýrsluna.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Inniheldur öll merki fyrir skýrsluna.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Merkjaeiningar sem tengjast dálkum hafa sniðið `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Merkjaeiningar hafa sniðið `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Merkimiðar eru skráðir í stafrófsröð.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Gögn og dálkar á efsta stigi Dálkar eru listaðir í stafrófsröð.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Gögn og dálkar sem eru ívafin á efsta stigi gagnahlutar. Dálkar eru listaðir í stafrófsröð undir viðkomandi gagnahlut.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Lokar atriði.|  
  
### <a name="custom-xml-part-in-word" />Sérsniðinn XML-hluti í Word

 Í Word opnarðu sérsniðinn XML-hluta á svæðinu **XML-vörpun** og notar svo svæðið til að varpa einingum í efnisstjórnun í Word-skjalinu. Svæðið **XML-vörpun** er aðgengilegt úr flipanum **Hönnuður** (nánari upplýsingar er að finna í [Sýna flipann Hönnuður á borðanum](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).  
  
 Einingarnar í **XML vörpun** svæðinu birtast með uppsetningu sem svipar til XML upprunans. Merkimiðareitir eru flokkaðir saman undir sameiginlegri einingu í **Merkimiðar** og gagnaatriðum og dálkum er raðað í stigveldisskipan sem samsvarar XML-upprunanum, með dálkar í stafrófsröð. Einingar eru auðkenndar á dálkheiti eins og það er skilgreint í gagnasafni skýrslunnar í AL-kóða. Frekari upplýsingar eru í [Skilgreina gagnasafni](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).  
  
 Eftirfarandi mynd sýnir einfaldan sérsniðinn XML-hluta úr fyrri hluta í **XML-vörpun** svæðinu í Word skjali.  
  
 ![Hluti af XML-vörpunarsvæði í word.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
* Til að bæta merki eða reit við útlitið er sett inn efnisstjórnun sem varpar í eininguna á svæðinu **XML-vörpun**.  
  
* Til að búa til endurteknar raðir af dálkum skal setja inn **Endurtekna** efnisstjórnun fyrir yfirgögn einingarinnar, og bæta svo við efnisstjórnun fyrir dálkana.  
  
* Fyrir merki er sá texti sem birtist í skýrslunni sem mynduð er gildi eiginleikans **Myndatexti** fyrir reitinn í gagnaatriðatöflunni (ef merkið tengist dálki í skýrslugagnamenginu), eða merki í Report Label Designer, (ef merkið tengist ekki dálki í gagnamenginu).  
  
* Tungumál merkisins sem birtist þegar skýrslan er keyrð fer eftir tungumálsstillingu skýrsluhlutarins.  
  
## <a name="see-also" />Sjá einnig

[Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
