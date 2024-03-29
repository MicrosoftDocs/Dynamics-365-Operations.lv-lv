---
title: Kolekcijas procesu automatizācijas parametru konfigurēšana
description: Šajā rakstā ir aprakstīti parametri, kas ietekmē automatizētos apkopošanas procesus un sniedz norādījumus to iestatīšanai, lai automatizētais process atspoguļotu jūsu nolūkiem un prognozēm.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c5d0f801c47ef2d98d8ba410dc593bd7640839c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900047"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Kolekcijas procesu automatizācijas parametru konfigurēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti parametri, kas ietekmē automatizētos apkopošanas procesus un sniedz norādījumus to iestatīšanai, lai automatizētais process atspoguļotu jūsu nolūkiem un prognozēm. Informāciju par kolekcijas procesu automatizēšanu skatiet sadaļā [Kolekciju procesu automatizēšana](collections-process-automate.md).

## <a name="general"></a>Vispārējā daļa
Laukā **Klientu īpatsvars uz katru pakešuzdevumu** ievadiet skaitu, lai noteiktu pakešuzdevumu skaitu katram automatizācijas procesam. Iestatiet opciju **Grāmato kolekciju vēstules automātiski** uz **Jā**, lai kolekcijas vēstules darbības veids automatizācijas laikā grāmatotu vēstuli. Iestatiet opciju **Izveidot darbības automatizācijai** uz **Jā**, lai izveidotu un aizvērtu aktivitātes darbību veidiem, kas nav saistīti ar aktivitātēm, lai skatītu visas automatizētās darbības, kas veikti kontā. Sadaļā **Dienas, kad uzturēt kolekciju procesa automatizācijas vēsturi** definējiet dienu skaitu, cik ilgi kolekcijas vēsture tiek glabāta. Kad rēķins sasniedzis parādu piedziņas pēdējo darbību, tas netiks izmantots, lai izveidotu turpmākus procesa automatizācijas darbības veidus, ja opcija **Izslēgt rēķinu pēc pēdējās procesa darbības aktivizēšanas** ir iestatīta uz **Jā**. Nākamais vecākais rēķins nosaka nākamo procesa automatizācijas darbību, lai nodrošinātu, ka tiek turpinātas parādu piedziņas procesa automatizācijas darbības. 

## <a name="payment-predictions"></a>Maksājumu prognozes
Sākot ar 10.0.21. versiju, klientu maksājumu prognozes no Finance Insights rādīs, vai rēķins tiks apmaksāts savlaicīgi, novēloti vai ļoti vēlu. Katru no šīm kategorijām varat konfigurēt Finance Insights. Ja tiek prognozēta vēla rēķinu apmaksa, ir svarīgi, ka uzsākat kolekciju apstrādi pirms rēķina termiņa beigu datuma. Šīs prognozes var izmantot, lai izveidotu kolekciju darbības, kad ir palaista Kolekciju procesa automatizācija. Iestatiet opciju **Iespējot maksājumu prognozes** uz **Jā**, lai lietotu klientu maksājumu prognozes, lai izveidotu kolekciju darbības, balstoties iespējamībā, ka rēķins tiks apmaksāts novēloti. 

Papildu informāciju par Klientu maksājumu prognozēm un Finance Insights skatiet sadaļā [Klientu maksājumu prognozes](payment-insights-overview.md).

Kad ir palaists klienta maksājumu prognožu modelis, tas piešķir īpatsvaru prognozei, ka rēķins tiks apmaksāts savlaicīgi, novēloti vai ļoti vēlu. Šo informāciju varat izmantot, lai automātiski sāktu kolekcijas darbības, izmantojot Kolekciju procesa automatizāciju gadījumos, kad ir sagaidāms novēlots maksājums. Šo īpatsvaru varat skatīt sadaļas **Kredīti un kolekcijas > Kolekcijas** lapā **Maksājumu prognozes katram klientam** vai **Maksājumu prognozes katrai transakcijai**. 

Ja vidējā klienta rēķina maksājuma prognoze ir mazāka par sliekšņa īpatsvaru, darbība netiek izveidota. Ja rēķina prognoze pārsniedz sliekšņa prognozi vai ir vienāda ar to, katram klientam tiek izveidota viena darbība. Opcijai **Prognoze: novēlots** ievadiet **Sliekšņa īpatsvaru** no laika, kad kolekcijas procesu automatizācijai vajadzētu izveidot kolekciju darbības. Tā ir gan novēlotā, gan ļoti novēlotā maksājuma apvienotā vērtība. Atlasiet **Biznesa dokumenta veidni**, lai to lietotu izveidotajai darbībai vai lai izveidotu jaunu. Tādējādi tiek identificēts **Veids**, **Mērķis** un **Dienas līdz darbības slēgšanai**. Ievadiet jebkādas **Piezīmes**, kuras pēc noklusējuma darbības laikā kļūs par aprakstu. Opcijai **Prognoze: ļoti vēls** ievadiet **Sliekšņa īpatsvaru** no laika, kad kolekcijas procesu automatizācijai vajadzētu izveidot kolekciju darbības klientam, kura rēķinu apmaksa tiek prognozēta ļoti vēlu. Atlasiet **Biznesa dokumenta veidni**, lai to lietotu izveidotajai darbībai. Tādējādi tiek identificēts **Veids**, **Mērķis** un **Dienas līdz darbības slēgšanai**. Ievadiet jebkādas **Piezīmes**, kuras pēc noklusējuma darbības laikā kļūs par aprakstu. 

### <a name="example"></a>Paraugs
Ja vēlā sliekšņa īpatsvars ir iestatīts uz 60%. Kad klienta maksājumu prognozes tiek palaistas katram rēķinam, sistēma piešķir īpatsvaru prognozei, ka rēķins tiks apmaksāts savlaicīgi, novēloti vai ļoti vēlu. Ja prognoze, ka rēķins tiks apmaksāts vēlu, ir 59% vai mazāka, automatizētās kolekcijas process rēķinam neizveidos darbību. Ja prognoze, ka klients apmaksās rēķinu, ir lielāka vai vienāda ar 60%, kolekcijas procesu automatizācijas laikā tiek izveidota kolekcijas darbība. 

> [!NOTE]
> Ļoti vēlās apmaksas prognoze tiek izvērtēta pirms novēlotās, jo ļoti vēlā prognoze ietver rēķinus, kuriem tiek prognozēta novēlota apmaksa. Kolekcijas process ģenerē tikai vienu darbību, ja rēķins ietilpts gan ļoti vēlās, gan novēlotās apmaksas robežvērtībā. Šādā gadījumā sistēma lieto ļoti vēlo darbību un biznesa dokumentu, jo ļoti vēlā apmaksa tiek prioritāri ierindota augstāk. Jebkuras citas darbības, kuras jau tikušas ģenerētas, netiks ģenerētas atkārtoti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
