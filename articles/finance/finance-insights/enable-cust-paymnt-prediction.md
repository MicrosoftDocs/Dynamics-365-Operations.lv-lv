---
title: Debitora maksājumu prognožu iespējošana
description: Šajā tēmā paskaidrots, kā ieslēgt un konfigurēt debitora maksājumu prognozēšanas līdzekli Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 16ccd7f2e11f0b46aaa646de272e668d29ccc0c0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752932"
---
# <a name="enable-customer-payment-predictions"></a>Debitora maksājumu prognožu iespējošana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā paskaidrots, kā ieslēgt un konfigurēt debitora maksājumu prognozēšanas līdzekli Finanšu ieskatos. Jūs ieslēdzat līdzekli līdzekļu pārvaldības **·** darbvietā un ievadāt konfigurācijas iestatījumus **finanšu ieskatu konfigurācijas** lapā. Šajā tēmā iekļauta arī informācija, kas var palīdzēt efektīvi izmantot līdzekli.

> [!NOTE]
> Pirms veicat tālāk norādītās darbības, pārliecinieties, vai ir paveiktas priekšnosacījumu darbības tēmā [Finanšu ieskatu konfigurēšana](configure-for-fin-insites.md).

1. Slēdziet debitoru maksājumu prognozēšanas līdzekli:

    1. Atveriet darbvietu **Funkcionalitātes pārvaldība**.
    2. Atlasiet **Pārbaudīt atjauninājumus**.
    3. Cilnē **Viss** meklējiet debitoru **maksājumu prognozes**. Ja neatradīsiet šo līdzekli, meklējiet **(priekšskatījums) debitora maksājuma** prognozes. 
    4. Ieslēgt funkciju.

    Debitora maksājumu prognozēšanas līdzeklis ir ieslēgts un gatavs konfigurēšanai.

2. Konfigurējiet debitora maksājumu ieskatu līdzekli:

    1. Dodieties uz **Kredīta un kolekcijas \> Iestatīšanas finanšu \> ieskatu debitoru maksājumu \>** prognozes.
    2. Finanšu ieskatu konfigurācijas lapā cilnē Debitoru maksājumu prognozes atlasiet Skatīt datu laukus, kas tiek izmantoti prognozēšanas modelī, lai atvērtu datu **·** **laukus** **·** **prognozēšanas modeļa** lapai. Tur varat apskatīt noklusējuma sarakstu ar laukiem, kas tiek izmantoti, lai izveidotu mākslīgā intelekta prognozēšanas modeli debitora maksājumu prognozēm.

        Lai izmantotu noklusējuma lauku sarakstu, lai izveidotu prognozēšanas modeli, aizveriet datu laukus prognozēšanas modeļa lapai un pēc tam finanšu ieskatu konfigurācijas lapā iestatiet opciju Iespējot uz **·** **·** **·** **·** Jā.

    3. Nosakiet darījumu periodu "ļoti novēloti", lai definētu, ko jūsu biznesam nozīmē prognozēšanas grozs **Ļoti novēloti**.

        Katram atvērtajam rēķinam sistēma prognozē maksājuma iespējamību trīs grozos: **Savlaicīgi**, **Novēloti** un **Ļoti novēloti**.

        - **Savlaicīgi** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti darījuma termiņā vai pirms tā.
        - **Novēloti** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti pēc darījuma termiņa beigām, bet pirms darījuma perioda "ļoti novēloti" sākuma.
        - **Ļoti novēloti** — šis grozs ietver maksājumus, kas tiek prognozēti kā apmaksāti pēc darījuma perioda "ļoti novēloti" sākuma.

        > [!NOTE]
        > Ja maināt darījumu periodu "ļoti novēloti" un atlasāt **Mainīt novēlošanas slieksni** pēc tam, kad ir izveidots mākslīgā intelekta modelis debitora maksājumiem, esošais prognozēšanas modelis tiek dzēsts, un tiek izveidots jauns modelis. Jaunais prognozēšanas modelis pārvietos darījumus uz periodu "ļoti novēloti", pamatojoties uz iestatījumiem, kas tika ievadīti, to definējot.

    4. Pēc tam, kad esat pabeidzis definēt darījumu periodu "ļoti novēloti", atlasiet **Izveidot prognozēšanas modeli**, lai izveidotu prognozēšanas modeli. **Prognozēšanas** modeļa sadaļa finanšu **ieskatu konfigurācijas lapā** parāda prognozēšanas modeļa statusu.

        > [!NOTE]
        > Jebkurā laikā, kamēr tiek veidots prognozēšanas modelis, varat atlasīt **Atiestatīt modeļa izveidi**, lai atiestatītu procesu.

    Līdzeklis tagad ir konfigurēts un ir gatavs lietošanai.

Pēc tam, kad funkcija ir ieslēgta un konfigurēta, un prognozēšanas modelis ir izveidots un darbojas, finanšu ieskatu parametru lapas prognozēšanas modelis parāda modeļa **·** **·** precizitāti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
