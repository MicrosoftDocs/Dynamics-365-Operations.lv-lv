---
title: Klienta atlaižu uzkrāšana neizdodas, ja tiek izmantotas krājumu atlaižu grupas
description: Ja izmantojat klienta atlaižu līgumus kopā ar krājumu atlaižu grupām, atlaides tiek aprēķinātas, bet uzkrāšana neizdodas.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760374"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Klienta atlaižu uzkrāšana neizdodas, ja tiek izmantotas krājumu atlaižu grupas

KB numurs: 4611372

## <a name="symptoms"></a>Simptomi

Ja izmantojat klienta atlaižu līgumus (*summas* tipa) kopā ar krājumu atlaižu grupām, atlaides tiek aprēķinātas, bet uzkrāšana neizdodas.

## <a name="resolution"></a>Novēršana

Sistēma darbojas kā paredzēts. Krājumu grupas grupē tikai krājumus, kuriem ir tāds pats sliekšņa nosacījums. Atlaides nosacījums (slieksnis) tiek iestatīts pret summu katram krājumam, nevis attiecībā pret uzkrāto summu jebkuram krājumam krājumu grupā.
