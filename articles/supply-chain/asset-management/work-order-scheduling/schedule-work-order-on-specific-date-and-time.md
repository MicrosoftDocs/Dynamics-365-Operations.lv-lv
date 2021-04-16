---
title: Plānot darba pasūtījumu noteiktā datumā un laikā
description: Šajā tēmā ir aprakstīts, kā plānot darba pasūtījumu noteiktā datumā un laikā Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 827f4ca16341d29413f1b1d928965aa1919abf59
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822519"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Plānot darba pasūtījumu noteiktā datumā un laikā

[!include [banner](../../includes/banner.md)]

 

Ja darba pasūtījums ir jāplāno noteiktā datumā *un* laikā, varat ignorēt standarta plānošanas procesu Līdzekļu pārvaldībā un izveidot konkrētu grafiku darba pasūtījumam.

1. Klikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Darba pasūtījuma sarakstā noklikšķiniet uz darba pasūtījuma ID kolonnā **Darba pasūtījums**.

3. Noklikšķiniet uz **Rediģēt**.

4. Kopsavilkuma cilnē **Darba pasūtījuma virsraksts** ievadiet sākuma un beigu datumu un laiku laukos **Paredzētais sākums** un **Paredzētās beigas**.

    ![1. attēls](media/05-work-order-scheduling.png)

5. Cilnē **Vispārīgi** noklikšķiniet uz **Grafiks**, lai izmantotu standarta plānošanas procesu, vai noklikšķiniet uz **Nosūtīt**, ja vēlaties piešķirt darba pasūtījumu konkrētam darbiniekam.

6. Lai ignorētu esošās noslodzes rezervācija un lai nodrošinātu, ka darba pasūtījums tiek ieplānots paredzētajā periodā, veiciet atlasi, kā parādīts attēlā tālāk, dialoglodziņā **Ieplānot darba pasūtījumu** > sadaļā **Ierobežota noslodze**. Tas nozīmē, ka plānošanas process ignorēs esošās noslodzes rezervācijas, jo darba pasūtījumam ir jāsākas ar paredzēto sākuma laiku.

    ![2. attēls](media/06-work-order-scheduling.png)

7. Lai sāktu plānošanu, noklikšķiniet uz **Labi**.

8. Ja plānošanas procesa rezultātā izveidojas divas rezervācijas, ekrānā tiek parādīts ziņojums, un jūs varat pielāgot saistītos darba pasūtījumus.

>[!NOTE]
>Lai darba pasūtījumam ieplānotu uzturēšanas speciālistu, šim uzturēšanas speciālistam ir jābūt pieejamam paredzētajā sākuma datumā un laikā. Darbinieku pieejamība tiek iestatīta [Nodarbināto kalendārā](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]