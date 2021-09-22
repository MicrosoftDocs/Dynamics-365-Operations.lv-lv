---
title: Pirkuma pasūtījuma apstiprināšanas laikā tiek rādīta kļūda "Objekta atsauce nav iestatīta"
description: Pirkuma pasūtījuma apstiprināšanas laikā tiek rādīta kļūda "Objekta atsauce nav iestatīta"
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477005"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>Pirkuma pasūtījuma apstiprināšanas laikā tiek rādīta kļūda "Objekta atsauce nav iestatīta"

## <a name="symptoms"></a>Simptomi

Apstiprinot pirkuma pasūtījumu saņemat šādu izņēmumu:

> Objekta atsauce nav iestatīta

## <a name="cause"></a>Iemesls

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

## <a name="resolution"></a>Novēršana

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
