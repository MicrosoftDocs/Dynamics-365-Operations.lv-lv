---
title: Čeku izveide ar statusu Tukšs
description: Šajā tēmā ir izskaidrots, kā izveidot tukšus čekus bankas kontam lapā Čeki.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: af79dd4831f2e7fc71c296922d73a9e42f7955b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176011"
---
# <a name="create-checks-that-have-blank-status"></a>Čeku izveide ar statusu Tukšs

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā ir izskaidrots, kā izveidot tukšus čekus. Piemēram, varat izveidot tukšu čeku, lai reģistrētu bojātu čeku, kuru nevar izmantot maksājumam.

Lapā **Čeki** varat veikt čekiem paredzētus uzturēšanas uzdevumus. Piemēram, varat izveidot jaunus čeku numurus un dzēst čekus. Varat arī izveidot čekus ar statusu **Tukšs**. Pēc tam, kad ir izveidoti tukši čeki, tos nevar dzēst vai izmantot sistēmā atkārtoti.

> [!NOTE]
> Šis līdzeklis ir pieejams lapā **Čeki** tikai tad, ja ieslēgsit līdzekli **Čeku izveide ar statusu Tukšs lapā Čeki** lapā **Līdzekļu pārvaldība**. Ja šis līdzeklis nav ieslēgts, čekus ar statusu **Tukšs** var izveidot tikai no dialoglodziņa **Maksājums ar čeku** maksājuma ģenerēšanas procesa laikā sadaļā Kreditori.

Lai atvērtu lapu **Čeki**, dodieties uz **Kases un bankas vadība \> Bankas konti \> Bankas konti** un pēc tam darbību rūtī cilnē **Pārvaldīt maksājumus** grupā **Saistītā informācijā** atlasiet **Čeki**. Vai arī dodieties uz **Kases un bankas vadība \> Pieprasījumi un pārskati \> Čeki**.

Pēc tam, lai izveidotu čekus ar statusu **Tukšs**, darbību rūtī atlasiet **Izveidot tukšus čekus**. Kamēr sistēma veido tukšus čekus, saistītais bankas konts tiek īslaicīgi deaktivizēts. Tas samazina risku, ka maksājumi tiks ģenerēti tajā pašā laikā, kad tiek veidoti tukši čeki. Kad apstrāde ir pabeigta, saistītais bankas konts tiek aktivizēts atkārtoti.
