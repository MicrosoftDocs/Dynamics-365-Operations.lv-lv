---
title: Vietas un noliktavas segums vispārējā plānošana, ja noliktava nav obligāta
description: Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensijas ir vieta un noliktava. Noliktavas dimensija nav obligāta.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6b9814a0a5a069d945c7888da17348ecfe4d4a7
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187534"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Vietas un noliktavas segums vispārējā plānošana, ja noliktava nav obligāta

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā tiek plānots krājums, kuram kā nodrošinājuma dimensijas ir vieta un noliktava. Noliktavas dimensija nav obligāta.

Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:

-   Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā. Šo iestatījumu nevar modificēt.
-   Noliktavas dimensija nav iestatīta kā obligāta. Noliktava var būt zināma, bet tā netiek izmantota vispārējās plānošanas aprēķinā.
-   Vieta un noliktavas dimensija ir iestatīti seguma plānošanai. Seguma plānošanai var iestatīt arī citas dimensijas. Tomēr tās neietekmēs daudzvietu funkcija.

Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana. Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:
-   Noliktava iestatīta kā Manuāli. Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**. Kopsavilkuma cilnē **Vispārējā plānošana** skatiet lauku **Manuāls**.
-   Krājuma segums tiek definēts krājumam. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces&gt; Izlaistās preces**. Atlasiet krājumu un pēc tam darbību rūts cilnē **Plāns** noklikšķiniet uz **Krājumu segums**.
-   Uzpildīšanas attiecības ir definētas noliktavai. Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**. Kopsavilkuma cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.
-   Noklusējuma pasūtījuma tips ir iestatīts uz Ražošana, Pirkšanas pasūtījums vai Kanban. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces&gt; Izlaistās preces**. Atlasiet krājumu un pēc tam darbību rūts cilnē **Plāns** noklikšķiniet uz **Pasūtījuma noklusējuma iestatījumi**. Formā **Pasūtījuma noklusējuma iestatījumi** skatiet lauku **Noklusējuma pasūtījuma tips** .

![Pieprasīt vietu un noliktavu, noliktavu nē](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Papildu resursi

[Vispārēja plānošanas un vairākvietu funkcionalitātes pārskats](master-plan-multisite-functionality.md)

[Vietas seguma vispārējā plānošana, ja noliktava ir obligāta](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Galvenais plāns vietas un noliktavas segumam, noliktava ir obligāta](master-plan-site-coverage-warehouse-mandatory.md)

[Galvenais plāns vietas un noliktavas segumam, noliktava nav obligāta](master-plan-site-coverage-warehouse-not-mandatory.md)

[MK versijas noteikšana](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]