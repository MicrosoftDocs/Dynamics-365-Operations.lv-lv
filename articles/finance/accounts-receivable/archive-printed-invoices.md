---
title: Izdrukātie debitoru rēķini ar jaukšanas numuriem — arhivēšana
description: Šajā rakstā ir aprakstīts, kā iespējot arhivēšanu, lai saglabātu drukātos debitoru rēķinus ar jaukšanas numuriem.
author: ilkond
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3f19968b4f4cf76a48ac5485e915785e9be5c7db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909190"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Izdrukātie debitoru rēķini ar jaukšanas numuriem — arhivēšana

[!include [banner](../includes/banner.md)]

Dažās valstīs pastāv tiesiska prasība glabāt aprēķinātos jauktos numurus sistēmā kopā ar dažu dokumentu izdrukām. Jauktos numurus var izmantot, lai ziņotu iestādēm, un auditu laikā.

Šajā rakstā skaidrots, kā konfigurēt arhivēšanu, lai saglabātu drukātos debitoru rēķinus ar jaukšanas numuriem.

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

