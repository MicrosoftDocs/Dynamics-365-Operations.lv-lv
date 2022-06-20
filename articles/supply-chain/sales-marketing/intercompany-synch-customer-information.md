---
title: Sinhronizēt starpuzņēmumu debitora informāciju
description: Šajā rakstā skaidrots debitoru informācijas sinhronizācija starpuzņēmumu pasūtījumiem
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a3a67c9bcf93f88375d2d4d78d87175200626d50
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897521"
---
# <a name="synchronize-intercompany-customer-information"></a>Sinhronizēt starpuzņēmumu debitora informāciju

[!include [banner](../../includes/banner.md)]

Debitora informācija tiek sinhronizēta, ja lauks **Debitoru informācija** ir aktivizēts, veidojot pārdošanas pasūtījumu vai veicot izmaiņas debitora, kreditora atsauces vai debitora pieprasījuma numuram.

Vērtību šajos sinhronizācijas laukos vienmēr var mainīt. Tomēr, atlasot šo parametru, var noteikt, vai šī vērtība tiek kopēta uz citiem starpuzņēmumu pasūtījumiem. Ja starpuzņēmuma pārdošanas pasūtījumā aktivizēts lauks **Debitoru informācija**, izmaiņas starpuzņēmuma pārdošanas pasūtījumā tiek sinhronizētas uz starpuzņēmumu pirkšanas pasūtījumu. Ja starpuzņēmumu pirkšanas pasūtījumā aktivizēts arī lauks **Debitoru informācija**, tas tiek sinhronizēts arī atpakaļ uz oriģinālo pārdošanas pasūtījumu.

> [!NOTE]
> Ja lauks **Debitoru informācija** ir aktivizēts gan starpuzņēmumu pirkšanas pasūtījumā, gan starpuzņēmumu pārdošanas pasūtījumā, vienas personas veiktie atjauninājumi vienā uzņēmumā tiek noraidīti ar atjauninājumiem, ko tajā pašā pasūtījumā veikusi cita persona citā uzņēmumā.

Vislabākā prakse ir aktivizēt lauku **Debitora informācija** starpuzņēmumu pirkšanas pasūtījumā. Tas aktivizē sinhronizāciju starp oriģinālo pārdošanas pasūtījumu un starpuzņēmumu pirkšanas pasūtījumu un no starpuzņēmumu pirkšanas pasūtījuma uz starpuzņēmumu pārdošanas pasūtījumu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
