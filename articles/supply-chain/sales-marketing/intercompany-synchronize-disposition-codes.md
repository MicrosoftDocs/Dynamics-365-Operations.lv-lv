---
title: Sinhronizēt izvietojuma kodus
description: Šajā tēmā skaidrots izvietojuma kodu sinhronizācija starpuzņēmumu komercijai
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 04a25324e79a1f9cb30a7da19d648bda995ba7b2
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548394"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Sinhronizēt starpuzņēmumu izvietojuma kodus

[!include [banner](../../includes/banner.md)]

Lai atbalstītu starpuzņēmumu atgriešanas, Microsoft Dynamics 365 Supply Chain Management sniedz funkcionalitāti ārēji definētu izvietojuma kodu kartēšanai uz korespondējošiem iekšējiem izvietojuma kodiem. Kad tiek iestatīta starpuzņēmumu ķēde, izvietojuma darbībām divos savstarpēji kartētos uzņēmumos jābūt vienādām. Ja tie atšķirsies, sinhronizācijas process nebūs veiksmīgs.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Par trīskājainiem tiešās atgriešanas izvietošanas kodiem

Izvietošanas kodi ir sinhronizēti no starpuzņēmumu pārdošanas pasūtījuma rindas uz sākotnējo pārdošanas pasūtījuma rindu. Tomēr sinhronizācijai ir tikai viena tūlītējā ietekme uz sākotnējo pārdošanas pasūtījuma rindu. Šīs sekas ir tas, ka rindas papildmaksas tiek dzēstas, balstoties uz izvietojuma kodu un papildmaksām, kas ir iestatītas Uzņēmumā A. Uzņēmums A ir uzņēmums, kas veido atgriešanas pasūtījumu.

Visas starpuzņēmumu pārdošanas pasūtījuma rindas izvietošanas darbības tiek atbalstītas trīskājainā tiešās piegādes ķēdē. Tomēr gadījumos, kad produkts tiek atgriezts klientam, ir svarīgi apstiprināt, ka piegādes adrese atgriešanas pasūtījumā saskan ar klienta piegādes adresi, kas ir norādīta oriģinālajā pasūtījumā.

> [!NOTE]
> Izvietojuma kodi nepastāv pirkšanas pasūtījumiem. Tāpēc izvietošanas kodu sinhronizācija no starpuzņēmumu pārdošanas pasūtījuma uz oriģinālo atgriešanas pasūtījumu ir jāveic no pārdošanas pasūtījuma uz pārdošanas pasūtījumu.

## <a name="replacing-returned-items"></a>Atgriezto krājumu aizvietošana

Ja atgrieztais krājums tiek aizvietots, un aizvietošanas pasūtījums jau ir ticis izveidots uzņēmumā B, izvietošanas kods nevar tikt atlasīts un uzņēmumā A netiek izveidots papildu aizvietošanas pasūtījums.

## <a name="rules-for-intercompany-direct-deliveries"></a>Starpuzņēmumu tiešo piegāžu kārtulas

Sekojošie vispārējie noteikumi attiecas uz oriģinālajiem atgriešanas pasūtījumiem starpuzņēmumu tiešās piegādes scenārijos:

- Ja oriģinālā pārdošanas pasūtījuma rindas izvietošanas pamatdarbība ir Kredīts un Brāķis, Kredīts, vai Atgriezt klientam, tad piemērotā izvietošanas darbība ir Kredīts. Tomēr darbības kods Atgriezt klientam iestata neto apjomu uz 0 (nulle) esošajā rindā un jaunajā, sinhronizētajā rindā no starpuzņēmumu pārdošanas pasūtījuma. Turklāt, brāķa rindas nekad netiek sinhronizētas. Kad starpuzņēmumu pārdošanas pasūtījumam tiek pievienota rinda, tā nekad nav sinhronizēta pārdošanas pasūtījumam ar pozitīvu daudzumu un brāķa izvietošanas darbībai (piemēram, Kredīts un Brāķis vai Aizvietot un Brāķis).
- Kredīts un Brāķis vai Aizvietot un Aizvietot izvietojuma pamatlīdzinājuma darbība netiek noraidīta. Kredīts un Brāķis vai Aizvietot un Aizvietot izvietojuma pamatlīdzinājuma darbība netiek noraidīta. Šis noteikums tiek piemērots, pat ja uzņēmumā A nav izveidota neviena brāķa rinda un uzņēmumā B nav izveidots aizvietošanas pasūtījums (uzņēmums, kas saņēma atgriezto krājumu). Aizvietošanas pasūtījums tiek izveidots uzņēmumā A tikai tad, kad tiek veikta pavadzīmes atjaunināšana.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
