---
title: Vietas seguma vispārējā plānošana, ja noliktava nav obligāta
description: Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram nodrošinājumam ir iestatīta vietas dimensija.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b306fec702f608d00c3459cecd957eb251361c0
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187582"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Vietas seguma vispārējā plānošana, ja noliktava nav obligāta

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram nodrošinājumam ir iestatīta vietas dimensija.

Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:

-   Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā.
-   Noliktavas dimensija nav iestatīta kā obligāta. Noliktava var būt zināma, bet tā netiek izmantota vispārējās plānošanas aprēķinā.
-   Vietas dimensija ir iestatīta seguma plānošanai.
-   Noliktavas dimensija seguma plānošanai nav iestatīta. Tāpēc piegādi un pieprasījumu apkopo pēc vietas un, iespējams, arī citas seguma plānotas dimensijas.

Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana. Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:
-   Krājuma segums tiek definēts krājumam. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**. Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Krājumu segums**.
-   Uzpildīšanas attiecības ir definētas noliktavai. Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**. Cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.
-   Noklusējuma pasūtījuma tips ir iestatīts uz ražošanu, pirkšanas pasūtījumu vai Kanban. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**. Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Pasūtījuma noklusējuma iestatījumi**. Veidlapā **Pasūtījuma noklusējuma iestatījumi**, skatiet lauku **Noklusējuma pasūtījuma tips**.

![Pieprasīt vietas segumu noliktava nav obligāta](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Papildu resursi

[Vispārēja plānošanas un vairākvietu funkcionalitātes pārskats](master-plan-multisite-functionality.md)

[Galvenais plāns vietas un noliktavas segumam, noliktava ir obligāta](master-plan-site-coverage-warehouse-mandatory.md)

[Vietas seguma vispārējā plānošana, ja noliktava ir obligāta](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Vietas seguma vispārējā plānošana, noliktava nav obligāta](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[MK versijas noteikšana](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]