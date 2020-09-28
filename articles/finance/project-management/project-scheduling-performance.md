---
title: Projekta resursu plānošanas veiktspēja
description: Šī tēma sniedz informāciju par to, kā uzlabot resursu plānošanas veiktspēju lielam projektu skaitam.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760609"
---
# <a name="project-resource-scheduling-performance"></a>Projekta resursu plānošanas veiktspēja

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Veiktspējas problēmas, kas saistītas ar resursu plānošanu, var notikt, kad projektu skaits sasniedz tūkstošus. Lai uzlabotu resursu plānošanas veiktspēju, ir pieejams līdzeklis, kas ļauj lietotājiem samazināt laiku, kas nepieciešams, lai palaistu resursu pieejamības veidlapu. Konkrēti tas noņem resursu noslodzes apkopošanas sinhronizācijas procesu un izmanto tabulu **ResProjectResource**, lai paātrinātu resursu meklēšanu. Ievērojiet, ka tabula **ResRollup** vairs netiks izmantota.

> [!IMPORTANT]
> Ja ir atkarība vai nu no resursu noslodzes apkopošanas sinhronizācijas procesa, vai no tabulas **ResProjectResource**, neizmantojiet šo līdzekli.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Iespējot resursu plānošanas veiktspējas uzlabojumu
Lai iespējotu resursu plānošanas veiktspējas uzlabojumu, veiciet šādas darbības.

1. Dodieties uz **Līdzekļu pārvaldība** > **Visas**, un līdzekļu sarakstā atrodiet **Iespējot projekta resursu plānošanas veiktspējas uzlabošanas līdzekli**.
2. Atlasiet **Iespējot tagad**.

> [!NOTE]
> Ja sarakstā nevarat atrast līdzekli, atlasiet **Pārbaudīt, vai nav atjauninājumu** lai atsvaidzinātu sarakstu.

3. Atsvaidziniet pārlūkprogrammu un pēc tam dodieties uz **Projektu vadība un uzskaite** > **Periodisks** > **Projektu resursi** > **Sinhronizēt resursu kalendāru noslodzi visiem uzņēmumiem**.
4. Iestatiet **Noņemt esošos noslodzes ierakstus** uz **Jā**, lai noņemtu iepriekšējos datus. Ja vēlaties ģenerēt inkrementālos datus, iestatiet to uz **Nē**.
5. Laukā **Perioda kods** atlasiet periodu, kurā jāģenerē dati. Ja atlasāt perioda kodu, sākuma un beigu datums nav jādefinē.
6. Ja atstājat tukšu lauku **Perioda kods**, atlasiet konkrētus sākuma un beigu datumus, lai ģenerētu datus.
7. Atlasiet **Labi**.

 > [!NOTE]
 > Tādējādi tabulā **ResCalendarCapacity** visos uzņēmumos jūsu vidē tiks izplatīti vispārīgi dati, tāpēc pakešuzdevums ir jāizpilda tikai vienā juridiskā personā. Šie pakešuzdevuma dati ir vajadzīgi, lai aprēķinātu resursu noslodz, izmantojot saistīto kalendāru.

8. Dodieties uz **Projektu vadība un uzskaite** > **Periodisks** > **Projektu resursi** > **Projekta resursu aizpildīšana visos uzņēmumos** un pēc tam atlasiet **Labi**. Šis ir datu jaunināšanas skripts vispārējiem datiem tabulās **ResProjectResource** , **ResCalendarDateTimeRange** un **ResEffectiveDateTimeRange**. Tiek atjauninātas arī lauka **PSAPRojSchedRole.RootActivity** vērtības. Ja tas netiek izpildīts, jūs saņemsiet brīdinājumu, kad mēģināsit izpildīt resursu plānošanas operācijas.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Izslēgt resursu plānošanas veiktspējas uzlabojumu

1. Dodieties uz **Līdzekļu pārvaldība** > **Visas**  un meklējiet **Iespējot projekta resursu plānošanas veiktspējas uzlabošanas līdzekli**.
2. Atlasiet līdzekli un pēc tam atlasiet pogu **Atspējot**.
3. Atsvaidziniet pārlūkprogrammu.
4. Dodieties uz **Projektu vadība un uzskaite** > **Periodisks** > **Noslodzes sinhronizācija** > **Sinhronizēt resursa noslodzes apkopojumus**.
5. Lapā **Noslodzes apkopošanas sinhronizācija** iestatiet **Esošo noslodzes ierakstu noņemšana** uz **Jā**, lai noņemtu iepriekšējos datus. Ja vēlaties ģenerēt inkrementālos datus, iestatiet to uz **Nē**.
6. Laukā **Perioda kods** atlasiet periodu, kurā jāģenerē dati. Ja atlasāt perioda kodu, sākuma un beigu datums nav jādefinē.
7. Ja atstājat tukšu lauku **Perioda kods**, atlasiet konkrētus sākuma un beigu datumus, lai ģenerētu datus.
8. Atlasiet **Labi**.

> [!NOTE]
> Tādējādi tabulā **ResRollup** visos uzņēmumos jūsu vidē tiks izplatīti vispārīgi dati, tāpēc pakešuzdevums ir jāizpilda tikai vienā juridiskā personā. Šis pakešuzdevums ir nepieciešams visiem **Resursu pieejamības** skatiem. Ja šis pakešuzdevums netiek izpildīts, **ResRollup** dati tiks ģenerēti ātri, kas var aizņemt laiku.
