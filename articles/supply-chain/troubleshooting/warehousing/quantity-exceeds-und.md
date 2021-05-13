---
title: Nevar apstiprināt kravu, jo daudzums pārsniedz nepilna pasūtījuma procentus
description: Nevar apstiprināt kravu, jo daudzums pārsniedz nepilna pasūtījuma procentus
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
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938509"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Nevar apstiprināt kravu, jo daudzums pārsniedz nepilna pasūtījuma procentus

Kļūdas kods: WAX1687

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Kravas nosūtīšanu %1 nevarēja apstiprināt, jo krājuma %2 daudzums pārsniedz nepilna pasūtījuma procentuālo vērtību.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Kravas vai sūtījuma daudzums ir tikai daļēji izdots. Daudzums pašlaik ir mazāks par izdoto daudzumu par procentiem, kas ir ārpus atļautajiem nepilna pasūtījuma procentiem.

## <a name="resolution"></a>Novēršana

Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.

- Iestatiet krāvas rindu daudzumu.
- Iestatiet nepilna pasūtījuma procentuālo vērtību.

### <a name="set-the-load-line-quantity"></a>Iestatiet krāvas rindu daudzumu

Lai uzstādītu kravas rindu daudzumu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz nepilnā pasūtījuma procentus.
1. Kopsavilkuma cilnē **Rindu detāļas** atlasiet **Pasūtījums**, lai pievienotu rindu.
1. Laukā **Daudzums** iestatiet vērtību uz izdoto daudzumu (t.i., uz **Darba izveidotā daudzuma** vērtību), lai varētu notikt nosūtīšanas apstiprinājums.

### <a name="set-the-underdelivery-percentage"></a>Iestatiet nepilna pasūtījuma procentuālo vērtību

Lai uzstādītu nepilnu pasūtījumu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz nepilnā pasūtījuma procentus.
1. Kopsavilkuma cilnē **Rindu detāļas** atlasiet **Vispārīgi**, lai pievienotu rindu.
1. Laukā **Nepilns pasūtījums** iestatiet lielāku procentuālo vērtību, kas atbilst izdotajam daudzumam attiecībā pret kravas daudzumu, lai varētu notikt kravas apstiprināšana.
