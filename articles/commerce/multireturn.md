---
title: Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos
description: Šajā tēmā ir aprakstīta funkcionalitāte, kas ļauj izmantot atgriešanu vairākos debitoru pasūtījumos un rēķinos programmā Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004462"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos

[!include [banner](includes/banner.md)]


Atgriešanu var veikt vairākos pasūtījumos un rēķinos. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Commerce konfigurēšana, lai atbalstītu atgriešanu vairākos debitoru pasūtījumos un rēķinos

1. Dodieties uz **Commerce parametri \> Debitoru pasūtījumi**.
1. Ieslēdziet parametru **Iespējot atgriešanu vairākiem pasūtījumiem**. 

## <a name="process-returns"></a>Atgriešanu apstrādāšana

Kad šis parametrs ir ieslēgts un izmaiņas ir sinhronizētas uz veikaliem, kasieris veikalā var atlasīt vairākus pārdošanas pasūtījumus vienam debitoram, lai tos atgrieztu.

Kad pasūtījumi ir atlasīti, tiek parādīts saraksts ar visām atgriežamajām precēm visos šo pasūtījumu rēķinos. Pēc tam kasieris var atlasīt atgriežamās preces. Visām atlasītajām precēm tiks izveidots viens atgriešanas pasūtījums.
