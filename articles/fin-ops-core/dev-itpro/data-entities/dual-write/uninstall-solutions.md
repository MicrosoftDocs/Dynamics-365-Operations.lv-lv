---
title: Atinstalēt duālās rakstīšanas programmas orķestrācijas risinājumus
description: Šajā rakstā ir aprakstīts, kā atinstalēt dubultās rakstīšanas programmas instrumentācijas risinājumus.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 676802ddabac69db4947cf806e9103f67cece3de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870379"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Atinstalēt duālās rakstīšanas programmas orķestrācijas risinājumus

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā atinstalēt dubultās rakstīšanas programmas instrumentācijas risinājumus.

Daži debitori nejauši instalē duālās rakstīšanas programmas instrumentālo pakotni, kas instalē vairākus risinājumus savā Microsoft Dataverse vidē. Pakotnes papildu risinājumu instalēšana var izraisīt neparedzētas un kļūdainas problēmas.

Lai novērstu problēmas, kas saistītas ar duālās rakstīšanas programmas instrumentācijas pakotnes instalēšanu, atinstalējiet nevajadzīgos duālās rakstīšanas risinājumus šādā secībā:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (ja tāds ir)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Lai atinstalētu šo risinājumu, ir jāatver atbalsta biļete ar programmu Microsoft.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Ja tika instalēti pušu un globālās adrešu grāmatas risinājumi, atinstalējiet risinājumus šādā secībā:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Puse
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
