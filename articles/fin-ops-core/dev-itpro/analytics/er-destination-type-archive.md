---
title: Arhīva ER adresāta tips
description: Šajā rakstā ir sniegta informācija par to, kā konfigurēt arhīva mērķi katrai mapei vai faila komponentam elektronisko pārskatu (ER) formātā.
author: kfend
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: d907bf391c0629d62da489cea90a05eabaf69ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285461"
---
# <a name="archive-er-destination-type"></a>Arhīva ER adresāta tips

[!include [banner](../includes/banner.md)]

Varat konfigurēt arhīva adresātu katram **Mapes** vai **Faila** komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai. Pamatojoties uz adresāta iestatījumu, ģenerētais dokuments tiek saglabāts kā ER darbu saraksta ieraksta pielikums. Lai skatītu rezultātus, atveriet sadaļu **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu darbi**.

Varat izmantot šo opciju, lai nosūtītu -ģenerēto dokumentu uz Microsoft SharePoint mapi vai Microsoft Azure krātuvi. Opciju **Iespējots** iestatiet uz **Jā**, lai izvadi sūtītu uz galamērķi, kas ir definēts ar atlasīto dokumentu tipu. Atlasei ir pieejami tikai tie dokumentu tipi, kur grupa ir iestatīta uz **Fails**. Dokuments jādefinē sadaļā [tipi](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) at **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu tipi**. Konfigurēšana ER galamērķiem ir tāda pati kā konfigurēšana dokumentu pārvaldības sistēmai.

[![Lapa Dokumentu tipi.](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Atrašanās vieta nosaka, kur fails tiek saglabāts. Kad ir iespējots galamērķis **Arhīvs**, rezultātus var saglabāt darbu arhīvā. Rezultātus varat skatīt sadaļā **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu arhivētie darbi**.

> [!NOTE]
> Atlasiet darbu arhīva dokumenta veidu, pārejot uz sadaļu **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu parametri**. Papildinformāciju skatiet tēmā [Elektronisko pārskatu (EP) veidošanas struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Varat saglabāt failu norādītajā SharePoint mapē. Lai definētu noklusējuma serveri SharePoint, pārejiet uz **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu pārvaldības parametri**. Cilnē **SharePoint** konfigurējiet mapi SharePoint. Pēc tam varat atlasīt to kā mapi, kurā tiks saglabāta ER izvade. Šajā dokumentu tipā jaatlasa atrašanās vieta **SharePoint**.

[![Risinājuma SharePoint mapes atlase.](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure krātuve

Kad dokumentu tipa atrašanās vieta ir iestatīta uz **Azure krātuve**, varat failu saglabāt Azure krātuvē.

> [!NOTE] 
> ER struktūra pastāvīgi glabā failus Azure Blob krātuvē atšķirībā no datu pārvaldības struktūras, kas piemēro septiņu dienu saglabāšanas politiku dokumentiem, kas ir jāapstrādā. Papildinformāciju skatiet šeit: [API ziņojuma statusa iegūšanai](../data-entities/recurring-integrations.md#api-for-getting-message-status) un [Stāvokļa pārbaudes API](../data-entities/data-management-api.md#status-check-api). Ar ER saistītie faili tiks glabāti Azure Blob krātuvē kā pielikumi programmas tabulas ierakstiem tik ilgi, cik nepieciešams. Viens fails tiks dzēsts no Azure Blob krātuves kopā ar programmas tabulas ierakstu, kuram šis fails tika pievienots.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)
- [Dokumentu pārvaldības konfigurēšana](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
