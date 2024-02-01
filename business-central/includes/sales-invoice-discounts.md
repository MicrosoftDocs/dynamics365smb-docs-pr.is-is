---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Þegar allar vörur hafa verið settar inn í línur er hægt að reikna út reikningsafsláttinn fyrir allt söluskjalið með því að velja aðgerðina **Reikna út reikningsafslátt**.

Afslátturinn er reiknaður út frá öllum línum í söluskjalinu þar sem hakað er í gátreitinn **Leyfa reikningsafslátt**. Reikningsafslættir eru sjálfgefið leyfðir. Línur með kostnaðarauka eru hins vegar til dæmis ekki teknar með í útreikningi reikningsafsláttar. Til að nota afslátt á slíkar línur skal færa inn gildi í reitinn **Línuafsláttarupphæð** í línunum.  

> [!NOTE]
> Reitirnir **Leyfa reikningsafsl.** og **Línuafsláttarupphæð** eru sjálfgefið faldir í línum. Ef reitirnir eru ekki tiltækir geturðu bætt þeim við með því að sérsníða síðuna. Sjá  [Sérsníða vinnusvæðið til að fá frekari upplýsingar](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

> [!TIP]
> Ef reiturinn **Reikna reikn.afsl.** er valinn á síðunni **Sölugrunnur** þá hefur reikningsafslátturinn verið reiknaður sjálfvirkt. Þegar útreikningurinn er mismunandi, eftir því um hvers konar söluskjal er að ræða.
>
> Ef þú ert að nota sölupöntun er afslátturinn reiknaður út þegar þú bætir við línu. Fyrir öll önnur söluskjöl, t.d. sölureikninga, er afslátturinn reiknaður út þegar þú gerir eina af eftirfarandi aðgerðum:
>
> * Skoða tölfræði
> * Skoða prufuskýrslu
> * Prenta
> * Færsla

Þú skilgreinir skilmála reikningsafsláttar fyrir viðskiptamann á síðunni **Reikningsafsl. viðskm.**. Kerfið notar gjaldmiðilskóðann í sölureikningnum til að finna skilmála reikningsafsláttar í samsvarandi gjaldmiðli.

Ef þú hefur ekki skilgreint reikningsafslætti fyrir erlenda gjaldmiðla eru afsláttarskilmálar á síðunni **Reikningsafsl. viðskm.** notaðir til að reikna afsláttinn. Útreikningurinn notar staðbundinn gjaldmiðil og gengi sem var gilt á bókunardagsetningu skjalsins.
