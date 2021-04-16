---
title: Standarta izmaksu atjauninājumu pārvaldība
description: Standarta izmaksu datu atjauninājumus var pārvaldīt, izmantojot divas dažādas pieejas — vienas versijas pieeju vai divu versiju pieeju.
author: AndersGirke
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: dfe55134a9a9f3c40ebddcafd1d9e481976134ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832350"
---
# <a name="manage-standard-cost-updates"></a>Standarta izmaksu atjauninājumu pārvaldība

[!include [banner](../includes/banner.md)]

Standarta izmaksu datu atjauninājumus var pārvaldīt, izmantojot divas dažādas pieejas — vienas versijas pieeju vai divu versiju pieeju.

Vienas versijas pieejā tiek izmantota viena izmaksu aprēķināšanas versija, kas satur visus izmaksu ierakstus. Šie ieraksti ietver sākotnējās izmaksas un visus izmaksu atjauninājumus.

Divu versiju pieejā tiek izmantota viena versija, kas satur sākotnējo izmaksu ierakstus, un otra versija, kas satur visu izmaksu atjauninājumu ierakstus. Primārā divu versiju pieejas priekšrocība ir skaidrais izmaksu atjauninājumu un izsekošanas attēlojums atsevišķā izmaksu novērtēšanas versijā, neietekmējot sākotnējo izmaksu novērtēšanas versiju. Divu versiju pieeju var izmantot, lai identificētu vairākus inkrementālus atjauninājumus, kuram katram ir atsevišķa izmaksu aprēķināšanas versija, kas satur inkrementālo izmaksu ierakstus.

## <a name="example"></a>Paraugs

Tālāk sniegtajā piemērā ir parādīts, kā vienas versijas un divu versiju pieeju var izmantot standarta izmaksu atjaunināšanai ražošanas vidē. Piemēram, atjauninājumi, kas attiecas uz jauniem krājumiem vai kļūdu labojumiem. Pieņemsim, ka viena izmaksu aprēķināšanas versija attiecas uz standarta izmaksām pašreizējā gadā. Šī versija identifikators ir 2020-STD. Versija 2020-STD satur visu krājumu pašreizējās aktīvās izmaksas. Turklāt tā satur visas ar maršrutēšanu saistītās izmaksu kategorijas un pieskaitāmo izmaksu aprēķināšanas formulas, kas bija zināmas 2020. gada sākumā. 2020-STD ir sākotnējā izmaksu aprēķināšanas versija.

- **Vienas versijas pieeja izmaksu datu atjauninājumiem** — vienas versijas pieejā sākotnējā izmaksu aprēķināšanas versija 2020-STD satur visus izmaksu ierakstus. Izmaksu atjauninājumi tiek reģistrēti versijā 2020-STD, un tiem tiek iestatīts statuss Gaida. Lai atainotu labojumus, gaidītās izmaksas var manuāli ievadīt, ja izmaksas ir saistītas ar jauniem iegādātajiem krājumiem, vai arī aprēķināt, ja izmaksas ir saistītas ar saražotu krājumu. Ja tiek izmantota vienas versijas pieeja, MK aprēķiniem nav nepieciešams atkāpšanās datu avots, jo visas aktīvās izmaksas ir ietvertas izmaksu noteikšanas versijā. Kad gaidāmās izmaksas kļūst aktīvas, sākotnēja izmaksu aprēķināšanas versija 2020-STD atkal satur visas pašreizējās aktīvās izmaksas.
- **Divu versiju pieeja izmaksu datu atjauninājumiem** — divu versiju pieejai nepieciešama papildu izmaksu aprēķināšanas versija, kas satur tikai izmaksu atjauninājumus. Šī versija identifikators ir 2020-STD-IZMAIŅAS. Izmaksu atjauninājumi tiek reģistrēti versijā 2020-STD-CHANGES, un tiem tiek iestatīts statuss Gaida. Ja tiek izmantota divu versiju pieeja, saražoto krājumu gaidāmo izmaksu MK aprēķiniem ir nepieciešams atkāpšanās datu avots. Tas ir tāpēc, ka papildu izmaksu aprēķināšanas versija 2020-STD-IZMAIŅAS satur tikai izmaksu datu apakškopu. Atkāpšanās var būt izteikta kā aktīvās izmaksas vai kā izmaksu aprēķināšanas versija 2020-STD, jo tās abas norāda versijā 2020-STD-IZMAIŅAS neietverto izmaksu datu avotu. Kad gaidāmās izmaksas kļūst aktīvas, izmaksu aprēķināšanas versija 2020-STD-IZMAIŅAS satur pašreizējās aktīvās izmaksas, kas ataino atjauninājumus, bet sākotnējā izmaksu aprēķināšanas versija 2020-STD paliek nemainīga. Ja tiek izmantota divu versiju pieeja, ir jāiestata sākotnējās izmaksu aprēķināšanas versijas bloķēšanas politikas, lai nepieļautu atjauninājumus. Papildu izmaksu aprēķināšanas versijai ir jāiestata tādas pašas bloķēšanas politikas, izņemot noteikto sākuma datumu un selektīvo bloķēšanas politiku izmantošanu, lai atļautu atjauninājumus. Noteiktajam sākuma datumam jātiek atjauninātam ar katru izmaiņu paketi, lai parādītu prognozēto aktivizēšanas datumu.

Šajā piemērā tika izmantota viena papildu izmaksu aprēķināšanas versija, lai pārvaldītu atjauninājumus par 2020. gadu. Var izmantot vairākas izmaksu aprēķināšanas versijas, piemēram, atsevišķu versiju katram atjauninājumu paketei. Ja tiek izmantotas vairākas papildu izmaksu aprēķināšanas versijas, atkāpšanās ir jāizsaka kā aktīvās izmaksas, jo aktīvās izmaksas ir ietvertas vairākās izmaksu aprēķināšanas versijās.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Finanšu dimensijas standarta izmaksu pārvērtēšanai

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Aktivizējot jaunu standarta cenu, rīcībā esošo krājumu vērtība parasti tiks pārvērtēta, izmantojot standarta izmaksu pārvērtēšanas darbības. Parasti krājuma finanšu dimensijas pēc tam tiek grāmatotas darbībās. Tomēr, ja vēlaties kontrolēt, vai un kā finanšu dimensijas ir iegrāmatotas, izmantojiet [līdzekļu pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu līdzekli ar nosaukumu *Noklusējuma finanšu dimensiju opcijas krājumu standarta izmaksu pārvērtēšanai*. Pēc šīs funkcijas iespējošanas dodieties uz **Izmaksu pārvaldība > Krājumu uzskaites politiku iestatījumi > Parametri** un iestatiet jauno **Finanšu dimensiju izcelsmes** nolaižamo sarakstu uz vienu no šīm vērtībām:

- **Nav** nozīmē, ka ārvalstu valūtas pārvērtēšanas transakcijās nav grāmatotas nekādas finanšu dimensijas. Ja konta struktūrā ir noteikta obligāta finanšu dimensija, pārvērtēšanas process tiek veikts, bet tiek izveidoti uzskaites ieraksti bez finanšu dimensijām. Šajā gadījumā lietotāji vispirms saņems brīdinājuma ziņojumu, tādējādi, ja nepieciešams, viņi var atcelt pārvērtēšanu.
- **Tabula** - Krājuma finanšu dimensijas pēc tam tiek grāmatotas pārvērtēšanas darbībās. Šis ir noklusētais iestatījums un atbilst sākotnējai sistēmas funkcionalitātei, ieslēdzot funkciju *Krājumu standarta izmaksu pārvērtēšanas noklusēto finanšu dimensiju*.
- **Grāmatošana** — ārvalstu valūtas pārvērtēšanas transakcijās tiek iegrāmatotas pārvērtētās transakcijas finanšu dimensijas. Pēc noklusējuma finanšu dimensijas no oriģinālās darbības krājumu konta tiks izmantotas gan krājumu kontam, gan pārvērtēšanas kontam.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]