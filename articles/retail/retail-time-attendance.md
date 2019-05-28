---
title: Laika un apmeklētības pārvaldība programmā Retail
description: Šajā tēmā ir aprakstīti scenāriji, kas tiek atbalstīti laika un apmeklētības pārvaldībai programmā Microsoft Dynamics 365 for Retail.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4c54909a02376a62a72a986e634649fa0ae54284
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567957"
---
# <a name="time-and-attendance-management-in-retail"></a>Laika un apmeklētības pārvaldība programmā Retail

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīti scenāriji, kas tiek atbalstīti laika un apmeklētības pārvaldībai programmā Microsoft Dynamics 365 for Retail.

## <a name="manage-worker-setup-and-scheduling"></a>Darbinieku iestatījumu un plānošanas pārvaldība

### <a name="initial-configuration"></a> sākotnējā konfigurācija

- Palaidiet konfigurācijas vedni.
- Reģistrējiet darbiniekus kā laika reģistrācijas darbiniekus.

### <a name="plan-worker-schedules"></a>Darbinieku grafika plānošana

- Izveidojiet profilus, izmantojot darbu plānošanas sistēmu. Papildinformāciju skatiet tēmā [Profilu izveide, izmantojot darbu plānošanas sistēmu](https://technet.microsoft.com/library/aa551234.aspx).

Papildinformāciju par konfigurācijas darbībām skatiet tēmā [Laika un apmeklētības iestatīšana](https://technet.microsoft.com/library/aa496971.aspx).

### <a name="retail-specific-configuration"></a>No mazumtirdzniecības modeļa atkarīga konfigurācija

- Iespējojiet funkcionalitātes Laika uzskaite profilu darbiniekiem, kuriem vēlaties aktivizēt laika reģistrāciju. Noklikšķiniet uz **POS funkcionalitātes profili** &gt; **Funkcijas** &gt; **POS laika reģistrācijas** &gt; **Aktivizēt laika reģistrācijas**.
- Konfigurējiet pārdošanas punkta (POS) atļaujas grupas, lai iespējotu funkcijas Skatīt laika uzskaites ierakstus atļauju. Ar šo atļauju lietotājs var skatīt citu veikala (un citu veikalu, ar kuriem lietotājs ir saistīts, izmantojot adrešu grāmatu) darbinieku laika uzskaites reģistrācijas ierakstus. Šo atļauju ieteicams aktivizēt vadītāja lomai, bet ne kasiera lomai. Noklikšķiniet uz **POS atļauju grupas** &gt; **Skatīt darba laika uzskaites ierakstus**.

## <a name="register-time"></a>Reģistra laiks

### <a name="cashier-and-non-cashier-time-registrations"></a>Kasiera un darbinieka, kas nav kasieris, laika reģistrācija

- Pārdošanas punktā (POS)

    - Ar ierašanos saistītās darbības.

        - Piesakieties, veicot ar naudas kasti nesaistītu darbību, vai sadaļā Jaunu maiņa.
        - Atlasiet darbību Laika uzskaite.
        - Atlasiet vēlamo darbību.

            - Ierašanās
            - Darba pārtraukums
            - Pusdienu pārtraukums
            - Aiziešana

        <table>
        <thead>
        <tr>
        <th>Pašreizējais statuss</th>
        <th>Pieejamās darbības</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Ierašanās</td>
        <td>
        <ul>
        <li>Darba pārtraukums</li>
        <li>Pusdienu pārtraukums</li>
        <li>Aiziešana</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>Darba pārtraukums</td>
        <td>Ierašanās</td>
        </tr>
        <tr>
        <td>Pusdienu pārtraukums</td>
        <td>Ierašanās</td>
        </tr>
        <tr>
        <td>Aiziešana</td>
        <td>Ierašanās</td>
        </tr>
        </tbody>
        </table>

        [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)

- Skatiet apstiprinājuma ziņojumu un pārbaudiet, vai pašreizējais aktivitātes laiks ir pareizs.
- Reģistrācijas žurnāls

    - Noklikšķiniet uz **Reģistrācijas žurnāls**, lai skatītu laika uzskaite aktivitāti.
    - Izmantojiet laika filtrus, lai atlasītu dažādus laika logus.
    - Ja strādājat vairākās veikala atrašanās vietās, laika reģistrācijas ieraksti ir redzami par visiem veikaliem, kuros ir reģistrēts laiks. Lai skatītu atlasītajā veikalā veiktās laika reģistrācijas, var izmantot veikalu filtru.

- Atšķirīgas laika zonas

    - Ja tiek skatīta laika uzskaite no citas atrašanās vietas (kasiera žurnālā vai izmantojot vadītāja scenārija opciju **Skatīt laika uzskaites ierakstus**) un šī atrašanās vieta atrodas citā laika joslā, redzamie laika uzskaites ieraksti tiek pārvērsti atbilstoši vietējai laika joslai. Piemēram, pieņemsim, ka esat divu veikalu vadītājs, no kuriem viens atrodas Arizonā, bet otrs atrodas Nevadā. Kasieris reģistrē ierašanos 9:00 pēc Arizonas laika. Šajā brīdī Nevadā ir 8:00. Tāpēc, ja atrodaties veikalā Nevadā un skatāt laika reģistrācijas ierakstus, ir redzams, ka laika reģistrācija ir atzīmēta 8:00.

## <a name="view-worker-time-registrations"></a>Darbinieku laika reģistrācijas ierakstu skatīšana

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Skatiet darbinieka laika reģistrācijas ierakstus un filtrējiet tos pēc veikala vai aktivitātes tipa.

Pārdošanas punktā (POS)

- Atlasiet opciju **Skatīt laika uzskaites ierakstus**.
- Var skatīt visu to darbinieku laika uzskaites reģistrācijas darbības, kas iedalīti tajos pašos veikalos, kur esat iedalīts jūs.
- Lai filtrētu laika reģistrācijas ierakstus, var izmantot aktivitātes tipa un veikala filtru.

## <a name="process-and-manage-time-registrations"></a>Laika reģistrācijas ierakstu apstrāde un pārvaldība

Dynamics 365 for Retail lietotājs izpilda darbplūsmu, lai aprēķinātu, apstiprinātu un pārsūtītu laika reģistrācijas ierakstus algas aprēķināšanai.

### <a name="primary-operations"></a>Primārās darbības

- Aprēķināt
- Apstiprināt
- Iesniegt algas aprēķināšanai

### <a name="other-common-operations"></a>Citas standarta darbības

- Aiziešana grupā
- Kavējuma reģistrēšana

Papildinformāciju par laika un apmeklētības ierakstu apstrādi skatiet tēmā[Laika un apmeklētības ierakstu apstrāde](https://technet.microsoft.com/library/aa573180.aspx).
