---
title: Mobilās ierīces izvēlnes vienuma iestatīšana pirkšanas pasūtījuma darba pabeigšanai
description: Šajā tēmā parādīts, kā iestatīt mobilās ierīces izvēlnes vienumu.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 905094ae4e76fadbebea1892ec20427f32e3e71d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216831"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Mobilās ierīces izvēlnes vienuma iestatīšana pirkšanas pasūtījuma darba pabeigšanai

[!include [banner](../../includes/banner.md)]

Šajā tēmā parādīts, kā iestatīt mobilās ierīces izvēlnes vienumu. Šajā piemērā izvēlnes vienums tiek lietots, lai veiktu darbu ar tipu Pirkšanas pasūtījums. Ar izvēlnes vienumu saistītā darba klase nosaka, kurš darbs ir derīgs. Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF. Parasti šo procedūru izpilda noliktavas pārvaldnieks.


## <a name="create-a-mobile-device-menu-item"></a>Mobilās ierīces izvēlnes elementa izveide
1. Pārejiet uz **Mobilās ierīces izvēlnes krājumi**, ievadot to meklēšanas joslā.
2. Atlasiet **Jauns**.
3. Laukā **Izvēlnes vienuma nosaukums** ievadiet vērtību. Ievadiet unikālu vērtību. Piemēram, jūs varat ierakstīt `POMove`. Atcerieties šo vērtību, jums tā vēlāk būs nepieciešama.  
4. Laukā **Nosaukums** ievadiet vērtību.  Tas ir nosaukums, kas tiks rādīts mobilajā ierīcē. Piemēram, jūs varat ierakstīt `PO Move`.  
5. Laukā **Režīms** atlasiet **Darba**.
6. Atlasiet **Jā** laukā **Izmantot esošo darbu**.
    - Šis mobilās ierīces izvēlnes elements tiek izmantots, lai veiktu esošu darbu. Šī vērtība jums ir jāiestata uz **jā**.  
    - Lauks **Attēlot krājumu statusu** nosaka, vai uz vietas esošā krājuma statuss mobilajā ierīcē tiks parādīts noliktavas darbiniekam.  
7. Laukā **Noteica:** atlasiet **Sistēmas grupēšana**. Kad jūs kaut ko atlasāt laukā **Noteica:** šīs lapas sadaļā **Vispārīgi** parādās papildu lauki. Rādītie lauki ir atkarīgi no jūsu veiktās atlases. Kad jūs atlasāt **Sistēmas grupēšana**, tiek pievienoti divi jauni lauki. Tie ir paskaidroti tālāk.  
8. Laukā **Sistēmas grupēšana** atlasiet **WorkPoolId**. Kad noliktavas darbinieki atver šo izvēlnes elementu, viņiem tiek lūgts skenēt darbu kopas ID. Visi darbu pasūtījumi ar šo darbu kopas ID un atvērtām darbu pasūtījuma rindām, kurās šim izvēlnes elementam ir pievienota viena no darbu klasēm, tiks padoti lietotājam.  
9. Laukā **Sistēmas grupēšanas etiķete** ierakstiet vērtību. Šis ir teksts, kas tiek rādīts lietotājam mobilajā ierīcē. Piemēram, jūs varat ierakstīt **Darba kopa**.  
10. Atlasiet **Jā** laukā **Ignorēt licences numura zīmi ievietošanas laikā**. Šī opcija noliktavas darbiniekiem ļauj ignorēt mērķa noliktavas vienības numura zīmi, kad krājumi tiek izvietoti no numura zīmes atkarīgā novietojumā.  
11. Atlasiet **Jā** laukā **Grupa nolikta malā**.
    - Ja visiem darbu pasūtījumiem izvietošanas rindās ir tas pats novietojums, tad lietotājs saņems vienu kombinētu izvietošanas instrukciju visām rindām. 
    - Audita veidnes ID: darba audita veidne jums ļauj norādīt, ka darba process kādam izvēlnes elementam ir jāpārtrauc, lai varētu izpildīt citu operāciju. Piemēram, ja šis izvēlnes elements ir paredzēts ienākošam darbam, tad audita veidnē var tikt pieprasīts, lai darbinieks pārbaudītu temperatūru. Procesa pārtraukšanas brīdis ir norādīts audita veidnē un tas var būt, piemēram, brīdis, kad darbs tiek sākts vai pabeigts, vai brīdis, kad tiek mainīts darba statuss.  
12. Izvērtiet sadaļu **Darba klases**.
13. Atlasiet **Jauns**.
14. Laukā **Darba klases ID** ierakstiet vērtību `Purchase`. Darbu veidne ierobežo darbu, kam šo izvēlnes elementu var izmantot. Šajā gadījumā tā tiks izmantota atvērtajām darbu pasūtījuma rindām, kam ir pirkšanas darba klases ID.  
15. Atlasiet **Saglabāt**.

## <a name="set-up-work-confirmation"></a>Darba apstiprinājuma iestatīšana
1. Atlasiet **Darba apstiprinājuma iestatīšana**.
2. Laukā **Darba tips atlasiet** vienumu **Izdošana**.
3. Atlasiet izvēles rūtiņu **Automātiski apstiprināt**. Darba instrukcija ar darba tipu Izdošana tiks apstiprināta automātiski. Šī instrukcija netiks parādīta lietotājam.  
4. Atlasiet **Jauns**.
5. Laukā **Darba veids** atlasiet “Ievietot”.
6. Atzīmējiet izvēles rūtiņu **Atrašanās vietas apstiprinājums**. Kad krājums tiek nolikts, noliktavas darbiniekam tiek lūgts izpildīt novietojuma apstiprinājuma skenēšanu.  
7. Atlasiet **Saglabāt**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Izvēlnes elementa pievienošana mobilās ierīces izvēlnei
1. Pārejiet uz **Mobilās ierīces izvēlne**, ievadot to meklēšanas joslā.
2. Atlasiet **Rediģēt**.
3. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet lauku **Nosaukums** ar lauka **ienākošais** vērtību. Jūs vēlaties atrast izvēlni, kuru izmantojat ienākošajiem izvēlnes elementiem. USMF tā nosaukums ir **Ienākošais**.  
4. Kokā atlasiet **vērtību**.
5. Atlasiet bultiņu, kas norāda pa labi.
6. Atlasiet **Saglabāt**.
7. Aizvērt lapu.
