---
title: Globālā ieturētā nodokļa valūtas maiņas kursa tipa un datuma veida iestatījumu iespējošana
description: Šajā rakstā ir izskaidrots, kā aktivizēt ieturētā nodokļa valūtas maiņas kursa tipa un datuma tipa globālos iestatījumus.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9db9cf41381b8b4de7dffe1c755a7df805a003ea
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573229"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Globālā ieturētā nodokļa valūtas maiņas kursa tipa un datuma veida iestatījumu iespējošana

[!include[banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā aktivizēt ieturētā nodokļa valūtas maiņas kursa tipa un datuma tipa globālos iestatījumus. Tagad ir iespējams atlasīt atvēlēto maiņas kursa tipu un maiņas kursa aprēķina datuma tipu ieturamā nodokļa valūtai. Šīs atlases nosaka ārvalstu valūtas maiņas kursu, kas tiek izmantots ieturamā nodokļa summas jāaprēķina ieturamā nodokļa valūtā maksājuma darbībās.

Šī funkcionalitāte ir pieejama Microsoft Dynamics 365 Finanšu versijā 10.0.29 vai jaunākā versijā.

1. Dodieties uz **nodokļu** \> **iestatījumu** \> **parametriem** \> **Virsgrāmatā.**
2. Cilnē Ieturētais **nodoklis iestatiet** opciju Aktivizēt papildu ieturētā **nodokļa valūtu** uz **Jā**.
3. Laukā **Maiņas kursa** tips atlasiet ieturamā nodokļa valūtas maiņas kursa tipu.
4. Laukā **Aprēķina datuma tips** atlasiet aprēķina datuma tipu, kas nosaka ieturamā nodokļa valūtas maiņas kursu:

    - **Maksājuma datums** – nosakiet valūtas kursu, pamatojoties uz maksājuma žurnāla grāmatošanas datumu.
    - **Rēķina datums** – nosakiet maiņas kursu, pamatojoties uz rēķina datumu rēķinu žurnālā. Ja dokumenta rēķina datums ir tukšs, tiek izmantots rēķina grāmatošanas datums. 
    - **Dokumenta datums** – nosakiet valūtas kursu, pamatojoties uz maksājuma žurnāla dokumenta datumu. Ja dokumenta dokumenta datums ir tukšs, tiks izmantots maksājuma datums.

5. Atlasiet **Saglabāt**.

Ja darbības valūta atšķiras no ieturamā nodokļa kodā definētās ieturamā nodokļa valūtas, summa ieturamā nodokļa valūtā tiks aprēķināta no darbības valūtas, pamatojoties uz iepriekšējiem iestatījumiem, un tiks reģistrēta grāmatotās ieturamā nodokļa darbībās.
