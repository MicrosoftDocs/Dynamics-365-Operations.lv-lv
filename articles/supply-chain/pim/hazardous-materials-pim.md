---
title: Bīstamie materiāli
description: Šajā tēmā ir sniegta informācija par bīstamiem materiālu dokumentiem un informāciju, kas glabājas jūsu vidē.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208469"
---
# <a name="hazardous-materials"></a>Bīstamie materiāli

[!include [banner](../includes/banner.md)]

Informācija par bīstamiem materiāliem ir iestatīta modulī Preču informācijas pārvaldība. Šis modulis nodrošina arī dokumentus, ko var izdrukāt ar noliktavas vadības starpniecību.

Kad nosūtāt materiālus, kas klasificēti kā bīstamas preces, sūtījumam jāpievieno papildu dokumenti. Bīstamo materiālu funkcionalitāte ļauj klientiem uzglabāt klasifikācijas informāciju un saistīt to ar izlaistajiem krājumiem. Šo informāciju var izmantot, lai palīdzētu sagatavot nosūtīšanas dokumentus.

> [!IMPORTANT]
> Lai palīdzētu pārvaldīt bīstamu preču sūtījumus, Microsoft Dynamics 365 Supply Chain Management ļauj iestatīt papildu atsauces informāciju, kas ir saistīta ar precēm. Varat arī iestatīt papildu nosūtīšanas dokumentus. Tomēr, sistēma nav automātiski atbilstoša jūsu valsts vai reģiona noteikumiem. Tā ir rīks, kas var palīdzēt vispārējai programmai.

Lai varētu lietot šo funkcionalitāti, nepieciešams tālak norādītais iestatījums.

- **Preču informācijas pārvaldība:** iestatiet kodus, kurus var lietot izlaistām precēm.
- **Noliktavas vadība:** lietojiet papildu nosūtīšanas dokumentus, lai drukātu piegādes informāciju.

## <a name="product-information-management"></a>Preču informācijas pārvaldība

Produktu informācijas pārvaldībā ir iekļauta virkne uzstādījumu tabulu, kurās varat pievienot atsauces informāciju, kas tiek sniegta bīstamo kravu sarakstos, kas paredzētas ceļu, gaisa un jūras kravām.

Lūk, daži no noteikumiem, uz kuriem bieži atsaucas.

- **ADR** – regulas, kas saistītas ar starptautiskajiem bīstamo kravu autopārvadājumiem
- **KM 49** – Amerikas Savienoto Valstu preču pārvadāšanas noteikumi bīstamo kravu pārvadāšanai
- **IMDG** – SStarptautisko jūras bīstamo kravu kodekss (IMDG) kodekss
- **IATA** – Starptautiskās gaisa transporta asociācijas (IATA) noteikumi par bīstamajām kravām

Katrai no šīm regulām ir bīstamo preču saraksts, kurā ietilpst atsauču kodi. Saraksti, kas paredzēti katram transporta veidam, tiek apvienoti ar kopīgām starptautiskām klasifikācijām. Piegādes ķēžu pārvaldība sniedz atsauču tabulu kopīgos kodus šajos sarakstos. Katram sarakstam ir arī daži unikāli kodi, kurus var definēt.

Lai sāktu konfigurēt šo informāciju, izveidojiet noteikumu, ko varat izmantot, lai konfigurētu sākotnējos parametrus.

## <a name="warehouse-management"></a>Noliktavas vadība

Kad krava ir sagatavota, var izdrukāt vairākus jaunus pārskatus. Šajos pārskatos izmanto informāciju, kas iestatīta preču informācijas pārvaldībā.
