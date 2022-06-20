---
title: Kreditoru apstiprināšana noteiktām sagādes kategorijām
description: Šajā rakstā skaidrots, kā apstiprināt kreditorus noteiktām sagādes kategorijām Dynamics 365 Supply Chain Management.
author: GalynaFedorova
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb6861c1cfbc7702fae74b4aa97fe618b50ac0bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903990"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Kreditoru apstiprināšana noteiktām sagādes kategorijām

[!include [banner](../../includes/banner.md)]

Šajā rakstā skaidrots, kā apstiprināt kreditorus noteiktām sagādes kategorijām Dynamics 365 Supply Chain Management. Kad pirkšanas pieprasījums ir izveidots, var būt prasība atlasīt apstiprinātu vai vēlamu kreditoru, atkarībā no tā, kā ir iestatītas pirkšanas politikas. Šajā procedūrā ir parādīts, kā norādīt, ka kreditors ir apstiprināts vai vēlams noteiktai sagādes kategorijai. Šo uzdevumu parasti veic sagādes speciālists. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.

1. Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Piegādātāji > Visi piegādātāji**.
2. Atlasiet kreditoru, kuru vēlaties iestatīt kā apstiprināto vai vēlamo kreditoru kādai kategorijai.
3. Darbību rūtī atlasiet **Vispārīgi**.
4. Atlasiet **Kategorijas**.
5. Atlasiet **Pievienot kategoriju**.
6. Laukā **Kategorija** atlasiet **BIROJA UN GALDA PIEDERUMI (BIROJA UN GALDA PIEDERUMI)**.
7. Laukā **Piegādātāja kategorijas statuss** atlasiet **Vēlamais**. Vienai kategorijai ir iespējams norādīt vairākus vēlamos kreditorus.  
8. Atlasiet **Saglabāt**.
9. Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Iepirkumu kategorijas**.
10. Kokā atlasiet **UZŅĒMUMA IEPIRKUMU KATEGORIJAS\BIROJA UN GALDA PIEDERUMI**.
11. Izvērsiet sadaļu **Piegādātāji**. Pārbaudiet, vai jūsu atlasītais kreditors ir redzams kā vēlamais kreditors kategorijai Biroja un kancelejas piederumi. Ja veicat šo procedūru kā uzdevuma vadītājs, jums var būt jāatlasa poga **Atbloķēt**, lai varētu ritināt uz leju uz piegādātāju sarakstu.  Šajā lapā ir iespējams pievienot vēlamos un apstiprinātos kreditorus.  
12. Kokā atlasiet **BIROJA UN GALDA PIEDERUMI** un atlasiet **Šķēres**.
13. Laukā **Mantot piegādātājus no galvenās kategorijas** atlasiet **Nē**.
14. Laukā **Mantot piegādātājus no galvenās kategorijas** atlasiet **Jā**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]