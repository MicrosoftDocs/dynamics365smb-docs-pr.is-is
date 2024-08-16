---
title: Stjórna aðgangi með öryggishópum
description: Í þessari grein er því lýst hvernig á að nota öryggisflokka til að skilgreina notendaheimildir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862, 9875_Primary, 9874_Primary, 9873_Primary, 9872_Primary, 9877_Primary, 9869_Primary, 9868_Primary, 9871_Primary'
ms.date: 04/15/2024
ms.service: dynamics-365-business-central
---

# Stjórna aðgangi að Business Central með öryggishópum

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Öryggishópar auðvelda stjórnendum að hafa umsjón með notendaheimildum. Til dæmis [!INCLUDE [prod_short](includes/prod_short.md)] eru þær endurnýtanlegar í Dynamics 365 forritum, svo sem SharePoint Online, CRM Online og [!INCLUDE [prod_short](includes/prod_short.md)]. Stjórnendur bæta heimildum við öryggishópa þeirra [!INCLUDE [prod_short](includes/prod_short.md)] og þegar þeir bæta notendum í hópinn eiga heimildirnar við um alla meðlimi. Til dæmis getur kerfisstjóri stofnað [!INCLUDE [prod_short](includes/prod_short.md)] öryggishóp sem gefur sölumönnum kleift að stofna og bóka sölupantanir. Einnig má láta innkaupaaðila gera það sama fyrir innkaupapantanir.

## Business Central á netinu og innanhúss

Hægt er að nota öryggishópa fyrir útgáfur á netinu og á staðnum [!INCLUDE [prod_short](includes/prod_short.md)]. Hópar eru búnir til með einni af eftirfarandi leiðum, allt eftir útgáfunni:

* Nota Microsoft Entra skal öryggishópa fyrir netútgáfuna. Nánari upplýsingar um stofnun hópsins fást með því að [fara í Stofna, breyta eða eyða öryggishópi í Microsoft 365 stjórnunarstöðinni](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* Öryggishópar eru aðeins studdir á staðnum ef virkjunin notar Windows-sannvottun. Til að stofna öryggishópa fyrir heimavistir skal nota Windows Active Directory hópa. Nánari upplýsingar eru notaðar til að [stofna hópreikning í Windows Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory). 

Síðan skal stofna samsvarandi öryggishóp í [!INCLUDE [prod_short](includes/prod_short.md)] og tengja hann síðan í hópinn sem stofnaður var. Til að fá nánari upplýsingar er farið í [Bæta við öryggishóp í Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Ef sett hefur verið upp sérstök tegund af notanda með leyfisgerð Windows Group í útgáfu af [!INCLUDE [prod_short](includes/prod_short.md)] öldunni innanhúss sem er fyrr en 2023 útgáfubylgju 1, þegar notandi er uppfærður [!INCLUDE [prod_short](includes/prod_short.md)] í öryggishóp. Nýi öryggishópurinn hefur sama heiti og heiti Windows-hópsins. Öryggishópurinn veitir betri yfirsýn yfir meðlimi flokksins og skilvirkar heimildir þeirra.

## Bæta við öryggishóp í Business Central

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **öryggishópa** og velja síðan viðeigandi tengja.
1. Velja skal **Nýtt** til að stofna hóp.
1. Stofna tengja í hópinn, eins og hér segir:

    * Velja [!INCLUDE [prod_short](includes/prod_short.md)] skal hópinn í reitnum **Microsoft Entra Nafn** öryggisflokks til að fá á netinu.
    * Velja [!INCLUDE [prod_short](includes/prod_short.md)] skal hópinn á staðnum í reitnum **Heiti** Windows-hóps.

> [!NOTE]
> Notendurnir birtast á **meðlimaspjaldinu** á upplýsingakassasvæðinu eða aðeins síðunni **Meðlimir öryggishóps** ef þeim er bætt við sem notendum í [!INCLUDE [prod_short](includes/prod_short.md)]. Til að fá nánari upplýsingar um hvernig notendum er bætt við er farið í Til að [bæta við notendum eða uppfæra notandaupplýsingar og leyfisúthlutun í Business Central](ui-how-users-permissions.md#adduser).  

### Úthluta heimildum til öryggisflokks

1. Á síðunni **Öryggishópar** skal velja hópinn og velja svo aðgerðina **Heimildir** .
1. Úthluta heimildum á eftirfarandi hátt:

    * Til að úthluta heimildarmengum fyrir sig skal í reitnum **heimildasamstæða**  reita velja heimildirnar sem á að úthluta.
    * Til að úthluta mörgum heimildarsamstæðum skal velja **Bæta við mörgum** aðgerðum og velja svo stæðurnar sem á að úthluta.
1. Ef heimildarsamstæðurnar eiga aðeins að eiga við um tiltekið fyrirtæki er dálkurinn Fyrirtæki **stilltur á** það fyrirtæki. Ef heimildasamstæða á að eiga við um öll fyrirtæki er dálkurinn **Fyrirtæki** hafður auður. [Fræðast meira](ui-define-granular-permissions.md#control-access-to-specific-companies).

## Fara yfir heimildirnar í öryggishópi

Á síðunni **Öryggishópar** sýnir **upplýsingakassasvæðið Heimildasafn** sem hópnum er úthlutað. Hver notandi sem skráður er á **Meðlimaspjaldinu** hefur þessar heimildir. Aðgerðin **heimildasamstæða eftir öryggishópi** veitir ítarlegra yfirlit. Einnig er hægt að skoða einstakar heimildir í hverjum öryggisflokki.

Heimildir eru einnig tiltækar á síðunni **Notendur** . Upplýsingakassasvæðið sýnir **heimildasafnin úr öryggishópnum** og **meðlimir meðlimir öryggishóps** fyrir valinn notanda.

## Öryggishópar og notendaflokkar

> [!NOTE]
> Notendaflokkar verða ekki lengur tiltækir í síðari útgáfu.

Öryggishópar eru mjög líkir þeim notendaflokkum sem eru tiltækir. Hins vegar eiga notendaflokkar aðeins við [!INCLUDE [prod_short](includes/prod_short.md)]. Öryggishópar byggjast á hópum í Microsoft Entra kenni eða Windows Active Directory eftir því hvort þú notar [!INCLUDE [prod_short](includes/prod_short.md)] netið eða á staðnum, hvort sem er á netinu eða á staðnum. Hópar gagnast stjórnendum vegna þess að þeir geta notað þá með öðrum Dynamics 365 forritum. Til dæmis, ef sölumenn nota [!INCLUDE [prod_short](includes/prod_short.md)] og SharePoint stjórnendur þurfa ekki að endurstýra hópnum og meðlimum þess.

### Valfrjálst: Umbreyta notendahópum í heimildasafn

Í 2023 gefa út bylgju 1 og síðar er hægt að umbreyta notendahópum í heimildasafn í leigjandanum. Heimildasamstæðurnar bjóða upp á sömu virkni og notendaflokkar. Hér eru nokkur dæmi:

* Hægt er að nota upplýsingakassann **Notendur** til að stjórna heimildum notenda.
* Hægt er að kafa niður á heiti heimildasamstæða til að bæta öðrum heimildarsamstæðum við safnið sem verið er að vinna í. Nánari upplýsingar eru notaðar með því að fara í Til að [bæta við öðrum heimildarsamstæðum](ui-define-granular-permissions.md#to-add-other-permission-sets).

Nota skal leiðsagnarforritið **um uppsetningu á flutningum notendaflokkur** til að umbreyta hópunum. Til að ræsa leiðbeiningarnar skal á síðunni Eiginleikastjórnun **finna** Eiginleikar: Breyta heimildum **notendaflokkur og velja** svo Alla notendur **í reitnum** Virkt fyrir **.**  Leiðsagnarforritið leiðsagnarforrit með aðstoð býður upp á eftirfarandi valkosti fyrir umbreytinguna.

|Valkostur  |Heimildasamstæða  |
|---------|---------|
|Úthluta notanda     | Úthluta heimildum í notendaflokkum beint til notendanna sem voru tengdir hópnum og fjarlægja notendaflokkur úthlutun þeirra.        |
|Breyta í heimildasamstæðu     | Stofna skal nýja heimild fyrir heimildirnar í hverri notendaflokkur. Nýju heimildasamstæða hefur verið úthlutað öllum meðlimum hvers notendaflokkur.          |

### Leyfisskilgreiningar eiga enn við

Hægt er að grunnstilla heimildir út frá [!INCLUDE [prod_short](includes/prod_short.md)] leyfi. Þessum heimildum er beint úthlutað til nýrra notenda. Þessar samskipanir eiga enn við, jafnvel þó að hafist sé handa við að nota öryggisflokka.

Til að nota öryggishópa eingöngu er mælt með því að leyfisskilgreiningarnar séu fjarlægðar. Til að fræðast meira um leyfisskilgreiningar er farið í [Stofna notendur samkvæmt leyfi.](ui-how-users-permissions.md)

Hægt er að fjarlægja leyfisskilgreiningar á **leyfisskilgreining**  síðunni. Velja skal leyfi og eyða svo öllum heimildarsamstæðum sem því eru úthlutaðar.

## Sjá einnig

[Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  
[Setja upp Business Central aðgang í teymum með Microsoft 365 leyfi](admin-access-with-m365-license-setup.md)  
[Fræðast um hópa og aðgangsheimildir í Microsoft Entra kenni](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Microsoft Entra öryggishópar](/windows-server/identity/ad-ds/manage/understand-security-groups)  
