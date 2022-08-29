---
title: NF-e XML failu kā pielikumu pārvietošana
description: Šajā rakstā skaidrots, kā pārvietot NF-e XML Microsoft Dynamics failus no jūsu 365 Finansu Dynamics 365 Supply Chain Management vai datu bāzes, un tā vietā padarīt tos pieejamus kā pielikumus.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 7bb0fb975c6d73cc4e990b39ea9b5a0c0455db74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270630"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>NF-e XML failu kā pielikumu pārvietošana

[!include [banner](../includes/banner.md)] 


Kad elektroniskie finanšu dokumenti (NF-e) ir izsniegti, XML Microsoft Dynamics faili tiek izveidoti un saglabāti 365 Finanšu un Dynamics 365 Supply Chain Management datu bāzēs. Brazīlijas lokalizācijā varat izmantot **NF-e XML** pārvietošanas kā pielikuma līdzekli, lai atbrīvotu datubāzes vietu, ko izmanto šie XML faili.

Funkcija konkrētam datumu diapazonam un finanšu iestādei pārvieto NF e XML failus no Finanšu vai piegādes ķēžu pārvaldības datu bāzes uz BLOB krātuvi no Jūsu Azure abonementa. Šī kustība padara failus pieejamus tikai kā pielikumus. Pēc XML failu veiksmīgas pārvietošanas uz BLOB krātuvi, oriģinālie faili tiek dzēsti no Finanšu vai piegādes ķēžu pārvaldības datu bāzes. Tāpēc vieta datu bāzē, kurā tiek atbrīvoti izmantotie faili.

Izpildiet šīs darbības, lai iespējotu **NF-e XML pārvietošanas kā pielikuma** līdzekli.

1. Finanšu vai piegādes ķēžu pārvaldībā atveriet līdzekļu **pārvaldības darbvietu**.
2. **Cilnē Viss** meklējiet un atlasiet **NF-e XML pārvietošanas kā pielikuma** līdzekli.
3. Atlasiet **Iespējot tagad**.

Sekojiet šiem soļiem, lai NF-e XML failus pārvietotu kā pielikumus.

1. Pārejiet uz **debitoru parādu** \> **finanšu dokumentiem** \> **elektronisko finanšu dokumentu** \> **pārvietošanas NF-e XML kā pielikumus.**
2. Laukos **No datuma** un **Līdz datumam** atlasiet sākuma un beigu datumus.
3. Laukā **Finanšu iestādes ID** atlasiet vērtību.
4. Atlasiet **Labi**.

> [!IMPORTANT]
> Šis process ir neatgriezenisks. Pēc NF e XML failu pārvietošanas lietotāji var **tos skatīt, tikai atlasot pielikumus** finanšu **dokumenta lapas** augšpusē.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
