---
title: " Mazumtirdzniecības izrakstu veikala konfigurācijas"
description: Šajā procedūra ir aprakstītas Commerce veikala konfigurācijas, kas ietekmē Commerce pārskatu izveides un grāmatošanas procesu.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e255c58997ed1c0ad5614b15867f14714a8bcfc8
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/24/2020
ms.locfileid: "4414203"
---
# <a name="store-configurations-for-retail-statements"></a> Mazumtirdzniecības izrakstu veikala konfigurācijas

[!include [banner](../includes/banner.md)]

Šajā procedūra ir aprakstītas Commerce veikala konfigurācijas, kas ietekmē Commerce pārskatu izveides un grāmatošanas procesu. Finanšu dimensijas veikalos tiek ietvertas citā procedūrā. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. **Navigācijas rūtī** dodieties uz **Moduļi > Retail un Commerce > Kanāli > Veikali > Visi mazumtirdzniecības veikali**.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Noklikšķiniet uz **Rediģēt**.
5. Kopsavilkuma cilnes **Izraksts/slēgšana** iestatījumi ietekmē veikala pārskata izveides, apstiprināšanas un grāmatošanas procesu. Izvērsiet kopsavilkuma cilni **Izraksts/slēgšana**.  
6. Laukā **Izraksta metode** atlasiet metodi, kuru vēlaties izmantot pārskata rindu grupēšanai.  
7. Atlasiet “Jā” sadaļā **Viens izraksts dienā**, ja, veidojot pārskatus no pārskata izveides pakešuzdevuma, dienā jāizveido tikai viens pārskats.  
8. Lauks **Norēķinu uzskaites aprēķins** nosaka, vai norēķinu deklarācijas jāpievieno kopā, vai arī jāizmanto pēdējā deklarācija.  
9. Laukā **Noapaļošana** atlasiet virsgrāmatas kontu, kur jāgrāmato noapaļošanas starpības.  
10. Laukā **Maksimālā noapaļošanas starpība** var ievadīt maksimālo atļauto noapaļošanas starpību.
11. Laukā **Grāmatošana** var ievadīt maksimālo kopējo grāmatošanas starpību, kas atļauta pārskatam.
12. Laukā **Maiņa** var ievadīt maksimālo kopējo maiņas starpību, kas atļauta pārskatam.  
13. Laukā **Transakcija** var ievadīt maksimālo kopējo starpību pārskata rindā.  
14. Laukā **Slēguma metode** var definēt, vai transakcijām, kas jāiekļauj pārskatā, jābūt daļai no slēgtas maiņas, vai arī tās var būt jebkuras transakcijas definētajā datuma/laika diapazonā.  
15. Laukā **Darba dienas beigas** var ievadīt laiku, kad transakcijas, kas tiek veiktas pēc pusnakts, ir jāgrāmato ar iepriekšējās dienas datumu.  
16. Atlasiet “Jā” laukā **Grāmatot kā darba dienu**, ja transakcijas, kas tiek veiktas pēc pusnakts, ir jāgrāmato ar iepriekšējās dienas datumu.  
17. Atlasiet “Jā” laukā **Sadalīt pēc izraksta metodes**, lai iegūtu pārskatus, kas izveidoti katrai definētajai pārskatu izveides metodei. Šī darbība var noderēt, ja ir jāuzlabo grāmatošanas veiktspēja veikaliem ar lielu transakciju apjomu, jo tādējādi tiks izveidots ievērojami mazāk pārskatu, ko var apstrādāt paralēli.  
18. Kopsavilkuma cilnes **Vispārīgi** laukā **Noklusējuma debitors** var atlasiet debitora kontu, ko lietot pārdošanas procesā debitoriem.  

