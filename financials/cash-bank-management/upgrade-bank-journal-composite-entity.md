---
title: "Atjaunināt bankas žurnāla salikto elementu"
description: "Lai saliktajam elementam BankJournalEntity pievienotu papildu lauku BankTransactionType, ir nepieciešams izpildīt tālāk aprakstītās darbības."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 364bdff8f8d825cc50760631bb533b531f8b2121
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>Atjaunināt bankas žurnāla salikto elementu

[!include[banner](../includes/banner.md)]


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





