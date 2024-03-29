---
title: Automatizētu uzdevumu konfigurēšana darbplūsmā
description: Šajā rakstā ir izskaidrots, kā konfigurēt rekvizītus automatizētam uzdevumam.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b482338c436ea9226d31f74c823ee1dc141b24cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891758"
---
# <a name="configure-automated-tasks-in-a-workflow"></a>Automatizētu uzdevumu konfigurēšana darbplūsmā

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā rakstā ir izskaidrots, kā konfigurēt rekvizītus automatizētam uzdevumam.

Lai konfigurētu automatizētu uzdevumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz uzdevuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**. Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu automatizētā uzdevuma rekvizītus.

## <a name="name-the-task"></a>Nosaukuma piešķiršana uzdevumam

Izpildiet tālākos norādījumus, lai ievadītu automatizētā uzdevuma nosaukumu.

1. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
2. Laukā **Nosaukums** uzdevumam ievadiet unikālu nosaukumu.

## <a name="specify-when-notifications-are-sent"></a>Norādīt, kad tiek sūtīti paziņojumi

Varat nosūtīt lietotājiem paziņojumus, kad automatizētais uzdevums ir palaists vai atcelts. Veiciet šīs darbības, lai norādītu, kad paziņojumi tiek sūtīti un kam tie tiek sūtīti.

1. Kreisajā rūtī noklikšķiniet uz **Paziņojumi**.
2. Atzīmējiet izvēles rūtiņu pie notikumiem, lai sūtītu paziņojumus par:

    - **Izpildi** — paziņojumi tiek nosūtīti, kad uzdevums ir palaists.
    - **Atcelšanu** — paziņojumi tiek nosūtīti, kad uzdevums ir atcelts.

3. Atlasiet tāda notikuma rindu, kuru atlasījāt 2. darbībā.
4. Cilnē **Paziņojuma teksts**, tekstlodziņā ievadiet paziņojuma tekstu.
5. Lai personalizētu paziņojumu, varat ievadīt vietturus. Vietturi tiks aizvietoti ar atbilstošiem datiem, kad paziņojums tiks parādīts lietotājiem. Veiciet šīs darbības, lai ievietotu vietturi:

    1. Tekstlodziņā noklikšķiniet uz vietas, kur jāparādās vietturim.
    2. Noklikšķiniet uz **Ievietot vietturi**.
    3. Parādītajā sarakstā atlasiet vietturi, kuru ievietot.
    4. Noklikšķiniet uz **Ievietot**.

6. Lai pievienotu paziņojuma tulkojumus, rīkojieties šādi:

    1. Noklikšķiniet uz **Tulkojumi**.
    2. Parādītajā lapā noklikšķiniet uz **Pievienot**.
    3. Parādītajā sarakstā izvēlieties valodu, kas tiek izmantota teksta ievadei.
    4. Laukā **Tulkotais teksts** ievadiet tekstu.
    5. Lai personalizētu tekstu, var ievadīt vietturus, kā aprakstīts 5. darbībā.
    6. Noklikšķiniet uz **Aizvērt**.

7. Cilnē **Adresāts** norādiet personu, kurai paziņojumi tiek nosūtīti. Atlasiet vienu no tālāk redzamajā tabulā minētajām opcijām un pēc tam veiciet papildu darbības attiecīgajai opcijai, pirms pārejat uz 8. darbību.

    <table>
    <thead>
    <tr>
    <th>Opcija</th>
    <th>Paziņojuma adresāti</th>
    <th>Papildu transakcijas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Dalībnieks</td>
    <td>Lietotāji, kuri ir piešķirti noteiktai grupai vai lomai</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Dalībnieks</strong>, cilnes <strong>Pēc lomas</strong> sarakstā <strong>Dalībnieka tips</strong> atlasiet grupas tipu vai lomu, kurai nosūtīt paziņojumu.</li>
    <li>Sarakstā <strong>Dalībnieks</strong> atlasiet grupu vai lomu, kurai nosūtīt paziņojumus.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Darbplūsmas lietotājs</td>
    <td>Lietotāji, kuri piedalās pašreizējā darbplūsmā</td>
    <td>
    <ul>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Darbplūsmas lietotājs</strong>, cilnes <strong>Darbplūsmas lietotājs</strong> sarakstā <strong>Darbplūsmas lietotājs</strong> atlasiet lietotāju, kas piedalās attiecīgajā darbplūsmā.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Lietotājs</td>
    <td>Īpaši lietotāji</td>
    <td>
    <ol>
    <li>Pēc tam, kad ir atlasīts vienums <strong>Lietotājs</strong>, noklikšķiniet uz cilnes <strong>Lietotājs</strong>.</li>
    <li>Sarakstā <strong>Pieejamie lietotāji</strong> ir ietverti visi lietotāji. Atlasiet lietotājus, kuriem sūtīt paziņojumus, un pēc tam pārvietojiet šos lietotājus uz sarakstu <strong>Atlasītie lietotāji</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Atkārtojiet 3.–7. darbību katram notikumam, ko atlasījāt 2. darbībā.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]