---
title: Lietotāju importēšana no Azure Active Directory
description: Sistēmas administratori var izmantot šo procedūru, lai manuāli importētu konkrētus lietotājus vai lielu skaitu lietotāju no Azure Active Directory.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679818"
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
4. Laukā **Partijas apstrāde** atlasiet **Jā.
6. Laukā **Partijas grupa** ievadiet vai atlasiet kādu vērtību. Šis solis nav obligāts.  
7. Laukā **Privāts** atlasiet **Jā**. Šis solis nav obligāts.  
8. Laukā **Kritisks darbs** atlasiet **Jā**. Šis solis nav obligāts.  
9. Laukā **Pārraudzības kategorija atlasiet kādu opciju.
10. Noklikšķiniet uz **Labi**.

Kad importēšana ir pabeigta, tiks prasīts piešķirt lomas lietotājiem.

## <a name="run-in-a-sandbox-environment"></a>Izpilde smilškastes vidē
1. Atlasiet **Partijas importēšana**.
2. Atlasiet **Labi**.
