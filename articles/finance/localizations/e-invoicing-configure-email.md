---
title: Konfigurēt e-pasta kanālu
description: Šajā rakstā ir izskaidrots, kā konfigurēt e-pasta kanālu elektronisko rēķinu saņemšanai.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9227b032ffe896ad6a67962e5047fd797a883ae1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902390"
---
# <a name="configure-an-email-channel"></a>Konfigurēt e-pasta kanālu

[!include [banner](../includes/banner.md)]

Ja funkcija Elektronisko rēķinu izrakstīšana, ko izveidojāt, importē elektroniskos kreditora rēķinus no pievienotajiem failiem, kas tiek saņemti ar e-pastu, jums ir jākonfigurē e-pasta konta kanāls.

1. Regulēšanas konfigurācijas pakalpojumā (RCS) atlasiet savu izveidoto elektronisko rēķinu izrakstīšanas līdzekli. Pārliecinieties, vai ir atlasīta versija ar statusu **Melnraksts**.
2. **Cilnē Iestatījumi** atlasiet **Pievienot**.
3. Nolaižamā dialoglodziņa **Izveidot līdzekļu** iestatījumu nolaižamajā izvēlnē Jauna lauku **grupa** atlasiet opciju Pielāgots **iestatījums**.
4. **Iestatījumu tipa lauku** grupā atlasiet datu kanāla **opciju**.
5. Laukā Datu **kanāla atlase** ievadiet Ienākošais **e-pasts**.
6. Atlasiet **Izveidot**.
7. Atlasiet izveidoto rindu un pēc tam atlasiet **Rediģēt**.
8. Cilnē Datu **kanāls** sadaļā Parametri iestatiet **šādus** nepieciešamos laukus.

    | Lauks                | Apraksts |
    |----------------------|-------------|
    | Datu kanāls         | Ievadiet unikālu nosaukumu, lai identificētu datu kanālu. Nosaukumam var būt ne vairāk kā 10 rakstzīmes. Uz to tiks atsauce piemērojamības noteikumos un pievienotajā programmā sakaru procesa laikā. |
    | Servera adrese       | Ievadiet e-pasta konta nodrošinātāja servera adresi. Piemēram, nodrošinātāja servera adrese `https://outlook.live.com` ir imap-mail.outlook.com. |
    | Servera ports          | Ievadiet tā porta numuru, ko izmanto e-pasta konta nodrošinātājs. Piemēram, servera ports nodrošinātājam `https://outlook.live.com` ir 993. |
    | Lietotājvārda noslēpums     | Ievadiet Atslēgas Microsoft Azure Pamatteksta noslēpuma vārdu, kas satur e-pasta lietotāja konta ID. Šis noslēpums ir jāizveido Key Siam, Toms un jāiestata jūsu apkalpošanas vidē. |
    | Lietotāja paroles noslēpums | Ievadiet Atslēgas Pamatteksta noslēpuma vārdu, kas satur e-pasta lietotāja konta paroli. |
    | Noilgums              | Maksimālais laika ierobežojums milisekundēs (ms), kas sistēmai jāgaida līdz atbildei. Noklusētā vērtība ir 10 000 ms (10 sekundes). |
    | Galvenā mape          | Norādiet e-pasta importēšanas avotu vai mapi, no kuras jāapstrādā e-pasta ziņojumi. |
    | Arhīva mape       | Norādiet mapi, kurā jāsaglabā apstrādātie e-pasta ziņojumi. Ja nenorādīsiet šo mapi, sistēma to izveidos automātiski. |
    | Kļūdu mape         | Norādiet mapi, uz kuru sistēmai ir jāpārvieto e-pasta ziņojumi, ja apstrāde neizdodas. Ja nenorādīsiet šo mapi, sistēma to izveidos automātiski. |
    | Maksimālais ziņojuma lielums     | Ievadiet viena apstrādātā ziņojuma maksimālo lielumu baitos. Noklusētā vērtība ir 20,000,000 baitiem. |
    | Maksimālais ziņojumu skaits   | Ievadiet maksimālo ziņojumu skaitu, ko apstrādāt vienai darbībai. Ja nevēlaties ierobežot ziņojumu skaitu, iestatiet vērtību **0** (nulle). |
    | No filtra          | Ievadiet virkni filtrēšanai pēc sūtītāja adreses. Tiks apstrādāti tikai tie e-pasta ziņojumi, kuros sūtītāja adrese atbilst filtram. Šis lauks nav obligāts. Lai norādītu vairākas sūtītāja adreses, lietojiet semikolus (;) kā atdalītājus. |
    | Tēmu filtrs       | Ievadiet virkni filtrēšanai pēc tēmas. Tiks apstrādāti tikai tie e-pasta ziņojumi, kuros tēma atbilst filtram. Šis lauks nav obligāts. Tiek atbalstīta vienkārša maska, piemēram **\*smth\*.ext**, kur katra zvaigznīte (\*) ir nulle vai vairāk jebkuras rakstzīmes gadījumu. |
    | Datuma filtrs          | Norādiet datumu, kurā definēt apstrādāto ziņojumu maksimālo vecumu dienās. Šis lauks nav obligāts. Noklusējuma vērtība ir 30 dienas. |
    | Apstrādes režīms      | <p>Atlasiet vienu no šīm opcijām, lai norādītu, vai visus e-pasta pielikumus var apstrādāt kopā vai arī katrs pielikums ir jāapstrādā atsevišķi:</p><ul><li><b>Ar pielikumu</b> – katram e-pasta pielikumam tiks izveidots jauns elektronisks dokuments. Piemēram, ja vienā e-pasta ziņojumā ir ietverti vairāki faili, kas satur e-rēķina datus, katrs fails sistēmā tiks uzskatīts par jaunu e-rēķinu.</li><li><b>Pa e-pastu</b> – viens pielikums tiks uzskatīts par pamata pielikumu, un viens elektroniskais rēķins tiks izveidots sistēmā. Citus pielikumus var izmantot kā atbalsta failus.</li></ul> |

9. **Sadaļā Pielikumu filtrs** pievienojiet informāciju par failu filtrēšanu. Tiks apstrādāti tikai tie pielikumi, kas atbilst definētam filtram. Piemēram, **\*.xml tiks** filtrēti pielikumiem, kuriem ir .xml faila nosaukuma paplašinājums. Pielikuma nosaukums tiek izmantots Dynamics 365 Finanses vai iestatīšanas Dynamics 365 Supply Chain Management laikā.

    - Ja iepriekšējā darbībā laukā **Apstrādes** režīms iestatāt **vērtību** Pa e-pastu, šeit varat pievienot vairākus filtrus. Nosaukums identificēs konkrētu dokumentu.
    - Ja apstrādes režīma lauks **tiek** iestatīts uz **Pēc pielikuma**, varat pievienot tikai vienu filtru.

10. Cilnē Piemērojamības **noteikumi** pārskatiet un atjauniniet kritērijus, kā nepieciešams. Kanāla lauka vērtībai **jābūt** vienādai ar vērtību, ko jūs ievadījāt **Datu kanāla** laukā 8. darbībā.
11. Atlasiet **Saglabāt** un aizveriet lapu.
