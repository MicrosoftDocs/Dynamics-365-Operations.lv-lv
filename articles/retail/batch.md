---
title: Uzlabota pēc partijas izsekoto krājumu apstrāde
description: Šajā tēmā ir aprakstīti uzlabojumi, kas ieviesti pēc partijas izsekoto krājumu apstrādē, kura tiek veikta mazumtirdzniecības pārskata grāmatošanas procesa laikā.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617393"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Uzlabota pēc partijas izsekoto krājumu apstrāde

Pārdošanas laikā Microsoft Dynamics 365 for Retail pārdošanas punktā (POS) nevar tvert partijas numurus pēc partijas izsekotajiem krājumiem. Tomēr attiecībā uz noteiktām konfigurācijām, ja galvenajā birojā pārdošana tiek grāmatota, izmantojot debitoru pasūtījumus vai grāmatojot pārskatu, sistēma Microsoft Dynamics sagaida, ka pastāv derīgi pēc partijas izsekoto krājumu partijas numuri un ka tie tiks izmantoti rēķinu izrakstīšanas procesā.

Ja precēm ir pieejami derīgi partijas numuri, tiek izmantots pārskatu grāmatošanas laikā veiktais debitora pasūtījumu rēķinu un pārdošanas pasūtījumu rēķinu izrakstīšanas process. Citādi debitora pasūtījumu rēķinu izrakstīšanas procesu nevar grāmatot, un POS lietotājs saņem kļūdas ziņojumu. Pēc tam pārskatu grāmatošanas procesam tiek aktivizēts kļūdas stāvoklis. Šis kļūdas stāvoklis rodas pat tad, ja precēm ir iespējoti negatīvi krājumi.

Ieviešot uzlabojumus Microsoft Dynamics for Retail 10.0.4 un jaunākās versijās, tika nodrošināts: ja pēc partijas izsekotiem krājumiem ir iespējoti negatīvie krājumi un krājuma daudzums ir 0 (nulle) vai nav pieejams partijas numurs, šiem krājumiem netiek bloķēta debitora pasūtījuma rēķinu un pārdošanas pasūtījuma rēķinu izrakstīšana pārskata grāmatošanas procesa laikā. Ja partijas numuri nav pieejami, jaunā funkcionalitāte pārdošanas rindām izmanto noklusējuma partijas ID.

Lai definētu debitora pasūtījumiem izmantojamo noklusējuma partijas ID, kopsavilkuma cilnes **Pasūtījums** lapas **Mazumtirdzniecības parametri** cilnē **Debitoru pasūtījumi** iestatiet vērtību laukā **Noklusējuma partijas ID**.

Lai definētu pārskatu grāmatošanas laikā pārdošanas pasūtījumu rēķinos izmantojamo noklusējuma partijas ID, kopsavilkuma cilnes **Krājumu atjaunināšana** lapas **Mazumtirdzniecības parametri** cilnē **Grāmatošana** iestatiet vērtību laukā **Noklusējuma partijas ID**.

> [!NOTE]
> Šī funkcionalitāte ir pieejama tikai tad, ja attiecīgajai veikala noliktavai un krājumiem ir iespējoti papildu noliktavas procesi. Turpmākajos laidienos šī funkcionalitāte tiks atbalstīta arī tad, ja netiks izmantots papildu noliktavas pārvaldības process.