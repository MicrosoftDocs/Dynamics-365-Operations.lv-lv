---
title: Traucējummeklēšanu veikala Commerce iestatīšanas un instalēšanas problēmas
description: Šajā rakstā ir izskaidrots, kā novērst iestatīšanas un instalēšanas problēmas Microsoft Dynamics 365 Commerce store Commerce programmā.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8af2c476ced05fc159a53131f8b51ad914a6c7c3
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168952"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Traucējummeklēšanu veikala Commerce iestatīšanas un instalēšanas problēmas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā novērst iestatīšanas un instalēšanas problēmas Microsoft Dynamics 365 Commerce store Commerce programmā.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Nevar aktivizēt programmu, un tiek saņemts savienojamības kļūdas ziņojums

Kad ievadāt derīgu Mākoņa pārdošanas punkta (CPOS) URL, varat saņemt savienojamības kļūdas ziņojumu, kas līdzīgs šim piemēram:

> Radās savienojamības kļūda, un ierīci nevar pievienot CPOS. Ierakstītajiem CPOS URL var būt dažas problēmas.

Šajā gadījumā pārskatiet url e-pastogrāfiskajām kļūdām vai nosakiet, vai CPOS nevar tikt sasniegts, jo tas ir bezsaistē.

Turklāt pārbaudiet, vai mākoņa mēroga vienības (CSU) versija ir 10.0.25 (9.35.\*.\*) vai jaunāka versija. Lai izmantotu store Commerce programmu, ir nepieciešama CPOS versija 10.0.25 vai jaunāka.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Programmu nevar instalēt, jo modern POS jau ir instalēts

Instalēšanas laikā var tikt parādīts kļūdas ziņojums, piemēram, šajā piemērā:

> Šī produkta (Modern POS) versija (9.\*.\*.\*) ir iepriekš instalēta, izmantojot mantojuma instalētāju.

Lai izlabotu kļūdu, jums jāatinstalē programma Modern Point of Sale (MPOS) visiem datorā ājiem un pēc tam jāmēģina vēlreiz. Varat apstiprināt, vai MPOS ir noņemts visiem lietotājiem, palaižot norādīto PowerShell komandu.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Nevar aktivizēt programmu nederīga vietrāža URL vai kļūdas stāvokļa dēļ

Ja ievadītais CPOS URL nav derīgs un jūs to vēlaties mainīt, vai, ja aktivizēšanas laikā Store Commerce programmas stāvoklis ir kļūda, varat restartēt procesu, atiestatījot programmu. Store Commerce programma saglabās tikai derīgu CPOS URL.

Lai atiestatītu programmu Store Commerce, veiciet šīs darbības.

1. Windows izvēlnē Sākt **atlasiet** un turiet (vai noklikšķiniet ar peles labo pogu) programmā un pēc tam atlasiet Iestatījumi **Papildu \> programma**.
2. Ritināt programmas iestatījumu lapu uz leju, līdz tiek meklēta **poga** Atiestatīt.
3. Atlasiet **Atiestatīt**. Pēc tam, kad tiek piedāvāts, apstipriniet, ka vēlaties atiestatīt programmu.
