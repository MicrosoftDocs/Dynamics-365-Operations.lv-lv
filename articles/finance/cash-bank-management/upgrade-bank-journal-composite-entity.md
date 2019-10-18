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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 974d6b3b11df92debdec26860fd9eea00a9f2313
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188031"
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




