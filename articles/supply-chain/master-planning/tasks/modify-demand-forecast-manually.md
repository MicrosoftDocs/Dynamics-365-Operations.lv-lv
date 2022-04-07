---
title: 'Ceļvedis: Pieprasījuma apjoma prognozes manuāla modificēšana'
description: Šajā tēmā aprakstīts, kā modificēt krājuma prognozi
author: t-benebo
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e5030bf97bee8dc475f22473ecc87e900298b6f
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469411"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Ceļvedis: Pieprasījuma apjoma prognozes manuāla modificēšana

[!include [banner](../../includes/banner.md)]

Šajā procedūrā parādīts, kā modificēt krājuma prognozi. Šī procedūra ir paredzēta ražošanas plānotājam.

## <a name="modify-the-forecast-for-a-selected-item"></a>Atlasītā krājuma prognozes modificēšana

Lai mainītu atlasītā krājuma prognozi:

1. Pārejiet uz sadaļu **Moduļi \> Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet krājumu, kuram vēlaties mainīt prognozi.
1. Darbību rūtī atveriet cilni **Plāns** un atlasiet **Pieprasījuma apjoma prognoze**.
1. Sarakstā atlasiet rindu. Ja nav nevienas prognožu rindas, izveidojiet jaunu rindu, darbību rūtī atlasot **Jauns**.  
1. Laukā **Pārdošanas daudzums** ievadiet pozitīvu skaitli. Šis daudzums apzīmē krājuma prognozēto daudzumu. Ja ievadīsiet negatīvu skaitli, tiks parādīta kļūda.
1. Pēc vajadzības aizpildiet parējos laukus.
1. Atlasiet **Saglabāt** darbību rūtī.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Modificējiet prognozi vienam vai vairākiem krājumiem Microsoft Excel

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
