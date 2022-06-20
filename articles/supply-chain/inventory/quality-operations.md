---
title: Operācijas neatbilstībai
description: Šajā rakstā ir aprakstīts, kā izveidot un izmantot neatbilstības operācijas.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2e63156dd2b230da7f1ea89e2c2006c1b4f3eeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847996"
---
# <a name="operations-for-nonconformances"></a>Operācijas neatbilstībai

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot un izmantot neatbilstības operācijas.

Var izmantot lapu **Operācijas**, lai definētu klasifikācijas darbam, ko var veikt apstiprinātajai neatbilstībai. Ja neatbilstībai piešķirat saistīto operāciju, varat nodrošināt detalizētu informāciju, piemēram, par saistīto materiālu, darba stundām un maksām, kas nepieciešamas operācijas izpildē. Sistēma izmanto šo informāciju, lai operācijai aprēķinātu novērtētās izmaksas. Detalizētā informācija un novērtētās izmaksas tiek nodrošinātas tikai atsauces nolūkā. Kvalitātes saistītās operācijas ir atšķirīgas no operācijām, ko var definēt ražošanas maršrutā.

> [!NOTE]
> Lai gan jūs varat izsekot izmaksas, laiku un krājumus, kas tiek izmantoti operācijā, kas saistīta ar neatbilstību, jūsu ievadītie dati ir tikai informatīvi. Tas nav automātiski integrēts ar Virsgrāmatu, krājumu apakšgrāmatu vai moduli **Laiks un apmeklētība**.

## <a name="examples-of-operations"></a>Operāciju piemēri

Jūs strādājat ražošanas uzņēmumā. Krājumiem, kam neizdevās kvalitātes tests, tika izveidota un apstiprināta neatbilstība. Labojums tika izveidots, lai norādītu, ka problēma tika saistīta ar slikto gultni iekārtā. Lai nomainītu gultni, nepieciešamas vairākas darbības, un tiek izsekota atbildība par katru operāciju. Piemēram, var būt nepieciešamas šādas darbības:

1. Ražošanas rinda tiek apturēta, un tiek veikta tīrīšanas rutīna.
1. Uzturēšanas personāls nomaina gultni.
1. Kvalitātes nodrošināšanas personāls pārbauda iekārtu, pirms tā tiek atkal ieslēgta.

Šajā piemērā var veidot šādas operācijas, lai attēlotu darbu, kas jāveic:

- Apturēt ražošanas rindu.
- Iztīrīt ražošanas rindu.
- Veikt iekārtas uzturēšanu.
- Pārbaudīt iekārtu.

## <a name="create-an-operation"></a>Operācijas izveide

1. Dodieties uz **Krājumu vadība \> Iestatīšana \> Kvalitātes pārvaldība \> Operācijas**.
1. Lai režģim pievienotu rindu, darbību rūtī atlasiet **Jauns**. Jaunajā rindā iestatiet šādus laukus:

    - **Operācija** - ievadiet operācijas unikālo ID vai nosaukumu.
    - **Apraksts** — ievadiet operācijas detālizēto aprakstu.
    - **Tips**– Ja operāciju var izmantot tikai ar neatbilstībām, kas attiecas uz noteiktu pasūtījuma tipu, atlasiet pasūtījuma tipu (*Pirkšanas pasūtījums* vai *Pārdošanas pasūtījums*).

1. Aizvērt lapu.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības pārskats](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Neatbilstības izveide un apstrāde](tasks/create-process-non-conformance.md)
- [Par neatbilstību apstiprināšanu atbildīgie darbinieki](quality-responsible-workers.md)
- [Karantīnas zonas neatbilstībai](quality-quarantine-zones.md)
- [Neatbilstību diagnostikas tipi](quality-diagnostic-types.md)
- [Kvalitātes maksa par neatbilstībām](quality-charges.md)
- [Neatbilstību problēmu tipi](quality-operations.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
