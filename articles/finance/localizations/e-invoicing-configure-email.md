---
title: E-pasta kanāla konfigurēšana
description: Šajā tēmā ir paskaidrots, kā konfigurēt e-pasta kanālu, lai saņemtu elektroniskos rēķinus.
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
ms.openlocfilehash: 6a5896a033212cf0f29f686eec0ab6fb3bc1d2a6
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371929"
---
# <a name="configure-an-email-channel"></a>E-pasta kanāla konfigurēšana

[!include [banner](../includes/banner.md)]

Ja izveidotais elektronisko rēķinu izrakstīšanas līdzeklis importē elektroniskos kreditoru rēķinus no pievienotajiem failiem, kas saņemti pa e-pastu, ir jākonfigurē e-pasta konta kanāls.

1. Regulatīvās konfigurācijas pakalpojumā (RCS) atlasiet izveidoto elektronisko rēķinu izrakstīšanas līdzekli. Noteikti atlasiet versiju, kuras statuss **ir Melnraksts**.
2. Cilnē **Uzstādījumi** atlasiet **Pievienot**.
3. Dialoglodziņa Līdzekļu iestatīšanas **izveide** nolaižamajā sarakstā **Jauns** lauku grupā atlasiet opciju **Pielāgota iestatīšana**.
4. **Lauku grupā Uzstādījumi tips** atlasiet opciju **Datu kanāls**.
5. Laukā **Atlasīt datu kanālu** ievadiet **Ienākošais e-pasts**.
6. Atlasiet **Izveidot**.
7. Atlasiet izveidoto rindu un pēc tam atlasiet **Rediģēt**.
8. Cilnes **Datu kanāls** **sadaļā Parametri** iestatiet šādus nepieciešamos laukus.

    | Lauks                | Apraksts |
    |----------------------|-------------|
    | Datu kanāls         | Ievadiet unikālu nosaukumu, lai identificētu datu kanālu. Nosaukumā var būt ne vairāk kā 10 rakstzīmes. Uz to attieksies piemērojamības noteikumos un saistītajās lietojumprogrammās saziņas procesā. |
    | Servera adrese       | Ievadiet e-pasta konta nodrošinātāja servera adresi. Piemēram, pakalpojumu sniedzēja servera adrese `https://outlook.live.com` ir imap-mail.outlook.com. |
    | Servera ports          | Ievadiet e-pasta konta nodrošinātāja izmantotā porta numuru. Piemēram, pakalpojumu sniedzēja servera ports `https://outlook.live.com` ir 993. |
    | Lietotājvārda noslēpums     | Ievadiet tā Atslēgas seifa noslēpuma Microsoft Azure nosaukumu, kurā ir e-pasta lietotāja konta ID. Šis noslēpums ir jāizveido Key Vault un jāiestata jūsu apkalpošanas vidē. |
    | Lietotāja paroles noslēpums | Ievadiet tā Atslēgas seifa noslēpuma nosaukumu, kurā ir e-pasta lietotāja konta parole. |
    | Noilgums              | Maksimālais termiņš milisekundēs (ms), ka sistēmai jāgaida atbilde. Noklusējuma vērtība ir 10 000 ms (10 sekundes). |
    | Galvenā mape          | Norādiet e-pasta importēšanas avotu vai mapi, no kuras pakalpojumam jāapstrādā e-pasta ziņojumi. |
    | Arhīva mape       | Norādiet mapi, kurā jāglabā apstrādātie e-pasta ziņojumi. Ja nenorādāt šo mapi, sistēma to automātiski izveidos. |
    | Kļūdu mape         | Norādiet mapi, uz kuru sistēmai jāpārvieto e-pasta ziņojumi, ja apstrāde neizdodas. Ja nenorādāt šo mapi, sistēma to automātiski izveidos. |
    | Maksimālais ziņojuma lielums     | Ievadiet viena apstrādātā ziņojuma maksimālo lielumu baitos. Noklusējuma vērtība tiek 20,000,000 baitiem. |
    | Maksimālais ziņojumu skaits   | Ievadiet maksimālo ziņojumu skaitu, kas jāapstrādā vienai darbībai. Ja nevēlaties ierobežot ziņojumu skaitu, iestatiet vērtību uz **0** (nulle). |
    | No filtra          | Ievadiet virkni, lai filtrētu pēc sūtītāja adreses. Tiks apstrādāti tikai tie e-pasta ziņojumi, kuros sūtītāja adrese atbilst filtram. Šis lauks nav obligāts. Lai norādītu vairākas sūtītāja adreses, izmantojiet semikolus (;) kā atdalītāji. |
    | Tēmu filtrs       | Ievadiet virkni, lai filtrētu pēc tēmas. Tiks apstrādāti tikai tie e-pasta ziņojumi, kuros tēma atbilst filtram. Šis lauks nav obligāts. Tiek atbalstīta vienkārša maska, piemēram **\*smth\*.ext**, kur katra zvaigznīte (\*) ir nulle vai vairāk jebkuras rakstzīmes gadījumu. |
    | Datuma filtrs          | Norādiet datumu, lai definētu apstrādāto ziņojumu maksimālo vecumu dienās. Šis lauks nav obligāts. Noklusējuma vērtība ir 30 dienas. |
    | Apstrādes režīms      | <p>Atlasiet vienu no šīm opcijām, lai norādītu, vai visus e-pasta ziņojuma pielikumus var apstrādāt kopā vai arī katrs pielikums ir jāapstrādā atsevišķi:</p><ul><li><b></b> Pielikumā – katram e-pasta pielikumam tiks izveidots jauns elektronisks dokuments. Piemēram, ja vienā e-pastā ir vairāki faili, kas satur e-rēķina datus, katrs fails sistēmā tiks uzskatīts par jaunu e-rēķinu.</li><li><b>Pa e-pastu</b> – viens pielikums tiks uzskatīts par pamata pielikumu, un sistēmā tiks izveidots viens elektroniskais rēķins. Citus pielikumus var izmantot kā atbalsta failus.</li></ul> |

9. **Filtru** sadaļā Pielikumi pievienojiet failu filtrēšanas informāciju. Tiks apstrādāti tikai tie pielikumi, kas atbilst definētajam filtram. Piemēram, **\*.xml** filtrēs pielikumus, kuriem ir .xml faila nosaukuma paplašinājums. Pielikuma nosaukums tiek izmantots Dynamics 365 Finance vai Dynamics 365 Supply Chain Management iestatīšanas laikā.

    - Ja iepriekšējā solī iestatījāt **lauku Apstrādes režīms** uz **Pa e-pastu**, šeit varat pievienot vairākus filtrus. Nosaukums identificēs konkrēto dokumentu.
    - Ja lauks Apstrādes režīms **ir iestatīts** uz **Pielikums** Pēc, varat pievienot tikai vienu filtru.

10. Cilnē Piemērojamības **kārtulas** pārskatiet un atjauniniet kritērijus pēc vajadzības. Lauka Kanāls **vērtībai** ir jābūt vienādai ar vērtību, ko ievadījāt **8. soļa laukā Datu kanāls**.
11. Atlasiet **Saglabāt** un aizveriet lapu.
