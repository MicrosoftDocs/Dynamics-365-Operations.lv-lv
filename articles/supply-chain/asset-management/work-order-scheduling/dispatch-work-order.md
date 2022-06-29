---
title: Darba pasūtījuma nosūtīšana
description: Šajā rakstā skaidrots, kā nosūtīt darba pasūtījumu Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f78e8642715b0c3fd3d01e8072645ccd9c58d685
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016860"
---
# <a name="dispatch-work-order"></a>Darba pasūtījuma nosūtīšana

[!include [banner](../../includes/banner.md)]

 

Varat plānot vienu vai vairākus darba pasūtījumus vienam darbiniekam, izmantojot funkcionalitāti **Nosūtīt**.

1. Noklikšķiniet **uz Līdzekļu pārvaldības** > **darbs pasūtījumiem** > **visi darba pasūtījumi** vai aktīvie **darba pasūtījumi**.

2. Sarakstā atlasiet darba pasūtījumu.

3. Cilnē **Vispārīgi** noklikšķiniet uz **Nosūtīt**.

4. Dialoglodziņā **Plānot darba pasūtījumu** atlasiet darbinieku laukā **Darbinieks**.

5. Laukā **Plānot stundas** varat ievietot paredzētās darba stundas, ja paredzētās darba stundas atšķiras no prognozētajām stundām.

6. Laukā **Plānotais sākums** varat rediģēt sākuma datumu un laiku, ja nepieciešams.

7. Ja plānošanas procesam ir piemērojami noslodzes ierobežojumi saistībā ar resursiem, kas jau ieplānoti citiem darbiem, nodrošiniet, lai pārslēgšanas pogas **Līdzeklis**, **Rīks** un **Darbinieks** ir iestatītas uz **Jā**. Lai skatītu sīkāku informāciju par plānošanas procesu, atlasiet **Jā**, nospiežot pārslēgšanas pogu **Izvērsti**. Tas nozīmē, ka detalizēta informācija par aprēķinātajiem rezultātiem attiecībā uz darba rezultātiem ir parādīta Informācijas žurnālā.

8. Atlasiet **Jā**, nospiežot pārslēgšanas pogu **Ignorēt grafiku**, lai ignorētu slēgtās dienas kalendārā (piemērojams līdzeklim, darbiniekam un rīkiem). Atlasiet **Jā**, nospiežot pārslēgšanas pogu **Ignorēt ieplānoto izpildi** ierobežojumu ignorēšanai, kuri, iespējams, tika atlasīti darba pasūtījumā attiecībā uz plānošanu. 

    Informāciju par ieplānotas izpildes iestatīšanu skatiet sadaļā [SIeplānota izpilde](../setup-for-work-orders/scheduled-execution.md).

9. Noklikšķiniet uz **Labi**. Darba pasūtījuma dzīves cikla stāvoklis tiek automātiski atjaunināts uz **Ieplānotu** dzīves cikla stāvokli, kas norādīts sadaļā **Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Dzīves cikla modeļi**.

Tālāk redzamais attēls parāda nosūtīšanas atlašu piemēru dialoglodziņā **Plānot darba pasūtījumu**.

![1. attēls.](media/04-work-order-scheduling.png)

[!NOTE]
Ja vēlaties dzēst darba pasūtījuma grafiku, atlasiet darba pasūtījumu sadaļā **Visi darba pasūtījumi** un pēc tam noklikšķiniet uz **Dzēst grafiku** cilnē **Vispārīgi**. Izdzēšot grafiku, neaizmirstiet manuāli atjaunināt darba pasūtījuma dzīves cikla stāvokli.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]