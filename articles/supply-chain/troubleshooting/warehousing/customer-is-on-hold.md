---
title: Nevar apstiprināt sūtījumu, jo klients ir aizturēts
description: Nevar apstiprināt sūtījumu, jo klients ir aizturēts.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012189"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Nevar apstiprināt sūtījumu, jo klients ir aizturēts

Kļūdas kods: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Sūtījumu %1 nevar apstiprināt, jo debitors ir aizturēts uz %2.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Kravas vai sūtījuma debitora konts ir aizturēts. Tāpēc klienta statuss neļauj saņemt kravas apstiprinājumu.

## <a name="resolution"></a>Novēršana

Lai atbloķētu debitora kontu, izmantojiet šādu procedūru.

1. Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.
1. Atveriet debitora kontu, kam nevar apstiprināt sūtījumu.
1. Kopsavilkuma cilnē **Kredīts un iekasēšana** iestatiet lauku **Rēķinu izrakstīšana un piegāde ir aizturēta** uz *Nē*.
1. Atkārtojiet šo procedūru visiem bloķētajiem kravas klientiem.
