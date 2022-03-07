---
title: Čeku izveide ar statusu Tukšs
description: Šajā tēmā ir izskaidrots, kā izveidot tukšus čekus bankas kontam lapā Čeki.
author: abruer
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3c431ed975aecf116fbf626018038b112a0a8cca063e1462e31e206480643e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720554"
---
# <a name="create-checks-that-have-blank-status"></a>Čeku izveide ar statusu Tukšs

[!include [banner](../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā izveidot tukšus čekus. Piemēram, varat izveidot tukšu čeku, lai reģistrētu bojātu čeku, kuru nevar izmantot maksājumam.

Lapā **Čeki** varat veikt čekiem paredzētus uzturēšanas uzdevumus. Piemēram, varat izveidot jaunus čeku numurus un dzēst čekus. Varat arī izveidot čekus ar statusu **Tukšs**. Pēc tam, kad ir izveidoti tukši čeki, tos nevar dzēst vai izmantot sistēmā atkārtoti.

> [!NOTE]
> Šis līdzeklis ir pieejams lapā **Čeki** tikai tad, ja ieslēgsit līdzekli **Čeku izveide ar statusu Tukšs lapā Čeki** lapā **Līdzekļu pārvaldība**. Ja šis līdzeklis nav ieslēgts, čekus ar statusu **Tukšs** var izveidot tikai no dialoglodziņa **Maksājums ar čeku** maksājuma ģenerēšanas procesa laikā sadaļā Kreditori.

Lai atvērtu lapu **Čeki**, dodieties uz **Kases un bankas vadība \> Bankas konti \> Bankas konti** un pēc tam darbību rūtī cilnē **Pārvaldīt maksājumus** grupā **Saistītā informācijā** atlasiet **Čeki**. Vai arī dodieties uz **Kases un bankas vadība \> Pieprasījumi un pārskati \> Čeki**.

Pēc tam, lai izveidotu čekus ar statusu **Tukšs**, darbību rūtī atlasiet **Izveidot tukšus čekus**. Kamēr sistēma veido tukšus čekus, saistītais bankas konts tiek īslaicīgi deaktivizēts. Tas samazina risku, ka maksājumi tiks ģenerēti tajā pašā laikā, kad tiek veidoti tukši čeki. Kad apstrāde ir pabeigta, saistītais bankas konts tiek aktivizēts atkārtoti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]