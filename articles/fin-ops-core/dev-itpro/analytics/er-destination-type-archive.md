---
title: Arhīva ER adresāta tips
description: Šajā tēmā ir sniegta informācija par to, kā konfigurēt arhīva adresātu katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019888"
---
# <a name="ArchiveDestinationType">Arhīva galamērķis</a>

[!include [banner](../includes/banner.md)]

Varat konfigurēt arhīva adresātu katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai. Pamatojoties uz adresāta iestatījumu, ģenerētais dokuments tiek saglabāts kā ER darbu saraksta ieraksta pielikums.

Varat izmantot šo opciju, lai nosūtītu -ģenerēto dokumentu uz Microsoft SharePoint mapi vai Microsoft Azure krātuvi. Opciju **Iespējots** iestatiet uz **Jā**, lai izvadi sūtītu uz galamērķi, kas ir definēts ar atlasīto dokumentu tipu. Atlasei ir pieejami tikai tie dokumentu tipi, kur grupa ir iestatīta uz **Fails**. Dokuments jādefinē sadaļā [tipi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu tipi**. Konfigurēšana ER galamērķiem ir tāda pati kā konfigurēšana dokumentu pārvaldības sistēmai.

[![Lapa Dokumentu tipi](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Atrašanās vieta nosaka, kur fails tiek saglabāts. Kad ir iespējots galamērķis **Arhīvs**, rezultātus var saglabāt darbu arhīvā. Rezultātus varat skatīt sadaļā **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu arhivētie darbi**.

> [!NOTE]
> Atlasiet darbu arhīva dokumenta veidu, pārejot uz sadaļu **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu parametri**. Papildinformāciju skatiet tēmā [Elektronisko pārskatu (EP) veidošanas struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Varat saglabāt failu norādītajā SharePoint mapē. Lai definētu noklusējuma serveri SharePoint, pārejiet uz **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu pārvaldības parametri**. Cilnē **SharePoint** konfigurējiet mapi SharePoint. Pēc tam varat atlasīt to kā mapi, kurā tiks saglabāta ER izvade. Šajā dokumentu tipā jaatlasa atrašanās vieta **SharePoint**.

[![SharePoint mapes atlase](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure krātuve

Kad dokumentu tipa atrašanās vieta ir iestatīta uz **Azure krātuve**, varat failu saglabāt Azure krātuvē.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)
- [Dokumentu pārvaldības konfigurēšana](../../fin-ops/organization-administration/configure-document-management.md)
