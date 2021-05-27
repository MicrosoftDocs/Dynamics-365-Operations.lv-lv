---
title: Pabeigtā pārskata atsaukšana izveido neparedzētu atvērtu darbību
description: Pabeigtā pārskata atsaukšana, kurai ir iezīmēšana, izveido atvērtu darbību, kurā anulētajam daudzumam ir tādas pašas krājumu dimensijas kā anulētajai darbībai.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026723"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Pabeigtā pārskata atsaukšana izveido neparedzētu atvērtu darbību

KB numurs: 4612469

## <a name="symptoms"></a>Simptomi

Ja atsaucat pabeigto pārskatu, kuram ir iezīmēšana, sistēma izveido atvērtu darbību, kurā anulētajam daudzumam ir tādas pašas krājumu dimensijas kā anulētajai darbībai.

## <a name="resolution"></a>Novēršana

Atsaucot pabeigto operāciju, krājumu dimensija tiek inicializēta no ražošanas žurnāla. Tāpēc tā iegūst partijas numuru. Iezīmēšanas dēļ pārdošanas pasūtījuma darījumi pārmantos partijas numuru.

Dimensiju var atiestatīt, kad tiek grāmatota pabeigšana.
