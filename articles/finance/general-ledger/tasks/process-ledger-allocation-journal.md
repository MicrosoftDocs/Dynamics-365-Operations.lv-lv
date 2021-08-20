---
title: Virsgrāmatas sadalījumu žurnāla apstrāde
description: Šajā tēmā ir paskaidrots, kā apstrādāt sadalījuma pieprasījumu pakalpojumā Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d37b1a9869cc130786d0e8fde68184e04c881bad1f64c86943174213025db82
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765672"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]