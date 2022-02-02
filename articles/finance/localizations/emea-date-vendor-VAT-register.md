---
title: Kreditora PVN reģistra datums
description: Šajā tēmā ir sniegta informācija par līdzekli kreditoru PVN reģistra datuma iespējošanai
author: anasyash
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: global
ms.author: anasyash
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 882d5a8718d819cff80bfa5b86e054a39e9db159
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7991732"
---
# <a name="date-of-vendor-vat-register"></a>Kreditora PVN reģistra datums

Microsoft versijā Dynamics 365 Finance 10.0.24 kreditoru rēķiniem ir pieejams jauns **kreditora PVN reģistra** lauks. Šis lauks norāda ar nodokli apliekamās piegādes datumu pirkumam.

Lai iespējotu jaunu lauku, dodieties uz līdzekļu pārvaldības darbvietu, atrodiet un atlasiet kreditoru PVN reģistra iespējot datumu kreditora rēķinu līdzeklī un pēc tam **atlasiet** Aktivizēt **·** **tagad**.

Ienākošajiem rēķiniem no piegādātājiem var būt divi datumi: datums, kad kreditors izsniedza rēķinu un ar nodokli apliekamās piegādes datums (t.i., datums, kad kreditoram jāmaksā pievienotās vērtības nodoklis [PVN]). Dažos scenārijos šie divi datumi var atšķirties.

Jūs variet atskaitīt ienākošo PVN summu pirkšanas rēķinam un iekļaut šo rēķinu PVN pārskatos vēlāk, datumā, kas atšķiras no abiem iepriekš minētajiem datumiem. Šo datumu kontrolē lokālie likumdošana noteikumi par atliktiem ienākošajiem PVN ieturējumiem dažiem scenārijiem. Tā atšķiras atkarībā no valsts vai reģiona.

Dažiem PVN pārskatiem, piemēram, PVN kontroles pārskatam Čehijas Republikai, pirkšanas dokumentam ir jāsniedz pārskats par ar nodokli [apliekamās](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) piegādes datumu. Šis datums ir jāsniedz pārskatā, lai nodokļu iestādes varētu saskaņot PVN pārskatus starp partneriem.

Finansēs varat definēt datumus šādos laukos:

- **Rēķina** datums – datums, kad piegādātājs izsniedza rēķinu.
- **PVN reģistra datums** – PVN summas ieturējuma datums pirkšanas rēķinam.
- **Kreditora PVN reģistra** datums – kreditora ar nodokli apliekamās piegādes datums.
- **Saņemt dokumenta** datumu – datumu, kad saņēmāt rēķinu.

Šie lauki ir iekļauti šajās lapās:

- Kreditora rēķins
- Kreditoru rēķinu reģistrs
- Kreditora rēķina apstiprinājums
- Kreditoru rēķinu žurnāls

Pēc kreditora rēķina grāmatošanas varat pārskatīt datumus lapās **Rēķinu žurnāls un Kreditora** **darbības**.
