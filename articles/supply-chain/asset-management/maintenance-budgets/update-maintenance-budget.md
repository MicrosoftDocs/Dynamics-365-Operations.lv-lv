---
title: Uzturēšanas budžeta atjaunināšana
description: Šajā tēmā ir paskaidrots, kā atjaunināt uzturēšanas budžetu programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 486782968816cc585d9cf2d753f32e82f85e4f7e
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874789"
---
# <a name="update-maintenance-budgets"></a>Uzturēšanas budžeta atjaunināšana

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Lapa **Uzturēšanas budžeta rindas** parāda visas budžeta rindas, kas ir izveidotas budžetā, kas ir atlasīts lapā **Uzturēšanas budžeti**. (Vairāk informācijas skatiet sadaļā [Uzturēšanas budžetu izveide](create-maintenance-budget.md).) Jūs varat pārrēķināt un pielāgot uzturēšanas budžeta rindas, līdz tiek apstiprināts uzturēšanas budžets. Kad budžeta periods ir pagājis un izmaksas ir ievietotas līdzekļu pārvaldībā, varat atjaunināt budžeta rindas ar faktiskajām izmaksām.

## <a name="recalculate-a-maintenance-budget"></a>Uzturēšanas budžeta pārrēķināšana

Jūs varat pārrēķināt uzturēšanas budžetu lapā **Uzturēšanas budžeta rindas**. Pārrēķinot uzturēšanas budžetu, esošās budžeta rindas tiek izdzēstas un tiek veikts jauns aprēķins.

1. Lapā **Uzturēšanas budžeta rindas** atlasiet **Pārrēķināt**.
2. Dialoglodziņā **Pārrēķināt budžetu** veiciet nepieciešamās izmaiņas jaunajam aprēķinam un pēc tam atlasiet **Labi**.

Atbilstoši iestatītajām vērtībām tiek izveidotas jaunas budžeta rindas.

## <a name="adjust-budget-lines"></a>Budžeta rindu pielāgošana

Tā vietā, lai pārrēķinātu visu uzturēšanas budžetu, varat pielāgot atlasītās rindas, kas saistītas ar budžeta izmaksām.

1. Lapā **Uzturēšanas budžeta rindas** atlasiet rindas, lai tām atjauninātu budžeta izmaksas.
2. Atlasiet **Pielāgot**.
3. Lai atlasītajām rindām pievienotu summu, atlasiet dialoglodziņu **Pievienot izmaksas** un tad ievadiet vērtību laukā **Pievienot vērtību**.
4. Lai reizinātu budžeta izmaksas atlasītajās budžeta rindās ar koeficientu, atlasiet dialoglodziņu **Reizināt izmaksas** un ievadiet koeficientu laukā **Reizināšanas vērtība**.

    Piemēram, ja jūs ievadāt vērtību **1,2** laukā **Reizināšanas vērtība**, jūs palielināt budžeta izmaksas izvēlētajām rindām par 20 procentiem. Ja jūs ievadāt vērtību **0,7**, jūs samazināt budžeta izmaksas izvēlētajām rindām par 30 procentiem.

5. Atlasiet **Labi**.

Atlasītās budžeta rindas tiek atjauninātas atbilstoši vērtībām, kuras iestatījāt 3. vai 4. darbībā.

## <a name="update-actual-costs"></a>Faktisko izmaksu atjaunināšana

Kad datumi budžeta rindās ir pagājuši un faktiskās izmaksas ir publicētas līdzekļu pārvaldībā, varat atjaunināt uzturēšanas budžeta faktiskās izmaksas.

1. Lapā **Uzturēšanas budžeta rindas** atlasiet **Atjaunināt izmaksas**.
2. Dialoglodziņā **Aprēķināt faktiskās izmaksas** atlasiet **Labi**.

Lauki **Faktiskās izmaksas** budžeta pozīcijās tiek atjaunināti, ja ir publicētas faktiskās izmaksas. Jaunas budžeta rindas var tikt izveidotas, ja kopš budžeta izveidošanas ir izveidoti jauni līdzekļu veidi un ja šie līdzekļu veidi ir izmantoti līdzekļiem, kuriem ir izveidoti darba pasūtījumi un par kuriem ir publicētas saistītās izmaksas. Jaunās budžeta rindas parāda tikai faktiskās izmaksas, jo tām netika aprēķinātas budžeta izmaksas.

> [!NOTE]
> Lai skatītu pārskatu par faktiskajām izmaksām, kas sadalītas profilaktiskajās, koriģējošajās un ieguldījumu izmaksās, lapā **Līdzekļu izmaksu kontrole** varat veikt aprēķinus par to pašu periodu. 

## <a name="manually-add-budget-lines"></a>Budžeta rindu manuāla pievienošana

Lapā **Uzturēšanas budžeta rindas** jūs varat manuāli pievienot jaunu budžeta rindu, atlasot **Jauns** un tad veicot nepieciešamās atlases rindā. Šeit ir daži situāciju piemēri, kad šī pieeja varētu būt noderīga.

- Jūs zināt, ka dažu līdzekļu atjaunošana pašlaik ir plānošanas posmā, bet saistītie uzdevumi vēl nav izveidoti līdzekļu pārvaldībā. Tomēr jūs vēlaties, lai šo uzdevumu budžeta izmaksas tiktu iekļautas uzturēšanas budžetā.
- Kopš budžeta uzturēšanas budžeta sastādīšanas ir izveidoti jauni līdzekļi vai līdzekļu veidi, taču šiem līdzekļiem vai līdzekļu veidiem vēl nav izveidoti uzturēšanas plāni. Tomēr jūs vēlaties, lai šo līdzekļu veidu budžeta izmaksas tiktu iekļautas uzturēšanas budžetā.
