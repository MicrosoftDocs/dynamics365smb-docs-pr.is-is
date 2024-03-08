---
title: Nota Samþykktarverkflæði
description: Hægt er að setja upp og nota verkflæði til að tengja verk viðskiptaferla eins og sjálfvirka bókun eða beiðni og veitingu samþykktar fyrir nýjar færslur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 09/13/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Nota Samþykktarverkflæði

Verkflæði er röð verka sem aðgerð, skilyrði eða regla setur af stað. Verkflæði eru yfirleitt innleidd til að samþætta viðskiptagrunn við fyrirtæki, t.d. aðskilnað aðgangsheimilda, sameiningu ferla eða til að nota bestu starfsvenjur.

Hægt er að hanna verkflæðin til að búa til beiðnir um samþykki á breytingu á færslureit meðan gömlu gögnin eru geymd ef beiðnin er ekki samþykkt. Nýja gildið verður ekki innleitt fyrr en síðasta beiðnin er samþykkt.

Viðskiptagrunnurinn gæti verið samþykki á:

- Ný aðalgögn eins og fjárhagsreikningar, viðskiptamenn, lánardrottnar eða vörur.
- Breytingar á reitum í fyrirliggjandi færslum innihalda viðkvæmar upplýsingar á borð við **Bankareikningsnúmer lánardrottins** eða **Lánamark viðskiptavinar**
- Breytingar á reitum í fyrirliggjandi færslum sem innihalda mikilvægar upplýsingar um viðskipti á borð við **Söluverð vöru**
- Nýir notendur eða breytingar á notendaheimildum.
- Innkaupaskjöl.
- Söluskjöl.
- Skjöl á innleið.
- Fjármálabækur á undan bókun.

Eftirfarandi skýringarmynd er dæmi um verkflæði með samþykktarröð sem notandi setur í gang. Með því að setja verkflæðið af stað verður samþykktarbeiðni búin til fyrir fyrsta samþykkjandann.  

![Mynd af verkflæði með samþykktarröð.](media/Workflows/approval-flow.png)

Þú sérð á myndinni hér að ofan hvernig beiðnin þarf að vera samþykkt af fyrsta samþykktaraðila áður en hún er send á þann næsta. Ef beiðnin er ekki samþykkt af fyrsta samþykktaraðilanum fer beiðnin aldrei áfram til þess næsta.

Leiðin sem farin er frá upphaflegri ræsingu verkflæðisins getur verið breytileg eftir því hvers eðlis samþykktin er.  

Eftirfarandi mynd sýnir samhliða samþykki sem notandi setur af stað. Samhliða samþykki þýðir að samþykktarbeiðnin er send til allra samþykktaraðila samtímis.  

![Mynd af verkflæði með samhliða samþykki.](media/Workflows/approval-flow-2.png)

Verkflæðinu er hinsvegar ekki lokið fyrr en allar beiðnirnar hafa verið samþykktar eins og sýnt er á eftirfarandi mynd:  

![Mynd af höfnuðu verkflæði með samhliða samþykki.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Fyrir verkflæði með mörgum samþykktaraðilum verða allir samþykktaraðilar að samþykkja hvert skref áður en verkflæðið getur fraið áfram yfir á næsta tilvik. Samþykki frá aðeins einum samþykktaraðila mun ekki færa verkflæðið áfram.

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Það er hægt að stofna sama verkflæðið oftar en einu sinni. Hvert verkflæði er ræst af tilviki með mismunandi síum. Þetta er gagnlegt ef samþykktarbeiðnin fyrir eina deild þarf að vera samþykkt af einum samþykktaraðila, en beiðnir fyrir aðrar deildir þurfa að vera samþykktar af öðrum samþykktaraðila. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Áður en hægt er að byrja að nota verkflæði verður að setja upp notendur verkflæðis, stofna verkflæði, hugsanlega eftir að hafa sérsniðið kóða og tilgreina hvernig notendur fá tilkynningar. Frekari upplýsingar má finna á [Uppsetning verkflæðis](across-set-up-workflows.md).

> [!NOTE]  
> Dæmigerð verkflæðisskref fela í sér að notendur biðji um samþykki verka og samþykktaraðilar samþykki eða hafni samþykktarbeiðnum. Þess vegna vísa mörg efni um hvernig nota eigi verkflæði til samþykkta.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.  

| **Til að** | **Sjá** |
|--|--|
| Settu upp samþykktarverkflæði til að hefjast handa þegar fyrsta tilvik færslupunkts á sér stað. | [Virkja samþykktarverkflæði](across-how-to-enable-workflows.md) |
| Samþykktarbeiðni fyrir verk, sem samþykktaraðili samþykkirðu, hafnarðu eða úthlutar samþykktum, og sendir eða ferð yfir samþykktartilkynningar. | [Hvernig á að nota samþykktarverkflæði](across-how-use-approval-workflows.md) |
| Stofnaðu verkflæðisskref sem takmarka að ákveðin færslugerð sé notuð áður en tiltekið tilvik á sér stað, til dæmis að færsla sé samþykkt. | [Takmarka og heimila notkun á færslu](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Skoðaðu tilvik verkflæðisskrefa með stöðuna **Lokið**. | [Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md) |
| Eyddu samþykktarverkflæði sem verður ekki notað aftur. | [Eyða verkflæði samþykkta](across-how-to-delete-workflows.md) |

## Sjá einnig .

[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Verkflæði](across-workflow.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
