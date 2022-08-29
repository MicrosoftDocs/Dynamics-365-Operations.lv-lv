---
title: Sinhronizēt ar Supply Chain Management cenu noteikšanas programmu pēc pieprasījuma
description: Šajā rakstā ir aprakstīts, kā izmantot cenu noteikšanas programmu programmā Microsoft Dynamics 365 Supply Chain Management no Microsoft Dynamics 365 Pārdošanas.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 727e60ceee3f5c8c33d2da93128eedc1dc7bcb9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288962"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Sinhronizēt ar Supply Chain Management cenu noteikšanas programmu pēc pieprasījuma

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management iekļauj cenu noteikšanas programmu, kas apstrādā tirdzniecības līgumus, cenu lapas, klientu lojalitātes programmas, veicināšanas pasākumus un atlaides. Cenu noteikšanas programma izmanto kompleksas kārtulas, lai noteiktu labāko cenu dotajam piedāvājumam vai pasūtījumam. Kad izmantojat dubultās rakstīšanas, 365 pārdošanā piedāvājumu un pasūtījumu lapās izmantojat vai nu statisko cenu noteikšanu, **·** **·** Microsoft Dynamics vai cenu noteikšanas programmu no Piegādes ķēdes pārvaldības.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Izmantot cenu noteikšanas programmu no Supply Chain Management pakalpojumā Sales

1. Pakalpojumā Sales dodieties uz **Pārdošana \> Pasūtījumi**.
1. Atlasiet **Jauns**, lai izveidotu jaunu pasūtījumu vai atlasītu esošu pasūtījumu sarakstā **Mani pasūtījumi**.
1. Pievienojiet jaunu pasūtījuma rindu.
1. Ja veidojat jaunu pasūtījumu, darbību rūtī **atlasiet** Cenu pasūtījums. Ja atjaunināt esošu pasūtījumu, darbību rūtī atlasiet **Pārrēķināt**.
1. Šādas kolonnas tiek automātiski aizpildītas:

    - Detalizēta summa
    - Atlaide %
    - Atlaide
    - Summa bez vedmaksas
    - Piegādes summa
    - Nodokļu kopsumma
    - Kopsumma

> [!NOTE]
> Līdzīgs process tiek lietots, veidojot piedāvājumus.

## <a name="how-it-works"></a>Kā tas darbojas

Kad jūs izveidojiet pasūtījumu pārdošanā, šis pasūtījums nekavējoties tiek sinhronizēts Piegādes ķēžu pārvaldībā, izmantojot vērtībās, ko ievadījāt Pārdošanā. Ja atlasāt **Cenu** **pasūtījumu** vai cenu piedāvājumu pārdošanā, Piegādes ķēdes pārvaldība aprēķina cenu katrai pasūtījuma rindai un kopējo pasūtījumu, balstoties uz tirdzniecības līguma nosacījumiem, kas definēti Piegādes ķēdes pārvaldībā. Tad jaunās aprēķinātās vērtības tiek sinhronizētas atpakaļ uz Pārdošanu.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Iestatīt tirdzniecības līgumu novērtēšanas opcijas Piegādes ķēžu pārvaldībā

Varat konfigurēt, lai Piegādes ķēdes pārvaldība ievērotu vai ignorētu tirdzniecības līgumus, kad tā aprēķina pasūtījuma cenu, kas tika izveidota pārdošanā. Izpildiet šīs darbības, lai iestatītu šo opciju.

1. Piesakieties savā Piegādes ķēdes pārvaldības vidē.
1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
1. Cilnē Cenas **kopsavilkuma** cilnē Tirdzniecības **līgumu vērtēšana** pievienojiet vai noņemiet rindu manuālai ievades **politikai pēc** jūsu pieprasītā. Šīs politikas klātbūtne vai kavējums kontrolē, vai Piegādes ķēdes pārvaldības cenu noteikšanas programma automātiski atstās spēkā pārdošanas cenu, kas ievadīta Pārdošanā.

    - Ja tirdzniecības **līgumu novērtēšanas** iestatījumos *nav* manuālas **ievades politikas**, piegādes ķēdes pārvaldība ir cenu šablons. **·** **Kad** lietotājs pārdošanas rūtī atlasa cenu pasūtījumu vai cenas piedāvājumu, tiek izsaukta Piegādes ķēdes pārvaldības cenu noteikšanas programma un pārdošanā ievadītā pārdošanas cena tiek pārrakstīta, ja tā nav vienāda ar pārdošanas cenu, kas tiek aprēķināta Piegādes ķēžu pārvaldībā.
    - Ja tirdzniecības **līgumu novērtēšanas** iestatījumos *ir* manuālas **ievades politika**, pārdošana ir cenu šablons. Pārdošanas cenā ievadītā **pārdošanas** **cena** netiek automātiski pārrakstīta, kad lietotājs pārdošanas rūtī atlasa Cenu pasūtījumu vai cenas piedāvājumu.
    - Pasūtījuma rindas un piedāvājuma rindas, **kuru** vienības cena un/**·** *vai atlaides vērtība ir 0 (nulle*) pārdošanā, tiek apstrādātas kā īpašs gadījums. Ja ir pieejama atbilstoša tirdzniecības līguma cena, Piegādes ķēžu pārvaldība *vienmēr* piemēros to šiem laukiem neatkarīgi no Tirdzniecības **līguma novērtēšanas** iestatījuma.

    Lai aplūkotu piemēru katram no šiem gadījumiem, skatiet sekošanas scenārijus.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>1. piemēra: tirdzniecības līguma vērtēšana bez manuālas ievades opcijas

Šajā scenārijā tirdzniecības līgumu **vērtēšanas iestatījums** Piegādes ķēžu pārvaldībā *neietver manuālo* **ievades** politiku. Pārdošanas lietotājs ievada pasūtījuma rindu, kuras pārdošanas cena nav nulle un piegādes ķēdes pārvaldībā nav definēta šī krājuma pārdošanas cena.

1. Pārdošanā lietotājs izveido pasūtījuma rindu, kuras vienības cena **ir** 1 ASV dolārs (USD).
1. Pasūtījuma rinda ir sinhronizēta piegādes ķēžu pārvaldībā ar pārdošanas cenu 1 USD.
1. Pārdošanas pasūtījumā lietotājs atlasa **cenas** pasūtījumu darbību rūtī.
1. Piegādes ķēdes pārvaldība meklē atbilstošas cenas un atlaides un pēc tam aprēķina kopsummas. Tā kā krājumam piegādes ķēžu pārvaldībā nav pārdošanas cenas, aprēķins atjaunina rindu, lai tā pārdošanas cena būtu 0 USD.
1. Rindas jaunā pārdošanas cena tiek sinhronizēta atpakaļ uz Pārdošanu.
1. Rezultāts ir pasūtījuma rinda pārdošanā, kuras pārdošanas cena ir 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>2. scenārijs: tirdzniecības līguma vērtēšana ar manuālas ievades opciju

Šajā scenārijā tirdzniecības līgumu **vērtēšanas iestatījums** Piegādes ķēžu pārvaldībā *neietver manuālo* **ievades** politiku. Pārdošanas lietotājs ievada pasūtījuma rindu, kuras pārdošanas cena nav nulle. Piegādes ķēdes pārvaldība ietver tirdzniecības līgumu, kas nosaka pasūtītā 2 USD pārdošanas cenu.

1. Pārdošanas pasūtījumā lietotājs izveido pasūtījuma rindu krājumam, kura **vienības cena** ir 1 USD.
1. Pasūtījuma rinda ir sinhronizēta piegādes ķēžu pārvaldībā ar pārdošanas cenu 1 USD.
1. Pārdošanas pasūtījumā lietotājs atlasa **cenas** pasūtījumu darbību rūtī.
1. Tā kā **Tirdzniecības līgumu vērtēšanas** **iestatījums** Piegādes ķēžu pārvaldībā ietver manuālu ievades politiku, pārdošanas cena netiek mainīta, pat ja piemērojams tirdzniecības līgums nosaka citu pārdošanas cenu.
1. Pārdošanas cena paliek nemainīga Pārdošanas un Piegādes ķēžu pārvaldībā.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>3. piemērs: tirdzniecības līguma vērtēšana krājumam, kura pārdošanas cena ir nulle

Šajā scenārijā tirdzniecības līgumu **vērtēšanas iestatījums** Piegādes ķēžu pārvaldībā *neietver manuālo* **ievades** politiku. Pārdošanas lietotājs ievada pasūtījuma rindu, kuras pārdošanas cena ir 0 (nulle). Piegādes ķēdes pārvaldība ietver tirdzniecības līgumu, kas nosaka pasūtītā 2 USD pārdošanas cenu.

1. Pārdošanas pasūtījumā lietotājs izveido pasūtījuma **rindu**, kuras vienības cena ir 0 USD **un** rindas atlaides 0 USD.
1. Pasūtījuma rinda ir sinhronizēta piegādes ķēžu pārvaldībā ar pārdošanas cenu 0 USD.
1. Tā kā tā saņēma pasūtījuma rindu, kuras pārdošanas cena ir 0 (nulle), Supply Chain Management izsauc tās cenu noteikšanas programmu, **pat** ja ir aktivizēta manuālas ievades opcija. Cenu noteikšanas programma atgriež pārdošanas cenu 2 USD, kas ir izveidota ar tirdzniecības līgumu, un atjaunina pasūtījuma rindu Piegādes ķēžu pārvaldībā.
1. Atjauninātā pārdošanas cena vēl nav sinhronizēta ar pārdošanas pasūtījuma rindu.
1. Pārdošanas pasūtījumā lietotājs atlasa **cenas** pasūtījumu darbību rūtī.
1. Piegādes ķēdes pārvaldības pasūtījuma rinda saglabā sava pārdošanas cenu 2 USD, kas tagad tiek sinhronizēta atpakaļ uz Pārdošanu. Tādēļ Pārdošanas pasūtījuma **rindas vienības** cena tiek atjaunināta no pārdošanas 0 USD līdz 2 USD.
1. Pārdošanas pasūtījumā lietotājs ievada jaunu rindas **atlaides vērtību** 0.50 USD. Pārdošana tagad aprēķina, ka rindas **paplašinātās** summas vērtība ir 1.50 USD.
1. Pasūtījuma rinda ir sinhronizēta piegādes ķēžu pārvaldībā ar rindas **atlaides** vērtību 0.50 USD.
1. Pārdošanas pasūtījumā lietotājs atlasa **cenas** pasūtījumu darbību rūtī.
1. Pārdošanas pasūtījuma rindā nav mainītas cenas vai atlaides.

## <a name="limitations"></a>Ierobežojumi

Kad programmā Sales ir aizpildītas kolonnas, tiek piemēroti šādi ierobežojumi:

- Pakalpojumā Sales netiek replicēti maksu un maksu sadalījumu iestatījumi no programmas Supply Chain Management.
- Cenu noteikšanā netiek ņemtas vērā īpašas mazumtirdzniecības cenas, kas konkretizētas pārdošanas pasūtījuma rindas lapas kolonnā **Mazumtirdzniecības kanāls** programmā Supply Chain Management.
- Atlaides, kas definētas programmas Supply Chain Management sadaļā **Mazumtirdzniecības atlaižu pārvaldība**.
- Cenu noteikšanā netiek ņemti pārdošanas līgumi.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
