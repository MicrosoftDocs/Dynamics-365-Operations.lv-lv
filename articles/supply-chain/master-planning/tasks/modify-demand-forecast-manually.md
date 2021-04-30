---
title: Pieprasījuma apjoma prognozes manuāla modificēšana
description: Šajā tēmā aprakstīts, kā modificēt krājuma prognozi
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889028"
---
# <a name="modify-a-demand-forecast-manually"></a>Pieprasījuma apjoma prognozes manuāla modificēšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā modificēt krājuma prognozi. USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei. Šī procedūra ir paredzēta ražošanas plānotājam.

## <a name="modify-the-forecast-for-a-selected-item"></a>Atlasītā krājuma prognozes modificēšana

Lai mainītu atlasītā krājuma prognozi:

1. Pārejiet uz sadaļu **Moduļi \> Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet krājumu, kuram vēlaties mainīt prognozi.
1. Darbību rūtī atveriet cilni **Plāns** un atlasiet **Pieprasījuma apjoma prognoze**.
1. Sarakstā atlasiet rindu. Ja nav nevienas prognožu rindas, izveidojiet jaunu rindu, darbību rūtī atlasot **Jauns**.  
1. Laukā **Pārdošanas daudzums** ievadiet pozitīvu skaitli. Šis daudzums apzīmē krājuma prognozēto daudzumu. Ja ievadīsiet negatīvu skaitli, tiks parādīta kļūda.
1. Pēc vajadzības aizpildiet parējos laukus.
1. Atlasiet **Saglabāt** darbību rūtī.

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a>Modificēt prognozi vienam vai vairākiem krājumiem Microsoft Excel

Lai modificētu prognozi vienam vai vairākiem krājumiem Microsoft Excel:

1. Veiciet vienu no tālāk norādītajām darbībām.
    - Atveriet lapu **Pieprasījuma apjoma prognoze** jebkuram krājumam (nav svarīgi kuram) kā aprakstīts iepriekšējā sadaļā.
    - Dodieties uz **Vispārējā plānošana \> Prognozēšana \> Manuāls prognozes ieraksts \> Pieprasījuma apjoma prognozes rindas**.
1. Darbību rūtī atveriet **Atvērt Microsoft Office \> Pieprasījuma apjoma prognozes ieraksti**.
1. Atlasiet lejupielādes vietu, saglabājiet un pēc tam atveriet lejupielādēto failu programmā Excel.
1. Ja ir redzams brīdinājums, izvēlieties **Iespējot rediģēšanu**.
1. Programmā Excel piesakieties Supply Chain Management, izmantojot Microsoft Dynamics uzdevumrūti. Ir jāpiesakās, ja opcija **Palikt pierakstītam** ir iespējota un jums ir jāuzticas datu savienojuma programmai.
1. Excel izklājlapa tagad rāda visas pašreizējās pieprasījuma apjoma prognozes rindas jūsu uzņēmumam.  Pēc nepieciešamības pievienojiet, dzēsiet un labojiet pieprasījuma prognozes rindas.
1. Atlasiet **Publicēt** pakalpojuma Microsoft Dynamics uzdevumrūtī, lai augšupielādētu izmaiņas atpakaļ Supply Chain Management.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
