---
title: Plānoto pasūtījumu uzturēšana
description: Šajā sadaļā ir sniegta informācija par to, kā pārvaldīt plānotos pasūtījumus. Tajā ir izskaidrots, kā var atjaunināt plānoto pasūtījumu statusu, apstiprināt tos un filtrēt pēc plānotajiem pasūtījumiem, kuriem ir tāds pats statuss kā atlasītajam plānotajam pasūtījumam.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993444"
---
# <a name="maintain-planned-orders"></a>Plānoto pasūtījumu uzturēšana

[!include [banner](../includes/banner.md)]

Šajā sadaļā ir sniegta informācija par to, kā pārvaldīt plānotos pasūtījumus. Tajā ir izskaidrots, kā var atjaunināt plānoto pasūtījumu statusu, apstiprināt tos un filtrēt pēc plānotajiem pasūtījumiem, kuriem ir tāds pats statuss kā atlasītajam plānotajam pasūtījumam.

Plānotos pasūtījumus var pārvaldīt no darbvietas **Vispārējā plānošana**, saraksta **Plānotais pasūtījums** vai saraksta **Plānotie ražošanas pasūtījumi**, **Plānotie pirkšanas pasūtījumi** un **Plānotā pārsūtīšana**. 

## <a name="planned-order-status"></a>Plānotā pasūtījuma statuss
Lai sekotu norisei, varat izmantot lauku **Statuss**. Tiek izmantotas šādas vērtības.

-   Kad vispārējā plānošana ģenerē plānotos pasūtījumus, tiem tiek piešķirts statuss **Neapstrādāts**.
-   Ja izvēlaties neapstiprināt plānoto pasūtījumu, tam var piešķirt statusu **Pabeigts**.
-   Ja vēlaties apstiprināt plānoto pasūtījumu, varat mainīt statusu uz **Apstiprināts**. Plānotos pasūtījumus ar statusu **Apstiprināts** ievēro vispārējā plānošana, tāpēc tie netiek modificēti vai dzēsti. 

## <a name="firming-planned-orders"></a>Apstiprinot plānotos pasūtījumus 
Apstiprinot plānotos pasūtījumus, tiek izveidoti faktiskie pasūtījumi. Tie ir zināmi arī kā *izdotie* vai *atvērti pasūtījumi*. Kad plānotais pasūtījums apstiprināts, tas tiek pārvietots attiecīgā moduļa pasūtījumu sadaļai.

No **Plānotie pasūtījumi** lapas varat atlasīt divas apstiprināšanas opcijas:

-   **Atstiprināt**— tas apstiprinās vienu vai vairākus atlasītos plānotos pasūtījumus.
-   **Apstiprināt visu**— tas apstiprinās visus plānotos pasūtījumus filtrā. Izmantojot **Apstiprināt visu** , nav jāatlasa plānotais pasūtījums, visi plānotie pasūtījumi filtrā tiks apstiprināti. Šī opcija var būt noderīga, ja jūs apstiprinājiet lielu skaitu plānoto pasūtījumu.

> [!NOTE]
> Jūs varat izsekot plānoto pasūtījumu, kas tika apstiprināts no **Apstiprināšanas vēsture** zem **Plānoto pasūtījumu forma > Skatīt > Apstiprināšanas vēsture.**

## <a name="parallelize-firming"></a>Veikt paralēlu apstiprināšanu
Ja jūs plānojat apstiprināt daudzus pasūtījumus vienlaicīgi, paralēlā izpilde var uzlabot izpildes laiku vai veiktspēju. Šī opcija ir pieejama, apstiprinot vairākus plānotos pasūtījumus ar **Atstiprināt** vai **Apstiprināt visu**. Ir pieejami šādi parametri:

-   **Paralēlā apstiprināšana** – ja **Jā**, apstiprināšanas process būs paralēls ar pavedienu skaitu, kas definēts **Pavedienu skaits** sadaļā.
-   **Pavedienu skaits**— kontrolē pavedienu skaitu izmantoto, lai apstiprināšanas process būtu paralēls. Parametrs parādās tikai tad, ja **Paralēlā apstiprināšana** ir iestatīta uz **Jā**.


<a name="additional-resources"></a>Papildu resursi
--------

[Vispārējie plāni](master-plans.md)



