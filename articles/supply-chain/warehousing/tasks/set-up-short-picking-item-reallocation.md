---
title: Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana
description: Šajā procedūrā parādīts kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eae86b307ac8d8539c3897293c2fc21ea57d2d60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148243"
---
# <a name="set-up-short-picking-item-reallocation"></a>Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu. Ir iespējams izmantot automātisku atkārtota sadalījuma procesu, kurā tiek izmantotas atrašanās vietas direktīvas, lai izgūtu preces, ja tās ir pieejamas citā atrašanās vietā. Vai arī, izmantojot manuālu atkārtotu sadalījumu, mobilajā ierīcē tiek parādīts atrašanās vietu saraksts ar pieejamo daudzumu, ļaujot noliktavas darbiniekam izvēlieties atrašanās vietu krājumu izmantošanai. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="set-up-work-exceptions"></a>Iestatīt darba izņēmumus
1. Sadaļā **Navigācijas rūts** pārejiet uz **Noliktavas pārvaldība > Iestatīšana > Darba > Darba izņēmumi**.
2. Klikšķiniet **Jauns**. Ir iespējams definēt vairākus darba izņēmumus ar dažādām krājumu pārdales politikām, kas ļauj noliktavas darbiniekam izvēlieties vienu, pamatojoties uz kravas apstrādes vajadzībām.  
3. Laukā **Darba izņēmuma kods** ierakstiet vērtību. Piešķiriet darba izņēmumam nosaukumu, lai norādītu, kādam nolūkam tas tiek izmantots. Piemēram, Saīsinātas izdošanas rokasgrāmata.  
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Izņēmuma veids** atlasiet 'Saīsinātā izdošana'.
6. Atlasiet izvēles rūtiņu **Krājumu koriģēšana**. Šī opcija norāda, ka krājumi tiks automātiski noregulēti uz vērtību 0 saīsinātas izdošanas atrašanās vietā.  
7. Laukā **Noklusējuma korekcijas veida kods** ievadiet vai atlasiet kādu vērtību. Piemēram, izmantojot USMF, jūs varat atlasīt 'Noņemt Res Adj Out'.  
8. Laukā **Krājuma atkārtots sadalījums** atlasiet 'Manuāls'. Ja atlasāt Manuāls vai Automātisks un manuāls, noliktavas darbiniekam jāļauj izmantot manuālu atkārtotu sadali.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Iestatīt darbinieku manuālas krājuma atkārtotas sadales izmantošanai
1. Aizvērt lapu.
2. Sadaļā **Navigācijas rūts** pārejiet uz **Noliktavas pārvaldība > Iestatīšana > Nodarbinātais**.
3. Noklikšķiniet uz **Rediģēt**.
4. Sarakstā atlasiet darbinieks 24.
5. Izvērsiet kopsavilkuma cilni **Darbs**.
6. Atlasiet 'Jā' laukā **Atļaut manuālu krājuma atkārtotu sadali**.

