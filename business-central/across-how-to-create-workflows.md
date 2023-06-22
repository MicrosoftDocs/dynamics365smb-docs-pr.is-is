---
title: Stofna samþykktarverkflæði til að tengja verk
description: Lærðu að stofna verkflæði sem tengja verk við mismunandi fólk í viðskiptaferlum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
---
# <a name="create-workflows-to-connect-tasks-in-business-processes" />Stofna verkflæði til að tengja verk í viðskiptaferlum

Hægt er að stofna verkflæði sem tengja verk í viðskiptaferlum sem eru framkvæmd af mismunandi notendum. Hægt er að taka kerfisverk með, svo sem sjálfvirka bókun, sem skref í verkflæði sem eru á undan eða eftir notendaverkefni. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

 **Á verkflæðissíðunni**  skal stofna verkflæði með því að skrá skrefin í línunum. Hvert skref samanstendur af kveikju og svari:

* Tilvik sem Tilgreinir skilyrðin sem ræsa verður verkflæðið.
* Verkflæðissvar sem skilgreinir hvað verkflæðið gerir.

[!INCLUDE[workflow](includes/workflow.md)]

Þegar verkflæði eru stofnuð er hægt að afrita skref úr núgildandi verkflæði eða úr verkflæðissniðmátum. Sniðmát verkflæðis eru ekki Breytanlegt verkflæði  [!INCLUDE[prod_short](includes/prod_short.md)]  útveita. Auðkenni fyrir sniðmát verkflæðis eru með "MS-", eins og í "MS-PIW". Frekari upplýsingar eru í [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Allar tilkynningar um verkflæðisskref eru sendar um verkröð. Gakktu úr skugga um að vinnsluröðin endurspegli þarfir fyrirtækisins. Frekari upplýsingar eru í [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Skýring á verkflæðisdæmi.":::

Verkflæði er skipt í þrjá kafla:

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

Valkostir fyrir viðburði og svör eru kerfisvarðar. Til að bæta við nýjum valkostum þarftu að þróa framlengingu.

## <a name="to-create-a-workflow" />Til að stofna verkflæði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Verkflæði** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Til að stofna verkflæðið úr sniðmáti verkflæðis, á  **síðunni verkflæði**, skal velja  **nýja verkflæðið úr sniðmátinu**  aðgerð. Frekari upplýsingar eru í [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  
5. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
6. Í **Flokkur** reitnum skal tilgreina hvaða flokki verkflæðið tilheyrir.  
7. Í reitnum **Þegar tilvik** skal tilgreina tilvik sem verður að eiga sér stað til að að verkflæðisskref geti hafist.  

   Þegar svæðið er valið birtist síða verkflæðistilviks  **í**  öllum tiltækum verkflæðistilvikum.  
8.  **Í reitnum skilyrði**  skal tilgreina eitt eða fleiri skilyrði sem verður að vera uppfyllt áður en atburðurinn í  **reitnum tilvik**  getur átt sér stað.  

   Þegar svæðið er valið birtir listi yfir skilyrði  **á**  síðunni afmörkunarreiti sem geta verið skilyrði fyrir tilvikinu. Hægt er að bæta við nýjum afmörkunarreitum ef vill.  

   Ef verkflæðistilvik er breyting tiltekins svæðis á færslu skal nota  **síðuna atvik skilyrða**  til að velja svæðið og gerð breytunnar.  

   1. Til að tilgreina reitarbreytingu fyrir tilvik skal, á síðunni **Aðstæður tilviks** í reitnum **Reitur** velja reitinn sem er breytt.  
   2. Í reitnum **Stjórnandi** skal velja annað hvort **Minnkað**, **Aukið**, eða **Breytt**.  
9. Í reitnum **Þá svörun**, tilgreinið viðbrögð sem fylgja þegar verkflæðistilvik á sér stað.  

   Þegar svæðið  **er valið birtir síða vinnuflæðisins**  lista yfir öll tiltæk svör og svarmöguleika verkflæðis.  
10.  **Á valkostunum fyrir valda svörun svarflipa**, Tilgreinið valkosti fyrir svar við verkflæði með því að velja gildi í mismunandi reitum sem birtast hér:  

    1. Til að tilgreian valkosti fyrir verkflæðissvar sem felur í sér að senda tilkyningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    > [!NOTE]
    > Þessi svæði eru breytileg eftir því hvaða svörun hefur verið valin.

       |Svæði|Heimildasamstæða|
       |-----|-----------|
       |**Tilkynna sendanda**|Tilgreinið hvort eigi að tilkynna samþykktarbeiðni eða í stað þess að viðtakandi samþykkis óski eftir því. Ef gátreiturinn er valinn  **er reiturinn notandakenni viðtakanda óvirkur því að Greiðslugeta**  samþykktarinnar, sendanda, verður látinn vita í staðinn. Heiti verkflæðissvars breytist til samræmis, í **Búa til tilkynningu fyrir &lt;Sendanda&gt;**. Ef gátreiturinn er ekki valinn er  **Heiti verkflæðissvars stofnað tilkynning fyrir  &lt; notanda&gt;**.|
       |**Notandaauðkenni viðtakanda**|Tilgreina notandann sem senda verður tilkynninguna til. **Athugið**: Þessi valmöguleiki er aðeins tiltækur fyrir verkflæðisvörun með staðgengil fyrir tiltekinn notanda. Fyrir verkflæði viðbragða án frátakara fyrir notendur er tilkynningarviðtalið yfirleitt skilgreint með  **notandauppsetningu** samþykktarinnar.|
       |**Færslugerð tilkynningar**|Tilgreinið kveikju fyrir tilkynningu verkflæðisins. Kveikjan getur verið færslubreyting, samþykktarbeiðni eða sendur Gjalddagi.|
       |**Tengja marksíðu**|Tilgreinið síðuna sem hlekkurinn í tilkynningunni opnar. Síðan verður að hafa sömu upprunatöflu og færslan sem um er að ræða.|
       |**Sérsniðinn tengill**|VEFSLÓÐ er tilgreind með tilkynningunni auk tengils við síðuna.|

    2. Til að tilgreina valkosti fyrir verkflæðissvar sem felur í sér að senda tilkynningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

       |Svæði|Heimildasamstæða|  
       |-----|-----------|  
       |**Reikniregla gjalddaga**|Tilgreinið fjölda daga sem samþykkjandinn hefur til að leysa beiðnina. Tímabilið hefst þegar beiðnin er send.|
       |**Framselja eftir**|Tilgreinið hvort og þegar samþykktarbeiðni er úthlutin sjálfkrafa til staðgengils. Hægt er að velja sjálfkrafa að úthluta einn, tvo eða fimm dögum eftir þá dagsetning þegar beðið var um samþykkt.|
       |**Gerð samþykkjanda**|Tilgreina hver er samþykkjandi, samkvæmt uppsetningu á notendum samþykktar og notendur verkflæði. Þegar reiturinn er stilltur  **á Sölumaður/innkaupaaðili** er notandinn tilgreindur í  **salespers./Purch. Reiturinn Kóti**  á  **uppsetningarsíðu**  samþykktarnotanda ákvarðar samþykkjandinn. Færslur fyrir samþykktarbeiðni eru þá stofnaðar samkvæmt gildinu í reitnum **Afmörkunargerð samþykkjanda**. Frekari upplýsingar um  [uppsetningu Samþykktarnotenda](across-how-to-set-up-workflow-users.md).|
       |**Sýna staðfestingarskilaboð**|Tilgreinið hvort sýna eigi staðfestingarboð eftir að notandi biður um samþykki.|
       |**Afmörkunargerð samþykkjanda**|Tilgreina skal hvaða áhrif takmarkanir á samþykkjendur hafa. Samþykktarmörk samþykkjanda verða að vera yfir andvirði beiðninnar. Eftirfarandi möguleikar eru til staðar: <ol><li>**Keðja samþykkjenda** tilgreinir að færslur samþykktarbeiðni eru stofnaðar fyrir alla samþykkjendur frá og með fyrsta samþykkjanda sem uppfyllir skilyrði</li><li>**Beinn samþykkjandi** tilgreinir að samþykktarbeiðnisfærsla er aðeins stofnuð fyrir næsta samþykkjanda, sama hver samþykktarmörk hans eru.</li><li>**Fyrsti Styrkhæfur samþykkjandi**  Tilgreinir að samþykktarbeiðni sé aðeins stofnuð fyrir fyrsta samþykkjanda umsækjandans.</li><li>**Tiltekinn samþykkjandi**  Tilgreinir að notandinn hafi valið í  **reitnum Kenni**  samþykkjanda.</li></ol>|

    3. Ef tilgreina á valkosti fyrir verkflæðissvörun sem felur í sér að stofna færslubókarlínur er fyllt út í reitina eins og lýst er í eftirfarandi töflu.  

       |Svæði|Heimildasamstæða|  
       |-----|-----------|  
       |**Heiti sniðmáts færslubókar**|Tilgreina heiti sniðmáts færslubókarinnar sem stofnuð eru í tilteknu bókarlínurnar.|  
       |**Heiti færslubókarkeyrslu**|Tilgreina heiti sniðmáts færslubókarrununnar sem stofnuð eru í tilteknu bókarlínurnar.|  

11. Velja skal hnappana **Auka inndrátt** og **Minnka inndrátt** til að draga tilviksheiti inn í reitnum **Þegar** til að skilgreina stöðu skrefsins í verkflæðinu.  

    1. Þrepa atburðarins undir heitinu fyrra skrefið til að gefa til kynna að það sé næsta skref.  
    2. Til kynna að skrefið sé eitt af mörgum skrefum sem gætu hafist, allt eftir ástandi þess, með því að innskrá heiti tilvikksins til að stemma við önnur aukaskref. Raðið slíkum valskrefum eftir forgangi með því að setja mikilvægasta skrefið efst.  

    > [!NOTE]  
    >  Einungis er hægt að breyta inntaki þrepa sem ekki hefur síðari skref.  

12. Endurtakið skref 7 til 11 til að bæta við fleiri verkflæðisskrefum, annað hvort á undan eða eftir skrefinu sem búið var til.  
13. Kveikja skal á  **virkjununni**  til að tilgreina að verkflæðið byrji þegar atburður á upphafsstigi  **af gerðinni**  færsla er á sér stað. Frekari upplýsingar má finna á [Nota verkflæði](across-use-workflows.md).  

> [!NOTE]  
> Ekki virkja verkflæði fyrr en þú ert viss um að það sé tilbúið.  

> [!TIP]  
> Til að kanna tengslin milli þeirra taflna sem notaðar eru í verkflæði skal velja þá  ![ljósaperu sem opnar aðgerðina segja](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"). Táknið, færa síðan inn  **verkflæði – töfluvensl**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events" />Dæmi um hvernig nýtt verkflæði er búið til með því að nota fyrirliggjandi tilvik

Eftirfarandi dæmi stofnar verkflæði til að samþykkja breytingu á nafni lánardrottins:

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
    2.  **Í reitnum á ástandi**  skal velja orðið  **alltaf**. Síðan, á atburðadagatinu  **, skal velja**  reitinn bæta við skilyrði þegar tengill svæðisvirðis breytist  **, velja**  síðan svæðið heiti  **.**  Niðurstaðan úr þessu skrefi er að skilyrðið lesist sem *Heiti er breytt*.  
    3.  **Í reitnum svar**  er  **valið svartengill** . Á síðunni viðbrögð  **við**  verkflæði, í  **reitnum velja svar**, er valið að  **Bakfæra gildi  \<Field\>  svæðisins á færslunni og breyta**  svari. Síðan skal tilgreina  **svæðið heiti**  í  **valkostunum fyrir valinn svarkafla** .  
    4.  **Veldu tengilinn bæta við fleiri svörum**, Bættu svo við færslu fyrir  **Stofnaðu samþykktarbeiðni fyrir færsluna með því að nota gerð  <%1>  samþykkjanda og  <%2>**  Svar.  
    5.  **Í valkostunum fyrir valinn svarkafla**  fyrir nýja svarið er reiturinn samþykkjagerð  **breytt**  í  **verkflæðisflokk** verkflæðis. Í  **reitnum notendaflokkur**  verkflæðis skal tilgreina notendaflokk. Frekari upplýsingar má finna á [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  
    6. Bæta við þriðja svari,  **senda samþykktarbeiðni um skráninguna og búa til tilkynningu**.  
    7. Bæta við fjórðu svörun,  **Sýna skilaboð " %1 "**. Síðan, í  **valkostunum fyrir valda svarhlutann**, í  **reitnum boð**  í reitnum skal tilgreina  **samþykktarbeiðni sem hefur verið send**.  
    8. Valið  **er í lagi**  til að fara aftur í verkflæðisþrepið.  

5. Í næstu línu er nýtt verkflæðisskref bætt við fyrir  **samþykktan**  atburð.

    1.  **Í svæðinu þegar atburður**  er skal tilgreina  **samþykktarbeiðni sem er samþykkt**.  
    2. Veldu línuvalmyndina og veldu  **síðan auka inndrátt**.  
    3.  **Veldu**  alltaf  **í reitnum á skilyrði**. Þá skal tilgreina  **í reitnum samþykktir í**  samþykktum  **0**. Skilyrðið Les sem  **biðlaunaréttur: 0**  til sönnunar því að beiðnin þarfnist ekki fleiri samþykkjendur.  
    4.  **Í reitnum svar**  er  **valið svartengill** . Á síðunni viðbrögð  **við**  verkflæði, í  **reitnum velja svar**, er valið  **senda samþykkisbeiðni fyrir færsluna og tilkynningarsvar**  stofnað.  
    5. Velja **Í lagi**.  
6. Í næstu línu er annað verkflæðisskref bætt við fyrir  **samþykktan**  atburð.  

    1.  **Í svæðinu þegar atburður**  er skal tilgreina  **samþykktarbeiðni sem er samþykkt**.
    2.  **Veldu**  alltaf  **í reitnum á skilyrði**. Síðan, í  **reitnum samþykki samþykkta**, er tilgreint  **> 0**. Skilyrðið Les sem  **Biðsamþykki: > 0**  til að gefa til kynna að þetta sé ekki Síðasti samþykkjandinn.  
    3.  **Í reitnum svar**  er  **valið svartengill** . Á síðunni viðbrögð  **við**  verkflæði, í  **reitnum velja svar**, er valið  **senda samþykkisbeiðni fyrir færsluna og tilkynningarsvar**  stofnað.  
    4. Velja **Í lagi**.  
7. Í næstu línu er verkflæðisskrefi bætt við fyrir  **samþykktarbeiðni er framselt**  tilvik.  

    1.  **Í reitnum þegar atburður**  er tilgreindur  **samþykktarbeiðni er úthlutin**.  
    2.  **Farið úr gildinu eins og**  alltaf  **í reitnum á svæði condition**.  
    3.  **Í reitnum svar**  er  **valið svartengill** . Á síðunni viðbrögð  **við**  verkflæði, í  **reitnum velja svar**, er valið  **senda samþykkisbeiðni fyrir færsluna og tilkynningarsvar**  stofnað.  
    4. Velja **Í lagi**.  
8. Í næstu línu er bætt við öðru verkflæðisskrefi fyrir  **samþykktarbeiðnina, tilvikinu hafnað** .  

    1.  **Í reitnum þegar atburður**  stendur skal tilgreina  **samþykktarbeiðni sem er hafnað**.  
    2.  **Farið úr gildinu eins og**  alltaf  **í reitnum á svæði condition**.  
    3.  **Í reitnum svar**  er  **valið svartengill** . Síðan er  **smellt á síðuna viðbrögð**  við verkflæði í  **reitnum**  Velja svar  **til að henda svari nýju gildi** .  
    4.  **Veldu tengilinn bæta við fleiri svörum**, Bættu svo við færslu fyrir  **höfnun samþykkisbeiðninnar fyrir færsluna og Búðu til tilkynningarsvar** 
    5. Velja **Í lagi**.  
9. Ef gera á verkflæðið virkt er kveikt á  **virkjunni**  skipta.  

Eftirfarandi mynd gefur yfirlit yfir niðurstöður þessarar aðgerðar.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Skýring á samþykktarverkflæði lánardrottnaheitis.":::

Næst skal prófa verkflæðið með því að opna fyrirliggjandi lánardrottnaspjald og breyta nafni þeirra. Staðfestið að samþykktarbeiðni sé send eftir að nafni lánardrottins er breytt.

## <a name="see-related-microsoft-trainingtrainingmodulescreate-workflows" />Sjá tengda [Microsoft þjálfun](/training/modules/create-workflows/)

## <a name="see-also" />Sjá einnig .

[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)  
[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Uppsetning tilkynninga um samþykktarverkflæði](across-setting-up-workflow-notifications.md)  
[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)  
[Eyða verkflæði samþykkta](across-how-to-delete-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
