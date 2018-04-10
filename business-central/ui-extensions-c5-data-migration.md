---
title: "Notkun C5 gagnaflutningsviðbótar | Microsoft Docs"
description: "Þessi viðbót er notuð til að flytja viðskiptamenn,lánardrottna, vörur og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a>C5 gagnaflutningsviðbót fyrir Business Central
Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna, vara og fjárhagsreikninga úr Microsoft Dynamics C5 2012 í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hægt er að flytja elrdi færslur fyrir fjárhagsreikning.

> [!Note]
> Fyrirtækið í [!INCLUDE[d365fin](includes/d365fin_md.md)] má ekki innihalda gögn. Að auki skaltu ekki búa til viðskiptavini, lánardrottna, vörur eða reikninga fyrr en flutningur lýkur.

##<a name="what-data-is-migrated"></a>Hvaða gögn eru flutt?
Eftirfarandi gögn eru flutt fyrir hverja einingu:

**Viðskiptavinum**
* Birgðageymsla
* Land
* Vídd viðskiptavina (deild, miðstöð, tilgangur)
* Afhendingarmáti
* Sölumaður
* Greiðsluskilmálar
* Greiðslumáti
* Verðflokkur viðskiptamanns
* Reikningsafsláttur viðskiptavinar

Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:

* Uppsetning bókunar viðskiptavinar
* Almenn færslubókarkeyrsla
* Opnar færslur (í viðskiptamannabók)

**Lánardrottnar**
* Birgðageymsla
* Land
* Vídd lánardrottins (deild, miðstöð, tilgangur)
* Reikningsafsláttur
* Afhendingarmáti
* Innkaupaaðili
* Greiðsluskilmálar
* Greiðslumáti
* Afsláttur lánardrottnareikninga

Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:

* Bókunarflokkur lánardrottins
* Almenn færslubókarkeyrsla
* Opnar færslur (fjárhagsfærslur lánardrottins)

**Birgðir**
* Birgðageymsla
* Land
* Vöruvíddir (deild, miðstöð, tilgangur)
* Sölulínuafslættir
* Afsláttarflokkar viðskiptamanna
* Vöruafsláttarflokkar
* Söluverð
* Tollnúmer
* Mælieiningar
* Vörurakningarkóti
* Verðflokkur viðskiptamanns

Ef reikningar eru fluttir eru eftirfarandi gögn einnig flutt:

* Birgðabókunargrunnur
* Almennur bókunargrunnur
* Birgðabókarkeyrsla
* Opnar færslur (birgðafærslur)

> [!Note]
> Ef opnar færslur eru til staðar sem nota erlenda gjaldmiðla er gengi þeirra einnig flutt inn. Önnur gengi eru ekki flutt inn.

## <a name="to-migrate-data"></a>Til að flytja gögn
Það eru aðeins nokkur skref fólgin í því að flytja út gögn úr C5 og flytja þau inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. Í C5 skaltu nota **Flytja út gagnagrunn** eiginleikann til að flytja út gögnin. Sendu síðan útflutningsmöppuna í þappaða möppu.  
2. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal velja ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Gagnaflutningur** og velja svo **Gagnaflutningur**.  
3. Ljúka skal skrefunum í leiðbeiningum um uppsetningu með hjálp. Gakktu úr skugga um að velja **Flytja inn úr Microsoft Dynamcis C5 2012** sem gagnagjafa.  

> [!Note]
> Fyrirtæki bæta oft við reitum til að sérsníða C5 fyrir tiltekna starfsemi. [!INCLUDE[d365fin](includes/d365fin_md.md)] flytur ekki gögn úr sérsniðnum reitum. Einnig mun flutningur mistakast ef fleiri en 10 sérsniðnir reitir eru til staðar.

## <a name="viewing-the-status-of-the-migration"></a>Skoðun stöðu á flutningi
Nota skal síðuna **Gagnaflutningsyfirlit** til að sjá stöðu flutningsins. Síðan sýnir upplýsingar, svo sem fjöldi færslna sem flutningurinn mun innihalda, stöðu flutningsins og fjölda vara sem hafa verið fluttar og hvort flutningur þeirra tókst. Hún sýnir einnig fjölda villna, gerir þér kleift að rannsaka hvað fór úrskeiðis og, þegar mögulegt er, auðveldar það að fara í færsluna til að laga vandamálin. Nánari upplýsingar eru í næsta hluta þessa efnisatriðis.  

> [!Note]
> Meðan beðið er eftir stöðu flutningsins þarf að uppfæra síðuna til að birta niðurstöðurnar.

## <a name="correcting-errors"></a>Leiðrétting villna
Ef eitthvað fer úrskeiðis og villur koma upp sýnir **Staða** reiturinn **Lokið með villum** og **Villutalning** reiturinn mun sýna fjöldann. Til að skoða lista yfir villurnar er hægt að opna **Villur í gagnaflutningi** síðuna með því að velja:  

* Talan í **Villutalning** reitnum fyrir eininguna.  
* Einingin og svo **Sýna villur** aðgerðin.  

Á **Villur í gagnaflutningi** síðunni, til að laga villu er hægt að velja villuboð og svo **Breyta færslu** til að opna síðu sem sýnir flutt gögn fyrir eininguna. Eftir að þú hefur lagað eina eða fleiri villur getur þú valið **Flytja** til að flytja aðeins einingarnar sem þú lagaðir án þess að þurfa að hefja flutninginn aftur.  

> [!Tip]
> Ef þú hefur lagað fleiri en eina villu geturðu notað **Velja fleira** valkostinn til að velja margar línur til að flytja. Ef villur eru til staðar sem ekki er mikilvægt að laga geturðu valið þær og svo **Sleppa vali**.

> [!Note]
> Ef vörur eru til staðar sem er að finna í uppskrift gætir þú þurft að flytja oftar en einu sinni ef upprunalega varan er ekki stofnuð fyrir afbrigðið sem vísa til hennar. Ef afbrigðið er búið til fyrst getur tilvísunin í upprunalegu vöruna valdið villuboðum.  

## <a name="verifying-data-after-migrating"></a>Staðfesting gagna eftir flutning
Ein leið til að sannreyna að gögnin hafi verið rétt flutt inn er með því að skoða eftirfarandi síður í C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamcis C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Viðskm.færslur| Almennar færslubækur|
|Lánardr.færslur| Almennar færslubækur|
|Birgðafærslur| Birgðabækur|

Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er lotan fyrir fluttu gögnin kölluð **C5MIGRATE**.

## <a name="stopping-data-migration"></a>Stöðvun gagnaflutnings
Þú getur hætt að flytja gögn með því að velja **Hætta við allan flutning**. Ef þú gerir það er líka hætt við allan flutning sem bíður.

## <a name="see-also"></a>Sjá einnig
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)  
[Hafist handa](product-get-started.md) 

