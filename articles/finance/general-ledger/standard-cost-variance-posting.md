---
title: Standarta izmaksu novirzes grāmatošana
description: Šajā tēmā sniegta informācija par grāmatošanas metožu iestatīšanu standarta izmaksu grāmatošanā.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: bc4f1bd7c1bf7a8f214f20460b10d371d8f3c790
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804642"
---
# <a name="standard-cost-variance-posting"></a>Standarta izmaksu novirzes grāmatošana

Kad jūs izmantojat standarta izmaksu ēšanu vienam vai vairākiem produktiem jūsu organizācijā, jums ir jākonfigurē [standarta izmaksu aprēķināšanas priekšnosacījumi](/supply-chain/cost-management/prerequisites-standard-costs.md). Šī tēma skaidro grāmatošanas kontus, kas ir nepieciešami 3. solim no priekšnosacījumi" "Virsgrāmatas kontu piešķiršana krājumu grāmatojumi, kas ir saistīti ar standarta izmaksu noviržu."

Pirkšanas un ražošanas pasūtījumiem var rasties dažādi noviržu tipi. Ražošanas noviržu piemērus skatiet sadaļā [Kopējie ražošanas noviržu avoti](/supply-chain/cost-management/common-sources-of-production-variances.md). Pirkšanas pasūtījuma cenas novirzes rodas, kad izmantojat pirktā krājuma standarta izmaksas, un pastāv starpība starp preces standarta izmaksām un rēķinā iekļautais daudzums pirkšanas pasūtījumā.

## <a name="sample-posting-profile-configuration"></a>Grāmatošanas metodes konfigurācijas paraugs

Tabulā redzami noklusētā grāmatošanas tipa piemēri. Tajā ir ietverti parauga galvenie konti un apraksti.

- "Debets/kredīts?" Kolonna norāda, vai darbība parasti ir debets vai kredīts. Dažos gadījumos darbība var grāmatot debetus vai kredītus.
- Kolonna Tīrīšanas konts norāda, ka grāmatošanas tips ir tīrīšanas konts. Citiem vārdiem sakot, šajā kontā grāmatotā summa tiek automātiski atcelta, grāmatojot vēlāku darbību.
- Kolonna "P/F" norāda grāmatošanas tipu. "P" parāda fizisko grāmatošanu, un "F" parāda finanšu grāmatošanu.
- Kolonna "Sekot" norāda, vai galvenais konts grāmatošanas tipam parasti ir tāds pats kā galvenais konts citam grāmatošanas tipam. It īpaši tas norāda grāmatošanas tipu, kas parasti tiek izmantots.

> [!NOTE]
> Galvenie konti un galveno kontu nosaukumi tabulā ir ieteikumi. Ieteicams strādāt ar savu grāmatvedi, lai noteiktu biznesa vajadzībām labāko konfigurāciju.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | P/F | Izpildiet | Apraksts |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Pirkšanas cenas novirze | 510310 | Pirkšanas cenas novirze | Izdevumi | Vai nu vai | Nē | F | Nav attiecināms | Šo kontu izmanto, kad pirkšanas pasūtījumā pastāv novirze starp pirkšanas cenu un standarta izmaksām. |
| Krājumu izmaksu pārvērtēšana | 510330 | Krājumu izmaksu pārvērtēšana | Izdevumi | Vai nu vai | Nē | F | Nav attiecināms | Šo kontu izmanto, kad standarta izmaksu krājumam tiek aktivizēta jauna izmaksu versija, lai pārvērtētu rīcībā esošos krājumus. |
| Izmaksu izmaiņas novirze | 510320 | Izmaksu izmaiņas novirze | Izdevumi | Vai nu vai | Nē | F | Nav attiecināms | Šo kontu izmanto, kad starp vietām ir atšķirīgas standarta izmaksas vai arī tiek atgriezts krājums un pastāv izmaiņas starp sākotnējām standarta izmaksām un pašreizējām produkta standarta izmaksām. |
| Ražošanas laidiena izmēra novirze | 510370 | Ražošanas laidiena izmēra novirze | Izdevumi | Vai nu vai | Nē | F | Nav attiecināms | Šo kontu izmanto, kad pastāv atšķirības starp materiālu komplektu (MK) aprēķina pamatu un faktisko daudzumu ražošanas pasūtījuma izmaksu aprēķinam. |
| Ražošanas cenas novirze | 510340 | Ražošanas cenas novirze | Izdevumi | Vai nu vai | Nē | F | Nav attiecināms | Šo kontu izmanto, kad pastāv cenu starpība starp prognozētajām izmaksām un faktiskajām ražošanas pasūtījuma izmaksām. |
| Ražošanas daudzuma novirze | 510350 | Ražošanas daudzuma novirze | Izdevumi | Vai nu vai | Nē | F | Nav attiecināms | Šo kontu izmanto, kad starp ražošanas pasūtījuma prognozētajām izmaksām un faktiskajām izmaksām pastāv daudzuma starpība. |
| Ražošanas aizstāšanas novirze | 510360 | Ražošanas aizstāšanas novirze | Izdevumi | Vai nu vai | Nē | F | Nav attiecināms | Šo kontu izmanto, kad ražošanas pasūtījumā ir neparedzēts patēriņš. |
| Noapaļošanas novirze | 618160 | Noapaļošanas starpība | Izdevumi | Vai nu vai | Nē | F | Nav attiecināms | Šo kontu izmanto, kad ir noapaļošanas starpība, kad ražošanas izmaksas tiek aprēķinātas no standarta izmaksām. |
