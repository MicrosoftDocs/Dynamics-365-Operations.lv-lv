---
title: Mazumtirdzniecības cenu pārskati
description: Šajā tēmā ir sniegts apskats par cenu pārskatu līdzekli, ko var izmantot, lai skatītu sašķiroto preču gaidāmās cenu izmaiņas.
author: shajain
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 7fa2710d64d632c6e4ef376528aff8316b02a380ce7e2a976d53a3dd39375fa7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767270"
---
# <a name="retail-price-reports"></a>Mazumtirdzniecības cenu pārskati

[!include [banner](includes/banner.md)]


Lai piedāvātu saviem debitoriem konkurētspējīgas cenas, mazumtirgotāji bieži maina preču cenas. Veikala vadītājiem ir vajadzīga iespēja viegli piekļuvi jaunākajām vai gaidāmajām cenu izmaiņām, lai viņi varētu plānot resursus, kas ir nepieciešami veikala plauktos redzamo preču etiķešu atjaunināšanai. Retail laidienā 10.0 veikala vadītājs var atvērt pārskatu **Cena**, pārejot uz sadaļu **Visi veikali \> Veikals \> Cenas pārskats** un skatot ar veikalu saistīto preču atjauninātās cenas. 

Lai iespējotu cenu pārskatu, ir jāiespējo parametrs **Iespējot cenu pārskatu par veikalu**. Šis parametrs atrodas cilnē **Commerce parametri \> Atlaides \> Dažādi**. Atverot lapu **Cenu pārskats**, tiek parādīts dialoglodziņš ar dažādām konfigurācijām. Tālāk ir norādītas pieejamās konfigurācijas.

| Konfigurācija | apraksts |
|---|---|
| Sākuma datums/beigu datums| Datumu diapazons, par kuru ir jāģenerē cenu pārskats. Pašlaik ilgums nedrīkst pārsniegt 7 dienas. |
| Kanāls| Veikals, par kuru ir jāģenerē cenu pārskats. |
| Parādīt preces, kam pieejami krājumi| Ja tiek iestatīta vērtība **Jā**, tiek rādītas tikai to preču cenas, kas pašlaik ir pieejamas veikala fiziskajos krājumos. |
| Parādīt variantu cenas | Ja tiek iestatīta vērtība **Jā**, tiek parādītas variantu, kā arī preču šablonu cenas. Šo opciju drīkst **iespējot** tikai tad, ja izmantojat variantiem raksturīgas cenas, jo būtiski palielinās rindu skaits. Turpmākajos laidienos tiks iespējotas no dimensijas atkarīgas cenas, lai veikala vadītājs varētu izvēlēties dimensijas, kuru cenas ir jāparāda. |
| Parādīt preces ar cenu izmaiņām | Ja ir iestatīta vērtība **Jā**, tiek parādītas cenas tikai tajos datumos, kad ir mainīta cena. Vienmēr tiek rādīta cena *vienu dienu pirms* laukā **Sākuma datums** atlasītā datuma, lai veikala vadītājs varētu viegli noteikt preces, kuru cenas nav mainītas visā atlasītajā periodā, kā arī skatīt pašreizējo cenu. |

Pēc pārskata izveides var lejupielādēt Excel failu, lai veiktu jebkāda veida papildu filtrēšanu. Cenu pārskatu var arī izmantot, lai pārbaudītu preču vēsturiskās cenas iepriekšējos datumos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]