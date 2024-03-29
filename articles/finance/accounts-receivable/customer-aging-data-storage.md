---
title: Klientu vecumstruktūras datu krātuve
description: Šajā rakstā ir aprakstīts process, kad debitoru vecumstruktūras datiem tiek izmantota ārējā krātuve. Jūs varat palaist Debitoru vecumstruktūras datu glabāšanas procesu, lai izvade būtu pieejama eksportam uz ārēju sistēmu.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7a66485cc9a538f5c3999009b6dbe295d7a5b9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894147"
---
# <a name="customer-aging-data-storage"></a>Klientu vecumstruktūras datu krātuve

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts process, kad debitoru vecumstruktūras datiem tiek izmantota ārējā krātuve. Microsoft Dynamics 365. finanšu gadā varat **palaist** debitoru vecumstruktūras datu glabāšanas procesu, lai padarītu izvadi pieejamu eksportam uz ārēju sistēmu. Kad izpildījāt procesu, ārējās sistēmā pieejamās vecumstruktūras pārskata opcijas ir pieejamas arī ārējās sistēmas. Dati vienmēr tiek iekļauti eksportētos datos.

Tas var būt lietderīgi, lai padarītu debitoru vecumstruktūras datus pieejamus ārējai sistēmai glabāšanai gadījumos, kad izvadei ir daudz debitoru un/vai daudzas darbības. Ja esošais Debitoru **vecumstruktūras** pārskats ieiet, jo tam ir pārāk daudz datu, ko drukāt, šī funkcija nodrošina alternatīvu veidu, kā iegūt tos pašus datus.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Iespējot debitoru vecumstruktūras datu glabāšanas līdzekli

Pirms varat lietot šo funkciju, jums tā ir jāiespējo savā sistēmā. Administratori var izmantot līdzekļu pārvaldības iestatījumus, lai pārbaudītu funkcijas statusu un aktivizētu to, ja nepieciešams. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis: kredīts** un kolekcijas
- **Līdzekļa nosaukums:** debitora vecumstruktūras datu krātuve

## <a name="run-the-customer-aging-data-storage-process"></a>Palaist debitora vecumstruktūras datu glabāšanas procesu

1. Pārejiet uz **Sadaļu Debitoru vecumstruktūras datu krātuve \> Kreditēt \> un iekasēšanas pieprasījumus \> un sniedz pārskatu par debitoru vecumstruktūras datu krātuvi**.
2. Atlasiet **Jauna**.
3. **Laukā** Nosaukums ievadiet procesa nosaukumu.
4. Iestatiet atlikušos parametrus pēc pieprasāmā.

    > [!NOTE]
    > Darbības detaļas tiek vienmēr iekļautas, un apstrāde vienmēr tiek veikta pakešuzdevumā.

5. Atlasiet **Labi**.
6. Atsvaidzināt lapu Debitoru **vecumstruktūras datu** krātuve **·** **, lai redzētu paketes nosaukumu un partijas izpildes laika** vērtības, kas tiek rādītas kopā ar **apstrādes statusa** vērtību. Kad pakešuzdevums ir pabeigts, apstrādes statusa **lauks ir** iestatīts uz Pabeigts **un** tiek **iestatīts vecumstruktūras** rindu skaits. Ja pakešuzdevums ir periodisks, apstrādes statusa **lauks ir** iestatīts uz **Gaida**.
7. Atlasiet pogu **Filtrs** blakus laukam **Vecumstruktūras rindas**, lai pārskatītu filtrus, kas ir pievienoti pakešuzdevumam.

Debitoru **vecumstruktūras datu** glabāšanas lapā nav ietverti rezultāti. Tomēr Debitora vecumstruktūras **datu krātuves** datu elements ļauj eksportēt izvadi uz jebkuru formātu, ko datu pārvaldība atbalsta.

> [!NOTE]
> Pirms eksportēšanas pievienojiet filtru, lai ierobežotu eksportētos rezultātus uz jaunākajām vecumstruktūrām. Piemēram, pievienojiet šādus kritērijus, lai atgrieztu pēdējo paketes darbību:
>
> (CustAgingDataStorageSysQueryRangeUtil:: getLatestBatchName())
>
> Vai arī pievienojiet šādus kritērijus, lai atgrieztu pašreizējā lietotāja jaunāko pakešuzdevumu:
>
> (CustAgingDataStorageSysQueryRangeUtil:: getLatestBatchNameForCurrentUser())
