---
title: "Hvernig á að bæta reitum við Word-skýrsluútlit | Microsoft Docs"
description: "Lýsir ferlinu við að bæta reitum í gagnasafni skýrslu við fyrirliggjandi Word-skýrsluútlit fyrir skýrslu."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 30d515822fd3e1ca3bf5b83e2bbc4e0841bea9cc
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="add-fields-to-a-word-report-layout"></a><span data-ttu-id="ffce0-103">Bæta reitum við Word-skýrsluútlit</span><span class="sxs-lookup"><span data-stu-id="ffce0-103">Add Fields to a Word Report Layout</span></span>
<span data-ttu-id="ffce0-104">Gagnasafn skýrslu getur samanstaðið af reitum sem birta merki, gögn og myndir.</span><span class="sxs-lookup"><span data-stu-id="ffce0-104">A report dataset can consist of fields that display labels, data, and images.</span></span> <span data-ttu-id="ffce0-105">Þetta efnisatriði lýsir ferlinu við að bæta reitum í gagnasafni skýrslu við fyrirliggjandi Word-skýrsluútlit fyrir skýrslu.</span><span class="sxs-lookup"><span data-stu-id="ffce0-105">This topic describes the procedure for adding fields of a report dataset to an existing Word report layout for a report.</span></span> <span data-ttu-id="ffce0-106">Reitum er bætt við með því að nota Word sérsniðinn XML-hluta fyrir skýrsluna og bæta við efnisstjórnun sem varpar í reiti gagnamengis skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="ffce0-106">You add fields by using the Word custom XML part for the report and adding content controls that map to the fields of the report dataset.</span></span> <span data-ttu-id="ffce0-107">Bæting reita þarfnast einhverrar þekkingar á gagnamengi skýrslunnar þannig að hægt er að bera kennsl á reitina sem á að bæta við útlitið.</span><span class="sxs-lookup"><span data-stu-id="ffce0-107">Adding fields requires that you have some knowledge of the report's dataset so that you can identify the fields that you want to add to the layout.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="ffce0-108">Ekki er hægt að breyta innbyggðu skýrsluútliti<!--Onprem. Built-in layouts can only be modified by using the development environment-->.</span><span class="sxs-lookup"><span data-stu-id="ffce0-108">You cannot modify built-in report layouts<!--Onprem. Built-in layouts can only be modified by using the development environment-->.</span></span>  

##  <a name="OpenXMLPart"></a><span data-ttu-id="ffce0-109">Til að opna sérsniðinn XML-hluta fyrir skýrsluna í Word</span><span class="sxs-lookup"><span data-stu-id="ffce0-109">To open the Custom XML part for the Report in Word</span></span>  
  
1.  <span data-ttu-id="ffce0-110">Ef það er ekki þegar opið skal opna Word-sniðmátsskjal fyrir skýrslu í Word.</span><span class="sxs-lookup"><span data-stu-id="ffce0-110">If not already open, then open the Word report layout document in Word.</span></span>  
  
     <span data-ttu-id="ffce0-111">Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="ffce0-111">For more information, see [Create and Modify a Custom Report Layout](ui-how-create-custom-report-layout.md).</span></span>  
  
2.  <span data-ttu-id="ffce0-112">Sýna flipann **Hönnuður** á borða Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="ffce0-112">Show the **Developer** tab in the ribbon of Microsoft Word.</span></span>  
  
     <span data-ttu-id="ffce0-113">Sjálfgefið er að **Hönnuður** er ekki sýnilegur í borðanum.</span><span class="sxs-lookup"><span data-stu-id="ffce0-113">By default, the **Developer** tab is not shown in the ribbon.</span></span> <span data-ttu-id="ffce0-114">Frekari upplýsingar eru í [Sýna flipann Hönnuður á borðanum](http://go.microsoft.com/fwlink/?LinkID=389631).</span><span class="sxs-lookup"><span data-stu-id="ffce0-114">For more information, see [Show the Developer Tab on the Ribbon](http://go.microsoft.com/fwlink/?LinkID=389631).</span></span>  
  
3.  <span data-ttu-id="ffce0-115">Á flipanum **Developer** skal velja **XML-vörpunarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="ffce0-115">On the **Developer** tab, choose **XML Mapping Pane**.</span></span>  
  
4.  <span data-ttu-id="ffce0-116">Á svæðinu **XML-vörpun**, á fellilistanum **Sérsniðinn XML-hluti** velurðu sérsniðinn XML-hluta fyrir ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->-skýrslu, sem er vanalega síðast á listanum.</span><span class="sxs-lookup"><span data-stu-id="ffce0-116">In the **XML Mapping** pane, in the **Custom XML Part** dropdown list, choose the custom XML part for ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]--> report, which is typically last in the list.</span></span> <span data-ttu-id="ffce0-117">Heiti sérstillta XML-hlutans er á eftirfarandi sniði:</span><span class="sxs-lookup"><span data-stu-id="ffce0-117">The name of the custom XML part has the following format:</span></span>  
  
     <span data-ttu-id="ffce0-118">urn:microsoft-dynamics-nav/reports/*skýrslu_heiti*/*/Kenni*</span><span class="sxs-lookup"><span data-stu-id="ffce0-118">urn:microsoft-dynamics-nav/reports/*report_name*/*ID*</span></span>  
  
     <span data-ttu-id="ffce0-119">*skýrsluheiti* er heitið sem er úthlutað á skýrsluna<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]--> í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="ffce0-119">*report_name* is the name that is assigned to the report<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.</span></span>  
  
     <span data-ttu-id="ffce0-120">*Auðkenni* er kenninúmer skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="ffce0-120">*ID* is the identification number of the report.</span></span>  
  
     <span data-ttu-id="ffce0-121">Eftir að þú velur sérsniðna XML-hlutann sýnir XML-vörpunarglugginn merki og reitastjórnun sem er í boði fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="ffce0-121">After you select the custom XML part, the XML Mapping pane displays the labels and field controls that are available for the report.</span></span>  
  
### <a name="to-add-a-label-or-data-field"></a><span data-ttu-id="ffce0-122">Til að bæta við merki eða gagnareit</span><span class="sxs-lookup"><span data-stu-id="ffce0-122">To add a label or data field</span></span>  
  
1.  <span data-ttu-id="ffce0-123">Setja skal bendilinn á skjalið þar sem þú vilt setja inn stjórnhnapp.</span><span class="sxs-lookup"><span data-stu-id="ffce0-123">Place your cursor in the document where you want to add the control.</span></span>  
  
2.  <span data-ttu-id="ffce0-124">Á svæðinu **XML-vörpun** skal hægrismella á stjórnhnappinn sem á að bæta við, velja **Fella inn í efnisstjórnun** og velja svo **Ósniðinn texti**.</span><span class="sxs-lookup"><span data-stu-id="ffce0-124">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Plain Text**.</span></span>  
  
    > [!NOTE]  
    >  <span data-ttu-id="ffce0-125">Ekki er hægt að bæta við reit með því að slá handvirkt inn heiti gagnamengisreits í efnisstjórnun.</span><span class="sxs-lookup"><span data-stu-id="ffce0-125">You cannot add a field by manually typing the dataset field name in the content control.</span></span> <span data-ttu-id="ffce0-126">Þú verður að nota **XML-vörpun** svæðið til að varpa reitunum.</span><span class="sxs-lookup"><span data-stu-id="ffce0-126">You must use the **XML Mapping** pane to map the fields.</span></span>  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a><span data-ttu-id="ffce0-127">Til að bæta við endurteknum línum gagnareita til að búa til lista</span><span class="sxs-lookup"><span data-stu-id="ffce0-127">To add repeating rows of data fields to create a list</span></span>  
  
1.  <span data-ttu-id="ffce0-128">Í töflunni skal bæta við töflulínu sem inniheldur dálk fyrir hvern reit sem á að endurtaka.</span><span class="sxs-lookup"><span data-stu-id="ffce0-128">In a table, add a table row that includes a column for each field that you want repeated.</span></span>  
  
     <span data-ttu-id="ffce0-129">Þessi lína virkar sem staðgengill fyrir endurtekna reiti.</span><span class="sxs-lookup"><span data-stu-id="ffce0-129">This row will act as a placeholder for the repeating fields.</span></span>  
  
2.  <span data-ttu-id="ffce0-130">Veldu alla röðina.</span><span class="sxs-lookup"><span data-stu-id="ffce0-130">Select the entire row.</span></span>  
  
3.  <span data-ttu-id="ffce0-131">Á svæðinu **XML-vörpun** skal hægrismella á stjórnhnappinn sem samsvarar skýrslugagnaatriðinu sem inniheldur reitina sem á að endurtaka, velja **Fella inn í efnisstjórnun** og velja svo **Endurtaka**.</span><span class="sxs-lookup"><span data-stu-id="ffce0-131">In the **XML Mapping** pane, right-click the control that corresponds to the report data item that contains the fields that you want repeated, choose **Insert Content Control**, and then choose **Repeating**.</span></span>  
  
4.  <span data-ttu-id="ffce0-132">Bættu endurtekna reitinum við röð svona:</span><span class="sxs-lookup"><span data-stu-id="ffce0-132">Add the repeating fields to the row as follows:</span></span>  
  
    1.  <span data-ttu-id="ffce0-133">Bendillinn er settur á dálk.</span><span class="sxs-lookup"><span data-stu-id="ffce0-133">Place your pointer in a column.</span></span>  
  
    2.  <span data-ttu-id="ffce0-134">Á svæðinu **XML-vörpun** skal hægrismella á stjórnhnappinn sem á að bæta við, velja **Fella inn í efnisstjórnun** og velja svo **Ósniðinn texti**.</span><span class="sxs-lookup"><span data-stu-id="ffce0-134">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Plain Text**.</span></span>  
  
    3.  <span data-ttu-id="ffce0-135">Endurtakið skref a og b fyrir hvern reit.</span><span class="sxs-lookup"><span data-stu-id="ffce0-135">For each field, repeat steps a and b.</span></span>  
  
## <a name="adding-image-fields"></a><span data-ttu-id="ffce0-136">Bæat avið myndareitum</span><span class="sxs-lookup"><span data-stu-id="ffce0-136">Adding Image Fields</span></span>  
 <span data-ttu-id="ffce0-137">Gagnasafn skýrslu getur innihaldið reit sem inniheldur mynd, t.d. fyrirtækjamerki eða mynd af hlut.</span><span class="sxs-lookup"><span data-stu-id="ffce0-137">A report dataset can include a field that contains an image, such as a company logo or a picture of an item.</span></span> <span data-ttu-id="ffce0-138">Til að bæta við mynd úr skýrslugagnamenginu er sett inn efnisstjórnunin **Mynd**.</span><span class="sxs-lookup"><span data-stu-id="ffce0-138">To add an image from the report dataset, you insert a **Picture** content control.</span></span>  
  
 <span data-ttu-id="ffce0-139">Myndir birtast efst í hægra horni efnisstýringar og laga stærð sína sjálfvirkt þannig að þær passi við mörk efnisstjórnunar.</span><span class="sxs-lookup"><span data-stu-id="ffce0-139">Images align in the top-left corner of the content control and resize automatically in proportion to fit the boundary of the content control.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="ffce0-140">Aðeins er hægt að bæta við myndum á sniði sem Word styður, t.d. .bmp, .jpeg, og .png skráargerðir.</span><span class="sxs-lookup"><span data-stu-id="ffce0-140">You can only add images that have a format that is supported by Word, such as .bmp, .jpeg, and .png file types.</span></span> <span data-ttu-id="ffce0-141">Ef þú bætir við mynd á sniði sem Word styður ekki færðu villu þegar þú keyrir skýrsluna úr ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]--> biðlaranum.</span><span class="sxs-lookup"><span data-stu-id="ffce0-141">If you add an image that has a format that is not supported by Word, you will get an error when you run the report from the ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]--> client.</span></span>  
  
#### <a name="to-add-an-image"></a><span data-ttu-id="ffce0-142">Til að bæta við mynd</span><span class="sxs-lookup"><span data-stu-id="ffce0-142">To add an image</span></span>  
  
1.  <span data-ttu-id="ffce0-143">Setja skal bendilinn á skjalið þar sem þú vilt setja inn stjórnhnapp.</span><span class="sxs-lookup"><span data-stu-id="ffce0-143">Place your pointer in the document where you want to add the control.</span></span>  
  
2.  <span data-ttu-id="ffce0-144">Á svæðinu **XML-vörpun** skal hægrismella á stjórnhnappinn sem á að bæta við, velja **Fella inn í efnisstjórnun** og velja svo **Mynd**.</span><span class="sxs-lookup"><span data-stu-id="ffce0-144">In the **XML Mapping** pane, right-click the control that you want to add, choose **Insert Content Control**, and then choose **Picture**.</span></span>  
  
3.  <span data-ttu-id="ffce0-145">Til að auka eða minnka myndastærðina dregurðu stærðarhandfang frá eða að miðju efnisstjórnunar.</span><span class="sxs-lookup"><span data-stu-id="ffce0-145">To increase or decrease the image size, drag a sizing handle away from or towards the center of the content control.</span></span>  

## <a name="custom-xml-part-overview"></a><span data-ttu-id="ffce0-146">Sérsniðinn XML-hluti yfirlit</span><span class="sxs-lookup"><span data-stu-id="ffce0-146">Custom XML Part Overview</span></span>
<span data-ttu-id="ffce0-147">Word-skýrsluútlit byggja á *sérsniðnum XML-hlutum*.</span><span class="sxs-lookup"><span data-stu-id="ffce0-147">Word report layouts are built on *custom XML parts*.</span></span> <span data-ttu-id="ffce0-148">Sérsniðinn XML-hluti fyrir skýrslu samanstendur af þáttum sem samsvara gagnahlutum, dálkum og merkingum sem saman mynda gagnamengi skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="ffce0-148">A custom XML part for a report consists of elements that correspond to the data items, columns, and labels that comprise the report's dataset.</span></span> <span data-ttu-id="ffce0-149"><!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Sérsniðinn XML-hluti er notaður til að varpa gögnunum í skýrslu þegar skýrslan er keyrð.</span><span class="sxs-lookup"><span data-stu-id="ffce0-149"><!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->The custom XML part is used to map the data into a report when the report is run.</span></span>

  
### <a name="xml-structure-of-custom-xml-part"></a><span data-ttu-id="ffce0-150">XML bygging sérsniðins XML-hluta</span><span class="sxs-lookup"><span data-stu-id="ffce0-150">XML Structure of Custom XML Part</span></span>  
<span data-ttu-id="ffce0-151">Eftirfarandi tafla sýnir einfaldað yfirlit yfir XML af sérsniðnum XML-hluta.</span><span class="sxs-lookup"><span data-stu-id="ffce0-151">The following table provides a simplified overview of the XML of a custom XML part.</span></span>  
  
|<span data-ttu-id="ffce0-152">XML-einingar</span><span class="sxs-lookup"><span data-stu-id="ffce0-152">XML Elements</span></span>|<span data-ttu-id="ffce0-153">Description</span><span class="sxs-lookup"><span data-stu-id="ffce0-153">Description</span></span>|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|<span data-ttu-id="ffce0-154">Haus</span><span class="sxs-lookup"><span data-stu-id="ffce0-154">Header</span></span>|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|<span data-ttu-id="ffce0-155">XML nafnbil tilgreint.</span><span class="sxs-lookup"><span data-stu-id="ffce0-155">XML namespace specification.</span></span> <span data-ttu-id="ffce0-156">`<reportname>` er heitið sem er úthlutað á skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="ffce0-156">`<reportname>` is the name that is assigned to the report.</span></span> <span data-ttu-id="ffce0-157">`<id>` er auðkennið sem tengt er úthlutað á skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="ffce0-157">`<id>` is the ID that is assigned to the report.</span></span>|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|<span data-ttu-id="ffce0-158">Inniheldur öll merki fyrir skýrsluna.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--></span><span class="sxs-lookup"><span data-stu-id="ffce0-158">Contains all the labels for the report.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--></span></span><br /><span data-ttu-id="ffce0-159">-   Merkjaeiningar sem tengjast dálkum hafa sniðið `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.</span><span class="sxs-lookup"><span data-stu-id="ffce0-159">-   Label elements that are related to columns have the format `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.</span></span><br /><span data-ttu-id="ffce0-160">-  Merkjaeiningar hafa sniðið `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.</span><span class="sxs-lookup"><span data-stu-id="ffce0-160">-  Label elements have the format `<LabelName>LabelName</LableName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.</span></span><br /><span data-ttu-id="ffce0-161">-   Merkimiðar eru skráðir í stafrófsröð.</span><span class="sxs-lookup"><span data-stu-id="ffce0-161">-   Labels are listed in alphabetical order.</span></span>|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|<span data-ttu-id="ffce0-162">Gögn og dálkar á efsta stigi</span><span class="sxs-lookup"><span data-stu-id="ffce0-162">Top-level data item and columns.</span></span> <span data-ttu-id="ffce0-163">Dálkar eru listaðir í stafrófsröð.</span><span class="sxs-lookup"><span data-stu-id="ffce0-163">Columns are listed in alphabetical order.</span></span><!--OnPrem <br /><br /> The element names and values are determined by the [Name Property-duplicate](../FullExperience/Name%20Property-duplicate.md) of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|<span data-ttu-id="ffce0-164">Gögn og dálkar sem eru ívafin á efsta stigi gagnahlutar.</span><span class="sxs-lookup"><span data-stu-id="ffce0-164">Data items and columns that are nested in the top-level data item.</span></span> <span data-ttu-id="ffce0-165">Dálkar eru listaðir í stafrófsröð undir viðkomandi gagnahlut.</span><span class="sxs-lookup"><span data-stu-id="ffce0-165">Columns are listed in alphabetical order under the respective data item.</span></span>|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|<span data-ttu-id="ffce0-166">Lokar atriði.</span><span class="sxs-lookup"><span data-stu-id="ffce0-166">Closing element.</span></span>|  
  
### <a name="custom-xml-part-in-word"></a><span data-ttu-id="ffce0-167">Sérsniðinn XML-hluti í Word</span><span class="sxs-lookup"><span data-stu-id="ffce0-167">Custom XML Part in Word</span></span>  
 <span data-ttu-id="ffce0-168">Í Word opnarðu sérsniðinn XML-hluta á svæðinu **XML-vörpun** og notar svo svæðið til að varpa einingum í efnisstjórnun í Word-skjalinu.</span><span class="sxs-lookup"><span data-stu-id="ffce0-168">In Word, you open the custom XML part in the **XML Mapping** pane, and then use the pane to map elements to content controls in the Word document.</span></span> <span data-ttu-id="ffce0-169">Svæðið **XML-vörpun** er aðgengilegt úr flipanum **Hönnuður** (nánari upplýsingar er að finna í [Sýna flipann Hönnuður á borðanum](http://go.microsoft.com/fwlink/?LinkID=389631)).</span><span class="sxs-lookup"><span data-stu-id="ffce0-169">The **XML Mapping** pane is accessible from the **Developer** tab (for more information, see [Show the Developer Tab on the Ribbon](http://go.microsoft.com/fwlink/?LinkID=389631)).</span></span>  
  
 <span data-ttu-id="ffce0-170">Einingarnar í **XML vörpun** svæðinu birtast með uppsetningu sem svipar til XML upprunans.</span><span class="sxs-lookup"><span data-stu-id="ffce0-170">The elements in the **XML Mapping** pane appear in a structure that is similar to the XML source.</span></span> <span data-ttu-id="ffce0-171">Merkimiðareitir eru flokkaðir saman undir sameiginlegri einingu í **Merkimiðar** og gagnaatriðum og dálkum er raðað í stigveldisskipan sem samsvarar XML-upprunanum, með dálkar í stafrófsröð.</span><span class="sxs-lookup"><span data-stu-id="ffce0-171">Label fields are grouped under a common **Labels** element and data item and columns are arranged in a hierarchal structure that corresponds to the XML source, with columns listed in alphabetical order.</span></span> <span data-ttu-id="ffce0-172">Einingar eru auðkenndar af heiti sínu eins og það er skilgreint í eiginleikanum Heiti í innbyggða skýrsluhönnuðinum í ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.</span><span class="sxs-lookup"><span data-stu-id="ffce0-172">Elements are identified by their name as defined by the Name property in Report Dataset Designer in ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.</span></span>  
  
 <span data-ttu-id="ffce0-173">Eftirfarandi mynd sýnir einfaldan sérsniðinn XML-hluta úr fyrri hluta í **XML-vörpun** svæðinu í Word skjali.</span><span class="sxs-lookup"><span data-stu-id="ffce0-173">The following figure illustrates the simple custom XML part from the previous section in the **XML Mapping** pane of a Word document.</span></span>  
  
 <span data-ttu-id="ffce0-174">![Hluti af XML vörpunarsvæði í word](media/nav_reportlayout_xmlmappingpane.png "NAV_SkýrslaÚtlit_XMLVörpunarSvæði")</span><span class="sxs-lookup"><span data-stu-id="ffce0-174">![Clip of the XML Mapping pane in word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")</span></span>  
  
-   <span data-ttu-id="ffce0-175">Til að bæta merki eða reit við útlitið er sett inn efnisstjórnun sem varpar í eininguna á svæðinu **XML-vörpun**.</span><span class="sxs-lookup"><span data-stu-id="ffce0-175">To add a label or field to the layout, you insert a content control that maps to the element in the **XML Mapping** pane.</span></span>  
  
-   <span data-ttu-id="ffce0-176">Til að búa til endurteknar raðir af dálkum skal setja inn **Endurtekna** efnisstjórnun fyrir yfirgögn einingarinnar, og bæta svo við efnisstjórnun fyrir dálkana.</span><span class="sxs-lookup"><span data-stu-id="ffce0-176">To create repeating rows of columns, insert a **Repeating** content control for the parent data item element, and then add content control for the columns.</span></span>  
  
-   <span data-ttu-id="ffce0-177">Fyrir merki er sá texti sem birtist í skýrslunni sem mynduð er gildi eiginleikans **Myndatexti** fyrir reitinn í gagnaatriðatöflunni (ef merkið tengist dálki í skýrslugagnamenginu), eða merki í Report Label Designer, (ef merkið tengist ekki dálki í gagnamenginu).</span><span class="sxs-lookup"><span data-stu-id="ffce0-177">For labels, the actual text that appears in the generated report is the value of the **Caption** property for the field in the data item table (if the label is related to the column in the report dataset) or a label in the Report Label Designer (if the label is not related to a column in the dataset).</span></span>  
  
-   <span data-ttu-id="ffce0-178">Tungumál merkisins sem birtist þegar skýrslan er keyrð fer eftir tungumálsstillingu skýrsluhlutarins.</span><span class="sxs-lookup"><span data-stu-id="ffce0-178">The language of the label that is displayed when you run the report depends on the language setting of the report object.</span></span> <!--OnPrem For more information, see [Multiple Document Languages](../FullExperience/Viewing%20the%20Application%20in%20Different%20Languages.md).-->  
  
## <a name="see-also"></a><span data-ttu-id="ffce0-179">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ffce0-179">See Also</span></span>  
 [<span data-ttu-id="ffce0-180">Búa til og breyta sérsniðnu skýrsluútliti</span><span class="sxs-lookup"><span data-stu-id="ffce0-180">Create and Modify a Custom Report Layout</span></span>](ui-how-create-custom-report-layout.md)   
