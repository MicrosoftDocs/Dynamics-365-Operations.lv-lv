---
title: SharePoint Kanāla konfigurēšana
description: Šajā tēmā skaidrots, kā konfigurēt Microsoft kanālu SharePoint ienākošo elektronisko rēķinu apstrādāt.
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
ms.openlocfilehash: ea3e14ed00b0661d3923c1839135378a8a550499
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371953"
---
# <a name="configure-a-sharepoint-channel"></a>SharePoint Kanāla konfigurēšana

[!include [banner](../includes/banner.md)]

Kā priekšnosacījums Microsoft kanāla konfigurēšanai SharePoint apstrādāt ienākošos dokumentus, veiciet aprakstītās darbības, kas aprakstītas [sadaļā Savienojuma SharePoint konfigurēšana](e-invoicing-create-sharepoint-connection.md).

Pēc tam varat izmantot kanālu SharePoint, lai importētu elektroniskos kreditora rēķinus no mapēs glabātajiem SharePoint failiem.

1. Jūsu vietnē SharePoint izveidojiet šādas mapes:

    - **Galvenā mape** – mape, no kuras pakalpojums apstrādās failus.
    - **Arhīva** mape – mape, kurā tiks uzglabāti apstrādātie faili.
    - **Kļūdas mape** – mape, uz kuru sistēma pārvietos failus, ja apstrāde neizdodas.

2. Regulatīvās konfigurācijas pakalpojumā (RCS) atlasiet izveidoto elektronisko rēķinu izrakstīšanas līdzekli. Noteikti atlasiet versiju, kuras statuss **ir Melnraksts**.
3. Cilnē **Iestatījumi** atlasiet **Pievienot**.
4. Dialoglodziņa Līdzekļu iestatīšanas **izveide** nolaižamajā sarakstā **Jauns** lauku grupā atlasiet opciju **Pielāgota iestatīšana**.
5. **Lauku grupā Uzstādījumi tips** atlasiet opciju **Datu kanāls**.
6. Laukā **Datu kanāla** atlase atlasiet **SharePoint mapi**.
7. Atlasiet **Izveidot**.
8. Atlasiet izveidoto rindu un pēc tam atlasiet **Rediģēt**.
9. Cilnes **Datu kanāls** **sadaļā Parametri** iestatiet šādus nepieciešamos laukus.

    | Lauks                 | Apraksts |
    |-----------------------|-------------|
    | Datu kanāls          | Ievadiet unikālu nosaukumu, lai identificētu datu kanālu. Nosaukumā var būt ne vairāk kā 10 rakstzīmes. Uz to tiks atsauce piemērojamības noteikumos un pievienotajā programmā sakaru procesa laikā. |
    | SharePoint adrese    | Ievadiet SharePoint URL. Piemēram, ievadiet `<domain>.sharepoint.com`. |
    | Pieteikuma ID        | Ievadiet Azure atslēgas Konta noslēpuma vārdu, kas satur lietotāja SharePoint konta ID. Šis noslēpums ir jāizveido Key Vault un jāiestata jūsu apkalpošanas vidē. Šī vērtība ir programmas **(klienta) ID vērtība** no konfigurācijas [SharePoint savienojuma](e-invoicing-create-sharepoint-connection.md). |
    | Pieteikuma noslēpums    | Ievadiet Atslēgas Konta noslēpuma vārdu, kas satur lietotāja konta SharePoint paroli. Šī vērtība ir Programmas reģistrācijas **slepenā vērtība** no [Konfigurēt SharePoint savienojumu](e-invoicing-create-sharepoint-connection.md). |
    | Vietnes nosaukums             | Ievadiet vietas SharePoint nosaukumu. |
    | Dokumentu bibliotēkas nosaukums | Ievadiet dokumentu bibliotēkas SharePoint nosaukumu. |
    | Noilgums               | Ievadiet maksimālo laiku milisekundēs (ms), kas sistēmai jāgaida līdz atbildei. Noklusējuma vērtība ir 10 000 ms (10 sekundes). |
    | Galvenā mape           | Norādiet faila importēšanas avotu vai mapi, no kuras pakalpojumam jāapstrādā faili. |
    | Arhīva mape        | Norādiet mapi, kur jāsaglabā apstrādātie faili. |
    | Kļūdu mape          | Norādiet mapi, uz kuru sistēmai jāpārvieto faili apstrādes kļūmes gadījumā. |
    | Maksimālais faila lielums         | Ievadiet viena apstrādātā faila maksimālo lielumu baitos. Noklusējuma vērtība tiek 20,000,000 baitiem. |
    | Maksimālais failu skaits      | Ievadiet maksimālo failu skaitu, ko apstrādāt vienai darbībai. Ja nevēlaties ierobežot failu skaitu, **iestatiet vērtību 0** (nulle). |
    | Failu filtrs           | Ievadiet virkni filtrēšanai pēc faila nosaukuma. Šis lauks nav obligāts. Tiek atbalstīta vienkārša maska, piemēram **\*smth\*.ext**, kur katra zvaigznīte (\*) ir nulle vai vairāk jebkuras rakstzīmes gadījumu. Piemēram, ievadiet **\*.pdf,** lai konfigurētu kanālu PDF failu lasīšanai. |
    | Pielāgots faila nosaukums      | Ievadiet klienta pielāgotā faila nosaukumu. |

10. Cilnē Piemērojamības **kārtulas** pārskatiet un atjauniniet kritērijus pēc vajadzības. Kanāla lauka vērtībai **jābūt** vienādai ar vērtību, kuru ievadījāt **iepriekšējā soļa** datu kanāla laukā.
11. Atlasiet **Saglabāt** un aizveriet lapu.
