---
title: Atjaunināt bankas žurnāla salikto elementu
description: Lai saliktajam elementam BankJournalEntity pievienotu papildu lauku BankTransactionType, ir nepieciešams izpildīt tālāk aprakstītās darbības.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565929"
---
# <a name="update-the-bank-journal-composite-entity"></a>Atjaunināt bankas žurnāla salikto elementu

[!include [banner](../includes/banner.md)]

Lai saliktajam elementam BankJournalEntity pievienotu papildu lauku BankTransactionType, ir nepieciešams izpildīt tālāk aprakstītās darbības.

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




