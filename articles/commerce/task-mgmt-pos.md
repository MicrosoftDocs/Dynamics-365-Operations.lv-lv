---
title: Uzdevumu pārvaldība punktā POS
description: Šajā tēmā aprakstīta uzdevumu pārvaldība Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f24ee67cd140fe75d65442484f673b17d32c1f93
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354545"
---
# <a name="task-management-in-pos"></a>Uzdevumu pārvaldība punktā POS

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīta uzdevumu pārvaldība Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.

Dynamics 365 Commerce POS programmai ir uzdevumu pārvaldības līdzekļi, kas ļauj veikala vadītājiem un darbiniekiem pārvaldīt uzdevumus un atjaunināt uzdevumu statusu. Veikala darbinieki var piekļūt uzdevumiem, atlasot elementu **Uzdevumi** POS sākumlapā vai atlasot uzdevumu paziņojumus. Pēc noklusējuma veikala darbinieki tiek uzņemti cilnē **Mani uzdevumi**, kur tie var skatīt sev piešķirtos uzdevumus. Tomēr viņi var viegli pārslēgties uz cilnēm **Nokavētie uzdevumi**, **Atvērtie uzdevumi** un **Uzdevumu saraksti**.

## <a name="task-operations-for-store-managers"></a>Uzdevumu operācijas veikala pārvaldniekiem

Veikala pārvaldnieki var veikt šādas uzdevumu darbības POS programmā, izmantojot pogas komandjoslā:

- **Piešķirt** – piešķir atlasītos uzdevumus veikala darbiniekam.
- **Uzdevuma statuss** — maina atlasīto uzdevumu statusu.
- **Filtrēt** – pēc noklusējuma tiek parādīti tikai aktīvie uzdevumi. Tomēr, lietojot filtrus, vadītāji var skatīt visus uzdevumus, pat uzdevumus, kas ir pabeigti vai atcelti.
- **Jauns uzdevums** — izveidojiet uzdevumu ar esošu uzdevumu sarakstu vai izveidojiet viena mērķa uzdevumu.

Veikala darbinieki var veikt šādas uzdevumu darbības POS programmā, izmantojot pogas komandjoslā:

- **Uzdevuma statuss** — maina atlasīto uzdevumu statusu.
- **Filtrēt** – pēc noklusējuma tiek parādīti tikai aktīvie uzdevumi. Tomēr, lietojot filtrus, darbinieki var skatīt visus uzdevumus, pat uzdevumus, kas ir pabeigti vai atcelti.

Šajā attēlā redzama cilne **Mani uzdevumi** programmā Commerce POS.

![Manu uzdevumu cilne Commerce POS programmā.](media/POS-task-management.png)

Nākamajā attēlā ir redzama cilne **Uzdevumu saraksti**.

![Uzdevumu sarakstu cilne Commerce POS programmā.](media/POS-task-lists-management.png)

## <a name="additional-resources"></a>Papildu resursi

[Uzdevumu pārvaldības pārskats](task-mgmt-overview.md)

[Uzdevumu pārvaldības konfigurēšana](task-mgmt-configure.md)

[Uzdevumu sarakstu izveidošana un uzdevumu pievienošana](task-mgmt-create-lists.md)

[Uzdevumu sarakstu piešķiršana veikaliem vai darbiniekiem](task-mgmt-assign-lists.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
