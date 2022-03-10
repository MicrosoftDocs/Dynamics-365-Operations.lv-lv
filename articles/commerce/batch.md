---
title: Uzlabota pēc partijas izsekoto krājumu apstrāde
description: Šajā tēmā ir aprakstīta uzlabota pēc partijas izsekoto krājumu apstrāde, kura tiek veikta pārskata grāmatošanas procesa laikā programmā Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 513b6ca84fa71e851a5a3e4275e0b6572789e1eb
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485787"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Uzlabota pēc partijas izsekoto krājumu apstrāde

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīta uzlabota pēc partijas izsekoto krājumu apstrāde, kura tiek veikta pārskata grāmatošanas procesa laikā programmā Microsoft Dynamics 365 Commerce.

Pārdošanas laikā Dynamics 365 Commerce pārdošanas punktā (POS) nevar tvert partijas numurus pēc partijas izsekotajiem krājumiem. Tomēr attiecībā uz noteiktām konfigurācijām, ja programmā Commerce Headquarters pārdošana tiek grāmatota, izmantojot debitoru pasūtījumus vai grāmatojot pārskatu, Commerce sistēma sagaida, ka pastāv derīgi pēc partijas izsekoto krājumu partijas numuri un ka tie tiks izmantoti rēķinu izrakstīšanas procesā.

Ja precēm ir pieejami derīgi partijas numuri, tiek izmantots pārskatu grāmatošanas laikā veiktais debitora pasūtījumu rēķinu un pārdošanas pasūtījumu rēķinu izrakstīšanas process. Ja precēm nav pieejami derīgi partijas numuri, debitora pasūtījumu rēķinu izrakstīšanas process nevar grāmatot, un POS lietotājs saņem kļūdas ziņojumu. Pārskatu grāmatošanai tiek aktivizēts kļūdas stāvoklis pat tad, ja precēm ir ieslēgti negatīvi krājumi.

Commerce uzlabojumi palīdz nodrošināt, ka, ja pēc partijas izsekotiem krājumiem ir iespējoti negatīvie krājumi un krājuma daudzums ir 0 (nulle) vai nav pieejams partijas numurs, šiem krājumiem netiek bloķēta debitora pasūtījuma rēķinu un pārdošanas pasūtījuma rēķinu izrakstīšana pārskata grāmatošanas procesa laikā. Ja partijas numuri nav pieejami, uzlabotā funkcionalitāte pārdošanas rindām izmanto noklusējuma partijas ID.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Noklusējuma partijas ID definēšana, ko izmanto debitoru pasūtījumiem

Lai definētu noklusējuma partijas ID, kas tiek izmantots debitoru pasūtījumiem, izpildiet tālāk norādītās darbības.

1. Programmā Commerce Headquarters dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Commerce parametri**.
1. Cilnes **Debitoru pasūtījumi** kopsavilkuma cilnē **Pasūtījums** ievadiet vērtību laukā **Noklusējuma partijas ID**.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Noklusējuma partijas ID definēšana, ko izmanto pārdošanas pasūtījuma rēķinu izrakstīšanai, izmantojot pārskatu grāmatošanu

Lai definētu noklusējuma partijas ID, ko izmanto pārdošanas pasūtījuma rēķinu izrakstīšanai, izmantojot pārskatu grāmatošanu, izpildiet tālāk norādītās darbības.

1. Programmā Commerce Headquarters dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Commerce parametri**.
1. Cilnes **Grāmatošana** kopsavilkuma cilnē **Krājumu atjaunināšana** ievadiet vērtību laukā **Noklusējuma partijas ID**.

> [!NOTE]
> - Noklusējuma partijas ID funkcionalitāte ir pieejama tikai tad, ja attiecīgajai veikala noliktavai un krājumiem ir iespējoti papildu noliktavas procesi. Turpmākajos laidienos noklusējuma partijas ID funkcionalitāte tiks atbalstīta arī tad, ja netiks iespējots papildu noliktavas pārvaldības process.
> - Commerce versijas 10.0.5. laidienā tika ieviests atbalsts uzlabotai pēc partijas izsekoto krājumu apstrādei izrakstu grāmatošanas laikā neuzlabotiem noliktavas pārvaldības scenārijiem.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
