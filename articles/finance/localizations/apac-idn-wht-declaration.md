---
title: Ieturētā nodokļa pārskats Indonēzijai
description: Šajā rakstā ir izskaidrots, kā konfigurēt un ģenerēt ieturētā nodokļa pārskatu Indonēzijai.
author: AdamTrukawka
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.search.scope: ''
ms.openlocfilehash: 732db563532ebc46c7b9fc69c2aaa128640084f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282441"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Ieturētā nodokļa pārskats Indonēzijai (ID-00005)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt un ģenerēt PPH ieturētā nodokļa failu, ko juridiskas personas, kas atrodas Indonēzijas, izmantojiet, lai ziņotu par ieturamajām darbībām e-Bupot programmā.

Indonēzijas nodokļu iestāde (DGT) nosaka, ka ar nodokli apliekamie krājumi (PKP), kas ir reģistrēti KPP Papildmaksā kā ienākumu nodokļa (PPh) īpašnieka/apkopotāja 23. un/vai 26. rakstu, elektroniski jāsniedz pārskats par ienākumu nodokļa atgriešanas 23. un 26. rakstu, izmantojot e-Bupot pieteikumu. 

- **23. dokuments** – pārskats ietver visas ieturētās darbības no kreditoriem, kur primārās adreses valsts/reģiona kods ir Indonēzijas kods.
- **26. dokuments** – pārskatā ir iekļautas visas ieturētās darbības no kreditoriem, kuru primārās adreses valsts/reģiona kods nav Indonēzijas kods.

## <a name="prerequisites"></a>Priekšnosacījumi

- Juridiskās personas primārajai adresei ir jābūt Indonēzija.
- Līdzekļu pārvaldības **darbvietā** jābūt iespējotai globālā **ieturētā** nodokļa līdzeklim. Papildinformāciju par līdzekļu iespējošanu skatiet rakstā [Pārskats par līdzekļu pārvaldību.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="download-electronic-reporting-configurations"></a>Elektronisko atskaišu veidošanas konfigurāciju lejupielāde

Importa faila izveides pamatā ir elektronisko pārskatu (ER) konfigurācijas. Papildinformāciju par konfigurējamām pārskata iespējām un koncepcijām skatiet sadaļā [Elektronisko pārskatu sniegšana](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Ražošanas un lietotāju pieņemšanas testēšanas (UAT) vidēs izpildiet instrukcijas, [kas atrodas Lejupielādes elektronisko pārskatu konfigurācijās no programmatūrai Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Lai ģenerētu importa failu, no repozitorija augšupielādējiet šādas konfigurācijas:

- **Nodokļu deklarācijas model.version.93.xml** vai jaunāka versija
- **Nodokļu deklarācijas modeļa mapping.version.93.153.xml** vai jaunāka versija
- **Kādas ir cenas shēmas imports (ID).version.93.14** vai jaunāka versija

## <a name="set-up-general-ledger-parameters"></a>Virsgrāmatas parametru iestatīšana

1. Dodieties uz **nodokļu** \> **iestatījumu** \> **virsgrāmatas parametriem.**
2. Cilnes Ieturētais **nodoklis** laukā Ko deklarācijas **formāta kartēšana** atlasiet **Kādas PPh shēmas imports (ID)**. 
3. Lai **iestatītu** \> **·** \> **·** \> **·** **Kode Bukti Potpotences** ieturētā nodokļa ieņēmumu tipu, dodieties uz nodokļu iestatījumu Ieturētā nodokļa ieturamā nodokļa ieņēmumu tipiem un pēc tam piešķiriet kodus saistītajām krājumu ieturētā nodokļa grupām. Kodi ir nepieciešami, lai izveidotu integrācijas failu, izmantojot e-Bupot programmu. 

## <a name="generate-the-withholding-import-file"></a>Ģenerēt ieturamo importa failu

E-Bupot faila sagatavošanas un ģenerēšanas process noteiktam periodam ir balstīts uz ieturētā nodokļa darbībām, kas tika grāmatotas apmaksas vai grāmatošanas nodokļa darba laikā.

Lai ģenerētu failu, sekojiet šiem soļiem.

1. Doties uz **nodokļu** \> **deklarāciju ieturamā** \> **·** \> **nodokļa PPH importa faila e-bupot 23 un 26.**
2. Atlasiet pārskata datumu "no" un "līdz" un pēc tam atlasiet apmaksas periodu.
3. Ievadiet darbības datumu un pēc tam atlasiet **Labi**.
4. Atlasiet valodu. Visi pārskati ir tulkoti ASV angļu (**lv-us) un** Indonēzijas (**ID**).
5. Atlasiet biznesa veidu un pēc tam ievadiet čeku un dokumentu numurus. 
6. Pārbaudiet, vai pārskatu ir parakstījis vadītājs. Šī informācija tiek ziņota failā. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
