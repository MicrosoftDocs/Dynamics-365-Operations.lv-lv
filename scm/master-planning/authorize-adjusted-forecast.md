---
title: "Autorizēt pielāgotu prognozi"
description: "Ne visi prognozes dati ir jāautorizē nekavējoties. Šajā tēmā ir izskaidrots, kā var norādīt periodu, kuram prognoze ir autorizēta. Tajā arī izskaidrots, kā var autorizēt noteiktu uzņēmumu prognozi un prognozes modeļus."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7ff7891e9a12be75b9171a23f0a9288b3c723730
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Autorizēt pielāgotu prognozi

[!include[banner](../includes/banner.md)]


Visi prognozes datu nav jāautorizē nekavējoties. Šajā tēmā ir izskaidrots, kā var norādīt periodu, kuram prognoze ir autorizēta. Tajā arī izskaidrots, kā var autorizēt noteiktu uzņēmumu prognozi un prognozes modeļus.

Visi prognozes datu nav jāautorizē nekavējoties. Var norādīt prognozes autorizētā perioda sākuma un beigu datumu. Šī funkcija ļauj iesaldēt noteiktus intervālus. 

Norādītajam sākuma un beigu datumam ir jāatbilst tā intervāla sākuma un beigu datumam, kurā šī prognoze ir ģenerēta. Šis ierobežojums ir noteikts sistēmā, un, ja ir jāveic korekcijas, datumi tiek automātiski pielāgoti. 

Lapas **Autorizācija** cilnē **Detalizēta informācija** var skatīt detalizētu informāciju par pēdējo ģenerēto prognozi. 

Var atlasīt uzņēmumus un prognožu modeļus, ko izmantot prognozes autorizēšanai. Pēc noklusējuma režģī ir iekļauti visi uzņēmumi, kam ir izveidots prognozes pieprasījums. Katram uzņēmumam iepriekš tiek ievadīts prognozes modelis, kas atbilst pašreizējam vispārējās plānošanas parametros iestatītajam prognozes plānam. Taču šo prognozes modeli var mainīt, izmantojot jebkuru šim uzņēmumam atbilstošo prognozes modeli. Ja atlasītajam uzņēmumam nav ģenerēti prognozes pieprasījuma dati, importēšanas laikā tiek parādīts brīdinājuma ziņojums. 

Ir ļoti svarīgi saprast izvēles rūtiņas **Saglabāt bāzlīnijas pieprasījuma apjoma prognozē manuāli veiktās korekcijas** darbības principus. Ja statistiskās bāzlīnijas prognoze ir manuāli koriģēta, tad koriģētās vērtības tiek autorizētas lietošanai pat tad, ja šīs izvēles rūtiņas atzīme ir noņemta. Tomēr pēc autorizācijas izmaiņas tiek atmestas. Nākamajā prognozes ģenerēšanas reizē šai prognozei ir tikai statiska nozīme, un tajā netiek manuāli pārrakstīti dati arī tad, ja izvēles rūtiņa **Pārsūtīt manuālās korekcijas uz pieprasījuma apjoma prognozi** ir atzīmēta. Tāpēc ir jāņem vēra izvēles rūtiņas **Saglabāt bāzlīnijas pieprasījuma apjoma prognozē manuāli veiktās korekcijas** darbības mehānisms, kas ļauj saglabāt vai atmest visas manuāli veiktās izmaiņas.

<a name="see-also"></a>Skatiet arī
--------

[Manuālu bāzlīnijas prognozes korekciju veikšana](manual-adjustments-baseline-forecast.md)

[Prognozes precizitātes pārraudzība](monitor-forecast-accuracy.md)



