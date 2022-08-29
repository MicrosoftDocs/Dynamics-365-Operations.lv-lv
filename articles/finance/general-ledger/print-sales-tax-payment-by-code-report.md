---
title: PVN maksājumu drukāšana pēc koda pārskata
description: Šajā rakstā ir sniegta informācija par iestatījumiem un darbībām, kas nepieciešamas, lai drukātu PVN maksājumu pēc koda pārskata uzskaites vai nodokļu koda valūtā.
author: AdamTrukawka
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.search.form: ''
ms.openlocfilehash: ea11826d21b66e6283abf24b3f7b0945e6eb9192
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272374"
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

    ![PVN maksājums pēc koda dialoglodziņš.](media/Sales-tax-payment-by-code.png)

Tālāk redzamajā attēlā ir parādīts ģenerēta pārskata piemērs. Pārskats rāda, ka pārskata kodam **101** ir valūta **EUR**, ja **PVN valūtas** lauks ir iestatīts uz **EUR** PVN kodam, kuram ir piešķirts pārskata kods.

![PVN maksājums pēc koda pārskata piemērs.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
