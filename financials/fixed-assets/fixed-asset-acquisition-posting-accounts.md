---
title: "Pamatlīdzekļu iegādes grāmatošanas konti"
description: "Šajā rakstā ir paskaidrots, kā iestatīt virsgrāmatas grāmatošanas kontus līdzekļu iegādei."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d89bff85317a6aee952d32a9c29f0ebdd27934ec
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-acquisition-posting-accounts"></a>Pamatlīdzekļu iegādes grāmatošanas konti

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots, kā iestatīt virsgrāmatas grāmatošanas kontus līdzekļu iegādei.

Pamatlīdzekļu iegādes grāmatošanai izmantotie konti ir atkarīgi no metodes, kādā līdzeklis tiek iegādāts. Lapā Pamatlīdzekļu grāmatošanas metodes, cilnē Virsgrāmatas konti atlasiet Iegāde un Iegādes korekcija, lai iestatītu pamatlīdzekļu kontus grāmatošanai virsgrāmatā. 

Žurnālos un pirkšanas pasūtījumos Virsgrāmatas konts parasti ir bilances konts, kur jaunā pamatlīdzekļa iegādes vērtība tiek ierakstīta debetā. Šis konts netiek parādīts žurnālā un to nevar aizstāt transakcijās. 

Korespondējošais konts ir arī bilances konts. Virsgrāmatas žurnālā un pamatlīdzekļu žurnālā šis konts bieži mēdz būt bankas konts, ko lieto, lai maksātu par pamatlīdzekļa iegādi. Korespondējošais konts ir noklusējuma konts, kas tiek norādīts žurnālos. Žurnālā to var nomainīt ar jebkuru citu kontu no kontu plāna vai ar kreditora kontu, ja pamatlīdzeklis tika pirkts no kreditora. 

Ja pamatlīdzekļu iegādei modulī Kreditori tiek lietots vienums Rēķinu žurnāls vai Pirkšanas pasūtījumi, tad pamatlīdzekļu transakcijas korespondējošais konts tiek aizstāts ar šai transakcijai atlasīto kreditora kontu.

Iegādēm, kas tiek grāmatotas, virsgrāmatā izmantojot žurnālu Krājumi pamatlīdzekļiem, pamatlīdzekļi netiek pirkti no ārējiem avotiem, bet pārsūtīti no paša uzņēmuma krājumiem. Tādējādi korespondējošais konts ir krājumu izejas plūsmas konts krājumu vienībām sadaļā Krājumu pārvaldība.

Papildinformāciju skatiet tēmā [Līdzekļu iegādāšanās, izmantojot iepirkuma procesu](acquire-assets-procurement.md).




