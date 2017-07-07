---
title: "Mazumtirdzniecības laiks un apmeklētība"
description: "Šajā tēmā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Finance and Operations — Retail atbalstītie laika un apmeklētības pārvaldības scenāriji."
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: b458d1938f49a2f33f7dd3ce3062880f0d4d7bfc
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017



---

# <a name="retail-time-and-attendance"></a>Mazumtirdzniecības laiks un apmeklētība

[!include[banner](includes/banner.md)]


Šajā tēmā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Finance and Operations — Retail atbalstītie laika un apmeklētības pārvaldības scenāriji. 

<a name="manage-worker-setup-and-scheduling"></a>Darbinieku iestatījumu un plānošanas pārvaldība
----------------------------------

### <a name="initial-configuration"></a> sākotnējā konfigurācija

-   Palaidiet konfigurācijas vedni.
-   Reģistrējiet darbiniekus kā laika reģistrācijas darbiniekus.

### <a name="plan-worker-schedules"></a>Darbinieku grafika plānošana

-   Izveidojiet profilus, izmantojot darbu plānošanas sistēmu. Sīkāku informāciju skatiet šeit: <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Informāciju par konfigurācijas soļiem skatiet šeit: <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>No mazumtirdzniecības modeļa atkarīga konfigurācija

-   Iespējojiet funkcionalitātes Laika uzskaite profilu darbiniekiem, kuriem vēlaties aktivizēt laika reģistrāciju. Noklikšķiniet uz **POS funkcionalitātes profili** &gt; **Funkcijas** &gt; **POS laika reģistrācijas** &gt; **Aktivizēt laika reģistrācijas**.
-   Konfigurējiet pārdošanas punkta (POS) atļaujas grupas, lai iespējotu funkcijas Skatīt laika uzskaites ierakstus atļauju. Ar šo atļauju lietotājs var skatīt citu veikala (un citu veikalu, ar kuriem lietotājs ir saistīts, izmantojot adrešu grāmatu) darbinieku laika uzskaites reģistrācijas ierakstus. Šo atļauju ieteicams aktivizēt vadītāja lomai, bet ne kasiera lomai. Noklikšķiniet uz **POS atļauju grupas** &gt; **Skatīt darba laika uzskaites ierakstus**.

## <a name="register-time"></a>Reģistra laiks
### <a name="cashier-and-non-cashier-time-registrations"></a>Kasiera un darbinieka, kas nav kasieris, laika reģistrācija

-   Pārdošanas punktā (POS)
    -   Ar ierašanos saistītās darbības.
        -   Piesakieties, veicot ar naudas kasti nesaistītu darbību, vai sadaļā Jaunu maiņa.
        -   Atlasiet darbību Laika uzskaite.
        -   Atlasiet vēlamo darbību.
            -   Ierašanās
            -   Darba pārtraukums
            -   Pusdienu pārtraukums
            -   Aiziešana

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Pašreizējais statuss</th>
    <th>Pieejamās darbības</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Ierašanās</td>
    <td><ul>
    <li>Darba pārtraukums</li>
    <li>Pusdienu pārtraukums</li>
    <li>Aiziešana</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Darba pārtraukums</td>
    <td>Ierašanās</td>
    </tr>
    <tr class="odd">
    <td>Pusdienu pārtraukums</td>
    <td>Ierašanās</td>
    </tr>
    <tr class="even">
    <td>Aiziešana</td>
    <td>Ierašanās</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Skatiet apstiprinājuma ziņojumu un pārbaudiet, vai pašreizējais aktivitātes laiks ir pareizs.
-   Reģistrācijas žurnāls
    -   Noklikšķiniet uz **Reģistrācijas žurnāls**, lai skatītu laika uzskaite aktivitāti.
    -   Izmantojiet laika filtrus, lai atlasītu dažādus laika logus.
    -   Ja strādājat vairākās veikala atrašanās vietās, laika reģistrācijas ieraksti ir redzami par visiem veikaliem, kuros ir reģistrēts laiks. Lai skatītu atlasītajā veikalā veiktās laika reģistrācijas, var izmantot veikalu filtru.

<!-- -->

-   Atšķirīgas laika zonas
    -   Ja tiek skatīta laika uzskaite no citas atrašanās vietas (kasiera žurnālā vai izmantojot vadītāja scenārija opciju **Skatīt laika uzskaites ierakstus**) un šī atrašanās vieta atrodas citā laika joslā, redzamie laika uzskaites ieraksti tiek pārvērsti atbilstoši vietējai laika joslai. Piemēram, pieņemsim, ka esat divu veikalu vadītājs, no kuriem viens atrodas Arizonā, bet otrs atrodas Nevadā. Kasieris reģistrē ierašanos 9:00 pēc Arizonas laika. Šajā brīdī Nevadā ir 8:00. Tāpēc, ja atrodaties veikalā Nevadā un skatāt laika reģistrācijas ierakstus, ir redzams, ka laika reģistrācija ir atzīmēta 8:00.

## <a name="view-worker-time-registrations"></a>Darbinieku laika reģistrācijas ierakstu skatīšana
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Skatiet darbinieka laika reģistrācijas ierakstus un filtrējiet tos pēc veikala vai aktivitātes tipa.

Pārdošanas punktā (POS)

-   Atlasiet opciju **Skatīt laika uzskaites ierakstus**.
-   Var skatīt visu to darbinieku laika uzskaites reģistrācijas darbības, kas iedalīti tajos pašos veikalos, kur esat iedalīts jūs.
-   Lai filtrētu laika reģistrācijas ierakstus, var izmantot aktivitātes tipa un veikala filtru.

## <a name="process-and-manage-time-registrations"></a>Laika reģistrācijas ierakstu apstrāde un pārvaldība
Programmatūras Dynamics 365 for Finance and Operations — Retail lietotājs var sekot līdzi darbplūsmai, lai aprēķinātu, apstiprinātu un pārsūtītu laika reģistrācijas ierakstus algas aprēķināšanai.

### <a name="primary-operations"></a>Primārās darbības

-   Aprēķināt
-   Apstiprināt
-   Iesniegt algas aprēķināšanai

### <a name="other-common-operations"></a>Citas standarta darbības

-   Aiziešana grupā
-   Kavējuma reģistrēšana

Papildinformāciju par laika un apmeklētības reģistrācijas ierakstu apstrādi skatiet šeit: <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




