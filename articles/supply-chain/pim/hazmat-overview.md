---
title: Bīstamo materiālu pārskats
description: Šī tēma sniedz apskatu par līdzekļiem, kas ir saistīti ar bīstamu materiālu apstrādi un dokumentēšanu preču informācijas pārvaldības un noliktavu pārvaldības laikā.
author: t-benebo
ms.date: 06/10/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: cfea2cd6a2699bdf2a14de72a8bdeb3e8cd32a17
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986280"
---
# <a name="hazardous-materials-overview"></a>Bīstamo materiālu pārskats

[!include [banner](../includes/banner.md)]

Lai saglabātu atbilstību kuģošanas un pārvadāšanas noteikumiem, organizācijām, kas piegādā materiālus, kas klasificēti kā bīstamas preces, ir jāiekļauj papildu dokumenti ar to sūtījumiem. Bīstamo materiālu līdzeklis ļauj klientiem glabāt informāciju, kas saistīta ar izlaistajiem krājumiem. Šo informāciju var izmantot, lai palīdzētu sagatavot nosūtīšanas dokumentus. Organizācijai, kas piegādā bīstamas kravas, ir pašai savi procesi un procedūras, lai pārvaldītu nosūtīšanas procesu. Microsoft Dynamics 365 Supply Chain Management ir tikai rīks, kas var palīdzēt ģenerēt pieprasītos dokumentus.

Sekojošajā diagrammā ir attēlotas darbības, kas jāveic, lai iestatītu un lietotu bīstamo materiālu līdzekli.

![Bīstamo materiālu iestatīšana un izmantošanas līdzeklis.](media/hazmat-overview.png "Bīstamo materiālu iestatīšana un izmantošanas līdzeklis")

Bīstamo materiālu līdzeklis ir iestatīts Preču informācijas pārvaldībā un nodrošina dokumentus, kurus var izdrukāt ar noliktavas pārvaldības starpniecību. Tāpēc vispārīgi runājot, šīs jomas ir divas galvenās jomas, kurās jūs pārskatīsiet, iestatīsit un izmantosiet šī līdzekļa funkcionalitāti:

- **Preču informācijas pārvaldība** - iestatiet kodus, kuri tiks lietoti izlaistajai precei.
- **Noliktavas pārvaldība** – strādājiet ar papildu piegādes dokumentiem, kas tiks drukāti kravām.

> [!IMPORTANT]
> Supply Chain Management norādītie bīstamie materiālu līdzekļi sniedz noderīgus preces informācijas laukus un saistīto funkcionalitāti, kas var palīdzēt reģistrēt un saistīt informāciju, kas saistīta ar jūsu bīstamajām precēm. Šos līdzekļus var arī izmantot, lai izstrādātu un izdrukātu nosūtīšanas dokumentus, kas ietver daļu no tās pašas informācijas par visiem bīstamajiem materiāliem, ko sūtāt. Tomēr sistēma automātiski neliks jums ievērot visus piemērojamos noteikumus jūsu valstī vai reģionā. Lai gan šie rīki ir paredzēti, lai palīdzētu jums ievērot kopīgos noteikumus, tie nav ne pietiekami, ne arī garantē to. Jūsu organizācija ir atbildīga par visu piemērojamo noteikumu pārzināšanu un visu nepieciešamo darbību veikšanu, lai tās izpildītu.

## <a name="product-information-management"></a>Preču informācijas pārvaldība

Preču informācijas pārvaldība nodrošina virkni uzstādījumu tabulu, kurās varat ievadīt atsauces informāciju dažādu bīstamo kravu sarakstiem, kas paredzētas ceļu, gaisa un jūras kravām.

Kad šī funkcionalitāte tika izstrādāta, tika minētas šādas kopējas regulas:

- **ADR** – regulas, kas saistītas ar starptautiskajiem bīstamo kravu autopārvadājumiem
- **KM 49** – Amerikas Savienoto Valstu preču pārvadāšanas noteikumi bīstamo kravu pārvadāšanai
- **IMDG** – SStarptautisko jūras bīstamo kravu kodekss (IMDG) kodekss
- **IATA** – Starptautiskās gaisa transporta asociācijas (IATA) noteikumi par bīstamajām kravām

Katra regulu kopa sniedz standartizētus bīstamo preču un atsauču kodu sarakstus. Tādēļ Supply Chain Management sniedz atsauču tabulu kopīgos kodus šajos sarakstos. Katram sarakstam ir arī daži unikāli kodi, kurus varat definēt.

Lai iegūtu vairāk informācijas par to, kā iestatīt noteikumus un vērtības bīstamiem materiāliem un kā piešķirt vērtības attiecīgajām precēm, skatiet sekojošās tēmas:

- [Bīstamo materiālu iestatīšana](hazmat-setup.md)
- [Bīstamie materiāli precēs, pasūtījumos, sūtījumos un kravās](hazmat-items.md)

## <a name="warehouse-management"></a>Noliktavas vadība

Sagatavojot sūtījumu Noliktavas pārvaldībā, varēsit drukāt vairākus jaunus pārskatus, kas izmanto informāciju, kas iestatīta preču informācijas pārvaldībā. Plašāku informāciju par pieejamiem pārskatiem un to lietošanu skatiet šeit: [Bīstamo materiālu pieprasījumi un pārskati](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]