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
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026701"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Klienta atlaižu uzkrāšana neizdodas, ja tiek izmantotas krājumu atlaižu grupas

KB numurs: 4611372

## <a name="symptoms"></a>Simptomi

Ja izmantojat klienta atlaižu līgumus (*summas* tipa) kopā ar krājumu atlaižu grupām, atlaides tiek aprēķinātas, bet uzkrāšana neizdodas.

## <a name="resolution"></a>Novēršana

Sistēma darbojas kā paredzēts. Krājumu grupas grupē tikai krājumus, kuriem ir tāds pats sliekšņa nosacījums. Atlaides nosacījums (slieksnis) tiek iestatīts pret summu katram krājumam, nevis attiecībā pret uzkrāto summu jebkuram krājumam krājumu grupā.
