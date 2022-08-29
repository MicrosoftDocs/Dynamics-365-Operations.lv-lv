---
title: Sākotnējā rēķina atsauces kredīta notās
description: Šajā rakstā skaidrots, kā iestatīt un drukāt oriģinālos rēķina numurus saistītās kredīta notās.
author: mrolecki
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: f1f9ca3914aa02cc38ddfe9f8dd88eb7fc88fd4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281241"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Sākotnējā rēķina atsauces kredīta notās

[!include [banner](../includes/banner.md)]


Dažās valstīs un reģionos pastāv juridiska prasība, ka drukātajās kredīta notās jāietver atsauces uz sākotnējiem rēķiniem. Šajā rakstā skaidrots, kā iestatīt un drukāt oriģinālos rēķina numurus saistītās kredīta notās.

## <a name="prerequisites"></a>Priekšnosacījumi

- Darbvietā **Līdzekļu pārvaldība** ieslēdziet līdzekli **Kredīta rēķinu izkārtojums pārdošanas un projekta rēķinu atskaitēs**. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Nepieciešamo dokumentu drukājamie formāti ir jākonfigurē Drukas pārvaldībā.

Šajā rakstā aprakstītā funkcionalitāte attiecas uz šādiem dokumentiem:

**Debitori**

- Kredīta nota brīvā tekstā
- Debitora kredīta nota

**Projektu pārvaldība un uzskaite**

- Projekta kredīta nota

## <a name="configure-accounts-receivable-parameters"></a>Debitoru parametru konfigurēšana

Izpildiet šīs darbības, lai iestatītu parametru, kas kontrolē, vai atsauces uz sākotnējiem rēķiniem tiek drukātas saistītajās kredīta notās.

1. Dodieties uz **Debitori** \> **Iestatīšana** \> **Debitoru parametri**.
2. Cilnes **Atjauninājumi** kopsavilkuma cilnē **Rēķins** iestatiet opciju **Lietot kredīta rēķinu izrakstīšanas izkārtojumu pārdošanas un projektu rēķinu pārskatos** uz **Jā**.

![Debitoru parametru konfigurēšana.](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Atsauču definēšana sākotnējiem rēķiniem

Izmantojiet tālāk uzskaitītās procedūras, lai definētu atsauces sākotnējiem rēķiniem, pamatojoties uz dokumenta veidu.

### <a name="free-text-credit-note"></a>Brīva teksta kredīta nota

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Izveidojiet jaunu kredīta notu vai atlasiet esošu kredīta notu.
3. Atveriet rēķinu.
4. Darbību rūtī, cilnē **Rēķins**, grupā **Funkcijas** atlasiet **Kredīta rēķinu izrakstīšana**.
5. Ievadiet atsauci uz sākotnējo rēķinu un atlasiet labojuma pamatojumu.

![Atsauču definēšana brīva teksta rēķinam.](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Debitora kredīta nota

1. Doties uz **Debitori** \> **Pasūtījumi** \> **Visi pārdošanas pasūtījumi**.
2. Atlasiet un atveriet rēķinā iekļauto pārdošanas pasūtījumu, kas ir jālabo.
3. Darbību rūtī, cilnē **Pārdošana**, grupā **Kredīta nota** atlasiet **Kredīta nota**.
4. Ievadiet labošanas iemeslu. Atsauce uz sākotnējo rēķinu tiek izveidota automātiski.

![Atsauču definēšana pārdošanas pasūtījumam.](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projekta kredīta nota

1. Dodieties uz **Projektu pārvaldība un uzskaite** \> **Projekta rēķini** \> **Projekta rēķini**.
2. Atlasiet un atveriet projekta rēķinu, kas ir jālabo.
3. Darbību rūtī, cilnē **Projekta rēķins**, grupā **Funkcijas** atlasiet **Atlasīt kredīta notai**.
4. Atlasiet **Kredīta rēķina izrakstīšana**.
5. Ievadiet labošanas iemeslu. Atsauce uz sākotnējo rēķinu tiek izveidota automātiski.

![Atsauču definēšana projekta rēķinam.](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Kredīta notu drukāšana

Drukājot brīvā teksta, klienta un projekta kredīta notas, tajās tiks iekļauta atsauce uz sākotnējo rēķinu un labošanas iemeslu.

![Drukāta kredīta nota.](media/credit-note-FTI.jpg)

> [!NOTE]
> Pārliecinieties, vai dokumentu drukājamie formāti ir pareizi konfigurēti, pieņemot, ka tiks drukātas atsauces uz sākotnējiem rēķiniem.

## <a name="references-to-original-invoices-in-debit-notes"></a>Atsauces uz sākotnējiem rēķiniem debeta notās

Pēc noklusējuma kredīta notām var ievadīt atsauces uz sākotnējiem rēķiniem. Piemēram, atsauces var ievadīt, ja veicat negatīvus (samazināmus) sākotnējo rēķinu labojumus.

Lai ievadītu atsauces, veicot pozitīvus (palielināšanas) oriģinālo rēķinu labojumus, **Līdzekļu pārvaldības** darbvietā iespējojiet **Atsauces uz sākotnējiem rēķiniem debeta notās**.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
