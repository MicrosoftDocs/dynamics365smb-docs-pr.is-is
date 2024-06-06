---
title: 'Úrræðaleit: aðgangur að myndavél og staðsetningu'
description: Í þessari grein er lýst hvernig á að leysa úr aðgangi að myndavél og staðsetningarupplýsingum í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.date: 04/01/2021
ms.topic: conceptual
ms.service: dynamics-365-business-central
---

# Úrræðaleit: aðgangur að myndavél og staðsetningu

Þú gætir rekist á nokkur vandamál þegar þú reynir að fá aðgang að myndavél og staðsetningargögn tækis frá [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að finna mögulegar orsakir á bak við þessi vandamál og hvernig á að vinna í kringum þau hér að neðan.

## Tækið verður að vera með myndavél og staðsetningareiginleika

Til að fá aðgang að myndavélinni eða staðsetningu notanda úr tæki verður tækið að vera með myndavél eða staðsetningareiginleika, eftir því sem við á.

Ef tækið þitt er með myndavél og staðsetningareiginleika en þú lendir enn í vandræðum er hugsanlegt að uppfæra þurfi einhverja rekla eða setja þá upp aftur. Jafnvel þótt þú sért ekki viss mælum við alltaf með því að þú uppfærir stýrikerfi tækisins, rekla og vafra í nýjustu útgáfuna til að upplifunin verði sem best.

## Aðgangsheimild ekki virk

Þú þarft að kveikja á almennum aðgangi að myndavél og staðsetningu úr persónuverndarstillingum tækisins og gefa sérstaklega heimild til [!INCLUDE[prod_short](includes/prod_short.md)] fyrir aðgang að þeim. Til að sjá eða breyta heimildum fyrir tæki sem keyrir í Windows skaltu fara í **Stillingar**, velja **Persónuvernd** og svo **Heimildir forrita**. 

Fyrir fartæki þarftu að gefa aðgang að myndavélinni og staðsetningareiginleika í [!INCLUDE[prod_short](includes/prod_short.md)] farsímaforritinu. Til að gera það fyrir  iOS  tæki, farið er í  **Settings**, veljið  **Privacy** og síðan  **myndavél**  eða  **staðsetningu**. Fyrir Android-tæki skal opna **Stillingar**, velja **Forrit og tilkynningar**, **Ítarlegt**, **Heimildastjórnun** og svo **Myndavél** eða **Staðsetning**.

Ef þú ert að nota [!INCLUDE[prod_short](includes/prod_short.md)] í vafra þarftu einnig að gefa [!INCLUDE[prod_short](includes/prod_short.md)] vefsvæðinu aðgang að myndavél eða staðsetningarupplýsingum. Til að skoða eða breyta heimildum vefsvæðis í Microsoft Edge-vafranum skaltu opna **Stillingar**, velja **Heimildir fyrir svæði** og svo **Myndavél** eða **Staðsetning**. Athugaðu að þetta gæti verið mismunandi fyrir aðra vafra.

Sjálfgefið er að tækið eða vafrinn birti beiðni um aðgang að þessum eiginleikum þegar notandinn virkjar þá í fyrsta sinn.

> [!NOTE]  
> Sumir gamlir vafrar veita ekki aðgang að myndavél og staðsetningu. Til dæmis er myndavél ekki í boði í Internet Explorer eða í gömlum Edge-vafra.

## Tenging vefbiðlara er ekki örugg

Eiginleikar myndavélar og staðsetningar eru aðeins tiltækir þegar verið er að opna vefbiðlarann í gegnum SSL-öruggar HTTP-tengingar með `https://` URI-skemanu. 

Eina undantekningin er tenging við `http://localhost`, sem notuð er í þróun og prófanir.


## Vinna með sýndartækni

Þegar þú tengist [!INCLUDE[prod_short](includes/prod_short.md)] í gegnum fjartengt skjáborð eða annan sýndarbúnað er hugsanlegt að aðgangur að myndavél eða staðsetningu sé ekki í boði. Ef svo er skaltu nota efnislegt stjórnkerfi í staðinn.

## Vírusvarnarhugbúnaður
Einhverjar gerðir vírusvarnarhugbúnaðar loka á aðgang að myndavél og staðsetningu. Mundu að athuga stillingar vírusvarnarhugbúnaðarins.

## Sjá einnig
[Innleiðing myndavélarinnar í AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Innleiðing staðsetninga í AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]