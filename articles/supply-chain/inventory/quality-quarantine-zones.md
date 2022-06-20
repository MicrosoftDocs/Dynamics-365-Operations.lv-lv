---
title: Karantīnas zonas neatbilstībai
description: Šajā rakstā ir aprakstīts, kā izveidot un izmantot karantīnas zonas neatbilstībai.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e556d2aa078a76ff4f81b6763535c38ce1cca0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857726"
---
# <a name="quarantine-zones-for-nonconformances"></a>Karantīnas zonas neatbilstībai

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot un izmantot karantīnas zonas neatbilstībai.

Izmantojiet lapu **Karantīnas zonas**, lai definētu zonas, ko var piešķirt neatbilstībām. Kad jūs izveidojat neatbilstību, jūs variet iestatīt laukus **Karantīnas zona** un **Karantīnas veids** cilnē **Vispārīgi** lapā **Neatbilstības**. Lauks **Karantīnas zona** parasti norāda apgabalu vai vietu, kur atrodas krājums. Lauks **Karantīnas veids** nosaka, vai krājums ir *Ierobežotas lietošanas* vai *Nav derīgs*.

Kad tiek drukāta neatbilstība vai labojumu pārskats par neatbilstību, varat apskatīt karantīnas zonu, kurā atrodas krājums.

Varat arī drukāt neatbilstības tagu neatbilstībai. Šis pārskats rāda piešķirto karantīnas zonu un informāciju par lietojumu, lai sniegtu norādījumus par to, kā jārīkojas ar bojātu materiālu. Karantīnas zonas var atbilst krājumu vietām vai operāciju resursiem.

## <a name="examples-of-quarantine-zones"></a>Karantīnas zonu piemēri

### <a name="example-1"></a>1. piemērs

Jūs strādājat elektronikas ražošanas uzņēmumā, kas ražo un izplata televizorus, skaļruņus un multivides atskaņotājus. Šajā gadījumā karantīnas zonu var konfigurēt, lai attēlotu katru produkta veidu.

### <a name="example-2"></a>2. piemērs

Trīs nodalījumi un divi statīvi tiek izmantoti, lai uzglabātu neatbilstošas preces. Šajā gadījumā var konfigurēt piecas karantīnas zonas – pa vienai katram nodalījumam un katram statīvam.

## <a name="create-a-quarantine-zone"></a>Izveidojiet karantīnas zonu

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Karantīnas zonas**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Karantīnas zona** – ievadiet karantīnas zonas unikālo ID vai nosaukumu.
    - **Apraksts** — ievadiet karantīnas zonas detālizēto aprakstu.

1. Aizvērt lapu.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības pārskats](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Par neatbilstību apstiprināšanu atbildīgie darbinieki](quality-responsible-workers.md)
- [Neatbilstību problēmu tipi](quality-quarantine-zones.md)
- [Neatbilstību diagnostikas tipi](quality-diagnostic-types.md)
- [Kvalitātes maksa par neatbilstībām](quality-charges.md)
- [Operācijas neatbilstībai](quality-operations.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
