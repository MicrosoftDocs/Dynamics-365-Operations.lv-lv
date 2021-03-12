---
title: Preču konfiguratora problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar preču konfiguratoru.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999610"
---
# <a name="troubleshoot-the-product-configurator"></a>Preču konfiguratora problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar preču konfiguratoru.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Krājuma teksts tiek pārrakstīts, konfigurējot preci pārdošanas pasūtījuma rindā.

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma rodas, veidojot pārdošanas pasūtījuma rindu konfigurējamam krājumam un pēc tam modificējot krājuma tekstu. Konfigurējot krājumu un pēc tam atlasot **Labi**, teksts tiek pārrakstīts ar standarta tekstu.

### <a name="issue-resolution"></a>Problēmas risinājums

Šāda darbība ir paredzama. Teksta lauks ietver varianta nosaukumu, kas tiek aizpildīts tikai pēc rindas konfigurēšanas. Tāpēc teksts ir jāmaina pēc rindas konfigurācijas, nevis pirms tam.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Ja tiek aprēķināti preču konfigurācijas modeļi, tiek nepareizi noapaļoti veseli skaitļi.

### <a name="issue-description"></a>Problēmas apraksts

Šī problēma var rasties, veicot šādas darbību sērijas:

1. Iestatiet šādus atribūtus ražošanas konfigurācijas modelim:

    - Ievade (vesels skaitlis)
    - Procenti (decimāls)
    - Rezultāts (vesels skaitlis)

2. Izveidojiet aprēķinu, kam ir turpmāk aprakstītā izteiksme:

    *Rezultāts* = *Ievade* x *Procenti* ÷ 100

Šādā gadījumā veselā skaitļa rezultāts ne vienmēr tiek noapaļots. Piemēram, ievade ir 1000, un procentuālā vērtība ir 2,40. Tāpēc paredzams, ka veselā skaitļa rezultāts ir 24, jo 2,40 procenti no 1000 ir 24 (vai 24,00 decimālā formā). Tā vietā rezultāts tiek attēlots kā 23. Tomēr, ja procentuālais daudzums ir 2,39, aprēķins tiek noapaļots uz 24, nevis 23. Kad procentuālais daudzums ir 2,50, aprēķins tiek noapaļots uz 25, kā paredzēts.

### <a name="issue-resolution"></a>Problēmas risinājums

Šī problēma rodas tādēļ, ka Microsoft Solver Foundation iekšēji ataino skaitļus, izmantojot daļskaitļus. Iepriekšējā piemērā aprēķina rezultāts, kur procentuālā vērtība ir 2,40, tiek parādīts kā 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375. Kad .NET šo vērtību izmanto kā veselu skaitli, tas atgriezīs 23.

Šo darbību nevar mainīt, jo no tās ir atkarīgi citi scenāriji. Iepriekšējā piemērā varat novērst problēmu, ieviešot papildu decimālu atribūtu un aprēķinu.

Piemēram, varat iestatīt šādus atribūtus ražošanas konfigurācijas modelim:

- Ievade (vesels skaitlis)
- Procenti (decimāls)
- ResultDecimal (decimāls)
- ResultInteger (vesels skaitlis)

Varat pievienot šādus aprēķinus:

- *ResultDecimal* = *Ievade* x *Procenti* ÷ 100
- *ResultInteger* = *ResultDecimal*
