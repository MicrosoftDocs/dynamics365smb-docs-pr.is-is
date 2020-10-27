---
title: 'Úrræðaleit: aðgangur að myndavél og staðsetningu'
description: Í þessari grein er lýst hvernig á að leysa úr aðgangi að myndavél og staðsetningarupplýsingum í Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 10/01/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.openlocfilehash: b44044b9ec2c71ad3b99f25b4a941a3ab473ca4f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912022"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="e2ea6-103">Úrræðaleit: aðgangur að myndavél og staðsetningu</span><span class="sxs-lookup"><span data-stu-id="e2ea6-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="e2ea6-104">Þú gætir rekist á nokkur vandamál þegar þú reynir að fá aðgang að myndavél og staðsetningargögn tækis frá [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e2ea6-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="e2ea6-105">Hægt er að finna mögulegar orsakir á bak við þessi vandamál og hvernig á að vinna í kringum þau hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="e2ea6-106">Tækið verður að vera með myndavél og staðsetningareiginleika</span><span class="sxs-lookup"><span data-stu-id="e2ea6-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="e2ea6-107">Til að fá aðgang að myndavélinni eða staðsetningu notanda úr tæki verður tækið að vera með myndavél eða staðsetningareiginleika, eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="e2ea6-108">Ef tækið þitt er með myndavél og staðsetningareiginleika en þú lendir enn í vandræðum er hugsanlegt að uppfæra þurfi einhverja rekla eða setja þá upp aftur.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="e2ea6-109">Jafnvel þótt þú sért ekki viss mælum við alltaf með því að þú uppfærir stýrikerfi tækisins, rekla og vafra í nýjustu útgáfuna til að upplifunin verði sem best.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="e2ea6-110">Aðgangsheimild ekki virk</span><span class="sxs-lookup"><span data-stu-id="e2ea6-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="e2ea6-111">Þú þarft að kveikja á almennum aðgangi að myndavél og staðsetningu úr persónuverndarstillingum tækisins og gefa sérstaklega heimild til [!INCLUDE[prodshort](includes/prodshort.md)] fyrir aðgang að þeim.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prodshort](includes/prodshort.md)] to access them.</span></span> <span data-ttu-id="e2ea6-112">Til að sjá eða breyta heimildum fyrir tæki sem keyrir í Windows skaltu fara í **Stillingar** , velja **Persónuvernd** og svo **Heimildir forrita** .</span><span class="sxs-lookup"><span data-stu-id="e2ea6-112">For example, to see or change permissions for a device running on Windows, go to **Settings** , choose **Privacy** , and then **App permissions** .</span></span> 

<span data-ttu-id="e2ea6-113">Fyrir fartæki þarftu að gefa aðgang að myndavélinni og staðsetningareiginleika í [!INCLUDE[prodshort](includes/prodshort.md)] farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prodshort](includes/prodshort.md)] Mobile App.</span></span> <span data-ttu-id="e2ea6-114">Til að gera það fyrir iOS-tæki skaltu opna **Stillingar** , velja **Persónuvernd** og svo **Myndavél** eða **Staðsetning** .</span><span class="sxs-lookup"><span data-stu-id="e2ea6-114">To do so for an iOS device, go to **Settings** , choose **Privacy** , and then **Camera** or **Location** .</span></span> <span data-ttu-id="e2ea6-115">Fyrir Android-tæki skal opna **Stillingar** , velja **Forrit og tilkynningar** , **Ítarlegt** , **Heimildastjórnun** og svo **Myndavél** eða **Staðsetning** .</span><span class="sxs-lookup"><span data-stu-id="e2ea6-115">For Android devices go to **Settings** , choose **Apps & Notifications** , **Advanced** , **Permission Manager** , and then **Camera** or **Location** .</span></span>

<span data-ttu-id="e2ea6-116">Ef þú ert að nota [!INCLUDE[prodshort](includes/prodshort.md)] í vafra þarftu einnig að gefa [!INCLUDE[prodshort](includes/prodshort.md)] vefsvæðinu aðgang að myndavél eða staðsetningarupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-116">In addition, if you are using [!INCLUDE[prodshort](includes/prodshort.md)] in a browser, you must also grant the [!INCLUDE[prodshort](includes/prodshort.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="e2ea6-117">Til að skoða eða breyta heimildum vefsvæðis í Microsoft Edge-vafranum skaltu opna **Stillingar** , velja **Heimildir fyrir svæði** og svo **Myndavél** eða **Staðsetning** .</span><span class="sxs-lookup"><span data-stu-id="e2ea6-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings** , choose **Site Permissions** , and then **Camera** or **Location** .</span></span> <span data-ttu-id="e2ea6-118">Athugaðu að þetta gæti verið mismunandi fyrir aðra vafra.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="e2ea6-119">Sjálfgefið er að tækið eða vafrinn birti beiðni um aðgang að þessum eiginleikum þegar notandinn virkjar þá í fyrsta sinn.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="e2ea6-120">Sumir gamlir vafrar veita ekki aðgang að myndavél og staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="e2ea6-121">Til dæmis er myndavél ekki í boði í Internet Explorer eða í gömlum Edge-vafra.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="e2ea6-122">Tenging vefbiðlara er ekki örugg</span><span class="sxs-lookup"><span data-stu-id="e2ea6-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="e2ea6-123">Eiginleikar myndavélar og staðsetningar eru aðeins tiltækir þegar verið er að opna vefbiðlarann í gegnum SSL-öruggar HTTP-tengingar með `https://` URI-skemanu.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="e2ea6-124">Eina undantekningin er tenging við `http://localhost`, sem notuð er í þróun og prófanir.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="e2ea6-125">Unnið með sýndartækni</span><span class="sxs-lookup"><span data-stu-id="e2ea6-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="e2ea6-126">Þegar þú tengist [!INCLUDE[prodshort](includes/prodshort.md)] í gegnum fjartengt skjáborð eða annan sýndarbúnað er hugsanlegt að aðgangur að myndavél eða staðsetningu sé ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-126">When connecting to [!INCLUDE[prodshort](includes/prodshort.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="e2ea6-127">Ef svo er skaltu nota efnislegt stjórnkerfi í staðinn.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="e2ea6-128">Vírusvarnarhugbúnaður</span><span class="sxs-lookup"><span data-stu-id="e2ea6-128">Antivirus Software</span></span>
<span data-ttu-id="e2ea6-129">Einhverjar gerðir vírusvarnarhugbúnaðar loka á aðgang að myndavél og staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="e2ea6-130">Mundu að athuga stillingar vírusvarnarhugbúnaðarins.</span><span class="sxs-lookup"><span data-stu-id="e2ea6-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2ea6-131">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e2ea6-131">See Also</span></span>
[<span data-ttu-id="e2ea6-132">Innleiðing myndavélarinnar í AL</span><span class="sxs-lookup"><span data-stu-id="e2ea6-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="e2ea6-133">Innleiðing staðsetninga í AL</span><span class="sxs-lookup"><span data-stu-id="e2ea6-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
