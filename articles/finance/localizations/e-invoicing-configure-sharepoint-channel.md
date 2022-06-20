---
title: Konfigurēt SharePoint kanālu
description: Šajā rakstā ir izskaidrots, kā konfigurēt Microsoft kanālu SharePoint ienākošo elektronisko rēķinu apstrādāšana.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 89538adde4d14212fb0deccad05f828d146f16db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910046"
---
# <a name="configure-a-sharepoint-channel"></a>Konfigurēt SharePoint kanālu

[!include [banner](../includes/banner.md)]

Kā priekšnosacījums Microsoft kanāla konfigurēšanai SharePoint apstrādāt ienākošos dokumentus, veiciet aprakstītās darbības, kas aprakstītas [sadaļā Savienojuma SharePoint konfigurēšana](e-invoicing-create-sharepoint-connection.md).

Pēc tam varat izmantot kanālu SharePoint, lai importētu elektroniskos kreditora rēķinus no mapēs glabātajiem SharePoint failiem.

1. Jūsu vietnē SharePoint izveidojiet šādas mapes:

    - **Galvenā mape** – mape, no kuras pakalpojums apstrādās failus.
    - **Arhīva** mape – mape, kurā tiks uzglabāti apstrādātie faili.
    - **Kļūdas mape** – mape, uz kuru sistēma pārvietos failus, ja apstrāde neizdodas.

2. Regulēšanas konfigurācijas pakalpojumā (RCS) atlasiet savu izveidoto elektronisko rēķinu izrakstīšanas līdzekli. Pārliecinieties, vai ir atlasīta versija ar statusu **Melnraksts**.
3. Cilnē **Iestatījumi** atlasiet **Pievienot**.
4. Nolaižamā dialoglodziņa **Izveidot līdzekļu** iestatījumu nolaižamajā izvēlnē Jauna lauku **grupa** atlasiet opciju Pielāgots **iestatījums**.
5. **Iestatījumu tipa lauku** grupā atlasiet datu kanāla **opciju**.
6. Laukā **Datu kanāla** atlase atlasiet **SharePoint mapi**.
7. Atlasiet **Izveidot**.
8. Atlasiet izveidoto rindu un pēc tam atlasiet **Rediģēt**.
9. Cilnē Datu **kanāls** sadaļā Parametri iestatiet **šādus** nepieciešamos laukus.

    | Lauks                 | Apraksts |
    |-----------------------|-------------|
    | Datu kanāls          | Ievadiet unikālu nosaukumu, lai identificētu datu kanālu. Nosaukumam var būt ne vairāk kā 10 rakstzīmes. Uz to tiks atsauce piemērojamības noteikumos un pievienotajā programmā sakaru procesa laikā. |
    | SharePoint adrese    | Ievadiet SharePoint URL. Piemēram, ievadiet `<domain>.sharepoint.com`. |
    | Pieteikuma ID        | Ievadiet Azure atslēgas Konta noslēpuma vārdu, kas satur lietotāja SharePoint konta ID. Šis noslēpums ir jāizveido Key Siam, Toms un jāiestata jūsu apkalpošanas vidē. Šī vērtība ir programmas **(klienta) ID vērtība** no konfigurācijas [SharePoint savienojuma](e-invoicing-create-sharepoint-connection.md). |
    | Pieteikuma noslēpums    | Ievadiet Atslēgas Konta noslēpuma vārdu, kas satur lietotāja konta SharePoint paroli. Šī vērtība ir Programmas reģistrācijas **slepenā vērtība** no [Konfigurēt SharePoint savienojumu](e-invoicing-create-sharepoint-connection.md). |
    | Vietnes nosaukums             | Ievadiet vietas SharePoint nosaukumu. |
    | Dokumentu bibliotēkas nosaukums | Ievadiet dokumentu bibliotēkas SharePoint nosaukumu. |
    | Noilgums               | Ievadiet maksimālo laiku milisekundēs (ms), kas sistēmai jāgaida līdz atbildei. Noklusētā vērtība ir 10 000 ms (10 sekundes). |
    | Galvenā mape           | Norādiet faila importēšanas avotu vai mapi, no kuras pakalpojumam jāapstrādā faili. |
    | Arhīva mape        | Norādiet mapi, kur jāsaglabā apstrādātie faili. |
    | Kļūdu mape          | Norādiet mapi, uz kuru sistēmai jāpārvieto faili apstrādes kļūmes gadījumā. |
    | Maksimālais faila lielums         | Ievadiet viena apstrādātā faila maksimālo lielumu baitos. Noklusētā vērtība ir 20,000,000 baitiem. |
    | Maksimālais failu skaits      | Ievadiet maksimālo failu skaitu, ko apstrādāt vienai darbībai. Ja nevēlaties ierobežot failu skaitu, **iestatiet vērtību 0** (nulle). |
    | Failu filtrs           | Ievadiet virkni filtrēšanai pēc faila nosaukuma. Šis lauks nav obligāts. Tiek atbalstīta vienkārša maska, piemēram **\*smth\*.ext**, kur katra zvaigznīte (\*) ir nulle vai vairāk jebkuras rakstzīmes gadījumu. Piemēram, ievadiet **\*.pdf,** lai konfigurētu kanālu PDF failu lasīšanai. |
    | Pielāgots faila nosaukums      | Ievadiet klienta pielāgotā faila nosaukumu. |

10. Cilnē Piemērojamības **noteikumi** pārskatiet un atjauniniet kritērijus, kā nepieciešams. Kanāla lauka vērtībai **jābūt** vienādai ar vērtību, kuru ievadījāt **iepriekšējā soļa** datu kanāla laukā.
11. Atlasiet **Saglabāt** un aizveriet lapu.
