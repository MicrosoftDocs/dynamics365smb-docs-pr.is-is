---
title: Stofna samþykktarverkflæði til að tengja verk
description: Læra hvernig á að stofna verkflæði sem tengja verk sem framkvæmd eru af ólíkum einstaklingum í viðskiptaferlum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/29/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Stofna verkflæði til að tengja verk í viðskiptaferlum

Hægt er að stofna verkflæði sem tengja verk í viðskiptaferlum sem eru framkvæmd af ólíkum notendum. Hægt er að taka kerfisverk eins og sjálfvirka bókun, sem skref í verkflæði sem á undan er komið eða á eftir notendaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði.  

Á síðunni **Verkflæði** skal stofna verkflæði með því að skrá verkstigin í línunum. Hvert skref samanstendur af kveikju og svari:

* Tilvik sem tilgreinir skilyrðin sem hefja verkflæðið.
* Verkflæðissvar sem skilgreinir hvað verkflæðið gerir.

[!INCLUDE[workflow](includes/workflow.md)]

Þegar verkflæði eru stofnuð er hægt að afrita skref úr núgildandi verkflæði eða úr verkflæðissniðmátum. Sniðmát verkflæðis eru óbreytanleg verkflæði veitir [!INCLUDE[prod_short](includes/prod_short.md)] . Kenni fyrir verkflæðissniðmát eru forskeytin "MS-" eins og í "MS-PIW". Frekari upplýsingar eru í [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Allar tilkynningar um verkflæðisskref eru sendar um verkröð. Ganga skal úr skugga um að verkröðin endurspegli þarfir fyrirtækisins. Frekari upplýsingar eru í [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Skýring á verkflæðisdæmi.":::

Verkflæði er skipt í þrjá hluta:

1. **Þegar atburður**  
   Hér er kveikurinn valinn.  
   Dæmi um gikk:
   * Aðalgagnafærslu er breytt
   * Færslubókarlína er stofnuð
   * Skjal á innleið er stofnað eða gefið út
   * Óskað er eftir samþykki skjals
2. **Við skilyrði**  
   Skilyrðin **eru** tengd atvikinu og leyfa stofnun afmarkana til að ákveða hvernig verkflæðið heldur áfram.
3. **Þá svar**  
   Svörin **tilgreina** næstu skref í verkflæðinu.

Valkostir fyrir atburði og svör eru skilgreindir af kerfinu. Til að bæta við nýjum valkostum þarf að þróa viðbót.

## Til að stofna verkflæði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Verkflæði** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Til að stofna verkflæðið úr verkflæðissniðmáti á síðunni **Verkflæði** skal velja aðgerðina **Nýtt verkflæði úr sniðmáti** . Frekari upplýsingar eru í [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  
5. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
6. Í **Flokkur** reitnum skal tilgreina hvaða flokki verkflæðið tilheyrir.  
7. Í reitnum **Þegar tilvik** skal tilgreina tilvik sem verður að eiga sér stað til að að verkflæðisskref geti hafist.  

   Þegar reiturinn **er valinn birtir** síðan Verkflæðisvik lista yfir öll tiltæk verkflæðisviðvik.  
8. Í reitnum **Á skilyrði** skal tilgreina eitt eða fleiri skilyrði sem þarf að uppfylla fyrir atburðinn í reitnum **Hvenær atburður** getur átt sér stað.  

   Þegar reiturinn er **valinn birtir** síðan Skilyrði tilviks afmörkunarreiti sem geta verið skilyrði fyrir atburðinum. Hægt er að bæta við nýjum afmörkunarreitum ef óskað er.  

   Ef verkflæðisvikið er breyting á tilteknum reit á færslu skal nota síðuna **Skilyrði tilviks** til að velja reitinn og tegund breytingarinnar.  

   1. Til að tilgreina reitarbreytingu fyrir tilvik skal, á síðunni **Aðstæður tilviks** í reitnum **Reitur** velja reitinn sem er breytt.  
   2. Í reitnum **Stjórnandi** skal velja annað hvort **Minnkað**, **Aukið**, eða **Breytt**.  
9. Í reitnum **Þá svörun**, tilgreinið viðbrögð sem fylgja þegar verkflæðistilvik á sér stað.  

   Þegar reiturinn **er valinn birtir síðan Verkflæðissvör** lista yfir öll tiltæk svör og svarvalkosti verkflæðis.  
10. Á flýtiflipanum **Valkostir fyrir valið svar** eru tilgreindir valkostir fyrir verkflæðissvarið með því að velja gildi í mismunandi reitum sem birtast, eins og hér segir:  

    1. Til að tilgreian valkosti fyrir verkflæðissvar sem felur í sér að senda tilkyningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    > [!NOTE]
    > Þessir reitir eru mismunandi eftir því hvaða svar var valið.

       |Svæði|Heimildasamstæða|
       |-----|-----------|
       |**Tilkynna sendanda**|Tilgreina hvort tilkynna skuli samþykktarbeiðnina í stað viðtakanda samþykktarbeiðninnar. Ef gátreiturinn er valinn er reiturinn **Notandakenni** viðtakanda óvirkur þar sem beiðnin um samþykkið, sendanda, verður tilkynnt í staðinn. Heiti verkflæðissvars breytist til samræmis, í **Búa til tilkynningu fyrir &lt;Sendanda&gt;**. Ef gátreiturinn er ekki valinn er **heiti verkflæðissvarsins Stofna tilkynningu fyrir &lt; notanda&gt;** stofnað.|
       |**Notandaauðkenni viðtakanda**|Tilgreina notandann sem senda verður tilkynninguna til. **Athugið**: Þessi valmöguleiki er aðeins tiltækur fyrir verkflæðisvörun með staðgengil fyrir tiltekinn notanda. Fyrir verkflæðissvör án frátaka fyrir notendur er tilkynningarmóttakandi yfirleitt skilgreindur af **notandauppsetningu samþykktar**.|
       |**Færslugerð tilkynningar**|Tilgreina kveik fyrir tilkynningu verkflæðis. Kveikurinn getur verið færslubreyting, samþykktarbeiðni eða gjalddagi.|
       |**Tengja marksíðu**|Tilgreina síðuna sem tengillinn í tilkynningunni opnast á. Síðan verður að hafa sömu upprunatöflu og færslan sem um ræðir.|
       |**Sérsniðinn tengill**|Tilgreina veffang tengils sem er innifalin í tilkynningunni auk tengils á síðuna.|

    2. Til að tilgreina valkosti fyrir verkflæðissvar sem felur í sér að senda tilkynningu skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

       |Svæði|Heimildasamstæða|  
       |-----|-----------|  
       |**Reikniregla gjalddaga**|Tilgreina dagafjölda sem samþykkjandi verður að leysa beiðnina. Tímabilið hefst þegar beiðnin er send.|
       |**Framselja eftir**|Tilgreina hvort og hvenær samþykktarbeiðni er sjálfkrafa úthlutað til staðgengilsins. Hægt er að velja sjálfkrafa að úthluta einn, tvo eða fimm dögum eftir þá dagsetning þegar beðið var um samþykkt.|
       |**Gerð samþykkjanda**|Tilgreina hver er samþykkjandi, samkvæmt uppsetningu á notendum samþykktar og notendur verkflæði. Þegar reiturinn er stilltur á **Sölumaður/innkaupaaðili** er notandinn sem tilgreindur er í reitnum **Sölumaður/Innkaup. Reiturinn Kóti** á síðunni **Notandauppsetning samþykktar** ákvarðar samþykkjandann. Færslur fyrir samþykktarbeiðni eru þá stofnaðar samkvæmt gildinu í reitnum **Afmörkunargerð samþykkjanda**. Fá nánari upplýsingar hjá [Notendum samþykktar](across-how-to-set-up-workflow-users.md).|
       |**Sýna staðfestingarskilaboð**|Tilgreina hvort birta eigi staðfestingarboð eftir að notandi biður um samþykki.|
       |**Afmörkunargerð samþykkjanda**|Tilgreina áhrif takmarkana fyrir samþykkendur. Samþykktarmörk samþykkjanda verða að vera yfir gildinu fyrir beiðnina. Eftirfarandi möguleikar eru til staðar: <ol><li>**Keðja samþykkjenda** tilgreinir að færslur samþykktarbeiðni eru stofnaðar fyrir alla samþykkjendur frá og með fyrsta samþykkjanda sem uppfyllir skilyrði</li><li>**Beinn samþykkjandi** tilgreinir að samþykktarbeiðnisfærsla er aðeins stofnuð fyrir næsta samþykkjanda, sama hver samþykktarmörk hans eru.</li><li>**Fyrsti viðurkenndi samþykkjandi** tilgreinir að samþykktarbeiðnifærsla sé aðeins stofnuð fyrir fyrsta samþykkjanda umsækjanda.</li><li>**Tiltekinn samþykkjandi** tilgreinir að notandinn sem valinn er sé tilkynntur í reitnum **Kenni** samþykkjanda.</li></ol>|

    3. Ef tilgreina á valkosti fyrir verkflæðissvar sem felur í sér að stofna færslubókarlínur er reitirnir fylltir út eins og lýst er í eftirfarandi töflu.  

       |Svæði|Heimildasamstæða|  
       |-----|-----------|  
       |**Heiti sniðmáts færslubókar**|Tilgreina heiti sniðmáts færslubókarinnar sem stofnuð eru í tilteknu bókarlínurnar.|  
       |**Heiti færslubókarkeyrslu**|Tilgreina heiti sniðmáts færslubókarrununnar sem stofnuð eru í tilteknu bókarlínurnar.|  

11. Velja skal hnappana **Auka inndrátt** og **Minnka inndrátt** til að draga tilviksheiti inn í reitnum **Þegar** til að skilgreina stöðu skrefsins í verkflæðinu.  

    1. Færa inn atburðinn undir heiti fyrra skrefs til að gefa til kynna að það sé næsta skref.  
    2. Tilgreina skal að verkstigið sé eitt af nokkrum öðrum skrefum sem kunna að hefjast, allt eftir ástandi þess, með því að færa inn nafn atburðarins til að passa við önnur skref. Raðið slíkum valskrefum eftir forgangi með því að setja mikilvægasta skrefið efst.  

    > [!NOTE]  
    >  Aðeins er hægt að breyta inndrætti verkstigs sem ekki á eftir að koma.  

12. Þrep 7 til 11 eru endurtekin til að bæta við fleiri verkflæðisskrefum, annað hvort fyrir eða eftir stofnað verkstig.  
13. Kveikja á vífærslunni **Virkt** til að tilgreina að verkflæðið muni hefjast þegar atburðurinn á fyrsta þrepinu af gerðinni **Komustaður** á sér stað. Frekari upplýsingar má finna á [Nota verkflæði](across-use-workflows.md).  

> [!NOTE]  
> Ekki virkja verkflæði fyrr en þú ert viss um að það sé tilbúið.  

> [!TIP]  
> Til að kanna tengslin milli taflna sem notaðar eru í verkflæðum skal velja Eiginleikann ![Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið skal færa inn **Verkflæði – Töflutengsl**.  

## Dæmi um hvernig nýtt verkflæði er búið til með því að nota fyrirliggjandi tilvik

Eftirfarandi dæmi stofnar verkflæði til að samþykkja breytingu á heiti lánardrottins:

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
    2. Í reitnum **Ástand** er valið orðið **Alltaf**. Á síðunni **Tilviksskilyrði** skal velja **Bæta við skilyrðum fyrir því hvenær gildi reits breytist** og síðan er reiturinn **Heiti** valinn. Niðurstaðan úr þessu skrefi er að skilyrðið lesist sem *Heiti er breytt*.  
    3. Í reitnum **Síðan svar** skal velja **tengilinn Velja svar** . Á síðunni **Verkflæðissvör**, í reitnum **Velja svar**, skal velja **bakfæra gildið í reitnum \<Field\> á færslunni og vista breytingasvarið** . Síðan er reiturinn **Heiti** tilgreindur **í valkostum fyrir hlutann Valið svar** .  
    4.  **Veldu tengilinn Bæta við fleiri svörum** og bættu svo við færslu fyrir **Stofna samþykktarbeiðni fyrir færsluna með því að nota tegund <%1> samþykkjanda og <%2>** svars.  
    5. Í hlutanum **Valkostir fyrir valið svar** fyrir nýja svarið er reitnum **Samþykkjandi** **breytt í Notendaflokkur** verkflæðis. Síðan skal tilgreina notendaflokk í reitnum **Notendaflokkur** verkflæðis. Frekari upplýsingar má finna á [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  
    6. Bæta við þriðja svari, **Senda beiðni um samþykki fyrir færsluna og stofna tilkynningu**.  
    7. Bæta við fjórðu svari,Sýna **skilaboð "%1"**. Síðan, í **valkostum fyrir hlutann Valið svar**, í reitnum **Skilaboð**, tilgreinið **samþykktarbeiðni.**  
    8. Velja skal **Í lagi** til að fara aftur í verkflæðisskrefið.  

5. Í næstu línu er nýju verkflæðisskrefi **bætt við fyrir samþykktarbeiðnina.** 

    1. Í reitnum **Þegar tilvik** er tilgreint **samþykktarbeiðni er samþykkt**.  
    2. Valmynd línunnar er valin og aukning inndráttar **valin**.  
    3. Í reitnum **Á skilyrði** skal velja **Alltaf**. Í reitnum **Samþykktir í undirbúningi** er síðan tilgreint **0**. Skilyrðið les sem **Bíður samþykktar:0** til að gefa til kynna að beiðnin krefst ekki fleiri samþykkjanda.  
    4. Í reitnum **Síðan svar** skal velja **tengilinn Velja svar** . Á síðunni **Verkflæðissvar**, í reitnum **Velja svar**, skal velja **Senda samþykktarbeiðni fyrir færsluna og stofna tilkynningarsvar** .  
    5. Velja **Í lagi**.  
6. Í næstu línu er bætt við öðru verkflæðisskrefi fyrir **samþykktarbeiðnina.**   

    1. Í reitnum **Þegar tilvik** er tilgreint **samþykktarbeiðni er samþykkt**.
    2. Í reitnum **Á skilyrði** skal velja **Alltaf**. Síðan er tilgreint í **reitnum**  Bíður samþykktar **>0**. Skilyrðið les sem **Bíður samþykktar:>0** til að gefa til kynna að þetta sé ekki síðasti samþykkjandinn.  
    3. Í reitnum **Síðan svar** skal velja **tengilinn Velja svar** . Á síðunni **Verkflæðissvar**, í reitnum **Velja svar**, skal velja **Senda samþykktarbeiðni fyrir færsluna og stofna tilkynningarsvar** .  
    4. Velja **Í lagi**.  
7. Í næstu línu skal bæta við verkflæðisskref fyrir **samþykktarbeiðnina er úthlutað tilviki** .  

    1. Í reitnum **Þegar tilvik** er tilgreint **samþykktarbeiðni er úthlutað**.  
    2. Í reitnum **Ástand** er gildið látið standa sem **Alltaf**.  
    3. Í reitnum **Síðan svar** skal velja **tengilinn Velja svar** . Á síðunni **Verkflæðissvar**, í reitnum **Velja svar**, skal velja **Senda samþykktarbeiðni fyrir færsluna og stofna tilkynningarsvar** .  
    4. Velja **Í lagi**.  
8. Í næstu línu er bætt við öðru verkflæðisskrefi fyrir **samþykktarbeiðnina er hafnað** .  

    1. Í reitnum **Þegar atvik** er tilgreint **samþykktarbeiðni er hafnað**.  
    2. Í reitnum **Ástand** er gildið látið standa sem **Alltaf**.  
    3. Í reitnum **Síðan svar** skal velja **tengilinn Velja svar** . Á síðunni Verkflæðissvör, í reitnum **Velja svar**, skal velja Fleygja nýju **gildissvarinu** . **·**   
    4. Tengillinn **Bæta við fleiri svörum** er valinn, síðan er færslu **hafnað samþykktarbeiðninni fyrir færsluna og tilkynningarsvar** stofnað
    5. Velja **Í lagi**.  
9. Til að virkja verkflæðið skal kveikja á virku **vífæringunni**.  

Eftirfarandi mynd birtir yfirlit yfir niðurstöður ferlisins.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Skýring á samþykktarverkflæði lánardrottnaheitis.":::

Næst skal prófa verkflæðið með því að opna lánardrottnaspjald sem þegar er til og breyta nafni þeirra. Ganga úr skugga um að beiðni um samþykki sé send eftir að nafni lánardrottins hefur verið breytt.

## Sjá einnig .

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
