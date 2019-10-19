---
title: Mazumtirdzniecības cenu pārskati
description: Šajā tēmā ir sniegts apskats par cenu pārskatu līdzekli, ko var izmantot, lai skatītu sašķiroto preču gaidāmās cenu izmaiņas.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 4fb02bdeca2d71d84ebdddfd16d471a532823e42
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025199"
---
# <a name="retail-price-reports"></a>Mazumtirdzniecības cenu pārskati

[!include [banner](includes/banner.md)]


Lai piedāvātu saviem debitoriem konkurētspējīgas cenas, mazumtirgotāji bieži maina preču cenas. Veikala vadītājiem ir vajadzīga iespēja viegli piekļuvi jaunākajām vai gaidāmajām cenu izmaiņām, lai viņi varētu plānot resursus, kas ir nepieciešami veikala plauktos redzamo preču etiķešu atjaunināšanai. Retail laidienā 10.0 veikala vadītājs var atvērt pārskatu **Cena**, pārejot uz sadaļu **Visi mazumtirdzniecības veikali \> Veikals \> Cenu pārskats** un skatot ar veikalu saistīto preču atjauninātās cenas. 

Lai iespējotu cenu pārskatu, ir jāiespējo parametrs **Iespējot cenu pārskatu par mazumtirdzniecības veikalam**. Šis parametrs atrodas cilnē **Mazumtirdzniecības parametri \> Atlaides \> Dažādi**. Atverot lapu **Cenu pārskats**, tiek parādīts dialoglodziņš ar dažādām konfigurācijām. Tālāk ir norādītas pieejamās konfigurācijas.

| Konfigurācija | apraksts |
|---|---|
| Sākuma datums/beigu datums| Datumu diapazons, par kuru ir jāģenerē cenu pārskats. Pašlaik ilgums nedrīkst pārsniegt 7 dienas. |
| Kanāls| Mazumtirdzniecības veikals, par kuru ir jāģenerē cenu pārskats. |
| Parādīt preces, kam ir pieejami krājumi| Ja tiek iestatīta vērtība **Jā**, tiek rādītas tikai to preču cenas, kas pašlaik ir pieejamas veikala fiziskajos krājumos. |
| Parādīt variantu cenas | Ja tiek iestatīta vērtība **Jā**, tiek parādītas variantu, kā arī preču šablonu cenas. Šo opciju drīkst**iespējot** tikai tad, ja izmantojat variantiem raksturīgas cenas, jo būtiski palielinās rindu skaits. Turpmākajos laidienos tiks iespējotas no dimensijas atkarīgas cenas, lai veikala vadītājs varētu izvēlēties dimensijas, kuru cenas ir jāparāda. |
| Parādīt preces ar cenu izmaiņām | Ja ir iestatīta vērtība **Jā**, tiek parādītas cenas tikai tajos datumos, kad ir mainīta cena. Vienmēr tiek rādīta cena *vienu dienu pirms* laukā **Sākuma datums** atlasītā datuma, lai veikala vadītājs varētu viegli noteikt preces, kuru cenas nav mainītas visā atlasītajā periodā, kā arī skatīt pašreizējo cenu. |

Pēc pārskata izveides var lejupielādēt Excel failu, lai veiktu jebkāda veida papildu filtrēšanu. Cenu pārskatu var arī izmantot, lai pārbaudītu preču vēsturiskās cenas iepriekšējos datumos.
