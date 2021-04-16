---
title: Sākotnējā rēķina atsauces kredīta notās
description: Šajā tēmā ir paskaidrots, kā iestatīt un drukāt sākotnējo rēķinu numurus saistītajās kredīta notās.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ce06a0ce4f2a308e1917ac2c7cbc66f0494a2ec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811514"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Sākotnējā rēķina atsauces kredīta notās

[!include [banner](../includes/banner.md)]


Dažās valstīs un reģionos pastāv juridiska prasība, ka drukātajās kredīta notās jāietver atsauces uz sākotnējiem rēķiniem. Šajā tēmā ir paskaidrots, kā iestatīt un drukāt sākotnējo rēķinu numurus saistītajās kredīta notās.

## <a name="prerequisites"></a>Priekšnosacījumi

- Darbvietā **Līdzekļu pārvaldība** ieslēdziet līdzekli **Kredīta rēķinu izkārtojums pārdošanas un projekta rēķinu atskaitēs**. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).
- Nepieciešamo dokumentu drukājamie formāti ir jākonfigurē Drukas pārvaldībā.

Šajā tēmā aprakstītā funkcionalitāte attiecas uz šādiem dokumentiem:

**Debitori**

- Brīva teksta kredīta nota
- Debitora kredīta nota

**Projektu pārvaldība un uzskaite**

- Projekta kredīta nota

## <a name="configure-accounts-receivable-parameters"></a>Debitoru parametru konfigurēšana

Izpildiet šīs darbības, lai iestatītu parametru, kas kontrolē, vai atsauces uz sākotnējiem rēķiniem tiek drukātas saistītajās kredīta notās.

1. Dodieties uz **Debitori** \> **Iestatīšana** \> **Debitoru parametri**.
2. Cilnes **Atjauninājumi** kopsavilkuma cilnē **Rēķins** iestatiet opciju **Lietot kredīta rēķinu izrakstīšanas izkārtojumu pārdošanas un projektu rēķinu pārskatos** uz **Jā**.

![Debitoru parametru konfigurēšana](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Atsauču definēšana sākotnējiem rēķiniem

Izmantojiet tālāk uzskaitītās procedūras, lai definētu atsauces sākotnējiem rēķiniem, pamatojoties uz dokumenta veidu.

### <a name="free-text-credit-note"></a>Brīva teksta kredīta nota

1. Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.
2. Izveidojiet jaunu kredīta notu vai atlasiet esošu kredīta notu.
3. Atveriet rēķinu.
4. Darbību rūtī, cilnē **Rēķins**, grupā **Funkcijas** atlasiet **Kredīta rēķinu izrakstīšana**.
5. Ievadiet atsauci uz sākotnējo rēķinu un atlasiet labojuma pamatojumu.

![Atsauču definēšana brīva teksta rēķinam](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Debitora kredīta nota

1. Doties uz **Debitori** \> **Pasūtījumi** \> **Visi pārdošanas pasūtījumi**.
2. Atlasiet un atveriet rēķinā iekļauto pārdošanas pasūtījumu, kas ir jālabo.
3. Darbību rūtī, cilnē **Pārdošana**, grupā **Kredīta nota** atlasiet **Kredīta nota**.
4. Ievadiet labošanas iemeslu. Atsauce uz sākotnējo rēķinu tiek izveidota automātiski.

![Atsauču definēšana pārdošanas pasūtījumam](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projekta kredīta nota

1. Dodieties uz **Projektu pārvaldība un uzskaite** \> **Projekta rēķini** \> **Projekta rēķini**.
2. Atlasiet un atveriet projekta rēķinu, kas ir jālabo.
3. Darbību rūtī, cilnē **Projekta rēķins**, grupā **Funkcijas** atlasiet **Atlasīt kredīta notai**.
4. Atlasiet **Kredīta rēķina izrakstīšana**.
5. Ievadiet labošanas iemeslu. Atsauce uz sākotnējo rēķinu tiek izveidota automātiski.

![Atsauču definēšana projekta rēķinam](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Kredīta notu drukāšana

Drukājot brīvā teksta, klienta un projekta kredīta notas, tajās tiks iekļauta atsauce uz sākotnējo rēķinu un labošanas iemeslu.

![Drukāta kredīta nota](media/credit-note-FTI.jpg)

> [!NOTE]
> Pārliecinieties, vai dokumentu drukājamie formāti ir pareizi konfigurēti, pieņemot, ka tiks drukātas atsauces uz sākotnējiem rēķiniem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
