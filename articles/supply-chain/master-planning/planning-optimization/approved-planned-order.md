---
title: Plānoto pasūtījumu apstiprināšana
description: Šajā tēmā ir aprakstīta plānošanas optimizācijas atbalstīto plānoto pasūtījumu apstiprināšana.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 8745a461986c1f16f2b3f9fd23011701d104a30c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264022"
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