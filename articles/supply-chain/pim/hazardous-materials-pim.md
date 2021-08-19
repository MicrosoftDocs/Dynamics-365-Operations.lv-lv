---
title: Bīstamie materiāli
description: Šajā tēmā ir sniegta informācija par bīstamiem materiālu dokumentiem un informāciju, kas glabājas jūsu vidē.
author: lachlancashMS
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b64ee1e0fb9a21dfcbdb283dc7a458171150c0f8d5dadd19102c0a788b8badc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777891"
---
# <a name="hazardous-materials"></a>Bīstamie materiāli

[!include [banner](../includes/banner.md)]

Informācija par bīstamiem materiāliem ir iestatīta modulī Preču informācijas pārvaldība. Šis modulis nodrošina arī dokumentus, ko var izdrukāt ar noliktavas vadības starpniecību.

Kad nosūtāt materiālus, kas klasificēti kā bīstamas preces, sūtījumam jāpievieno papildu dokumenti. Bīstamo materiālu funkcionalitāte ļauj klientiem uzglabāt klasifikācijas informāciju un saistīt to ar izlaistajiem krājumiem. Šo informāciju var izmantot, lai palīdzētu sagatavot nosūtīšanas dokumentus.

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Management norādītie bīstamie materiālu līdzekļi sniedz noderīgus preces informācijas laukus un saistīto funkcionalitāti, kas var palīdzēt reģistrēt un saistīt informāciju, kas saistīta ar jūsu bīstamajām precēm. Šos līdzekļus var arī izmantot, lai izstrādātu un izdrukātu nosūtīšanas dokumentus, kas ietver daļu no tās pašas informācijas par visiem bīstamajiem materiāliem, ko sūtāt. Tomēr sistēma automātiski neliks jums ievērot visus piemērojamos noteikumus jūsu valstī vai reģionā. Lai gan šie rīki ir paredzēti, lai palīdzētu jums ievērot kopīgos noteikumus, tie nav ne pietiekami, ne arī garantē to. Jūsu organizācija ir atbildīga par visu piemērojamo noteikumu pārzināšanu un visu nepieciešamo darbību veikšanu, lai tās izpildītu.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]