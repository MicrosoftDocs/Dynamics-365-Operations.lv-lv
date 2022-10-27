---
title: Bankas žurnāla salikto elementu atjaunināšana
description: Šajā rakstā ir uzskaitīti soļi, kas ir nepieciešami papildu Lauka BankTransactionType pievienošanai kompozītam BankJournalEntity.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1855f9680ba6bcf8eb46608882a128b4a21f0dac
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715295"
---
# <a name="update-the-bank-journal-composite-entity"></a>Bankas žurnāla salikto elementu atjaunināšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir uzskaitīti soļi, kas ir nepieciešami papildu Lauka BankTransactionType pievienošanai kompozītam BankJournalEntity.

Lai saliktajam elementam BankJournalEntity pievienotu papildu lauku BankTransactionType, izpildiet tālāk aprakstītās darbības.

1.  Kompilējiet un sinhronizējiet tālāk uzskaitītos bankas žurnālu saliktos elementus, elementus un sagatavošanas tabulas.
    -   Saliktais elements\\BankJournalEntity
    -   Elements\\BankJournalHeaderEntity
    -   Elements\\BankJournalLineEntity
    -   Tabula\\BankJournalHeaderStaging
    -   Tabula\\BankJournalLineStaging

2.  Datu pārvaldība\\datu projekti
    -   Atklājiet tipu **Bankas transakcija** izkārtojumā **Avota dati**.
        -   Avota datu formāts = XML elements
        -   Elementa nosaukums = Bankas žurnāls
        -   Augšupielādes datu fails = jaunas versijas SampleBankJournalCompositeEntity.xml
        -   Noklikšķiniet uz **Jā**, lai pārrakstītu esošo failu.
        -   Noklikšķiniet uz **Jā**, lai ģenerētu kartējumu no sākuma.
        -   Pārbaudiet, vai ir kartēts Bankas transakcijas tips.
            -   Noklikšķiniet uz **Skatīt karti** elementā Rinda.
            -   Pārbaudiet, vai Bankas transakcijas tips ir kartēts no avota uz sagatavošanu.

3.  Importēt jauno izrakstu.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
