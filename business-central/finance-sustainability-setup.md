---
title: Sjálfbærniuppsetning
description: Læra hvernig setja á upp sjálfbærniaðgerðir.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, equivalent, CO2e, CO2, carbon, role center, fees'
ms.search.form: '6221, 6235, 6245'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-module-setup"></a>Uppsetning sjálfbærnieiningar

Áður en einingin Sjálfbærni getur unnið rétt þarf að setja upp nokkur grunneftirlit og leiðbeiningar sem tengjast allri virkninni.

Til að setja upp eininguna Sjálfbærni skal fylgja skrefunum:

## <a name="role-center"></a>Mitt hlutverk

Mælt er með því að nýta *hlutverkamiðstöð sjálfbærnistjóra fyrir einstaklinga sem hafa aðalábyrgð* á sjálfbærni. Til að grunnstilla þetta hlutverk skal fylgja skrefunum:  

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Mínar** stillingar og velja síðan viðeigandi tengja.
2. Í reitnum **Hlutverk** er síðan Tiltæk hlutverk **valin** .
3.  **Línan Sjálfbærnistjóri** er valin.
4. Valið er **Í lagi**.

 *Hlutverkamiðstöð sjálfbærnistjóra auðveldar* skilvirka stjórnun allra lykilsvæða sem tengjast sjálfbærni. Hún nær yfir grunnaðgerðir sjálfbærni, sem og fjárhags- og innkaupaferli. Þar að auki veitir það sýnileika inn í mikilvægustu sjálfbærnitengd afkastaþörf afkastaþarfa.

## <a name="sustainability-setup"></a>Sjálfbærniuppsetning

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Sjálfbærnigrunnur** og velja síðan viðeigandi tengja.
2. Á flýtiflipanum **Almennt** eru skilgreindir nauðsynlegir reitir sem tengjast einingunni Sjálfbærni.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | **Kóti mælieiningar útblásturs** | Tilgreina mælieiningarkótann sem er notaður til að skrá losun. |
    | **Aukastafir í útblæstri** | Tilgreina fjölda aukastafa sem sýndir eru fyrir útblástursupphæðir. Sjálfgefna stillingin *2:5* merkir að minnst tveir tugastafir og mest fimm tugastafir eru sýndir fyrir allar upphæðir. Einnig er hægt að færa inn fast númer. Ef til dæmis er fært inn *2* birtast tveir aukastafir fyrir allar upphæðir. |
    | **Land/svæði áskilið** | Tilgreina þarf hvort land/svæði er áskilið. Notendur geta stillt lands-/svæðisreitinn í færslubókum jafnvel þótt þessi reitur sé ekki valinn. Hins vegar þarf notendur að stilla lands-/svæðisreitinn áður en bókað er. |
    | **Ábyrgðarstöð áskilin** | Tilgreina þarf hvort ábyrgðarstöðin sé áskilin. Ábyrgðarstöðina er hægt að nota sem aðstöðu til að mæla losun sem byggir á aðstöðu. Notendur geta stillt ábyrgðarstöðina í færslubókum jafnvel þótt ekki sé valinn þessi reitur. En með því að velja hana er þess krafist að notendur stilli reitinn ábyrgðarstöð áður en bókað er. |
    | **Loka breytingu á útreikningi ef færslur eru til** | Tilgreint er hvort breytingar á útreikningsstofni (reiknireglu) á stigi reikningstegundar eru lokaðar þegar sjálfbærnifærslan hefur þegar verið jöfnuð. |
    | **Gera villuprófun bakgrunns virka** | Tilgreina hvort bakgrunnsvilluprófun á sjálfbærnibókarlínum er virk. |

    > [!NOTE]
    > Þegar bakgrunnsvilluprófun hefur verið gerð virk eða gerð virk í færslubókum þarf að skrá sig aftur inn áður en nýja uppsetningin er sett í gang.

3. Á flýtiflipanum **Innkaup** eru skilgreindir nauðsynlegir reitir sem tengjast notkun sjálfbærniaðgerða í innkaupaferlinu.  

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | **Nota losun í innkaupaskjölum** | Ef þessi reitur er virkjaður birtast sjálfbærnitengdir reitir og aðgerðir í innkaupaskjölum, svo sem **Sjálfbærnireikningur** eða mismunandi losun. |

4. Á flýtiflipanum **Útreikningar** eru nauðsynlegir reitir sem eru tengdir reiknireglunum sem notaðar eru til að reikna út útblástur.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | **Eldsneyti/rafmagn aukastafir** | Tilgreina fjölda aukastafa sem sýndir eru fyrir upphæðir eldsneytis/rafmagns. Sjálfgefna stillingin *2:5* merkir að minnst tveir tugastafir og mest fimm tugastafir eru sýndir fyrir allar upphæðir. Einnig er hægt að færa inn fast númer. Ef til dæmis er fært inn *2* birtast tveir aukastafir fyrir allar upphæðir. |
    | **Fjarlægð tugastafir** | Tilgreindur er fjöldi aukastafa sem sýndir eru fyrir mælingar á fjarlægð. Sjálfgefna stillingin *2:5* merkir að minnst tveir tugastafir og mest fimm tugastafir eru sýndir fyrir allar upphæðir. Einnig er hægt að færa inn fast númer. Ef til dæmis er fært inn *2* birtast tveir aukastafir fyrir allar upphæðir. |
    | **Sérsniðnir aukastafir í upphæð** | Tilgreina fjölda aukastafa sem sýndir eru fyrir sérsniðnar upphæðir. Sjálfgefna stillingin *2:5* merkir að minnst tveir tugastafir og mest fimm tugastafir eru sýndir fyrir allar upphæðir. Einnig er hægt að færa inn fast númer. Ef til dæmis er fært inn *2* birtast tveir aukastafir fyrir allar upphæðir. |

5. Á flýtiflipanum **Skýrslur** skal ljúka uppsetningunni með því að grunnstilla reitina sem tengjast skýrslugerð til yfirvalda.

    > [!NOTE]
    > Í útgáfu 24.0 [!INCLUDE[prod_short](includes/prod_short.md)]  styður engin yfirvöld skýrslugerð. Þess vegna eru reitir sem eru tengdir grunnstillingu þessarar aðgerðar á flýtiflipanum **Skýrslur** fyrir síðari skýrslugerðarmöguleika. Félagar geta þó einnig notað þessa reiti í staðfærðum útgáfum.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | **Losun eining skipurits mælieiningarkóti** | Tilgreina skal mælieiningarkótann sem er notaður til að gefa skýrslu um losun þar sem hægt er að nota aðra mælieiningu þegar yfirvöld gefa skýrslu um það. Þessi reitur á ekki við staðlaðar skýrslur. |
    | **Skýrslugerðarstuðull** | Tilgreina skal mælieiningarstuðulinn sem er notaður til að skrá losun ef notuð er önnur mælieining þegar yfirvöld eru send til yfirvalda. |
    | **Losun sléttunarnákvæmni** | Tilgreina stærð þess tímabils sem notað er við sléttun útblástursupphæða þegar yfirvöld eru send til yfirvalda. |
    | **Tegund útblásturs sléttun** | Tilgreina hvernig kerfið sléttar losunarupphæðir þegar skýrslur eru gerðar til yfirvalda. Eftirfarandi valkostir eru í boði: **Næst**, **Upp** og **Niður**. |

## <a name="emission-fees"></a>Losunargjöld

Til að rekja innri kolefnisgjöld eða reikna losun þína með því að nota CO2-jafngildisgildi þarf að grunnstilla **síðuna Útblástursgjöld** . Til að setja upp þessar upplýsingar skal fylgja eftirfarandi skrefum:  

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Losunargjöld** og velja síðan viðeigandi tengja. 
2. Í reitnum **Tegund** losunar skal velja GHG losun sem á að grunnstilla: **CO2**, **CH4** eða **N2O**. Þessi valkostur er áskilinn.   
3. Nánari tegund **sviðs** er tilgreind. Ef reiturinn er hafður auður gildir hann um öll svið en hægt er að grunnstilla fyrir hvert umfang.  
4. Hægt er að grunnstilla **upphafsdagsetningu** og **lokadagsetningu**. Það agnir þýðir að hægt er að nota mismunandi grunnstillingar á mismunandi tímabili. 
5. Lands **-/svæðiskóti** og **ábyrgðarkóti** eru valfrjálsir reitir og hægt er að velja hvort nota eigi þá. Þessir reitir geta verið gagnlegir þar sem hægt er að hafa mismunandi kolefnisgjöld eftir löndum eða nota mismunandi umbreytingar í CO2e fyrir hvert land eða á aðstöðu (ábyrgðarstöð).  
6. Reiturinn **Kolefnisgjald** stendur fyrir innra kolefnisgjaldið sem fyrirtækið innheimtir sjálft fyrir hverja einingu CO2 jafngildi því sem það gefur út. Hana má nota samkvæmt sumum reglum innanlands eða svæðis, en einnig við innri útreikninga. **Kolefnisgjald** verður reiknað í hvert sinn sem losun er bókuð og þessar upplýsingar birtast í **Sjálfbærnibókarfærslunum**, án frekari bókunar í **fjárhag**. Hægt er að setja upp **Kolefnisgjald** á hverja mælieiningu sem til er í **Sjálfbærniuppsetningunni** og aðeins er hægt að útbúa það fyrir línuna þar sem **tegund** losunar er **CO2**. 
7. Jafngildisstuðullinn **kolefnisjafnar** tilgreinir safnkostinn sem breytir áhrifum ýmissa gróðurhúsalofttegunda í jafngildismagn koltvísýrings samkvæmt hnattrænni hlýnun þeirra. Ef útblásturstegundin **er** CO2 **verður** Jafngildisstuðull *kolefnis alltaf 1* og ekki er hægt að breyta því gildi, vegna þess að CO2 er það tilvísunargas sem notað er til að reikna út hnattræna hlýnunarmöguleika (GWP) annarra gróðurhúsalofttegunda; þar sem CO2 er grunnlínan er GWP þess stillt á *1*. Fyrir aðrar GHG-gastegundir verða notendur að grunnstilla gildin handvirkt. Til að gera rétta útreikninga er hægt að nota eftirfarandi dæmi: Ef við gerum ráð fyrir að 1 kíló af N2O jafngildi 298 kílóum af CO2, þá þarf að reikna 1/298 og útkoman sem þú þarft til að hópa verður 0.00336.  

> [!NOTE]
> **Reiturinn Kolefnisgjald** í **sjálfbærnibókarfærslunum** verður ekki reiknaður út frá gildum **CO2-losunar** . Þess í stað mun reiturinn [!INCLUDE[prod_short](includes/prod_short.md)] CO2e Losun **notast sem grunnur að þessari reiknireglu** . **Reiturinn CO2e Losun** verður reiknaður út frá öllum losun sem bókuð er til færslu og **Kolefnisjöfnunarstuðullinn** sem er grunnstilltur fyrir hverja gastegund á síðunni **Losunargjöld** .  

Ef losunargjöldin **voru ekki grunnstillt** áður en sjálfbærnifærslurnar voru bókaðar og reikna á kolefnisgjöldin og CO2e afturvirkt þarf að keyra aðgerðina **Reikna út útblástursgjöld** til að uppfæra gildi í **Sjálfbærnibókarfærslunum**.  

## <a name="see-also"></a>Sjá einnig .

[Fjármál](finance.md)    
[Yfirlit yfir sjálfbærnistjórnun](finance-manage-sustainability.md)    
[Bókhaldslykill sjálfbærnireikninga og fjárhagur](finance-sustainability-accounts-ledger.md)    
[Skrá sjálfbærnifærslur](finance-sustainability-journal.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
