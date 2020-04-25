---
title: Uzturēšanas grafiks
description: Šajā tēmā ir paskaidrotas uzturēšanas grafiks programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc45dc73073f32db78dc5a8203c661d78437e55f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203300"
---
# <a name="maintenance-schedule"></a>Uzturēšanas grafiks

[!include [banner](../../includes/banner.md)]

 

Uzturēšanas grafiks satur sarakstu ar visiem paredzamajiem preventīvajiem uzturēšanas plāniem, uzturēšanas pieprasījumiem un uzturēšanas cikliem, kuri ir jāveic. Dažas grafika rindas var konvertēt darba pasūtījumos.

Četri uzturēšanas grafika skati ir nedaudz atšķirīgi, atkarībā no tā, kuras uzturēšanas grafika rindas vēlaties redzēt.

| Izvēlnes elements                  | Satura apraksts                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Viss uzturēšanas grafiks       | Tiek uzrādītas visas uzturēšanas grafika rindas.     |
| Mans līdzekļu grafiks        | Visas uzturēšanas grafika rindas, kas satur līdzekļus, kas instalēti funkcionālajā novietojumā, ar kuru esat saistīts kā speciālists (uzstādītas sadaļā [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md)) tiek parādītas šajā sarakstā. |
| Atvērt uzturēšanas grafika rindas | Uzturēšanas grafika rindas ar statusu "Izveidota" - kas nozīmē, ka tās vēl nav konvertētas darba pasūtījumā vai atceltas - tiek uzrādītas šajā sarakstā.                                            |
| Atvērt uzturēšanas grafika kopas | Uzturēšanas grafika rindas, kuras ir saistītas ar darba pasūtījumu kopu, tiek uzrādītas šajā sarakstā.                                                                                                                  |

>[!NOTE]
>Ja pasūtījuma grafika rinda ir ietverta vairākās darba pasūtījumu kopās (skatīt [Darba pasūtījumu kopas](../work-orders/work-order-pools.md)), katrai kopai tiek uzrādīts viens ieraksts opcijā **Atvērt uzturēšanas grafiku kopas**. Tas tiek darīts, lai optimizētu filtrēšanas opcijas darba pasūtījumu kopām.

Lai atvērtu uzturēšanas grafiku:

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas grafiks** > **Visi uzturēšanas grafiki** vai **Atvērt uzturēšanas grafika rindas** vai **Atvērt uzturēšanas grafika kopas**.

2. Lai atjauninātu uzturēšanas grafiku, noklikšķiniet uz **Uzturēšanas plāns** vai **Uzturēšanas cikli**. 

3. Jūs varat rediģēt uzturēšanas grafika rindu, atlasot to un noklikšķinot uz **Rediģēt**. Piemēram, jūs varat viegli atjaunināt servisa līmeni vai par darbu atbildīgo speciālistu. Jūs varat rediģēt vienīgi tās uzturēšanas grafika rindas, kuras vēl nav savienotas ar darba pasūtījumu.

4. Jūs varat dzēst uzturēšanas grafika rindu, atlasot to saraksta lapā un noklikšķinot uz **Dzēst**.

5. Jūs varat atcelt uzturēšanas grafika rindu, atlasot to saraksta lapā un noklikšķinot uz **Atcelt**. Šī funkcija ir noderīga, ja, piemēram, līdzeklim ir 2000 km uzturēšanas plāns un 10 000 km uzturēšanas plāns. Tādā gadījumā jūs varat vēlēties atcelt rindu, kas izveidota no 2000 km uzturēšanas plāna, ja tas sakrīt ar 10 000 km, 20 000 km, 30 000 km u.t.t. Ja jūs atceļat uzturēšanas grafika rindu, kas ir saistīta ar uzturēšanas plānu, šī rinda nekad vairs neparādīsies, kad šis uzturēšanas plāns tiek ieplānots.

6. Jūs varat atlasīt uzturēšanas rindu skaitu sadaļā **Visi uzturēšanas grafiki** un noklikšķināt uz **Darba pasūtījumu kopa**, ja jūs vēlaties, lai visas atlasītās rindas tiek iekļautas vienā darba pasūtījumu kopā.

7. Jūs varat atlasīt uzturēšanas rindas sadaļā **Visi uzturēšanas grafiki** vai **Atvērt uzturēšanas grafiku rindas** vai **Atvērt uzturēšanas grafiku kopas** un noklikšķināt uz **Pielāgot grafiku**, ja vēlaties veikt vienādus pielāgojumus vairākām rindām. Jūs varat mainīt paredzamos sākuma un beigu datumus, servisa līmeni un atbildīgo uzturēšanas speciālistu grupu vai atbildīgo uzturēšanas speciālistu, kas ir saistīts ar atlasītajām uzturēšanas grafika rindām.

- Kad uzturēšanas grafika rinda ir saistīta ar darba pasūtījumu, darba pasūtījuma ID tiks uzrādīts laukā **Darba pasūtījums**.  
- Detalizētajā skatā **Visi līdzekļi** kopsavilkuma cilnē **Līdzekļu uzturēšanas plāni** jūs varat līdzeklim atlasīt uzturēšanas plānu. Pēc tam, ja dzēšat uzturēšanas plāna rindu, kas saistīta ar līdzekli sadaļā **Visi līdzekļi**, jūs varat arī automātiski dzēst visas uzturēšanas grafika rindas ar statusu "Izveidota", kuras ir izveidotas, pamatojoties uz šo pašu uzturēšanas plānu. Skatīt arī [Izveidot līdzekli](../objects/create-an-object.md).

Ilustrācijā zemāk uzrādīta saraksta lapa **Visi uzturēšanas grafiki**.

![1. attēls](media/16-preventive-maintenance.png)

