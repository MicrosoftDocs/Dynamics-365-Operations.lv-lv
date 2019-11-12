---
title: Kļūmes pievienošana darba pasūtījumam
description: Šajā tēmā ir paskaidrots, kā pievienot kļūmes reģistrācijas darba pasūtījumiem programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2b58cc31578d7bb102c6b5aa8b4ce2d6cfe8c893
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626205"
---
# <a name="add-fault-to-work-order"></a>Pievienot kļūmi darba pasūtījumam

[!include [banner](../../includes/banner.md)]



Kļūmes, kas iestatītas kļūmju noformētājā, varat pievienot darba pasūtījumam. Vienam vai vairākiem kļūdas ierakstiem jābūt piesaistītiem tiem līdzekļu veidiem, kas tiek izmantoti darba pasūtījumā atlasītajam līdzeklim. Plašāku informāciju par iestatīšanu skatiet zem saites [KĻūmju pārvaldība](../setup-for-work-orders/fault-management.md).

1. Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Atlasiet darba pasūtījumu, kuram izveidot kļūmju reģistrāciju, un pēc tam darbības rūts cilnē **Darba pasūtījums**, kas atrodas grupā **Līdzekļi**, atlasiet **Līdzekļa kļūme**.

3. Kopsavilkuma cilnē **Simptomi** atlasiet **Pievienot rindu**. Laukā **Kļūme** automātiski tiek ievadīts kļūmes kārtas numurs.

4. Laukā **Kļūmes simptoms** atlasiet attiecīgo kļūmes simptomu.

5. Laukā **Kļūmes apgabals** un **Kļūmes veids** atlasiet atbilstīgās vērtības.

6. Laukā **Kļūmes datums** automātiski tiek ievadīts esošais datums. Pēc vajadzības varat atlasīt citu datumu.

7. Kopsavilkuma cilnē **Atlasītā simptoma iemesli** pievienojiet rindu, kas apraksta problēmas iemeslu.

8. Kopsavilkuma cilnē **Atlasītā simptoma labojumi** pievienojiet rindu, kas apraksta iespējamo problēmas risinājumu.

9. Atlasiet **Saglabāt**.

Attēlā tālāk parādīts kļūmes reģistrācijas piemērs.

![1. attēls](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Līdzekļa kļūmju skatīšana

Sarakstā **Līdzekļu kļūmes** ir pārskats par visām līdzekļiem reģistrētajām kļūmēm.

Saraksta **Līdzekļu kļūmes** lapā ir pārskats par visām kļūmēm, kas reģistrētas līdzekļiem. Lai atvērtu lapu, atlasiet **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļu kļūme** > **Līdzekļu kļūmes**.


## <a name="print-asset-fault-report"></a>Līdzekļu kļūmju pārskata izdrukāšana

Saraksta **Visi līdzekļi** lapā varat izdrukāt līdzekļu kļūmju pārskatu, kas parāda visas kļūmju reģistrācijas un kļūmju statistikas grafisko pārskatu.

1. Atlasiet **Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Visi līdzekļi**

2. Atlasīt līdzekli, kuram jādrukā kļūmju pārskats.

3. Darbību rūts cilnē **Vispārīgi**, grupā **ārskati** atlasiet **Līdzekļu kļūmes**.

4. Ievadiet konkrētu periodu vai izvēlieties kļūmes veidu.

5. Atlasiet **Labi**, lai izdrukātu pārskatu.

>[!NOTE]
>Lai izdrukātu kļūmju pārskatu vairākiem līdzekļiem vai līdzekļu veidiem, atlasiet **Līdzekļu pārvaldība** > **Pārskati** > **Līdzekļi** > **Līdzekļu kļūmes**.

