--- 
title: " Mazumtirdzniecības izrakstu veikala konfigurācijas"
description: "Šajā procedūra ir aprakstītas mazumtirdzniecības veikala konfigurācijas, kas ietekmē mazumtirdzniecības pārskatu izveides un grāmatošanas procesu."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 45aa0caf6fcef4cc49952557a251dd78f816125e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/14/2017

---
# <a name="store-configurations-for-retail-statements"></a> Mazumtirdzniecības izrakstu veikala konfigurācijas

[!include[task guide banner](../includes/task-guide-banner.md)]

Šajā procedūra ir aprakstītas mazumtirdzniecības veikala konfigurācijas, kas ietekmē mazumtirdzniecības pārskatu izveides un grāmatošanas procesu. Finanšu dimensijas mazumtirdzniecības veikalos tiek ietvertas citā procedūrā. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.

1. Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Sadaļas Izraksts/slēgšana iestatījumi ietekmē veikala pārskata izveides, apstiprināšanas un grāmatošanas procesu.  Atveriet sadaļu Izraksts/slēgšana.  
    * Atlasiet metodi, ko vēlaties izmantot izraksta rindu grupēšanai.  
    * Atlasiet Jā, ja, veidojot pārskatus no pārskata izveides pakešuzdevuma, dienā jāizveido tikai viens pārskats.  
    * Laukā Norēķinu uzskaites aprēķins nosaka, vai norēķinu deklarācijas jāpievieno kopā, vai arī jāizmanto pēdējā deklarācija.  
    * Atlasiet virsgrāmatas kontu, kur jāgrāmato noapaļošanas starpības.  
    * Laukā Maksimālā noapaļošanas starpība var ievadīt maksimālo atļauto noapaļošanas starpību.  
    * Laukā Grāmatošana var ievadīt maksimālo kopējo grāmatošanas starpību, kas atļauta pārskatam.  
    * Laukā Maiņa var ievadīt maksimālo kopējo maiņas starpību, kas atļauta pārskatam.  
    * Laukā Transakcija var ievadīt maksimālo kopējo starpību pārskata rindā.  
    * Laukā Slēguma metode var definēt, vai transakcijām, kas jāiekļauj pārskatā, jābūt daļai no slēgtas maiņas, vai arī tās var būt jebkuras transakcijas definētajā datuma/laika diapazonā.  
    * Laukā Darba dienas beigas var ievadīt laiku, kad transakcijas, kas tiek veiktas pēc pusnakts, ir jāgrāmato ar iepriekšējās dienas datumu.  
    * Atlasiet Jā, ja transakcijas, kas tiek veiktas pēc pusnakts, ir jāgrāmato ar iepriekšējās dienas datumu.  
    * Atlasiet Jā, lai iegūtu pārskatus, kas izveidoti katrai definētajai pārskatu izveides metodei. Tas var noderēt, ja ir jāuzlabo grāmatošanas veiktspēja veikaliem ar lielu transakciju apjomu, jo tādējādi tiks izveidots ievērojami mazāk pārskatu, ko var apstrādāt paralēli.  
    * Laukā Noklusējuma debitors var atlasiet debitora kontu, ko lietot pārdošanas procesā debitoriem.  


