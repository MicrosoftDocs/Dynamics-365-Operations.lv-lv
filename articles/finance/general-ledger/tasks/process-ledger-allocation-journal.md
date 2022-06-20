---
title: Virsgrāmatas sadalījumu žurnāla apstrāde
description: Šajā rakstā ir izskaidrots, kā apstrādāt sadalījuma pieprasījumu Dynamics 365 Finansēs.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b86f8f5d090d624e812d9e7e6c0bc0212e5e9716
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902434"
---
# <a name="process-ledger-allocation-journal"></a>Virsgrāmatas sadalījumu žurnāla apstrāde

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā apstrādāt iedalīšanas pieprasījumu. Izmantojiet lapu Apstrādāt piešķiršanas pieprasījumu, lai izveidotu sadalījuma žurnālu, ko var pārskatīt un apstiprināt pirms grāmatošanas Virsgrāmatā vai grāmatot tieši Virsgrāmatā. Pirms varēsiet izveidot sadalījumu žurnālu, jābūt vismaz vienai aktīvai Virsgrāmatas sadalījuma kārtulai. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Navigācijas rūtī dodieties uz sadaļu **Virsgrāmatas > Sadalījuma > Apstrādājiet sadalījuma pieprasījumu**.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
