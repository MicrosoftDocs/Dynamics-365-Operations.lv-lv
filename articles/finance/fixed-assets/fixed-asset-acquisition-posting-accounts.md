---
title: Pamatlīdzekļu ieguves grāmatošanas konti
description: Šajā rakstā ir paskaidrots, kā iestatīt Virsgrāmatas grāmatošanas kontus līdzekļu iegādei.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: kfend
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93cbfc46fb41e47fba8b6cecf7811c0cf838e7d3
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719825"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a>Pamatlīdzekļu ieguves grāmatošanas konti

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā iestatīt Virsgrāmatas grāmatošanas kontus līdzekļu iegādei.

Pamatlīdzekļu iegādes grāmatošanai izmantotie konti ir atkarīgi no metodes, kādā līdzeklis tiek iegādāts. Lapā Pamatlīdzekļu grāmatošanas metodes, cilnē Virsgrāmatas konti atlasiet Iegāde un Iegādes korekcija, lai iestatītu pamatlīdzekļu kontus grāmatošanai virsgrāmatā. 

Žurnālos un pirkšanas pasūtījumos Virsgrāmatas konts parasti ir bilances konts, kur jaunā pamatlīdzekļa iegādes vērtība tiek ierakstīta debetā. Šis konts netiek parādīts žurnālā un to nevar aizstāt transakcijās. 

Korespondējošais konts ir arī bilances konts. Virsgrāmatas žurnālā un pamatlīdzekļu žurnālā šis konts bieži mēdz būt bankas konts, ko lieto, lai maksātu par pamatlīdzekļa iegādi. Korespondējošais konts ir noklusējuma konts, kas tiek norādīts žurnālos. Žurnālā to var nomainīt ar jebkuru citu kontu no kontu plāna vai ar kreditora kontu, ja pamatlīdzeklis tika pirkts no kreditora. 

Ja pamatlīdzekļu iegādei modulī Kreditori tiek lietots vienums Rēķinu žurnāls vai Pirkšanas pasūtījumi, tad pamatlīdzekļu transakcijas korespondējošais konts tiek aizstāts ar šai transakcijai atlasīto kreditora kontu.

Iegādēm, kas tiek grāmatotas, virsgrāmatā izmantojot žurnālu Krājumi pamatlīdzekļiem, pamatlīdzekļi netiek pirkti no ārējiem avotiem, bet pārsūtīti no paša uzņēmuma krājumiem. Tādējādi korespondējošais konts ir krājumu izejas plūsmas konts krājumu vienībām sadaļā Krājumu pārvaldība.

Papildinformāciju skatiet tēmā [Līdzekļu iegādāšanās, izmantojot iepirkuma procesu](acquire-assets-procurement.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
