---
title: Vietas un noliktavas segums vispārējā plānošana, ja noliktava ir obligāta
description: Šajā rakstā ir aprakstīts, kā tiek plānots krājums ar vietu un noliktavu kā vajadzības dimensijas. Noliktavas dimensija ir obligāta.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcb2d41ff70714b6bc9c28f3e23ce95f5292f2e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740064"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Vietas un noliktavas segums vispārējā plānošana, ja noliktava ir obligāta

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā tiek plānots krājums ar vietu un noliktavu kā vajadzības dimensijas. Noliktavas dimensija ir obligāta.

Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:

-   Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā.
-   Noliktavas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma darbībā.
-   Vieta un noliktavas dimensija ir iestatīta seguma plānošanai. Seguma plānošanai var iestatīt arī citas dimensijas. Tomēr tās neietekmēs daudzvietu funkcija.

Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana. Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:
-   Noliktavas iestatījums ir **Manuāli**. Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**. Kopsavilkuma cilnē **Vispārējā plānošana** skatiet lauku **Manuāls**.
-   Krājuma segums tiek definēts krājumam. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces&gt; Izlaistās preces**. Atlasiet krājumu un pēc tam darbību rūts cilnē **Plāns** noklikšķiniet uz **Krājumu segums**.
-   Uzpildīšanas attiecības ir definētas noliktavai. Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**. Kopsavilkuma cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.
-   Noklusējuma pasūtījuma tips ir iestatīts uz Ražošana, Pirkšanas pasūtījums vai Kanban. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces&gt; Izlaistās preces**. Atlasiet krājumu un pēc tam darbību rūts cilnē **Plāns** noklikšķiniet uz **Pasūtījuma noklusējuma iestatījumi**. Formā **Pasūtījuma noklusējuma iestatījumi** skatiet lauku **Noklusējuma pasūtījuma tips** .

![Pieprasīt vietas un noliktavas segumu, ja obligāts.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Papildu resursi

- [Vispārējās plānošanas un vairākvietu funkcionalitātes pārskats](master-plan-multisite-functionality.md)
- [Vietas seguma vispārējā plānošana, ja noliktava ir obligāta](master-plan-site-coverage-warehouse-mandatory.md)
- [Vietas seguma vispārējā plānošana, noliktava nav obligāta](master-plan-site-coverage-warehouse-not-mandatory.md)
- [Galvenais plāns vietas un noliktavas segumam, noliktava nav obligāta](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [MK versijas noteikšana](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]