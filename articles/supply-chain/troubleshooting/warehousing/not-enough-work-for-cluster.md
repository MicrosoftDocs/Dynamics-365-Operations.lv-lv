---
title: Klasterim nav atrasts pietiekami daudz darba pēc profila konfigurēšanas
description: Pēc klastera profila konfigurēšanas, iespējams, saņemsit kļūdas ziņojumu, kurā teikts, ka nav iespējams atrast pietiekami daudz darba. Rediģējiet profilu un iestatiet pozīciju aktivizēšanu uz vērtību "Nē".
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476950"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Klasterim nav atrasts pietiekami daudz darba, lietojot sistēmā virzītu klasteru izdošanu

## <a name="symptoms"></a>Simptomi

Lietojot *Sistēmā virzītu klasteru izdošanas* procesu, ja konfigurējat klastera profilu, kurā var izdot, piemēram, 10 pozīcijas, process darbojas kā paredzēts, ja pietiek darba, lai izdotu 10 pozīcijas. Taču, ja var izdot tikai 8 pozīcijas, saņemsit šādu kļūdas ziņojumu:

> Klasterim nav atrasts pietiekami daudz darba.

## <a name="resolution"></a>Novēršana

Lai novērstu problēmu, rediģējiet klastera profilu un iestatiet opciju **Aktivizēt pozīcijas** uz vērtību *Nē*.
