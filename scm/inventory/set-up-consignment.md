---
title: "Sūtījuma iestatīšana"
description: "Šajā tēmā ir paskaidrots, kā konfigurēt ienākošo sūtījumu krājumu darbības."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7268b59e0cd550178367e08284b2c3a417b33498
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-consignment"></a>Sūtījuma iestatīšana

[!include[banner](../includes/banner.md)]


Šajā tēmā ir paskaidrots, kā konfigurēt ienākošo sūtījumu krājumu darbības. 

Sūtījuma krājumi ir krājumi, kas pieder kreditoram, bet tiek glabāti jūsu bāzes vietā. Kad esat gatavs patērēt vai izmantot krājumu, jūs pārņemat krājuma īpašumtiesības. Šajā tēmā ir aprakstīta iestatīšana, kas ir nepieciešama, lai nodrošinātu sūtījuma procesus. Plašāku informāciju par sūtījuma procesiem skatiet sadaļā [Sūtījums](consignment.md).

## <a name="inventory-owners"></a>Krājumu īpašnieki
Lai ierakstītu fizisko ienākošo sūtījumu krājumu, nepieciešams definēt kreditora īpašnieku. Tas tiek veikts lapā **Krājumu īpašnieks**. Atlasot **Kreditora konts**, tiek izveidotas noklusētās vērtības laukiem **Nosaukums** un **Īpašnieks**. Vērtība laukā **Īpašnieks** būs redzama kreditoram, tāpēc jūs varētu vēlēties to mainīt, ja jūsu kreditora kontu nosaukumi nav viegli atpazīstami citiem cilvēkiem. Iespējams rediģēt lauku **Īpašnieks**, bet tikai līdz brīdim, kad saglabājat ierakstu **Krājumu īpašnieks**. Lauks **Nosaukums** tiek aizpildīts ar puses nosaukumu, ar kuru ir saistīts kreditora konts, un to nevar mainīt. 

[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Izsekošanas dimensijas grupa
Krājumus, kas tiks izmantoti sūtījuma procesos, nepieciešams saistīt ar **Izsekošanas dimensijas grupa**, kur dimensija **Īpašnieks** ir iestatīta uz **Aktīvs**. Īpašnieka dimensijai vienmēr ir atlasītas opcijas **Fiziskie krājumi** un **Finanšu krājumi**. **Vajadzības plāns pa dimensijām** nekad netiek atlasīts. 

[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Krājumu īpašumtiesību izmaiņu žurnāls
**Krājumu īpašumtiesību izmaiņu**žurnāls tiek izmantots, lai ierakstītu sūtījuma krājumu īpašumtiesību maiņu no kreditora uz pašreizējo juridisko personu, kas to patērē. Kā jebkuram krājumu žurnālam, tam jābūt norādītam Krājumu žurnāla nosaukumam. Šie nosaukumi tiek izveidoti lapā **Krājumu žurnālu nosaukumi**, un **Žurnāla tips** jābūt iestatītam uz **Īpašumtiesību izmaiņa**. 

[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Kreditora sadarbība sūtījuma procesos
Ja jūsu kreditoriem ir kreditoru sadarbības interfeiss, viņi var izmantot šo, lai pārraudzītu krājumu patēriņu jūsu bāzes vietā. Lai iegūtu papildu informāciju par kreditoru iestatīšanu kreditoru sadarbības izmantošanai, skatiet [Drošības konfigurācija kreditoru sadarbības lietotājiem](../procurement/configure-security-vendor-portal-users.md).



