---
title: Lietotāju importēšana no Azure Active Directory
description: Sistēmas administratori var izmantot šo procedūru, lai manuāli importētu konkrētus lietotājus vai lielu skaitu lietotāju no Azure Active Directory.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571009"
---
# <a name="import-users-from-azure-active-directory"></a>Lietotāju importēšana no Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Konkrētu lietotāju importēšana

Sistēmas administratori var izmantot šo procedūru, lai importētu konkrētus lietotājus no Azure Active Directory (Azure AD).

1. Lietotājs tiks importēts kopā ar pašreizējo sesijas uzņēmumu kā noklusējuma uzņēmumu. Pirms lietotāju importēšanas mainiet pašreizējo uzņēmumu, ja piemērojams.
2. Pārejiet uz sadaļu **Sistēmas administrēšana > Lietotāji > Lietotāji**.
3. Noklikšķiniet uz **Importēt lietotājus**.
4. Atlasiet lietotājus, kas jāimportē, un atlasiet **Importēt lietotājus**.

Kad importēšana ir pabeigta, tiks prasīts piešķirt lomas lietotājiem.

## <a name="import-users-in-bulk"></a>Lietotāju lielapjoma importēšana

Sistēmas administratori var izmantot šo procedūru, lai importētu lielu skaitu lietotāju no Azure Active Directory.
Ņemiet vērā, ka, izmantojot partijas importēšanas opciju, nav iespējams atlasīt lietotājus.

## <a name="run-the-import-as-a-batch-job"></a>Palaidiet importēšanu kā pakešuzdevumu
1. Lietotājs tiks importēts kopā ar pašreizējo sesijas uzņēmumu kā noklusējuma uzņēmumu. Pirms lietotāju importēšanas mainiet pašreizējo uzņēmumu, ja piemērojams.
2. Pārejiet uz sadaļu **Sistēmas administrēšana > Lietotāji > Lietotāji**.
3. Noklikšķiniet uz **Partijas importēšana**.
4. Izvērsiet sadaļu **Palaist fonā**.
4. Laukā **Partijas apstrāde** atlasiet **Jā**.
6. Laukā **Partijas grupa** ievadiet vai atlasiet kādu vērtību. Šis solis nav obligāts.  
7. Laukā **Privāts** atlasiet **Jā**. Šis solis nav obligāts.  
8. Laukā **Kritisks darbs** atlasiet **Jā**. Šis solis nav obligāts.  
9. Laukā **Pārraudzības kategorija** atlasiet kādu opciju.
10. Noklikšķiniet uz **Labi**.

Kad importēšana ir pabeigta, tiks prasīts piešķirt lomas lietotājiem.

## <a name="run-in-a-sandbox-environment"></a>Izpilde smilškastes vidē
1. Atlasiet **Partijas importēšana**.
2. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]