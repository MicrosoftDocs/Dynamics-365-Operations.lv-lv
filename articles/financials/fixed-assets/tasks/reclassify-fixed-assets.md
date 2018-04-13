--- 
title: "Pamatlīdzekļu pārklasificēšana"
description: "Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: 6bce294329c7ec6dc436c3d3baf6597e0283c9bd
ms.contentlocale: lv-lv
ms.lasthandoff: 10/30/2017

---
# <a name="reclassify-fixed-assets"></a>Pamatlīdzekļu pārklasificēšana

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā. 

Kad pamatlīdzeklis ir pārklasificētas:

• Visi esošā pamatlīdzekļa vērtības modeļi tiek izveidoti jaunajam pamatlīdzeklim. Visa sākotnējam pamatlīdzeklim iestatītā informācija tiek kopēta uz jauno pamatlīdzekli. Vērtības modeļu statuss oriģinālajam pamatlīdzeklim ir Slēgts. 

• Jaunā pamatlīdzekļa jaunie vērtības modeļi satur pārklasificēšanas datumu laukā Iegādes datums. Datums laukā Nolietojuma sākuma datums tiek kopēts no sākotnējā līdzekļa informācijas. Ja nolietojums jau ir sākts, tad laukā Pēdējais nolietojuma aprēķināšanas datums ir redzams pārklasificēšanas datums. 

• Esošās pamatlīdzekļa transakcijas sākotnējam pamatlīdzeklim tiek atceltas un pārģenerētas jaunajam pamatlīdzeklim.

1. Dodieties uz Pamatlīdzekļi > Periodiskie uzdevumi > Pārklasificēšana.
2. Laukā Pamatlīdzekļu grupa atlasiet grupu, ko vēlaties pārklasificēt.
3. Laukā Pamatlīdzekļa numurs atlasiet, kuru pamatlīdzekli pārklasificēt.
4. Laukā Jauna pamatlīdzekļu grupa atlasiet grupu, uz kuru pārsūtīt šo pamatlīdzekli.
    * Ja jaunā pamatlīdzekļu grupa ir pievienota kādai numuru sērijai, tad lauks Jauns pamatlīdzekļa numurs tiek atjaunināts ar numuru no jaunās pamatlīdzekļu grupas numuru sērijas. Pretējā gadījumā lauks Jauns pamatlīdzekļa numurs tiek atjaunināts ar numuru no numuru sērijas, kas ir iestatīta lapā Pamatlīdzekļu parametri. Ja lapā Pamatlīdzekļu parametri nav iestatīta numuru sērija, ievadiet kādu numuru laukā Jauns pamatlīdzekļa numurs.  
5. Laukā Pārklasificēšanas datums ievadiet kādu datumu.
6. Laukā Dokumentu sērijas ievadiet vai atlasiet kādu vērtību.
7. Noklikšķiniet uz OK.


