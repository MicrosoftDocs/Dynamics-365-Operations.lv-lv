---
title: Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos
description: Šajā tēmā ir aprakstīta funkcionalitāte, kas ļauj izmantot atgriešanu vairākos debitoru pasūtījumos un rēķinos programmā Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2019
ms.locfileid: "373072"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Dynamics 365 for Finance and Operations versijā 10.0 atgriešanu var veikt vairākos pasūtījumos un rēķinos, bet laidienos pirms versijas 10.0 atgriešanu vienlaikus varēja apstrādāt tikai vienam rēķinam. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Retail konfigurēšana, lai atbalstītu atgriešanu vairākos debitoru pasūtījumos un rēķinos

1. Dodieties uz **Retail parametri \> Debitoru pasūtījumi**.
1. Ieslēdziet parametru **Iespējot atgriešanu vairākiem pasūtījumiem**. 

## <a name="process-returns"></a>Atgriešanu apstrādāšana

Kad šis parametrs ir ieslēgts un izmaiņas ir sinhronizētas uz veikaliem, kasieris veikalā var atlasīt vairākus pārdošanas pasūtījumus vienam debitoram, lai tos atgrieztu.

Kad pasūtījumi ir atlasīti, tiek parādīts saraksts ar visām atgriežamajām precēm visos šo pasūtījumu rēķinos. Pēc tam kasieris var atlasīt atgriežamās preces. Visām atlasītajām precēm tiks izveidots viens atgriešanas pasūtījums.