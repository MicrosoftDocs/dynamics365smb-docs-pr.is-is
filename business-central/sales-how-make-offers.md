---
title: Gera sölutilboð
description: Lestu um hvernig á að stofna sölutilboð eða skjal með beiðni um tilboð (RFQ) til að skrá tilboð til viðskiptavinar eða tilfangs um að selja vörur samkvæmt tilteknum skilmálum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 02/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="make-sales-quotes"></a>Gera sölutilboð

Búið er til sölutilboð til að skrá tilboðið við viðskiptavin eða tilfang um að selja tilteknar vörur með tilteknum afhendingar- og greiðsluskilmálum. Hægt er að senda sölutilboð til viðskiptamannsins til að miðla tilboðinu. Hægt er að senda skjalið í tölvupósti sem PDF viðhengi. Hægt er að láta meginmálslínur tölvupósts vera útfyllt fyrirfram með tilboði. Nánari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md#to-send-documents-by-email).

Þegar samið er við viðskiptavin eða tilfang er hægt að breyta og endursenda sölutilboðið eins mikið og oft og þörf er á. Þegar viðskiptamaður tekur tilboði, er sölutilboðinu breytt í sölureikning eða sölupöntun þar sem salan er meðhöndluð. Nánari upplýsingar eru í [Reikningsfæra sölu](sales-how-invoice-sales.md) eða [Selja vörur.](sales-how-sell-products.md)

Í flestum tilfellum sendirðu sölutilboð á hugsanlega viðskiptavini. Oft er um að ræða tengilið sem samið er við. Ef viðkomandi samþykkir síðan tilboðið frá þér breytir þú sölutilboðinu í pöntun og skráir tilfangið sem viðskiptavin í [!INCLUDE [prod_short](includes/prod_short.md)]. Í eftirfarandi ferli leggjum við áherslu á tengiliði, en einnig er hægt að senda tilboð til núverandi viðskiptavina.  

## <a name="to-create-a-sales-quote"></a>Sölutilboð búin til:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölutilboð** og velja síðan viðkomandi tengil.
2. Tilgreindu tengilið eða viðskiptavin sem á að senda sölutilboðið til.

    - Ef sölutilboðið er fyrir tengilið sem þegar er til staðar skaltu tilgreina nafnið í **Númer tengiliðar** .  

        Ef sölutilboðið er fyrir núverandi viðskiptavin skal tilgreina viðskiptavininn í reitnum **Viðskiptavinur**.
    - Ef tengiliðurinn er ekki skráður skal fylgja eftirfarandi skrefum:

        1. Í **Númer tengiliðar** reitnum skal velja breytingarhnappinn :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. Í svarglugganum um val á tengilið er aðgerðin **Nýr** valin og síðan eru viðeigandi reitir fylltir út. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Frekari upplýsingar eru í [Stofna tengiliði](marketing-create-contact-companies.md).  
        3. Þegar þú hefur lokið við tengiliðaspjaldið skaltu velja nýlega stofnaðan tengiliðinn úr listanum yfir tengiliði og síðan velja hnappinn Í lagi til að fara aftur í sölutilboðið.

        Margir reitir í sölutilboði eru nú fullir af upplýsingar sem tilgreindar voru á nýja tengiliðaspjaldinu.

        > [!NOTE]
        > Til að reikna skatta og verð fyrir verðtilboð á réttan hátt þarf að velja viðeigandi sniðmát fyrir viðskiptavini í reitnum **Sniðmátskóði viðskiptavinar**. Sniðmátið verður notað til að breyta tengiliðnum í viðskiptavin þegar tilboðinu hefur verið breytt í sölupöntun eða reikning.
    -  Ef tilboðið er fyrir nýjan viðskiptavin þarf að bæta við viðskiptavini. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).  

3. Fylltu í eftirstandandi reikningana á síðunni **sölutilboð** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Nú er hægt að fylla út sölulínurnar fyrir vörur sem verið er að selja eða fyrir viðskipti við viðskiptamanninn eða væntanlegan möguleika á að skrá í fjárhagsreikning.  

    Ef endurteknar sölulínur hafa verið settar upp fyrir viðskiptamanninn, svo sem mánaðarlegar endurnýjunarpantanir, er hægt að færa línuna inn í pöntunina með því að velja aðgerðina **Endurteknar sölulínur**.  

4. Á flýtiflipanum **Línur** í reitnum **Tegund** er valið hvaða tegund vöru, gjalds eða færslu sem bóka á fyrir viðskiptamanninn í sölulínunni.
5. Í reitnum **númer** Reitnum er valin færsla til að bóka samkvæmt gildinu í reitnum **Tegund** reit.

    Þú skilur **nr.** reitur tómur í eftirfarandi tilfellum:
    - Ef línan er ætluð athugasemd. Rita athugasemdina í **Lýsing** reitinn.
    - Ef línan er fyrir vörulistavöru. Velja **Velja vörulistaatriði** aðgerð. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).

6. Í reitnum **Magn** er fært inn hversu margar einingar vöru, kostnaðarauka eða færslu sem línan skráir fyrir viðskiptamanninn.

    > [!NOTE]  
    >  Ef varan er af gerðinni **Þjónusta** eða reiturinn **Gerð** inniheldur **Forðann** þá er magnið tíaeining á borð við klukkustundir, eins og táknað er í **Mælieiningarkóði** reitnum á línunni. Frekari upplýsingar eru í [Setja upp mælieiningu vara](inventory-how-setup-units-of-measure.md)

    Gildið í reitnum **Línuupphæð** er reiknaður sem *Einingarverð* x *Magn*.  

    Verð- og línuupphæðirnar eru sýndar með eða án VSK, en það fer eftir því hvað var valið í reitnum **verð með skatti** á viðskiptamannaspjaldinu.  
7. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.  

    Ef sérstakt vöruverð hefur verið sett upp á flýtiflipanum **Afslættir söluverðs og sölulínu** á viðskiptamanns- eða vöruspjaldinu, uppfærist verðið og upphæðin á tilboðslínunni sjálfvirkt ef umsamin verðviðmið hafa náðst. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Endurtakið skref 4 til 7 fyrir hverja vöru sem bjóða á tengiliðnum.

    Samtölur fyrir neðan línurnar eru sjálfkrafa reiknaðar þegar þú stofnar eða breytir línum.  
9. Í reitinn **Reikningsafsl.upphæð** er færð upphæð sem á að draga frá gildinu sem sýnt er í reitnum **Heildarupphæð með VSK** .

    Ef reikningsafslættir hafa verið settir upp fyrir viðskiptamanninn, er tilgreint prósentugildi sjálfvirkt fært inn í reitinn **reikningsafsláttur %** ef viðmiðum hefur verið mætt og upphæðin færð inn í reitinn **afsláttarupphæð án skatts**. Nánari upplýsingar eru í [Skrá söluverð, afslátt og greiðslusamkomulag](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Til að fá **Tilboð í gildi fram að dagsetningu** fyllt út sjálfvirkt með ákveðnum dagafjölda eftir stofnun tilboðs er hægt að fylla út reitinn **Útreikningur á gildistíma tilboðs** á síðunni **Sala & útistandandi**.

10. Þegar sölutilboðslínunum er lokið, skal velja **Senda í tölvupósti** aðgerðina.
11. Á síðunni **Senda tölvupóst** skal fylla út eftirstandandi reiti og fara yfir innfelld sölutilboð. Nánari upplýsingar eru í [Senda skjöl í tölvupósti](ui-how-send-documents-email.md#to-send-documents-by-email).
12. Ef tengiliður samþykkir tilboðið skal velja aðgerðina **Stofna pöntun**.  

    Annars, ef fyrirtækið kýs það ferli, skaltu velja aðgerðina **Gera reikning**.  
    > [!NOTE]
    > Ef þú bættir viðskiptavini við í skrefi 2 verður beðið um að staðfesta breytinguna á tilboði yfir í pöntun.  
    >
    > Ef þú bættir við tengilið frá væntanlegum viðskiptavini í skrefi 2 verður beðið um að fara í gegnum þessi skref:
    >
    >  - Breyttu tengilið eða viðfangi í viðskiptavin með því að velja eitt af sniðmátum tengiliðabreytingar. Frekari upplýsingar eru í [Að stofna viðskiptamann, lánardrottin, starfsmann eða bankareikning úr tengilið](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Staðfestu breytingu tilboðsins í pöntun.

Breytingin fjarlægir sölutilboðið úr gagnagrunninum. Sölureikningur eða sölupöntun er stofnuð út frá upplýsingunum í sölutilboðinu svo hægt sé að ganga frá sölunni. Í reitnum **Tilboð nr.** á sölureikningnum eða sölupöntun er hægt að sjá fjölda sölutilboða sem hann var búinn til úr. Nánari upplýsingar eru í [Reikningsfæra sölu](sales-how-invoice-sales.md) eða [Selja vörur.](sales-how-sell-products.md)  

## <a name="external-document-number"></a>Númer ytra skjals

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md#to-send-documents-by-email)  
[Safnvista skjöl](across-how-to-archive-documents.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
