---
title: Importa un eksporta nodokļa aprēķini
description: Šajā tēmā sniegta informācija par nodokļu aprēķināšanas pakalpojuma importa un eksporta funkcionalitāti.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 76ea99510455e984d94a93d87ee788fdcf00c376
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891361"
---
# <a name="import-and-export-tax-calculations"></a>Importa un eksporta nodokļa aprēķini

Šajā tēmā sniegta informācija par nodokļu aprēķināšanas pakalpojuma importa un eksporta funkcionalitāti. Šī funkcionalitāte palīdz nodrošināt elastīgu un efektīvu konfigurācijas pieredzi.

## <a name="import-and-export-tax-codes"></a>Importa un eksporta nodokļu kodi

### <a name="export-templates"></a>Veidņu eksports

1. Piesakieties [regulēšanas konfigurācijas pakalpojumā (RCS)](https://marketing.configure.global.dynamics.com/).
2. Darbvietā **Globalizācijas** līdzekļi atlasiet Līdzekļi un pēc tam atlasiet elementu **Nodokļu** **aprēķins**.
3. Atlasiet esošu līdzekli vai [izveidojiet jaunu](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) līdzekli.
4. Režģī **Versijas** atlasiet **Rediģēt**.
5. Lapā **Nodokļu aprēķina** līdzeklis iestatiet konfigurācijas [versiju](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Cilnē **Nodokļu kodi** atlasiet **Importēt**.
7. Atlasiet **Nodokļu koda veidnes eksportu, lai** lejupielādētu **TaxCodesTemplate.zip** failu.
8. Unzip **TaxCodesTemplate.zip.** Nodokļu kodu veidnes tiek saspiestas atsevišķi atbilstoši Aprēķina **izcelsmes** vērtībai.
9. Izarhivēt **pēc Neto summas.zip,** lai iegūtu šādus ar komatu atdalītu vērtību (CSV) failus:

    - **TaxCode.csv** – ievadiet nodokļa kodus.
    - **TaxLimit.csv** – ievadiet nodokļa ierobežojumus katram nodokļa kodam.
    - **TaxRate.csv** – ievadiet nodokļa likmes katram nodokļa kodam.

> [!NOTE]
> Pēc noklusējuma nodokļu koda **parauga ieraksti ir pieejami** veidnēs. Ja **parauga** nodokļa kods netiek noņemts no CSV failiem, tas tiks importēts līdzeklī.

### <a name="import-tax-codes"></a>Importa nodokļu kodi

Izpildiet šīs **darbības, lai** importētu parauga nodokļu kodu veidnē nodokļu aprēķināšanas līdzeklī.

1. RCS nodokļu aprēķina **līdzekļa** lapā nodokļu **kodu cilnē** atlasiet **Importēt**.
2. Atlasiet **Pārlūkot**, atrast un atlasīt failu TaxCode.csv un pēc **tam** laukā Mērķa tabula **atlasiet** **Nodokļa** kodu.
3. Atlasiet **Ok,** lai importētu nodokļa kodu.
4. Atrodiet un atlasiet **failu TaxRate.csv** un pēc tam laukā Mērķa tabula **atlasiet Nodokļu** **likme**.
5. Atlasiet **Labi,** lai importētu nodokļa likmi.
6. Atrodiet un atlasiet **failu TaxLimit.csv** un pēc tam laukā Mērķa tabula atlasiet **Nodokļu** **ierobežojums**.
7. Atlasiet **Labi,** lai importētu nodokļa limitu.

Jūs varat arī tieši importēt zip failu, kas ietver visus trīs CSV failus. Šādā veidā varat ātri un viegli pabeigt importu.

1. RCS nodokļu aprēķina **līdzekļa** lapā nodokļu **kodu cilnē** atlasiet **Importēt**.
2. Atlasiet **Pārlūkot**, atrodiet un atlasiet **failu Pēc neto summas.zip** un pēc tam atlasiet **Labi**.

### <a name="export-tax-codes"></a>Eksporta nodokļu kodi

1. RCS nodokļu aprēķina **līdzekļa** lapā nodokļu **kodu cilnē** atlasiet **Eksportēt**.

    Poga **Eksports** ir pieejama tad, kad nodokļu kodu režģī ir vismaz **viens nodokļu** kods.

2. Atlasiet **Labi**, lai eksportētu visus funkcionalitātes nodokļu kodus pasta failā.

> [!NOTE]
> Izmantojiet eksportēto failu kā veidni, lai importētu nodokļu kodus atbilstošajā līdzeklī.

## <a name="import-and-export-applicability-rules"></a>Importēt un eksportēt piemērojamības noteikumus

### <a name="export-applicability-rules"></a>Eksportēt piemērojamības kārtulas

1. Pierakstieties [RCS](https://marketing.configure.global.dynamics.com/).
2. Darbvietā **Globalizācijas** līdzekļi atlasiet Līdzekļi un pēc tam atlasiet elementu **Nodokļu** **aprēķins**.
3. Atlasiet esošu līdzekli vai [izveidojiet jaunu](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) līdzekli.
4. Režģī **Versijas** atlasiet **Rediģēt**.
5. Lapā **Nodokļu aprēķina** līdzeklis iestatiet konfigurācijas [versiju](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Cilnē Nodokļu **grupas** piemērojamība atlasiet rindas, kas ir sadaļā **Iestatīt nodokļu grupas piemērojamības** režģi.
7. Atlasiet pogu **Atvērt pogu Un pēc tam atlasiet nodokļu pakalpojuma Microsoft Office** **dinamiskās piemērojamības** matrica.

    [![Tiek eksportēti Microsoft Excel piemērojamības noteikumi uz nodokļu aprēķina līdzekļa lapu.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Atlasiet **Lejupielādēt**, lai eksportētu atlasītās rindas Microsoft Excel darblapā.

### <a name="import-applicability-rules"></a>Importēt piemērojamības noteikumus

Lejupielādētā Excel darblapa ietver nodokļu grupas **piemērojamības režģa** iestatīšanas struktūru. Jaunus noteikumus var pievienot tieši darblapā. Kad esat beidzis, izpildiet šīs darbības, lai importētu jaunos noteikumus atpakaļ **iestatīt nodokļu grupas piemērojamības** režģī.

1. Excel darba lapā atlasiet un kopējiet importē visas rindas.
2. RCS nodokļu aprēķina līdzekļu lapas cilnē Nodokļu grupas piemērojamība atlasiet Pievienot, lai ievietotu tukšu ierakstu režģa Iestatīt nodokļu **grupu** **·** **·** **piemērojamību** apakšā.
3. Atlasiet **Ctrl+V,** lai ielīmētu režģī kopētās rindas.
4. Atlasiet **Saglabāt**.