---
title: "Mazumtirdzniecības kanālu sakaru definēšana (Commerce Data Exchange)"
description: "Šajā rakstā ir sniegts pārskats par Commerce Data Exchange un tā komponentiem. Rakstā ir paskaidrots, kāda katram komponentam ir nozīme datu pārsūtīšanā starp programmatūru Microsoft Dynamics 365 for Operations un mazumtirdzniecības kanāliem."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ba1bb54a29250a2bb59622ee4391b64ac455af33
ms.contentlocale: lv-lv
ms.lasthandoff: 04/26/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Mazumtirdzniecības kanālu sakaru definēšana (Commerce Data Exchange)

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par Commerce Data Exchange un tā komponentiem. Rakstā ir paskaidrots, kāda katram komponentam ir nozīme datu pārsūtīšanā starp programmatūru Microsoft Dynamics 365 for Operations un mazumtirdzniecības kanāliem.

<a name="overview"></a>Pārskats
--------

Commerce Data Exchange ir sistēma, kas pārsūta datus starp Dynamics 365 for Operations un mazumtirdzniecības kanāliem, piemēram, tiešsaistes veikaliem vai fiziskajiem veikaliem. Datu bāze, kurā tiek glabāti dati mazumtirdzniecības kanālam, ir atsevišķi no Dynamics 365 for Operations datu bāzes. Kanāla datu bāze ietver tikai tos datus, kas ir nepieciešami mazumtirdzniecības transakcijām. Pamatdati tiek konfigurēti programmatūrā Dynamics 365 for Operations un izplatīti uz kanāliem. Transakciju dati tiek izveidoti pārdošanas punkta (POS) sistēmā vai tiešsaistes veikalā un pēc tam augšupielādēti uz Dynamics 365 for Operations. Datu izplatīšana ir asinhrona. Citiem vārdiem sakot — datu apkopošanas un iepakošanas process avotā notiek atsevišķi no saņemšanas un lietošana procesa datu galamērķī. Noteiktiem scenārijiem, piemēram, cenu un krājumu uzmeklēšanai, dati ir jāizgūst reālajā laikā. Lai atbalstītu šos scenārijus, Commerce Data Exchange ietver arī pakalpojumu, kas nodrošina reāllaika sakarus starp Dynamics 365 for Operations un kanālu. 

[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Asinhronais serviss
Lai noteiktu datu izmaiņas, kas ir jānosūta uz kanāliem, tiek izmantota Microsoft SQL Server izmaiņu izsekošana Dynamics 365 for Operations datu bāzē. Pamatojoties uz sadales grafiku, Dynamics 365 for Operations iepako šos datus un tos saglabā centrālajā krātuvē (Azure Blob krātuve). Atsevišķas pakešveida apstrādes izmanto Commerce Data Exchange: Async klienta bibliotēku, lai šo datu pakotni ievietotu kanāla datu bāzē. 

[![Asinhronais serviss](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Mazumtirdzniecības plānotājs

Plānotāja darbi ir mehānisms, ar ko tiek veikta datu izplatīšana uz novietojumiem un no tiem. Darbi sastāv no apakšdarbiem, kuri norāda tabulas un tabulu laukus, kas satur izplatāmos datus. Dynamics 365 for Operations ietver iepriekš definētus plānotāja darbus un apakšdarbus, kas atbilst replicēšanas prasībām lielākajā daļā organizāciju. Tiek izveidoti tālāk norādītie iepriekš definēto darbu tipi.

-   **Lejupielādes darbi** — lejupielādes darbi no Dynamics 365 for Operations uz kanāla datu bāzēm sūta datus, kas ir mainījušies. Ierakstiem veiktas modifikācijas tiek izsekotas ar SQL Server izmaiņu reģistrēšanu.
-   **Augšupielādes darbi (P darbi)** — augšupielādes darbi no kanāla uz Microsoft Dynamics 365 for Operations datu bāzi izvelk (Pull) pārdošanas transakcijas. P darbi datus augšupielādē pakāpeniski. Kad tiek palaists P darbs, Async klienta bibliotēka pārbauda replicēšanas skaitītāju ierakstiem, kas jau ir saņemti no novietojuma. Ieraksts tiek augšupielādēts tikai tad, ja tā replicēšanas skaitītājs ir lielāks par lielāko atrasto vērtību. P darbi neatjaunina datus, kas tika augšupielādēti iepriekš.

Sadales grafiks tiek izmantots, lai palaistu datu pārsūtīšanu — manuāli vai ar pakešuzdevumu plānošanu programmatūrā Dynamics 365 for Operations. Sadales grafiks var ietvert vienu vai vairākas kanālu datu grupas, kā arī vienu vai vairākus plānotāja darbus.

## <a name="realtime-service"></a>Realtime Service
Commerce Data Exchange: Real-time Service ir integrēts pakalpojums, kas nodrošina reāllaika sakarus starp Dynamics 365 for Operations un mazumtirdzniecības kanāliem. Real-time Service atsevišķiem POS datoriem un tiešsaistes veikaliem ļauj reālajā laikā izgūt noteiktus datus no Dynamics 365 for Operations. Lai gan lielākā daļa galveno operāciju var veikt lokālajā kanāla datu bāzē, tālāk norādītajiem scenārijiem ir nepieciešama tieša piekļuve datiem, kas tiek glabāti programmatūrā Dynamics 365 for Operations.

-   Dāvanu karšu izsniegšana un izpirkšana.
-   Lojalitātes programmas punktu izpirkšana.
-   Kredītrēķinu izsniegšana un izpirkšana.
-   Debitoru ierakstu izveidošana un atjaunināšana.
-   Pārdošanas pasūtījumu izveidošana, atjaunināšana un pabeigšana.
-   Krējumu saņemšana pret pirkšanas pasūtījumu vai pārsūtīšanas pasūtījumu.
-   Krājumu uzskaites veikšana.
-   Pārdošanas transakciju izgūšana dažādos veikalos un atgriešanas transakciju izpildīšana.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Tiek izveidots iepriekš definēts Real-time Service profils.




