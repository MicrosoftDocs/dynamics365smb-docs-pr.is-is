---
author: edupont04
ms.topic: include
ms.date: 02/15/2022
ms.author: edupont
ms.openlocfilehash: c947d843a17c46323febee83a01c80a574982bbd
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142498"
---
> [!NOTE]
> Eftirfarandi hlutar gera ráð fyrir að þú hafir stjórnandaaðgang að Exchange Online.

Áður en hægt er að setja upp póstinnskráningu þarf að undirbúa Office 365 [almenningsmöppur](/exchange/collaboration-exo/public-folders/public-folders). Hægt er að gera þetta í [Exchange stjórnendamiðstöðinni](/exchange/exchange-admin-center?preserve-view=true) eða nota [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true).

> [!TIP]
> Ef þú vilt nota [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true) getur þú leitað eftir innblæstri um hvernig á að setja upp forskrift í sýnisforskriftinni sem við birtum í [BCTech-geymslunni](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Fylgdu skrefunum hér fyrir neðan til að setja upp Exchange Online, með tenglum á hvar þú getur fengið frekari upplýsingar.

### <a name="create-an-admin-role-group"></a>Stofna stjórnandahlutverkhóp

Stofna stjórnandahlutverkshóp fyrir opnar möppur á grunni upplýsinganna í eftirfarandi töflu:

|Eiginleiki        |Gildi:                     |
|----------------|--------------------------|
|Name            |Stjórnun almenningsmappa |
|Valin hlutverk  |Opnar möppur            |
|Valdir notendur  |Tölvupóstur notandareiknings sem Business Central mun nota til að keyra verk tölvupóstsskráningar|

Nánari upplýsingar fást með því [að stjórna hlutverkaflokkum í Exchange Online](/exchange/permissions-exo/role-groups).

### <a name="create-a-new-public-folder-mailbox"></a>Stofna nýja almenna möppu í pósthólfi

Stofnið nýtt pósthólf með opna möppu á grundvelli upplýsinganna í eftirfarandi töflu:

|Eiginleiki        |Gildi:                     |
|----------------|--------------------------|
|Name            |Opið pósthólf            |

Nánari upplýsingar má finna [í Create almenningsmöppu](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### <a name="create-new-public-folders"></a>Stofna nýjar almenningsmöppur

1. Stofnið nýja opna möppu með heitinu **Tölvupóstsskráning** í rótinni þannig að slóðin á möppuna verði `\Email Logging\`
2. Búa til tvær undirmöppur þannig að útkoman sé eftirfarandi heilar slóðir í möppurnar:

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Frekari upplýsingar má fá [með því að stofna opinbera möppu](/exchange/collaboration-exo/public-folders/create-public-folder).

### <a name="set-public-folder-ownership"></a>Setja eignarhald á opna möppu

Stillið notanda tölvupóstsskráningar sem eiganda að báðum opnu möppunum, opnu möppunum *Biðröð* og *Geymsla*.

Frekari upplýsingar er að finna í [Úthluta heimildum fyrir opnu möppuna](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### <a name="mail-enable-the-queue-public-folder"></a>Virkja tölvupóst fyrir *biðröð* opinnar möppu

  Nánari upplýsingar er að finna [í Mail-gera í almenningsrafmöppu](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### <a name="mail-enable-sending-emails-to-the-queue-public-folder"></a>Þegar tölvupóstur er virkjaður er hægt að senda tölvupóst á *biðröð* opnu möppunnar

Þegar tölvupóstur er virkjaður er hægt að senda tölvupóst á *biðröð* opnu möppunnar með Outlook eða Exchange Management Shell

Frekari upplýsingar er að finna á [Heimila ónafngreindum notendum að senda tölvupóst í opna möppu þar sem búið er að virkja tölvupóst](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true)

### <a name="create-mail-flow-rules"></a>Stofna póstflæðisreglur

Búa til tvær reglur um póstflæði út frá upplýsingunum í eftirfarandi töflu

|Tilgangur  |Name |Nota þessa reglu ef ...             |Gera eftirfarandi ...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|Regla fyrir móttekinn tölvupóst |Skrá tölvupóst sem sendur er til þessa fyrirtækis|*Sendandi* er staðsettur *utan fyrirtækis* og *viðtakandinn* er staðsettur *innan fyrirtækis*|Sendu falið afrit til netfangsins sem tilgreint er fyrir *biðröð* opnu möppurnar|
|Regla fyrir sendan tölvupóst | Skrá tölvupóst sem sendur er frá þessu fyrirtæki |*Sendandi* er staðsettur *innan fyrirtækisins* og *viðtakandinn* er staðsettur *utan fyrirtækis*|Sendu falið afrit til netfangsins sem tilgreint er fyrir *biðröð* opnu möppurnar|

Frekari upplýsingar er að finna á [Reglum um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Aðgerðum reglu um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Ef gerðar eru breytingar á Exchange Management Shell verða breytingarnar sýnilegar í stjórnunarmiðstöð Exchange eftir nokkra töf. Einnig verða breytingar sem gerðar hafa verið í Exchange í boði í [!INCLUDE[prod_short](prod_short.md)] eftir seinkun. Seinkunin gæti verið margar klukkustundir.
