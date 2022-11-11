---
title: Vietas seguma vispārējā plānošana, ja noliktava ir obligāta
description: Šajā rakstā ir aprakstīts, kā tiek plānots krājums, kam ir vieta seguma dimensijas veidā. Noliktava ir obligāta dimensija.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df58017c25737cc946d09bf86ff7ad8bd33f4176
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741045"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Vietas seguma vispārējā plānošana, ja noliktava ir obligāta

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā tiek plānots krājums, kam ir vieta seguma dimensijas veidā. Noliktava ir obligāta dimensija.

Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:

-   Vietas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma transakcijā. Šo iestatījumu nevar modificēt.
-   Noliktavas dimensija ir iestatīta kā obligāta un tā jāievada pieprasījuma darbībā.
-   Vietas dimensija ir iestatīta seguma plānošanai. Seguma plānošanai var būt iestatītas arī citas dimensijas. Tomēr tās neietekmē šī vairākvietu funkcionalitāte.
-   Noliktavas dimensija seguma plānošanai nav iestatīta. Tāpēc piegādi un pieprasījumu apkopo pēc vietas un, iespējams, arī citas seguma plānotas dimensijas.

Nākamajā grafikā ir attēlots, kā tiek veikta vispārējā plānošana. Parametri, kas izmantoti grafikā, un to atrašanās vietas ir šādas:
-   Krājuma segums tiek definēts krājumam. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces&gt; Izlaistās preces**. Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Krājumu segums**.
-   Uzpildīšanas attiecības ir definētas noliktavai. Noklikšķiniet uz **Krājumu vadība &gt; Iestatījumi &gt; Noliktavu sadalījums &gt; Noliktavas**. Cilnē **Vispārējā plānošana** skatiet lauku grupu **Galvenā noliktava**.
-   Noklusējuma pasūtījuma tips ir iestatīts uz Ražošana, Pirkšanas pasūtījums vai Kanban. Noklikšķiniet uz **Preču informācijas pārvaldība &gt; Preces&gt; Izlaistās preces**. Atlasiet krājumu un pēc tam noklikšķiniet uz **Plānošana &gt; Pasūtījuma noklusējuma iestatījumi**. Formā **Pasūtījuma noklusējuma iestatījumi** skatiet lauku **Noklusējuma pasūtījuma tips** .

![Pieprasīt vietas segumu noliktava obligāta.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Papildu resursi

- [Vispārējās plānošanas un vairākvietu funkcionalitātes pārskats](master-plan-multisite-functionality.md)
- [Galvenais plāns vietas un noliktavas segumam, noliktava ir obligāta](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Vietas seguma vispārējā plānošana, ja noliktava ir obligāta](master-plan-site-coverage-warehouse-mandatory.md)
- [Galvenais plāns vietas un noliktavas segumam, noliktava nav obligāta](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [MK versijas noteikšana](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]