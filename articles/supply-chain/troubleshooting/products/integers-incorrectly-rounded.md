---
title: Veseli skaitļi tiek nepareizi noapaļoti produkta konfigurācijas modeļu aprēķinos
description: Veselo skaitļu rezultāti netiek vienmēr pareizi noapaļoti, kad tiek aprēķināti produkta konfigurācijas modeļi. Novērsiet šo kļūdu, pievienojot decimāldaļas atribūtu un aprēķinus.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477003"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Veseli skaitļi tiek nepareizi noapaļoti, kad tiek aprēķināti produkta konfigurācijas modeļi

## <a name="symptoms"></a>Simptomi

Šī problēma var rasties, veicot šādas darbību sērijas:

1. Iestatiet šos atribūtus produkta konfigurācijas modelī:

    - Ievade (vesels skaitlis)
    - Procenti (decimāls)
    - Rezultāts (vesels skaitlis)

2. Izveidojiet aprēķinu, kam ir turpmāk aprakstītā izteiksme:

    *Rezultāts* = *Ievade* x *Procenti* ÷ 100

Šādā gadījumā veselā skaitļa rezultāts ne vienmēr tiek noapaļots. Piemēram, ja ievade ir 1000 un īpatsvars ir 2,40, ir sagaidāms, ka rezultāts veselā skaitlī būs 24, jo 2,40 procentos no 1000 ir 24 (vai 24,00, izsakot decimālformā). Tā vietā rezultāts tiek attēlots kā 23. Tomēr, ja procentuālais daudzums ir 2,39, aprēķins tiek noapaļots uz 24, nevis 23. Kad procentuālais daudzums ir 2,50, aprēķins tiek noapaļots uz 25, kā paredzēts.

## <a name="cause"></a>Iemesls

Šī problēma rodas tādēļ, ka Microsoft Solver Foundation iekšēji ataino skaitļus, izmantojot daļskaitļus. Iepriekšējā piemērā aprēķina rezultāts, kur procentuālā vērtība ir 2,40, tiek parādīts kā 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Kad .NET šo vērtību izmanto kā veselu skaitli, tas atgriezīs 23.

## <a name="resolution"></a>Novēršana

Šāda darbība nemainīsies, jo citi scenāriji ir atkarīgi no tās. Šajā piemērā varat problēmu novērst, ieviešot papildu decimāldaļu atribūtu un aprēķinus.

Piemēram, ražošanas konfigurācijas modelī iestatiet šādus atribūtus.

- Ievade (vesels skaitlis)
- Procenti (decimāls)
- ResultDecimal (decimāls)
- ResultInteger (vesels skaitlis)

Varat pievienot šādus aprēķinus:

- *ResultDecimal* = *Ievade* x *Procenti* ÷ 100
- *ResultInteger* = *ResultDecimal*
