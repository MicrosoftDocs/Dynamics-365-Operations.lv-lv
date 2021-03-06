---
title: Kreditoru apstiprināšana noteiktām sagādes kategorijām
description: Šajā tēmā paskaidrots, kā apstiprināt piegādātājus noteiktām iepirkumu kategorijām pakalpojumā Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 887905c35c684f2f60c3ce17eb652532831193cc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812450"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Kreditoru apstiprināšana noteiktām sagādes kategorijām

[!include [banner](../../includes/banner.md)]

Šajā tēmā paskaidrots, kā apstiprināt piegādātājus noteiktām iepirkumu kategorijām pakalpojumā Dynamics 365 Supply Chain Management. Kad pirkšanas pieprasījums ir izveidots, var būt prasība atlasīt apstiprinātu vai vēlamu kreditoru, atkarībā no tā, kā ir iestatītas pirkšanas politikas. Šajā procedūrā ir parādīts, kā norādīt, ka kreditors ir apstiprināts vai vēlams noteiktai sagādes kategorijai. Šo uzdevumu parasti veic sagādes speciālists. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.

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