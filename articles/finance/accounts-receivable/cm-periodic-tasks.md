---
title: Periodiski kredītu pārvaldības uzdevumi
description: Šajā tēmā aprakstīti periodiskie uzdevumi, kas ir daļa no debitoru kredīta limitu pārvaldības procesa.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 53b7cd00b3287f18ba65391842ac259ab2434b86
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735441"
---
# <a name="periodic-credit-management-tasks"></a>Periodiski kredītu pārvaldības uzdevumi

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīti periodiskie uzdevumi, kas ir daļa no debitoru kredīta limitu pārvaldības procesa.

## <a name="update-risk-scores"></a>Atjaunināt riska rādītājus

Uzņēmējdarbībai attīstoties un mainoties apstākļiem, var mainīties arī attiecīgā debitora kredīta riski. Lai palīdzētu uzturēt attiecīgos kredīta limitus saviem debitoriem, jums periodiski jāpārbauda katra riska rezultāta kritēriji un jāatjaunina rādītāji katram debitoram. Varat atjaunināt šādus rezultātus, izmantojot lapu **Atjaunināt riska rezultātus** (**Kredīts un iekasēšana \> Periodiskie uzdevumi \> Kredīta pārvaldība \> Atjaunināt riska rezultātus**). Visi lietotāja definētie aprēķini arī tiek apstrādāti.

- **Vidējais apmaksas dienu skaits** — šis rezultāts ir vidējais dienu skaits, kad debitors veic rēķinu apmaksu.
- **Debitors kopš** — šis rezultāts ir gadu skaits, kad debitors ir bijis jūsu organizācijas debitors.
- **Uzņēmējdarbībā kopš** — šis rezultāts ir gadu skaits, cik debitors ir darbojies uzņēmējdarbībā. Tas izmanto lauka **Uzņēmējdarbības sākums** vērtību lapā **Debitori**.
- **Vidējais maksājuma saņemšanas laiks** — šis rezultāts ir balstīts uz debitoru parādu bilanci, pārdošanas ieņēmumiem un dienu skaitu iepriekšējā 12 mēnešu periodā.
- **Vidējā bilance** — šis rezultāts ir balstīts uz debitoru parādu bilanci par iepriekšējo 12 mēnešu periodu.
- **Kredīta pārvaldības grupa**, **Konta statuss** un **Valsts** — šie rezultāti izmanto informāciju no debitora.

## <a name="update-customer-balance-statistics"></a>Klienta bilances statistikas atjaunināšana

Varat palaist procesu **Atjaunināt debitora bilances statistikas**, lai atjauninātu bilances statistiku, kas tiek rādīta lapā **Bilances statistikas pieprasījums**. Šī informācija tiek izmantota, lai aprēķinātu riska rādītājus un vērtības, kas tiek rādītas kredīta statistikas papildinformācijas lapā **Debitors**.

Palaižot procesu, tas atjaunina debitora bilances statistiku vienam debitoram. Lai iestatītu pakešuzdevumu vairāku debitoru procesa izpildei, varat izmantot lapu **Aprēķināt bilances statistiku** (**Kredīta pārvaldība \> Periodiskie uzdevumi \> Aprēķināt bilances statistiku**).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
