---
title: Piegādātāja rēķina grāmatošanas laikā tiek rādīts izņēmums
description: Piegādātā rēķina grāmatošanas laikā tiek rādīts izņēmums "Izsaukšanas mērķis ir radījis izņēmumus".
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
ms.openlocfilehash: ecc63cb7d0d2392105d8e4290f8e837945ae0781
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476980"
---
# <a name="an-exception-occurs-during-vendor-invoice-posting"></a>Piegādātāja rēķina grāmatošanas laikā tiek rādīts izņēmums


## <a name="symptoms"></a>Simptomi

Grāmatojot piegādātāja rēķinu, tiek saņemts šāds izņēmums:

> Izņēmumu ir radījis izsaukuma mērķis

## <a name="cause"></a>Iemesls

Šī problēma var rasties pirkšanas pasūtījuma sadaļu neatbilstības dēļ.

## <a name="resolution"></a>Novēršana

Lai atrisinātu šo problēmu un atiestatītu pirkšanas pasūtījumu uz stāvokli *Melnraksts*, dodieties uz **Sagāde un avoti \> Periodiskie uzdevumi \> Tīrīt \> Pirkšanas pasūtījuma sadales atiestatīšana**. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas pasūtījuma sadales kļūdas atrisināšana Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
