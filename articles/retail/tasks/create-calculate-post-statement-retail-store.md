---
title: Mazumtirdzniecības veikala pārskatu izveidošana, aprēķināšana un grāmatošana
description: Šajā tēmā ir aprakstītas manuālās veikala izraksta izveides, aprēķināšanas un grāmatošanas darbības.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4517b9ddeb648b3d789773fc0dcb1ecd3c8be85c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024802"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Mazumtirdzniecības veikala pārskatu izveidošana, aprēķināšana un grāmatošana

[!include[task guide banner](../includes/task-guide-banner.md)]

Šajā tēmā ir aprakstītas manuālās veikala izraksta izveides, aprēķināšanas un grāmatošanas darbības. Ir aprakstīti arī pakešuzdevumi, ko var konfigurēt vieniem tiem pašiem uzdevumiem. Pakešuzdevumu konfigurēšanas un izpildes darbības ir aprakstītas citās tēmās. Lai izpildītu šo procedūru, ir nepieciešamas transakcijas, kas ir pabeigtas POS un pēc tam importētas programmā Dynamics 365 Retail. Šajā ierakstā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. Sākuma lapā atlasiet **Mazumtirdzniecības veikala finanses**.
2. Atlasiet **Jauns izraksts**.
3. Laukā **Veikala numurs** atlasiet opciju no nolaižamā saraksta.
4. Atlasiet **Labi**.
5. **Iestatīšanas** grupā ir pieejami iestatījumi, kas nosaka, kādas transakcijas ir ietvertas pārskatā un kā tās tiek grupētas izraksta rindās. **Iestatīšanas** grupu var atvērt un mainīt šos iestatījumus vai var izmantot noklusējuma iestatījumus.  
    - Laukā **Izraksta metode** tiek noteikts, kā tiks grupētas izraksta rindas.  
    - Atlasiet darbinieku vai reģistru laukā **darbinieki/reģistrs**, ja vēlaties aprēķināt izrakstu tikai noteiktam darbiniekam vai reģistram.  
6. Laukā **Slēgšanas metode** atlasiet opciju.
7. Darbību rūtī atlasiet **Aprēķināt izrakstu**.
8. Atlasiet **Jā**.
    - Pēc izraksta aprēķināšanas jātiek izveidotām rindām ar kopsummu katrai izmantotajai maksāšanas un izraksta izveides metodei.  
    - Aprēķināto summu ievadiet katrā rindā, ja tā ir jāievada un atjaunina. Aprēķinātais lauks tiek aizpildīts ar norēķinu uzskaites summām, kas aprēķinātas, izmantojot POS.  
9. Darbību rūtī atlasiet **Grāmatot izrakstu**.
10. Atlasiet **Aizvērt**.
11. Aizveriet rūti.
12. Sākuma lapā atlasiet **Mazumtirdzniecības veikala finanses**.
13. Atlasiet cilni **Iegrāmatotie izraksti**.

