---
title: Skatīt, pārvaldīt un apstiprināt plānotos pasūtījumus
description: Šajā tēmā ir sniegta informācija par to, kā skatīt, pārvaldīt un apstiprināt plānotos pasūtījumus plānošanas optimizācijā.
author: ChristianRytt
ms.date: 04/07/2021
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
ms.openlocfilehash: 2d7daac5a33c77e1b49f689061a8dbcf17c3a1d3501461cf3abc0e9cac5121ba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713666"
---
# <a name="view-manage-and-approve-planned-orders"></a>Skatīt, pārvaldīt un apstiprināt plānotos pasūtījumus

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegta informācija par to, kā skatīt, pārvaldīt un apstiprināt plānotos pasūtījumus plānošanas optimizācijā.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Skatīt un pārvaldīt plānotos pasūtījumus

Plānotos pasūtījumus var skatīt un pārvaldīt jebkurā plānoto pasūtījumu saraksta lapā. Atkarībā no plānotā pasūtījuma tipa, ar kuru vēlaties strādāt, dodieties uz vienu no šīm vietām:

- Vispārējā plānošana \> Darbvietas \> Vispārējā plānošana
- Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi
- Ražošanas kontrole \> Ražošanas pasūtījumi \> Plānotie ražošanas pasūtījumi
- Sagāde un avoti \> Pirkšanas pasūtījumi \> Plānotie pirkšanas pasūtījumi
- Krājumu pārvaldība \> Ienākošie pasūtījumi \> Plānotie pārvedumi
- Krājumu pārvaldība \> Izējošie pasūtījumi \> Plānotie pārvedumi

## <a name="view-and-edit-the-status-of-planned-orders"></a>Skatiet un rediģēt plānoto pasūtījumu statusu

Jūs varat izmantot katra plānotā pasūtījuma lauku **Statuss**, lai palīdzētu atsekot norises gaitu vai izmainīt plānotā pasūtījuma apstrādes veidu. Ir pieejami sekojošas **Statuss** vērtības:

- **Neapstrādāts** - Kad vispārējā plānošana ģenerē plānotos pasūtījumus, tiem tiek piešķirts statuss. Plānotie pasūtījumi, kam ir šis statuss tiks dzēsti nākamās plānošanas izpildes laikā.
- **Pabeigts** – šis statuss norāda, ka plānotais pasūtījums ir pabeigts. Ja izvēlaties neapstiprināt plānoto pasūtījumu, varat manuāli mainīt tā statusu uz *Pabeigts*. Ievērojiet, ka sistēma izturas vienādi pret statusiem *Neapstrādāts* un *Pabeigts*.
- **Apstiprināts** – šis statuss norāda, ka plānotais pasūtījums ir apstiprināts apstiprināšanai. Ja vēlaties apstiprināt plānoto pasūtījumu, varat mainīt tā statusu uz *Apstiprināts*. Ja vēlaties saglabāt rediģējumus, kas veikti plānotajam pasūtījumam, vai, ja plānojat apstiprināt plānoto pasūtījumu, mainiet tā statusu uz *Apstiprināts*. Plānotie pasūtījumi ar statusu *Apstiprināts* tiek uzskatīti par fiksētiem un paredzamiem piegādēm pēc vispārējās plānošanas. Tāpēc tie netiek modificēti vai dzēsti vēlāku vispārējās plānošanas palaišanas laikā. Lai to panāktu, plānošanas loģika kopē plānotos pasūtījumus ar statusu *Apstiprinātos* no vecās plāna versijas uz jauno plāna versiju vispārējās plānošanas laikā. Ievērojiet, ka plānotie pasūtījumi, kuru statuss ir *Apstiprināts* plānotie pasūtījumi tiek uzskatīti par piegādēm tikai noteiktajā galvenājā plānā.

Lai mainītu atsevišķa plānotā pasūtījuma statusu, [atveriet jebkuru plānoto pasūtījumu saraksta lapu](#view-planned-orders), atveriet pasūtījumu un tad izpildiet vienu no tālāk minētajām darbībām.

- Kopsavilkuma cilnē **Vispārīgi** mainiet lauka **Statuss** vērtību.
- Darbību rūtī cilnē **Plānotais pasūtījums** grupā **Process** atlasiet **Mainīt statusu**.
- Darbību rūtī atlasiet **Apstiprināt**, lai atzīmētu pasūtījumu kā apstiprinātu.

Lai vienlaicīgi mainītu vairāku plānoto pasūtījumu statusu, [atveriet jebkuru plānoto pasūtījumu saraksta lapu](#view-planned-orders), atzīmējiet izvēles rūtiņu katram pasūtījumam, kuru vēlaties mainīt, un pēc tam izpildiet vienu no šīm darbībām:

- Darbību rūtī cilnē **Plānotais pasūtījums** grupā **Process** atlasiet **Mainīt statusu**.
- Darbību rūtī atlasiet **Apstiprināt**, lai atzīmētu pasūtījumus kā apstiprinātus.

## <a name="approve-planned-orders"></a>Plānoto pasūtījumu apstiprināšana

Plānoto pasūtījumu apstiprināšana ir neobligāts solis apstiprināta pasūtījuma izveides procesā no plānotā pasūtījuma.

Šajā attēlā parādīts, kā var izmantot vērtību **Statuss**, kas ir piešķirta katram plānotajam pasūtījumam, lai ieviestu apstiprināšanas darbplūsmu. Lai ieviestu apstiprināšanas procesu, manuāli pielāgojiet vērtību **Statuss** katram plānotajam pasūtījumam, kā aprakstīts iepriekšējā sadaļā.

![Plānotā pasūtījumu plūsma.](media/approved-planned-orders-1.png)

> [!TIP]
> Modificētus plānotos pasūtījumus ieteicams apstiprināt. Pretējā gadījumā nākamās plānošanas darbības laikā labojumi tiks ignorēti un pārrakstīti.

## <a name="additional-resources"></a>Papildu resursi

- [Plānoto pasūtījumu apstiprināšana](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
