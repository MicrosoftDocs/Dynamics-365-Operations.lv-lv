---
title: Līdzekļu nomas līgumi
description: Šajā tēmā ir aprakstīti līgumi iznomātajiem līdzekļiem.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67c4d2b7162cf6bda2eedfecef43ff0b216e6e6c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881812"
---
# <a name="asset-leasing-conventions"></a>Līdzekļu nomas līgumi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir aprakstīti līgumi iznomātajiem līdzekļiem. Nomas līgumi tiek izmantoti, lai noteiktu nomas grāmatas sākuma datumu. Ja nomas līgums ir iestatīts uz **Nav**, sākuma datums ir tāds pats kā nomas sākuma datums (t.i., **Nomas sākuma datuma** lauka vērtība). Ja nomas līgums ir iestatīts uz **Pilnu mēnesi**, sākuma datums ir mēneša pirmā diena, kurā beidzas nomas sākuma datums.

Sākuma datums nosaka perioda sākuma datumu saistību amortizācijas un līdzekļu nolietojuma grafikiem. Procentu izdevumi un nolietojuma izdevumi tiek grāmatoti atbilstošo grafiku perioda beigu datumā. Sākotnējais atzīšanas un korekciju žurnāla ieraksts tiek grāmatots sākuma datumā.

> [!NOTE]
> Nomas līgumu līdzekli nav iespējams ieslēgt, izmantojot Līdzekļu pārvaldību. **Līdzekļu pārvaldības** darbvietā atrodiet un atlasiet līdzekli ar nosaukumu **Nomas līgums līdzekļa iznomāšanai**, un pēc tam atlasiet **Iespējot tūlīt**.

Nomas līgumi ir piešķirti nomas līdzekļu grāmatas iestatījumiem.

Lai skatītu vai piešķirtu nomas līgumu, izpildiet šīs darbības.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grāmatas**.
2. Laukā **Nomas līgums** atlasiet vienu no šīm vērtībām.

    | Nomas līgums | Apraksts |
    |--------------------|-------------|
    | None               | Saistību norakstīšanas un līdzekļu nolietojuma grafiki sākas nomas sākuma datumā, jo sākuma datums ir vienāds ar nomas sākuma datumu. Beigu datums ir vienu mēnesi vēlāk. Šis nomas līgums negarantē, ka procenti tiks grāmatoti katra mēneša pēdējā dienā. |
    | Pilns mēnesis         | Nomām, kurām ir sākuma datums, kas ir jebkurā mēneša datumā, saistību norakstīšanas un līdzekļu nolietojuma grafiki sāk uzkrāt izdevumus šī mēneša pirmajā dienā. Šis nomas līgums nodrošina, ka procenti tiek uzkrāti katra mēneša pēdējā dienā par visu mēnesi. |

3. Atlasiet **Saglabāt**.

Izveidojot nomu, katras grāmatas sākuma datums tiek automātiski ievadīts, pamatojoties uz nomas sākuma datumu un uz nomas līgumu, kas norādīts grāmatai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
