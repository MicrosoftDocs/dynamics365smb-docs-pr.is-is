---
title: Bókamerki tengja á síðu eða skýrslu um mitt hlutverk
description: Með því að nota bókamerkistáknið er hægt að bæta við aðgerð sem opnar síðu eða skýrslu úr yfirlitsvalmynd hlutverksins.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Bókamerki síðu eða skýrslu í mínu hlutverki

Með því að nota bókamerkistáknið er hægt að bæta við aðgerð sem opnar síðu eða skýrslu úr yfirlitsvalmynd hlutverksins. Þetta gerir þér kleift að nálgast eftirlætisefnið eða viðskiptaverkefnin þín á fljótlegan hátt. Bókamerkinu er bætt við af marksíðu eða skýrslu sem þýðir að skjárinn sem tengja í hlutverkinu á að opnast.

Táknið fyrir bókamerki er sýnt efst í hægra horninu á síðu og einnig í glugga **Viðmótsleitar** þar sem hægt er að bæta bókamerki við margar síður eða skýrslur. Ef bókamerki er þegar til fyrir síðuna, þá er teiknið dimmt og verkfæratáknið segir „bókamerkt“.

## <a name="bookmark-the-target-page"></a>Bókamerki marksíðunnar

1. Opna skal hvaða síðu sem tengja á í mitt hlutverk.
2. Veldu ![Bókamerkið.](media/ui_bookmark_icon.png "Bókamerki")  

Aðgerð sem nefnd er eftir síðunni er nú bætt í yfirlitsvalmyndina í mínu hlutverki.

## <a name="bookmark-the-target-report"></a>Bókamerki markskýrslunnar

1. Opna skal hvaða skýrslubeiðnisíðu sem á að tengja fyrir í mitt hlutverk.
2. Veldu ![Bókamerkið.](media/ui_bookmark_icon.png "Bókamerki")  

Aðgerð sem nefnd er eftir skýrslunni er nú bætt í yfirlitsvalmyndina í mínu hlutverki.

## <a name="bookmark-a-page-or-report-from-the-tell-me-window"></a>Bókamerki síðu eða skýrslu úr glugganum Segja mér

1. Opnaðu **Viðmótsleit** glugga og Sláðu inn, til dæmis **sölupantanirnar**.
2. Haltu músarbendlinum yfir leitarniðurstöðunni fyrir síðuna **Sölupantanir** eða skýrslu og veldu svo ![Bókamerkið.](media/ui_bookmark_icon.png "Bókamerki")  

Aðgerð sem nefnd er eftir síðunni eða skýrslunni er nú bætt í yfirlitsvalmyndina í mínu hlutverki.

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="can-i-reorganize-my-bookmarks"></a>Má ég endurraða bókamerkjum mínum?

Já. Hægt er að sérsníða mitt hlutverk og færa aðgerðir í bestari röð eða færa þær í fyrirliggjandi hópa eða undirhópa.  
Kynntu þér hvernig [Sérstilla verksvæði](ui-personalization-user.md).

### <a name="how-do-i-remove-a-bookmark"></a>Hvernig fjarlægi ég bókamerki?

Á marksíðu eða skýrslu skal velja bókamerkistáknið aftur til að fjarlægja aðgerðina sem um ræðir úr hlutverkinu. Einnig er hægt að sérstilla mitt hlutverk og fela aðgerðir tímabundið án þess að fjarlægja þær að fullu.

### <a name="where-do-i-find-my-bookmarks"></a>Hvar finn ég bókamerkin mín?

Þegar bókamerki er bætt við síðu eða skýrslu er nýju aðgerðinni bætt við efstu yfirlitsvalmyndina á núverandi heimaskjá (mitt hlutverk). Ef þú ert með margar aðgerðir getur þurft að virkja hnappinn **Meira** til að birta þær allar þar sem nýju aðgerðinni er alltaf bætt við í lok þessara aðgerða.
<!-- Should we add a screenshot here? -->

### <a name="i-dont-have-a-bookmark-icon-is-something-wrong"></a>Ég er ekki með bókamerkistákn. Er eitthvað að?

Möguleikinn á að bókamerkja síðu eða skýrslu er ein af mörgum sérstillingaraðgerðum í Business Central. Ef bókamerkjatáknið er ekki birt er líklegt að stjórnandi hafi slökkt á sérstillingum.

### <a name="why-cant-i-bookmark-certain-pages-or-reports"></a>Hvers vegna get ég ekki bókað ákveðnar síður eða skýrslur?

Ekki er hægt að bókamerkja allar síður og skýrslur. Þegar síða eða skýrslur eru keyrðar innan sérstaks samhengis sem viðskiptaforritið stjórnar er bókamerkjatákn ekki birt. Til dæmis munu síður sem finnast ekki í glugganum **Viðmótsleit** en eru ræstar annars staðar ekki birta bókamerkjatákn. Á sama hátt birta síður skýrslubeiðna sem eru aðeins notaðar til að safna síum án þess að keyra skýrsluna ekki bókamerkjatákn.

  Sjá tæknilegar upplýsingar um [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) og [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

### <a name="when-clearing-my-personalization-will-my-bookmarks-also-be-cleared"></a>Þegar sérstilling mín er hreinsuð verða bókamerkin mín einnig hreinsuð?

Já. Bókamerki eru í yfirlitsvalmynd. Ef breytingar eru hreinsaðar á yfirlitsvalmyndinni af einhverri síðu eða allar sérstillingar í hlutverkamiðstöðinni eru allar nýjar aðgerðir fjarlægðar varanlega.

### <a name="why-does-the-bookmark-icon-continue-to-indicate-its-still-not-bookmarked"></a>Hvers vegna heldur bókamerkistáknið áfram að gefa til kynna að það sé enn ekki bókamerkt?

Þegar bókamerki er bætt við er nýju aðgerðinni bætt við yfirlitsvalmyndina í hlutverkamiðstöðinni og síðari heimsóknir á síðuna eða skýrslan sýnir dökkt bókamerkistákn. Ef mitt hlutverk er sérstillt og aðgerðir endurskipulagðar með því að færa þær í hópa verður bókamerkistáknið ekki lengur dökkt og hægt er að bæta öðru bókamerki við sömu síðu eða skýrslu. Þetta gerir þér kleift að bæta við mörgum aðgerðum á sömu síðu eða skýrslu og flokka þær í mismunandi flokka.

### <a name="why-does-my-link-to-a-report-display-a-different-report"></a>Hvers vegna birtir tengja mín í skýrslu annarri skýrslu?

Sumum skýrslum kann að vera skipt út fyrir aðrar skýrslur eftir að viðbót hefur verið notuð í Business Central. Þegar staðgengill er notaður er texti nýju aðgerðarinnar ekki uppfærður og mun halda áfram að birta heiti upprunalegu skýrslunnar, en fara í nýrri skýrsluna. Til að leiðrétta texta nýju aðgerðarinnar er hægt að fjarlægja nýju aðgerðina og bæta henni við aftur.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

### <a name="is-bookmarking-available-for-xmlports"></a>Er bókamerki í boði fyrir XMLports?

Fj. Sem stendur er ekki hægt að bæta við aðgerðum til að opna XMLports úr notandaviðmótinu.

### <a name="will-my-bookmarks-be-translated-when-i-change-my-language-in-business-central"></a>Verða bókamerkin mín þýdd þegar ég breyti tungumáli mínu í Business Central?

Þegar nýrri aðgerð er bætt við er öllum þýddum texta sem var tiltækur á þeim tíma notað þegar verið er að bókamerkja. Ef nýjum þýddum texta er bætt við síðar mun nýja aðgerðin ekki innihalda nýrri þýðingarnar.

### <a name="why-cant-i-add-text-in-a-page-right-after-opening-it-with-the-bookmark"></a>Því get ég ekki bætt texta inn á síðu beint eftir að hann er opnaður með bókamerkinu?

Þegar síða er bókamerkt mun síðan alltaf opnast í skoðunarstillingu frá bókamerkinu&mdash;jafnvel þótt hún hafi verið í breytingastillingu þegar hún var bókamerkt. Með því að velja táknið **Gera breytingar á síðunni** ![Birtist blýantstáknið til að breyta síðunni.](media/edit-pencil.png) þá er hægt að bæta við texta í reitina sem hægt er að breyta.

## <a name="see-also"></a>Sjá einnig .

[Sérstilling verksvæðis](ui-personalization-user.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta grunnstillingum](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
