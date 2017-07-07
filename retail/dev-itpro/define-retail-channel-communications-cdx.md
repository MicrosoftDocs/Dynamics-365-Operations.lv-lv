---
title: "Mazumtirdzniecības kanālu sakaru definēšana (Commerce Data Exchange)"
description: "Šajā rakstā ir sniegts pārskats par Commerce Data Exchange un tā komponentiem. Tajā ir paskaidrots, kāda ir katra komponenta nozīme datu pārsūtīšanā starp programmatūru Microsoft Dynamics 365 for Retail un mazumtirdzniecības kanāliem."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Mazumtirdzniecības kanālu sakaru definēšana (Commerce Data Exchange)

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par Commerce Data Exchange un tā komponentiem. Tajā ir paskaidrots, kāda ir katra komponenta nozīme datu pārsūtīšanā starp programmatūru Microsoft Dynamics 365 for Retail un mazumtirdzniecības kanāliem.

<a name="overview"></a>Pārskats
--------

Commerce Data Exchange ir sistēma, kas nodrošina datu pārsūtīšanu starp programmatūru Dynamics 365 for Retail un mazumtirdzniecības kanāliem, piemēram, tiešsaistes veikaliem vai fiziskiem veikaliem. Mazumtirdzniecības dari tiek glabāti no Dynamics 365 for Retail datu bāzes atsevišķā datu bāzē. Kanāla datu bāze ietver tikai tos datus, kas ir nepieciešami mazumtirdzniecības transakcijām. Pamatdati tiek konfigurēti programmatūrā Dynamics 365 for Retail un izplatīti uz kanāliem. Transakciju dati tiek izveidoti pārdošanas punkta (POS) sistēmā vai tiešsaistes veikalā un pēc tam augšupielādēti programmatūrā Dynamics 365 for Retail. Datu izplatīšana ir asinhrona. Citiem vārdiem sakot — datu apkopošanas un iepakošanas process avotā notiek atsevišķi no saņemšanas un lietošana procesa datu galamērķī. Noteiktiem scenārijiem, piemēram, cenu un krājumu uzmeklēšanai, dati ir jāizgūst reālajā laikā. Šo gadījumu vajadzībām sistēmā Commerce Data Exchange ir ietverts arī pakalpojums, kas nodrošina reāllaika sakarus starp programmatūru Dynamics 365 for Retail un kanālu. 

[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Asinhronais serviss
Lai noteiktu datu izmaiņas, kas ir jānosūta uz kanāliem, tiek izmantota Microsoft SQL Server izmaiņu izsekošana Dynamics 365 for Retail datu bāzē. Pamatojoties uz sadales grafiku, programmatūra Dynamics 365 for Retail nodrošina šo datu ievietošanu pakotnēs un saglabāšanu centrālajā krātuvē (Azure Blob krātuvē). Atsevišķas pakešveida apstrādes izmanto Commerce Data Exchange: Async klienta bibliotēku, lai šo datu pakotni ievietotu kanāla datu bāzē. 

[![Asinhronais serviss](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Mazumtirdzniecības plānotājs

Plānotāja darbi ir mehānisms, ar ko tiek veikta datu izplatīšana uz novietojumiem un no tiem. Darbi sastāv no apakšdarbiem, kuri norāda tabulas un tabulu laukus, kas satur izplatāmos datus. Programmatūrā Dynamics 365 for Retail ir ietverti iepriekš definēti plānotāja darbi un apakšdarbi, kas atbilst replicēšanas prasībām vairumā organizāciju. Tiek izveidoti tālāk norādītie iepriekš definēto darbu tipi.

-   **Lejupielādes darbi** — lejupielādes darbi nodrošina izmainīto datu nosūtīšanu no programmatūras Dynamics 365 for Retail uz kanālu datu bāzēm. Ierakstiem veiktas modifikācijas tiek izsekotas ar SQL Server izmaiņu reģistrēšanu.
-   **Augšupielādes darbi (P darbi)** — augšupielādes darbi nodrošina pārdošanas transakciju izvilkšanu no kanāla no nosūtīšanu uz Dynamics 365 for Retail datu bāzi. P darbi datus augšupielādē pakāpeniski. Kad tiek palaists P darbs, Async klienta bibliotēka pārbauda replicēšanas skaitītāju ierakstiem, kas jau ir saņemti no novietojuma. Ieraksts tiek augšupielādēts tikai tad, ja tā replicēšanas skaitītājs ir lielāks par lielāko atrasto vērtību. P darbi neatjaunina datus, kas tika augšupielādēti iepriekš.

Sadales grafiks tiek izmantots, lai palaistu datu pārsūtīšanas procesu manuāli vai ieplānojot pakešuzdevumu programmatūrā Dynamics 365 for Retail. Sadales grafiks var ietvert vienu vai vairākas kanālu datu grupas, kā arī vienu vai vairākus plānotāja darbus.

## <a name="realtime-service"></a>Realtime Service
Commerce Data Exchange: Real-time Service ir integrēts pakalpojums, kas nodrošina reāllaika sakarus starp programmatūru Dynamics 365 for Retail un mazumtirdzniecības kanāliem. Pakalpojums Real-time Service sniedz atsevišķiem POS datoriem un tiešsaistes veikaliem iespēju reāllaikā izgūt noteiktus datus no programmatūras Dynamics 365 for Retail. Lai gan vairumu galveno operāciju var veikt lokālajā kanāla datu bāzē, tālāk norādītajos gadījumos ir nepieciešama tieša piekļuve programmatūrā Dynamics 365 for Retail glabātajiem datiem.

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




