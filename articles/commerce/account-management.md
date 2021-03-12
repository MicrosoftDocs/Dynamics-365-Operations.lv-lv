---
title: Konta pārvaldības lapas un moduļi
description: Šajā tēmā ietvertas konta pārvaldības lapas un moduļi programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c465b8883438eee886b177274bf89ddb86aa00b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980560"
---
# <a name="account-management-pages-and-modules"></a>Konta pārvaldības lapas un moduļi

[!include [banner](includes/banner.md)]

Šajā tēmā ietvertas konta pārvaldības lapas un moduļi programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Konta pārvaldība attiecas uz lapu grupu, kas tiek izmantota, lai pārvaldītu ar lietotāja konta saistīto informāciju programmā Dynamics 365 Commerce. Konta pārvaldības lapās ir ietverta konta pārvaldības mērķlapa, lietotāja profila lapa, lietotāja adreses lapa, pasūtījuma vēstures lapa, pasūtījuma informācijas lapa, lojalitātes programmas lapa un vēlmju saraksta lapa.

### <a name="account-management-landing-page"></a>Konta pārvaldības mērķlapa

Konta pārvaldības mērķlapā tiek izmantoti šādi moduļi.

- **Konteiners** — visas konta pārvaldības izvietošanas lapas moduļi jāievieto konteinerā. 
- **Konta sveiciena elements** — šis modulis tiek izmantots, lai nodrošinātu sveiciena ziņojumu konta pārvaldības lapā. Tas ietver galvenes rekvizītus.
- **Konta vispārīgais elements** — šis modulis var tikt izmantots, lai nodrošinātu pozīcijas un saites uz kontu pārvaldības lapām, piemēram, lapas “Pasūtījumu vēsture” vai “Mans profils”. Vispārīgo mozaīkas moduli var izmantot, lai konfigurētu mozaīku jebkurai lapai. Fabrikam šis modulis tiek izmantots lapas “Pasūtījumu vēsture” un “Mans profils” saitēm konta pārvaldības izvietošanas lapā.
- **Konta vēlmju elements** — šis modulis tiek izmantots, lai sniegtu elementu kopsavilkumu klienta vēlmju sarakstā. Piemēram, tas var norādīt: “Jūsu vēlmju sarakstā ir 10 elementi.” Tajā ir iekļauti rekvizīti virsrakstam un saitei “Skatīt detalizētu informāciju”. Saite “Skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz vēlmju saraksta lapu. 
- **Konta adreses elements** — šis modulis tiek izmantots, lai sniegtu lietotāja adrešu kopsavilkumu. Piemēram, tas var norādīt: “Jūsu kontam ir pievienotas 2 adreses.” Tajā ir iekļauti rekvizīti virsrakstam un saitei “Skatīt detalizētu informāciju”. Saite “Skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lietotāja adreses lapu.
- **Konta lojalitātes programmas elements** — šis modulis tiek izmantots, lai parādītu un izveidotu saiti ar informāciju par lojalitātes programmu. Šim elementam ir divi stāvokļi: viens stāvoklis rāda saites, lai pievienotos lojalitātes programmai, ja lietotājs jau nav dalībnieks. Otrs stāvoklis rāda saites, lai skatītu lojalitātes programmas informācijas lapu, kad lietotājs jau ir dalībnieks. Rekvizītos ietilpst galvene, saite “Reģistrēšanās” un saite “Skatīt lojalitātes programmas”. Saite “Skatīt lojalitāti” ir jākonfigurē novirzīšanai uz lojalitātes programmas lapu. Saite “Pierakstīšanās” ir jākonfigurē novirzīšanai uz lapu, kur lietotāji var pievienoties lojalitātes programmai. 

### <a name="order-history-page"></a>Pasūtījumu vēstures lapa

Pasūtījumu vēstures lapā tiek izmantots pasūtījuma vēstures modulis, lai parādītu visus pēdējos lietotāja veiktos pasūtījumus.

### <a name="order-details-page"></a>Pasūtījumu informācijas lapa

Pasūtījumu informācijas lapa sniedz detalizētu informāciju par katru pasūtījumu, un tai var piekļūt no pasūtījumu vēstures lapas. Tā izmanto pasūtījuma informācijas moduli, kas pieprasa pārdošanas ID vai transakcijas ID, lai izgūtu pasūtījuma informāciju.

### <a name="user-profile-page"></a>Lietotāja profila lapa

Lietotāja profila lapā tiek rādīta lietotāja konta informācija, piemēram, lietotāja vārds un e-pasta adrese. Tā izmanto lietotāja profila informāciju un lietotāja profila rediģēšanas moduļus. Lai gan e-pasta adresi nevar noņemt, to var rediģēt. Lietotāja profila lapā tiek rādītas arī lietotāja preferences, kas ļauj lietotājam piedalīties vai atteikties no noteiktām funkcijām, piemēram, ieteikumu sarakstu personalizēšanas. 

### <a name="user-address-page"></a>Lietotāja adreses lapa

Lietotāja adreses lapā tiek parādīts to adrešu saraksts, kuras ir saistītas ar lietotāja kontu. Lietotājs vai nu sniedzis šīs adreses norēķināšanās laikā, vai arī tās tieši pievienojis šajā lapā. Lietotāja adreses modulis tiek izmantots, lai pievienotu un rediģētu adreses, iestatītu primāro adresi un atveidotu esošās adreses lapā.

### <a name="wish-list-page"></a>Vēlmju saraksta lapa

Vēlmju saraksta lapā ir redzami elementi, kas tika pievienoti klienta vēlmju sarakstā. Tā izmanto vēlmju saraksta moduli, lai atveidotu vēlmju saraksta elementus.

### <a name="loyalty-page"></a>Lojalitātes lapa

Izmantojot lojalitātes programmas lapu, klienti var skatīt informāciju par savu lojalitātes programmu, ja viņi jau ir dalībnieki. Viņi var arī skatīt punktus, ko nopelnījuši un izpirkuši pēdējās transakcijās. Lapa izmanto lojalitātes programmas informācijas moduli, lai parādītu lojalitātes programmas detaļas. 

Lai pievienotos lojalitātes programmai, mārketinga lapu var izveidot, izmantojot lojalitātes programmas pierakstīšanās un lojalitātes programmas moduļus. Ja lietotājs nav lojalitātes programmas dalībnieks, šie moduļi ļaus lietotājam reģistrēties.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Konteinera modulis](add-container-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
