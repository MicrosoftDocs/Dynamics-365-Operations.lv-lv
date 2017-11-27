---
title: "PVN likmju aprēķins, pamatojoties uz laukiem Aprēķina pamatā un Aprēķina metode"
description: "Šajā tēmā ir paskaidrots, kā laukos Aprēķina pamatā un Aprēķina metode norādītās vērtības nosaka nodokļu likmes pārdošanas un pirkšanas transakcijās."
author: twheeloc
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf0f8f2e3f553ea181e8cc9ab5b712fce64a89d4
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>PVN likmju aprēķins, pamatojoties uz laukiem Aprēķina pamatā un Aprēķina metode

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā laukos Aprēķina pamatā un Aprēķina metode norādītās vērtības nosaka nodokļu likmes pārdošanas un pirkšanas transakcijās.

Lauks Aprēķina pamatā, kurš atrodas lapas Pārdošanas nodokļa kodi kopsavilkuma cilnē Aprēķins, nosaka, kura summa tiek izmantota atbilstošo nodokļu likmju atlasīšanai no likmēm lapā Pārdošanas nodokļa kodu vērtības. Summas tips laukā Aprēķina pamatā kopā ar metodi laukā Aprēķina metode nosaka loģiku transakcijas pareizo nodokļu likmju atrašanai. 

Dažādas vērtību kombinācijas šajos laukos rada ļoti dažādus PVN aprēķinus, kā parādīts turpmākajos piemēros. Piemēros tiek izmantoti tādas pašas nodokļu intervālu vērtības, kādas ir iestatītas katram nodokļu kodam lapā Pārdošanas nodokļa kodu vērtības. Lai atvērtu šo lapu, lapā PVN kodi noklikšķiniet uz PVN kods &gt; Vērtības.

> [!Important]                                                                                                                  
> Ja vērtība Aprēķina pamatā vienā vai vairākos pārdošanas nodokļa kodos ir balstīta uz rindu summām vai vienībām, tad lauka Aprēķina metode vērtība lapā Virsgrāmatas parametri ir jāiestata uz Rinda. |

## <a name="net-amount-per-line"></a> Neto summa rindai
Atlasiet šo opciju, lai pārdošanas nodokļa likmes noteiktu, pamatojoties uz neto summu rēķina rindām, izslēdzot pārējos nodokļus.

### <a name="example"></a>Paraugs

Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.

| Summas intervāls    | Nodokļa likme |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100–0 (&gt;100) | 10%      |

> [!NOTE]                                                                                                             
> Augšējā robeža nulle (0) pēdējā intervālā nozīmē, ka visas summas, kas pārsniedz 100, tiek iekļautas intervālā.

Aprēķina pamatā: **Neto summa rindai** 

Aprēķina metode: **Intervāls** 

Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā. 

Rēķina rindas neto summa ir 200,00. 

Nodokli aprēķina šādi: 

PVN kopsumma = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35,00 

Rēķina kopsumma = 200,00 + 35,00 = 235,00 

**Novirze** 

Ja rēķinā ir divas rindas ar četrām precēm katrā rindā, katras rindas neto summa ir 100,00 un PVN tiek aprēķināts tālāk norādītajā veidā. 

1. rindas PVN = 50 x 30% + 50 x 20% = 15 + 10 = 25,00 

2. rindas PVN = 50 x 30% + 50 x 20% = 15 + 10 = 25,00 

PVN kopsumma = 25,00 + 25,00 = 50,00 

Rēķina kopsumma = 200,00 + 50,00 = 250,00

## <a name="net-amount-per-unit"></a> Neto summa uz vienību
Atlasiet šo opciju, lai noteiktu pārdošanas nodokļa likmes, pamatojoties uz katras vienības vērtību, izslēdzot pārējos nodokļus. Ja ir atlasīta no vienības atkarīga vērtība Aprēķina pamatā, tad Pārdošanas nodokļa kodam ir jānorāda arī Vienība.

### <a name="example"></a>Paraugs

Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.

| Summa             | Nodokļa likme |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100–0 (&gt;100) | 10%      |

Aprēķina pamatā: **Neto summa uz vienību** 

Aprēķina metode: **Pilna summa** 

Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā. 

Rēķina rindas neto summa ir 200,00. 

Nodoklis tiek aprēķināts šādi: Pārdošanas nodoklis uz vienību = 25,00 x 30% = 7,50 Kopējais pārdošanas nodoklis = 7,50 x 8 vienības = 60,00 Rēķina kopsumma = 200,00 + 60,00 = 260,00

## <a name="net-amount-of-invoice-balance"></a> Rēķina bilances neto summa

Atlasiet šo opciju, lai pārdošanas nodokļa likmes noteiktu, pamatojoties uz rēķina kopējo vērtību, izslēdzot pārējos nodokļus.

### <a name="example"></a>Paraugs

Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.

| Summa            | Nodokļa likme |
|-------------------|----------|
| 0 - 50            | 30%      |
| 50 - 100          | 20%      |
| 100–0 (&gt;100) | 10%      |

Aprēķina pamatā: **Rēķina bilances neto summa** 

Aprēķina metode: **Intervāls** Pārdošanas rēķinā ir 2 rindas, un katrā rindā ir 4 lampas par 25,00 katra. Rēķina bilances neto summa ir 4 x 25,00 + 4 x 25,00 = 200,00. Nodoklis tiek aprēķināts šādi: Kopējais pārdošanas nodoklis = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Rēķina kopsumma = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a> Bruto summa uz rindu

Atlasiet šo opciju, lai pārdošanas nodokļa likmes noteiktu, pamatojoties uz rindas vērtību, ietverot visus pārējos nodokļus attiecīgajai rindai.

> [!NOTE]
> Pārdošanas nodokļu grupā var būt tikai viens pārdošanas nodokļa kods ar šādu atlasi laukā Aprēķina pamatā.

### <a name="example"></a>Paraugs

Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.

| Summa             | Nodokļa likme |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100–0 (&gt;100) | 10%      |

Aprēķina pamatā: **Bruto summa pa rindām**. Aprēķina metode: **Intervāls**. Papildus ir aprēķināts vēl viens nodokļa kods speciālam nodoklim 5,00 apmērā par katru lampu. Nodokli pievieno neto summai pirms PVN aprēķina. Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā. Rēķina rindas neto summa ir 200,00. Rēķina rindas bruto summa ir 8 x 25,00 + 8 x 5,00 = 240,00. Nodoklis tiek aprēķināts šādi: Kopējais pārdošanas nodoklis = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Kopējais nodoklis = 5,00 x 8 = 40,00 Rēķina kopsumma = 200,00 + 39,00 + 40,00 = 279,00

**Novirze** 

Ja rēķins tiek izveidots, izmantojot 2 rēķina rindas ar 4 precēm katrā, rēķina rindas neto summa ir 100,00. Bruto summa (iekļaujot nodokli 4 x 5,00) uz rēķina rindu būtu 120,00, un pārdošanas nodoklis tiek izveidots šādi: 1. pārdošanas nodokļa rēķina rinda = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 2. pārdošanas nodokļa rēķina rinda = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Kopējais pārdošanas nodoklis = 27,00 + 27,00 = 54,00 Kopējais nodoklis = 5,00 x 8 = 40,00 Rēķina kopsumma = 200,00 + 54,00 + 40,00 = 294,00

## <a name="gross-amount-per-unit"></a> Bruto summa uz vienību

Atlasiet šo opciju, lai noteiktu pārdošanas nodokļa likmes, pamatojoties uz vienības vērtību, ietverot pārējos nodokļus.

> [!NOTE]
> Pārdošanas nodokļu grupā var būt tikai viens pārdošanas nodokļa kods ar šādu atlasi laukā Aprēķina pamatā.

### <a name="example"></a>Paraugs

Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.

| Summa             | Nodokļa likme |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100–0 (&gt;100) | 10%      |

Aprēķina pamatā: **Bruto summa uz vienību** Pastāv speciāls nodoklis 5,00 par katru lampu. Nodokli pievieno neto summai pirms PVN aprēķina. Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā. Vienības bruto summa ir 30,00. Nodoklis tiek aprēķināts šādi: Pārdošanas nodoklis uz vienību = 30 x 30% = 9,00 Kopējais pārdošanas nodoklis = 9,00 x 8 = 72,00 Kopējais nodoklis = 5,00 x 8 = 40,00 Rēķina kopsumma = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> Rēķina kopsumma, iesk. pārējās pārdošanas nodokļa summas

Atlasiet šo opciju, lai pārdošanas nodokļa likmes noteiktu, pamatojoties uz rēķina kopējo vērtību, iekļaujot pārējos nodokļus.
> [!NOTE]
> Ja ir atlasīta šī lauka Aprēķina pamatā vērtība, PVN grupā var ietvert tikai vienu PVN kodu

### <a name="example"></a>Paraugs

Pārdošanas nodokļa likmes tiek iestatītas tālāk norādītajiem intervāliem.

| Summa             | Nodokļa likme |
|--------------------|----------|
| 0 - 50             | 30%      |
| 50 - 100           | 20%      |
| 100–0 (&gt;100) | 10%      |

Aprēķina pamatā: **Rēķina kopsumma, iesk. citas PVN summas** Aprēķina metode: **Intervāls**   
Katra lampa ir aplikta ar īpašu nodokli 5,00. Nodokli pievieno neto summai pirms PVN aprēķina. Jūs iegādājaties 8 lampas, kas maksā 25,00/gabalā. Rēķina neto summa ir 200,00. Rēķina bruto summa ir 200,00 + (8 x 5,00) = 240,00. Nodoklis tiek aprēķināts šādi: Kopējais pārdošanas nodoklis = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Kopējais nodoklis = 5,00 x 8 = 40,00 Rēķina kopsumma = 200,00 + 39,00 + 40,00 = 279,00

Papildinformāciju skatiet tēmās [PVN kodu visas summas un intervāla aprēķināšanas opcijas](whole-amount-interval-options-sales-tax-codes.md) un [PVN aprēķina metodes laukā Izcelsme](sales-tax-calculation-methods-origin-field.md).




