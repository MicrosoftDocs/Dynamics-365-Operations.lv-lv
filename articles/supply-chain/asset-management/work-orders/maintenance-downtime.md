---
title: Dīkstāve uzturēšanas dēļ
description: Šajā tēmā aprakstīta dīkstāve uzturēšanas dēļ programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918248"
---
# <a name="maintenance-downtime"></a>Dīkstāve uzturēšanas dēļ


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrācijas līdzeklī, kas atlasīts darba pasūtījumā. Tas ir noderīgi, ja vēlaties reģistrēt dīkstāvi uzturēšanas dēļ vienā vai vairākās iekārtās ražošanas zonā. Vispirms jūs izveidojat dīkstāves uzturēšanas dēļ iemeslu kodus, kurus vēlaties izmantot, piemēram, salūšana vai plānota pārtraukšana. Tas tiek darīts sadaļā **Dīkstāves uzturēšanas dēļ iemeslu kodi**. Pēc tam jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrācijas sadaļā **Dīkstāve uzturēšanas dēļ** un pievienot atbilstošos iemeslu kodus.

## <a name="create-maintenance-downtime-reason-codes"></a>Dīkstāves uzturēšanas dēļ iemeslu kodu izveide

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādījums** > **Darba pasūtījumi** > **Dīkstāves uzturēšanas dēļ iemeslu kodi**.

2. Klikšķiniet **Jauns**.

3. Laukā **Dīkstāves uzturēšanas dēļ iemeslu kods** ievadiet ID.

4. Laukā **Nosaukums** ievadiet iemesla kodu.

5. Atlasiet izvēles rūti **KPI ietver**, ja iemesla kodu ir jāiekļauj līdzekļa KPI aprēķinos. Kopumā plānotajiem ražošanas pārtraukumiem nevajadzētu tikt iekļautiem KPI aprēķinos, jo tiem nav ietekmes uz sagaidāmo sniegumu.

6. Noklikšķiniet uz **Saglabāt**.

![1. attēls](media/15-work-orders.png)


Kad esat izveidojis dīkstāves uzturēšanas dēļ iemeslu kodus, kurus vēlaties izmantot, jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrācijas darba pasūtījumiem un līdzekļiem.


## <a name="create-maintenance-downtime-registrations"></a>Dīkstāves uzturēšanas dēļ reģistrāciju izveide

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Atlasiet darba pasūtījumu un noklikšķiniet uz **Dīkstāve uzturēšanas dēļ**.

3. Klikšķiniet **Jauns**.

4. Ievadiet dīkstāves uzturēšanas dēļ reģistrācijas laiku un datumu laukos **No** un **Uz**.

5. Atstājot lauku **Uz**, ilgums stundās tiek automātiski ievietots laukā **Ilgums**.

6. Laukā **Dīkstāves uzturēšanas dēļ iemeslu kods** ievadiet iemesla kodu.

7. Ja vēlaties pievienot papildu reģistrācijas, atkārtojiet 3.–6. darbību.

8. Noklikšķiniet uz **Saglabāt**.


![2. attēls](media/16-work-orders.png)


Kalendārs, kuru izmanto, lai aprēķinātu dīkstāves uzturēšanas dēļ reģistrāciju, ir atkarīgs no jūsu veiktās līdzekļu un parametru uzstādījumu izvēles. Ja sadaļā **Visi līdzekļi** > **Fiksētais līdzeklis** kopsavilkuma cilnē > laukā **Resurss** ir atlasīts resurss, tiek izmantots kalendāra uzstādījums saistītajai resursu grupai, kā parādīts šajā attēlā.

![3. attēls](media/17-work-orders.png)


Ja līdzeklim nav atlasīts neviens resurss, tiek izmantots standarta kalendārs, kas atlasīts sadaļā **Līdzekļu pārvaldības parametri**, kā uzrādīts šajā attēlā.

![4. attēls](media/18-work-orders.png)


Noklikšķiniet uz **Uzņēmuma līdzekļu pārvaldība** > **Pieprasījumi** > **Dīkstāve uzturēšanas dēļ**, lai redzētu pārskatu par visām dīkstāves uzturēšanas dēļ reģistrācijām.

>[!NOTE]
>Visi kalendāri, kas tiek izmantoti modulī **Līdzekļu pārvaldība**, tiek iestatīti **Organizācijas administrēšana** > **Uzstādīšana** > **Kalendāri** > **Kalendāri**.

