---
title: Kopuma apstrādes konfigurēšana
description: Šajā ceļvedī aprakstīts, kā iestatīt kritērijus, kas nosaka, vai kopumi tiek apstrādāti manuāli vai automātiski, un darbam, kas tiek ģenerēts noliktavai, apstrādājot kopumu, kā arī vai kopumi tiek apstrādāti automātiski vai manuāli.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e22816b33739141fbcd188d631a07313db415959
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977292"
---
# <a name="configure-wave-processing"></a>Kopuma apstrādes konfigurēšana

[!include [banner](../../includes/banner.md)]

Šajā ceļvedī aprakstīts, kā iestatīt kritērijus, kas nosaka, vai kopumi tiek apstrādāti manuāli vai automātiski, un darbam, kas tiek ģenerēts noliktavai, apstrādājot kopumu, kā arī vai kopumi tiek apstrādāti automātiski vai manuāli. Norādiet kritērijus, izveidojot kopuma veidnes un vaicājumus, kas sakrīt ar kopumu izsniegtajām rindām pārdošanas pasūtījumos, ražošanas pasūtījumos un kanban. Kopuma apstrādes tiek izmantotas noliktavās, kuras izmanto noliktavas vadības moduli, un ne tās, kas izmanto funkcionalitāti moduļa krājuma vadībā. Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF.

1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Uzstādīšana > Kopumi > Kopumu veidnes**.
2. Klikšķiniet **Jauns**.
3. Ierakstiet vērtību laukā **Kopuma veidnes nosaukums**. Iestatot kopuma veidni, norādiet secību, kādā veidnes tiks saskaņotas ar izlaistajām rindām pārdošanas pasūtījumos, ražošanas pasūtījumos vai kanban. Kad rindas tiek nodotas uz noliktavu vai uz ražošanu, tiek izmantota pirmā kopuma veidne, kas atbilst kritērijiem. Mēs iesakām šī saraksta sākumā novietot veidnes ar visspecifiskākajiem kritērijiem. Jo plašāki kritēriji, jo vairāk iespējams, ka rinda atbildīs kritērijiem, un rezultātā rindas var tikt piešķirtas nepareizajam kopumam.  
4. Laukā **Kopuma veidnes apraksts** ierakstiet kādu vērtību.
5. Laukā **Vieta** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat atlasīt "Vieta 2".  
6. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību. Ja izmantojat krājumu USMF, varat atlasīt 24. noliktavu.  
7. Iestatiet lauku **Automatizēt kopuma izveidi** uz **Jā**. Atlasiet šo opciju, lai automātiski izveidotu kopumu, kad pārdošanas pasūtījums, ražošanas pasūtījums vai Kanban tiek nodotas izpildei noliktavā.  
8. Iestatiet opciju **Apstrādāt kopumu, to pārvietojot uz noliktavu** uz **Jā**. Atlasiet šo opciju, lai automātiski apstrādātu kopumu un izveidotu darbu, kad rinda tiek nodotas izpildei noliktavā.  
9. Iestatiet opciju **Automatizēt kopuma izlaidi** uz **Jā**. Atlasiet šo opciju, lai automātiski izlaistu kopumu. Izdošanas darbs ir izveidots un pieejams mobilajās ierīcēs.  
10. Iestatiet opciju **Piešķirt atvērtiem kopumiem** uz **Jā**. Rindas tiek piešķirtas kopumiem, pamatojoties uz kopuma veidnes vaicājuma filtru.  
11. Iestatiet opciju **Apstrādāt kopumu automātiski pie sliekšņvērtības** uz **Jā**. Atlasiet šo opciju, lai automātiski apstrādātu kopumu, kad tā vērtības sasniedz svara, sūtījuma un lauku grupā Kopuma robežvērtības norādīto rindu robežvērtības. Šī opcija ir pieejama tikai tad, ja laukā Kopuma veidnes tips ir atlasīta opcija Nosūtīšana.  
12. Iestatiet opciju **Automatizēt papildināšanas darbu izlaidi** uz **Jā**. Atlasiet šo opciju, lai izveidotu uz pieprasījuma balstītu papildināšanas darbu un automātiski to izlaistu. Jums ir jāpievieno papildināšanas kopuma metode kopuma veidnei un jāizveido papildināšanas veidne, kuras tips ir Kopuma pieprasījums.  
13. Izvērsiet sadaļu **Metodes**.

    - Kopuma veidnes metodes ļauj kontrolēt darbību secību, kurām katrs kopums iet cauri, kad tas tiek apstrādāts. Piemēram, jums var būt kopuma papildināšanas metode. Pievienojot metodi, tā automātiski tiek uzskaitīta atbilstošajā atrašanās vietā darbību secībā. Ja esat iestatījis Automatizēt papildināšanas darba izpildes opciju kā Jā, jums ir jāpievieno papildināšanas metode šeit.  
    - Kopuma atribūti darbojas kā filtri, lai ierobežotu vienumus, kas var izmantot laidienu. Piemēram, jūs varētu norādīt krājumu grupu.  
14. Noklikšķiniet uz **Saglabāt**.
15. Aizvērt lapu.
16. Dodieties uz **Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri**.
17. Izvērsiet sadaļu **Kopuma apstrāde**.
18. Laukā **Kopuma apstrādes partijas grupa** ievadiet vai atlasiet kādu vērtību.
19. Iestatiet opciju **Veikt kopumiem pakešveida apstrādi** uz **Jā**.
20. Laukā **Gaidīt slēgu (ms)** ievadiet skaitli. Ievadiet milisekundēs izteiktu laiku, cik ilgi sadalījuma darbībai ir jāgaida sistēmas resurss, kuru ir bloķējusi cita sadalījuma darbība. Kad šis laiks ir pagājis, kopums netiek apstrādāts un tiek parādīts kļūdas ziņojums.  
21. Noklikšķiniet uz **Saglabāt**.
22. Aizvērt lapu.
23. Dodieties uz **Navigācijas rūts > Moduļi > Ražošanas kontrole > Iestatīšana > Ražošanas kontroles parametri**.
24. Laukā **Pārvietot uz noliktavu** atlasiet opciju.

Pārdošanas pasūtījumiem un Kanban pasūtījumiem pirms pasūtījuma pārvietošanas uz noliktavu attiecīgie krājumi ir jārezervē. Pretējā gadījumā krājumus vai sadalījuma rindas nevar apstrādāt kopumā. Ražošanas pasūtījumiem, jums ir iespēja atlasīt Atļaut daļēju rezervēšanu. Tas var noderēt, piemēram, ja jums ir ražošanas sākšanai nepieciešamie materiāli, un varat pagaidīt, līdz kļūst pieejami papildu materiāli, lai pabeigtu procesu. Ja atlasāt šo opciju, pārvietošana uz noliktavu ir manuāli jāatkārto, kad papildu materiāli kļūst pieejami.  
25. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]