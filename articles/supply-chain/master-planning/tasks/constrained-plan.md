---
title: Ierobežotā plāna ģenerēšana
description: Šajā tēmā paskaidrots, kā izveidot plānu, kurā ņemti vērā gan materiāla, gan noslodzes ierobežojumi.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8372f4e35b34ff66ef55c0961b867a1aff7a5e6
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468949"
---
# <a name="generate-a-constrained-plan"></a>Ierobežotā plāna ģenerēšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā paskaidrots, kā izveidot plānu, kurā ņemti vērā gan materiāla, gan noslodzes ierobežojumi. Šis plāns nodrošina, ka ražošana nesākas, pirms materiāli kļūst pieejami, un resursiem netiek pārsniegta rezervācija. 

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta ražošanas plānotājam.


## <a name="set-up-a-constrained-plan"></a>Iestatīt ierobežotu plānu
1. Sākumlapā izvēlieties **Vispārējās plānošanas** darbvietu.
2. Izvēlieties **Galvenie plāni** saišu sarakstā darbvietas tālajā labajā pusē.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Piemērs: **StatisksPlāns**  
4. Atlasiet **Jā** laukā **Galīgā noslodze**.
5. Laukā **Galīgās noslodzes robežas** ievadiet `30`.
6. Izvērsiet sadaļu **Laika robežas dienās**.
7. Atlasiet **Jā** laukā **Noslodze**.
8. Laukā **Noslodzes plānošanas laika robežas (dienas)** ievadiet skaitli. Piemērs: `60`  
9. Atlasiet **Jā** laukā **Aprēķinātie kavējumi**.
10. Laukā **Aprēķināt kavējumu laiku robežas (dienas)** ievadiet skaitli. Piemērs: `60` 
11. Izvērsiet sadaļu **Aprēķinātie kavējumi**.
12. Atlasiet **Jā** visos laukos **Pievienot aprēķināto kavējumu prasības datumam**.
13. Aizvērt lapu.

## <a name="create-a-constrained-plan"></a>Ierobežota plāna izveide
1. Atlasiet **Izpildīt**.
2. Laukā **Vispārējais plāns** ievadiet vai atlasiet plānu, kam esat iestatījis ierobežojumus.  
3. Atlasiet **Labi**.
4. Atlasiet **Plānotie pasūtījumi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]