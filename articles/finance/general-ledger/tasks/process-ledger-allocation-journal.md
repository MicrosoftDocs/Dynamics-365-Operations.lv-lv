---
title: Virsgrāmatas sadalījumu žurnāla apstrāde
description: Šajā rakstā ir paskaidrots, kā apstrādāt sadalījuma pieprasījumu Dynamics 365 Finance.
author: aprilolson
ms.date: 11/15/2022
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
ms.openlocfilehash: 1f22b5042e0e3726afcb1061852fdbd8de770c61
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779397"
---
# <a name="process-ledger-allocation-journal"></a>Virsgrāmatas sadalījumu žurnāla apstrāde

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā apstrādāt sadalījuma pieprasījumu. **Izmantojiet lapu Sadalījuma pieprasījuma** apstrāde, lai izveidotu sadalījuma žurnālu, kuru var pārskatīt un apstiprināt pirms grāmatošanas virsgrāmatā vai grāmatot tieši Virsgrāmatā. Pirms varēsiet izveidot sadalījumu žurnālu, jābūt vismaz vienai aktīvai Virsgrāmatas sadalījuma kārtulai. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Navigācijas rūtī dodieties uz sadaļu **Virsgrāmata > Sadalījumi > Procesa sadalījuma pieprasījums**.
2. Laukā **Noteikums** nolaižamajā sarakstā atlasiet vēlamo ierakstu.
3. Laukā **No datuma** ievadiet datumu.

    - Lauks **No datuma** ir ļoti svarīgs, ja virsgrāmata ir noteikuma datu avots. Šis datums kontrolē, kuras Virsgrāmatas bilances iekļaut sadalījumā.  
    - Laukā **Nulles avots** atlasiet **Apturēt**. Tādējādi tiks apturēts sadalīšanas process un parādīsies ziņojums, kurā teikts, ka ir atlasīts nulles avota apjoms.  

4. Laukā **Priekšlikuma opcijas** atlasiet **Tikai priekšlikums**. Atlasiet **Tikai** priekšlikums, lai pirms sadalījuma grāmatošanas virsgrāmatā pārskatītu un pēc izvēles apstiprinātu rezultātu **sadalījuma žurnālos**.  
5. **Laukā GL grāmatošanas datums** ievadiet datumu.
6. Atlasiet **Labi**.
7. Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Sadalījums > Sadalījuma žurnāli**.
8. Atlasiet **Rindas**.
9. Atlasiet **Grāmatot**.
10. Atlasiet **Grāmatot**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
