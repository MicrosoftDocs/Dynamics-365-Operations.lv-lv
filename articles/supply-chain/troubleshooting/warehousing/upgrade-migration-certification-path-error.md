---
title: Sertifikācijas ceļa kļūda, veicot jaunināšanu vai migrēšanu uz WMS
description: Ja, veicot jaunināšanu vai migrēšanu uz WMS, programmā tiek rādīta kļūda "Sertificēšanas ceļa uzticamības enkurs nav atrasts", šī lapa sniedz informāciju par to, kā novērst šo problēmu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476958"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Atjauninot un migrējot uz WMS, nav atrasts uzticamības enkurss sertifikācijas ceļam

## <a name="symptoms"></a>Simptomi

Veicot jaunināšanu un migrēšanu uz papildu noliktavas pārvaldību (WMS), programmā Warehouse Management var tikt parādīts šāds kļūdas ziņojums:

> java.security.cert.certPathValidatorException: Sertificēšanas ceļa drošības enkurs nav atrasts.

## <a name="cause"></a>Iemesls

Tas notiek, jo pašparakstītie sertifikāti nav uzticami Android 8+ lokālajā vidē.

## <a name="resolution"></a>Novēršana

Izmantojiet ārēju (publisku) sertificēšanas iestādi (CA). Šīs problēmas labojums ir pieejams programmas Warehouse Management 1.9.0.0 versijā. Papildinformāciju par šo problēmu un to, kā to labot, skatiet sadaļā [Uzticamības enkurss sertifikācijas ceļam nav atrasts, iestatot programmas savienojumu](certification-path-app-connection-error.md).
