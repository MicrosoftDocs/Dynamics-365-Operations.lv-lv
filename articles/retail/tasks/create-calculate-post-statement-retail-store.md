---
title: " Mazumtirdzniecības veikala izraksta izveide, aprēķins un grāmatošana"
description: Šajā procedūrā ir aprakstītas manuālās veikala izraksta izveides, aprēķināšanas un grāmatošanas darbības.
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
ms.openlocfilehash: 9ea30e7e008bfcce77a7ee2f4d7d01a6cf1ababc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "354395"
---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Mazumtirdzniecības veikala izraksta izveide, aprēķins un grāmatošana

[!include[task guide banner](../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstītas manuālās veikala izraksta izveides, aprēķināšanas un grāmatošanas darbības. Ir aprakstīti arī pakešuzdevumi, ko var konfigurēt vieniem tiem pašiem uzdevumiem. Pakešuzdevumu konfigurēšanas un izpildes darbības ir aprakstītas citās tēmās. Lai izpildītu šo procedūru, ir nepieciešamas transakcijas, kas ir pabeigtas POS un pēc tam importētas programmā Dynamics AX. Šajā ierakstā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati. Šī procedūra var attiekties uz programmu Microsoft Dynamics AX. Lūdzu, ņemiet vērā, ka programma Dynamics AX tagad tiek saukta par Microsoft Dynamics 365 for Operations.

1. Dodieties uz Visas darbvietas > .. > Mazumtirdzniecības veikala finanses.
2. Noklikšķiniet uz Jauns izraksts.
3. Laukā Veikala numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Noklikšķiniet uz OK.
    * Laukā Iestatījumu grupā ir pieejami iestatījumi, kas nosaka, kādas transakcijas ir ietvertas pārskatā un kā tās tiek grupētas izraksta rindās. Lauku Iestatīšanas grupa var atvērt un mainīt šos iestatījumus vai var izmantot noklusējuma iestatījumus.  
    * Lauku Izraksta metode tiek noteikts, kā tiks grupētas izraksta rindas.  
    * Atlasiet darbinieku vai reģistru, ja vēlaties aprēķināt izrakstu tikai noteiktam darbiniekam vai reģistram.  
6. Laukā Slēguma metode atlasiet opciju.
7. Noklikšķiniet uz Aprēķināt izrakstu.
8. Noklikšķiniet uz Jā.
    * Pēc izraksta aprēķināšanas jātiek izveidotām rindām ar kopsummu katrai izmantotajai maksāšanas un izraksta izveides metodei.  
    * Aprēķināto summu ievadiet katrā rindā, ja tā ir jāievada un atjaunina. Aprēķinātais lauks tiek aizpildīts ar norēķinu uzskaites summām, kas aprēķinātas, izmantojot POS.  
9. Noklikšķiniet uz Grāmatot izrakstu.
10. Noklikšķiniet uz Aizvērt.
11. Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikala finanses.
12. Noklikšķiniet uz cilnes Iegrāmatotie izraksti.

