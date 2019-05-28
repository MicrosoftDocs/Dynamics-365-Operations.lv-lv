---
title: Bieži uzdotie jautājumi par darbplūsmu
description: Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509295"
---
# <a name="workflow-system"></a>Darbplūsmas sistēma

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegtas atbildes uz bieži uzdotajiem jautājumiem par darbplūsmas sistēmu programmā Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Paziņojumi

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Kāpēc darba vienuma noraidīšanas gadījumā tiek saņemti vairāki paziņojumi?
Darba vienuma noraidīšanas gadījumā šis darba vienums tiek pabeigts ar statusu Noraidīts. Tiek izveidots cits darba vienums, kas tiek piešķirts veidotājam. Tas nozīmē, ka veidotājs saņem paziņojumu par noraidīto darba vienumu, bet lietotājs, kas ir piešķirts jaunajam izmaiņu pieprasījuma darba vienumam, saņem atsevišķu paziņojumu. 

Katrs paziņojums ir saistīts ar atšķirīgu darba vienumu, taču to līdzība var radīt apjukumu. Mēs meklējam veidus, kā uzlabot šo situāciju nākamajā laidienā.

### <a name="why-are-my-workflow-exports-failing"></a>Kāpēc manas darbplūsmas tiek eksportētas neveiksmīgi?
Pašlaik darbplūsmas eksportēšanas līdzeklī ir noteikts ierobežojums, kas neļauj darbplūsmas nosaukumiem pārsniegt 48 rakstzīmes. Izmantojot nosaukumu, kas ir garāks par 48 rakstzīmēm, var rasties kļūda “Serveris nevarēja autentificēt pieprasījumu” un/vai iespējamība, ka faila eksportēšana netiks ļauta bez faila tipa. Detalizēta informācija ir pieejama šajā emuāra ziņā: [Darbplūsmas eksportēšanas problēmu risināšana](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).
