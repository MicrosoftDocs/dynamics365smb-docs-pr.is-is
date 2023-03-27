---
title: Stofna samþykktarverkflæði til að tengja verk
description: Lærðu að stofna verkflæði sem tengja verk við mismunandi fólk í viðskiptaferlum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/11/2022
ms.author: bholtorf
---
# Stofna verkflæði til að tengja verk í viðskiptaferlum

Hægt er að stofna verkflæði sem tengja verk í viðskiptaferlum sem eru framkvæmd af mismunandi notendum. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af verkflæðistilvikum sem breytt er af tilvikaskilyrðum og verkflæðisviðbrögðum með viðbragðavalkostum. Þú skilgreinir skref í verkflæði með því að fylla út í reiti í verkflæðislínum úr föstum listum yfir gildi tilvika og svara sem standa fyrir verkflæðissviðsmyndir sem kóði forritsins styður.  

[!INCLUDE[workflow](includes/workflow.md)]

Þegar verkflæði eru stofnuð er hægt að afrita skref úr núgildandi verkflæði eða úr verkflæðissniðmátum. Verkflæðissniðmát eru óbreytanleg verkflæði sem eru til staðar í altæku útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)]. Kótinn fyrir sniðmát verkflæðis sem bætast við hjá Microsoft eru forlaginn með "MS-", eins og í "MS-PIW". Frekari upplýsingar eru í [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Allar tilkynningar um verkflæðisskref eru sendar um verkröð. Gakktu úr skugga um að vinnsluröðin endurspegli þarfir fyrirtækisins. Frekari upplýsingar eru í [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Skýring á verkflæðisdæmi.":::

Verkflæðið skiptist í þrennt:

1. **Þegar atburður**  
   Hér er kveikurinn valinn.  
   Dæmi um kveikju:
   * Aðalgagnafærslu er breytt
   * Færslubókarlína er stofnuð
   * Komandi skjal er stofnað eða gefið út
   * Óskað er eftir samþykki skjals
2. **Um skilyrði**  
    **Skilyrðin**  tengjast tilvikinu og gera kleift að stofna afmarkanir til að ákveða hvernig verkflæðið er haldið áfram.
3. **Þá svarar**  
    **Svörin**  Tilgreina næstu skref í verkflæðinu.

Fyrir bæði atburði og viðbrögð eru kostirnir kerfisvarinn. Nýjar þær þarf að bæta með þróun Framlengingar.

## Til að stofna verkflæði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Verkflæði** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Til að stofna verkflæðið úr sniðmáti verkflæðis, á  **síðunni verkflæði**, skal velja  **nýja verkflæðið úr sniðmátinu**  aðgerð. Frekari upplýsingar eru í [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  
5. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
6. Í **Flokkur** reitnum skal tilgreina hvaða flokki verkflæðið tilheyrir.  
7. Í reitnum **Þegar tilvik** skal tilgreina tilvik sem verður að eiga sér stað til að að verkflæðisskref geti hafist.  

   Þegar svæðið  **er valið opnast síða verkflæðistilviks**  þannig að hægt sé að velja úr öllum tiltækum atvikum verkflæðis.  
8.  **Í reitnum skilyrði**  skal tilgreina eitt eða fleiri skilyrði sem verður að vera uppfyllt áður en atburðurinn í  **reitnum tilvik**  getur átt sér stað.  

   Þegar svæðið  **er valið opnast síðan Atburðarskilyrði**  svo hægt sé að velja um lista yfir afmörkunarreiti sem tengjast því sem skilyrði fyrir tilvikinu sem um ræðir. Hægt er að bæta við nýjum afmörkunarreitum sem á að nota sem tilvikskilyrði. Þú stillir tilvikaaðstæður með sama hætti og þú stillir afmarkanir á skýrslubeiðnisíðum.  

   Ef verkflæðistilvik er breyting á tilteknum reit í færslu opnast síðan **Skilyrði tilviks** með valkostum um að velja reit og gerð breytingar.  

   1. Til að tilgreina reitarbreytingu fyrir tilvik skal, á síðunni **Aðstæður tilviks** í reitnum **Reitur** velja reitinn sem er breytt.  
   2. Í reitnum **Stjórnandi** skal velja annað hvort **Minnkað**, **Aukið**, eða **Breytt**.  
9. Í reitnum **Þá svörun**, tilgreinið viðbrögð sem fylgja þegar verkflæðistilvik á sér stað.  

   Þegar svæðið  **er valið opnast síða verkflæðisviðbragða**  þar sem svo er hægt að velja úr öllum tiltækum svörum um verkflæði og settum svarmöguleika fyrir valið svar.  
10.  **Á valkostunum fyrir valda svörun svarflipa**, Tilgreinið valkosti fyrir svar við verkflæði með því að velja gildi í mismunandi reitum sem birtast hér:  

    1. Til að tilgreian valkosti fyrir verkflæðissvar sem felur í sér að senda tilkyningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    > [!NOTE]
    > Þessi svæði eru breytileg eftir því hvaða svörun hefur verið valin.

       |Svæði|Description|
       |-----|-----------|
       |**Tilkynna sendanda**|Tilgreindu hvort samþykkisbeiðandi fái tilkynningu í staðinn fyrir viðtakanda samþykkisbeiðninnar. Ef gátreiturinn er valinn er slökkt á reitnum **Notandaauðkenni viðtakanda** vegna þess að tilkynning berst til þess sem sendi beiðnina fær tilkynningu í staðinn. Heiti verkflæðissvars breytist til samræmis, í **Búa til tilkynningu fyrir &lt;Sendanda&gt;**. Ef gátreiturinn er ekki valinn er  **Heiti verkflæðissvars stofnað tilkynning fyrir  &lt; notanda&gt;**.|
       |**Notandaauðkenni viðtakanda**|Tilgreina notandann sem senda verður tilkynninguna til. **Athugið**: Þessi valmöguleiki er aðeins tiltækur fyrir verkflæðisvörun með staðgengil fyrir tiltekinn notanda. Fyrir verkflæði viðbragða án frátakara fyrir notendur er tilkynningarviðtalið yfirleitt skilgreint með  **notandauppsetningu** samþykktarinnar.|
       |**Færslugerð tilkynningar**|Tilgreinið ef verkflæðistilkynningu er hrundið af stað með færslu breytinga, samþykktarbeiðni eða skilaskyldum gögnum.|
       |**Tengja marksíðu**|Tilgreindu aðra síðu sem tengill í tilkynningunni opnar í stað þeirrar sjálfgefnu. Síðan verður að hafa sömu upprunatöflu og færslan sem um er að ræða.|
       |**Sérsniðinn tengill**|VEFSLÓÐ er tilgreind með tilkynningunni auk tengils við síðuna.|

    2. Til að tilgreina valkosti fyrir verkflæðissvar sem felur í sér að senda tilkynningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

       |Svæði|Description|  
       |-----|-----------|  
       |**Reikniregla gjalddaga**|Tilgreina hversu margir dagar mega líða þar til leysa þarf úr samþykktarbeiðni frá þeim degi sem hún var send.|
       |**Framselja eftir**|Tilgreinið hvort og þá hvenær samþykktarbeiðni er úthlutin sjálfkrafa til viðeigandi staðgengils. Hægt er að velja sjálfkrafa að úthluta einn, tvo eða fimm dögum eftir þá dagsetning þegar beðið var um samþykkt.|
       |**Gerð samþykkjanda**|Tilgreina hver er samþykkjandi, samkvæmt uppsetningu á notendum samþykktar og notendur verkflæði. Þegar reiturinn er stilltur  **á Sölumaður/innkaupaaðili** er notandinn sem er settur upp í  **salespers./Purch. Reiturinn Kóti**  á  **uppsetningarsíðu**  samþykktarnotanda ákvarðar samþykkjandinn. Færslur fyrir samþykktarbeiðni eru þá stofnaðar samkvæmt gildinu í reitnum **Afmörkunargerð samþykkjanda**. Frekari upplýsingar um  [uppsetningu Samþykktarnotenda](across-how-to-set-up-workflow-users.md).|
       |**Sýna staðfestingarskilaboð**|Tilgreina ef staðfestingarskilaboð birtist notendum eftir að þeir óska ​​eftir samþykki.|
       |**Afmörkunargerð samþykkjanda**|Tilgreinið hvernig samþykkjandi samþykktarmörk hafa áhrif þegar samþykktarbeiðafærslur eru stofnaðar fyrir þær. Hæfur samþykkjandi er samþykkjandi sem hefur samþykktarmörk sem eru hærri en gildið á umræddri beiðni. Eftirfarandi möguleikar eru til staðar: <ol><li>**Keðja samþykkjenda** tilgreinir að færslur samþykktarbeiðni eru stofnaðar fyrir alla samþykkjendur frá og með fyrsta samþykkjanda sem uppfyllir skilyrði</li><li>**Beinn samþykkjandi** tilgreinir að samþykktarbeiðnisfærsla er aðeins stofnuð fyrir næsta samþykkjanda, sama hver samþykktarmörk hans eru.</li><li>**Fyrsti hæfi samþykkjandi** tilgreinir að samþykktarbeiðnisfærsla er aðeins stofnuð fyrir fyrsta samþykkjanda sem uppfyllir skilyrði.</li><li>**Tiltekinn samþykkjandi**  Tilgreinir að notandinn hafi valið í  **reitnum Kenni**  samþykkjanda.</li></ol>|
    3. Til að tilgreina valkostir fyrir verkflæðissvar sem inniheldur að stofna færslubókarlínur skal fylla í reitirnir eins og lýst er í eftirfarandi töflu.  

       |Svæði|Description|  
       |-----|-----------|  
       |**Heiti sniðmáts færslubókar**|Tilgreina heiti sniðmáts færslubókarinnar sem stofnuð eru í tilteknu bókarlínurnar.|  
       |**Heiti færslubókarkeyrslu**|Tilgreina heiti sniðmáts færslubókarrununnar sem stofnuð eru í tilteknu bókarlínurnar.|  

11. Velja skal hnappana **Auka inndrátt** og **Minnka inndrátt** til að draga tilviksheiti inn í reitnum **Þegar** til að skilgreina stöðu skrefsins í verkflæðinu.  

    1. Tilgreinið það skref sem er næst í verkflæðiröðinni með því að innskrá atviksheiti undir atburðaheiti fyrra skrefs.  
    2. Til kynna að skrefið sé eitt af mörgum skrefum sem gætu hafist, allt eftir ástandi þess, með því að innskrá heiti tilvikksins til að stemma við önnur aukaskref. Raðið slíkum valskrefum eftir forgangi með því að setja mikilvægasta skrefið efst.  

    > [!NOTE]  
    >  Aðeins er hægt að breyta inndrætti skrefs sem ekki hefur skref á eftir sér.  

12. Endurtakið skref 7 til 11 til að bæta við fleiri verkflæðisskrefum, annað hvort á undan eða eftir skrefinu sem búið var til.  
13. Kveikja skal á  **Virkjapunktinum**  til að tilgreina að verkflæðið byrji um leið og atburður á upphafsstigi  **af gerðinni**  færsla kemur. Frekari upplýsingar má finna á [Nota verkflæði](across-use-workflows.md).  

> [!NOTE]  
> Ekki gera verkflæði virkt fyrr en þú ert viss um að verkflæðið sé fullklárað og að þátt verkflæðisskrefa geti hafist.  

> [!TIP]  
> Til að sjá vensl milli taflna sem notaðar eru í verkflæði skal velja þá  ![ljósaperu sem opnar aðgerðina segja](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Táknið, færa síðan inn  **verkflæði – töfluvensl**.  

## Dæmi um hvernig nýtt verkflæði er búið til með því að nota fyrirliggjandi tilvik

Í dæminu hér á eftir er nýtt verkflæði samþykkt til að samþykkja breytingar á heitinu á núverandi lánardrottni:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Verkflæði** opnast.
3. Í verkflæðishlutanum skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.

    |Svæði  |Gildi:  |
    |---------|---------|
    |**Kóði**|**VENDAPN-01**|
    |**Lýsing**|**Samþykki fyrir nafnbreytingu lánardrottins** |
    |**Flokkur**|**INNK**|

4. Eftirfarandi er gert til að stofna fyrsta verkflæðisskrefið.

    1. Í reitnum **Þegar tilvik** skal tilgreina að *Lánardrottnafærslu er breytt*.  
    2.  **Í reitnum á ástandi**  skal velja orðið  **alltaf**. Síðan, á atburðadagatinu  **, skal velja**  reitinn bæta við skilyrði þegar tengill svæðisvirðis breytist  **, velja**  síðan svæðið heiti  *.*  Niðurstaðan úr þessu skrefi er að skilyrðið lesist sem *Heiti er breytt*.  
    3.  **Í reitnum svar**  er  **valið svartengill** . Á síðunni viðbrögð  **við**  verkflæði, í  **reitnum velja svar**, er valið að  *Bakfæra gildi  \<Field\>  svæðisins á færslunni og breyta*  svari. Síðan skal tilgreina  **svæðið heiti**  í  *valkostunum fyrir valinn svarkafla* .  
    4.  **Veldu tengilinn bæta við fleiri svörum**, Bættu svo við færslu fyrir  *Stofnaðu samþykktarbeiðni fyrir færsluna með því að nota gerð  <%1>  samþykkjanda og  <%2>*  Svar.  
    5.  **Í valkostunum fyrir valinn svarkafla**  fyrir nýja svarið þarf að breyta  **svæðinu**  samþykkjanda  *í verkflæði notendaflokks*, í  **reitnum notendaflokkur**  verkflæðis og tilgreina viðkomandi notendaflokk. Frekari upplýsingar má finna á [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  
    6. Bættu við þriðja svarinu: *Senda samþykktarbeiðni fyrir færsluna og stofna tilkynningu.*  
    7. Bæta við fjórða svari,  *Sýna skilaboð " %1*, síðan, í  **valkostunum fyrir valinn svarkafla**, í  **svæðinu boð**, og tilgreina  **samþykktarbeiðni sem hefur verið send**.  
    8. Valið  **er í lagi**  til að fara aftur í verkflæðisþrepið.  

5. Í næstu línu skal bæta við nýju verkflæðisskrefi fyrir *Samþykktarbeiðni er samþykkt.* tilvik.

    1. Í reitnum **Þegar tilvik** skal tilgreina *Samþykktarbeiðni er samþykkt*.  
    2. Veldu línuvalmyndina og veldu  **síðan auka inndrátt**.  
    3.  **Í reitnum um skilyrði**  er orðið  **alltaf** valið, í  **reitnum samþykktir**  í undirbúningi er tilgreint  *0*. Árangurinn af þessu skrefi er sá að skilyrðið Les eins og  *samþykki fyrir bið: 0*  til að gefa til kynna að þetta sé Síðasti samþykkjandinn.  
    4.  **Í reitnum svar**  er  **valið svartengill** . Á síðunni viðbrögð  **við**  verkflæði, í  **reitnum velja svar**, er valið  *senda samþykkisbeiðni fyrir færsluna og tilkynningarsvar*  stofnað.  
    5. Velja **Í lagi**.  
6. Í næstu línu bætir þú við öðru verkflæðisskrefi fyrir tilvikið *Samþykktarbeiðni er samþykkt*.  

    1. Í reitnum **Þegar tilvik** skal tilgreina *Samþykktarbeiðni er samþykkt*.
    2.  **Í reitnum um skilyrði**  er orðið  **alltaf** valið, í  **reitnum samþykki**  er tilgreint  *> 0*. Árangurinn af þessu skrefi er sá að skilyrðin eru lesin sem  *Biðsamþykki: > 0*  til að gefa til kynna að þetta sé  *ekki*  Síðasti samþykkjandinn.  
    3.  **Í reitnum svar**  er  **valið svartengill** . Á síðunni viðbrögð  **við**  verkflæði, í  **reitnum velja svar**, er valið  *senda samþykkisbeiðni fyrir færsluna og tilkynningarsvar*  stofnað.  
    4. Velja **Í lagi**.  
7. Í næstu línu er verkflæðisskrefi bætt við fyrir  *samþykktarbeiðni er framselt*  tilvik.  

    1.  **Í reitnum þegar atburður**  er tilgreindur  *samþykktarbeiðni er úthlutin*.  
    2. Í reitnum **Með skilyrði** skal halda gildinu *Alltaf*.  
    3.  **Í reitnum svar**  er  **valið svartengill** . Á síðunni viðbrögð  **við**  verkflæði, í  **reitnum velja svar**, er valið  *senda samþykkisbeiðni fyrir færsluna og tilkynningarsvar*  stofnað.  
    4. Velja **Í lagi**.  
8. Í næstu línu skal bæta við öðru verkflæðisskrefi fyrir tilvikið *Samþykktarbeiðni er hafnað*.  

    1. Í reitnum **Þegar tilvik** skal tilgreina *Samþykktarbeiðni er hafnað*.  
    2. Í reitnum **Með skilyrði** skal halda gildinu *Alltaf*.  
    3.  **Í reitnum svar**  er  **valið svartengill** . Síðan er  **smellt á síðuna viðbrögð**  við verkflæði í  **reitnum**  Velja svar  *til að henda svari nýju gildi* .  
    4.  **Veldu tengilinn bæta við fleiri svörum**, Bættu svo við færslu fyrir  *höfnun samþykkisbeiðninnar fyrir færsluna og Búðu til tilkynningarsvar* 
    5. Velja **Í lagi**.  
9. Ef gera á verkflæðið virkt er kveikt á  **virkjunni**  skipta.  

Eftirfarandi mynd gefur yfirlit yfir niðurstöður þessarar aðgerðar.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Skýring á samþykktarverkflæði lánardrottnaheitis.":::

Næst skal prófa verkflæðið með því að opna fyrirliggjandi lánardrottnaspjald og breyta nafni þeirra. Staðfestið að samþykktarbeiðni sé send eftir að nafni lánardrottins er breytt.

## Sjá tengda [Microsoft þjálfun](/training/modules/create-workflows/)

## Sjá einnig .

[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)  
[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Uppsetning tilkynninga um samþykktarverkflæði](across-setting-up-workflow-notifications.md)  
[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)  
[Eyða samþykktarverkflæðum](across-how-to-delete-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
