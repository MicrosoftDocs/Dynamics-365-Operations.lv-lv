---
title: Eksperimenta statusa pārskatīšana
description: Šajā tēmā ir paskaidrots, kāds ir eksperimenta statuss eksperimenta dzīves ciklā pakalpojumā Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ae459ddaf947db6c3de2602a706390edab49efa1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250862"
---
# <a name="review-the-status-of-an-experiment"></a>Eksperimenta statusa pārskatīšana
Eksperimenta iestatīšana un izpildīšana pakalpojumā Dynamics 365 Commerce ir saistīta ar daudzām darbībām. Informāciju par eksperimenta dzīves ciklu skatiet sadaļā [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).

Lai uzzinātu, kur dzīves ciklā šobrīd atrodas eksperiments, kreisajā navigācijas rūtī Commerce vietņu veidotājā atlasiet **Eksperimenti**. Tiks parādīts eksperimentu saraksts ar katra eksperimenta statusu gan pakalpojumā Commerce, gan trešās puses pakalpojumā, kas tiek izmantots, lai iespējotu eksperimentu veidošanu, variantu piešķiršanu un datu analizēšanu.

Kolonnā **Commerce statuss** var tikt parādītas tālāk norādītās vērtības. 
- **Melnraksts** – eksperiments ir pievienots lapai vai fragmentam pakalpojumā Commerce un tiek rediģēts.
- **Publicēts** – eksperimenta varianti ir gatavi parādīšanai tīmekļa vietnē. Ja eksperiments tiek izpildīts trešās puses pakalpojumā, tīmekļa vietnes lietotāji redzēs lapas vai fragmenta variantu, kuru atlasījis trešās puses pakalpojums.
- **Nepublicēts** – eksperiments vairs nav pieejams vietnē. Pat ja eksperiments tiek izpildīts trešās puses pakalpojumā, tīmekļa vietnes lietotāji redzēs tikai lapas vai fragmenta noklusējuma versiju.
- **Pabeigts** – eksperiments ir izpildīts un variants tika publicēts visu tīmekļa vietnes lietotāju pieejamībai.

Līdzīgi **trešās puses statusa** kolonnā var tikt parādītas tālāk esošās vērtības, lai norādītu, kāds ir eksperimentu statuss trešās puses pakalpojumā.
- **Melnraksts** – eksperiments ir iestatīts trešās puses pakalpojumā, bet nav sākts.
- **Izpilde** – eksperiments tika sākts trešās puses pakalpojumā un veic datu apkopošanu.
- **Apturēts** – eksperiments ir apturēts un nenotiek datu apkopošana. Jums ir jāatsāk eksperiments, lai tas atkal apkopotu datus.
- **Arhivēts** – eksperiments ir izpildīts un tas ir kataloģizēts trešās puses pakalpojumā turpmākai atsaucei.

Diagrammā ir parādītas abas statusu kopas un kā tās ir savstarpēji saistītas.

[ ![Eksperimentu statusi](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]