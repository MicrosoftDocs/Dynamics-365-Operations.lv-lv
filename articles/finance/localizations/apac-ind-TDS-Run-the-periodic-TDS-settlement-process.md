---
title: Periodisko TDS norēķinu procesa palaišana
description: Šajā tēmā skaidrots, kā nomaksāt periodisko No kopējās ienākumu summas atskaitīto nodokli (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5b4c3a83f3fed0907dacd415f5aff9fad3c10bc6
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408384"
---
# <a name="run-the-periodic-tds-settlement-process"></a>Periodisko TDS norēķinu procesa palaišana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā nomaksāt periodisko No kopējās ienākumu summas atskaitīto nodokli (TDS).

1. Atveriet **Nodoklis \> Deklarācijas \> Ieturētais nodoklis \> Ieturētā nodokļa maksājums**.

    [![Ieturētā nodokļa maksājuma dialoga lodziņš.](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)

2. Dialoglodziņa **Ieturētā nodokļa maksājums** laukā **Nodokļa tips** atlasiet **TDS**.
3. Laukā **Nodokļu konta numurs (TAN)** atlasiet Nodokļu konta numuru (TAN), lai izpildītu norēķinu procesu.
4. Laukā **Ieturētā nodokļa komponentu grupa** atlasiet TDS sastāvdaļu grupu, lai palaistu norēķinu procesu.
5. Laukā **Norēķinu periods** atlasiet TDS norēķinu periodu, lai palaistu norēķinu procesu.

    > [!NOTE]
    > TDS norēķinu process tiek izpildīts visiem periodiem, kas ir iestatīti TDS norēķinu periodam cilnes **Periodi** lapā **Ieturētā nodokļa norēķinu periodi** (**Nodoklis \> Netiešie nodokļi \> Ieturētais nodoklis \> Ieturētā nodokļa norēķinu periodi**).

6. Laukā **sākuma datums** atlasiet sākuma datumu, no kā palaist TDS norēķinu procesu.

    Noteiktam periodam norēķinu periodā sākuma datumu, kas definēts šim periodam, uzskata par “no” datumu. Piemēram, TDS norēķinu periodam ir divi periodi: 2009. gada 1. aprīļa līdz 30. aprīlim, un no 2009. gada 1. maija – 31. maijam. Ja atlasāt **06/04/2009** (2009. gada 6. aprīli) kā sākuma datumu laukā **sākuma datums**, norēķinu process joprojām darbosies no 2009. gada 1. aprīļa.

    Ja laukā **sākuma datums** ievadāt vēlāku periodu, bet nenosedzot iepriekšējo periodu norēķinu periodā, norēķinu periods neparādīsies nevienam iepriekšējam periodam. Piemēram, TDS norēķinu periodam ir trīs periodi: 2009. gada 1. aprīlis līdz 30. aprīlis, 2009. gada 1. maijs līdz 31. maijs un 2009. gada 1. jūnijs līdz 30. jūnijs. ja atlasāt **01/05/2009** (2009. gada 1. maijs) kā sākuma datumu laukā **sākuma datums** norēķinu process tiks veikts tikai no 2009. gada 1. maija līdz 31. maijam. Norēķini nebūs no 2009. gada 1. aprīļa līdz 30. aprīlim.

7. Laukā **Darījuma datums** atlasiet datumu, kad grāmatot TDS norēķinu darījumu.
8. Dialoglodziņa **Ieturētā nodokļa maksājuma versija** atlasiet TDS norēķinu versiju:

     - **Sākotnējais** – izmantojiet šo opciju, lai palaistu TDS norēķinu procesu pirmo reizi. Sākotnējā maksājuma versija tiek izmantota tikai vienu reizi, lai palaistu TDS norēķinu procesu attiecībā uz TAN, ieturētā nodokļa komponenta grupas un ieturētā nodokļa norēķinu perioda kombināciju.
    - **Jaunākās versijas** – izmantojiet šo opciju, ja TDS norēķinu process jau ticis palaists norādītajam periodam. Ietveriet atpakaļ datētu darījumu, kas tika grāmatotas pēc tam, kad perioda norēķinu process tika veikts iepriekš. Šo opciju var izmantot, lai norēķinu procesu palaistu vairākas reizes.

9. Atzīmējiet izvēles rūtiņu **Atjaunināt** , lai palaistu TDS norēķinu procesu un grāmatotu summas virsgrāmatas kontos. Ja šī izvēles rūtiņa ir notīrīta, norēķinu process netiks palaists un finanšu ieraksti netiks ģenerēti.
10. Atlasiet **Labi**, lai palaistu TDS norēķinu procesu un ģenerētu ieturētā nodokļa maksājuma pārskatu. To TDS darījumu statuss, kas ietvertas norēķinu procesā, tiek rādīts kā **Nosegts** laukā **Norēķini** (dodieties uz **Kreditori \> Maksājumi \> Kreditoru maksājumu žurnāls**, atlasiet **Rindas**, atlasiet **Funkcijas** un pēc tam atlasiet **Norēķini**).

### <a name="important-points"></a>Svarīga informācija

- Ja norēķinu procesa laikā nav atlasīta ieturētā nodokļa komponentu grupa, norēķini notiek visām ieturētā nodokļa komponentu grupām atlasītajā TAN un norēķinu periodā. Katrai ieturētā nodokļa komponentu grupai lapā **Atvērt darījuma rediģēšanu** tiek izveidota atsevišķa rinda.
- Norēķinu process balstās uz norēķinu perioda vērtētāja rakstura kategoriju. Darījumi, kuros vērtētāja rakstura kategorija ir **Uzņēmums**, tiek norēķināti un tiek rādīti vienā rindā lapā **Atvērt darījuma rediģēšanu**. Darījumi, kuros vērtētāja raksturs ir kas cits, nevis **Uzņēmums**, tiek norēķināti un tiek rādīti vienā rindā lapā **Atvērt darbību rediģēšanu**.
- Apmaksāto TDS darījumu rindu izpildes termiņš lapā **Atvērt darbību rediģēšanu** ir balstīts uz maksājumu noteikumiem, kas TDS iestādes kreditoram ir noteikti lapā **Kreditori**. Ja maksājumu nosacījumi nav definēti TDS iestādes kreditoram, apmaksas perioda pēdējā diena tiek parādīta kā apmaksas datums.
