---
title: Konta pārvaldības lapas un moduļi
description: Šajā tēmā ietvertas konta pārvaldības lapas un moduļi programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785388"
---
# <a name="account-management-pages-and-modules"></a>Konta pārvaldības lapas un moduļi

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ietvertas konta pārvaldības lapas un moduļi programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Konta pārvaldība attiecas uz lapu grupu, kas tiek izmantota, lai pārvaldītu ar lietotāja konta saistīto informāciju programmā Dynamics 365 Commerce. Konta pārvaldības lapās ir ietverta konta pārvaldības mērķlapa, lietotāja profila lapa, lietotāja adreses lapa, pasūtījuma vēstures lapa, pasūtījuma informācijas lapa, lojalitātes programmas lapa un vēlmju saraksta lapa.

### <a name="account-management-landing-page"></a>Konta pārvaldības mērķlapa

Konta pārvaldības mērķlapā tiek izmantoti šādi moduļi.

- **Satura izvietojums** — šis modulis ir konteinera modulis, kas ietver visus moduļus konta pārvaldības mērķlapā.
- **Konta sveiciena elements** — šis modulis tiek izmantots, lai nodrošinātu sveiciena ziņojumu konta pārvaldības lapā. Tajā ir iekļauti virsraksta un elementa izmēra rekvizīti. Rekvizīts **Elementa izmērs** nosaka moduļa platumu satura izvietojuma modulī. Vērtību diapazons ir no **1** līdz **12**, kur **12** ir pilns satura izvietošanas konteinera platums.
- **Konta pasūtījuma izvietošanas elements** — šis modulis tiek izmantots, lai sniegtu kopsavilkumu par pasūtījumu skaitu, ko ievietoja lietotāja konts. Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram un saitei “skatīt detalizētu informāciju”. Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz pasūtījumu vēstures lapu.
- **Konta profila novietojuma elements** — šis modulis tiek izmantots, lai sniegtu lietotāja profila kopsavilkumu. Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram un saitei “skatīt detalizētu informāciju”. Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lietotāja profila lapu.
- **Konta vēlmju elements** — šis modulis tiek izmantots, lai sniegtu elementu kopsavilkumu klienta vēlmju sarakstā. Piemēram, tas var norādīt: “Jūsu vēlmju sarakstā ir 10 elementi.” Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram un saitei “skatīt detalizētu informāciju”. Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz vēlmju saraksta lapu.
- **Konta adreses elements** — šis modulis tiek izmantots, lai sniegtu lietotāja adrešu kopsavilkumu. Piemēram, tas var norādīt: “Jūsu kontam ir pievienotas 2 adreses.” Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram un saitei “skatīt detalizētu informāciju”. Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lietotāja adreses lapu.
- **Konta lojalitātes programmas elements** — šis modulis tiek izmantots, lai parādītu un izveidotu saiti ar informāciju par lojalitātes programmu. Tajā ir iekļauti rekvizīti virsrakstam, elementa izmēram, saitei “skatīt detalizētu informāciju” un saitei “kļūt par dalībnieku”. Saite “skatīt detalizētu informāciju” ir jākonfigurē novirzīšanai uz lojalitātes programmas lapu. Saite “kļūt par dalībnieku” ir jākonfigurē novirzīšanai uz lapu, kur lietotāji var pievienoties lojalitātes programmai.

### <a name="order-history-page"></a>Pasūtījumu vēstures lapa

Pasūtījumu vēstures lapā tiek izmantots pasūtījuma vēstures modulis, lai parādītu visus pēdējos lietotāja veiktos pasūtījumus.

### <a name="order-details-page"></a>Pasūtījumu informācijas lapa

Pasūtījumu informācijas lapa sniedz detalizētu informāciju par katru pasūtījumu, un tai var piekļūt no pasūtījumu vēstures lapas. Tā izmanto pasūtījuma informācijas moduli, kas pieprasa pārdošanas ID vai transakcijas ID, lai izgūtu pasūtījuma informāciju.

### <a name="user-profile-page"></a>Lietotāja profila lapa

Lietotāja profila lapā tiek rādīta lietotāja konta informācija, piemēram, lietotāja vārds un e-pasta adrese. Tā izmanto lietotāja profila moduli. Lai gan e-pasta adresi nevar noņemt, to var rediģēt.

### <a name="user-address-page"></a>Lietotāja adreses lapa

Lietotāja adreses lapā tiek parādīts to adrešu saraksts, kuras ir saistītas ar lietotāja kontu. Lietotājs vai nu sniedzis šīs adreses norēķināšanās laikā, vai arī tās tieši pievienojis šajā lapā. Lietotāja adreses modulis tiek izmantots, lai pievienotu un rediģētu adreses, iestatītu primāro adresi un atveidotu esošās adreses lapā.

### <a name="wish-list-page"></a>Vēlmju saraksta lapa

Vēlmju saraksta lapā ir redzami elementi, kas tika pievienoti klienta vēlmju sarakstā. Tā izmanto vēlmju saraksta moduli, lai atveidotu vēlmju saraksta elementus.

### <a name="loyalty-page"></a>Lojalitātes lapa

Izmantojot lojalitātes programmas lapu, klienti var pievienoties lojalitātes programmai vai, ja tie jau ir lojalitātes programmas dalībnieki, skatīt informāciju par savu programmu. Viņi var arī skatīt punktus, ko nopelnījuši un izpirkuši pēdējās transakcijās.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Container modulis](add-container-module.md)

[Iegādes lodziņa modulis](add-buy-box.md)

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Pasūtījuma apstiprinājuma modelis](order-confirmation-module.md)

[Galvenes modulis](author-header-module.md)

[Kājenes modulis](author-footer-module.md)
