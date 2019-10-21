---
title: Detalizētas bankas darbību saskaņošanas MT940 importēšana – Salikta datu elementa jaunināšana
description: Secības numurs jāpievieno bankas izraksta importēšanas elementam, lai atbalstītu MT940 formātu.
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
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188468"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Detalizētas bankas darbību saskaņošanas MT940 importēšana – Salikta datu elementa jaunināšana

[!include [banner](../includes/banner.md)]

Secības numurs jāpievieno bankas izraksta importēšanas elementam, lai atbalstītu MT940 formātu. 

Lai pievienotu bankas izraksta importēšanas elementu MT940 formāta atbalstam, veiciet šādas darbības.

1.  Kompilējiet un sinhronizējiet:
    -   Salikts elements\\BankStatementImportEntity
    -   Elements\\BankStatementBalanceEntity
    -   Elements\\BankStatementDocumentEntity
    -   Elements\\BankStatementEntity
    -   Elements\\BankStatementLineEntity
    -   Tabulas\\BankStatementStaging

2.  Datu pārvaldība\\datu projekti.
    1.  Ielādēt MT940 projekta(-u) importēšanu
        1.  Mainīt XSLT.
            -   Noklikšķiniet uz **Skatīt karti**.
            -   Noklikšķiniet uz **Skatīt karti** uz bankas izraksta dokumenta.
            -   Noklikšķiniet uz **Transformācijas**
            -   Dzēst BankReconiliation-to-Composite.xslt failu.
            -   Pievienot jaunu faila BankReconiliation Composite.xsl versiju.

        2.  Atklāt **Sērijas numuru** izkārtojumā **Avota dati**.
            1.  Avota datu formāts = XML elements.
            2.  Elementa nosaukums = Bankas izraksti.
            3.  Augšupielādēt datu failu = SampleBankCompositeEntity.xml jauna versija.
            4.  Noklikšķiniet uz **Jā**, lai pārrakstītu esošo failu.
            5.  Noklikšķiniet uz **Jā**, lai ģenerētu jaunu kartējumu.
            6.  Apstipriniet, ka S**equenceNumber** ir kartēts.
                -   Noklikšķiniet uz **Skatīt karti** uz bankas izraksta elementa.
                -   Apstipriniet, ka **SequenceNumber** ir kartēts no Avota uz Sagatavošanu.

3.  Importēt jauno izrakstu.




