---
title: Krājumu vērtības pārskatu piemēri un loģika
description: Šajā rakstā sniegti daži rezultātu piemēri, kas parādīti katram krājumu vērtības pārskata tipam. Krājumu vērtību pārskati sniedz detalizētu informāciju par jūsu krājumu fiziskajiem un finanšu daudzumiem un summām.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e6c6387be5204fde6ebc7a4983567801900974af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877658"
---
# <a name="inventory-value-report-examples-and-logic"></a>Krājumu vērtības pārskatu piemēri un loģika

[!include [banner](../includes/banner.md)]

Krājumu vērtību pārskati sniedz detalizētu informāciju par jūsu krājumu fiziskajiem un finanšu daudzumiem un summām. Šajā rakstā sniegti daži rezultātu piemēri, kas parādīti katram krājumu vērtības pārskata tipam.

Papildinformāciju par to, kā ģenerēt un izmantot katru krājumu vērtības pārskata tipu, skatiet krājumu [vērtību pārskatos](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Šajos piemēros izmantotie parauga dati

Šī raksta piemēri ir balstīti uz krājumu darījumu parauga datiem, kas ir aprakstīti šajā sadaļā.

### <a name="storage-dimension-setup"></a>Noliktavas dimensiju iestatīšana

Piemēra sistēmā ir ietverti šādi glabāšanas dimensiju iestatījumi.

| Vārds/nosaukums | Aktīva | Fizisks krājums | Finanšu krājumi |
|---|---|---|---|
| Vietne | Jā | Jā | Jā |
| Noliktava | Jā | Jā | Nē |

### <a name="inventory-model"></a>Krājumu modelis

Piemēram, sistēma krājumu modelis izlaistajām *precēm ir FIFO*, **un** izmaksu cenas lauks krājumu modelim tiek iestatīts uz *Iekļaut fizisko vērtību*.

### <a name="inventory-transactions"></a>Krājumu darbības

Piemēram, sistēma satur šādas krājumu darbības izlaistai precei ar krājuma numuru *B0001*.

| Atsauce | Vietne | Noliktava | Saņemšana | Problēma | Fiziskais datums | Finansiālais datums | Daudzums | Izmaksu summa | Fiziskā izmaksu summa |
|---|---|---|---|---|---|---|---|---|---|
| Pirkšanas pasūtījums | 1 | 11. | Nopirkts | | 15. marts | 15. marts | 10. | 1000 | 1000 |
| Pirkšanas pasūtījums | 2 | 21 | Nopirkts | | 15. marts | 15. marts | 10. | 2,000 | 2,000 |
| Pirkšanas pasūtījums | 1 | 11. | Saņemts | | 15. aprīlis | | 5 | | 375 |
| Pārsūtīšanas pasūtījums | 1 | 11. | | Pārdots | 2. maijs | 2. maijs | -5 | -458,33 | -458,33 |
| Pārsūtīšanas pasūtījums | 1 | 12. | Nopirkts | | 2. maijs | 2. maijs | 5 | 458.33 | 458.33 |
| Pārdošanas pasūtījums | 1 | 12. | | Pārdots | 3. maijs | 3. maijs | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Krājumu vērtības pārskata konfigurācija

Piemēram sistēma ietver krājumu vērtības pārskata konfigurāciju, kas satur šādus iestatījumus:

- **Diapazons: grāmatošanas** *datums*
- **Krājumi:** *Jā*
- **Aprēķināt vidējās vienības izmaksas:** *Jā*
- **Kopējais daudzums un vērtība:** *Jā*
- **Vieta, skats:** *Atlasīts*
- **Resursa ID, skats:** *Jā*
- **Līmenis:** *kopsummas*

## <a name="inventory-value-report-example-1"></a>Krājumu vērtības pārskata 1. piemērs

Šajā tabulā un ilustrācijās ir attēloti rezultāti, kas iegūti, izmantojot parauga datus un pārskata konfigurāciju, kas ir aprakstīta iepriekš šajā rakstā.

| Resursa tips | Resurss | Vietne | Atsauce | Krājumi: finansiālais daudzums | Krājumi: finanšu summa | Krājumi: grāmatotais fiziski pieejamais daudzums | Krājumi: grāmatotā fiziski pieejamā summa | Krājumi: daudzums | Krājumi: summa | Vidējās vienības izmaksas |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiāls | B0001(s) | 1 | Beigu bilance | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Materiāls | B0001(s) | 2 | Beigu bilance | 10,00 | 2,000.00 | 0,00 | 0,00 | 10,00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Piemēram, standarta krājumu vērtības pārskats 1

Šajā attēlā parādīts standarta krājumu **vērtības pārskats,** piemēram, 1. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Krājumu vērtības pārskats, piemēram, 1.](media/inventory-value-report-ex1-small.png "Piemēram, krājumu vērtības pārskats 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Piemēram, krājumu vērtības pārskata glabāšanas pārskats

Šajā attēlā parādīts, piemēram **, 1. krājuma** vērtības pārskata glabāšanas pārskats. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Piemēram, krājumu vērtības pārskata glabāšanas pārskats 1.](media/inventory-value-report-storage-ex1-small.png "Piemēram, krājumu vērtības pārskata glabāšanas pārskats")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Krājumu vērtības pārskata 2. piemērs

Šajā tabulā un ilustrācijās ir attēloti rezultāti, kad lietojat parauga datus, kas ir aprakstīti iepriekš šajā rakstā, **·** *bet* pārskata konfigurācijā vērtību no lauka Līmenis var mainīt uz Darbības un, **·** *palaižot pārskatu, lauku No datuma iestatāt uz 15*. marts.

| Resursa tips | Resurss | Vietne | Datums | Numurs | Atsauce | Krājumi: finansiālais daudzums | Krājumi: finanšu summa | Krājumi: grāmatotais fiziski pieejamais daudzums | Krājumi: grāmatotā fiziski pieejamā summa | Krājumi: daudzums | Krājumi: summa |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiāls | B0001(s) | 1 | 3/15/2021 | 00000126 | Pirkšanas pasūtījums | 0,00 | 0,00 | 10,00 | 1,000.00 | **10,00** | **1,000.00** |
| Materiāls | B0001(s) | 1 | 3/15/2021 | 00000126 | Pirkšanas pasūtījums | 10,00 | 1,000.00 | -10,00 | -1000,00 | **0.00** | **0.00** |
| Materiāls | B0001(s) | 1 | 4/15/2021 | 00000128 | Pirkšanas pasūtījums | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Materiāls | B0001(s) | 1 | 5/2/2021 | 000003 | Pārsūtīšanas pasūtījuma nosūtīšanas p/z | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Materiāls | B0001(s) | 1 | 5/2/2021 | 000003 | Pārsūtīšanas pasūtījuma saņemšanas p/z | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiāls | B0001(s) | 1 | 5/3/2021 | 000835 | Pārdošanas pasūtījums | 0,00 | 0,00 | -1,00 | -91,67 | **-1.00** | **-91.67** |
| Materiāls | B0001(s) | 1 | 5/3/2021 | 000835 | Pārdošanas pasūtījums | -1,00 | -91,67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Materiāls | B0001(s) | 2 | 3/15/2021 | 00000127 | Pirkšanas pasūtījums | 0,00 | 0,00 | 10,00 | 2,000.00 | **10,00** | **2,000.00** |
| Materiāls | B0001(s) | 2 | 3/15/2021 | 00000127 | Pirkšanas pasūtījums | 10,00 | 2,000.00 | -10,00 | -2000,00 | **0.00** | **0.00** |
| Materiāls | B0001(s) | 2 | 5/2/2021 | 000003 | Pārsūtīšanas pasūtījuma nosūtīšanas p/z | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Materiāls | B0001(s) | 2 | 5/2/2021 | 000003 | Pārsūtīšanas pasūtījuma saņemšanas p/z | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Piemēram, standarta krājumu vērtības pārskats 2

Šajā attēlā parādīts standarta krājumu **vērtības pārskats**, piemēram, 2. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Krājumu vērtības pārskats, piemēram, 2.](media/inventory-value-report-ex2-small.png "Piemēram, 2. krājumu vērtības pārskats")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Piemēram, krājumu vērtības pārskata glabāšanas pārskats 2

Šajā attēlā parādīts, piemēram **, 2. krājuma** vērtības pārskata glabāšanas pārskats. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Piemēram, 2. krājumu vērtības pārskata glabāšanas pārskats.](media/inventory-value-report-storage-ex2-small.png "Piemēram, krājumu vērtības pārskata glabāšanas pārskats 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Krājumu vērtības pārskata 3. piemērs

Ieteicams veikt krājumu vērtību pārskatus pēc pārrēķina vai krājumu slēgšanas, lai jūs būtu darbības un summas, kuras ietekmē pārrēķināšana vai krājumu slēgšana.

Tālāk minētās apakšsadaļas parāda krājumu vērtību pārskatus, kas ģenerēti pēc krājumu slēgšanas līdz 30. maijam.

### <a name="example-3-when-the-totals-level-is-used"></a>3. piemērs, kad tiek izmantots kopsummas līmenis

Šajā tabulā ir parādīti rezultāti, izmantojot parauga datus un pārskata konfigurāciju, kas ir aprakstīta iepriekš šajā rakstā. (Šajā pārskata konfigurācijā: **Līmeņa** lauks ir iestatīts uz *Kopsummas*.)

| Resursa tips | Resurss | Vietne | Atsauce | Krājumi: finansiālais daudzums | Krājumi: finanšu summa | Krājumi: grāmatotais fiziski pieejamais daudzums | Krājumi: grāmatotā fiziski pieejamā summa | Krājumi: daudzums | Krājumi: summa | Vidējās vienības izmaksas |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiāls | B0001(s) | 1 | Beigu bilance | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Materiāls | B0001(s) | 2 | Beigu bilance | 10,00 | 2,000.00 | 0,00 | 0,00 | 10,00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>3. piemērs, kad tiek izmantots Darījumu līmenis

Šajā tabulā ir parādīti rezultāti, ja lietojat parauga datus, kas ir aprakstīti iepriekš šajā rakstā, **·** *bet* pārskata konfigurācijā maināt lauka Līmenis vērtību uz Darbības.

| Resursa tips | Resurss | Vietne | Datums | Numurs | Atsauce | Krājumi: finansiālais daudzums | Krājumi: finanšu summa | Krājumi: grāmatotais fiziski pieejamais daudzums | Krājumi: grāmatotā fiziski pieejamā summa | Krājumi: daudzums | Krājumi: summa |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiāls | B0001(s) | 1 | 3/15/2021 | 00000126 | Pirkšanas pasūtījums | 0,00 | 0,00 | 10,00 | 1,000.00 | 10,00 | 1,000.00 |
| Materiāls | B0001(s) | 1 | 3/15/2021 | 00000126 | Pirkšanas pasūtījums | 10,00 | 1,000.00 | -10,00 | -1000,00 | 0,00 | 0,00 |
| Materiāls | B0001(s) | 1 | 4/15/2021 | 00000128 | Pirkšanas pasūtījums | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Materiāls | B0001(s) | 1 | 5/2/2021 | 000003 | Pārsūtīšanas pasūtījuma nosūtīšanas p/z | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiāls | B0001(s) | 1 | 5/2/2021 | 000003 | Pārsūtīšanas pasūtījuma saņemšanas p/z | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiāls | B0001(s) | 1 | 5/3/2021 | 000835 | Pārdošanas pasūtījums | 0,00 | 0,00 | -1,00 | -91,67 | -1,00 | -91,67 |
| Materiāls | B0001(s) | 1 | 5/3/2021 | 000835 | Pārdošanas pasūtījums | -1,00 | -91,67 | 1.00 | 91.67 | 0,00 | 0,00 |
| Materiāls | B0001(s) | 1 | 5/31/2021 | 000835 | Pārdošanas pasūtījums | 0,00 | -8.33 | 0,00 | 0,00 | 0,00 | -8.33 |
| Materiāls | B0001(s) | 1 | 5/31/2021 | 000003 | Pārsūtīšanas pasūtījuma nosūtīšanas p/z | 0,00 | -41.67 | 0,00 | 0,00 | 0,00 | -41.67 |
| Materiāls | B0001(s) | 1 | 5/31/2021 | 000003 | Pārsūtīšanas pasūtījuma saņemšanas p/z | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiāls | B0001(s) | 2 | 3/15/2021 | 00000127 | Pirkšanas pasūtījums | 0,00 | 0,00 | 10,00 | 2,000.00 | 10,00 | 2,000.00 |
| Materiāls | B0001(s) | 2 | 3/15/2021 | 00000127 | Pirkšanas pasūtījums | 10,00 | 2,000.00 | -10,00 | -2000,00 | 0,00 | 0,00 |
| Materiāls | B0001(s) | 2 | 5/2/2021 | 000003 | Pārsūtīšanas pasūtījuma nosūtīšanas p/z | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Materiāls | B0001(s) | 2 | 5/2/2021 | 000003 | Pārsūtīšanas pasūtījuma saņemšanas p/z | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Materiāls | B0001(s) | 2 | 5/31/2021 | 000003 | Pārsūtīšanas pasūtījuma nosūtīšanas p/z | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Materiāls | B0001(s) | 2 | 5/31/2021 | 000003 | Pārsūtīšanas pasūtījuma saņemšanas p/z | 0,00 | -41.67 | 0,00 | 0,00 | 0,00 | -41.67 |
