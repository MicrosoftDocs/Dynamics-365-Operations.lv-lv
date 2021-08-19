---
title: Izdrukātie debitoru rēķini ar jaukšanas numuriem — arhivēšana
description: Šajā tēmā paskaidrots, kā iespējot arhivēšanu, lai glabātu drukātos klientu rēķinus ar jaukšanas numuriem.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 474f5f19d709f3f04a2dbf4383360f58db7ecc8953e8624d9eef92286c52d4d8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724211"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Izdrukātie debitoru rēķini ar jaukšanas numuriem — arhivēšana

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dažās valstīs pastāv tiesiska prasība glabāt aprēķinātos jauktos numurus sistēmā kopā ar dažu dokumentu izdrukām. Jauktos numurus var izmantot, lai ziņotu iestādēm, un auditu laikā.

Šajā tēmā paskaidrots, kā konfigurēt arhivēšanu, lai glabātu drukātos klientu rēķinus ar jaukšanas numuriem.

## <a name="prerequisites"></a>Priekšnosacījumi

- Darbvietā **Līdzekļu pārvaldība** iespējojiet līdzekli **Arhivēt drukātos klientu rēķinus ar jauktajiem numuriem**. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigurējiet nepieciešamo dokumentu drukājamos formātus **Drukāšanas pārvaldībā**.

Šī funkcionalitāte ir piemērojama šādiem dokumentiem:

**Debitori**
- Rēķins debitoram
- Debitora kredīta nota
- Brīva teksta rēķins
- Kredīta nota brīvā tekstā

**Projektu pārvaldība un uzskaite**
- Projekta rēķins
- Projekta kredīta nota

## <a name="configure-customer-master-data"></a>Klienta pamatdatu konfigurēšana
Izpildiet šīs darbības, lai konfigurētu klienta datus un iespējotu iespēju automātiski saglabāt drukātos rēķinus kā pielikumus.

1. Dodieties uz **Debitori** > **Visi klienti**. 
2. Atlasiet klientu un kopsavilkuma cilnē **Rēķins un piegāde**, sadaļā **Elektroniskais rēķins**, laukā **Elektroniskā rēķina pielikums** atlasiet **Jā**.

## <a name="print-invoices"></a>Rēķinu drukāšana
Jūs varat izvietot un drukāt jebkuru brīvā teksta, klienta un projekta rēķinu vai kredīta notu klientam, kas konfigurēts iepriekšējā procedūrā.

Atveriet drukātā rēķina lapu **Pielikumi**. Kopsavilkuma cilnē **Pielikums**, lauka grupā **Papildu informācija**, laukā **Dokumenta jauktais numurs** atrodiet glabāto jaukto numuru, kas aprēķināts drukātajam rēķinam.

![Pielikuma jauktais numurs.](media/attach-hash-num.jpg)

