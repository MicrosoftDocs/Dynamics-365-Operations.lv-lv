---
title: PVN maksājumi un noapaļošanas kārtulas
description: Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā.
author: kailiang
ms.date: 10/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: kfend
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c24a9850543e9d08ee1726186f433c7cfd26608
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865688"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>PVN maksājumi un noapaļošanas kārtulas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā.

Periodiski ir jāziņo par PVN un tas ir jāsamaksā nodokļu iestādēm. Šo darbību var pabeigt, palaižot procesu Nosegt un grāmatot PVN lapā **PVN**. Noteikta perioda PVN tiek nosegts no PVN kontiem, un PVN apmaksas kontā tiek grāmatota PVN bilance. PVN apmaksas kontā grāmatoto PVN bilanci var noapaļot atbilstoši nodokļu iestāžu prasībām, iestatot noapaļošanas kārtulu lapā **PVN**. 

Noapaļošanas starpība tiek grāmatota PVN noapaļošanas kontā, kas ir atlasīts virsgrāmatas laukā Automātisko darījumu konti.

Tālāk sniegtajā piemērā ir attēlots, kā darbojas noapaļošanas kārtula nodokļu iestādei.

## <a name="examples"></a>Piemēri

Kopējā PVN summa par periodu atbilst kredīta bilancei –98 765,43. Juridiskā persona ir saņēmusi lielāku PVN summu, nekā tā ir samaksājusi. Tāpēc juridiskā persona ir parādā nodokļu iestādei. 

Juridiskā persona vēlas izmantot noapaļošanas metodi, kas noapaļo bilanci līdz tuvākajam veselam skaitlim (1,00). Lietotājs, kurš ir atbildīgs par PVN uzskaiti, veic tālāk norādītās darbības.

1. Noklikšķiniet uz **Nodokļi** > **Netiešie nodokļi** > **PVN** > **Nodokļu iestādes**.
2. Kopsavilkuma cilnes **Vispārīgi** laukā **Noapaļošanas veids** atlasiet opciju **Parastais**.
3. Laukā **Noapaļošana** ievadiet vērtību 1,00.
4. Kad ir pienācis laiks maksāt PVN nodokļu iestādei, dodieties uz **Nodokļi** > **Deklarācijas** > **PVN** > **Nosegt un grāmatot PVN**. PVN apmaksas kontā jūs redzēsiet nodokļu parāda summa **98 765,43** tiek noapaļota līdz **98 765**.

Tālāk esošajā tabulā ir parādīts, kā summa 98 765,43 tiek noapaļota, izmantojot katru noapaļošanas metodi, kas ir pieejama lapas **Nodokļu iestādes** laukā **Noapaļošanas veids**.

> [!NOTE]                                                                                  
> Ja noapaļošanas vērtība ir iestatīta kā 0,00, tad:
>
> - Normālai noapaļošanai uzvedība ir tāda pati kā **Noapaļošana = 0,01**.
> - Opcijām **Noapaļošanas veida opcijas**, **Uz zemāku**, **Noapaļošana** un **Pašu priekšrocība** uzvedība ir tāda pati kā **Noapaļošana = 1,00**.

| Noapaļošanas veida opcija                | Noapaļošanas vērtība = 0,01 | Noapaļošanas vērtība = 0,10 | Noapaļošanas vērtība = 1,00 | Noapaļošanas vērtība = 100,00 | Noapaļošanas vērtība = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Parasta                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Uz zemāku                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Noapaļošana                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Pašu priekšrocība kredīta bilancei | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Pašu priekšrocība debeta bilancei  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Normāla noapaļošana, un noapaļošanas precizitāte ir 0,01

```<table>
  <tr>
    <td>Rounding
    </td>
    <td>Calculation process
    </td>
  </tr>
    <tr>
    <td>round(1.015, 0.01) = 1.02
    </td>
    <td>
      <ol>
        <li>round(1.015 / 0.01, 0) = round(101.5, 0) = 102
        </li>
        <li>102 * 0.01 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.014, 0.01) = 1.01
    </td>
    <td> <ol>
        <li>round(1.014 / 0.01, 0) = round(101.4, 0) = 101
        </li>
        <li>101 * 0.01 = 1.01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.011, 0.02) = 1.02
    </td>
    <td> <ol>
        <li>round(1.011 / 0.02, 0) = round(50.55, 0) = 51
        </li>
        <li>51 * 0.02 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.009, 0.02) = 1.00
    </td>
    <td> <ol>
        <li>round(1.009 / 0.02, 0) = round(50.45, 0) = 50
        </li>
        <li>50 * 0.02 = 1.00
        </li>
      </ol>
    </td>
  </tr>
</table>
```

> [!NOTE]                                                                                  
> Ja atlasāt opciju Pašu priekšrocība, noapaļošana vienmēr tiek veikta atbilstoši juridiskās personas interesēm. 

Lai iegūtu papildu informāciju, skatiet šādas tēmas:
- [PVN apskats](indirect-taxes-overview.md)
- [PVN maksājuma izveide](tasks/create-sales-tax-payment.md)
- [PVN transakciju izveide dokumentos](tasks/create-sales-tax-transactions-documents.md)
- [Grāmatoto PVN transakciju skatīšana](tasks/view-posted-sales-tax-transactions.md)
- [noapaļošanas funkcija](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
