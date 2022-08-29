---
title: Iespējot globālā ieturētā nodokļa valūtas maiņas kursa tipu un datuma tipa iestatījumus
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
ms.openlocfilehash: 41f12a33651c14439f3a59c5c2f2d34019dada2d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229981"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Iespējot globālā ieturētā nodokļa valūtas maiņas kursa tipu un datuma tipa iestatījumus

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

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
