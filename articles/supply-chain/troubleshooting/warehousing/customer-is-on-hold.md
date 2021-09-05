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
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344268"
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
