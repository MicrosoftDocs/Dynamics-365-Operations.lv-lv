---
title: Nodokļu aprēķina noapaļošanas kārtulas
description: Šajā tēmā sniegta informācija par noapaļošanas noteikumiem nodokļu aprēķināšanas pakalpojuma nodokļu aprēķina parametros.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 167db4d836aa754509bb28677916a30901cebbbb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694179"
---
# <a name="tax-calculation-rounding-rules"></a>Nodokļu aprēķina noapaļošanas kārtulas

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegta informācija par noapaļošanas noteikumiem nodokļu aprēķināšanas pakalpojuma nodokļu aprēķina parametros.

> [!NOTE] 
> Ja nodokļu aprēķina pakalpojums ir iespējots, noapaļošanas noteikumi lapās **PVN kods** un **PVN grupa** nav spēkā.

Varat skatīt noapaļošanas kārtulu konfigurāciju nodokļu aprēķina pakalpojumiem sadaļā **PVN noapaļošanas kārtula** kopsavilkuma cilnē **Aprēķins** cilnes **Vispārīgi** lapā **Nodokļu aprēķina parametri** (**Nodokļi** \> **Iestatījumi** \> **Nodokļu konfigurācija** \> **Nodokļu aprēķina parametri**).

[![Noapaļošanas noteikumu konfigurācija Nodokļu aprēķina parametru lapā](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

Lauki **Noapaļošanas precizitāte** un **Noapaļošanas metode** nosaka, kā tiek noapaļotas aprēķinātās summas lietderīgajā slodze no nodokļu aprēķināšanas pakalpojuma.

## <a name="rounding-precision"></a>Noapaļošanas precizitāte

**Noapaļošanas precizitātes** lauki atbalsta vērtību, kas aiz komata ir līdz sešām decimālzīmēm. Piemēram, ja jūs **iestatāt** **Noapaļošanas precizitātes lauku 0.000000**, Microsoft Dynamics aprēķinātās summas tiek noapaļotas līdz sešām decimālzīmēm un pēc tam nosūtītas uz 365 Finansēm. Piemēram, ja tiek lietota **Parastā** noapaļošanas metode, summa **987,1234567** tiek noapaļota uz **987,123457**.

> [!NOTE]
> Finanšu noapaļošanas summas atbilstoši valūtas noapaļošanas kārtulām. Tāpēc nodokļu summas, kas tiek rādītas un ierakstītas darbībās, ietekmē gan nodokļu aprēķina noapaļošanas noteikumi, gan valūtas noapaļošanas noteikumi.

## <a name="rounding-method"></a>Noapaļošanas metode

Noapaļošanas metodi nodokļu aprēķināšanai var konfigurēt katrai juridiskajai personai. Laukā **Noapaļošanas metode** varat atlasīt no trim opcijām: **Parasta**, **Lejupvērsta** un **Noapaļošana**.

### <a name="rounding-example"></a>Noapaļošanas piemērs

Šajā tabulā sniegts piemērs, kā tiek noapaļota summa **987,345** dažādām precizitātes un noapaļošanas metožu kombinācijām.

<table>
<thead>
<tr>
<th rowspan="2">Noapaļošanas metode</th>
<th colspan="8">Noapaļošanas precizitāte</th>
</tr>
<tr>
<th>0.00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10,00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Parasta</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Uz zemāku</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Noapaļošana</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Nodokļu summu aprēķināšanas un noapaļošanas loģiku var konfigurēt atbilstoši taksācijas noteikumiem.

## <a name="rounding-by"></a>Noapaļošana uz 

Laukā **Noapaļot pēc** atlasiet noapaļošanas principu, kuru lieto nodokļiem. Pieejamas šādas opcijas:

- **Nodokļu kodi** – noapaļot nodokļa summu katram nodokļa kodam.
- **Nodokļu kodu kombinācijas** – noapaļot nodokļa summu rindas nodokļu kodu kombinācijā.

## <a name="calculation-method"></a>Aprēķina metode

Laukā **Aprēķina metode** atlasiet, vai rēķinos nodokļi tiek aprēķināti katrai rindai vai visām rindām. Pieejamas šādas opcijas:

- **Rinda** - aprēķina nodokļa summu, pamatojoties uz rindu. Katras rindas nodokļa summu neietekmē citu rindu nodokļa summa.
- **Kopsumma** – aprēķiniet nodokļa summu visām viena dokumenta rindām.

### <a name="rounding-calculation-example"></a>Noapaļošanas aprēķina piemērs

Šajā piemērā ir norādīti dažādi aprēķini, kurus var veikt vienam rēķinam dažādām **Noapaļot pēc** un **Aprēķina metodes** vērtību kombinācijām. Šajā piemērā ir spēkā šāds iestatījums:

- Rēķinam ir četras rindas.
- Ir divi nodokļu kodi: **PVN1** (10 procenti) un **PVN2** (10 procenti).
- Noapaļošanas precizitāte ir iestatīta uz **0,01**.
- Noapaļošanas metode ir iestatīta uz **Noapaļošana**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Noapaļošana pēc = Nodokļu kodi un Aprēķina metode = Rinda

| Rindas numurs | Rindas neto summa | Noteikti nodokļu kodi | Nodokļa summa pirms noapaļošanas | Noapaļotā nodokļa apmērs |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11,11           | PVN1                 | 1,111                      | 1,12               |
| 2           | 22,22           | PVN1; PVN2           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33,33           | PVN1                 | 3,333                      | 3,34               |
| 4           | 44,44           | PVN1; PVN2           | 4,444; 4;444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Noapaļošana pēc = Nodokļu kodu kombinācijas un Aprēķina metode = Rinda

| Rindas numurs | Rindas neto summa | Noteikti nodokļu kodi | Nodokļa summa pirms noapaļošanas | Noapaļotā nodokļa apmērs |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11,11           | PVN1                 | 1,111                      | 1,12               |
| 2\*         | 22,22           | PVN1; PVN2           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33,33           | PVN1                 | 3,333                      | 3,34               |
| 4\*\*       | 44,44           | PVN1; PVN2           | 4,444; 4;444               | 4,45; 4,44         |

\*2. rinda = Noapaļot\[22,22 × (10 procenti + 10 procenti) \] = 2,23 + 2,22

\*\* 4. rinda = Noapaļot\[44,44 × (10 procenti + 10 procenti)\]  = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Noapaļošana pēc = Nodokļu kodi un Aprēķina metode = Kopsumma

| Rindas numurs | Rindas neto summa | Noteikti nodokļu kodi | Nodokļa summa pirms noapaļošanas | Noapaļotā nodokļa apmērs |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11,11           | PVN1\*               | 1,111                      | 1,12               |
| 2           | 22,22           | PVN1\*; PVN2\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33,33           | PVN1\*               | 3,333                      | 3,33               |
| 4           | 44,44           | PVN1\*; PVN2\*\*     | 4,444; 4;444               | 4,44; 4,44         |

\*PVN1(1. rinda, 2. rinda, 3. rinda, 4. rinda) = Noapaļot\[(11,11 + 22,22 + 33,33 + 44,44) × 10 procenti\] = 1,12 + 2,22 + 3,33 + 4,44

\*\* PVN2 (2. rinda, 4. rinda) = Noapaļot\[ (22,22 + 44,44) × 10 procenti\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Noapaļot pēc = Nodokļu kodu kombinācijas un Aprēķina metode = Kopsumma

| Rindas numurs | Rindas neto summa | Noteikti nodokļu kodi | Nodokļa summa pirms noapaļošanas | Noapaļotā nodokļa apmērs |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11,11           | PVN1                 | 1,111                      | 1,12               |
| 2\*\*       | 22,22           | PVN1; PVN2           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33,33           | PVN1                 | 3,333                      | 3,33               |
| 4\*\*       | 44,44           | PVN1; PVN2           | 4,444; 4;444               | 4,44; 4,45         |

\* 1. rinda, 3. rinda = Noapaļot\[(11,11 + 33,33) × 10 procenti\] = 1,12 + 3,33

\*\* 2. rinda, 4. rinda = Noapaļot\[(22,22 + 44,44) × (10 procenti + 10 procenti)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
