---
title: Termiņatlaides
description: Termiņatlaides tiek iestatītas un koplietotas moduļiem Parādi kreditoriem un Debitoru parādi.  Pieejamo termiņatlaidi var definēt debitora rēķinā vai kreditora rēķinā, un tā tiek izmantota, ja rēķins tiek apmaksāts termiņatlaides datumu diapazonā.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 139fb4fdb7d4f8034bff5e9668dc794f29fb327e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178874"
---
# <a name="cash-discounts"></a>Termiņatlaides

[!include [banner](../includes/banner.md)]

Termiņatlaides tiek iestatītas un koplietotas moduļiem Parādi kreditoriem un Debitoru parādi.  Pieejamo termiņatlaidi var definēt debitora rēķinā vai kreditora rēķinā, un tā tiek izmantota, ja rēķins tiek apmaksāts termiņatlaides datumu diapazonā. 

## <a name="cash-discounts"></a>Termiņatlaides

Gan debitoriem, gan kreditoriem termiņatlaides var izveidot lapā Termiņatlaides. Izmantojot lauku Nākamais atlaižu kods, varat arī norādīt sēriju ar termiņatlaidēm, kas seko viena otrai, beidzoties iepriekšējās termiņatlaides datumiem. Plašāku informāciju skatiet tālāk šajā tēmā, sadaļā “Piemērs. Termiņatlaižu sērijas”. Ja rēķins, kredīta transakcija (maksājums vai kredīta nota) vai tie abi tiek ievadīti valūtā, kas nav juridiskās personas uzskaites valūta, tad termiņatlaide tiek aprēķināta, izmantojot valūtas maiņas kursu, kurš ir balstīts uz maksājuma vai kredīta notas datumu. Ja rēķins un kredīta dokuments tiek ievadīti dažādās juridiskajās personās un ja uzskaites valūtas šīm juridiskajām personām atšķiras, tad valūtas maiņas kurss tiek ņemts no rēķina juridiskās personas attiecīgā kredīta dokumenta datumā. Plašāku informāciju skatiet tālāk šajā tēmā, sadaļā “Piemērs. Valūtas maiņas kursi termiņatlaidēm”.

## <a name="defaulting-order-of-cash-discount-main-account"></a>Termiņatlaides galvenā konta pasūtījuma noklusējuma secība

Ja rēķins ir segts laikā, lai saņemtu termiņatlaidi, šī termiņatlaide tiek automātiski grāmatota uz termiņatlaides galveno kontu atbilstoši šādai noklusējuma prioritātei:
1.  Galvenais konts, kas norādīts laukā Alternatīvais termiņatlaides konts debitora lapā Nosegt atvērtās transakcijas vai kreditora lapā Nosegt atvērtās transakcijas.
2.  Galvenais konts, kas ir norādīts laukā Debitora termiņatlaide vai laukā Kreditora termiņatlaide tajā virsgrāmatas grāmatošanas grupā, kas ir piešķirta rēķina pārdošanas nodokļa kodam. Iestatiet virsgrāmatas grāmatošanas grupas lapā Virsgrāmatas grāmatošanas grupas un piešķiriet tās pārdošanas nodokļa kodiem lapā Pārdošanas nodokļa kodi.
3.  Galvenais grāmatošanas konts lapā Termiņatlaides laukā Galvenais konts debitoru atlaidēm vai lapā Galvenais konts kreditoru atlaidēm attiecībā uz termiņatlaides kodu, kas ir norādīts nosegtajā rēķinā.
4.  Galvenais konts termiņatlaidēm, kā definēts lapā Automātisko transakciju konti.

## <a name="example-series-of-cash-discounts"></a>Piemērs. Termiņatlaižu sērijas
Iestatiet trīs termiņatlaižu kodus šādā veidā:
-   Kods 5D10% – 10% termiņatlaide, ja summa tiek samaksāta 5 dienu laikā.
-   Kods 10D5% – 5% termiņatlaide, ja summa tiek samaksāta 10 dienu laikā.
-   Kods 14D2% – 2% termiņatlaide, ja summa tiek samaksāta 14 dienu laikā.

Laukā Nākamais atlaižu kods:
-   Kodam 5D10% atlasiet 10D5%
-   Kodam 10D5% atlasiet 14D2%.
-   Kodam 14D2% lauku Nākamais atlaižu kods atstājiet tukšu.

Maksājuma datumam pārsniedzot iepriekšējo rēķinā norādītās termiņatlaides datumu, šīs trīs termiņatlaides seko cita citai. Apmaksājot rēķinu, tiek piešķirta tikai viena termiņatlaide, pamatojoties uz to, kurš termiņatlaides datums šajā termiņatlaižu secībā tiek ievērots.

## <a name="example-exchange-rates-for-cash-discounts"></a>Piemērs. Valūtas maiņas kursi termiņatlaidēm
Jūsu juridiskās personas uzskaites valūta ir EUR, un šāds valūtas maiņas kurss ir norādīts attiecībā uz USD:
-   1. februāris = 110
-   1. marts = 80

Rēķins par 1000 USD ar termiņatlaides nosacījumiem 20D2% tiek grāmatots 15. februārī. Rēķina summa uzskaites valūtā ir 1100 EUR. Maksājums par 980 USD šim rēķinam tiek nosegts 1. martā. Termiņatlaides summa ir 20 USD. Maksājuma summa uzskaites valūtā ir 784 EUR. Termiņatlaides uzskaites valūtas summa tiek aprēķināta, izmantojot valūtas maiņas kursu no 1. marta: 20 \* 80 / 100 = 16 EUR.

> [!NOTE]
> Ja lapā Debitoru moduļa parametri vai Kreditoru moduļa parametri ir atlasīta opcija Aprēķināt termiņatlaides daļējiem maksājumiem, tiek izmantots valūtas maiņas kurss, kas ir spēkā katra daļējā maksājuma datumā. 

