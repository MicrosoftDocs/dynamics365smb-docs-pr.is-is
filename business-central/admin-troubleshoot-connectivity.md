---
title: Úrræðaleit tengigetu
description: Lýsir því hvernig á að nota síðu úrræðaleitar vegna tengigetu til að bera kennsl á og laga vandamál við að tengjast Business Central á netinu.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'connectivity, troubleshooting, connection problems'
ms.date: 11/24/2023
ms.author: jswymer
ROBOTS: NOINDEX
ms.service: dynamics-365-business-central
---

# <a name="troubleshoot-connectivity-for-business-central"></a>Úrræðaleit vegna tengingar fyrir Business Central

> **Á VIÐ UM:** [!INCLUDE[prod_short](includes/prod_short.md)] á netinu
>
> Þessi eiginleiki er í forútgáfu sem stendur. Virknin og fylgigögn geta breyst í síðari útgáfum. Veldu ![Breyta grein í GitHub](media/github-edit-pencil.png) ef þú vilt leggja þitt af mörkum ef þú rekur augun í eitthvað í fylgigögnunum. **Breyta** og leggja til breytingar. Við munum síðan skoða málið!

[!INCLUDE[prod_short](includes/prod_short.md)] á netinu inniheldur síðuna **Úrræðaleita tengigetu** sem hægt er að nota til að bera kennsl á vandamál varðandi tengingu þína við netþjónustuna. Það eru nokkur atriði sem hafa áhrif á tengigetu við Business Central, eins og stillingar á eldvegg netkerfisins eða skilgreiningu á þjónustu lénsheitis. Síðan gerir þér kleift að keyra lista yfir tékka sem greina algeng Business Central tengingar vandamál. Hægt er að nota upplýsingarnar til að reyna að laga vandamálin á eigin spýtum eða koma þeim áleiðis til þjónustufulltrúa.

> [!NOTE]
> Síðan **Úrræðaleita tengigetu** prófar ekki afköst eða áreiðanleika netkerfisins, eins og hraða tengingarinnar. Það staðfestir aðeins tengigetu við mismunandi tilföng.

## <a name="start-the-connectivity-check"></a>Hefja athugun á tengigetu

1. Opnaðu netvafra.
2. Í veffanginu skal færa inn vefslóðina sem er notuð til að opna Business Central og bættu við `/connectivity` í lokin. 

    Ef þú notar til dæmis `https://businesscentral.dynamics.com` skal færa inn:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

    Eða, ef vefslóðin inniheldur auðkenni leigjanda, eins og `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB`, þá myndir þú færa inn:

    ```http
    https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
    ```
 
3. Á síðunni **Úrræðaleita tengigetu** skal velja **Hefja athugun**.

    Röð athugana er keyrð og niðurstaða hverrar athugunar er sýnd:

    - ![Athugun tengigetu tókst.](media/connectivity-check.png) gefur til kynna að athugunin hafi heppnast.
    - ![Athugun á tengigetu mistókst.](media/connectivity-failed.png) gefur til kynna að athugunin hafi misheppnast. Farðu yfir skilaboðin hér að neðan til að fá frekari upplýsingar.
    - ![Athugun tengigetu var ekki keyrð.](media/connectivity-blocked.png) gefur til kynna að athugunin var ekki keyrð, yfirleitt vegna þess að fyrri athugun mistókst. Farðu yfir skilaboðin hér að neðan til að fá frekari upplýsingar.

4. Til að keyra athugunina aftur skaltu velja **Endurræsa athugun**.

Í eftirfarandi köflum eru athuganir sem eru keyrðar útskýrðar og gefnar nokkrar ábendingar til að laga vandamálin.

## <a name="basic-internet-connectivity"></a>Grunntenging við internetið

Athugar hvort þú sért með tengingu við internetið með því að staðfesta hvort þú hafir aðgang að þekktu almennu léni eins og www.bing.com.

|Vandamál|Það sem hægt er að prófa|
|-------|-------------|
|Vafrinn þinn styður ekki þessa prófun|Opnaðu síðuna í studdum vafra og reyndu aftur. Listi yfir studda vafra er að finna í [Lágmarkskröfur fyrir notkun Business Central - Vafrar](product-requirements.md#browsers)|
|Ekki tókst að senda ping-skipun á þjóninn á eftirfarandi vefslóð: {url}|Athugaðu stillingar eldveggsins.|

## <a name="cdn-content-delivery-network-resources-loading"></a>Hleðsla á CDN-úrræðum

[!INCLUDE[prod_short](includes/prod_short.md)] notar Azure-efnisbirtingarnet (CDN) til að bjóða upp á úrræði sem þarf til að keyra Business Central-vefbiðlarann. Þessi athugun staðfestir að nauðsynleg úrræði séu til staðar og aðgengileg með því að senda ping-skipun á tilvik Business Central í CDN.

|Vandamál|Það sem hægt er að prófa|
|-------|-------------|
|Vafrinn þinn styður ekki þessa prófun|Sjá athugunina **Grunntenging við internetið**.|
|Ekki tókst að senda ping-skipun á þjóninn á eftirfarandi vefslóð: {url}|Athugaðu stillingar eldveggsins.|

## <a name="user-authentication"></a>Sannvottun notanda

Athugar hvort gildandi notandi skráir sig inn með gildum Business Central reikningi.

|Vandamál|Það sem hægt er að prófa|
|-------|-------------|
|Enginn notandi er auðkenndur eins og er|Skráðu þig inn í Business Central með gildu notandanafni og aðgangsorði.|

## <a name="business-central-environments-discovery"></a>Uppgötvun um umhverfi Business Central

Athuganir á umhverfum Business Central sem eru tiltækar sannvottuðum notanda, staðfestir síðan hvort hægt sé að auðkenna notandann í umhverfinu.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Vandamál|Það sem hægt er að prófa|
|-------|-------------|
|Enginn auðkenndur notandi til að framkvæma þessa athugun fyrir|Sjá athugunina **Sannvottun notanda**.|
|Ekki tókst að sækja tiltæk umhverfi fyrir reikninginn.|Skoða lista yfir tiltæk umhverfi í stjórnendamiðstöð Business Central.|
|Rangt notandanafn eða aðgangsorð eða notandi er ekki með gildan reikning.| Ganga þarf úr skugga um að notandi skrái sig inn með réttu notandanafni og aðgangsorði.|

## <a name="application-service-connectivity"></a>Tengigeta hugbúnaðarþjónustu

Gengur úr skugga um að sannvottaður notandi geti tengst við uppgötvað umhverfi, sem hefst yfirleitt á vinnsluumhverfinu.

|Vandamál|Það sem hægt er að prófa|
|-------|-------------|
|Enginn auðkenndur notandi til að framkvæma þessa athugun fyrir|Sjá **Athugun á sannvottun notanda**.|
|Ekki tókst að sækja tiltæk umhverfi fyrir reikninginn.|Sjá **Uppgötvun um umhverfi Business Central**.|
|Ekkert klasaaðsetur til að framkvæma þessa athugun fyrir|Skoða lista yfir tiltæk umhverfi í stjórnendamiðstöð Business Central.|
|Endastöð útgáfu er ekki til|Skoða lista yfir tiltæk umhverfi í stjórnendamiðstöð Business Central.|

## <a name="web-server-connectivity"></a>Tengigeta vefþjóns

Athugar hvort sannvottaður notandi getur komið á tengslum við vefþjóninn.

|Vandamál|Það sem hægt er að prófa|
|-------|-------------|
|Enginn sannvottaður notandi til að framkvæma þessa athugun|Sjá **Athugun á sannvottun notanda**.|
|Ekki tókst að sækja tiltæk umhverfi fyrir reikninginn.|Sjá **Uppgötvun um umhverfi Business Central**.|
|Ekkert klasaaðsetur til að framkvæma þessa athugun fyrir|Skoða lista yfir tiltæk umhverfi í stjórnendamiðstöð Business Central.|
|Ekki tókst að koma á tengingu við vefþjóninn|Hreinsa skyndiminnið og endurhlaða síðuna.|

## <a name="service-health-status"></a>Ástand þjónustu

Gefur skýrslur um þjónustuheilbrigðisstöðu Business Central með því að athuga með lýsandi faraldur.

|Vandamál|Það sem hægt er að prófa|
|-------|-------------|
|Enginn sannvottaður notandi til að framkvæma þessa athugun|Sjá **Athugun á sannvottun notanda**.|
|Því miður, Business Central er ekki til bráðabirgða. Reyna skal aftur síðar.|Reyna skal aftur síðar.|

## <a name="see-also"></a>Sjá einnig .

[Tilföng fyrir Hjálp og notendaþjónustu](product-help-and-support.md)  
[Yfirlit yfir verkefni til að setja upp Business Central](setup.md)  
[Algengar spurningar um notkun Business Central](across-faq.yml)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Stjórnunarmiðstöð Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
