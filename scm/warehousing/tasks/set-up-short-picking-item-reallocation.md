--- 
title: "Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana"
description: "Šajā procedūrā parādīts kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedd815cddfea4e00ed61ec6e176b633468c8fb2
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu. Ir iespējams izmantot automātisku atkārtota sadalījuma procesu, kurā tiek izmantotas atrašanās vietas direktīvas, lai izgūtu preces, ja tās ir pieejamas citā atrašanās vietā. Vai arī, izmantojot manuālu atkārtotu sadalījumu, mobilajā ierīcē tiek parādīts atrašanās vietu saraksts ar pieejamo daudzumu, ļaujot noliktavas darbiniekam izvēlieties atrašanās vietu krājumu izmantošanai. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.


## <a name="set-up-work-exceptions"></a>Iestatīt darba izņēmumus
1. Dodieties uz Noliktavas vadība > Iestatīšana > Darbs > Darba izņēmumi.
2. Noklikšķiniet uz Jauns.
    * Ir iespējams definēt vairākus darba izņēmumus ar dažādām krājumu pārdales politikām, kas ļauj noliktavas darbiniekam izvēlieties vienu, pamatojoties uz kravas apstrādes vajadzībām.  
3. Laukā Darba izņēmuma kods ierakstiet vērtību.
    * Piešķiriet darba izņēmumam nosaukumu, lai norādītu, kādam nolūkam tas tiek izmantots. Piemēram, Saīsinātas izdošanas rokasgrāmata.  
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Izņēmuma tips atlasiet 'Saīsinātā izdošana'.
6. Atlasiet izvēles rūtiņu Krājumu koriģēšana.
    * Šī opcija norāda, ka krājumi tiks automātiski noregulēti uz vērtību 0 saīsinātas izdošanas atrašanās vietā.  
7. Laukā Noklusējuma korekcijas veida kods ievadiet vai atlasiet kādu vērtību.
    * Piemēram, izmantojot USMF, jūs varat atlasīt 'Noņemt Res Adj Out'.  
8. Laukā Krājuma atkārtots sadalījums atlasiet 'Manuāls'.
    * Ja atlasāt Manuāls vai Automātisks un manuāls, noliktavas darbiniekam jāļauj izmantot manuālu atkārtotu sadali.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Iestatīt darbinieku manuālas krājuma atkārtotas sadales izmantošanai
1. Aizvērt lapu.
2. Dodieties uz Noliktavas vadība > Iestatīšana > Nodarbinātais.
3. Noklikšķiniet uz Rediģēt.
4. Sarakstā atlasiet darbinieks 24.
5. Izvērsiet sadaļu Darbs.
6. Atlasiet Jā laukā Atļaut manuālu krājuma atkārtotu sadali.


