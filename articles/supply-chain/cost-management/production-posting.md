---
title: Ražošanas uzdevuma grāmatošana
description: Šajā rakstā ir sniegta informācija par dažādu tipu grāmatojumiem ražošanas procesā.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee3eaf11f5d77861e7abd29bb428f67b57a3e0e3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565955"
---
# <a name="production-posting"></a>Ražošanas uzdevuma grāmatošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par dažādu tipu grāmatojumiem ražošanas procesā.

Ražošanas grāmatošanas aktivitātes seko ražošanas procesiem, kas ir aprakstīti turpmākajās sadaļās.

## <a name="material-consumption"></a>Materiālu patēriņš
Materiāli tiek reģistrēti kā patērēti ražošanas procesa laikā, kad ražošanas izdošanas saraksta žurnāls tiek iegrāmatots. Šis process izveido izejas plūsmas transakcijas, kas atskaita rīcībā esošos krājumus. Izmantojot ražošanas parametrus, varat norādīt to, vai Virsgrāmatā ir jāgrāmato nepabeigtās ražošanas \[NP\] izejmateriālu vērtība. Pēc tam nepabeigtās ražošanas [NP] izejmateriālu vērtība tiek grāmatota atvēlētajā izdošanas saraksta kontā un atvēlētajā izdošanas saraksta korespondējošā kontā.

## <a name="time-consumption"></a>laika patēriņš.
Laiks, ko darbinieki tērē uz ražošanas darbiem, tiek reģistrēts Maršruta kartes žurnālā vai Darba kartes žurnālā. Kad šie žurnāli tiek grāmatoti, tiek apstrādāta Virsgrāmatas grāmatošana kontā, kas atvēlēts resursiem nepabeigtā projektā (NP). Šī grāmatošana atspoguļo laika vērtību, kas pavadīts pie ražošanas pasūtījuma. Pēc tam, kad ražošanas pasūtījums ir reģistrēts kā pabeigts, šie NP konti tiek nosegti.

## <a name="reporting-finished-goods-and-error-quantities"></a>Pārskati par pabeigtām precēm un kļūdainiem daudzumiem
Kad ir reģistrēta ražošanas pasūtījuma pabeigšana, krājumu vadībā, izmantojot funkciju Pabeigšanas žurnāls, tiek atjaunināts pabeigto krājumu daudzums. Ja veicat NP grāmatvedību, ko var iestatīt ražošanas parametros, Virsgrāmatas žurnāls tiek veidots, lai samazinātu NP kontu skaitu un palielinātu pabeigto preču krājumu skaitu. Žurnālā tiek izmantotas standarta izmaksas, kas ir definētas precei.

## <a name="ending-the-production-order"></a>Ražošanas pasūtījuma pabeigšana
Pirms ražošanas pasūtījuma pabeigšanas faktiskās izmaksas tiek aprēķinātas saražotajam daudzumam. Visas novērtētās materiālu, darbu un papildu atbalsta izmaksas tiek apgrieztas un aizstātas ar faktiskajām izmaksām. Vispārējās pabeigtā krājuma izmaksas tiek debitētas no krājuma Ieejas plūsmas konta un kreditētas uz krājuma Izejas plūsmas kontu. Ja, veicot izmaksu aprēķināšanu, atzīmējat izvēles rūtiņu **Pēdējais darbs**, ražošanas pasūtījuma statuss tiek mainīts uz **Pabeigts**. Šis statuss neļauj pabeigtā ražošanas pasūtījumā nejauši iegrāmatot papildu izmaksas. Varat norādīt, ka ziņojot par pabeigšanu paziņotā kļūdaino daudzumu vērtība ir jāpiešķir preču daudzumiem, par kuriem ir ziņots, ka tie ir pabeigti. Alternatīvi, var norādīt, ka kļūdainu daudzumu vērtība jāgrāmato atvēlētajā brāķa kontā.

## <a name="controlling-the-level-of-ledger-posting"></a>Grāmatošanas Virsgrāmatā kontroles līmenis
Sadaļā **Ražošanas kontroles parametri** lauku **Grāmatošana Virsgrāmatā** var izmantot, lai iestatītu grāmatošanas Virsgrāmatā līmeni ražošanas procesiem. Ir pieejamas šādas vērtības:

-   **Krājums un resurss** — izmantot Virsgrāmatas kontus, kas iestatīti izejmateriālu un pabeigto preču krājumu grupās. NP laika patēriņam tiek ņemts no resursa vai resursu grupas no maršruta operācijām.
-   **Krājums un kategorija** — izmantot Virsgrāmatas kontus, kas iestatīti izejmateriālu un pabeigto preču krājumu grupās. NP laika patēriņam tiek ņemts no izmaksu kategorijām, kas ir saistītas ar maršruta operācijām.
-   **Ražošanas uzdevumu grupas** — izmantot Virsgrāmatas kontus, kas iestatīti ražošanas uzdevumu grupās materiālu un laika patēriņam. Ražošanas uzdevumu grupas ir saistītas ar izlaistajām precēm un kopētas uz ražošanas pasūtījumiem, kad šie pasūtījumi tiek izveidoti. Tad ražošanas pasūtījumu grāmatošana sekos ražošanas uzdevumu grupām, kas ir saistīti ar ražošanas pasūtījumu.

**Piezīme:** ja pabeigto krājumu izmaksu aprēķināšanai tika izmantota standarta metode, šo faktu parāda arī beigu transakcijas. Ja, izmantojot standarta metodi, ir atšķirība starp faktiskajām izmaksām un aprēķinātajām izmaksām, tā tiek grāmatota uz kontu, kas rāda peļņu vai zaudējumus.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]