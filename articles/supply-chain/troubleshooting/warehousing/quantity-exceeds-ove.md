---
title: Nevar apstiprināt kravu, jo daudzums pārsniedz pasūtījuma pārsniegīšanas procentus
description: Nevar apstiprināt kravu, jo daudzums pārsniedz pasūtījuma pārsniegīšanas procentus
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b25050572662afebbeaa39fa5a96e70cef618ac671dceba189fab1315480ede2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755159"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>Nevar apstiprināt kravu, jo daudzums pārsniedz pasūtījuma pārsniegīšanas procentus

Kļūdas kods: WAX1687

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Kravas nosūtīšanu %1 nevarēja apstiprināt, jo krājuma %2 daudzums pārsniedz pasūtījumam noteikto procentuālo vērtību.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Kravas vai sūtījuma daudzums ir tikai daļēji izdots. Daudzums pašlaik pārsniedz izdoto daudzumu par procentiem, kas ir ārpus atļautajiem pārsniegšanas procentiem.

## <a name="resolution"></a>Novēršana

Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Iestatiet krāvas rindu daudzumu.
- Iestatiet pārsnieguma procentuālo vērtību.

### <a name="set-the-load-line-quantity"></a>Iestatiet krāvas rindu daudzumu

Lai uzstādītu kravas rindu daudzumu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz pasūtījuma pārsnieguma procentus.
1. Kopsavilkuma cilnē **Rindu detāļas** atlasiet **Pasūtījums**, lai pievienotu rindu.
1. Laukā **Daudzums** iestatiet vērtību uz izdoto daudzumu (t.i., uz **Darba izveidotā daudzuma** vērtību), lai varētu notikt nosūtīšanas apstiprinājums.

### <a name="set-the-overdelivery-percentage"></a>Iestatiet pārsnieguma procentuālo vērtību

Lai uzstādītu nepilnu pasūtījumu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz pasūtījuma pārsnieguma procentus.
1. Kopsavilkuma cilnē **Rindu detāļas** atlasiet **Vispārīgi**, lai pievienotu rindu.
1. Laukā **Pasūtījuma pārsniegšana** iestatiet lielāku procentuālo vērtību, kas atbilst izdotajam daudzumam attiecībā pret kravas daudzumu, lai varētu tikt veikta kravas apstiprināšana.
