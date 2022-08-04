---
title: Kravu un sūtījumu plānošana, izmantojot kravu plānošanas rīku
description: Šajā rakstā ir norādīts, kā izmantot kravu plānošanas resursu, lai izveidotu pārdošanas pasūtījuma noslodzi.
author: Mirzaab
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e53b7667dd4589a7c6c14b8aaf8ba51017eee0d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068336"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Kravu un sūtījumu plānošana, izmantojot kravu plānošanas rīku

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir norādīts, kā izmantot kravu plānošanas resursu, lai izveidotu pārdošanas pasūtījuma noslodzi. Kā priekšnosacījumu mēs vispirms izveidosim pārdošanas pasūtījumu. Šī procedūra ir daļa no transportēšanas koordinatora ikdienas darba. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-a-sales-order"></a>Izveidot pārdošanas pasūtījumu
1. Dodieties uz **Navigācijas rūts > Moduļi > Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**.
3. Laukā **Debitora konts** atlasiet nolaižamā saraksta pogu, lai atvērtu pārlūku.
4. Atlasiet kontu **US-004**.
5. Atlasiet **Labi**.
6. Laukā **Krājuma kods** atlasiet nolaižamā saraksta pogu, lai atvērtu pārlūku.
7. Atlasiet preci **A0001**. **A0001** ir iespējots transportēšanas pārvaldībai.  
8. Laukā **Vieta** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu, pēc tam atlasiet preci.
9. Laukā **Daudzums** ierakstiet kādu skaitli.
10. Laukā **Noliktava** šim piemēram ierakstiet vērtību '24'. Šī noliktava ir iespējota transportēšanas pārvaldības un noliktavas pārvaldības procesiem (WMS).  
11. Atlasiet **Saglabāt**.
12. Aizvērt lapu.

## <a name="create-a-new-load"></a>Jaunas noslodzes izveide
1. Dodieties uz **Navigācijas rūts > Moduļi > Transportēšanas pārvaldība > Plānošana > Noslodzes plānošanas rīks**.
2. Atlasiet cilni **Pārdošanas rindas**. Tagad varat izveidot kravu tikko izveidotajam pārdošanas pasūtījumam. Kravas var veidot, balstoties uz piedāvājumu un pieprasījumu no pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem un pārdošanas pasūtījumiem.  
3. Darbību rūtī atlasiet **Piedāvājums un pieprasījums**.
4. Atlasiet **Uz jaunu noslodzi**.
5. Laukā **Kravas veidnes ID** atlasiet nolaižamā saraksta pogu, lai atvērtu uzmeklēšanu. Kravas veidne nosaka maksimālos mērījumus visas kravas svaram un tilpumam. Piemēram, kravas veidne var atspoguļot konteinera vai kravas automašīnas lielumu. Atlasiet krājumu.
6. Atlasiet **Labi**.

## <a name="rate-and-route-the-load"></a>Noslodzes novērtēšana un maršrutēšana
1. Atlasiet **Novērtēšana un maršrutēšana**.
2. Atlasiet **Likmju un maršrutu rīks**.
3. Atlasiet **Likmes veikals**.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Atlasiet **Piešķirt**.
6. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]