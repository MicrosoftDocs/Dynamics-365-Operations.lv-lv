---
title: Darba laika kalendāra izveide
description: Definējiet darba laika kalendāru, brīvdienas un ārpusdarba laikus pakalpojumā Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ea55ad7f86e0c7d5ccc6e6de0af475299b05639
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052437"
---
# <a name="create-a-working-time-calendar"></a>Darba laika kalendāra izveide

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Darba laika kalendārs programmā Dynamics 365 Human Resources rāda dienas un stundas, kuras darbinieki strādā jūsu organizācijā. Kad darbinieks iesniedz brīvā laika pieprasījumu, viņiem nav jāraizējas par brīvdienām un slēgšanu.

Lai racionalizētu brīvā laika pieprasījumus, konfigurējiet šos elementus savai organizācijai:

- Darba laika kalendārs
- Brīvdienas un slēgšana
- Nestrādājamais laiks

Varat pievienot pēdējos divus elementus, kad iestatāt darba laika kalendāru. Varat arī tos konfigurēt vai atjaunināt atsevišķi.

## <a name="set-up-a-working-time-calendar"></a>Darba laika kalendāra iestatīšana

Iestatiet vismaz vienu darba laika kalendāru, kas rāda darbības dienas un stundas. Ja jums ir atrašanās vietas vairākās valstīs un reģionos, iespējams, vēlēsities iestatīt darba laika kalendāru katram apgabalam.

1. Lapā **Organizācijas administrēšana** atlasiet **Kalendāri**.

2. Atlasiet **Jauns** un ievadiet sava kalendāra nosaukumu un aprakstu.

3. Sadaļā **Ģenerēšanas opcijas** atlasiet savas organizācijas darba dienas un ievadiet darba laikus. 
   - Lai pievienotu atvaļinājumu vai slēgšanu, atlasiet pogu **Pievienot** blakus **Brīvdienas un slēgšana**.
   - Lai pievienotu nestrādājamo laiku, piemēram, pusdienas vai pārtraukumus, atlasiet **Pievienot** sadaļā **Nestrādājamais laiks** un ievadiet nosaukumu un laika diapazonu.

4. Sadaļā **Dienas** atlasiet **Ģenerēt**, lai ģenerētu dienas kalendārā. Ievadiet datumu diapazonu savam kalendāram un atlasiet **Ģenerēt dienas**.

5. Lai pievienotu darba grafikus, sadaļā **Darba grafiks** atlasiet **Pievienot** un pēc tam ievadiet laiku katram darba grafikam.

## <a name="configure-holidays-and-closures"></a>Brīvdienu un slēgšanas konfigurēšana

Brīvdienas un slēgšanu var pievienot vai mainīt atsevišķi no darba laika kalendāra.

1. Lapā **Organizācijas administrēšana** atlasiet **Brīvdienas un slēgšana**.

2. Atlasiet **Jauns** un ievadiet brīvdienas vai slēgšanas nosaukumu un datumu.

## <a name="configure-non-work-time"></a>Nestrādājamā laika konfigurēšana

Nestrādājamo laiku var pievienot vai mainīt atsevišķi no darba laika kalendāra.

1. Lapā **Organizācijas administrēšana** atlasiet **Nestrādājamais laiks**.

2. Atlasiet **Jauns** un ievadiet nestrādājamā laika nosaukumu un laika diapazonu.

Ja esat iespējojis atvaļinājumu un prombūtnes bankas brīvdienu labošanas priekšskatījuma līdzekli, Human Resources izmanto brīvdienas un slēgšanas datumus, lai noteiktu dienu skaitu, kas jāpielāgo darbiniekiem, kas reģistrēti kalendārā.

## <a name="see-also"></a>Skatiet arī

- [Atvaļinājumu un kavējumu apskats](hr-leave-and-absence-overview.md)
- [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]