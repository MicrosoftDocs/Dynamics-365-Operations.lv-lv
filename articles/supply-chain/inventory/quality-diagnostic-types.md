---
title: Neatbilstību diagnostikas tipi
description: Šajā tēmā ir aprakstīts, kā izmantot un izveidot diagnostikas tipus, kas var tikt izmantoti ar neatbilstībām.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 560627bf5ecd38f3fc79448629390acb549e40fb1388958d9eac094517925039
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781517"
---
# <a name="diagnostic-types-for-nonconformances"></a>Neatbilstību diagnostikas tipi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izmantot un izveidot diagnostikas tipus, kas var tikt izmantoti ar neatbilstībām.

Izmantojiet lapu **Diagnostikas tipi**, lai definētu diagnostikas darbību klasifikāciju. Pēc tam, veidojot neatbilstības labojumu, atlasiet diagnostiku. Labojumā norāda, kāda veida diagnostikas darbība jāveic attiecībā uz apstiprināto neatbilstību un kam tā ir jāveic. Tajā norāda arī pieprasīto un plānotais pabeigšanas datumu.

## <a name="examples-of-diagnostic-types"></a>Diagnostikas tipu paraugi

Jūs strādājat ražošanas uzņēmumā, un vairākiem krājumiem ir nesekmīgi kvalitātes testi. Šie krājumi tiek pārvietoti karantīnas zonā un iezīmēti kā neatbilstoši produkti. Neatbilstības ieraksts tiek izveidots programmā Microsoft Dynamics 365 Supply Chain Management, lai varētu izsekot detalizētu informāciju, izmantojot problēmas atrisināšanu.

Šajā gadījumā kvalitātes problēmas rodas tāpēc, ka iekārtas gultņi, kas sapako preces, ir bijuši slikti un pārkarsuši. Šīs problēmas labojums ir aizvietot iekārtas daļas.

Konfigurējot diagnostikas tipus, var izveidot daudzus ierakstus, no kuriem katrs parāda atšķirīgu problēmas tipu, kāds var būt iekārtai. Alternatīvi jūs varat izveidot vienu vispārēju diagnostikas tipu, kas pārstāv iekārtu remontu.

## <a name="create-a-diagnostic-type"></a>Izveidot diagnostikas tipu

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Diagnostikas tipi**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Diagnostika** - Ievadiet unikālu diagnostikas tipa ID vai nosaukumu.
    - **Apraksts** — ievadiet diagnostikas tipa detālizēto aprakstu.

1. Aizvērt lapu.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības pārskats](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Par neatbilstību apstiprināšanu atbildīgie darbinieki](quality-responsible-workers.md)
- [Karantīnas zonas neatbilstībai](quality-quarantine-zones.md)
- [Neatbilstību problēmu tipi](quality-problem-types.md)
- [Kvalitātes maksa par neatbilstībām](quality-charges.md)
- [Operācijas neatbilstībai](quality-operations.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
