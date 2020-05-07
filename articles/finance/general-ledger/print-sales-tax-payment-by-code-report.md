---
title: PVN maksājuma drukāšana pēc koda pārskata
description: Šī tēma sniedz informāciju par iestatījumiem un darbībām, kas nepieciešamas, lai drukātu PVN maksājumu pēc koda pārskata uzskaites vai nodokļu koda valūtā.
author: anasyash
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3c3b251aadfa997f453e60b0842f89a6f09eb9cb
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260259"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>PVN maksājuma drukāšana pēc koda pārskata 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Lai drukātu **PVN maksājumu pēc koda** pārskata, dodieties uz **Nodoklis** \> **Pieprasījumi un pārskati** \> **PVN pārskati** \> **PVN maksājumi pēc koda**. Pēc noklusējuma pārskata summas tiek ģenerētas juridiskās personas uzskaites valūtā visiem pārskata kodiem, kas iestatīti **PVN pārskatu kodu** lapā.

Jūs varat arī ģenerēt šo pārskatu, lai tas parāda PVN maksājumu summas PVN kodu valūtās visiem pārskatu kodiem, kas piešķirti PVN kodiem **PVN kodu** lapā.

## <a name="turn-on-the-feature"></a>Līdzekļa ieslēgšana

**Līdzekļu pārvaldības** darbvietā ieslēdziet tālāk norādīto līdzekli: **Ģenerējiet PVN maksājumu pēc koda pārskata PVN koda valūtā**.

## <a name="run-the-report"></a>Palaist pārskatu

1. Dodieties uz sadaļu **Nodokļi** \> **Pieprasījumi un pārskati** \> **PVN pārskati** \> **PVN maksājums pēc koda**.
2. Laukā **Pārskata valūta** atlasiet vienu no šīm vērtībām:

    - **Uzskaites valūta** — drukāt pārskata summas uzskaites valūtā.
    - **PVN koda valūta** — drukāt pārskatu summas PVN kodu valūtās.

    ![PVN maksājums pēc koda dialoglodziņš](media/Sales-tax-payment-by-code.png)

Tālāk redzamajā attēlā ir parādīts ģenerēta pārskata piemērs. Pārskats rāda, ka pārskata kodam **101** ir valūta **EUR**, ja **PVN valūtas** lauks ir iestatīts uz **EUR** PVN kodam, kuram ir piešķirts pārskata kods.

![PVN maksājums pēc koda pārskata piemērs](media/Sales-tax-payment-by-code-2.png)