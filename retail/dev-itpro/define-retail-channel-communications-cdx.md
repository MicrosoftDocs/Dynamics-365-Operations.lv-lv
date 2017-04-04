---
title: "Mazumtirdzniecības kanālu sakaru definēšana (Commerce Data Exchange)"
description: "Šajā rakstā ir sniegts pārskats par Commerce Data Exchange un tā komponentiem. Tas skaidro daļu, kas katram komponentam spēlē pārsūtīt datus starp Microsoft Dynamics 365 operācijām un mazumtirdzniecības kanāliem."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Mazumtirdzniecības kanālu sakaru definēšana (Commerce Data Exchange)

Šajā rakstā ir sniegts pārskats par Commerce Data Exchange un tā komponentiem. Tas skaidro daļu, kas katram komponentam spēlē pārsūtīt datus starp Microsoft Dynamics 365 operācijām un mazumtirdzniecības kanāliem.

<a name="overview"></a>Pārskats
--------

Tirdzniecības datu apmaiņa ir sistēma, kas nodod datus starp Dynamics 365 operācijām un mazumtirdzniecības kanālus, piemēram, tiešsaistes veikali vai ķieģeļu un javas veikali. Datu bāzi, kurā glabājas dati par mazumtirdzniecības kanāls ir atdalīts no Dynamics 365 operācijas datu bāzei. Kanāla datu bāze ietver tikai tos datus, kas ir nepieciešami mazumtirdzniecības transakcijām. Galvenie dati ir konfigurēta Dynamics 365 operācijām un sadalīti kanāliem. Transakciju datus tiek veidota sale (POS) sistēmas būtību vai tiešsaistes uzglabāt, un tad augšupielādēt Dynamics 365 operācijām. Datu izplatīšana ir asinhrona. Citiem vārdiem sakot — datu apkopošanas un iepakošanas process avotā notiek atsevišķi no saņemšanas un lietošana procesa datu galamērķī. Noteiktiem scenārijiem, piemēram, cenu un krājumu uzmeklēšanai, dati ir jāizgūst reālajā laikā. Atbalstīt šos scenārijus, tirdzniecības datu apmaiņa ietver arī pakalpojumu, kas ļauj reālā laika komunikācija starp Dynamics 365 operācijām un kanālu. 

[![atjaunināti mazumtirdzniecības grafika](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Asinhronais serviss
Microsoft SQL servera izmaiņu reģistrēšana par dinamiku 365 operāciju bāzes tiek izmantota, lai noteiktu datu izmaiņas, kas jānosūta kanālus. Pamatojoties uz sadalījuma grafiks, Dynamics 365 operācijām paketes datus un saglabā to centrālā krātuve (debeszils lāse uzglabāšana). Atsevišķas pakešveida apstrādes izmanto Commerce Data Exchange: Async klienta bibliotēku, lai šo datu pakotni ievietotu kanāla datu bāzē. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Mazumtirdzniecības plānotājs

Plānotāja darbi ir mehānisms, ar ko tiek veikta datu izplatīšana uz novietojumiem un no tiem. Darbi sastāv no apakšdarbiem, kuri norāda tabulas un tabulu laukus, kas satur izplatāmos datus. Dinamika 365 operācijām ietver iepriekš definētu plānotāju darba un subjobs, lielākā daļa organizāciju prasībām replikāciju. Tiek izveidoti tālāk norādītie iepriekš definēto darbu tipi.

-   **Lejupielādējiet darbi** -Download darbus sūtīt datus, kas ir mainījies no Dynamics 365 operācijām kanāla datu bāzēm. Ierakstiem veiktas modifikācijas tiek izsekotas ar SQL Server izmaiņu reģistrēšanu.
-   **Augšupielādēt darbi (P darbi)** -Upload darbus pavelciet pārdošanas darījumus no kanāla programmā Dynamics 365 operācijas datu bāzei. P darbi datus augšupielādē pakāpeniski. Kad tiek palaists P darbs, Async klienta bibliotēka pārbauda replicēšanas skaitītāju ierakstiem, kas jau ir saņemti no novietojuma. Ieraksts tiek augšupielādēts tikai tad, ja tā replicēšanas skaitītājs ir lielāks par lielāko atrasto vērtību. P darbi neatjaunina datus, kas tika augšupielādēti iepriekš.

Sadalījuma grafiks tiek izmantota, lai palaistu datu pārsūtīšanai vai nu manuāli, vai plānošanas pakešuzdevums programmā Dynamics 365 operācijām. Sadales grafiks var ietvert vienu vai vairākas kanālu datu grupas, kā arī vienu vai vairākus plānotāja darbus.

## <a name="realtime-service"></a>Reāllaika pakalpojumu
Tirdzniecības datu apmaiņa: Reālā laika apkalpošana ir integrēts pakalpojums, kas nodrošina reālā laika komunikācija starp Dynamics 365 operācijām un mazumtirdzniecības kanāliem. Reālā laika pakalpojums ļauj atsevišķu POS datorus un interneta veikalos, lai noteiktu datu izgūšana no Dynamics 365 darbību reālajā laikā. Kaut arī lielākā daļa galveno operāciju var veikt vietējo kanālu datu bāzi, šādos gadījumos nepieciešama tieša piekļuve datiem, kas glabājas programmā Dynamics 365 operācijām:

-   Dāvanu karšu izsniegšana un izpirkšana.
-   Lojalitātes programmas punktu izpirkšana.
-   Kredītrēķinu izsniegšana un izpirkšana.
-   Debitoru ierakstu izveidošana un atjaunināšana.
-   Pārdošanas pasūtījumu izveidošana, atjaunināšana un pabeigšana.
-   Krējumu saņemšana pret pirkšanas pasūtījumu vai pārsūtīšanas pasūtījumu.
-   Krājumu uzskaites veikšana.
-   Pārdošanas transakciju izgūšana dažādos veikalos un atgriešanas transakciju izpildīšana.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Iepriekš definētu reālā laika pakalpojuma profila izveidošanas.


