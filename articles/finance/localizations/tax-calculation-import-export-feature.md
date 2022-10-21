---
title: Importa un eksporta nodokļu aprēķini
description: Šajā rakstā ir sniegta informācija par nodokļu aprēķināšanas pakalpojuma importa un eksporta funkcionalitāti.
author: Kai-Cloud
ms.date: 10/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690238"
---
# <a name="import-and-export-tax-calculations"></a>Importa un eksporta nodokļu aprēķini

Šajā rakstā ir sniegta informācija par nodokļu aprēķināšanas pakalpojuma importa un eksporta funkcionalitāti. Šī funkcionalitāte palīdz nodrošināt elastīgu un efektīvu konfigurācijas pieredzi.

## <a name="import-and-export-tax-codes"></a>Importa un eksporta nodokļu kodi

### <a name="export-templates"></a>Veidņu eksports

1. Piesakieties regulēšanas [konfigurācijas pakalpojumā (RCS)](https://marketing.configure.global.dynamics.com/).
2. Darbvietā **Globalizācijas** līdzekļi atlasiet Līdzekļi **un** pēc tam atlasiet elementu **Nodokļu** aprēķins.
3. Atlasiet esošu līdzekli vai [izveidojiet jaunu līdzekli](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Režģī **Versijas** atlasiet **Rediģēt**.
5. **Lapā Nodokļu aprēķina** līdzeklis iestatiet konfigurācijas [versiju](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. **Cilnē Nodokļu kodi** atlasiet **Importēt**.
7. Atlasiet **Nodokļu koda veidnes eksportu,** lai lejupielādētu **TaxCodesTemplate.zip** failu.
8. Unzip **TaxCodesTemplate.zip**. Nodokļu kodu veidnes tiek saspiestas atsevišķi atbilstoši Aprēķina izcelsmes **vērtībai**.
9. Izarhivēt **pēc Neto summas.zip,** lai iegūtu šādus ar komatu atdalītu vērtību (CSV) failus:

    - **TaxCode.csv** – ievadiet nodokļa kodus.
    - **TaxLimit.csv** – ievadiet nodokļa ierobežojumus katram nodokļa kodam.
    - **TaxRate.csv** – ievadiet nodokļa likmes katram nodokļa kodam.

> [!NOTE]
> Pēc noklusējuma nodokļu koda **parauga** ieraksti ir pieejami veidnēs. Ja parauga **nodokļa** kods netiek noņemts no CSV failiem, tas tiks importēts līdzeklī.

### <a name="import-tax-codes"></a>Importa nodokļu kodi

Izpildiet šīs darbības, lai **importētu** parauga nodokļu kodu veidnē nodokļu aprēķināšanas līdzeklī.

1. RCS nodokļu aprēķina **līdzekļa** lapā nodokļu **kodu cilnē** atlasiet **Importēt**.
2. Atlasiet **Pārlūkot**, atrast un atlasīt **failu TaxCode.csv** un pēc tam laukā **Mērķa tabula** atlasiet **Nodokļa kodu**.
3. Atlasiet **Ok,** lai importētu nodokļa kodu.
4. Atrodiet un atlasiet failu **TaxRate.csv** un pēc tam laukā **Mērķa tabula** atlasiet Nodokļu **likme**.
5. Atlasiet **Labi,** lai importētu nodokļa likmi.
6. Atrodiet un atlasiet failu **TaxLimit.csv** un pēc tam laukā Mērķa **tabula** atlasiet Nodokļu **ierobežojums**.
7. Atlasiet **Labi,** lai importētu nodokļa limitu.

Jūs varat arī tieši importēt zip failu, kas ietver visus trīs CSV failus. Šādā veidā varat ātri un viegli pabeigt importu.

1. RCS nodokļu aprēķina **līdzekļa** lapā nodokļu **kodu cilnē** atlasiet **Importēt**.
2. Atlasiet **Pārlūkot**, atrodiet un atlasiet failu **Pēc neto summas.zip** un pēc tam atlasiet **Labi**.

### <a name="export-tax-codes"></a>Eksporta nodokļu kodi

1. RCS nodokļu aprēķina **līdzekļa** lapā nodokļu **kodu cilnē** atlasiet **Eksportēt**.

    Poga **Eksports** ir pieejama tad, kad nodokļu kodu režģī ir vismaz viens **nodokļu** kods.

2. Atlasiet **Labi**, lai eksportētu visus funkcionalitātes nodokļu kodus pasta failā.

> [!NOTE]
> Izmantojiet eksportēto failu kā veidni, lai importētu nodokļu kodus atbilstošajā līdzeklī.

## <a name="import-and-export-applicability-rules"></a>Importēt un eksportēt piemērojamības noteikumus

### <a name="export-applicability-rules"></a>Eksportēt piemērojamības kārtulas

1. Pierakstieties [RCS](https://marketing.configure.global.dynamics.com/).
2. Darbvietā **Globalizācijas** līdzekļi atlasiet Līdzekļi **un** pēc tam atlasiet elementu **Nodokļu** aprēķins.
3. Atlasiet esošu līdzekli vai [izveidojiet jaunu līdzekli](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Režģī **Versijas** atlasiet **Rediģēt**.
5. **Lapā Nodokļu aprēķina** līdzeklis iestatiet konfigurācijas [versiju](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Cilnē Nodokļu **grupas piemērojamība** atlasiet rindas, kas ir sadaļā Iestatīt **nodokļu grupas piemērojamības režģi**.
7. Atlasiet pogu Atvērt **pogu Un Microsoft Office** pēc tam atlasiet nodokļu pakalpojuma dinamiskās **piemērojamības matrica**.

    [![Tiek eksportēti piemērojamības Microsoft Excel noteikumi uz nodokļu aprēķina līdzekļa lapu.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Atlasiet **Lejupielādēt,** lai eksportētu atlasītās rindas darblapā Microsoft Excel.

### <a name="import-applicability-rules"></a>Importēt piemērojamības noteikumus

Lejupielādētā Excel darblapa ietver nodokļu grupas piemērojamības **režģa iestatīšanas** struktūru. Jaunus noteikumus var pievienot tieši darblapā. Kad esat beidzis, izpildiet šīs darbības, lai importētu jaunos noteikumus atpakaļ **iestatīt nodokļu grupas piemērojamības** režģī.

1. Excel darba lapā atlasiet un kopējiet importē visas rindas.
2. RCS nodokļu **aprēķina** **līdzekļu** lapas cilnē Nodokļu grupas piemērojamība atlasiet Pievienot, **·** **lai ievietotu tukšu ierakstu režģa Iestatīt nodokļu grupu piemērojamību apakšā.**
3. Atlasiet **Ctrl+V**, lai ielīmētu režģī kopētās rindas.
4. Atlasiet **Saglabāt**.

## <a name="import-feature-demo-data"></a>Importēt līdzekļu demonstrācijas datus

Sekojiet šiem soļiem, lai importētu līdzekļu demonstrācijas datus.

1. Pierakstieties [RCS](https://marketing.configure.global.dynamics.com/).
2. Darbvietā **Globalizācijas** līdzekļi atlasiet Līdzekļi **un** pēc tam atlasiet elementu **Nodokļu** aprēķins.
3. Atlasiet **Importēt** un pēc tam lapā Importēt no **globālā repozitorija** atlasiet **Sinhronizēt**. 
4. Tabulā atlasiet nodokļu aprēķina funkcijas-demonstrācijas **datu** funkciju un pēc tam atlasiet **Importēt**.
5. Atlasiet **Skatīt**, lai pārskatītu importētā līdzekļa definētos nodokļu kodus, grupas un piemērojamības noteikumus.
6. Finansēs pārejiet uz LEGALF juridisko **personu un pēc tam dodieties uz nodokļu iestatījumu** **·**\> nodokļa **·**\> konfigurācijas **nodokļa**\> aprēķina parametriem.**·**
7. Cilnē Vispārīgi **atlasiet** Iespējot nodokļu **aprēķināšanas pakalpojumu**.
8. Līdzekļa **iestatījuma** nosaukuma laukā **atlasiet nodokļu aprēķina funkciju-demonstrācijas datus**.
9. Atlasiet apmaksas **periodu un** Virsgrāmatas grāmatošanas **grupu jaunajiem** demonstrācijas nodokļu kodiem un pēc tam atlasiet **Apstiprināt**.
10. Atlasiet **Saglabāt**.

> [!NOTE]
> Nodokļu **aprēķina funkciju-demonstrācijas datu demonstrācijas** **funkcija ir balstīta uz funkcionalitātes versijas versiju 40.54.234** **un izveidotaZĒF** demonstrācijas juridiskajai personai. Pārliecinieties, ka Finanses un RCS ir jauninātas uz versiju 10.0.26 vai jaunāku versiju.
