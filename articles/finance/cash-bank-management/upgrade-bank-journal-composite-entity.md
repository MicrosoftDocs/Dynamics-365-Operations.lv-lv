---
title: Atjaunināt bankas žurnāla salikto elementu
description: Lai saliktajam elementam BankJournalEntity pievienotu papildu lauku BankTransactionType, ir nepieciešams izpildīt tālāk aprakstītās darbības.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec196600a54a2aed4565cf422dc386d6646ff524
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445454"
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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]