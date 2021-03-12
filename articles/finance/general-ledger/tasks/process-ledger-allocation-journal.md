---
title: Virsgrāmatas sadalījumu žurnāla apstrāde
description: Šajā tēmā ir paskaidrots, kā apstrādāt sadalījuma pieprasījumu pakalpojumā Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7e8c3ef6fa85daec2a191b433b1ec4ece441ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968483"
---
# <a name="process-ledger-allocation-journal"></a>Virsgrāmatas sadalījumu žurnāla apstrāde

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā apstrādāt sadalījuma pieprasījumu. Izmantojiet lapu Apstrādāt piešķiršanas pieprasījumu, lai izveidotu sadalījuma žurnālu, ko var pārskatīt un apstiprināt pirms grāmatošanas Virsgrāmatā vai grāmatot tieši Virsgrāmatā. Pirms varēsiet izveidot sadalījumu žurnālu, jābūt vismaz vienai aktīvai Virsgrāmatas sadalījuma kārtulai. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Sadalījums > Apstrādāt sadalījuma pieprasījumu**.
2. Laukā **Noteikums** nolaižamajā sarakstā atlasiet vēlamo ierakstu.
3. Laukā **No datuma** ievadiet datumu.

    - Lauks **No datuma** ir ļoti svarīgs, ja virsgrāmata ir noteikuma datu avots. Šis datums kontrolē, kuras Virsgrāmatas bilances iekļaut sadalījumā.  
    - Laukā **Nulles avots** atlasiet **Apturēt**. Tādējādi tiks apturēts sadalīšanas process un parādīsies ziņojums, kurā teikts, ka ir atlasīts nulles avota apjoms.  

4. Laukā **Priekšlikuma opcijas** atlasiet **Tikai priekšlikums**. Atlasiet **Tikai priekšlikums**, lai izskatītu un pēc izvēles apstiprinātu rezultātu sadalījuma žurnālos pirms grāmatot sadalījumu virsgrāmatā.  
5. Laukā Virsgrāmatas grāmatošanas datums ievadiet datumu.
6. Atlasiet **Labi**.
7. Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Sadalījums > Sadalījuma žurnāli**.
8. Atlasiet **Rindas**.
9. Atlasiet **Grāmatot**.
10. Atlasiet **Grāmatot**.

