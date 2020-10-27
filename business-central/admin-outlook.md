---
title: Notkun Business Central með Outlook| Microsoft Docs
description: Þessi þjónusta er rækilega samþætt Microsoft 365, sem gerir þér kleift að stjórna öllum fyrirtækja- og tölvupóstsamskiptum við viðskiptamenn og lánardrottna í Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2167336c2fe4555a28d3d3eeaf4829d815d8fa04
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915736"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Notkun Business Central sem fyrirtækjainnhólf í Outlook

[!INCLUDE[d365fin](includes/d365fin_md.md)] kynnir möguleikann á að stjórna samskiptum innan fyrirtækisins við viðskiptamenn og lánardrottna beint í Microsoft Outlook. Með [!INCLUDE[d365fin](includes/d365fin_md.md)] Outlook innbótinni er hægt að skoða fjárhagsleg gögn sem tengjast viðskiptamönnum og lánardrottnum, ásamt því að semja og senda fjárhagsleg skjöl, svo sem tilboð og reikninga.  

## <a name="getting-the-add-in"></a>Að fá viðbótina
Það er auðvelt að hefjast handa með [!INCLUDE[d365fin](includes/d365fin_md.md)]-innbótinni fyrir Outlook. Í uppsetningarleiðbeiningum með hjálp fyrir **Setja upp fyrirtækjainnhólf í Outlook** er hægt að setja upp tenginguna fyrir sjálfan þig eða fyrirtækið þitt ef fyrirtækið notar Microsoft 365. Sláðu einfaldlega inn notandanafn og lykilorð fyrir Microsoft 365 ef þú ert beðið er um það og láttu okkur vita ef þú vilt fá sent sýnishorn af tölvupóstskeyti. Innbót [!INCLUDE[d365fin](includes/d365fin_md.md)] er þá sjálfkrafa bætt við Outlook. Frekari upplýsingar er að finna í [Lágmarkskröfur fyrir Outlook](product-requirements.md#outlook).  

Þegar þú opnar Outlook muntu sjá tölvupóst frá *Dynamics 365 Business Central-stjórnanda* . Nýju innbótunum er bætt við Outlook-borðann og í vafranum er hægt að sjá [!INCLUDE[prodshort](includes/prodshort.md)]-innbæturnar beint fyrir ofan eða neðan meginmál tölvupóstskeytisins. Innbæturnar eru uppfærðar reglulega og þú munt fá tilkynningu um að ný útgáfa sé tilbúin fyrir þig í Outlook.  

> [!TIP]
> Ef þú notar nýja Outlook á vefnum, geta [!INCLUDE[prodshort](includes/prodshort.md)]-innbæturnar verið faldar undir **Fleiri aðgerðir** . Ef þú notar innbótina oft er hægt að festa hana þannig að hún sjáist alltaf strax. Frekari upplýsingar eru í [Notkun innbóta í Outlook á vefnum](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16)  

Ef þú vinnur með fleiri en eitt [!INCLUDE[prodshort](includes/prodshort.md)] fyrirtæki geturðu auðveldlega skipt á milli fyrirtækja í Outlook. Í aðgerðastiku viðbótarinnar  skaltu velja **Fleiri aðgerðir** og þá geturðu séð valkostinn til að skipta á milli fyrirtækja.  

<!--TEMP-->
> [!NOTE]
> Ef skipt er á milli fyrirtækja þarf [!INCLUDE[prodshort](includes/prodshort.md)] 2019 útgáfutímabil 2 eða nýrri að vera í [útgáfuáætluninni](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Sum fyrirtæki sem nota Microsoft 365  takmarka heimildir notenda til að taka í notkun innbætur. Því þarf að ganga úr skugga um að þú hafir Microsoft 365  áskrift sem felur í sér tölvupóst og gerir það mögulegt að nota innbætur. Ef þú samt prófa innbæturnar geturðu [prófað Microsoft 365  endurgjaldslaust](https://www.microsoft.com/microsoft-365/try).  

## <a name="using-the-contact-insights-add-in"></a>Notaðu viðbótina Talnagögn tengiliða
Segjum að þú fáir tölvupóst frá viðskiptavini sem vill fá tilboð í sumum hlutum. Beint í Outlook, getur þú opnað [!INCLUDE[d365fin](includes/d365fin_md.md)] viðbótina, sem viðurkennir sendanda sem viðskiptavin, og opnar viðskiptavinakortið fyrir fyrirtæki hans. Í þessu yfirliti má sjá yfirlit yfir upplýsingar um viðskiptamann, auk þess sem hægt er að kafa niður fyrir nánari upplýsingar um tiltekin skjöl. Einnig má fá frekari upplýsingar um söluferil viðskiptamannsins. Ef það er nýr tengiliður getur þú búið hann til sem nýjan viðskiptamann í [!INCLUDE[d365fin](includes/d365fin_md.md)] án þess að yfirgefa Outlook.  

Í innbótinni er hægt að stofna sölutilboð og senda það aftur til þessa viðskiptamanns án þess að fara úr Outlook. Allar upplýsingar sem þarf að senda sölutilboðið eru tiltækar í viðskiptainnhólfinu í Outlook.  
Þegar búið er að færa inn gögnin er hægt að bóka tilboðið. Síðan er hægt að senda það með tölvupósti. [!INCLUDE[d365fin](includes/d365fin_md.md)] býr til PDF-skrá með sölutilboðinu og tengir það við tölvupóstskilaboðin sem notandi býr til í innbótinni.  

Á sama hátt, ef þú færð tölvupóst frá seljanda geturðu notað viðbótina til að vinna með söluaðilum og kaupa reikninga.  

Stundum viltu sjá fleiri reiti en þú sérð í viðbótinni, svo sem þegar þú vilt fylla út línur í reikningi. Til að fá aðeins meira vinnurými er hægt að setja innbótina í aðskilda síðu. Hún er enn hluti af Outlook en vinnuýmið er meira. Þegar gögn eru færð inn í skjalið í aðskilda glugganum eru breytingarnar vistaðar sjálfkrafa. Þegar þú ert búinn að slá inn gögn fyrir skjalið geturðu valið **Í lagi** hnappinn. Með því að velja innbótina í Outlook endurnýjast skjalið sjálfkrafa með breytingunum sem veru gerðar í aðskilda glugganum.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Búðu til reikninga frá fundum þínum
Sum fyrirtæki skrá alla reikninga sem hægt er að greiða í Outlook dagbókinni. Með [!INCLUDE[d365fin](includes/d365fin_md.md)] getur þú búið til reikninginn fyrir viðskiptavininn rétt frá dagatalinu: Opnaðu skipunina og þá getur þú opnað [!INCLUDE[d365fin](includes/d365fin_md.md)] viðbótina, skoðað uppliggjandi upplýsingar eða búið til reikning eða annað söluskrá þarna.  

## <a name="doing-quick-document-lookup"></a>Fljótleg uppfletting skjala
[!INCLUDE[d365fin](includes/d365fin_md.md)] Skjalatenglar viðbótin gefur þér skjótan aðgang að skjölum sem nefnd eru í tölvupósti. Innbótin er tiltæk fyrir tölvupóstskilaboð ef fylgiskjalsnúmer er þekkt í meginmáli skeytisins. Opnun innbótarinnar veitir skjótan aðgang að skjalinu.  

Til dæmis, ef þú færð tölvupóstskeyti sem nefnir textann *S-QUO100* , skilgreinir [!INCLUDE[d365fin](includes/d365fin_md.md)] sem sölutilboð og svo þú getur opnað þetta skjal í Outlook. Í Outlook skal velja hnappinn **Tenglar á skjöl** beint fyrir ofan meginmál tölvupóstskilaboðanna. Í Outlook Web App skal velja *S-QUO1001* textann í meginmáli tölvupóstskilaboðanna.  

Í viðbótinni Document Links er hægt að breyta og grípa til aðgerða með skjalinu, rétt eins og þú getur í [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Bæta við viðbótunum handvirkt
Í sumum tilfellum fá viðbætur ekki sjálfkrafa bætt við Outlook. Jafnvel þótt þú eða samstarfsmaður hljóp aðstoðaruppsetningarhandbókina fyrir hönd fyrirtækisins, gæti [!INCLUDE[d365fin](includes/d365fin_md.md)] ekki birst í Outlook. Ef þú finnur fyrir þessu vandamáli geturðu bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)] viðbótunum handvirkt.  

Í fyrsta lagi verður þú að staðfesta að þú hafir aðgang að viðbótunum á Microsoft 365 reikningnum þínum. Opnaðu einfaldlega Outlook í vafra, opnaðu skilaboð, veldu **Fleiri aðgerðir** (...) efst í skilaboðunum og síðan, neðst í listanum, skaltu velja **Sækja innbætur** . Þetta opnar síðuna **Innbætur fyrir Outlook** þar sem hægt er að virkja [!INCLUDE[prodshort](includes/prodshort.md)] fyrir Outlook. Þá, þegar þú vafrar aftur til Outlook, ætti [!INCLUDE[prodshort](includes/prodshort.md)] að vera tiltæk.  

Á svipaðan hátt í Outlook skjáborðsþjóninum getur þú staðfest að [!INCLUDE[d365fin](includes/d365fin_md.md)] er skráð á síðunni **Sækja innbætur** .  

Í báðum tilvikum, ef [!INCLUDE[d365fin](includes/d365fin_md.md)] er ennþá ekki tiltækt, verður þú að fá innskráningarskrárnar. Nánari upplýsingar fást hjá Microsoft 365 stjórnandanum þínum.

## <a name="using-other-email-accounts"></a>Notkun annarra tölvupóstreikninga

Viðbæturnar eru ætlaðar til notkunar með Microsoft 365 . Ef þú notar [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum veit stjórnandinn þinn hvort þú getir notað [!INCLUDE[prodshort](includes/prodshort.md)]-innbæturnar í Outlook. Frekari upplýsingar er að finna í greinunum [Hvaða netfang get ég notað með [!INCLUDE[prodshort](includes/prodshort.md)]?](across-faq.md#email) og [Eiginleikar sem krefjast sérstakra aðstæðna](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances?toc=/dynamics365/business-central/toc.json) og hlutanum [Hvers vegna virkar ekki Outlook-innbótin fyrir notendur mína?](/dynamics365/business-central/dev-itpro/faq#why-doesnt-the-outlook-add-in-work-for-my-users?toc=/dynamics365/business-central/toc.json) í algengum spurningum í stjórnunarefninu.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Hafist handa](product-get-started.md)  
[Sækja Business Central í fartækið mitt](install-mobile-app.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Fjármál](finance.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Lágmarkskröfur fyrir Outlook](product-requirements.md#outlook)  
[Notkun innbóta í Outlook á vefnum](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  
