---
title: Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos
description: Šajā tēmā ir aprakstīta funkcionalitāte, kas ļauj izmantot atgriešanu vairākos debitoru pasūtījumos un rēķinos programmā Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760254"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos

[!include [banner](includes/banner.md)]


Šajā rakstā ir aprakstīti divi līdzekļi, kas optimizē debitora pasūtījumu atgriešanu vairākos rēķinos. 

## <a name="enable-refunds-over-multiple-captures"></a>Iespējot atmaksas vairākos tvērumos

Šis līdzeklis aktivizē vairākas saistītās atmaksas vienā un tajā pašā debitora pasūtījumā. 

1. Dodieties uz darbvietu **Līdzekļu pārvaldība** un meklējiet **Iespējot atmaksas vairākos tvērumos**.
2. Atlasiet **Iespējot atmaksas vairākos pasūtījumos** un pēc tam noklikšķiniet uz **Iespējot**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai

Šis līdzeklis nodrošina, ka gadījumā, ja pasūtījums tiek atgriezts vairākus rēķinos, nodokļi beigās būs vienādi ar sākotnēji iekasēto nodokļu summu. 

1. Dodieties uz darbvietu **Līdzekļu pārvaldība** un meklējiet **Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai**.
2. Atlasiet **Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai** un pēc tam noklikšķiniet uz **Iespējot**. 


## <a name="process-returns"></a>Atgriešanu apstrādāšana

Kad šie līdzekļi ir ieslēgti un izmaiņas ir sinhronizētas uz veikaliem, kasieris veikalā var atlasīt vairākus pārdošanas pasūtījumus vienam debitoram, lai tos atgrieztu.

Kad pasūtījumi ir atlasīti, tiek parādīts saraksts ar visām atgriežamajām precēm visos šo pasūtījumu rēķinos. Pēc tam kasieris var atlasīt atgriežamās preces. Visām atlasītajām precēm tiks izveidots viens atgriešanas pasūtījums.

Ja pasūtījums tiek pilnībā atgriezts, debitoram atgriezto nodokļu summa būs vienāda ar sākotnēji iekasēto nodokļu summu.

