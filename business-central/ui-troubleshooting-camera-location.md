---
title: 'Úrræðaleit: aðgangur að myndavél og staðsetningu'
description: Í þessari grein er lýst hvernig á að leysa úr aðgangi að myndavél og staðsetningarupplýsingum í Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 04/22/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.openlocfilehash: 10338040ddcfb64dd91e9e55f607280e99720403
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781136"
---
# <a name="troubleshooting-accessing-camera-and-location"></a>Úrræðaleit: aðgangur að myndavél og staðsetningu

Þú gætir rekist á nokkur vandamál þegar þú reynir að fá aðgang að myndavél og staðsetningargögn tækis frá [!INCLUDE[prodshort](includes/prodshort.md)]. Hægt er að finna mögulegar orsakir á bak við þessi vandamál og hvernig á að vinna í kringum þau hér að neðan.

## <a name="device-must-have-camera-and-location-capabilities"></a>Tækið verður að vera með myndavél og staðsetningareiginleika

Til að fá aðgang að myndavélinni eða staðsetningu notanda úr tæki verður tækið að vera með myndavél eða staðsetningareiginleika, eftir því sem við á.

Ef tækið þitt er með myndavél og staðsetningareiginleika en þú lendir enn í vandræðum er hugsanlegt að uppfæra þurfi einhverja rekla eða setja þá upp aftur. Jafnvel þótt þú sért ekki viss mælum við alltaf með því að þú uppfærir stýrikerfi tækisins, rekla og vafra í nýjustu útgáfuna til að upplifunin verði sem best.

## <a name="access-permissions-not-enabled"></a>Aðgangsheimild ekki virk

Þú þarft að kveikja á almennum aðgangi að myndavél og staðsetningu úr persónuverndarstillingum tækisins og gefa sérstaklega heimild til [!INCLUDE[prodshort](includes/prodshort.md)] fyrir aðgang að þeim. Til að sjá eða breyta heimildum fyrir tæki sem keyrir í Windows skaltu fara í **Stillingar**, velja **Persónuvernd** og svo **Heimildir forrita**. 

Fyrir fartæki þarftu að gefa aðgang að myndavélinni og staðsetningareiginleika í [!INCLUDE[prodshort](includes/prodshort.md)] farsímaforritinu. Til að gera það fyrir iOS-tæki skaltu opna **Stillingar**, velja **Persónuvernd** og svo **Myndavél** eða **Staðsetning**. Fyrir Android-tæki skal opna **Stillingar**, velja **Forrit og tilkynningar**, **Ítarlegt**, **Heimildastjórnun** og svo **Myndavél** eða **Staðsetning**.

Ef þú ert að nota [!INCLUDE[prodshort](includes/prodshort.md)] í vafra þarftu einnig að gefa [!INCLUDE[prodshort](includes/prodshort.md)] vefsvæðinu aðgang að myndavél eða staðsetningarupplýsingum. Til að skoða eða breyta heimildum vefsvæðis í Microsoft Edge-vafranum skaltu opna **Stillingar**, velja **Heimildir fyrir svæði** og svo **Myndavél** eða **Staðsetning**. Athugaðu að þetta gæti verið mismunandi fyrir aðra vafra.

Sjálfgefið er að tækið eða vafrinn birti beiðni um aðgang að þessum eiginleikum þegar notandinn virkjar þá í fyrsta sinn.

> [!NOTE]  
> Sumir gamlir vafrar veita ekki aðgang að myndavél og staðsetningu. Til dæmis er myndavél ekki í boði í Internet Explorer eða í gömlum Edge-vafra.

## <a name="web-client-connection-not-secure"></a>Tenging vefbiðlara er ekki örugg

Eiginleikar myndavélar og staðsetningar eru aðeins tiltækir þegar verið er að opna vefbiðlarann í gegnum SSL-öruggar HTTP-tengingar með `https://` URI-skemanu. 

Eina undantekningin er tenging við `http://localhost`, sem notuð er í þróun og prófanir.


## <a name="working-with-virtualization-technologies"></a>Unnið með sýndartækni

Þegar þú tengist [!INCLUDE[prodshort](includes/prodshort.md)] í gegnum fjartengt skjáborð eða annan sýndarbúnað er hugsanlegt að aðgangur að myndavél eða staðsetningu sé ekki í boði. Ef svo er skaltu nota efnislegt stjórnkerfi í staðinn.

## <a name="antivirus-software"></a>Vírusvarnarhugbúnaður
Einhverjar gerðir vírusvarnarhugbúnaðar loka á aðgang að myndavél og staðsetningu. Mundu að athuga stillingar vírusvarnarhugbúnaðarins.

## <a name="see-also"></a>Sjá einnig
[Innleiðing myndavélarinnar í AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Innleiðing staðsetninga í AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
