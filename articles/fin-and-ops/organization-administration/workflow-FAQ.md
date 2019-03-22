---
title: Bieži uzdotie jautājumi par darbplūsmu
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/01/2019
ms.locfileid: "773221"
---
# <a name="workflow-system"></a>Darbplūsmas sistēma

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu programmā Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Paziņojumi

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Kāpēc darba vienuma noraidīšanas gadījumā tiek saņemti vairāki paziņojumi?
Darba vienuma noraidīšanas gadījumā šis darba vienums tiek pabeigts ar statusu Noraidīts. Tiek izveidots cits darba vienums, kas tiek piešķirts veidotājam. Tas nozīmē, ka veidotājs saņem paziņojumu par noraidīto darba vienumu, bet lietotājs, kas ir piešķirts jaunajam izmaiņu pieprasījuma darba vienumam, saņem atsevišķu paziņojumu. 

Katrs paziņojums ir saistīts ar atšķirīgu darba vienumu, taču to līdzība var radīt apjukumu. Mēs meklējam veidus, kā uzlabot šo situāciju nākamajā laidienā.
