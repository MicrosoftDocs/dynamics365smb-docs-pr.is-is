---
title: "Nota forstillingar til að flokka tengiliði"
description: "Setja upp spurningalista forstillingar til að auðvelda flokkun á viðskiptatengiliðum"
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 05/09/2018
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 00cfce8b467040a4de419c1b59a258c0eacf0b9a
ms.contentlocale: is-is
ms.lasthandoff: 05/15/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="53ecf-103">Nota spurningalista forstillingar til að flokka viðskiptatengiliði</span><span class="sxs-lookup"><span data-stu-id="53ecf-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="53ecf-104">Hægt er að setja upp spurningalista sem á að nota þegar upplýsingar um forstillingu tengiliða eru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="53ecf-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="53ecf-105">Innan hvers spurningalista er hægt að setja upp þær mismunandi spurningar sem spyrja á tengiliðina.</span><span class="sxs-lookup"><span data-stu-id="53ecf-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="53ecf-106">Einnig er hægt að keyra spurningalistann til að svara sjálfkrafa nokkrum spurningum samkvæmt gögnum um tengiliði, viðskiptamenn eða lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="53ecf-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="53ecf-107">Til að bæta við spurningalista forstillingar</span><span class="sxs-lookup"><span data-stu-id="53ecf-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="53ecf-108">Velja skal táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Uppsetning spurningalisti** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="53ecf-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="53ecf-109">Á flipanum **Heim** í flokknum **Nýtt** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="53ecf-109">On the **Home** tab, in the **New** group, choose **New**.</span></span>  
3.  <span data-ttu-id="53ecf-110">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="53ecf-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="53ecf-111">Til að bæta spurningum við spurningalista forstillingar</span><span class="sxs-lookup"><span data-stu-id="53ecf-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="53ecf-112">Veljið viðeigandi spurningalista forstillingar og síðan í flipanum **Heim**, í flokknum **Vinna úr**, skal velja **Breyta uppsetningu spurningalista**.</span><span class="sxs-lookup"><span data-stu-id="53ecf-112">Choose the relevant profile questionnaire, and then on the **Home** tab, in the **Process** group, choose **Edit Questionnaire Setup**.</span></span>  
2.  <span data-ttu-id="53ecf-113">Í fyrstu auðu línunni reitnum **Tegund**, veljið **Spurning** ritið spurninguna í reitinn **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="53ecf-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="53ecf-114">Aðrir reitir í línunni eru fylltir út.</span><span class="sxs-lookup"><span data-stu-id="53ecf-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="53ecf-115">Í næstu auðu línu er smellt á reitinn **Tegund**, valið **Svar** og svarið ritað í reitinn **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="53ecf-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="53ecf-116">Í reitnum **Forgangur** veljið forganginn.</span><span class="sxs-lookup"><span data-stu-id="53ecf-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="53ecf-117">Í reitunum **Frá virði** og **Til virðis** skilgreinið bil.</span><span class="sxs-lookup"><span data-stu-id="53ecf-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="53ecf-118">Tengiliðir sem fá stig innan skilgreinda bilsins fá svarið.</span><span class="sxs-lookup"><span data-stu-id="53ecf-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="53ecf-119">Skrefin eru endurtekin til að færa inn allar spurningar og svör í spurningalistanum.</span><span class="sxs-lookup"><span data-stu-id="53ecf-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="53ecf-120">Þegar búið er að stofna spurningalista þarf að stofna tengiliðaflokkanir til að flokka tengiliðina.</span><span class="sxs-lookup"><span data-stu-id="53ecf-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="53ecf-121">Einnig er hægt að setja fram spurningar sem eru metnar sjálfkrafa í samræmi við upplýsingar tengiliðarspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="53ecf-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="53ecf-122">Ef færð er inn spurning sem er svarað sjálfkrafa skal velja <STRONG>Lína</STRONG> og svo <STRONG>Upplýs. um spurningar</STRONG> til að færa inn skilyrðin sem notuð eru til að svara spurningunni sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="53ecf-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="53ecf-123">Sjálfvirk flokkun tengiliða</span><span class="sxs-lookup"><span data-stu-id="53ecf-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="53ecf-124">Hægt er að flokka tengiliði sjálfvirkt eftir viðskiptamanna-, lánardrottna-, og tengiliðaupplýsingum með því að setja upp sjálfvirkt svöruðum forstillingarspurningum í glugganum **Uppsetning spurningalisti forstillingar**.</span><span class="sxs-lookup"><span data-stu-id="53ecf-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions in the **Profile Questionnaire Setup** window.</span></span>  

> [!NOTE]
> <span data-ttu-id="53ecf-125">Aðeins er hægt að flokka tengiliði sem skráðir eru sem viðskiptamenn á grunni viðskiptamannaupplýsinga og aðeins er flokka tengilið sem skráðir eru sem lánardrottnar á grundvelli lánardrottnaupplýsinga.</span><span class="sxs-lookup"><span data-stu-id="53ecf-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="53ecf-126">Sjálfvirk flokkun uppfærist ekki sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="53ecf-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="53ecf-127">Þar af leiðandi er ráðlegt að uppfæra spurningalista forstillingar þegar viðskiptamanna-, lánardrottna- eða tengiliðaupplýsingum sem þeir byggja á er breytt.</span><span class="sxs-lookup"><span data-stu-id="53ecf-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="53ecf-128">Þegar sjálfvirkt svaraðar forstillingarspurningar hafa verið settar upp, ef þú úthlutar tengiliði forstillingarspurningar sem innihalda þessar spurningar, mun [!INCLUDE[d365fin](includes/d365fin_md.md)] sjálfkrafa úthluta réttu svörunum fyrir tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="53ecf-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="53ecf-129">Dæmi</span><span class="sxs-lookup"><span data-stu-id="53ecf-129">Example</span></span>
<span data-ttu-id="53ecf-130">Hægt er að flokka tengiliði eftir því hversu mikið þeir hafa keypt:</span><span class="sxs-lookup"><span data-stu-id="53ecf-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53ecf-131"><strong>Svar</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="53ecf-132"><strong>Gildir um</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53ecf-133">A</span><span class="sxs-lookup"><span data-stu-id="53ecf-133">A</span></span></p></td>
<td><p><span data-ttu-id="53ecf-134">tengiliði sem keyptu fyrir 500.000 SGM eða meira</span><span class="sxs-lookup"><span data-stu-id="53ecf-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53ecf-135">B</span><span class="sxs-lookup"><span data-stu-id="53ecf-135">B</span></span></p></td>
<td><p><span data-ttu-id="53ecf-136">tengiliði sem keyptu fyrir 100.000 til 499.999 SGM</span><span class="sxs-lookup"><span data-stu-id="53ecf-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53ecf-137">C</span><span class="sxs-lookup"><span data-stu-id="53ecf-137">C</span></span></p></td>
<td><p><span data-ttu-id="53ecf-138">tengiliði sem keyptu fyrir 99.999 SGM eða minna</span><span class="sxs-lookup"><span data-stu-id="53ecf-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="53ecf-139">Það er gert með því að fylla í gluggann **Uppsetning á spurningalista forstillingar** sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="53ecf-139">To do this, fill in the **Profile Questionnaire Setup** window as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53ecf-140"><strong>Tegund</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="53ecf-141"><strong>Lýsing</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="53ecf-142"><strong>Sjálfvirk flokkun</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="53ecf-143"><strong>Frá virði</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="53ecf-144"><strong>Til virðis</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53ecf-145">Spurning</span><span class="sxs-lookup"><span data-stu-id="53ecf-145">Question</span></span></p></td>
<td><p><span data-ttu-id="53ecf-146">ABC-flokkun</span><span class="sxs-lookup"><span data-stu-id="53ecf-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="53ecf-147">Smellt er til að færa inn gátmerki</span><span class="sxs-lookup"><span data-stu-id="53ecf-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53ecf-148">Svar</span><span class="sxs-lookup"><span data-stu-id="53ecf-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="53ecf-149">A</span><span class="sxs-lookup"><span data-stu-id="53ecf-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53ecf-150">500,000</span><span class="sxs-lookup"><span data-stu-id="53ecf-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53ecf-151">Svar</span><span class="sxs-lookup"><span data-stu-id="53ecf-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="53ecf-152">B</span><span class="sxs-lookup"><span data-stu-id="53ecf-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53ecf-153">100,000</span><span class="sxs-lookup"><span data-stu-id="53ecf-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="53ecf-154">499,999</span><span class="sxs-lookup"><span data-stu-id="53ecf-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53ecf-155">Svar</span><span class="sxs-lookup"><span data-stu-id="53ecf-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="53ecf-156">C</span><span class="sxs-lookup"><span data-stu-id="53ecf-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="53ecf-157">99,999</span><span class="sxs-lookup"><span data-stu-id="53ecf-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="53ecf-158">Síðan er glugginn **Upplýs. forstillingarspurningar** fylltur út sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="53ecf-158">Then fill in the **Profile Question Details** window as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53ecf-159"><strong>Reitur</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="53ecf-160"><strong>Gildi</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="53ecf-161"><strong>Flokkunarreitur viðskiptavinar</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="53ecf-162"><emphasis>Sala (SGM)</emphasis></span><span class="sxs-lookup"><span data-stu-id="53ecf-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53ecf-163"><strong>Flokkunaraðferð</strong></span><span class="sxs-lookup"><span data-stu-id="53ecf-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="53ecf-164"><emphasis>Skilgreint virði</emphasis></span><span class="sxs-lookup"><span data-stu-id="53ecf-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="53ecf-165">Þegar spurningalista forstillingar sem inniheldur þessa spurningu er úthlutað á tengilið færir kerfið sjálfkrafa viðeigandi svar fyrir tengiliðinn í forstillingarlínurnar á tengiliðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="53ecf-165">When you assign the profile questionnaire containing this question to a contact, the program automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="53ecf-166">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="53ecf-166">See Also</span></span>
[<span data-ttu-id="53ecf-167">Einstaklingstengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="53ecf-167">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="53ecf-168">Stofna einstaklingstengilið</span><span class="sxs-lookup"><span data-stu-id="53ecf-168">Create Contact Persons</span></span>](marketing-how-create-contact-persons.md)  
[<span data-ttu-id="53ecf-169">Fyrirtækjatengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="53ecf-169">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  

