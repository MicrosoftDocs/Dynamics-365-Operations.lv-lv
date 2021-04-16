---
title: PVN maksājuma drukāšana pēc koda pārskata
description: Šī tēma sniedz informāciju par iestatījumiem un darbībām, kas nepieciešamas, lai drukātu PVN maksājumu pēc koda pārskata uzskaites vai nodokļu koda valūtā.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815456"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>PVN maksājuma drukāšana pēc koda pārskata 

[!include [banner](../includes/banner.md)]

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]