---
title: Plānoto pasūtījumu apstiprināšana
description: Šajā tēmā ir aprakstīta plānošanas optimizācijas atbalstīto plānoto pasūtījumu apstiprināšana.
author: ChristianRytt
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 6c215a89403f16336caae5c62cde6df469c4091c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825895"
---
# <a name="approve-planned-orders"></a>Plānoto pasūtījumu apstiprināšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegta informācija par to, kā atjaunināt plānoto pasūtījumu statusu plānošanas optimizācijā.

Ņemiet vērā, ka plānoto pasūtījumu apstiprināšana ir neobligāts solis, lai izveidotu apstiprinātu pasūtījumu no plānotā pasūtījuma. Ieteicams apstiprināt modificētos plānotos pasūtījumus, pretējā gadījumā labojumi tiks ignorēti un pārrakstīti ar nākamo plānošanas izpildi.

![Plānotā pasūtījumu plūsma](media/approved-planned-orders-1.png)

Lauks **Statuss** palīdz izlīdzināt jūsu progresu, izmantojot tālāk norādītās vērtības:

- **Neapstrādāts:** Kad vispārējā plānošana ģenerē plānotos pasūtījumus, tiem tiek piešķirts statuss *Neapstrādāts*. Plānotie pasūtījumi ar šo statusu tiks dzēsti nākamās plānošanas izpildes laikā.
- **Pabeigts:** Ja izlemjat neapstiprināt plānoto pasūtījumu, varat mainīt statusu uz *Pabeigts* , lai norādītu, ka esat pabeiguši šī plānotā pasūtījuma novērtēšanu. Ņemiet vērā, ka pret statusiem *Neapstrādāts* un *Pabeigts* sistēma izturas vienādi.
- **Apstiprināts:** Ja vēlaties saglabāt labojumus vai plānojat apstiprināt plānoto pasūtījumu, mainiet statusu uz *Apstiprināts*. Plānotos pasūtījumus ar statusu *Apstiprināts* tiek uzskatīti par fiksētiem un paredzamiem galvenās plānošanas pakalpojumiem, tāpēc tie netiek modificēti vai izdzēsti vēlāku vispārējās plānošanas palaišanu laikā. Lai to sasniegtu, plānošanas loģika kopē *Apstiprinātos* plānotos pasūtījumus no vecās plāna versijas uz jauno plāna versiju vispārējās plānošanas laikā. Ņemiet vērā, ka *Apstiprinātie* plānotie pasūtījumi tiek uzskatīti par piegādēm tikai noteiktajā galvenājā plānā.

Plānotos pasūtījumus var pārvaldīt no darbvietas  **Vispārējā plānošana**  , saraksta  **Plānotais pasūtījums**  vai saraksta  **Plānotie ražošanas pasūtījumi**,  **Plānotie pirkšanas pasūtījumi** un  **Plānotā pārsūtīšana**  .


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]