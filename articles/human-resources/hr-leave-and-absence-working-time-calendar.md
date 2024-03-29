---
title: Darba laika kalendāra izveide
description: Definējiet darba laika kalendāru, brīvdienas un ārpusdarba laikus pakalpojumā Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dac3ad583be9e4cbd6eacbc6d228819bd298628b
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323579"
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
   - Lai pievienotu laiku, kas nav darba laiks, piemēram, pusdienlaiks vai pārtraukumi, **·** **atlasiet** Pievienot sadaļā Ne darba laiks un ievadiet nosaukumu un laika diapazonu.

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
