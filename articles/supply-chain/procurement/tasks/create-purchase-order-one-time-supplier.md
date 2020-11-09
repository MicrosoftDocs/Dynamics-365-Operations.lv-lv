---
title: Pirkšanas pasūtījuma izveide vienreizējam piegādātājam
description: Šajā procedūrā ir parādīts, kā izveidot pirkšanas pasūtījumu vienreizējam piegādātājam.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc935b346adfe9548b024f22a2fbfb5af9a802d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018102"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Pirkšanas pasūtījuma izveide vienreizējam piegādātājam

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot pirkšanas pasūtījumu vienreizējam piegādātājam. Piegādātājs tiek automātiski izveidots ar pirkšanas pasūtījumu, nevis kreditora konts ir jāizveido manuāli. Pirkuma pasūtījumu parasti veic iepirkuma aģenti. Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF. Pastāv priekšnosacījums, kas vienreizējā kreditora kontam ir jābūt iestatītam lapā Kreditoru parametri.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Pirkšanas pasūtījuma izveide vienreizējam piegādātājam
1. Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Atlasiet Jā laukā Vienreizējs piegādātājs.
    * Kreditora konts tiek automātiski izveidots un piešķirts pirkšanas pasūtījumam. Kreditora konts tiek izveidots, pamatojoties uz veidni, kas ir norādīta kreditoru parametru lapas cilnē Vispārīgi.  
4. Laukā Nosaukums ierakstiet nosaukumu šim piegādātājam.
5. Noklikšķiniet uz OK.
    * Pirkšanas pasūtījumu tagad var pabeigt un apstrādāt tāpat kā jebkuru citu pasūtījumu. Ar veidu, kā tas tiek darīts, nav saistīta neviena izteikta īpašība. Rēķins ņems vērā veicamu transakciju uz kreditora kontu, kas tika izveidota ar šo pasūtījumu, un pēc tam tiks apstrādāts maksājums.

