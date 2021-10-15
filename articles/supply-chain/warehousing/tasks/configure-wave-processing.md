---
title: Kopuma apstrādes konfigurēšanas paraugs
description: Šajā ceļvedī aprakstīts, kā iestatīt kritērijus, kas nosaka, vai kopumi tiek apstrādāti manuāli vai automātiski, un darbam, kas tiek ģenerēts noliktavai, apstrādājot kopumu, kā arī vai kopumi tiek apstrādāti automātiski vai manuāli.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39c3fecf9250ee89c22003d5dff4ea662c3042e3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572989"
---
# <a name="configure-wave-processing-example"></a>Kopuma apstrādes konfigurēšanas paraugs

[!include [banner](../../includes/banner.md)]

Šajā ceļvedī aprakstīts, kā iestatīt kritērijus, kas nosaka, vai kopumi tiek apstrādāti manuāli vai automātiski, un darbam, kas tiek ģenerēts noliktavai, apstrādājot kopumu, kā arī vai kopumi tiek apstrādāti automātiski vai manuāli. Norādiet kritērijus, izveidojot kopuma veidnes un vaicājumus, kas sakrīt ar kopumu izsniegtajām rindām pārdošanas pasūtījumos, ražošanas pasūtījumos un kanban.

## <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta demonstrācijas dati. Pirms sākat, jāatlasa arī **USMF** juridiskā persona.

## <a name="example-scenario-configure-wave-processing"></a>Parauga situācija: kopuma apstrādes konfigurēšana

Šajā piemērā tiek rādīti daudzi dažādi iestatījumi, kas ietekmē kopumu izveides, aizpildītas, apstrādātas un izlaistas darbības.

1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas pārvaldība > Uzstādīšana > Kopumi > Kopumu veidnes**.
1. Atlasiet **Jauns**.
1. Ierakstiet vērtību laukā **Kopuma veidnes nosaukums**. Iestatot kopuma veidni, norādiet secību, kādā veidnes tiks saskaņotas ar izlaistajām rindām pārdošanas pasūtījumos, ražošanas pasūtījumos vai Kanban. Kad rindas tiek nodotas uz noliktavu vai uz ražošanu, tiek izmantota pirmā kopuma veidne, kas atbilst kritērijiem. Mēs iesakām šī saraksta sākumā novietot veidnes ar visspecifiskākajiem kritērijiem. Jo plašāki kritēriji, jo vairāk iespējams, ka rinda atbildīs kritērijiem, un rezultātā rindas var tikt piešķirtas nepareizajam kopumam.  
1. Laukā **Kopuma veidnes apraksts** ierakstiet kādu vērtību.
1. Laukā **Vieta** ievadiet vai atlasiet kādu vērtību. Ja izmantojat USMF, varat atlasīt "Vieta 2".  
1. Laukā **Noliktava** ievadiet vai atlasiet kādu vērtību. Ja izmantojat krājumu USMF, varat atlasīt 24. noliktavu.  
1. Iestatiet lauku **Automatizēt kopuma izveidi** uz **Jā**. Atlasiet šo opciju, lai automātiski izveidotu kopumu, kad pārdošanas pasūtījums, ražošanas pasūtījums vai Kanban tiek nodotas izpildei noliktavā.  
1. Iestatiet opciju **Apstrādāt kopumu, to pārvietojot uz noliktavu** uz **Jā**. Atlasiet šo opciju, lai automātiski apstrādātu kopumu un izveidotu darbu, kad rinda tiek nodotas izpildei noliktavā.  
1. Iestatiet opciju **Automatizēt kopuma izlaidi** uz **Jā**. Atlasiet šo opciju, lai automātiski izlaistu kopumu. Izdošanas darbs ir izveidots un pieejams mobilajās ierīcēs.  
1. Iestatiet opciju **Piešķirt atvērtiem kopumiem** uz **Jā**. Rindas tiek piešķirtas kopumiem, pamatojoties uz kopuma veidnes vaicājuma filtru.  
1. Iestatiet opciju **Apstrādāt kopumu automātiski pie sliekšņvērtības** uz **Jā**. Atlasiet šo opciju, lai automātiski apstrādātu kopumu, kad tā vērtības sasniedz svara, sūtījuma un lauku grupā **Kopuma robežvērtības** norādīto rindu robežvērtības. Šī opcija ir pieejama tikai tad, ja laukā **Kopuma veidnes tips** ir atlasīta opcija **Nosūtīšana**.  
1. Iestatiet opciju **Automatizēt papildināšanas darbu izlaidi** uz **Jā**. Atlasiet šo opciju, lai izveidotu uz pieprasījuma balstītu papildināšanas darbu un automātiski to izlaistu. Jums ir jāpievieno papildināšanas kopuma metode kopuma veidnei un jāizveido papildināšanas veidne **Kopuma pieprasījuma** tipam.  
1. Lai piešķirtu kopuma atribūtus, izmantojiet grupas **Noklusējuma vērtības** fiksētās vērtības iestatījumus. Kopuma atribūti darbojas kā filtri, lai ierobežotu vienumus, kas var izmantot laidienu. Piemēram, jūs varētu norādīt krājumu grupu.  
1. Izvērsiet sadaļu **Metodes** un iestatiet ar kopuma veidni veicamās darbības. Kopuma veidnes metodes ļauj kontrolēt darbību secību, kurām katrs kopums iet cauri, kad tas tiek apstrādāts. Piemēram, jums var būt kopuma papildināšanas metode. Pievienojot metodi, tā automātiski tiek uzskaitīta atbilstošajā atrašanās vietā darbību secībā. Ja esat iestatījis **Automatizēt papildināšanas darba izpildes** opciju kā **Jā**, jums ir jāpievieno papildināšanas metode šeit.  
1. Atlasiet **Saglabāt**.
1. Aizvērt lapu.
1. Dodieties uz **Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri**.
1. Izvērsiet sadaļu **Kopuma apstrāde**.
1. Laukā **Kopuma apstrādes partijas grupa** ievadiet vai atlasiet kādu vērtību.
1. Iestatiet opciju **Veikt kopumiem pakešveida apstrādi** uz **Jā**.
1. Laukā **Gaidīt slēgu (ms)** ievadiet skaitli. Ievadiet milisekundēs izteiktu laiku, cik ilgi sadalījuma darbībai ir jāgaida sistēmas resurss, kuru ir bloķējusi cita sadalījuma darbība. Kad šis laiks ir pagājis, kopums netiek apstrādāts un tiek parādīts kļūdas ziņojums.  
1. Atlasiet **Saglabāt**.
1. Aizvērt lapu.
1. Dodieties uz **Navigācijas rūts > Moduļi > Ražošanas kontrole > Iestatīšana > Ražošanas kontroles parametri**.
1. Laukā **Pārvietot uz noliktavu** atlasiet opciju.

    Pārdošanas pasūtījumiem un Kanban pasūtījumiem pirms pasūtījuma pārvietošanas uz noliktavu attiecīgie krājumi ir jārezervē. Pretējā gadījumā krājumus vai sadalījuma rindas nevar apstrādāt kopumā. Ražošanas pasūtījumiem, jums ir iespēja atlasīt **Atļaut daļēju rezervēšanu**. Tas var noderēt, piemēram, ja jums ir ražošanas sākšanai nepieciešamie materiāli, un varat pagaidīt, līdz kļūst pieejami papildu materiāli, lai pabeigtu procesu. Ja atlasāt šo opciju, pārvietošana uz noliktavu ir manuāli jāatkārto, kad papildu materiāli kļūst pieejami.
1. Aizvērt lapu.

## <a name="additional-resources"></a>Papildu resursi

- [Kopumu izveide un apstrāde](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
