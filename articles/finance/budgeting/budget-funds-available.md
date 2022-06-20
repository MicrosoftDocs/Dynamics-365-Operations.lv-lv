---
title: Pieejamie budžeta līdzekļi
description: Šajā rakstā ir sniegta informācija par pieejamo budžeta līdzekļu līdzekli un sniegta informācija, kas var jums palīdzēt konfigurēt budžeta kontroli, lai optimizētu jūsu organizācijas finanšu resursu pārvaldību.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: b6f94931ba3514c1c66d80b64846d882861d555c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898245"
---
# <a name="budget-funds-available"></a>Pieejamie budžeta līdzekļi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā rakstā ir sniegta informācija par pieejamo budžeta līdzekļu līdzekli un sniegta informācija, kas var jums palīdzēt konfigurēt budžeta kontroli, lai optimizētu jūsu organizācijas finanšu resursu pārvaldību.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Budžeta pieejamajiem budžeta līdzekļiem paredzēts uzlabots aprēķina līdzeklis

Tikai **atsekošanas summas** budžeta fondos pieejamo aprēķinu iespēju ļauj jums izsekot pakārtotās budžeta kontroles tabulas dokumentu tipiem un stāvotiem, **balstoties uz iestatījumiem lapā Definēt budžeta kontroles parametrus**.

Dažām budžeta kontroles konfigurācijas opcijām ir jābūt noteiktiem funkcijas iestatījumiem, lai funkcija darbotos pareizi. Šīs opcijas tiek atlasītas vai dzēstas lapas **Definēt budžeta** kontroles parametru **cilnē Pieejamie budžeta** līdzekļi. Tālāk sniegtajā tabulā ir norādīti iestatījumi, kas nepieciešami pieejamo budžeta līdzekļu funkcijai.

| Ja ir atlasīta šī opcija | Ir jāatlasa arī šī opcija. |
| ------------------------- | -------------------------------- |
| Budžeta rezervācijas apgrūtinājumiem bez juridiskām saistībām | Budžeta rezervācijas apgrūtinājumiem un *faktiskajiem* izdevumiem |
| Budžeta rezervācijas apgrūtinājumiem | Faktiskie izdevumi |
| Budžeta rezervācijas apgrūtinājumiem ar pirkšanas pieprasījuma veida dokumentiem | Budžeta rezervācijas apgrūtinājumiem bez juridiskām saistībām |

Šī funkcija ietekmē tikai jaunos dokumentus. Esošo dokumentu summas tiks izsekotas un rādītas budžeta kontroles statistikas vaicājumā līdz brīdim, kad tiks mainīts pieejamo budžeta līdzekļu iestatījums un aktivizēta jaunā budžeta kontroles konfigurācija. Šajā brīdī budžeta izsekošanas dati tiks noņemti dokumentiem, kas tika noņemti no budžeta līdzekļu pieejamā aprēķina.

Ieteicams atstāt opciju Negrāmatoti **faktiskie izdevumi notīrītu**. Atlasot šo lauku, laikietilpīgs budžeta kontroles aprēķins tiks veikts negrāmatotiem dokumentiem, piemēram, neizlemtiem kreditora rēķiniem.
