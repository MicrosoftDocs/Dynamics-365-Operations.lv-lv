---
title: Iestatīt nodokļu kodus
description: Šajā tēmā skaidrots, kā iestatīt nodokļu kodus nodokļu aprēķinu pakalpojumā.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 8bdb194e7d8b704d1e58d3c25bf2e1f6bff1ba00
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883907"
---
# <a name="set-up-tax-codes"></a>Iestatīt nodokļu kodus

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt nodokļu kodus nodokļu aprēķina pakalpojumā. Tajā ir iekļauts vienkārša scenārija iestatījums, lai nodokļu kods darbotos un informācija par daļu no papildu nodokļu koda funkcionalitātes sarežģītiem scenārijiem.

> [!IMPORTANT]
> Nodokļu kodu iestatījums nodokļu aprēķinu pakalpojumā ir juridiska persona – diagnostika. Šo iestatījumu varat pabeigt regulēšanas konfigurācijas pakalpojumā (RCS) tikai vienu reizi. Nodokļu kodi tiek automātiski sinhronizēti korporācijai Dynamics 365 Finance Microsoft, iespējojot nodokļu aprēķina pakalpojumu atlasītai juridiskajai personai finansēs.

## <a name="simple-setup"></a>Vienkāršs iestatījums

Izpildiet šīs darbības, lai izmantotu nodokļu kodu vienkāršā scenārijā, piemēram, scenārijā, kur ir tikai viena nodokļu likme.

1. Piesakieties [regulēšanas konfigurācijas pakalpojumā](https://marketing.configure.global.dynamics.com/).
2. Doties uz **darbvietām** \> **globalizācijas līdzekļu** \> **nodokļu** aprēķins.
3. Izvēlieties līdzekli un versiju, ko vēlaties iestatīt, un izvēlieties **Rediģēt**.
4. Cilnē **Vispārīgi** atlasiet **Konfigurācijas** versija.
5. Cilnē **Nodokļu kodi** atlasiet **Pievienot** un ievadiet nodokļa kodu un aprakstu.
6. Atlasiet **Aprēķina izcelsmi**. Aprēķina izcelsme ir metožu grupa, kas definēta atlasītajā nodokļu konfigurācijas versijā. Šim vienkāršam scenārijam atlasiet **Pēc neto summas**.
7. Atlasiet **Saglabāt**. Vairāk lauku kļūst pieejami, balstoties uz atlasīto aprēķina izcelsmi.
8. Kopsavilkuma cilnē **Likmes** atlasiet Pievienot, lai šim nodokļu **kodam** pievienotu vienu nodokļu likmi.
9. Atlasiet **Saglabāt**.

## <a name="calculation-origin"></a>Aprēķina izcelsme

Aprēķina izcelsme nosaka, kā tiek aprēķināta nodokļa pamatsumma un nodokļa summa. To konfigurē elektronisko pārskatu darbvietas **nodokļu** konfigurācija. Laukā Aprēķina izcelsme ir pieejamas **šādas** vērtības:

- Pēc neto summas
- Pēc bruto summas
- Pēc daudzuma
- Pēc rezerves
- Nodoklis no nodokļa

### <a name="by-net-amount"></a>Pēc neto summas

Ja atlasāt Pēc neto summas laukā Aprēķina izcelsme, nodokļu summa tiek aprēķināta kā pirkšanas vai pārdošanas summas procenti, izņemot **·** **jebkurus** citus nodokļu kodus.

Piemēram, nodokļa likme ir 25 procenti, rēķina rinda rāda daudzumu 10 krājumiem katrā par 1,00, un debitoram ir atļauta 10 procentu rindas atlaide. Šajā gadījumā summas tiek aprēķinātas šādi:

- **Neto summa:** (10 × 1,00) – 10 procenti = 9,00 
- **PVN:** 9,00 × 25 procenti = 2,25 
- **Rēķina kopsumma:** 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Pēc bruto summas

Ja **atlasāt Pēc bruto** summas **laukā** Aprēķina izcelsme, nodokļa summa tiek aprēķināta kā bruto pārdošanas summas procenti. Bruto summa ir rindas neto summa plus visi nodokļi un maksas rindai, izņemot vienu nodokli, kur Aprēķina izcelsmes lauks ir iestatīts **uz** Bruto **summu**.

Piemēram, nodokļu iestāde krājumu ir piemērojusi speciāliem nodokļiem. Nodokļu summas tiek pievienotas neto summai pirms nodokļa aprēķina. Tiek izmantoti šādi nodokļu kodi:

- **1**. nodoklis – likme ir 10 procenti, un tiek izmantota metode Pēc neto **summas**.
- **2**. nodoklis – likme ir 20 procenti, un tiek izmantota metode Pēc neto **summas**.
- **Nodokļa** likme – likme ir 25 procenti, un tiek izmantota metode Pēc bruto **summas**.

Ja neto summa ir 10,00, 1. nodokļa summa ir 1.00 (10.00 × 10 procenti), un 2. nodokļa summa ir 2.00 (10.00 × 20 procentiem). Šajā gadījumā summas tiek aprēķinātas šādi: 

- **Bruto summa: neto summa + 1. nodokļa summa + 2. nodokļa summa** = 10,00 + 1,00 + 2,00 = 13,00 
- **Nodokļa summa:** 13,00 × 25 procenti = 3,25 
- **Kopējie nodokļi un nodoklis:** 1,00 + 2,00 + 3,25 = 6,25 
- **Rēķina kopsumma:** 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Pēc daudzuma

Ja atlasāt Pēc daudzuma laukā Aprēķina izcelsme, nodokļu summa tiek aprēķināta kā fiksēta summa uz vienu vienību un reizināta ar daudzumu, kas **ir** **ievadīts** dokumenta rindā. Summa uz vienību ir norādīta kopsavilkuma **cilnē** Likmes.

Piemēram, nodokļa kods uz vienību ir iestatīts kā 1,20. Pārdošanas rēķina rindā tiek pārdotas 25 krājuma vienības. Šajā gadījumā nodokļa summa tiek aprēķināta kā 25 × 1,20 = 30,00.

### <a name="by-margin"></a>Pēc rezerves

Ja **atlasāt Pēc** seguma summas **laukā Aprēķina** izcelsme, nodokļa summa tiek aprēķināta kā pārdošanas rezerves procenti. Pārdošanas uzcenojums ir pārdošanas summa mīnus izmaksu summa. Šī aprēķina metode tiek piemērota tikai pārdošanas darbībām.

Piemēram, nodokļa likme ir 25 procenti, rēķina rinda rāda daudzumu 10 krājumiem par 10,00 katrs un krājuma izmaksas ir 6. Šajā gadījumā summas tiek aprēķinātas šādi:

- **Pārdošanas peļņa:** 10 × ( 10,00 – 6,00) = 40,00
- **Nodokļa summa:** 40,00 × 25 procenti = 10,00
- **Kopējā rēķina summa:** 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Nodoklis no nodokļa

Ja **atlasāt Nodokli no nodokļa laukā Aprēķina izcelsme, PVN tiek aprēķināts kā visu pārējo nodokļu summu procenti tajā** **pašā dokumenta** rindā.

Piemēram, tiek izmantoti šādi nodokļu kodi:

- **1**. nodoklis – likme ir 10 procenti, un tiek izmantota metode Pēc neto **summas**.
- **2**. nodoklis – likme ir 20 procenti, un tiek izmantota metode Pēc neto **summas**.
- **Nodoklis no** nodokļa – likme ir 25 procenti, un tiek **izmantota nodokļu aprēķina** metode.

Šajā gadījumā summas tiek aprēķinātas šādi:

- **Neto summa:** 10,00 
- **1. nodoklis:** 10,00 × 10 procenti = 1,00 
- **2. nodoklis:** 10,00 × 20 procenti = 2,00 
- **Nodoklis par nodokli:** 3,00 × 25 procenti = 0,75
- **Kopējais nodoklis:** 1,00 + 2,00 + 0,75 = 3,75 
- **Rēķina kopsumma:** 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Papildu funkcionalitāte

Šī sadaļa izskaidro daļu no nodokļu koda iestatījuma papildu funkcionalitātes sarežģītiem scenārijiem.

### <a name="tax-exemption"></a>Nodokļu atbrīvojums

Ja iestatāt opciju Neapliekams kopsavilkuma cilnē Vispārīgi, nodokļa summa vienmēr tiks ignorēta uz 0 (nulle), neskatoties uz **faktisko** **·** **nodokļa** likmi.

Lauku **Neapliekams** kods var iestatīt, lai norādītu atbrīvojuma iemeslu. 

Varat aktivizēt galveno datu meklēšanu **neapliekamā koda** laukam. Tādā veidā var izvēlēties no neapliekamām kodu vērtībām, kas definētas Finansēs. Papildinformāciju par to, kā iespējot pamatdatu uzmeklēšanu, skatiet sadaļā Galveno [datu uzmeklēšanas iespējošana nodokļu aprēķina konfigurācijā.](tax-service-set-up-environment-master-data-lookup.md)

Piemēram, nodokļa likme ir 25 procenti, un opcija Ir neapliekams nodokļa kodā tiek **iestatīta** uz **Jā**. Rēķina rindā parādītas 10 preces par katru 1,00, un debitoram ir atļauta 10 procentu rindas atlaide. Šajā gadījumā summas tiek aprēķinātas šādi:

- **Neto summa:** (10 × 1,00) – 10 procenti = 9,00 
- **PVN:** 0,00 
- **Rēķina kopsumma:** 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Importa nodoklis

Ja iestatāt opciju Izmantot nodokli kopsavilkuma cilnē Vispārīgi, nodokļu summa tiek grāmatota kreditora kopsavilkuma konta vietā kontā Izmantot **nodokli** **·** **·** **·** **kreditoriem**.

Piemēram, nodokļa likme ir 25 procenti, un opcija Vai izmantot nodokli nodokļa kodam **ir** iestatīta uz **Jā**. Rēķina rindā parādītas 10 preces par katru 1,00, un debitoram ir atļauta 10 procentu rindas atlaide. Šajā gadījumā summas tiek aprēķinātas šādi:

- **Neto summa:** (10 × 1,00) – 10 procenti = 9,00 
- **Izmantotais nodoklis:** 9,00 × 25 procenti = 2,25
- **Rēķina kopsumma:** 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Ja gan opcija Ir neapliekama, gan opcija Vai izmantot nodokli nodokļa nodokļa kodam ir iestatīta uz Jā, kods tiks atpazīts kā ar nodokli neapliekams pārdošanas darbībām un kā pirkšanas **darbībām** **·** **lietots** nodoklis.

### <a name="reverse-charges"></a>Apgrieztās maksas

Ja iestatāt opciju Ir atgrieztā maksa uz Jā kopsavilkuma **cilnē** **·** **Vispārīgi**, nodokļu likmi var konfigurēt kā negatīvu. Apgrieztās maksas scenārijam ir ieteicams iestatīt divus nodokļu kodus: vienu ar pozitīvu nodokļu likmi un vienu ar negatīvu nodokļa likmi. Abiem nodokļu kodiem ir jābūt vienādai likmes vērtībai, un nodokļa kodam ar negatīvu nodokļa likmi ir jāiestata opcija **Ir** **atgriezes** maksa. Papildinformāciju par atgrieztās maksas risinājumu programmā Finance skatiet [Apgrieztās maksas mehānisms PVN/GST shēmai](emea-reverse-charge.md).

Piemēram, vienā rēķina rindā tiek noteikti divi nodokļu kodi. Viena nodokļa likme ir 25 procenti. Otra nodokļu likme ir -25 procenti, un opcija Ir apgrieztā maksa otrajā nodokļa kodā **ir** iestatīta uz **Jā**. Rēķina rindā parādītas 10 vienības par summu 1,00 katra. Šajā gadījumā summas tiek aprēķinātas šādi:

- **Neto summa:** (10 × 1,00) = 10,00 
- **1. nodokļa** kods: 10,00 × 25 procenti = 2,50
- **2. nodokļa kods:** 10 × -25 procenti = -2,50
- **Kopējā rēķina summa:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Izslēgšana no pamatsummas aprēķiniem

Ja iestatāt opciju Izslēgt no pamatsummas aprēķina kopsavilkuma cilnē Vispārīgi, nodokļu koda aprēķinātā nodokļu summa tiek izslēgta no nodokļu pamatsummas citiem nodokļu kodu aprēķiniem **cenu** **·** **ietveršanas** scenārijā.

Papildinformāciju skatiet sadaļā [Aprēķināt nodokļus cenām, kad cenās ir iekļauti](global-exclude-from-tax-base-amount-calculation.md) nodokļi.

### <a name="rates"></a>Likmes

Kopsavilkuma **cilnē** Likme varat definēt dažādas nodokļu likmes dažādiem nodokļu pamatsummu diapazoniem. Lai aprēķinātu nodokļa summu, nodokļu aprēķināšanas pakalpojums vienmēr izmanto likmi, kas atbilst nodokļu bāzes summai.

Piemēram, nodokļu likmes var konfigurēt tā, kā parādīts šajā tabulā.

| Minimālā summa | Maksimālais apjoms | Nodokļa likme   |
| -------------- | -------------- | ---------- |
| 0              | 1000          | 10 procenti |
| 1000          | 5000          | 15 procenti |
| 5000          | 10,000         | 20 procenti |
| 10,000         | 0              | 30 procenti |

Šajā gadījumā nodokļa summa tiek aprēķināta šādi:

- Ja nodokļa pamatsumma ir 300,00, nodokļa likme ir 10 procenti un nodokļa summa ir 300,00 × 10 procenti = 30,00.
- Ja nodokļa pamatsumma ir 3000,00, nodokļa likme ir 15 procenti un nodokļa summa ir 3000,00 × 15 procenti = 450,00.
- Ja nodokļa pamatsumma ir 6000,00, nodokļa likme ir 20 procenti un nodokļa summa ir 6000,00 × 10 procenti = 1200,00.
- Ja nodokļa pamatsumma ir 20,000.00, nodokļa likme ir 30 procenti, un nodokļa summa ir 20,000.00 × 30 procenti = 6000,00.

> [!NOTE]
> Ja nodokļu bāzes summa var atbilst gan maksimālajai summai vienā rindā, gan minimālajai summai citā rindā, tad bāzē tiks izmantota nodokļu likme, kas atbilst minimālajai pamatsummas summai. Piemēram, ja nodokļa pamatsumma ir 1000,00, nodokļa likme ir 15 procenti un nodokļa summa ir 1000,00 × 15 procenti = 150,00.

### <a name="limits"></a>Ierobežojumi

Kopsavilkuma cilnē Ierobežojumi varat definēt nodokļu ierobežojumus, lai ignorētu aprēķināto nodokļa summu, ja nodokļa **summa** krīt minimālo/maksimālo diapazonu.

- Ja aprēķinātā nodokļa summa ir lielāka par vai vienāda ar maksimālo nodokļu summu, kas ir konfigurēta kopsavilkuma cilnē Ierobežojumi, galīgā nodokļa summa ir vienāda ar **maksimālo** nodokļa summu.
- Ja aprēķinātā nodokļa summa ir mazāka par minimālo nodokļu summu, kas ir konfigurēta kopsavilkuma cilnē Ierobežojumi, galīgā nodokļa summa **ir** 0 (nulle).

Piemēram, nodokļu ierobežojumi tiek konfigurēti šādā veidā:

- **Minimālā nodokļa summa:** 100 
- **Maksimālā nodokļa summa:** 1000

Ja aprēķinātā nodokļa summa ir 2000, galīgā nodokļa summa ir 1000.

Ja aprēķinātā nodokļa summa ir 500, galīgā nodokļa summa ir 500.

Ja aprēķinātā nodokļa summa ir 80, galīgā nodokļa summa ir 0 (nulle).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
