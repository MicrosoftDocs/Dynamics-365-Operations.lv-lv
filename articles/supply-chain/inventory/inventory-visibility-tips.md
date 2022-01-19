---
title: Krājumu redzamības padomi
description: Šajā tēmā sniegti daži padomi, kurus būtu jāņem vērā, kad iestatāt un izmantojat krājumu redzamības pievienojumprogrammu.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1f6ade36ac184a3c8bf790fc0d899ea01d90c8d2
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952419"
---
# <a name="inventory-visibility-tips"></a>Krājumu redzamības padomi

[!include [banner](../includes/banner.md)]

Šeit sniegti daži padomi, kas jāievēro, iestatot un lietojot pievienojumprogrammu Krājumu redzamība:

- Pašlaik krājumu redzamības pievienojumprogramma atbalsta tikai vides, Microsoft Dataverse kas izveidotas, izmantojot Microsoft Dynamics lifecycle Services (LCS). Ja vide tika izveidota citādi Dataverse (piemēram, izmantojot administrēšanas centru) un ja tā ir saistīta ar vidi, vispirms jālūdz krājumu redzamības produktu komandai labot kartēšanas Power Apps Dynamics 365 Supply Chain Management problēmu. Varat sazināties ar darba grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Komanda ļaus jums zināt, kad jūsu vide ir gatava instalēt Krājumu redzamību.
- Ja ir vairāk nekā viena LCS vide, izveidojiet atšķirīgu Azure Active Directory Azure AD () programmu katrai videi. Ja lietojat vienu lietojumprogrammas ID un nomnieka ID, lai instalētu Inventory Visibility lietojumprogrammu atšķirīgām vidēm, vecākām vidēm tiks rādīta marķiera problēma. Ir derīga tikai pēdējā instalētā krājumu redzamības pievienojumprogrammas instance.
- Mākonī viesotajām vidēm krājumu redzamība pašlaik netiek atbalstīta. Tas tiek atbalstīts tikai pakāpju-2+ vidēm.
- Programmas programmēšanas interfeiss (API) pašlaik atbalsta vaicājumus līdz 100 atsevišķiem krājumiem pēc `ProductID` vērtības. Katrs `SiteID``LocationID` vaicājumā var norādīt vairākas vērtības. Maksimālais ierobežojums ir definēts `NumOf(SiteID) * NumOf(LocationID) <= 100` kā.
- Lielapjoma API var atgriezt maksimāli 512 ierakstus katram pieprasījumam.
- Datu `fno` avots ir rezervēts Piegādes ķēžu pārvaldībai. Ja krājumu redzamības pievienojumprogramma ir integrēta Piegādes ķēdes pārvaldības vidē, mēs iesakām nedzēšam konfigurācijas, kas saistītas `fno`[ar datu](inventory-visibility-configuration.md#data-source-configuration) avotu.
- Krājumu redzamību nevar mainīt datu avota `fno` datus. Datu plūsma ir vienvirziena, kas nozīmē, ka visām daudzuma izmaiņām `fno` datu avotam ir jābūt no jūsu Piegādes ķēžu pārvaldības vides. Tādēļ jūs nevarat izmantot API, lai nosūtītu rīcībā esošos izmaiņu vai rezervēšanas pieprasījumus datu `fno` avotam.
- Ja pievienosiet vienu vai vairākus jaunus pasākumus jūsu Piegādes ķēdes pārvaldības videi, jums tie jāpievieno arī krājumu redzamībai. Tomēr visām daudzuma izmaiņām jaunam daudzumam ir jābūt no Jūsu Piegādes ķēdes pārvaldības vides.
- Nodalījuma [konfigurācija pašlaik sastāv no divām](inventory-visibility-configuration.md#partition-configuration) pamatdimensijām `SiteId``LocationId` (un), kas norāda, kā dati tiek sadalīti. Operācijas vienā un tajā pašā nodalījumā var piegādāt lielāku veiktspēju par zemākām izmaksām. Risinājums ietver šo nodalījuma konfigurāciju pēc noklusējuma. Tādēļ *to nav jādefinē* pats. Ne pielāgojiet noklusējuma nodalījuma konfigurāciju. Ja to dzēšat vai maināt, iespējams, radusies negaidīta kļūda.
- Pamatdimensijas, kas ir definētas nodalījuma konfigurācijā, nav jādefinē [preču indeksa hierarhijas konfigurācijā.](inventory-visibility-configuration.md#index-configuration)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
