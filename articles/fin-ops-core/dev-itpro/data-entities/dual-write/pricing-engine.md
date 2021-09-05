---
title: Sinhronizēt ar Supply Chain Management cenu noteikšanas programmu pēc pieprasījuma
description: Šajā tēmā aprakstīts, kā izmantot cenu noteikšanas programmu programmā Microsoft Dynamics 365 Supply Chain Management no pakalpojuma Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c9f94ec35ebed5a14252377fb543de09cb994ffd
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416184"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Sinhronizēt ar Supply Chain Management cenu noteikšanas programmu pēc pieprasījuma

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management iekļauj cenu noteikšanas programmu, kas apstrādā tirdzniecības līgumus, cenu lapas, klientu lojalitātes programmas, veicināšanas pasākumus un atlaides. Cenu noteikšanas programma izmanto kompleksas kārtulas, lai noteiktu labāko cenu dotajam piedāvājumam vai pasūtījumam. Izmantojot duālo ierakstu, jūs izmantojat vai nu statisko cenu noteikšanu vai cenu noteikšanas programmu no Dynamics 365 Supply Chain Management piedāvājumu un pasūtījumu lapās pakalpojumā Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Izmantot cenu noteikšanas programmu no Supply Chain Management pakalpojumā Sales

1. Pakalpojumā Sales dodieties uz **Pārdošana \> Pasūtījumi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu pasūtījumu vai atlasītu esošu pasūtījumu sarakstā **Mani pasūtījumi**.
3. Pievienojiet jaunu pasūtījuma rindu.
4. Ja veidojat jaunu pasūtījumu, darbību rūtī atlasiet **Cenas pasūtījums**. Ja atjaunināt esošu pasūtījumu, darbību rūtī atlasiet **Pārrēķināt**.

    Šādas kolonnas tiek automātiski aizpildītas:

    + Detalizēta summa
    + Atlaide %
    + Atlaide
    + Summa bez vedmaksas
    + Piegādes summa
    + Nodokļu kopsumma
    + Kopsumma
    
5. Lai nodrošinātu, ka sistēma ņem vērā tirdzniecības un pārdošanas līgumus, lai aprēķinātu cenu:
    1. Dodieties uz Supply Chain Management vidi.
    2. Navigējiet uz **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
    3. Atlasiet cilni **Cenas** sānu navigācijas joslā.
    4. Saskaņā ar **Tirdzniecības līguma vērtēšanas** kopsavilkuma cilni, noņemiet atzīmi no **Manuālas ievades** opcijas.

## <a name="how-it-works"></a>Kā tas darbojas

Pakalpojumā Sales atlasot **Cenas pasūtījums** saistītajam pārdošanas pasūtījumam tiek izsaukta funkcija **Kopsumma** programmas Supply Chain Management cilnē **Pārdošanas pasūtījums \> Skatīt**. Vērtības pasūtījuma kopsummā pakalpojumā Sales tiek izmantotas, lai aizpildītu atbilstošās kolonnas programmā Supply Chain Management.

Kad pārdošanas pasūtījuma kopsumma tiek aprēķināta programmā Supply Chain Management, aprēķinā novērtē esošos tirdzniecības līgumus un pārdošanas līgumus klientam un preces, kas norādītas pārdošanas pasūtījumā. Šī informācija tiek izmantota kopsummu aprēķināšanai. Kad ir atlasīts **Cenas pasūtījums**, programma Sales automātiski ataino visus iestatījumus, kas veikti programmā Supply Chain Management.

## <a name="limitations"></a>Ierobežojumi

Kad programmā Sales ir aizpildītas kolonnas, tiek piemēroti šādi ierobežojumi:

+ Pakalpojumā Sales netiek replicēti maksu un maksu sadalījumu iestatījumi no programmas Supply Chain Management.
+ Cenu noteikšanā netiek ņemtas vērā īpašas mazumtirdzniecības cenas, kas konkretizētas pārdošanas pasūtījuma rindas lapas kolonnā **Mazumtirdzniecības kanāls** programmā Supply Chain Management.
+ Atlaides, kas definētas programmas Supply Chain Management sadaļā **Mazumtirdzniecības atlaižu pārvaldība**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]