---
title: Darba pasūtījumu dīkstāve uzturēšanas dēļ
description: Šajā tēmā aprakstīts, kā izveidot dīkstāve uzturēšanas dēļ reģistrācijas līdzeklī, kas ir atlasīts darba pasūtījumā.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53487a0173453ef7a8f5ea818672d999fe71cb65
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020915"
---
# <a name="maintenance-downtime-for-work-orders"></a>Darba pasūtījumu dīkstāve uzturēšanas dēļ

[!include [banner](../../includes/banner.md)]


Jūs varat izveidot dīkstāve uzturēšanas dēļ reģistrācijas līdzeklī, kas ir atlasīts darba pasūtījumā. Šī iespēja ir noderīga, ja vēlaties reģistrēt dīkstāve uzturēšanas dēļ vienā vai vairākās iekārtās ražošanas zonā. Vispirms jūs izveidojat dīkstāves uzturēšanas dēļ pamatojuma kodus, kurus vēlaties izmantot, piemēram, **Sadalījums** vai **Plānota pārtraukšana**. Šī darbība tiek veikta lapā **Dīkstāves uzturēšanas dēļ pamatojuma kodi**. Pēc tam jūs varat izveidot reģistrācijas dīkstāves uzturēšanas dēļ lapā **Dīkstāve uzturēšanas dēļ** un pievienot atbilstošos dīkstāve uzturēšanas dēļ pamatojuma kodus.

## <a name="create-maintenance-downtime-reason-codes"></a>Dīkstāves uzturēšanas dēļ iemeslu kodu izveide

1. Atlasiet **Līdzekļu pārvaldība** > **Uzstādījums** > **Darba pasūtījumi** > **Dīkstāves uzturēšanas dēļ pamatojuma kodi**.

2. Atlasiet **Jauns**.

3. Laukā **Dīkstāve uzturēšanas dēļ pamatojuma kods** ievadiet ID dīkstāve uzturēšanas dēļ pamatojuma kodam.

4. Laukā **Nosaukums** ievadiet nosaukumu.

5. Atzīmējiet izvēles rūtiņu **KPI iekļaut**, ja pamatojuma kods ir jāietver pamatlīdzekļa izpildes pamatrādītāja (key performance indicators - KPIs) aprēķinos. Kopumā plānotajiem ražošanas pārtraukumiem nevajadzētu tikt iekļautiem KPI aprēķinos, tāpēc ka tiem nav ietekmes uz sagaidāmo sniegumu.

6. Atlasiet **Saglabāt**.

Šajā attēlā ir parādīts lapas **Dīkstāves uzturēšanas dēļ pamatojuma kodi** piemērs.

![1. attēls](media/15-work-orders.png)

Pēc tam, kad esat izveidojis dīkstāves uzturēšanas dēļ iemeslu kodus, kurus vēlaties izmantot, jūs varat izveidot dīkstāves uzturēšanas dēļ reģistrācijas darba pasūtījumiem un līdzekļiem.


## <a name="create-maintenance-downtime-registrations"></a>Dīkstāves uzturēšanas dēļ reģistrāciju izveide

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.

2. Atlasiet darba pasūtījumu un pēc tam cilnē **Darba pasūtījums** grupā **Līdzeklis** atlasiet **Dīkstāve uzturēšanas dēļ**.

3. Atlasiet **Jauns**.

4. Laukos **No** un **Uz** ievadiet dīkstāves uzturēšanas dēļ reģistrācijas laiku un datumu.

>[!NOTE]
>Atstājot lauku **Uz**, ilgums stundās tiek automātiski ievietots laukā **Ilgums**.

5. Laukā **Dīkstāves uzturēšanas dēļ iemeslu kods** atlasiet iemesla kodu.

6. Atkārtojiet 3. līdz 5. soli, lai pievienotu vairāk reģistrāciju.

7. Atlasiet **Saglabāt**.

Attēlā tālāk parādīts dīkstāve uzturēšanas dēļ reģistrācijas piemērs.

![2. attēls](media/16-work-orders.png)

Kalendārs, kuru izmanto, lai aprēķinātu dīkstāves uzturēšanas dēļ reģistrāciju, ir atkarīgs no jūsu līdzekļu un parametru uzstādījumu izvēles. Ja sadaļā **Resurss** kopsavilkuma cilnē **Fiksētais līdzeklis** lapā **Visi līdzekļi** ir atlasīts resurss, tiek izmantots kalendārs, kas ir uzstādīts saistītajai resursu grupai, kā parādīts šajā ilustrācijā.

![3. attēls](media/17-work-orders.png)

Ja līdzeklim nav atlasīts neviens resurss, tiek izmantots standarta kalendārs, kas ir atlasīts lapā **Līdzekļu pārvaldības parametri**, kā uzrādīts šajā ilustrācijā.

![4. attēls](media/18-work-orders.png)

Lai redzētu pārskatu par visām dīkstāves uzturēšanas dēļ reģistrācijām, noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Dīkstāve uzturēšanas dēļ**.

>[!NOTE]
>Visi kalendāri, izmantoti modulī **Līdzekļu pārvaldība**, tiek iestatīti **Organizācijas administrēšana** > **Uzstādīšana** > **Kalendāri** > **Kalendāri**.

