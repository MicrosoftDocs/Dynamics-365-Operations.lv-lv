---
title: Noliktavu iestatīšana pārsūtīšanas pasūtījumiem
description: Šajā tēmā ir aprakstīts, kā var iestatīt noliktavas pārsūtīšanas pasūtījumiem.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e482567eb92b9ab891d41d82d10cbb87f9b7fb01
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017487"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Noliktavu iestatīšana pārsūtīšanas pasūtījumiem 

[!include [banner](../includes/banner.md)]

Var izmantot noliktavas līmeņus, lai izveidotu hierarhiju, kas atbalsta pārsūtīšanas pasūtījumus starp noliktavām. Pamatojoties uz šo iestatījumu, vispārējā (grafika) plānošana aprēķina krājuma vajadzības atsevišķās noliktavas līmenī un izveido plānotos pārsūtīšanas pasūtījumus no piešķirtās avota noliktavas, lai tos izpildītu.

1.  Noklikšķiniet uz **Krājumu vadība > Iestatījumi > Noliktavu sadalījums > Noliktavas**.

2.  Atlasiet noliktavu, kas jāuzpilda.

3.  Kopsavilkuma cilnē **Vispārējā plānošana** atzīmējiet izvēles rūtiņu **Uzpilde**.

4.  Laukā **Galvenā noliktava** atlasiet to noliktavu, ko vēlaties piešķirt kā uzpildes noliktavu. Vispārējā plānošana aprēķina pārsūtīšanas pieprasījumu atlasītajai noliktavai un ģenerē plānotās pārsūtīšanas pasūtījumu no piešķirtās **Galvenās noliktavas**.
   
    > [!NOTE]
    > <P>Ja noņem atzīmi izvēles rūtiņā <STRONG>Uzpilde</STRONG>, atlasītajai noliktavai tiek piešķirts noliktavas līmenis saistībā ar <STRONG>Galveno noliktavu</STRONG>, bet <STRONG>Galvenā noliktava</STRONG> netiek iestatīta kā uzpildes noliktava.</P>

5.  Lai lietotu jauno iestatījumu, aizveriet lapu.


> [!TIP]
> <P>Ja uzpildīšanai vēlaties piešķirt noliktavu, vispirms lapā <STRONG>Noliktavas dimensiju grupas</STRONG> ir jāiestata noliktava kā noliktavas dimensija. Šajā lapā atlasiet noliktavai lauku <STRONG>Aktīva</STRONG> un lauku <STRONG>Vajadzības plāns pa dimensijām</STRONG>.</P>

## <a name="set-up-transport-lead-time"></a>Transportēšanas izpildes laika iestatīšana

Lapā **Transportēšanas dienas** ir jāiestata arī transportēšanas izpildes laiks starp noliktavām. 
1. Atveriet sadaļu **Krājumu vadība > Iestatījumi > Sadale > Transportēšanas dienas**.
2. Laukā **Saņemšanas punkts** atlasiet vienumu **noliktava**.
3. Atlasiet **Nosūtītāja noliktava** , **Saņēmēja noliktava** un **Transportēšanas dienas**. 
4. (Nav obligāti) Varat arī iestatīt transportēšanas laiku atkarībā no piegādes veida cilnē **Transportēšanas dienas atbilstoši piegādes veidam**.
