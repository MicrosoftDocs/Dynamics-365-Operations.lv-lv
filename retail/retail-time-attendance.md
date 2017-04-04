---
title: "Mazumtirdzniecības laiks un apmeklētība"
description: "Šajā tēmā ir aprakstīts, kurus atbalsta Microsoft Dynamics 365 operācijām - mazumtirdzniecības laika un apmeklējumu vadības scenārijiem."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>Mazumtirdzniecības laiks un apmeklētība

Šajā tēmā ir aprakstīts, kurus atbalsta Microsoft Dynamics 365 operācijām - mazumtirdzniecības laika un apmeklējumu vadības scenārijiem. 

<a name="manage-worker-setup-and-scheduling"></a>Pārvaldīt darbinieku iestatīšanas un plānošanas
----------------------------------

### <a name="initial-configuration"></a> sākotnējā konfigurācija

-   Palaidiet konfigurācijas vedni.
-   Reģistrējiet darbiniekus kā laika reģistrācijas darbiniekus.

### <a name="plan-worker-schedules"></a>Darbinieku grafika plānošana

-   Izveidojiet profilus, izmantojot darbu plānošanas sistēmu. Sīkāku informāciju skatiet šeit: <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Informāciju par konfigurācijas soļiem skatiet šeit: <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>No mazumtirdzniecības modeļa atkarīga konfigurācija

-   Iespējojiet funkcionalitātes Laika uzskaite profilu darbiniekiem, kuriem vēlaties aktivizēt laika reģistrāciju. Noklikšķiniet uz **POS funkcionalitāti profili**&gt;**funkcijas**&gt;**POS laika reģistrācijām**&gt;**iespējot laika reģistrācijas**.
-   Konfigurējiet pārdošanas punkta (POS) atļaujas grupas, lai iespējotu funkcijas Skatīt laika uzskaites ierakstus atļauju. Ar šo atļauju lietotājs var skatīt citu veikala (un citu veikalu, ar kuriem lietotājs ir saistīts, izmantojot adrešu grāmatu) darbinieku laika uzskaites reģistrācijas ierakstus. Šo atļauju ieteicams aktivizēt vadītāja lomai, bet ne kasiera lomai. Noklikšķiniet uz **POS permission grupas**&gt;**apskatīt ierakstus, laika pulksteni**.

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
    -   Ja tiek skatīta laika uzskaite no citas atrašanās vietas (kasiera žurnālā vai izmantojot vadītāja scenārija opciju **Skatīt laika uzskaites ierakstus**) un šī atrašanās vieta atrodas citā laika joslā, redzamie laika uzskaites ieraksti tiek pārvērsti atbilstoši vietējai laika joslai. Piemēram, jūs esat vadītājs divi veikali, viens Arizonā un citu Nevada. Kase reģistrē ierašanās pie 9:00 A.M. Arizona. Šajā brīdī Nevadā ir 8:00. Tāpēc, ja atrodaties veikalā Nevadā un skatāt laika reģistrācijas ierakstus, ir redzams, ka laika reģistrācija ir atzīmēta 8:00.

## <a name="view-worker-time-registrations"></a>Skatiet darbinieka laika reģistrācijas
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Skatiet darbinieka laika reģistrācijas ierakstus un filtrējiet tos pēc veikala vai aktivitātes tipa.

Pārdošanas punktā (POS)

-   Atlasiet opciju **Skatīt laika uzskaites ierakstus**.
-   Var skatīt visu to darbinieku laika uzskaites reģistrācijas darbības, kas iedalīti tajos pašos veikalos, kur esat iedalīts jūs.
-   Lai filtrētu laika reģistrācijas ierakstus, var izmantot aktivitātes tipa un veikala filtru.

## <a name="process-and-manage-time-registrations"></a>Apstrādāt un pārvaldīt laika reģistrācijas
Dynamics 365 operācijām - mazumtirdzniecības lietotāja izriet aprēķināšana, apstiprināšana un pārsūtīt laika reģistrācijas algas darbplūsmu.

### <a name="primary-operations"></a>Primārās darbības

-   Aprēķināt
-   Apstiprināt
-   Iesniegt algas aprēķināšanai

### <a name="other-common-operations"></a>Citas standarta darbības

-   Aiziešana grupā
-   Kavējuma reģistrēšana

Papildinformāciju par laika un apmeklētības reģistrācijas ierakstu apstrādi skatiet šeit: <https://technet.microsoft.com/en-us/library/aa573180.aspx>.


