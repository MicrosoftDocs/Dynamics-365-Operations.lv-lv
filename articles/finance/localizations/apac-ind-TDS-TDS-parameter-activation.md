---
title: TDS parametru iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt parametrus, lai aktivizētu No kopējo ienākumu summas atskaitītā nodokļa (TDS) funkcionalitāti norādītajos darījumos. Šis ir nepieciešams solis, lai izmantotu No kopējo ienākumu summas atskaitītā nodokļa funkciju.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e0c0c830391b790f3bc066e319a855b44f7e243f4e086144bbafaa6bb2fa1df3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781711"
---
# <a name="set-the-tds-parameters"></a>TDS parametru iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt parametrus, lai aktivizētu No kopējo ienākumu summas atskaitītā nodokļa (TDS) funkcionalitāti norādītajos darījumos. Šis ir nepieciešams solis, lai izmantotu No kopējo ienākumu summas atskaitītā nodokļa funkciju.

1. Dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmatas parametri**.
2. Cilnes **Tiešie nodokļi** sadaļā **No kopējo ienākumu summas atskaitītais nodoklis** iestatiet **Aktivizēt TDS** opciju uz **Jā**, lai aktivizētu TDS funkcionalitāti un tai izmantotās lapas un laukus.
3. Iestatiet opciju **Rēķins** uz **Jā**, lai aktivizētu laukus, kas tiek izmantoti, lai aprēķinātu un atskaitītu TDS rēķina līmenī.
4. Iestatiet opciju **Maksājums** uz **Jā**, lai aktivizētu laukus, kas tiek izmantoti, lai aprēķinātu un atskaitītu TDS maksājuma līmenī.

    [![Tiešie nodokļi cilne.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Cilnē **Numuru sērijas** atrodiet rindu, kur **Atsauces** lauks ir iestatīts uz **Ieturētā nodokļa maksājumu**. Rindas laukā **Numuru sērijas kods** atlasiet numuru sērijas kodu. Numuru sērijas kods tiek lietots, lai ģenerētu dokumentu numurus periodiskā TDS norēķinu procesam.

    > [!NOTE]
    > Lai palaistu periodisko TDS norēķinu procesu, dodieties uz **Nodoklis \> Deklarācijas \> Ieturētais nodoklis \> Ieturētā nodokļa maksājums**.

    [![Cilne Numuru sērijas.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Aizvērt lapu.
