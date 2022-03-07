---
title: Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana
description: Šajā tēmā ir izskaidrots, kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu.
author: Mirzaab
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fe17246037a35e44d12476f184af3bd4c806022
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565236"
---
# <a name="set-up-short-picking-item-reallocation"></a>Saīsinātas izdošanas krājuma atkārtotas sadales iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir izskaidrots, kā ļaut noliktavas darbiniekiem ātri atrast alternatīvas atrašanās vietas, ja atrašanās vietā, uz kuru viņi tika novirzīti, nav pietiekami daudz krājumu. 

Atkārtotas sadales procesu kontrolē **Darba izņēmums** un izmanto noliktavā **nodarbinātais.**

Ir iespējams izmantot automātisku, manuālu vai šos abus atkārtotas sadales procesus.

- Automātiska atkārtota sadale — novietojuma direktīvas tiek izmantotas, lai noteiktu, vai preces ir pieejamas citā atrašanās vietā. Ja tas ir iespējams, darbs tiks atjaunināts un noliktavas darbinieks tiks novirzīts uz alternatīvu atrašanās vietu.
- Manuāla atkārtota sadale — ļauj noliktavas darbiniekam izvēlēties no vienas vai vairākām atrašanās vietām, kurās ir nerezervēti preču daudzumi. 
- Automātiska un manuāla — ja sistēma nevar veikt automātisku atkārtotu sadali, un ir pieejamas atrašanās vietas ar nerezervētiem daudzumiem, lietotājam tiks rādīts uzaicinājums atlasīt atrašanās vietu.

## <a name="set-up-work-exceptions"></a>Iestatīt darba izņēmumus
Ir iespējams definēt vairākus darba izņēmumus ar dažādām krājumu pārdales politikām, kas ļauj noliktavas darbiniekam izvēlieties vienu, pamatojoties uz kravas apstrādes vajadzībām.

Šīs procedūras izveidošanai tika izmantots demonstrācijas datu uzņēmums USMF.

1. Sadaļā **Navigācijas rūts** pārejiet uz **Noliktavas pārvaldība > Iestatīšana > Darba > Darba izņēmumi**.
2. Klikšķiniet **Jauns** 
3. Laukā **Darba izņēmuma kods** ierakstiet vērtību. Šis ir izņēmuma nosaukums. Piemēram, Saīsinātas izdošanas rokasgrāmata.
4. Laukā **Apraksts** ierakstiet kādu vērtību. Šis ir izņēmuma lietojuma īss apraksts. Piemēram, Saīsinātā izdošana — krājums nav pieejams.
5. Veida laukā **Izņēmums** atlasiet **Saīsinātā izdošana**.
6. Atlasiet izvēles rūtiņu **Krājumu koriģēšana**. Ja atlasīsit šo opciju, krājumi tiks automātiski noregulēti uz vērtību 0 saīsinātas izdošanas atrašanās vietā.
7. Laukā **Noklusējuma korekcijas veida kods** ievadiet vai atlasiet kādu vērtību. Piemēram, USMF varat atlasīt **Noņemt Res Adj Out**. Katrs korekcijas tipa kods ietver četrus raksturlielumus: nosaukumu, aprakstu, krājumu žurnāla nosaukumu un **Noņemt rezervācijas**. Ja ir iespējota opcija **Noņemt rezervācijas**, saīsināti izdotā pasūtījuma rindas rezervācijas tiks noņemtas.  
8. Laukā **Krājumu atkārtota sadale** atlasiet vērtību, piemēram, Manuāla. Ja atlasāt Manuāls vai Automātisks un manuāls, noliktavas darbiniekam jāļauj izmantot manuālu atkārtotu sadali.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Iestatīt darbinieku manuālas krājuma atkārtotas sadales izmantošanai

Šīs procedūras izveidošanai tika izmantots demonstrācijas datu uzņēmums USMF.

1. Aizvērt lapu.
2. Sadaļā **Navigācijas rūts** pārejiet uz **Noliktavas pārvaldība > Iestatīšana > Nodarbinātais**.
3. Noklikšķiniet uz **Rediģēt**.
4. Sarakstā atlasiet nodarbināto. Piemēram, Jūlija Funderburka.
5. Izvērsiet kopsavilkuma cilni **Lietotāji**.
6. Sarakstā atlasiet **Lietotāja ID**. Piemēram, 24.
7. Izvērsiet kopsavilkuma cilni **Darbs**.
8. Laukā **Atļaut manuālu krājuma atkārtotu sadali** atlasiet vērtību **Jā**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]