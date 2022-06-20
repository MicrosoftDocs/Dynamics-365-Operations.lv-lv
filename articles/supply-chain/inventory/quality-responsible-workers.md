---
title: Par neatbilstību apstiprināšanu atbildīgie darbinieki
description: Šajā rakstā ir aprakstīts, kā konfigurēt darbiniekus, kas ir atbildīgi par neatbilstību apstiprināšanu.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a108fc1f8954e32719c93656a64d1d27fda03fb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907411"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Par neatbilstību apstiprināšanu atbildīgie darbinieki

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt darbiniekus, kas ir atbildīgi par neatbilstību apstiprināšanu.

Neatbilstības ir jāapstiprina, pirms lietotāji var sākt ievadīt tādu detalizētu informāciju kā labojumi vai operācijas. Pirms lietotāji var apstiprināt vai noraidīt neatbilstības, viņu lietotāja ID (lietotāja ierakstam) jābūt saistītam ar darbinieka ierakstu. Pēc izvēles varat konfigurēt darbiniekus, kuri ir atbildīgi par kvalitāti, un pēc tam vienam darbiniekam ļaut apstiprināt darbu cita darbinieka vārdā.

## <a name="enable-a-user-for-nonconformance-processing"></a>Iespējojiet lietotājam neatbilstību apstrādi

Pirms lietotājs var apstiprināt vai noraidīt neatbilstības, viņu lietotāja ieraksts ir jāsaista ar darbinieka ierakstu. Apstiprinājuma laukus pēc tam var iestatīt automātiski, un pašreizējo lietotāju var automātiski aizpildīt darba laika uzskaites tabulā. Lai lietotājs varētu izmantot dokumenta piezīmes, jums jāaktivizē dokumentu apstrāde lietotāja opcijās.

1. Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.
1. Atrodiet un atveriet lietotāju, kuram jābūt iespējai apstiprināt vai noraidīt neatbilstības.
1. Laukā **Persona** iestatiet darbinieka vārdu, kas ir saistīts ar pašreizējo lietotāja ierakstu.
1. Darbību rūtī atlasiet **Lietotāja opcijas**.
1. Pašreizējā lietotāja ieraksta lapā **Opcijas** cilnē **Preferences** iestatiet opciju **Iespējot dokumentu apstrādi** uz *Jā*.
1. Aizveriet lapas.

## <a name="define-workers-that-are-responsible-for-quality"></a>Definēt par kvalitāti atbildīgos darbiniekus

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Kvalitātes kontrole \> Par kvalitāti atbildīgie darbinieki**.
2. Darbību rūtī atlasiet **Jauns**.
3. Laukā **Darbinieks** atlasiet darbinieku, kas ievada kvalitātes datus.
4. Laukā **Atbildīgais darbinieks** atlasiet darbinieku, kura vārdā atlasītais darbinieks ievada darbu. Kad neatbilstības ir izveidotas un atjauninātas, darbinieks laukos **Darbinieks** tiks ievadīts pēc noklusējuma.

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības pārskats](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Kvalitātes papildmaksas](quality-charges.md)
- [Karantīnas zonas neatbilstībai](quality-quarantine-zones.md)
- [Neatbilstību diagnostikas tipi](quality-diagnostic-types.md)
- [Kvalitātes maksa par neatbilstībām](quality-charges.md)
- [Operācijas neatbilstībai](quality-operations.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
