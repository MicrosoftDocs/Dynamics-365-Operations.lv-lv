---
title: Čeku izveide ar statusu Tukšs
description: Šajā rakstā ir izskaidrots, kā izveidot tukšus čekus bankas kontam.
author: angelad116
ms.date: 10/24/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 86020d9088d8135c83716128a77090608536a78f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804024"
---
# <a name="create-checks-that-have-blank-status"></a>Čeku izveide ar statusu Tukšs

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā izveidot tukšus čekus. Piemēram, varat izveidot tukšu čeku, lai reģistrētu bojātu čeku, kuru nevar izmantot maksājumam.

Lapā **Čeki** varat veikt čekiem paredzētus uzturēšanas uzdevumus. Piemēram, varat izveidot jaunus čeku numurus un dzēst čekus. Varat arī izveidot čekus ar statusu **Tukšs**. Pēc tam, kad ir izveidoti tukši čeki, tos nevar dzēst vai izmantot sistēmā atkārtoti.

> [!NOTE]
> Šis līdzeklis ir pieejams lapā **Čeki** tikai tad, ja ieslēgsit līdzekli **Čeku izveide ar statusu Tukšs lapā Čeki** lapā **Līdzekļu pārvaldība**. Ja šis līdzeklis nav ieslēgts, čekus ar statusu **Tukšs** var izveidot tikai no dialoglodziņa **Maksājums ar čeku** maksājuma ģenerēšanas procesa laikā sadaļā Kreditori.

Lai atvērtu lapu **Čeki**, dodieties uz **Kases un bankas vadība \> Bankas konti \> Bankas konti** un pēc tam darbību rūtī cilnē **Pārvaldīt maksājumus** grupā **Saistītā informācijā** atlasiet **Čeki**. Vai arī dodieties uz **Kases un bankas vadība \> Pieprasījumi un pārskati \> Čeki**.

Pēc tam, lai izveidotu čekus ar statusu **Tukšs**, darbību rūtī atlasiet **Izveidot tukšus čekus**. Kamēr tiek veidoti tukšie čeki, saistītais bankas konts tiek īslaicīgi deaktivizēts. Tas samazina risku, ka maksājumi tiks ģenerēti tajā pašā laikā, kad tiek veidoti tukši čeki. Kad apstrāde ir pabeigta, saistītais bankas konts tiek aktivizēts atkārtoti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
