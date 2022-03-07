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
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714214"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Pabeigtā pārskata atsaukšana izveido neparedzētu atvērtu darbību

KB numurs: 4612469

## <a name="symptoms"></a>Simptomi

Ja atsaucat pabeigto pārskatu, kuram ir iezīmēšana, sistēma izveido atvērtu darbību, kurā anulētajam daudzumam ir tādas pašas krājumu dimensijas kā anulētajai darbībai.

## <a name="resolution"></a>Novēršana

Atsaucot pabeigto operāciju, krājumu dimensija tiek inicializēta no ražošanas žurnāla. Tāpēc tā iegūst partijas numuru. Iezīmēšanas dēļ pārdošanas pasūtījuma darījumi pārmantos partijas numuru.

Dimensiju var atiestatīt, kad tiek grāmatota pabeigšana.
