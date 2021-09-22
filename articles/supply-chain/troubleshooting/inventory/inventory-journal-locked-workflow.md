---
title: Jūsu krājuma žurnāls ir bloķēts un darbplūsmas pakešuzdevums nedarbojas
description: Viens no jūsu krājuma žurnāliem ir slēgts ar kādu darbību un netiek atvērts
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476957"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Jūsu krājuma žurnāls ir bloķēts un darbplūsmas pakešuzdevums nedarbojas

## <a name="symptoms"></a>Simptomi

Kādu no jūsu krājumu žurnāliem ir bloķējusi kāda operācija un tā nav nodota izpildei. Piemēram, ja grāmatošanas laikā rodas nezināma kļūda (kas ir sistēmas bloķēšanas operācija), žurnālam var būt sistēmas bloķēts statuss. Šajā gadījumā darbplūsmas darba vienuma apdarinātājam rodas kļūda, bloķējot validāciju.

## <a name="resolution"></a>Novēršana

Piesakieties SQL Server instancē Supply Chain Management un pārbaudiet, vai **InventJournalTable.SystemBlocked** ir iestatīts uz *1*. Pārliecinieties, vai žurnāla statuss nav bloķēts, un pēc tam atiestatiet **InventJournalTable.SystemBlocked** uz *0*.
